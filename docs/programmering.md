
# Programmering
---

## Et distribueret system
I forhold til at opnå læringsmålene for 3. semester har teamet valgt at fokusere på at lave et distribueret system.<br/>
Team 2 har gjort dette ved at ved at oprette flere projects i den samlet solution.
De fire projekter er som følger:

### Blazor
Under projektet blazor ligger alt frontend koden.

### Data
I projektet <b>data</b> er data-laget. Der ligger alt forbindelse til databasen.
<br/>
I mappen <b>entities</b>, indholder den alle de klasser, der bliver brugt til at lave migrations til databasen.
Herigennem er der også C# attributes, for eks. at fortælle databasen om der er tale om en Primary key eller ForeignKey
<br/>
```
[Key]
public int Id { get; set; }
...
[ForeignKey("Creator")]
public string CreatorId { get; set; }
```
Disse relationer får betydning, når tabeller bliver oprettet i databasen.

I mappen <b>DbContexts</b> finder vi context til databasen.
Vi ser først at ROContext arver fra IdentityDbContext:<br/>
`public class ROContext : IdentityDbContext<User>` 
<br/>
Det betyder at der er brugt ASP.NET Cores metode for at oprette og autorisere brugere.
<br/><br/>
Herefter ser vi nogle properties, hvor de forskellige tables bliver sat i databasen.<br/>
<i>De tabeller der bliver oprettet igennem Identity, er dog ikke vist her.</i>

```
public DbSet<Item> Items { get; set; }
public DbSet<Course> Courses { get; set; }
public DbSet<UserCourse> UserCourses { get; set; }
public DbSet<CourseItem> courseItems { get; set; }
```

Under metoden `protected override void OnModelCreating(ModelBuilder modelBuilder)`, bliver der oprettet alle de relationer, der i databasen imellem de forskellige tabeller. 
```
modelBuilder.Entity<UserCourse>()
    .HasOne(uc => uc.User)
    .WithMany(u => u.UserCourses)
    .HasForeignKey(utc => utc.UserId)
    .OnDelete(DeleteBehavior.Restrict);
```    
Her  oprettes der tabellen `UserCourse`. Tabellen har et one-to-many relationship.
Den tabel har en relation til én User med Mange UserCourses.
De er relateret hinanden igennem UserId.

Slutligt bliver der seedet data til databasen.
```             
modelBuilder.Entity<Item>()
.HasData(
new Item()
{
    Id = 1,
    Name = "Start",
    Description = "...",
},
....
```
<br/>


### API
I API projektet er der hvor størstedelen logikken er samlet, og hvor der bliver lavet diverse kald til databasen.

#### Arkitekturen

### Test

Her findes alle test, der er blevet skrevet igennem projektets [systemudviklingsmetoder](systemudvikling.md)

---

# Oprettelse af kursus

For at oprette et kursus i vores system, skal brugeren først registrere sig og logge ind. Dette er nødvendigt for at sikre, at kun autoriserede brugere kan oprette kurser.

## Registrering

For at registrere, skal brugeren udfylde en formular med følgende felter:

- Fornavn
- Efternavn
- Brugernavn
- Adgangskode

Når formularen er udfyldt, sendes dataen til vores backend via en HTTP POST-anmodning til `/api/Auth/Register` endpointet.

## Login

Efter registrering kan brugeren logge ind ved at indtaste deres brugernavn og adgangskode i login-formularen. Disse oplysninger sendes til vores backend via en HTTP POST-anmodning til `/api/Auth/Login` endpointet. Hvis login er succesfuldt, returnerer backenden en token, som gemmes i lokal lagring for senere brug.

## Oprettelse af kursus

Når brugeren er logget ind, kan de oprette et nyt kursus ved at klikke på "Opret bane" knappen. Dette udløser en HTTP POST-anmodning til `/api/course/create-course/{userId}` endpointet, hvor `{userId}` er brugerens unikke ID. Hvis oprettelsen er succesfuld, returnerer backenden detaljerne for det nyoprettede kursus.

## Ekstraktion af userId fra Token

Når en bruger logger ind, genererer vores backend en token, som indeholder brugerens unikke ID (`userId`). Dette `userId` er indlejret i token som en af dens claims.

Når vi skal oprette et nyt kursus, har vi brug for at kende `userId` for den aktuelt logget ind bruger. Dette `userId` er gemt i token, som vi har gemt i lokal lagring efter brugeren loggede ind.

For at få `userId` fra token, gør vi følgende:

1. Vi henter token fra lokal lagring.
2. Vi parser token ved hjælp af en `JwtSecurityTokenHandler`. Dette giver os et `JwtSecurityToken` objekt.
3. Vi finder "nameidentifier" claim i `JwtSecurityToken` objektet. Værdien af denne claim er `userId`, som vi har brug for.

Her er en kodebid, der viser, hvordan det gøres:

<figure markdown="span">
  ![Code snippet: UserId extraction](images/UserIdFraToken.png){ width="600" }
</figure>

Nu har vi `userId` for den aktuelt logget ind bruger, som vi kan bruge til at oprette et nyt kursus.


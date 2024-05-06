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

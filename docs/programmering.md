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

# Project Scope

### Projektets overordnede mål
* Udvikle en platform til NcH.
* Platformen skal optimere arbejdsprocesserne ved udarbejdelsen af baner til træning.
* Platformen skal give mulighed for at instruktører kan samarbejde om bane design og dele udfærdige baner med hinanden.
* Platformen skal give mulighed for at instruktører kan kommentere på baner der er delt med dem.
* Platformen skal fungere som primær kommunikationskanal og give instruktørerne mulighed for at kommunikere internt og med deres træningshold.

### Nøgleinteressenter
* **Nordfyns Civile Hundeførerforening (NcH)**: NcH er den primære bruger og modtager af platformen. De vil bruge platformen til at designe og dele træningsbaner, samt til at kommunikere internt og med deres træningshold. Deres feedback og behov vil være afgørende for platformens design og funktionalitet.

* **Instruktører**: Instruktørerne er de primære brugere af platformen. De vil bruge platformen til at designe træningsbaner, og samarbejde med andre instruktører. Deres brugeroplevelse og tilfredshed er afgørende for platformens succes.

### Projektmål for udviklingsteamet
* Implementer “RealTime” samarbejdsfunktioner, så instruktører kan arbejde simultant på samme bane.
* Udvikle en brugervenlig grænseflade, der tillader let design af baner med træk og slip funktionalitet.
* Integrere regel validering for banedesign, der automatisk kontrollerer overensstemmelse med gældende regler og standarder for de forskellige klasser ved konkurrencebaner.
* Opret en database til lagring af baner, så brugere kan gemme og genbruge deres designs
* Implementer brugeradgangskontrol, der giver ejerne af banen mulighed for at dele med udvalgte brugere.
* Udvikle en kommentar funktion, der muliggør feedback og diskussion mellem brugere på designet bane.
* Udvikle et besked-/notifikationssystem, der giver instruktører mulighed for at modtage og svare på vigtige meddelelser fra andre instruktører.
* Skab mulighed for oprettelse af grupper eller teams, så instruktører kan organisere sig og kommunikere med hinanden.

### Prioriteret Feature List
Her finde du den prioriteret [Feature list](featureDrivenDevelopment.md#feature-list)

### Tidsramme og Milepæle
Projektet igangsat d. 12. feb. 2024.  forventet slutdato er d. 15 maj. 2024.

* Milepæl 1 (efter 2 uger): Overordnet model designet
* Milepæl 2 (efter 3 uger): Overordnet model og CRUD funktionalitet implementeret
* Milepæl 3 (efter 5 uger): - bestemmes ud fra features fra feature list
* Milepæl 4 (efter 7 uger): - bestemmes ud fra features fra feature list
* Milepæl 5 (efter 9 uger): - bestemmes ud fra features fra feature list
* Milepæl 6 (efter 13 uger): Fejlrettelse og færdiggørelse.

### Teknologisk Stak
Platformen vil blive udviklet som en webapplikation ved brug af følgende teknologier:

* **Front-end**: Blazor vil blive brugt til at skabe en dynamisk og interaktiv brugergrænseflade.
* **Back-end**: ASP.NET med C# vil blive brugt i en objektorienteret, lagdelt arkitektur. Dette vil håndtere server-side logik og kommunikation med databasen.
* **Database**: SQL Server Management Studio (SSMS) vil blive brugt til robust og effektiv dataopbevaring.

Disse teknologier vil arbejde sammen for at danne et distribueret system, der sikrer en modulær og fremtidssikret løsning. Dette vil gøre det muligt at udvide med yderligere funktionalitet og let vedligeholde systemet.

* **Hosting**: Vi vil bruge Microsoft Azure til at hoste vores webapplikation. Azure tilbyder pålidelig og skalerbar cloud hosting med høj tilgængelighed.
* **Sikkerhed**: Vi vil implementere sikkerhedsforanstaltninger på flere niveauer. Dette inkluderer HTTPS for sikker dataoverførsel, brug af sikre password hashing algoritmer til opbevaring af brugerpasswords, og brug af JWT (JSON Web Tokens) til sikker brugerautorisering og -autentificering.
 
### Teststrategi og Kvalitetskontrol

For at sikre kvalitet og fejlfri ydeevne i vores projekt, vil vi anvende en kombination af forskellige testmetoder:

* **Unit Tests**: Vi vil bruge MSTest frameworket til at skrive unit tests for vores kode. Dette vil hjælpe os med at identificere og rette fejl på et tidligt tidspunkt i udviklingsprocessen. Vi vil stræbe efter at have en høj testdækning for at sikre, at alle dele af vores kode fungerer som forventet. 

* **Integration Tests**: Vi vil skrive integration tests for at teste, hvordan forskellige dele af vores system fungerer sammen. Dette vil hjælpe os med at identificere eventuelle problemer, der kan opstå, når forskellige dele af systemet interagerer.

* **Acceptance Tests**: Vi vil arbejde tæt sammen med vores Product Owner (PO) for at definere og udføre acceptance tests. Disse tests vil sikre, at systemet opfylder de forventede krav og fungerer som forventet i et realistisk miljø.

* **Code Reviews**: Vi vil regelmæssigt gennemføre code reviews for at sikre, at vores kode overholder de bedste praksis for kodning og design. Dette vil også give os mulighed for at lære af hinanden og forbedre vores kodningsevner.

* **Møder med Product Owner (PO)**: Vi vil have regelmæssige møder med vores PO (mindst en gang om måneden) for at diskutere projektets fremskridt, afklare eventuelle tvivlsspørgsmål og modtage feedback. Dette vil hjælpe os med at sikre, at vi er på rette vej og opfylder PO's forventninger.

Ved at følge denne teststrategi og fokusere på kvalitetskontrol, stræber vi efter at udvikle et højkvalitetsprodukt, der opfylder vores kunders behov og forventninger.

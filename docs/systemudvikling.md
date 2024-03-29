# Systemudvikling
Team 2 på 3. semester skal vælge og arbejde med mindst 2 systemudviklingsmetoder til deres eksamensprojekt. De vil reflektere over fordele og ulemper ved hver metode og tilpasse dem til projektet efter behov. Denne side vil give et overblik over de valgte metoder, samt dokumentere deres anvendelse i projektet `Rally Obedience`.

## Systemudviklingsmetoder

### FDD - Feature Driven Development
Team 2 har valgt `Feature Driven Development`, også kaldet `FDD`, som den første systemudviklingsmetode at arbejde ud fra.

FDD er en agil metode, der oftest anvendes af store teams. Afgørende for denne tilgang er oprettelsen af en liste over funktioner [Feature List](featureDrivenDevelopment.md#feature-list) for at identificere projektets krav og håndtere opgaver relateret til udviklingen af produktet.

Features, kan anskues som `Use Cases` i RUP `(Rational Unified Process)`, og som `User's stories` i Scrum. Disse udgør grundlaget for projektets krav og planlægning og udtrykkes som `handling-resultat-objekt`.

#### Best Practices in FDD
Der er 8 bedste praksis `(best pratices)` som bør benyttes når FDD anvendes som systemudviklingsmetode. 

*   __Domain object modeling:__
    * En overordnet domænemodel `(An overall model)` opbygges, der fungere som et rammeværk og fællesforståelses ramme for udvikling af features.
    * Se mere dokumentation af [Team 2's overall model her](featureDrivenDevelopment.md#An-overall-model).
*   __Developing by feature:__
    * Features-sæt bliver nedbrudt, indtil de når det mindste punkt, der er håndterbart nok til at levere resultater.
    Dette indbærer at opdele de overordnede systemkrav i mindre, mere håndterbare features, som derefter kan fungere som de grundlæggende opgaver `(Tasks)`, som systemet skal kunne udfører, og yderligere opdele dem i mindre dele, der kan udvikles individuelt.
    * Se mere dokumentation af [Team 2's Developing by feature her](featureDrivenDevelopment.md#Developing-by-feature)
*   __Component/Class Ownership:__
    * Ansvaret for en given feature der skal udvikles, tildeles én udvikler eller ét udviklingsteam, som bliver holdt til ansvar for kode-konsistensen, ydeevne og integritet til det overordnede projekts mål og krav overholders i forhold til processejeren.
    * Se mere dokumentation af [Team 2's Component/Class Ownership her](featureDrivenDevelopment.md#Component-class-ownership)
*   __Feature Teams:__
    * Dette er mindre udviklings grupper/teams, som dynamisk bliver formet, opløst og formet igen, alt efter hvilke features der skal udvikles.
    * Se mere dokumentation af [Team 2's Feature Teams her](featureDrivenDevelopment.md#Component-class-ownership)
*   __Inspections:__
    * Indarbejd regelmæssige inspektionsaktiviteter i udviklingsprocessen. Dette kan omfatte `peer reviews` og `systemgennemgang`. Det kan også omfatte `kvalitetssikringsaktiviteter` i udviklingsprocessen, da FDD er en `iterativ udviklingsmetode` som gør brug af af en `cyklisk procesmodel`.
    * Se mere dokumentation af [Team 2's Inspections her](featureDrivenDevelopment.md#inspections)
*   __Configuration Management:__
    * Ændringer i produktet/systemet dokumenteres og vedligeholdes til fremtidige referencer.
    * Det er formålet med denne website at fungere som dokumentation af hele `projekt Rally Obedience`.
*   __Regular Builds:__
    * For at sikre produktet er relevant og brugbart, udgives mindre dele af produktet reglmæssigt indtil hele projektet er færdigt.
    * Disse mindre udgivelser af produktet, anvendes til reviews med PO, hvor feedback og evt. ændringer defineres og tages i betragtning i den videre udviklingsproces.
*   __Visibility of progress and results:__
    * For at sikre at udviklingen af det færdige produkt er på rette spor, monitorerers progration i udviklingsprocessen og rapoteres.
    * Se mere dokumentation af [Team 2's Visibility of progress her](featureDrivenDevelopment.md#visibility-of-progress)

#### Stages in FDD
Overordnet arbejdes der i 5 faser/`(stages)` i FDD. Undervejs gennem de 5 stages anvendes de 8 best pratices. Selvom de 5 stages er listet herunder, er det vigtigt at forstå at stages bliver genbesøgt gennem den cykliske processmodel. For hvert genbesøg dokumenteres evt. ændringer og tilføjelser.

*   Stage 1 - Develop an overall model
    * Se mere dokumentation af [Team 2's overall model her](featureDrivenDevelopment.md#An-overall-model).
*   Stage 2 - Build a features list
    * Se mere dokumentation af [Team 2's Feature List her](featureDrivenDevelopment.md#feature-list)
*   Stage 3 - Plan by feature
    * Se mere dokumentation af [Team 2's Plan by feature her](featureDrivenDevelopment.md#plan-by-feature)
*   Stage 4 - Design by feature
    * Se mere dokumentation af [Team 2's Design by features](featureDrivenDevelopment.md#design-by-feature)
*   Stage 5 - Build by feature

---
## Tilpasning af FDD
Team 2 har udfærdiget artefaktorne `Business Case` og `Use Case Diagram` som supplerende værktøjer til teknikken `Develop an overall modell`. For nærmere beskrivelse af selve teknikken se [Team 2's overall model her](featureDrivenDevelopment.md#An-overall-model).

### Business Case {#BusinessCase-section}

### Use Case Diagram {#use-case-diagram}

---

## Refleksioner over FDD {#relections-on-fdd}
skriv løbende vores refleksioner ved brugen af FDD i dette afsnit. Husk både godt og mindre godt:

---








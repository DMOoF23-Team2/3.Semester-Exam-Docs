# Systemudvikling
---

Team 2 på 3. semester skal vælge og arbejde med mindst 2 systemudviklingsmetoder til deres eksamensprojekt. De vil reflektere over fordele og ulemper ved hver metode og tilpasse dem til projektet efter behov. Denne side vil give et overblik over de valgte metoder, samt dokumentere deres anvendelse i projektet `Rally Obedience`.

---

## Opstarts fasen
Inden den første systemudviklingsmetode vælges er der udfærdiget en foranalyse, som indeholder:

* Businesscase
* Krav til systemet
* Sprogbrug i domænet

Denne foranalyse er udfærdigt med baggrund i en præsentation af projektet som PO afholdte i starten af 3.semester og dermed i opstartsfasen af projektet.
Det betyder også at den første iteration af foranalysen tager udgangspunkt i 2.semester stof, da Team 2 på dette tidspunkt i projektet ikke var introduceret til nye begreber eller ikke har tilegnet sig mere viden siden 2.semester om begreberne:

* Procesmodeller
* Fokusområder
* Systemudviklingsmetoder
* Teknikker
* Værktøjer
* Usikkerhedder
* Kompleksitet

---

## Foranalyse - 1.iteration
### Krav til systemet
Overordnet kan systemet deles op i to sub-systemet. Et Bane system og et Chat system.
Følgende lister de identificerede krav til hvert af de to systemer.

#### Bane system
- Automatisk skiltenummer, pile og udfyldelse af skilteoversigt
- Mærker på baner, niveau, tema og antal skilte
- Lave baner, der overholder reglementet
- Lave baner, til træning, som ikke nødvendigvis overholder relementet
- Samarbejde om bane design i reltid
- Oprette interaktivt baner, trække og slippe skilte ind på banen
- Dele baner med andre instukrtører/dommer plus tildele dem rettigheder som ReadOnly eller Edit

#### Chat system
- oprette en trå mellem to instruktører
- oprette en gruppechat mellem flere instruktører
- evt. udvide de to ovenstående til at inkludere dommere

### Businesscase {#Businesscase}
#### Beskrivelse af problemområdet

**Forretningsmæssig baggrund** - Nordfyns Civile Hundeførerforening (NcH) er en del af organisationen Danmarks Civile hundeførerforening (DCH). 
DcH tilbyder undervisning i forskellige typer af hundesport, heriblandt Rally lydighed. 
NcH har en række frivillige instruktører som står for denne undervisning af ekvipage (hund og fører). En del af instruktørens rolle er at designe baner som ekvipage skal gennemføres i træning. 
På nuværende tidspunkt anvender instruktørerne et PowerPoint (PPT) til at designe disse baner og Facebook som kommunikationsplatform. 
Ved afholdelse af konkurrencer står en landsdækkende dommer for at designe banen. Det antages at dommerne anvender samme PPT som instruktørerne i denne proces.

**Forretningsmæssig problemstilling** - På nuværende tidspunkt, er der ikke ét dedikeret værktøj som rummer alle NcH og Dommeres behov.
Den nuværende praksis for planlægning, design og deling af træningsbaner står dog overfor flere væsentlige udfordringer. 
Disse inkluderer ineffektivitet i oprettelse og deling af baner, manglende evne til let at tilpasse baner til specifikke niveauer eller temaer, og vanskeligheder ved at sikre overensstemmelse med officielle regler. 
Den eksisterende løsning baseret på PowerPoint og Facebook tilbyder begrænset funktionalitet og understøtter ikke effektivt samarbejde mellem instruktører eller kommunikation med engagerede hundeførere.

#### Kravspecifikation
Idet at NcH skal bruge et værktøj, der skal kunne fungere som en platform, hvor flere intressenter skal kunne samarbejde omkring en bane, både samtidig, men også forskudt, er det blevet fastlagt, at en webbaseret løsningen ville passe bedst til NcHs krav.
I og med at de allerede bruger Facebook og Powerpoint, skal de heller ikke invistere i nyt udstyr, men de kan bruge de enheder, som de allerede har til rådighed.

#### Interessenter
#### Kerneinteressenter:
1. Nordfyns Civile Hundeførerforening (NcH)
2. Instruktører

#### Nære Primærer interessenter:
1. Danmarks Civile Hundeførerforening (DcH)
2. Dommere
3. Hundefører

#### Scenarie oversigt
#### 0-scenariet
NcH fortsætter med at bruge PowerPoint og Facebook til oprettelse af baner og kommunikarion

- **Fordele**: Der skal ikke investeres i et nyt system. Ingen tidskrævende overgangsfase eller introduktion til det nye system.
- **Ulemper**: Den nuværende ineffektive og tidskrævende proces ved banedesign fortsættes uændret.

#### 1-scenariet
**Formålet** - At tilbyde en platform for NcH, der giver deres instruktører mulighed for at samarbejde om design af baner, mulighed for at dele, gemme og genbruge oprettede baner. 
Derudover skal instruktørerne have mulighed for at kommunikere med hinanden gennem platformen. Både i form af chat funktionalitet, så de instruktørerende kan vidensdele og andet, og så de kan kommunikere omkring bane design.

**Forretningsmæssig løsningsbeskrivelse** - Løsningen skal dels sikre, at design og deling af rally lydighed baner foregår mere effektivt og struktureret, og dels muliggøre realtidssamarbejde og feedback mellem instruktører.

Den nuværende praksis med manuelt at tegne baner i PowerPoint og dele dem i en Facebook-gruppe, hvor feedback gives i kommentarfeltet, erstattes af en integreret webbaseret platform. Denne platform vil gøre det muligt for instruktører at designe baner, validere dem automatisk mod reglementet, dele dem med specifikke personer eller grupper, og modtage og give feedback direkte i systemet.

I første omgang er løsningen tiltænkt rally lydighed instruktører, men med potentiale for senere at udvide til dommer. 
Det vurderes, at løsningen umiddelbart kan forbedre kvaliteten og effektiviteten af træning betydeligt og fremme et tættere samarbejde og vidensdeling mellem instruktører og evt. dommere.

**it-mæssig løsningsbeskrivelse** - Rally Lydighed udvikles som en webapplikation ved brug af Blazor for front-end, for at visualisere data og funktionaliteter på en dynamisk og interaktiv måde. 

Back-end delen bygges i ASP.NET med C# i en objektorienteret, lagdelt arkitektur, som kommunikerer med databasen og sender respons til front-end. 

Databasen håndteres via SQL Server Management Studio (SSMS) for robust og effektiv dataopbevaring. 

Disse komponenter arbejder sammen for at danne et distribueret system, som tilsammen sikrer en modulær og fremtidssikret løsning, hvor det er muligt at udvide med yderligere funktionalitet og let at vedligeholde systemet.

**Forretningsmæssige effekter** - **Økonomiske effekter** - Bedre vilkår og mere effektivt at være intruktør, hvilket kan gøre det mere attraktivt at være instruktør.
hvis Nch opnår flere instruktører kan der oprettes flere træningshold og med flere træningshold vil der opstå en øget indtægt.

**Gevinster** - En webapplikation vil give NcH en mere effektiv metode at designe baner.
Gennem bedre kommunikation og samarbejde, vil disse baner blive forbedret i forhold til fællesskabets feedback.
Det vil give instruktørerne en større glæde og lyst til at oprette baner og dele dem med hinanden. Samtidig er der et katalog over alle banerne, der alt sammen vil være med til at øge fællesskabet og kvaliteten af baner og træning.

**Implementering og opfølgning** - Platformen skal implementeres gennem oplæring og opfølgning ved at gå igennem følgende:

- **Platformen og dokumentation overdrages til Product Owner (PO)** - PO får en detaljeret gennemgang af opsætning og brug af platformen. Der skal aftales faste tidspunkter til gennemgang og feedback.
- **Test og validering** - NcH medlemmer får i første omgang, som de eneste adgang til systemet. Dette skal ses som en demo. I en given periode får de lov at anvende og teste platformen. De afgiver feedback til PO.
- **Feedback og tilpasning** - Den feedback NcH har videregivet PO gennemgås mellem udviklingsteamet og PO. Platformen tilpasses i forhold til feedbacken, så ønsker bliver implementeret og fejl tilrettes.

Dette skal ses som en cyklisk proces, der fortsætter indtil NcH oplever det produkt som de efterspørger. Herefter kan platformen udgives som en færdig version, hvor DcHs dommer får adgang.

**KPI'er**

- Antal aktive brugere på platformen.
- Gennemsnitlig tid brugt på at designe en bane.
- Brugertilfredshedsmålinger
- Overholdelse af regler i banedesign
- Antallet af oprettede baner (x% forøgelse,i forhold til hvad der er nu)
- Aktivitet på oprettede baner (Kommentarer, delinger)
- En tilfredshedscore på 8/10, laver på baggrund af brugerundersøgelser

#### Sprogbrug i domænet
- **Klasse**: Sværhedsgrad / niveau for en bane
- **Øvelse/Momenter**: Det som hunden skal udføre. Det kan være et spring, stå, højre handlet etc.
- **Ekvipage**: Hund og hundefører
- **Skilt**: Det skilt på banen, hvor der står angivet hvad ekvipage skal udføre
- **Rally lydighed**: Hundesport
- **Reglementet**: De officelle regler/retningslinjer fra Landsforeningen Danmarks Civilie Hundeførerforering, anvendes i forbindelse med konkurrence baner.
- **Instruktør**: frivillige underviser i de lokale foreninger.

---

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

### Use Case Diagram {#use-case-diagram}

---

## Refleksioner over FDD {#relections-on-fdd}
skriv løbende vores refleksioner ved brugen af FDD i dette afsnit. Husk både godt og mindre godt:

---








# Feature Driven Development

## An overall model {#An-overall-model}
Her defineres det overodnede `scope` for `Rally Obedience` projektet. Dette er både en del a best pratices og Stage 1 når FDD anvendes som systemudviklingsmetode.

En systemudviklingsmetode består af en række sammenhængende teknikker, der hver især udføres ved hjælp af et eller flere værktøjer. En teknik er en generisk beskrivelse af aktiviteter, samt målet med denne aktivitet. Et værktøj er en specifik angivelse af hvad man vil benytte for at udfører aktiviteten i teknikken. For at sikre sammenhængen mellem teknikkerne i metoden, bliver `outputtet` fra den ene teknik anvendt som `input` til den næste teknik.

An overall model - som teknik:

*   Formål: 
    * At skabe en fællesforståelse ramme for udviklingsteamet.
    * At skabe en overordnet domæne model.
    * At identificere systemkrav til at skabe en `Feature List`.
    * At identificere interessenter/`stackholders`.
*   Værktøjer:
    * Use Cases - `UC`
    * Use Case Diagram - `UCD`
    * Objektmodel - `OM`
    * Domænemodel - `DM`
    * Business Case - `BC`
    * Project Scope Description - `PSD`
*   Output:
    * Opnå viden om emner listet under formål
    * At kunne skabe en [Feature List](featureDrivenDevelopment.md#feature-list) når overall model er færdig.

### Use Cases
**Bane-system**

<figure markdown="span">
  ![Use Case: Oprettelse af træningsbane](images/UseCaseOprettelseAfTræningsbane.png){ width="600" }
</figure>
<figure markdown="span">
  ![Use Case: Oprettelse af bane ifølge DCH reglement](images/UseCaseOprettelseBaneReglement.png){ width="600" }
</figure>
<figure markdown="span">
  ![Use Case: Deling af bane med anden instruktør ](images/UseCaseDelingBaneInstruktør.png){ width="600" }
</figure>
<figure markdown="span">
  ![Use Case: Tilgå og kommentere en delt bane ](images/UseCaseTilgåKommenterBane.png){ width="600" }
</figure>
<figure markdown="span">
  ![Use Case: Live samarbejde ved oprettelse af bane ](images/UseCaseLiveSamarbejdeBane.png){ width="600" }
</figure>

**Chat-system**
<figure markdown="span">
  ![Use Case: Chat mellem to instruktører ](images/UseCaseChatToInstruktører.png){ width="600" }
</figure>
<figure markdown="span">
  ![Use Case: Opret gruppechat for instruktører ](images/UseCaseOpretGruppeChatInstruktører.png){ width="600" }
</figure>
<figure markdown="span">
  ![Use Case: Kommunikation i gruppechat ](images/UseCaseKommunikationGruppeChat.png){ width="600" }
</figure>

---

## Feature list {#feature-list}
*Note: beskrive vores indledende arbejde med businesscase, use cases, usecase-diagram og møde med PO i processen om at identificere og udfærdige Feature-listen.*

Igennem problemstillingen ved [BusinessCase](systemudvikling.md#Businesscase) er der blevet fundet frem til en række features, der kan opfylde NcHs behov.
Feature listen er blevet prioriteret PO.
Listen i prioriteret rækkefølge:

| Opret trænings bane | klik på opret bane --> klik på til træning --> |
| ----------- | ----------- |
| Feature | Viser en tom template. |
| Feature | Vise alle skilte og elementer (kegler, pile med betydning som gå i ring mm.). |
| Feature | Trække og slippe skilte og andre elementer ind i som udgør bane designet. |
| Feature | Systemet generer automatisk skilte numre "på banen". |
| Feature | Systemet genere automatisk en tabel med skilterækkefølgen og deres ID |
| Feature | Systemet generer automatisk pile som viser vejen gennem banen. |

| Opret bane til reglement | klik på opret bane --> klik på efter reglement--> Vælg klasse banen skal være til --> |
| ----------- | ----------- |
| Feature | Viser en tom template. |
| Feature | Vise alle skilte og elementer (kegler, pile med betydning som gå i ring mm.) til den valgte klasse. |
| Feature | Systemet validere antal skilte, rækkefølgen af skilte ift. reglement |
| Feature | Systemet generer automatisk skilte numre "på banen". |
| Feature | Systemet genere automatisk en tabel med skilterækkefølgen og deres ID |
| Feature | Systemet generer automatisk pile som viser vejen gennem banen. |

| Deling af træningsbane med anden instruktør | klik på del bane --> |
| ----------- | ----------- |
| Feature | Viser en liste med alle instruktører |
| Feature | Del knap - systemet håndtere/opretter associationer |
| Feature | En notifikationer om en bane er blevet del med dig |

| Tilgå og kommentere en delt bane | klik på baner --> Delte baner |
| ----------- | ----------- |
| Feature | Viser en liste med alle baner der er delt med useren (instruktøren). |
| Feature | en valgte bane vises. |
| Feature | En notifikationer om en bane er blevet del med dig |
| Feature | Tilføje en kommentar til banen. |
| Feature | Vise kommentar historikken i et kommentarspor. |	

| Live samarbejde ved oprettelse af træningsbane | Klik på opret bane --> klik på til træning --> |
| ----------- | ----------- |
| Feature | Viser en tom template. |
| Feature | Viser alle skilte og elementer (kegler, pile med betydning som gå i ring mm.). |
| Feature | Viser en "Live share" knap. |
| Feature | Systemet skal kunne håndtere RealTime samarbejde mellem to users (muligvis gennem et link der bliver delt) |

| Chat mellem to instruktører | Klik på Instruktører --> Vælg instruktør --> Klik start chat |
| ----------- | ----------- |
| Feature | Liste over instruktør |
| Feature | Vælg start chat med en instruktør |
| Feature | Vis tom chat vindue |
| Feature | Skriv besked |
| Feature | Send besked |
| Feature | Chat historik bliver gemt |
| Feature | Slet en besked - systemet skal kunne fjerne en besked fra visningen (måske skal den gemmes i en log - sikkerhed). |
| Feature | Rediger en besked - systemet skal kunne håndtere at en user ønsker at redigere i sin egen allerede postede besked. |

| Chat mellem to instruktører | Klik på Instruktører --> Vælg instruktør --> Klik start chat |
| ----------- | ----------- |
| Feature | Liste over instruktører |
| Feature | Vælg start chat med en instruktør |
| Feature | Vis tom chat vindue |
| Feature | Skriv besked |
| Feature | Send besked |
| Feature | Chat historik bliver gemt |
| Feature | Slet en besked - systemet skal kunne fjerne en besked fra visningen (måske skal den gemmes i en log - sikkerhed) |
| Feature | Rediger en besked - systemet skal kunne håndtere at en bruger ønsker at redigere i sin egen allerede postede besked |

| Opret gruppechat for instruktører | |
| ----------- | ----------- |
| Feature | Viser en liste med alle instruktører |
| Feature | Systemet tilknytter en bruger til den oprettede gruppe |
| Feature | Tilføj bruger efter gruppechatten er oprettet |
| Feature | Forlad gruppen |
| Feature | Slet gruppechat |
| Feature | Visning over alle medlemmer af gruppechatten |
| Feature | Visning over alle "mine" grupper |
| Feature | Viser et tekstfelt til oprettelse af besked |
| Feature | Send/post besked - systemet gemmer beskeden, så den er synlig for de andre medlemmer af gruppen |
| Feature | Systemet viser beskedhistorikken, så der er styr på hvem der skrev hvad hvornår i visningen af alle beskeder |
| Feature | Slet en besked - systemet skal kunne fjerne en besked fra visningen (måske skal den gemmes i en log - sikkerhed) |
| Feature | Rediger en besked - systemet skal kunne håndtere at en bruger ønsker at redigere i sin egen allerede postede besked |

| Kommunikation i gruppechat | |
| ----------- | ----------- |
| Feature | Der skal være et tekstfelt, hvor der kan skrives en besked |
| Feature | Der skal være en 'send knap' som sender teksten i tekstfeltet til modtagerne |
| Feature | Der skal være en feedback der viser at modtagerne har modtaget beskeden, og når modtagerne har læst beskeden |
| Feature | Der skal være mulighed for at redigere eller slette en tidligere besked eller tekst |
| Feature | Der skal være mulighed for at svare direkte på en besked i chatten |
| Feature | Der skal være en visning af hvem der er afsender på de enkelte beskeder |
| Feature | Der skal være 'time stamps' på alle de beskeder der bliver sendt |


## Developing by features {#Developing-by-feature}
Indsæt dokumentation om hvordan vi har planlagt og anvender developing by features, samt hvordan vi nedbryder features til de mindste og mest håndterbare tasks/features.

## Component/Class ownership {#Component-class-ownership}
Beskriver hvordan vi har tildelt ansvaret for bestemte features til mindre teams. Nævn gerne brugen af `github Kanban eller nogle af de andre` og vores Assignet TO: ... Husk at beskriv hvordan vi anvender `Feature Teams`, lige som har delt os op i grupperne, hvor BC og KFM har feature alle skilte og JJ og KKN har vis en tom bane.

## Inspctions and quality assurance {#inspections}
Beskriv vores Kvalitetssikrings protokoller og aktiviteter. Beskriv hvordan vi til vores gruppemøder har afholdt peer-reviewa mellem de to mindre feature-teams.

## Visibility of progress {#visibility-of-progress}
beskriv brugen af milepæle `(milestones i github)`. Indsær gerne billeder af milepæle.
lave et roademap sorteret på milepæle og indsæt billede også.

## Plan by feature {#plan-by-feature}
Beskrive brugen af scrum og beskriv hvordan vi anvender diverse relevante github projektstyringsværktøjer. Husk at referere til at feature listen diktere hvilket features der arbejdes på.

## Design by feature {#design-by-feature}
Beskriv hvordan vores design proces af hver feature forgår i overordnede træk.
Lav en under oversskrift med den feature du arbejder på, og dokumenter den her. Husk at indsætte billeder eller lign. af evt. artefakter der er anvendt.
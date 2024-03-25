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

<figure markdown="span">
  ![Use Case: Oprettelse af træningsbane](images/UseCaseOprettelseAfTræningsbane.png){ width="600" }
</figure>

## Feature list {#feature-list}
beskrive vores indledende arbejde med businesscase, use cases, usecase-diagram og møde med PO i processen om at identificere og udfærdige Feature-listen.

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
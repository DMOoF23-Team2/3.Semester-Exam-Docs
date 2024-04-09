# Project Scope

### Projektets overordnede m�l
* Udvikle en platform til NcH.
* Platformen skal optimere arbejdsprocesserne ved udarbejdelsen af baner til tr�ning.
* Platformen skal give mulighed for at instrukt�rer kan samarbejde om bane design og dele udf�rdige baner med hinanden.
* Platformen skal give mulighed for at instrukt�rer kan kommentere p� baner der er delt med dem.
* Platformen skal fungere som prim�r kommunikationskanal og give instrukt�rerne mulighed for at kommunikere internt og med deres tr�ningshold.

### N�gleinteressenter
* **Nordfyns Civile Hundef�rerforening (NcH)**: NcH er den prim�re bruger og modtager af platformen. De vil bruge platformen til at designe og dele tr�ningsbaner, samt til at kommunikere internt og med deres tr�ningshold. Deres feedback og behov vil v�re afg�rende for platformens design og funktionalitet.

* **Instrukt�rer**: Instrukt�rerne er de prim�re brugere af platformen. De vil bruge platformen til at designe tr�ningsbaner, og samarbejde med andre instrukt�rer. Deres brugeroplevelse og tilfredshed er afg�rende for platformens succes.

### Projektm�l for udviklingsteamet
* Implementer �RealTime� samarbejdsfunktioner, s� instrukt�rer kan arbejde simultant p� samme bane.
* Udvikle en brugervenlig gr�nseflade, der tillader let design af baner med tr�k og slip funktionalitet.
* Integrere regel validering for banedesign, der automatisk kontrollerer overensstemmelse med g�ldende regler og standarder for de forskellige klasser ved konkurrencebaner.
* Opret en database til lagring af baner, s� brugere kan gemme og genbruge deres designs
* Implementer brugeradgangskontrol, der giver ejerne af banen mulighed for at dele med udvalgte brugere.
* Udvikle en kommentar funktion, der muligg�r feedback og diskussion mellem brugere p� designet bane.
* Udvikle et besked-/notifikationssystem, der giver instrukt�rer mulighed for at modtage og svare p� vigtige meddelelser fra andre instrukt�rer.
* Skab mulighed for oprettelse af grupper eller teams, s� instrukt�rer kan organisere sig og kommunikere med deres tr�ningshold. //!!

### Prioriteret Feature List
* Opret tr�ningsbane
  * Viser en tom template.
  * Vise alle skilte og elementer (kegler, pile med betydning som "g� i ring" mm.).
  * Tr�kke og slippe skilte og andre elementer ind som udg�r bane designet.
  * Systemet generer automatisk skilte numre "p� banen".
  * Systemet genere automatisk en tabel med skilter�kkef�lgen og deres ID.
  * Systemet generer automatisk pile som viser vejen gennem banen.

* Deling af tr�ningsbane med anden instrukt�r
  * Viser en liste med alle instrukt�rer.
  * Del knap - systemet h�ndtere/opretter associationer.
  * En notifikation om en bane er blevet del med dig bliver sendt.

* Opret bane til reglement
  * Viser en tom template.
  * Vise alle skilte og elementer (kegler, pile med betydning som "g� i ring" mm.) til den valgte klasse.
  * Tr�kke og slippe skilte og andre elementer ind som udg�r bane designet.
  * Systemet validerer antal skilte og r�kkef�lgen af skilte ift. reglement.
  * Systemet generer automatisk skilte numre "p� banen".
  * Systemet genere automatisk en tabel med skilter�kkef�lgen og deres ID.
  * Systemet generer automatisk pile som viser vejen gennem banen.

* Live samarbejde ved oprettelse af tr�ningsbane
  * Viser en tom template.
  * Viser alle skilte og elementer (kegler, pile med betydning som "g� i ring" mm.).
  * Viser en "Live share" knap.
  * Systemet skal kunne h�ndtere RealTime samarbejde mellem to brugere (muligvis gennem et link der bliver delt).

* Tilg� og kommentere en delt bane
  * Viser en liste med alle baner der er delt med brugeren (instrukt�ren).
  * Den valgte bane vises.
  * Tilf�je en kommentar til banen.
  * Vise kommentar historikken i et kommentarspor.

* Chat mellem to instrukt�rer
  * Liste over instrukt�rer.
  * V�lg start chat med en instrukt�r.
  * Vis tom chat vindue.
  * Skriv besked.
  * Send besked.
  * Chat historik bliver gemt.
  * Slet en besked - systemet skal kunne fjerne en besked fra visningen (m�ske skal den gemmes i en log - sikkerhed).
  * Rediger en besked - systemet skal kunne h�ndtere at en user �nsker at redigere i sin egen allerede postede besked.
	
//Droppede vi gruppechat?

* Opret gruppechat for instrukt�rer
  * Viser en liste med alle instrukt�rer.
  * Systemet tilknytter en user til den oprettede gruppe.
  * Tilf�j user efter gruppechatten er oprette.
  * Forlad gruppen.
  * Slet gruppe chat.
  * Visning over alle medlemmer af gruppechatten.
  * Visning over alle "mine" grupper.
  * Viser et tekst felt til oprettelse af "besked".
  * Send/post besked - systemet gemmer beskeden, s� den er synlig for de andre medlemmer af gruppen.
  * Systemet viser besked historikken, s� der er styr p� hvem der skrev hvad hvorn�r i visningen af alle beskeder.
  * Slet en besked - systemet skal kunne fjerne en besked fra visningen (m�ske skal den gemmes i en log - sikkerhed).
  * Rediger en besked - systemet skal kunne h�ndtere at en user �nsker at redigere i sin egen allerede postede besked.

* Kommunikation i gruppechat
  * Der skal v�re et tekstfelt, hvor der kan skrives en besked.
  * Der skal v�re en 'send knap' som sender teksten i tekstfeltet til modtagerne.
  * Der skal v�re en feedback der viser at modtagene har modtaget beskeden, og n�r modtagerne har l�st beskeden.
  * Der skal v�re mulighed for at redigere eller slette en en tidligere besked eller tekst.
  * Der skal v�re mulighed for at svare direkte p� en besked i chatten.
  * Der skal v�re en visning af hvem der er afsender p� de enkelte beskeder. 
  * Der skal v�re 'time stamps' p� alle de besker der bliver sendt.

### Tidsramme og Milep�le
Projektet igangsat d. 12. feb. 2024.  forventet slutdato er d. 15 maj. 2024.
* Milep�l 1 (efter 2 uger): Overordnet model designet
* Milep�l 2 (efter 3 uger): Overordnet model og CRUD funktionalitet implementeret
* Milep�l 3 (efter 5 uger): - bestemmes ud fra features fra feature list
* Milep�l 4 (efter 7 uger): - bestemmes ud fra features fra feature list
* Milep�l 5 (efter 9 uger): - bestemmes ud fra features fra feature list
* Milep�l 6 (efter 13 uger): Fejlrettelse og f�rdigg�relse.

### Teknologisk Stak
Platformen vil blive udviklet som en webapplikation ved brug af f�lgende teknologier:

* **Front-end**: Blazor vil blive brugt til at skabe en dynamisk og interaktiv brugergr�nseflade.
* **Back-end**: ASP.NET med C# vil blive brugt i en objektorienteret, lagdelt arkitektur. Dette vil h�ndtere server-side logik og kommunikation med databasen.
* **Database**: SQL Server Management Studio (SSMS) vil blive brugt til robust og effektiv dataopbevaring.

Disse teknologier vil arbejde sammen for at danne et distribueret system, der sikrer en modul�r og fremtidssikret l�sning. Dette vil g�re det muligt at udvide med yderligere funktionalitet og let vedligeholde systemet.

// Bud p� hosting og sikkerhed
* **Hosting**: Vi vil bruge Microsoft Azure til at hoste vores webapplikation. Azure tilbyder p�lidelig og skalerbar cloud hosting med h�j tilg�ngelighed.
* **Sikkerhed**: Vi vil implementere sikkerhedsforanstaltninger p� flere niveauer. Dette inkluderer HTTPS for sikker dataoverf�rsel, brug af sikre password hashing algoritmer til opbevaring af brugerpasswords, og brug af JWT (JSON Web Tokens) til sikker brugerautorisering og -autentificering.
 
### Teststrategi og Kvalitetskontrol

For at sikre kvalitet og fejlfri ydeevne i vores projekt, vil vi anvende en kombination af forskellige testmetoder:

* **Unit Tests**: Vi vil bruge MSTest frameworket til at skrive unit tests for vores kode. Dette vil hj�lpe os med at identificere og rette fejl p� et tidligt tidspunkt i udviklingsprocessen. Vi vil str�be efter at have en h�j testd�kning for at sikre, at alle dele af vores kode fungerer som forventet. //Eller m�ske ikke, men lader det st� om fluff for nu :)

* **Integration Tests**: Vi vil skrive integration tests for at teste, hvordan forskellige dele af vores system fungerer sammen. Dette vil hj�lpe os med at identificere eventuelle problemer, der kan opst�, n�r forskellige dele af systemet interagerer.

* **Acceptance Tests**: Vi vil arbejde t�t sammen med vores Product Owner (PO) for at definere og udf�re acceptance tests. Disse tests vil sikre, at systemet opfylder de forventede krav og fungerer som forventet i et realistisk milj�. // I en perfekt verden

* **Code Reviews**: Vi vil regelm�ssigt gennemf�re code reviews for at sikre, at vores kode overholder de bedste praksis for kodning og design. Dette vil ogs� give os mulighed for at l�re af hinanden og forbedre vores kodningsevner.

* **M�der med Product Owner (PO)**: Vi vil have regelm�ssige m�der med vores PO (mindst en gang om m�neden) for at diskutere projektets fremskridt, afklare eventuelle tvivlssp�rgsm�l og modtage feedback. Dette vil hj�lpe os med at sikre, at vi er p� rette vej og opfylder PO's forventninger.

Ved at f�lge denne teststrategi og fokusere p� kvalitetskontrol, str�ber vi efter at udvikle et h�jkvalitetsprodukt, der opfylder vores kunders behov og forventninger.

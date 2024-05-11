# Extream Programming

## Foranalyse / analyse af projektets situation
Som en del af den løbende analyse af projektets situation, er følgende `Usikkerheder` og `Kompleksiteter` identificeret på nuværende tidspunkt i projektet.

- Projektet skal kunne håndtere flere brugere på en gang, tiltænkt teknologi til at løse dette i forbindelse med `live-shar af bane` er `SingalR`. Da udviklings teamet aldrig har arbejdet med singnalR før, er deres viden omkring implementering af dette ikke eksisterende og skal tilegnes undervejs.
- Projektet sjal have et login-system / funktionalitet, dette er på nuværende tidspunkt implementeret, således, at `data-laget` anvender `AspNetCore.Identity` og `AspNetCore.Identity.EntityFramworkCore`. Igen er udviklingsteamets viden begrænset da de ikke har arbejdet med login før. Derfor skal viden omkring implementeringen af dette tilegnes undervejs.
- projektets `front-end` del udvikles i `Blazor`. Igen er der første gang udviklingsteamet arbejder med Blazor og dermed endnu en ny teknologi, hvor viden skal tilegnes undervejs.
- projektet skal være et `distribueret-system`, da dette projekt er første gang udviklings teamets arbejder med distribueret systemer, skal viden om arkitekturen og ansvarsfordeling for de kommende sub systemer tilegnes undervejs.

### Usikkerheder
* Teknologier
    * SignalR
        * Hvad er signalR? - WebSocket
        * Hvordan implementeres signalR?
        * I hvilken kontekst anvendes signalR? - real-time web funktionaliteter
    * Identity on ASP.NET Core
        * Hvad er Identity? - Anvendes til login funktionaliteter
        * Hvor i den distribuerede arkitektur skal Identity implementeres? (Blazor, API eller Data - solution? er det et samspil imellem lagene).
    * JSON web Tokens - JWT
        * Hvordan sikres API'et bedst? - ved en token pr. user? eller andet ?
        * Hvordan kan JWT og Identity hænge sammen
    * Blazor
        * Hvad er Blazor?
        * Hosting og kommunikation med API ?

### Uklare Krav
* Hvilket `roller` skal have adgang til hvilket funktionaliteter?
* Skal der være en Admin rolle og hvad skal denne anvendes til`
    * Tilføje nye useres?
    * Tildele roller til eksisterende users?
    * Gendannelse af baner hvis de bliver slettet ved et uheld?

### Kompleksiteter
* Flere brugere
    * Forskellige roller
    * Forskellig brug og formål med systemet
    * mange scenarier der berør klasserne `Course` og `User`
* Integrationer/hosting
    * Kommunikation mellem
        * Data-solution - Skolens VPN og server
        * API - Azure (brugen af JWT)
        * Blazor - ??

### Samlet vurdering af Usikkerheder og Kompleksiteter
Projektet befinder sig i en situation hvor der er `høj-usikkerhed` og `mellem til høj - kompleksitet`.




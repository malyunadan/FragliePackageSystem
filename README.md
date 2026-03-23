# FragliePackageSystem 
FragilePackageSystemer et samlet software‑projekt, der håndterer registrering, overvågning og visualisering af skrøbelige pakker. Systemet består af flere moduler, der arbejder sammen: en backend‑bibliotekskerne, et REST API, et SenseHat‑baseret IoT‑modul og en web‑frontend. Projektet demonstrerer, hvordan hardware, backend‑logik og brugergrænseflade kan integreres i én samlet løsning.

Backend – PackageLibrary
- link: https://github.com/malyunadan/PackageLibrary
- Et C#‑bibliotek der indeholder:
- Datamodeller for pakker
- Validering
- Forretningslogik
- Håndtering af skrøbelighed, status og metadata
Dette modual fungerer som den centrale logik i systemet og bruges af rest API'et.


REST API - FragilePackageAPI-_
- link: https://github.com/malyunadan/FragilePackageAPI-_
- Et REST‑API bygget i C#/.NET, der gør det muligt at:
- Oprette, hente og opdatere pakker
- Kommunikere med frontend og IoT‑modulet
- Eksponere data i JSON‑format
- Sikre struktureret og skalerbar kommunikation
API'et bruger PackageLibrary til al logik og databehandlig.



Hardware - SenseHat UDP
link: https://github.com/malyunadan/sensehat-UDP
- Et Python‑script der:
- Kommunikerer med SenseHat via UDP
- Sender målinger eller status til API’et
- Visualiserer pakke‑tilstande på SenseHat LED‑matrix
- Demonstrerer hardware‑integration i et større system
Dette modul gør systemet i stand til at reagere på fysiske hændelser.


Frontend - Web Interface
- link: https://github.com/malyunadan/Frontend-s
- En web‑frontend der:
- Viser pakker og deres status
- Kommunikerer med API’et
- Giver brugeren et visuelt overblik
- Kan udvides med dashboards, grafer og real‑time data
Frontend er det lag, slutbrugeren interagerer med.

Systemet fungerer som en kæde:
SenseHat(IoT) → REST API → PackageLibrary → REST API → Frontend.
- IoT‑modulet sender data til API’et
- API’et bruger backend‑biblioteket til at behandle data
- Frontend henter data fra API’et og viser det til brugeren
Det giver en komplet løsning fra hardware til brugergrænseflade.

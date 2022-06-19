# QGIS-DMP-Plugin-installation

QGIS DMP Manager er et plugin, som giver brugeren mulighed for at downloade valgfri datalag fra DAI, Miljøportalen. 

Data placeres i en lokal database baseret datakilde i form en tabel. Modtager databasen kan være af typen PostgreSQL, Oracle Spatial, MS-SQLServer, GeoPackage eller SpatiaLite.  

Download funktionen medfører, at der oprettes to tabeller for hvert data-lag, som hentes fra DAI: Et ”redigeringslag”, som brugeren kan rette i, dvs. oprette nye samt modificere eller slette eksisterende poster. Samtidigt oprettes en ”referencelag” i samme database hvor referencelaget struktur- og datamæssigt er fuldkommen ens med redigeringslaget (før brugeren begynder at rette data) - blot under et andet tabelnavn .
Redigeringslaget er et helt almindeligt data-lag i QGIS og du kan derfor benytte alle QGIS’s avancerede redigeringsfunktioner på dette lag. (Du må ikke rette i referencelaget, da man fjerner muligheden for plugin’et senere kan sammenligne dataindhold i redigeringslag og referencelag.)

Man kan downloade flere typer af data-lag fra DAI, således at disse lag findes samtidigt som redigerings/referencelag i QGIS. Dette giver mulighed for at tilrette data på tværs af forskellige data-lag fra DAI. 

Når tilretning er færdiggjort i redigeringslaget kan brugeren sammenligne data mellem redigeringslag og referencelag vha. en funktion i plugin-et. Funktionen finder alle forskelle mellem redigerings- og referencelag (oprettelser, rettelser og sletninger) og viser disse som lag - hhv. ”Oprettet”, ”Rettet” eller ”Slettet” i QGIS kortvinduet. Brugeren kan herefter kontrollere de enkelte modificerede elementer og efter kontrol ”skubbe” (uploade) modifikationerne tilbage til DAI.

Plugin-et har mulighed for at gemme en tematisering (symbolisering) for hver DAI lagtype, således at samme tematisering vil blive benytte ved senere downloads af data-lag fra DAI. 

Plugin-et har slutteligt en række administrative funktioner, f.eks. at kunne opstarte QGIS geometri-tjekker på det valgte lag.

Plugin-et kan benyttes til både demo-miljøet og produktionsmiljøet hos DAI, Miljøportalen.  

## Vejledninger

Download af alle filer i repository som én zip-fil udføres ved at trykke på den grønne knap i hovedskærmbilledet for repository og vælge "Download ZIP" i undermenuen.

Der findes to vejledninger til plugin: "Installationvejledning.docx", som beskriver hvorledes systemet skal installeres. Og "Brugervejledning.docx", som beskriver den daglige brug af systemet.


## Rettigheder, licens o.a.:

Dette system et QGIS plugin dvs. en integreret udvidelse af QGIS. Dette betyder, at koden til det udførte arbejde er underlagt samme licens som selve QGIS: GPL- licensen. 

Kort fortalt medfører denne licens, at du som modtager af systemet:

- Har fået den fulde programtekst (kildekoden) udleveret sammen med plugin-systemet.

- Kan selv tilrette eller videreudvikle kildekoden uden tilladelse fra - eller kompensation til leverandøren. 

- Kan videreformidle plugin-systemet og kildekode til tredjepart uden tilladelse fra eller kompensation til leverandøren.

- Eventuelle ændringer og tilføjelser til kildekoden bliver automatisk tvangsunderlagt samme GPL–licens som originalen. Og ved videreformidling af programsystem og kildekode til tredjepart forbliver disse under GPL–licensen. Dvs. der gælder samme licensforhold mellem dig og tredjepart,
 som der gælder mellem den oprindelige udvikler og dig.

Man kan kort sige, at du har fuld råderet til plugin-programmet og kildekode. Men det er ikke muligt at ændre på licensen og konsekvenserne af samme; 
ej heller på de programdele, som du evt. selv har videreudviklet.

Se i øvrigt: https://www.gnu.org/licenses/gpl.html for en uddybende forklaring.
  
## Et lille hjertesuk:

Du kan downloade og bruge dette system uden at skulle betale licens til udvikleren. Det er helt gratis!

Men selv om systemet er gratis er min tid brugt til evt. assistance *ikke*. Så hvis du henvender dig til mig vedr. hjælp til opsætning eller med forslag til forbedringer/fejlrettelser - så må du også forvente at få en faktura fra mig for tiden brugt til at hjælpe dig.

På den anden side vil du aldrig få en faktura fra mig uden at vi på forhånd har aftalt dette. Og alle forbedringer og rettelser betalt af dig vil fremadrettet være til glæde for alle brugere af systemet. Så det er en god idé at finde andre interessenter og slå sig sammen for at dele udgiften til større forbedringer. 

Min nuv. timesats (19/6 2022) er 985,- kr. eks. moms pr. påbegyndt time.

# QGIS DMP Manager

**Denne plugin er beregnet til QGIS ver. 3.22 eller senere.**

**NB! Ny version fra den 4/7 2025, se nederst i denne readme.** 

QGIS DMP Manager er et plugin, som giver brugeren mulighed for at downloade valgfri datalag fra DAI, Miljøportalen. Man kan herefter bearbejde data ligesom alle andre redigérbare lag i QGIS. Slutteligt kan de redigerede data kopieres tilbage til Miljøportalen. 

Data placeres i en lokal datakilde i form en tabel i en database. Modtager-databasen kan være af typen PostgreSQL eller GeoPackage.  

Download funktionen medfører, at der oprettes to tabeller for hvert data-lag der hentes fra DAI: Et ”redigeringslag”, som brugeren kan rette i; dvs. oprette nye,  modificere eller slette poster. Samtidigt oprettes en ”referencelag” i samme database hvor referencelaget struktur- og indholdsmæssigt er fuldkommen ens med redigeringslaget (før brugeren begynder at rette data) - blot under et andet tabel-navn.

Redigeringslaget er et helt almindeligt data-lag i QGIS og du kan derfor benytte alle QGIS’s avancerede redigeringsfunktioner på dette lag. (Du må ikke rette i referencelaget, da man fjerner muligheden for plugin’et senere kan sammenligne dataindhold i redigeringslag og referencelag.)

Man kan downloade flere typer af data-lag fra DAI, således at disse lag findes samtidigt som redigerings/referencelag i QGIS. Dette giver mulighed for at tilrette data på tværs af forskellige data-lag fra DAI. 

Når data tilretning er færdiggjort i redigeringslaget kan brugeren sammenligne data mellem redigeringslag og referencelag vha. en funktion i plugin-et. Funktionen finder alle forskelle mellem redigerings- og referencelag (oprettelser, rettelser og sletninger) og viser disse som lag - hhv. ”Oprettet”, ”Rettet” eller ”Slettet” i QGIS kortvinduet. Brugeren kan herefter kontrollere de enkelte modificerede elementer og efter kontrol ”skubbe” (uploade) modifikationerne tilbage til DAI.

Plugin-et har mulighed for at gemme en tematisering (symbolisering) for hver DAI lagtype, således at samme tematisering vil blive benytte ved senere downloads af data-lag fra DAI. 

Plugin-et har slutteligt en række administrative funktioner, f.eks. at kunne opstarte QGIS geometri-tjekker på det valgte lag.

Plugin-et kan benyttes til både demo-miljøet og produktionsmiljøet hos DAI, Miljøportalen.  

## Vejledninger

Download af alle filer i repository som én zip-fil udføres ved at trykke på den grønne knap med teksten "Code" i hovedskærmbilledet for repository (https://github.com/AestasGIS/QGIS-DMP-Plugin-installation) og vælge "Download ZIP" i undermenuen.

Der findes to vejledninger til plugin: "Installationvejledning.docx", som beskriver hvorledes systemet skal installeres. Og "Brugervejledning.docx", som beskriver den daglige brug af systemet.

Da systemet er noget kringlet at installere, anbefales det **kraftigt** at læse både installations- og bruger-vejledning før installation og brug...

## Rettigheder, licens o.a.:

Dette system et QGIS plugin dvs. en integreret udvidelse af QGIS. Dette betyder, at koden til det udførte arbejde er underlagt samme licens som selve QGIS: GPL- licensen. 

Kort fortalt medfører denne licens, at du som modtager af systemet:

- Har fået den fulde programtekst (kildekoden) udleveret sammen med plugin-systemet.

- Kan selv tilrette eller videreudvikle kildekoden uden tilladelse fra - eller kompensation til leverandøren. 

- Kan videreformidle plugin-systemet og kildekode til tredjepart uden tilladelse fra - eller kompensation til leverandøren.

- Eventuelle ændringer og tilføjelser til kildekoden bliver automatisk tvangsunderlagt samme GPL–licens som originalen. Og ved videreformidling af programsystem og kildekode til tredjepart forbliver disse under GPL–licensen. Dvs. der gælder samme licensforhold mellem dig og tredjepart, som der gælder mellem den oprindelige udvikler og dig.

Man kan kort sige, at du har fuld råderet til plugin-programmet og kildekode. Men det er ikke muligt at ændre på licensen og konsekvenserne af samme; 
ej heller på de programdele, som du evt. selv har videreudviklet.

Se i øvrigt: https://www.gnu.org/licenses/gpl.html for en uddybende forklaring.
  
## Rapportering af fejl:

Alle fejlrapporter, forslag til forbedringer osv. bør først og fremmest oprettes som "issues" i dette repository (https://github.com/AestasGIS/QGIS-DMP-Plugin-installation/issues). Og før du laver en fejlrapport: Download og installér venligst den sidste nye udgave af plugin - og tjek om fejlen allerede er rettet. Det vil spare tid for både dig og mig :-)  

Hvis du ikke har - og ikke ønsker at oprette - en GitHub account kan du alternativt bruge mailing listen (Se næste afsnit)

## Mailing liste for plugin:
Der er oprettet en mailing lsite: dmp-plugin@googlegroups.com, hvor medlemmer kan stille spørgsmål, indberette fejl og forslag til nye funktioner. Tilmelding kan ske ved at sende en mail til bvt@aestas.dk med oplysning om navn og mail adresse.

## Ny version på vej:
Se "ForslagNyeFunktioner.docx" og "PrioriteringForslag.xslx"

## Et lille hjertesuk:

Du kan downloade og bruge dette system uden at skulle betale licens til udvikleren. Det er helt gratis!

Men selv om systemet er gratis er min tid brugt til evt. assistance *ikke*. Så *hvis* du henvender dig til mig vedr. hjælp til opsætning eller med ønsker om forbedringer - så må du også forvente at få en faktura fra mig for tiden brugt til at hjælpe dig.

På den anden side vil du aldrig få en faktura fra mig uden at vi på forhånd har aftalt dette. Og alle forbedringer og rettelser betalt af dig vil fremadrettet være til glæde for alle brugere af systemet. Så det er en god idé at finde andre interessenter og slå sig sammen for at dele udgiften til større forbedringer. 

Min nuv. timesats (19/6 2022) er 985,- kr. eks. moms pr. påbegyndt time.

## Ny version pr. 4/7 2025

Miljøportalen har i løbet af 2025 ændret http adresserne på kommunikation til Miljøportalen. Dette er nu rettet til de nye værdier i plugin.

Miljøportalen har skiftet teknologi, således at opsætning af den initiale kommunikation mellem plugin og Miljøportalens web server nu tager længere tid. Det betyder at ventetiden ved opstart er sat op fra 1 sekund til 5 sekunder af driftstekniske årsager. Det påvirker ikke den efterfølgende brug, som hverken er langsommere eller hurtigere end tidligere. Opstartstiden kan muligvis sættes noget ned, men det længere tidsrum er valgt for at undgå driftsfejl.

Plugin kan nu modtage, behandle og uploade såkaldte "domain-multi" datatyper, dvs. felter, hvor det er tilladt at tildele flere værdier til et enkelt felt. Denne metode blev ikke brugt (eller dokumenteret) da DMP Manager plugin'et blev udviklet for en del år tilbage, men er blevet taget i  brug for "Beskyttede Sten og Jorddiger 2022" (type 2002), felt "beskyt-kode" / "Beskyttelsesårsag" 
Visuelt er QGIS attribut dialogen ændret for dette felt, således der vises en afkrydsnings liste i stedet for en dropdown liste.

Brugen af "domain -multi" felter medførte at funktionen til at loade data lokalt i GeoPackage ikke virkede længere. Dette er rettet.

Den tidligere udgave af DMP Manager placerede et downloadet lag tilfældigt i projektet. Nu placeres et downloadet lag altid øverst i QGIS projektet. 

Vær opmærksom på at MiljøPortalen begrænser download antal til maksimalt 10.000 poster. Det påvirker bl.a. "Beskyttede Sten og Jorddiger 2022", da der landsdækkende er flere diger end 10.000. DMP Manager har en facilitet til kun at downloade data  indenfor  kortvinduet. Denne kan bruges til at garantere, at alle data indenfor et geografisk afgrænset område kommer med. 

Plugin er blevet installeret og testet mod "demo" udgave af Miljøportalen i QGIS versionerne  3.40, 3.42 og 3.44. Plugin fungerer muligvis på tidligere udgaver af QGIS, men er dette er ikke afprøvet.

Ved opgradering til den nye version er det _ikke_ nødvendigt at geninstallere .Net runtime. Den eksisterende version af .Net runtim fungerer fint med den ney version af DMP Manager plugin'et.
Når DMP Manager geninstalleres, bliver opsætningen til database nulstillet, så husk at indstille DMP Manager til at bruge jeres Postgres database / GeoPackage igen.




Med venlig hilsen

Bo Victor Thomsen

Civ.Ing., GIS- og Database-konsulent

AestasGIS Danmark


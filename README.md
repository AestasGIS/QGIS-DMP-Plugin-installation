# QGIS-DMP-Plugin-installation

**Installationsvejledning til QGIS DMP Manager – ET QGIS baseret plugin til håndtering og redigering af data fra Miljøportalen**

Dette QGIS plugin indeholder funktioner til:

- Download af DAI lag fra Miljøportalen, således data optræder som normale lag i QGIS.
- Data lagres i to lag: Redigeringslaget, som brugeren efter download kan benytte til redigering af data; samt referencelaget, som vil blive benyttet til sammenligning i forbindelse med upload af ændringer til Miljøportalen.
- Redigeringslaget kan redigeres (insert, update og delete) med alle QGIS redigeringsværktøjer. Redigerings session kan strække sig over flere sessioner i QGIS, hvis det af DMP plugin oprette projekt gemmes.
- Efter redigering findes der værktøjer til sammenligning mellem de oprindelige data og de redigerede data.
- Slutteligt findes der værktøjer til at uploade de redigerede data til Miljøportalen og registrere resultatet

###


### Installation af .NET Runtime 3.1.26

Plugin&#39;et benytter nogle funktioner i .NET Runtime. Så denne runtime skal installeres før selve plugin&#39;et installeres.

Installationsfil til .NET Runtime kan findes på følgende hjemmeside:

[https://dotnet.microsoft.com/en-us/download/dotnet/3.1](https://dotnet.microsoft.com/en-us/download/dotnet/3.1)

Der vælges en installationfil til &quot;.NET Runtime 3.1.26&quot; eller en senere version. Det er **ikke** nødvendigt at downloade hverken &quot;SDK&quot;, &quot;Desktop&quot; eller &quot;ASP&quot; udgaven af runtime. Man skal vælge den korrekte installationsfil afhængig af operativsystem og computer arkitektur. Dette vil i langt de fleste tilfælde være:
 "Installers" -> "Windows" ->["X64"](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-3.1.26-windows-x64-installer)

 For at installationen kan gennemføres er det nødvendigt at Windows brugeren har &quot;local admin&quot; rettigheder.

 Installationen startes (og fuldføres) ved at dobbeltklikke på installationsfilen.

### Installation af DMP Manger plugin.

Plugin zip fil kan downloades fra hjemmesiden:

[https://github.com/AestasGIS/QGIS-DMP-Plugin-installation/blob/main/dmp\_manager.zip](https://github.com/AestasGIS/QGIS-DMP-Plugin-installation/blob/main/dmp_manager.zip)

og trykke på knap &quot;Download&quot;

Efter download af plugin zip-fil foretages installationen i QGIS med følgende:

Tryk på menupunkt &quot;Plugins&quot; -\&gt; &quot;Manage and Install Plugins….&quot; -\&gt; Faneblad &quot;Install from ZIP&quot;

Følgende brugerdialog vises:


![](/Billede1.jpg)

Tryk på knappen fremhævet med gult og vælg filen &quot;dmp\_manager.zip&quot; fra mappe &quot;Overførelser&quot; (eller hvor zip-filen blev downloadet til)

Installationen gennemføres herefter ved at trykke på knap &quot;Install Plugin&quot;.

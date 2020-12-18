# Mars Agriculture and Research Service - project groep 14, Server
*door Timo De Clercq, Annelin De Gols, Robin De Kinders Laurens Giesen, Cedric Puystjens*



[![License](https://img.shields.io/badge/License-SonarlintClient%201.0-Green.svg)](https://sonar.ti.howest.be/sonar/dashboard?id=2020.project-ii%3Amars-client-14) [![License](https://img.shields.io/badge/License-SonarlintServer%201.0-Green.svg)](https://sonar.ti.howest.be/sonar/dashboard?id=2020.project-ii%3Amars-server-14)

![Website Home Page](./img/Home.png)
<br></br>

---
##Inhoudstafel

* [Beschrijving](#beschrijving)
* [Flowchart](#flowchart)
* [Server](#server)
  + [Informatie](#informatie)
  + [Installatie](#installatie)
  + [Configuratie](#configuratie)
* [Client](#client)
  + [Informatie](#informatie-1)
  + [Installatie](#installatie-1)
  + [Configuratie](#configuratie-1)
<br><br>
---
## Beschrijving

Al snel werd het duidelijk dat we het probleem van voedselschaarste wilden
aanpakken. Het zou zinloos zijn als je steeds moet wachten op de volgende levering
voedsel van Aarde naar Mars. Met ons concept Mars Agricultural Research Service
(verder afgekort als MARS) proberen we mensen samen te brengen om een
autonome samenleving te creëren op vlak van voedsel.
<br> <br>
---
## Flowchart
![Flowchart](img/flowchart.png)
<br><br>

---
## Server
### Informatie

Om de server op te zetten start je met het [Clonen](#installatie) van de server. Als de server succesvol gecloned is kan je deze [configureren](#configuratie) in de **conf/config.json**. Hier moet je een poort specifiëren waarop je de server wilt draaien. In deze configuratie file kan u ook de gegevens voor de database wijzigen. In de file: [MarsOpenApiBridge](NYI) worden alle requests afgehandeld die in de [OpenAPI File](NYI) omschreven zijn. Deze file staat in contact met de [MarsController](NYI), in deze MarsController worden de repo's aangemaakt waarmee we zaken kunnen doen zoals gebruikers aanmaken, gewassen oplijsten, ...
<br><br>

---
### Installatie
```
git clone git@git.ti.howest.be:TI/2020-2021/s3/project-ii/projects/groep-14/server.git

```
Of
``` 
git clone https://git.ti.howest.be/TI/2020-2021/s3/project-ii/projects/groep-14/server.git

```
<br />

---
### Configuratie

**Path: conf/config.json**

```json

{
  "http": {
    "port": 8080
  },
  "db" : {
    "url": "jdbc:h2:~/mars-db",
    "username": "group-14",
    "password": "t3sfe1k3nUe",
    "webconsole.port": 9000
  }
}

```
<br> <br>

---
## Client
<br />

---
### Informatie
<br />

Als u de repository mooi binnengehaald hebt via git clone, dan kunt u alle files geordend zien. In [assets](NYI) bevinden zich alle css-files, javascript-files en images. Als u onze [index.html](NYI) in de browser opent, kan u de volledige client-side ervaren. Aan de hand van requests die zich bevinden in de javascript-files, communiceert onze client met de server (Java). De code wordt gecontroleerd via [SonarLint](https://sonar.ti.howest.be/sonar/projects?search=14+mars). Dit is een tool die fouten/bugs zoekt in onze code. In de [package.json](NYI) zitten alle scripts die de code valideren. Zo zijn we verplicht om kwaliteitsvolle code te schrijven.
<br><br>

---
### Installatie

```
git clone git@git.ti.howest.be:TI/2020-2021/s3/project-ii/projects/groep-14/client.git

```
Of

``` 
git clone https://git.ti.howest.be/TI/2020-2021/s3/project-ii/projects/groep-14/client.git

```
<br><br>

---
### Configuratie

**Path: Client/src/config.json**
```json
{
  "host": "http://localhost:8080",
  "folder": "",
  "group": "mars-14"
}

```
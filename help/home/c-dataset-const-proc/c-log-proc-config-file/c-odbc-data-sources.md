---
description: De server van de gegevenswerkbank (InsightServer64.exe) kan gebeurtenisgegevens van om het even welk SQL gegevensbestand (bijvoorbeeld, Oracle of de Server van Microsoft SQL) lezen die een ODBC 3.0 volgzame bestuurder heeft.
title: ODBC-gegevensbronnen
uuid: 5b37cd41-2d79-472c-8e6d-00ff894991a9
exl-id: b22b1e27-9b6c-4708-b45c-a9605807689a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 0%

---

# ODBC-gegevensbronnen{#odbc-data-sources}

{{eol}}

De server van de gegevenswerkbank (InsightServer64.exe) kan gebeurtenisgegevens van om het even welk SQL gegevensbestand (bijvoorbeeld, Oracle of de Server van Microsoft SQL) lezen die een ODBC 3.0 volgzame bestuurder heeft.

De ODBC-ondersteuning van de gegevenswerkbankserver is vergelijkbaar met bestaande ondersteuning voor het laden van gegevens van sensoren of logbestanden die zijn gegenereerd door externe processen. Er zijn echter enkele aanvullende overwegingen en beperkingen:

* De ODBC-ondersteuning van de server op de gegevenswerkbank is compatibel met de clusteringmogelijkheden. De gegevens worden verdeeld onder alle verwerkingsservers, en alle verdere verwerking (met inbegrip van vraagverwerking) profiteert volledig van het groeperen.
* ODBC-ondersteuning is afhankelijk van ODBC-stuurprogramma&#39;s van derden. Om ODBC-ondersteuning te kunnen gebruiken, moeten deze stuurprogramma&#39;s zijn geconfigureerd op de computer waarop de gegevenswerkbankserver wordt uitgevoerd, met hulpprogramma&#39;s die zich buiten het Adobe-platform bevinden. Voor gegevenswerkbankmachines is geen aanvullende configuratie vereist.
* De lijst of de mening waarvan het gegeven wordt geladen moet een stijgende kolom van identiteitskaart hebben. Voor een rij mag de waarde in deze kolom (die een werkelijke kolom in de tabel of een SQL-kolomexpressie kan zijn) niet dalen wanneer nieuwe rijen in de database worden ingevoegd. Als deze beperking wordt overtreden, gaan de gegevens verloren. Voor een goede prestatie is een index vereist voor deze kolom of kolomexpressie.

   >[!NOTE]
   >
   >Meerdere rijen kunnen dezelfde waarde hebben in het dialoogvenster [!DNL Increasing ID] kolom. Eén mogelijkheid is een tijdstempelkolom met minder dan perfecte precisie.

* De server van de gegevenswerkbank kan geen kolommen met lange gegevens laden (gegevens boven een bepaalde lengte zoals die door de specifieke gegevensbestandtoepassing in gebruik wordt bepaald).
* Het ophalen van gegevens uit een database gaat langzamer dan het lezen van gegevens uit een schijfbestand. Datasets die gegevens uit een ODBC-bron laden, duurt veel langer om te verwerken (met name bij opwerking) dan gegevenssets van gelijke grootte waarvan de gegevens afkomstig zijn van sensoren of andere schijfbestanden.

Voor informatie over het opnieuw verwerken van uw gegevens raadpleegt u [Opwerking en heromzetting](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

**Om de Server van het Inzicht voor ODBC te vormen[!DNL event data]**

Als u de gegevenswerkbankserver configureert om gegevens uit een SQL-database te laden, moet u eerst de volgende stappen in volgorde uitvoeren:

1. Installeer de juiste databasecliontensoftware, inclusief een ODBC-stuurprogramma, op de computer van de gegevenswerkbankserver waarop de gegevensset wordt verwerkt.

   >[!NOTE]
   >
   >Als u ODBC-gebeurtenisgegevens laadt voor verwerking in een servercluster van een gegevenswerkbank, moet u de databasecliënt installeren op alle verwerkingsservers in de cluster. Voor informatie over het specificeren van verwerkingsservers in een cluster, zie *Handleiding voor installatie en beheer van serverproducten*.

1. Vorm een Gegevensbron gebruikend de Beheerder van de Gegevensbron ODBC voor Vensters.

   Het is belangrijk om op te merken dat de server van de gegevenswerkbank (InsightServer64.exe) als dienst van Vensters loopt. Daarom moet de Gegevensbron gewoonlijk als systeem DSN eerder dan een gebruiker DSN voor de server van de gegevenswerkbank worden gevormd om het te kunnen gebruiken. Meer informatie over deze configuratiestap vindt u in de documentatie bij de databasesoftware.

Na het installeren van de software van de gegevensbestandcliënt op de aangewezen machine van de gegevenswerkbankserver, kunt u de dataset vormen om de ODBC- gegevensbron te gebruiken door de aangewezen parameters in te geven [!DNL Log Processing] configuratiebestand voor het gewenste profiel.

## Parameters {#section-15c0218d93364693a565f2609a12f73e}

Voor gegevens van gegevensbestanden die de Open norm van de Connectiviteit van het Gegevensbestand (ODBC) gebruiken, zijn de volgende parameters beschikbaar:

<table id="table_606D8A90DA4A43C29F2C6130F8C753F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> De id voor de ODBC-bron. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam gegevensbron </td> 
   <td colname="col2"> Een DSN, zoals verstrekt door een beheerder van de machine van de gegevenswerkbankserver waarop de dataset wordt verwerkt, die naar het gegevensbestand verwijst waarvan gegevens moeten worden geladen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Wachtwoord database </td> 
   <td colname="col2"> Het wachtwoord dat moet worden gebruikt wanneer verbinding wordt gemaakt met de database. Als een wachtwoord voor DSN in is gevormd <span class="wintitle"> Gegevensbronbeheerder</span>, kan dit leeg worden gelaten. Om het even welk die wachtwoord hier wordt verstrekt treedt het wachtwoord met voeten voor DSN in <span class="wintitle"> Gegevensbronbeheerder</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikersnaam database </td> 
   <td colname="col2"> De gebruikersnaam die moet worden gebruikt wanneer verbinding wordt gemaakt met de database. Als een gebruiker - identiteitskaart voor DSN in is gevormd <span class="wintitle"> Gegevensbronbeheerder</span>, kan dit leeg worden gelaten. Om het even welke die gebruikers - identiteitskaart hier wordt verstrekt treedt de gebruiker - identiteitskaart met voeten voor DSN in <span class="wintitle"> Gegevensbronbeheerder</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Velden </td> 
   <td colname="col2"> Een vector van kolomvoorwerpen die een afbeelding van gegevenskolommen in het gegevensbestand aan gegevensgebieden in de motor van de gegevenswerkbankserveruitvoering specificeert. Elke kolom bevat items <span class="wintitle"> Kolomnaam</span> en <span class="wintitle"> Veldnaam</span>. <span class="wintitle"> Kolomnaam</span> is een SQL kolomuitdrukking die in de context van de lijst geldig moet zijn die door wordt geïdentificeerd <span class="wintitle"> Tabel-id</span> hierboven beschreven. Dit kan een kolomnaam of een SQL-expressie zijn op basis van een willekeurig aantal kolommen in de tabel. Een opmaakfunctie kan nodig zijn om waarden van bepaalde gegevenstypen op een bepaalde manier in tekenreeksen om te zetten zonder de precisie te verliezen. Alle gegevens worden impliciet geconverteerd naar tekenreeksen met behulp van de standaard opmaakmethode van de database. Dit kan gegevensverlies veroorzaken voor bepaalde typen kolomgegevens (zoals de gegevenstypen datum-/tijdgegevens) als geen expliciete opmaakexpressies worden gebruikt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Id-kolom vergroten </td> 
   <td colname="col2"> <p>Een kolomnaam of SQL-kolomexpressie die voldoet aan het criterium dat de waarde toeneemt (of ten minste niet afneemt) wanneer nieuwe rijen worden toegevoegd. Met andere woorden, als Rij B later aan de tabel wordt toegevoegd dan Rij A, moet de waarde van deze kolom (of kolomexpressie) in Rij B groter zijn (volgens de native sorteervolgorde van de database) dan de corresponderende waarde in Rij A. </p> <p> 
     <ul id="ul_EBF6AEE4746B41B3B5BB6CC74194DAED"> 
      <li id="li_A5C9BE52B01649DE9726ECEC68B99828"> De <span class="wintitle"> Id-kolom vergroten </span>De naam mag dezelfde zijn als de naam van een bestaande kolom, maar dit hoeft niet zo te zijn. </li> 
      <li id="li_CF69EAB4AFB14F4894F7A5CDCAF06947"> Deze expressie wordt verondersteld een SQL-gegevenstype te hebben. Als de werkelijk stijgende kolom van identiteitskaart van een ander gegevenstype is, moet deze waarde een kolomuitdrukking zijn om het in een koord om te zetten. Omdat dit gewoonlijk betekent dat vergelijkingen lexicografisch (karakter door karakter) zijn, is het belangrijk om de waarde zorgvuldig te formatteren. </li> 
      <li id="li_58977431962E48039C898CFC47C53323"> De uitdrukking wordt gebruikt in SQL ORDER DOOR clausules en vergeleken met in SQL WAAR clausules. Het is van cruciaal belang dat een index wordt gebaseerd op de exacte kolomexpressie die wordt gebruikt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Logbron-id </td> 
   <td colname="col2"> <p>De waarde van deze parameter kan elke tekenreeks zijn. Als een waarde wordt gespecificeerd, laat deze parameter u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het veld x-log-source-id wordt gevuld met een waarde die de logbron voor elke logbestandvermelding identificeert. Bijvoorbeeld, als u logboekingangen van een bron ODBC genoemd ODBCSource01 wilt identificeren, kon u typen <span class="filepath"> uit ODBCSource01.</span> en die tekenreeks zou worden doorgegeven aan het veld x-log-source-id voor elke logbestandvermelding uit die bron. </p> <p> Voor informatie over het x-log-source-id veld raadpleegt u <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> Gebeurtenisgegevensrecordvelden</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoeren op server </td> 
   <td colname="col2"> Indexwaarde in het dialoogvenster <span class="filepath"> profile.cfg</span> bestand van de verwerkingsserver die de ODBC-query's maakt om gegevens van de database op te halen. (De parameter Verwerkingsservers in het dialoogvenster <span class="filepath"> profile.cfg</span> het dossier maakt een lijst van alle verwerkingsservers voor de dataset, en elke server heeft een indexwaarde, eerste is 0.) De standaardwaarde is 0. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tabel-id </td> 
   <td colname="col2"> An SQL expression that names the table or view from which data is to be loaded. Een typische lijstherkenningsteken is van de vorm SCHEMA.TABLE. </td> 
  </tr> 
 </tbody> 
</table>

In dit voorbeeld wordt het [!DNL Log Processing] configuratievenster in gegevenswerkbank met een ODBC- gegevensbron. Deze gegevensbron neemt gegevens van een lijst genoemd [!DNL VISUAL.VSL] in een database met [!DNL Data Source Name] &quot;VSTestO.&quot; Vijf (5) kolomobjecten ( [!DNL Fields]) kaartgegevens van de gegevenskolommen in het gegevensbestand aan de server van de gegevenswerkbank.

![](assets/cfg_LogProcessing_LogSources_ODBC.png)

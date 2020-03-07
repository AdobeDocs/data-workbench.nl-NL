---
description: De server van de gegevenswerkbank (InsightServer64.exe) kan gebeurtenisgegevens van om het even welk SQL gegevensbestand (bijvoorbeeld, Oracle of de Server van Microsoft SQL) lezen dat een ODBC 3.0 volgzame bestuurder heeft.
solution: Analytics
title: ODBC-gegevensbronnen
topic: Data workbench
uuid: 5b37cd41-2d79-472c-8e6d-00ff894991a9
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# ODBC-gegevensbronnen{#odbc-data-sources}

De server van de gegevenswerkbank (InsightServer64.exe) kan gebeurtenisgegevens van om het even welk SQL gegevensbestand (bijvoorbeeld, Oracle of de Server van Microsoft SQL) lezen dat een ODBC 3.0 volgzame bestuurder heeft.

De ondersteuning van ODBC van de server van de gegevenswerkbank is gelijkaardig aan bestaande steun voor het laden van gegevens van Sensors of van logboekdossiers die door externe processen worden geproduceerd. Er zijn echter nog enkele andere overwegingen en beperkingen:

* De ondersteuning van ODBC van de server van de gegevenswerkbank is compatibel met de clusteringsmogelijkheden. Het gegeven wordt verdeeld onder alle verwerkingsservers, en alle verdere verwerking (met inbegrip van vraagverwerking) voordelen volledig van zich het groeperen.
* De steun ODBC hangt van derdeODBC bestuurders af. Voor steun ODBC om te werken, moeten deze bestuurders op de machine worden gevormd waarop de server van de gegevenswerkbank loopt, gebruikend hulpmiddelen buiten het platform van Adobe. De werkbankmachines van gegevens vereisen geen extra configuratie.
* De lijst of de mening waarvan het gegeven wordt geladen moet een stijgende kolom van identiteitskaart hebben. Voor om het even welke rij, moet de waarde in deze kolom (die een daadwerkelijke kolom in de lijst of om het even welke SQL kolomuitdrukking kan zijn) niet verminderen aangezien de nieuwe rijen in het gegevensbestand worden opgenomen. Als deze beperking wordt overtreden, wordt het gegeven verloren. Voor adequate prestaties, wordt een index vereist op deze kolom of kolomuitdrukking.

   >[!NOTE]
   >
   >Het is mogelijk voor veelvoudige rijen om de zelfde waarde in de [!DNL Increasing ID] kolom te hebben. Één mogelijkheid is een timestamp kolom met minder dan perfecte precisie.

* De server van de gegevenswerkbank kan geen kolommen met lange gegevens laden (gegevens boven een bepaalde lengte zoals die door de specifieke gegevensbestandtoepassing in gebruik wordt bepaald).
* Het terugwinnen van gegevens van een gegevensbestand is langzamer dan lezend het van een schijfdossier. Datasets die gegevens van een bron ODBC laden duurt veel langer om te verwerken (in het bijzonder wanneer het opwerken) dan equivalent gerangschikte datasets de waarvan gegevens uit Sensors of andere schijfdossiers komen.

Voor informatie over het opnieuw verwerken van uw gegevens, zie [Verwerking en Herschikking](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md).

**Om de Server van het Inzicht voor ODBC te vormen[!DNL event data]**

Het vormen van de server van de gegevenswerkbank om gegevens van een SQL gegevensbestand te laden vereist dat u eerst de volgende stappen in orde uitvoert:

1. Installeer de aangewezen software van de gegevensbestandcliënt, met inbegrip van een bestuurder ODBC, op de de servermachine van de gegevenswerkbank waarop de dataset wordt verwerkt.

   >[!NOTE]
   >
   >Als u ODBC gebeurtenisgegevens voor verwerking op een de servercluster van de gegevenswerkbank laadt, moet u de software van de gegevensbestandcliënt op alle verwerkingsservers in de cluster installeren. Voor informatie over het specificeren van verwerkingsservers in een cluster, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

1. Vorm een Gegevensbron gebruikend de Beheerder van de Gegevensbron ODBC voor Vensters.

   Het is belangrijk om op te merken dat de server van de gegevenswerkbank (InsightServer64.exe) als dienst van Vensters loopt. Daarom moet de Gegevensbron gewoonlijk als systeem DSN eerder dan een Gebruiker DSN voor de server van de gegevenswerkbank worden gevormd om het te kunnen gebruiken. U kunt meer informatie over deze configuratiestap in de documentatie voor uw gegevensbestandsoftware vinden.

Na het installeren van de software van de gegevensbestandcliënt op de aangewezen server van de gegevenswerkbank, kunt u de dataset vormen om de ODBC gegevensbron te gebruiken door de aangewezen parameters in het [!DNL Log Processing] configuratiedossier voor het gewenste profiel uit te geven.

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
   <td colname="col2"> Het herkenningsteken voor de bron ODBC. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Naam gegevensbron </td> 
   <td colname="col2"> Een DSN, zoals die door een beheerder van de de servermachine van de gegevenswerkbank wordt verstrekt waarop de dataset wordt verwerkt, die naar het gegevensbestand verwijst waarvan het gegeven moet worden geladen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Database-wachtwoord </td> 
   <td colname="col2"> Het wachtwoord dat moet worden gebruikt wanneer het verbinden met het gegevensbestand. Als een wachtwoord voor DSN in de Beheerder <span class="wintitle"> van de</span>Gegevensbron is gevormd, kan dit leeg worden verlaten. Om het even welk hier verstrekt wachtwoord treedt het wachtwoord met voeten dat voor DSN in de Beheerder van de <span class="wintitle"> Gegevensbron</span>wordt gevormd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebruikersnaam database </td> 
   <td colname="col2"> De gebruiker - identiteitskaart die moet worden gebruikt wanneer het verbinden met het gegevensbestand. Als een gebruiker - identiteitskaart voor DSN in de Beheerder <span class="wintitle"> van de</span>Gegevensbron is gevormd, kan dit leeg worden verlaten. Om het even welke die gebruiker - identiteitskaart hier wordt verstrekt treedt de gebruiker - identiteitskaart met voeten voor DSN in de Beheerder van de <span class="wintitle"> Gegevensbron</span>wordt gevormd die. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Gebieden </td> 
   <td colname="col2"> Een vector van kolomvoorwerpen die een afbeelding van gegevenskolommen in het gegevensbestand aan gegevensgebieden in de de uitvoeringsmotor van de gegevenswerkbankserver specificeert. Elke kolom heeft ingangen <span class="wintitle"> de Naam</span> van de Kolom en de Naam <span class="wintitle"> van het Gebied</span>. <span class="wintitle"> De Naam</span> van de kolom is een SQL kolomuitdrukking die in de context van de lijst geldig moet zijn die door het <span class="wintitle"> hierboven beschreven Herkenningsteken</span> van de Lijst wordt geïdentificeerd. Het kan een kolomnaam of om het even welke SQL uitdrukking zijn die op om het even welk aantal kolommen in de lijst wordt gebaseerd. Een het formatteren functie kan noodzakelijk zijn om waarden van bepaalde gegevenstypes in koorden om te zetten op een manier die geen precisie verliest. Alle gegevens worden impliciet omgezet in koorden gebruikend de standaard het formatteren methode van het gegevensbestand, die gegevensverlies voor sommige types van kolomgegevens (zoals datum/tijdgegevenstypes) kan veroorzaken als de expliciete het formatteren uitdrukkingen niet worden gebruikt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stijgende kolom van identiteitskaart </td> 
   <td colname="col2"> <p>Een kolomnaam of SQL kolomuitdrukking die aan het criterium voldoet dat het (of minstens niet vermindert) verhoogt aangezien de nieuwe rijen worden toegevoegd. Namelijk als Rij B aan de lijst in een recentere tijd dan Rij A wordt toegevoegd, moet de waarde van deze kolom (of kolomuitdrukking) in Rij B groter zijn (volgens de inheemse sorterende orde van het gegevensbestand) dan de overeenkomstige waarde in Rij A. </p> <p> 
     <ul id="ul_EBF6AEE4746B41B3B5BB6CC74194DAED"> 
      <li id="li_A5C9BE52B01649DE9726ECEC68B99828"> De <span class="wintitle"> Toenemende </span>naam van de Kolom van identiteitskaart kan het zelfde zijn als de naam van een bestaande kolom, maar moet niet zijn. </li> 
      <li id="li_CF69EAB4AFB14F4894F7A5CDCAF06947"> Deze uitdrukking wordt verondersteld om een SQL type van karaktergegevens te hebben. Als de daadwerkelijke stijgende kolom van identiteitskaart van een ander gegevenstype is, moet deze waarde een kolomuitdrukking zijn om het in een koord om te zetten. Omdat dit gewoonlijk betekent de vergelijkingen lexicografisch (karakter door karakter) zijn, is het belangrijk om de waarde zorgvuldig te formatteren. </li> 
      <li id="li_58977431962E48039C898CFC47C53323"> De uitdrukking wordt gebruikt in SQL ORDE DOOR clausules en vergeleken bij in SQL WAAR clausules. Het is kritiek belangrijk om een index te hebben die op de nauwkeurige kolomuitdrukking wordt voortgebouwd die wordt gebruikt. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ID Logbron </td> 
   <td colname="col2"> <p>De waarde van deze parameter kan om het even welk koord zijn. Als een waarde wordt gespecificeerd, laat deze parameter u toe om logboekingangen van verschillende logboekbronnen voor bronidentificatie of gerichte verwerking te onderscheiden. Het x-logboek-bron-identiteitskaart- gebied is bevolkt met een waarde die de logboekbron voor elke logboekingang identificeren. Bijvoorbeeld, als u logboekingangen van een bron wilt identificeren ODBC genoemd ODBCSource01, kon u <span class="filepath"> van ODBCSource01 typen.</span> en dat koord zou tot het x-logboek-bron-identiteitskaart- gebied voor elke logboekingang uit die bron worden overgegaan. </p> <p> Voor informatie over het x-logboek-bron-identiteitskaart- gebied, zie de Gebieden <a href="../../../home/c-dataset-const-proc/c-ev-data-rec-fields.md#concept-06bda4be1a4649a2905a4422e9e6c42f"> van het Verslag van de Gegevens van de</a>Gebeurtenis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoeren op server </td> 
   <td colname="col2"> De waarde van de index in het <span class="filepath"> profile.cfg</span> - dossier van de verwerkingsserver die de vragen ODBC maakt om gegevens van het gegevensbestand te krijgen. (De parameter van de Servers van de Verwerking in het <span class="filepath"> profile.cfg</span> - dossier maakt een lijst van alle verwerkingsservers voor de dataset, en elke server heeft een indexwaarde, eerste is 0.) De standaardwaarde is 0. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tabelidentificator </td> 
   <td colname="col2"> Een SQL uitdrukking die de lijst of de mening noemt waarvan het gegeven moet worden geladen. Een typisch lijstherkenningsteken is van de vorm SCHEMA.TABLE. </td> 
  </tr> 
 </tbody> 
</table>

Dit voorbeeld toont het [!DNL Log Processing] configuratievenster in gegevenswerkbank met een ODBC gegevensbron. Deze Gegevensbron neemt gegevens van een lijst genoemd [!DNL VISUAL.VSL] in een gegevensbestand met [!DNL Data Source Name] &quot;VSTestO.&quot; Vijf (5) kolomvoorwerpen ( [!DNL Fields]) kaartgegevens van de gegevenskolommen in het gegevensbestand aan de server van de gegevenswerkbank.

![](assets/cfg_LogProcessing_LogSources_ODBC.png)


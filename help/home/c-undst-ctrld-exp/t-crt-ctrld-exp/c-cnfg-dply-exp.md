---
description: Nadat u uw doel, hypothese, en experimentdetails evenals creeerde uw testinhoud hebt bepaald, moet u Sensor vormen om het gecontroleerde experiment op te stellen.
solution: Analytics,Analytics
title: Het vormen en het Opstellen van de Experimenteer
uuid: 460d3ea4-a6c8-4ac4-9a3f-eab71f65b096
exl-id: 957c2ea2-72a5-4bb2-af1d-65187613c26d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1486'
ht-degree: 0%

---

# Het vormen en het Opstellen van de Experiment{#configuring-and-deploying-the-experiment}

Nadat u uw doel, hypothese, en experimentdetails evenals creeerde uw testinhoud hebt bepaald, moet u Sensor vormen om het gecontroleerde experiment op te stellen.

## Het experimentele configuratiebestand {#section-037fe7dea9c94aee9cdc354dafdb7c03} configureren

Om het experiment te vormen, moet u het spreadsheet voltooien van de proefconfiguratie die door Adobe wordt verstrekt (genoemd [!DNL TestExperiment.xls] door gebrek). Dit dossier vormt [!DNL Sensor] om het experiment uit te voeren en is de versie van Excel van het tekstdossier dat u in [het Wijzigen van de Parameter ExpFile](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28) specificeerde.

Dit bestand kan informatie bevatten over meerdere experimenten, die op hetzelfde of op verschillende tijdstippen kunnen worden uitgevoerd en verschillende groepen en percentages gebruiken, maar deze experimenten zijn op geen enkele manier gecorreleerd.

De gebruikers worden geplaatst in een groep voor elk experiment dat in het dossier wordt vermeld dat om op dit ogenblik wordt gevormd te lopen.

>[!NOTE]
>
>Elk experiment staat los van alle andere experimenten. Wijzigingen die u aanbrengt in het ene experiment hebben geen invloed op andere experimenten en hoewel bezoekers wellicht meerdere experimenten uitvoeren, hebben de resultaten geen betrekking op elkaar. Als u denkt dat er een correlatie bestaat tussen de veranderingen in meerdere experimenten, moet u een nieuw experiment maken dat deze veranderingen samen test.

**Uw experiment configureren**

U moet dit bestand voltooien voordat het experiment begint en de informatie niet wijzigen terwijl het experiment wordt uitgevoerd.

>[!NOTE]
>
>Elk experiment is onmiddellijk ongeldig als de definitie van het experiment verandert nadat het experiment is begonnen.

1. Als u beheerdertoegang tot uw Web of toepassingsservers hebt, navigeer aan [!DNL Sensor] installatiemap op om het even welke [!DNL Sensor] machine in uw Webcluster om tot [!DNL TestExperiment.xls] dossier toegang te hebben. Als u geen beheerdersrechten hebt, neemt u contact op met uw Adobe-accountmanager om het [!DNL TestExperiment.xls]-bestand aan te vragen.

1. Open het bestand [!DNL TestExperiment.xls] (u kunt desgewenst de naam van dit bestand wijzigen) en vul de volgende velden in:

<table id="table_FDD6AE631C614F97AD7AE8829E53CCAC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Veld </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Experimenteer </td> 
   <td colname="col2"> <p>Een beschrijvende naam voor het experiment. Elke naam van het experiment moet uniek zijn en mag geen spaties bevatten. </p> <p>Bij de weergave van de resultaten van experimenten in <span class="keyword"> Insight </span> worden namen van experimenten gebruikt. De namen worden weergegeven als de eerste helft van de elementnamen in de gecontroleerde experimentele dimensie. De tweede helft van de elementnaam is de groepsnaam van het veld Groep in dit bestand. Elke groep krijgt een naam in de volgende notatie met de naam van het experiment gevolgd door de naam van de groep: </p> <p><i>Naam ExperimentName.Group</i> </p> <p>Bijvoorbeeld: <span class="filepath"> New_Homepage.Control </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Start </td> 
   <td colname="col2"> <p>De datum en het tijdstip waarop het experiment moet beginnen. Als u geen waarden opgeeft, begint het experiment direct nadat het bestand is geïmplementeerd. </p> <p>Indeling: DD-MM-YYYY H:MM </p> 
    <ul id="ul_FB8B50C688584683AC2226FCBED40AF9"> 
     <li id="li_223EF962CFC64454965444E66284F670">Als je de start- en stoptijden leeg laat, loopt het experiment oneindig. </li> 
     <li id="li_0544C9A98635418CAECD85B67F345772">U kunt begin- en stoptijden lang van tevoren definiëren; daarom kunt u al uw experimenten voor het volgende jaar in één keer vormen indien gewenst. </li> 
     <li id="li_BDFBB74B1D134E57B37DC5C3457AA1A9">De begin- en eindtijd zijn gebaseerd op de systeemtijd van de webserver. Als die klok om welke reden dan ook verandert, kan uw experiment onverwacht starten of stoppen. </li> 
     <li id="li_3295FE5B2AC64B6CA90CC7F31B808EB9">Als u een experiment als ingang van het configuratiedossier zou willen toevoegen maar niet het experiment in de nabije toekomst wilt lopen, kunt u uit de experimentinformatie commentaren gebruikend het aantalteken "#"of begin en ophoudtijden in het verleden bepalen. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Stoppen </td> 
   <td colname="col2"> <p>De datum en tijd waarop het experiment moet worden beëindigd. Wanneer de einddatum en de tijd voorkomen, <span class="wintitle"> zal de sensor </span> ophouden verzendend de koekjeswaarden die als testgroep aan de test URIs worden geïdentificeerd en zal alle koekjes naar de controlegroep URIs verzenden. </p> <p>Indeling: DD-MM-YYYY H:MM </p> <p>Zie de notities voor het veld <span class="wintitle"> Start </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Groep </td> 
   <td colname="col2"> <p>Een beschrijvende naam voor elke groep bezoekers in het experiment. Groepsnamen mogen geen spaties bevatten. </p> <p>De namen van de groep worden gebruikt wanneer het tonen van de resultaten van experimenten in <span class="keyword"> Inzicht </span>. Zie de beschrijving in het veld Experimenteren voor meer informatie. </p> <p>Een controlegroep kan impliciet of uitdrukkelijk worden bepaald gebaseerd op de waarde ingegaan op het gebied van het Percentage. </p> <p> <p>Opmerking:  Om te voldoen aan het aantal bezoekers dat nodig is gedurende de vastgestelde periode voor het statistisch geldige experiment, moet u het betrouwbaarheidsniveau verlagen of de periode verlengen. Als uw tijdsperiode bijvoorbeeld vijf dagen is, is uw betrouwbaarheidsniveau 98% en het aantal bezoekers dat u nodig hebt, overschrijdt het voor die periode verwachte aantal, moet u de tijdsperiode verlengen of het betrouwbaarheidsniveau verlagen totdat het aantal bezoekers dat wordt verwacht, het aantal bezoekers overschrijdt dat nodig is om een statistisch geldig experiment uit te voeren. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Percentage </td> 
   <td colname="col2"> <p>Het percentage websitebezoekers dat in elke gedefinieerde groep moet worden opgenomen. Deze waarden kunnen als percentages of decimale waarden worden uitgedrukt. Bovendien moeten beide waarden groter dan of kleiner dan één zijn. </p> <p>Bijvoorbeeld: </p> <p>33,3% en 66,7% </p> <p>.99 en .01 </p> <p>Als de som voor alle groepen minder dan 100 is, blijft het niet bepaalde overtollige gebrek aan een controlegroep. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Oorspronkelijke URL </td> 
   <td colname="col2"> <p>De URI van de inhoud die opnieuw moet worden toegewezen, gevolgd door $. Deze waarde is hoofdlettergevoelig. </p> <p>Indeling: index.asp$ </p> <p>Oorspronkelijke URI's kunnen worden opgegeven met een dollarteken ($) aan het einde van de URI, om aan te geven dat een exacte overeenkomst met de bestandsnaam vereist is. De expressie <span class="filepath"> /product/product_view.asp$ </span> komt bijvoorbeeld alleen overeen met die exacte pagina, terwijl <span class="filepath"> /product </span> overeenkomt met elke pagina in de map <span class="filepath"> /product </span> en kan worden gebruikt om die volledige substructuur opnieuw toe te wijzen. Oorspronkelijke URL-items die het $-teken aan het einde van de bestandsnaam niet opgeven, worden door het experiment genegeerd, tenzij de parameter ExpPartialMatch is ingesteld op "on." Zie <a href="../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expplmth-prm.md#concept-9c817c4c49b74287b0f70d6a1a37655e"> De parameter ExpPartialMatch wijzigen (optioneel) </a> voor meer informatie over deze parameter. </p> <p>De gecontroleerde experimentfunctionaliteit negeert vraagkoorden die aan de stem van URI worden toegevoegd. De pagina </p> <p> <span class="filepath"> /product/product_view.asp?production=53982  </span> is not a valid URI, but the page  <span class="filepath"> /product/product_view.asp  </span> is a valid URI. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opnieuw toegewezen URL </td> 
   <td colname="col2"> <p>De URI van de alternatieve inhoud. </p> <p>Indeling: index2.asp </p> <p>Zie de opmerkingen voor het veld Oorspronkelijke URL. </p> </td> 
  </tr> 
 </tbody> 
</table>

Hieronder ziet u een voorbeeld van een voltooide [!DNL TextExperiment.xls]-spreadsheet:

![](assets/TestExperimentSpreadsheet.png)

>[!NOTE]
>
>Wijzig de kolomposities in het werkblad niet.

Dit voorbeeld geeft aan dat het experiment New_Homepage begint op 1 juni 2006, eindigt op 30 juni 2006, en bevat een controlegroep met 50% van de bezoekers en een testgroep met 50% van de bezoekers, die verschillende inhoud voor één URI zien.

>[!NOTE]
>
>Hoewel in het voorbeeldbestand hierboven een expliciete controlegroep is gedefinieerd, is het niet nodig om expliciet een controlegroep te definiëren. Het experiment maakt dan automatisch de controlegroep. Als de som van de percentages voor alle groepen in een experiment minder dan 100% is, wordt een impliciete controlegroep toegewezen aan gebruikers die niet in één van de expliciete groepen vallen.

1. Als u opmerkingen wilt invoegen voor aanvullende informatie over specifieke experimenten, begint u met een hekje (#) in de cel en volgt u de opmerkingen. Opmerkingen kunnen overal in het bestand worden ingevoegd.
1. Nadat u de variabelen in de spreadsheet van de experimentconfiguratie hebt voltooid, sparen de veranderingen, dan sparen het dossier in lusje-afgebakende tekstformaat ( [!DNL *.txt]) gebruikend de naam die u in de parameter ExpFile in het [!DNL Sensor] configuratiedossier specificeerde. Zie [De parameter ExpFile wijzigen](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28).

   Hieronder ziet u een voorbeeld van een tekstbestand voor een testconfiguratie:

   ![](assets/testexperiment.png)

   >[!NOTE]
   >
   >Bewerk het tekstbestand voor de testconfiguratie niet handmatig, omdat dit bestand over de tabbladen moet beschikken. Als u wijzigingen in het bestand wilt aanbrengen, brengt u de wijzigingen aan in het Excel-bestand voor de experimentele configuratie en slaat u het bestand opnieuw op als een tekstbestand met tabs als scheidingsteken.

Als u begin- en stoptijden hebt gedefinieerd, is er geen reden om ooit een experiment uit het configuratiebestand van het experiment te verwijderen. Het houden van al uw experimenten die in het dossier van de experimentconfiguratie worden vermeld is eigenlijk een goede manier om een verslag van te houden hoe u elk van uw experimenten bepaalde.

## Het opstellen van het Dossier van de Configuratie en de Inhoud van de Test {#section-34ff29649f584b93bc6129b75084b37c}

U moet het dossier van de experimentconfiguratie aan elke machine in uw Webcluster opstellen die [!DNL Sensor] in werking stelt en de pagina&#39;s te dienen betrokken bij het experiment. U kunt dit doen door een handmatige procedure of uw bestaande contentbeheersysteem te gebruiken.

**Uw testinhoud implementeren**

* Op elke toepassing of webserver waarop een [!DNL Sensor] wordt uitgevoerd die pagina&#39;s bedient die bij het experiment betrokken zijn, gebruikt u het bestaande publicatieproces om de testinhoud op de juiste locatie te plaatsen.

   Als u bijvoorbeeld de testgroeppagina [!DNL index2.asp] naar de testmap voor uw website ( [!DNL mysite.com]) wilt publiceren, publiceert u het bestand naar [!DNL www.mysite.com/test].

   >[!NOTE]
   >
   >Koppel niet rechtstreeks vanuit een pagina op uw website naar een van uw testbestanden. Als u dit doet, worden de testresultaten en de indexscores ongeldig.

**Uw experiment implementeren**

* Voor elke toepassing of Webserver die een [!DNL Sensor] in werking stelt die pagina&#39;s gedienen betrokken bij het experiment, plaats het dossier van de proefconfiguratie in de folder die u in de parameter ExpFile in het [!DNL Sensor] configuratiedossier specificeerde. Zie [De parameter ExpFile wijzigen](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28).

[!DNL Sensor] selecteert willekeurig websitebezoekers voor elke groep op basis van de percentages die u in het bestand hebt gedefinieerd en dient de inhoud van de test- of controlegroep waar nodig bij hen.

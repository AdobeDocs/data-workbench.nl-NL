---
description: Als u met gegevens werkt die van websiteverkeer worden verzameld, kunt u de transformatie gebruiken Sessionize om te bepalen hoe de zittingen worden bepaald.
solution: Analytics
title: Sessionize
topic: Data workbench
uuid: c6e2487a-80e5-4e00-b4d4-2ce013fac3ea
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Sessionize{#sessionize}

Als u met gegevens werkt die van websiteverkeer worden verzameld, kunt u de transformatie gebruiken Sessionize om te bepalen hoe de zittingen worden bepaald.

De transformatie neemt als zijn input timestamp en een volgende identiteitskaart en output een zittingsaantal voor elke logboekingang. Het zittingsaantal is &quot;1&quot;voor de eerste zitting met een bepaalde volgende identiteitskaart, &quot;2&quot;voor de tweede zitting met zelfde volgende identiteitskaart, etc. De output kan direct als zittingssleutel worden gebruikt omdat het een unieke waarde voor elke zitting heeft.

>[!NOTE]
>
>Om te werken, vereist de [!DNL Sessionize] transformatie dat het gegeven in tijd wordt bevolen en door volgende identiteitskaart in uw brongegevens gegroepeerd. Daarom werkt het [!DNL Sessionize] slechts wanneer bepaald in het [!DNL Transformation.cfg] dossier of in een [!DNL Transformation Dataset Include] dossier.

<table id="table_34984DF9340149C0A5016F08EABAD158"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoertijdstempel </td> 
   <td colname="col2"> Het gebied dat de waarden van te gebruiken timestamp bevat. </td> 
   <td colname="col3"> x-timestamp </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ID Invoer volgen </td> 
   <td colname="col2"> <p>Het gebied dat de waarden van het volgen identiteitskaart bevat dat moet worden gebruikt. De waarde moet een 64 beetje (16 cijfer) of kleiner hexadecimaal aantal of een decimale gehelen van 16 cijfers of minder zijn. </p> <p> <p>Opmerking: Als u wenst om een gebied buiten x-trackingidentiteitskaart voor volgende identiteitskaart te gebruiken, moet u het gebied eerst knoeien. Zie <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-hash.md#concept-9c353923264941c3aea4428fed66d369"> Hash</a>. </p> </p> </td> 
   <td colname="col3"> x-trackingid </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Maximale duur sessie </p> </td> 
   <td colname="col2">De langste lengte van zitting vóór een nieuwe zitting is begonnen. (Dit houdt Web-pagina's die autoinhoud hebben die van het creëren van zittingen verfrissen die willekeurig lang zijn.) Als de <span class="wintitle"> Voorwaarde</span> van de Onderbreking wordt tevredengesteld en de verwijzende van een klik aan één van de ingangen in de Interne parameter van Domeinen wordt geplaatst, wordt de MaximumDuur van de Zitting gebruikt om het eind van een zitting te bepalen. Geen zitting kan langer zijn dan de gespecificeerde MaximumDuur van de Zitting ongeacht hoeveel klikken het bevat. De aanbevolen waarde is 48 uur. Voor meer informatie over de MaximumDuur van de Zitting en de Interne parameters van Domeinen, zie de Montages van de <a href="../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519"> Configuratie voor de Gegevens</a>van het Web. </td> 
   <td colname="col3"> 48 uur </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoersessienummer </td> 
   <td colname="col2"> Het gebied waarin het zittingsaantal wordt opgeslagen. Dit gebied heeft een unieke waarde voor elke zitting voor elke bezoeker. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Time-out sessie </td> 
   <td colname="col2"> <p>De hoeveelheid tijd die tussen logboekingangen van een bepaalde bezoeker moet overgaan om het eind van één zitting en het begin van een nieuwe zitting (namelijk de typische onderbreking te bepalen die wordt gebruikt om een gebruikerszitting te bepalen) te bepalen. De geadviseerde waarde van deze parameter is 30 minuten. Als de Voorwaarde van de Onderbreking niet wordt tevredengesteld en de verwijzer van een klik niet aan één van de verwijzingen in de Interne parameter van Domeinen wordt geplaatst, wordt de Onderbreking van de Zitting gebruikt om de zitting te bepalen. </p> <p> Als de Voorwaarde van de Onderbreking wordt tevredengesteld en cs (verwijzing-domein) voor een logboekingang in de lijst van interne domeinen is, dan bepaalt de MaximumDuur van de Zitting of de huidige logboekingang deel van een bestaande zitting of het begin van een nieuwe zitting uitmaakt. </p> <p> Voor meer informatie over de parameter van de Onderbreking van de Zitting, zie de Montages van de <a href="../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519"> Configuratie voor de Gegevens</a>van het Web. </p> </td> 
   <td colname="col3"> 30 minuten </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Time-out-voorwaarde </td> 
   <td colname="col2"> De voorwaarde die voor een logboekingang moet worden voldaan om als begin van een nieuwe zitting te worden beschouwd. Merk op dat de hoeveelheid tijd die tussen de logboekingang en de vorige logboekingang overgaat minstens de waarde van de parameter van de Onderbreking van de Zitting moet zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Een nieuwe zitting begint wanneer om het even welke volgende situaties voorkomt:

* De volgende identiteitskaart verandert.
* De tijd sinds de laatste logboekingang is minstens gelijk aan de waarde van de parameter van de Onderbreking van de Zitting en de Voorwaarde van de Onderbreking wordt tevredengesteld.
* De tijd sinds de eerste logboekingang van de laatste zitting overschrijdt de waarde van de Maximum parameter van de Duur van de Zitting.

>[!NOTE]
>
>Als u reeds de MaximumDuur van de Zitting en Onderbreking van de Zitting als parameters in het [!DNL Session Parameters.cfg] dossier hebt bepaald, ga geen waarden voor hen in de configuratie in. U kunt de parameters van verwijzingen voorzien door *$ (parameternaam)* te typen zoals aangetoond in het volgende voorbeeld. Voor meer informatie over deze parameters, zie de Montages van de [Configuratie voor de Gegevens](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)van het Web.

De [!DNL Sessionize] transformatie in dit voorbeeld neemt als input de x-timestamp en x-trackingid gebieden en registreert het zittingsaantal voor elke logboekingang op het x-zitting-zeer belangrijke gebied. De transformatie [!DNL Timeout Condition] is gebaseerd op een [!DNL Neither] voorwaarde: Als het cs (verwijzing-domein) gebied voor een logboekingang een lid van de Interne parameter van Domeinen aanpast, evalueert de voorwaarde aan vals. Neem nota van de verwijzingen naar de Interne Domeinen en parameters van de Onderbreking van de Zitting.

Voor informatie over [!DNL NeitherCondition], zie [Voorwaarden](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md). Voor informatie over de Interne Domeinen en parameters van de Onderbreking van de Zitting, zie de Montages van de [Configuratie voor de Gegevens](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519)van het Web.

![](assets/cfg_TransformationType_Sessionize.png)


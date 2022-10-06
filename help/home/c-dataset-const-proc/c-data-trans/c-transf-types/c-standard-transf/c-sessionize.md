---
description: Als u werkt met gegevens die zijn verzameld uit websiteverkeer, kunt u met de transformatie Sessioneren bepalen hoe sessies worden gedefinieerd.
title: Sessioneren
uuid: c6e2487a-80e5-4e00-b4d4-2ce013fac3ea
exl-id: bb25cb4b-7185-4524-8ff5-740b672e1cd9
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---

# Sessioneren{#sessionize}

{{eol}}

Als u werkt met gegevens die zijn verzameld uit websiteverkeer, kunt u met de transformatie Sessioneren bepalen hoe sessies worden gedefinieerd.

De transformatie neemt als invoer een tijdstempel en een trackingsidentiteitskaart en voert een zittingsaantal voor elke logboekingang uit. Het sessienummer is &quot;1&quot; voor de eerste sessie met een bepaalde id voor bijhouden, &quot;2&quot; voor de tweede sessie met dezelfde id, enzovoort. De uitvoer kan rechtstreeks als een sessiesleutel worden gebruikt, omdat deze voor elke sessie een unieke waarde heeft.

>[!NOTE]
>
>Om te werken, [!DNL Sessionize] voor transformatie moeten de gegevens in de tijd worden geordend en met de tracking-id in de brongegevens worden gegroepeerd. Daarom [!DNL Sessionize] werkt alleen wanneer deze zijn gedefinieerd in het dialoogvenster [!DNL Transformation.cfg] of in een [!DNL Transformation Dataset Include] bestand.

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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Tijdstempel invoeren </td> 
   <td colname="col2"> Het veld met de waarden van de te gebruiken tijdstempel. </td> 
   <td colname="col3"> x-timestamp </td> 
  </tr> 
  <tr> 
   <td colname="col1"> ID Invoer bijhouden </td> 
   <td colname="col2"> <p>Het veld met de waarden van de te gebruiken tracking-id. De waarde moet een 64-bits (16 cijfers) of kleiner hexadecimaal getal of een decimaal geheel getal van 16 cijfers of minder zijn. </p> <p> <p>Opmerking: Als u een ander veld dan x-trackingid wilt gebruiken voor de id voor bijhouden, moet u het veld eerst hashen. Zie <a href="../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-hash.md#concept-9c353923264941c3aea4428fed66d369"> Hash</a>. </p> </p> </td> 
   <td colname="col3"> x-trackingid </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Maximale sessieduur </p> </td> 
   <td colname="col2">De langste duur van de sessie voordat een nieuwe sessie wordt gestart. (Zo blijven webpagina's waarvan de inhoud automatisch wordt vernieuwd, bestaan uit het maken van sessies die willekeurig lang zijn.) Als de <span class="wintitle"> Time-outvoorwaarde</span> is tevreden en de referentie van een klik wordt geplaatst aan één van de ingangen in de Interne parameter van Domeinen, wordt de Maximale Duur van de Zitting gebruikt om het eind van een zitting te bepalen. Geen enkele sessie kan langer zijn dan de opgegeven maximale sessieduur, ongeacht het aantal klikken dat deze bevat. De aanbevolen waarde is 48 uur. Voor meer informatie over de Maximale duur van de Zitting en de Interne parameters van Domeinen, zie <a href="../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519"> Configuratie-instellingen voor webgegevens</a>. </td> 
   <td colname="col3"> 48 uur </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoersessienummer </td> 
   <td colname="col2"> Het veld waarin het sessienummer wordt opgeslagen. Dit veld heeft een unieke waarde voor elke sessie voor elke bezoeker. </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Time-out sessie </td> 
   <td colname="col2"> <p>De hoeveelheid tijd die tussen logboekingangen van een bepaalde bezoeker moet overgaan om het eind van één zitting en het begin van een nieuwe zitting te bepalen (namelijk de typische onderbreking die wordt gebruikt om een gebruikerszitting te bepalen). De aanbevolen waarde van deze parameter is 30 minuten. Als de timeout-voorwaarde niet wordt vervuld en de referentie van een klik niet is ingesteld op een van de referenties in de parameter Internal Domains, wordt de Session Timeout gebruikt om de sessie te definiëren. </p> <p> Als de Voorwaarde van de Onderbreking wordt tevredengesteld en cs (verwijzing-domein) voor een logboekingang in de lijst van interne domeinen is, dan bepaalt de Maximale Duur van de Zitting of de huidige logboekingang deel van een bestaande zitting of de aanvang van een nieuwe zitting uitmaakt. </p> <p> Voor meer informatie over de parameter van de Onderbreking van de Zitting, zie <a href="../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519"> Configuratie-instellingen voor webgegevens</a>. </p> </td> 
   <td colname="col3"> 30 minuten </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Time-outvoorwaarde </td> 
   <td colname="col2"> De voorwaarde die voor een logboekingang moet worden voldaan om als begin van een nieuwe zitting te worden beschouwd. Merk op dat de hoeveelheid tijd die tussen de logboekingang en de vorige logboekingang overgaat minstens de waarde van de parameter van de Onderbreking van de Zitting moet zijn. </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Een nieuwe sessie begint wanneer een van de volgende situaties zich voordoet:

* De id voor bijhouden wordt gewijzigd.
* De tijd sinds de laatste logboekingang is minstens gelijk aan de waarde van de parameter van de Onderbreking van de Zitting en de Voorwaarde van de Onderbreking wordt voldaan.
* De tijd sinds de eerste logboekingang van de laatste zitting overschrijdt de waarde van de Maximale parameter van de Duur van de Zitting.

>[!NOTE]
>
>Als u de maximale sessieduur en sessietime-out al hebt gedefinieerd als parameters in het dialoogvenster [!DNL Session Parameters.cfg] geen waarden voor de bestanden in de configuratie. U kunt naar de parameters verwijzen door te typen *$(parameternaam)* zoals getoond in het volgende voorbeeld. Zie voor meer informatie over deze parameters [Configuratie-instellingen voor webgegevens](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

De [!DNL Sessionize] De transformatie in dit voorbeeld neemt als input de x-timestamp en x-trackingid gebieden en registreert het zittingsaantal voor elke logboekingang in het x-session-zeer belangrijke gebied. De transformaties [!DNL Timeout Condition] is gebaseerd op een [!DNL Neither] voorwaarde: Als het veld cs(reference-domain) voor een logbestandvermelding overeenkomt met een lid van de parameter Internal Domains, levert de voorwaarde false op. Neem nota van de verwijzingen naar de Interne Domeinen en parameters van de Onderbreking van de Zitting.

Voor informatie over de [!DNL NeitherCondition], zie [Voorwaarden](../../../../../home/c-dataset-const-proc/c-conditions/c-abt-cond.md). Voor informatie over de interne parameters van Domeinen en van de Onderbreking van de Zitting, zie [Configuratie-instellingen voor webgegevens](../../../../../home/c-dataset-const-proc/c-config-web-data/c-config-web-data.md#concept-9a306b65483a484bb3f6f3c1d7e77519).

![](assets/cfg_TransformationType_Sessionize.png)

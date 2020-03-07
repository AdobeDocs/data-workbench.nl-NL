---
description: U bepaalt nieuwe metriek (die als afgeleide metriek wordt bedoeld) en geeft bestaande metrische definities uit gebruikend de Metrische Redacteur.
solution: Analytics
title: Werk met afgeleide metriek
topic: Data workbench
uuid: 9767c170-e0cb-47b4-94f1-e9f6950b5926
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Werk met afgeleide metriek{#work-with-derived-metrics}

U bepaalt nieuwe metriek (die als afgeleide metriek wordt bedoeld) en geeft bestaande metrische definities uit gebruikend de Metrische Redacteur.

Voor meer informatie over metriek dan in deze sectie en in de Syntaxis [van de Taal van de](../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f)Vraag wordt verstrekt, zie de Gids *van de* Metrische, Afmetingen, en van Filters.

## Creeer afgeleide metrisch {#section-d57b98bf0a9940daba4920ff7efc808d}

U gebruikt een [!DNL Metric Editor] om nieuwe metrisch door naam, formule, en formaat te bepalen, die aan de omslag van de Metriek \*profile_name* \ van de Gebruiker voor recenter gebruik wordt opgeslagen.

1. Open een nieuw [!DNL Metric Editor] gebruikend de **[!UICONTROL Admin]** > **[!UICONTROL Profile]** menuoptie of door de **[!UICONTROL User]** kolom voor de omslag met de rechtermuisknop aan te klikken waarin u metrisch wilt tot stand brengen en **[!UICONTROL Create]** > klikken **[!UICONTROL New Metric]**.

   Een [!DNL Metric Editor] scherm.

1. In de parameter van de Naam, typ een naam voor nieuwe metrisch.

   Merk op dat de ruimten () worden toegestaan terwijl de onderstreepingen (_) niet zijn. Bovendien kunt u niet de volgende symbolen gebruiken:

   `+ - * /`

   ![](assets/vis_MetricEditor_NewAndEditing.png)

1. In de parameter van de Formule, typ een uitdrukking voor nieuwe metrisch. Merk op dat de filters binnen haakjes moeten worden bepaald [ ] in de uitdrukking.

   Voor de extra metrische regels van de uitdrukkingssyntaxis, zie [Syntaxis voor Metrische Uitdrukkingen](../../../../home/c-get-started/c-qry-lang-syntx/c-syntx-mtrc-exp.md#concept-bbf440a0307549e088df491b51b51d66).

   De volgende lijst verstrekt steekproefuitdrukkingen voor uitgebreide metriek.

   <table id="table_ED77997FC08F492490DCAC3C4153781C"> 
   <thead> 
   <tr> 
      <th colname="col1" class="entry"> Uitgebreide metrische naam </th> 
      <th colname="col2" class="entry"> Uitdrukking </th> 
   </tr>
   </thead>
   <tbody> 
   <tr> 
      <td colname="col1"> <p>Percentage eerste sessies </p> </td> 
      <td colname="col2"> <p><span class="filepath"> Sessies [Session_Number="1"]/Sessies</span> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Eerste sessies conversie </p> </td> 
      <td colname="col2"> <p><span class="filepath"> Omzetting [Session_Number="1"]</span> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Gemiddelde waarde per bezoeker </p> </td> 
      <td colname="col2"> <p><span class="filepath"> Waarde/bezoekers</span> </p> </td> 
   </tr> 
   </tbody> 
   </table>

   >[!NOTE]
   >
   >Wanneer een aangewezen uitdrukking is ingegaan, toont de voorproeflijn de waarde van nieuwe metrisch. Als er een fout in de uitdrukking is, toont de voorproeflijn een foutenmelding.

1. Klik met de rechtermuisknop **[!UICONTROL (New)]** en klik op **[!UICONTROL Save]**.

   Wanneer u sparen metrisch, wordt een dossier dat nieuwe metrisch vertegenwoordigt gecreeerd op uw computer in de folder van de Installatie van de Werkbank van Gegevens \User\*profiel naam* \ de omslag van Metriek.

   ![](assets/vis_MetricEditor_NewAndEditing.png)

U kunt nieuwe metrisch door het huidige profiel nu gebruiken door het te selecteren aangezien u om het even welke ingebouwd metrisch zou zijn. Om de orde te veranderen waarin uw metriek op het metriekmenu verschijnen, zie het [Aanpassen van Menu&#39;s Gebruikend de Dossiers](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999)van Order.txt.

Als u alle gebruikers van het profiel zou willen metrisch gebruiken die u creeerde, moet u het aan het werkende profiel publiceren gebruikend [!DNL Profile Manager]. Zie Bestanden [publiceren in uw werkprofiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).

## Geef een afgeleide metriek uit {#section-db6d924cf4e14bcc8d57cfe1059fc797}

1. In [!DNL Profile Manager] of [!DNL Metrics Manager], in de kolom van de *profielnaam* , klik het vinkje voor het metrische dossier met de rechtermuisknop aan dat u wilt uitgeven, dan klikken **[!UICONTROL Make Local]**.
1. Klik het vinkje voor het metrische dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.

   >[!NOTE]
   >
   >U kunt ook een openen [!DNL Metric Editor] door om het even welk metrisch-verwant gebied binnen een visualisatie met de rechtermuisknop aan te klikken om het metrische menu te tonen. Voor meer informatie, zie het [Werken met de Menu&#39;s van de Metrische en van de Dimensie](../../../../home/c-get-started/c-vis/c-met-dim-menus.md#concept-50f07ae47c3e4f94ad7d3d7f8293ccac).

1. In [!DNL Metric Editor], geef en bewaar zonodig de metrische definitie uit gebruikend Stappen 2-4 in het [Creëren van Nieuwe Voortgekomen Metriek](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#section-d57b98bf0a9940daba4920ff7efc808d).

   Als u alle gebruikers van het profiel zou willen metrisch gebruiken die u uitgeeft, moet u het aan het het werk profiel publiceren gebruikend [!DNL Profile Manager]. Zie Bestanden [publiceren in uw werkprofiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).


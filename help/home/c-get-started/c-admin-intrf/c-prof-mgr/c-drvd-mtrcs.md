---
description: U bepaalt nieuwe metriek (die als afgeleide metriek wordt bedoeld) en geeft bestaande metrische definities uit gebruikend de Metrische Redacteur.
title: Werken met afgeleide metriek
uuid: 9767c170-e0cb-47b4-94f1-e9f6950b5926
exl-id: 83467c64-4b9a-44ab-91a2-202c76c89979
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Werken met afgeleide metriek{#work-with-derived-metrics}

{{eol}}

U bepaalt nieuwe metriek (die als afgeleide metriek wordt bedoeld) en geeft bestaande metrische definities uit gebruikend de Metrische Redacteur.

Voor meer informatie over metriek dan in deze sectie en in wordt verstrekt [Syntaxis zoektaal](../../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f), zie de *Handleiding Metrisch, Dimension en Filters*.

## Een afgeleide metrische waarde maken {#section-d57b98bf0a9940daba4920ff7efc808d}

U gebruikt een [!DNL Metric Editor] om een nieuwe metrische waarde op naam, formule, en formaat te bepalen, die aan de omslag van Gebruiker \*profile_name* \ Metrics voor later gebruik wordt bewaard.

1. Een nieuwe [!DNL Metric Editor] met de **[!UICONTROL Admin]** > **[!UICONTROL Profile]** of door met de rechtermuisknop op de knop **[!UICONTROL User]** kolom voor de map waarin u metrisch wilt maken en op **[!UICONTROL Create]** > **[!UICONTROL New Metric]**.

   A [!DNL Metric Editor] worden weergegeven.

1. Typ een naam voor de nieuwe metrische waarde in de parameter Naam.

   Spaties ( ) zijn toegestaan terwijl onderstrepingstekens (_) dat niet doen. Bovendien kunt u de volgende symbolen niet gebruiken:

   `+ - * /`

   ![](assets/vis_MetricEditor_NewAndEditing.png)

1. Typ in de parameter Formule een expressie voor de nieuwe metrische waarde. Filters moeten tussen haakjes worden gedefinieerd [ ] in de expressie.

   Voor extra metrische regels van de uitdrukkingssyntaxis, zie [Syntaxis voor metrische expressies](../../../../home/c-get-started/c-qry-lang-syntx/c-syntx-mtrc-exp.md#concept-bbf440a0307549e088df491b51b51d66).

   De volgende tabel bevat voorbeeldexpressies voor uitgebreide metriek.

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
      <td colname="col1"> <p>Conversie eerste sessies </p> </td> 
      <td colname="col2"> <p><span class="filepath"> Conversie [Session_Number="1"]</span> </p> </td> 
   </tr> 
   <tr> 
      <td colname="col1"> <p>Gemiddelde waarde per bezoeker </p> </td> 
      <td colname="col2"> <p><span class="filepath"> Waarde/bezoekers</span> </p> </td> 
   </tr> 
   </tbody> 
   </table>

   >[!NOTE]
   >
   >Wanneer een aangewezen uitdrukking is ingegaan, toont de voorproeflijn de waarde van nieuwe metrisch. Als de expressie een fout bevat, wordt een foutbericht weergegeven in de voorbeeldregel.

1. Klikken met rechtermuisknop **[!UICONTROL (New)]** en klik op **[!UICONTROL Save]**.

   Wanneer u de metrische gegevens opslaat, wordt op uw computer een bestand met de nieuwe metrische waarde gemaakt in de map Data Workbench Installation \User\*profile name*\Metrics.

   ![](assets/vis_MetricEditor_NewAndEditing.png)

U kunt nu nieuwe metrisch door het huidige profiel te selecteren zoals u om het even welke ingebouwde metrisch zou gebruiken. Als u de volgorde wilt wijzigen waarin de metriek in het menu Metriek wordt weergegeven, raadpleegt u [Menu&#39;s aanpassen met Order.txt-bestanden](../../../../home/c-get-started/c-intf-anlys-ftrs/c-ctm-menus/t-cstm-menus-ordr-files.md#task-a391800a8dd444deb3e1516d5189f999).

Als u wilt dat alle gebruikers van het profiel de maateenheid gebruiken die u hebt gemaakt, moet u deze naar het werkprofiel publiceren met het gereedschap [!DNL Profile Manager]. Zie [Bestanden publiceren naar uw werkprofiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).

## Een afgeleide metriek bewerken {#section-db6d924cf4e14bcc8d57cfe1059fc797}

1. In de [!DNL Profile Manager] of [!DNL Metrics Manager]in de *profielnaam* kolom, klikt u met de rechtermuisknop op het vinkje voor het metrische bestand dat u wilt bewerken en klikt u vervolgens op **[!UICONTROL Make Local]**.
1. Klik met de rechtermuisknop op het vinkje voor het metrische bestand in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.

   >[!NOTE]
   >
   >U kunt ook een [!DNL Metric Editor] door met de rechtermuisknop te klikken op een willekeurig metrisch gebied binnen een visualisatie om het metrische menu weer te geven. Zie voor meer informatie [Werken met metrische en Dimension-menu&#39;s](../../../../home/c-get-started/c-vis/c-met-dim-menus.md#concept-50f07ae47c3e4f94ad7d3d7f8293ccac).

1. In de [!DNL Metric Editor]Bewerk en sla de metrische definitie indien nodig op met Stap 2-4 in [Nieuwe afgeleide metriek maken](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-drvd-mtrcs.md#section-d57b98bf0a9940daba4920ff7efc808d).

   Als u wilt dat alle gebruikers van het profiel de metrische waarde gebruiken die u hebt bewerkt, moet u deze naar het werkprofiel publiceren met de opdracht [!DNL Profile Manager]. Zie [Bestanden publiceren naar uw werkprofiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).

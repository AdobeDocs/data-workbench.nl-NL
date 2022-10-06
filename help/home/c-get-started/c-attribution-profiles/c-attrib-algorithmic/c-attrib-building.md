---
description: Open kenmerk Best Fit in het menu Premium en voer de volgende stappen uit om een model voor kenmerk Best Fit te maken.
title: Een passend kenmerkmodel maken
uuid: d1fd0340-1917-41bc-9a08-e78a79d084e7
exl-id: e0a42374-2500-46a3-a72a-708ab2d228db
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Een passend kenmerkmodel maken{#build-a-best-fit-attribution-model}

{{eol}}

Open kenmerk Best Fit in het menu Premium en voer de volgende stappen uit om een model voor kenmerk Best Fit te maken.

Een overzicht bekijken van [Kenmerk best passend](../../../../home/c-get-started/c-attribution-profiles/c-attrib-algorithmic/c-attrib-algorithmic.md#concept-237feb6e9c4d49efaf75399297dcb9d1).

1. Openen **Kenmerk best passend**.

   Een werkruimte openen en klikken **[!UICONTROL Premium]** > **[!UICONTROL Best Fit Attribution]**.

   ![](assets/attrib_windows_launch.png)

   >[!NOTE]
   >
   >De kenmerk Best Fit is een Adobe Analytics Premium-functie waarvoor u Premium in uw profiel moet inschakelen. Hiervoor moet u uw certificaat bijwerken en het Premium-profiel toevoegen aan het bestand profile.cfg. Zie [Upgrade van DWB-server: 6.2 t/m 6.3](/help/home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-6-2-to-6-3-upgrade.md) voor DWB 6.3.

1. Stel de **[!UICONTROL Success]** metrisch.

   >[!NOTE]
   >
   >U kunt metrisch slepen vanuit een **[!UICONTROL Finder]** aan de linkerruit van de visualisatie van de Attributie, of selecteer van **Invoer** -menu.

   Klik op **[!UICONTROL Inputs]** > **[!UICONTROL Set Success]**. Het menu Metrisch wordt geopend. ![](assets/attrib_set_success_metric.png)

   Selecteer metrisch die een succesvolle omzetting identificeert.

1. (optioneel) Stel de **Ontvangsten** metrisch.

   Plaats metrisch om opbrengst over het omzettingsproces te evalueren.

1. Stel de **Aanraken** metrisch.

   >[!NOTE]
   >
   >Het instellen van een aanraakmetrisch is alleen vereist als u cijfers voor succes automatisch probeert te maken door dimensie-elementen naar de visualisatie te slepen.

   Klik op de knop **[!UICONTROL Inputs]** en selecteert u **Aanraken instellen** of sleep een metrische waarde uit de Finder. ![](assets/attrib_set_touch.png)

   Dit zal worden gebruikt om kanaalmetriek af te leiden wanneer de afmetingselementen als input worden gebruikt.

1. Een **Succes** venster.

   Klik op [!DNL Inputs > Success Window]. Selecteer een datumbereik in een tabel en geef het venster Succes een naam. Klikken **[!UICONTROL Workspace Selection]** en de geselecteerde datums worden toegewezen als het tijdbereik voor de metrische waarde Succes.

   ![](assets/attrib_set_success_window.png)

   >[!NOTE]
   >
   >Aangezien het venster van het Succes een werkstationselectie is, kunt u om het even welke afmeting(en) aan uw venster van het Succes omvatten.

1. Een **[!UICONTROL Touch Window]**.

   Klik op [!DNL Inputs > Touch Window]. Selecteer een datumbereik in een tabel en geef het venster Touch een naam. Klikken **[!UICONTROL Workspace Selection]** en de geselecteerde datums worden toegewezen als het tijdbereik voor de metrische waarde Succes.

   ![](assets/attrib_set_touch_window.png)

   Standaard worden de **Aanraken** wordt ingesteld op dezelfde periode als de periode **[!UICONTROL Success]** venster.

1. (optioneel) Stel een trainingsfilter in.

   U kunt ook een **Trainingsfilter** in de werkruimte om bezoekersgegevens te filteren.

   >[!NOTE]
   >
   >Bij het instellen van zowel het venster Succes als het venster Touch kunt u het filter Training toepassen op de selecties van de huidige werkruimte om uw gegevens verder te beperken.

   ![](assets/attrib_filter.png)

   >[!NOTE]
   >
   >De trainingsset is altijd afkomstig van bezoekers die aan het venster Succes voldoen. Door te filteren met de Filtereditor kunt u een subset bezoekers maken die in het venster Succes wordt gerapporteerd.

1. Geef kanaalmetriek op die touches vertegenwoordigen.

   Sleep metrische gegevens naar de visualisatie of kies ze in het menu [!DNL Inputs] > [!DNL Add Channel] -menu. Als u nog geen metriek hebt die voor campagnes of kanalen wordt bepaald, maar afmetingen die kanalen vertegenwoordigen hebben, kan visualisatie hen voor u automatisch met de specificatie van metrisch van de Aanraking bouwen.

   Als de aanraakmethode bijvoorbeeld is ingesteld op [!DNL Hits]en een [!DNL dimension] gebeld [!DNL Media Type] met elementen die dingen als [!DNL Email], [!DNL Press Release], [!DNL Print Ad], en [!DNL Social Media]resulteert de visualisatie in Kanaalwaarden van het formulier [!DNL Hits where Media Type = Email] wanneer u het element of de elementen naar de visualisatie sleept.

1. Druk **Ga**.

   Het Best Fit Analysis-proces wordt uitgevoerd en een grafiek geeft de toewijzingen per kanaal weer op basis van de geselecteerde invoer.

   >[!NOTE]
   >
   >Klikken met rechtermuisknop **Model voltooid** over de voltooide analyse om statistieken voor het toerekeningsmodel te bekijken.

   ![](assets/attrib_visualization.png)

Na voltooiing wordt in een grafiek een per kanaal berekend toewijzingsmodel en een verdeling van de *Ontvangsten* metrisch (indien ingesteld). Het model kan intern worden opgeslagen of naar andere systemen worden geëxporteerd.

>[!NOTE]
>
>**[!UICONTROL Streaming]**, **[!UICONTROL Online]** en **[!UICONTROL Offline]** modi produceren verschillende effecten bij het maken van een toewijzingsmodel op basis van de latentie van de gegevens die worden geëvalueerd. In de modus Streaming worden de details **[!UICONTROL Model Complete]** bericht wordt weergegeven. In de modi Online en Offline worden de details weergegeven **[!UICONTROL Local Model Complete]** wordt weergegeven.

## Menu Opties {#section-22288867f6c8483a8a38410f4b948346}

De **Opties** biedt geavanceerde functies voor het instellen en weergeven van de analyse Aanpassen aan beste kenmerken.

<table id="table_8F6F517B7DBF4259814BEC6D07A72EAC">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Menu Opties </th>
   <th colname="col2" class="entry"> Beschrijving </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="uicontrol"> Trainingsfilter instellen </span> </td>
   <td colname="col2"> Het trainingsfilter wordt samen met het venster Succes gebruikt om de populatie te filteren bij het maken van het toewijzingsmodel. Dit levert een subset gegevens op die alleen de bezoekers bevat die u wilt analyseren. <p>Opmerking: Ervaren gebruikers kunnen ook gebruikmaken van de flexibiliteit van filters om zich na de tijdlijn van het venster Succes en Touch Windows te concentreren. U kunt bijvoorbeeld niet alleen een tijdbereik selecteren, maar ook een set <i>Refererende domeinen</i> alleen de toewijzing voor gebruikers uit die domeinen te onderzoeken. </p> </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> Omschrijving complex filter tonen </span> </td>
   <td colname="col2"> Hiermee geeft u de filtercode weer voor Trainingsfilter, Venster Voltooien en Venster aanraken. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> Model opslaan </span> </td>
   <td colname="col2"> Hiermee slaat u het huidige toewijzingsmodel op voor toekomstig gebruik. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> Model laden </span> </td>
   <td colname="col2"> Opent een eerder opgeslagen attributiemodel. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> Presentatieweergave </span> </td>
   <td colname="col2"> Hiermee verbergt u de bovenste menubalk voor de presentatie. </td>
  </tr>
  <tr>
   <td colname="col1"> <p><b>Opties &gt; Geavanceerd</b> bevat functies om de omvang van de trainingsset in te stellen en de aanpak te specificeren die moet worden gevolgd bij een onbalans tussen klassen. </p> </td>
   <td colname="col2"> </td>
  </tr>
  <tr>
   <td colname="col1"><span class="uicontrol"> Geavanceerd &gt; Formaat trainingsset </span> </td>
   <td colname="col2"> <p>Hiermee stelt u de grootte van de trainingsset in. </p> <p>Opmerking: De standaardtrainingsgrootte is Groot voor 250.000 bezoekers. </p>
    <ul id="ul_5F17C60227C34A85A2C476A32F2B5DCD">
     <li id="li_A076FC2AD0214ADDBFCFD82AEA5F0880">Tiny = 50.000 </li>
     <li id="li_17E77E01D5374068BEBC80B3AD4CCD41">Klein = 75.000 </li>
     <li id="li_7F6B4834742A4BFCBC3DB214425B88C3">Normaal = 100,000 </li>
     <li id="li_0BB7F791603745028CFC661EBC94D8B4">Groot = 250,00 </li>
     <li id="li_34B60233C84F48F1BCB8040C5195411A">Groot = 500.000 </li>
    </ul> </td>
  </tr>
  <tr>
   <td colname="col1"><b>Geavanceerd &gt; Klassebalans </b> </td>
   <td colname="col2"> <p>Identificeert en bepaalt het aantal inputverslagen voor een kwestie van de klassenonbalans te produceren die op de grootte van dataset wordt gebaseerd. </p> </td>
  </tr>
 </tbody>
</table>

| Opties voor Opnieuw instellen en verwijderen | Beschrijving |
|---|---|
| **[!UICONTROL Reset Model]** | Van de **[!UICONTROL Reset]** menu, selecteert u **[!UICONTROL Reset Model]** om de visualisatie te wissen, maar invoermeetgegevens te behouden. |
| **[!UICONTROL Reset All]** | Van de **[!UICONTROL Reset]** menu, selecteert u **[!UICONTROL Reset All]** om de visualisatie en invoermeetgegevens te wissen. |
| **[!UICONTROL Remove]** | Klik met de rechtermuisknop op een willekeurige invoer en selecteer **[!UICONTROL Remove]** om de metrische waarde uit de geselecteerde invoer te verwijderen. |
| **[!UICONTROL Remove All]** | Klikken met rechtermuisknop aan op *Kanalen* en selecteert u **[!UICONTROL Remove All]** om alle invoermeetgegevens te wissen. |

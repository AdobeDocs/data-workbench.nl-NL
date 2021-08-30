---
description: Met de exportfunctie van Customer Record Service (CRS) kunt u gegevens van Data Workbench exporteren naar de Adobe Analytics Core Services om deze te integreren met de mogelijkheden van andere Analytics, waaronder Rapporten en Analytics.
title: Exporteren naar Analytics Core Services
uuid: 8fd7e8d8-989a-4ad6-bab5-61bfd37b0201
exl-id: 573085e8-2260-4872-be90-a84ad61145bb
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Exporteren naar Analytics Core Services{#exporting-to-analytics-core-services}

Met de exportfunctie van Customer Record Service (CRS) kunt u gegevens van Data Workbench exporteren naar de Adobe Analytics Core Services om deze te integreren met de mogelijkheden van andere Analytics, waaronder Rapporten en Analytics.

>[!NOTE]
>
>De exportfunctie van CRS werkt alleen als de analyse-id van een bezoeker is gebaseerd op de Experience Cloud ID-service (ECID). Hoewel ECID in Data Workbench kan worden ingevuld voor een bezoeker, werkt de CRS-export niet voor die bezoeker als de client zich in de respijtperiode bevindt of als het cookie van de bezoeker niet is vervangen door ECID. Zie [Bezoekers identificeren](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-visid.html) en [ID Service Grace Period](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/grace-period.html) voor meer informatie.

Van **Detail Lijst** (klik **[!UICONTROL Tools]** > **[!UICONTROL Detail Table]** in een werkruimte met de rechtermuisknop aan), kunt u attributenwaarden en de variabelen plaatsen die worden vereist om met de Rapporten &amp; Analytics van de Analytics (gebruikend de Diensten van de Pijpleiding van Adobe te integreren).

1. **Klik met de rechtermuisknop op de tabelkoptekst en klik op Nieuwe service voor klantrecord.**

   ![](assets/6_4_CRS.png)

1. **Geef het exportbestand een naam en sla het op.**

   Het bewerkingsvenster voor het exportbestand wordt geopend.

1. **** **OpenQuery > CRS Configuration**.
1. **Klik met de rechtermuisknop op CRS-kenmerken > Nieuw toevoegen.**
1. **** ***EnterCRS-*** **parameters**.

   Open de nieuwe ingang en ga of verifieer waarden in de *sectie van de Attributen van CRS* van het de uitvoerdossier in:

   ![](assets/6_4_CRS1.png)

   <table id="table_8156A2C66C0E41D381C31F1082CCA479"> 
    <tbody> 
      <tr> 
      <td colname="col1"> <p><b>Kenmerknaam</b> </p> </td> 
      <td colname="col2">Naam van de <i>Klantkenmerken</i> variabele weergegeven in <i>Rapporten &amp; Analytics</i>. </td> 
      </tr> 
      <tr> 
      <td colname="col1"><b>Type kenmerk</b> </td> 
      <td colname="col2"> <p>Deze parameter accepteert waarden van (<i>int</i>, <i>string</i>). </p> <p>Opmerking: Als een attribuut <b>not</b> geabonneerd aan in Analytics is: <p> 
      <ul id="ul_B77BF6FDA3FB4F1BBF9380C2FD938270"> 
       <li id="li_3D099456AF6B4103B227D841C81AB936">Het kenmerk wordt gemaakt met elk geldig kenmerktype dat door Analytics wordt ondersteund (in deze versie is het alleen beperkt tot <i>string</i> en <i>int</i>). </li> 
       <li id="li_EA1DBDB2E6BE49278C6CD6A5503EDC8A">Als een ongeldig kenmerktype is ingevoerd, wordt een fout weergegeven die aangeeft dat er geen abonnement is genomen op Analytics. </li> 
      </ul> </p> <p>Als een attribuut <b>reeds</b> geabonneerd aan in Analytics is: </p> <p> 
      <ul id="ul_16415B639F1C49A5AE9932C128184171"> 
       <li id="li_83C90D44FE5C4D979DEA786660C7F3EC">Zorg ervoor dat u het juiste kenmerktype opgeeft voor het kenmerk dat al is geabonneerd op kenmerk. </li> 
       <li id="li_02C5024E335C4C59B4F7B0084232CC24">Als u het verkeerde type voor de attributen ingaat, dan zal zijn gedrag afhankelijk van de behandeling van Analytics van attributentypes zijn. </li> 
      </ul> </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p><b>Veldnaam</b> </p> </td> 
      <td colname="col2">Naam van de afmeting of metrische waarde waarvan de kenmerkwaarden worden geselecteerd. <p>Opmerking: De <i><b>Veldnaam</b></i> onder <i>CRS-kenmerken</i> moet hetzelfde zijn als de <b><i>Uitvoervelden</i> &gt; <i>Veldnaam</i></b> (die automatisch wordt ingevuld op basis van het geselecteerde kenmerk). Als <i>Veldnaam</i> ongeldig is, wordt het exporteren niet uitgevoerd. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Klik met de rechtermuisknop **[!UICONTROL Report Suite]** > **[!UICONTROL Add New]**.
1. Voer de **[!UICONTROL Report Suite ID]** in.

   Open de nieuwe ingang en ga of verifieer waarden in *de sectie van de Reeks* van het de uitvoerdossier in:

   <table id="table_A3279CADB74C441DA2E062E2123CE9D4"> 
    <tbody> 
      <tr> 
      <td colname="col1"><b>Rapportsuite</b> </td> 
      <td colname="col2">Id van de rapportsuite in <i>Rapporten &amp; Analytics</i> ter identificatie van de <i>Kenmerk van klant</i> variabelen die worden geëxporteerd. <p> <p>Opmerking: Hoewel u <i>Rapporten &amp; Analytics</i> aan veelvoudige rapportreeksen kunt toevoegen, zal Data Workbench 6.4 slechts één enkele rapportreeks uitvoeren die bij <i>index 0</i> wordt geïdentificeerd. <p>De waarde van de rapportsuite die u in dit veld invoert, is de id van de rapportsuite (en niet de naam van de rapportsuite). </p> </p> </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Voer de parameter ECID-veld in.

   **ECID-veld**: Naam van de dimensie in uw profiel die de Adobe Experience Cloud-id vertegenwoordigt. Dit is een verplicht veld en eventuele ongeldige waarde voor afmetingen wordt niet geëxporteerd.

1. (optioneel) Vul de parameter Veld bezoeker-id in.

   **Veld** bezoekersidentiteitskaart: Als de gebruiker een andere aangepaste id voor een bezoeker in zijn of haar gegevens wil verzenden, voert de gebruiker de naam van de dimensie in die de aangepaste bezoeker-id vertegenwoordigt. Dit is een optioneel veld dat leeg kan worden gelaten.

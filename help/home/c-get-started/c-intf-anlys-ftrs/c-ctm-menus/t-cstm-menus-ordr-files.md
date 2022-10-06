---
description: U kunt de weergave van elk menu aanpassen door het bestand order.txt te bewerken dat aan dat menu is gekoppeld.
title: Een menu aanpassen met de bestanden order.txt
uuid: 4346114a-05d0-4d15-9633-09c9d869cdd6
exl-id: 3803a56f-19b7-4792-a277-97f76c11ec0e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# Een menu aanpassen met de bestanden order.txt{#customize-a-menu-using-order-txt-files}

{{eol}}

U kunt de weergave van elk menu aanpassen door het bestand order.txt te bewerken dat aan dat menu is gekoppeld.

De stappen in deze sectie zijn van toepassing op alle typen menu&#39;s.

**Het bestand order.txt bewerken om een menu aan te passen**

1. In de [!DNL Profile Manager]in de *profielnaam* kolom, klikt u met de rechtermuisknop op het vinkje voor de [!DNL order.txt] bestand en klik op **[!UICONTROL Make Local]**.
1. Klik met de rechtermuisknop op het vinkje voor het dialoogvenster [!DNL order.txt] in het [!DNL User] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. De [!DNL order.txt] wordt weergegeven.

   ![Stapinfo](assets/cfg_ordertxt.png)

1. (Optioneel) Voeg de [Inclusief] of [Exclusief] indien gewenst boven aan het bestand instellen. Met deze instelling bepaalt u of items die niet in het dialoogvenster [!DNL order.txt] bestand maar aanwezig in [!DNL Profile Manager] wordt weergegeven in het menu. U kunt onder andere de volgende opties kiezen:

   * **[Inclusief]:** Dit is de standaardinstelling. Deze instelling resulteert in menu-items die niet zijn opgegeven in het dialoogvenster [!DNL order.txt]bestand dat onder aan het menu wordt weergegeven, in alfabetische volgorde. Als de [!DNL Profile Manager] bevat een profielitem naast de items die in het dialoogvenster [!DNL order.txt] hierboven wordt Profiel weergegeven onder Gegevens.

   * **[Exclusief]:** Deze instelling resulteert in menu-items die niet zijn opgegeven in het dialoogvenster [!DNL order.txt] bestand dat wordt uitgesloten van het menu. Als de [!DNL Profile Manager] bevat een profielitem naast de items die in het dialoogvenster [!DNL order.txt] hierboven, zou het Profiel nergens op het menu worden getoond.

   * **leeg:** Als beide [Inclusief] of [Exclusief] boven aan het bestand wordt weergegeven, worden de menu-items door Data Workbench weergegeven alsof de instelling [Inclusief].

1. Voer een of meer van de volgende stappen uit:

   <table id="table_C5D5313DF5E4470499B0B285BA2690F0"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> Deze taak uitvoeren... </th> 
    <th colname="col2" class="entry"> Ga als volgt te werk... </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Menuopdrachten opnieuw ordenen </p> </td> 
    <td colname="col2"> <p>Typ de itemnamen in de volgorde waarin u ze in de Data Workbench wilt weergeven. </p> <p>Als de naam van elk menu-item bijvoorbeeld overeenkomt met de naam van het overeenkomstige bestand of de overeenkomstige map, resulteert het volgende in<b> Tabel toevoegen</b> eerst verschijnt, dan <b>Visualisatie toevoegen</b>, <b>Legenda toevoegen</b>, en <b>Notitie toevoegen</b> als laatste. </p> <p><b>Tabel toevoegen </b> </p> <p><b>Visualisatie toevoegen </b> </p> <p><b>Legenda toevoegen </b> </p> <p><b>Notitie toevoegen </b> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>De naam van een menu-item wijzigen </p> </td> 
    <td colname="col2"> <p>Wijzig de naam van het corresponderende bestand of de corresponderende map in het dialoogvenster <span class="wintitle"> Profielbeheer</span>Wijzig vervolgens de naam van het item in het dialoogvenster <span class="filepath"> order.txt</span> bestand. </p> <p>Als u bijvoorbeeld de naam Annotatie toevoegen aan nieuwe annotatie wilt wijzigen, wijzigt u de naam van de map Annotatie toevoegen in het dialoogvenster <span class="wintitle"> Profielbeheer</span> in Nieuwe aantekening, dan verander de naam van het Add punt van de Annotatie in <span class="filepath"> order.txt</span> bestand naar nieuwe aantekening. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Een menu-item verbergen </p> </td> 
    <td colname="col2"> <p>Als u het menu-item wilt verbergen, maar niet het item zelf wilt verwijderen, typt u een minteken (-) aan het begin van de naam. </p> <p>Het volgende resulteert bijvoorbeeld in <span class="wintitle"> Annotatie toevoegen</span> verschijnt niet in het menu. </p> <p>Legenda toevoegen </p> <p>-Annotatie toevoegen </p> <p>Als u het verborgen menu-item opnieuw wilt weergeven, verwijdert u gewoon het minteken (-) of gebruikt u de parameter Alles verbergen in het dialoogvenster <span class="filepath"> Insight.cfg</span> bestand, zie <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> Configuratieparameters van Insight</a>. </p> <p>U kunt menu-items ook verbergen met de volgende methoden: 
    <ul id="ul_CC9A82AFCE784CA49CC912C9256BAC1A"> 
    <li id="li_28C28CA0DE4B4A8F9C2C2C2B3BDD0557"> <p>De parameter Tonen in een <span class="filepath"> .filter</span>, <span class="filepath"> .metrisch</span>, of <span class="filepath"> .dim</span> het dossier verbergt filters, afgeleide metriek en afmetingen, en uitgebreide afmetingen van hun respectieve menu's. Als u deze optie gebruikt, wordt het item niet vermeld in het menu, maar wel in het profiel en is het beschikbaar voor gebruik. </p> <p>Als u deze parameter wilt gebruiken om filters en afgeleide metriek en afmetingen te verbergen, voegt u de volgende regel toe aan het einde van het dialoogvenster <span class="filepath"> .metrisch</span>, <span class="filepath"> .dim</span>, of <span class="filepath"> .filter</span> bestand: </p> <p><span class="filepath"> show = bool: false</span> </p> <p>Zie Hoofdstuk 10 van het dialoogvenster <i>Configuratie-handleiding voor gegevensset</i> voor instructies. </p> <p>Met deze methode kunt u verborgen items tijdelijk zichtbaar maken door de parameter Alles verbergen in te stellen in het dialoogvenster <span class="filepath"> Insight.cfg</span> bestand. Zie voor meer informatie over deze parameter <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> Configuratieparameters van Insight</a>. </p> </li> 
    <li id="li_2CB65D594DD04C59A8D27A17DBF278FA">De parameter Hidden in het dialoogvenster <span class="filepath"> Transformation.cfg</span> het dossier of om het even welke dataset omvat dossierverbergen uitgebreide dimensies van het dimensiemenu. Als u deze optie gebruikt, wordt het item niet vermeld in het menu, maar wel in het profiel en is het beschikbaar voor gebruik. <p> <p>Opmerking: Wanneer het verbergen van uitgebreide dimensies die deze methode gebruiken, moet u uw dataset voor de afmetingen opnieuw omzetten om worden verborgen. </p> </p> <p>Met deze methode kunt u verborgen items tijdelijk zichtbaar maken door de parameter Alles verbergen in te stellen in het dialoogvenster <span class="filepath"> Insight.cfg</span> bestand. Zie voor meer informatie over deze parameter <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> Configuratieparameters van Insight</a>. </p> </li> 
    <li id="li_6E161953FEA44EC18237D88D7173DC60"> <p>Met nulbytebestanden kunt u elk type item in een willekeurig menu verbergen. Als u deze optie gebruikt, wordt de aanwezigheid van een bestand met dezelfde naam dat gegevens bevat, verborgen in een leeg bestand (nulbyte). Data Workbench behandelt bestanden met een lengte van nul bytes alsof ze niet bestaan. Zie voor meer informatie <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491"> Bestanden verbergen met lege bestanden (nulbyte)</a>. </p> </li> 
    </ul> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Een menu-item verwijderen </p> </td> 
    <td colname="col2"> <p>Als dit bestand is ingesteld op de optie [Exclusief], kunt u gewoon het menu-item uit dit bestand verwijderen. Het item zelf bevindt zich nog steeds in het profiel, maar wordt niet vermeld in het menu. </p> <p>Als dit bestand is ingesteld op de optie [Inclusief], moet u de naam van het menu-item uit dit bestand verwijderen en het bijbehorende bestand verwijderen of op nul byte zetten om het item uit het menu te verwijderen. </p> <p>Voor informatie over het verwijderen van bestanden raadpleegt u <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-del-files-wkg-prof.md#task-1e29c25e6c824cc9b51cb651e835856b"> Bestanden verwijderen uit uw werkprofiel</a>. Zie voor informatie over bestanden van nul bytes <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491"> Bestanden verbergen met lege bestanden (nulbyte)</a>. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Een groepsheader toevoegen </p> </td> 
    <td colname="col2"> <p>Typ drie afbreekstreepjes voor en na de koptekst die u wilt weergeven. </p> <p>Het volgende resulteert bijvoorbeeld in een groepsheader Beheren voor een set gerelateerde menu-items. </p> <p>—Beheren— </p> <p>Profiel </p> <p>Gegevensset </p> <p> <img id="image_DB5BB8A33553499A9FC6B53C544CD4CC" src="assets/cfg_ordertxt_example.png"> </img> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Een lijn toevoegen aan afzonderlijke gedeelten van een menu </p> </td> 
    <td colname="col2"> <p>Typ drie afbreekstreepjes op de plaats waar u een lijn wilt weergeven. </p> <p>De volgende resultaten resulteren bijvoorbeeld in een regel die fungeert als scheidingsteken voor Annotatie toevoegen en Aangepast toevoegen. </p> <p>Annotatie toevoegen </p> <p>— </p> <p>Aangepast toevoegen </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Sla het bestand op en sluit het.
1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het witte vinkje voor het [!DNL order.txt] in het [!DNL User] kolom en klik op **[!UICONTROL Save to]** > * **[!UICONTROL working profile name]**.

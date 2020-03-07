---
description: U kunt de verschijning van om het even welk menu aanpassen door het order.txt- dossier uit te geven verbonden aan dat menu.
solution: Analytics
title: Pas een menu aan gebruikend order.txt dossiers
topic: Data workbench
uuid: 4346114a-05d0-4d15-9633-09c9d869cdd6
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Pas een menu aan gebruikend order.txt dossiers{#customize-a-menu-using-order-txt-files}

U kunt de verschijning van om het even welk menu aanpassen door het order.txt- dossier uit te geven verbonden aan dat menu.

De stappen in deze sectie zijn op alle types van menu&#39;s van toepassing.

**Om het order.txt- dossier uit te geven om een menu aan te passen**

1. In [!DNL Profile Manager], in de kolom van de *profielnaam* , klik het vinkje voor het [!DNL order.txt] dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.
1. Klik het vinkje voor het [!DNL order.txt] dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL order.txt] dossier toont.

   ![Stapgegevens](assets/cfg_ordertxt.png)

1. (Facultatief) voeg of verander [Inclusief] of [Exclusieve] het plaatsen bij de bovenkant van het dossier toe indien gewenst. Dit het plaatsen controleert of de punten niet vermeld in het [!DNL order.txt] dossier maar aanwezig in [!DNL Profile Manager] is vermeld op het menu. De opties omvatten:

   * **[Inclusief]:**Dit is standaard het plaatsen. Dit het plaatsen resulteert in menupunten die niet in het[!DNL order.txt]dossier worden gespecificeerd die bij de bodem van het menu in alfabetische orde worden vermeld. Bijvoorbeeld, als het een punt van het Profiel naast de in[!DNL Profile Manager][!DNL order.txt]hierboven vermelde bevatte, zou het Profiel hieronder Gegevens tonen.

   * **[Exclusief]:**Dit het plaatsen resulteert in menupunten die niet in het[!DNL order.txt]dossier worden gespecificeerd die van het menu worden uitgesloten. Bijvoorbeeld, als het[!DNL Profile Manager]bevatte een punt van het Profiel naast die vermeld in[!DNL order.txt]hierboven, zou het Profiel nergens op het menu worden getoond.

   * **blanco:** Als noch [Inclusief] noch [Exclusief] bij de bovenkant van het dossier verschijnt, toont de Werkbank van Gegevens de menupunten alsof het plaatsen [Inclusief]was.

1. Voer een of meer van de volgende stappen uit:

   <table id="table_C5D5313DF5E4470499B0B285BA2690F0"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> Om deze taak uit te voeren... </th> 
    <th colname="col2" class="entry"> Doe het volgende... </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Menu-items opnieuw ordenen </p> </td> 
    <td colname="col2"> <p>Typ de puntnamen in de orde dat u hen in de Werkbank van Gegevens wilt verschijnen. </p> <p>Bijvoorbeeld, zolang elke naam van het menupunt zijn overeenkomstig dossier of omslagnaam aanpast, zou het volgende in<b> Add Lijst</b> resulteren die eerst verschijnt, dan <b>voeg Visualisatie</b>toe, <b>voeg Legend</b>toe, en <b>voeg Nota</b> toe die het laatst verschijnt. </p> <p><b>Tabel toevoegen </b> </p> <p><b>Visualisatie toevoegen </b> </p> <p><b>Legenda toevoegen </b> </p> <p><b>Opmerking toevoegen </b> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Naam van menu-item wijzigen </p> </td> 
    <td colname="col2"> <p>Noem het overeenkomstige dossier of de omslag in de Manager <span class="wintitle"> van het</span>Profiel anders, dan verander de naam van het punt in het <span class="filepath"> order.txt</span> - dossier. </p> <p>Bijvoorbeeld, om Annotatie toevoegen aan Nieuwe Annotatie anders te noemen, noem de Add omslag van de Annotatie in de Manager <span class="wintitle"> van het</span> Profiel aan Nieuwe Annotatie anders, dan verander de naam van het Add punt van de Annotatie in het <span class="filepath"> order.txt</span> - dossier in Nieuwe Annotatie. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Een menu-item verbergen </p> </td> 
    <td colname="col2"> <p>Om het menupunt te verbergen maar niet het punt zelf te schrappen, typ een minus teken (-) aan het begin van zijn naam. </p> <p>Bijvoorbeeld, de volgende resultaten in <span class="wintitle"> toevoegen Annotatie</span> die niet in het menu verschijnt. </p> <p>Legenda toevoegen </p> <p>-Annotatie toevoegen </p> <p>Om het verborgen menupunt opnieuw te tonen, verwijder eenvoudig het minteken (-) of gebruik Unhide Al parameter in het <span class="filepath"> Insight.cfg</span> - dossier, zie de Parameters <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> van de Configuratie van het</a>Inzicht. </p> <p>U kunt menupunten ook verbergen gebruikend de volgende methodes: 
    <ul id="ul_CC9A82AFCE784CA49CC912C9256BAC1A"> 
    <li id="li_28C28CA0DE4B4A8F9C2C2C2B3BDD0557"> <p>De parameter van de Show in een <span class="filepath"> .filter</span>, <span class="filepath"> .metric</span>, of <span class="filepath"> .dim</span> dossier verbergt filters, afgeleide metriek en afmetingen, en uitgebreide afmetingen van hun respectieve menu's. Wanneer u deze optie gebruikt, wordt het item niet weergegeven in het menu, maar het is nog steeds in het profiel en is beschikbaar voor gebruik. </p> <p>Om deze parameter te gebruiken om filters en afgeleide metriek en afmetingen te verbergen, voeg de volgende lijn aan het eind van het <span class="filepath"> .metric</span>, <span class="filepath"> .dim</span>, of <span class="filepath"> .filter</span> dossier toe: </p> <p><span class="filepath"> show = bool: vals</span> </p> <p>Om deze parameter te gebruiken om uitgebreide afmetingen te verbergen, zie Hoofdstuk 10 van de Gids <i>van de Configuratie van de</i> Dataset voor instructies. </p> <p>U kunt punten tijdelijk verbergen verborgen gebruikend deze methode door Unhide Al parameter in het dossier <span class="filepath"> Insight.cfg</span> te plaatsen. Voor meer informatie over deze parameter, zie de Parameters <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> van de Configuratie van het</a>Inzicht. </p> </li> 
    <li id="li_2CB65D594DD04C59A8D27A17DBF278FA">De verborgen parameter in het <span class="filepath"> Transformation.cfg</span> - dossier of om het even welke dataset omvat dossierhuiden uitgebreide afmetingen van het afmetingsmenu. Wanneer u deze optie gebruikt, wordt het item niet weergegeven in het menu, maar het is nog steeds in het profiel en is beschikbaar voor gebruik. <p> <p>Opmerking:  Wanneer het verbergen van uitgebreide afmetingen die deze methode gebruiken, moet u uw dataset voor de te verbergen afmetingen opnieuw omzetten. </p> </p> <p>U kunt punten tijdelijk verbergen verborgen gebruikend deze methode door Unhide Al parameter in het dossier <span class="filepath"> Insight.cfg</span> te plaatsen. Voor meer informatie over deze parameter, zie de Parameters <a href="../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b"> van de Configuratie van het</a>Inzicht. </p> </li> 
    <li id="li_6E161953FEA44EC18237D88D7173DC60"> <p>De nul-bytedossiers verbergen om het even welk type van punt op om het even welk menu. Wanneer het gebruiken van deze optie, verbergt een leeg (nul-byte) dossier de aanwezigheid van een dossier met de zelfde naam die gegevens bevat. De Werkbank van gegevens behandelt nul-bytedossiers alsof zij niet bestaan. Voor meer informatie, zie het <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491"> Hiding van Dossiers Gebruikend Lege (Nul-byte) Dossiers</a>. </p> </li> 
    </ul> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Een menu-item verwijderen </p> </td> 
    <td colname="col2"> <p>Als dit dossier wordt geplaatst om de [Exclusieve] optie te gebruiken, kunt u het menupunt van dit dossier eenvoudig schrappen. Het punt zelf is nog in het profiel, maar het is niet vermeld in het menu. </p> <p>Als dit dossier wordt geplaatst om de [Inclusieve] optie te gebruiken, moet u de naam van het menupunt uit dit dossier verwijderen en of schrappen of nul-byte het overeenkomstige dossier om het punt uit het menu te verwijderen. </p> <p>Zie Bestanden verwijderen uit uw werkprofiel <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-del-files-wkg-prof.md#task-1e29c25e6c824cc9b51cb651e835856b"></a>voor meer informatie over het verwijderen van bestanden. Voor informatie over nul-bytedossiers, zie het <a href="../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491"> Hiding van Dossiers Gebruikend de Lege (Nul-byte) Dossiers</a>. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Voeg een groepkoptekst toe </p> </td> 
    <td colname="col2"> <p>Typ drie koppeltekens voor en na de koptekst die u wilt verschijnen. </p> <p>Bijvoorbeeld, zou het volgende in een Manage groepskopbal voor een reeks verwante menupunten resulteren. </p> <p>—Beheer— </p> <p>Profiel </p> <p>Dataset </p> <p> <img id="image_DB5BB8A33553499A9FC6B53C544CD4CC" src="assets/cfg_ordertxt_example.png"> </img> </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Voeg een lijn aan afzonderlijke secties van een menu toe </p> </td> 
    <td colname="col2"> <p>Typ drie koppeltekens waar u een lijn wilt verschijnen. </p> <p>Bijvoorbeeld, de volgende resultaten in een lijn die Annotatie scheidt toevoegen en Douane toevoegen. </p> <p>Annotatie toevoegen </p> <p>--- </p> <p>Aangepast toevoegen </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Sparen en sluit het dossier.
1. (Facultatief) om de veranderingen ter beschikking te stellen van alle gebruikers van het het werk profiel, klik het witte vinkje voor het [!DNL order.txt] dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Save to]** > * **[!UICONTROL working profile name]**.

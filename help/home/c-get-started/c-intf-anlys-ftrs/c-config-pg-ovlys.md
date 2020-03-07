---
description: De bekledingen van de pagina worden gevormd slechts in de toepassing van de Plaats, maar zij kunnen voor andere toepassingen worden gevormd.
solution: Analytics
title: Een paginabedekking configureren
topic: Data workbench
uuid: c4c612ed-5154-4b20-96ab-24b74fba19a2
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Een paginabedekking configureren{#configure-a-page-overlay}

De bekledingen van de pagina worden gevormd slechts in de toepassing van de Plaats, maar zij kunnen voor andere toepassingen worden gevormd.

Voor informatie over het vormen van paginabekleding voor een andere toepassing, de Raadplegende Diensten van contactAdobe.

De visualisatie van de paginabekleding is een hulpmiddel voor de verbindingsanalyse van HTML. Wanneer u om een bekleding voor een bepaalde pagina verzoekt, neemt de Werkbank van Gegevens een momentopname van de daadwerkelijke pagina aangezien het in Webbrowser zou verschijnen en de code van HTML ontleedt die verbindingen volgens een lijst van regelmatige uitdrukkingen vertegenwoordigt die u bepaalt. Voor elke verbinding op de geselecteerde pagina, probeert de software om een regelmatige gelijke van het uitdrukkingspatroon te vinden door onderaan de lijst te werken tot de eerste gelijke wordt gevonden. Als er een gelijke is, verschijnt de verbinding benadrukt in de paginalay-out.

De bekleding van de pagina toont gegevens slechts wanneer u een kleurenlegende aan de werkruimte toevoegt die de paginabekleding bevat.

>[!NOTE]
>
>Het vormen van paginabekleding vereist zorgvuldig configuratiewerk, en het is mogelijk om misleidende resultaten tot stand te brengen als de verbindingen aan de gegevens verkeerd in kaart worden gebracht. Het werk betrokken bij het vormen van paginabekleding voor een specifieke plaats hangt van af hoe de verbindingen binnen de code van HTML op de pagina&#39;s van de plaats worden voorgesteld.

De bekleding van de pagina, door zijn aard, stelt aan de gebruiker het mentale model voor dat het &quot;toont waar de mensen klikken.&quot; Als de gegevens die de visualisatie ondersteunen niet overeenkomen met dit model, is de kans op verwarring groot.

In [!DNL Site], vertegenwoordigt een verbinding typisch een element van Volgende URI of de Volgende afmeting van de Verbinding, maar u kunt een verbinding aan om het even welke afmeting in kaart brengen die voor uw analyse steek houdt. Voor informatie over het vormen van paginabekleding voor andere afmetingen, contacteer Adobe Consulting Services.

>[!NOTE]
>
>Het gebruiken van de afmeting van de Pagina voor paginabekleding wordt niet geadviseerd. De gebruikers kunnen de elementen van de dimensies van de Pagina anders noemen, daardoor veranderend de verbindingssyntaxis waarop de functionaliteit van de paginaluik baseert.

Om paginabekleding voor te vormen [!DNL Site], moet u twee dossiers uitgeven:

* **[!DNL Page Overlay.vw]:**Dit dossier is een malplaatjedossier voor het creëren van paginabekledingsvisualisaties. Minstens één malplaatjedossier moet in het profiel aanwezig zijn waarvoor u paginabekleding vormt.
* **[!DNL Page Overlay Link Templates.cfg]:**Wanneer de visualisatie van de paginabekleding een pagina laadt, identificeert het automatisch de verbindingen in de pagina en hun bestemmingen. Om deze verbindingen met elementen in de gegevens in verband te brengen, moet u een reeks regelmatige uitdrukkingen in dit dossier bepalen.

   U kunt veelvoudige regelmatige uitdrukkingen bepalen tegen de elementen van de afmeting aan te passen. De orde waarin u de uitdrukkingen bepaalt is belangrijk. Wanneer u om een bekleding voor een bepaalde pagina verzoekt, neemt de Werkbank van Gegevens een momentopname van de daadwerkelijke pagina aangezien het in Webbrowser zou verschijnen en de code van HTML ontleedt die verbindingen volgens een lijst van regelmatige uitdrukkingen vertegenwoordigt die u bepaalt. Voor elke verbinding op de geselecteerde pagina, probeert de software om een regelmatige gelijke van het uitdrukkingspatroon te vinden door onderaan de lijst te werken tot de eerste gelijke wordt gevonden. De eerste uitdrukking om een afmetingselement aan te passen is gebruikt. Daarom is het best om van de regelmatige uitdrukking met het meest specifieke passende patroon eerst een lijst te maken, dat door minder specifieke uitdrukkingen wordt gevolgd. Als er een gelijke is, verschijnt de verbinding benadrukt in de visualisatie van de paginalay-out.

**Om paginabekleding voor Plaats te vormen**

1. I

   In de [!DNL Profile Manager], navigeer aan **[!UICONTROL Context]** > **[!UICONTROL Dimension Element]** > **[!UICONTROL URI]**.

   >[!NOTE]
   >
   >De folder van het Element van de Dimensie bevat de punten van het contextmenu die verschijnen wanneer u een afmetingselement met de rechtermuisknop aanklikt. Bijvoorbeeld, open een lijst van URI, dan selecteer een element van URI. Klik de Bekleding van URI met de rechtermuisknop aan en van de Pagina verschijnt.

1. In de omslag van URI, klik het vinkje naast het [!DNL Page Overlay.vw] dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. Specificeer het Domein (en Browser Hoogte, indien nodig).

   ```
   window = simpleBorderWindow: 
     client = scrollWindow: 
       client = PageOverlay: 
         URI Template = string: http://%Domain%%Element%
         URI Parameters = map: 
           Domain = string: domain name
           Element = ref: Element/Name
         Dim = ref: wdata/model/dim/URI
         Dim Element = ref: Element/Name
         Level = ref: wdata/model/dim/Page View
         Group = ref: wdata/model/dim/Session
         Browser Height = int: browser height
     pos = v3d: (518, 202, 0)
     size = v3d: (810, 610, 0)
     titleBar = editor: 
       size = v3d: (61, 19, 0)
       text = string: 
   ```

1. Sla het bestand op.
1. Als u deze wijziging beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u in het [!DNL Profile Manager]venster met de rechtermuisknop op het vinkje voor het [!DNL .vw] bestand in de [!DNL User] kolom en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

   >[!NOTE]
   >
   >U kunt extra malplaatjedossiers voor andere plaatsen of subdomeinen tot stand brengen. Elk malplaatje dat u creeert verschijnt in het [!DNL Page Overlay menu].

1. In de omslag van de Context van [!DNL Profile Manager], klik het vinkje naast het [!DNL Page Overlay Link Templates.cfg] dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.

   Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.
1. Klik met de rechtermuisknop **[!UICONTROL Link Templates]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Regular Expression]**.
1. Geef zonodig de parameters voor vector LinkRegex uit:

<table id="table_24DD4BB5009542F7BB1DA3318E2E6E2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Verstrek deze informatie... </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Afmetingen </p> </td> 
   <td colname="col2"> <p>De afmeting (typisch de Volgende afmeting van URI) die door de verbinding wordt vertegenwoordigd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uitdrukking </p> </td> 
   <td colname="col2"> <p>De regelmatige uitdrukking die wordt gebruikt om het relevante deel van de verbinding van HTML te selecteren om het volgende element van de Dimensie te vinden. De regelmatige uitdrukking moet een nauwkeurige gelijke zijn, en het gewenste outputpatroon wordt gegroepeerd met haakjes. Voor details over regelmatige uitdrukkingen, zie de Gids <i>van de Configuratie van de</i>Dataset. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uitvoerpatroon </p> </td> 
   <td colname="col2"> <p>Het outputpatroon van de regelmatige uitdrukking die wordt gebruikt om het resulterende element van de parameter van de Dimensie te halen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het volgende steekproefdossier toont drie regelmatige uitdrukkingen:

![](assets/cfg_PageOverlayLinkTemplates_Example.png)

1. Om het dossier te bewaren, klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. Als u deze wijziging beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor [!DNL Page Overlay Link Templates.cfg] in de [!DNL User] kolom en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.


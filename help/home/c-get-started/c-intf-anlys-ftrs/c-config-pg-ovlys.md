---
description: Pagina-overlays worden alleen geconfigureerd in de sitetoepassing, maar ze kunnen ook worden geconfigureerd voor andere toepassingen.
title: Een paginabedekking configureren
uuid: c4c612ed-5154-4b20-96ab-24b74fba19a2
exl-id: 4e0dfce8-def2-49f3-93e8-41d82922fb88
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# Een paginabedekking configureren{#configure-a-page-overlay}

Pagina-overlays worden alleen geconfigureerd in de sitetoepassing, maar ze kunnen ook worden geconfigureerd voor andere toepassingen.

Voor informatie over het vormen van paginaoverlay voor een andere toepassing, contacteer de Raadplegende Diensten van de Adobe.

De visualisatie van de paginabedekking is een hulpmiddel voor de analyse van HTML-koppelingen. Wanneer u voor een bepaalde pagina een bedekking aanvraagt, maakt Data Workbench een momentopname van de pagina zoals deze in een webbrowser wordt weergegeven en parseert de HTML-code die koppelingen vertegenwoordigt volgens een lijst met reguliere expressies die u definieert. Voor elke koppeling op de geselecteerde pagina probeert de software een overeenkomende reguliere-expressiepatroon te vinden door onderaan de lijst te werken totdat de eerste overeenkomst is gevonden. Als er een overeenkomst is, wordt de koppeling gemarkeerd weergegeven in de paginaoverlay.

Bij paginabedekking worden alleen gegevens weergegeven wanneer u een kleurlegenda toevoegt aan de werkruimte die de paginabedekking bevat.

>[!NOTE]
>
>Voor het configureren van paginaoverlay is een zorgvuldige configuratie vereist en het is mogelijk om misleidende resultaten te maken als koppelingen op onjuiste wijze aan de gegevens worden toegewezen. De manier waarop u paginaoverlay voor een bepaalde site configureert, is afhankelijk van de manier waarop koppelingen worden weergegeven in de HTML-code op de pagina&#39;s van de site.

Door de aard van de paginaoverlapping wordt aan de gebruiker het mentale model voorgesteld dat het toont &quot;waar de mensen klikken.&quot; Als de gegevens die de visualisatie ondersteunen niet overeenkomen met dit model, is de kans op verwarring groot.

In [!DNL Site], vertegenwoordigt een verbinding typisch een element van Volgende URI of Volgende afmeting van de Verbinding, maar u kunt een verbinding aan om het even welke afmeting in kaart brengen die voor uw analyse steek houdt. Voor informatie over het vormen van paginabekleding voor andere dimensies, contacteer de Raadplegende Diensten van de Adobe.

>[!NOTE]
>
>Het wordt niet aanbevolen de pagina-afmeting voor paginabedekking te gebruiken. Gebruikers kunnen de naam van de elementen van de pagina-afmetingen wijzigen en zo de koppelingssyntaxis wijzigen waarop de functie voor paginaoverlay is gebaseerd.

Als u paginabedekking voor [!DNL Site] wilt configureren, moet u twee bestanden bewerken:

* **[!DNL Page Overlay.vw]:** Dit bestand is een sjabloonbestand voor het maken van paginaoverlayvisualisaties. Er moet ten minste één sjabloonbestand aanwezig zijn in het profiel waarvoor u paginaoverlay configureert.
* **[!DNL Page Overlay Link Templates.cfg]:** Wanneer de pagina-overlayvisualisatie een pagina laadt, worden automatisch de koppelingen op de pagina en hun bestemmingen geïdentificeerd. Als u deze koppelingen wilt koppelen aan elementen in de gegevens, moet u een set reguliere expressies definiëren in dit bestand.

   U kunt meerdere reguliere expressies definiëren die overeenkomen met de elementen van de dimensie. De volgorde waarin u de expressies definieert, is belangrijk. Wanneer u voor een bepaalde pagina een bedekking aanvraagt, maakt Data Workbench een momentopname van de pagina zoals deze in een webbrowser wordt weergegeven en parseert de HTML-code die koppelingen vertegenwoordigt volgens een lijst met reguliere expressies die u definieert. Voor elke koppeling op de geselecteerde pagina probeert de software een overeenkomende reguliere-expressiepatroon te vinden door onderaan de lijst te werken totdat de eerste overeenkomst is gevonden. De eerste expressie die moet overeenkomen met een dimensie-element is de expressie die wordt gebruikt. Daarom is het beter om eerst de reguliere expressie met het meest specifieke overeenkomende patroon weer te geven, gevolgd door minder specifieke expressies. Als er een overeenkomst is, wordt de koppeling gemarkeerd weergegeven in de visualisatie van de paginabedekking.

**Pagina-overlay voor site configureren**

1. I

   Navigeer in [!DNL Profile Manager] naar **[!UICONTROL Context]** > **[!UICONTROL Dimension Element]** > **[!UICONTROL URI]**.

   >[!NOTE]
   >
   >De map Dimension Element bevat de contextmenu-items die worden weergegeven wanneer u met de rechtermuisknop op een dimensie-element klikt. Open bijvoorbeeld een URI-tabel en selecteer vervolgens een URI-element. Klik met de rechtermuisknop op de URI en de paginaoverlay.

1. Klik in de map URI met de rechtermuisknop op het vinkje naast het bestand [!DNL Page Overlay.vw] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].
1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. Geef het domein op (en Browserhoogte, indien nodig).

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
1. Als u deze wijziging beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand [!DNL .vw] in de kolom [!DNL User] en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

   >[!NOTE]
   >
   >U kunt aanvullende sjabloonbestanden maken voor andere sites of subdomeinen. Elke sjabloon die u maakt, wordt weergegeven in de [!DNL Page Overlay menu].

1. Klik in de map Context van het [!DNL Profile Manager] met de rechtermuisknop op het vinkje naast het bestand [!DNL Page Overlay Link Templates.cfg] en klik op **[!UICONTROL Make Local]**.

   Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**.
1. Klik met de rechtermuisknop **[!UICONTROL Link Templates]** en klik **[!UICONTROL Add new]** > **[!UICONTROL Regular Expression]**.
1. Bewerk indien nodig de parameters voor de LinkRegex-vector:

<table id="table_24DD4BB5009542F7BB1DA3318E2E6E2B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Deze informatie opgeven... </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Dimension </p> </td> 
   <td colname="col2"> <p>De dimensie (doorgaans de volgende URI-dimensie) die door de koppeling wordt vertegenwoordigd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uitdrukking </p> </td> 
   <td colname="col2"> <p>De reguliere expressie die wordt gebruikt om het desbetreffende gedeelte van de HTML-koppeling te selecteren en het volgende element in de Dimension te zoeken. De reguliere expressie moet exact overeenkomen en het gewenste uitvoerpatroon wordt tussen haakjes gegroepeerd. Voor details over regelmatige uitdrukkingen, zie <i>de Gids van de Configuratie van de Dataset</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uitvoerpatroon </p> </td> 
   <td colname="col2"> <p>Het uitvoerpatroon van de reguliere expressie die wordt gebruikt om het resulterende element van de parameter Dimension te extraheren. </p> </td> 
  </tr> 
 </tbody> 
</table>

In het volgende voorbeeldbestand worden drie reguliere expressies getoond:

![](assets/cfg_PageOverlayLinkTemplates_Example.png)

1. Als u het bestand wilt opslaan, klikt u met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klikt u op **[!UICONTROL Save]**.
1. Als u deze wijziging beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het vinkje voor [!DNL Page Overlay Link Templates.cfg] in de kolom [!DNL User] en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

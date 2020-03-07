---
description: De informatie over Web-specifieke montages die in de Dataset van de Transformatie worden bepaald omvat dossiers die met de profielen van Adobe voor Plaats worden geleverd.
solution: Analytics
title: Web-specifieke Montages voor Transformatie
topic: Data workbench
uuid: 282f0f4d-43d7-41cf-bae8-5cac6b4d81a0
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Web-specifieke Montages voor Transformatie{#web-specific-settings-for-transformation}

De informatie over Web-specifieke montages die in de Dataset van de Transformatie worden bepaald omvat dossiers die met de profielen van Adobe voor Plaats worden geleverd.

De voorwaarden, de afmetingen, en de parameters die door deze montages worden bepaald worden gecreeerd tijdens de transformatiefase van datasetconstructie.

* [Voorwaarde voor paginaweergave](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-transf.md#section-cc2807a12a88492f8b64a43234a1f835)
* [URI-dimensie](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-transf.md#section-348f7e9099d049d197a7cdcbc8a6c234)
* [Afmetingen referentie](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-transf.md#section-8a97ec34d18b4814b5f95495ac4f8638)
* [Sessieparameters](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-transf.md#section-0a209b0c504041a5801f7f71a963c8b1)

## Voorwaarde voor paginaweergave {#section-cc2807a12a88492f8b64a43234a1f835}

Het [!DNL Page View Condition] is een voorwaardenverrichting die bepaalt of een bepaalde logboekingang (namelijk een paginaverzoek) in de gegevens zou moeten worden omvat die over de geschiedenis van de de paginamening van een bezoeker worden verzameld. Wanneer de logboekingang voldoet aan [!DNL Page View Condition], wordt het een element van de telbare dimensie van de Mening van de Pagina. Als een logboekingang niet voldoet aan [!DNL Page View Condition], zijn zijn zijn gegevensgebieden nog toegankelijk door andere afmetingen. Naast de dimensie van de Mening van de Pagina, kunnen de volgende afmetingen door de resultaten van worden beïnvloed [!DNL Page View Condition]:

* **[!DNL URI]en[!DNL Page]:**Deze dimensies worden rechtstreeks beïnvloed door de[!DNL Page View Condition]. Als de bepaalde pagina niet overgaat[!DNL Page View Condition,]is het niet inbegrepen in de afmetingen van URI of van de Pagina.

* **[!DNL Visitor Page Views]en[!DNL Session Page Views]:**De de Meningen van de Pagina van de Bezoeker en dimensies van de Meningen van de Pagina van de Zitting zijn een telling van het aantal pagina&#39;s die door een bezoeker aan of in een bepaalde zitting, respectievelijk worden bekeken. De pagina&#39;s die uit door de pagina worden gefiltreerd[!DNL Page View Condition]maken geen deel uit van deze telling.

* **Sessienummer:** Het [!DNL Page View Condition] heeft een indirect effect op de dimensie van het Aantal van de Zitting. De dimensie van het Aantal van de Zitting wordt gecreeerd voorafgaand aan [!DNL Page View Condition]; daarom is het mogelijk om , wanneer [!DNL Session Number] in verband met het [!DNL Page Views]onderwerp wordt overwogen , sessies te houden zonder opvattingen op de pagina .

Uw standaardimplementatie van [!DNL Site] omvat een [!DNL Transformation Dataset Include] dossier waarin de telbare dimensie van de Mening van de Pagina en verwante [!DNL Page View Condition] worden bepaald.

Voor informatie over telbare afmetingen, zie [Uitgebreide Afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

**Om de configuratiemontages voor de Voorwaarde van de Mening van de Pagina uit te geven**

1. Open het [!DNL Profile Manager] binnen uw datasetprofiel en open het [!DNL Dataset\Transformation\Traffic\Page View.cfg] dossier.

   >[!NOTE]
   >
   >Als u uw implementatie van hebt aangepast, kan het dossier waarin deze configuratiemontages bestaan van de beschreven plaats verschillen. [!DNL Site]

1. Herzie of geef de waarden van de parameters van uit [!DNL Page View Condition] zoals nodig. Gebruik het volgende voorbeeld als gids. In dit dossier, [!DNL Page View Condition] wordt bepaald door een [!DNL Copy] transformatie. Merk op dat dit dossier ook de definitie van de telbare dimensie van de Mening van de Pagina bevat.

   ![](assets/cfg_WebParameters_PageView.png)

   >[!NOTE]
   >
   >Voor informatie over telbare afmetingen, zie [Uitgebreide Afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md). Voor informatie over de [!DNL Copy] transformatie, zie de Transformaties [van](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md)Gegevens.

1. Sparen het dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken, dan klik **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## URI-dimensie {#section-348f7e9099d049d197a7cdcbc8a6c234}

Als u met werkt, moet u de dimensie van URI bepalen de waarvan elementen de stammen van URI van de bekeken websitepagina&#39;s zijn. [!DNL Site] Uw standaardimplementatie omvat een [!DNL Transformation Dataset Include] dossier waarin de eenvoudige afmeting van URI wordt bepaald.

Voor informatie over eenvoudige afmetingen, zie [Uitgebreide Afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

**Om de configuratiemontages voor de dimensie van URI uit te geven**

1. Open het [!DNL Profile Manager] binnen uw datasetprofiel en open het [!DNL Dataset\Transformation\Traffic\URI.cfg] dossier.

   >[!NOTE]
   >
   >Als u uw implementatie van hebt aangepast, kan het dossier waarin deze configuratiemontages bestaan van de beschreven plaats verschillen. [!DNL Site]

1. Herzie of geef de waarden van de parameters van het dossier uit zoals gewenst. Gebruik het volgende voorbeeld en de informatie als gidsen.

![](assets/cfg_WebParameters_URI.png)

De configuratiemontages voor de dimensie van URI omvatten de volgende twee parameters:

* **Gevallengevoelig:** Waar of vals. Als waar, wordt het brievengeval (hoger/lager) overwogen in het identificeren van unieke pagina&#39;s. De standaardwaarde is waar.
* **Maximum aantal elementen:** Het maximumaantal elementen (namelijk URIs) voor de afmeting van URI. De standaardwaarde is 32768.

   >[!NOTE]
   >
   >Het veranderen van deze waarde kan ernstige prestatieskwesties veroorzaken. Verander deze waarde niet zonder Adobe te raadplegen.

* Sparen het [!DNL URI.cfg] dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken, dan klik **[!UICONTROL Save]**.

* Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## Afmetingen referentie {#section-8a97ec34d18b4814b5f95495ac4f8638}

Als u met werkt, moet u de dimensie van de Referateur bepalen de waarvan elementen uit de tweede niveaudomeinen van de verwijzingen van de eerste logboekingangen in alle zittingen bestaan. [!DNL Site] Uw standaardimplementatie omvat een [!DNL Transformation Dataset Include] dossier waarin de eenvoudige afmeting van de Referateur wordt bepaald.

Voor informatie over eenvoudige afmetingen, zie [Uitgebreide Afmetingen](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

**Om de configuratiemontages voor de afmeting van de Referrer uit te geven**

1. Open het [!DNL Profile Manager] binnen uw datasetprofiel en open het [!DNL Dataset\Transformation\Traffic\Referrer.cfg] dossier.

   >[!NOTE]
   >
   >Als u uw implementatie van hebt aangepast, kan het dossier waarin deze configuratiemontages bestaan van de beschreven plaats verschillen. [!DNL Site]

1. Herzie of geef de waarden van de parameters van het dossier uit zoals gewenst. Gebruik het volgende voorbeeld en de informatie als gidsen.

   ![](assets/cfg_WebParameters_Referrer.png)

   De configuratiemontages voor de afmeting van de Referateur omvatten de Maximale parameter van Elementen, die het maximumaantal elementen (namelijk verwijzingen) voor de afmeting van de Referateur specificeert. De standaardwaarde is 32768.

   >[!NOTE]
   >
   >In het voorbeeld hierboven, wordt de [!DNL Maximum Elements] parameter geplaatst aan 0. Wanneer deze parameter aan 0 wordt geplaatst, gebruikt de server van de gegevenswerkbank zijn interne standaardwaarde van 32768.

1. Sparen het [!DNL Referrer.cfg] dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken, dan klik **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## Sessieparameters {#section-0a209b0c504041a5801f7f71a963c8b1}

Als u met werkt, kunt u parameters specificeren die de grenzen van de zitting van een bezoeker op een website bepalen. [!DNL Site] Deze parameters zijn geldig slechts wanneer bepaald in een [!DNL Transformation Dataset Include] dossier binnen uw [!DNL Site] implementatie.

De volgende parameters zijn uniek in zoverre dat zij leden van de [!DNL Transformation Dataset Include] vector van het [!DNL Parameters] dossier kunnen zijn, of zij kunnen als individuele parameters in het [!DNL Transformation.cfg]dossier worden vermeld. Een parameter kan precies eens worden bepaald, zodat worden deze parameters bepaald of in het [!DNL Transformation.cfg]dossier of in de [!DNL Parameters] vector van de dataset omvat dossier - niet in beide dossiers.
**Maximale duur sessie en time-out sessie**

De maximum Duur van de Zitting en Onderbreking van de Zitting zijn koordparameters die de lengte van de zitting van een bezoeker bepalen. Deze parameters werken met de Interne parameter van Domeinen om zittingslengte te bepalen.

De maximum Duur van de Zitting specificeert de langste lengte van zitting alvorens een nieuwe zitting is begonnen. Dit houdt Web-pagina&#39;s die autoinhoud hebben die van het creëren van zittingen verfrissen die willekeurig lang zijn. Als de referentie van een klik aan één van de ingangen in de Interne parameter van Domeinen wordt geplaatst, wordt deze onderbreking gebruikt om het eind van een zitting te bepalen. Geen zitting kan langer zijn dan de gespecificeerde MaximumDuur van de Zitting ongeacht hoeveel klikken het bevat. De aanbevolen waarde is 48 uur.

De Onderbreking van de zitting specificeert de hoeveelheid tijd die tussen logboekingangen van een bepaalde bezoeker moet overgaan om het eind van één zitting en het begin van een nieuwe zitting (namelijk de typische onderbreking te bepalen die wordt gebruikt om een gebruikerszitting te bepalen) te bepalen. De geadviseerde waarde van deze parameter is 30 minuten. Als de referentie van een klik niet aan één van de verwijzingen in de Interne parameter van Domeinen wordt geplaatst, wordt deze onderbreking gebruikt om de zitting te bepalen. Als cs (verwijzing-domein) voor een logboekingang in de lijst van interne domeinen is, dan bepaalt de MaximumDuur van de Zitting of de huidige logboekingang deel van een bestaande zitting of het begin van een nieuwe zitting uitmaakt.

Overweeg een situatie waarin een bezoeker van zijn computer voor een periode langer dan de Onderbreking van de Zitting terwijl in het midden van het doorbladeren van de plaats wordt geroepen. Bij het terugkeren blijft hij doorbladeren waar hij weg ging. Omdat de bezoeker nooit de plaats verlaat of zijn browser sluit, is cs (verwijzing-domein) van zijn volgende klik het zelfde als het interne domein, en zijn originele zitting blijft actief zolang het Maximum plaatsen van de Duur van de Zitting niet wordt bereikt. Als het domein van de site wordt vermeld als een intern domein en de maximale time-out niet wordt bereikt, wordt de interactie van de bezoeker weergegeven als één sessie en niet als twee afzonderlijke sessies. Nochtans, als de bezoeker aan zijn computer terugkeert en zijn volgende klik een externe (of lege) verwijzer heeft, begint een nieuwe zitting.

>[!NOTE]
>
>De [!DNL Sessionize] transformatie speelt [!DNL Timeout Condition] ook een rol in het bepalen van de duur van de sessie van een bezoeker. Als de Onderbreking van de Zitting en de MaximumDuur van de Zitting niet van toepassing zijn, [!DNL Timeout Condition] wordt gecontroleerd om te bepalen of een logboekingang als begin van een nieuwe zitting zou moeten worden beschouwd. Voor meer informatie, zie de Transformaties van [Gegevens](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md).

**Om de Maximale parameters van de Duur van de Zitting en van de Onderbreking van de Zitting uit te geven**

Als u met werkt, omvat uw standaardimplementatie waarschijnlijk een [!DNL Site][!DNL Transformation Dataset Include] dossier waarin de namen en de geadviseerde waarden van deze parameters worden gespecificeerd.

1. Open het [!DNL Profile Manager] binnen uw datasetprofiel en ga naar [!DNL Dataset\Transformation\Traffic\Session Parameters.cfg].

   >[!NOTE]
   >
   >Als u uw implementatie van hebt aangepast, [!DNL Site]kan het dossier waarin deze parameters worden bepaald van de beschreven plaats verschillen.

1. Geef de waarden van de parameters uit zoals gewenst. Ben zeker om de gewenste eenheden (notulen, uren, etc.) te specificeren.

   ![](assets/cfg_WebParameters_SessionParameters.png)

1. Sparen het [!DNL Session Parameters.cfg] dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > **[!UICONTROL profile name]**, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

**[!DNL Internal Domains]**

[!DNL Internal Domains] is een vectorparameter die van de gastheren van het domeinniveau (interne verwijzingen) een lijst maakt die als deel van een bepaalde website zouden moeten worden behandeld. Deze gastheren worden verwijderd uit de verwijzingsdimensie (die een lijst van de externe verwijzingsinformatie is). Wanneer cs (verwijzing-domein) om het even welke koorden aanpast die in de reeks interne domeinen worden vermeld, wordt de Onderbreking van de Zitting genegeerd en de MaximumDuur van de Zitting wordt gebruikt om zittingslengte te bepalen.

De interne parameter van Domeinen kan ook worden gebruikt om het begin van een nieuwe zitting te verhinderen wanneer de bezoekers zich onder de veelvoudige domeinen van een bedrijf bewegen verbonden op een manier die zittingsonderbreking overschrijdt. Bijvoorbeeld, overweeg een bedrijf dat delen van zijn plaats heeft die over twee domeinen worden verdeeld: wordt geregistreerd ( [!DNL xyz.com]), en andere wordt niet geregistreerd ( [!DNL xyz-unlogged.com]). Als deze plaatsen op een manier worden geïntegreerd die de naadloze beweging van verkeer over de twee domeinen vergemakkelijkt, is het niet wenselijk om een verschillende zitting te produceren telkens als de bezoeker zich van [!DNL xyz-unlogged.com] domein terug naar het [!DNL xyz.com] domein beweegt. Het aanbieden [!DNL xyz-unlogged.com] als intern domein houdt zittingen van het worden verdeeld in veelvoudige zittingen als resultaat van verkeer over deze twee domeinen zolang het Maximum plaatsen van de Duur van de Zitting niet wordt bereikt.

**Om een intern domein toe te voegen**

Als u met werkt, omvat uw standaardimplementatie een [!DNL Site][!DNL Transformation Dataset Include] dossier voor het bepalen van de Interne parameter van Domeinen. In dit dossier, wordt de parameter genoemd; u gaat enkel de interne domeinen in die u het bijgewerkte dossier wilt omvatten en opslaan.

1. Open de [!DNL Profile Manager] binnen uw datasetprofiel en ga naar [!DNL Dataset\Transformation\Traffic\Internal Domains.cfg.]

   >[!NOTE]
   >
   >Als u uw implementatie van hebt aangepast, kan het dossier waarin de Interne parameter van Domeinen wordt bepaald van de beschreven plaats verschillen. [!DNL Site]

1. Klik **[!UICONTROL Value]** voor de Interne vectorparameter van Domeinen met de rechtermuisknop aan en klik **[!UICONTROL Add new]** > **[!UICONTROL Value]**.

1. Geef de waarden uit zoals gewenst.

   ![](assets/cfg_WebParameters_InternalDomains.png)

1. Sparen het [!DNL Internal Domains.cfg] dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waar de profielnaam de naam van het datasetprofiel of het geërfte profiel is waartot de dataset omvat dossier behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.


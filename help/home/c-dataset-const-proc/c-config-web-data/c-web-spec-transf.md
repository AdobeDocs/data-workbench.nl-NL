---
description: Informatie over webspecifieke instellingen die zijn gedefinieerd in Dataset voor transformatie Inclusief bestanden die worden geleverd met Adobe-profielen voor site.
title: Web-specifieke instellingen voor transformatie
uuid: 282f0f4d-43d7-41cf-bae8-5cac6b4d81a0
exl-id: 737f5e7a-7ab3-4ff7-8d92-7ccd87c28743
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '2035'
ht-degree: 0%

---

# Web-specifieke Montages voor Transformatie{#web-specific-settings-for-transformation}

Informatie over webspecifieke instellingen die zijn gedefinieerd in Dataset voor transformatie Inclusief bestanden die worden geleverd met Adobe-profielen voor site.

De voorwaarden, de afmetingen, en de parameters die door deze montages worden bepaald worden gecreeerd tijdens de transformatiefase van datasetconstructie.

* [Voorwaarde paginaweergave](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-transf.md#section-cc2807a12a88492f8b64a43234a1f835)
* [URI Dimension](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-transf.md#section-348f7e9099d049d197a7cdcbc8a6c234)
* [Referrer Dimension](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-transf.md#section-8a97ec34d18b4814b5f95495ac4f8638)
* [Sessieparameters](../../../home/c-dataset-const-proc/c-config-web-data/c-web-spec-transf.md#section-0a209b0c504041a5801f7f71a963c8b1)

## Voorwaarde paginaweergave {#section-cc2807a12a88492f8b64a43234a1f835}

[!DNL Page View Condition] is een voorwaardenverrichting die bepaalt of een bepaalde logboekingang (namelijk een paginaverzoek) in de gegevens zou moeten worden omvat die over de geschiedenis van de de paginamening van een bezoeker worden verzameld. Wanneer de logboekingang [!DNL Page View Condition] tevredenstelt, wordt het een element van de telbare afmeting van de Mening van de Pagina. Als een logbestandvermelding niet voldoet aan [!DNL Page View Condition], zijn de gegevensvelden nog steeds toegankelijk voor andere dimensies. Naast de dimensie Paginaweergave kunnen de volgende afmetingen worden beïnvloed door de resultaten van de [!DNL Page View Condition]:

* **[!DNL URI]en  [!DNL Page]:** Deze afmetingen worden rechtstreeks beïnvloed door de  [!DNL Page View Condition]. Als de opgegeven pagina niet de [!DNL Page View Condition,] doorgeeft, wordt deze niet opgenomen in de URI- of paginaafmetingen.

* **[!DNL Visitor Page Views]en  [!DNL Session Page Views]:** De weergaven Paginaweergave van bezoekers en Paginaweergaven van sessie zijn een aantal pagina&#39;s die worden weergegeven door een bezoeker van of in een bepaalde sessie. Pagina&#39;s die worden uitgefilterd door de [!DNL Page View Condition] maken geen deel uit van deze telling.

* **Sessienummer:** Het  [!DNL Page View Condition] heeft een indirect effect op de dimensie Sessienummer. De dimensie van het Aantal van de Zitting wordt gecreeerd voorafgaand aan [!DNL Page View Condition]; Wanneer u [!DNL Session Number] in relatie tot [!DNL Page Views] overweegt, is het daarom mogelijk om sessies zonder paginaweergaven te hebben.

Uw standaardimplementatie van [!DNL Site] omvat een [!DNL Transformation Dataset Include] dossier waarin de telbare dimensie van de Mening van de Pagina en verwante [!DNL Page View Condition] worden bepaald.

Voor informatie over telbare afmetingen, zie [Uitgebreide Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

**De configuratie-instellingen voor de weergavevoorwaarde Pagina bewerken**

1. Open [!DNL Profile Manager] binnen uw datasetprofiel en open het [!DNL Dataset\Transformation\Traffic\Page View.cfg] dossier.

   >[!NOTE]
   >
   >Als u uw implementatie van [!DNL Site] hebt aangepast, kan het dossier waarin deze configuratiemontages bestaan van de beschreven plaats verschillen.

1. Controleer of bewerk indien nodig de waarden van de parameters van [!DNL Page View Condition]. Gebruik het volgende voorbeeld als richtlijn. In dit bestand wordt [!DNL Page View Condition] gedefinieerd door een [!DNL Copy]-transformatie. Merk op dat dit dossier ook de definitie van de telbare afmeting van de Mening van de Pagina bevat.

   ![](assets/cfg_WebParameters_PageView.png)

   >[!NOTE]
   >
   >Voor informatie over telbare afmetingen, zie [Uitgebreide Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md). Zie [Gegevenstransformaties](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md) voor informatie over de [!DNL Copy]-transformatie.

1. Sla het bestand op door met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster te klikken en vervolgens **[!UICONTROL Save]** te klikken.

1. Als u wilt dat de lokaal aangebrachte wijzigingen van kracht worden, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## URI Dimension {#section-348f7e9099d049d197a7cdcbc8a6c234}

Als u met [!DNL Site] werkt, moet u de afmeting van URI bepalen waarvan de elementen de URI stammen van de bekeken website pagina&#39;s zijn. Uw standaardimplementatie omvat een [!DNL Transformation Dataset Include] dossier waarin de eenvoudige afmeting van URI wordt bepaald.

Voor informatie over eenvoudige afmetingen, zie [Uitgebreide Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

**De configuratie-instellingen voor de URI-dimensie bewerken**

1. Open [!DNL Profile Manager] binnen uw datasetprofiel en open het [!DNL Dataset\Transformation\Traffic\URI.cfg] dossier.

   >[!NOTE]
   >
   >Als u uw implementatie van [!DNL Site] hebt aangepast, kan het dossier waarin deze configuratiemontages bestaan van de beschreven plaats verschillen.

1. Controleer of bewerk de waarden van de parameters van het bestand naar wens. Gebruik het volgende voorbeeld en informatie als hulplijnen.

![](assets/cfg_WebParameters_URI.png)

De configuratie-instellingen voor de URI-dimensie omvatten de volgende twee parameters:

* **Hoofdlettergevoelig:** Waar of Onwaar. Indien waar (true), wordt hoofdletter (boven/onder) gebruikt bij het identificeren van unieke pagina&#39;s. De standaardwaarde is true.
* **Maximum aantal elementen:** het maximum aantal elementen (dat wil zeggen URI&#39;s) voor de URI-dimensie. De standaardwaarde is 32768.

   >[!NOTE]
   >
   >Als u deze waarde wijzigt, kunnen er ernstige prestatieproblemen optreden. Wijzig deze waarde niet zonder Adobe te raadplegen.

* Sla het [!DNL URI.cfg]-bestand op door met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster te klikken en vervolgens **[!UICONTROL Save]** te klikken.

* Als u wilt dat de lokaal aangebrachte wijzigingen van kracht worden, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## Referrer Dimension {#section-8a97ec34d18b4814b5f95495ac4f8638}

Als u met [!DNL Site] werkt, moet u de afmeting van de Referateur bepalen de waarvan elementen uit de tweede niveaudomeinen van de verwijzingen van de eerste logboekingangen in alle zittingen bestaan. Uw standaardimplementatie omvat een [!DNL Transformation Dataset Include] dossier waarin de eenvoudige afmeting van de Referrer wordt bepaald.

Voor informatie over eenvoudige afmetingen, zie [Uitgebreide Dimension](../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

**De configuratie-instellingen voor de verwijzingsdimensie bewerken**

1. Open [!DNL Profile Manager] binnen uw datasetprofiel en open het [!DNL Dataset\Transformation\Traffic\Referrer.cfg] dossier.

   >[!NOTE]
   >
   >Als u uw implementatie van [!DNL Site] hebt aangepast, kan het dossier waarin deze configuratiemontages bestaan van de beschreven plaats verschillen.

1. Controleer of bewerk de waarden van de parameters van het bestand naar wens. Gebruik het volgende voorbeeld en informatie als hulplijnen.

   ![](assets/cfg_WebParameters_Referrer.png)

   De configuratiemontages voor de afmeting van de Verwijzer omvatten de Maximum parameter van Elementen, die het maximumaantal elementen (namelijk verwijzingen) voor de afmeting van de Verwijzing specificeert. De standaardwaarde is 32768.

   >[!NOTE]
   >
   >In het bovenstaande voorbeeld is de parameter [!DNL Maximum Elements] ingesteld op 0. Wanneer deze parameter op 0 wordt geplaatst, gebruikt de server van de gegevenswerkbank zijn interne standaardwaarde van 32768.

1. Sla het [!DNL Referrer.cfg]-bestand op door met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster te klikken en vervolgens **[!UICONTROL Save]** te klikken.

1. Als u wilt dat de lokaal aangebrachte wijzigingen van kracht worden, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

## Sessieparameters {#section-0a209b0c504041a5801f7f71a963c8b1}

Als u met [!DNL Site] werkt, kunt u parameters specificeren die de grenzen van de zitting van een bezoeker op een website bepalen. Deze parameters zijn alleen geldig wanneer ze zijn gedefinieerd in een [!DNL Transformation Dataset Include]-bestand in uw [!DNL Site]-implementatie.

De volgende parameters zijn uniek in die zin dat zij lid kunnen zijn van [!DNL Transformation Dataset Include] vector van het dossier [!DNL Parameters], of zij kunnen als individuele parameters in [!DNL Transformation.cfg]dossier worden vermeld. Een parameter kan precies één keer worden gedefinieerd, zodat deze parameters in het [!DNL Transformation.cfg]bestand of in de [!DNL Parameters]-vector van de dataset bestand opnemen - niet in beide bestanden worden gedefinieerd.
**Maximale sessieduur en sessietime-out**

Maximale sessieduur en sessietime-out zijn tekenreeksparameters die de lengte van de sessie van een bezoeker definiëren. Deze parameters werken met de parameter Interne domeinen om de sessielengte te bepalen.

Met Maximale sessieduur wordt de langste duur van de sessie opgegeven voordat een nieuwe sessie wordt gestart. Zo blijven webpagina&#39;s waarvan de inhoud automatisch wordt vernieuwd, bestaan uit het maken van sessies die willekeurig lang zijn. Als de referentie van een klik aan één van de ingangen in de Interne parameter van Domeinen wordt geplaatst, wordt deze onderbreking gebruikt om het eind van een zitting te bepalen. Geen enkele sessie kan langer zijn dan de opgegeven maximale sessieduur, ongeacht het aantal klikken dat deze bevat. De aanbevolen waarde is 48 uur.

De Onderbreking van de zitting specificeert de hoeveelheid tijd die tussen logboekingangen van een bepaalde bezoeker moet overgaan om het eind van één zitting en het begin van een nieuwe zitting te bepalen (namelijk de typische onderbreking die wordt gebruikt om een gebruikerszitting te bepalen). De aanbevolen waarde van deze parameter is 30 minuten. Als de referentie van een klik niet aan één van de verwijzingen in de Interne parameter van Domeinen wordt geplaatst, wordt deze onderbreking gebruikt om de zitting te bepalen. Als cs (verwijzing-domein) voor een logboekingang in de lijst van interne domeinen is, dan bepaalt de Maximale Duur van de Zitting of de huidige logboekingang deel van een bestaande zitting of het begin van een nieuwe zitting uitmaakt.

Neem bijvoorbeeld een situatie waarin een bezoeker tijdens het bladeren door de site voor een langere periode dan de time-out voor de sessie wordt afgeroepen van zijn computer. Na zijn terugkeer, blijft hij doorbladeren waar hij wegging. Omdat de bezoeker de site nooit verlaat of zijn browser sluit, is de cs(reference-domain) van de volgende klik hetzelfde als het interne domein en blijft de oorspronkelijke sessie actief zolang de instelling Maximale duur sessie niet is bereikt. Als het domein van de site wordt vermeld als een intern domein en de maximale time-out niet wordt bereikt, wordt de interactie van de bezoeker weergegeven als één sessie en niet als twee afzonderlijke sessies. Als de bezoeker echter terugkeert naar zijn computer en de volgende klik een externe (of lege) referentie heeft, wordt een nieuwe sessie gestart.

>[!NOTE]
>
>De [!DNL Sessionize] transformatie [!DNL Timeout Condition] speelt ook een rol in het bepalen van de lengte van de zitting van een bezoeker. Als de Onderbreking van de Zitting en Maximale Duur van de Zitting niet van toepassing zijn, [!DNL Timeout Condition] wordt gecontroleerd om te bepalen of een logboekingang als begin van een nieuwe zitting zou moeten worden beschouwd. Zie [Gegevenstransformaties](../../../home/c-dataset-const-proc/c-data-trans/c-abt-transf.md) voor meer informatie.

**De parameters Maximale sessieduur en Sessietime-out bewerken**

Als u met [!DNL Site] werkt, omvat uw standaardimplementatie waarschijnlijk een [!DNL Transformation Dataset Include] dossier waarin de namen en de geadviseerde waarden van deze parameters worden gespecificeerd.

1. Open [!DNL Profile Manager] binnen uw datasetprofiel en ga naar [!DNL Dataset\Transformation\Traffic\Session Parameters.cfg].

   >[!NOTE]
   >
   >Als u de implementatie van [!DNL Site] hebt aangepast, kan het bestand waarin deze parameters zijn gedefinieerd afwijken van de beschreven locatie.

1. Bewerk de waarden van de parameters naar wens. Geef de gewenste eenheden op (minuten, uren, enzovoort).

   ![](assets/cfg_WebParameters_SessionParameters.png)

1. Sla het [!DNL Session Parameters.cfg]-bestand op door met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster te klikken en **[!UICONTROL Save]** te klikken.

1. Als u wilt dat de lokaal aangebrachte wijzigingen van kracht worden, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en vervolgens op **[!UICONTROL Save to]** > **[!UICONTROL profile name]**, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset inclusief bestand behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

**[!DNL Internal Domains]**

[!DNL Internal Domains] is een vectorparameter die een lijst maakt van hosts op domeinniveau (interne referenties) die als onderdeel van een bepaalde website moeten worden behandeld. Deze gastheren worden verwijderd uit de verwijzingsdimensie (die een lijst van de externe verwijzersinformatie is). Wanneer cs(reference-domain) overeenkomt met een van de tekenreeksen die in de set interne domeinen worden vermeld, wordt de Time-out voor sessie genegeerd en wordt de maximale sessieduur gebruikt om de sessielengte te bepalen.

De parameter Interne domeinen kan ook worden gebruikt om het begin van een nieuwe zitting te verhinderen wanneer de bezoekers zich onder de veelvoudige domeinen van een bedrijf bewegen verbonden op een manier die zittingsonderbreking overschrijdt. Neem bijvoorbeeld een bedrijf dat delen van zijn site heeft die over twee domeinen zijn gesplitst: één wordt geregistreerd ( [!DNL xyz.com]), en andere wordt niet geregistreerd ( [!DNL xyz-unlogged.com]). Als deze plaatsen op een manier worden geïntegreerd die de naadloze beweging van verkeer over de twee domeinen vergemakkelijkt, is het niet wenselijk om een verschillende zitting te produceren telkens als de bezoeker zich van [!DNL xyz-unlogged.com] domein terug naar [!DNL xyz.com] domein beweegt. Als u [!DNL xyz-unlogged.com] als intern domein opgeeft, worden sessies niet gesplitst in meerdere sessies als gevolg van verkeer over deze twee domeinen zolang de instelling Maximale sessieduur niet is bereikt.

**Een intern domein toevoegen**

Als u met [!DNL Site] werkt, bevat uw standaardimplementatie een [!DNL Transformation Dataset Include]-bestand voor het definiëren van de parameter Interne domeinen. In dit bestand wordt de parameter benoemd. Voer alleen de interne domeinen in die u wilt opnemen en sla het bijgewerkte bestand op.

1. Open [!DNL Profile Manager] binnen uw datasetprofiel en ga naar [!DNL Dataset\Transformation\Traffic\Internal Domains.cfg.]

   >[!NOTE]
   >
   >Als u de implementatie van [!DNL Site] hebt aangepast, kan het bestand waarin de parameter Interne domeinen is gedefinieerd afwijken van de beschreven locatie.

1. Klik met de rechtermuisknop **[!UICONTROL Value]** voor de vectorparameter Interne domeinen en klik **[!UICONTROL Add new]** > **[!UICONTROL Value]**.

1. Bewerk de waarden naar wens.

   ![](assets/cfg_WebParameters_InternalDomains.png)

1. Sla het [!DNL Internal Domains.cfg]-bestand op door met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster te klikken en **[!UICONTROL Save]** te klikken.

1. Als u wilt dat de lokaal aangebrachte wijzigingen van kracht worden, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

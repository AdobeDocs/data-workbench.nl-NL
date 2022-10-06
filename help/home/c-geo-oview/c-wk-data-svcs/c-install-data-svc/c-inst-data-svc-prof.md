---
description: De profielen van de gegevensdienst (IP Geo-intelligentie en IP Geo-location) zijn interne profielen die extra functionaliteit aan uw toepassing van de Adobe verstrekken.
title: Het profiel voor de gegevensservice installeren
uuid: 1c03d0cd-7eaa-4e48-bbff-8bfad8fed9e9
exl-id: 51d080bb-f874-426c-91ea-3912ffd38419
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Het profiel voor de gegevensservice installeren{#installing-the-data-service-profile}

{{eol}}

De profielen van de gegevensdienst (IP Geo-intelligentie en IP Geo-location) zijn interne profielen die extra functionaliteit aan uw toepassing van de Adobe verstrekken.

Net als bij alle andere interne profielen die door Adobe worden geleverd, mogen deze profielen niet worden gewijzigd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

De profielen van de gegevensdienst omvatten de volgende dataset dossiers die op een server van de gegevenswerkbank moeten worden geïnstalleerd:

* **Profielen\*profielnaam *\Gegevensset\Logverwerking\Verkeer\IP.cfg:** Maakt een lijst van het c-ip gebied dat van logboekverwerking aan transformatie moet worden overgegaan.
* **Profielen\*profielnaam *\Dataset\Transformation\Geography\IPLookup.cfg:** Bepaalt een transformatie IPLookup die verscheidene gebieden van geografische gegevens gebruikend het verstrekte IP Geo-intelligentie of IP Geo-location raadplegingsdossier veroorzaakt.

Voor informatie over transformatiedataset omvat dossiers, zie *Configuratie-handleiding voor gegevensset*.

Bovendien voorziet elk profiel van de gegevensdienst u van een dossier van de elementenpuntlaag genoemd [!DNL IP Coordinates.layer]. Dit laagdossier laat u toe om plaatsen in uw dataset op de wereld dynamisch in kaart te brengen gebruikend IP adressen. Na de installatie wordt de laag opgeslagen in de map Profiles\*data service name*\Maps in de installatiemap van de gegevenswerkbench-server.

De [!DNL IP Coordinates.layer] het dossier verwijst naar de dimensie van Coördinaten, die in [!DNL Coordinates.cfg] het dossier van [!DNL Geography] en bevindt zich in de map Dataset\Transformation\Geography. Elk element van de dimensie van Coördinaten die in uw dataset wordt bepaald wordt in kaart gebracht op de wereld gebruikend de breedte en lengteinformatie in dat element. Zie voor meer informatie over elementpuntlagen die dynamische punten gebruiken [Elementpuntlagen definiëren met behulp van dynamische punten](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3).

>[!NOTE]
>
>Als u IP Geo-intelligentie en IP de dienst van Geo-plaats gegevens voorafgaand aan versie 5.1 installeerde, verwijzingen uw dossier van de de laaglaag van het elementenpunt een raadplegingsdossier in plaats van het gebruiken van dynamische punten. Elk laagdossier verwijst naar het IP dossier van de Geocodes raadpleging en de IP dimensie Geocode. Het IP dossier van de raadpleging van Geocodes bevat een lijst van IP geocodes (geografische plaatsen die op IP adres worden gebaseerd) en de breedte en de lengte voor elk. Elk element van een IP Geocode die afmeting in uw dataset wordt bepaald wordt in kaart gebracht op de globe gebruikend de breedte en de lengtegraad die voor dat IP geocode in het IP dossier van de Geocodes worden vermeld.

De naam van het laagbestand en de bestanden waarnaar het verwijst, verschillen voor elke gegevensservice:

* De [!DNL IP Geocodes D.layer] wordt geïnstalleerd met het IP-profiel Geo-intelligence (Digital Envoy). Deze elementpuntlaag verwijst naar de [!DNL IP Geocodes D yyyymmdd.txt] opzoekbestand (dat u regelmatig moet bijwerken) en de IP Geocode D-dimensie.

* De [!DNL IP Geocodes Q.layer] Het bestand wordt geïnstalleerd met het IP-profiel Geo-location (Quova). Deze elementpuntlaag verwijst naar de [!DNL IP Geocodes Q yyyymmdd.txt] opzoekbestand (dat u regelmatig moet bijwerken) en de IP Geocode Q-dimensie.

Zie voor meer informatie over elementpuntlagen die opzoekbestanden gebruiken [Elementpuntlagen definiëren die verwijzen naar opzoekbestanden](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyrs-ref-lkp-files.md#concept-c40bd0890a984112bce831b596827f0f).

## IP Geo-intelligentie of IP Geo-location profiel installeren {#section-6dff402ffdcb4b31b9bcd0c40a5f7625}

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u de gegevenswerkbank hebt geïnstalleerd en een verbinding tot stand hebt gebracht tussen de gegevenswerkbank en de gegevenswerkbench-server waarop u de gegevenswerkbank installeert [!DNL Geography]. Als u dit niet hebt gedaan, raadpleegt u de *Gebruikershandleiding voor Data Workbench*.

1. Open de map Profielen in het menu [!DNL .zip] bestand dat u hebt ontvangen van Adobe.
1. Kopieer de IP-map Geo-intelligence of IP Geo-location naar de map Profiles in de installatiemap van de gegevenswerkbank. U wilt eindigen met een ...\Profiles\IP Geo-intelligence-map of a..\Profiles\IP Geo-location op uw gegevenswerkbankserver, zoals in het volgende voorbeeld wordt getoond. De namen van de andere mappen in de [!DNL Profiles] kan verschillen van de weergegeven mappen.

   ![](assets/Geo_installProfiles_dirIP.png)

1. Gebruik de volgende stappen om de [!DNL profile.cfg] bestand voor elk profiel waarmee u het [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] profiel.

   1. Open de **[!UICONTROL Profile Manager]**.
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De [!DNL profile.cfg] wordt weergegeven.

   1. In de [!DNL profile.cfg]venster, klik met de rechtermuisknop **[!UICONTROL Directories]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Als u de nieuwe map wilt toevoegen aan het einde van de lijst met mappen, klikt u met de rechtermuisknop op het nummer of de naam van de laatste map in de lijst en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe map: [!DNL IP Geo-intelligence] of I [!DNL P Geo-location].

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

>[!NOTE]
>
>Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die worden geleverd door Adobe (inclusief de [!DNL IP Geo-location] of [!DNL IP Geo-intelligence] ), aangezien uw veranderingen worden beschreven wanneer u updates aan deze profielen installeert.

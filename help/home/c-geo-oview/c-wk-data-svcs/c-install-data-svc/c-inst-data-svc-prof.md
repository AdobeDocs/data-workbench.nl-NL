---
description: De profielen van de datadienst (IP Geo-intelligence en IP Geo-location) zijn interne profielen die extra functionaliteit aan uw toepassing van Adobe verstrekken.
solution: Analytics
title: Het profiel van de gegevensservice installeren
topic: Data workbench
uuid: 1c03d0cd-7eaa-4e48-bbff-8bfad8fed9e9
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het profiel van de gegevensservice installeren{#installing-the-data-service-profile}

De profielen van de datadienst (IP Geo-intelligence en IP Geo-location) zijn interne profielen die extra functionaliteit aan uw toepassing van Adobe verstrekken.

Zoals met alle andere interne profielen die door Adobe worden verstrekt, zouden deze profielen niet moeten worden veranderd. Al aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

De profielen van de datadienst omvatten de volgende dataset dossiers die op een server van de gegevenswerkbank moeten worden geïnstalleerd:

* **Profielen\*profielnaam *\Dataset\Log Processing\Traffic\IP.cfg:** Maakt een lijst van het c-ip- gebied dat van logboekverwerking aan transformatie moet worden overgegaan.
* **Profielen \*profielnaam *\Dataset\Transformation\Geography\IPLookup.cfg:** bepaalt een transformatie IPLookup die verscheidene gebieden van geografische gegevens gebruikend verstrekt IP geointelligentie of IP Geo-location raadplegingsdossier veroorzaakt.

Voor informatie over transformatiedataset omvat dossiers, zie de Gids *van de Configuratie van de* Dataset.

Bovendien voorziet elk profiel van de datadienst u van een dossier van de elementenpuntlaag genoemd [!DNL IP Coordinates.layer]. Dit laagdossier laat u toe om plaatsen in uw dataset op de bol dynamisch in kaart te brengen gebruikend IP adressen. Na installatie, wordt de laag opgeslagen in de de dienstnaam van Profielen \*gegevens de omslag van Kaarten \ in de de installatiefolder van de gegevenswerkbank server.

De [!DNL IP Coordinates.layer] dossierverwijzingen de afmeting van Coördinaten, die in het [!DNL Coordinates.cfg] dossier wordt bepaald dat van het [!DNL Geography] profiel wordt voorzien en in Dataset\Transformation\Geography folder wordt gevestigd. Elk element van de afmeting van Coördinaten die in uw dataset wordt bepaald wordt in kaart gebracht op de bol gebruikend de breedtegraad en lengteinformatie in dat element. Voor meer informatie over de lagen van het elementpunt die dynamische punten gebruiken, zie het [Bepalen van de Lagen van het Punt van het Element Gebruikend Dynamische Punten](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3).

>[!NOTE]
>
>Als u de IP Geo-intelligentie en IP de dienst van geolocatie gegevens voorafgaand aan versie 5.1 installeerde, de het dossierverwijzingen van uw elementenpunt een raadplegingsdossier in plaats van het gebruiken van dynamische punten. Elke verwijzing van het laagdossier het IP dossier van de coderaadpleging van Geocodes en de IP dimensie Geocode. Het IP dossier van de coderaadpleging van Geocodes bevat een lijst van IP geocodes (geografische plaatsen die op IP adres worden gebaseerd) en de breedte en de lengtegraad voor elk. Elk element van een IP dimensie van de Geocode die in uw dataset wordt bepaald wordt in kaart gebracht op de bol gebruikend de breedte en de lengtegraad die voor die IP geo-code in het IP dossier van de de coderaadpleging van Geocodes wordt vermeld.

De naam van het laagdossier en de dossiers dat het verwijzingen voor elke datadienst verschillen:

* Het [!DNL IP Geocodes D.layer] dossier is geïnstalleerd met het IP Geo-Intelligentie (Digitale Gezant) profiel. Dit element richt laagverwijzingen het [!DNL IP Geocodes D yyyymmdd.txt] raadplegingsdossier (dat u periodiek) en de IP dimensie van Geocode D moet bijwerken.

* Het [!DNL IP Geocodes Q.layer] dossier is geïnstalleerd met het IP Geo-Plaats (Quova) profiel. Dit element richt laagverwijzingen het [!DNL IP Geocodes Q yyyymmdd.txt] raadplegingsdossier (dat u periodiek) en de IP dimensie van Geocode Q moet bijwerken.

Voor meer informatie over de lagen van het elementenpunt die raadplegingsdossiers gebruiken, zie het [Bepalen van de Lagen van het Punt van het Element die de Dossiers](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyrs-ref-lkp-files.md#concept-c40bd0890a984112bce831b596827f0f)van de Raadpleging van het Refereren van.

## Om IP Geo-intelligentie of IP Geo-locatieprofiel te installeren {#section-6dff402ffdcb4b31b9bcd0c40a5f7625}

>[!NOTE]
>
>De volgende installatieinstructies veronderstellen dat u een werkbank voor gegevens hebt geïnstalleerd en een verbinding tussen de werkbank voor gegevens en de server van de gegevenswerkbank hebt gevestigd waarop u de werkbank voor gegevens installeert [!DNL Geography]. Als u dit niet hebt gedaan, zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.

1. Open de omslag van Profielen van het [!DNL .zip] dossier dat u van Adobe ontving.
1. Kopieer de IP Geo-intelligentie of IP Geo-locatieomslag aan de omslag van Profielen in uw de installatiefolder van de gegevenswerkbank. Je wilt eindigen met een ...\Profiles\IP Geo-intelligence folder or a ...\Profiles\IP Geo-location on your data workbench server as shown in the following example. De namen van de andere omslagen binnen de [!DNL Profiles] omslag kunnen van getoond verschillen.

   ![](assets/Geo_installProfiles_dirIP.png)

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor elk profiel bij te werken waarmee u het [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] profiel wilt gebruiken.

   1. Open de **[!UICONTROL Profile Manager]**.
   1. Klik het vinkje naast met de rechtermuisknop aan [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

   1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL profile.cfg] venster wordt weergegeven.

   1. Klik in het [!DNL profile.cfg]venster met de rechtermuisknop **[!UICONTROL Directories]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Om de nieuwe folder aan het eind van de lijst van folders toe te voegen, klik het aantal of de naam van de laatste folder in de lijst met de rechtermuisknop aan en klik **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe folder: [!DNL IP Geo-intelligence] of ik [!DNL P Geo-location].

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in de [!DNL Profile Manager], rechtsklik op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

>[!NOTE]
>
>Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd (inclusief het [!DNL IP Geo-location] of het [!DNL IP Geo-intelligence] profiel), omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.


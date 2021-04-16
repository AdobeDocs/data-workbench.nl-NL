---
description: De profielen van de gegevensdienst (IP Geo-intelligentie en IP Geo-location) zijn interne profielen die extra functionaliteit aan uw toepassing van de Adobe verstrekken.
title: Het profiel voor de gegevensservice installeren
uuid: 1c03d0cd-7eaa-4e48-bbff-8bfad8fed9e9
exl-id: 51d080bb-f874-426c-91ea-3912ffd38419
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Het profiel voor de gegevensservice installeren{#installing-the-data-service-profile}

De profielen van de gegevensdienst (IP Geo-intelligentie en IP Geo-location) zijn interne profielen die extra functionaliteit aan uw toepassing van de Adobe verstrekken.

Net als bij alle andere interne profielen die door Adobe worden geleverd, mogen deze profielen niet worden gewijzigd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

De profielen van de gegevensdienst omvatten de volgende dataset dossiers die op een server van de gegevenswerkbank moeten worden geïnstalleerd:

* **Profielen\*profielnaam *\Dataset\Log Processing\Traffic\IP.cfg:** Hiermee geeft u het veld c-ip weer dat wordt doorgegeven van logverwerking naar transformatie.
* **Profielen\*profielnaam *\Dataset\Transformation\Geography\IPLookup.cfg:** bepaalt een IPLookup transformatie die verscheidene gebieden van geografische gegevens gebruikend het verstrekte IP Geo-intelligentie of IP Geo-location raadplegingsdossier veroorzaakt.

Voor informatie over transformatiedataset omvat dossiers, zie *de Gids van de Configuratie van de Dataset*.

Bovendien voorziet elk profiel van de gegevensdienst u van een dossier van de elementenpuntlaag genoemd [!DNL IP Coordinates.layer]. Dit laagdossier laat u toe om plaatsen in uw dataset op de wereld dynamisch in kaart te brengen gebruikend IP adressen. Na de installatie wordt de laag opgeslagen in de map Profiles\*data service name*\Maps in de installatiemap van de gegevenswerkbench-server.

Het [!DNL IP Coordinates.layer] dossier verwijst naar de dimensie van Coördinaten, die in [!DNL Coordinates.cfg] dossier wordt bepaald dat met het [!DNL Geography] profiel wordt voorzien en in Dataset\Transformation\Geography folder wordt gevestigd. Elk element van de dimensie van Coördinaten die in uw dataset wordt bepaald wordt in kaart gebracht op de wereld gebruikend de breedte en lengteinformatie in dat element. Zie [Elementpuntlagen definiëren met dynamische punten](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3) voor meer informatie over elementpuntlagen die dynamische punten gebruiken.

>[!NOTE]
>
>Als u IP Geo-intelligentie en IP de dienst van Geo-plaats gegevens voorafgaand aan versie 5.1 installeerde, verwijzingen uw dossier van de de laaglaag van het elementenpunt een raadplegingsdossier in plaats van het gebruiken van dynamische punten. Elk laagdossier verwijst naar het IP dossier van de Geocodes raadpleging en de IP dimensie Geocode. Het IP dossier van de raadpleging van Geocodes bevat een lijst van IP geocodes (geografische plaatsen die op IP adres worden gebaseerd) en de breedte en de lengte voor elk. Elk element van een IP Geocode die afmeting in uw dataset wordt bepaald wordt in kaart gebracht op de globe gebruikend de breedte en de lengtegraad die voor dat IP geocode in het IP dossier van de Geocodes worden vermeld.

De naam van het laagbestand en de bestanden waarnaar het verwijst, verschillen voor elke gegevensservice:

* Het [!DNL IP Geocodes D.layer]-bestand wordt geïnstalleerd met het IP-profiel Geo-intelligence (Digital Envoy). Deze elementpuntlaag verwijst naar het [!DNL IP Geocodes D yyyymmdd.txt] opzoekbestand (dat u regelmatig moet bijwerken) en de IP Geocode D-dimensie.

* Het [!DNL IP Geocodes Q.layer] dossier wordt geïnstalleerd met IP Geo-location (Quova) profiel. Deze elementpuntlaag verwijst naar het [!DNL IP Geocodes Q yyyymmdd.txt] raadplegingsdossier (dat u periodiek moet bijwerken) en de IP dimensie van Geocode Q.

Voor meer informatie over de lagen van het elementpunt die raadplegingsdossiers gebruiken, zie [Bepalend de Lagen van het Punt van het Element Verwijzend de Dossiers van de Opzoekopdracht](../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyrs-ref-lkp-files.md#concept-c40bd0890a984112bce831b596827f0f).

## IP Geo-intelligentie of IP Geo-location profiel {#section-6dff402ffdcb4b31b9bcd0c40a5f7625} installeren

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u een werkbank voor gegevens hebt geïnstalleerd en een verbinding tot stand hebt gebracht tussen de gegevenswerkbank en de gegevenswerkbench-server waarop u de gegevenswerkbank [!DNL Geography] installeert. Als u dit niet hebt gedaan, zie *de Gids van de Gebruiker van de Data Workbench*.

1. Open de map Profielen in het [!DNL .zip]-bestand dat u van Adobe hebt ontvangen.
1. Kopieer de IP-map Geo-intelligence of IP Geo-location naar de map Profiles in de installatiemap van de gegevenswerkbank. U wilt eindigen met een ...\Profiles\IP Geo-intelligence folder or a ...\Profiles\IP Geo-location on your data workbench server as shown in the following example. De namen van de andere mappen in de map [!DNL Profiles] kunnen afwijken van de mappen die worden weergegeven.

   ![](assets/Geo_installProfiles_dirIP.png)

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor elk profiel bij te werken waarmee u [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] profiel wilt gebruiken.

   1. Open **[!UICONTROL Profile Manager]**.
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het venster [!DNL profile.cfg] verschijnt.

   1. Klik in het venster [!DNL profile.cfg]met de rechtermuisknop **[!UICONTROL Directories]** en klik **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Als u de nieuwe map wilt toevoegen aan het einde van de lijst met directory&#39;s, klikt u met de rechtermuisknop op het nummer of de naam van de laatste map in de lijst en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe map: [!DNL IP Geo-intelligence] of I [!DNL P Geo-location].

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

>[!NOTE]
>
>Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd (inclusief het profiel [!DNL IP Geo-location] of [!DNL IP Geo-intelligence]), omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

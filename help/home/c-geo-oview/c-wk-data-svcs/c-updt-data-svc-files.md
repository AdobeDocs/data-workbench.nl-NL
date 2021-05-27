---
description: Als u zich abonneert op een van de gegevensservices, moet u de gegevensservicebestanden die door Adobe worden aangeboden periodiek bijwerken.
title: Gegevensservicebestanden bijwerken
uuid: 8c14be34-fde3-4c4c-9c22-739863317d6e
exl-id: bb92d40c-cc8d-4ecf-bd48-ed962fd5d73b
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Gegevensservicebestanden bijwerken{#updating-data-service-files}

Als u zich abonneert op een van de gegevensservices, moet u de gegevensservicebestanden die door Adobe worden aangeboden periodiek bijwerken.

Hiervoor hebt u toegang nodig tot de bestanden op de gegevenswerkbankserver.

Als u [!DNL IP Geo-location] of [!DNL IP Geo-intelligence] gegevensbestanden wilt laden, moet u de volgende procedures voltooien.

## Gegevensbestand {#section-2b53c2951ae04c6fa8b3bdf080469ff6} vervangen

1. Klik op de **[!UICONTROL Servers Manager]**-miniatuur op de tab [!DNL Admin] > [!DNL Dataset and Profile] in de gegevenswerkbank om de [!DNL Servers Manager]-werkruimte te openen.

1. Klik in het venster [!DNL Servers Manager] met de rechtermuisknop op het pictogram van de gegevenswerkbankserver waarop u de bestanden wilt laden en klik op **[!UICONTROL Server Files]**.

1. Klik in [!DNL Server Files Manager] met de rechtermuisknop in de **[!UICONTROL Temp]**-kolom voor **[!UICONTROL Lookups\IP Geo-location]** of **[!UICONTROL Lookups\IP Geo-intelligence]** en klik **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]***.

1. Kopieer het gegevensbestand [!DNL .bin] dat door Adobe wordt verstrekt naar het de omslagvenster van Geo-Plaats van Lookups \ IP of van Lookups \ IP Geo-intelligentie.
1. Sla het bestand op de gegevenswerkbankservercomputer op door met de rechtermuisknop op de kolom [!DNL Temp] voor het gegevensbestand te klikken en op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>* te klikken.

   Als u een cluster uitvoert, uploadt u de bestanden naar de master gegevenswerkbankserver in de cluster.

## De IPLookup-transformatie {#section-a8b99afe3eb04afabe88e15bd465f935} bijwerken

1. Klik in [!DNL Profile Manager] op **[!UICONTROL Dataset]**, **[!UICONTROL Transformation]** en **[!UICONTROL Geography]**.

1. Klik met de rechtermuisknop op het vinkje naast [!DNL IP Lookup.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Er wordt een venster voor transformatieconfiguratie weergegeven.

1. Klik in het venster op **[!UICONTROL Transformation]** en vervolgens op **[!UICONTROL Transformations]**.

1. Zoek en klik op **[!UICONTROL IPLookup Quova]** of **[!UICONTROL IPLookup Digital Envoy]**.

1. Werk voor de parameter File de naam van het bestand bij, zodat deze overeenkomt met de naam van het nieuwe gegevensbestand ( [!DNL .bin]) dat door Adobe wordt geleverd.
1. Sla het transformatieconfiguratiebestand op door met de rechtermuisknop **[!UICONTROL (modified)]** boven aan het configuratievenster te klikken en **[!UICONTROL Save]** te klikken.

1. Sla het gewijzigde configuratiebestand op in elk profiel dat de gegevensservice gebruikt. Klik hiertoe met de rechtermuisknop op het vinkje naast [!DNL IP Lookup.cfg] in de kolom [!DNL User] en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*. De gegevens worden opnieuw getransformeerd nadat het gegevenssetprofiel is gesynchroniseerd.

   Voor informatie over hertransformatie van uw dataset, zie het hoofdstuk van de Verwerking en van de Hervorming van *Gids van de Configuratie van de Dataset*.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd (inclusief het profiel [!DNL IP Geo-location] of [!DNL IP Geo-intelligence]), omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

Als u de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] gegevensservice voor versie 5.1 of later hebt geïnstalleerd, hebt u de update van de gegevensservice voltooid. Als u echter de [!DNL IP Geo-intelligence]- en [!DNL IP Geo-location]-gegevensservice vóór versie 5.1 hebt geïnstalleerd, moet u de volgende aanvullende procedures doorlopen.

## Opzoekbestand {#section-ced1efa38a76419d812edd35423dbff7} vervangen

Voer de volgende stappen alleen uit als u de [!DNL IP Geo-intelligence]- en [!DNL IP Geo-location]-gegevensservice vóór versie 5.1 hebt geïnstalleerd.

1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-intelligence]** of **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-location]** en klik vervolgens op **[!UICONTROL Maps]** om de inhoud ervan weer te geven.

1. Klik met de rechtermuisknop in de kolom **[!UICONTROL Temp]** voor **[!UICONTROL Maps]** en klik **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]**>*.

1. Kopieer het nieuwe [!DNL .txt] dossier door Adobe aan het de omslagvenster van Kaarten wordt verstrekt.
1. Sla het bestand op de gegevenswerkbankservercomputer op door met de rechtermuisknop op het vinkje in de kolom [!DNL Temp] voor het bestand [!DNL .txt] te klikken en op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>* te klikken.

>[!NOTE]
>
>Als u een cluster uitvoert, uploadt u de bestanden naar de master gegevenswerkbankserver in de cluster.

## De laagbestanden {#section-8b84e7099bad40c9a69665a4890fe66e} bijwerken

>[!NOTE]
>
>Voer de volgende stappen alleen uit als u de [!DNL IP Geo-intelligence]- en [!DNL IP Geo-location]-gegevensservice vóór versie 5.1 hebt geïnstalleerd.

Voer deze stappen uit voor elk laagbestand ( [!DNL .layer]) dat verwijst naar het opzoekbestand [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] ( [!DNL .txt]).

1. Open het [!DNL .layer]-bestand in een teksteditor, zoals Kladblok, in de map Profiles\*data service name*\Maps in de installatiemap van de gegevenswerkbank.

1. Werk in de [!DNL Data Paths]-vector de naam van het [!DNL .txt]-opzoekbestand bij, zodat deze overeenkomt met de naam van het nieuwe [!DNL .txt]-bestand dat wordt geleverd door Adobe, zoals wordt weergegeven in het volgende bestandsvoorbeeld:

   ```
   Layer = ElementPointLayer:
     Data Paths = vector: 1 items
       0 = Path: Maps\\LookupFileName.txt
     Longitude Column = string: LongitudeColumnName
     Latitude Column = string: LatitudeColumnName
     Name Column = string: LocationColumnName
     Key Column = string: KeyColumnName
     Dimension = ref: wdata/model/dim/DimensionName
     Metric = ref: wdata/model/metric/MetricName
   ```

1. Sla het bijgewerkte laagbestand op.
1. Herhaal stap 2 en 3 voor elk [!DNL .layer]-bestand dat verwijst naar het [!DNL IP Geo-intelligence]- of [!DNL IP Geo-location] [!DNL .txt]-bestand.

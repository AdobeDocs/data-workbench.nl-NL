---
description: Als u zich abonneert op een van de gegevensservices, moet u de gegevensservicebestanden die door Adobe worden aangeboden periodiek bijwerken.
title: Gegevensservicebestanden bijwerken
uuid: 8c14be34-fde3-4c4c-9c22-739863317d6e
exl-id: bb92d40c-cc8d-4ecf-bd48-ed962fd5d73b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# Gegevensservicebestanden bijwerken{#updating-data-service-files}

{{eol}}

Als u zich abonneert op een van de gegevensservices, moet u de gegevensservicebestanden die door Adobe worden aangeboden periodiek bijwerken.

Hiervoor hebt u toegang nodig tot de bestanden op de gegevenswerkbankserver.

Te laden [!DNL IP Geo-location] of [!DNL IP Geo-intelligence] gegevensbestanden, moet u de volgende procedures voltooien.

## Het gegevensbestand vervangen {#section-2b53c2951ae04c6fa8b3bdf080469ff6}

1. Op de werkbank Gegevens, op de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** miniatuur om de [!DNL Servers Manager] werkruimte.

1. Binnen de [!DNL Servers Manager] venster, klikt u met de rechtermuisknop op het pictogram van de gegevenswerkbankserver waarop u de bestanden wilt laden en klikt u op **[!UICONTROL Server Files]**.

1. In de [!DNL Server Files Manager], klikt u met de rechtermuisknop in het dialoogvenster **[!UICONTROL Temp]** kolom voor **[!UICONTROL Lookups\IP Geo-location]** of **[!UICONTROL Lookups\IP Geo-intelligence]** en klik op **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]**>*.

1. Kopieer de [!DNL .bin] gegevensbestand dat door Adobe wordt verstrekt aan het IP van Lookups Geo-location of Lookups \ IP Geo-intelligence omslagvenster.
1. Sla het bestand op de gegevenswerkbankserver op door met de rechtermuisknop op de [!DNL Temp] kolom voor het gegevensbestand en het klikken **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

   Als u een cluster uitvoert, uploadt u de bestanden naar de master gegevenswerkbankserver in de cluster.

## De IPLookup-transformatie bijwerken {#section-a8b99afe3eb04afabe88e15bd465f935}

1. In de [!DNL Profile Manager], klikt u op **[!UICONTROL Dataset]**, **[!UICONTROL Transformation]**, en **[!UICONTROL Geography]**.

1. Klik met de rechtermuisknop op het vinkje naast [!DNL IP Lookup.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.

1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Er wordt een venster voor transformatieconfiguratie weergegeven.

1. Klik in het venster op **[!UICONTROL Transformation]** en klik vervolgens op **[!UICONTROL Transformations]**.

1. Zoeken en klikken op **[!UICONTROL IPLookup Quova]** of **[!UICONTROL IPLookup Digital Envoy]**.

1. Werk voor de parameter File de naam van het bestand bij zodat deze overeenkomt met de naam van de nieuwe gegevens ( [!DNL .bin]) opgegeven door Adobe.
1. Sla het transformatieconfiguratiebestand op door met de rechtermuisknop te klikken **[!UICONTROL (modified)]** boven aan het configuratievenster en klikken op **[!UICONTROL Save]**.

1. Sla het gewijzigde configuratiebestand op in elk profiel dat de gegevensservice gebruikt door met de rechtermuisknop op het vinkje naast [!DNL IP Lookup.cfg] in de [!DNL User] kolom en klikken **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*. De gegevens worden opnieuw getransformeerd nadat het gegevenssetprofiel is gesynchroniseerd.

   Voor informatie over retransformation van uw dataset, zie het hoofdstuk van de Verwerking en van de Hervorming van *Configuratie-handleiding voor gegevensset*.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die worden geleverd door Adobe (inclusief de [!DNL IP Geo-location] of [!DNL IP Geo-intelligence] ), aangezien uw veranderingen worden beschreven wanneer u updates aan deze profielen installeert.

Als u de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] de datadienst voor versie 5.1 of later, hebt u de update van de datadienst voltooid. Als u echter de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] Voor versie 5.1 moet u de volgende aanvullende procedures voltooien.

## Opzoekbestand vervangen {#section-ced1efa38a76419d812edd35423dbff7}

Voer de volgende stappen alleen uit als u de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] datadienst voorafgaand aan versie 5.1.

1. In de [!DNL Server Files Manager]Klik op een van de **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-intelligence]** of **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-location]** en klik vervolgens op **[!UICONTROL Maps]** om de inhoud te bekijken.

1. Klik met de rechtermuisknop in het dialoogvenster **[!UICONTROL Temp]** kolom voor **[!UICONTROL Maps]** en klik op **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]**>*.

1. Nieuw kopiëren [!DNL .txt] bestand dat door Adobe aan het Maps-mapvenster wordt geleverd.
1. Sla het bestand op de gegevenswerkbankserver op door met de rechtermuisknop op het vinkje in het dialoogvenster [!DNL Temp] kolom voor de [!DNL .txt] bestand en klikken **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

>[!NOTE]
>
>Als u een cluster uitvoert, uploadt u de bestanden naar de master gegevenswerkbankserver in de cluster.

## De laagbestanden bijwerken {#section-8b84e7099bad40c9a69665a4890fe66e}

>[!NOTE]
>
>Voer de volgende stappen alleen uit als u de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] datadienst voorafgaand aan versie 5.1.

Voer de volgende stappen uit voor elke laag ( [!DNL .layer]) dat verwijst naar het [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] lookup ( [!DNL .txt]).

1. Open in de map Profiles\*data service name*\Maps in de installatiemap van de gegevenswerkbench-server de map [!DNL .layer] bestand in een teksteditor, zoals Kladblok.

1. In de [!DNL Data Paths] vector, de naam van de vector bijwerken [!DNL .txt] opzoekbestand dat overeenkomt met de naam van het nieuwe [!DNL .txt] bestand opgegeven door Adobe, zoals wordt weergegeven in het volgende bestandsvoorbeeld:

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
1. Herhaal stap 2 en 3 voor elke [!DNL .layer] bestand dat verwijst naar het [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] [!DNL .txt] bestand.

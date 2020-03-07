---
description: Als u aan één van beide datadienst intekent, moet u periodiek de dossiers bijwerken van de datadienst die door Adobe worden verstrekt.
solution: Analytics
title: Gegevensservicebestanden bijwerken
topic: Data workbench
uuid: 8c14be34-fde3-4c4c-9c22-739863317d6e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Gegevensservicebestanden bijwerken{#updating-data-service-files}

Als u aan één van beide datadienst intekent, moet u periodiek de dossiers bijwerken van de datadienst die door Adobe worden verstrekt.

Om dit te doen, moet u toegang tot de dossiers op de server van de gegevenswerkbank hebben.

Om [!DNL IP Geo-location] of [!DNL IP Geo-intelligence] gegevensdossiers te laden, moet u de volgende procedures voltooien.

## Het gegevensbestand vervangen {#section-2b53c2951ae04c6fa8b3bdf080469ff6}

1. In gegevenswerkbank, op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de [!DNL Servers Manager] werkruimte te openen.

1. Klik in het [!DNL Servers Manager] venster met de rechtermuisknop op het pictogram van de server van de gegevenswerkbank waarop u de bestanden wilt laden en op **[!UICONTROL Server Files]**.

1. Klik in de [!DNL Server Files Manager], rechtsklik in de **[!UICONTROL Temp]** kolom voor **[!UICONTROL Lookups\IP Geo-location]** of **[!UICONTROL Lookups\IP Geo-intelligence]** en klik op **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]**>*.

1. Kopieer het [!DNL .bin] gegevensdossier dat door Adobe aan de Geo-plaats van de Raadplegingen \ IP of IP van Raadplegingen wordt verstrekt Geo-Intelligentie omslagvenster van de Raadplegingen.
1. Sla het bestand op in het serversysteem van de gegevenswerkbank door met de rechtermuisknop op de [!DNL Temp] kolom voor het gegevensbestand te klikken en te klikken op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

   Als u een cluster in werking stelt, upload de dossiers aan de server van de hoofdgegevenswerkbank in de cluster.

## Het bijwerken van de Transformatie IPLookup {#section-a8b99afe3eb04afabe88e15bd465f935}

1. In [!DNL Profile Manager], klik **[!UICONTROL Dataset]**, **[!UICONTROL Transformation]**, en **[!UICONTROL Geography]**.

1. Klik het vinkje naast met de rechtermuisknop aan [!DNL IP Lookup.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

1. Klik het nieuwe vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Er verschijnt een venster voor transformatieconfiguratie.

1. In het venster, klik **[!UICONTROL Transformation]**, dan klik **[!UICONTROL Transformations]**.

1. Bepaal de plaats en klik of **[!UICONTROL IPLookup Quova]** of **[!UICONTROL IPLookup Digital Envoy]**.

1. Voor de parameter van het Dossier, werk de naam van het dossier bij om de naam van het nieuwe gegevens () dossier aan te passen dat door Adobe wordt verstrekt. [!DNL .bin]
1. Sparen het dossier van de transformatieconfiguratie door **[!UICONTROL (modified)]** bij de bovenkant van het configuratievenster met de rechtermuisknop te klikken en te klikken **[!UICONTROL Save]**.

1. Sparen het gewijzigde configuratiedossier aan elk profiel dat de datadienst door de controlemarkering naast [!DNL IP Lookup.cfg] in de [!DNL User] kolom met de rechtermuisknop aan te klikken en **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>* te klikken gebruikt. De hertransformatie van de gegevens begint na synchronisatie van het datasetprofiel.

   Voor informatie over retransformation van uw dataset, zie het hoofdstuk van de Reprocessing en van de Herschikking van de Gids *van de Configuratie van de* Dataset.

   >[!NOTE]
   >
   >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd (inclusief het [!DNL IP Geo-location] of het [!DNL IP Geo-intelligence] profiel), omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

Als u de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] datadienst voor versie 5.1 of later installeerde, hebt u de update van de datadienst voltooid. Nochtans, als u de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] de datadienst voorafgaand aan versie 5.1 installeerde, moet u de volgende extra procedures voltooien.

## Het vervangen van het Dossier van de Raadpleging {#section-ced1efa38a76419d812edd35423dbff7}

U zou de volgende stappen slechts moeten voltooien als u de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] de datadienst voorafgaand aan versie 5.1 installeerde.

1. In [!DNL Server Files Manager], klik of **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-intelligence]** of **[!UICONTROL Profiles]** > **[!UICONTROL IP Geo-location]**, dan klik **[!UICONTROL Maps]** om zijn inhoud te bekijken.

1. Klik met de rechtermuisknop in de **[!UICONTROL Temp]** kolom voor **[!UICONTROL Maps]** en klik **[!UICONTROL Open]** > *&lt;**[!UICONTROL folder]**>*.

1. Kopieer het nieuwe [!DNL .txt] dossier dat door Adobe aan het de omslagvenster van Kaarten wordt verstrekt.
1. Sla het bestand op in het serversysteem van de gegevenswerkbank door met de rechtermuisknop te klikken op het vinkje in de [!DNL Temp] kolom voor het [!DNL .txt] bestand en te klikken op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

>[!NOTE]
>
>Als u een cluster in werking stelt, upload de dossiers aan de server van de hoofdgegevenswerkbank in de cluster.

## De laagbestanden bijwerken {#section-8b84e7099bad40c9a69665a4890fe66e}

>[!NOTE]
>
>U zou de volgende stappen slechts moeten voltooien als u de [!DNL IP Geo-intelligence] en [!DNL IP Geo-location] de datadienst voorafgaand aan versie 5.1 installeerde.

Voltooi deze stappen voor elk laag ( [!DNL .layer]) dossier dat verwijzingen het [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] raadplegings ( [!DNL .txt]) dossier.

1. In de de dienstnaam van Profielen \*data van Profielen* \ de omslag van Kaarten binnen de de installatiefolder van de gegevenswerkbank, open het [!DNL .layer] dossier in een tekstredacteur zoals Blocnote.

1. In de [!DNL Data Paths] vector, werk de naam van het [!DNL .txt] raadplegingsdossier bij om de naam van het nieuwe die [!DNL .txt] dossier aan te passen door Adobe wordt verstrekt, zoals aangetoond in de volgende dossiersteekproef wordt benadrukt:

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

1. Sparen het bijgewerkte laagdossier.
1. Herhaal Stappen 2 en 3 voor elk [!DNL .layer] dossier dat verwijzingen het [!DNL IP Geo-intelligence] of [!DNL IP Geo-location] [!DNL .txt] dossier.


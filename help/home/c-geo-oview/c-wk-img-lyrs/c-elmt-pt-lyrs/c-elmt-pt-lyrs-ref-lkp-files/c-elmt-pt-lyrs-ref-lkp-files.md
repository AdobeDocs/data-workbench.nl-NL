---
description: Wanneer u een elementpuntlaag maakt die verwijst naar een opzoekbestand om breedte- en lengtegegevens te verkrijgen, wordt de locatie van het punt opgehaald door elk element en de bijbehorende breedte en lengte op te halen uit het opzoekbestand.
title: Elementpuntlagen definiëren die verwijzen naar opzoekbestanden
uuid: 99d08d43-bdbb-42e1-927a-edf320686c79
exl-id: b6928821-c825-43e2-8c7b-2ce0f49aa67e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Elementpuntlagen definiëren die verwijzen naar opzoekbestanden{#defining-element-point-layers-referencing-lookup-files}

{{eol}}

Wanneer u een elementpuntlaag maakt die verwijst naar een opzoekbestand om breedte- en lengtegegevens te verkrijgen, wordt de locatie van het punt opgehaald door elk element en de bijbehorende breedte en lengte op te halen uit het opzoekbestand.

In plaats van een opzoekbestand te gebruiken, kunt u de opdracht [!DNL Dynamic Points] functionaliteit, die de breedte en lengte van een locatie insluit in de naam van elk element van een dimensie. Zie [Elementpuntlagen definiëren met behulp van dynamische punten](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3).

Als u een elementpuntlaag wilt definiëren die verwijst naar een opzoekbestand, moet u het volgende maken of al beschikbaar hebben:

* **Een dimensie** in de [!DNL Transformation.cfg] bestand of een gegevensset voor transformatie bevat een bestand. Voor informatie over de dossiers van de transformatieconfiguratie, zie *Configuratie-handleiding voor gegevensset*.

* **Een opzoekbestand** met de gegevens die worden gebruikt om elk gegevenspunt te plotten. Dit bestand moet ten minste drie kolommen gegevens bevatten voor elk gegevenspunt: de sleutel, de lengtegraad en de breedtegraad. Voor meer informatie over het vereiste formaat van het raadplegingsdossier, zie [Opzoekbestandsindeling voor elementpunt](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lkp-file-frmt.md#concept-c059121019ea4dbcb1c17129567f4121).

* **Een laagbestand** Hiermee geeft u de locatie van het opzoekbestand op en geeft u de gerelateerde afmetingen en metrische waarde, alsmede de namen van de kolommen sleutel, lengte en breedte in het opzoekbestand aan. Ga voor meer informatie over de vereiste indeling van het laagbestand naar [Laagbestandsindeling voor elementpunt](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981).

>[!NOTE]
>
>De [!DNL Zip Points.layer] het dossier, verstrekt met [!DNL Geography] profiel, is een elementpuntlaag die de [!DNL Zipcode.dim] bestand, de [!DNL Sessions.metric] bestand, de [!DNL Zip Points.txt] opzoekbestand en de namen van de kolommen key, longitude, latitude en name in het opzoekbestand.

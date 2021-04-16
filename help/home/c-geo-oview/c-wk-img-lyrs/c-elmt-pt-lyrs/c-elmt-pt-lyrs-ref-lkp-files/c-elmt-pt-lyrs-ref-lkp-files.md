---
description: Wanneer u een elementpuntlaag maakt die verwijst naar een opzoekbestand om breedte- en lengtegegevens te verkrijgen, wordt de locatie van het punt opgehaald door elk element en de bijbehorende breedte en lengte op te halen uit het opzoekbestand.
title: Elementpuntlagen definiëren die verwijzen naar opzoekbestanden
uuid: 99d08d43-bdbb-42e1-927a-edf320686c79
exl-id: b6928821-c825-43e2-8c7b-2ce0f49aa67e
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Elementpuntlagen definiëren die verwijzen naar opzoekbestanden{#defining-element-point-layers-referencing-lookup-files}

Wanneer u een elementpuntlaag maakt die verwijst naar een opzoekbestand om breedte- en lengtegegevens te verkrijgen, wordt de locatie van het punt opgehaald door elk element en de bijbehorende breedte en lengte op te halen uit het opzoekbestand.

In plaats van een opzoekbestand te gebruiken, kunt u de functie [!DNL Dynamic Points] gebruiken, waarmee de breedte en lengte van een locatie in de naam van elk element van een dimensie worden ingesloten. Zie [Elementpuntlagen definiëren met behulp van dynamische punten](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3).

Als u een elementpuntlaag wilt definiëren die verwijst naar een opzoekbestand, moet u het volgende maken of al beschikbaar hebben:

* **Een** dimensie die in het  [!DNL Transformation.cfg] dossier of een transformatiedataset wordt bepaald omvat dossier. Voor informatie over de dossiers van de transformatieconfiguratie, zie *de Gids van de Configuratie van de Dataset*.

* **Een opzoekbestand** met de gegevens die worden gebruikt om elk gegevenspunt te plotten. Dit bestand moet ten minste drie kolommen gegevens bevatten voor elk gegevenspunt: de sleutel, de lengtegraad en de breedtegraad. Voor meer informatie over het vereiste formaat van het raadplegingsdossier, zie [het Formaat van het Dossier van het Opzoeken van het Punt van het Element](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lkp-file-frmt.md#concept-c059121019ea4dbcb1c17129567f4121).

* **Een laagbestand** dat de locatie van het opzoekbestand opgeeft en dat de gerelateerde afmetingen en metrische waarden en de namen van de kolommen sleutel, lengte en breedte in het opzoekbestand aangeeft. Voor meer informatie over het vereiste formaat van het laagdossier, zie [het Formaat van het Dossier van de Laag van het Punt van het Element](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981).

>[!NOTE]
>
>Het [!DNL Zip Points.layer]-bestand met het profiel [!DNL Geography] is een elementpuntlaag die het [!DNL Zipcode.dim]-bestand, het [!DNL Sessions.metric]-bestand, het [!DNL Zip Points.txt]-opzoekbestand en de namen van de sleutelkolommen, lengtegraad, breedtegraad en naamkolommen in het opzoekbestand aangeeft.

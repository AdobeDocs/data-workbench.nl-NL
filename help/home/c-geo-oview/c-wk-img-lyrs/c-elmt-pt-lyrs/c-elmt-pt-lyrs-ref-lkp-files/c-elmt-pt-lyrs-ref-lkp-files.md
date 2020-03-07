---
description: Wanneer het creëren van een laag van het elementenpunt die verwijzingen een raadplegingsdossier om breedtegraad en lengtegegevens te verkrijgen, wordt de plaats van het punt verkregen door elk element en zijn bijbehorende breedtegraad en lengtegraad uit het raadplegingsdossier terug te winnen.
solution: Analytics
title: Het bepalen van de Lagen van het Punt van het Element die de Dossiers van de Raadpleging van verwijzingen voorzien
topic: Data workbench
uuid: 99d08d43-bdbb-42e1-927a-edf320686c79
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het bepalen van de Lagen van het Punt van het Element die de Dossiers van de Raadpleging van verwijzingen voorzien{#defining-element-point-layers-referencing-lookup-files}

Wanneer het creëren van een laag van het elementenpunt die verwijzingen een raadplegingsdossier om breedtegraad en lengtegegevens te verkrijgen, wordt de plaats van het punt verkregen door elk element en zijn bijbehorende breedtegraad en lengtegraad uit het raadplegingsdossier terug te winnen.

In plaats van het gebruiken van een raadplegingsdossier, kunt u de [!DNL Dynamic Points] functionaliteit gebruiken, die de breedte en de lengtegraad van een plaats in de naam van elk element van een afmeting inbedt. Zie het [bepalen van de Lagen van het Punt van het Element Gebruikend Dynamische Punten](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-dyn-pts.md#concept-77ae65bedc3f465489bc135ae7e3c2f3).

Om een laag van het elementenpunt te bepalen dat de verwijzingen een raadplegingsdossier, u moeten tot stand brengen of reeds beschikbaar het volgende hebben:

* **Een dimensie** die in het [!DNL Transformation.cfg] dossier of een transformatiedataset wordt bepaald omvat dossier. Voor informatie over de dossiers van de transformatieconfiguratie, zie de Gids *van de Configuratie van de* Dataset.

* **Een raadplegingsdossier** dat de gegevens bevat die worden gebruikt om elk gegevenspunt te plot. Dit dossier moet minstens drie kolommen van gegevens voor elk gegevenspunt bevatten: de sleutel, de lengtegraad, en de breedtegraad. Voor meer informatie over het vereiste formaat van het raadplegingsdossier, zie het Formaat [van het Dossier van de Raadpleging van het Punt van het](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lkp-file-frmt.md#concept-c059121019ea4dbcb1c17129567f4121)Element.

* **Een laagdossier** dat de plaats van het raadplegingsdossier specificeert en de verwante afmeting en metrisch evenals de sleutel, de lengtegraad, en de namen van de breedtelijn in het raadplegingsdossier identificeert. Voor meer informatie over het vereiste formaat van het laagdossier, zie het Formaat [van het Dossier van de Laag van het Punt van het](../../../../../home/c-geo-oview/c-wk-img-lyrs/c-elmt-pt-lyrs/c-elmt-pt-lyrs-ref-lkp-files/c-elmt-pt-lyr-file-frmt/c-elmt-pt-lyr-file-frmt.md#concept-678a95cb69644105a7af1b86ad5a5981)Element.

>[!NOTE]
>
>Het [!DNL Zip Points.layer] dossier, dat van het [!DNL Geography] profiel wordt voorzien, is een laag van het elementenpunt die het [!DNL Zipcode.dim] dossier, het [!DNL Sessions.metric] dossier, het [!DNL Zip Points.txt] raadplegingsdossier, en de namen van de sleutel, de lengte, de breedtegraad, en de naamkolommen in het raadplegingsdossier identificeert.


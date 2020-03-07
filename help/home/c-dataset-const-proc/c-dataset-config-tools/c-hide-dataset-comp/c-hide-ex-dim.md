---
description: U kunt of de Verborgen parameter of de parameter van de Show gebruiken om uitgebreide afmetingen te verbergen zodat tonen zij niet op het afmetingsmenu in gegevenswerkbank.
solution: Analytics
title: Uitgebreide afmetingen verbergen
topic: Data workbench
uuid: c32f47ad-0246-4611-b54c-0c9f0eb396bd
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Uitgebreide afmetingen verbergen{#hiding-extended-dimensions}

U kunt of de Verborgen parameter of de parameter van de Show gebruiken om uitgebreide afmetingen te verbergen zodat tonen zij niet op het afmetingsmenu in gegevenswerkbank.

Wanneer u het aangewezen plaatsen voor één van beide parameter ingaat, is de afmetingsnaam niet vermeld in het menu in gegevenswerkbank, maar het is nog in het profiel en beschikbaar om worden gebruikt. Om het even welke gebruiker van de gegevenswerkbank kan verborgen afmetingen tijdelijk losmaken door Unhide Al parameter in het [!DNL Insight.cfg] dossier aan waar te plaatsen.

Voor meer informatie over Unhide Al parameter, zie de bijlage over de configuratieparameters van de gegevenswerkbank in de Gids *van de Gebruiker van de Werkbank van* Gegevens.

De volgende secties beschrijven hoe te om de Verborgen te gebruiken en parameters te tonen om uitgebreide afmetingen te verbergen.

* [Het verbergen van Uitgebreide Afmetingen die de Verborgen Parameter gebruiken](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-ex-dim.md#section-7167a6f6241a4bc78f2f322e048d65cf)
* [Het verbergen van Uitgebreide Afmetingen die de Parameter van de Show gebruiken](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-ex-dim.md#section-4dceb1079c7f40d2bffc686d1f73f8ad)

## Het verbergen van Uitgebreide Afmetingen die de Verborgen Parameter gebruiken {#section-7167a6f6241a4bc78f2f322e048d65cf}

De verborgen parameter is een facultatieve parameter die u kunt gebruiken wanneer het bepalen van uitgebreide afmetingen in [!DNL Transformation Dataset Configuration] dossiers.

1. Open [!DNL Transformation Dataset Configuration] dossiers waarin de uitgebreide dimensie die u wilt verbergen wordt bepaald. Zie Bestaande gegevensset [bewerken met bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077).

1. Bepaal de plaats van de Verborgen parameter voor de gewenste afmeting in het configuratievenster en typ *waar*.
1. Sla het bestand lokaal op en sla het vervolgens op in het juiste profiel op de server. Zie Bestaande gegevensset [bewerken met bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077).

De dataset hertransformeert, waarna verschijnt de uitgebreide afmeting niet op het afmetingsmenu in gegevenswerkbank. Voor meer informatie over de Verborgen parameter, zie [Uitgebreide Afmetingen](../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

Als u het plaatsen van de Verborgen parameter verandert, moet u de dataset voor de verandering opnieuw omzetten om van kracht te worden.

## Het verbergen van Uitgebreide Afmetingen die de Parameter van de Show gebruiken {#section-4dceb1079c7f40d2bffc686d1f73f8ad}

De parameter van de Show is geen één van de parameters beschikbaar voor het bepalen van uitgebreide afmetingen in [!DNL Transformation Dataset Configuration] dossiers. In plaats daarvan, wordt de parameter bepaald in de [!DNL .dim] dossiers voor om het even welke afgeleide afmetingen die u creeert. Daarom om de parameter van de Show te gebruiken om een uitgebreide afmeting te verbergen, moet u eerst een afgeleide afmeting tot stand brengen die op de uitgebreide afmeting gebaseerd is zoals die in de volgende procedure wordt beschreven:

1. Gebruik een tekstredacteur zoals Blocnote om een leeg dossier tot stand te brengen genoemd &lt;*afmetingsnaam*>.dim het dossier - de naam zou de naam van de afmeting moeten aanpassen die u wilt verbergen. Bijvoorbeeld, om de Volgende dimensie van de Pagina te verbergen, zou u een [!DNL Next Page.dim] dossier tot stand brengen.

1. Voeg de volgende tekst aan het dossier toe:

   * entiteit = ref: gegevens/model/dim/ouder/+naam
   * show = bool: vals

1. Sla het bestand op in de map Afmetingen van het profiel. U kunt het dossier aan subdirectory bewaren indien gewenst.

Wanneer u de parameter van de Show gebruikt om een uitgebreide afmeting te verbergen, moet u niet uw dataset opnieuw omzetten om de verandering te maken van kracht worden. U kunt verkiezen om de afmeting in uw lokale versie van het profiel te verbergen of te tonen (d.w.z., kunt u sparen het [!DNL .dim] dossier aan uw omslag van de Gebruiker), of u kunt het [!DNL .dim] dossier aan de server voor gebruik door andere gebruikers van het profiel bewaren.

U kunt de parameter van de Show ook gebruiken om metriek en filters te verbergen. Voor informatie, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse in de Gids *van de Gebruiker van de Werkbank van* Gegevens.

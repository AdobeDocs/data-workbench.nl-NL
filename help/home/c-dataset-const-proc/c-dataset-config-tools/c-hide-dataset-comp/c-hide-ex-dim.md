---
description: U kunt de parameter Verborgen of de parameter Tonen gebruiken om uitgebreide afmetingen te verbergen, zodat ze niet worden weergegeven in het menu Dimensie in de werkbank Gegevens.
title: Uitgebreide Dimension verbergen
uuid: c32f47ad-0246-4611-b54c-0c9f0eb396bd
exl-id: 5baccf39-6f3b-40a1-b1c0-a8e5d6a61211
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---

# Uitgebreide Dimension verbergen{#hiding-extended-dimensions}

U kunt de parameter Verborgen of de parameter Tonen gebruiken om uitgebreide afmetingen te verbergen, zodat ze niet worden weergegeven in het menu Dimensie in de werkbank Gegevens.

Wanneer u de juiste instelling voor een van beide parameters invoert, wordt de naam van de dimensie niet vermeld in het menu op de werkbank Gegevens, maar blijft deze in het profiel en is deze beschikbaar voor gebruik. Om het even welke gebruiker van de gegevenswerkbank kan verborgen afmetingen tijdelijk ongedaan maken door de Unhide Al parameter in het [!DNL Insight.cfg] dossier aan waar te plaatsen.

Voor meer informatie over Unhide Al parameter, zie het bijlage over de configuratieparameters van de gegevenswerkbank in *de Gids van de Gebruiker van de Data Workbench*.

In de volgende secties wordt beschreven hoe u de parameters Verborgen en Weergeven kunt gebruiken om uitgebreide afmetingen te verbergen.

* [Uitgebreide Dimension verbergen met de verborgen parameter](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-ex-dim.md#section-7167a6f6241a4bc78f2f322e048d65cf)
* [Uitgebreide Dimension verbergen met de parameter Tonen](../../../../home/c-dataset-const-proc/c-dataset-config-tools/c-hide-dataset-comp/c-hide-ex-dim.md#section-4dceb1079c7f40d2bffc686d1f73f8ad)

## Uitgebreide Dimension verbergen met de verborgen parameter {#section-7167a6f6241a4bc78f2f322e048d65cf}

De parameter Hidden is een optionele parameter die u kunt gebruiken bij het definiëren van uitgebreide afmetingen in [!DNL Transformation Dataset Configuration]-bestanden.

1. Open [!DNL Transformation Dataset Configuration] dossiers waarin de uitgebreide afmeting die u wilt verbergen wordt bepaald. Zie [Bestaande gegevensset bewerken, inclusief bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077).

1. Zoek de parameter Verborgen voor de gewenste afmeting in het configuratievenster en typ *true*.
1. Sla het bestand lokaal op en sla het vervolgens op in het juiste profiel op de server. Zie [Bestaande gegevensset bewerken, inclusief bestanden](../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077).

De dataset hertransformeert, waarna de uitgebreide afmeting niet op het afmetingsmenu in gegevenswerkbank verschijnt. Voor meer informatie over de Verborgen parameter, zie [Uitgebreide Dimension](../../../../home/c-dataset-const-proc/c-ex-dim/c-abt-ex-dim.md).

Als u het plaatsen van de Verborgen parameter verandert, moet u de dataset voor de verandering opnieuw omzetten om van kracht te worden.

## Uitgebreide Dimension verbergen met de parameter {#section-4dceb1079c7f40d2bffc686d1f73f8ad} tonen

De parameter Show is geen van de parameters beschikbaar voor het definiëren van uitgebreide afmetingen in [!DNL Transformation Dataset Configuration]-bestanden. In plaats daarvan, wordt de parameter bepaald in [!DNL .dim] dossiers voor om het even welke afgeleide dimensies die u creeert. Daarom om de parameter van de Show te gebruiken om een uitgebreide dimensie te verbergen, moet u eerst een afgeleide dimensie tot stand brengen die op de uitgebreide dimensie zoals die in de volgende procedure wordt beschreven gebaseerd is:

1. Gebruik een teksteditor, zoals Kladblok, om een leeg bestand te maken met de naam &lt;*naam van dimensie*>.dim De bestandsnaam moet overeenkomen met de naam van de dimensie die u wilt verbergen. Als u bijvoorbeeld de dimensie Volgende pagina wilt verbergen, maakt u een [!DNL Next Page.dim]-bestand.

1. Voeg de volgende tekst toe aan het bestand:

   * entiteit = ref: wdata/model/dim/parent/+name
   * show = bool: false

1. Sla het bestand op in de map Dimension van het profiel. U kunt het bestand desgewenst opslaan in een submap.

Wanneer u de parameter van de Show gebruikt om een uitgebreide afmeting te verbergen, moet u niet uw dataset opnieuw omzetten om de verandering van kracht te maken. U kunt ervoor kiezen om de afmetingen in uw lokale versie van het profiel te verbergen of weer te geven (u kunt het [!DNL .dim]-bestand in de map Gebruiker opslaan), of u kunt het [!DNL .dim]-bestand opslaan op de server voor gebruik door andere gebruikers van het profiel.

U kunt de parameter Tonen ook gebruiken om metriek en filters te verbergen. Voor informatie, zie het het Vormen hoofdstuk van de Eigenschappen van de Interface en van de Analyse in *de Gids van de Gebruiker van de Data Workbench*.

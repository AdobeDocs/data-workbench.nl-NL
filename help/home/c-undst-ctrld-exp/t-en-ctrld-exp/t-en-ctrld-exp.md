---
description: Om gecontroleerde experimenteren toe te laten, moet iemand met beheerdertoegang tot uw Web of toepassingsservers de parameter ExpFile in het de configuratiedossier van de Sensor (gewoonlijk genoemd gebruikend txlogd.conf) op elke Web of toepassingsserver in uw Webcluster wijzigen waarop een Sensor wordt geïnstalleerd.
solution: Analytics,Analytics
title: Gecontroleerde experimenten inschakelen
topic: Data workbench
uuid: 27d68fad-ae2d-4a2e-b449-fbaf88286cfa
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# Gecontroleerde experimenten inschakelen{#enabling-controlled-experimentation}

Om gecontroleerde experimenteren toe te laten, moet iemand met beheerdertoegang tot uw Web of toepassingsservers de parameter ExpFile in het de configuratiedossier van de Sensor (gewoonlijk genoemd gebruikend txlogd.conf) op elke Web of toepassingsserver in uw Webcluster wijzigen waarop een Sensor wordt geïnstalleerd.

Daarnaast kunnen twee andere parameters in dit bestand worden gewijzigd om een testgereedschap (parameter ExpCookieURL) te implementeren of om grote delen van uw website (parameter ExpPartialMatch) opnieuw toe te wijzen. In dit hoofdstuk vindt u meer informatie over deze parameters.

**Het bestand txlogd.conf bewerken**

Voer de volgende stappen uit als u beheerderstoegang hebt. Als u geen beheerdertoegang hebt, contacteer uw systeemarchitect om de veranderingen te verzoeken, die hen van de volgende stappen voorzien.

1. Navigeer naar de [!DNL Sensor] installatiemap op een web- of toepassingsserver in uw webcluster waarop een [!DNL Sensor] installatiemap is geïnstalleerd.
1. Open het [!DNL Sensor] configuratiebestand (gewoonlijk aangeduid met [!DNL txlogd.conf]) met een teksteditor en bewerk het bestand zoals aangegeven in [Modifying the ExpFile Parameter](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28).

   (En optioneel bij het [wijzigen van het parameter ExpCookieURL (optioneel)](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expckurl-prm.md#concept-215bf86bab4e4ec0b0cc803ec48a8fcf) en het [wijzigen van de parameter ExpPartialMatch (optioneel)](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expplmth-prm.md#concept-9c817c4c49b74287b0f70d6a1a37655e).)

1. Sla het bestand op en sluit het.
1. Herhaal deze procedure voor elke web- of toepassingsserver in uw webcluster waarop een toepassing [!DNL Sensor] is geïnstalleerd.

---
description: Om gecontroleerde experimentatie toe te laten, moet iemand met beheerdertoegang tot uw Web of toepassingsservers de parameter ExpFile in het de configuratiedossier van de Sensor (gewoonlijk genoemd gebruikend txlogd.conf) op elk Web of toepassingsserver in uw Webcluster wijzigen waarop een Sensor geïnstalleerd is.
solution: Insight,Analytics
title: Het toelaten van Gecontroleerde Experimentatie
topic: Data workbench
uuid: 27d68fad-ae2d-4a2e-b449-fbaf88286cfa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het toelaten van Gecontroleerde Experimentatie{#enabling-controlled-experimentation}

Om gecontroleerde experimentatie toe te laten, moet iemand met beheerdertoegang tot uw Web of toepassingsservers de parameter ExpFile in het de configuratiedossier van de Sensor (gewoonlijk genoemd gebruikend txlogd.conf) op elk Web of toepassingsserver in uw Webcluster wijzigen waarop een Sensor geïnstalleerd is.

Bovendien kunnen twee andere parameters in dit dossier worden gewijzigd om een het testen hulpmiddel (parameter ExpCookieURL) uit te voeren of grote secties van uw website (parameter ExpPartialMatch) opnieuw in kaart te brengen. Dit hoofdstuk verstrekt meer informatie over deze parameters.

**Om het txlogd.conf- dossier uit te geven**

Als u beheerderstoegang hebt, voltooi de volgende stappen. Als u beheerdertoegang niet hebt, contacteer uw systeemarchitect om de veranderingen te verzoeken, verstrekkend hen van de volgende stappen.

1. Navigeer aan de [!DNL Sensor] installatiemap op een Web of toepassingsserver in uw Webcluster waarop een [!DNL Sensor] geïnstalleerd is.
1. Open het [!DNL Sensor] configuratiedossier (gewoonlijk genoemd gebruikend [!DNL txlogd.conf]) gebruikend een tekstredacteur en geef het dossier uit zoals die in het Wijzigen van de Parameter [](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expfile-prm.md#concept-25232b386a654870becc789d4f1fcc28)wordt vermeld ExpFile.

   (En naar keuze in het [Wijzigen van de (Facultatieve)](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expckurl-prm.md#concept-215bf86bab4e4ec0b0cc803ec48a8fcf) Paramter ExpCookieURL en het [Wijzigen van de (Facultatieve)](../../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expplmth-prm.md#concept-9c817c4c49b74287b0f70d6a1a37655e)Parameter ExpPartialMatch.)

1. Sparen en sluit het dossier.
1. Herhaal deze procedure voor elke Web of toepassingsserver in uw Webcluster waarop een [!DNL Sensor] geïnstalleerd is.

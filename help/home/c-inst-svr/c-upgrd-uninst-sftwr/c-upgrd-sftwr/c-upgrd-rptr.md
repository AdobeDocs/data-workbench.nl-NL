---
description: Instructies om Repeater te bevorderen gebruikend Inzicht of aan verbetering door dossiers te kopiëren.
solution: Analytics
title: Repeater bijwerken
uuid: 2027ed9e-9dd9-40f5-b7e9-2709f8745b5c
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Repeater bijwerken{#upgrading-repeater}

Instructies om Repeater te bevorderen gebruikend Inzicht of aan verbetering door dossiers te kopiëren.

U kunt een van de volgende methoden gebruiken om een upgrade uit te voeren [!DNL Repeater] vanaf Platform 4.x of hoger:

* Als u een verbinding tussen [!DNL Insight] en [!DNL Repeater] zoals die in het [Creëren van een Verbinding tussen Inzicht en Repeater](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118)wordt beschreven creeerde, kunt u gebruiken [!DNL Insight] om te bevorderen [!DNL Repeater]. Zie [Bevorderen Repeater gebruikend Inzicht](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-59c24448fd0f45c08abd0245ad746764).

   -of-

* Als u geen verbinding tussen [!DNL Insight] en kunt maken of niet hebt gemaakt, moet u de upgradebestanden rechtstreeks naar de [!DNL Repeater][!DNL Repeater] computer kopiëren. Zie Repeater [bijwerken door bestanden](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-202f2209f6604f19a15d96b517ea1bc1)te kopiëren.

## Herhaling verbeteren met Inzicht {#section-59c24448fd0f45c08abd0245ad746764}

1. Kopieer op de [!DNL Insight] computer de [!DNL bin] map van het [!DNL Insight Server] upgradepakket naar de [!DNL Temp] map in de map waarin [!DNL Insight] is geïnstalleerd.
1. Start [!DNL Insight].
1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het gedeelte [!DNL Repeater] dat u wilt bijwerken en klik op **[!UICONTROL Server Files]**.
1. Voer in het [!DNL Server Files Manager]gedeelte de volgende handelingen uit om de upgradebestanden naar de server te uploaden:

   1. Zoek de [!DNL bin] map.
   1. Klik met de rechtermuisknop op het vinkje voor de [!DNL bin] map in de map Temperatuur en selecteer **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL server name]**>*.

>[!NOTE]
>
>Er verschijnt een bericht dat aangeeft dat deze stap bestanden met dezelfde naam op de server overschrijft. Klik **[!UICONTROL Yes]** om door te gaan.

>[!NOTE]
>
>Als u extra bestanden moet uploaden om de [!DNL Repeater] upgrade te voltooien, geeft Adobe hiervoor instructies.

Nadat u de upgradebestanden naar de [!DNL Repeater] computer hebt geüpload, [!DNL Repeater] start u zichzelf automatisch opnieuw en laadt u de nieuwe versie.

## Repeater bijwerken door bestanden te kopiëren {#section-202f2209f6604f19a15d96b517ea1bc1}

1. Open het upgradebestand van Adobe. Waarschijnlijk is dit bestand een [!DNL .zip] bestand dat u wilt bijwerken [!DNL Insight Server].
1. Ga naar de map waarin u hebt geïnstalleerd [!DNL Repeater] (bijvoorbeeld [!DNL D:\Adobe\Repeater]).
1. Kopieer de [!DNL bin] map in het [!DNL .zip] bestand en plak deze in de [!DNL Repeater] installatiemap om de bestaande [!DNL bin] map te overschrijven.

>[!NOTE]
>
>Als u extra bestanden moet uploaden om de [!DNL Insight Server] upgrade te voltooien, geeft Adobe hiervoor instructies.

Nadat u de upgradebestanden naar de [!DNL Repeater] computer hebt gekopieerd, wordt de toepassing [!DNL Repeater] automatisch opnieuw gestart en wordt de nieuwe versie geladen.

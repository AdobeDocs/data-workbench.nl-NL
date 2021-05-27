---
description: Instructies om Repeater te bevorderen gebruikend Inzicht of aan verbetering door dossiers te kopiëren.
title: Repeater bijwerken
uuid: 2027ed9e-9dd9-40f5-b7e9-2709f8745b5c
exl-id: f81fa79e-f660-48fd-b2ff-419961d49c55
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Repeater bijwerken{#upgrading-repeater}

Instructies om Repeater te bevorderen gebruikend Inzicht of aan verbetering door dossiers te kopiëren.

U kunt één van de volgende methodes gebruiken om [!DNL Repeater] van Platform 4.x of later te bevorderen:

* Als u een verbinding tussen [!DNL Insight] en [!DNL Repeater] zoals die in [het Creëren van een Verbinding tussen Inzicht en Repeater](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118) wordt beschreven, kunt u [!DNL Insight] gebruiken om [!DNL Repeater] te bevorderen. Zie [Repeater bijwerken met Inzicht](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-59c24448fd0f45c08abd0245ad746764).

   -of-

* Als u geen verbinding tussen [!DNL Insight] en [!DNL Repeater] kon of niet kon tot stand brengen, moet u de verbeteringsdossiers aan [!DNL Repeater] machine direct kopiëren. Zie [Repeater bijwerken door bestanden te kopiëren](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-202f2209f6604f19a15d96b517ea1bc1).

## Repeater bijwerken met Inzicht {#section-59c24448fd0f45c08abd0245ad746764}

1. Kopieer op de [!DNL Insight]-computer de [!DNL bin]-map van het [!DNL Insight Server]-upgradepakket naar de [!DNL Temp]-map in de map waarin [!DNL Insight] is geïnstalleerd.
1. Start [!DNL Insight].
1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van de [!DNL Repeater] die u wilt bijwerken en klik op **[!UICONTROL Server Files]**.
1. Voer in [!DNL Server Files Manager] de volgende handelingen uit om de upgradebestanden naar de server te uploaden:

   1. Zoek de map [!DNL bin].
   1. Klik met de rechtermuisknop op het vinkje voor de map [!DNL bin] in de map Temp en selecteer **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL server name]**>*.

>[!NOTE]
>
>Er verschijnt een bericht dat aangeeft dat deze stap bestanden met dezelfde naam op de server overschrijft. Klik op **[!UICONTROL Yes]** om door te gaan.

>[!NOTE]
>
>Als u extra bestanden moet uploaden om de [!DNL Repeater]-upgrade te voltooien, geeft Adobe hiervoor instructies.

Nadat u de upgradebestanden naar de [!DNL Repeater]-computer hebt geüpload, wordt [!DNL Repeater] automatisch opnieuw opgestart en wordt de nieuwe versie geladen.

## Repeater bijwerken door bestanden {#section-202f2209f6604f19a15d96b517ea1bc1} te kopiëren

1. Open het upgradebestand van Adobe. Dit bestand is waarschijnlijk een [!DNL .zip]-bestand om [!DNL Insight Server] te upgraden.
1. Ga naar de directory waarin u [!DNL Repeater] hebt geïnstalleerd (bijvoorbeeld [!DNL D:\Adobe\Repeater]).
1. Kopieer de map [!DNL bin] in het bestand [!DNL .zip] en plak deze in de installatiemap [!DNL Repeater] om de bestaande map [!DNL bin] te overschrijven.

>[!NOTE]
>
>Als u extra bestanden moet uploaden om de [!DNL Insight Server]-upgrade te voltooien, geeft Adobe hiervoor instructies.

Nadat u de verbeteringsdossiers aan [!DNL Repeater] machine kopieert, [!DNL Repeater] automatisch opnieuw begint en laadt de nieuwe versie.

---
description: Instructies om Repeater te bevorderen gebruikend Inzicht of aan verbetering door dossiers te kopiëren.
title: Repeater bijwerken
uuid: 2027ed9e-9dd9-40f5-b7e9-2709f8745b5c
exl-id: f81fa79e-f660-48fd-b2ff-419961d49c55
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Repeater bijwerken{#upgrading-repeater}

{{eol}}

Instructies om Repeater te bevorderen gebruikend Inzicht of aan verbetering door dossiers te kopiëren.

U kunt een van de volgende methoden gebruiken om een upgrade uit te voeren [!DNL Repeater] uit Platform 4.x of hoger:

* Als u een verbinding hebt gemaakt tussen [!DNL Insight] en [!DNL Repeater] zoals beschreven in [Het creëren van een Verbinding tussen Insight en Repeater](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118)kunt u [!DNL Insight] om te upgraden [!DNL Repeater]. Zie [Herhaling verbeteren met Inzicht](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-59c24448fd0f45c08abd0245ad746764).

   -of-

* Als u geen verbinding kon maken tussen [!DNL Insight] en [!DNL Repeater], moet u de upgradebestanden rechtstreeks naar de [!DNL Repeater] machine. Zie [Repeater bijwerken door bestanden te kopiëren](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-202f2209f6604f19a15d96b517ea1bc1).

## Herhaling verbeteren met Inzicht {#section-59c24448fd0f45c08abd0245ad746764}

1. Op de [!DNL Insight] computer, kopieer de [!DNL bin] uit de [!DNL Insight Server] upgradepakket naar de [!DNL Temp] map in de map waarin [!DNL Insight] is geïnstalleerd.
1. Start [!DNL Insight].
1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het dialoogvenster [!DNL Repeater] u wilt bevorderen en klikken **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager]Voer de volgende handelingen uit om de upgradebestanden naar de server te uploaden:

   1. Zoek de [!DNL bin] map.
   1. Klik met de rechtermuisknop op het vinkje voor het dialoogvenster [!DNL bin] map in de map Temperatuur en selecteer **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL server name]**>*.

>[!NOTE]
>
>Er verschijnt een bericht dat aangeeft dat deze stap bestanden met dezelfde naam op de server overschrijft. Klikken **[!UICONTROL Yes]** om door te gaan.

>[!NOTE]
>
>Als u extra bestanden moet uploaden om uw [!DNL Repeater] Adobe zal hiervoor instructies geven.

Nadat u de upgradebestanden naar de [!DNL Repeater] machine, [!DNL Repeater] start zichzelf automatisch opnieuw en laadt de nieuwe versie.

## Repeater bijwerken door bestanden te kopiëren {#section-202f2209f6604f19a15d96b517ea1bc1}

1. Open het upgradebestand van Adobe. Dit bestand is waarschijnlijk een [!DNL .zip] bestand voor upgrade [!DNL Insight Server].
1. Ga naar de map waarin u hebt geïnstalleerd [!DNL Repeater] (bijvoorbeeld [!DNL D:\Adobe\Repeater]).
1. Kopieer de [!DNL bin] in de [!DNL .zip] bestand en plak het in uw [!DNL Repeater] installatiemap om de bestaande [!DNL bin] map.

>[!NOTE]
>
>Als u extra bestanden moet uploaden om uw [!DNL Insight Server] Adobe zal hiervoor instructies geven.

Nadat u de upgradebestanden naar de [!DNL Repeater] machine, [!DNL Repeater] start zichzelf automatisch opnieuw en laadt de nieuwe versie.

---
description: Instructies om Repeater te bevorderen die Inzicht gebruiken of te bevorderen door dossiers te kopiëren.
solution: Insight
title: Repeater verbeteren
uuid: 2027ed9e-9dd9-40f5-b7e9-2709f8745b5c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Repeater verbeteren{#upgrading-repeater}

Instructies om Repeater te bevorderen die Inzicht gebruiken of te bevorderen door dossiers te kopiëren.

U kunt één van de volgende methodes gebruiken om [!DNL Repeater] van Platform 4.x of later te bevorderen:

* Als u een verbinding tussen [!DNL Insight] en [!DNL Repeater] zoals die in het [Creëren van een Verbinding tussen Inzicht en Repeater](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118)wordt beschreven creeerde, kunt u gebruiken [!DNL Insight] om te bevorderen [!DNL Repeater]. Zie Repeater [Bevorderen Gebruikend Inzicht](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-59c24448fd0f45c08abd0245ad746764).

   -of-

* Als u geen verbinding tussen kon of niet creeerde en [!DNL Insight] , moet u de verbeteringsdossiers aan de [!DNL Repeater][!DNL Repeater] machine direct kopiëren. Zie Repeater [bevorderen door Dossiers](../../../../home/c-inst-svr/c-upgrd-uninst-sftwr/c-upgrd-sftwr/c-upgrd-rptr.md#section-202f2209f6604f19a15d96b517ea1bc1)te kopiëren.

## Het bevorderen van Repeater die Inzicht gebruikt {#section-59c24448fd0f45c08abd0245ad746764}

1. Voor de [!DNL Insight] computer, kopieer de [!DNL bin] omslag van het [!DNL Insight Server] verbeteringspakket aan de [!DNL Temp] omslag in de folder waar [!DNL Insight] wordt geïnstalleerd.
1. Begin [!DNL Insight].
1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van het pictogram met de rechtermuisknop aan [!DNL Repeater] u wilt bevorderen en klikken **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], doe het volgende de verbeteringsdossiers aan de server uploaden:

   1. Bepaal de plaats van de [!DNL bin] omslag.
   1. Klik met de rechtermuisknop op het vinkje voor de [!DNL bin] map in de map Temp en selecteer **[!UICONTROL Save Directory to]** > *&lt;**[!UICONTROL server name]**>*.

>[!NOTE]
>
>U zult een bericht erop wijzen zien dat deze stap dossiers van de zelfde naam beschrijft die op de server bestaan. Klik **[!UICONTROL Yes]** om door te gaan.

>[!NOTE]
>
>Als u extra dossiers moet uploaden om uw [!DNL Repeater] verbetering te voltooien, zal Adobe instructies verstrekken om dit te doen.

Nadat u de verbeteringsdossiers aan de [!DNL Repeater] machine uploadt, begin [!DNL Repeater] automatisch opnieuw zichzelf en laadt de nieuwe versie.

## Repeater upgraden door bestanden te kopiëren {#section-202f2209f6604f19a15d96b517ea1bc1}

1. Open het verbeteringsdossier dat door Adobe wordt verstrekt. Waarschijnlijk, is dit dossier een [!DNL .zip] dossier voor bevordering [!DNL Insight Server].
1. Ga naar de folder waar u installeerde [!DNL Repeater] (bijvoorbeeld, [!DNL D:\Adobe\Repeater]).
1. Kopieer de [!DNL bin] omslag binnen het [!DNL .zip] dossier en kleef het in uw [!DNL Repeater] installatiefolder om de bestaande [!DNL bin] omslag te beschrijven.

>[!NOTE]
>
>Als u extra dossiers moet uploaden om uw [!DNL Insight Server] verbetering te voltooien, zal Adobe instructies verstrekken om dit te doen.

Nadat u de verbeteringsdossiers aan de [!DNL Repeater] machine kopieert, begin [!DNL Repeater] automatisch opnieuw zichzelf en laadt de nieuwe versie.

---
description: Om de server van de gegevenswerkbank te veranderen waarmee een Sensor (de doelserver) communiceert, moet u het txlogd.conf- dossier op elk van de Webservers uitgeven waarop de Sensor geïnstalleerd is.
solution: Insight
title: Het veranderen van de Server van de Werkbank van de Gegevens van het Doel
uuid: 931d376d-8622-4858-8290-19ce91538570
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het veranderen van de Server van de Werkbank van de Gegevens van het Doel{#changing-the-target-data-workbench-server}

Om de server van de gegevenswerkbank te veranderen waarmee een Sensor (de doelserver) communiceert, moet u het txlogd.conf- dossier op elk van de Webservers uitgeven waarop de Sensor geïnstalleerd is.

**Om te veranderen in doel[!DNL data workbench server]**

1. Stop zowel de originele doelserver als de nieuwe doelserver.
1. Kopieer het huidigste [!DNL .vsl] dossier van de originele doelserver aan de nieuwe doelserver. Wanneer u de nieuwe doelserver in een recentere stap opnieuw begint, veroorzaakt dit dat alle nieuwe [!DNL Sensor] gegevens worden toegevoegd aan het huidige, bestaande [!DNL .vsl] dossier in plaats van het creëren van een nieuw [!DNL .vsl] dossier. Voer daartoe de volgende stappen uit:

   1. Voor de originele doelserver, doorblader aan de [!DNL \Logs] omslag in de [!DNL data workbench server] installatiefolder.

   1. Kopieer het huidigste [!DNL .vsl] dossier in de omslag.
   1. Voor de nieuwe doelserver, doorblader aan de [!DNL \Logs] omslag in de [!DNL data workbench server] installatiefolder en kleef het [!DNL .vsl] dossier aan deze omslag.

1. Op één van de Webservers waarop geïnstalleerd [!DNL Sensor] is, open en geef het [!DNL txlogd.conf] dossier uit. Voer daartoe de volgende stappen uit:

   1. Doorblader aan de [!DNL Sensor] installatiefolder en open het [!DNL txlogd.conf] dossier in een tekstredacteur.

   1. Bepaal de plaats van de parameter ServerAddress en verander het om op het adres van de nieuwe doelserver te wijzen.
   1. Sparen en sluit het dossier.

1. Herhaal stappen 2-3 op alle resterende Webservers waarop [!DNL Sensor] wordt geïnstalleerd.
1. Start de oorspronkelijke doelserver (als deze nog moet worden gebruikt) en de nieuwe doelserver opnieuw op.
1. De gegevens zullen beginnen overbrengend aan de nieuwe doelserver die u hebt gespecificeerd.

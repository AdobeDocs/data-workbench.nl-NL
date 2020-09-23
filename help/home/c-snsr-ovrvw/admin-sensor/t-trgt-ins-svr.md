---
description: Om de server van de gegevenswerkbank te veranderen waarmee een Sensor (de doelserver) communiceert, moet u het txlogd.conf- dossier op elk van de Webservers uitgeven waarop Sensor wordt geïnstalleerd.
solution: Analytics
title: De doelserver voor Data Workbench wijzigen
uuid: 931d376d-8622-4858-8290-19ce91538570
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---


# De doelserver voor Data Workbench wijzigen{#changing-the-target-data-workbench-server}

Om de server van de gegevenswerkbank te veranderen waarmee een Sensor (de doelserver) communiceert, moet u het txlogd.conf- dossier op elk van de Webservers uitgeven waarop Sensor wordt geïnstalleerd.

**Wijzigen in doel[!DNL data workbench server]**

1. Stop zowel de oorspronkelijke doelserver als de nieuwe doelserver.
1. Kopieer het meest recente [!DNL .vsl] bestand van de oorspronkelijke doelserver naar de nieuwe doelserver. Wanneer u de nieuwe doelserver later opnieuw opstart, worden alle nieuwe [!DNL Sensor] gegevens toegevoegd aan het huidige, bestaande [!DNL .vsl] bestand in plaats van een nieuw [!DNL .vsl] bestand te maken. Voer daartoe de volgende stappen uit:

   1. Blader op de oorspronkelijke doelserver naar de [!DNL \Logs] map in de [!DNL data workbench server] installatiemap.

   1. Kopieer het meest recente [!DNL .vsl] bestand in de map.
   1. Blader op de nieuwe doelserver naar de [!DNL \Logs] map in de [!DNL data workbench server] installatiemap en plak het [!DNL .vsl] bestand in deze map.

1. Open en bewerk het [!DNL Sensor] bestand op een van de webservers waarop het [!DNL txlogd.conf] is geïnstalleerd. Voer daartoe de volgende stappen uit:

   1. Blader naar de [!DNL Sensor] installatiemap en open het [!DNL txlogd.conf] bestand in een teksteditor.

   1. Bepaal de plaats van de parameter ServerAddress en verander het om op het adres van de nieuwe doelserver te wijzen.
   1. Sla het bestand op en sluit het.

1. Herhaal stap 2-3 op alle resterende webservers waarop [!DNL Sensor] is geïnstalleerd.
1. Start de oorspronkelijke doelserver (als deze nog moet worden gebruikt) en de nieuwe doelserver opnieuw.
1. Gegevens worden verzonden naar de nieuwe doelserver die u hebt opgegeven.

---
description: Om de server van de gegevenswerkbank te veranderen waarmee een Sensor (de doelserver) communiceert, moet u het txlogd.conf- dossier op elk van de Webservers uitgeven waarop Sensor wordt geïnstalleerd.
title: De doelserver voor Data Workbench wijzigen
uuid: 931d376d-8622-4858-8290-19ce91538570
exl-id: 9d18cae1-4037-48c6-8514-3278e2c73b47
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# De doelserver voor Data Workbench wijzigen{#changing-the-target-data-workbench-server}

{{eol}}

Om de server van de gegevenswerkbank te veranderen waarmee een Sensor (de doelserver) communiceert, moet u het txlogd.conf- dossier op elk van de Webservers uitgeven waarop Sensor wordt geïnstalleerd.

**Wijzigen in doel[!DNL data workbench server]**

1. Stop zowel de oorspronkelijke doelserver als de nieuwe doelserver.
1. De meest recente kopiëren [!DNL .vsl] van de oorspronkelijke doelserver naar de nieuwe doelserver. Wanneer u de nieuwe doelserver in een latere stap opnieuw start, veroorzaakt dit alle nieuwe [!DNL Sensor] gegevens die moeten worden toegevoegd aan de huidige, bestaande [!DNL .vsl] in plaats van een nieuw bestand te maken [!DNL .vsl] bestand. Voer daartoe de volgende stappen uit:

   1. Blader op de oorspronkelijke doelserver naar de [!DNL \Logs] in de [!DNL data workbench server] installatiemap.

   1. De meest recente kopiëren [!DNL .vsl] in de map.
   1. Blader op de nieuwe doelserver naar de [!DNL \Logs] in de [!DNL data workbench server] installatiemap en plak de [!DNL .vsl] bestand naar deze map.

1. Op een van de webservers waarop [!DNL Sensor] is geïnstalleerd, opent en bewerkt u de [!DNL txlogd.conf] bestand. Voer daartoe de volgende stappen uit:

   1. Bladeren naar de [!DNL Sensor] installatiemap en open de [!DNL txlogd.conf] in een teksteditor.

   1. Bepaal de plaats van de parameter ServerAddress en verander het om op het adres van de nieuwe doelserver te wijzen.
   1. Sla het bestand op en sluit het.

1. Herhaal stap 2-3 op alle resterende webservers waarop [!DNL Sensor] is geïnstalleerd.
1. Start de oorspronkelijke doelserver (als deze nog moet worden gebruikt) en de nieuwe doelserver opnieuw.
1. Gegevens worden verzonden naar de nieuwe doelserver die u hebt opgegeven.

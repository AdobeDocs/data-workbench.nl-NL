---
description: Stappen om de vereiste Microsoft-componenten te installeren.
title: Vereiste componenten installeren
uuid: e23fba09-4684-4daf-8426-ea91169b3348
exl-id: d39cb14e-7cce-4088-8301-8ff566c0bde4
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Vereiste componenten installeren{#installing-required-components}

{{eol}}

Stappen om de vereiste Microsoft-componenten te installeren.

1. Installeer Microsoft .NET Framework v4.0.

   >[!NOTE]
   >
   >Dit moet slechts na het installeren en het vormen van de Rol van het Web IIS worden geïnstalleerd.

1. Volg de wizard en kies de standaardinstellingen als u hierom wordt gevraagd om de installatie te voltooien.
1. Zodra geïnstalleerd, verifieer dat de ASP.NET v.4.0 toepassingspool binnen werd toegevoegd **[!UICONTROL Application Pools]** lijst in IIS.
1. Installeer de Microsoft SQL Server-database.

   Gebruik om het even welke versie van SQL Server 2008 of 2008 R2 (Uitdrukkelijke wordt gesteund) met de Hulpmiddelen van het Beheer (Adobe adviseert SQL Server 2008 R2 SP1 - Uitdrukkelijke Uitgave). 1. Voor een generische installatie zonder bestaande SQL instanties van de Server die voortijdig lopen, gelieve te selecteren **[!UICONTROL Default Instance]** de optie **[!UICONTROL Instance Configuration]** scherm.
1. Voor de rest van de configuratieopties, volg de tovenaar en kies gebreken wanneer ertoe aangezet om de installatie te voltooien.
1. Installeer Microsoft Web Deploy v2.0.

   Voor de meeste installaties, **[!UICONTROL Typical]** installatie is prima. Als u echter externe implementaties wilt uitvoeren, moet u een volledige installatie uitvoeren (kies **[!UICONTROL Complete]**).

   Als alle voorwaarden correct zijn geïnstalleerd, kunt u de gegevensworkbench-servers voorbereiden op communicatie met het dashboard.

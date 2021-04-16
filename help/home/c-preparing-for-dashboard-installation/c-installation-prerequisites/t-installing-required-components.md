---
description: Stappen om de vereiste componenten van Microsoft te installeren.
title: Vereiste componenten installeren
uuid: e23fba09-4684-4daf-8426-ea91169b3348
exl-id: d39cb14e-7cce-4088-8301-8ff566c0bde4
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# Vereiste componenten installeren{#installing-required-components}

Stappen om de vereiste componenten van Microsoft te installeren.

1. Installeer Microsoft .NET Framework v4.0.

   >[!NOTE]
   >
   >Dit moet slechts na het installeren en het vormen van de Rol van het Web IIS worden geïnstalleerd.

1. Volg de wizard en kies de standaardinstellingen als u hierom wordt gevraagd om de installatie te voltooien.
1. Zodra geïnstalleerd, verifieer dat de ASP.NET v.4.0 toepassingspool binnen **[!UICONTROL Application Pools]** lijst in IIS werd toegevoegd.
1. Installeer de Microsoft SQL Server-database.

   Gebruik om het even welke versie van SQL Server 2008 of 2008 R2 (Uitdrukkelijke wordt gesteund) met de Hulpmiddelen van het Beheer (Adobe adviseert SQL Server 2008 R2 SP1 - Uitdrukkelijke Uitgave). 1. Voor een generieke installatie zonder bestaande SQL Server-instanties die van tevoren worden uitgevoerd, selecteert u de optie **[!UICONTROL Default Instance]** op het **[!UICONTROL Instance Configuration]**-scherm.
1. Voor de rest van de configuratieopties, volg de tovenaar en kies gebreken wanneer ertoe aangezet om de installatie te voltooien.
1. Microsoft Web Deploy v2.0 installeren.

   Voor de meeste installaties is de **[!UICONTROL Typical]** installatie in orde. Als u echter externe implementaties wilt uitvoeren, moet u een volledige installatie uitvoeren (kies **[!UICONTROL Complete]**).

   Als alle voorwaarden correct zijn geïnstalleerd, kunt u de gegevensworkbench-servers voorbereiden op communicatie met het dashboard.

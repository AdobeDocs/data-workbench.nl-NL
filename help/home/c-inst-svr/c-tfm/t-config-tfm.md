---
description: De functionaliteit van de transformatie stelt op een machine van FSU van de Server van het Inzicht in werking om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.
title: Transformatie configureren
uuid: 0526704a-71b2-4094-9d3a-1ba84f4dc287
exl-id: 5dbd70e4-55fc-4446-b687-525e7957209b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Transformatie configureren{#configuring-transform}

De functionaliteit van de transformatie stelt op een machine van FSU van de Server van het Inzicht in werking om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.

[!DNL Transform] U kunt  [!DNL .vsl] bestanden, logbestanden, XML-bestanden en ODBC-gegevens lezen en de gegevens exporteren als  [!DNL .vsl] bestanden, tekstbestanden of tekstbestanden met scheidingstekens die kunnen worden gebruikt door het laden van routines, controlebureaus of andere doelen in een gegevenspakhuis. De gegevensextractie en -transformatie kunnen doorlopend of op een andere geplande basis worden uitgevoerd. Elk [!DNL Insight Server] FSU dat output van veranderde gebeurtenisgegevens verstrekt moet [!DNL Transform] in werking stellen.

>[!NOTE]
>
>[!DNL Transform] wordt meestal op een [!DNL Insight Server] FSU geïnstalleerd. Uw implementatie moet mogelijk worden geïnstalleerd op een [!DNL Insight Server] DPU. Neem voor meer informatie contact op met Adobe.

Raadpleeg het document *Minimale systeemvereisten* voor informatie over de systeemvereisten voor het installeren, configureren en gebruiken van [!DNL Transform].

Adobe verspreidt de [!DNL Transform]-functionaliteit als een profiel binnen het [!DNL .zip]-bestand voor het [!DNL Insight Server]-releasepakket. Het profiel [!DNL Transform] is een intern profiel dat extra functionaliteit aan [!DNL Insight Server] verstrekt. Zoals bij alle andere interne profielen die door Adobe worden verstrekt, zou het profiel niet moeten worden veranderd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Het profiel bestaat uit de volgende bestanden:

* [!DNL Log Processing.cfg]
* [!DNL [!DNL Insight] Transform.cfg]
* [!DNL [!DNL Insight] Transform Mode.cfg]
* een gegevensbestand van de logboekverwerking omvat

Al deze bestanden bevinden zich in de map [!DNL Dataset] voor het profiel.

**Het  [!DNL Transform] profiel installeren op[!DNL Insight Server]**

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u [!DNL Insight] hebt geïnstalleerd en een verbinding tot stand hebt gebracht tussen [!DNL Insight] en [!DNL Insight Server] waarop u [!DNL Transform] installeert. Als u dit niet hebt gedaan, zie * [!DNL Insight] Gids van de Gebruiker*.

1. Open het [!DNL .zip]-bestand voor het [!DNL Insight Server]-releasepakket en open de map [!DNL Profiles] in dat [!DNL .zip]-bestand.
1. Kopieer de map [!DNL Transform] naar de map [!DNL Profiles] in de installatiemap [!DNL Insight Server]. U wilt uiteindelijk een [!DNL ...\Profiles\Transform] map op uw [!DNL Insight Server] plaatsen, zoals in het volgende voorbeeld wordt getoond.

   ![Stapinfo](assets/win_installTransformProfile.png)

   >[!NOTE]
   >
   >Als u alle stappen voor het installeren van [!DNL Insight Server] (zie [Insight Server](../../../home/c-inst-svr/c-msr-server/c-msr-server.md)) hebt gevolgd, hebt u mogelijk al een [!DNL Transform] omslag in de folder van Profielen.

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor het profiel bij te werken waarmee u [!DNL Transform] wilt gebruiken. De dataset herwerkt na voltooiing van deze stappen.

   1. Open [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het venster [!DNL profile.cfg] verschijnt.

   1. Klik in het venster [!DNL profile.cfg]met de rechtermuisknop **[!UICONTROL Directories]** en klik **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Als u de nieuwe map wilt toevoegen aan het einde van de lijst met directory&#39;s, klikt u met de rechtermuisknop op het nummer of de naam van de laatste map in de lijst en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe map: [!DNL Transform]
   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd (inclusief het profiel), omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

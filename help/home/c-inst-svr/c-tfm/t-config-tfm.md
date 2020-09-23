---
description: De functionaliteit van de transformatie stelt op een machine van FSU van de Server van het Inzicht in werking om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.
solution: Analytics
title: Transformatie configureren
uuid: 0526704a-71b2-4094-9d3a-1ba84f4dc287
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---


# Transformatie configureren{#configuring-transform}

De functionaliteit van de transformatie stelt op een machine van FSU van de Server van het Inzicht in werking om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.

[!DNL Transform] U kunt [!DNL .vsl] bestanden, logbestanden, XML-bestanden en ODBC-gegevens lezen en de gegevens exporteren als [!DNL .vsl] bestanden, tekstbestanden of tekstbestanden met scheidingstekens die kunnen worden gebruikt door het laden van routines, controlebureaus of andere doelen in een gegevenspakhuis. De gegevensextractie en -transformatie kunnen doorlopend of op een andere geplande basis worden uitgevoerd. Elke [!DNL Insight Server] FSU die output van veranderde gebeurtenisgegevens verstrekt moet lopen [!DNL Transform].

>[!NOTE]
>
>Meestal [!DNL Transform] is dit geïnstalleerd op een [!DNL Insight Server] FSU. Nochtans, kan uw implementatie installatie op [!DNL Insight Server] DPU vereisen. Neem voor meer informatie contact op met Adobe.

Raadpleeg het document [!DNL Transform]Minimale systeemvereisten voor ** informatie over de systeemvereisten voor installatie, configuratie en werking.

Adobe verspreidt de [!DNL Transform] functionaliteit als een profiel binnen het [!DNL .zip] bestand voor het [!DNL Insight Server] releasepakket. Het [!DNL Transform] profiel is een intern profiel dat aanvullende functionaliteit biedt aan [!DNL Insight Server]. Zoals bij alle andere interne profielen die door Adobe worden verstrekt, zou het profiel niet moeten worden veranderd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Het profiel bestaat uit de volgende bestanden:

* [!DNL Log Processing.cfg]
* [!DNL [!DNL Insight] Transform.cfg]
* [!DNL [!DNL Insight] Transform Mode.cfg]
* een gegevensbestand van de logboekverwerking omvat

Al deze bestanden bevinden zich in de [!DNL Dataset] map voor het profiel.

**Het[!DNL Transform]profiel installeren op[!DNL Insight Server]**

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u een verbinding hebt geïnstalleerd [!DNL Insight] en tot stand hebt gebracht tussen [!DNL Insight] en de [!DNL Insight Server] installatie waarop u installeert [!DNL Transform]. Zie de * [!DNL Insight] Gebruikershandleiding* als u dit nog niet hebt gedaan.

1. Open het [!DNL .zip] bestand voor het [!DNL Insight Server] releasepakket en open de [!DNL Profiles] map in dat [!DNL .zip] bestand.
1. Kopieer de [!DNL Transform] map naar de [!DNL Profiles] map in de [!DNL Insight Server] installatiemap. U wilt eindigen met een [!DNL ...\Profiles\Transform] map op uw computer, [!DNL Insight Server] zoals in het volgende voorbeeld wordt getoond.

   ![Stapinfo](assets/win_installTransformProfile.png)

   >[!NOTE]
   >
   >Als u alle stappen voor het installeren volgde [!DNL Insight Server] (zie de Server [van het](../../../home/c-inst-svr/c-msr-server/c-msr-server.md)Inzicht), kunt u reeds een [!DNL Transform] omslag in de folder van Profielen hebben.

1. Voer de volgende stappen uit om het [!DNL profile.cfg] bestand bij te werken voor het profiel waarmee u wilt werken [!DNL Transform]. De dataset herwerkt na voltooiing van deze stappen.

   1. Open de [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL User] kolom wordt een vinkje voor dit bestand weergegeven.

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het [!DNL profile.cfg] venster verschijnt.

   1. Klik in het [!DNL profile.cfg]venster met de rechtermuisknop **[!UICONTROL Directories]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Als u de nieuwe map wilt toevoegen aan het einde van de lijst met mappen, klikt u met de rechtermuisknop op het nummer of de naam van de laatste map in de lijst en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe map: [!DNL Transform]
   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik in het [!DNL Profile Manager]vak met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd (inclusief het profiel), omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.


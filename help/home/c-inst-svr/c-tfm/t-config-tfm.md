---
description: De functionaliteit van de transformatie stelt op een machine van FSU van de Server van het Inzicht in werking om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.
title: Transformatie configureren
uuid: 0526704a-71b2-4094-9d3a-1ba84f4dc287
exl-id: 5dbd70e4-55fc-4446-b687-525e7957209b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# Transformatie configureren{#configuring-transform}

{{eol}}

De functionaliteit van de transformatie stelt op een machine van FSU van de Server van het Inzicht in werking om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.

[!DNL Transform] kan lezen [!DNL .vsl] bestanden, logbestanden, XML-bestanden en ODBC-gegevens en exporteer de gegevens als [!DNL .vsl] bestanden, tekstbestanden of tekstbestanden met scheidingstekens die kunnen worden gebruikt door het laden van routines, auditbureaus of andere doelen in een gegevenspakhuis. De gegevensextractie en -transformatie kunnen doorlopend of op een andere geplande basis worden uitgevoerd. Elk [!DNL Insight Server] FSU die output van veranderde gebeurtenisgegevens verstrekt moet lopen [!DNL Transform].

>[!NOTE]
>
>Doorgaans [!DNL Transform] is geïnstalleerd op een [!DNL Insight Server] FSU. Voor uw implementatie is mogelijk installatie op een [!DNL Insight Server] DPU. Neem voor meer informatie contact op met Adobe.

Voor informatie over de systeemvereisten voor installatie, configuratie en werking [!DNL Transform], zie de *Minimale systeemvereisten* document.

Adobe verspreidt de [!DNL Transform] als een profiel binnen de [!DNL .zip] bestand voor de [!DNL Insight Server] releasepakket. De [!DNL Transform] profiel is een intern profiel dat aanvullende functionaliteit biedt voor [!DNL Insight Server]. Zoals bij alle andere interne profielen die door Adobe worden verstrekt, zou het profiel niet moeten worden veranderd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Het profiel bestaat uit de volgende bestanden:

* [!DNL Log Processing.cfg]
* [!DNL [!DNL Insight] Transform.cfg]
* [!DNL [!DNL Insight] Transformatiemodus.cfg]
* een gegevensbestand van de logboekverwerking omvat

Al deze bestanden bevinden zich in het dialoogvenster [!DNL Dataset] voor het profiel.

**Als u het dialoogvenster [!DNL Transform] profiel op[!DNL Insight Server]**

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u [!DNL Insight] en een verband tot stand heeft gebracht tussen [!DNL Insight] en de [!DNL Insight Server] waarop u installeert [!DNL Transform]. Als u dit nog niet hebt gedaan, raadpleegt u de * [!DNL Insight] Gebruikershandleiding*.

1. Open de [!DNL .zip] bestand voor de [!DNL Insight Server] releasepakket en open de [!DNL Profiles] map binnen die [!DNL .zip] bestand.
1. Kopieer de [!DNL Transform] aan de [!DNL Profiles] in uw [!DNL Insight Server] installatiemap. U wilt eindigen met een [!DNL ...\Profiles\Transform] map op uw [!DNL Insight Server] zoals getoond in het volgende voorbeeld.

   ![Stapinfo](assets/win_installTransformProfile.png)

   >[!NOTE]
   >
   >Als u alle stappen voor de installatie hebt uitgevoerd [!DNL Insight Server] (zie [Insight Server](../../../home/c-inst-svr/c-msr-server/c-msr-server.md)), hebt u mogelijk al een [!DNL Transform] in de map Profielen.

1. Gebruik de volgende stappen om de [!DNL profile.cfg] bestand voor het profiel dat u wilt gebruiken [!DNL Transform]. De dataset herwerkt na voltooiing van deze stappen.

   1. Open de [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. De [!DNL profile.cfg] wordt weergegeven.

   1. In de [!DNL profile.cfg]venster, klik met de rechtermuisknop **[!UICONTROL Directories]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Als u de nieuwe map wilt toevoegen aan het einde van de lijst met mappen, klikt u met de rechtermuisknop op het nummer of de naam van de laatste map in de lijst en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe map: [!DNL Transform]
   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd (inclusief het profiel), omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

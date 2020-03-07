---
description: De functionaliteit van de transformatie loopt op een machine van FSU van de Server van het Inzicht om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.
solution: Insight
title: Transformatie configureren
uuid: 0526704a-71b2-4094-9d3a-1ba84f4dc287
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Transformatie configureren{#configuring-transform}

De functionaliteit van de transformatie loopt op een machine van FSU van de Server van het Inzicht om de uitvoer van logboekbrongegevens voor gebruik door andere toepassingen toe te laten.

[!DNL Transform] kan [!DNL .vsl] dossiers, logboekdossiers, de dossiers van XML, en ODBC- gegevens lezen en de gegevens uitvoeren als [!DNL .vsl] dossiers, tekstdossiers, of afgebakende tekstdossiers die door het laden van het gegevenspakhuis routines, controlebureaus, of andere doelstellingen kunnen worden gebruikt. De gegevensextractie en -transformatie kan op een continue of andere geplande basis worden uitgevoerd. Elke [!DNL Insight Server] FSU die output van veranderde gebeurtenisgegevens verstrekt moet lopen [!DNL Transform].

>[!NOTE]
>
>Typisch, [!DNL Transform] is geïnstalleerd op een [!DNL Insight Server] FSU. Nochtans, kan uw implementatie installatie op een [!DNL Insight Server] DPU vereisen. Voor meer informatie, contacteer Adobe.

Raadpleeg het document [!DNL Transform]Systeemvereisten *voor informatie over de systeemvereisten voor installatie, configuratie en gebruik* in het documentMinimale systeemvereisten.

Adobe verdeelt de [!DNL Transform] functionaliteit als profiel binnen het [!DNL .zip] dossier voor het [!DNL Insight Server] versiepakket. Het [!DNL Transform] profiel is een intern profiel dat extra functionaliteit aan verstrekt [!DNL Insight Server]. Zoals met alle andere interne profielen die door Adobe worden verstrekt, zou het profiel niet moeten worden veranderd. Al aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Het profiel bestaat uit de volgende bestanden:

* [!DNL Log Processing.cfg]
* [!DNL [!DNL Insight] Transform.cfg]
* [!DNL [!DNL Insight] Transform Mode.cfg]
* een dataset van de logboekverwerking omvat dossier

Al deze dossiers worden gevestigd in de [!DNL Dataset] omslag voor het profiel.

**Om het[!DNL Transform]profiel te installeren op[!DNL Insight Server]**

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u een verbinding hebt geïnstalleerd [!DNL Insight] en gemaakt tussen [!DNL Insight] en de [!DNL Insight Server] installatie waarop u de installatie uitvoert [!DNL Transform]. Als u dit nog niet hebt gedaan, raadpleegt u de * [!DNL Insight] Gebruikershandleiding*.

1. Open het [!DNL .zip] dossier voor het [!DNL Insight Server] versiepakket, en open de [!DNL Profiles] omslag binnen dat [!DNL .zip] dossier.
1. Kopieer de [!DNL Transform] omslag aan de [!DNL Profiles] omslag in uw [!DNL Insight Server] installatiefolder. U wilt met een [!DNL ...\Profiles\Transform] omslag op uw eindigen [!DNL Insight Server] zoals aangetoond in het volgende voorbeeld.

   ![Stapgegevens](assets/win_installTransformProfile.png)

   >[!NOTE]
   >
   >Als u alle stappen voor het installeren [!DNL Insight Server] (zie de Server [van het](../../../home/c-inst-svr/c-msr-server/c-msr-server.md)Inzicht) volgde, kunt u reeds een [!DNL Transform] omslag in de folder van Profielen hebben.

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor het profiel bij te werken waarmee u wilt gebruiken [!DNL Transform]. De dataset verwerkt na voltooiing van deze stappen opnieuw.

   1. Open de [!DNL Profile Manager].
   1. Klik het vinkje naast met de rechtermuisknop aan [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

   1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het [!DNL profile.cfg] venster wordt weergegeven.

   1. Klik in het [!DNL profile.cfg]venster met de rechtermuisknop **[!UICONTROL Directories]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Om de nieuwe folder aan het eind van de lijst van folders toe te voegen, klik het aantal of de naam van de laatste folder in de lijst met de rechtermuisknop aan en klik **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe folder: [!DNL Transform]
   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in de [!DNL Profile Manager], rechtsklik op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe (inclusief het profiel) worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.


---
description: Als Insight geen verbinding kan maken met de Insight Server(s) met behulp van de opgegeven instellingen, wordt een rood knooppunt weergegeven in de Servers Manager.
title: Verbindingsproblemen oplossen
uuid: 17190cee-da5c-449f-aca5-8e9e35e0a5fd
exl-id: 7938d4d6-e1ab-46d9-9ccb-cf79677c5688
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Verbindingsproblemen oplossen{#connection-troubleshooting}

{{eol}}

Als Insight geen verbinding kan maken met de Insight Server(s) met behulp van de opgegeven instellingen, wordt een rood knooppunt weergegeven in de Servers Manager.

Dit kan bijvoorbeeld gebeuren als u de verbinding onjuist configureert of als u geen toestemming hebt om de [!DNL Insight Server’s] status.

**Om te bepalen waarom Insight geen verbinding kan vestigen**

1. Klik met de rechtermuisknop op het rode serverknooppunt en klik op **[!UICONTROL Detailed Status]**.
1. In de [!DNL Detailed Status] interface, klik **[!UICONTROL Network Connections]** en breid de genummerde items uit. De [!DNL Status] parameter verstrekt informatie over waarom Insight geen verbinding kan vestigen:

   * Een statuscode in de jaren 500 geeft een configuratiefout aan.
   * Een statuscode van 403 geeft meestal aan dat u geen toestemming hebt om de status van de server weer te geven.

U kunt aanvullende statusinformatie weergeven in het dialoogvenster [!DNL insight.log] bestand. Dit logbestand bevindt zich in het dialoogvenster [!DNL Trace] map in de map waarin u Insight hebt geïnstalleerd. Open het bestand in een teksteditor, zoals Kladblok, om het bestand weer te geven.

Als u hulp nodig hebt om de informatie in de [!DNL insight.log] , neemt u eerst contact op met de systeembeheerder. Neem contact op met de klantenservice van Adobe als u verdere hulp nodig hebt.

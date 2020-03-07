---
description: Als het Inzicht geen verbinding kan maken met de Insight Server(s) met behulp van de opgegeven instellingen, wordt een rode node weergegeven in de Servers Manager.
title: Problemen met verbindingen oplossen
uuid: 17190cee-da5c-449f-aca5-8e9e35e0a5fd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Problemen met verbindingen oplossen{#connection-troubleshooting}

Als het Inzicht geen verbinding kan maken met de Insight Server(s) met behulp van de opgegeven instellingen, wordt een rode node weergegeven in de Servers Manager.

Dit zou kunnen voorkomen, bijvoorbeeld, als u verkeerd de verbinding vormt of u hebt geen toestemming om de [!DNL Insight Server’s] status te bekijken.

**Om te bepalen waarom het Inzicht geen verbinding kan vestigen**

1. Klik de rode serverknoop met de rechtermuisknop aan en klik **[!UICONTROL Detailed Status]**.
1. In de [!DNL Detailed Status] interface, klik **[!UICONTROL Network Connections]** en breid de genummerde punten uit. De [!DNL Status] parameter verstrekt informatie over waarom het Inzicht geen verbinding kan vestigen:

   * Een statuscode in de 500s wijst op een configuratiefout.
   * Een statuscode van 403 wijst gewoonlijk erop dat u geen toestemming hebt om de status van de server te bekijken.

U kunt extra statusinformatie in het [!DNL insight.log] dossier bekijken. Dit logboekdossier wordt gevestigd in de [!DNL Trace] omslag in de folder waar u Inzicht installeerde. Om het dossier te bekijken, open het in een tekstredacteur zoals Blocnote.

Als u hulp nodig hebt die de informatie in het [!DNL insight.log] dossier begrijpt, contacteer eerst uw systeembeheerder. Als u verdere hulp vereist, contacteer de Zorg van de Klant van Adobe.

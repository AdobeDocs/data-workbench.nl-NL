---
description: Informatie over het werken met de server van de Data Workbench of off-line of online.
title: Offline en online werken
uuid: 613699d4-6d06-4c3c-b0aa-620933ae4d67
exl-id: 1c9e0f4f-3172-40d3-b751-ebe6f9f57f8a
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Offline werken{#working-offline-and-online}

Informatie over het werken met de server van de Data Workbench of off-line of online.

Data Workbench downloadt automatisch updates van het profiel en de bijbehorende gegevens van de server van de Data Workbench als u een netwerkverbinding met [!DNL server] hebt en online werkt. Als u niet hebt opgegeven dat u online wilt werken, laadt Data Workbench het profiel en de bijbehorende gegevens uit de cache van uw computer. In dit geval bekijkt u de versie van het profiel en de bijbehorende gegevens die de laatste keer zijn gedownload dat u online met het profiel hebt gewerkt.

Offline werken biedt een voordeel voor de verwerkingssnelheid omdat u werkt vanuit de lokale cache en de gegevens opvraagt op uw eigen computer. Wanneer het werken online, moet elke vraag terug naar de server van de Data Workbench gaan, die langer duurt en u dwingt om met andere online gebruikers voor servermiddelen te concurreren. Zolang u een netwerkverbinding met de server van de Data Workbench hebt, houdt het werken off-line de server van de Data Workbench van het bijwerken van de profielen of de gegevens op uw Data Workbench, maar het verhindert u niet punten aan de server van de Data Workbench op te slaan.

Wegens de capaciteit om offline te werken, wordt de server van de Data Workbench gerangschikt om één of andere hoeveelheid verkeersinput in real time en één of andere hoeveelheid gegevens in de dataset, samen met één of ander aantal gebruikers van de Data Workbench te behandelen, maar het moet niet worden gerangschikt om het maximumaantal gezamenlijke gebruikers (die in de praktijk niet vaak) te steunen. Omdat de gebruikers gewoonlijk trends en verhoudingen zoeken, die de gegevens onderzoeken aangezien u gaat, in de meeste gevallen hebt u geen nauwkeurige tellingen nodig. Als er een behoefte is om aan nauwkeurige tellingen te vragen en op te lossen gebruikend huidige gegevens, kunt u online werken en dat krijgen, maar de vragen nemen langer om tot 100 percenten op te lossen.

**Online of offline werken**

Klik op de zijbalk op de instelling **[!UICONTROL Connection]** en klik op **[!UICONTROL Work Online]**.

![](assets/sidebar_work_online.png)

Wanneer u online werkt, verbindt de Data Workbench met de server van de Data Workbench en synchroniseert de informatie op uw machine met het profiel en zijn datasetinformatie die op de server van de Data Workbench verblijft.

De standaardconfiguratie voor Data Workbench moet offline werken, maar zoals beschreven in de volgende sectie, kan elke gebruiker zijn [!DNL Insight.cfg] dossier veranderen om hun geval van Data Workbench online door gebrek te maken werken.

**Standaard online werken**

1. Navigeer naar de installatiemap voor Insight.
1. Open het [!DNL Insight.cfg] dossier in een tekstredacteur.
1. Voeg de gemarkeerde regel toe aan het bestand, zoals in het volgende voorbeeld wordt getoond:

```
Update Software = bool: true
Default to Online = bool: true
Color Set = int: 0
```

De volgende keer dat u Data Workbench opent, maakt deze verbinding met de server van de Data Workbench en werkt standaard online.

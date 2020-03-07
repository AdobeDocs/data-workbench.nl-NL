---
description: Informatie over het werken met de server van de Werkbank van Gegevens of offline of online.
solution: Analytics
title: offline en online werken
topic: Data workbench
uuid: 613699d4-6d06-4c3c-b0aa-620933ae4d67
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# offline en online werken{#working-offline-and-online}

Informatie over het werken met de server van de Werkbank van Gegevens of offline of online.

De Werkbank van gegevens downloadt automatisch updates aan het profiel en zijn gegevens van de server van de Werkbank van Gegevens als u een netwerkverbinding aan hebt [!DNL server] en online werkt. Als u niet hebt gespecificeerd om online te werken, laadt de Werkbank van Gegevens het profiel en zijn gegevens van het geheime voorgeheugen van uw computer. In dit geval, bekijkt u de versie van het profiel en zijn gegevens die de laatste keer werd gedownload dat u online met het profiel werkte.

Het werken offline biedt een voordeel van de verwerkingssnelheid aan omdat u van het lokale geheime voorgeheugen werkt en de gegevens over uw eigen computer vraagt. Wanneer het werken online, moet elke vraag terug naar de server van de Werkbank van Gegevens gaan, die langer duurt en u dwingt om met andere online gebruikers voor servermiddelen te concurreren. Zolang u een netwerkverbinding met de server van de Werkbank van Gegevens hebt, houdt het werken offline de server van de Werkbank van Gegevens van het bijwerken van de profielen of de gegevens op uw Werkbank van Gegevens tegen, maar het houdt u niet tegen opslaat punten aan de server van de Werkbank van Gegevens.

Wegens de capaciteit om offline te werken, wordt de server van de Werkbank van Gegevens gerangschikt om één of andere hoeveelheid verkeersinput in real time en één of andere hoeveelheid gegevens in de dataset, samen met één of ander aantal gebruikers van de Werkbank van Gegevens te behandelen, maar het moet niet worden gerangschikt om het maximumaantal gezamenlijke gebruikers te steunen (die in de praktijk niet vaak gebeurt). Omdat de gebruikers gewoonlijk trends en verhoudingen zoeken, die de gegevens onderzoeken aangezien u gaat, in de meeste gevallen hebt u geen nauwkeurige tellingen nodig. Als er een behoefte aan vraag is en aan nauwkeurige tellingen op te lossen gebruikend huidige gegevens is, kunt u online werken en dat krijgen, maar de vragen duren langer om aan 100 percenten op te lossen.

**Om online of offline te werken**

In de zijbar, klik het **[!UICONTROL Connection]** plaatsen en klik **[!UICONTROL Work Online]**.

![](assets/sidebar_work_online.png)

Wanneer u online werkt, verbindt de Werkbank van Gegevens met de server van de Werkbank van Gegevens en synchroniseert de informatie over uw machine met het profiel en zijn datasetinformatie die op de server van de Werkbank van Gegevens verblijven.

De standaardconfiguratie voor de Werkbank van Gegevens moet off-line werken, maar zoals die in de volgende sectie wordt beschreven, kan elke gebruiker hun [!DNL Insight.cfg] dossier veranderen om hun geval van het werk van de Werkbank van Gegevens online door gebrek te maken.

**Standaard online werken**

1. Navigeer aan uw de installatiefolder van het Inzicht.
1. Open het [!DNL Insight.cfg] dossier in een tekstredacteur.
1. Voeg de benadrukte lijn aan het dossier toe zoals aangetoond in het volgende voorbeeld:

```
Update Software = bool: true
Default to Online = bool: true
Color Set = int: 0
```

De volgende tijd dat u de Werkbank van Gegevens opent, verbindt het met de server van de Werkbank van Gegevens en werkt online door gebrek.

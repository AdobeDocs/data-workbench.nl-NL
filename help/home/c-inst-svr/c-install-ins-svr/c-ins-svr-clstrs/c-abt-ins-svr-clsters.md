---
description: Een cluster van de Server van het Inzicht wordt vereist wanneer de hoeveelheid gegevens u voor uw gebruikers van Inzicht en Rapport wilt verwerken en toegankelijk maken de capaciteit van één enkele Server van het Inzicht overschrijdt.
solution: Analytics
title: Over Insight Server Clusters
uuid: d65e0fe5-f87d-4d8e-a208-9192e9d62fb5
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# Over Insight Server Clusters{#about-insight-server-clusters}

Een cluster van de Server van het Inzicht wordt vereist wanneer de hoeveelheid gegevens u voor uw gebruikers van Inzicht en Rapport wilt verwerken en toegankelijk maken de capaciteit van één enkele Server van het Inzicht overschrijdt.

Door een [!DNL Insight Server] cluster op te zetten, kunt u één enkele analysedataset over veelvoudige machines in een cluster verdelen om het verwerkingsvermogen van veelvoudige [!DNL Insight Servers]te gebruiken.

De eerste stap in de implementatie van een [!DNL Insight Server] cluster is het toewijzen van de [!DNL Insight Server] machines in uw cluster. De eerste [!DNL Insight Server] machine die u instelt, is uw master [!DNL Insight Server] (ook wel primair [!DNL Insight Server]).

>[!NOTE]
>
>Als u een Eenheid van de Server van het [!DNL Insight Server] Dossier (FSU) gebruikt, adviseert Adobe dat u FSU als master vormt [!DNL Insight Server]. Voor informatie over het vormen van een FSU, zie de Gids *van de Configuratie van de* Dataset.

Master [!DNL Insight Server] beheert de communicatie tussen elkaar [!DNL Insight Servers] in de cluster (genoemd verwerkingsservers of, soms, vraagservers) en instanties van [!DNL Insight] en [!DNL Report]. Voor een bepaalde dataset, komt de verwerking van het logboekdossier op (één of meerdere) aangewezen [!DNL Insight Servers] (master of verwerking) zoals die in de [!DNL Insight Server] configuratiedossiers wordt gespecificeerd voor. Wanneer het werken in een gegroepeerd milieu, [!DNL Insight] worden de installaties gevormd om tot master toegang te hebben [!DNL Insight Server], maar de vragen kunnen door om het even welk van [!DNL Insight Servers] binnen de cluster worden behandeld.

>[!NOTE]
>
>Het **bestand PAServer.cfg** . Als u de Predictive Analytics die banen groeperen aan de Servers van het Inzicht wilt voorleggen, dan zult u het [!DNL PAServer.cfg] dossier voor de behandeling van server-zij groeperen indieningen moeten vormen. Het aangepaste profiel moet de voorvertoning overnemen [!DNL PAServer.cfg] van het profiel Predictive Analytics ([!DNL Server\Profiles\Predictive Analytics\Dataset]). Stel een *Master server* in dit bestand in en sla de server [!DNL PAServer.cfg] op de implementatiesite op.
>
>
```
>PAServer = PAServerConfig: 
>   Master Server = serverInfo: 
>       Address = string: 
>       Port = int: 80
>       Use SSL = bool: false
>```

>[!IMPORTANT]
>
>De instructies in dit hoofdstuk zijn niet van toepassing op het maken van een [!DNL Insight Server] cluster die uit meer dan vijf (5) bestaat [!DNL Insight Servers]. Neem contact op met Adobe voor systeemvereisten en aanbevelingen voor profielconfiguratie voor clusters groter dan vijf [!DNL Insight Servers].

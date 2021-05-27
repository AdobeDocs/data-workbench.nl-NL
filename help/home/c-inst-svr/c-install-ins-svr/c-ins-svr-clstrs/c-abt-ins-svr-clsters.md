---
description: Een cluster van de Server van het Inzicht wordt vereist wanneer de hoeveelheid gegevens u voor uw gebruikers van Inzicht en Rapport wilt verwerken en toegankelijk maken de capaciteit van één enkele Server van het Inzicht overschrijdt.
title: Over Insight Server Clusters
uuid: d65e0fe5-f87d-4d8e-a208-9192e9d62fb5
exl-id: b26e0f63-76db-461d-91e7-0968624aa0f7
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Info over Insight Server Clusters{#about-insight-server-clusters}

Een cluster van de Server van het Inzicht wordt vereist wanneer de hoeveelheid gegevens u voor uw gebruikers van Inzicht en Rapport wilt verwerken en toegankelijk maken de capaciteit van één enkele Server van het Inzicht overschrijdt.

Door een [!DNL Insight Server] cluster op te zetten, kunt u één enkele analysedataset over veelvoudige machines in een cluster verdelen om het verwerkingsvermogen van veelvoudige [!DNL Insight Servers] te gebruiken.

De eerste stap in de implementatie van een [!DNL Insight Server] cluster is de [!DNL Insight Server] machines in uw cluster toe te wijzen. De eerste [!DNL Insight Server] machine die u opstelling is uw master [!DNL Insight Server] (die soms als uw primaire [!DNL Insight Server] wordt bedoeld).

>[!NOTE]
>
>Als u een [!DNL Insight Server] Eenheid van de Server van het Dossier (FSU) gebruikt, adviseert Adobe dat u FSU als master [!DNL Insight Server] vormt. Voor informatie over het vormen van een FSU, zie *de Gids van de Configuratie van de Dataset*.

Master [!DNL Insight Server] beheert de communicatie tussen andere [!DNL Insight Servers] in de cluster (genoemd verwerkingsservers of, soms, vraagservers) en instanties van [!DNL Insight] en [!DNL Report]. Voor een bepaalde dataset, komt de verwerking van het logboekdossier op (één of meerdere) aangewezen [!DNL Insight Servers] (master of verwerking) zoals die in de [!DNL Insight Server] configuratiedossiers wordt gespecificeerd voor. Wanneer het werken in een gegroepeerde milieu, [!DNL Insight] de installaties worden gevormd om tot master [!DNL Insight Server] toegang te hebben, maar de vragen kunnen door om het even welk [!DNL Insight Servers] binnen de cluster worden behandeld.

>[!NOTE]
>
>Het bestand **PAServer.cfg**. Als u de Predictive Analytics groeperende banen aan de Servers van het Inzicht wilt voorleggen, dan zult u het [!DNL PAServer.cfg] dossier voor de behandeling van server-zij groeperen indieningen moeten vormen. Het aangepaste profiel moet de [!DNL PAServer.cfg] overnemen van het profiel voor voorspellende analyse ([!DNL Server\Profiles\Predictive Analytics\Dataset]). Stel een *Master server* in dit bestand in en sla [!DNL PAServer.cfg] op de implementatiesite op.
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
>De instructies in dit hoofdstuk zijn niet van toepassing op het maken van een [!DNL Insight Server]-cluster die uit meer dan vijf (5) [!DNL Insight Servers] bestaat. Neem contact op met Adobe voor systeemvereisten en aanbevelingen voor profielconfiguratie voor clusters groter dan vijf [!DNL Insight Servers].

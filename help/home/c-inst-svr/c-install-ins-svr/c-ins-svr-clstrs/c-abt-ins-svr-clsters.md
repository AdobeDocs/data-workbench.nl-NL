---
description: Een cluster van de Server van het Inzicht wordt vereist wanneer de hoeveelheid gegevens u voor uw gebruikers van Inzicht en Rapport wilt verwerken en toegankelijk maken de capaciteit van één enkele Server van het Inzicht overschrijdt.
title: Over Insight Server Clusters
uuid: d65e0fe5-f87d-4d8e-a208-9192e9d62fb5
exl-id: b26e0f63-76db-461d-91e7-0968624aa0f7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Over Insight Server Clusters{#about-insight-server-clusters}

{{eol}}

Een cluster van de Server van het Inzicht wordt vereist wanneer de hoeveelheid gegevens u voor uw gebruikers van Inzicht en Rapport wilt verwerken en toegankelijk maken de capaciteit van één enkele Server van het Inzicht overschrijdt.

Door een [!DNL Insight Server] cluster, kunt u één enkele analysedataset over veelvoudige machines in een cluster verdelen om het verwerkingsvermogen van veelvoudige [!DNL Insight Servers].

De eerste stap in de uitvoering van een [!DNL Insight Server] cluster moet de [!DNL Insight Server] in uw cluster. De eerste [!DNL Insight Server] de machine die u instelt, is uw master [!DNL Insight Server] (wordt ook wel de primaire [!DNL Insight Server]).

>[!NOTE]
>
>Als u een [!DNL Insight Server] De Eenheid van de Server van het dossier (FSU), Adobe adviseert dat u FSU als master vormt [!DNL Insight Server]. Voor informatie over het vormen van FSU, zie *Configuratie-handleiding voor gegevensset*.

De master [!DNL Insight Server] beheert de communicatie tussen elkaar [!DNL Insight Servers] in de cluster (verwerkingsservers of soms queryservers genoemd) en instanties van [!DNL Insight] en [!DNL Report]. Voor een bepaalde dataset, komt de verwerking van het logboekdossier op (één of meerdere aangewezen) voor [!DNL Insight Servers] (master of verwerkt) zoals gespecificeerd in de [!DNL Insight Server] configuratiebestanden. Wanneer het werken in een gegroepeerde milieu, [!DNL Insight] de installaties worden gevormd om tot master toegang te hebben [!DNL Insight Server], maar de vragen kunnen door om het even welk van [!DNL Insight Servers] binnen de cluster.

>[!NOTE]
>
>De **PAServer.cfg** bestand. Als u de Predictive Analytics groeperende banen aan de Servers van het Inzicht wilt voorleggen, dan zult u moeten vormen [!DNL PAServer.cfg] bestand voor de verwerking van serverclusteringverzendingen. Het aangepaste profiel moet de eigenschap [!DNL PAServer.cfg] uit het profiel Predictive Analytics ([!DNL Server\Profiles\Predictive Analytics\Dataset]). Een *Master server* in dit bestand en sla de [!DNL PAServer.cfg] naar de implementatielocatie.
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
>De instructies in dit hoofdstuk zijn niet van toepassing op het maken van een [!DNL Insight Server] cluster bestaande uit meer dan vijf (5) [!DNL Insight Servers]. Neem contact op met Adobe voor systeemvereisten en aanbevelingen voor profielconfiguratie voor clusters groter dan vijf [!DNL Insight Servers].

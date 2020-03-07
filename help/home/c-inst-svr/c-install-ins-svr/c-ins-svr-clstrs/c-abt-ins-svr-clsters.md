---
description: Een cluster van de Server van het Inzicht wordt vereist wanneer de hoeveelheid gegevens u toegankelijk voor uw gebruikers van Inzicht en Rapport wilt verwerken en maken de capaciteit van één enkele Server van het Inzicht overschrijdt.
solution: Insight
title: Over Insight Server Clusters
uuid: d65e0fe5-f87d-4d8e-a208-9192e9d62fb5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Over Insight Server Clusters{#about-insight-server-clusters}

Een cluster van de Server van het Inzicht wordt vereist wanneer de hoeveelheid gegevens u toegankelijk voor uw gebruikers van Inzicht en Rapport wilt verwerken en maken de capaciteit van één enkele Server van het Inzicht overschrijdt.

Door vestiging kan een [!DNL Insight Server] cluster, u één enkele analysetoevoegsel over veelvoudige machines in een cluster verdelen om de verwerkingscapaciteit van veelvoudige te gebruiken [!DNL Insight Servers].

De eerste stap in de implementatie van een [!DNL Insight Server] cluster is de [!DNL Insight Server] machines in uw cluster toe te wijzen. De eerste [!DNL Insight Server] machine die u opstelt, is uw master [!DNL Insight Server] (soms uw primaire [!DNL Insight Server]).

>[!NOTE]
>
>Als u een Eenheid van de Server van het [!DNL Insight Server] Dossier (FSU) gebruikt, adviseert Adobe dat u FSU als uw meester vormt [!DNL Insight Server]. Voor informatie over het vormen van een FSU, zie de Gids *van de Configuratie van de* Dataset.

De meester [!DNL Insight Server] beheert de communicatie tussen andere [!DNL Insight Servers] in de cluster (genoemd verwerkingsservers of, soms, vraagservers) en instanties van [!DNL Insight] en [!DNL Report]. Voor een bepaalde dataset, komt de verwerking van het logboekdossier op (één of meerdere) aangewezen voor [!DNL Insight Servers] (meester of verwerking) zoals die in de [!DNL Insight Server] configuratiedossiers wordt gespecificeerd. Wanneer het werken in een gegroepeerd milieu, worden de [!DNL Insight] installaties gevormd om tot de meester toegang te hebben [!DNL Insight Server], maar de vragen kunnen door om het even welk van de [!DNL Insight Servers] binnen de cluster worden behandeld.

>[!NOTE]
>
>Het **PAServer.cfg** - dossier. Als u Predictive Analytics wilt voorleggen die banen groeperen zich aan de Servers van het Inzicht, dan zult u het [!DNL PAServer.cfg] dossier voor de behandeling van server-zij groeperende indieningen moeten vormen. Het douaneprofiel zou [!DNL PAServer.cfg] van het Predictive Analytics profiel ( [!DNL Server\Profiles\Predictive Analytics\Dataset]) moeten erven. Plaats een *HoofdServer* in dit dossier en sla [!DNL PAServer.cfg] aan de implementatieplaats op. >
>
```>
>PAServer = PAServerConfig: 
>   Master Server = serverInfo: 
>       Address = string: 
>       Port = int: 80
>       Use SSL = bool: false
>```>



>[!IMPORTANT]
>
>De instructies in dit hoofdstuk zijn niet van toepassing op het aanmaken van een [!DNL Insight Server] cluster bestaande uit meer dan vijf (5) [!DNL Insight Servers]. Tevreden om Adobe te contacteren om systeemvereisten en de aanbevelingen van de profielconfiguratie voor clusters te verkrijgen groter dan vijf [!DNL Insight Servers].


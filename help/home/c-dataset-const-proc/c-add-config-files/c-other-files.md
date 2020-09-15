---
description: De map Dataset bevat aanvullende bestanden die vereist zijn voor de werking van de software of die aanvullende functionaliteit bieden voor de Adobe-implementatie.
solution: Analytics
title: Overige bestanden
topic: Data workbench
uuid: 87d83fa5-df25-4da1-8b11-16639902d8d7
translation-type: tm+mt
source-git-commit: 98452ba81d71db65c75e3d07712eefa18c003f53
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# Overige bestanden{#other-files}

De map Dataset bevat aanvullende bestanden die vereist zijn voor de werking van de software of die aanvullende functionaliteit bieden voor de Adobe-implementatie.

* **[!DNL Client.cfg:]** Het [!DNL Client.cfg] bestand in de map Dataset voor het [!DNL Base] profiel is vereist voor de werking van de software. Verwijder of wijzig geen parameters in het [!DNL Client.cfg] bestand.

* **[!DNL Cluster.cfg:]** Het [!DNL Cluster.cfg] bestand in de map Dataset voor het [!DNL Base] profiel is vereist voor de werking van de software. In het [!DNL Cluster.cfg] dossier, zou u slechts de Normalize parameter van de Server moeten wijzigen als u een dataset vormt die op een de servercluster van de gegevenswerkbank moet worden verwerkt. Voor instructies om de Normalize parameter van de Server te wijzigen, zie het [Creëren van een Gecentraliseerde Server van de Normalisatie voor een Cluster](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

* **[!DNL Insight Transform.cfg]en[!DNL Insight Transform Mode.cfg]:** Als u transformatiefunctionaliteit gebruikt, hebt u twee extra configuratiebestanden, gegevenswerkbank [!DNL Transform.cfg] en gegevenswerkbank [!DNL TransformMode.cfg], in de directory Gegevensset voor het [!DNL Transform] profiel. Zie Functionaliteit [](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/transform/t-config-tfm.html)transformeren voor informatie over deze bestanden en de bijbehorende parameters.

* Het **bestand PAServer.cfg** . Als u de Predictive Analytics die banen groeperen aan de Servers van het Inzicht wilt voorleggen, dan zult u het [!DNL PAServer.cfg] dossier voor de behandeling van server-zij groeperen indieningen moeten vormen.
Het aangepaste profiel moet het overnemen [!DNL PAServer.cfg] van het profiel Voorspellende analyse ( [!DNL Server\Profiles\Predictive Analytics\Dataset]).

   >[!IMPORTANT]
   >
   >Stel een *Master server* in dit bestand in en sla de server [!DNL PAServer.cfg] op de implementatiesite op.
   >
   >
   ```
   >PAServer = PAServerConfig: 
   >   Master Server = serverInfo: 
   >       Address = string: 
   >       Port = int: 80
   >       Use SSL = bool: false
   >```


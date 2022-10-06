---
description: De map Dataset bevat aanvullende bestanden die vereist zijn voor de werking van de software of die aanvullende functionaliteit bieden voor de Adobe-implementatie.
title: Overige bestanden
uuid: 87d83fa5-df25-4da1-8b11-16639902d8d7
exl-id: 0a1fb37c-00ac-46d4-9d0a-904ebd3ccfba
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Overige bestanden{#other-files}

{{eol}}

De map Dataset bevat aanvullende bestanden die vereist zijn voor de werking van de software of die aanvullende functionaliteit bieden voor de Adobe-implementatie.

* **[!DNL Client.cfg:]** De [!DNL Client.cfg] bestand in de map DataSet voor de [!DNL Base] profiel is vereist voor de werking van de software. Verwijder of wijzig geen parameters in het dialoogvenster [!DNL Client.cfg] bestand.

* **[!DNL Cluster.cfg:]** De [!DNL Cluster.cfg] bestand in de map DataSet voor de [!DNL Base] profiel is vereist voor de werking van de software. In de [!DNL Cluster.cfg] dossier, zou u slechts de Normalize parameter van de Server moeten wijzigen als u een dataset vormt die op een de servercluster van de gegevenswerkbank moet worden verwerkt. Voor instructies om de Normalize parameter van de Server te wijzigen, zie [Een gecentraliseerde normalisatieserver maken voor een cluster](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

* **[!DNL Insight Transform.cfg]en [!DNL Insight Transform Mode.cfg]:** Als u transformatiefunctionaliteit gebruikt, hebt u twee extra configuratiebestanden, gegevenswerkbank [!DNL Transform.cfg] en gegevenswerkbank [!DNL TransformMode.cfg], in de directory Gegevensset voor de [!DNL Transform] profiel. Voor informatie over deze bestanden en hun parameters raadpleegt u [Transformatiefunctionaliteit](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/transform/t-config-tfm.html).

* De **PAServer.cfg** bestand. Als u de Predictive Analytics groeperende banen aan de Servers van het Inzicht wilt voorleggen, dan zult u moeten vormen [!DNL PAServer.cfg] bestand voor de verwerking van serverclusteringverzendingen.
Het aangepaste profiel moet de eigenschap [!DNL PAServer.cfg] uit het profiel Predictive Analytics ( [!DNL Server\Profiles\Predictive Analytics\Dataset]).

   >[!IMPORTANT]
   >
   >Een *Master server* in dit bestand en sla de [!DNL PAServer.cfg] naar de implementatielocatie.
   >
   >
   ```
   >PAServer = PAServerConfig: 
   >   Master Server = serverInfo: 
   >       Address = string: 
   >       Port = int: 80
   >       Use SSL = bool: false
   >```

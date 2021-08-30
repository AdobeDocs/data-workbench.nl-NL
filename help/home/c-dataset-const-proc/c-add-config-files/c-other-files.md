---
description: De map Dataset bevat aanvullende bestanden die vereist zijn voor de werking van de software of die aanvullende functionaliteit bieden voor de Adobe-implementatie.
title: Overige bestanden
uuid: 87d83fa5-df25-4da1-8b11-16639902d8d7
exl-id: 0a1fb37c-00ac-46d4-9d0a-904ebd3ccfba
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Overige bestanden{#other-files}

De map Dataset bevat aanvullende bestanden die vereist zijn voor de werking van de software of die aanvullende functionaliteit bieden voor de Adobe-implementatie.

* **[!DNL Client.cfg:]** Het  [!DNL Client.cfg] bestand in de map Dataset voor het  [!DNL Base] profiel is vereist voor de werking van de software. Verwijder of wijzig geen parameters in het [!DNL Client.cfg] dossier.

* **[!DNL Cluster.cfg:]** Het  [!DNL Cluster.cfg] bestand in de map Dataset voor het  [!DNL Base] profiel is vereist voor de werking van de software. In het [!DNL Cluster.cfg] dossier, zou u slechts de Normalize parameter van de Server moeten wijzigen als u een dataset vormt die op een de servercluster van de gegevenswerkbank moet worden verwerkt. Voor instructies om de Normalize parameter van de Server te wijzigen, zie [Creërend een Gecentraliseerde Server van de Normalisatie voor een Cluster](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

* **[!DNL Insight Transform.cfg]en  [!DNL Insight Transform Mode.cfg]:** Als u de transformatiefunctionaliteit gebruikt, hebt u twee extra configuratiedossiers, werkbank van gegevens  [!DNL Transform.cfg] en gegevenswerkbank  [!DNL TransformMode.cfg], in de folder van de Dataset voor het  [!DNL Transform] profiel. Zie [Functionaliteit transformeren](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/transform/t-config-tfm.html) voor informatie over deze bestanden en de bijbehorende parameters.

* Het bestand **PAServer.cfg**. Als u de Predictive Analytics groeperende banen aan de Servers van het Inzicht wilt voorleggen, dan zult u het [!DNL PAServer.cfg] dossier voor de behandeling van server-zij groeperen indieningen moeten vormen.
Het aangepaste profiel moet de [!DNL PAServer.cfg] overerven van het profiel voor voorspellende analyse ( [!DNL Server\Profiles\Predictive Analytics\Dataset]).

   >[!IMPORTANT]
   >
   >Stel een *Master server* in dit bestand in en sla [!DNL PAServer.cfg] op de implementatiesite op.
   >
   >
   ```
   >PAServer = PAServerConfig: 
   >   Master Server = serverInfo: 
   >       Address = string: 
   >       Port = int: 80
   >       Use SSL = bool: false
   >```

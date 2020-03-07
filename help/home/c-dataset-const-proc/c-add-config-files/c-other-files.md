---
description: De folder van de Dataset omvat extra dossiers die of voor de verrichting van de software worden vereist of extra functionaliteit voor uw implementatie van Adobe verstrekken.
solution: Analytics
title: Andere bestanden
topic: Data workbench
uuid: 87d83fa5-df25-4da1-8b11-16639902d8d7
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Andere bestanden{#other-files}

De folder van de Dataset omvat extra dossiers die of voor de verrichting van de software worden vereist of extra functionaliteit voor uw implementatie van Adobe verstrekken.

* **[!DNL Client.cfg:]** Het [!DNL Client.cfg] dossier binnen de folder van de Dataset voor het [!DNL Base] profiel wordt vereist voor verrichting van de software. Schrap of wijzig geen van de parameters in het [!DNL Client.cfg] dossier.

* **[!DNL Cluster.cfg:]** Het [!DNL Cluster.cfg] dossier binnen de folder van de Dataset voor het [!DNL Base] profiel wordt vereist voor verrichting van de software. In het [!DNL Cluster.cfg] dossier, zou u slechts de Normalize parameter van de Server moeten wijzigen als u een dataset vormt die op een de servercluster van de gegevenswerkbank moet worden verwerkt. Voor instructies om de Normalize parameter van de Server te wijzigen, zie het [Creëren van een Centrale Server van de Normalisatie voor een Cluster](../../../home/c-dataset-const-proc/c-log-proc-config-file/c-ins-svr-file-svr-unit.md).

* **[!DNL Insight Transform.cfg]en[!DNL Insight Transform Mode.cfg]:**Als u transformatiefunctionaliteit gebruikt, hebt u twee extra configuratiedossiers, gegevenswerkbank[!DNL Transform.cfg]en gegevenswerkbank[!DNL TransformMode.cfg], in de folder van de Dataset voor het[!DNL Transform]profiel. Voor informatie over deze dossiers en hun parameters, zie de Functionaliteit[van de](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/transform/t-config-tfm.html)Transformatie.

* Het **PAServer.cfg** - dossier. Als u Predictive Analytics wilt voorleggen die banen groeperen zich aan de Servers van het Inzicht, dan zult u het [!DNL PAServer.cfg] dossier voor de behandeling van server-zij groeperende indieningen moeten vormen.
Het douaneprofiel zou [!DNL PAServer.cfg] van het Predictive Analytics profiel ( [!DNL Server\Profiles\Predictive Analytics\Dataset]) moeten erven.

   >[!IMPORTANT]
   >
   >Plaats een *HoofdServer* in dit dossier en sla [!DNL PAServer.cfg] aan de implementatieplaats op.   >
   >
   >
   ```>
   >PAServer = PAServerConfig: 
   >   Master Server = serverInfo: 
   >       Address = string: 
   >       Port = int: 80
   >       Use SSL = bool: false
   >```  >
   >




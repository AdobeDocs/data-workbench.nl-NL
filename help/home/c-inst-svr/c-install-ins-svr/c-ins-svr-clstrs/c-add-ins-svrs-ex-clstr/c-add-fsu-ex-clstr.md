---
description: U kunt een Server FSU van het Inzicht aan een bestaande cluster willen toevoegen als u brongegevens op een extra dossierserver wilt opslaan of als u file voor uw master Server van het Inzicht wilt opstelling.
title: Een Insight Server FSU toevoegen aan een bestaande cluster
uuid: 57d6ef52-eef9-4425-943a-331e4c9c4207
exl-id: b3b08016-42ad-4972-a8b7-ee714493fa52
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# Een Insight Server FSU toevoegen aan een bestaande cluster{#adding-an-insight-server-fsu-to-an-existing-cluster}

{{eol}}

U kunt een Server FSU van het Inzicht aan een bestaande cluster willen toevoegen als u brongegevens op een extra dossierserver wilt opslaan of als u file voor uw master Server van het Inzicht wilt opstelling.

Om een [!DNL Insight Server] FSU aan een bestaande cluster, moet u de volgende procedures uitvoeren:

1. [De configuratiebestanden op de Master server bijwerken](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-b5f21f2edb35493da4475de2cdeefca1)
1. [De FSU van de nieuwe Insight Server installeren](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-dddad299dd8642aa91cbe19a395ef3f4)
1. [Het vormen van de Nieuwe Server FSU van het Inzicht](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-c39334c5bd754d5b98d41ad094333108)

## De configuratiebestanden op de Master server bijwerken {#section-b5f21f2edb35493da4475de2cdeefca1}

In [!DNL Insight], opent u de [!DNL Server Files Manager] voor uw master [!DNL Insight Server] (gewoonlijk een [!DNL Insight Server] FSU) en voer de volgende handelingen uit voor elke FSU die u aan de cluster wilt toevoegen:

1. Het adresbestand op het master bestand bewerken [!DNL Insight Server] de naam en het adres van de nieuwe FSU op te nemen, zoals beschreven in [De servers van het Inzicht van de Verwerking aan het Dossier van het Adres toevoegen](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d). Voeg de naam en het adres van nieuwe FSU aan de groep toe waarin de huidige cluster [!DNL Insight Servers] worden weergegeven.

1. Bewerk het toegangsbeheerbestand op het master [!DNL Insight Server] om het IP adres van de nieuwe FSU op te nemen zoals die in [Het toegangscontrolebestand voor een cluster bijwerken](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b).

## De FSU van de nieuwe Insight Server installeren {#section-dddad299dd8642aa91cbe19a395ef3f4}

1. Maak op uw huidige FSU een zip-bestand van de [!DNL Insight Server] en kopieer het bestand naar de nieuwe FSU.
1. Pak het bestand uit op de locatie waar u het bestand wilt plaatsen [!DNL Insight Server] software.
1. Download en installeer het digitale certificaat voor de nieuwe FSU zoals beschreven in [Digitale certificaten downloaden en installeren](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).
1. Stel de parameters voor het geheugengebruik van Windows in op de nieuwe FSU.
1. De naam van de [!DNL .address] bestand om de naam van de FSU weer te geven, zoals beschreven in [De netwerklocatie van de server definiëren](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649).

1. Als de schijfstructuur op het nieuwe FSU anders is dan die op het primaire FSU, moet u de [!DNL Disk Files.cfg] bestand.

   1. Open de [!DNL Disk Files.cfg] op de nieuwe FSU.
   1. De instellingen aanpassen aan de stations van het primaire FSU, zoals beschreven in [Gegevensruimte controleren](../../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-dtst-data-spc.md#task-6223fa2c718845678824a0a96df96a03).
   1. Sla het bestand lokaal op en op de server op.

1. Registreren [!DNL Insight Server] als Windows-service op de nieuwe FSU-computer, zoals beschreven in [Insight Server registreren als Windows-service](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).

1. Herhaal stap 1 tot en met 6 voor elke extra FSU die u aan de cluster toevoegt.

## Het vormen van de Nieuwe Server FSU van het Inzicht {#section-c39334c5bd754d5b98d41ad094333108}

De volgende procedures verstrekken instructies voor specifieke configuratietaken. Volg de instructies die geschikt zijn voor uw implementatie van de nieuwe FSU.

**De FSU configureren voor opslag van brongegevens**

Als nieuwe FSU extra brongegevens voor de dataset opslaat die op de cluster lopen, moet u het configuratieproces van de dossierserver voltooien zoals die in het Vormen van wordt beschreven [!DNL Insight Server] De eenheid van de Server van het dossier in het hoofdstuk van het Dossier van de Configuratie van de Logverwerking van het Dossier van het Dossier *Configuratie-handleiding voor gegevensset*.

**De back-up voor de master [!DNL Insight Server] FSU**

Als u van de nieuwe FSU de back-up voor de master [!DNL Insight Server] (die fungeert als een FSU voor de cluster), moet u het synchronisatiebestand op de nieuwe (back-up)FSU aanpassen, zodat deze zich synchroniseert met de master FSU.

1. Op de back-up [!DNL Insight Server] FSU, gebruik de [!DNL Server Files Manager] om de [!DNL Synchronize.cfg] in het [!DNL Components for Processing Servers] aan de [!DNL Components] map.

1. Open de [!DNL Synchronize.cfg] bestand (in het [!DNL Components] map) in [!DNL Insight].

1. Zoek de SynchronizeDir die de plaats van de folder van Componenten specificeert. Er kunnen verscheidene synchrone folders onder Folders zijn, zodat kunt u de inhoud voor vele van hen (door het serveraantal te klikken) moeten bekijken om de gewenste server te vinden).
1. Bewerk het SynchronizeDir-item en voeg een tweede SynchronizeDir-item toe, zoals in het onderstaande voorbeeld wordt getoond.

   ![](assets/cfg_cluster_SynchronizeDirEditComponents.png)

1. Sla het gewijzigde bestand op onder een andere naam, zoals [!DNL FSU_Synchronize.cfg] zodat u het niet verwart met de [!DNL Synchronize.cfg] bestanden op de DPU&#39;s in de cluster.

1. Gebruik de [!DNL Server Files Manager] om de lokale kopie van het bestand met de nieuwe naam op te slaan op de server. De back-up-FSU downloadt de bestanden in de opgegeven directory&#39;s van de master [!DNL Insight Server] FSU en haalt dynamisch bijgewerkte kopieën van deze bestanden op uit de master [!DNL Insight Server] FSU wanneer ze veranderen.

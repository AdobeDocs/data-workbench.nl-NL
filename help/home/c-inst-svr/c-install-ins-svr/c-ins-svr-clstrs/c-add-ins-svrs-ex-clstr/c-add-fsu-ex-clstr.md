---
description: U kunt een Server FSU van het Inzicht aan een bestaande cluster willen toevoegen als u brongegevens op een extra dossierserver wilt opslaan of als u file voor uw master Server van het Inzicht wilt opstelling.
title: Een Insight Server FSU toevoegen aan een bestaande cluster
uuid: 57d6ef52-eef9-4425-943a-331e4c9c4207
exl-id: b3b08016-42ad-4972-a8b7-ee714493fa52
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# Een Insight Server FSU toevoegen aan een bestaande cluster{#adding-an-insight-server-fsu-to-an-existing-cluster}

U kunt een Server FSU van het Inzicht aan een bestaande cluster willen toevoegen als u brongegevens op een extra dossierserver wilt opslaan of als u file voor uw master Server van het Inzicht wilt opstelling.

Als u een [!DNL Insight Server] FSU aan een bestaande cluster wilt toevoegen, moet u de volgende procedures uitvoeren:

1. [De configuratiebestanden op de Master server bijwerken](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-b5f21f2edb35493da4475de2cdeefca1)
1. [De FSU van de nieuwe Insight Server installeren](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-dddad299dd8642aa91cbe19a395ef3f4)
1. [Het vormen van de Nieuwe Server FSU van het Inzicht](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-c39334c5bd754d5b98d41ad094333108)

## De configuratiebestanden op de Master server {#section-b5f21f2edb35493da4475de2cdeefca1} bijwerken

Open [!DNL Insight] voor uw master [!DNL Insight Server] (gewoonlijk een [!DNL Insight Server] FSU) de [!DNL Server Files Manager] en voer de volgende handelingen uit voor elk FSU dat u aan het cluster wilt toevoegen:

1. Bewerk het adresbestand op de master [!DNL Insight Server] om de naam en het adres van de nieuwe FSU op te nemen, zoals beschreven in [De servers van het Inzicht van de Verwerking toevoegen aan het Dossier van het Adres](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d). Voeg de naam en het adres van de nieuwe FSU toe aan de groep waarin de huidige [!DNL Insight Servers] van uw cluster worden vermeld.

1. Bewerk het toegangsbeheerbestand op het master [!DNL Insight Server] om het IP-adres van de nieuwe FSU op te nemen, zoals beschreven in [Het toegangsbeheerbestand voor een cluster bijwerken.](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b)

## De FSU {#section-dddad299dd8642aa91cbe19a395ef3f4} van de nieuwe Insight-server installeren

1. Maak op uw huidige FSU een ZIP-bestand van de installatiemap [!DNL Insight Server] en kopieer het bestand naar de nieuwe FSU.
1. Pak het bestand uit op de locatie waar u de [!DNL Insight Server]-software wilt plaatsen.
1. Download en installeer het digitale certificaat voor de nieuwe FSU zoals beschreven in [De digitale certificaten downloaden en installeren](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).
1. Stel de parameters voor het geheugengebruik van Windows in op de nieuwe FSU.
1. Wijzig de naam van het [!DNL .address]-bestand om de naam van de FSU weer te geven, zoals beschreven in [De netwerklocatie van de server definiëren](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649).

1. Als de schijfstructuur op het nieuwe FSU anders is dan op het primaire FSU, moet u het [!DNL Disk Files.cfg]-bestand bewerken.

   1. Open het [!DNL Disk Files.cfg] dossier op nieuwe FSU.
   1. Werk de instellingen bij zodat deze overeenkomen met de stations van het primaire FSU, zoals beschreven in [Dataset Data Space](../../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-dtst-data-spc.md#task-6223fa2c718845678824a0a96df96a03) controleren.
   1. Sla het bestand lokaal op en op de server op.

1. Registreer [!DNL Insight Server] als dienst van Vensters op de nieuwe machine van FSU zoals die in [wordt beschreven Registrerend de Server van het Inzicht als Dienst van Vensters ](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).

1. Herhaal stap 1 tot en met 6 voor elke extra FSU die u aan de cluster toevoegt.

## De FSU {#section-c39334c5bd754d5b98d41ad094333108} van de nieuwe Insight-server configureren

De volgende procedures verstrekken instructies voor specifieke configuratietaken. Volg de instructies die geschikt zijn voor uw implementatie van de nieuwe FSU.

**De FSU configureren voor opslag van brongegevens**

Als de nieuwe FSU extra brongegevens opslaat voor de dataset die op de cluster loopt, moet u het configuratieproces van de dossierserver voltooien zoals die in het Vormen van een [!DNL Insight Server] Eenheid van de Server van het Dossier in het hoofdstuk van het Dossier van de Configuratie van de Logverwerking van *Gids van de Configuratie van de Dataset* wordt beschreven.

**De back-up voor het master  [!DNL Insight Server] FSU maken naar nieuwe FSU**

Als u de nieuwe FSU de back-up wilt maken voor de master [!DNL Insight Server] (die fungeert als een FSU voor de cluster), moet u het synchronisatiebestand op de nieuwe (back-up) FSU aanpassen zodat deze wordt gesynchroniseerd met de master FSU.

1. Voor de steun [!DNL Insight Server] FSU, gebruik [!DNL Server Files Manager] om het [!DNL Synchronize.cfg] dossier in [!DNL Components for Processing Servers] omslag aan &lt;a4 te kopiëren/> omslag.[!DNL Components]

1. Open het [!DNL Synchronize.cfg]-bestand (in de map [!DNL Components]) in [!DNL Insight].

1. Zoek de SynchronizeDir die de plaats van de folder van Componenten specificeert. Er kunnen verscheidene synchrone folders onder Folders zijn, zodat kunt u de inhoud voor vele van hen (door het serveraantal te klikken) moeten bekijken om de gewenste server te vinden).
1. Bewerk het SynchronizeDir-item en voeg een tweede SynchronizeDir-item toe, zoals in het onderstaande voorbeeld wordt getoond.

   ![](assets/cfg_cluster_SynchronizeDirEditComponents.png)

1. Sla het gewijzigde bestand op onder een nieuwe naam, zoals [!DNL FSU_Synchronize.cfg], zodat u dit bestand niet verwart met de [!DNL Synchronize.cfg]-bestanden op de DPU&#39;s in de cluster.

1. Gebruik [!DNL Server Files Manager] om het lokale exemplaar van het anders genoemde dossier aan de server op te slaan. De back-up van FSU downloadt de bestanden in de opgegeven directory&#39;s van de master [!DNL Insight Server] FSU en haalt dynamisch bijgewerkte kopieën van deze bestanden op van de master [!DNL Insight Server] FSU wanneer deze worden gewijzigd.

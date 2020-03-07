---
description: U kunt een Server FSU van het Inzicht aan een bestaande cluster willen toevoegen als u brongegevens op een extra dossierserver wilt opslaan of als u aan opstelling een file voor uw hoofdserver van het Inzicht wilt.
solution: Insight
title: Het toevoegen van een FSU van de Server van het Inzicht aan een Bestaande Cluster
uuid: 57d6ef52-eef9-4425-943a-331e4c9c4207
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het toevoegen van een FSU van de Server van het Inzicht aan een Bestaande Cluster{#adding-an-insight-server-fsu-to-an-existing-cluster}

U kunt een Server FSU van het Inzicht aan een bestaande cluster willen toevoegen als u brongegevens op een extra dossierserver wilt opslaan of als u aan opstelling een file voor uw hoofdserver van het Inzicht wilt.

Om een [!DNL Insight Server] FSU aan een bestaande cluster toe te voegen, moet u de volgende procedures uitvoeren:

1. [Het bijwerken van de Dossiers van de Configuratie op de HoofdServer](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-b5f21f2edb35493da4475de2cdeefca1)
1. [Het installeren van de Nieuwe Server FSU van het Inzicht](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-dddad299dd8642aa91cbe19a395ef3f4)
1. [Het vormen van de Nieuwe Server FSU van het Inzicht](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-add-ins-svrs-ex-clstr/c-add-fsu-ex-clstr.md#section-c39334c5bd754d5b98d41ad094333108)

## Het bijwerken van de Dossiers van de Configuratie op de HoofdServer {#section-b5f21f2edb35493da4475de2cdeefca1}

In [!DNL Insight], open [!DNL Server Files Manager] voor uw meester [!DNL Insight Server] (gewoonlijk een [!DNL Insight Server] FSU) en doe het volgende voor elke FSU die u aan de cluster wilt toevoegen:

1. Geef het adresdossier op de meester uit [!DNL Insight Server] om de naam en het adres van nieuwe FSU te omvatten zoals die in het [Toevoegen van de Servers van het Inzicht van de Verwerking aan het Dossier](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d)van het Adres wordt beschreven. Voeg de naam en het adres van nieuwe FSU aan de groep toe waarin de stroom van uw cluster vermeld [!DNL Insight Servers] zijn.

1. Geef het toegangsbeheerdossier op de meester uit [!DNL Insight Server] om het IP adres van nieuwe FSU te omvatten zoals die in het [Bijwerken van het Dossier van het Toegangsbeheer voor een Cluster](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b)wordt beschreven.

## Het installeren van de Nieuwe Server FSU van het Inzicht {#section-dddad299dd8642aa91cbe19a395ef3f4}

1. Maak op uw huidige FSU een zip-bestand van de [!DNL Insight Server] installatiefolder en kopieer het bestand naar de nieuwe FSU.
1. Unzip het dossier aan de plaats waar u wenst om de [!DNL Insight Server] software te plaatsen.
1. Download en installeer het digitale certificaat voor de nieuwe FSU, zoals beschreven in het [Downloaden en installeren van de Digitale Certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).
1. Plaats de parameters van het het geheugengebruik van Vensters op nieuwe FSU.
1. Verander de naam van het [!DNL .address] dossier om op de naam van FSU te wijzen zoals die in het [Bepalen van de Plaats](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649)van het Netwerk van de Server wordt beschreven.

1. Als de schijfstructuur op de nieuwe FSU anders is dan die op de primaire FSU, moet u het [!DNL Disk Files.cfg] bestand bewerken.

   1. Open het [!DNL Disk Files.cfg] bestand op het nieuwe FSU.
   1. Werk de instellingen bij die overeenkomen met de stations van het primaire FSU, zoals beschreven in de gegevensruimte [voor gegevensverzameling](../../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-dtst-data-spc.md#task-6223fa2c718845678824a0a96df96a03)bewaken.
   1. Sla het bestand lokaal en op de server op.

1. Register [!DNL Insight Server] als dienst van Vensters op de nieuwe machine van FSU zoals die in de Server van het [Registreren van het Inzicht als Dienst](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)van Vensters wordt beschreven.

1. Herhaal stappen 1 door 6 voor elke extra FSU die u aan de cluster toevoegt.

## Het vormen van de Nieuwe Server FSU van het Inzicht {#section-c39334c5bd754d5b98d41ad094333108}

De volgende procedures verstrekken instructies voor specifieke configuratietaken. Volg de instructies op die geschikt zijn voor uw implementatie van de nieuwe FSU.

**Om FSU voor brongegevensopslag te configureren**

Als nieuwe FSU extra brongegevens voor de dataset opslaat die op de cluster loopt, moet u het configuratieproces van de dossierserver voltooien zoals die in het Vormen van een Eenheid van de Server van het [!DNL Insight Server] Dossier in het hoofdstuk van het Dossier van de Configuratie van de Verwerking van het Logboek van de Gids *van de Configuratie van de* Dataset wordt beschreven.

**Om aan nieuwe FSU de steun voor de meester[!DNL Insight Server]FSU te maken**

Als u wenst om van nieuwe FSU de steun voor de meester te maken [!DNL Insight Server] (die als FSU voor de cluster dient), moet u het synchronisatiedossier op nieuw (steun) FSU wijzigen zodat het met masterFSU synchroniseert.

1. Voor de steun [!DNL Insight Server] FSU, gebruik het [!DNL Server Files Manager] om het [!DNL Synchronize.cfg] dossier in de [!DNL Components for Processing Servers] omslag aan de [!DNL Components] omslag te kopiëren.

1. Open het [!DNL Synchronize.cfg] - dossier (in de [!DNL Components] omslag) in [!DNL Insight].

1. Vind SynchronizeDir die de plaats van de folder van Componenten specificeert. Er kunnen verscheidene gesynchroniseerde folders zijn die onder Folders worden vermeld, zodat kunt u de inhoud voor veel van hen (door het serveraantal te klikken) moeten bekijken om de gewenste server te vinden).
1. Geef de ingang SynchronizeDir uit en voeg een tweede ingang SynchronizeDir zoals aangetoond in het hieronder voorbeeld toe.

   ![](assets/cfg_cluster_SynchronizeDirEditComponents.png)

1. Sparen het gewijzigde dossier met een nieuwe naam zoals [!DNL FSU_Synchronize.cfg] zodat u niet het met de [!DNL Synchronize.cfg] dossiers op DPUs in de cluster verwart.

1. Gebruik [!DNL Server Files Manager] om het lokale exemplaar van het anders genoemde dossier aan de server op te slaan. De back-upFSU downloadt de bestanden in de geïdentificeerde directory&#39;s van de master [!DNL Insight Server] FSU en haalt dynamisch bijgewerkte kopieën van deze bestanden op van de master- [!DNL Insight Server] FSU wanneer deze worden gewijzigd.


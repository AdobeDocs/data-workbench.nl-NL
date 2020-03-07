---
description: De administratieve taken voor repeaterfunctionaliteit zijn zeer gelijkaardig aan die voor de Server van het Inzicht.
solution: Insight
title: Repeater beheren
uuid: 4fbfce3a-2610-4dcd-a585-cb7ee07b90db
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Repeater beheren{#administering-repeater}

De administratieve taken voor repeaterfunctionaliteit zijn zeer gelijkaardig aan die voor de Server van het Inzicht.

De volgende administratieve taken zijn van toepassing: de uitzonderingen of de veranderingen die u moet aanbrengen zodat [!DNL Insight Server] DPU met de repeaterserver kan worden gebruikt worden genoteerd na elke stap.

* [Het digitale certificaat opnieuw valideren](../../../home/c-inst-svr/c-admin-inst-svr/c-reval-dgtl-cert.md#concept-f0020a6f0d6f477099b7a8f0b6e2944c)
* [Bevestigend dat de Dienst in de lijst van de diensten in het de controlepaneel van de Diensten loopt](../../../home/c-inst-svr/c-admin-inst-svr/c-cfrm-svc-rng.md#concept-15b046e92d254bbd95dec829abc76677) , zoek &quot;Repeater.&quot;

* [Toegangsbeheer configureren](../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d)
* [De Ruimte](../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/c-mntr-disk-spc.md#concept-a83447e44f4e47aba282328be395a0d4) van de Schijf van de controle De gegevenstypes die op de repeaterserver van toepassing zijn zijn zijn gebeurtenis, werkend systeem, en systeemgegevens. Als u de repeaterserver voor reserveopslag gebruikt en het noodzakelijk wordt om meer ruimte van de gegevensopslag beschikbaar te maken op de machine, kunt u allen behalve de het logboekdossiers van de meest huidige dag naar een andere machine of gegevensopslagmiddel (zip aandrijving, band, etc.) verplaatsen. Het bewegen van de gegevens vereist u niet om de repeaterdienst tegen te houden.

   >[!NOTE]
   >
   >U zou de integriteit van de reserveexemplaren van uw [!DNL .vsl] dossiers moeten verifiëren alvorens om het even welk van hen van Repeater te schrappen.

* [Administratieve waarschuwingen configureren](../../../home/c-inst-svr/c-admin-inst-svr/t-config-adm-alrts.md#task-0858f588da4941aa9d4952f6592681aa)
* [Toezicht op administratieve gebeurtenissen](../../../home/c-inst-svr/c-admin-inst-svr/t-mntr-adm-evts.md#task-4c78325b3e6e4dde8fa94c1896e19e34)
* [Controle van controleverslagen](../../../home/c-inst-svr/c-admin-inst-svr/t-mntr-adt-lgs.md#task-5dd9830424fe440ea1369215a1aca231)
* [Communicatie configureren](../../../home/c-inst-svr/c-admin-inst-svr/t-config-com.md#task-471305ecf7a644789a288f93c42514ec)
* [Het opnieuw opstarten van de Service](../../../home/c-inst-svr/c-admin-inst-svr/t-rest-svc.md#task-97f97f1019bc440080ab2fddfdc04c74) [!DNL Repeater] -functionaliteit is ontworpen om continu te worden uitgevoerd. Als u het systeem opnieuw opstart, wordt de repeater automatisch opnieuw opgestart. Als u repeater moet beginnen en ophouden manueel, kunt u dit doen gebruikend het de controlepaneel van de Diensten in Vensters.


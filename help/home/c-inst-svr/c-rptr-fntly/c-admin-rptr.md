---
description: De administratieve taken voor herhalingsfunctionaliteit zijn zeer gelijkaardig aan die voor de Server van het Inzicht.
title: Beheerder
uuid: 4fbfce3a-2610-4dcd-a585-cb7ee07b90db
exl-id: 5c7a4f95-be4b-4c2c-8dea-19037ba0b5cc
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Beheerder{#administering-repeater}

{{eol}}

De administratieve taken voor herhalingsfunctionaliteit zijn zeer gelijkaardig aan die voor de Server van het Inzicht.

De volgende administratieve taken zijn van toepassing: de uitzonderingen of de veranderingen die u moet aanbrengen zodat [!DNL Insight Server] DPU kan met de repeaterserver worden gebruikt wordt genoteerd na elke stap.

* [Het digitale certificaat opnieuw valideren](../../../home/c-inst-svr/c-admin-inst-svr/c-reval-dgtl-cert.md#concept-f0020a6f0d6f477099b7a8f0b6e2944c)
* [Bevestigen dat de service wordt uitgevoerd](../../../home/c-inst-svr/c-admin-inst-svr/c-cfrm-svc-rng.md#concept-15b046e92d254bbd95dec829abc76677) Zoek in de lijst met services in het configuratiescherm Services naar &quot;Repeater&quot;.

* [Toegangsbeheer configureren](../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d)
* [Schijfruimte controleren](../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/c-mntr-disk-spc.md#concept-a83447e44f4e47aba282328be395a0d4) De gegevenstypen die op de herhalingsserver van toepassing zijn, zijn gebeurtenis, werkend systeem, en systeemgegevens. Als u de herhalingsserver gebruikt voor back-upopslag en het nodig wordt meer opslagruimte voor gegevens beschikbaar te maken op de computer, kunt u alle logbestanden van de huidige dag, behalve de meest recente, verplaatsen naar een andere computer of een ander opslagmedium (ZIP-station, tape enzovoort). Als u de gegevens verplaatst, hoeft u de herhalingsservice niet te stoppen.

   >[!NOTE]
   >
   >Controleer de integriteit van de back-upexemplaren van uw [!DNL .vsl] bestanden voordat u een van deze bestanden uit Repeater verwijdert.

* [Beheerswaarschuwingen configureren](../../../home/c-inst-svr/c-admin-inst-svr/t-config-adm-alrts.md#task-0858f588da4941aa9d4952f6592681aa)
* [Bewaking van administratieve gebeurtenissen](../../../home/c-inst-svr/c-admin-inst-svr/t-mntr-adm-evts.md#task-4c78325b3e6e4dde8fa94c1896e19e34)
* [Controleregroepen](../../../home/c-inst-svr/c-admin-inst-svr/t-mntr-adt-lgs.md#task-5dd9830424fe440ea1369215a1aca231)
* [Communicatie configureren](../../../home/c-inst-svr/c-admin-inst-svr/t-config-com.md#task-471305ecf7a644789a288f93c42514ec)
* [De service opnieuw opstarten](../../../home/c-inst-svr/c-admin-inst-svr/t-rest-svc.md#task-97f97f1019bc440080ab2fddfdc04c74)  [!DNL Repeater] is ontworpen om continu te worden uitgevoerd. Als u de computer opnieuw opstart, wordt deze automatisch opnieuw opgestart. Als u repeater manueel moet beginnen en tegenhouden, kunt u dit doen gebruikend het de controlepaneel van de Diensten in Vensters.

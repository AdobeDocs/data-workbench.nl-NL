---
description: De functionaliteit van de repeater laat een Server FSU van het Inzicht toe om Sensor-verworven gebeurtenisgegevens van één of meerdere bronnen te ontvangen en de gegevens aan één of meerdere Server FSUs van het Inzicht te herhalen die de Dienst van de Replicatie van de Server van het Inzicht in werking stellen.
title: Repeater-functionaliteit configureren
uuid: 45dca069-a91f-4fd4-bd47-c8c2e6aab834
exl-id: 61b70772-07fb-4963-b09f-6b2cf97b01a1
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---

# De vormende Functionaliteit van de Repeater{#configuring-repeater-functionality}

De functionaliteit van de repeater laat een Server FSU van het Inzicht toe om Sensor-verworven gebeurtenisgegevens van één of meerdere bronnen te ontvangen en de gegevens aan één of meerdere Server FSUs van het Inzicht te herhalen die de Dienst van de Replicatie van de Server van het Inzicht in werking stellen.

Zie [Insight Server Replication Service](../../../../home/c-inst-svr/c-ins-svr-rep-svc/c-ins-svr-rep-svc.md#concept-926e654e80d943a0b6ac44a82a510d92). Met deze functie wordt gegevensreplicatie naar redundante voorzieningen mogelijk voor noodherstel. De doelservers handelen als netwerkcliënten, die met bron FSU verbinden om exemplaren van de gebeurtenisgegevens voor opneming in veelvoudige datasets te verzoeken.

U kunt herhalingsfunctionaliteit in netwerkinfrastructuur met veelvoudige lagen van het vuurwerk gebruiken om enig-haven aan enig-haven mededelingen tussen componenten te bereiken die door firewalls worden gescheiden.

Raadpleeg het document *Minimale systeemvereisten* voor informatie over de systeemvereisten voor het installeren, configureren en gebruiken van [!DNL Repeater].

Als u [!DNL Repeater] wilt installeren, moet u de stappen uitvoeren die voor de volgende twee procedures worden vermeld:

* [Het vormen van een Server FSU van het Inzicht voor Repeater](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-cfg-fsu-rptr.md#task-1ad7fa5777b845f4bd398f97226e56b2)
* [Toegangsbeheer voor doelapparaten configureren](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-cfg-acc-ctrll-tgt-mach.md#task-0e49953728444839bc0a26234501a4c5)

Als netwerkfirewalls toegang tot uw [!DNL Repeater] van [!DNL Insight] verlenen, kunt u een verbinding tot stand brengen zoals die in [het Creëren van een Verbinding tussen Inzicht en Repeater](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118) wordt beschreven.

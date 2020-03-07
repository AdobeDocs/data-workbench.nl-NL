---
description: De functionaliteit van de repeater laat een FSU van de Server van het Inzicht toe om Sensor-verworven gebeurtenisgegevens van één of meerdere bronnen te ontvangen en de gegevens te herhalen aan één of meerdere Server FSUs van het Inzicht die de Dienst van de Replicatie van de Server van het Inzicht in werking stellen.
solution: Insight
title: Het vormen Functionaliteit van de Repeater
uuid: 45dca069-a91f-4fd4-bd47-c8c2e6aab834
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen Functionaliteit van de Repeater{#configuring-repeater-functionality}

De functionaliteit van de repeater laat een FSU van de Server van het Inzicht toe om Sensor-verworven gebeurtenisgegevens van één of meerdere bronnen te ontvangen en de gegevens te herhalen aan één of meerdere Server FSUs van het Inzicht die de Dienst van de Replicatie van de Server van het Inzicht in werking stellen.

Zie de Dienst van de Replicatie van de Server van het [Inzicht](../../../../home/c-inst-svr/c-ins-svr-rep-svc/c-ins-svr-rep-svc.md#concept-926e654e80d943a0b6ac44a82a510d92). Deze eigenschap laat gegevensreplicatie aan overtollige faciliteiten voor de doeleinden van de rampenterugwinning toe. De doelservers fungeren als netwerkclients, die verbinding maken met de bron-FSU om kopieën van de gebeurtenisgegevens aan te vragen voor opname in meerdere datasets.

U kunt repeaterfunctionaliteit in netwerkinfrastructuur met veelvoudige lagen van het firewalling gebruiken om enig-haven aan enig-havenmededelingen tussen componenten te bereiken die door firewalls worden gescheiden.

Raadpleeg het document [!DNL Repeater]Systeemvereisten *voor informatie over de systeemvereisten voor installatie, configuratie en gebruik* in het documentMinimale systeemvereisten.

Om te installeren [!DNL Repeater], moet u de stappen uitvoeren die voor de volgende twee procedures worden vermeld:

* [Het vormen van een Server FSU van het Inzicht voor Repeater](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-cfg-fsu-rptr.md#task-1ad7fa5777b845f4bd398f97226e56b2)
* [Het vormen Toegangsbeheer voor de Machines van het Doel](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-cfg-acc-ctrll-tgt-mach.md#task-0e49953728444839bc0a26234501a4c5)

Als de netwerkfirewalls toegang tot uw verlenen [!DNL Repeater] van [!DNL Insight], kunt u een verbinding tot stand brengen zoals die in het [Creëren van een Verbinding tussen Inzicht en Repeater](../../../../home/c-inst-svr/c-rptr-fntly/c-cnfg-rptr-fntly/t-crt-conn-ins-rptr.md#task-785bfe5f0e31484683e4345038add118)wordt beschreven.

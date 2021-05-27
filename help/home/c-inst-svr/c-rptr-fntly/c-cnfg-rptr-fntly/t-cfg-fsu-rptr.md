---
description: Instructies om een Server FSU van het Inzicht voor gebruik met Repeater te installeren en te vormen.
title: Het vormen van een Server FSU van het Inzicht voor Repeater
uuid: c2bae862-37d3-4841-b31b-59593c1e4316
exl-id: dacbabd5-f6f5-4201-8709-146075eae679
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Een Insight Server FSU configureren voor Repeater{#configuring-an-insight-server-fsu-for-repeater}

Instructies om een Server FSU van het Inzicht voor gebruik met Repeater te installeren en te vormen.

Voltooi de volgende taken in volgorde. Eventuele uitzonderingen of wijzigingen die u moet doorvoeren zodat de FSU [!DNL Insight Server] als een herhalingsserver kan worden gebruikt, worden na elke stap vermeld.

1. Installeer de [!DNL Insight Server] programmabestanden zoals beschreven in [Insight Server installeren](../../../../home/c-inst-svr/c-install-ins-svr/c-install-ins-svr.md#concept-1c796b4ca427474f99ec6ba34d8254cd).

   Omdat de computer waarop u deze bestanden installeert wordt gebruikt om Repeater uit te voeren, is het handig om de installatiemap een beschrijvende naam te geven, zoals [!DNL D:\Adobe\Repeater].

1. Installeer het [!DNL Insight Server] digitale certificaat zoals beschreven in [Digitale certificaten downloaden en installeren](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).

   Nadat u zich bij de Server van de Vergunning van de Adobe hebt aangemeld, herinner me om naar de certificaatnaam te zoeken die de server gemeenschappelijke naam van de aangewezen repeatermachine aanpast.

1. Controleer de poortinstellingen in het [!DNL Communications.cfg]-bestand zoals beschreven in [De poortinstellingen controleren](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-chk-pt-stgs.md#task-a91191b0a19e4437aa535a27c734ae64).

   Als de toegewezen havens (Haven en SSL Haven) door een ander proces worden gebruikt dat op de zelfde machine loopt, moet u de haventaken in een ongebruikt paar veranderen.

1. Wijzig zo nodig de logmap voor de [!DNL Sensor]-gegevens die moeten worden verzameld en opgeslagen op deze computer. Zie [Gebeurtenisgegevensruimte controleren](../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-evt-data-spc.md#task-a54d4bd16b96437f943cd09e5d848440) voor instructies.
1. Wijzig het [!DNL Access Control.cfg] dossier om administratieve toegang tot [!DNL Insight Server] van [!DNL Insight] toe te staan zoals die in [Bijwerken van het Dossier van het Toegangsbeheer](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-updt-accss-ctrl-file.md#concept-fb9aa0c0e0664c018528f56d01c4808d) wordt beschreven.
1. Wijzig het [!DNL server.address]-bestand om de netwerklocatie van de server te definiëren zoals gedefinieerd in [De netwerklocatie van de server definiëren](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649).
1. Stel Windows-parameters voor geheugengebruik in.
1. Registreer [!DNL Insight Server] als dienst van Vensters zoals die in [wordt beschreven het Registreren van de Server van het Inzicht als Dienst ](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540) van Vensters.

---
description: Instructies om een Server FSU van het Inzicht voor gebruik met Repeater te installeren en te vormen.
solution: Insight
title: Het vormen van een Server FSU van het Inzicht voor Repeater
uuid: c2bae862-37d3-4841-b31b-59593c1e4316
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen van een Server FSU van het Inzicht voor Repeater{#configuring-an-insight-server-fsu-for-repeater}

Instructies om een Server FSU van het Inzicht voor gebruik met Repeater te installeren en te vormen.

Voltooi de volgende taken in orde. Om het even welke uitzonderingen of veranderingen die u moet aanbrengen zodat [!DNL Insight Server] FSU als repeaterserver kan worden gebruikt worden genoteerd na elke stap.

1. Installeer de [!DNL Insight Server] programmadossiers zoals die in het [Installeren van de Server](../../../../home/c-inst-svr/c-install-ins-svr/c-install-ins-svr.md#concept-1c796b4ca427474f99ec6ba34d8254cd)van het Inzicht worden beschreven.

   Omdat de machine waarop u deze dossiers installeert wordt gebruikt om Repeater in werking te stellen, is het nuttig om de installatiefolder een beschrijvende naam zoals [!DNL D:\Adobe\Repeater]te geven.

1. Installeer het [!DNL Insight Server] digitale certificaat zoals beschreven in het [Downloaden van en het Installeren van de Digitale Certificaten](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).

   Nadat u aan de Server van de Vergunning van Adobe het programma hebt geopend, herinner me om de certificaatnaam te zoeken die de server gemeenschappelijke naam van de aangewezen repeatermachine aanpast.

1. Controleer de havenmontages in het [!DNL Communications.cfg] dossier zoals die in het [Controleren van de Montages](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/t-chk-pt-stgs.md#task-a91191b0a19e4437aa535a27c734ae64)van de Haven worden beschreven.

   Als de toegewezen havens (Haven en SSL Haven) door een ander proces worden gebruikt dat op de zelfde machine loopt, moet u de haventaken in een ongebruikt paar veranderen.

1. Indien nodig, verander de logboekfolder voor de [!DNL Sensor] gegevens die op dit systeem moeten worden verzameld en worden opgeslagen. Voor instructies, zie de Ruimte [van de Gegevens van de Gebeurtenis van de](../../../../home/c-inst-svr/c-admin-inst-svr/c-mntr-disk-spc/t-mntr-evt-data-spc.md#task-a54d4bd16b96437f943cd09e5d848440)Controle.
1. Wijzig het [!DNL Access Control.cfg] dossier om administratieve toegang tot van toe te staan [!DNL Insight Server] zoals die in het [!DNL Insight] Bijwerken van het Dossier [](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-updt-accss-ctrl-file.md#concept-fb9aa0c0e0664c018528f56d01c4808d)van het Toegangsbeheer wordt beschreven.
1. Wijzig het [!DNL server.address] dossier om de het netwerkplaats van de server te bepalen zoals die in het [Bepalen van de Plaats](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649)van het Netwerk van de Server wordt bepaald.
1. De vastgestelde parameters van het het geheugengebruik van Vensters.
1. Register [!DNL Insight Server] als dienst van Vensters zoals die in de Server van het Inzicht van het [Registreren als Dienst](../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)van Vensters wordt beschreven.

---
description: Typisch, wilt u een DPU van de Server van het Inzicht aan een bestaande cluster toevoegen wanneer de hoeveelheid gegevens u toegankelijk voor uw gebruikers van Inzicht en Rapport wilt verwerken en maken de capaciteit van de huidige configuratie van uw cluster overschrijdt.
solution: Insight
title: Het toevoegen van een Server DPU van het Inzicht aan een Bestaande Cluster
uuid: 1977a90e-bd51-4838-9498-f7692891109f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het toevoegen van een Server DPU van het Inzicht aan een Bestaande Cluster{#adding-an-insight-server-dpu-to-an-existing-cluster}

Typisch, wilt u een DPU van de Server van het Inzicht aan een bestaande cluster toevoegen wanneer de hoeveelheid gegevens u toegankelijk voor uw gebruikers van Inzicht en Rapport wilt verwerken en maken de capaciteit van de huidige configuratie van uw cluster overschrijdt.

## Het bijwerken van de Dossiers van de Configuratie op de HoofdServer {#section-7c9a23754a994d73b722d53f999f0e82}

In [!DNL Insight], open [!DNL Server Files Manager] voor uw meester [!DNL Insight Server] (gewoonlijk een [!DNL Insight Server] FSU) en doe het volgende voor elke DPU die u aan de cluster wilt toevoegen:

1. Geef het adresdossier op de meester uit [!DNL Insight Server] om de naam en het adres van nieuwe DPU te omvatten zoals die in het [Toevoegen van de Servers van het Inzicht van de Verwerking aan het Dossier](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d)van het Adres wordt beschreven. Voeg de naam en het adres van nieuwe DPU aan de groep toe waarin de stroom van uw cluster vermeld [!DNL Insight Servers] zijn.

1. Geef het toegangsbeheerdossier op de meester uit [!DNL Insight Server] om het IP adres van nieuwe DPU te omvatten zoals die in het [Bijwerken van het Dossier van het Toegangsbeheer voor een Cluster](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b)wordt beschreven.

## Het installeren van de Nieuwe Server DPU van het Inzicht {#section-8ce9a5957db24f94b3a3250caaccc7ba}

Deze taak is slechts op Vensters 32 beetje van toepassing.

1. Kopieer de volgende folders van één van huidige DPUs in uw cluster aan nieuwe DPU:

   * [!DNL Insight Server] installatiefolder/bin/
   * [!DNL Insight Server] installatiefolder/Certificaten/
   * [!DNL Insight Server] installatiefolder/componenten/

1. De download en installeert het digitale certificaat voor nieuwe DPU zoals die in het [Downloaden van en het Installeren van de Digitale Certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17)wordt beschreven.
1. Plaats de parameters van het het geheugengebruik van Vensters op nieuwe DPU.
1. Register [!DNL Insight Server] als dienst van Vensters op de nieuwe machine DPU zoals die in de [Registrerende Server van het Inzicht als Dienst](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540)van Vensters wordt beschreven.

1. Controleer de logboeken van het Spoor om ervoor te zorgen dat DPU aan de meester synchroniseert [!DNL Insight Server].
1. Herhaal stappen 1 door 6 voor elke extra DPU die u aan de cluster toevoegt.

## Het toevoegen van de Nieuwe Server DPU van het Inzicht aan de Servers van de Verwerking van het Profiel van de Dataset {#section-cdc6c3913b9f4010b5e17cc7ec85e849}

Als nieuwe DPU de zelfde dataset zoals andere DPUs in de cluster verwerkt, voeg de gemeenschappelijke naam van nieuwe DPU aan het [!DNL profile.cfg] dossier op meester toe [!DNL Insight Server] zoals die in het [Specificeren van de Servers van de Verwerking in Profile.cfg](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9)wordt beschreven.

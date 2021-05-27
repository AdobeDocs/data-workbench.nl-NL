---
description: Typisch, wilt u een DPU van de Server van het Inzicht aan een bestaande cluster toevoegen wanneer de hoeveelheid gegevens u aan uw gebruikers van Inzicht en Rapport verwerken en toegankelijk maken de capaciteit van de huidige configuratie van uw cluster overschrijdt.
title: Een Insight Server DPU toevoegen aan een bestaande cluster
uuid: 1977a90e-bd51-4838-9498-f7692891109f
exl-id: 9cac2795-626b-4fe3-8a7c-f36c9f1dc68f
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Een Insight Server DPU toevoegen aan een bestaande cluster{#adding-an-insight-server-dpu-to-an-existing-cluster}

Typisch, wilt u een DPU van de Server van het Inzicht aan een bestaande cluster toevoegen wanneer de hoeveelheid gegevens u aan uw gebruikers van Inzicht en Rapport verwerken en toegankelijk maken de capaciteit van de huidige configuratie van uw cluster overschrijdt.

## De configuratiebestanden op de Master server {#section-7c9a23754a994d73b722d53f999f0e82} bijwerken

Open [!DNL Insight] voor uw master [!DNL Insight Server] (gewoonlijk een [!DNL Insight Server] FSU) de [!DNL Server Files Manager] en voer de volgende handelingen uit voor elke DPU die u aan het cluster wilt toevoegen:

1. Bewerk het adresbestand op de master [!DNL Insight Server] om de naam en het adres van de nieuwe DPU op te nemen, zoals beschreven in [De servers van het Inzicht van de Verwerking toevoegen aan het Dossier van het Adres](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-2fe5298180164e8dbaa59ea6b6ff682d). Voeg de naam en het adres van nieuwe DPU aan de groep toe waarin de stroom [!DNL Insight Servers] van uw cluster wordt vermeld.

1. Bewerk het toegangsbeheerbestand op het master [!DNL Insight Server] om het IP-adres van de nieuwe DPU op te nemen, zoals wordt beschreven in [Het toegangsbeheerbestand voor een cluster bijwerken](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-mstr-ins-svr-clstr.md#section-fce1367d92a445168c35e9ca506e7d6b).

## De nieuwe DPU van de Server van het Inzicht installeren {#section-8ce9a5957db24f94b3a3250caaccc7ba}

Deze taak is alleen van toepassing op Windows 32-bits.

1. Kopieer de volgende folders van één van huidige DPUs in uw cluster aan nieuwe DPU:

   * [!DNL Insight Server] installatiemap/bin/
   * [!DNL Insight Server] installatiemap/Certificaten/
   * [!DNL Insight Server] installatiemap/Componenten/

1. Download en installeer het digitale certificaat voor de nieuwe DPU, zoals beschreven in [De digitale certificaten downloaden en installeren](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#concept-4f79c240492f4e52b6375b4b3bbefa17).
1. Plaats de parameters van het het geheugengebruik van Vensters op nieuwe DPU.
1. Registreer [!DNL Insight Server] als dienst van Vensters op de nieuwe machine DPU zoals die in [het Registreren van de Server van het Inzicht als Dienst van Vensters wordt beschreven](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-reg-wdws-svc.md#concept-f2c7aa891d544a2595aa01d0d796a540).

1. Controleer het spoor logboeken om ervoor te zorgen dat DPU aan master [!DNL Insight Server] synchroniseert.
1. Herhaal stap 1 door 6 voor elke extra DPU die u aan de cluster toevoegt.

## De nieuwe DPU van de Server van het Inzicht toevoegen aan de Servers van de Verwerking van het Profiel van de Dataset {#section-cdc6c3913b9f4010b5e17cc7ec85e849}

Als nieuwe DPU de zelfde dataset zoals andere DPUs in de cluster verwerkt, voeg de gemeenschappelijke naam van nieuwe DPU aan het [!DNL profile.cfg] dossier op master [!DNL Insight Server] zoals die in [wordt beschreven het Specificeren van de Servers van de Verwerking in Profile.cfg](../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9) toe.

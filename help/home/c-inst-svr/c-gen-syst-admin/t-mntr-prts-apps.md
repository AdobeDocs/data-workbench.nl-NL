---
description: Om uw implementatie grondiger te controleren, kunt u alle havens op uw servermachines evenals de softwareproducten controleren die op elk van die havens lopen.
title: Poorten en toepassingen bewaken
uuid: 63d92718-81df-49eb-adda-8b49bde57a9d
exl-id: 418b2e5c-42ec-40f0-9cae-375194288143
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# De Havens en Toepassingen van de controle{#monitoring-ports-and-applications}

Om uw implementatie grondiger te controleren, kunt u alle havens op uw servermachines evenals de softwareproducten controleren die op elk van die havens lopen.

**Aanbevolen frequentie:** elke 5-10 minuten

Gebruikend een toepassing of een manuscript, kunt u de haven van TCP controleren waarop elke toepassing (typisch haven 80 of 443) loopt om ervoor te zorgen dat de toepassing aan die haven verbindend is. Hiervoor vraagt u een statuspagina voor de toepassing op van het systeem dat u wilt controleren.

**De statuspagina van de toepassing aanvragen**

1. Op de machine wilt u controleren, wijzig de Controles van de Toegang om uw controletoepassing of manuscript toe te staan om tot de machine toegang te hebben. Voor instructies, zie [Vormend Toegangsbeheer](../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d).
1. Verbind met [!DNL https://IP Address/Status/], waar IP het Adres het IP adres van de machine is waarvoor u status wilt ontvangen.

   Voorbeeld: [!DNL https://127.0.0.1/Status/]

   De computer moet reageren met een beschrijving van de serverstatus. Als de toepassing niet reageert, controleert u uw gebeurtenissenlogboeken en neemt u contact op met de klantenservice van Adobe.

   Neem voor meer informatie over dit type geavanceerde controle contact op met de Adobe Consulting Services.

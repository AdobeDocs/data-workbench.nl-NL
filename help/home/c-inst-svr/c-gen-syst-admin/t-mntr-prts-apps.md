---
description: Om uw implementatie grondiger te controleren, kunt u alle havens op uw servermachines evenals de softwareproducten controleren die op elk van die havens lopen.
solution: Insight
title: De havens en de Toepassingen van de controle
uuid: 63d92718-81df-49eb-adda-8b49bde57a9d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De havens en de Toepassingen van de controle{#monitoring-ports-and-applications}

Om uw implementatie grondiger te controleren, kunt u alle havens op uw servermachines evenals de softwareproducten controleren die op elk van die havens lopen.

**Aanbevolen frequentie:** Om de 5-10 minuten

Gebruikend een toepassing of een manuscript, kunt u de haven van TCP controleren waarop elke toepassing loopt (typisch haven 80 of 443) om ervoor te zorgen dat de toepassing aan die haven verbindend is. Om dit te doen, vraagt u een pagina van de toepassingsstatus van het systeem u wilt controleren.

**Om de pagina van de toepassingsstatus te verzoeken**

1. Voor de machine wilt u controleren, de Controles van de Toegang wijzigen om uw controletoepassing of manuscript toe te staan om tot de machine toegang te hebben. Voor instructies, zie het [Vormen Toegangsbeheer](../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-config-acs-ctrl.md#concept-ac385e870dbe4b57a72bf7266b60f93d).
1. Verbind met [!DNL https://IP Address/Status/], waar IP het Adres het IP adres van de machine is waarvoor u status wilt ontvangen.

   Voorbeeld: [!DNL https://127.0.0.1/Status/]

   Het systeem moet reageren met een beschrijving van de serverstatus. Als het niet antwoordt, controleer uw gebeurtenislogboeken en contacteer de Zorg van de Klant van Adobe.

   Voor meer informatie over dit type van geavanceerde controle, gelieve te contacteren de Raadplegende Diensten van Adobe.


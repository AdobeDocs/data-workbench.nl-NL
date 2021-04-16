---
description: Als de cliënten een Server van het Inzicht door veelvoudige netwerken (bijvoorbeeld, door het collectieve Intranet en door Internet) kunnen bereiken, moet het adresdossier een afzonderlijke netwerkplaats voor elk van de IP van de server adressen bepalen.
title: Meerdere IP-adressen voor een Insight Server
uuid: 6ed00b47-8ba3-4127-a5db-7e684e573d9c
exl-id: 71654a60-af82-45f2-826b-29ecc7127b0b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Meerdere IP-adressen voor een Insight Server{#multiple-ip-addresses-for-an-insight-server}

Als de cliënten een Server van het Inzicht door veelvoudige netwerken (bijvoorbeeld, door het collectieve Intranet en door Internet) kunnen bereiken, moet het adresdossier een afzonderlijke netwerkplaats voor elk van de IP van de server adressen bepalen.

Als server [!DNL VS01.myCompany.com] bijvoorbeeld een IP-adres van 10.2.1.70 heeft op een intern netwerk en een IP-adres van 65.196.125.167 op internet, bevat het adresbestand een netwerklocatie voor elk van de adressen, zoals in het onderstaande voorbeeld wordt geïllustreerd:

```
0 = NetworkLocation: 
  Addresses = vector: 1 items
    0 = AddressDefinition: 
      Address = string: 10.2.1.70
      Name = string: VS01.myCompany.com
  Name = string: MyCorporateIntranet
  Parent = string: 
1 = NetworkLocation: 
  Addresses = vector: 1 items
    0 = AddressDefinition: 
      Address = string: 65.196.125.167
      Name = string: VS01.myCompany.com
  Name = string: Internet
  Parent = string:
```

Wanneer gebruikers verbinding maken met een [!DNL Insight Server], gebruiken ze de parameter NetworkLocation (in de gebruikersinterface van de client) om de netwerklocatie op te geven waarlangs ze de algemene naam van de server willen laten oplossen. Bijvoorbeeld, gezien een adresdossier met de twee hierboven getoonde NetworkLocations, zou een gebruiker de parameter NetworkLocation aan &quot;MyCorporate Intranet&quot;plaatsen om met [!DNL Insight Server] door het interne netwerk en aan &quot;Internet&quot;te verbinden met de server door Internet.

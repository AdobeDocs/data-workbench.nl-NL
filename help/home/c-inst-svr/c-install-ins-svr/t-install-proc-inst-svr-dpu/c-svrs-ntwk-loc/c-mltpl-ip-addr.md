---
description: Als de cliënten een Server van het Inzicht door veelvoudige netwerken (bijvoorbeeld, door het collectieve Intranet en door Internet) kunnen bereiken, moet het adresdossier een afzonderlijke netwerkplaats voor elk van de IP van de server adressen bepalen.
title: Meerdere IP-adressen voor een Insight Server
uuid: 6ed00b47-8ba3-4127-a5db-7e684e573d9c
exl-id: 71654a60-af82-45f2-826b-29ecc7127b0b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Meerdere IP-adressen voor een Insight Server{#multiple-ip-addresses-for-an-insight-server}

{{eol}}

Als de cliënten een Server van het Inzicht door veelvoudige netwerken (bijvoorbeeld, door het collectieve Intranet en door Internet) kunnen bereiken, moet het adresdossier een afzonderlijke netwerkplaats voor elk van de IP van de server adressen bepalen.

Bijvoorbeeld als server [!DNL VS01.myCompany.com] heeft een IP adres van 10.2.1.70 op een intern netwerk, en een IP adres van 65.196.125.167 op Internet, zou het adresdossier een netwerkplaats voor elk van de adressen omvatten zoals die in het voorbeeld hieronder worden geïllustreerd:

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

Wanneer gebruikers verbinding maken met een [!DNL Insight Server], gebruiken zij de parameter NetworkLocation (in het cliëntgebruikersinterface) om de netwerkplaats te specificeren waardoor zij de gemeenschappelijke naam van de server willen oplossen. Bijvoorbeeld, gezien een adresdossier met twee hierboven getoonde NetworkLocations, zou een gebruiker de parameter NetworkLocation aan &quot;MyCorporate Intranet&quot;plaatsen om te verbinden met [!DNL Insight Server] via het interne netwerk en op &quot;Internet&quot;om met de server door Internet te verbinden.

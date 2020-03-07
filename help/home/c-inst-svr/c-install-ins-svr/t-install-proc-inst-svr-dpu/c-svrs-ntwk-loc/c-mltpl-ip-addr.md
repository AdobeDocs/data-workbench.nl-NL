---
description: Als de cliënten een Server van het Inzicht door veelvoudige netwerken (bijvoorbeeld, door het collectieve Intranet en door Internet) kunnen bereiken, moet het adresdossier een afzonderlijke netwerkplaats voor elk van de IP van de server adressen bepalen.
solution: Insight
title: Veelvoudige IP Adressen voor een Server van het Inzicht
uuid: 6ed00b47-8ba3-4127-a5db-7e684e573d9c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Veelvoudige IP Adressen voor een Server van het Inzicht{#multiple-ip-addresses-for-an-insight-server}

Als de cliënten een Server van het Inzicht door veelvoudige netwerken (bijvoorbeeld, door het collectieve Intranet en door Internet) kunnen bereiken, moet het adresdossier een afzonderlijke netwerkplaats voor elk van de IP van de server adressen bepalen.

Bijvoorbeeld, als de server een IP adres van 10.2.1.70 op een intern netwerk, en een IP adres van 65.196.125.167 op Internet [!DNL VS01.myCompany.com] heeft, zou het adresdossier een netwerkplaats voor elk van de adressen omvatten zoals die in het voorbeeld hieronder worden geïllustreerd:

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

Wanneer de gebruikers met een [!DNL Insight Server]verbinden, gebruiken zij de parameter NetworkLocation (in het cliëntgebruikersinterface) om de netwerkplaats te specificeren waardoor zij de gemeenschappelijke naam van de server willen oplossen. Bijvoorbeeld, gezien een adresdossier met twee hierboven getoonde NetworkLocations, zou een gebruiker de parameter NetworkLocation aan &quot;MyCorporate Intranet&quot;plaatsen om met [!DNL Insight Server] door het interne netwerk en met &quot;Internet&quot;te verbinden om met de server door Internet te verbinden.

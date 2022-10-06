---
description: Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd bevat vier vooraf bepaalde netwerkplaatsen.
title: Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd
uuid: a58d36d8-e1a3-43e7-91c5-c57351e1be49
exl-id: 12e9bfa2-99ac-4584-b761-38401d1bc3d1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd{#the-address-file-installed-on-insight-server}

{{eol}}

Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd bevat vier vooraf bepaalde netwerkplaatsen.

De procedure in de volgende sectie beschrijft hoe te om dit dossier te vormen.

```
Locations = vector: 4 items  
  0 = NetworkLocation:  
    Addresses = vector: 1 items 
      0 = AddressDefinition:  
        Address = string:  
        Name = string:  
    Name = string:  
    Parent = string:  
  1 = NetworkLocation:  
    Addresses = vector: 0 items 
    Name = string: Insight 
    Parent = string:  
  2 = NetworkLocation:  
    Addresses = vector: 0 items 
    Name = string: Insight Server 
    Parent = string: 
  3 = NetworkLocation:  
    Addresses = vector: 0 items 
    Name = string: Report Server 
    Parent = string:
```

* NetworkLocation 0 is een lege, naamloze netwerkplaats die u uitgeeft om de gemeenschappelijke naam van uw te associëren [!DNL Insight Server] aan zijn IP adres. Als de server veelvoudige IP adressen heeft, creeert u extra NetworkLocations.
* NetworkLocation 1 is de [!DNL Insight] netwerklocatie. Als u niet uitdrukkelijk de parameter NetworkLocation plaatst, [!DNL Insight] Hiermee worden algemene namen via deze netwerklocatie opgelost.

* NetworkLocation 2 is de [!DNL Insight Server] netwerklocatie. Wanneer [!DNL Insight Servers] werken in een cluster, gebruiken zij deze netwerkplaats om gemeenschappelijke namen voor inter-servermededeling op te lossen.

* NetworkLocation 3 is de [!DNL Report] Servernetwerklocatie. Als u niet uitdrukkelijk de parameter NetworkLocation plaatst, [!DNL Report] Hiermee worden algemene namen via deze netwerklocatie opgelost.

## Om het Dossier van het Adres te vormen {#section-10caab9854a244e39b09071946f7bd27}

De volgende procedure beschrijft hoe te om het adresdossier te vormen om een netwerkplaats (of netwerkplaatsen) voor uw te bepalen [!DNL Insight Server].

1. Ga naar de [!DNL Addresses] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server] (bijvoorbeeld [!DNL C:\Adobe\Server\Addresses)].

1. Zoek de [!DNL server.address] en wijzig de naam van dit bestand om de algemene naam van de server weer te geven. Als de algemene naam bijvoorbeeld [!DNL server.mycompany.com], geeft u het bestand een andere naam [!DNL server.mycompany.com.address].

1. Open het hernoemde bestand in een teksteditor, zoals Kladblok.
1. Bewerk NetworkLocation 0 om de algemene naam en het IP-adres van het [!DNL Insight Server] zoals hieronder weergegeven. Als uw server veelvoudige IP adressen heeft, gebruik NetworkLocation 0 om het IP van de server adres op het lokale, niet routable netwerk (bijvoorbeeld, zijn plaats op het interne netwerk) te specificeren.

   ```
   Locations = vector: 3 items 
   0 = NetworkLocation: 
     Addresses = vector: 1 items 
       0 = AddressDefinition: 
         Address = string: IPAddress 
         Name = string: CommonName 
     Name = string: NetworkLocationName 
     Parent = string: 
   ```

<table id="table_02C2A1630CCD40C4A51B314C3CB683F1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze waarde... </th> 
   <th colname="col2" class="entry"> Opgeven </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>IP-adres</i> </td> 
   <td colname="col2"> <p>Het numerieke IP-adres van het <span class="keyword"> Insight Server </span> machine. </p> <p>Voorbeeld: 192 168 124 176 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Algemene naam </i> </td> 
   <td colname="col2"> <p>De algemene naam die aan het digitale certificaat is toegewezen voor <span class="keyword"> Insight Server </span>. </p> <p>Voorbeeld: <span class="filepath"> server.mijnbedrijf.com </span></p> <p>Opmerking: Zorg ervoor dat u deze naam precies zo typt als op het certificaat wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Naam netwerklocatie </i> </td> 
   <td colname="col2"> <p>De naam u aan de inzameling van gemeenschappelijke namen en IP adressen wilt toewijzen die dit NetworkLocation vertegenwoordigt. De naam moet uniek zijn in het adresbestand. </p> <p>Voorbeeld: Bedrijfsintranet </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Als uw [!DNL Insight Server] heeft extra IP adressen, creeer een extra NetworkLocation voor elk adres. (Een gemakkelijke manier om dit te doen is een exemplaar van NetworkLocation te maken u hierboven creeerde en het IP adres in het exemplaar bij te werken.)

   U kunt nieuwe NetworkLocation aan het eind van het adresdossier toevoegen of het tussen bestaande definities opnemen NetworkLocation. (De positie van een NetworkLocation binnen het adresdossier is niet significant; de [!DNL Insight], [!DNL Insight Server], en [!DNL Report] Servernetwerklocaties worden doorgaans aan het einde van het bestand geplaatst.)

   Nadat u noodzakelijke NetworkLocations hebt toegevoegd, doe het volgende de punten in het dossier opnieuw nummeren:

   1. Werk het puntaantal voor de structuur van Plaatsen bij om het totale aantal definities NetworkLocation in het dossier aan te passen. Bijvoorbeeld, als uw dossier vier definities NetworkLocation bevat, zou de lijn van Plaatsen als volgt kijken:

      ```
      Locations = vector: 4 items
      ```

   1. Werk de NetworkLocation puntaantallen bij zodat NetworkLocations achtereenvolgens (die van 0 beginnen) worden genummerd.
   Een voorbeeld van een adresbestand dat een [!DNL Insight Server] met twee IP adressen, zie het voorbeeld in deze sectie.

1. In de [!DNL Insight] en [!DNL Report] De het netwerkplaatsen van de server, geef de parameter van de Ouder zoals hieronder getoond uit om de naam van NetworkLocation te specificeren die [!DNL Insight] en [!DNL Report] gebruiken als hun standaardnetwerkplaatsen. (Zie het voorbeeld in deze sectie voor een voorbeeld van hoe de parameter Bovenliggend eruitziet wanneer deze is geconfigureerd.)

   ```
   1 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Insight 
     Parent = string: ClientDefaultNetworkLocation 
   
   3 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Report Server 
     Parent = string: ClientDefaultNetworkLocation
   ```

   Als uw [!DNL Insight Server] heeft één enkel IP adres en, daarom, heeft slechts één NetworkLocation, richt de parameter van de Ouder aan die NetworkLocation. Als uw [!DNL Insight Server] heeft veelvoudige IP adressen, punt de parameter van de Ouder aan NetworkLocation die het adres bepaalt waaraan uw [!DNL Insight] en [!DNL Report] clients maken meestal verbinding.

1. In de [!DNL Insight Server] netwerklocatie, bewerk de parameter Bovenliggend zoals hieronder wordt weergegeven om naar de NetworkLocation te wijzen die de server gebruikt om algemene namen van andere [!DNL Insight Servers] wanneer het in een cluster werkt. (Hoewel deze netwerklocatie niet wordt gebruikt tenzij een [!DNL Insight Server] werkt in een cluster, is het een goede praktijk, zelfs in één enkele serverconfiguratie, om de parameter van de Ouder aan een netwerkplaats te richten die het interne IP van de server adres. identificeert)

   ```
   2 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Insight Server 
     Parent = string: ServerDefaultNetworkLocation
   ```

In het volgende voorbeeld wordt een voltooid adresbestand getoond. Dit bestand definieert vijf netwerklocaties.

* De punten 0 en 1 van NetworkLocation bepalen netwerkplaatsen genoemd &quot;MyCorporateIntranet&quot;en &quot;Internet.&quot; Deze netwerklocaties definiëren twee verschillende IP-adressen voor een server met een naam [!DNL VS01.myCompany.com].
* NetworkLocation-item 2 is het [!DNL Insight] netwerklocatie. Dit is de standaardnetwerklocatie die wordt gebruikt door [!DNL Insight]. In dit voorbeeld wordt [!DNL Insight] de netwerkplaats erft zijn AddressDefinitions van &quot;Internet&quot;NetworkLocation.

* NetworkLocation-item 3 is het [!DNL Insight Server] netwerklocatie. Dit is de standaardnetwerklocatie [!DNL Insight Server] gebruikt wanneer het met andere servers in een cluster communiceert. In dit voorbeeld wordt [!DNL Insight Server] de netwerkplaats erft zijn AddressDefinitions van &quot;MyCorporate Intranet&quot;NetworkLocation.

* NetworkLocation-item 4 is het [!DNL Report] Servernetwerklocatie. Dit is de standaardnetwerklocatie die wordt gebruikt door [!DNL Report]. In dit voorbeeld wordt [!DNL Report] De het netwerkplaats van de server erft zijn AddressDefinitions van &quot;Internet&quot;NetworkLocation.

   ```
   Locations = vector: 5 items 
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
   
     2 = NetworkLocation:  
       Addresses = vector: 0 items 
       Name = string: Insight 
       Parent = string: Internet 
   
     3 = NetworkLocation:  
       Addresses = vector: 0 items 
       Name = string: Insight Server 
       Parent = string: MyCorporateIntranet 
   
     4 = NetworkLocation:  
       Addresses = vector: 0 items 
       Name = string: Report Server 
       Parent = string: Internet
   ```

---
description: Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd bevat vier vooraf bepaalde netwerkplaatsen.
title: Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd
uuid: a58d36d8-e1a3-43e7-91c5-c57351e1be49
exl-id: 12e9bfa2-99ac-4584-b761-38401d1bc3d1
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Het adresbestand geïnstalleerd op Insight Server{#the-address-file-installed-on-insight-server}

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

* NetworkLocation 0 is een lege, naamloze netwerkplaats die u uitgeeft om de gemeenschappelijke naam van uw [!DNL Insight Server] aan zijn IP adres te associëren. Als de server veelvoudige IP adressen heeft, creeert u extra NetworkLocations.
* NetworkLocation 1 is de [!DNL Insight] netwerklocatie. Als u niet expliciet de parameter NetworkLocation instelt, [!DNL Insight] lost gemeenschappelijke namen door deze netwerkplaats op.

* NetworkLocation 2 is de [!DNL Insight Server] netwerklocatie. Wanneer [!DNL Insight Servers] in een cluster werkt, gebruiken zij deze netwerkplaats om gemeenschappelijke namen voor interservermededeling op te lossen.

* NetworkLocation 3 is de [!DNL Report] netwerklocatie van de server. Als u niet expliciet de parameter NetworkLocation instelt, [!DNL Report] lost gemeenschappelijke namen door deze netwerkplaats op.

## Om het Dossier van het Adres {#section-10caab9854a244e39b09071946f7bd27} te vormen

De volgende procedure beschrijft hoe te om het adresdossier te vormen om een netwerkplaats (of netwerkplaatsen) voor uw [!DNL Insight Server] te bepalen.

1. Navigeer naar de map [!DNL Addresses] in de map waarin u [!DNL Insight Server] hebt geïnstalleerd (bijvoorbeeld [!DNL C:\Adobe\Server\Addresses)].

1. Zoek het bestand [!DNL server.address] en geef dit bestand een andere naam om de algemene naam van de server weer te geven. Als de algemene naam bijvoorbeeld [!DNL server.mycompany.com] was, zou u de naam van het bestand [!DNL server.mycompany.com.address] wijzigen.

1. Open het hernoemde bestand in een teksteditor, zoals Kladblok.
1. Bewerk NetworkLocation 0 om de algemene naam en het IP-adres van [!DNL Insight Server] op te geven, zoals hieronder wordt weergegeven. Als uw server veelvoudige IP adressen heeft, gebruik NetworkLocation 0 om het IP van de server adres op het lokale, niet routable netwerk (bijvoorbeeld, zijn plaats op het interne netwerk) te specificeren.

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
   <td colname="col2"> <p>Het numerieke IP-adres van de <span class="keyword"> Insight Server </span>-computer. </p> <p>Voorbeeld: 192 168 124 176 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Algemene naam  </i> </td> 
   <td colname="col2"> <p>De algemene naam die is toegewezen aan het digitale certificaat voor <span class="keyword"> Insight Server </span>. </p> <p>Voorbeeld: <span class="filepath"> server.mijnbedrijf.com </span></p> <p>Opmerking: Zorg ervoor dat u deze naam precies zo typt als op het certificaat wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Naam netwerklocatie  </i> </td> 
   <td colname="col2"> <p>De naam u aan de inzameling van gemeenschappelijke namen en IP adressen wilt toewijzen die dit NetworkLocation vertegenwoordigt. De naam moet uniek zijn in het adresbestand. </p> <p>Voorbeeld: Bedrijfsintranet </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Als uw [!DNL Insight Server] extra IP adressen heeft, creeer een extra NetworkLocation voor elk adres. (Een gemakkelijke manier om dit te doen is een exemplaar van NetworkLocation te maken u hierboven creeerde en het IP adres in het exemplaar bij te werken.)

   U kunt nieuwe NetworkLocation aan het eind van het adresdossier toevoegen of het tussen bestaande definities opnemen NetworkLocation. (De positie van een NetworkLocation binnen het adresdossier is niet significant; echter, [!DNL Insight], [!DNL Insight Server], en [!DNL Report] de Netwerkplaatsen van de Server worden typisch geplaatst aan het eind van het dossier.)

   Nadat u noodzakelijke NetworkLocations hebt toegevoegd, doe het volgende de punten in het dossier opnieuw nummeren:

   1. Werk het puntaantal voor de structuur van Plaatsen bij om het totale aantal definities NetworkLocation in het dossier aan te passen. Bijvoorbeeld, als uw dossier vier definities NetworkLocation bevat, zou de lijn van Plaatsen als volgt kijken:

      ```
      Locations = vector: 4 items
      ```

   1. Werk de NetworkLocation puntaantallen bij zodat NetworkLocations achtereenvolgens (die van 0 beginnen) worden genummerd.
   Voor een voorbeeld van een adresdossier dat [!DNL Insight Server] met twee IP adressen bepaalt, zie het voorbeeld in deze sectie.

1. Bewerk in de netwerklocaties [!DNL Insight] en [!DNL Report] de parameter Parent, zoals hieronder wordt weergegeven, om de naam op te geven van de NetworkLocation die [!DNL Insight] en [!DNL Report] als hun standaardnetwerklocaties gebruiken. (Zie het voorbeeld in deze sectie voor een voorbeeld van hoe de parameter Bovenliggend eruitziet wanneer deze is geconfigureerd.)

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

   Als uw [!DNL Insight Server] één enkel IP adres heeft en daarom slechts één NetworkLocation heeft, richt de parameter van de Ouder aan die NetworkLocation. Als uw [!DNL Insight Server] veelvoudige IP adressen heeft, richt de parameter van de Ouder aan NetworkLocation die het adres bepaalt waaraan uw [!DNL Insight] en [!DNL Report] cliënten het vaakst verbinden.

1. Bewerk in de netwerklocatie [!DNL Insight Server] de parameter Bovenliggend, zoals hieronder wordt weergegeven, om naar de NetworkLocation te verwijzen die de server gebruikt om algemene namen van andere [!DNL Insight Servers] op te lossen wanneer deze in een cluster werkt. (Hoewel deze netwerklocatie niet wordt gebruikt tenzij een [!DNL Insight Server] in een cluster werkt, is het een goede praktijk, zelfs in één serverconfiguratie, om de parameter Bovenliggende naar een netwerklocatie te richten die het interne IP-adres van de server identificeert.)

   ```
   2 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Insight Server 
     Parent = string: ServerDefaultNetworkLocation
   ```

In het volgende voorbeeld wordt een voltooid adresbestand getoond. Dit bestand definieert vijf netwerklocaties.

* De punten 0 en 1 van NetworkLocation bepalen netwerkplaatsen genoemd &quot;MyCorporateIntranet&quot;en &quot;Internet.&quot; Deze netwerklocaties definiëren twee verschillende IP-adressen voor een server met de naam [!DNL VS01.myCompany.com].
* NetworkLocation punt 2 is de [!DNL Insight] netwerkplaats. Dit is de standaardnetwerklocatie die wordt gebruikt door [!DNL Insight]. In dit voorbeeld, erft [!DNL Insight] netwerkplaats zijn AddressDefinitions van &quot;Internet&quot;NetworkLocation.

* NetworkLocation-item 3 is de netwerklocatie [!DNL Insight Server]. Dit is de standaardnetwerklocatie die [!DNL Insight Server] gebruikt wanneer deze communiceert met andere servers in een cluster. In dit voorbeeld, erft [!DNL Insight Server] netwerkplaats zijn AddressDefinitions van &quot;MyCorporate Intranet&quot;NetworkLocation.

* NetworkLocation-item 4 is de locatie van het [!DNL Report]-servernetwerk. Dit is de standaardnetwerklocatie die wordt gebruikt door [!DNL Report]. In dit voorbeeld overerft de [!DNL Report] netwerklocatie van de server zijn AddressDefinitions van de &quot;Internet&quot;NetworkLocation.

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

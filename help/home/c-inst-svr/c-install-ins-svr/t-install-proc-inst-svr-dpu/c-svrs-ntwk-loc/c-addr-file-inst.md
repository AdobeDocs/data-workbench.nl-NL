---
description: Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd bevat vier vooraf bepaalde netwerkplaatsen.
solution: Analytics
title: Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd
uuid: a58d36d8-e1a3-43e7-91c5-c57351e1be49
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---


# Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd{#the-address-file-installed-on-insight-server}

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
* NetworkLocation 1 is de [!DNL Insight] netwerkplaats. Als u niet uitdrukkelijk de parameter NetworkLocation plaatst, [!DNL Insight] lost gemeenschappelijke namen door deze netwerkplaats op.

* NetworkLocation 2 is de [!DNL Insight Server] netwerkplaats. Wanneer zij in een cluster [!DNL Insight Servers] werken, gebruiken zij deze netwerkplaats om gemeenschappelijke namen voor inter-servermededeling op te lossen.

* NetworkLocation 3 is de het netwerkplaats van de [!DNL Report] Server. Als u niet uitdrukkelijk de parameter NetworkLocation plaatst, [!DNL Report] lost gemeenschappelijke namen door deze netwerkplaats op.

## Om het Dossier van het Adres te vormen {#section-10caab9854a244e39b09071946f7bd27}

De volgende procedure beschrijft hoe te om het adresdossier te vormen om een netwerkplaats (of netwerkplaatsen) voor uw te bepalen [!DNL Insight Server].

1. Navigeer naar de [!DNL Addresses] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server] (bijvoorbeeld [!DNL C:\Adobe\Server\Addresses)].

1. Zoek het [!DNL server.address] bestand en wijzig de naam van dit bestand in de algemene naam van de server. Als de algemene naam bijvoorbeeld [!DNL server.mycompany.com]is, wordt de naam van het bestand gewijzigd [!DNL server.mycompany.com.address].

1. Open het hernoemde bestand in een teksteditor, zoals Kladblok.
1. Bewerk NetworkLocation 0 om de algemene naam en het IP-adres van het netwerk op te geven, [!DNL Insight Server] zoals hieronder wordt weergegeven. Als uw server veelvoudige IP adressen heeft, gebruik NetworkLocation 0 om het IP van de server adres op het lokale, niet routable netwerk (bijvoorbeeld, zijn plaats op het interne netwerk) te specificeren.

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
   <td colname="col2"> <p>Het numerieke IP adres van de <span class="keyword"> </span> machine van de Server van het Inzicht. </p> <p>Voorbeeld: 192 168 124 176 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Algemene naam </i> </td> 
   <td colname="col2"> <p>De algemene naam die aan het digitale certificaat voor de Server van het <span class="keyword"> Inzicht wordt toegewezen </span>. </p> <p>Voorbeeld: <span class="filepath"> server.mijnbedrijf.com </span></p> <p>Opmerking: Zorg ervoor dat u deze naam precies zo typt als op het certificaat wordt weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Naam netwerklocatie </i> </td> 
   <td colname="col2"> <p>De naam u aan de inzameling van gemeenschappelijke namen en IP adressen wilt toewijzen die dit NetworkLocation vertegenwoordigt. De naam moet uniek zijn in het adresbestand. </p> <p>Voorbeeld: Bedrijfsintranet </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Als uw [!DNL Insight Server] extra IP adressen heeft, creeer een extra NetworkLocation voor elk adres. (Een gemakkelijke manier om dit te doen is een exemplaar van NetworkLocation te maken u hierboven creeerde en het IP adres in het exemplaar bij te werken.)

   U kunt nieuwe NetworkLocation aan het eind van het adresdossier toevoegen of het tussen bestaande definities opnemen NetworkLocation. (De positie van een NetworkLocation binnen het adresdossier is niet significant; nochtans, worden [!DNL Insight], [!DNL Insight Server], en [!DNL Report] Server NetworkLocations typisch geplaatst aan het eind van het dossier.)

   Nadat u noodzakelijke NetworkLocations hebt toegevoegd, doe het volgende de punten in het dossier opnieuw nummeren:

   1. Werk het puntaantal voor de structuur van Plaatsen bij om het totale aantal definities NetworkLocation in het dossier aan te passen. Bijvoorbeeld, als uw dossier vier definities NetworkLocation bevat, zou de lijn van Plaatsen als volgt kijken:

      ```
      Locations = vector: 4 items
      ```

   1. Werk de NetworkLocation puntaantallen bij zodat NetworkLocations achtereenvolgens (die van 0 beginnen) worden genummerd.
   Een voorbeeld van een adresdossier dat een [!DNL Insight Server] met twee IP adressen bepaalt, zie het voorbeeld in deze sectie.

1. In de het netwerkplaatsen van de [!DNL Insight] Server en [!DNL Report] Server, geef de parameter van de Ouder zoals hieronder getoond uit om de naam van NetworkLocation te specificeren die [!DNL Insight] en [!DNL Report] gebruik als hun standaardnetwerkplaatsen. (Zie het voorbeeld in deze sectie voor een voorbeeld van hoe de parameter Bovenliggend eruitziet wanneer deze is geconfigureerd.)

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

   Als uw één enkel IP adres [!DNL Insight Server] heeft en, daarom, slechts één NetworkLocation heeft, richt de parameter van de Ouder aan die NetworkLocation. Als uw veelvoudige IP adressen [!DNL Insight Server] heeft, richt de parameter van de Ouder aan NetworkLocation die het adres bepaalt waaraan uw [!DNL Insight] en [!DNL Report] cliënten het vaakst verbinden.

1. In de [!DNL Insight Server] netwerkplaats, geef de parameter van de Ouder zoals hieronder getoond uit om aan NetworkLocation te richten die de server gebruikt om gemeenschappelijke namen van andere op te lossen [!DNL Insight Servers] wanneer het in een cluster werkt. (Hoewel deze netwerkplaats niet wordt gebruikt tenzij een netwerk in een cluster [!DNL Insight Server] werkt, is het een goede praktijk, zelfs in één enkele serverconfiguratie, om de parameter van de Ouder aan een netwerkplaats te richten die het interne IP van de server adres. identificeert)

   ```
   2 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Insight Server 
     Parent = string: ServerDefaultNetworkLocation
   ```

In het volgende voorbeeld wordt een voltooid adresbestand getoond. Dit bestand definieert vijf netwerklocaties.

* De punten 0 en 1 van NetworkLocation bepalen netwerkplaatsen genoemd &quot;MyCorporateIntranet&quot;en &quot;Internet.&quot; Deze netwerklocaties definiëren twee verschillende IP-adressen voor een server met de naam [!DNL VS01.myCompany.com].
* NetworkLocation punt 2 is de [!DNL Insight] netwerkplaats. Dit is de standaardnetwerklocatie die door wordt gebruikt [!DNL Insight]. In dit voorbeeld, erft de [!DNL Insight] netwerkplaats zijn AddressDefinitions van &quot;Internet&quot;NetworkLocation.

* NetworkLocation punt 3 is de [!DNL Insight Server] netwerkplaats. Dit is de standaardnetwerklocatie die [!DNL Insight Server] wordt gebruikt wanneer deze communiceert met andere servers in een cluster. In dit voorbeeld, erft de [!DNL Insight Server] netwerkplaats zijn AddressDefinitions van &quot;MyCorporate Intranet&quot;NetworkLocation.

* NetworkLocation punt 4 is de het netwerkplaats van de [!DNL Report] Server. Dit is de standaardnetwerklocatie die door wordt gebruikt [!DNL Report]. In dit voorbeeld, erft de het netwerkplaats van de [!DNL Report] Server zijn AddressDefinitions van &quot;Internet&quot;NetworkLocation.

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


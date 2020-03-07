---
description: Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd bevat vier vooraf bepaalde netwerkplaatsen.
solution: Insight
title: Het adresdossier dat op de Server van het Inzicht wordt geïnstalleerd
uuid: a58d36d8-e1a3-43e7-91c5-c57351e1be49
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

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
* NetworkLocation 1 is de [!DNL Insight] netwerkplaats. Als u niet uitdrukkelijk de parameter NetworkLocation plaatst, lost gemeenschappelijke namen door deze netwerkplaats op, [!DNL Insight] die.

* NetworkLocation 2 is de [!DNL Insight Server] netwerkplaats. Wanneer [!DNL Insight Servers] werken in een cluster, gebruiken zij deze netwerkplaats om gemeenschappelijke namen voor inter-servermededeling op te lossen.

* NetworkLocation 3 is de het netwerkplaats van de [!DNL Report] Server. Als u niet uitdrukkelijk de parameter NetworkLocation plaatst, lost gemeenschappelijke namen door deze netwerkplaats op, [!DNL Report] die.

## Om het Dossier van het Adres te vormen {#section-10caab9854a244e39b09071946f7bd27}

De volgende procedure beschrijft hoe te om het adresdossier te vormen om een netwerkplaats (of netwerkplaatsen) voor uw te bepalen [!DNL Insight Server].

1. Navigeer aan de [!DNL Addresses] omslag in de folder waar u installeerde [!DNL Insight Server] (bijvoorbeeld, [!DNL C:\Adobe\Server\Addresses)].

1. Bepaal de plaats van het [!DNL server.address] dossier en noem dit dossier anders om op de gemeenschappelijke naam van de server te wijzen. Bijvoorbeeld, als de gemeenschappelijke naam was [!DNL server.mycompany.com], zou u het dossier anders noemen [!DNL server.mycompany.com.address].

1. Open het anders genoemde dossier in een tekstredacteur zoals Blocnote.
1. Geef NetworkLocation 0 uit om de gemeenschappelijke naam en IP adres van [!DNL Insight Server] zoals hieronder getoond te specificeren. Als uw server veelvoudige IP adressen heeft, gebruik NetworkLocation 0 om het IP van de server adres op het lokale, niet routable netwerk (bijvoorbeeld, zijn plaats op het interne netwerk) te specificeren.

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
   <th colname="col2" class="entry"> Specificeren </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>IP-adres</i> </td> 
   <td colname="col2"> <p>Het numerieke IP adres van de <span class="keyword"> machine van de Server van het Inzicht </span> is. </p> <p>Voorbeeld: 192 168 124 176 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Algemene naam </i> </td> 
   <td colname="col2"> <p>De gemeenschappelijke naam die aan het digitale certificaat voor de Server van het <span class="keyword"> Inzicht wordt toegewezen </span>. </p> <p>Voorbeeld: <span class="filepath"> server.mycompany.com </span></p> <p>Opmerking: Ben zeker om deze naam precies te typen aangezien het op het certificaat verschijnt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Naam netwerklocatie </i> </td> 
   <td colname="col2"> <p>De naam u aan de inzameling van gemeenschappelijke namen en IP adressen wilt toewijzen die dit NetworkLocation vertegenwoordigt. De naam moet binnen het adresdossier uniek zijn. </p> <p>Voorbeeld: Bedrijfsintranet </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Als uw extra IP adressen [!DNL Insight Server] heeft, creeer een extra NetworkLocation voor elk adres. (Een gemakkelijke manier om dit te doen is een exemplaar van NetworkLocation te maken u hierboven creeerde en het IP adres in het exemplaar bij te werken.)

   U kunt nieuwe NetworkLocation aan het eind van het adresdossier toevoegen of het tussen bestaande definities opnemen NetworkLocation. (De positie van een NetworkLocation binnen het adresdossier is niet significant; nochtans, worden de [!DNL Insight], [!DNL Insight Server], en [!DNL Report] Server NetworkLocations typisch geplaatst aan het eind van het dossier.)

   Nadat u noodzakelijke NetworkLocations hebt toegevoegd, doe het volgende de punten in het dossier hernummeren:

   1. Werk de punttelling voor de structuur van Plaatsen bij om het totale aantal definities NetworkLocation in het dossier aan te passen. Bijvoorbeeld, als uw dossier vier definities NetworkLocation bevat, zou de lijn van Plaatsen als volgt kijken:

      ```
      Locations = vector: 4 items
      ```

   1. Werk de het puntaantallen bij NetworkLocation zodat NetworkLocations achtereenvolgens (beginnend van 0) worden genummerd.
   Bij een voorbeeld van een adresdossier dat [!DNL Insight Server] met twee IP adressen bepaalt, zie het voorbeeld in deze sectie.

1. In de het netwerkplaatsen [!DNL Insight] en van de [!DNL Report] Server, geef de parameter van de Ouder zoals hieronder getoond uit om de naam van NetworkLocation te specificeren die [!DNL Insight] en als hun standaardnetwerkplaatsen [!DNL Report] gebruiken. (Bij een voorbeeld van wat de parameter van de Ouder als kijkt wanneer het wordt gevormd, zie het voorbeeld in deze sectie.)

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

1. In de [!DNL Insight Server] netwerkplaats, geef de parameter van de Ouder zoals hieronder getoond uit om aan NetworkLocation te richten die de server gebruikt om gemeenschappelijke namen van andere op te lossen [!DNL Insight Servers] wanneer het in een cluster werkt. (Hoewel deze netwerkplaats niet wordt gebruikt tenzij een [!DNL Insight Server] werkt in een cluster, is het een goede praktijk, zelfs in één enkele serverconfiguratie, om de parameter van de Ouder aan een netwerkplaats te richten die het interne IP van de server adres. identificeert)

   ```
   2 = NetworkLocation:  
     Addresses = vector: 0 items 
     Name = string: Insight Server 
     Parent = string: ServerDefaultNetworkLocation
   ```

Het volgende voorbeeld toont een voltooid adresdossier. Dit dossier bepaalt vijf netwerkplaatsen.

* De punten 0 en 1 van NetworkLocation bepalen netwerkplaatsen genoemd &quot;MyCorporateIntranet&quot;en &quot;Internet.&quot; Deze netwerkplaatsen bepalen twee verschillende IP adressen voor een server genoemd [!DNL VS01.myCompany.com].
* NetworkLocation punt 2 is de [!DNL Insight] netwerkplaats. Dit is de standaardnetwerkplaats die door wordt gebruikt [!DNL Insight]. In dit voorbeeld, erft de [!DNL Insight] netwerkplaats zijn AddressDefinitions van &quot;Internet&quot;NetworkLocation.

* NetworkLocation punt 3 is de [!DNL Insight Server] netwerkplaats. Dit is het gebruik van de standaardnetwerkplaats [!DNL Insight Server] wanneer het met andere servers in een cluster communiceert. In dit voorbeeld, erft de [!DNL Insight Server] netwerkplaats zijn AddressDefinitions van het &quot;MyCorporate Intranet&quot;NetworkLocation.

* NetworkLocation punt 4 is de het netwerkplaats van de [!DNL Report] Server. Dit is de standaardnetwerkplaats die door wordt gebruikt [!DNL Report]. In dit voorbeeld, erft de het netwerkplaats van de [!DNL Report] Server AddressDefinitions van &quot;Internet&quot;NetworkLocation.

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


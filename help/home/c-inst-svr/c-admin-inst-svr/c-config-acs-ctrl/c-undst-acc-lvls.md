---
description: Toegangsniveaus beschrijven welke URI's op de computer een groep gebruikers mag lezen of wijzigen.
title: Toegangsniveaus
uuid: e9091ae1-9a34-4e00-a928-20d04119ee9e
exl-id: 64e2dc39-1ca1-425b-bec7-acb10a8819c0
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---

# Toegangsniveaus begrijpen{#understanding-access-levels}

Toegangsniveaus beschrijven welke URI&#39;s op de computer een groep gebruikers mag lezen of wijzigen.

Volg deze richtlijnen om toegangsniveaus te bepalen zoals gewenst voor de gebruikers van uw organisatie:

* Specifieke URI&#39;s zonder slash-teken beperken alleen de toegang tot die URI. [!DNL /Components/Communications.cfg] biedt bijvoorbeeld alleen toegang tot het [!DNL Communications.cfg]bestand.

* Een slash (/) die aan het einde van een map aangeeft, geeft groepsleden toegang tot elke URI die met die tekenreeks begint. /Profiles/ biedt bijvoorbeeld toegang tot de gehele map Profielen.
* Een navolgend dollarsymbool ($) beperkt toegang tot nauwkeurige URI slechts, zelfs als het een folder is. /Profiles/$ biedt bijvoorbeeld toegang om de hoofdmap Profielen te lezen, maar niet om bestanden in die map te lezen.

   Voor toegang tot specifieke bestanden hoeft u geen navolgende $ te gebruiken.

   [!DNL /Components/Communications.cfg] en [!DNL /Components/Communications.cfg$] bieden bijvoorbeeld dezelfde toegang.

* Een percentagesymbool (%) kan met CN (Gemeenschappelijke Naam) worden gebruikt om toegang toe te staan. /Users/%CN%/ staat bijvoorbeeld toegang toe tot de gebruikersmap die overeenkomt met de algemene naam van het SSL-certificaat van de [!DNL Insight]-gebruiker. Deze syntaxis kan slechts eenmaal worden gebruikt in een URI.

URIs in de vooraf bepaalde groepen van de toegangscontrole is gevormd als volgt:

<table id="table_8E6FDD741BF24E2DAD96A2919FAE6C7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Groepsnaam </th> 
   <th colname="col2" class="entry"> Alleen-lezen toegang </th> 
   <th colname="col3" class="entry"> Leesschrijftoegang </th> 
   <th colname="col4" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Beheerders </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/ </p> </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot alle <span class="keyword"> folders van de Server van het Inzicht</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sensoren </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/SensorInit.vsp </p> <p>/Submit.vsp </p> </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot de twee dossiers die <span class="wintitle"> Sensors</span> gebruiken om met <span class="keyword"> de Server van het Inzicht te communiceren</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikers </p> </td> 
   <td colname="col2"> <p>/Profielen/ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> /Users/%CN%/ </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot de folder van de Gebruiker die de SSL gemeenschappelijke naam van het certificaat van <span class="keyword"> Insight</span> - gebruiker aanpassen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Energiegebruikers </p> </td> 
   <td colname="col2"> <p>/Profielen/$ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> <p>/Profielen/ </p> <p>/Users/%CN%/ </p> </td> 
   <td colname="col4"> <p>De Gebruikers van de macht worden toegestaan de zelfde toegang zoals Gebruikers, met de toegevoegde capaciteit om aan de folder van Profielen te schrijven. Deze gebruikers kunnen profielen bewerken en ervoor zorgen dat wijzigingen automatisch worden bijgewerkt voor andere <span class="keyword"> Insight</span>-gebruikers, zoals bij het verspreiden van nieuw gedefinieerde werkruimten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Clusterservers </p> </td> 
   <td colname="col2"> <p>/Components for Processing Servers/ </p> <p>/Adressen/ </p> <p>/Profielen/ </p> <p>/Lookups/ </p> <p>/Access Control/ </p> <p>/Bin/ </p> <p>/Logboeken/ </p> </td> 
   <td colname="col3"> <p>/Cluster/ </p> </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot de folder van de Cluster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportservers </p> </td> 
   <td colname="col2"> <p>/Profielen/$ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> <p>/Profielen/ </p> <p>/Users/%CN%/ </p> <p>/ReportStatus.vsp </p> </td> 
   <td colname="col4"> <p>Rapportcomputers hebben dezelfde toegang als Power Users, met de toegevoegde mogelijkheid om naar het bestand <span class="filepath"> ReportStatus.vsp</span> te schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Toegangsbeheer configureren**

Wanneer het bepalen van toegangsbeheergroepen, moet u alle Beheerders van het Systeem, gebruikers, clusterservers, en gebruikers van de Server van het Rapport omvatten die toegang tot deze [!DNL Insight Server] computer vereisen. U kunt toegang verlenen gebruikend IP adres of SSL certificaatinformatie, zoals de gemeenschappelijke naam of organisatie.

>[!NOTE]
>
>Wanneer het [!DNL Access Control.cfg] dossier op [!DNL Insight Server] wordt veranderd, worden alle bestaande verbindingen geëindigd en gedwongen om opnieuw aan te sluiten. De verbindingen worden gecontroleerd tegen de toestemmingen in het bijgewerkte [!DNL Access Control.cfg] dossier. In de interface van de Manager van Servers, wordt het [!DNL Insight Server] pictogram tijdelijk rood en dan groen opnieuw omdat de verbinding wordt geëindigd en gedwongen om samen met alle anderen opnieuw aan te sluiten.

1. Klik op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van de [!DNL Insight Server] die u wilt configureren en klik op **[!UICONTROL Files]**.

1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Access Control]** om de inhoud ervan weer te geven. Het [!DNL Access Control.cfg]-bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* voor [!DNL Access Control.cfg] en klik op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Access Control.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**.

1. Klik in het venster [!DNL Access Control.cfg] op **[!UICONTROL Access Control Groups]** om de inhoud ervan weer te geven.

   ![](assets/access_ctrl_cfg.png)

1. Een nieuwe toegangsbeheergroep toevoegen:

   1. Klik met de rechtermuisknop **[!UICONTROL Access Control Groups]** en klik **[!UICONTROL Add new]** > **[!UICONTROL Group]**.

   1. Klik met de rechtermuisknop **[!UICONTROL Members]** en klik **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

      De leden voor de standaardgroepen zijn niet vooraf gedefinieerd. Door gebrek, wordt de toegang van de Beheerder verleend aan 127.0.0.1 (lokale gastheer), en [!DNL Sensor] toegang wordt verleend aan IP:*. Alle andere leden van de toegangsbeheergroep moeten worden bepaald.

   1. Voltooi de parameters.

1. Om nieuwe leden aan een bestaande toegangsbeheergroep toe te voegen:

   1. Klik **[!UICONTROL Members]** onder de aangewezen toegangsbeheergroep met de rechtermuisknop aan en klik **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

1. Sla het bestand op door met de rechtermuisknop op **[!UICONTROL (modified)]** boven in het venster te klikken en vervolgens op **[!UICONTROL Save]** te klikken.

1. Als u de lokaal aangebrachte wijzigingen in de [!DNL Insight Server]-computer wilt opslaan, klikt u in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor [!DNL Access Control.cfg] in de [!DNL Temp]-kolom en klikt u vervolgens op **[!UICONTROL Save to]** *&lt;**[!UICONTROL server name]**>*.

---
description: Toegangsniveaus beschrijven welke URI's op de computer een groep gebruikers mag lezen of wijzigen.
title: Toegangsniveaus
uuid: e9091ae1-9a34-4e00-a928-20d04119ee9e
exl-id: 64e2dc39-1ca1-425b-bec7-acb10a8819c0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---

# Toegangsniveaus{#understanding-access-levels}

{{eol}}

Toegangsniveaus beschrijven welke URI&#39;s op de computer een groep gebruikers mag lezen of wijzigen.

Volg deze richtlijnen om toegangsniveaus te bepalen zoals gewenst voor de gebruikers van uw organisatie:

* Specifieke URI&#39;s zonder slash-teken beperken alleen de toegang tot die URI. Bijvoorbeeld: [!DNL /Components/Communications.cfg] verleent toegang tot [!DNL Communications.cfg]alleen bestand.

* Een slash (/) die aan het einde van een map aangeeft, geeft groepsleden toegang tot elke URI die met die tekenreeks begint. /Profiles/ biedt bijvoorbeeld toegang tot de gehele map Profielen.
* Een navolgend dollarsymbool ($) beperkt toegang tot nauwkeurige URI slechts, zelfs als het een folder is. /Profiles/$ biedt bijvoorbeeld toegang om de hoofdmap Profielen te lezen, maar niet om bestanden in die map te lezen.

   Voor toegang tot specifieke bestanden hoeft u geen navolgende $ te gebruiken.

   Bijvoorbeeld: [!DNL /Components/Communications.cfg] en [!DNL /Components/Communications.cfg$] dezelfde toegang verlenen.

* Een percentagesymbool (%) kan met CN (Gemeenschappelijke Naam) worden gebruikt om toegang toe te staan. /Users/%CN%/ staat bijvoorbeeld toegang toe tot de gebruikersmap die overeenkomt met de algemene naam van het SSL-certificaat van de [!DNL Insight] gebruiker. Deze syntaxis kan slechts eenmaal worden gebruikt in een URI.

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
   <td colname="col4"> <p>Toegang tot iedereen lezen en schrijven <span class="keyword"> Insight Server</span> directory's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sensoren </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/SensorInit.vsp </p> <p>/Submit.vsp </p> </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot de twee dossiers die <span class="wintitle"> Sensoren</span> gebruiken om te communiceren met de <span class="keyword"> Insight Server</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikers </p> </td> 
   <td colname="col2"> <p>/Profielen/ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> /Users/%CN%/ </td> 
   <td colname="col4"> <p>U kunt toegang lezen en schrijven naar de gebruikersmap die overeenkomt met de algemene naam van het SSL-certificaat van de <span class="keyword"> Inzicht</span> gebruiker. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Energiegebruikers </p> </td> 
   <td colname="col2"> <p>/Profielen/$ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> <p>/Profielen/ </p> <p>/Users/%CN%/ </p> </td> 
   <td colname="col4"> <p>De Gebruikers van de macht worden toegestaan de zelfde toegang zoals Gebruikers, met de toegevoegde capaciteit om aan de folder van Profielen te schrijven. Deze gebruikers kunnen profielen bewerken en wijzigingen automatisch laten bijwerken voor andere <span class="keyword"> Inzicht</span> gebruikers, zoals bij het verspreiden van nieuw gedefinieerde werkruimten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Clusterservers </p> </td> 
   <td colname="col2"> <p>/Components for Processing Servers/ </p> <p>/Adressen/ </p> <p>/Profielen/ </p> <p>/Lookups/ </p> <p>/Toegangsbeheer/ </p> <p>/Bin/ </p> <p>/Logboeken/ </p> </td> 
   <td colname="col3"> <p>/Cluster/ </p> </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot de folder van de Cluster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportservers </p> </td> 
   <td colname="col2"> <p>/Profielen/$ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> <p>/Profielen/ </p> <p>/Users/%CN%/ </p> <p>/ReportStatus.vsp </p> </td> 
   <td colname="col4"> <p>Rapportcomputers hebben dezelfde toegang als Power Users, met de extra mogelijkheid om naar de <span class="filepath"> ReportStatus.vsp</span> bestand. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Toegangsbeheer configureren**

Wanneer het bepalen van toegangsbeheergroepen, moet u alle Beheerders van het Systeem, gebruikers, clusterservers, en de gebruikers van de Server van het Rapport omvatten die toegang tot dit vereisen [!DNL Insight Server] computer. U kunt toegang verlenen gebruikend IP adres of SSL certificaatinformatie, zoals de gemeenschappelijke naam of organisatie.

>[!NOTE]
>
>Wanneer de [!DNL Access Control.cfg] bestand is gewijzigd op [!DNL Insight Server], worden alle bestaande verbindingen beëindigd en gedwongen om opnieuw aan te sluiten. De verbindingen worden gecontroleerd tegen de toestemmingen in bijgewerkte [!DNL Access Control.cfg] bestand. In de interface van de Manager van Servers, [!DNL Insight Server] het pictogram wordt tijdelijk rood en vervolgens weer groen omdat de verbinding wordt verbroken en samen met alle andere gebruikers opnieuw moet worden verbonden.

1. Op de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van het dialoogvenster [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Files]**.

1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Access Control]** om de inhoud te bekijken. De [!DNL Access Control.cfg] bestand bevindt zich in deze map.

1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom voor [!DNL Access Control.cfg] en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Access Control.cfg].

1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**.

1. In de [!DNL Access Control.cfg] venster, klikt u op **[!UICONTROL Access Control Groups]** om de inhoud te bekijken.

   ![](assets/access_ctrl_cfg.png)

1. Een nieuwe toegangsbeheergroep toevoegen:

   1. Klikken met rechtermuisknop **[!UICONTROL Access Control Groups]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Group]**.

   1. Klikken met rechtermuisknop **[!UICONTROL Members]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

      De leden voor de standaardgroepen zijn niet vooraf gedefinieerd. Standaard heeft de beheerder toegang tot 127.0.0.1 (lokale host), en [!DNL Sensor] toegang wordt verleend aan IP:&#42;. Alle andere leden van de toegangsbeheergroep moeten worden bepaald.

   1. Voltooi de parameters.

1. Om nieuwe leden aan een bestaande toegangsbeheergroep toe te voegen:

   1. Klikken met rechtermuisknop **[!UICONTROL Members]** onder de betreffende toegangsbeheergroep en klik op **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

1. Sla het bestand op door met de rechtermuisknop te klikken **[!UICONTROL (modified)]** boven aan het venster en klik vervolgens op **[!UICONTROL Save]**.

1. Als u de lokaal aangebrachte wijzigingen wilt opslaan in het dialoogvenster [!DNL Insight Server] in de [!DNL Server Files Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL Access Control.cfg] in de [!DNL Temp] kolom, klik vervolgens op **[!UICONTROL Save to]** *&lt;**[!UICONTROL server name]**>*.

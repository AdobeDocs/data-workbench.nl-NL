---
description: De niveaus van de toegang beschrijven welke URIs op de machine een groep gebruikers wordt toegelaten om te lezen of te wijzigen.
solution: Insight
title: Het begrip van de Niveaus van de Toegang
uuid: e9091ae1-9a34-4e00-a928-20d04119ee9e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het begrip van de Niveaus van de Toegang{#understanding-access-levels}

De niveaus van de toegang beschrijven welke URIs op de machine een groep gebruikers wordt toegelaten om te lezen of te wijzigen.

Volg deze richtlijnen om toegangsniveaus te bepalen zoals die voor de gebruikers van uw organisatie worden gewenst:

* Specifieke URIs zonder het slepen schuine streepkarakter beperkt toegang tot dat URI slechts. Bijvoorbeeld, [!DNL /Components/Communications.cfg] verleent toegang tot het slechts [!DNL Communications.cfg]dossier.

* Een het slepen schuine streep (/), die een folder specificeert, verleent groepsleden toegang tot om het even welk URI die met dat koord begint. Bijvoorbeeld, verstrekt /Profiles/ toegang tot de volledige folder van Profielen.
* Een het slepen dollarteken ($) beperkt toegang tot nauwkeurige URI slechts, zelfs als het een folder is. Bijvoorbeeld, verstrekt /Profiles/$ toegang om de belangrijkste folder van Profielen te lezen, maar geen dossiers binnen die folder te lezen.

   Voor toegang tot specifieke dossiers, te hoeven u niet om geen het slepen $ te gebruiken.

   Bijvoorbeeld, [!DNL /Components/Communications.cfg] en [!DNL /Components/Communications.cfg$] verstrek de zelfde toegang.

* Een percentensymbool (%) kan met CN (Gemeenschappelijke Naam) worden gebruikt om toegang toe te laten. Bijvoorbeeld, /Users/%CN%/ staat toegang tot de folder van de Gebruiker toe die de SSL certificaat gemeenschappelijke naam van de [!DNL Insight] gebruiker aanpast. Merk op dat deze syntaxis slechts één keer in URI kan worden gebruikt.

URIs in de vooraf bepaalde toegangsbeheergroepen is gevormd als volgt:

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
   <td colname="col1"> <p>Administrateurs </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/ </p> </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot alle <span class="keyword"> folders van de Server</span> van het Inzicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sensoren </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>/SensorInit.vsp </p> <p>/Submit.vsp </p> </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot de twee dossiers die de <span class="wintitle"> Sensoren</span> om met de Server <span class="keyword"> van het</span>Inzicht gebruiken te communiceren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikers </p> </td> 
   <td colname="col2"> <p>/Profielen/ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> /Users/%CN%/ </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot de folder van de Gebruiker die de SSL certificaat gemeenschappelijke naam van de gebruiker van het <span class="keyword"> Inzicht</span> aanpassen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Energiegebruikers </p> </td> 
   <td colname="col2"> <p>/Profielen/$ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> <p>/Profielen/ </p> <p>/Users/%CN%/ </p> </td> 
   <td colname="col4"> <p>De Gebruikers van de macht worden toegestaan de zelfde toegang zoals Gebruikers, met de toegevoegde capaciteit om aan de folder van Profielen te schrijven. Deze gebruikers kunnen profielen uitgeven en veranderingen toelaten om automatisch voor andere gebruikers van het <span class="keyword"> Inzicht</span> , zoals wanneer het verdelen van pas bepaalde werkruimten worden bijgewerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Clusterservers </p> </td> 
   <td colname="col2"> <p>/Components for Processing Servers/ </p> <p>/Adressen/ </p> <p>/Profielen/ </p> <p>/Lookups/ </p> <p>/Access Control/ </p> <p>/Bin/ </p> <p>/logs/ </p> </td> 
   <td colname="col3"> <p>/Cluster/ </p> </td> 
   <td colname="col4"> <p>Lees en schrijf toegang tot de folder van de Cluster. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportservers </p> </td> 
   <td colname="col2"> <p>/Profielen/$ </p> <p>/Status/ </p> <p>/Software/ </p> <p>/Adressen/ </p> <p>/Users/$ </p> </td> 
   <td colname="col3"> <p>/Profielen/ </p> <p>/Users/%CN%/ </p> <p>/ReportStatus.vsp </p> </td> 
   <td colname="col4"> <p>De machines van het rapport worden toegestaan de zelfde toegang zoals de Gebruikers van de Macht, met de toegevoegde capaciteit om aan het <span class="filepath"> ReportStatus.vsp</span> - dossier te schrijven. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Om toegangsbeheer te vormen**

Wanneer het bepalen van toegangsbeheergroepen, moet u alle Beheerders van het Systeem, gebruikers, clusterservers, en de gebruikers van de Server van het Rapport omvatten die toegang tot deze [!DNL Insight Server] computer vereisen. U kunt toegang verlenen gebruikend IP adres of SSL certificaatinformatie, zoals de gemeenschappelijke naam of de organisatie.

>[!NOTE]
>
>Wanneer het [!DNL Access Control.cfg] dossier wordt veranderd [!DNL Insight Server], worden alle bestaande verbindingen geëindigd en gedwongen om opnieuw aan te sluiten. De verbindingen worden gecontroleerd tegen de toestemmingen in het bijgewerkte [!DNL Access Control.cfg] dossier. In de interface van de Manager van Servers, wordt het [!DNL Insight Server] pictogram tijdelijk rood en dan groen opnieuw omdat de verbinding wordt geëindigd en gedwongen om samen met alle anderen opnieuw aan te sluiten.

1. Voor het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.

1. Klik het pictogram van het pictogram met de rechtermuisknop aan [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Files]**.

1. In [!DNL Server Files Manager], klik **[!UICONTROL Access Control]** om zijn inhoud te bekijken. Het [!DNL Access Control.cfg] dossier wordt gevestigd binnen deze folder.

1. Klik het vinkje in de kolom van de *servernaam* voor met de rechtermuisknop aan [!DNL Access Control.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Access Control.cfg].

1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Workstation]**.

1. In het [!DNL Access Control.cfg] venster, klik **[!UICONTROL Access Control Groups]** om zijn inhoud te bekijken.

   ![](assets/access_ctrl_cfg.png)

1. Om een nieuwe toegangsbeheergroep toe te voegen:

   1. Klik met de rechtermuisknop **[!UICONTROL Access Control Groups]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Group]**.

   1. Klik met de rechtermuisknop **[!UICONTROL Members]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

      De leden voor de standaardgroepen zijn niet vooraf bepaald. Door gebrek, wordt de toegang van de Beheerder verleend aan 127.0.0.1 (lokale gastheer), en de [!DNL Sensor] toegang wordt verleend aan IP:*. Alle andere leden van de toegangsbeheergroep moeten worden bepaald.

   1. Voltooi de parameters.

1. Om nieuwe leden aan een bestaande toegangsbeheergroep toe te voegen:

   1. Klik **[!UICONTROL Members]** onder de aangewezen toegangsbeheergroep met de rechtermuisknop aan en klik **[!UICONTROL Add new]** > **[!UICONTROL Member]**.

1. Sparen het dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en dan te klikken **[!UICONTROL Save]**.

1. Als u de lokaal aangebrachte wijzigingen in het [!DNL Insight Server] systeem wilt opslaan, klikt u in het [!DNL Server Files Manager]selectievakje met de rechtermuisknop op het vinkje voor [!DNL Access Control.cfg] in de [!DNL Temp] kolom en klikt u op **[!UICONTROL Save to]** &lt; *>**[!UICONTROL server name]***.


---
description: Als de netwerkfirewalls toegang tot de repeaterserver van de machines van het Inzicht niet verhinderen, kunt u een verbinding tussen de repeaterserver en Inzicht tot stand brengen zodat u de repeaterserver kunt leiden gebruikend Inzicht.
solution: Insight
title: Het creëren van een Verbinding tussen Inzicht en Repeater
uuid: dccce83a-8708-4763-a19a-64d905a9f624
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het creëren van een Verbinding tussen Inzicht en Repeater{#creating-a-connection-between-insight-and-repeater}

Als de netwerkfirewalls toegang tot de repeaterserver van de machines van het Inzicht niet verhinderen, kunt u een verbinding tussen de repeaterserver en Inzicht tot stand brengen zodat u de repeaterserver kunt leiden gebruikend Inzicht.

**Om een verbinding tussen[!DNL Insight]en de repeaterserver tot stand te brengen**

1. In [!DNL Insight], op het [!DNL Admin] lusje, klik de **[!UICONTROL Configure Connections to Servers]** duimnagel om de Configure Verbindingen aan de werkruimte van Servers te openen.
1. Klik in het [!DNL Insight.cfg] venster met de rechtermuisknop **[!UICONTROL Servers]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Server]**.
1. Voor de nieuwe server, voltooi de volgende parameters:

<table id="table_DD79587255134B5A888A0F57CF10E5B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Specificeren... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2">(Facultatief) de naam die u dit <span class="keyword"> Inzicht</span> wilt gebruiken om de repeaterserver in zijn gebruikersinterface te vertegenwoordigen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres </td> 
   <td colname="col2"> <p>De gastheernaam of het numerieke IP adres van uw repeaterserver. </p> <p>Voorbeeld: <span class="filepath"> Repeater.mycompany.com</span> of 192.168.1.90 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-clientcertificaat </td> 
   <td colname="col2"> <p>Facultatief tenzij u meer dan één certificaat hebt. De naam van het dossier dat het digitale certificaat voor dit exemplaar van <span class="keyword"> Inzicht</span>bevat. (Dit is het dossier dat u terwijl het installeren van <span class="keyword"> Inzicht</span>. downloadde) </p> <p>Voorbeeld: <span class="filepath"> Samantha Smith.pem</span></p> <p>Als u deze parameterspatie verlaat, gebruikt het <span class="keyword"> Inzicht</span> welk certificaat ook aanwezig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL-server </p> <p>Algemene naam </p> </td> 
   <td colname="col2">De gemeenschappelijke naam die aan de repeaterserver wordt toegewezen. Deze naam moet de gemeenschappelijke naam aanpassen die aan de repeaterserver binnen zijn vergunningscertificaat wordt toegewezen. Als u toegang tot het het certificaatdossier van de repeater (<span class="filepath"> Certificaten \ server_cert.pem</span>) hebt, kunt u de gemeenschappelijke naam vinden door het dossier met een tekstredacteur zoals Blocnote te openen. De gangbare naam wordt in het certificaat in het GN-veld vermeld. </td> 
  </tr> 
 </tbody> 
</table>

1. Sparen het dossier door **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Save]**. [!DNL Insight] zal proberen om met de repeaterserver te verbinden gebruikend de montages u hebt gespecificeerd. Als een verbinding wordt gevestigd, verschijnt een groen serverpictogram in de [!DNL Servers Manager] interface. Als een verbinding niet kan worden gevestigd, verschijnt een rood pictogram.

   Voor meer informatie over de [!DNL Servers Manager] interface, zie de * [!DNL Insight] Gids van de Gebruiker*.


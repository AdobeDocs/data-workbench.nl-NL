---
description: Als de netwerkfirewalls toegang tot de herhalingsserver van de machines van het Inzicht niet verhinderen, kunt u een verbinding tussen de repeaterserver en Inzicht tot stand brengen zodat u de herhalingsserver kunt beheren gebruikend Inzicht.
solution: Analytics
title: Het creëren van een Verbinding tussen Insight en Repeater
uuid: dccce83a-8708-4763-a19a-64d905a9f624
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# Het creëren van een Verbinding tussen Insight en Repeater{#creating-a-connection-between-insight-and-repeater}

Als de netwerkfirewalls toegang tot de herhalingsserver van de machines van het Inzicht niet verhinderen, kunt u een verbinding tussen de repeaterserver en Inzicht tot stand brengen zodat u de herhalingsserver kunt beheren gebruikend Inzicht.

**Verbinding maken tussen[!DNL Insight]en de herhalingsserver**

1. Klik op [!DNL Insight]het [!DNL Admin] tabblad op de **[!UICONTROL Configure Connections to Servers]** miniatuur om de werkruimte Verbindingen met servers configureren te openen.
1. Klik in het [!DNL Insight.cfg] venster met de rechtermuisknop **[!UICONTROL Servers]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Server]**.
1. Voer voor de nieuwe server de volgende parameters in:

<table id="table_DD79587255134B5A888A0F57CF10E5B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Opgeven... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2">(Optioneel) De naam die door dit <span class="keyword"> Insight</span> moet worden gebruikt om de herhalingsserver in de gebruikersinterface te vertegenwoordigen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres </td> 
   <td colname="col2"> <p>De hostnaam of het numerieke IP-adres van uw herhalingsserver. </p> <p>Voorbeeld: <span class="filepath"> Repeater.mijnbedrijf.com</span> of 192.168.1.90 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-clientcertificaat </td> 
   <td colname="col2"> <p>Optioneel, tenzij u meer dan één certificaat hebt. De naam van het bestand dat het digitale certificaat voor deze kopie van <span class="keyword"> Insight</span>bevat. (Dit is het bestand dat u hebt gedownload tijdens de installatie van <span class="keyword"> Insight</span>.) </p> <p>Voorbeeld: <span class="filepath"> Samantha Smith.pem</span></p> <p>Als u deze parameter leeg laat, gebruikt het <span class="keyword"> Inzicht</span> welk certificaat aanwezig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL-server </p> <p>Algemene naam </p> </td> 
   <td colname="col2">De algemene naam die aan de herhalingsserver is toegewezen. Deze naam moet overeenkomen met de algemene naam die is toegewezen aan de herhalingsserver in het licentiecertificaat. Als u toegang hebt tot het certificaatbestand van de repeater (<span class="filepath"> Certificates\server_cert.pem</span>), kunt u de algemene naam vinden door het bestand te openen met een teksteditor, zoals Kladblok. De algemene naam wordt vermeld in het GN-veld in het certificaat. </td> 
  </tr> 
 </tbody> 
</table>

1. Sla het bestand op door met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster te klikken en vervolgens te klikken **[!UICONTROL Save]**. [!DNL Insight] probeert verbinding te maken met de herhalingsserver met de instellingen die u hebt opgegeven. Als er een verbinding tot stand is gebracht, verschijnt er een groen serverpictogram in de [!DNL Servers Manager] interface. Als er geen verbinding kan worden gemaakt, verschijnt er een rood pictogram.

   Zie voor meer informatie over de [!DNL Servers Manager] interface de * [!DNL Insight] User Guide*.


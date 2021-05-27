---
description: Als de netwerkfirewalls toegang tot de herhalingsserver van de machines van het Inzicht niet verhinderen, kunt u een verbinding tussen de repeaterserver en Inzicht tot stand brengen zodat u de herhalingsserver kunt beheren gebruikend Inzicht.
title: Het creëren van een Verbinding tussen Insight en Repeater
uuid: dccce83a-8708-4763-a19a-64d905a9f624
exl-id: 81e81db5-0517-41d4-a958-d08cd3975096
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Het creëren van een Verbinding tussen Inzicht en Repeater{#creating-a-connection-between-insight-and-repeater}

Als de netwerkfirewalls toegang tot de herhalingsserver van de machines van het Inzicht niet verhinderen, kunt u een verbinding tussen de repeaterserver en Inzicht tot stand brengen zodat u de herhalingsserver kunt beheren gebruikend Inzicht.

**Verbinding maken tussen  [!DNL Insight] en de herhalingsserver**

1. Klik op [!DNL Insight] op het tabblad [!DNL Admin] op de miniatuur **[!UICONTROL Configure Connections to Servers]** om de werkruimte Verbindingen met servers configureren te openen.
1. Klik in het venster [!DNL Insight.cfg] met de rechtermuisknop **[!UICONTROL Servers]** en klik **[!UICONTROL Add new]** > **[!UICONTROL Server]**.
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
   <td colname="col2">(Optioneel) De naam die u met deze <span class="keyword"> Insight</span> wilt gebruiken om de herhalingsserver in de gebruikersinterface te vertegenwoordigen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Adres </td> 
   <td colname="col2"> <p>De hostnaam of het numerieke IP-adres van uw herhalingsserver. </p> <p>Voorbeeld: <span class="filepath"> Repeater.mijnbedrijf.com</span> of 192.168.1.90 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> SSL-clientcertificaat </td> 
   <td colname="col2"> <p>Optioneel, tenzij u meer dan één certificaat hebt. De naam van het bestand dat het digitale certificaat bevat voor deze kopie van <span class="keyword"> Insight</span>. (Dit is het bestand dat u hebt gedownload tijdens de installatie van <span class="keyword"> Insight</span>.) </p> <p>Voorbeeld: <span class="filepath"> Samantha Smith.pem</span></p> <p>Als u deze parameter leeg laat, <span class="keyword"> Insight</span> gebruikt welk certificaat aanwezig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SSL-server </p> <p>Algemene naam </p> </td> 
   <td colname="col2">De algemene naam die aan de herhalingsserver is toegewezen. Deze naam moet overeenkomen met de algemene naam die is toegewezen aan de herhalingsserver in het licentiecertificaat. Als u toegang hebt tot het certificaatbestand van de repeater (<span class="filepath"> Certificates\server_cert.pem</span>), kunt u de algemene naam vinden door het bestand te openen met een teksteditor zoals Kladblok. De algemene naam wordt vermeld in het GN-veld in het certificaat. </td> 
  </tr> 
 </tbody> 
</table>

1. Sla het bestand op door met de rechtermuisknop op **[!UICONTROL (modified)]** boven in het venster te klikken en op **[!UICONTROL Save]** te klikken. [!DNL Insight] probeert verbinding te maken met de herhalingsserver met de instellingen die u hebt opgegeven. Als een verbinding tot stand is gebracht, wordt een groen serverpictogram weergegeven in de [!DNL Servers Manager]-interface. Als er geen verbinding kan worden gemaakt, verschijnt er een rood pictogram.

   Voor meer informatie over de [!DNL Servers Manager] interface, zie * [!DNL Insight] Gids van de Gebruiker*.

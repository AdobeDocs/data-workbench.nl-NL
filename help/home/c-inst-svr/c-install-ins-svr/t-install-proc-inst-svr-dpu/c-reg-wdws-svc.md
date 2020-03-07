---
description: Procedure om de Server van het Inzicht te beginnen en het gelijktijdig te registreren als Dienst van Microsoft Windows.
solution: Insight
title: Insight Server registreren als Windows-service
uuid: 1b3d53ca-d50f-4520-abf5-6d5c40493b88
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# Insight Server registreren als Windows-service{#registering-insight-server-as-a-windows-service}

Procedure om de Server van het Inzicht te beginnen en het gelijktijdig te registreren als Dienst van Microsoft Windows.

>[!NOTE]
>
>Wanneer u [!DNL Insight Server] voor het eerst begint, verbindt het automatisch met de Server van de Vergunning van Adobe om uw digitaal certificaat te registreren. Als u het registratieproces wilt voltooien, moet uw computer zijn verbonden met internet wanneer u de volgende stappen uitvoert.

**Om het als Dienst van Vensters te beginnen[!DNL Insight Server]en te registreren**

1. Open een bevelherinnering en navigeer aan de baksubfolder in de omslag waar u installeerde [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\bin]

1. Bij de bevelherinnering, voer het volgende bevel uit om het te beginnen [!DNL Insight Server] en gelijktijdig te registreren om als dienst onder Microsoft Windows te lopen:

   ```
   <filepath>
   InsightServer64.exe /regserver 
   </filepath>
   ```

1. Om te bevestigen dat [!DNL Insight Server] correct loopt, klik **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. Deze bevelopeenvolging kan variëren afhankelijk van welke versie van Vensters u gebruikt.

   1. In de de dienstlijst, bepaal de plaats van de ingang voor **[!DNL Adobe Insight Server]** en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is.
   1. Sluit het de controlepaneel van de Diensten.

1. Om te controleren of er tijdens het opstarten fouten zijn [!DNL Insight Server] opgetreden, klikt u op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**. Deze bevelopeenvolging kan variëren afhankelijk van welke versie van Vensters u gebruikt.

   1. In de linkerruit van het [!DNL Event Viewer] venster, selecteer het **[!UICONTROL Application]** logboek.
   1. In de juiste ruit, zoek gebeurtenissen met &quot;Adobe&quot;in de [!DNL Source] kolom.
   1. Als u een fout van &quot;Adobe vindt,&quot;klik de fout tweemaal om het [!DNL Event Properties] venster te tonen. Dit venster verstrekt gedetailleerde informatie over de fout.

1. Wanneer u klaar bent met het onderzoeken van het [!DNL Applications] logboek, sluit de Kijker van de Gebeurtenis.

U hebt de installatie van voltooid [!DNL Insight Server]. [!DNL Insight Server] is ontworpen om ononderbroken te lopen. Als u het systeem opnieuw opstart, wordt het automatisch opnieuw [!DNL Insight Server] opgestart. Als u moet beginnen en [!DNL Insight Server] manueel ophouden, kunt u dit doen gebruikend het de controlepaneel van de Diensten in Vensters. Zoals beschreven in de volgende sectie, kunt u de [!DNL Insight Server] dienst naar keuze vormen om periodiek automatisch opnieuw te beginnen.

## De service configureren om automatisch opnieuw te starten {#section-f9bb91614513435f84ee55c0ec8edb13}

[!DNL Insight Server] is ontworpen om ononderbroken te blijven lopen. Het wordt typisch tegengehouden of begonnen slechts wanneer het uitvoeren van niet frequente taken zoals softwareverbeteringen of certificaatveranderingen of in het geval van bepaalde systeemfouten. Het is niet nodig om de [!DNL Insight Server] service tijdens normaal gebruik van het systeem te stoppen of opnieuw te starten; nochtans, kunt u de dienst vormen om periodiek (dagelijks, wekelijks, of maandelijks) opnieuw te beginnen om, bijvoorbeeld, de gebeurtenisberichten te ontruimen.

**Om de[!DNL Insight Server]dienst te vormen automatisch opnieuw te beginnen**

1. Navigeer aan de [!DNL Components] omslag in de folder waar u installeerde [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Gebruik een tekstredacteur zoals Blocnote om een nieuw geroepen dossier tot stand te brengen [!DNL ScheduledRestart.cfg].
1. Ga de volgende tekst in het [!DNL ScheduledRestart.cfg] dossier in:

   ```
   component = ScheduledRestart:  
     Start Time = string: Month DD, YYYY HH:MM:SS TZone 
     Restart Every = string: frequency
   ```

   <table id="table_AC05861E141E4928BE844C8611DEC43D"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Voor deze waarde... </th> 
      <th colname="col2" class="entry"> Specificeren </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <i>Maand DD, JJJJ UU:MM:SS TZone</i> </td> 
      <td colname="col2"> <p>De tijd wanneer u de Server van het <span class="keyword"> Inzicht voor het eerst opnieuw </span> wilt zijn begonnen. </p> <p>Voorbeeld: 13 augustus 2013 22:30:00 EST </p> <p> <p>Opmerking:  U moet een tijdzone specificeren. De tijdzone blijft niet in gebreke aan systeemtijd indien niet gespecificeerd. Als u wenst om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-verschuivend beleid uit te voeren, moet u het <span class="filepath"> .dst </span> - dossier bewaren dat de aangewezen regels in de Base\Dataset\Timezone directory on the <span class="keyword"> machine van de Server van het Inzicht bevat </span> . Voor een lijst van gesteunde afkortingen van de tijdzone en informatie over het uitvoeren van de Tijd van de Besparing van het Daglicht, zie de Codes van de <a href="../../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> Tijdzone </a>. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <i>frequentie</i> </td> 
      <td colname="col2"> <p>Één van de volgende waarden: 
       <ul id="ul_C29A40CD8FBB4333B5FA1D9E7DAD35EC"> 
       <li id="li_9FE07DD30C524CBB81C8F7968E7C733E">maand </li> 
       <li id="li_E5E1B97ED8FB43C0BDA496C620D24A4C">week </li> 
       <li id="li_E6043B382FAE4B5D85CAADDFA60E4902">dag </li> 
       </ul> </p> <p>Om op de frequentie te wijzen waarbij u de Server van het <span class="keyword"> </span> Inzicht na de aanvankelijke tijd wilt opnieuw worden begonnen die in de Tijd van het Begin wordt gespecificeerd. </p> <p>Bijvoorbeeld, als u de Server van het <span class="keyword"> </span> Inzicht één keer per week wilde opnieuw beginnen, zou u deze waarde aan "week plaatsen." </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Sla het [!DNL ScheduledRestart.cfg] bestand op.

   Verifieer dat het [!DNL ScheduledRestart.cfg] dossier in de [!DNL Components] omslag in de folder is waar u installeerde [!DNL Insight Server].

---
description: Procedure om de Server van het Inzicht te beginnen en het gelijktijdig als Dienst van Microsoft Windows te registreren.
solution: Analytics
title: Insight Server registreren als Windows-service
uuid: 1b3d53ca-d50f-4520-abf5-6d5c40493b88
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---


# Insight Server registreren als Windows-service{#registering-insight-server-as-a-windows-service}

Procedure om de Server van het Inzicht te beginnen en het gelijktijdig als Dienst van Microsoft Windows te registreren.

>[!NOTE]
>
>Wanneer u [!DNL Insight Server] voor het eerst start, wordt automatisch verbinding gemaakt met de Adobe-licentieserver om uw digitale certificaat te registreren. Om het registratieproces met succes te voltooien, moet uw computer met Internet worden verbonden wanneer u de volgende stappen uitvoert.

**Om het als Dienst van Vensters te beginnen[!DNL Insight Server]en te registreren**

1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\bin]

1. Bij de bevelherinnering, voer het volgende bevel uit om het te beginnen [!DNL Insight Server] en gelijktijdig te registreren om als dienst onder Microsoft Windows te lopen:

   ```
   <filepath>
   InsightServer64.exe /regserver 
   </filepath>
   ```

1. Om te bevestigen dat [!DNL Insight Server] correct loopt, klik **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.

   1. In de de dienstlijst, bepaal de plaats van de ingang voor **[!DNL Adobe Insight Server]** en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is.
   1. Sluit het configuratiescherm Services.

1. Als u wilt controleren of er fouten zijn opgetreden tijdens het opstarten, klikt u op [!DNL Insight Server] > **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** **[!UICONTROL Event Viewer]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.

   1. Selecteer het [!DNL Event Viewer] logbestand in het linkerdeelvenster van het **[!UICONTROL Application]** venster.
   1. Zoek in het rechterdeelvenster naar gebeurtenissen met &quot;Adobe&quot; in de [!DNL Source] kolom.
   1. Als er een fout optreedt bij &quot;Adobe&quot;, dubbelklikt u op de fout om het [!DNL Event Properties] venster weer te geven. Dit venster bevat gedetailleerde informatie over de fout.

1. Wanneer u klaar bent met het bekijken van het [!DNL Applications] logbestand, sluit u de Event Viewer.

U hebt de installatie van [!DNL Insight Server]voltooid. [!DNL Insight Server] is ontworpen om continu te worden uitgevoerd. Als u de computer opnieuw opstart, wordt deze automatisch [!DNL Insight Server] opnieuw opgestart. Als u moet beginnen en [!DNL Insight Server] manueel ophouden, kunt u dit doen gebruikend het de controlepaneel van de Diensten in Vensters. Zoals beschreven in de volgende sectie, kunt u naar keuze de [!DNL Insight Server] dienst vormen om periodiek opnieuw te beginnen.

## De service automatisch opnieuw starten configureren {#section-f9bb91614513435f84ee55c0ec8edb13}

[!DNL Insight Server] is ontworpen om zonder onderbreking te blijven werken. De toepassing wordt doorgaans alleen gestopt of gestart wanneer niet-frequente taken worden uitgevoerd, zoals software-upgrades of certificaatwijzigingen, of wanneer zich bepaalde systeemfouten voordoen. Het is niet nodig de [!DNL Insight Server] service tijdens normale werking van het systeem te stoppen of opnieuw te starten. nochtans, kunt u de dienst vormen om periodiek (dagelijks, wekelijks, of maandelijks) opnieuw te beginnen om, bijvoorbeeld, de gebeurtenisberichten te ontruimen.

**De[!DNL Insight Server]service automatisch opnieuw starten configureren**

1. Navigeer naar de [!DNL Components] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Gebruik een teksteditor, zoals Kladblok, om een nieuw bestand met de naam [!DNL ScheduledRestart.cfg].
1. Voer de volgende tekst in het [!DNL ScheduledRestart.cfg] bestand in:

   ```
   component = ScheduledRestart:  
     Start Time = string: Month DD, YYYY HH:MM:SS TZone 
     Restart Every = string: frequency
   ```

   <table id="table_AC05861E141E4928BE844C8611DEC43D"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Voor deze waarde... </th> 
      <th colname="col2" class="entry"> Opgeven </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <i>Maand DD, YYYY HH:MM:SS Tone</i> </td> 
      <td colname="col2"> <p>De tijd wanneer u de Server van het <span class="keyword"> Inzicht voor het eerst opnieuw </span> wilt beginnen. </p> <p>Voorbeeld: 13 augustus 2013 22:30:00 EST </p> <p> <p>Opmerking:  U moet een tijdzone opgeven. De tijdzone wordt niet standaard ingesteld op de systeemtijd als deze niet is opgegeven. Als u wenst om de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid uit te voeren, moet u het <span class="filepath"> .dst </span> - dossier opslaan dat de aangewezen regels in de Base\Dataset\Timezone directory on the <span class="keyword"> machine van de Server van het Inzicht bevat </span> . Voor een lijst van gesteunde tijdzoneafkortingen en informatie over het uitvoeren van de Tijd van de Besparing van het Daglicht, zie de Codes van de <a href="../../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> Tijdzone </a>. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <i>frequentie</i> </td> 
      <td colname="col2"> <p>Een van de volgende waarden: 
       <ul id="ul_C29A40CD8FBB4333B5FA1D9E7DAD35EC"> 
       <li id="li_9FE07DD30C524CBB81C8F7968E7C733E">maand </li> 
       <li id="li_E5E1B97ED8FB43C0BDA496C620D24A4C">week </li> 
       <li id="li_E6043B382FAE4B5D85CAADDFA60E4902">dag </li> 
       </ul> </p> <p>Om op de frequentie te wijzen waarbij u de Server van het <span class="keyword"> </span> Inzicht na de aanvankelijke tijd wilt opnieuw beginnen die in de Tijd van het Begin wordt gespecificeerd. </p> <p>Bijvoorbeeld, als u de Server van het <span class="keyword"> </span> Inzicht één keer per week wilde opnieuw beginnen, zou u deze waarde aan "week"plaatsen. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Sla het [!DNL ScheduledRestart.cfg] bestand op.

   Controleer of het [!DNL ScheduledRestart.cfg] bestand zich in de [!DNL Components] map bevindt waarin u het hebt geïnstalleerd [!DNL Insight Server].

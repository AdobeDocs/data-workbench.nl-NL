---
description: Procedure om de Server van het Inzicht te beginnen en het gelijktijdig als Dienst van Microsoft Windows te registreren.
title: Insight Server registreren als Windows-service
uuid: 1b3d53ca-d50f-4520-abf5-6d5c40493b88
exl-id: ba74d4c0-5d99-47a4-8b92-c65d0ec514e2
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# Inzichtsserver registreren als Windows-service{#registering-insight-server-as-a-windows-service}

Procedure om de Server van het Inzicht te beginnen en het gelijktijdig als Dienst van Microsoft Windows te registreren.

>[!NOTE]
>
>Wanneer u [!DNL Insight Server] voor het eerst start, wordt er automatisch verbinding gemaakt met de Adobe-licentieserver om uw digitale certificaat te registreren. Om het registratieproces met succes te voltooien, moet uw computer met Internet worden verbonden wanneer u de volgende stappen uitvoert.

**Om het als Dienst van Vensters te beginnen  [!DNL Insight Server] en te registreren**

1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u [!DNL Insight Server] hebt geïnstalleerd.

   Voorbeeld: [!DNL C:\Adobe\Server\bin]

1. Bij de bevelherinnering, voer het volgende bevel uit om [!DNL Insight Server] te beginnen en gelijktijdig het te registreren om als dienst onder Microsoft Windows te lopen:

   ```
   <filepath>
   InsightServer64.exe /regserver 
   </filepath>
   ```

1. Om te bevestigen dat [!DNL Insight Server] correct loopt, klik **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.

   1. Zoek in de servicelijst de vermelding voor **[!DNL Adobe Insight Server]** en bevestig dat de status is gestart en dat het opstarttype Automatisch is.
   1. Sluit het configuratiescherm Services.

1. Om te controleren of [!DNL Insight Server] fouten ondervond tijdens het opstarten, klikt u op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.

   1. Selecteer in het linkerdeelvenster van het venster [!DNL Event Viewer] het logbestand **[!UICONTROL Application]**.
   1. Zoek in het rechterdeelvenster naar gebeurtenissen met &quot;Adobe&quot; in de kolom [!DNL Source].
   1. Als u een fout van &quot;Adobe vindt,&quot;dubbelklik de fout om het [!DNL Event Properties] venster te tonen. Dit venster bevat gedetailleerde informatie over de fout.

1. Wanneer u klaar bent met het bekijken van het [!DNL Applications] logboek, sluit de Kijker van de Gebeurtenis.

U hebt de installatie van [!DNL Insight Server] voltooid. [!DNL Insight Server] is ontworpen om continu te worden uitgevoerd. Als u de computer opnieuw opstart, wordt [!DNL Insight Server] automatisch opnieuw opgestart. Als u [!DNL Insight Server] manueel moet beginnen en tegenhouden, kunt u dit doen gebruikend het de controlepaneel van de Diensten in Vensters. Zoals in de volgende sectie wordt beschreven, kunt u desgewenst de [!DNL Insight Server]-service zodanig configureren dat deze periodiek opnieuw wordt gestart.

## De service voor automatisch opnieuw opstarten configureren {#section-f9bb91614513435f84ee55c0ec8edb13}

[!DNL Insight Server] is ontworpen om zonder onderbreking te blijven werken. De toepassing wordt doorgaans alleen gestopt of gestart wanneer niet-frequente taken worden uitgevoerd, zoals software-upgrades of certificaatwijzigingen, of wanneer zich bepaalde systeemfouten voordoen. Het is niet nodig de [!DNL Insight Server]-service te stoppen of opnieuw te starten tijdens normaal systeemgebruik. nochtans, kunt u de dienst vormen om periodiek (dagelijks, wekelijks, of maandelijks) opnieuw te beginnen om, bijvoorbeeld, de gebeurtenisberichten te ontruimen.

**De  [!DNL Insight Server] service automatisch opnieuw opstarten configureren**

1. Navigeer naar de map [!DNL Components] in de map waarin u [!DNL Insight Server] hebt geïnstalleerd.

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Gebruik een tekstredacteur zoals Blocnote om een nieuw dossier tot stand te brengen genoemd [!DNL ScheduledRestart.cfg].
1. Voer de volgende tekst in het [!DNL ScheduledRestart.cfg]-bestand in:

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
      <td colname="col2"> <p>Het tijdstip waarop <span class="keyword"> Insight Server </span> voor het eerst opnieuw moet worden gestart. </p> <p>Voorbeeld: 13 augustus 2013 22:30:00 EST </p> <p> <p>Opmerking:  U moet een tijdzone opgeven. De tijdzone wordt niet standaard ingesteld op de systeemtijd als deze niet is opgegeven. Als u zomertijd of een gelijkaardig klok-veranderende beleid wilt uitvoeren, moet u <span class="filepath"> .dst </span> dossier opslaan die de aangewezen regels in Base\Dataset\Timezone directory on the <span class="keyword"> de machine van de Server </span> van het Inzicht bevatten. Zie <a href="../../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> Tijdzonecodes </a> voor een lijst met ondersteunde tijdzoneafkortingen en informatie over het implementeren van zomertijd. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <i>frequentie</i> </td> 
      <td colname="col2"> <p>Een van de volgende waarden: 
       <ul id="ul_C29A40CD8FBB4333B5FA1D9E7DAD35EC"> 
       <li id="li_9FE07DD30C524CBB81C8F7968E7C733E">maand </li> 
       <li id="li_E5E1B97ED8FB43C0BDA496C620D24A4C">week </li> 
       <li id="li_E6043B382FAE4B5D85CAADDFA60E4902">dag </li> 
       </ul> </p> <p>Om de frequentie aan te geven waarmee <span class="keyword"> de Server </span> van het Inzicht na de aanvankelijke tijd moet worden opnieuw begonnen die in de Tijd van het Begin wordt gespecificeerd. </p> <p>Als u bijvoorbeeld <span class="keyword"> Insight Server </span> één keer per week opnieuw wilt starten, stelt u deze waarde in op "week". </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Sla het [!DNL ScheduledRestart.cfg]-bestand op.

   Controleer of het [!DNL ScheduledRestart.cfg]-bestand zich in de map [!DNL Components] in de map bevindt waarin u [!DNL Insight Server] hebt geïnstalleerd.

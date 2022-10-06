---
description: Procedure om de Server van het Inzicht te beginnen en het gelijktijdig te registreren als de Dienst van Microsoft Windows.
title: Insight Server registreren als Windows-service
uuid: 1b3d53ca-d50f-4520-abf5-6d5c40493b88
exl-id: ba74d4c0-5d99-47a4-8b92-c65d0ec514e2
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---

# Insight Server registreren als Windows-service{#registering-insight-server-as-a-windows-service}

{{eol}}

Procedure om de Server van het Inzicht te beginnen en het gelijktijdig te registreren als de Dienst van Microsoft Windows.

>[!NOTE]
>
>Wanneer u begint [!DNL Insight Server] voor het eerst wordt automatisch verbinding gemaakt met de Adobe-licentieserver om uw digitale certificaat te registreren. Om het registratieproces met succes te voltooien, moet uw computer met Internet worden verbonden wanneer u de volgende stappen uitvoert.

**Aan begin [!DNL Insight Server] en registreer het als Dienst van Vensters**

1. Open een opdrachtprompt en navigeer naar de submap bin in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\bin]

1. Bij de bevelherinnering, voer het volgende bevel uit om te beginnen [!DNL Insight Server] en registreer het om als dienst onder Microsoft Windows te lopen:

   ```
   <filepath>
   InsightServer64.exe /regserver 
   </filepath>
   ```

1. Bevestig dat [!DNL Insight Server] correct wordt uitgevoerd, klikt u op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Services]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.

   1. Zoek in de lijst met services de vermelding voor **[!DNL Adobe Insight Server]** en bevestig dat zijn status Begonnen is en zijn starttype Automatisch is.
   1. Sluit het configuratiescherm Services.

1. Controleren of [!DNL Insight Server] heeft bij het opstarten fouten opgelopen en klikt u op **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Event Viewer]**. Deze opdrachtvolgorde kan variëren, afhankelijk van de versie van Windows die u gebruikt.

   1. In het linkerdeelvenster van het dialoogvenster [!DNL Event Viewer] venster, selecteert u de **[!UICONTROL Application]** log.
   1. Zoek in het rechterdeelvenster naar gebeurtenissen met &quot;Adobe&quot; in het dialoogvenster [!DNL Source] kolom.
   1. Als u een fout vindt van &quot;Adobe&quot;, dubbelklikt u op de fout om de fout weer te geven [!DNL Event Properties] venster. Dit venster bevat gedetailleerde informatie over de fout.

1. Wanneer u klaar bent met het onderzoeken van de [!DNL Applications] , sluit de Event Viewer.

U hebt de installatie van [!DNL Insight Server]. [!DNL Insight Server] is ontworpen om continu te worden uitgevoerd. Als u de computer opnieuw opstart, [!DNL Insight Server] wordt automatisch opnieuw gestart. Als u moet starten en stoppen [!DNL Insight Server] manueel, kunt u dit doen gebruikend het de controlepaneel van de Diensten in Vensters. Zoals beschreven in de volgende sectie, kunt u naar keuze vormen [!DNL Insight Server] automatisch opnieuw opstarten.

## De service automatisch opnieuw starten configureren {#section-f9bb91614513435f84ee55c0ec8edb13}

[!DNL Insight Server] is ontworpen om zonder onderbreking te blijven werken. De toepassing wordt doorgaans alleen gestopt of gestart wanneer niet-frequente taken worden uitgevoerd, zoals software-upgrades of certificaatwijzigingen, of wanneer zich bepaalde systeemfouten voordoen. Het is niet nodig de [!DNL Insight Server] de dienst tijdens de normale werking van het systeem; nochtans, kunt u de dienst vormen om periodiek (dagelijks, wekelijks, of maandelijks) opnieuw te beginnen om, bijvoorbeeld, de gebeurtenisberichten te ontruimen.

**Om het [!DNL Insight Server] automatisch opnieuw opstarten**

1. Ga naar de [!DNL Components] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

   Voorbeeld: [!DNL C:\Adobe\Server\Components]

1. Een teksteditor, zoals Kladblok, gebruiken om een nieuw bestand te maken met de naam [!DNL ScheduledRestart.cfg].
1. Voer de volgende tekst in het dialoogvenster [!DNL ScheduledRestart.cfg] bestand:

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
      <td colname="col1"> <i>DD maand, YYYY HH:MM:SS TZone</i> </td> 
      <td colname="col2"> <p>De tijd waarop u wilt <span class="keyword"> Insight Server </span> voor het eerst opnieuw te beginnen. </p> <p>Voorbeeld: 13 augustus 2013 22:30:00 EST </p> <p> <p>Opmerking: U moet een tijdzone opgeven. De tijdzone wordt niet standaard ingesteld op de systeemtijd als deze niet is opgegeven. Als u de Tijd van de Besparing van het Daglicht of een gelijkaardig klok-veranderende beleid wilt uitvoeren, moet u sparen <span class="filepath"> .dst </span> bestand met de desbetreffende regels in de map Base\Dataset\Timezone in het dialoogvenster <span class="keyword"> Insight Server </span> machine. Voor een lijst van gesteunde tijdzoneafkortingen en informatie over het uitvoeren van de Tijd van de Besparing van het Daglicht, zie <a href="../../../../home/c-inst-svr/c-time-zn-cds.md#concept-eed5ba32d5d347cf94b76db83b29f211"> Tijdzonecodes </a>. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <i>frequentie</i> </td> 
      <td colname="col2"> <p>Een van de volgende waarden: 
       <ul id="ul_C29A40CD8FBB4333B5FA1D9E7DAD35EC"> 
       <li id="li_9FE07DD30C524CBB81C8F7968E7C733E">maand </li> 
       <li id="li_E5E1B97ED8FB43C0BDA496C620D24A4C">week </li> 
       <li id="li_E6043B382FAE4B5D85CAADDFA60E4902">dag </li> 
       </ul> </p> <p>De gewenste frequentie aangeven <span class="keyword"> Insight Server </span> opnieuw te beginnen na de aanvankelijke tijd die in de Tijd van het Begin wordt gespecificeerd. </p> <p>Bijvoorbeeld als u wilt <span class="keyword"> Insight Server </span> om één keer per week opnieuw te beginnen, zou u deze waarde aan "week"plaatsen. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Sla de [!DNL ScheduledRestart.cfg] bestand.

   Controleer of de [!DNL ScheduledRestart.cfg] bestand bevindt zich in het [!DNL Components] map in de map waarin u hebt geïnstalleerd [!DNL Insight Server].

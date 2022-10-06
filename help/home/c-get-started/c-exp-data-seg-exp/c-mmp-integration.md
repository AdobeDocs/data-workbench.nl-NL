---
description: Met Data Workbench kunt u bestanden exporteren om deze te integreren met de exportopties voor profielen en soorten publiek als onderdeel van een geïntegreerde Adobe Experience Cloud.
title: Master marketingprofiel exporteren
uuid: bae0f0c5-a452-4afd-9f2c-5f3ab69a12d2
exl-id: 9fc89815-d31d-41a7-a0c0-de1e84b24baa
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Master marketingprofiel exporteren{#master-marketing-profile-export}

{{eol}}

Met Data Workbench kunt u bestanden exporteren en integreren met profielen en soorten publiek als onderdeel van een geïntegreerde Adobe Experience Cloud.

<!-- <a id="section_731922BC8628479198A41EF3EA72F2FF"></a> -->

Profielen en soorten publiek maken deel uit van de [Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html), een kerndienst van de [!DNL Adobe Experience Cloud]. Met de export Profielen en Soorten publiek kunnen soorten publiek door de Experience Cloud worden gedeeld met behulp van een unieke Experience Cloud-id (ECID) die aan elke bezoeker is toegewezen en die vervolgens door [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html). De [!DNL ExportIntegration.exe] application ( [!DNL E:\Server\Scripts]) wordt gebruikt om zowel MMP- als Adobe Target-export te genereren.

**De FSU-server configureren voor het gebruik van profielen en soorten publiek**

1. Open uw FSU-server.
1. Open het bestand MMPExport.cfg. `Server/Admin/Export/MMPExport.cfg`.
1. Voer desgewenst waarden in in alle velden. Bijvoorbeeld:

   >[!NOTE]
   >
   >De integratie MMP/AAM is afhankelijk van de Amazon s3 bucket voor gegevensoverdracht.
   >
   >
   >De s3 informatie die voor overdracht MMP (s3) wordt vereist kan van het team van de Audience Manager worden verkregen.

   ```
   Sample MMPExport.cfg
   MMP Export Configuration = MMPExportConfiguration: 
   s3 Bucket = string: aws_bucket_for_mmp 
   s3 Object Directory = string: test/files/ 
   s3 Region = string: us-east-1 
   s3 Access Key = string: ZZKI62OO5YBA 
   s3 Secret Key = string: ioqwa3OpNE5 
   data Provider Name = string: 895 
   client ID = string: mcprofile2-test 
   client Secret = string: saea1287617212987q 
   username = string: mmptest 
   password = string: pass 
   numRecordsPerChunk = int:  
   numThreads = int:  
   maxRetriesOnSendFailure = unsigned int:
   ```

   >[!NOTE]
   >
   >De [!DNL MMPExport.cfg]Met dit bestand kunt u ook alle records vastleggen, deze in sets splitsen en records maken. De stukjes records worden vervolgens geëxporteerd naar Amazon S3. Er zijn drie verplichte parameters nodig om records te maken: [!DNL numRecordsPerChunk], [!DNL numThreads], en [!DNL maxRetriesOnSendFailure].

**Definitie van parameters**

<table id="table_DDEFBC45895A4663973F9C2EB9052FEF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Definitie </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <i>s3 Emmertje</i> </td> 
   <td colname="col2"> Het AWS S3-emmertje waarnaar de uitvoer wordt overgedragen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 Object Directory</i> </td> 
   <td colname="col2"> Een pad om s3-bestanden op te slaan. Dit ondersteunt submappen. <p> <p>Belangrijk: Spatie- en multibyte-tekens zijn niet toegestaan in het pad en leiden tot fouten bij het exporteren. (Het afbreekstreepje is toegestaan.) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 Regio</i> </td> 
   <td colname="col2"> Het AWS s3-gebied waarnaar de export wordt verzonden. Voorbeeld. us-East-1 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 Toegangstoets</i> </td> 
   <td colname="col2"> AWS s3 Access Key </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>s3 Geheime sleutel</i> </td> 
   <td colname="col2"> AWS s3 Geheime sleutel </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>Naam gegevensaanbieder</i> </td> 
   <td colname="col2"> Dit zal de omslagnaam zijn die voor het opslaan van segmenten en eigenschappen in AAM respectievelijk wordt gebruikt. Dit zou uniek per klant moeten zijn. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>client-id</i> </td> 
   <td colname="col2"> Dit is een unieke client-id die aan een klant wordt verstrekt wanneer deze voor MMP wordt ingericht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>clientgeheim</i> </td> 
   <td colname="col2"> <p><i></i>Dit is een uniek cliëntgeheim dat aan een klant wordt verstrekt wanneer hij/zij voor MMP wordt voorzien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>gebruikersnaam</i> </td> 
   <td colname="col2"> MMP-gebruikersnaam </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>password</i> </td> 
   <td colname="col2"> MMP-wachtwoord </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>numRecordsPerChunk</i> </td> 
   <td colname="col2"> <p>Bepaalt de brokgrootte in termen van aantal verslagen. </p> <p>De implementatie knipt de door de gebruiker opgegeven waarde tot min = 1000 records&amp;nbsp;(~50 kB blokken)&amp;nbsp; en max = 50000 records (~2,5 MB blokken).&amp;nbsp;Een standaardwaarde van 10000 wordt gebruikt voor het geval de gebruiker dit configuratiebezit niet specificeert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>numThreads</i> </td> 
   <td colname="col2"> <p>Bepaalt het parallellisme van het segment dat deel verzendt. Het keurt een waarde tussen 1 tot 24 draden goed, en zijn standaardwaarde is 12 draden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <i>maxRetriesOnSendFailed</i> </td> 
   <td colname="col2"> <p>Hiermee bepaalt u het aantal pogingen om opnieuw te proberen dat moet worden uitgevoerd in het geval van 'chunk send'-fouten. De standaardwaarde is 0 waarmee wordt opgegeven dat het niet opnieuw wordt geprobeerd. </p> <p>Tussen pogingen wordt een slaapinterval van 2 seconden gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

**MMP-export van de client genereren**

1. Open vanuit de client een werkruimte en klik met de rechtermuisknop **[!UICONTROL Tools]**> **[!UICONTROL Detail Table]**.
1. Toevoegen **Niveau**.
1. Klik met de rechtermuisknop op de koptekst en selecteer **Kenmerken toevoegen**.
1. Klik met de rechtermuisknop op de koptekst en selecteer **Nieuw Master marketingprofiel exporteren**. ![](assets/mmp_mmp_export.png)
1. Uitbreiden **Query**.

   ![](assets/mmp_mmp_query.png)

1. Uitbreiden **MMP-configuratie**.
1. (vereist) Voer de **Naam van MMP-segment** en **Veld voor MMP-bezoeker-id**. Deze parameters mogen niet leeg blijven.
1. De **Naam van MMP-segment** moet overeenkomen met de Segment-id die is gedefinieerd in het MMP.
1. De **Id van MMP-bezoeker** is de in stap 4 gedefinieerde kenmerkkolom die overeenkomt met de **Bezoeker-id**.
1. Nadat u deze velden hebt ingevoerd, kunt u het exporteren opslaan door met de rechtermuisknop op de koptekst voor het exporteren te klikken en **Opslaan** als &quot;Gebruiker\.export&quot;.
1. Openen **Beheer** > **Profielbeheer** en sla het exporteren naar het profiel op.

   Als alle gegevens correct zijn ingevoerd, wordt een exportbestand gegenereerd in de FSU ([!DNL Server/Exports]) en zal de uitvoer naar de AWS ook met behulp van de in [!DNL MMPExport.cfg]. Het logboek hiervoor is beschikbaar in [!DNL Server/Trace/]. bijv. [!DNL MMP-102014-133651- `<Segment Export Name>` .log]

```
Query = SegmentExportQuery: 
Command = string: ExportIntegration.exe 
Command Arguments = string: \"%file%.cfg\" \"%file%\" 
Filter = string: 
Level = string: Page View 
MMP Configuration = MMPConfiguration: 
MMP Segment Name = string: 12345 
MMP Visitor ID Field = string: Tracking ID 
Oneshot = bool: true 
Output Fields = vector: 3 items 
0 = ColumnDefinition: 
Column Name = string: 
Field Name = string: Tracking ID 
1 = ColumnDefinition: 
Column Name = string: 
Field Name = string: PID 
2 = ColumnDefinition: 
Column Name = string: 
Field Name = string: SID 
Output File = string: MMPTest.txt 
Output Format = string: %1%\t%2%\t%3%\r\n 
Schedule End Time = string: 
Schedule Every = string: 
Schedule Start Time = string: 
Time Limit (sec) = double: 1800 
```

| Configuratiedetails | Beschrijving |
|---|---|
| MMP-segment-id | Vereist. Dit is een id die u eerst in de Audience Manager definieert. |
| Veld voor MMP-bezoeker-id | Wijs de ECID toe. |

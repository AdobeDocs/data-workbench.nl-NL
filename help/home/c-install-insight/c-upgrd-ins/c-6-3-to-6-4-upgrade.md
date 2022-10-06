---
description: Voer de volgende stappen uit om te upgraden naar Data Workbench v6.4.
title: Upgrade van 6.3 naar 6.4
uuid: 2461c1ab-cf99-4fb5-b431-d7062df7a53d
exl-id: 540deb86-2463-4820-b67a-a32d68b4346e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Upgrade van 6.3 naar 6.4{#upgrading-to}

{{eol}}

Voer de volgende stappen uit om te upgraden naar Data Workbench v6.4.

## Upgradevereisten en Recommendations {#section-8704a9ac358246cd81233dd0982d534f}

Volg deze eisen en aanbevelingen bij de upgrade naar Data Workbench 6.4.

>[!IMPORTANT]
>
>U wordt aangeraden de nieuw geïnstalleerde standaardconfiguratiebestanden te gebruiken en deze aan te passen in plaats van bestanden van een vorige installatie te verplaatsen, met de volgende uitzonderingen:

* **Toevoegen** ***Uitgesloten processen*** for *MS System Center Endpoint Protection in Windows 2012 Servers* voor de volgende uitvoerbare bestanden:

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**

   Dit zal de rechten van de lijst van gewenste personen voor deze interface uitvoerbare voorwerpen toelaten.

* **Werk de *Trust_ca_cert.pem* certificaat op de servers**.
* **Herorganisatie van kenmerkprofielen**.

   * De *Attributie* map is hernoemd naar ***Attributie - Premium*** (bevindt zich in de standaardinstallatie op *Profielen*\*Attributie - Premium*).

   * De *Premium* profiel is verwijderd en de werkruimte is verplaatst naar het nieuwe ***Attributie - Premium*** map.

* **Bijwerken *Attribution-Premium* instellingen**. Als u aangepaste profielen hebt met parameterinstellingen die de standaardinstellingen overschrijven *Adobe SC* -profiel, moet u de aangepaste velden in deze configuratiebestanden bijwerken:

   * **[!DNL Decoding Instructions.cfg]**
   * **[!DNL SC Fields.cfg]**

* Vanwege deze reorganisatie wilt u de oude *Attributie* en *Premium* mappen vanaf de installatie van de server.

   **Deze instellingen wijzigen**

   ```
   Profile = profileInfo:  
     Active = bool: true 
     Directories = vector: 6 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\\ 
   
       4 = string: Attribution\\ 
       5 = string: Premium\\
   ```

   op deze instellingen:

   ```
   Profile = profileInfo:  
     Active = bool: true 
     Directories = vector: 5 items 
       0 = string: Base\\ 
       1 = string: Geography\\ 
       2 = string: Predictive Analytics\\ 
       3 = string: Adobe SC\
       4 = string: Attribution - Premium\\
   ```

* **Aangepaste bestanden Meta.cfg bijwerken** (indien nodig).

   De **[!DNL Meta.cfg]** bestanden in **[!DNL Base\Context and AdobeSC\Context]** zijn bijgewerkt in deze versie.

   Als u de **meta.cfg** moet uw profielkopie tijdens de installatie worden bijgewerkt met deze parameters en de **metagegevensvector** op passende wijze ingevoerd:

   ```
   94 = meta: 
     path = string: SegmentExport:CRS Configuration/CRS Attributes 
     acceptable children = vector: 1 items 
       0 = Template: 
         name = string: CRS Attributes 
         value = CRSAttributeConfiguration: 
           Attribute Name = string: 
           Attribute Type(int,string) = string: 
           Field Name = string: 
   
   95 = meta: 
     path = string: SegmentExportQuery:CRS Configuration/Report Suite 
     acceptable children = vector: 1 items 
       0 = Template 
         name = string: Add Report Suite 
         value = string:
   ```

* **Machtigingen rapportserver instellen** om Microsoft Excel-rapporten te genereren op Windows 2012-servers.

   1. Toestemming voor de hoofdmap instellen (**[!DNL E:\ReportServer\]**) naar *Iedereen = volledige controle*.

   1. Maak de volgende mappen met de juiste machtigingen:

      ```
      C:\Windows\SysWOW64\config\systemprofile\AppData\Local\Microsoft\Windows\INetCac‌he 
      C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\INetCac‌he 
      C:\Windows\System32\config\systemprofile\Desktop 
      C:\Windows\SysWOW64\config\systemprofile\Desktop
      ```

      >[!NOTE]
      >
      >Als u de Server van het Rapport op de Server 2012 van Vensters in werking stelt, moet u de Server 2012 R2 hebben van Vensters geïnstalleerd.

   1. Wijs &quot;SYSTEM&quot;als eigenaar voor deze omslagen toe.

* **Voeg doopvonten aan de Server van het Rapport toe.** In de **[!DNL ReportServer.cfg]**bestand, voeg deze lettertypen toe (voor alle talen):

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```

* **Werk uw versie van Microsoft Excel bij **(indien nodig).

   Met de versie van Data Workbench 6.4, is de steun voor Excel 2007 gestopt. Ook omdat de Data Workbench slechts op Microsoft Vensters voor architectuur met 64 bits loopt, wordt het geadviseerd dat u ook een versie met 64 bits van Microsoft Excel installeert.

* **64-bits architectuur** vereist voor installatie van Workstation (client).
* **Voer de Tovenaar van de Opstelling van het Werkstation in**.

   Installeer de nieuwe versie van het werkstation (client) door te downloaden en te starten ***InsightSetup.exe*** en door de opstellingsinstructies te gaan. De installatiewizard installeert uw bestanden standaard op een nieuwe locatie:

   Programmabestanden worden nu standaard opgeslagen in:

   ```
   C:\Program Files\Adobe\Adobe Analytics\Data Workbench
   ```

   Gegevensbestanden (profielen, certificaten, traceringslogbestanden en gebruikersbestanden) worden nu standaard opgeslagen naar:

   ```
   C:\Users\<username>\AppData\Local\Adobe\Adobe Analytics\Data Workbench\
   ```

* **Lettertypen toevoegen aan het werkstation**.

   In de **[!DNL Insight.cfg]** bestand, voeg deze lettertypen toe (voor alle talen):

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```

---
description: Voer de volgende stappen uit om te upgraden naar Data Workbench v6.4.
title: Upgrade van 6.3 naar 6.4
uuid: 2461c1ab-cf99-4fb5-b431-d7062df7a53d
translation-type: tm+mt
source-git-commit: 2930bd3ae06e700e75144221fc993efdd6bd1e85
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---


# Upgrade van 6.3 naar 6.4{#upgrading-to}

Voer de volgende stappen uit om te upgraden naar Data Workbench v6.4.

## Upgradevereisten en aanbevelingen {#section-8704a9ac358246cd81233dd0982d534f}

Volg deze eisen en aanbevelingen bij de upgrade naar Data Workbench 6.4.

>[!IMPORTANT]
>
>U wordt aangeraden de nieuw geïnstalleerde standaardconfiguratiebestanden te gebruiken en deze aan te passen in plaats van bestanden van een vorige installatie te verplaatsen, met de volgende uitzonderingen:

* **Voeg** ***Uitgesloten Processen*** voor de Bescherming van het Eindpunt van het Centrum van het *Systeem van MS in Vensters 2012 Servers* voor de volgende uitvoerbare lijnen toe:

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**
   Dit zal allowlist rechten voor deze interface uitvoerbare voorwerpen toelaten.

* **Werk het *certificaat Trust_ca_cert.pem*bij op de servers**.
* **Reorganisatie van kenmerkprofielen**.

   * De naam van de map *Attribution* is gewijzigd in ***Attribution - Premium*** (in de standaardinstallatie van *Profiles*\*Attribution - Premium*).

   * Het *Premium* -profiel is verwijderd en de werkruimte is verplaatst naar de nieuwe map ***Attribution - Premium*** .

* **Werk *Attribution-Premium*-instellingen** bij. Als u aangepaste profielen hebt met parameterinstellingen die het standaard *Adobe SC* -profiel overschrijven, moet u de aangepaste velden in deze configuratiebestanden bijwerken:

   * **[!DNL Decoding Instructions.cfg]**
   * **[!DNL SC Fields.cfg]**

* Vanwege deze reorganisatie wilt u de oude mappen *Attribution* en *Premium* verwijderen uit de serverinstallatie.

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

* **Werk aangepaste bestanden** Meta.cfg bij (indien nodig).

   De **[!DNL Meta.cfg]** bestanden in **[!DNL Base\Context and AdobeSC\Context]** mappen zijn bijgewerkt in deze release.

   Als u het bestand **meta.cfg** tijdens de installatie overschrijft, moet uw profielkopie worden bijgewerkt met deze parameters en moet de juiste **metagegevensvector** worden ingevoerd:

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

* **Stel Rapportservermachtigingen** in om Microsoft Excel-rapporten te genereren op Windows 2012-servers.

   1. Stel machtigingen voor de hoofdmap (**[!DNL E:\ReportServer\]**) in op *Iedereen = volledige controle*.

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

* **Voeg doopvonten aan de Server van het Rapport toe.** Voeg in het bestand **[!DNL ReportServer.cfg]**deze lettertypen toe (voor alle talen):

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```

* **Werk uw versie van Microsoft Excel bij **(indien nodig).

   Met de versie van Data Workbench 6.4, is de steun voor Excel 2007 gestopt. Ook omdat de Data Workbench slechts op Microsoft Windows voor architectuur met 64 bits loopt, adviseert men dat u ook een versie met 64 bits van Microsoft Excel installeert.

* **64-bits architectuur** vereist voor Workstation (client)-installatie.
* **Voer de wizard** Workstation instellen uit.

   Installeer de nieuwe versie van het werkstation (cliënt) door ***InsightSetup.exe*** te downloaden en te lanceren en door de opstellingsinstructies te stappen. De installatiewizard installeert uw bestanden standaard op een nieuwe locatie:

   Programmabestanden worden nu standaard opgeslagen in:

   ```
   C:\Program Files\Adobe\Adobe Analytics\Data Workbench
   ```

   Gegevensbestanden (profielen, certificaten, traceringslogbestanden en gebruikersbestanden) worden nu standaard opgeslagen naar:

   ```
   C:\Users\<username>\AppData\Local\Adobe\Adobe Analytics\Data Workbench\
   ```

* **Voeg lettertypen toe aan het werkstation**.

   Voeg in het **[!DNL Insight.cfg]** bestand de volgende lettertypen toe (voor alle talen):

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```


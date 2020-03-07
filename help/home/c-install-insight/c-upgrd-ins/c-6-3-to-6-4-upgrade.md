---
description: Volg deze stappen om aan de Werkbank van Gegevens v6.4 te bevorderen.
title: Verbetering 6.3 tot 6.4
uuid: 2461c1ab-cf99-4fb5-b431-d7062df7a53d
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# Verbetering 6.3 tot 6.4{#upgrading-to}

Volg deze stappen om aan de Werkbank van Gegevens v6.4 te bevorderen.

## Vereisten en aanbevelingen voor upgrades {#section-8704a9ac358246cd81233dd0982d534f}

Volg deze vereisten en aanbevelingen wanneer het bevordering aan de Werkbank van Gegevens 6.4.

>[!IMPORTANT]
>
>Men adviseert dat u de onlangs geïnstalleerde standaardconfiguratiedossiers gebruikt en hen aanpast, eerder dan het bewegen van dossiers van een vorig installatie-met deze uitzonderingen aanpast:

* **Voeg** ***Uitgesloten Processen*** voor de Bescherming van het Eindpunt van het Centrum van het Systeem van *MS in de Servers* van Vensters 2012 voor de volgende executables toe:

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**
   Dit zal &quot;witte lijst&quot;rechten voor deze het omzetten uitvoerbare voorwerpen toestaan.

* **Werk het *Trust_ca_cert.pem*- certificaat op de servers** bij.
* **Reorganisatie van Attributieprofielen**.

   * De map *Attribution* is gewijzigd in ***Attribution - Premium*** (gevonden in de standaardinstallatie op *Profielen*\*Attribution - Premium*).

   * Het *Premium* -profiel is verwijderd en de werkruimte is verplaatst naar de nieuwe map ***Attribution - Premium*** .

* **Update *Attribution-Premium*settings**. Als u profielen met parametermontages hebt aangepast die het profiel van standaard *Adobe SC* met voeten treden, dan moet u de douanegebieden in deze configuratiedossiers bijwerken:

   * **[!DNL Decoding Instructions.cfg]**
   * **[!DNL SC Fields.cfg]**

* Wegens deze reorganisatie, zult u de oude omslagen van de *Attributie* en van de *Premium* uit uw serverinstallatie willen verwijderen.

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

   aan deze montages:

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

* **De douaneMeta.cfg- dossiers** van de update (indien nodig).

   De **[!DNL Meta.cfg]** dossiers in **[!DNL Base\Context and AdobeSC\Context]** omslagen zijn bijgewerkt in deze versie.

   Als u het **meta.cfg** - dossier tijdens installatie met voeten treedt, dan moet uw profielexemplaar met deze parameters en de geëigende **meta-gegevensvector** worden bijgewerkt ingegaan:

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

* **De vastgestelde toestemmingen** van de Server van het Rapport om de rapporten van Microsoft Excel over Vensters te produceren 2012 servers.

   1. Vastgestelde toestemming van de wortelomslag (**[!DNL E:\ReportServer\]**) aan *iedereen = volledige controle*.

   1. Creeer de volgende omslagen met aangewezen toestemmingen:

      ```
      C:\Windows\SysWOW64\config\systemprofile\AppData\Local\Microsoft\Windows\INetCac‌he 
      C:\Windows\System32\config\systemprofile\AppData\Local\Microsoft\Windows\INetCac‌he 
      C:\Windows\System32\config\systemprofile\Desktop 
      C:\Windows\SysWOW64\config\systemprofile\Desktop
      ```

      >[!NOTE]
      >
      >Als u de Server van het Rapport op de Server 2012 van Vensters in werking stelt, moet u de Server 2012 R2 hebben van Vensters geïnstalleerd.

   1. Wijs &quot;SYSTEEM&quot;als eigenaar voor deze omslagen toe.

* **Voeg doopvonten aan de Server van het Rapport toe.** In het **[!DNL ReportServer.cfg]**dossier, voeg deze doopvonten (voor alle talen) toe:

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```

* **Werk uw versie van Microsoft Excel bij **(indien nodig).

   Met de versie van Werkbank 6.4 van Gegevens, is de steun voor Excel 2007 stopgezet. Ook omdat de Werkbank van Gegevens slechts op Microsoft Windows voor architectuur met 64 bits loopt, adviseert men dat u ook een versie met 64 bits van Microsoft Excel installeert.

* **64-bits architectuur** vereist voor installatie van werkstations (client).
* **Stel de Tovenaar** van de Opstelling van het Werkstation in werking.

   Installeer de nieuwe versie van het werkstation (cliënt) door ***InsightSetup.exe te downloaden en te lanceren*** en door de opstellingsinstructies te stappen. De opstellingstovenaar zal uw dossiers aan een nieuwe plaats door gebrek installeren:

   De dossiers van het programma worden nu bewaard door gebrek aan:

   ```
   C:\Program Files\Adobe\Adobe Analytics\Data Workbench
   ```

   De Dossiers van gegevens (profielen, certificaten, spoorlogboeken, en gebruikersdossiers) worden nu bewaard door gebrek aan:

   ```
   C:\Users\<username>\AppData\Local\Adobe\Adobe Analytics\Data Workbench\
   ```

* **Voeg doopvonten aan het Werkstation** toe.

   In het **[!DNL Insight.cfg]** dossier, voeg deze doopvonten (voor alle talen) toe:

   ```
   Fonts = vector: 3 items 
     0 = string: Arial 
     1 = string: SimSun 
     2 = string: MS Mincho
   ```


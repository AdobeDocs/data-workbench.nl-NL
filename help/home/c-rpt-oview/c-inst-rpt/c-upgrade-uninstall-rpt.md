---
description: Informatie over de bevordering van en het desinstalleren van uw software van de Server van het Rapport.
solution: Analytics
title: De Server van het Rapport bevorderen en desinstalleren
topic: Data workbench
uuid: 42f0d190-1a88-424d-be4b-90338144d287
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De Server van het Rapport bevorderen en desinstalleren{#upgrading-and-uninstalling-report-server}

Informatie over de bevordering van en het desinstalleren van uw software van de Server van het Rapport.

* [Upgraden Report](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-95fea4bddad74616a8aea450dcdb2282)
* [Rapport verwijderen](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-96eb3281c45a45c0a7065deaa6845c25)

## De Server van het Rapport van de verbetering {#section-95fea4bddad74616a8aea450dcdb2282}

Als u aan [!DNL Report Server] 5.4 bevordert, kunt u de instructies gebruiken om uw [!DNL Report Server] software te bevorderen. Als u [!DNL Report Server] 3.6 of vroeger gebruikt, contacteer Adobe voor hulp met uw verbetering.

Om [!DNL Report Server] 5.4 te bevorderen, gebruik gegevenswerkbank om een verbeteringsdossier aan de server van de gegevenswerkbank te kopiëren waarmet [!DNL Report Server] verbindt. Na het doen van dit, [!DNL Report] bevorderen de instanties van de Server automatisch zich wanneer zij met die server verbinden en een profiel laden.

>[!NOTE]
>
>Voordat u een upgrade uitvoert, moet u ervoor zorgen dat u de serversoftware van uw gegevenswerkbank en de profielen die op de server van de gegevenswerkbank worden uitgevoerd, correct hebt bijgewerkt. [!DNL Report Server] Voor meer informatie, contacteer de Raadplegende Diensten van Adobe.

Om de volgende procedure uit te voeren, moet u eerst het verbeteringsdossier voor verkrijgen [!DNL Report Server].

**Om aan[!DNL Report Server]5.4 en recentere versies te bevorderen**

1. Maak een steun van alle dossiers onder [!DNL E:\Portal] en verwijder alle dossiers en omslagen binnen deze folder.
1. Kopieer de inhoud van de nieuwe bouwstijl in [!DNL E:\Portal].
1. Wijzig [!DNL global.asa], [!DNL email.asp], en [!DNL TopNavigation.xml] volgens de instructies in de vorige sectie.

1. Kopieer de [!DNL users.mdb] back-up.

   >[!NOTE]
   >
   >Als u niet eerder rapporten met een .png output produceerde, moet u in de individuele rapportomslagen gaan en wijzigen [!DNL reports.xml] om een rapportformaat van te omvatten png. Anders kunt u een fout van 500 krijgen. Uw origineel [!DNL reports.xml] zou iets als het volgende kijken:

   ```
      <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
   <REPORTS>
    <REPORT format="xls">
     <NAME>Dashboard</NAME>
     <PATH>Dashboard.xls</PATH>
     <WEB_PATH>Dashboard.xls</WEB_PATH>
    </REPORT>
   </REPORTS>
   ```

   Het zou als volgt moeten worden gewijzigd:

   ```
   <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
   <REPORTS>
    <REPORT format="xls">
     <NAME>Dashboard</NAME>
     <PATH>Dashboard.xls</PATH>
     <WEB_PATH>Dashboard.xls</WEB_PATH>
    </REPORT>
    <REPORT format="png">
    <NAME>Dashboard</NAME>
     <PATH>Dashboard.png</PATH>
     <WEB_PATH>Dashboard.png</WEB_PATH>
    </REPORT>
   </REPORTS>
   ```

1. In [!DNL report.cfg], omvat een outputformaat van png en bewaar. Als u vooruit gaat, moet u rapporten genereren in png-indeling.

**Om aan[!DNL Report Server]4.0 te bevorderen**

1. Voor de computer van de gegevenswerkbank, kopieer het de verbeteringsdossier van de Server van het Rapport aan de [!DNL Temp\Software] omslag in de folder waar de gegevenswerkbank geïnstalleerd is.
1. De werkbank van het begin en laadt het [!DNL Configuration] profiel.
1. Klik de **[!UICONTROL Configure Connection to Servers]** duimnagel.
1. Klik in het [!DNL Servers Manager]dialoogvenster met de rechtermuisknop op het serverpictogram van de gegevenswerkbank en klik op **[!UICONTROL Server Files]**.

1. In de omslag van de Software, open de [!DNL Report Server] omslag.
1. Klik met de rechtermuisknop op het **[!UICONTROL Temp]** vinkje voor [!DNL ReportServer.exe] en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Rapportserver verwijderen {#section-96eb3281c45a45c0a7065deaa6845c25}

**Verwijderen[!DNL Report Server]**

1. Registreer de [!DNL Report Windows] service ongedaan.

   1. Open een bevelherinnering en navigeer aan de baksubfolder in de omslag waar u de server van de gegevenswerkbank (InsightServer64.exe.) installeerde Voorbeeld: [!DNL D:\Adobe\Report\bin]
   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en unregister: [!DNL visualreport /unregserver]

1. Schrap de de installatiefolder van de Server van het Rapport.


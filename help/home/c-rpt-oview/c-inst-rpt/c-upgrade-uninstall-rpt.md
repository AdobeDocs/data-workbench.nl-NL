---
description: Informatie over de bevordering van en het verwijderen van uw software van de Server van het Rapport.
title: Rapportserver upgraden en verwijderen
uuid: 42f0d190-1a88-424d-be4b-90338144d287
exl-id: 86d0d848-4e2a-45cb-a1b3-b8a856332d33
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Rapportserver upgraden en verwijderen{#upgrading-and-uninstalling-report-server}

{{eol}}

Informatie over de bevordering van en het verwijderen van uw software van de Server van het Rapport.

* [Rapport wordt bijgewerkt](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-95fea4bddad74616a8aea450dcdb2282)
* [Rapport wordt verwijderd](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-96eb3281c45a45c0a7065deaa6845c25)

## Rapportserver upgraden {#section-95fea4bddad74616a8aea450dcdb2282}

Als u een upgrade uitvoert naar [!DNL Report Server] 5.4, kunt u de instructies gebruiken om uw [!DNL Report Server] software. Als u [!DNL Report Server] 3.6 of eerder, contacteer Adobe voor hulp met uw verbetering.

Upgrade uitvoeren [!DNL Report Server] 5.4, de werkbank van gebruiksgegevens om een verbeteringsdossier aan de server van de gegevenswerkbank te kopiëren waarnaar [!DNL Report Server] verbindt. Na dit te hebben gedaan, [!DNL Report] Serverinstanties upgraden zichzelf automatisch wanneer ze verbinding maken met die server en laden een profiel.

>[!NOTE]
>
>Voordat u de upgrade uitvoert [!DNL Report Server], zorgt u ervoor dat u de software van de gegevenswerkbank en de profielen die op de gegevenswerkbankserver worden uitgevoerd correct hebt bijgewerkt. Neem voor meer informatie contact op met de Adobe Consulting Services.

Om de volgende procedure uit te voeren, moet u eerst het verbeteringsdossier verkrijgen voor [!DNL Report Server].

**Upgrade uitvoeren naar [!DNL Report Server] 5.4 en latere versies**

1. Maak een back-up van alle bestanden onder [!DNL E:\Portal] en verwijder alle bestanden en mappen in deze map.
1. Kopieer de inhoud van de nieuwe build in [!DNL E:\Portal].
1. Wijzigen [!DNL global.asa], [!DNL email.asp], en [!DNL TopNavigation.xml] volgens de instructies in de voorgaande paragraaf.

1. Kopieer de [!DNL users.mdb] uit uw back-up.

   >[!NOTE]
   >
   >Als u niet eerder rapporten met een .png output produceerde, moet u in de individuele rapportomslagen gaan en wijzigen [!DNL reports.xml] om een rapportformaat van png op te nemen. Anders krijgt u mogelijk een fout van 500. Uw origineel [!DNL reports.xml] zou er ongeveer als volgt uitzien:

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

   Het moet als volgt worden gewijzigd:

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

1. In de [!DNL report.cfg], neemt u de uitvoerindeling png op en slaat u deze op. Als u doorgaat, worden rapporten in png-indeling gegenereerd.

**Upgrade uitvoeren naar [!DNL Report Server] 4,0**

1. Voor de computer van de gegevenswerkbank, kopieer het de verbeteringsdossier van de Server van het Rapport aan [!DNL Temp\Software] map in de directory waarin de gegevenswerkbank is geïnstalleerd.
1. Start de gegevenswerkbank en laad de [!DNL Configuration] profiel.
1. Klik op de knop **[!UICONTROL Configure Connection to Servers]** miniatuur.
1. In de [!DNL Servers Manager], klikt u met de rechtermuisknop op het serverpictogram van de gegevenswerkbank en klikt u op **[!UICONTROL Server Files]**.

1. Open in de map Software de map [!DNL Report Server] map.
1. Klik met de rechtermuisknop op de knop **[!UICONTROL Temp]** vinkje voor [!DNL ReportServer.exe] en selecteert u **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Rapportserver verwijderen {#section-96eb3281c45a45c0a7065deaa6845c25}

**Om te verwijderen[!DNL Report Server]**

1. Registratie van de [!DNL Report Windows] service.

   1. Open een bevelherinnering en navigeer aan de bak subdirectory in de omslag waar u de server van de gegevenswerkbank (InsightServer64.exe.) installeerde. Voorbeeld: [!DNL D:\Adobe\Report\bin]
   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en te verwijderen: [!DNL visualreport /unregserver]

1. Verwijder de installatiemap van Rapportserver.

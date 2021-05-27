---
description: Informatie over de bevordering van en het verwijderen van uw software van de Server van het Rapport.
title: Rapportserver upgraden en verwijderen
uuid: 42f0d190-1a88-424d-be4b-90338144d287
exl-id: 86d0d848-4e2a-45cb-a1b3-b8a856332d33
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Rapportserver{#upgrading-and-uninstalling-report-server} upgraden en verwijderen

Informatie over de bevordering van en het verwijderen van uw software van de Server van het Rapport.

* [Rapport wordt bijgewerkt](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-95fea4bddad74616a8aea450dcdb2282)
* [Rapport wordt verwijderd](../../../home/c-rpt-oview/c-inst-rpt/c-upgrade-uninstall-rpt.md#section-96eb3281c45a45c0a7065deaa6845c25)

## Rapportserver {#section-95fea4bddad74616a8aea450dcdb2282} bijwerken

Als u een upgrade uitvoert naar [!DNL Report Server] 5.4, kunt u de instructies gebruiken om uw [!DNL Report Server]-software bij te werken. Als u [!DNL Report Server] 3.6 of vroeger gebruikt, contacteer Adobe voor hulp met uw verbetering.

Als u [!DNL Report Server] 5.4 wilt upgraden, gebruikt u de gegevenswerkbank om een upgradebestand te kopiëren naar de gegevenswerkbench-server waarmee [!DNL Report Server] verbinding maakt. Hierna upgraden de [!DNL Report] Server-instanties zichzelf automatisch wanneer ze verbinding maken met die server en een profiel laden.

>[!NOTE]
>
>Voordat u [!DNL Report Server] gaat upgraden, moet u controleren of u de software van de gegevenswerkbank en de profielen die op de gegevenswerkbankserver worden uitgevoerd, op de juiste wijze hebt bijgewerkt. Neem voor meer informatie contact op met de Adobe Consulting Services.

Om de volgende procedure uit te voeren, moet u eerst het verbeteringsdossier voor [!DNL Report Server] verkrijgen.

**Bijwerken naar versie  [!DNL Report Server] 5.4 en hoger**

1. Maak een back-up van alle bestanden onder [!DNL E:\Portal] en verwijder alle bestanden en mappen in deze map.
1. Kopieer de inhoud van de nieuwe build naar [!DNL E:\Portal].
1. Wijzig [!DNL global.asa], [!DNL email.asp], en [!DNL TopNavigation.xml] volgens de instructies in de vorige sectie.

1. Kopieer [!DNL users.mdb] van uw steun.

   >[!NOTE]
   >
   >Als u niet eerder rapporten met een .png output produceerde, moet u in de individuele rapportomslagen gaan en [!DNL reports.xml] wijzigen om een rapportformaat van png te omvatten. Anders krijgt u mogelijk een fout van 500. Uw origineel [!DNL reports.xml] zou er ongeveer als volgt uitzien:

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

1. Neem in [!DNL report.cfg] een uitvoerindeling van png op en sla deze op. Als u doorgaat, worden rapporten in png-indeling gegenereerd.

**Upgrade uitvoeren naar  [!DNL Report Server] 4.0**

1. Kopieer op de computer van de gegevenswerkbank het de verbeteringsdossier van de Server van het Rapport aan de [!DNL Temp\Software] omslag in de folder waar de gegevenswerkbank wordt geïnstalleerd.
1. Start de gegevenswerkbank en laad het profiel [!DNL Configuration].
1. Klik op de miniatuur **[!UICONTROL Configure Connection to Servers]**.
1. Klik in [!DNL Servers Manager] met de rechtermuisknop op het serverpictogram van de gegevenswerkbank en klik op **[!UICONTROL Server Files]**.

1. Open in de map Software de map [!DNL Report Server].
1. Klik met de rechtermuisknop op het vinkje **[!UICONTROL Temp]** voor [!DNL ReportServer.exe] en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Rapportserver {#section-96eb3281c45a45c0a7065deaa6845c25} verwijderen

**Om te verwijderen[!DNL Report Server]**

1. Registreer de [!DNL Report Windows]-service niet.

   1. Open een bevelherinnering en navigeer aan de bak subdirectory in de omslag waar u de server van de gegevenswerkbank (InsightServer64.exe.) installeerde. Voorbeeld: [!DNL D:\Adobe\Report\bin]
   1. Bij de bevelherinnering, voer het volgende bevel uit om het als dienst onder Microsoft Windows tegen te houden en te verwijderen: [!DNL visualreport /unregserver]

1. Verwijder de installatiemap van Rapportserver.

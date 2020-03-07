---
description: Het volgende is vereisten en aanbevelingen voor het installeren van het Werkstation (Cliënt) in de Werkbank van Gegevens.
solution: Analytics
title: Vereisten voor werkstations
topic: Data workbench
uuid: 3c4ba2e8-efbc-45fe-8ac1-923d070bc710
translation-type: tm+mt
source-git-commit: 2e4991206394ca0c463210990ea44dfb700341a5

---


# Vereisten voor werkstations{#workstation-requirements}

Het volgende is vereisten en aanbevelingen voor het installeren van het Werkstation (Cliënt) in de Werkbank van Gegevens.

Zie [Serversysteemvereisten](https://docs.adobe.com/help/en/data-workbench/using/server-admin-install/c-msr-server.html) voor aanvullende systeemvereisten voor een werkbank.

>[!IMPORTANT]
>
>De server, de rapportserver, en de cliëntcomponenten worden bevorderd om op de werkende systemen met 64 bits van Vensters te lopen.

**Voordat u begint**

Zorg ervoor dat u de volgende taken hebt voltooid voordat u het werkstation van de Data Workbench (client) installeert:

* **Voeg** ***Uitgesloten Processen*** voor de Bescherming van het Eindpunt van het Centrum van het Systeem van *MS in de Servers* van Vensters 2012 voor de volgende executables toe:

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**
   Dit zal &quot;witte lijst&quot;rechten voor deze het omzetten uitvoerbare voorwerpen toestaan.

* **Installeer Microsoft Excel om analysegegevens uit te voeren.** Om gegevens van werkruimten als dossiers van Microsoft Excel ( [!DNL .xls] of [!DNL .xlsx]) uit te voeren, moet de computer waarop u de Werkbank van Gegevens installeert Excel geïnstalleerd en geregistreerd hebben. Als Excel niet is geregistreerd en de Werkbank van Gegevens probeert om tot het voor het eerst toegang te hebben, toont Excel een vakje van de registratiegroep. Als u niet zeker bent of het exemplaar wordt geregistreerd, begin manueel Excel, en als een doos van de registratiedialoog verschijnt, voltooi het registratieproces.

   >[!NOTE]
   >
   >Met de versie van Werkbank 6.4 van Gegevens, is de steun voor Excel 2007 stopgezet. Ook, omdat de Werkbank van Gegevens slechts op Microsoft Windows voor architectuur met 64 bits loopt, adviseert men dat u ook een versie met 64 bits van Microsoft Excel installeert.

* **Het installeren van Adobe[!DNL Acrobat]voor druk schraapte werkruimten aan PDF.** Om geschraapte werkruimten aan het formaat van Adobe PDF te drukken, moet de computer waarop u de Werkbank van Gegevens installeerde Adobe hebben [!DNL Acrobat] geïnstalleerd.

* **Het verlenen van toegang tot een printer voor drukwerkruimten.** Om werkruimten van de Werkbank van Gegevens te drukken, moet de computer waarop u de Werkbank van Gegevens installeert toegang tot een printer hebben. De Werkbank van gegevens kan werkruimten aan kleur of zwart-wit printers drukken en vereist postscript of andere geavanceerde printereigenschappen niet. Voor optimale resultaten, adviseert Adobe drukwerkruimten in kleur.
* **Veiligheidsmaatregelen uitvoeren.** U zou het normale beleid van de ondernemingsveiligheid van uw bedrijf voor de computers van de Werkbank van Gegevens moeten volgen. Om zijn primaire doeleinden te dienen, vereist de Werkbank van Gegevens slechts de capaciteit om met een server (via havens 80 en 443) en aan om het even welke servers te verbinden die gegevens verzamelen. U kunt de hardware van de Werkbank van Gegevens voor een ander doel gebruiken zolang u de software van de Werkbank van Gegevens handhaaft en minstens 10 GB van opslagruimte voor de Werkbank van Gegevens toewijst.
* Om visualisaties nauwkeurig terug te geven, moet de computer waarop u de werkbank installeert een aangewezen geïnstalleerde **grafiekadapter** hebben (zie de vereisten van de Grafische Adapter hieronder).

**Vereisten voor datacWorkbench-client**

**Besturingssysteem**

* Microsoft Windows 7 64-bits
* Microsoft Windows 8.1 64-bits
* Microsoft Windows 10 64-bits

>[!NOTE]
>
>Windows XP wordt niet gesteund voor Werkbank 6.1 van Gegevens en recentere versies.

**Resolutie**

* Vereist: 1.024 x 768 (XGA)
* Aanbevolen: 1.920 x 1.200 (WUXGA)

**Grafische adapter**

* Vereist: OpenGL hardwareversnelling voor ondersteuning van OpenGL 3.2
* Aanbevolen: Specifieke videoadapter (bijvoorbeeld NVIDIA- of ATI-adapter)

**Processor**

* Vereist: 1,2 GHz of hoger Intel of AMD
* Aanbevolen: ICore 2 Duo-klasse

**RAM**

* Vereist: 2 GB
* Aanbevolen: 4 GB

**Connectiviteit**

* Vereist: 512 Kbps verbinding met DPU
* Aanbevolen: 2Mbps of snellere verbinding aan DPU

**Bestandssysteem**

NTFS

**Schijfopslag**

Ten minste tien (10) GB of meer vrije ruimte op de vaste schijf

**Afdrukken**

Printertoegang (kleurenprinters of grijsschaalprinters) voor het afdrukken van werkruimten en rapporten

**Overige**

* Speciale muis
* Arbeidsomgeving met weinig licht
* Matte monitor


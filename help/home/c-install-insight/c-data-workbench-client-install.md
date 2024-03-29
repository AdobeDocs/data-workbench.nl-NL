---
description: Hieronder vindt u vereisten en aanbevelingen voor het installeren van het werkstation (client) in Data Workbench.
title: Workstationvereisten
uuid: 3c4ba2e8-efbc-45fe-8ac1-923d070bc710
exl-id: 35e259e3-3d6d-45c8-a923-2f8de117489d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Workstationvereisten{#workstation-requirements}

{{eol}}

Hieronder vindt u vereisten en aanbevelingen voor het installeren van het werkstation (client) in Data Workbench.

Zie [Serversysteemvereisten](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/c-msr-server.html?lang=en) voor aanvullende eisen inzake het Data Workbench-systeem.

>[!IMPORTANT]
>
>De server, de rapportserver, en de cliëntcomponenten worden bevorderd om op werkende systemen met 64 bits van Vensters te lopen.

**Voordat u begint**

Zorg ervoor u deze voltooide taken hebt alvorens het Werkstation van de Data Workbench (Cliënt) te installeren:

* **Toevoegen** ***Uitgesloten processen*** for *MS System Center Endpoint Protection in Windows 2012 Servers* voor de volgende uitvoerbare bestanden:

   * **[!DNL InsightServer64.exe]**
   * **[!DNL ReportServer.exe]**
   * **[!DNL ExportIntegration.exe]**

   Dit zal de rechten van de lijst van gewenste personen voor deze interface uitvoerbare voorwerpen toelaten.

* **Installeer Microsoft Excel om analysegegevens te exporteren.** Gegevens uit werkruimten exporteren als Microsoft Excel ( [!DNL .xls] of [!DNL .xlsx]), moet Excel zijn geïnstalleerd en geregistreerd op de computer waarop u Data Workbench installeert. Als Excel niet is geregistreerd en de Data Workbench probeert om tot het voor het eerst toegang te hebben, toont Excel een registratiedialoogdoos. Als u niet zeker weet of de kopie is geregistreerd, start u Excel handmatig en als er een dialoogvenster voor registratie wordt weergegeven, voltooit u het registratieproces.

   >[!NOTE]
   >
   >Met de versie van Data Workbench 6.4, is de steun voor Excel 2007 gestopt. Bovendien, omdat de Data Workbench slechts op Microsoft Windows voor architectuur met 64 bits loopt, adviseert men dat u ook een versie met 64 bits van Microsoft Excel installeert.

* **Adobe installeren [!DNL Acrobat] voor het afdrukken van geschaalde werkruimten naar PDF.** Als u geschaalde werkruimten wilt afdrukken naar de Adobe PDF-indeling, moet de computer waarop u de Data Workbench hebt geïnstalleerd, over Adobe beschikken [!DNL Acrobat] geïnstalleerd.

* **Toegang tot een printer bieden voor het afdrukken van werkruimten.** Voor het afdrukken van werkruimten vanuit Data Workbench, moet de computer waarop u Data Workbench installeert, toegang hebben tot een printer. Data Workbench kunnen werkruimten afdrukken op kleuren- of monochrome printers en hebben geen postscript- of andere geavanceerde printerfuncties nodig. Voor optimale resultaten raadt Adobe aan werkruimten in kleur af te drukken.
* **Beveiligingsmaatregelen uitvoeren.** U zou het normale beleid van de ondernemingsveiligheid voor de computers van de Data Workbench van uw bedrijf moeten volgen. Om zijn primaire doeleinden te dienen, vereist de Data Workbench slechts de capaciteit om met een server (via havens 80 en 443) en aan om het even welke servers te verbinden die gegevens verzamelen. U kunt de hardware van de Data Workbench voor elk ander doel gebruiken zolang u de software van de Data Workbench handhaaft en minstens 10 GB opslagruimte voor Data Workbench toewijst.
* Om de visualisaties correct te renderen, moet de computer waarop u de werkbank installeert een aangewezen hebben **grafische adapter** geïnstalleerd (zie hieronder de vereisten voor grafische adapters).

**Vereisten voor Data Workbench-client**

**Besturingssysteem**

* Microsoft Windows 7 64-bits
* Microsoft Windows 8.1 64-bits
* Microsoft Windows 10 64-bits

>[!NOTE]
>
>Windows XP wordt niet ondersteund voor Data Workbench 6.1 en latere versies.

**Resolutie**

* Vereist: 1024 x 768 (XGA)
* Aanbevolen: 1.920 x 1.200 (WUXGA)

**Grafische adapter**

* Vereist: OpenGL-hardwareversnelling ter ondersteuning van OpenGL 3.2
* Aanbevolen: Speciale grafische kaart (bijvoorbeeld NVIDIA- of ATI-adapter)

**Processor**

* Vereist: 1,2 GHz of hoger Intel of AMD
* Aanbevolen: ICore 2 duo-klasse

**RAM**

* Vereist: 2 GB
* Aanbevolen: 4 GB

**Connectiviteit**

* Vereist: 512 Kbps verbinding aan DPU
* Aanbevolen: 2Mbps of snellere verbinding aan DPU

**Bestandssysteem**

NTFS

**Schijfopslag**

Minimaal tien (10) GB of meer vrije ruimte op de vaste schijf

**Afdrukken**

Printertoegang (kleuren- of grijswaardenprinters) voor het afdrukken van werkruimten en rapporten

**Overige**

* Speciale muis
* Lage-glare werkomgeving
* Matte monitor

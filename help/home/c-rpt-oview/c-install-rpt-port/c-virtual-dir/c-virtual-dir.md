---
description: Om het Portaal van het Rapport te vormen, moet u zijn toepassingsdossiers aan virtuele folders in kaart brengen.
title: Wijs de Poortpagina's van het Rapport aan Virtuele Folders toe
uuid: 75ca85d5-d526-48f9-b2c4-ca77c903c6af
exl-id: 13e457d4-7039-491a-a65d-f23ad7e9fe77
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# Wijs de Poortpagina&#39;s van het Rapport aan Virtuele Folders toe{#map-the-report-portal-pages-to-virtual-directories}

{{eol}}

Om het Portaal van het Rapport te vormen, moet u zijn toepassingsdossiers aan virtuele folders in kaart brengen.

Een virtuele folder bepaalt het adres dat browser de cliënten gebruiken om van een fysieke middel op de IIS toepassingsserver de plaats te bepalen. Toegang tot [!DNL Report Portal], wijzen de cliënten hun browsers aan de virtuele folder die u aan het portaal toewijst.

De naam van de virtuele map die u toewijst aan [!DNL Report Portal] moet de naam aanpassen die u voor de omslag VSVirtualPortalName in Stap 3 van de vorige sectie gebruikte. Als u bijvoorbeeld &quot;Portal&quot; wilt gebruiken als naam voor uw [!DNL Report Portal], moet u de bestanden van de portal toewijzen aan een virtuele map met de naam &quot;Portal&quot;. In het volgende voorbeeld wordt de URI weergegeven die clients zouden gebruiken om toegang te krijgen tot een [!DNL Report Portal] toegewezen aan de virtuele map [!DNL VisualReportPortal] op een server met de naam myWebServer:

[!DNL https://myWebServer/VisualReportPortal]

In de volgende procedures wordt beschreven hoe u de kaart kunt toewijzen [!DNL Report Portal] aan een virtuele folder op IIS 5.0, 6.0, en 7.0 of hoger.

Volg de reeks procedures voor de versie van IIS die u gebruikt:

* [Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 7.0)](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-7.md#concept-9fc9595bb83147238965be4832df0a08)
* [Het Portaal van het Rapport van de toewijzing aan een Virtuele Folder (IIS 5.0)](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-5.md#concept-402cb33c50d640e480098517140ffc74)
* \ [Het sessieconfiguratiebestand bewerken](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7)

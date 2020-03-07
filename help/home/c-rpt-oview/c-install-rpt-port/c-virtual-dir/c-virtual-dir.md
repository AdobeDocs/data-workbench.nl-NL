---
description: Om het Portaal van het Rapport te vormen, moet u zijn toepassingsdossiers aan virtuele folders in kaart brengen.
solution: Analytics
title: Breng de Poortpagina's van het Rapport aan Virtuele Folders in kaart
topic: Data workbench
uuid: 75ca85d5-d526-48f9-b2c4-ca77c903c6af
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Breng de Poortpagina&#39;s van het Rapport aan Virtuele Folders in kaart{#map-the-report-portal-pages-to-virtual-directories}

Om het Portaal van het Rapport te vormen, moet u zijn toepassingsdossiers aan virtuele folders in kaart brengen.

Een virtuele folder bepaalt het adres dat browser cliënten gebruiken om van een fysiek middel op de IIS toepassingsserver de plaats te bepalen. Om toegang te hebben [!DNL Report Portal], richten de cliënten hun browsers aan de virtuele folder die u aan het portaal toewijst.

De naam van de virtuele folder die u toewijst aan [!DNL Report Portal] moet de naam aanpassen die u voor de omslag VSVirtualPortalName in Stap 3 van de vorige sectie gebruikte. Bijvoorbeeld, als u &quot;Portaal&quot;als naam van uw wilt gebruiken, moet u de dossiers van het portaal aan een virtuele folder in kaart brengen genoemd &quot;Portaal.&quot; [!DNL Report Portal] Het volgende voorbeeld toont URI dat de cliënten zouden gebruiken om tot een [!DNL Report Portal] toegewezen aan de virtuele folder [!DNL VisualReportPortal] op een server toegang te hebben genoemd myWebServer:

[!DNL http://myWebServer/VisualReportPortal]

De volgende procedures beschrijven hoe te om [!DNL Report Portal] aan een virtuele folder op IIS 5.0, 6.0, en 7.0 in kaart te brengen of hoger.

Volg de reeks procedures voor de versie van IIS die u gebruikt:

* [Het Portaal van het Rapport van de afbeelding aan een Virtuele Folder (IIS 7.0)](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-7.md#concept-9fc9595bb83147238965be4832df0a08)
* [Het Portaal van het Rapport van de afbeelding aan een Virtuele Folder (IIS 5.0)](../../../../home/c-rpt-oview/c-install-rpt-port/c-virtual-dir/c-map-rpt-port-vdir-5.md#concept-402cb33c50d640e480098517140ffc74)
* \ [Geef het Dossier van de Configuratie van de Zitting uit](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7)


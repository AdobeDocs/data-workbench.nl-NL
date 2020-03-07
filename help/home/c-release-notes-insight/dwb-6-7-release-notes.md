---
description: Nieuwe eigenschappen, moeilijke situaties, en bekende kwesties in Werkbank 6.7 van Gegevens.
title: Data Workbench 6.7 Release Notes
uuid: b84f5f2b-4f1c-490c-982b-6bd8d3a63e25
translation-type: tm+mt
source-git-commit: 2cba66a160fec9154796f093d04a422a5b0da265

---


# Data Workbench 6.7 Release Notes{#data-workbench-release-notes}

Nieuwe eigenschappen, moeilijke situaties, en bekende kwesties in Werkbank 6.7 van Gegevens.

## Data Workbench 6.7 Release Notes {#topic-7655534554ac4a4b816af1bd73b06aad}

Nieuwe eigenschappen, moeilijke situaties, en bekende kwesties in Werkbank 6.7 van Gegevens.

## Nieuwe eigenschappen in Versie 6.7 {#section-8bd7a36ac3a24b8497a9ea9724e0d750}

**Nieuw authentificatiemodel voor het Werkstation van de Werkbank van Gegevens (integratie IMS)**

Het Werkstation van de Werkbank van gegevens steunt nu gebruikersauthentificatie door gebruikersbenaming en wachtwoord. Met deze nieuwe methode kunnen beheerders hun eigen gebruikersaccounts maken en beheren, waardoor het niet nodig is contact op te nemen met de klantenservice.

Voor meer informatie, zie [zelf-Levering van Gebruikers](https://docs.adobe.com/content/help/en/data-workbench/using/client/c-self-provisioning-users.html).

**Opzoeken van bestanden met platte opnamen**

Het Werkstation van de Werkbank van gegevens steunt nu gebruikersauthentificatie door gebruikersbenaming en wachtwoord. Met deze nieuwe methode kunnen beheerders hun eigen gebruikersaccounts maken en beheren, waardoor het niet nodig is contact op te nemen met de klantenservice.

De vlakke dossierraadpleging laadde eerder het volledige dossier in in-geheugenbuffers, opblaasend geheugengebruik en creërend prestatieskwesties voor andere subsystemen. De dossiers kunnen nu geheugen in kaart gebracht en in het voorgeheugen ondergebracht in Vensters zijn, optimaliserend geheugengebruik door de Geheugen in kaart gebrachte Dossiers *van de Raadpleging aan waar in te plaatsen* [!DNL MemorySettings.cfg].

Voor meer informatie, zie [zelf-Levering van Gebruikers](https://docs.adobe.com/content/help/en/data-workbench/using/client/c-self-provisioning-users.html).

**Geheugengebruik**

Het grote gebruik van de Pagina kan nu worden onbruikbaar gemaakt door de Grote Pagina&#39;s *van het* Gebruik aan vals in te plaatsen [!DNL MemorySettings.cfg]. Zie Geheugengebruik [](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/admin-dwb-server/t-mntr-mry-usg.html) controleren voor meer informatie.

**Beveiligingscifers**

Toegevoegde steun voor ECDHE en DHE.

E-mailondersteuning in [!DNL User List.cfg]

Extra ondersteuning voor e-mailkenmerken in [!DNL User List.cfg]. Voor meer informatie, zie het Beleid van de [Gebruiker van de Leden](https://docs.adobe.com/help/en/data-workbench/using/server-admin-install/admin-dwb-server/access-control/dwb-self-admin-member-access.html)van de Groep.

**Menu Help**

Het menu van de hulp toont nu een kortere weg om de folder van Certificaten te openen.

**`TargetBulkUpload`exporteren **

URLs zal aan het eind van het de spoordossier van de uitvoer en het `targetbulkuploadexportname.log.completed` dossier worden verstrekt om het verslag van vastgelopen partijen te volgen.

Een nieuw dossier, [!DNL TargetBulkUpload.cfg], is verstrekt om het Maximum interval van de Onderbreking (in notulen) te vormen. Het dossier wordt gevonden in [!DNL Server\Admin\Export\].

## Fixes {#section-160baf6ea04c45a993777ee4260691ed}

* Vast een kwestie waar de de Klickthrough van de Campagne dimensie opgeblazen waarden toonde.
* Vast een kwestie met het produceren van Excel dossiers van de rapportserver.
* RC4 de cipher is nu gehandicapt door gebrek.
* Vaste een kwestie veroorzakend het werkstation van de Werkbank van Gegevens om te crashen wanneer het toevoegen van een afmetingselement aan een lijst van de waardelegende.
* Vaste een kwestie met de Werkbank van Gegevens aan de uitvoer van AAM die onderbrekingen veroorzaakte.
* Vaste een kwestie veroorzakend het werkstation van de Werkbank van Gegevens om te botsen wanneer een gebruiker zonder voldoende toegangsniveau de werkruimte aan Server bewaarde.
* Vast een kwestie met het datumformaat in [!DNL report.cfg] die onjuist of niet gelokaliseerd zijn.
* Vast een kwestie met de mobiele en productrijen in de voer AVRO die verwarrende informatie tonen.
* Vaste een kwestie die het opdracht geven tot van `*.1cd` en `*.1ad` dossiers in verhinderde [!DNL order.txt].

* De voorlegging aan de optie van de Server is onbruikbaar gemaakt voor het algoritme van de Maximalisering van de Verwachting terwijl het lopen het Groeperen.
* Vaste een kwestie met het uitvoerbare `TargetBulkUpload` stalling en het nalaten om volledig te lopen.

## Bekende problemen {#section-d76322bdac5043f087ab303dc68b8fff}

* Bij logout, wordt het [!DNL user cache.db] dossier schoongemaakt.
* IMS-e-mailadressen met &#39;+&#39; of &#39;%&#39; tekens worden niet ondersteund.
* De gebruiker kan zich niet aanmelden tijdens een fout in de verbindingsstatus. Als alternerende actie, logout op off-line wijze.
* Het login venster IMS geeft niet behoorlijk op sommige hardware met hoge resolutie en hoge DPI terug. Als alternerende actie, klik met de rechtermuisknop aan [!DNL Insight.exe] en navigeer aan **[!UICONTROL Properties]** > **[!UICONTROL Compatability]**, dan controleer de doos **[!UICONTROL Override high DPI scaling behavior]**.

## Upgradevereisten {#section-b74adf981ac8446a8d7ffcdc4e9cf939}

1. Update [!DNL trust_ca_cert.pem] op de Servers van het Inzicht die deel van bouwstijlpakket uitmaakt.
1. Het certificaat van de Server van de update en van de Server van het Rapport door nieuwe certificaten van [https://aap.adobe.com](https://aap.adobe.com)te downloaden.
1. Om Werkstation en de Server van het Rapport automatisch bij te werken, werk manueel [!DNL trust_ca_cert.pem] voor allebei bij door het van de Server van de Vergunning te downloaden.
1. De automatische updateeigenschap van de sensor vereist versie 5.0 om met versie 6.70 van de Server van het Inzicht te communiceren. Ook, [!DNL trust_ca_cert.pem] moet Sensor manueel worden bijgewerkt door het van de Server van de Vergunning te downloaden.

## Systeemupdates {#section-c1b4949ea734440aa62658ac313261db}

De nieuwe dossiers omvatten:

1. [!DNL Server\Admin\Export\TargetBulkUpload.cfg]
1. [!DNL Server\Components for Processing Servers\MemorySettings.cfg]
1. [!DNL Server\Components\MemorySettings.cfg]

De bijgewerkte dossiers omvatten:

1. [!DNL trust_ca_cert.pem] voor alle onderdelen.
1. [!DNL Access Control.cfg] om configuratie te steunen IMS.
1. [!DNL Base\Context\meta.cfg] voor het steunen van de formaten van de Datum van het Begin en van de Einddatum in [!DNL Report.cfg]

1. Toevoegingen aan [!DNL Insight.cfg] om volmacht voor authentificatie te steunen IMS:

   ```
   IMS Proxy Info = IMSProxyInfo: 
     Proxy Password = EncryptedString:
     Proxy User Name = string:
   ```

Zie de [gearchiveerde versienota&#39;s](https://docs.adobe.com/content/help/en/data-workbench/using/release-notes/release-notes.html) voor Werkbank van Gegevens 5.3 tot 5.52.

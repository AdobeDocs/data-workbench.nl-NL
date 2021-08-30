---
description: Nieuwe functies, oplossingen en bekende problemen in Data Workbench 6.7.
title: Opmerkingen bij de release Data Workbench 6.7
uuid: b84f5f2b-4f1c-490c-982b-6bd8d3a63e25
exl-id: e5ec3224-66d1-47a6-9bf3-8be9f6568b8d
source-git-commit: 050468bf6a9ef9c07719ded79c8ab68753d58647
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 0%

---

# Opmerkingen bij de release Data Workbench 6.7{#data-workbench-release-notes}

Nieuwe functies, oplossingen en bekende problemen in Data Workbench 6.7.

## Opmerkingen bij de release Data Workbench 6.7 {#topic-7655534554ac4a4b816af1bd73b06aad}

Nieuwe functies, oplossingen en bekende problemen in Data Workbench 6.7.

## Nieuwe functies in Release 6.7 {#section-8bd7a36ac3a24b8497a9ea9724e0d750}

**Nieuw verificatiemodel voor Data Workbench Workstation (IMS-integratie)**

Het Werkstation van de Data Workbench steunt nu gebruikersauthentificatie door gebruikersbenaming en wachtwoord. Met deze nieuwe methode kunnen beheerders hun eigen gebruikersaccounts maken en beheren, zodat er geen contact hoeft te worden opgenomen met de klantenservice.

Voor meer informatie, zie [Zelfinrichting van Gebruikers](https://experienceleague.adobe.com/docs/data-workbench/using/client/c-self-provisioning-users.html).

**Platte bestandsopzoekhandeling**

Het Werkstation van de Data Workbench steunt nu gebruikersauthentificatie door gebruikersbenaming en wachtwoord. Met deze nieuwe methode kunnen beheerders hun eigen gebruikersaccounts maken en beheren, zodat er geen contact hoeft te worden opgenomen met de klantenservice.

Bij een platte bestandsopzoekopdracht werd het gehele bestand eerder in geheugenbuffers geladen, waardoor het geheugengebruik opliep en er prestatieproblemen voor andere subsystemen ontstaan. De bestanden kunnen nu worden toegewezen aan geheugen en in cache worden geplaatst in Windows, zodat het geheugengebruik wordt geoptimaliseerd door *Toegewezen opzoekbestanden voor geheugen in te stellen op true in [!DNL MemorySettings.cfg].*

Voor meer informatie, zie [Zelfinrichting van Gebruikers](https://experienceleague.adobe.com/docs/data-workbench/using/client/c-self-provisioning-users.html).

**Geheugengebruik**

Het gebruik van grote pagina&#39;s kan nu worden uitgeschakeld door *Grote pagina&#39;s gebruiken* in te stellen op false in [!DNL MemorySettings.cfg]. Zie [Geheugenverbruik controleren](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/admin-dwb-server/t-mntr-mry-usg.html) voor meer informatie.

**Beveiligingscifers**

Toegevoegde steun voor ECDHE en DHE.

E-mailondersteuning in [!DNL User List.cfg]

Toegevoegde ondersteuning voor E-mailkenmerk in [!DNL User List.cfg]. Voor meer informatie, zie [Gebruikersbeheer van Groepsleden](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/admin-dwb-server/access-control/dwb-self-admin-member-access.html?lang=en).

**Menu Help**

In het menu Help ziet u nu een snelkoppeling naar de map Open Certificates.

**`TargetBulkUpload`export**

URLs zal aan het eind van het de spoordossier van het de uitvoer en `targetbulkuploadexportname.log.completed` dossier worden verstrekt om het verslag van vastgezette partijen te volgen.

Er is een nieuw bestand, [!DNL TargetBulkUpload.cfg], opgegeven voor het configureren van het maximale time-outinterval (in minuten). Het bestand staat in  [!DNL Server\Admin\Export\].

## Oplossingen {#section-160baf6ea04c45a993777ee4260691ed}

* Probleem verholpen waarbij de Campagne Clickthrough-dimensie opgewekte waarden liet zien.
* Probleem verholpen met het genereren van Excel-bestanden vanaf de rapportserver.
* RC4-versleuteling is nu standaard uitgeschakeld.
* Probleem verholpen waarbij het werkstation van de Data Workbench vastliep bij het toevoegen van een dimensie-element aan een waardelegendetabel.
* Probleem opgelost met Data Workbench op AAM export die tot onderbrekingen leidde.
* Probleem verholpen waarbij het werkstation van de Data Workbench vastliep wanneer een gebruiker zonder voldoende toegangsniveau de werkruimte naar de server had opgeslagen.
* Probleem verholpen waarbij de datumnotatie in [!DNL report.cfg] onjuist of niet gelokaliseerd was.
* Probleem verholpen waarbij verwarrende informatie werd weergegeven op de mobiele rijen en de productrijen in de AVRO-feed.
* Probleem verholpen waarbij de volgorde van `*.1cd`- en `*.1ad`-bestanden in [!DNL order.txt] werd voorkomen.

* De optie Verzenden naar server is uitgeschakeld voor het algoritme voor maximalisatie van verwachtingen tijdens het uitvoeren van clustering.
* Probleem verholpen waarbij het uitvoerbare bestand `TargetBulkUpload` niet volledig kon worden uitgevoerd.

## Bekende problemen {#section-d76322bdac5043f087ab303dc68b8fff}

* Bij het afmelden wordt het [!DNL user cache.db]-bestand schoongemaakt.
* E-mailadressen van IMS-gebruikers met de tekens &#39;+&#39; of &#39;%&#39; worden niet ondersteund.
* Gebruiker kan zich niet afmelden tijdens een fout in de verbindingsstatus. Meld u af in de offlinemodus als tijdelijke oplossing.
* Het IMS-aanmeldvenster wordt niet correct weergegeven bij bepaalde hardware met hoge resolutie en hoge DPI. Als tussenoplossing klikt u met de rechtermuisknop op [!DNL Insight.exe] en navigeert u naar **[!UICONTROL Properties]** > **[!UICONTROL Compatability]**. Schakel vervolgens het selectievakje **[!UICONTROL Override high DPI scaling behavior]** in.

## Upgradevereisten {#section-b74adf981ac8446a8d7ffcdc4e9cf939}

1. Werk [!DNL trust_ca_cert.pem] op de Servers van het Inzicht bij die deel van bouwstijlpakket uitmaken.
1. Het certificaat van de Server van de update en van de Server van het Rapport door nieuwe certificaten van [https://aap.adobe.com](https://aap.adobe.com) te downloaden.
1. Als u het werkstation en de rapportserver automatisch wilt bijwerken, werkt u [!DNL trust_ca_cert.pem] voor beide handmatig bij door het te downloaden vanaf de licentieserver.
1. De automatische updatefunctie van de sensor vereist versie 5.0 om met versie 6.70 van de Server van het Inzicht te communiceren. Daarnaast moet de [!DNL trust_ca_cert.pem] van de sensor handmatig worden bijgewerkt door deze te downloaden van de licentieserver.

## Systeemupdates {#section-c1b4949ea734440aa62658ac313261db}

Nieuwe bestanden zijn:

1. [!DNL Server\Admin\Export\TargetBulkUpload.cfg]
1. [!DNL Server\Components for Processing Servers\MemorySettings.cfg]
1. [!DNL Server\Components\MemorySettings.cfg]

Bijgewerkte bestanden zijn:

1. [!DNL trust_ca_cert.pem] voor alle componenten.
1. [!DNL Access Control.cfg] om IMS-configuratie te ondersteunen.
1. [!DNL Base\Context\meta.cfg] voor ondersteuning van de indelingen Begindatum en Einddatum in  [!DNL Report.cfg]

1. Toevoegingen aan [!DNL Insight.cfg] om volmacht voor authentificatie te steunen IMS:

   ```
   IMS Proxy Info = IMSProxyInfo: 
     Proxy Password = EncryptedString:
     Proxy User Name = string:
   ```

Zie [gearchiveerde releaseopmerkingen](https://experienceleague.adobe.com/docs/data-workbench/using/release-notes/release-notes.html) voor Data Workbench 5.3 tot en met 5.52.

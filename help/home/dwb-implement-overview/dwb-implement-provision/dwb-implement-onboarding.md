---
description: Voer de volgende stappen uit om het instapproces voor Adobe Data Workbench (DWB), een onderdeel van Adobe Analytics Premium (AAP), te starten.
title: Basisinstructies aan boord voor DWB Managed Services
uuid: ad44a4eb-00ea-49c7-8401-58976d8fe39e
exl-id: 49fb6afe-b417-4554-9238-fd6381c00029
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# Basisinstructies aan boord voor DWB Managed Services{#basic-onboarding-instructions-for-dwb-managed-services}

Voer de volgende stappen uit om het instapproces voor Adobe Data Workbench (DWB), een onderdeel van Adobe Analytics Premium (AAP), te starten.

Deze instapinstructies zijn bedoeld voor klanten die Data Workbench implementeren met één rapportsuite die services met Adobe-beheer gebruikt zonder services te raadplegen. Als u een nieuwe klant bent van het AAP die DWB implementeert, zal het Adobe Onboarding team uw eerste contact zijn. Als u een upgrade uitvoert vanaf de Adobe Analytics-standaard of een eerdere versie van DWB, helpt een Adobe Customer Success Manager u.

## Info aan boord: Wat wij van u nodig hebben {#section-bdeb9aa26dc14e45a6c90920832becaa}

Adobe zal contact met u opnemen om:

* Identificeer een Primaire Gebruiker voor DWB om een certificaat specifiek voor die gebruiker op de netwerkfolder te produceren. De primaire gebruiker zal ook als puntpersoon handelen om met de Zorg van de Klant van Adobe in wisselwerking te staan.
* Identificeer de rapportreeks die in DWB moet worden geladen.

De Adobe Digital Marketing-teams gebruiken vervolgens uw gegevens om profielen te maken, accounts in te stellen en een configuratiebestand voor DWB te leveren.

**Adobe aan boord nemen van taken**

* Adobe Customer Care maakt een DWB-account met licentie. De klantenservice van Adobe genereert een DWB-certificaat voor de primaire gebruiker.
* De klantendienst van Adobe bepaalt de primaire gebruiker als &quot;gesteunde gebruiker,&quot;de persoon die voor gesteunde vraag en probleemresolutie wordt geïdentificeerd.
* De klantenservice van Adobe laadt het softwarepakket naar de DWB-licentie en softwareportal (SoftDocs/Software en Docs-profiel) om naar uw organisatie te worden gedownload.
* Het team van Adobe TechOps bereidt de milieu&#39;s van de Productie en van de Ontwikkeling en hun profielen (per contract) voor DWB voor.
* Adobe TechOps-team configureert gegevensfeeds en scripts voor profielbeheer.
* Het team van TechOps van Adobe creeert en verzendt het DWB- configuratiedossier (Insight.cfg) naar het Adobe Onboarding team verantwoordelijk voor aan boord komende taken verbonden aan uw organisatie.

Na het aanpassen van uw gegevensvoer en het produceren van geloofsbrieven, certificaten, en een profielconfiguratie, zal de Zorg van de Klant van de Adobe uw configuratiedossier en geloofsbrieven verzenden om de volgende stap te nemen.

## Toegang tot uw aangepaste installatiebestanden {#section-26962bf57fef435dbd1c5486d4b6f688}

U ontvangt deze installatiebestanden van de klantenservice van Adobe om het DWB-werkstation op uw clientcomputer te installeren.

* Uw aangepaste DWB-configuratiebestand (Insight.cfg)

   Dit configuratiebestand op de clientcomputer bevat verbindingen met uw beheerde DWB-servers.

* Aanmeldingsgegevens waarmee de Licentieportal de wizard DWB Setup en het vereiste certificaat (.pem-bestand) kan downloaden met de naam van uw primaire gebruiker.

**Aanvullende instellingsbestanden downloaden**

1. Bladeren naar: license.visualsciences.com om u vergunningscertificaat en uitvoerbaar DWB van de Tovenaar van de Opstelling te downloaden.
1. Voer uw organisatie (accountnaam), de naam van de primaire gebruiker en het wachtwoord in dat u van de klantenservice van Adobe hebt ontvangen en klik op aanmelden.

   >[!NOTE]
   >
   >Mogelijk wordt u in uw browser gevraagd om nu een digitaal certificaat voor te leggen. Als dit het geval is, klikt u op Annuleren om het dialoogvenster te sluiten.

1. Zoek het certificaat dat is uitgegeven voor uw exemplaar van Adobe Data Workbench (`<PrimaryUser>`.pem) in de sectie Downloads en download.
1. Zoek het standaardinstallatieprogramma voor clients in de sectie Downloads om de wizard DWB Setup (InsightSetup-x.xx.exe-bestand) te downloaden.
1. Nadat u bestanden van de klantenservice van Adobe hebt ontvangen en gedownload, voert u de wizard DWB Setup uit om de werkstationsoftware op de clientcomputer te installeren.

>[!NOTE]
De tovenaar van de Opstelling DWB zal u door installatie van het DWB cliëntwerkstation lopen en zal helpen van Insight.cfg en `<PrimaryUser>`.pem dossiers de plaats bepalen in de vereiste omslagen te plaatsen. Het Insight.cfg- dossier verblijft met het Insight.exe- dossier in uw geïnstalleerd cliëntwerkstation. Het bestand `<PrimaryUser>`.pem bevindt zich in de map Certificates met het bestand trust_ca_cert.pem. DWB werkt alleen als alle certificaat- en configuratiebestanden aanwezig zijn.

Voor extra informatie, zie [DWB Tovenaar van de Opstelling](https://experienceleague.adobe.com/docs/data-workbench/using/install/workstation-setup/install-setup.html).

## Verbinding maken met uw DWB-servers {#section-8e79c4e07c2a4342a5bb8af6ee7be3c9}

Uw beheerde servers worden geïdentificeerd in het Insight.cfg- dossier dat u van de Zorg van de Klant van Adobe ontvangt en op uw cliëntwerkstation verblijft. Adobe TechOps stelt uw servers in en de klantenservice van Adobe voegt verwijzingen naar deze beheerde servers en profielen toe aan het bestand Insight.cfg voordat deze naar u worden verzonden. (De Configure verbindingen aan server in stap 12 van de documentatie van de Tovenaar van de Opstelling DWB zullen worden voltooid.)

>[!NOTE]
In de werkruimte Werkstationconfiguratie op het DWB-clientwerkstation kunt u de aangesloten servers en profielen bekijken.

**Beheerde services van Adobe**

・ Adobe TechOps beheert de infrastructuur inclusief netwerk, datacenter, servers en opslag. De controle van de infrastructuur en de reactie op alarm komt op een 24x7 basis voor alarm voor vereist actie TechOps. Voor andere waarschuwingen zal TechOps de klantendienst van Adobe op de hoogte brengen om met u te coördineren.

・ Adobe TechOps zal onderhoud en ingebouwde programmatuurupdates voor uw beheerde servers uitvoeren. Voor onderhoud dat uitvaltijd veroorzaakt, ontvangt u minimaal twee weken van tevoren meldingen van de klantenservice voor onderhoudsvensters. Adobe TechOps zal aan directe behoeften zo snel mogelijk richten. De kennisgeving hangt af van de urgentie en zal worden opgelost zodra het schema bekend is.

・ Adobe TechOps plaatst opstelling een geplande taak om gegevens automatisch te beheren. De gegevens van de analytische feed worden naar DWB verplaatst voor verwerking en omzetting elke avond vanaf 21:00 de tijd van de rapportsuite.

・ Adobe TechOps verwerkt indien nodig andere door Adobe beheerde services, zoals gegevensback-ups, FTP-accounts, gegevensarchivering en gegevensoverdracht.

・ Adobe TechOps zal de primaire productiecluster vormen om drie maanden rolgegevens te bevatten die maandelijks worden teruggesteld en opnieuw verwerkt. De updates aan raadplegingen (Geografie, DeviceAtlas, Standaard Classificaties) zullen ook als deel van de opwerkingstaak voorkomen. Standaard wordt de taak uitgevoerd op de eerste vrijdag van elke maand. Indien nodig kan het schema door de klantenservice worden gewijzigd.

Neem voor aanvullende informatie contact op met [Adobe Klantenservice](https://helpx.adobe.com/support/programs/enterprise-support-terms.html).

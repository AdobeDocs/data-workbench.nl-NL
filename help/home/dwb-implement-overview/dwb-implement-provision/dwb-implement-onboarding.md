---
description: Volg deze stappen om het instapproces voor de Werkbank van de Gegevens van Adobe (DWB), een component van de Premium van de Analyse van Adobe (AAP) te beginnen.
title: Basisinstructies aan boord voor DWB Managed Services
uuid: ad44a4eb-00ea-49c7-8401-58976d8fe39e
translation-type: tm+mt
source-git-commit: ded50c4eeadea80156c17a4cad985d0ceddd5500

---


# Basisinstructies aan boord voor DWB Managed Services{#basic-onboarding-instructions-for-dwb-managed-services}

Volg deze stappen om het instapproces voor de Werkbank van de Gegevens van Adobe (DWB), een component van de Premium van de Analyse van Adobe (AAP) te beginnen.

Deze onboarding instructies zijn voor klanten die de Werkbank van Gegevens met één enkele rapportreeks uitvoeren gebruikend de beheerde diensten van Adobe zonder de diensten te raadplegen. Als u een nieuwe klant bent die van het AAP DWB uitvoert, zal Adobe Onboarding team uw eerste contact zijn. Als bevordering van de norm van de Analyse van Adobe of van een vroegere versie van DWB, zal een Manager van het Succes van de Klant van Adobe u helpen.

## Gegevens aan boord: Wat wij van u nodig hebben {#section-bdeb9aa26dc14e45a6c90920832becaa}

Adobe zal u contacteren aan:

* Identificeer een Primaire Gebruiker voor DWB om een certificaat specifiek voor die gebruiker op de netwerkfolder te produceren. De primaire gebruiker zal ook als puntpersoon handelen om met de Zorg van de Klant van Adobe in wisselwerking te staan.
* Identificeer de rapportreeks die in DWB moet worden geladen.

De digitale de Marketing teams van Adobe zullen dan uw informatie nemen om profielen tot stand te brengen, rekeningen te plaatsen, en een configuratiedossier voor DWB te leveren.

**Adobe On-boarding Taken**

* De Zorg van de Klant van Adobe leidt tot een DWB vergunning gegeven rekening. De Zorg van de Klant van Adobe produceert een DWB- certificaat voor de primaire gebruiker.
* De Zorg van de Klant van Adobe bepaalt de primaire gebruiker als &quot;gesteunde gebruiker,&quot;de persoon die voor gesteunde vraag en probleemresolutie wordt geïdentificeerd.
* De Klantzorg van Adobe laadt softwarepakket aan de DWB- vergunning en softwareportaal (SoftDocs/Software en het profiel van Dokken) om aan uw organisatie worden gedownload.
* Het team van Adobe TechOps bereidt de milieu&#39;s van de Productie en van de Ontwikkeling en hun profielen (per contract) voor DWB voor.
* Het team van Adobe TechOps vormt gegevensvoer en de manuscripten van het profielbeheer.
* Het team van Adobe TechOps creeert en verzendt het DWB configuratiedossier (Insight.cfg) naar het team van Adobe Onboarding verantwoordelijk voor aan boord plaatsende taken verbonden aan uw organisatie.

Na het aanpassen van uw gegevensvoer en het produceren van geloofsbrieven, certificaten, en een profielconfiguratie, zal de Zorg van de Klant van Adobe uw configuratiedossier en geloofsbrieven verzenden om de volgende stap te nemen.

## Heb toegang tot uw Douane installeert Dossiers {#section-26962bf57fef435dbd1c5486d4b6f688}

U zult deze opstellingsdossiers van de Zorg van de Klant van Adobe ontvangen om het Werkstation DWB op uw cliëntcomputer te installeren.

* Uw douaneDWB configuratiedossier (Insight.cfg)

   Dit configuratiedossier op de cliëntcomputer zal verbindingen aan uw beheerde servers DWB omvatten.

* Login geloofsbrieven voor het Portaal van het Verlenen van vergunningen om de Tovenaar van de Opstelling DWB en vereiste certificaat (.pem dossier) met de naam van uw primaire gebruiker te downloaden.

**Extra installatiebestanden downloaden**

1. Bladeren naar: licence.visualsciences.com om u vergunningscertificaat en uitvoerbaar de Tovenaar van de Opstelling te downloaden DWB.
1. Ga uw Organisatie (de Naam van de Rekening), de naam van de primaire Gebruiker, en het Wachtwoord in dat u van de Zorg van de Klant van Adobe ontving, dan login klikt.

   >[!NOTE]
   >
   >Uw browser zou u kunnen ertoe aanzetten om een digitaal certificaat op dit punt voor te stellen. Als het, annuleert de klik om de dialoogdoos te verwerpen.

1. Bepaal de plaats van het certificaat dat voor uw geval van de Werkbank van de Gegevens van Adobe (`<PrimaryUser>`.pem) wordt uitgegeven in de sectie van Downloads en download.
1. Bepaal de plaats van de StandaardInstallateur van de Cliënt in de sectie van Downloads om de Tovenaar van de Opstelling te downloaden DWB (InsightSetup-x.xx.exe- dossier).
1. Na het ontvangen van en het downloaden van dossiers van de Zorg van de Klant van Adobe, stel de Tovenaar van de Opstelling DWB in werking om de werkstationsoftware aan uw cliëntcomputer te installeren.

>[!NOTE]
De tovenaar van de Opstelling DWB zal u door installatie van het DWB cliëntwerkstation lopen en zal helpen van de dossiers van Insight.cfg en `<PrimaryUser>`.pem de plaats bepalen om in de vereiste omslagen te plaatsen. Het dossier Insight.cfg verblijft met het dossier Insight.exe in uw geïnstalleerd cliëntwerkstation. Het `<PrimaryUser>`.pem- dossier verblijft in de omslag van Certificaten met het trust_ca_cert.pem- dossier. Alle certificaat en configuratiedossiers moeten voor DWB aanwezig zijn om te functioneren.

Voor extra informatie, zie de Tovenaar [van de Opstelling](https://docs.adobe.com/content/help/en/data-workbench/using/install/workstation-setup/install-setup.html)DWB.

## Verbinding met uw DWB-servers {#section-8e79c4e07c2a4342a5bb8af6ee7be3c9}

Uw beheerde servers worden geïdentificeerd in het Insight.cfg- dossier dat u van de Zorg van de Klant van Adobe ontvangt en op uw cliëntwerkstation verblijft. Adobe TechOps zal opstelling uw servers en de Zorg van de Klant van Adobe zal verwijzingen naar deze beheerde servers en profielen aan het Insight.cfg- dossier toevoegen alvorens het naar u te verzenden. (De Configure verbindingen aan server in stap 12 van de documentatie van de Tovenaar van de Opstelling DWB zullen worden voltooid.)

>[!NOTE]
In de werkruimte van de Configuratie van het Werkstation op het DWB cliëntwerkstation, zult u uw verbonden servers en profielen kunnen zien.

**De Beheerde Diensten van Adobe**

・ Adobe TechOps beheert de infrastructuur met inbegrip van netwerk, gegevenscentrum, servers, en opslag. De controle van de infrastructuur en de reactie op alarm komt op een 24x7 basis voor alarm voor dat de actie van TechOps vereist. Voor ander alarm, zal TechOps de Zorg van de Klant van Adobe om met u op de hoogte brengen te coördineren.

・ Adobe TechOps zal onderhoud en ingebouwde programmatuurupdates voor uw beheerde servers uitvoeren. Voor onderhoud dat uitvaltijd veroorzaakt, ontvangt u minimaal twee weken van tevoren meldingen van de klantenservice voor het onderhoudvenster. Adobe TechOps zal op directe behoeften zo snel mogelijk gericht zijn. De kennisgeving hangt af van de urgentie en zal worden opgelost zodra het schema bekend is.

・ Adobe TechOps plaatst - omhoog een geplande taak om gegevens automatisch te beheren. De analytische voedergegevens worden verplaatst naar DWB voor verwerking en transformatie elke avond die bij 21:00 tijd van de rapportreeks begint.

・ Adobe TechOps zal andere Adobe Beheerde Diensten verwerken omvat gegevenssteunen, de rekeningen van FTP, het archiveren van gegevens, en gegevensoverdracht wanneer nodig.

・ Adobe TechOps zal de primaire productiecluster vormen om drie maanden het rollen gegevens te bevatten die maandelijks moeten worden teruggesteld en worden opnieuw verwerkt. De updates aan raadplegingen (Geografie, DeviceAtlas, Standaard Classificaties) zullen ook als deel van de opwerkingstaak voorkomen. Door gebrek, de taaklooppas op de eerste Vrijdag van elke maand. Indien nodig kan het programma door de klantenservice worden gewijzigd.

Voor extra informatie contacteer de Zorg van de Klant van [Adobe van de Klant](https://helpx.adobe.com/support/programs/enterprise-support-terms.html)van Adobe.

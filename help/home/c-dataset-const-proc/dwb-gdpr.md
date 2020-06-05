---
description: Adobe Data Workbench biedt gereedschappen en processen waarmee u uw gegevens kunt voorbereiden op naleving van de algemene gegevensbeschermingsregels (GDPR).
solution: Analytics
title: Ondersteuning voor Data Workbench voor GDPR
topic: Data workbench
translation-type: tm+mt
source-git-commit: 279e71f3da3f0ebc29091e88b87666a22a36a8d6
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 1%

---


# Ondersteuning voor Data Workbench voor GDPR

Adobe Data Workbench biedt gereedschappen en processen om ervoor te zorgen dat uw gegevens voldoen aan de [!DNL General Data Protection Regulations] (GDPR).

Net als alle andere Adobe Analytics-oplossingen biedt Data Workbench ondersteuning voor GDPR door analytische variabelen tijdens de verwerking van de gegevensfeed van Adobe Analytics op te schonen, te verwijderen en te labelen. Ter ondersteuning van GDPR-implementaties kunt u met Adobe processen voor GDPR instellen in overeenstemming met de machtigingen van uw bedrijf die zijn vastgelegd in uw overeenkomst met Adobe. Zie [Adobe Analytics en GDPR voor meer informatie](https://docs.adobe.com/content/help/en/analytics/admin/data-governance/an-gdpr-overview.html).

In de GDPR-verordening worden de rollen en verplichtingen van de verschillende partijen die verantwoordelijk zijn voor GDPR-activering (zie [GDPR en Uw bedrijf](https://www.adobe.com/privacy/general-data-protection-regulation.html)) vastgesteld.

* Uw organisatie fungeert als de **gegevenscontroller** om de context en het bewaren van persoonsgegevens te bepalen op basis van uw behoeften en beperkingen. Adobe verwerkt en slaat deze gegevens vervolgens namens u op.
* Adobe is de **gegevensverwerker** die de software en services levert voor het implementeren van GDPR-vereisten op basis van uw overeenkomst met Adobe.
* Na integratie van Data Workbench met de GDPR-service en volgens de GDPR-standaarden kunnen bezoekers van een site (de **betrokkenen**) hun &quot;recht om te worden vergeten&quot; uitoefenen door Adobe, de gegevensverwerker. Om het recht te bereiken om te worden vergeten, kunt u als gegevenscontroller uitgevochten bezoeker-id&#39;s uploaden van een interface of API naar Adobe. Raadpleeg de documentatie bij de GDPR-workflow [van](https://docs.adobe.com/help/en/analytics/admin/data-governance/an-gdpr-workflow.html) Adobe Analytics voor meer informatie, zoals de sectie [Verzendings- en verwijderingsverzoeken](https://docs.adobe.com/content/help/en/analytics/admin/data-governance/gdpr-submit-access-delete.html) .

>[!NOTE]
>
>Voor andere gegevensbronnen, zal uw organisatie voor het schoonmaken van uitgedaagde bezoeker IDs van andere logboekbronnen, zoals CRM, POS, IVR, en andere ruwe gegevensbronnen verantwoordelijk zijn. Aangepast-scoped de dienstenpakketten zullen beschikbaar zijn om steun aan organisaties te verlenen door een volledige vervangingsreeks dossiers voor elke gegevensbron _te_ verstrekken die de aan de gang zijnde dienstbewaarders moeten steunen of handhaven.

## DWB bijwerken voor GDPR-implementatie

De raadpleging zal u adviseren over het aangewezen dienstenpakket om bestaande implementaties in overeenstemming te brengen. Neem contact op met uw Customer Success Manager (CSM) voor meer informatie.

Indien vereist:

* [Voer een upgrade uit naar de nieuwste versie](https://docs.adobe.com/content/help/en/data-workbench/using/release-notes/release-notes.html) van Data Workbench. Voor de hoogste veiligheid, werden de nieuwe certificaten en veiligheidseigenschappen toegevoegd in DWB 6.7 versies die voor GDPR integratie worden vereist.
* Als u de logbestanden van gebeurtenissen met betrekking tot TSV-analyse gebruikt, voert u een upgrade uit naar de [Avro-gegevensfeed](https://docs.adobe.com/content/help/en/data-workbench/using/dataset/log-proc-config-file/c-log-sources.html#section-9a824b4c3d5549e7952a7111232035b2).
* Als het gebruiken van erfenis UCP (het Verenigde Proces van de Klant) met Transformatie om bestaande logboeken bij te werken, bevorder aan het huidige proces. Het bijgewerkte proces produceert direct een hoofdraadplegingsdossier voor het in kaart brengen van bezoeker IDs over bronnen.
* De gegevensstroom standaardiseren voor de GDPR-service.
* Vestig een douane-scoped de dienstenpakket om andere logboekbronnen zoals CRM, POS, IVR, en andere ruwe gegevensbronnen te beheren.
* Bevestig de bewaarperiode voor standaardgegevens van 25 maanden of meer in het Analytics-contract.

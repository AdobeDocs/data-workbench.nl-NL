---
description: Adobe Data Workbench biedt tools en processen om uw gegevens gereed te maken om te voldoen aan de algemene gegevensbeschermingsvoorschriften (GDPR).
title: Ondersteuning van Data Workbench voor GDPR
exl-id: fdc43567-0c57-4851-9073-e295258a8074
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Ondersteuning van Data Workbench voor GDPR

De Data Workbench van Adobe verstrekt hulpmiddelen en processen om uw gegevens klaar te maken om aan [!DNL General Data Protection Regulations] (GDPR) te voldoen.

Net als alle Adobe Analytics-oplossingen biedt Data Workbench ondersteuning voor GDPR door analytische variabelen tijdens de verwerking van de Adobe Analytics-gegevensfeed op te schonen, te verwijderen en te labelen. Ter ondersteuning van GDPR-implementaties kunt u met Adobe processen voor GDPR instellen in overeenstemming met de machtigingen van uw bedrijf die zijn vastgelegd in uw overeenkomst met Adobe. Zie [Adobe Analytics en GDPR voor aanvullende informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html).

In de GDPR-verordening worden de rollen en verplichtingen van de verschillende partijen die verantwoordelijk zijn voor GDPR-activering vastgesteld (zie [GDPR en Uw bedrijf](https://www.adobe.com/nl/privacy/general-data-protection-regulation.html)).

* Uw organisatie fungeert als **gegevenscontroller** om de context en het bewaren van persoonlijke gegevens te bepalen op basis van uw behoeften en beperkingen. Adobe verwerkt en slaat deze gegevens vervolgens namens u op.
* Adobe fungeert als de **gegevensprocessor** om de software en services te leveren voor het implementeren van GDPR-vereisten op basis van uw overeenkomst met Adobe.
* Na integratie van de Data Workbench met de GDPR-service en volgens de GDPR-normen kunnen bezoekers van een site (de **betrokkenen**) hun &quot;recht om te worden vergeten&quot; uitoefenen door Adobe, de gegevensverwerker. Om het recht te verwezenlijken om te worden vergeten, kunt u als gegevenscontroller uitgevochten bezoeker-id&#39;s uploaden naar Adobe vanuit een gebruikersinterface of API. Zie de [Adobe Analytics GDPR Workflow](https://docs.adobe.com/help/en/analytics/admin/data-governance/an-gdpr-workflow.html) documentatie voor meer informatie, met inbegrip van [voorlegt toegang en schrapt verzoeken](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-submit-access-delete.html) sectie.

>[!NOTE]
>
>Voor andere gegevensbronnen, zal uw organisatie voor het schoonmaken van uitgedaagde bezoeker IDs van andere logboekbronnen, zoals CRM, POS, IVR, en andere ruwe gegevensbronnen verantwoordelijk zijn. Pakketten met aangepaste services zijn beschikbaar om organisaties te ondersteunen door _een volledige vervangende set bestanden te bieden voor elke gegevensbron_ die doorlopende servicereinders moeten ondersteunen of onderhouden.

## DWB bijwerken voor GDPR-implementatie

De raadpleging zal u adviseren over het aangewezen dienstenpakket om bestaande implementaties in overeenstemming te brengen. Neem contact op met uw Customer Success Manager (CSM) voor meer informatie.

Indien vereist:

* [Voer een upgrade uit naar de nieuwste ](https://experienceleague.adobe.com/docs/data-workbench/using/release-notes/release-notes.html) versie van Data Workbench. Voor de hoogste veiligheid, werden de nieuwe certificaten en veiligheidseigenschappen toegevoegd in DWB 6.7 versies die voor GDPR integratie worden vereist.
* Als het gebruiken van de gebeurtenislogboeken van de Analyse van de erfenisTSV, bevorder aan [Avro gegevensvoer](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/log-proc-config-file/c-log-sources.html#section-9a824b4c3d5549e7952a7111232035b2).
* Als het gebruiken van erfenis UCP (het Verenigde Proces van de Klant) met Transformatie om bestaande logboeken bij te werken, bevorder aan het huidige proces. Het bijgewerkte proces produceert direct een master raadplegingsdossier voor het in kaart brengen van bezoeker IDs over bronnen.
* De gegevensstroom standaardiseren voor de GDPR-service.
* Vestig een douane-scoped de dienstenpakket om andere logboekbronnen zoals CRM, POS, IVR, en andere ruwe gegevensbronnen te beheren.
* Bevestig de bewaarperiode voor standaardgegevens van 25 maanden of meer in het Analytics-contract.

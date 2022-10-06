---
description: Adobe Data Workbench biedt tools en processen om uw gegevens gereed te maken om te voldoen aan de algemene gegevensbeschermingsvoorschriften (GDPR).
title: Ondersteuning van Data Workbench voor GDPR
exl-id: fdc43567-0c57-4851-9073-e295258a8074
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Ondersteuning van Data Workbench voor GDPR

{{eol}}

Adobe Data Workbench biedt tools en processen om uw gegevens te laten voldoen aan de [!DNL General Data Protection Regulations] (GDPR).

Net als alle Adobe Analytics-oplossingen biedt Data Workbench ondersteuning voor GDPR door analytische variabelen tijdens de verwerking van de Adobe Analytics-gegevensfeed op te schonen, te verwijderen en te labelen. Ter ondersteuning van GDPR-implementaties kunt u met Adobe processen voor GDPR instellen in overeenstemming met de machtigingen van uw bedrijf die zijn vastgelegd in uw overeenkomst met Adobe. Zie [Adobe Analytics en GDPR voor aanvullende informatie](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-overview.html).

In de GDPR-verordening worden de rollen en verplichtingen van de verschillende partijen die verantwoordelijk zijn voor GDPR-activering vastgesteld (zie [GDPR en uw bedrijf](https://www.adobe.com/nl/privacy/general-data-protection-regulation.html)).

* Uw organisatie fungeert als de **gegevenscontroller** om de context en het behoud van persoonsgegevens te bepalen op basis van uw behoeften en beperkingen. Adobe verwerkt en slaat deze gegevens vervolgens namens u op.
* Adobe fungeert als de **gegevensverwerker** om de software en services te leveren voor het implementeren van GDPR-vereisten op basis van uw overeenkomst met Adobe.
* Na integratie van de Data Workbench met de GDPR-dienst en overeenkomstig de GDPR-normen, kunnen bezoekers naar een site (de **betrokkenen**) kunnen hun &quot;recht om te worden vergeten&quot; uitoefenen door Adobe, de gegevensverwerker. Om het recht te verwezenlijken om te worden vergeten, kunt u als gegevenscontroller uitgevochten bezoeker-id&#39;s uploaden naar Adobe vanuit een gebruikersinterface of API. Zie de [Adobe Analytics GDPR Workflow](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/an-gdpr-workflow.html?lang=en) documentatie voor meer informatie, waaronder de [verzoeken om toegang en verwijdering verzenden](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-submit-access-delete.html) sectie.

>[!NOTE]
>
>Voor andere gegevensbronnen, zal uw organisatie voor het schoonmaken van uitgedaagde bezoeker IDs van andere logboekbronnen, zoals CRM, POS, IVR, en andere ruwe gegevensbronnen verantwoordelijk zijn. Pakketten met aangepaste services zijn beschikbaar voor ondersteuning van organisaties door _een volledige vervangende set bestanden voor elke gegevensbron verstrekken_ dat de doorlopende dienstverleners moeten steunen of handhaven.

## DWB bijwerken voor GDPR-implementatie

De raadpleging zal u adviseren over het aangewezen dienstenpakket om bestaande implementaties in overeenstemming te brengen. Neem contact op met uw Customer Success Manager (CSM) voor meer informatie.

Indien vereist:

* [Upgrade naar de nieuwste versie](https://experienceleague.adobe.com/docs/data-workbench/using/release-notes/release-notes.html) van Data Workbench. Voor de hoogste veiligheid, werden de nieuwe certificaten en veiligheidseigenschappen toegevoegd in DWB 6.7 versies die voor GDPR integratie worden vereist.
* Als u oude tsv Analytics-gebeurtenislogboeken gebruikt, voert u een upgrade uit naar de [Avro-gegevensfeed](https://experienceleague.adobe.com/docs/data-workbench/using/dataset/log-proc-config-file/c-log-sources.html#section-9a824b4c3d5549e7952a7111232035b2).
* Als het gebruiken van erfenis UCP (het Verenigde Proces van de Klant) met Transformatie om bestaande logboeken bij te werken, bevorder aan het huidige proces. Het bijgewerkte proces produceert direct een master raadplegingsdossier voor het in kaart brengen van bezoeker IDs over bronnen.
* De gegevensstroom standaardiseren voor de GDPR-service.
* Vestig een douane-scoped de dienstenpakket om andere logboekbronnen zoals CRM, POS, IVR, en andere ruwe gegevensbronnen te beheren.
* Bevestig de bewaarperiode voor standaardgegevens van 25 maanden of meer in het Analytics-contract.

---
description: Er zijn vijf vooraf gebouwde toegangsbeheergroepen beschikbaar, maar u kunt desgewenst extra groepen maken en beheren.
title: Toegangsbeheergroepen
uuid: ff783078-6d2f-4a64-ab11-8083e35d765f
exl-id: 35353b0a-7f08-4215-8a2c-ee1e26d9f5db
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# Toegangsbeheergroepen{#understanding-access-control-groups}

{{eol}}

Er zijn vijf vooraf gebouwde toegangsbeheergroepen beschikbaar, maar u kunt desgewenst extra groepen maken en beheren.

U kunt de leden van elke groep van de toegangscontrole, evenals de folders bepalen waaraan elke groep read-Only of Read-Write toegang heeft.

De vooraf gedefinieerde groepen worden als volgt gedefinieerd:

| Groep | Beschrijving |
|---|---|
| Beheerders | Hiermee krijgt u toegang tot alle mappen en bestanden. Het standaardIP adres is 127.0.0.1 (lokale gastheer). |
| Sensoren | Hiermee wordt alleen toegang toegestaan tot de bestanden die worden gebruikt door [!DNL Sensor] om gegevens te verzenden. |
| Gebruikers | Hiermee wordt alleen-lezen toegang toegestaan tot de elementen die vereist zijn voor een [!DNL Insight] gebruiker om elementaire analystaken uit te voeren. |
| Energiegebruikers | Hiermee wordt alleen-lezen toegang toegestaan tot de elementen die vereist zijn voor een [!DNL Insight] gebruiker voor het uitvoeren van elementaire analysetaken, plus lees- en schrijftoegang tot de [!DNL Profiles] map voor het wijzigen van profielen. |
| Clusterservers | Hiermee wordt toegang toegestaan tot [!DNL Insight Servers] die zijn aangewezen als clusterservers. |
| Rapportservers | Hiermee wordt toegang toegestaan tot [!DNL Report] machines die verbinding maken met de [!DNL Insight Server]. |

De leden van een toegangsbeheergroep worden bepaald gebruikend hun IP adressen of SSL certificaatinformatie.

Als er geen SSL-certificaat beschikbaar is, kan een IP-adres worden gebruikt om een groepslid te definiëren. De standaardinstallatie van [!DNL Insight] bevat een SSL-certificaat, terwijl het gebruik van certificaten voor [!DNL Sensor(s)] is optioneel. Voor [!DNL Insight Server], worden de Servers van de Cluster bepaald gebruikend IP adressen in plaats van SSL certificaten.

De volgende codes kunnen worden gebruikt om groepsleden te definiëren:

| Code toegangstypen | Definitie |
|---|---|
| O | Organisatie |
| GN | Algemene naam |
| L | Locatie |
| ST | Staat of provincie |
| C | Land |
| OU | Organisatorische eenheid |
| E-mail | E-mailadres |

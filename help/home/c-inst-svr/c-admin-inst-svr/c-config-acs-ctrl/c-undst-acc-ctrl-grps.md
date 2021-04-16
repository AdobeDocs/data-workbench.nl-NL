---
description: Er zijn vijf vooraf gebouwde toegangsbeheergroepen beschikbaar, maar u kunt desgewenst extra groepen maken en beheren.
title: Toegangsbeheergroepen
uuid: ff783078-6d2f-4a64-ab11-8083e35d765f
exl-id: 35353b0a-7f08-4215-8a2c-ee1e26d9f5db
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# Toegangsbeheergroepen{#understanding-access-control-groups}

Er zijn vijf vooraf gebouwde toegangsbeheergroepen beschikbaar, maar u kunt desgewenst extra groepen maken en beheren.

U kunt de leden van elke groep van de toegangscontrole, evenals de folders bepalen waaraan elke groep read-Only of Read-Write toegang heeft.

De vooraf gedefinieerde groepen worden als volgt gedefinieerd:

| Groep | Beschrijving |
|---|---|
| Beheerders | Hiermee krijgt u toegang tot alle mappen en bestanden. Het standaardIP adres is 127.0.0.1 (lokale gastheer). |
| Sensoren | Hiermee wordt alleen toegang toegestaan tot de bestanden die door [!DNL Sensor] worden gebruikt voor het verzenden van gegevens. |
| Gebruikers | Staat read-only toegang tot de elementen toe die voor een [!DNL Insight] gebruiker worden vereist om basisteanalystaken uit te voeren. |
| Energiegebruikers | Hiermee geeft u alleen-lezen toegang tot de elementen die een [!DNL Insight]-gebruiker nodig heeft om elementaire analysetaken uit te voeren, plus lees- en schrijftoegang tot de map [!DNL Profiles] voor het wijzigen van profielen. |
| Clusterservers | Hiermee wordt toegang toegestaan tot [!DNL Insight Servers] die zijn aangewezen als clusterservers. |
| Rapportservers | Hiermee wordt toegang toegestaan tot [!DNL Report]-computers die verbinding maken met [!DNL Insight Server]. |

De leden van een toegangsbeheergroep worden bepaald gebruikend hun IP adressen of SSL certificaatinformatie.

Als er geen SSL-certificaat beschikbaar is, kan een IP-adres worden gebruikt om een groepslid te definiëren. De standaardinstallatie van [!DNL Insight] bevat een SSL-certificaat, terwijl het gebruik van certificaten voor [!DNL Sensor(s)] optioneel is. Voor [!DNL Insight Server], worden de Servers van de Cluster bepaald gebruikend IP adressen in plaats van SSL certificaten.

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

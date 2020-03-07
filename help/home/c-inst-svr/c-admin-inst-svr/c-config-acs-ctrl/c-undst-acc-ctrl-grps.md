---
description: Vijf pre-gebouwde toegangsbeheergroepen zijn beschikbaar, maar u kunt extra groepen tot stand brengen en leiden zoals vereist.
solution: Insight
title: Het begrip van de Groepen van het Toegangsbeheer
uuid: ff783078-6d2f-4a64-ab11-8083e35d765f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het begrip van de Groepen van het Toegangsbeheer{#understanding-access-control-groups}

Vijf pre-gebouwde toegangsbeheergroepen zijn beschikbaar, maar u kunt extra groepen tot stand brengen en leiden zoals vereist.

U kunt de leden van elke toegangsbeheergroep, evenals de folders bepalen waaraan elke groep read-only of read-Write toegang heeft.

De vooraf gedefinieerde groepen worden als volgt gedefinieerd:

| Groep | Beschrijving |
|---|---|
| Administrateurs | Staat toegang tot alle folders en dossiers toe. Het standaardIP adres is 127.0.0.1 (lokale gastheer). |
| Sensoren | Staat toegang tot slechts die dossiers toe die door worden gebruikt om gegevens over [!DNL Sensor] te brengen. |
| Gebruikers | Staat read-only toegang tot de elementen toe die voor een [!DNL Insight] gebruiker worden vereist om fundamentele analysetaken uit te voeren. |
| Energiegebruikers | Staat read-only toegang tot de elementen toe die voor een [!DNL Insight] [!DNL Profiles] gebruiker worden vereist om basisanalysetaken uit te voeren, plus gelezen en schrijf toegang tot de omslag voor het wijzigen van profielen. |
| Clusterservers | Staat toegang tot toe [!DNL Insight Servers] die als clusterservers worden aangewezen. |
| Rapportservers | Staat toegang tot [!DNL Report] machines toe die met het verbinden [!DNL Insight Server]. |

De leden van een toegangsbeheergroep worden bepaald gebruikend hun IP adressen of SSL certificaatinformatie.

Als een SSL certificaat niet beschikbaar is, kan een IP adres worden gebruikt om een groepslid te bepalen. De typische installatie van [!DNL Insight] omvat een SSL certificaat, terwijl het gebruik van certificaten voor [!DNL Sensor(s)] facultatief is. Voor [!DNL Insight Server], worden de Servers van de Cluster bepaald gebruikend IP adressen in plaats van SSL certificaten.

De volgende codes kunnen worden gebruikt om groepsleden te definiëren:

| Code toegangstypen | Definitie |
|---|---|
| O | Organisatie |
| GN | Algemene naam |
| L | Localiteit |
| ST | Staat of provincie |
| C | Land |
| OU | Organisatorische eenheid |
| E-mailen | E-mailadres |


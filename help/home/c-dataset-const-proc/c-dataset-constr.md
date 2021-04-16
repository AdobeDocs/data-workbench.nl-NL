---
description: Een dataset van Adobe bevat de gegevens die door de server van de gegevenswerkbank zijn geladen en verwerkt.
title: Werken met gegevenssetconstructie
uuid: 540d159d-3f72-49dd-9929-107f1fc62b2b
exl-id: 111e98b5-d899-4f79-90ce-70f520d527d6
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 0%

---

# Begrijpen van gegevenssetconstructie{#understanding-dataset-construction}

Een dataset van Adobe bevat de gegevens die door de server van de gegevenswerkbank zijn geladen en verwerkt.

De stappen betrokken bij het laden en de verwerking van de gegevens door de server van de gegevenswerkbank (InsightServer64.exe) maken omhoog het proces van de datasetconstructie.

>[!NOTE]
>
>Een server van de gegevenswerkbank die gegevens van een dataset van de Adobe verwerkt en dient wordt genoemd een eenheid van de gegevensverwerking of DPU. Het wordt soms bedoeld als verwerkingsserver of een vraagserver. Gegevensworkbench en [!DNL Report] clients werken rechtstreeks samen met DPU&#39;s.

Tijdens datasetconstructie, leest de server van de gegevenswerkbank brongegevens van logboekbronnen, past transformaties op specifieke gebieden van gegevens toe, en bepaalt uitgebreide dimensies die van de getransformeerde gebieden moeten worden gecreeerd. Het bouwproces verloopt in twee fasen: *Logverwerking* en *Transformatie*. Nadat de dataset wordt geconstrueerd, kunt u de uitgebreide dimensies van de dataset gebruiken om afgeleide metriek en afmetingen voor uw specifieke analysedoeleinden tot stand te brengen.

De constructie van gegevenssets is vergelijkbaar met een productieproces. U selecteert de gegevens (de grondstoffen) die moeten worden gebruikt om de dataset te bouwen, en u bepaalt de gegevenstransformaties (de processtappen) die de informatie in de gegevens manipuleren om uitgebreide afmetingen (de geproduceerde producten) tot stand te brengen.

<!--
c_log_proc.xml
-->

De logboeken worden gefilterd en de gegevensvelden die aan de transformatiefase moeten worden doorgegeven, worden geïdentificeerd. Aan het eind van de fase van de logboekverwerking, worden de gegevens gegroepeerd door volgende identiteitskaart (namelijk worden alle logboekingangen met zelfde volgingsidentiteitskaart gegroepeerd) en in tijd bevolen. Tijdens de fase van de logboekverwerking, kunt u niet tot de verwerkte gegevens toegang hebben om voor analyse te gebruiken.

## Logbronnen {#section-75279dd6a7304d469735562796741d0f} opgeven

De bronnen van het logboek zijn dossiers die de gegevens bevatten die moeten worden gebruikt om een dataset te bouwen. De gegevens die beschikbaar zijn in de logbronnen worden gebeurtenisgegevens genoemd omdat elke gegevensrecord een transactierecord of één instantie van een gebeurtenis vertegenwoordigt. Bovendien bevat elke record of elk logbestandvermelding een waarde die wordt aangeduid als een tracking-id.

>[!NOTE]
>
>Wanneer het selecteren van logboekbronnen, zorg ervoor dat elke logboekingang een volgende identiteitskaart voor de entiteit bevat die het hoogste niveau moet vertegenwoordigen waarop uw gegevens moeten worden gegroepeerd. Als u bijvoorbeeld werkt met gegevens die zijn verzameld via websiteverkeer, kunt u waarschijnlijk kiezen dat de bezoeker deze entiteit is. Elke bezoeker heeft een unieke tracking-id en alle gegevens over een bepaalde bezoeker van de site kunnen worden gegroepeerd. Neem voor hulp contact op met Adobe.

Een logbronnen gebeurtenisgegevens worden verzameld in real time door [!DNL Sensors] of uit gearchiveerde gegevensbronnen door de Server van het Insight gehaald. Gebeurtenisgegevens die door sensoren van HTTP- en toepassingsservers worden verzameld, worden naar Insight Servers verzonden, die de gegevens in sterk gecomprimeerde logbestanden ( [!DNL .vsl]) converteren. Gebeurtenisgegevens die zich in een plat bestand, XML-bestand of een ODBC-gegevensbron bevinden, worden gelezen door Insight Server, die decoders biedt die u definieert om een algemene set logvelden uit deze verschillende indelingen te extraheren.

## Transformaties {#section-55a8cdb47379484081e53087f074778d} definiëren

Een transformatie is een set instructies die u kunt definiëren om informatie in de gebeurtenisgegevens te extraheren of te bewerken. Elke transformatie die u definieert, wordt toegepast op elke record met gebeurtenisgegevens (logbestandvermelding) om bestaande logvelden bij te werken of nieuwe velden te maken. De resultaten van transformaties worden gebruikt samen met de voorwaarden van de logboekingang om te evalueren welke logboekingangen uit de dataset tijdens logboekverwerking worden gefiltreerd.

Niet kunnen alle types van transformaties tijdens de logboekverwerkingsfase van het proces van de datasetconstructie worden gebruikt.

## Logbestanden {#section-6172ca0fb0eb4177925151bb49fdbc02} filteren

De dataset bevat verscheidene parameters die worden gebruikt om de gegevens te filtreren die uit de transformaties stromen. Filteren wordt gebruikt om aan te geven welke logitems worden gebruikt in volgende verwerkingsstappen. Bijvoorbeeld, kunnen de filters door, tijdwaaier, de status van de reactie van de server, of IP adres en gebruiker-agent informatie worden bepaald. De [!DNL Log Entry Condition] is een aanpasbare filtertest. De test zoekt naar bepaalde voorwaarden op de gebieden van elke logboekingang om te bepalen of die ingang in het proces van de gegevenssetconstructie verder zou moeten gaan. Als een logbestandvermelding niet aan de voorwaarde voldoet, wordt de vermelding uit het constructieproces verwijderd.

## Velden identificeren voor transformatie {#section-eef98ca723e54547b887aefdf0514c47}

Als een gebied van gegevens van de logboekverwerkingsfase tot de transformatiefase voor verdere verwerking moet worden overgegaan, moet u het tijdens logboekverwerking identificeren. Deze vereiste is van toepassing ongeacht of het veld beschikbaar is in de logbronnen of is gemaakt op basis van gegevenstransformaties die tijdens de logverwerking op de gegevens zijn toegepast.

<!--
c_transformation.xml
-->

Tijdens de transformatiefase van datasetconstructie, komt de verwerking op de gegroepeerde en bevolen gegevens voor die output van logboekverwerking is. Er worden extra gegevenstransformaties uitgevoerd en uitgebreide gegevensafmetingen gemaakt voor gebruik in uw analyses. Tijdens de transformatiefase kunt u toegang krijgen tot een statistisch voorbeeld van de gegevens die groter worden wanneer de transformatiefase bijna is voltooid.

## Transformaties {#section-001b3fd4c1dd4dd38a5536872bc9de68} definiëren

U kunt transformaties bepalen die tijdens de transformatiefase van het proces van de datasetconstructie moeten worden gebruikt om de verwezenlijking van de uitgebreide afmetingen te vergemakkelijken. Elke transformatie wordt toegepast op elke gebeurtenisgegevensrecord (logbestandvermelding) die wordt doorgegeven via de logverwerking.

## Logbestanden {#section-3fed0a00ca344a719b5e8db363f64f06} filteren

[!DNL Log Entry Condition] kan tijdens transformatie worden toegepast om specifieke voorwaarden op de gebieden van elke logboekingang te zoeken die uit logboekverwerking komen. Als een logbestandvermelding niet aan de voorwaarde voldoet, wordt de vermelding uit het constructieproces verwijderd.

## Uitgebreide Dimension {#section-25efafd0bfc84c86b9717d453a88c91b} definiëren

Uitgebreide afmetingen zijn de eindproducten van het bouwproces van de dataset. Zij vertegenwoordigen verhoudingen tussen de logboekgebieden in de gegevens. U gebruikt hen om visualisaties tot stand te brengen, uitgebreide metriek te bouwen, of analyse uit te voeren om de verrichtingen en de kwesties te begrijpen specifiek voor uw zaken.

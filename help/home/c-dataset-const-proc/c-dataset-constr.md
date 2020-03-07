---
description: Een dataset van Adobe bevat de gegevens die door de server van de gegevenswerkbank zijn geladen en verwerkt.
solution: Analytics
title: Begrijpen van de bouw van de Dataset
topic: Data workbench
uuid: 540d159d-3f72-49dd-9929-107f1fc62b2b
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Begrijpen van de bouw van de Dataset{#understanding-dataset-construction}

Een dataset van Adobe bevat de gegevens die door de server van de gegevenswerkbank zijn geladen en verwerkt.

De stappen betrokken bij de lading en de verwerking van de gegevens door de server van de gegevenswerkbank (InsightServer64.exe) maken omhoog het proces van de datasetconstructie.

>[!NOTE]
>
>Een server van de gegevenswerkbank die verwerkt en gegevens van een dataset van Adobe dient wordt genoemd een gegevensverwerkingseenheid of DPU. Het wordt soms bedoeld als verwerkingsserver of een vraagserver. De werkbank van gegevens en de [!DNL Report] cliënten werken direct met DPUs in wisselwerking.

Tijdens datasetconstructie, leest de server van de gegevenswerkbank brongegevens uit logboekbronnen, past transformaties op specifieke gebieden van gegevens toe, en bepaalt uitgebreide afmetingen die van de getransformeerde gebieden moeten worden gecreeerd. Het bouwproces verloopt in twee fasen: *Logverwerking* en *transformatie*. Nadat de dataset wordt geconstrueerd, kunt u de uitgebreide afmetingen van de dataset gebruiken om afgeleide metriek en afmetingen voor uw specifieke analysedoeleinden tot stand te brengen.

De bouw van de dataset is als een productieproces. U selecteert de gegevens (de grondstoffen) die moeten worden gebruikt om de dataset te bouwen, en u bepaalt de gegevenstransformaties (de processtappen) die de informatie beschikbaar in de gegevens manipuleren om uitgebreide afmetingen (de vervaardigde producten) tot stand te brengen.

<!--
c_log_proc.xml
-->

De logboeken worden gefiltreerd, en de gebieden van gegevens die tot de transformatiefase moeten worden overgegaan worden geïdentificeerd. Aan het eind van de fase van de logboekverwerking, wordt het gegeven gegroepeerd door identiteitskaart te volgen (namelijk worden alle logboekingangen met zelfde volgende identiteitskaart gegroepeerd) en op tijd bevolen. Tijdens de fase van de logboekverwerking, kunt u niet tot de verwerkte gegevens toegang hebben voor analyse te gebruiken.

## Het specificeren van de Bronnen van het Logboek {#section-75279dd6a7304d469735562796741d0f}

De bronnen van het logboek zijn dossiers die de gegevens bevatten die moeten worden gebruikt om een dataset te bouwen. De gegevens beschikbaar in de logboekbronnen worden genoemd gebeurtenisgegevens omdat elk gegevensverslag een transactieverslag of één enkel geval van een gebeurtenis vertegenwoordigt. Bovendien bevat elk verslag, of logboekingang, een waarde die als volgende identiteitskaart wordt bedoeld.

>[!NOTE]
>
>Wanneer het selecteren van logboekbronnen, zorg ervoor dat elke logboekingang een volgende identiteitskaart voor de entiteit bevat die het hoogste niveau moet vertegenwoordigen waarop uw gegevens moeten worden gegroepeerd. Bijvoorbeeld, als u met gegevens werkt die van websiteverkeer worden verzameld, zult u waarschijnlijk bezoeker kiezen om deze entiteit te zijn. Elke bezoeker heeft een unieke volgende identiteitskaart, en alle gegevens over een bepaalde plaatsbezoeker kunnen worden gegroepeerd. Voor hulp, contacteer Adobe.

Een logbrongebeurtenisgegeven wordt verzameld in real time door [!DNL Sensors] of uit gearchiveerde gegevensbronnen door de Server van het Inzicht gehaald. De gegevens van de gebeurtenis die door Sensors van HTTP en toepassingsservers worden verzameld worden overgebracht naar de Servers van het Inzicht, die de gegevens in hoogst samengeperste logboek ( [!DNL .vsl]) dossiers omzetten. De gegevens van de gebeurtenis die in een vlak dossier, het dossier van XML, of een ODBC- gegevensbron verblijven worden gelezen door de Server van het Inzicht, die decoders verstrekt die u bepaalt om een gemeenschappelijke reeks logboekgebieden van deze verschillende formaten te halen.

## Transformaties definiëren {#section-55a8cdb47379484081e53087f074778d}

Een transformatie is een reeks instructies die u kunt bepalen om informatie in de gebeurtenisgegevens te halen of te manipuleren. Elke transformatie die u bepaalt wordt toegepast op elk verslag van gebeurtenisgegevens (logboekingang) om bestaande logboekgebieden bij te werken of nieuwe gebieden te veroorzaken. De resultaten van transformaties worden gebruikt samen met de voorwaarden van de logboekingang om te evalueren welke logboekingangen uit de dataset tijdens logboekverwerking worden gefiltreerd.

Niet kunnen alle types van transformaties tijdens de fase van de logboekverwerking van het proces van de datasetconstructie worden gebruikt.

## Logbestanden filteren {#section-6172ca0fb0eb4177925151bb49fdbc02}

De dataset bevat verscheidene parameters die worden gebruikt om de gegevens te filtreren die uit de transformaties vloeien. Het filtreren wordt gebruikt om te specificeren welke logboekingangen in verdere verwerkingsstappen worden gebruikt. Bijvoorbeeld, kunnen de filters door, tijdwaaier, de status van de reactie van de server, of IP adres en gebruiker-agent informatie worden bepaald. Het [!DNL Log Entry Condition] is een klantgerichte het filtreren test. De test zoekt naar bepaalde omstandigheden in de velden van elke logboekingang om te bepalen of die ingang in het proces van de gegevensset verder zou moeten gaan. Als een logboekingang niet aan de voorwaarde voldoet, wordt de ingang verwijderd uit het bouwproces.

## Gebieden voor transformatie identificeren {#section-eef98ca723e54547b887aefdf0514c47}

Als een gebied van gegevens van de logboekverwerkingsfase aan de transformatiefase voor verdere verwerking moet worden overgegaan, moet u het tijdens logboekverwerking identificeren. Deze eis is van toepassing ongeacht of het gebied bij de logboekbronnen beschikbaar is of van gegevenstransformaties gecreeerd die op de gegevens tijdens logboekverwerking worden toegepast.

<!--
c_transformation.xml
-->

Tijdens de transformatiefase van datasetconstructie, komt de verwerking op de gegroepeerde en bevolen gegevens voor die output van logboekverwerking is. De extra gegevenstransformaties worden uitgevoerd en de uitgebreide gegevensafmetingen worden gecreeerd voor gebruik in uw analyses. Tijdens de transformatiefase, kunt u tot een statistische steekproef van de gegevens toegang hebben die groter wordt aangezien de transformatiefase dichtbijt voltooiing.

## Transformaties definiëren {#section-001b3fd4c1dd4dd38a5536872bc9de68}

U kunt transformaties bepalen die tijdens de transformatiefase van het proces van de datasetconstructie moeten worden gebruikt om de verwezenlijking van de uitgebreide afmetingen te vergemakkelijken. Elke transformatie wordt toegepast op elk verslag van gebeurtenisgegevens (logboekingang) dat van logboekverwerking wordt overgegaan.

## Logbestanden filteren {#section-3fed0a00ca344a719b5e8db363f64f06}

De methode [!DNL Log Entry Condition] kan tijdens de transformatie worden toegepast om specifieke omstandigheden op de gebieden van elke logboekingang te zoeken die uit logboekverwerking komt. Als een logboekingang niet aan de voorwaarde voldoet, wordt de ingang verwijderd uit het bouwproces.

## Uitgebreide afmetingen definiëren {#section-25efafd0bfc84c86b9717d453a88c91b}

De uitgebreide afmetingen zijn de eindproducten van het proces van de datasetconstructie. Zij vertegenwoordigen verband tussen de logboekgebieden in de gegevens. U gebruikt hen om visualisaties tot stand te brengen, uitgebreide metriek te bouwen, of analyse uit te voeren om de verrichtingen en de kwesties te begrijpen specifiek voor uw zaken.

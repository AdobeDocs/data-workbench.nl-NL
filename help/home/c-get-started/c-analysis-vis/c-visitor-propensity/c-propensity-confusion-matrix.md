---
description: De statistische berekeningen voor het scoren van de dichtheid worden gedefinieerd.
solution: Analytics
title: Het berekenen van het Score van de Propensiteit
topic: Data workbench
uuid: 67270864-0468-4cc9-b48b-0e880f813555
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het berekenen van het Score van de Propensiteit{#calculating-propensity-scoring}

De statistische berekeningen voor het scoren van de dichtheid worden gedefinieerd.

Conceptueel, is de score die voor elke bezoeker wordt berekend een geschatte waarschijnlijkheid dat de gespecificeerde gebeurtenis (die door de doelfilter wordt bepaald) zou kunnen gebeuren, resulterend in een waaier van de scorewaarde van 0 tot 100 percenten. De scoringsprocedure gebruikt bestaande steekproeven als opleidingsgegevens om het verband tussen de gebeurteniswaarschijnlijkheid en de geselecteerde onafhankelijke variabelen van belang te vinden.

Mathematisch, worden dergelijke verhoudingen weerspiegeld in elke kwantitatieve waarde verbonden aan elke onafhankelijke variabele. Die waarden worden modelcoëfficiënten genoemd. ScoreDim gebruikt momenteel het Iteratively Regewogen algoritme van de Minst Squares (IRLS) om de modelcoëfficiënten te schatten. IRLS gaat door de steekproeven veelvoudige tijden tot het verschil van coëfficiënten tussen huidige pas en de vorige pas minder dan 1.0e-6 is, waarbij het wordt genoemd **samengekomen**. Nochtans, afhankelijk van de gegevens, kan IRLS geen convergentie kunnen bereiken.

In dat geval eindigt de modeltraining wanneer

* het coëfficiëntverschil wordt groter in plaats van kleiner;
* 1000 passages zijn bereikt, of
* een wiskundige fout verhindert verdere herhaling.

Als IRLS niet samenkomt, zal een reservealgoritme genoemd het Stochastische Decent van de Gradiënt (SGD) worden gebruikt. SGD zal ook door de opleidingssteekproeven veelvoudige tijden gaan. Maar in tegenstelling tot IRLS worden de SGD-modelcoëfficiënten gecontroleerd, zodat het verschil tussen iteratie altijd exponentieel zal afnemen. Evenzo zal SGD eindigen wanneer het coëfficiëntverschil onder 1,0e-6 of 100.000 passages is bereikt. De mislukking van IRLS en de betrokkenheid van SGD zullen in spoorlogboek worden geregistreerd.

Voor beide algoritmen, niet gaan alle steekproeven in modelopleiding. Op dit moment wordt 80 procent gebruikt om het model te trainen. Nadat het model wordt opgeleid, zullen de resterende 20 percenten steekproeven worden gebruikt om de modelsterkte in termen van Nauwkeurigheid, Rappel, en Nauwkeurigheid te beoordelen die uit de verwarringsmatrijs wordt berekend. Hoe dichter bij 100%, hoe beter het scoremodel.

---
description: De statistische berekeningen voor het waarderen van de volheid worden gedefinieerd.
title: Correctie berekenen
uuid: 67270864-0468-4cc9-b48b-0e880f813555
exl-id: 679e1363-fd10-4a44-a85a-ef0daefaf303
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Correctie berekenen{#calculating-propensity-scoring}

{{eol}}

De statistische berekeningen voor het waarderen van de volheid worden gedefinieerd.

Conceptueel, is de score die voor elke bezoeker wordt berekend een geschatte waarschijnlijkheid dat de gespecificeerde gebeurtenis (die door de doelfilter wordt bepaald) zou kunnen gebeuren, resulterend in een score waaier van 0 tot 100 percenten. De scoringsprocedure gebruikt bestaande steekproeven als opleidingsgegevens om het verband tussen de gebeurteniswaarschijnlijkheid en de geselecteerde onafhankelijke variabelen van belang te vinden.

Dergelijke relaties worden wiskundig weergegeven in elke kwantitatieve waarde die aan elke onafhankelijke variabele is gekoppeld. Deze waarden worden modelcoëfficiënten genoemd. ScoreDim gebruikt momenteel het algoritme Iterously Reweight Least Squares (IRLS) om de modelcoëfficiënten te schatten. De IRLS doorloopt de steekproeven veelvoudige tijden tot het verschil van coëfficiënten tussen stroom en de vorige pas minder dan 1.0e-6 is, waarbij het wordt genoemd **samengekomen**. Afhankelijk van de gegevens is het echter mogelijk dat de IRLS geen convergentie kunnen bereiken.

In dat geval wordt de modelopleiding beëindigd wanneer

* het coëfficiëntieverschil wordt groter in plaats van kleiner;
* 1000 passages zijn bereikt, of
* een wiskundige fout voorkomt herhaling.

Als IRLS niet samenkomt, zal een reservealgoritme genoemd Stochastic Gradient Decent (SGD) worden gebruikt. SGD zal ook de opleidingssteekproeven veelvoudige tijden doornemen. Maar in tegenstelling tot IRLS worden de SGD-modelcoëfficiënten zodanig beheerd dat het verschil tussen iteratie altijd exponentieel afneemt. Evenzo zal SGD eindigen wanneer het verschil in coëfficiënt onder 1,0e-6 of 100.000 passages is bereikt. De mislukking van de IRLS en de betrokkenheid van SGD zullen in spoorlogboek worden geregistreerd.

Voor beide algoritmen gaan niet alle steekproeven naar modelopleiding. 80 procent wordt momenteel gebruikt om het model te trainen. Nadat het model is opgeleid, zullen de resterende 20 percenten steekproeven worden gebruikt om de modelsterkte in termen van Nauwkeurigheid, Herhaling, en Precisie te beoordelen die van de verwarringsmatrijs wordt berekend. Hoe dichter bij 100%, hoe beter het scoremodel.

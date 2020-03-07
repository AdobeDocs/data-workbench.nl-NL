---
description: Informatie over het beoordelen en controleren van de belasting van de Ruimte van het Adres.
solution: Insight
title: Bewaking van geheugengebruik
uuid: e7f1c51b-d874-43f4-a074-1c064b5f298a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bewaking van geheugengebruik{#monitoring-memory-usage}

Informatie over het beoordelen en controleren van de belasting van de Ruimte van het Adres.

**De lading van de Ruimte van het Adres controleren**

**Aanbevolen frequentie:** Dagelijks

De lading van de Ruimte van het Adres is een maatregel van de fractie van de maximumRuimte van het Adres die behoorlijk gevormd [!DNL Insight Server] gebruik. Zelfs als de configuratieparameters worden veranderd om geheugengebruik te verminderen, vermindert het gewoonlijk niet tot de [!DNL Insight Server] dienst opnieuw is begonnen.

Een veiligheidsmarge wordt gebouwd in het maximum van de belasting van de Ruimte van het Adres om voor onverwachte verhogingen in het gebruik van de Ruimte van het Adres rekenschap te geven. Je moet nooit bewust in deze veiligheidsmarge snijden. Het bestaat voor noodsituaties en niet voor de steun van functionaliteit die aan uw toepassing van Adobe wordt toegevoegd.

>[!NOTE]
>
>Om meer Ruimte van het Adres beschikbaar te maken en de fouten van de geheugenuitputting te vermijden, zorg ervoor dat uw werkend systeem de /3GB toegelaten Schakelaar heeft en dat de Laag van de Fragmentatie Heap werkt.

De fouten die aan het logboek van [!DNL Insight Server] gebeurtenisgegevens worden geregistreerd kunnen een aanwijzing verstrekken dat de problemen met uw lading van de Ruimte van het Adres zich ontwikkelen:

* De &quot;Gevraagde byteblok van X is te groot&quot;fouten wijzen erop dat iets een bovenmatig effect op de lading van de Ruimte van het Adres, prestaties, en netwerkbandbreedte kan hebben. Dergelijke grote blokken kunnen zeer bijdragen aan het gebruik van de Ruimte van het Adres, zowel door veel geheugen te gebruiken als door grote aangrenzende blokken van de Ruimte van het Adres te vereisen.

   Om dit probleem aan te pakken, kunt u de kardinaliteit van uw grootste afmetingen verminderen, die uw belasting van de Ruimte van het Adres verhoogt. Als u niet de kardinaliteit van de afmetingen kunt verminderen, zou u moeten proberen om de lading van de Ruimte van het Adres klein genoeg te houden zodat u een onverwachte verhoging kunt behandelen.
* De &quot;begroting van het geheugen overschreden&quot;fouten wijzen erop dat u de Grens van het Geheugen van de Vraag zou kunnen moeten verhogen. Het geheugen dat door vragen wordt gebruikt is proportioneel aan afmetingskardinaliteit en, in sommige gevallen, de lengten van de elementennamen. Als u de Grens van het Geheugen van de Vraag verhoogt, verhoogt u uw totale lading van de Ruimte van het Adres en krimpt de grote afmetingen.

>[!NOTE]
>
>Door gebrek, wordt het gebruik van grote pagina&#39;s toegestaan en de geheugen-in kaart gebrachte raadpleging is gehandicapt. In DWB 6.7 en later, kan dit in datasetconfiguratie worden veranderd. Om het even welke veranderingen vereisen een nieuw begin van de Server.

**Om de belasting van de Ruimte van het Adres te beoordelen**

Om de lading van de Ruimte van het Adres voor uw systeem nauwkeurig te beoordelen, adviseert Adobe opverwerkend de dataset, uitvoerend sommige normale vragen zonder later opnieuw te beginnen [!DNL Insight Server], en dan het bekijken van de gemeten lading van de Ruimte van het Adres door deze stappen te volgen.

Als een [!DNL Insight Server] niet opnieuw verwerkt en beduidend gevraagd is sinds het het laatst opnieuw werd begonnen, zou u geen conclusies uit de Ruimtelading van het Adres moeten trekken.

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van het pictogram met de rechtermuisknop aan [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Detailed Status]**.
1. In de Gedetailleerde interface van de Status, klik **[!UICONTROL Memory Status]** om zijn inhoud te bekijken. In de parameter van de Lading van de Ruimte van het Adres, kunt u de lading van de Ruimte van het Adres zien die als percentage en een parenthetische beschrijving wordt uitgedrukt die op status wijzen.

   De volgende lijst stelt waaiers en status voor de Ruimte van het Adres voor. Een geadviseerde actie is vermeld voor elke waaier.

   | Laden van adresruimte (%) | Status | Aanbevolen actie |
   |---|---|---|
   | 0-15 | mager en gemiddeld | Geen. |
   | 15-33 | licht | Geen. |
   | 33-66 | gematigd | Geen. |
   | 66-100 | zwaar | Om de mislukkingen van de geheugenuitputting te vermijden, voeg geen significante extra functionaliteit toe of probeer om meer gegevens te verwerken. |
   | 100-125 | betrouwbaarheid gecompromitteerd | Pas uw datasetconfiguratie aan om de belasting van de Ruimte van het Adres te verminderen. |
   | 125 of meer | dreigend falen | Pas uw datasetconfiguratie aan om de belasting van de Ruimte van het Adres te verminderen. Het is mogelijk dat u de status van de dreigende storing niet ziet voordat de fout optreedt. |

   Als u een lading van de Ruimte van het Adres boven 100% ziet, zou u de configuratie moeten zo spoedig mogelijk veranderen om het gebruik van de Ruimte van het Adres te verminderen.


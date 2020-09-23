---
description: Informatie over het beoordelen van en het controleren van de lading van de Ruimte van het Adres.
solution: Analytics
title: Geheugengebruik controleren
uuid: e7f1c51b-d874-43f4-a074-1c064b5f298a
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 1%

---


# Geheugengebruik controleren{#monitoring-memory-usage}

Informatie over het beoordelen van en het controleren van de lading van de Ruimte van het Adres.

**Het controleren van de Lading van de Ruimte van het Adres**

**Aanbevolen frequentie:** Dagelijks

De lading van de Ruimte van het Adres is een maatregel van de fractie van de maximumRuimte van het Adres die correct gevormd [!DNL Insight Server] gebruikt. Zelfs als de configuratieparameters worden veranderd om geheugengebruik te verminderen, vermindert het gewoonlijk niet tot de [!DNL Insight Server] dienst opnieuw is begonnen.

Een veiligheidsmarge wordt ingebouwd in het maximum van de Ruimte van het Adres om voor onverwachte verhogingen in het gebruik van de Ruimte van het Adres rekening te houden. U mag nooit bewust in deze veiligheidsmarge snijden. Het bestaat voor noodsituaties en niet voor de ondersteuning van functionaliteit die aan uw Adobe-toepassing is toegevoegd.

>[!NOTE]
>
>Om meer Ruimte van het Adres beschikbaar te maken en de fouten van de geheugenuitputting te vermijden, zorg ervoor dat uw werkend systeem de /3GB toegelaten Schakelaar heeft en dat de Lage Heap van de Fragmentatie werkt.

De fouten die aan het logboek van [!DNL Insight Server] gebeurtenisgegevens worden geregistreerd kunnen een idee verstrekken dat de problemen zich met uw lading van de Ruimte van het Adres ontwikkelen:

* &quot;Gevraagd X byteblok is te groot&quot;de fouten wijzen erop dat iets een bovenmatige invloed op de lading van de Ruimte van het Adres, prestaties, en netwerkbandbreedte kan hebben. Dergelijke grote blokken kunnen zeer tot het gebruik van de Ruimte van het Adres bijdragen, zowel door veel geheugen te gebruiken als door grote aangrenzende blokken van de Ruimte van het Adres te vereisen.

   Om dit probleem aan te pakken, kunt u de kardinaliteit van uw grootste dimensies verminderen, die uw lading van de Ruimte van het Adres verhoogt. Als u de kardinaliteit van de afmetingen niet kunt verminderen, zou u moeten proberen om de Ruimte van het Adres te houden klein genoeg laden zodat u een onverwachte verhoging kunt behandelen.
* Het &quot;Geheugenbudget overschreden&quot;fouten wijzen erop dat u de Limiet van het Geheugen van de Vraag zou kunnen moeten verhogen. Het geheugen dat door vragen wordt gebruikt is evenredig aan afmetingskardinaliteit en, in sommige gevallen, de lengten van de elementennamen. Als u de Limiet van het Geheugen van de Vraag verhoogt, verhoogt u uw totale lading van de Ruimte van het Adres en krimpt de grote afmetingen.

>[!NOTE]
>
>Standaard is het gebruik van grote pagina&#39;s toegestaan en opzoeken in geheugentoewijzing is uitgeschakeld. In DWB 6.7 en later, kan dit in datasetconfiguratie worden veranderd. Voor alle wijzigingen moet de server opnieuw worden opgestart.

**Om de lading van de Ruimte van het Adres te beoordelen**

Om de lading van de Ruimte van het Adres voor uw systeem nauwkeurig te beoordelen, adviseert Adobe het herverwerken van de dataset, het uitvoeren van sommige normale vragen zonder daarna opnieuw te beginnen [!DNL Insight Server], en dan het bekijken van de gemeten lading van de Ruimte van het Adres door deze stappen te volgen.

Als een [!DNL Insight Server] niet is herverwerkt en niet beduidend is gevraagd sinds het laatst opnieuw werd begonnen, zou u geen conclusies uit de lading van de Ruimte van het Adres moeten trekken.

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het [!DNL Insight Server] object dat u wilt configureren en klik op **[!UICONTROL Detailed Status]**.
1. Klik in de interface Gedetailleerde status op **[!UICONTROL Memory Status]** om de inhoud ervan weer te geven. In de parameter van de Lading van de Ruimte van het Adres, kunt u de lading zien van de Ruimte van het Adres die als percentage en een haakjesbeschrijving op status wordt uitgedrukt die wijst.

   De volgende lijst stelt waaiers en status voor de lading van de Ruimte van het Adres voor. Voor elk bereik wordt een aanbevolen actie weergegeven.

   | Laden van adresruimte (%) | Status | Aanbevolen actie |
   |---|---|---|
   | 0-15 | mager en gemiddeld | Geen. |
   | 15-33 | licht | Geen. |
   | 33-66 | gematigd | Geen. |
   | 66-100 | zwaar | Als u fouten met de uitputting van het geheugen wilt voorkomen, voegt u geen significante extra functionaliteit toe of probeert u meer gegevens te verwerken. |
   | 100-125 | betrouwbaarheid aangetast | Pas uw datasetconfiguratie aan om de lading van de Ruimte van het Adres te verminderen. |
   | 125 of hoger | dreigende mislukking | Pas uw datasetconfiguratie aan om de lading van de Ruimte van het Adres te verminderen. Mogelijk ziet u de status die op het punt staat van de fout niet voordat de fout optreedt. |

   Als u een lading van de Ruimte van het Adres boven 100% ziet, zou u de configuratie zo spoedig mogelijk moeten veranderen om het gebruik van de Ruimte van het Adres te verminderen.


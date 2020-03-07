---
description: Een server van de gegevenswerkbank wordt zich bewust van een bron van gegevens, zoals een Sensor, wanneer het gegevens van die bron ontvangt.
solution: Insight
title: Het begrip "vanaf"tijd
uuid: a1853573-e77c-41f7-8b99-2843e38cc82d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het begrip &quot;vanaf&quot;tijd{#understanding-as-of-time}

Een server van de gegevenswerkbank wordt zich bewust van een bron van gegevens, zoals een Sensor, wanneer het gegevens van die bron ontvangt.

De termijn is een waarborg dat de gegevens voor alle gegevensbronnen waarvan zij op de hoogte is, [!DNL data workbench server] zijn.

Laten we zeggen dat we een reeks van drie hebben [!DNL Sensors] die gegevens naar een [!DNL data workbench server]sturen: WEB1, WEB2, en WEB3. Aangezien [!DNL data workbench server] ontvangt en verwerkt de gegevens van deze [!DNL Sensors], komt het automatisch om gegevens van elk van deze bronnen te verwachten. Vanaf tijd wijst op de laatste tijd dat de [!DNL data workbench server] ontvangen gegevens van alle drie van deze bronnen.

In praktische termen, geeft de [!DNL data workbench server] enige om het Eind van tijd en niet wat zou kunnen worden bedoeld als &quot;muurtijd,&quot;of de tijd van een klok op de muur. De tijd [!DNL data workbench server] weet alleen maar als &#39;s avonds. Dit is met name van belang voor rapportagedoeleinden, aangezien het garandeert dat de rapporten altijd worden uitgevoerd op basis van het tijdstip waarop de rapportage plaatsvindt, hetgeen garandeert dat verslagen met slechts gedeeltelijke gegevens nooit aan de eindgebruikers van het systeem kunnen worden toegezonden.

Het [!DNL data workbench server] gebruiks gegevens die van de zender worden verzonden om te verstrekken zoals van tijd, of het daadwerkelijke die gegevens zijn van de website worden verzameld of periodieke hartslagen door uw [!DNL Sensors]worden verzonden. Deze hartslagen dienen twee doelen:

1. Om een HTTP/1.1 blijvende verbinding open tussen te houden [!DNL Sensor] en [!DNL data workbench server].

1. Om het van tijd huidig te houden in het geval dat het websiteverkeer niet wordt verzameld en naar de [!DNL data workbench server]wordt verzonden.


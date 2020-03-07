---
description: De plaats gebruikt koekjes om bezoekers aan uw website uniek te identificeren en hun gedrag in tijd te volgen.
solution: Analytics
title: Het begrijpen van de v1st Koekje
topic: Data workbench
uuid: 6112cafe-51e3-42f0-8554-4a653dea782a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het begrijpen van de v1st Koekje{#understanding-the-v-st-cookie}

De plaats gebruikt koekjes om bezoekers aan uw website uniek te identificeren en hun gedrag in tijd te volgen.

De eerste keer dat een bepaalde browser (als bezoeker beschouwd) een verzoek indient op uw website, [!DNL Sensor] werkt met uw webserver om een persistent cookie, cs(cookie)(v1st), in te stellen, wat intern binnen het systeem wordt geïnterpreteerd als x-trackingid. Dit persistente cookie wordt ingesteld naast een ander cookie dat je site anders kan instellen. Dit koekje optimaliseert uw capaciteit om uw bezoekers over veelvoudige zittingen te volgen, die vele soorten analyse toelaat die anders onmogelijk zijn.

[!DNL Sensor] wijst een numerieke sleutel met 64 bits in het koekje toe om nieuwe bezoekers te identificeren die een verzoek van de plaats als uniek herkenningsteken indienen. Wanneer de gebruiker een verzoek van een browser [!DNL Sensor] ziet, controleert hij of &quot;cs (cookie)(v1st)&quot;, een eerste-partij persistente cookie die is ingesteld door, [!DNL Sensor]voorkomt in de aanvraaggegevens. Als cs (koekje) (v1st) niet aanwezig is, [!DNL Sensor]door uw Webserver, vertelt browser om het te plaatsen. In tegenstelling tot andere oplossingen, [!DNL Sensor] kan dit koekje op het eerste verzoek van de bezoeker plaatsen.

Hieronder is de standaard persistente cookie header die naar de browser wordt gestuurd op zijn eerste verzoek van je site door je webserver, in de richting van [!DNL Sensor]. Het formaat kan op het tijdstip van configuratie worden bepaald als een verschillende naam of een vervaldatum wordt gewenst. Bijvoorbeeld:

```
Set-Cookie:v1st=3D80DCA944D60E16; path=/; expires=Wed, 19 Feb 2020 14:28:00 GMT
```

Dit koekje wordt geplaatst enkel eens, op het allereerste verzoek dat door die bezoeker aan uw plaats wordt gedaan. Het wordt dan verzameld bij die bezoeker telkens als browser een verzoek (of pagina of ingebed objecten verzoek) van uw plaats in de toekomst indient. Het koekje is zeer klein in grootte om de hoeveelheid bandbreedte te minimaliseren die wordt gebruikt om het aan uw servers met elk verzoek van dat browser aan uw plaats over te brengen.

Het goedkeuren van een blijvend koekje is bij browser discreet. De meeste webgebruikers begrijpen wat cookies doen en erkennen ook dat cookies van de eerste partij een waardevol voordeel voor hen zijn omdat ze de mogelijkheid bieden om de inhoud van de site aan te passen aan hun voorkeuren. Deze koekjes van de eerste-partij worden niet geblokkeerd door de standaardveiligheidsmontages van populaire browsers. Als een gebruiker verkiest om de koekjes van de eerste-partij te blokkeren, worden hun verzoeken van de paginamening nog geregistreerd, maar de metingsgegevens van die verzoeken kunnen niet betrouwbaar gecorreleerd zijn met een bepaalde bezoeker of hun zittingen op de plaats. Vele plaatsen, vooral de verfijnde dynamische plaatsen, gebruiken reeds de koekjes van de eerste-partij, die in veel gevallen noodzakelijk zijn om Webtoepassingen toe te laten om voor de bezoeker te werken. Een stap terug van een hardnekkig koekje is een zittingskoekje, dat een reeks verzoeken toestaat om samen in een zitting te worden vastgebonden, maar intersessiebezoeker het volgen niet toestaat. [!DNL Site] is in staat om bezoekersgegevens te sessioniseren op basis van sessiecookies of op basis van IP-nummer, maar beide methoden tasten aanzienlijk af van de soorten en de waarde van analyses die kunnen worden uitgevoerd met [!DNL Site] of een ander webactiviteitsanalyse- en rapportagesysteem.

---
description: Een typische configuratie van de Plaats gebruikt koekjes om bezoekers aan uw website uniek te identificeren en hun gedrag in tijd te volgen.
solution: Insight,Analytics
title: Hoe identificeert de plaats Bezoekers?
topic: Data workbench
uuid: e1e451b8-e827-4010-bda9-9147c3b09958
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Hoe identificeert de plaats Bezoekers?{#how-does-site-identify-visitors}

Een typische configuratie van de Plaats gebruikt koekjes om bezoekers aan uw website uniek te identificeren en hun gedrag in tijd te volgen.

De eerste keer dat een bepaalde browser (als bezoeker beschouwd) een verzoek indient van uw website, [!DNL Sensor] werkt met uw Webserver om een blijvend koekje (door gebrek [!DNL cs(cookie)(v1st)]) te plaatsen, dat intern binnen het systeem zoals wordt geïnterpreteerd [!DNL x-trackingid]. Dit cookie wordt slechts eenmaal ingesteld op het allereerste verzoek dat deze bezoeker aan uw website heeft gericht. Het wordt dan verzameld bij die bezoeker telkens als browser een verzoek (of pagina of ingebed objecten verzoek) van uw website in de toekomst indient.

Het goedkeuren van een blijvend koekje is bij browser discreet. Als een gebruiker verkiest om blijvende koekjes te blokkeren, worden hun verzoeken van de paginamening nog geregistreerd, maar de metingsgegevens van die verzoeken zijn niet gecorreleerd met een bepaalde bezoeker of hun zittingen op de website tenzij u een afwisselende methode van bezoekersidentificatie uitvoert, zoals het gebruiken van de transformatie van de Hash op de IP en gebieden UserAgent.

>[!NOTE]
>
>De experimenten van de plaats kunnen slechts in datasets worden geanalyseerd waar de enige methode van bezoekersidentificatie in gebruik de vastgestelde persistente koekjesmethode is. [!DNL Sensor] Sensoren die op J2EE-servers (JBoss, Tomcat, WebLogic en WebSphere) draaien, ondersteunen gecontroleerde experimenten niet.

Tijdens een gecontroleerd experiment kunnen gebruikers die geen cookies accepteren in verschillende experimentele groepen worden geplaatst, van één klik tot één klik. Dit wordt een kwestie slechts als u uw testanalyse met de Breuken Uitgezette Filter van de Zitting uitvoert, die Adobe niet geadviseerd [!DNL Insight].

Zie de * [!DNL Insight] Gebruikershandleiding* voor meer informatie over het Broken Session Filter.

Als een bezoeker het cookie tijdens een experiment wist, krijgt de bezoeker een nieuw cookie toegewezen en kan deze mogelijk aan een andere groep worden toegewezen. Omdat Adobe de bezoeker als nieuw identificeert, wordt het experiment niet ongeldig gemaakt.

---
description: Informatie over het oplossen van problemen met webservers, zoals wanneer de webserver uit de rotatie is gehaald of wanneer de webserver uitvalt.
title: Begrijpen wat de oorzaken zijn
uuid: a2801040-c859-4bf8-90d7-daf3d4f633f3
exl-id: 008116b0-7ef5-41ee-bd2e-a86d61acd634
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Begrijpen wat de oorzaken zijn{#understanding-the-causes}

{{eol}}

Informatie over het oplossen van problemen met webservers, zoals wanneer de webserver uit de rotatie is gehaald of wanneer de webserver uitvalt.

## Wanneer een webserver uit rotatie is gehaald {#section-b9f709099cb44b4f9d1acb38ca5330e3}

Wanneer een Webserver uit omwenteling van een pool van servers wordt gehaald, maar anders met de zender die periodieke hartslagen verzendt verbonden is, wordt het Eind van tijd huidig gehouden en geen interventie van om het even welk deel wordt vereist.

## Wanneer een webserver uitvalt {#section-19280cf83ca44bd7b1ee11bfc74494d2}

Wanneer een webserver volledig offline is als gevolg van een catastrofale fout of geen gegevens of hartslagen verzendt, wordt de waarde &#39;s middags weergegeven op de [!DNL data workbench server] houdt op om ervoor te zorgen dat het de laatste keer vertegenwoordigt [!DNL data workbench server] ontvangen gegevens van ALLE gegevensbronnen waarvan het op de hoogte is. Het systeem zelf blijft gegevens verwerken, die nog steeds beschikbaar zijn voor analyse in de Data Workbench, maar om het even wat in het [!DNL data workbench server] dat is gebaseerd op &#39;as Of time&#39; werkt niet. Bijvoorbeeld, brengt het Vanaf tijd rapportering teweeg en wordt gebruikt om vele afgeleide dimensies in het systeem tot stand te brengen. Wanneer de As-Of-tijd is gestopt, wordt geen rapportage gestart en zijn deze specifieke afgeleide afmetingen niet beschikbaar.

Als WEB2 bijvoorbeeld op 15 juni offline zou gaan en gedurende vijf dagen geen gegevens zou verzenden, zou de &#39;Vanaf&#39;-tijd ergens op 15 juni zijn. De dimensie van gisteren zou bijvoorbeeld 14 juni zijn, hoewel de datum van vandaag 20 juni is.

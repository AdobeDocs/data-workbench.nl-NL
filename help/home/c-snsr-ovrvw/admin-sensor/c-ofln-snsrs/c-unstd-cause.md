---
description: Informatie over het oplossen van problemen met webservers, zoals wanneer de webserver uit de rotatie is gehaald of wanneer de webserver uitvalt.
title: Begrijpen wat de oorzaken zijn
uuid: a2801040-c859-4bf8-90d7-daf3d4f633f3
exl-id: 008116b0-7ef5-41ee-bd2e-a86d61acd634
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Begrijpen van de oorzaken{#understanding-the-causes}

Informatie over het oplossen van problemen met webservers, zoals wanneer de webserver uit de rotatie is gehaald of wanneer de webserver uitvalt.

## Wanneer een webserver uit rotatie {#section-b9f709099cb44b4f9d1acb38ca5330e3} is gehaald

Wanneer een Webserver uit omwenteling van een pool van servers wordt gehaald, maar anders met de zender die periodieke hartslagen verzendt verbonden is, wordt het Eind van tijd huidig gehouden en geen interventie van om het even welk deel wordt vereist.

## Wanneer een webserver {#section-19280cf83ca44bd7b1ee11bfc74494d2} mislukt

Wanneer een webserver volledig offline is als gevolg van een catastrofale fout of geen gegevens of hartslagen verzendt, stopt de functie Op tijd op [!DNL data workbench server] om te garanderen dat deze de laatste keer vertegenwoordigt dat de [!DNL data workbench server] gegevens heeft ontvangen van ALLE gegevensbronnen waarvan de server op de hoogte is. Het systeem zelf blijft gegevens verwerken, die nog voor analyse in Data Workbench beschikbaar zijn, maar om het even wat in [!DNL data workbench server] die op aangezien van tijd gebaseerd is werkt niet. Bijvoorbeeld, brengt het Vanaf tijd rapportering teweeg en wordt gebruikt om vele afgeleide dimensies in het systeem tot stand te brengen. Wanneer de As-Of-tijd is gestopt, wordt geen rapportage gestart en zijn deze specifieke afgeleide afmetingen niet beschikbaar.

Als WEB2 bijvoorbeeld op 15 juni offline zou gaan en gedurende vijf dagen geen gegevens zou verzenden, zou de &#39;Vanaf&#39;-tijd ergens op 15 juni zijn. De dimensie van gisteren zou bijvoorbeeld 14 juni zijn, hoewel de datum van vandaag 20 juni is.

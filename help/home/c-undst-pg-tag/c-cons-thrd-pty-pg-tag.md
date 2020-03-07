---
description: Conceptuele informatie over het etiketteren door derden en het voorkomen van cookie-blokkering met P3P.
solution: Analytics
title: P3P Overwegingen voor het Etiketteren van de Pagina van de derde
topic: Data workbench
uuid: b88d0d22-0ff8-4b63-9be9-7acc12061146
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# P3P Overwegingen voor het Etiketteren van de Pagina van de derde{#p-p-considerations-for-third-party-page-tagging}

Conceptuele informatie over het etiketteren door derden en het voorkomen van cookie-blokkering met P3P.

## Begrijpend de Etikettering van de Pagina van de Derde {#section-8dc5b6b99e454ef7a7cf578ebbf9efca}

In de meeste implementaties, wordt het blijvende koekje van Adobe bekeken als eerste-partijkoekje. De koekjes van de eerste-partij worden gedefinieerd als die verbonden aan het gastheerdomein.

Veronderstel een gebruikersbezoeken http://www.example.com/. Veronderstellend dat een Sensor en operationeel op de Webserver geïnstalleerd is die het domein ontvangt, wordt een blijvend koekje van Adobe geplaatst en als eerstepartijkoekje bekeken. U kunt, echter, meetgegevens van een derdeplaats door het gebruik van ingebedde voorwerpen willen verzamelen, die worden gevraagd en van uw server geladen die [!DNL Sensor] in plaats van de derdeserver loopt die het pagina of reclameprogramma ontvangt. Bijvoorbeeld, dient http://www.example2.com/ een Web-pagina met een ingebed objecten verzoek dat van http://www.example.com/ wordt gediend. Het verzoek om het ingebedde voorwerp van http://www.example.com/ resulteert in een koekje dat wordt geplaatst; nochtans, in deze context, bekijkt Webbrowser of gebruiker-agent het koekje als derdekoekje.

In nieuwere Webbrowsers zoals IE6 van Microsoft, privacy kenmerkt filterkoekjes die op hun compact beleid worden gebaseerd dat in de de reactiekopbal van HTTP van de Webserver wordt verzonden. In de standaardIE6 montages, die de meeste gebruikers nooit veranderen, worden de derdekoekjes geblokkeerd wanneer zij onbestaand of onbevredigend compact beleid hebben. De meeste plaatsen die koekje-blokkerende problemen ervaren hebben derdekoekjes op hun plaats die niet het aangewezen compacte beleid hebben dat in de de reactiekop van HTTP wordt verzonden. Bovendien, komen sommige koekje-blokkerende problemen voor wanneer een plaats door een andere plaats wordt ontworpen. Bijvoorbeeld, kan een online opslag die deel van een online winkelportaal uitmaakt in een kader verschijnen dat door het portaal wordt verstrekt. Vanuit het perspectief van browser, kan de opslaginhoud schijnen om derdeinhoud te zijn wanneer opgesteld door het portaal. Nochtans, als een bezoeker rechtstreeks naar de online opslag gaat zonder door het portaal te gaan, zal de inhoud eerste-partijinhoud zijn. Aldus, vindt de online opslag hun koekjes worden geblokkeerd slechts wanneer de bezoekers binnen door het portaal komen.

De Web-based postsystemen veroorzaken een gelijkaardig probleem. Als een websitebezoeker een Web-pagina aan een vriend e-mailt die een web-based postsysteem gebruikt, verschijnt het e-mailbericht als derdeinhoud aan browser van de vriend omdat het door het e-mailsysteem wordt opgesteld. Als er cookies zijn gekoppeld aan de pagina die per e-mail is verstuurd, worden ze door IE6 behandeld als cookies van derden.

## Het gebruiken van P3P om het Koekje-Blokkeren te verhinderen {#section-96831cad887649f295aec6931750e41a}

P3P verstrekt een standaardmanier voor websites om hun privacybeleid in een computer-leesbaar formaat van XML te coderen. P3P-Toegelaten Webbrowsers en andere P3P gebruikersagenten halen automatisch P3P privacybeleid, ontleden hen, en vergelijken hen met de privacyvoorkeur van een gebruiker.

Om IE6 te verhinderen koekjes op uw plaats te blokkeren, moet u het volgende verzekeren:

1. Alle koekjes die in een derdecontext worden geplaatst hebben P3P compact beleid verbonden aan hen.
1. Het aangewezen compacte beleid wordt verzonden gebruikend een de reactiekop van douaneHTTP.
1. Dit compacte beleid wordt door IE6 bevredigend geacht.
1. Als de derdekoekjes door een ander bedrijf worden geplaatst, kunt u hen moeten vragen om P3P toe te laten en P3P compact beleid te plaatsen. Om het even welke gastheer die een P3P compact beleid plaatst moet ook een overeenkomstig volledig P3P beleid hebben. De gebruikers kunnen hun montages veranderen IE6 zodat de koekjes ook onder andere voorwaarden worden geblokkeerd; het plaatsen van bevredigend compact beleid op derdekoekjes verhindert echter de meeste IE6 koekjesblokkering.

Het volgende is een voorbeeld van zulk een P3P kopbal:

```
P3P: policyref=” http://www.myserver.com/w3c/p3p.xml”, CP=”NOI DSP COR PSA PSD OUR IND COM NAV”
```

In dit voorbeeld, [!DNL p3p.xml] wordt het dossier gebruikt om een bijbehorend [!DNL policy.xml] dossier van verwijzingen te voorzien dat op uw Webserver verblijft dat de soorten informatie aangeeft uw website verzamelt, de methodes van de geschillenbeslechting die uw organisatie volgt, hoe de verzamelde gegevens worden gebruikt, wie de gegevens, en andere standaardinformatie met betrekking tot de Privacy van Internet bezit. De drie karaktercodes na &quot;CP&quot;zijn de compacte beleidscodes die nastreven wat binnen uw [!DNL policy.xml] dossier wordt verklaard.

Alle compacte beleidsregels en de dossiers van beleidXML zouden voor de respectieve organisatie moeten worden aangepast waarvoor zij worden opgesteld, nauwkeurig specificerend hun intern privacybeleid met betrekking tot de inzameling van websitegegevens. Een groot aantal P3P beleidsredacteurs kan online samen met meer diepgaande informatie met betrekking tot het uitvoeren van een aangewezen privacybeleid binnen uw website worden gevonden.

Voor meer informatie over hoe Internet Explorer 6 kopballen P3P behandelt, gelieve te bezoeken:

[http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnpriv/html/ie6privacyfeature.asp](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnpriv/html/ie6privacyfeature.asp)

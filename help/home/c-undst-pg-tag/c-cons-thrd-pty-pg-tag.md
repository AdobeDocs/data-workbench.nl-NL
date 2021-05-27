---
description: Conceptuele informatie over het coderen van cookies door derden en het voorkomen van het blokkeren van cookies met P3P.
title: P3P Overwegingen bij paginatags van derden
uuid: b88d0d22-0ff8-4b63-9be9-7acc12061146
exl-id: 8eb521b6-802c-4d9f-a6b4-b1c4f694b8b8
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---

# P3P Overwegingen bij paginatags van derden{#p-p-considerations-for-third-party-page-tagging}

Conceptuele informatie over het coderen van cookies door derden en het voorkomen van het blokkeren van cookies met P3P.

## Pagina&#39;s van derden coderen {#section-8dc5b6b99e454ef7a7cf578ebbf9efca}

In de meeste implementaties wordt de Adobe permanente cookie beschouwd als een eersteklas cookie. Cookies van de eerste partij worden gedefinieerd als cookies die zijn gekoppeld aan het hostdomein.

Stel dat een gebruiker http://www.example.com/ bezoekt. Ervan uitgaande dat een sensor is geïnstalleerd en operationeel is op de webserver waarop het domein wordt gehost, wordt een Adobe-permanente cookie ingesteld en weergegeven als een cookie van de eerste partij. Het kan echter zijn dat u meetgegevens wilt verzamelen van derden via het gebruik van ingesloten objecten, die worden opgevraagd en geladen van de server waarop [!DNL Sensor] wordt uitgevoerd in plaats van van de externe server waarop de pagina of het advertentieprogramma wordt gehost. Bijvoorbeeld: http://www.example2.com/ dient een webpagina met een ingesloten objectverzoek van http://www.example.com/. De aanvraag voor het ingesloten object van http://www.example.com/ resulteert in een cookie die wordt ingesteld. in deze context echter, ziet Webbrowser of gebruiker-agent het koekje als derdekoekje.

In nieuwere webbrowsers, zoals IE6 van Microsoft, filtercookies met privacyfuncties op basis van hun compacte beleid dat in de HTTP-antwoordheader van de webserver wordt verzonden. In de standaard IE6-instellingen, die de meeste gebruikers nooit wijzigen, worden cookies van andere bedrijven geblokkeerd wanneer ze een niet-bestaand of onbevredigend compact beleid hebben. De meeste sites die problemen ondervinden met het blokkeren van cookies hebben cookies van derden op hun site die niet het juiste compacte beleid hebben dat wordt verzonden in de HTTP-antwoordheader. Bovendien treden sommige cookie-blokkerende problemen op wanneer een site door een andere site wordt geframed. Een onlinewinkel die deel uitmaakt van een online winkelportaal, kan bijvoorbeeld worden weergegeven in een kader dat door het portaal wordt geleverd. Vanuit het perspectief van browser, kan de opslaginhoud schijnen om derdeinhoud te zijn wanneer opgesteld door het portaal. Als een bezoeker echter rechtstreeks naar de online winkel gaat zonder het portaal te doorlopen, is de inhoud inhoud inhoud van de eerste partij. Zo vindt de online winkel dat hun cookies alleen worden geblokkeerd wanneer bezoekers via de portal binnenkomen.

Webmailsystemen veroorzaken een vergelijkbaar probleem. Als een websitebezoeker een webpagina per e-mail verzendt naar een vriend die een op internet gebaseerd e-mailsysteem gebruikt, wordt het e-mailbericht weergegeven als inhoud van derden voor de browser van de vriend, omdat het wordt opgesteld door het e-mailsysteem. Als er cookies zijn gekoppeld aan de pagina die per e-mail is verzonden, worden deze door IE6 beschouwd als cookies van derden.

## P3P gebruiken om cookie-blokkeren te voorkomen {#section-96831cad887649f295aec6931750e41a}

P3P biedt websites een standaardmanier om hun privacybeleid te coderen in een voor computers leesbare XML-indeling. P3P-webbrowsers en andere P3P-gebruikersagents halen automatisch P3P-privacybeleid, parseren deze en vergelijken deze met de privacyvoorkeuren van een gebruiker.

Om te voorkomen dat IE6 cookies op uw site blokkeert, moet u het volgende doen:

1. Alle koekjes die in een derdecontext worden geplaatst hebben P3P compact beleid verbonden aan hen.
1. Het aangewezen compacte beleid wordt verzonden gebruikend een de reactiekop van douaneHTTP.
1. Dit compacte beleid wordt door IE6 bevredigend geacht.
1. Als de derdekoekjes door een ander bedrijf worden geplaatst, kunt u hen moeten vragen om P3P toe te laten en P3P compact beleid te plaatsen. Om het even welke gastheer die een P3P compact beleid plaatst moet ook een overeenkomstig volledig P3P beleid hebben. Gebruikers kunnen hun IE6-instellingen wijzigen, zodat cookies ook onder andere omstandigheden worden geblokkeerd. het plaatsen van bevredigende compacte beleidsregels op cookies van derden voorkomt echter dat cookies van de meeste IE6-cookies worden geblokkeerd.

Hier volgt een voorbeeld van een dergelijke P3P-header:

```
P3P: policyref=” http://www.myserver.com/w3c/p3p.xml”, CP=”NOI DSP COR PSA PSD OUR IND COM NAV”
```

In dit voorbeeld wordt het bestand [!DNL p3p.xml] gebruikt om te verwijzen naar een gekoppeld [!DNL policy.xml]-bestand dat zich op uw webserver bevindt. Dit bestand geeft het soort informatie aan dat uw website verzamelt, methoden voor geschillenbeslechting die uw organisatie volgt, hoe de verzamelde gegevens worden gebruikt, wie de gegevens bezit en andere standaardinformatie met betrekking tot internetprivacy. De drie karaktercodes na &quot;CP&quot;zijn de compacte beleidscodes die emuleren wat binnen uw [!DNL policy.xml] dossier wordt verklaard.

Alle compacte beleidsregels en beleid-XML-bestanden moeten zijn toegesneden op de respectievelijke organisatie waarvoor ze worden geïmplementeerd, waarbij hun interne privacybeleid met betrekking tot het verzamelen van websitegegevens nauwkeurig wordt aangegeven. Een groot aantal P3P-beleidseditors vindt u online, samen met meer gedetailleerde informatie over de implementatie van een geschikt privacybeleid op uw website.

Voor meer informatie over hoe Internet Explorer 6 de Kopballen van P3P behandelt, gelieve te bezoeken:

[http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnpriv/html/ie6privacyfeature.asp](http://msdn.microsoft.com/library/default.asp?url=/library/en-us/dnpriv/html/ie6privacyfeature.asp)

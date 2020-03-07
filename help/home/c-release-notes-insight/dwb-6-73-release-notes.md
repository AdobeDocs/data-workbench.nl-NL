---
description: Nieuwe eigenschappen en moeilijke situaties in Werkbank 6.73 van Gegevens.
title: Gegevens Workbench 6.73 Release Notes
uuid: bba63a8c-9cb7-4334-b66a-22db92153066
translation-type: tm+mt
source-git-commit: 2cba66a160fec9154796f093d04a422a5b0da265

---


# Gegevens Workbench 6.73 Release Notes{#data-workbench-release-notes}

Nieuwe eigenschappen en moeilijke situaties in Werkbank 6.73 van Gegevens.

## Gegevens Workbench 6.73 Release Notes {#topic-7655534554ac4a4b816af1bd73b06aad56757}

Nieuwe eigenschappen en moeilijke situaties in Werkbank 6.73 van Gegevens.

## Fixes {#section-160baf6ea04c45a993777ee4260691ed}

* Vaste een probleem in Werkstation waar gebruikers niet konden inloggen op bepaalde hardware met hoge resolutie en hoge DPI.
* Vast een kwestie in de server aan waar E-mail in de dossiernamen van het Archief toen het gebruiken van login IMS ontbrak.
* Bijgewerkt OpenSSL aan versie 1.1.0h die verscheidene kwetsbaarheidsmoeilijke situaties en nieuwe SSL Ciphers omvat.
* Bijgewerkt de hieronder vermelde open bronbibliotheken aan de recentste stabiele versies

   * libssh2 1,8,0
   * Apache Xerces 3.2.1
   * Apache Xalan 1,11
   * libpng 1,6,34
   * libarchief 3.3.2
   * zlib 1.2.11
   * pm 8.42

* Toegevoegde fout registreren wanneer de telling van de de dossierrij van de Raadpleging meer dan gesteunde 357913908 rijen overschrijdt.

## Bekende kwestie {#section-f2cb932f6225457a872fb916a78df89a}

* Versie van het Werkstation van de Werkbank van gegevens 6.73 verbindt niet met versies van de Servers van de Werkbank van Gegevens 6.61 en ouder. De reden is, de oudere serverversies gebruiken een zwakke vorm van ciphers niet die in versie 6.73 worden gesteund. Om steun voor oudere versies toe te laten

   1. De standaardSSL van de opheffing lijst van CIFERS op de server met een sterke die cijferlijst door OpenSSL versie 1.0.1h wordt gesteund. Om met voeten te treden, voeg zeer belangrijke &quot;SSL CIFERS&quot;in de dossiers &quot;Communications.cfg&quot;beschikbaar in &quot;Componenten&quot;en &quot;Componenten voor de Verwerking van Servers&quot;folders toe. Bijvoorbeeld: `SSL Ciphers = string: !aNULL:AESGCM`

      >[!NOTE]
      >
      >Zorg ervoor dat de sleutel op het zelfde niveau wordt geplaatst zoals de SSL Haven. Voor details verwijs naar de Montages van de [Communicatie Configuratie](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/config-settings/c-comm-cfg-stgs.html)

   1. Plaats het recentste trust_ca_cert.pem- dossier op de server 6.61 en oudere servers. Dit het plaatsen is toepasselijk op al Werkstation 6.7x versies.

Zie de [gearchiveerde versienota&#39;s](https://docs.adobe.com/content/help/en/data-workbench/using/release-notes/release-notes.html) voor Werkbank van Gegevens 5.3 tot 5.52.

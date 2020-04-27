---
description: Nieuwe functies en correcties in Data Workbench 6.73.
title: Opmerkingen bij de release Data Workbench 6.73
uuid: bba63a8c-9cb7-4334-b66a-22db92153066
translation-type: tm+mt
source-git-commit: 9552a2f9fe4e450b1e212b38a09f77252a009419

---


# Opmerkingen bij de release Data Workbench 6.73{#data-workbench-release-notes}

Nieuwe functies en correcties in Data Workbench 6.73.

## Oplossingen {#section-160baf6ea04c45a993777ee4260691ed}

* Probleem verholpen in Workstation waarbij gebruikers zich niet konden aanmelden op een hardware met hoge resolutie en hoge DPI.
* Probleem verholpen waarbij e-mail ontbrak in bestandsnamen archiveren bij gebruik van IMS-aanmelding.
* Bijgewerkte OpenSSL naar versie 1.1.0h, die verscheidene kwetsbaarheidsmoeilijke situaties en nieuwe SSL CIFERS omvat.
* De onderstaande opensource-bibliotheken bijgewerkt met de nieuwste stabiele versies

   * libssh2 1.8.0
   * Apache Xerces 3.2.1
   * Apache Xalan 1.11
   * libpng 1.6.34
   * libarchive 3.3.2
   * zlib 1.2.11
   * pcre 8.42

* Toegevoegde foutenregistratie wanneer het aantal rijen van de het dossierrij van de Opzoeken meer dan gesteunde 357913908 rijen overschrijdt.

## Bekend probleem {#section-f2cb932f6225457a872fb916a78df89a}

* Data Workbench Workstation versie 6.73 maakt geen verbinding met Data Workbench Servers versie 6.61 en ouder. De reden hiervoor is dat oudere serverversies een zwakke vorm van ciphers gebruiken die niet wordt ondersteund in versie 6.73. Ondersteuning voor oudere versies inschakelen

   1. Overschrijf de standaard-SSL-ciphers-lijst op de server met een sterke lijst van citeurs die wordt ondersteund door OpenSSL-versie 1.0.1h. Als u de code wilt overschrijven, voegt u de sleutel &quot;SSL-ciphers&quot; toe aan de bestanden &quot;Communications.cfg&quot; in de mappen &quot;Components&quot; en &quot;Components for Processing Servers&quot;. Bijvoorbeeld: `SSL Ciphers = string: !aNULL:AESGCM`

      >[!NOTE]
      >
      >Zorg ervoor dat de sleutel op het zelfde niveau wordt geplaatst zoals de SSL Haven. Voor details verwijs naar de Montages van de Configuratie van de [Mededelingen](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/config-settings/c-comm-cfg-stgs.html)

   1. Plaats het nieuwste bestand trust_ca_cert.pem op de server 6.61 en oudere servers. Deze instelling is van toepassing op alle 6,7x-werkstations.

Zie [gearchiveerde releaseopmerkingen](https://docs.adobe.com/content/help/en/data-workbench/using/release-notes/release-notes.html) voor Data Workbench 5.3 tot en met 5.52.

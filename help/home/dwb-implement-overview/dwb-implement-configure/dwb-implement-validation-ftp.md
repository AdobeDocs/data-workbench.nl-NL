---
description: Dit is een snelle handleiding die u de minimale stappen geeft die nodig zijn om de interne en externe FTP-installatie te valideren.
title: Validatie van interne en externe FTP-servers
uuid: bc381c1d-df27-4009-920b-1a804b36c204
exl-id: 8eecfda7-ffa0-458c-a518-434758344bfe
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Validatie van interne en externe FTP-servers{#validation-of-internal-and-external-ftp-servers}

{{eol}}

Dit is een snelle handleiding die u de minimale stappen geeft die nodig zijn om de interne en externe FTP-installatie te valideren.

Een interne FTP wordt gebruikt wanneer een consultant/architect die intern is met Adobe verbinding moet maken met de FTP-site voor het uploaden of downloaden van bestanden, terwijl een externe FTP voornamelijk voor u als gebruiker is om de vereiste gegevensbestanden te uploaden.

Voor meer informatie over het instellen van FTP-servers raadpleegt u [File Transfer Protocol](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/ftp-overview.html).

## Validatiestappen - Externe FTP {#section-24428111b5c542ce81a765cd63424b97}

1. Een opdrachtprompt openen. (Windows+R en type cmd)
1. Type ftp `<ftp server>`
1. Geef een gebruikersnaam en wachtwoord op. ![](assets/dwb_impl_ftp1.png)

1. Wijzig de lokale map van waaruit een bestand kan worden verplaatst. Gebruik deze opdracht:

[!DNL ftp> lcd C:\Users\andixit\Desktop]

lokale map nu [!DNL C:\Users\andixit\Desktop].

1. Kopieer het bestand van de lokale naar de externe locatie. ![](assets/dwb_impl_ftp2.png)

1. Afmelden bij externe server. (Gebruik onder opdracht)

[!DNL ftp> bye]

[!DNL 221 Goodbye]

>[!NOTE]
>
>Een andere manier om FTP te valideren is door Filezilla te gebruiken. Geef de hostnaam, gebruikersnaam, wachtwoord en poort op. De rechterzijde van het deelvenster is een externe site en de linkerzijde is een lokale site. Als u FTP wilt valideren, kunt u bestanden van de lokale naar de externe site en v.v. slepen en neerzetten.

![](assets/dwb_impl_ftp3.png)

## Validatiestappen - Interne FTP {#section-b1f7a789ad6848cf9027f7953d81066e}

De bovenstaande stappen kunnen worden uitgevoerd om interne ftp van elke Adobe-server te valideren.

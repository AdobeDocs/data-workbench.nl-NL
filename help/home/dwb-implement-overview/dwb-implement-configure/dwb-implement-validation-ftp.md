---
description: Dit is een snelle gids die u de minimumstappen geeft die worden vereist om de Interne en Externe opstelling van FTP te bevestigen.
title: Validatie van interne en externe FTP-servers
uuid: bc381c1d-df27-4009-920b-1a804b36c204
translation-type: tm+mt
source-git-commit: ded50c4eeadea80156c17a4cad985d0ceddd5500

---


# Validatie van interne en externe FTP-servers{#validation-of-internal-and-external-ftp-servers}

Dit is een snelle gids die u de minimumstappen geeft die worden vereist om de Interne en Externe opstelling van FTP te bevestigen.

Een intern FTP wordt gebruikt wanneer een consultant/architect intern met Adobe met de plaats van FTP voor dossier moet verbinden uploadt of downloadt, terwijl extern FTP hoofdzakelijk voor u als gebruiker is om de vereiste gegevensdossiers te uploaden.

Voor extra informatie bij de servers van opstellingsFTP, zie het Protocol van de Overdracht van het [Dossier](https://docs.adobe.com/content/help/en/analytics/export/ftp-and-sftp/ftp-overview.html).

## Bevestigingsstappen - Extern FTP {#section-24428111b5c542ce81a765cd63424b97}

1. Open een Herinnering van het Bevel. (Windows+R en type cmd)
1. Type ftp `<ftp server>`
1. Verstrek gebruikersnaam en wachtwoord. ![](assets/dwb_impl_ftp1.png)

1. De lokale folder van de verandering van waar één of ander dossier kan worden bewogen. Gebruik dit bevel:

[!DNL ftp> lcd C:\Users\andixit\Desktop]

lokale map nu [!DNL C:\Users\andixit\Desktop].

1. Het dossier van het exemplaar van lokaal aan verre plaats. ![](assets/dwb_impl_ftp2.png)

1. Afmelden bij externe server. (Gebruik onder bevel)

[!DNL ftp> bye]

[!DNL 221 Goodbye]

>[!NOTE]
>
>Een andere manier om FTP te bevestigen is Filezilla te gebruiken. Verstrek de Naam van de Gastheer, de Naam van de Gebruiker, het Wachtwoord en de Haven. De rechterkant van het paneel is verre plaats en de linkerkant is lokale plaats. Om FTP te bevestigen sleep en laat vallen dossiers van lokaal aan verre plaats en v.v.

![](assets/dwb_impl_ftp3.png)

## Bevestigingsstappen - intern FTP {#section-b1f7a789ad6848cf9027f7953d81066e}

De bovengenoemde stappen kunnen worden gevolgd om interne FTP van om het even welke server van Adobe te bevestigen.

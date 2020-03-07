---
description: Instructies voor het gebruiken van douanecertificaten.
title: Het gebruiken van de Certificaten van de Douane in de Werkbank van Gegevens
uuid: c3a2db27-bdb2-44b3-95dd-65eedd05c957
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# Het gebruiken van de Certificaten van de Douane in de Werkbank van Gegevens{#using-custom-certificates-in-data-workbench}

Instructies voor het gebruiken van douanecertificaten.

Een certificaat dat door of de cliënt of de server van de Werkbank van Gegevens wordt gebruikt moet door vertrouwde op CA (de Autoriteit van het Certificaat) worden ondertekend. De klanten van de Werkbank van gegevens ontvangen certificaten die door de Visuele Wetenschappen CA. worden ondertekend. Deze certificaten worden vertrouwd op door de software van de Werkbank van Gegevens, aangezien [!DNL trust_ca_cert.pem] (die samen met de software van het Inzicht wordt verstrekt en in de folder van **Certificaten** van zowel servers als cliënten wordt opgeslagen) een Certificaat *van CA van de* Wortel voor Visual Sciences CA bevat. Deze certificaten worden gebruikt voor zowel het verlenen van vergunningen van de software als authentificatie wanneer de cliënten en de servers met elkaar gebruikend SSL communiceren. Slechts kunnen de certificaten die door Visuele Wetenschappen CA worden uitgegeven voor vergunning worden gebruikt, maar andere certificaten kunnen voor mededeling en authentificatie worden gebruikt. Certificaten die door andere CA&#39;s dan Visual Sciences zijn afgegeven, worden hieronder aangeduid als *douanecertificaten.*

**Belangrijke opmerking:** Voor servers en cliënten, gebruikt de software van de Werkbank van Gegevens de certificaatdossiers die in de cliënt of de folder van de **Certificaten** van de server worden geïnstalleerd of certificaten die uitdrukkelijk in zijn configuratie worden geïdentificeerd. Nochtans, kunt u de Opslag [van het Certificaat van](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/crypto-api.md#concept-4acb13b7de9340ea8cde8ad84b93358d) Vensters voor cliënten ook gebruiken.

De volgende instructies beschrijven de procedures die moeten worden gevolgd om douanecertificaten voor communicatie tussen de cliënten en de servers van de Werkbank van Gegevens te gebruiken. Niet elk detail is een harde eis en er kunnen verschillende variaties in het proces worden toegepast. De onderstaande procedures zijn echter getest om te werken.

## Aangepaste clientcertificaten instellen {#section-2083fd41973e451fa404e7a4ae4da591}

1. Voeg het certificaat van het uitgeven CA aan toe [!DNL trust_cert_ca.pem], dat in de folder van **Certificaten** van de cliënt en dat van elke server in elke cluster geïnstalleerd is die moet worden betreden gebruikend dit douanecertificaat.

1. Verkrijg een douanecertificaat voor elke server in de cluster met de volgende voorwaarden:

   1. Het certificaat is geformatteerd als [!DNL .pem] certificaat.
   1. Het certificaat bevat zijn sleutel en is unencrypted (d.w.z., heeft het geen wachtwoord/pasuitdrukking).

      Een certificaat bevat zijn sleutel met één van de volgende lijnen:

      ```
      BEGIN PRIVATE KEY 
      BEGIN RSA PRIVATE KEY
      ```

      Één manier om de wachtwoorduitdrukking uit een [!DNL .pem] certificaat te verwijderen:

      ```
      openssl rsa  -in password-protected-cert.pem -out no-password-cert.pem 
      openssl x509 -in password-protected-cert.pem >> no-password.pem
      ```

   1. Het certificaat heeft de GN, O, OU, enz. zoals vereist voor deze cliënt in het dossier van de servers [!DNL Access Control.cfg] .
   1. Certificaat werd afgegeven met een *doel **** van *cliënt* (of zowel *server* **als** *cliënt*).

      Om te verifiëren dat een certificaat een doelcode van server en/of cliënt heeft, kunnen de volgende bevelen worden gebruikt:

      ```
      openssl verify -CAfile trust_ca_cert.pem -purpose sslserver -x509_strict custom_communications_cert.pem 
      openssl verify -CAfile trust_ca_cert.pem -purpose sslclient -x509_strict custom_communications_cert.pem
      ```

      Voor een servercertificaat, zouden beide bevelen moeten opbrengen:

      ```
      custom_communications_cert.pem: OK
      ```

      Voor een cliëntcertificaat, slechts wordt het tweede bevel vereist om op te brengen [!DNL OK].

1. Plaats het certificaat in de folder van de **Certificaten** van de cliënt.
1. In [!DNL Insight.cfg] onder *serverInfo* voor elke cluster die u dit certificaat wilt gebruiken, zorg ervoor de *douanecliënt cert* wordt genoemd, zoals:

   ```
   Servers = vector: 1 items 
     0 = serverInfo: 
       SSL Client Certificate = string:
   <my_custom_client_cert.pem>
   ```

## Aangepaste servercertificaten instellen {#setting-up-custom-server-certificates}

Deze sectie veronderstelt dat u een cluster hebt die in gebruik is, gebruikend Visual Sciences verstrekte certificaten, en de configuratie volgt gemeenschappelijke praktijken (zoals de *Componenten voor de folder van de Servers* van de Verwerking op de meester gesynchroniseerd aan de *folders van Componenten* van alle DPUs) volgt.

1. Voeg het certificaat van het uitgeven CA aan toe [!DNL trust_cert_ca.pem] die op elke server in de cluster en elke cliënt geïnstalleerd is die met deze cluster moet communiceren.
1. Verkrijg een douanecertificaat voor elke server in de cluster met deze vereisten:

   1. Het certificaat van de douane is geformatteerd als [!DNL .pem] certificaat.
   1. Het certificaat bevat zijn sleutel en is unencrypted (d.w.z., heeft het geen wachtwoord/pasuitdrukking).

      Een certificaat bevat zijn sleutel als het een lijn zoals heeft:

      ```
      BEGIN PRIVATE KEY 
      BEGIN RSA PRIVATE KEY
      ```

      Één manier om de wachtwoorduitdrukking uit een [!DNL .pem] certificaat te verwijderen:

      ```
      openssl rsa  -in password-protected-cert.pem -out no-password-cert.pem 
      openssl x509 -in password-protected-cert.pem >> no-password.pem
      ```

   1. Het certificaat heeft de zelfde GN zoals [!DNL server_cert.pem] momenteel geïnstalleerd op de server.
   1. Het certificaat werd uitgegeven met een doel van *server* en *cliënt*.

      Om te verifiëren dat een certificaat een doelcode van server en/of cliënt heeft, kunnen de volgende bevelen worden gebruikt:

      ```
      openssl verify -CAfile trust_ca_cert.pem -purpose sslserver -x509_strict custom_communications_cert.pem 
      openssl verify -CAfile trust_ca_cert.pem -purpose sslclient -x509_strict custom_communications_cert.pem
      ```

      Voor een servercertificaat, zouden beide bevelen moeten opbrengen:

      ```
      custom_communications_cert.pem: OK
      ```

      Voor een cliëntcertificaat, slechts wordt het tweede bevel vereist om op te brengen [!DNL OK].

1. Installeer het douanecertificaat van elke server in de folder van **Certificaten** van de server zoals [!DNL custom_communications_cert.pem].

1. Gebruikend een tekstredacteur, voeg de volgende lijn aan **Communications.cfg** - dossier in zowel de *Componenten* als *Componenten voor de folders van de Servers* van de Verwerking, direct onder de eerste lijn ([!DNL component = CommServer]) toe:

   ```
   Certificate = string: Certificates\\custom_communications_cert.pem
   ```

1. Start alle servers opnieuw op.

**Informatie over waarschuwing voor fouten in certificaten**

Wanneer de server of de cliënt van het Inzicht een **vergunningscertificaat** in de folder van **Certificaten** zoekt, probeert het om alle certificaten (behalve [!DNL trust_ca_cert.pem]), tegen een hard gecodeerd exemplaar van het certificaat van CA van het Inzicht te bevestigen, dat op om het even welk douanecertificaat ontbreekt dat in de folder aanwezig is. De server geeft deze waarschuwing uit:

```
Certificate failed to verify. Error 20 at 0 depth. Desc: unable to get local issuer certificate. Cert details:
```

Deze waarschuwing kan veilig worden genegeerd.

---
description: Instructies voor het gebruik van aangepaste certificaten.
title: Aangepaste certificaten gebruiken in Data Workbench
uuid: c3a2db27-bdb2-44b3-95dd-65eedd05c957
exl-id: f813d599-723f-4b5d-a0b5-f4d71c1b1a22
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# Aangepaste certificaten gebruiken in Data Workbench{#using-custom-certificates-in-data-workbench}

{{eol}}

Instructies voor het gebruik van aangepaste certificaten.

Een certificaat dat door de client of server van de Data Workbench wordt gebruikt, moet door een vertrouwde certificeringsinstantie (Certificate Authority) worden ondertekend. Klanten van Data Workbench ontvangen certificaten die door de Visual Sciences CA zijn ondertekend. Deze certificaten worden vertrouwd door de software van de Data Workbench, aangezien [!DNL trust_ca_cert.pem] (wordt samen met de Insight-software geleverd en in het **Certificaten** map van zowel servers als clients) bevat een *Root CA-certificaat* voor de Visual Sciences CA. Deze certificaten worden gebruikt voor zowel licenties voor de software als verificatie wanneer clients en servers met elkaar communiceren via SSL. Alleen door de Visual Sciences CA uitgegeven certificaten kunnen worden gebruikt voor licenties, maar andere certificaten kunnen worden gebruikt voor communicatie en verificatie. Door andere CA&#39;s dan Visual Sciences uitgegeven certificaten worden hieronder aangeduid als *aangepaste certificaten.*

**Belangrijke opmerking:** Voor servers en clients gebruikt de software van de Data Workbench de certificaatbestanden die zijn geïnstalleerd op de client of server **Certificaten** map of certificaten die expliciet in de configuratie ervan worden geïdentificeerd. U kunt echter ook de opdracht [Windows-certificaatarchief](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/crypto-api.md#concept-4acb13b7de9340ea8cde8ad84b93358d) voor clients.

De volgende instructies beschrijven de procedures die moeten worden gevolgd om douanecertificaten voor communicatie tussen de cliënten en de servers van de Data Workbench te gebruiken. Niet elk detail is een harde eis en er kunnen verschillende variaties in het proces worden toegepast. Onderstaande procedures zijn echter getest om te werken.

## Aangepaste clientcertificaten instellen {#section-2083fd41973e451fa404e7a4ae4da591}

1. Voeg het certificaat van de uitgevende CA toe aan de [!DNL trust_cert_ca.pem], die in de **Certificaten** directory van de client en die van elke server in elke cluster waartoe met dit aangepaste certificaat toegang moet worden verkregen.

1. Vraag een aangepast certificaat aan voor elke server in de cluster met de volgende voorwaarden:

   1. Certificaat is opgemaakt als een [!DNL .pem] certificaat.
   1. Het certificaat bevat de sleutel en is niet versleuteld (het heeft dus geen wachtwoord/woordgroep).

      Een certificaat bevat de sleutel met een van de volgende regels:

      ```
      BEGIN PRIVATE KEY 
      BEGIN RSA PRIVATE KEY
      ```

      Een manier om de wachtwoorduitdrukking te verwijderen uit een [!DNL .pem] certificaat:

      ```
      openssl rsa  -in password-protected-cert.pem -out no-password-cert.pem 
      openssl x509 -in password-protected-cert.pem >> no-password.pem
      ```

   1. Het certificaat heeft de CN, O, OU, enz. zoals vereist voor deze client in de servers [!DNL Access Control.cfg] bestand.
   1. Het certificaat is afgegeven met een *doel&#42;&#42;&#42;* van *client* (of beide *server* **en** *client*).

      Om te verifiëren dat een certificaat een doelcode van server en/of cliënt heeft, kunnen de volgende bevelen worden gebruikt:

      ```
      openssl verify -CAfile trust_ca_cert.pem -purpose sslserver -x509_strict custom_communications_cert.pem 
      openssl verify -CAfile trust_ca_cert.pem -purpose sslclient -x509_strict custom_communications_cert.pem
      ```

      Voor servercertificaten moeten beide opdrachten het volgende opleveren:

      ```
      custom_communications_cert.pem: OK
      ```

      Voor een clientcertificaat is alleen de tweede opdracht vereist om te renderen [!DNL OK].

1. Het certificaat in de client plaatsen **Certificaten** directory.
1. In [!DNL Insight.cfg] onder de *serverInfo* voor elke cluster die u dit certificaat wilt gebruiken, controleert u of de *aangepast clientcertificaat* wordt genoemd, zoals:

   ```
   Servers = vector: 1 items 
     0 = serverInfo: 
       SSL Client Certificate = string:
   <my_custom_client_cert.pem>
   ```

## Aangepaste servercertificaten instellen {#setting-up-custom-server-certificates}

Deze sectie veronderstelt dat u een cluster hebt die in werking is, gebruikend Visual Sciences uitgegeven certificaten, en de configuratie volgt gemeenschappelijke praktijken (zoals *Componenten voor het verwerken van servers* op de master map wordt gesynchroniseerd met de *Componenten* mappen van alle DPU&#39;s).

1. Voeg het certificaat van de uitgevende CA toe aan de [!DNL trust_cert_ca.pem] Deze wordt geïnstalleerd op elke server in de cluster en op elke client die met deze cluster moet communiceren.
1. Vraag een aangepast certificaat aan voor elke server in de cluster met de volgende vereisten:

   1. Aangepast certificaat is opgemaakt als een [!DNL .pem] certificaat.
   1. Het certificaat bevat de sleutel en is niet versleuteld (het heeft dus geen wachtwoord/woordgroep).

      Een certificaat bevat zijn sleutel als het een lijn zoals heeft:

      ```
      BEGIN PRIVATE KEY 
      BEGIN RSA PRIVATE KEY
      ```

      Een manier om de wachtwoorduitdrukking te verwijderen uit een [!DNL .pem] certificaat:

      ```
      openssl rsa  -in password-protected-cert.pem -out no-password-cert.pem 
      openssl x509 -in password-protected-cert.pem >> no-password.pem
      ```

   1. Het certificaat heeft dezelfde GN als het [!DNL server_cert.pem] momenteel op de server geïnstalleerd.
   1. Het certificaat is uitgegeven met het doel *server* en *client*.

      Om te verifiëren dat een certificaat een doelcode van server en/of cliënt heeft, kunnen de volgende bevelen worden gebruikt:

      ```
      openssl verify -CAfile trust_ca_cert.pem -purpose sslserver -x509_strict custom_communications_cert.pem 
      openssl verify -CAfile trust_ca_cert.pem -purpose sslclient -x509_strict custom_communications_cert.pem
      ```

      Voor servercertificaten moeten beide opdrachten het volgende opleveren:

      ```
      custom_communications_cert.pem: OK
      ```

      Voor een clientcertificaat is alleen de tweede opdracht vereist om te renderen [!DNL OK].

1. Installeer het aangepaste certificaat van elke server in het dialoogvenster **Certificaten** directory van de server als [!DNL custom_communications_cert.pem].

1. Voeg met een teksteditor de volgende regel toe aan **Communications.cfg** in beide *Componenten* en *Componenten voor het verwerken van servers* directory&#39;s, direct onder de eerste regel ([!DNL component = CommServer]):

   ```
   Certificate = string: Certificates\\custom_communications_cert.pem
   ```

1. Start alle servers opnieuw.

**Waarschuwing bij certificaatfout**

Wanneer de Insight-server of -client op zoek is naar een **licentie** in het **Certificaten** map, wordt geprobeerd alle certificaten te valideren (behalve [!DNL trust_ca_cert.pem]), tegen een hard gecodeerde kopie van het Insight CA-certificaat, die mislukt op een aangepast certificaat dat aanwezig is in de directory. De server geeft deze waarschuwing af:

```
Certificate failed to verify. Error 20 at 0 depth. Desc: unable to get local issuer certificate. Cert details:
```

Deze waarschuwing kan veilig worden genegeerd.

---
description: Nadat u de Insight-programmabestanden hebt geïnstalleerd, moet u het digitale certificaat downloaden en installeren dat u van Adobe hebt ontvangen.
title: Het digitale certificaat downloaden en installeren (Insight)
uuid: 93ab2222-a977-4279-9e1e-71038b1d1cfa
exl-id: 0dff95ae-880b-45d5-96df-4eb6bea58891
source-git-commit: 235b8816c7397ac1ab71df650a1d4c2d681b3b2d
workflow-type: tm+mt
source-wordcount: '2744'
ht-degree: 0%

---

# Het digitale certificaat downloaden en installeren{#downloading-and-installing-the-digital-certificate}

Nadat u de Insight-programmabestanden hebt geïnstalleerd, moet u het digitale certificaat downloaden en installeren dat u van Adobe hebt ontvangen.

## Het digitale certificaat downloaden en installeren {#topic-fed3b44e472c4e4ca6dd5852af14cdb9}

Nadat u de Insight-programmabestanden hebt geïnstalleerd, moet u het digitale certificaat downloaden en installeren dat u van Adobe hebt ontvangen.

## Digitale certificaten {#concept-9eed01c8d95440cda6ce29d68e65098c}

Adobe gebruikt X.509 digitale certificaten om de cliënt en servercomponenten te identificeren en voor authentiek te verklaren die omhoog een implementatie maken.

<!--
c_undst_dgtl_crtf.xml
-->

Wanneer u Insight installeert, moet u het digitale certificaat installeren dat een benoemde persoon (bijvoorbeeld Jane Smith) toestaat de geïnstalleerde clienttoepassing te gebruiken.

>[!NOTE]
>
>Als u Inzicht naar een andere computer of een andere genoemde gebruiker moet migreren, moet u een nieuw certificaat van Adobe verkrijgen. Neem hiervoor contact op met de klantenservice van Adobe.

Insight geeft dit digitale certificaat weer om toegang te krijgen tot een servercomponent. Een beheerder van een servercomponent kan toegang tot servermiddelen beperken die op de gemeenschappelijke naam of organisatorische eenheidwaarden worden gebaseerd die in het certificaat van de gebruiker verschijnen.

De X.509 digitale certificaten die met Adobe toepassingen worden geïnstalleerd laten ook zijn cliënt en servercomponenten toe om informatie over de Veilige Laag van Contactdozen (SSL) uit te wisselen. SSL beveiligt transmissies over HTTP gebruikend een publiek-en-privé zeer belangrijk encryptiesysteem. Adobe&#39;s implementatie van SSL ondersteunt 1024-bits RSA-sleutels en gebruikt een 128-bits RC4-versleutelingsalgoritme.

Naast beveiliging werkt het digitale certificaat dat u installeert ook als licentiecode waarmee u Insight kunt uitvoeren. Een digitaal certificaat kan alleen correct functioneren als het is vergrendeld en actueel is, of als de toepassing wordt gestart.

## Door knooppunten vergrendelde certificaten {#section-984aa8f2f5a1448cadc4afea978aedc9}

Een door knooppunten vergrendeld certificaat is een digitaal certificaat dat is geregistreerd op de computer waarop het is geïnstalleerd. Knooppuntvergrendeling koppelt een certificaat permanent aan een specifieke knooppunt-id (een waarde die een bepaalde computer uniek identificeert). Als u het certificaat wilt vergrendelen op een knooppunt, moet uw computer toegang hebben tot internet van de Adobe-licentieserver of een proxyserver die toegang heeft tot de licentieserver.

Als u een computer installeert die geen toegang heeft tot internet, moet u een speciaal vooraf vergrendeld certificaat verkrijgen en installeren, zoals beschreven in [Digitale certificaten gebruiken op computers zonder internettoegang](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#section-d3c060131d7f45cda27f68848b704fa1).

Als u op een computer installeert die tot Internet kan toegang hebben, zal uw digitaal certificaat knoop-gesloten automatisch zijn de eerste keer dat u Insight begint. Nadat het knooppunt-vergrendeld is, kan het certificaat niet op een andere computer worden gebruikt. Als u Inzicht naar een andere computer moet migreren, moet u een nieuw, niet-vergrendeld certificaat verkrijgen van Adobe.

## Huidige certificaten {#section-0816b031df3e415ab3f0205b720c723e}

Uw digitale certificaat moet niet alleen zijn vergrendeld door knooppunten, maar ook actueel zijn. Uw certificaat moet regelmatig opnieuw worden gevalideerd (gewoonlijk om de 30 dagen, maar kan afhankelijk van uw toestemming met Adobe variëren) om actueel te blijven. Als uw computer toegang tot internet heeft, is het proces voor opnieuw valideren volledig transparant. Het inzicht verbindt automatisch met de Server van de Vergunning en bevestigt het certificaat wanneer noodzakelijk. Als uw computer geen internettoegang heeft, moet u handmatig een bijgewerkt certificaat installeren, zoals beschreven in de volgende sectie.

## Digitale certificaten gebruiken op computers zonder internettoegang {#section-d3c060131d7f45cda27f68848b704fa1}

Als u op een computer installeert die tot Internet niet kan toegang hebben, moet u een vooraf gesloten certificaat voor uw installatie van Insight vragen. Een vooraf vergrendeld certificaat is een digitaal certificaat dat Adobe handmatig vergrendelt op de knooppuntidentificatie voor de computer.

Als u een vooraf vergrendeld certificaat wilt aanvragen, moet u de knooppuntidentificatie en uw certificaatnummer naar de klantenservice van Adobe sturen. Om de knoopherkenningsteken voor uw computer te verkrijgen, contacteer de Zorg van de Klant van Adobe om de Adobe te verzoeken [!DNL Node Identifier] nut. U kunt de knoopherkenningsteken van het alarm ook verkrijgen dat de kwesties van het Inzicht wanneer het probeert om met de Server van de Vergunning te verbinden en niet kan. Wanneer u het vooraf vergrendelde certificaat ontvangt, installeert u dit zoals beschreven in de laatste twee stappen van [Digitale certificaten installeren](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#task-1dad1e1d86d04100a7bcf87f26303c38).

Wanneer het certificaat opnieuw moet worden gevalideerd, moet u een nieuw, gevalideerd certificaat downloaden van de licentieserver en dit opnieuw op uw computer installeren (tenzij u akkoord gaat met Adobe, anders).

## Digitale certificaten installeren {#task-1dad1e1d86d04100a7bcf87f26303c38}

<!--
t_install_dgtl_crtf.xml
-->

**Het digitale certificaat downloaden en installeren**

1. Webbrowser openen voor [!DNL https:\\license.visualsciences.com].

   >[!NOTE]
   >
   >Mogelijk wordt u in uw browser gevraagd om nu een digitaal certificaat voor te leggen. Als dit het geval is, klikt u op **[!UICONTROL Cancel]** om het dialoogvenster te sluiten.

1. Voer in het aanmeldingsscherm de [!DNL Account Name] en de [!DNL Password] die u van Adobe hebt ontvangen, klikt u vervolgens op **[!UICONTROL login]**.
1. Zoek het certificaat dat is uitgegeven voor uw Insight-instantie ( *Uw naam*.pem) en klik op ![](assets/btn_save_certificatedownload.PNG) pictogram dat aan dat certificaat is gekoppeld.
1. Klik wanneer u wordt gevraagd het certificaat op te slaan op **[!UICONTROL Save]**.
1. Download het bestand naar de [!DNL Certificates] map in de map waarin u Insight hebt geïnstalleerd.

   Deze map bevat een certificaatbestand met de naam [!DNL trust_ca_cert.pem]. Beide certificaatbestanden moeten altijd aanwezig zijn om Insight te kunnen gebruiken.

## Windows-certificaatarchief {#concept-4acb13b7de9340ea8cde8ad84b93358d}

Met het Windows-certificaatarchief kunt u het certificaat en de persoonlijke sleutel van de client opslaan in het Windows-certificaatarchief voor SSL-communicatie met servers.

<!--
crypto-api.xml
-->

Het Windows-certificaatarchief voor de client is een nieuwe functie waarmee u het SSL-communicatiecertificaat en de persoonlijke sleutel kunt opslaan in het Windows-certificaatarchief in plaats van in `Insight/Certificates/<CertName>.pem` bestand. Het gebruik van het Windows-certificaatarchief heeft de voorkeur als u het certificaatarchief voor andere toepassingen gebruikt en het certificaatbeheer op één plaats wilt uitvoeren, of als u wilt genieten van het aanvullende Windows-auditlogboek dat door het Windows-certificaatarchief wordt geleverd.

>[!NOTE]
>
>Licentie met de licentieserver blijft behouden met behulp van de bestaande `<Common Name>.pem` en dat het certificaat dat is verkregen uit het certificaatarchief alleen wordt gebruikt voor communicatie met de servers die u opgeeft.

## Vereisten {#section-69b18600052145ff8e5299b7123e69c5}

1. U moet toegang hebben tot de [!DNL certmgr.msc] bestand met de mogelijkheid om een certificaat en sleutel te importeren in de **Persoonlijk** opslaan. (Dit zou voor de meeste gebruikers van Vensters moeten waar zijn.)

1. De gebruiker die de configuratie doet moet een exemplaar van hebben **OpenSSL** opdrachtregelprogramma.
1. De server en de client moeten al zijn geconfigureerd voor het gebruik van een aangepast SSL-certificaat. Hiermee krijgt u instructies om het clientcertificaat op te slaan in het Windows-certificaatarchief in plaats van het op te slaan in het **Certificaten** directory.

## Het Windows-certificaatarchief configureren {#section-3629802122e947d4b4f63e8b732cfe27}

Het Windows-certificaatarchief voor clients wordt als volgt ingeschakeld:

**Stap 1: Importeer het SSL-certificaat en de persoonlijke sleutel van de gebruiker naar het Windows-certificaatarchief.**

In [Aangepaste certificaten gebruiken in Data Workbench](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd) u wordt opgedragen het SSL-certificaat en de sleutel in de volgende map te plaatsen:

```
<
<filepath>
  DWB Install folder
</filepath>>\Certificates\
```

De naam van het certificaat is `<Common Name>.pem` zoals Analytics Server 1.pem (niet het bestand trust_ca_cert.pem).

Voordat het certificaat en de persoonlijke sleutel kunnen worden geïmporteerd, moeten ze zijn omgezet van . [!DNL pem] opmaken naar een [!DNL .pfx] opmaak, zoals [!DNL pkcs12.pfx] ).

1. Open een opdrachtprompt of terminal en navigeer naar de map:

   ```
   <CommonName>.pem c: cd \<filepath>DWB Install folder</filepath>>\Certificates
   ```

1. Uitvoeren [!DNL openssl] met de volgende argumenten (met de daadwerkelijke [!DNL .pem] bestandsnaam):

   ```
   openssl pkcs12 -in "<Common Name>.pem" -export -out "<Common Name>.pfx"
   ```

   Druk op **Enter** om het invoeren van een exportwachtwoord over te slaan.

1. Uitvoeren [!DNL certmgr.msc] van de looppasherinnering, beginmenu, of bevellijn.
1. Open de **Persoonlijk** certificaatarchief voor de huidige gebruiker.

   ![](assets/6_5_crypto_api_0.png)

1. Klikken met rechtermuisknop **Certificaten** en klik op **Alle taken** > **Importeren**.

   Zorg ervoor dat de **Huidige gebruiker** is geselecteerd en klikt u vervolgens op **Volgende**.

   ![](assets/6_5_crypto_api_4.png)

1. Klikken **Bladeren** en selecteert u de `<CommonName>.pfx` bestand dat u eerder hebt gemaakt. U moet de vervolgkeuzelijst voor bestandsextensies wijzigen van een X.509-certificaat in een van de volgende **Uitwisseling van persoonlijke gegevens** of aan **Alle bestanden** om het te zien.

   Selecteer het bestand en klik op **Openen** en vervolgens **Volgende**.

1. Voer geen wachtwoord in en controleer of alleen de opties **Deze sleutel als exporteerbaar markeren** en **Alle uitgebreide eigenschappen opnemen** zijn geselecteerd.

   ![](assets/6_5_crypto_api_3.png)

   Klikken **Volgende**.

1. Controleer of **Alle certificaten in de volgende winkel plaatsen** is geselecteerd en dat het vermelde certificaatarchief is **Persoonlijk**. (Als u een gevorderde gebruiker bent, kunt u een andere opslag op dit punt selecteren, maar u zult de configuratie later moeten veranderen.)

1. Klikken **Volgende** en klik vervolgens op **Voltooien**. Er wordt een dialoogvenster weergegeven waarin u wordt aangegeven dat het importeren is gelukt. Uw certificaat wordt weergegeven in de map Certificates in de winkel.

   >[!NOTE]
   >
   >Let met name op de **Uitgegeven aan** en **Uitgegeven door** velden. U zult deze in de volgende stap nodig hebben.

**Stap 2: Bewerk het bestand Insight.cfg.**

De [!DNL Insight.cfg] bestand moet worden bewerkt om Data Workbench de Windows-certificaatopslagfunctie te laten gebruiken. Voor elk serveritem in dit bestand moeten aanvullende parameters worden opgegeven. Als de parameters worden weggelaten, zal het werkstation aan het gebruiken van de bestaande certificaatconfiguratie in gebreke blijven. Als de parameters worden gespecificeerd maar onjuiste waarden hebben, zal het werkstation een foutenstaat ingaan en u zult naar het logboekdossier voor fouteninformatie moeten verwijzen.

1. Open de **Insight.cfg** bestand (in het dialoogvenster **Inzicht** installatiemap).

1. De rol neer aan de serveringang die u wenst te vormen. Als u het Windows-certificaatarchief voor elke server wilt gebruiken, moet u deze wijzigingen aanbrengen in elke vermelding in de vector van [!DNL serverInfo] objecten.
1. Deze parameters toevoegen aan hun [!DNL Insight.cfg] bestand. U kunt dit vanuit het werkstation doen of handmatig door de volgende parameters toe te voegen aan de [!DNL serverInfo] object. (Gebruik spaties in plaats van tabtekens en maak geen andere typografische of syntaxisfouten in dit bestand. )

   ```
   SSL Use CryptoAPI = bool: true
   SSL CryptoAPI Cert Name = string: <Common Name>
   SSL CryptoAPI Cert Issuer Name = string: Visual Sciences,LLC
   SSL CryptoAPI Cert Store Name = string: My
   ```

   De Booleaanse waarde schakelt de functie in of uit. De certificaatnaam komt overeen met **Uitgever aan** in de certificaatbeheerder. De naam van de certificaatuitgever komt overeen **Uitgegeven door** en de **Winkelnaam** moet overeenkomen met de opslagnaam van het certificaat.

   >[!NOTE]
   >
   >De naam &quot;Persoonlijk&quot;in de Manager van het Certificaat (certmgr.msc) verwijst eigenlijk naar het certificaatopslag genoemd **Mijn.** Daarom als u uw SSL-communicatiecertificaat en -sleutel (.PFX) in de **Persoonlijk** certificaatarchief als aanbevolen instellen **SSL CryptoAPI Cert Store Name** tekenreeks naar &quot;Mijn&quot;. Het instellen van deze parameter op &#39;Persoonlijk&#39; werkt niet. Dit is een eigenaardigheid van het Windows-certificaatarchief.

   Een volledige lijst van de vooraf bepaalde systeemopslag kan hier worden verkregen: [https://msdn.microsoft.com/en-us/library/windows/desktop/aa388136(v=vs.85).aspx](https://msdn.microsoft.com/en-us/library/windows/desktop/aa388136%28v=vs.85%29.aspx). Mogelijk bevat uw systeem extra certificaatopslagruimten. Als u een andere opslagplaats dan &quot;Persoonlijk&quot; wilt gebruiken (zoals **Mijn**), moet u de canonieke naam van het certificaatarchief opvragen en deze in het [!DNL Insight.cfg] bestand. (De naam van de systeemopslag &quot;Mijn&quot;wordt inconsistent bedoeld als &quot;Mijn&quot;en &quot;MIJN&quot;door de documentatie van Vensters. De parameter lijkt niet hoofdlettergevoelig te zijn.)

1. Nadat u deze parameters hebt toegevoegd en hebt gecontroleerd dat de waarden overeenkomen met de lijst in Windows Certificate Manager, slaat u de [!DNL Insight.cfg] bestand.

U kunt het werkstation nu starten (of de verbinding met de server verbreken of opnieuw tot stand brengen). Data Workbench moet uw certificaat en sleutel laden uit het certificaatarchief en normaal verbinding maken.

## Logboekuitvoer {#section-a7ef8c9e90ef4bbabaa3cd51a2aca3ab}

Wanneer een certificaat niet wordt gevonden of ongeldig is, wordt dit foutbericht gegenereerd voor de [!DNL HTTP.log] bestand.

```
ERROR Fatal error: the cert could not be found!
```

>[!NOTE]
>
>Het L4 registrerenkader kan worden toegelaten door opstelling [!DNL L4.cfg] bestand (raadpleeg uw accountmanager om dit in te stellen).

## Aangepaste certificaten gebruiken in Data Workbench {#concept-ee6a9b5015f84a0ba64a11428b0a72dd}

Instructies voor het gebruik van aangepaste certificaten.

<!--
using-custom-certificates-DWB.xml
-->

Een certificaat dat door de client of server van de Data Workbench wordt gebruikt, moet door een vertrouwde certificeringsinstantie (Certificate Authority) worden ondertekend. Klanten van Data Workbench ontvangen certificaten die door de Visual Sciences CA zijn ondertekend. Deze certificaten worden vertrouwd door de software van de Data Workbench, aangezien [!DNL trust_ca_cert.pem] (wordt samen met de Insight-software geleverd en in het **Certificaten** map van zowel servers als clients) bevat een *Root CA-certificaat* voor de Visual Sciences CA. Deze certificaten worden gebruikt voor zowel licenties voor de software als verificatie wanneer clients en servers met elkaar communiceren via SSL. Alleen door de Visual Sciences CA uitgegeven certificaten kunnen worden gebruikt voor licenties, maar andere certificaten kunnen worden gebruikt voor communicatie en verificatie. Door andere CA&#39;s dan Visual Sciences uitgegeven certificaten worden hieronder aangeduid als *aangepaste certificaten.*

**Belangrijke opmerking:** Voor servers en clients gebruikt de software van de Data Workbench de certificaatbestanden die zijn geïnstalleerd op de client of server **Certificaten** map of certificaten die expliciet in de configuratie ervan worden geïdentificeerd. U kunt echter ook het Windows-certificaatarchief voor clients gebruiken.

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
   1. Het certificaat is afgegeven met een *doel **** van *client* (of beide *server* **en** *client*).

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

1. Voeg met een teksteditor de volgende regel toe aan **Communications.cfg** in beide *Componenten* en *Componenten voor het verwerken van servers* directory&#39;s, direct onder de eerste regel ( [!DNL component = CommServer]):

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

## String Encryption {#concept-35da0b53650a4d7e82b240ad27f6d45a}

Codeer wachtwoorden en andere koorden wanneer het communiceren tussen de cliënt en de server.

<!--
string_encryption.xml
-->

Wanneer het communiceren tussen de cliënt van de Data Workbench (werkstation) en de server, kunt u een parameter van de Waarde (zoals een wachtwoord) met het Type van opslaan *EncryptedString*. Hierdoor wordt de parameter verborgen en wordt de tekenreeks opgeslagen in de *Windows Credential Store* op de server met de corresponderende geretourneerde sleutel. Dit slaat hoofdzakelijk geloofsbrieven op die in uitvoer worden gebruikt maar kan worden gebruikt om het even welke parameter te coderen.

* Een nieuwe map is toegevoegd op de server\**EncryptStrings**.

   Hier stelt u het configuratiebestand zo in dat tekenreeksen worden gecodeerd.

* Een nieuw configuratiebestand is toegevoegd op de server\Component\**EncryptedStrings.cfg**.

   ```
   component = EncryptionComponent:
     Path = Path: EncryptStrings\\*.cfg
   ```

   Dit bestand pollt de *Server*\*EncryptStrings* omslag voor de dossiers van de encryptieconfiguratie.

**Een tekenreeks coderen**:

1. Een **EncryptedStrings.cfg** configuratiebestand voor een tekenreeks met deze velden ingesteld:

   ```
   Names = vector: 1 items
    0 = NameEncryptValuePair:
     EncryptValue = EncryptedString: // left empty as input then output will be filled by server
     Name = string: // Name for identifier
     Value = string: // Value to be encrypted
   ```

   * *Waarde* - Dit veld bevat de tekenreeks zonder opmaak die moet worden gecodeerd.

      Dit is alleen servercodering. De *Waarde* instelling wordt alleen op de servercomputer gecodeerd.

   * *Naam* - Dit veld bevat een waarde die de gecodeerde tekenreeks identificeert.
   * *EncryptValue* - Dit veld blijft leeg in het invoerconfiguratiebestand. De gecodeerde waarde wordt in dit veld geretourneerd.

   U kunt meerdere **NameEncryptValuePair** waarden voor verschillende velden voor versleuteling.

   >[!NOTE]
   >
   >Alle lege waardevelden worden verwijderd.

1. Sla de **EncryptedStrings.cfg** bestand naar de server\**EncryptStrings** map.

**Uitvoerbestand**

Er wordt een uitvoerbestand gegenereerd met dezelfde naam als het invoerbestand met een &lt;*filename*>.*gecodeerd* extensie. Als het invoerbestand bijvoorbeeld een naam heeft *sample.cfg* dan krijgt het uitvoerbestand een naam *sample.cfg.encrypted*.

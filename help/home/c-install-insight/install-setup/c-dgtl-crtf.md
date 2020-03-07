---
description: Nadat u de het programmadossiers van het Inzicht hebt geïnstalleerd, moet u het digitale certificaat downloaden en installeren dat aan u door Adobe wordt verstrekt.
title: Het downloaden en installeren van het Digitale Certificaat
uuid: 93ab2222-a977-4279-9e1e-71038b1d1cfa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het downloaden en installeren van het Digitale Certificaat{#downloading-and-installing-the-digital-certificate}

Nadat u de het programmadossiers van het Inzicht hebt geïnstalleerd, moet u het digitale certificaat downloaden en installeren dat aan u door Adobe wordt verstrekt.

## Het downloaden en installeren van het Digitale Certificaat {#topic-fed3b44e472c4e4ca6dd5852af14cdb9}

Nadat u de het programmadossiers van het Inzicht hebt geïnstalleerd, moet u het digitale certificaat downloaden en installeren dat aan u door Adobe wordt verstrekt.

## Het begrip van Digitale Certificaten {#concept-9eed01c8d95440cda6ce29d68e65098c}

Adobe gebruikt X.509 digitale certificaten om de cliënt en servercomponenten te identificeren en voor authentiek te verklaren die omhoog een implementatie maken.

<!--
c_undst_dgtl_crtf.xml
-->

Wanneer u Inzicht installeert, moet u het digitale certificaat installeren dat een genoemd individu (bijvoorbeeld, Jane Smith) machtigt om de geïnstalleerde cliënttoepassing te gebruiken.

>[!NOTE]
>
>Als u Inzicht aan een andere computer of een andere genoemde gebruiker moet migreren, moet u een nieuw certificaat van Adobe verkrijgen. Om dit te doen, contacteer de Zorg van de Klant van Adobe.

Het inzicht stelt dit digitale certificaat voor om tot een servercomponent toegang te krijgen. Een beheerder van een servercomponent kan toegang tot servermiddelen beperken die op de gemeenschappelijke naam of organisatorische eenheidswaarden worden gebaseerd die in het certificaat van de gebruiker verschijnen.

De X.509 digitale certificaten die met de toepassingen van Adobe worden geïnstalleerd laten ook zijn cliënt en servercomponenten toe om informatie over de Veilige Laag van Contactdozen te ruilen (SSL). SSL beveiligt transmissies over HTTP gebruikend een openbaar-en-privé zeer belangrijk encryptiesysteem. De implementatie van Adobe van SSL steunt 1024 beetjeRSA sleutels en gebruikt een 128 beetjeRC4 encryptiealgoritme.

Naast veiligheid, functioneert het digitale certificaat dat u installeert ook als vergunningssleutel die u toelaat om Inzicht in werking te stellen. Om behoorlijk te functioneren, moet een digitaal certificaat knoop-gesloten en huidig zijn, of de toepassing zal niet beginnen.

## Certificaten zonder noden {#section-984aa8f2f5a1448cadc4afea978aedc9}

Een knoop-gesloten certificaat is een digitaal certificaat dat aan de computer is geregistreerd waarop het geïnstalleerd is. Het sluiten van de knoop associeert permanent een certificaat met een specifiek knoopherkenningsteken (een waarde die uniek een bepaalde computer identificeert). Om knoop te sluiten moet uw certificaat, uw computer de toegang van Internet tot de Server van de Vergunning van Adobe of aan een volmachtsserver hebben die toegang tot de Server van de Vergunning heeft.

Als u op een computer installeert die tot Internet niet kan toegang hebben, moet u een speciaal vooraf gesloten certificaat verkrijgen en installeren zoals die in het [Gebruiken van Digitale Certificaten op Computers zonder de Toegang](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#section-d3c060131d7f45cda27f68848b704fa1)van Internet wordt beschreven.

Als u op een computer installeert die tot Internet kan toegang hebben, zal uw digitaal certificaat automatisch knoop-gesloten zijn de eerste keer dat u Inzicht begint. Na het zijn knoop-gesloten, kan het certificaat niet op een andere computer worden gebruikt. Als u Inzicht aan een andere computer moet migreren, moet u een nieuw, ontgrendeld certificaat van Adobe verkrijgen.

## Huidige certificaten {#section-0816b031df3e415ab3f0205b720c723e}

Naast het zijn knoop-gesloten, moet uw digitaal certificaat huidig zijn. Om huidig te blijven, moet uw certificaat op een regelmatige basis (over het algemeen om de 30 dagen opnieuw worden bevestigd, maar kan afhankelijk van uw overeenkomst met Adobe variëren). Als uw computer de toegang van Internet heeft, is het herbevestigingsproces volledig transparant. Het inzicht verbindt automatisch met de Server van de Vergunning en bevestigt het certificaat wanneer nodig opnieuw. Als uw computer geen toegang tot Internet heeft, moet u een bijgewerkt certificaat manueel installeren zoals die in de volgende sectie wordt beschreven.

## Het gebruiken van Digitale Certificaten op Computers zonder de Toegang van Internet {#section-d3c060131d7f45cda27f68848b704fa1}

Als u op een computer installeert die tot Internet niet kan toegang hebben, moet u een vooraf gesloten certificaat voor uw installatie van Inzicht aanvragen. Een pre-gesloten certificaat is een digitaal certificaat dat Adobe manueel aan het knoopherkenningsteken voor de computer sluit.

Om een vooraf gesloten certificaat aan te vragen, moet u het knoopherkenningsteken en uw certificaataantal naar de Zorg van de Klant van Adobe verzenden. Om het knoopherkenningsteken voor uw computer te verkrijgen, contacteer de Zorg van de Klant van Adobe om het [!DNL Node Identifier] nut van Adobe te verzoeken. U kunt ook het knoopherkenningsteken uit het alarm verkrijgen dat de kwesties van het Inzicht wanneer het probeert om met de Server van de Vergunning te verbinden en niet kan. Wanneer u het vooraf vergrendelde certificaat ontvangt, installeert u het zoals beschreven in de laatste twee stappen van de [installatie van digitale certificaten](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#task-1dad1e1d86d04100a7bcf87f26303c38).

Wanneer het certificaat opnieuw moet worden bevestigd, moet u een nieuw, bevestigd certificaat van de Server van de Vergunning downloaden en het opnieuw installeren op uw computer (tenzij uw overeenkomst met Adobe anders verklaart).

## Digitale certificaten installeren {#task-1dad1e1d86d04100a7bcf87f26303c38}

<!--
t_install_dgtl_crtf.xml
-->

**Om het digitale certificaat te downloaden en te installeren**

1. Open uw Webbrowser aan [!DNL http:\\license.visualsciences.com].

   >[!NOTE]
   >
   >Uw browser zou u kunnen ertoe aanzetten om een digitaal certificaat op dit punt voor te stellen. Als het, klik **[!UICONTROL Cancel]** om de dialoogdoos te verwerpen.

1. Voor het login scherm, ga de [!DNL Account Name] en [!DNL Password] die u van Adobe ontving in, dan klik **[!UICONTROL login]**.
1. Bepaal de plaats van het certificaat dat voor uw geval van Inzicht ( *Uw Naam*.pem) is uitgegeven en klik het ![](assets/btn_save_certificatedownload.PNG) pictogram verbonden aan dat certificaat.
1. Wanneer ertoe aangezet om het certificaat te bewaren, klik **[!UICONTROL Save]**.
1. Download het dossier aan de [!DNL Certificates] omslag in de folder waar u Inzicht installeerde.

   Deze omslag bevat een certificaatdossier genoemd [!DNL trust_ca_cert.pem]. Beide certificaatdossiers moeten altijd aanwezig zijn voor Inzicht om te functioneren.

## Windows Certificate Store {#concept-4acb13b7de9340ea8cde8ad84b93358d}

De Opslag van het Certificaat van Vensters staat u toe om het certificaat van de cliënt en de privé sleutel in de Opslag van het Certificaat van Vensters voor SSL mededeling met servers op te slaan.

<!--
crypto-api.xml
-->

De opslag van het Certificaat van Vensters voor de Cliënt is een nieuwe eigenschap die u toestaat om het SSL communicatie certificaat en de privé sleutel in de Opslag van het Certificaat van Vensters eerder dan in `Insight/Certificates/<CertName>.pem` dossier op te slaan. Het gebruik van de Windows Certificate Store kan de voorkeur genieten als u de certificaatopslag voor andere toepassingen gebruikt en het certificaatbeheer op één plaats wenst te doen, of als u wilt genieten van de extra Windows-controlelogboeken die de Windows-certificaatopslag biedt.

>[!NOTE]
>
>Het verlenen van vergunningen met de vergunningsserver wordt nog gehandhaafd gebruikend het bestaande `<Common Name>.pem` dossier, en dat het certificaat dat van de certificaatopslag wordt verkregen slechts voor mededeling aan de servers zal worden gebruikt die u specificeert.

## Voorwaarden {#section-69b18600052145ff8e5299b7123e69c5}

1. U moet toegang tot het [!DNL certmgr.msc] dossier met de capaciteit hebben om een certificaat en een sleutel in de **Persoonlijke** opslag in te voeren. (Dit zou door gebrek voor de meeste gebruikers van Vensters waar moeten zijn.)

1. De gebruiker die de configuratie doet moet een exemplaar van het bevel-lijn **OpenSSL** hulpmiddel hebben.
1. De server en de cliënt moeten reeds worden gevormd om een douaneSSL certificaat te gebruiken, dat instructies geeft om het cliëntcertificaat in de het certificaatopslag van Vensters eerder dan het opslaan van het in de folder van **Certificaten** op te slaan.

## De Windows Certificate Store configureren {#section-3629802122e947d4b4f63e8b732cfe27}

De opslag van het Certificaat van Vensters voor Cliënten wordt toegelaten na deze stappen:

**Stap 1: Voer het SSL van de gebruiker certificaat en de privé sleutel in de Opslag van het Certificaat van Vensters in.**

In het [Gebruiken van de Certificaten van de Douane in de Werkbank](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd) van Gegevens wordt u geleid om het SSL certificaat en de sleutel in de volgende folder te zetten:

```
< 
<filepath>
  DWB Install folder 
</filepath>>\Certificates\
```

De naam van het certificaat is `<Common Name>.pem` zoals Server 1.pem van de Analyse (niet het trust_ca_cert.pem- dossier.)

Alvorens het certificaat en de privé sleutel kunnen worden ingevoerd, moeten zij van worden omgezet. [!DNL pem] formatteren in een [!DNL .pfx] formaat, zoals [!DNL pkcs12.pfx] ).

1. Open een bevelherinnering of terminal en navigeer aan de folder:

   ```
   <CommonName>.pem c: cd \<filepath>DWB Install folder</filepath>>\Certificates
   ```

1. Looppas [!DNL openssl] met de volgende argumenten (met het daadwerkelijke [!DNL .pem] dossier - noem):

   ```
   openssl pkcs12 -in "<Common Name>.pem" -export -out "<Common Name>.pfx"
   ```

   Indien ertoe aangezet, **ga binnen** om het ingaan van een de uitvoerwachtwoord over te slaan.

1. Looppas [!DNL certmgr.msc] van de looppasherinnering, beginmenu, of bevellijn.
1. Open de **Persoonlijke** certificaatopslag voor de huidige gebruiker.

   ![](assets/6_5_crypto_api_0.png)

1. Klik **Certificaten** met de rechtermuisknop aan en klik **Alle Taken** > de **Invoer**.

   Zorg ervoor de **Huidige optie van de Gebruiker** wordt geselecteerd, dan klik **daarna**.

   ![](assets/6_5_crypto_api_4.png)

1. Klik **doorbladeren** en selecteren het `<CommonName>.pfx` dossier u eerder creeerde. U zult de dropdown doos van de dossieruitbreiding van een X.509- Certificaat in of de **Persoonlijke Uitwisseling** van de Informatie of in **Alle Dossiers** moeten veranderen om het te zien.

   Selecteer het dossier en klik **Open**, en dan **daarna**.

1. Ga geen wachtwoord in, en zorg ervoor dat slechts de opties deze sleutel **markeren als exporteerbaar** en alle uitgebreide eigenschappen **** omvatten worden geselecteerd.

   ![](assets/6_5_crypto_api_3.png)

   Klik op **Volgende**.

1. Zorg ervoor dat **Plaats alle certificaten in de volgende opslag** wordt geselecteerd, en dat de vermelde certificaatopslag **Persoonlijk** is. (Als u een geavanceerde gebruiker bent, kunt u een andere opslag op dit punt selecteren, maar u zult de configuratie later moeten veranderen.)

1. Klik **daarna** en klik dan **Afwerking**. U zou een dialoogdoos moeten zien vertellend u dat de invoer succesvol was en uw certificaat in de omslag van Certificaten van de opslag zien.

   >[!NOTE]
   >
   >In het bijzonder aandacht besteden aan de **uitgifte aan** en **uitgifte door** velden. Je hebt deze nodig in de volgende stap.

**Stap 2: Geef het dossier Insight.cfg uit.**

Het [!DNL Insight.cfg] dossier moet worden uitgegeven om de Werkbank van Gegevens te leiden om de eigenschap van de Opslag van het Certificaat van Vensters te gebruiken. Elke serveringang in dit dossier moet sommige extra gespecificeerde parameters hebben. Als de parameters worden weggelaten, zal het werkstation aan het gebruiken van de bestaande certificaatconfiguratie in gebreke blijven. Als de parameters worden gespecificeerd maar onjuiste waarden hebben, zal het werkstation een foutenstaat ingaan en u zult naar het logboekdossier voor fouteninformatie moeten verwijzen.

1. Open het **Insight.cfg** - dossier (dat in de de installatiefolder van het **Inzicht** wordt gevestigd).

1. Rol neer aan de serveringang die u wenst om te vormen. Als u wenst om de opslag van het Certificaat van Vensters voor elke server te gebruiken, moet u deze wijzigingen aan elke ingang in de vector van [!DNL serverInfo] voorwerpen maken.
1. Voeg deze parameters aan hun [!DNL Insight.cfg] dossier toe. U kunt dit van het werkstation doen, of manueel door de volgende parameters aan het [!DNL serverInfo] voorwerp toe te voegen. (Ben zeker om ruimten in plaats van lusjekarakters te gebruiken, en maak geen andere typografische of syntaxisfouten in dit dossier. )

   ```
   SSL Use CryptoAPI = bool: true  
   SSL CryptoAPI Cert Name = string: <Common Name>  
   SSL CryptoAPI Cert Issuer Name = string: Visual Sciences,LLC  
   SSL CryptoAPI Cert Store Name = string: My 
   ```

   Boolean schakelt de functie in of uit. De certificaatnaam past **Uitgever aan** in de certificaatmanager aan. De naam van de certificaatuitgever past **door**, en de Naam **van de** Opslag moet de naam van de certificaatopslag aanpassen.

   >[!NOTE]
   >
   >De naam &quot;Persoonlijk&quot;in de Manager van het Certificaat (certmgr.msc) verwijst eigenlijk naar de certificaatopslag genoemd **Mijn.** Derhalve als u uw SSL communicatie certificaat en sleutel (.PFX) in de **Persoonlijke** certificaatopslag zoals geadviseerd invoert, moet u het koord van de Naam **van de Opslag van de** SSL CryptoAPI Cert aan &quot;Mijn&quot;plaatsen. Het plaatsen van deze parameter aan &quot;Persoonlijk&quot;zal niet werken. Dit is een eigenaardigheid van de het certificaatopslag van Vensters.

   Een volledige lijst van de vooraf bepaalde systeemopslag kan hier worden verkregen: [https://msdn.microsoft.com/en-us/library/windows/desktop/aa388136(v=vs.85).aspx](https://msdn.microsoft.com/en-us/library/windows/desktop/aa388136%28v=vs.85%29.aspx). Het is mogelijk dat uw systeem extra certificaatopslag heeft. Als u wenst om een opslag buiten &quot;Persoonlijk&quot;te gebruiken (zoals **Mijn**), moet u de canonische naam van de certificaatopslag verkrijgen en het verstrekken in het [!DNL Insight.cfg] dossier. (De naam van de systeemopslag &quot;Mijn&quot;wordt inconsequent bedoeld als &quot;Mijn&quot;en &quot;MIJN&quot;door de documentatie van Vensters. De parameter lijkt niet hoofdlettergevoelig te zijn.)

1. Nadat u deze parameters hebt toegevoegd en geverifieerd dat de waarden de lijst in de Manager van het Certificaat van Vensters aanpassen, sparen het [!DNL Insight.cfg] dossier.

U kunt het werkstation (of losmaken/opnieuw verbinden met de server) nu beginnen. De Werkbank van gegevens zou uw certificaat en sleutel van de certificaatopslag moeten laden en normaal verbinden.

## Loguitvoer {#section-a7ef8c9e90ef4bbabaa3cd51a2aca3ab}

Wanneer een certificaat niet wordt gevonden of ongeldig is, wordt deze foutenmelding geworpen aan het [!DNL HTTP.log] dossier.

```
ERROR Fatal error: the cert could not be found!
```

>[!NOTE]
>
>Het L4 registrerenkader kan worden toegelaten door opstelling het [!DNL L4.cfg] dossier (zie uw rekeningsmanager aan opstelling dit).

## Het gebruiken van de Certificaten van de Douane in de Werkbank van Gegevens {#concept-ee6a9b5015f84a0ba64a11428b0a72dd}

Instructies voor het gebruiken van douanecertificaten.

<!--
using-custom-certificates-DWB.xml
-->

Een certificaat dat door of de cliënt of de server van de Werkbank van Gegevens wordt gebruikt moet door vertrouwde op CA (de Autoriteit van het Certificaat) worden ondertekend. De klanten van de Werkbank van gegevens ontvangen certificaten die door de Visuele Wetenschappen CA. worden ondertekend. Deze certificaten worden vertrouwd op door de software van de Werkbank van Gegevens, aangezien [!DNL trust_ca_cert.pem] (die samen met de software van het Inzicht wordt verstrekt en in de folder van **Certificaten** van zowel servers als cliënten wordt opgeslagen) een Certificaat *van CA van de* Wortel voor Visual Sciences CA bevat. Deze certificaten worden gebruikt voor zowel het verlenen van vergunningen van de software als authentificatie wanneer de cliënten en de servers met elkaar gebruikend SSL communiceren. Slechts kunnen de certificaten die door Visuele Wetenschappen CA worden uitgegeven voor vergunning worden gebruikt, maar andere certificaten kunnen voor mededeling en authentificatie worden gebruikt. Certificaten die door andere CA&#39;s dan Visual Sciences zijn afgegeven, worden hieronder aangeduid als *douanecertificaten.*

**Belangrijke opmerking:** Voor servers en cliënten, gebruikt de software van de Werkbank van Gegevens de certificaatdossiers die in de cliënt of de folder van de **Certificaten** van de server worden geïnstalleerd of certificaten die uitdrukkelijk in zijn configuratie worden geïdentificeerd. Nochtans, kunt u de Opslag van het Certificaat van Vensters voor cliënten ook gebruiken.

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

1. Gebruikend een tekstredacteur, voeg de volgende lijn aan **Communications.cfg** - dossier in zowel de *Componenten* als *Componenten voor de folders van de Servers* van de Verwerking, direct onder de eerste lijn ( [!DNL component = CommServer]) toe:

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

## String Encryption {#concept-35da0b53650a4d7e82b240ad27f6d45a}

Codeer wachtwoorden en andere koorden wanneer het communiceren tussen de cliënt en de server.

<!--
string_encryption.xml
-->

Wanneer het communiceren tussen de cliënt van de Werkbank van Gegevens (werkstation) en server, kunt u een parameter van de Waarde (zoals een wachtwoord) met het Type van *EncryptedString* bewaren. Dit verbergt de parameter en bewaart het koord aan de Credentiële Opslag *van* Vensters op de server met de overeenkomstige teruggekeerde sleutel. Dit slaat hoofdzakelijk geloofsbrieven op die in uitvoer worden gebruikt maar kan worden gebruikt om het even welke parameter te coderen.

* Een nieuwe omslag werd toegevoegd bij Server \**EncryptStrings**.

   Dit is waar u het configuratiedossier plaatst om koorden te coderen.

* Een nieuw configuratiedossier werd toegevoegd in Server\Component\**EncryptedStrings.cfg**.

   ```
   component = EncryptionComponent: 
     Path = Path: EncryptStrings\\*.cfg
   ```

   Dit dossier opinieert de omslag van de *Server*\*EncryptStrings* voor de dossiers van de encryptieconfiguratie.

**Om een koord** te coderen:

1. Creeer een **EncryptedStrings.cfg** - configuratiedossier voor een koord met deze reeks gebieden:

   ```
   Names = vector: 1 items 
    0 = NameEncryptValuePair: 
     EncryptValue = EncryptedString: // left empty as input then output will be filled by server 
     Name = string: // Name for identifier  
     Value = string: // Value to be encrypted
   ```

   * *Waarde* - Dit gebied bevat het duidelijke tekstkoord dat moet worden gecodeerd.

      Dit is alleen servercodering. De *waarde* die wordt geplaatst wordt gecodeerd slechts op de servercomputer.

   * *Naam* - Dit gebied bevat een waarde die het gecodeerde koord identificeert.
   * *EncryptValue* - Dit gebied zal leeg in het dossier van de inputconfiguratie worden verlaten. De gecodeerde waarde zal op dit gebied zijn teruggekeerd.
   U kunt veelvoudige waarden **NameEncryptValuePair** voor verschillende gebieden voor encryptie toevoegen.

   >[!NOTE]
   >
   >Alle lege gebieden van de Waarde zullen worden verwijderd.

1. Sla het bestand **EncryptedStrings.cfg** op in de map Server\**EncryptStrings**.

**Uitvoerbestand**

Een outputdossier zal met de zelfde naam worden geproduceerd zoals het inputdossier met &lt;*filename*>.*gecodeerde* uitbreiding. Bijvoorbeeld, als het inputdossier *sample.cfg* wordt genoemd dan zal het outputdossier *sample.cfg.encrypted* worden genoemd.

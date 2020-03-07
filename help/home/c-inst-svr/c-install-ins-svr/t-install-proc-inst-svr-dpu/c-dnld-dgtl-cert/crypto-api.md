---
description: De Opslag van het Certificaat van Vensters staat u toe om het certificaat van de cliënt en de privé sleutel in de Opslag van het Certificaat van Vensters voor SSL mededeling met servers op te slaan.
title: Windows Certificate Store
uuid: a8021295-375a-460b-8686-acf3bc43cd17
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Windows Certificate Store{#windows-certificate-store}

De Opslag van het Certificaat van Vensters staat u toe om het certificaat van de cliënt en de privé sleutel in de Opslag van het Certificaat van Vensters voor SSL mededeling met servers op te slaan.

De opslag van het Certificaat van Vensters voor de Cliënt is een nieuwe eigenschap die u toestaat om het SSL communicatie certificaat en de privé sleutel in de Opslag van het Certificaat van Vensters eerder dan in `Insight/Certificates/<CertName>.pem` dossier op te slaan. Het gebruik van de Windows Certificate Store kan de voorkeur genieten als u de certificaatopslag voor andere toepassingen gebruikt en het certificaatbeheer op één plaats wenst te doen, of als u wilt genieten van de extra Windows-controlelogboeken die de Windows-certificaatopslag biedt.

>[!NOTE]
>
>Het verlenen van vergunningen met de vergunningsserver wordt nog gehandhaafd gebruikend het bestaande `<Common Name>.pem` dossier, en dat het certificaat dat van de certificaatopslag wordt verkregen slechts voor mededeling aan de servers zal worden gebruikt die u specificeert.

## Voorwaarden {#section-69b18600052145ff8e5299b7123e69c5}

1. U moet toegang tot het [!DNL certmgr.msc] dossier met de capaciteit hebben om een certificaat en een sleutel in de **Persoonlijke** opslag in te voeren. (Dit zou door gebrek voor de meeste gebruikers van Vensters waar moeten zijn.)

1. De gebruiker die de configuratie doet moet een exemplaar van het bevel-lijn **OpenSSL** hulpmiddel hebben.
1. De server en de cliënt moeten reeds worden gevormd om een douaneSSL certificaat te gebruiken, zoals die in het [Gebruiken van de Certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/using-custom-certificates-dwb.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd)van de Douane wordt beschreven, die instructies geven om het cliëntcertificaat in de het certificaatopslag van Vensters eerder dan het opslaan van het in de folder van **Certificaten** op te slaan.

## De Windows Certificate Store configureren {#section-3629802122e947d4b4f63e8b732cfe27}

De opslag van het Certificaat van Vensters voor Cliënten wordt toegelaten na deze stappen:

**Stap 1: Voer het SSL van de gebruiker certificaat en de privé sleutel in de Opslag van het Certificaat van Vensters in.**

In het [Gebruiken van de Certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/using-custom-certificates-dwb.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd) van de Douane wordt u geleid om het SSL certificaat en de sleutel in de volgende folder te zetten:

```
< 
<filepath>
  DWB Install folder 
</filepath>>\Certificates\
```

De naam van het certificaat is `<Common Name>.pem` (zoals [!DNL Analytics Server 1.pem](niet het [!DNL trust_ca_cert.pem] dossier.)

Alvorens het certificaat en de privé sleutel kunnen worden ingevoerd, moeten zij van worden omgezet. [!DNL pem] formatteren in een [!DNL .pfx] formaat, zoals [!DNL pkcs12.pfx] ).

1. Open een bevelherinnering of terminal en navigeer aan de folder:

   ```
   <CommonName>.pem c: cd \<DWB Install folder \Certificates
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

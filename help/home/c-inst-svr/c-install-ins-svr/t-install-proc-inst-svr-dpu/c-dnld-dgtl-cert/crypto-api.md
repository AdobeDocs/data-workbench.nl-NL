---
description: Met het Windows-certificaatarchief kunt u het certificaat en de persoonlijke sleutel van de client opslaan in het Windows-certificaatarchief voor SSL-communicatie met servers.
title: Windows-certificaatarchief
uuid: a8021295-375a-460b-8686-acf3bc43cd17
translation-type: tm+mt
source-git-commit: a766b64ef809e2223fed869d8d63b75f270a3d39
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---


# Windows-certificaatarchief{#windows-certificate-store}

Met het Windows-certificaatarchief kunt u het certificaat en de persoonlijke sleutel van de client opslaan in het Windows-certificaatarchief voor SSL-communicatie met servers.

Het Windows-certificaatarchief voor de client is een nieuwe functie waarmee u het SSL-communicatiecertificaat en de persoonlijke sleutel kunt opslaan in het Windows-certificaatarchief in plaats van in het `Insight/Certificates/<CertName>.pem` bestand. Het gebruik van het Windows-certificaatarchief heeft de voorkeur als u het certificaatarchief voor andere toepassingen gebruikt en het certificaatbeheer op één plaats wilt uitvoeren, of als u wilt genieten van het aanvullende Windows-auditlogboek dat door het Windows-certificaatarchief wordt geleverd.

>[!NOTE]
>
>Het verlenen van vergunningen met de vergunningsserver wordt nog gehandhaafd gebruikend het bestaande `<Common Name>.pem` dossier, en dat het certificaat dat van het certificaatopslag wordt verkregen slechts voor mededeling aan de servers zal worden gebruikt die u specificeert.

## Vereisten {#section-69b18600052145ff8e5299b7123e69c5}

1. U moet toegang hebben tot het [!DNL certmgr.msc] bestand met de mogelijkheid om een certificaat en sleutel te importeren in de **persoonlijke** opslag. (Dit zou voor de meeste gebruikers van Vensters moeten waar zijn.)

1. De gebruiker die de configuratie uitvoert moet een exemplaar van het bevel-lijn **OpenSSL** hulpmiddel hebben.
1. De server en de client moeten al zijn geconfigureerd voor het gebruik van een aangepast SSL-certificaat, zoals wordt beschreven in Aangepaste certificaten [](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/using-custom-certificates-dwb.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd)gebruiken. Hiermee krijgt u instructies om het clientcertificaat op te slaan in het Windows-certificaatarchief in plaats van het op te slaan in de map **Certificates** .

## Het Windows-certificaatarchief configureren {#section-3629802122e947d4b4f63e8b732cfe27}

Het Windows-certificaatarchief voor clients wordt als volgt ingeschakeld:

**Stap 1: Importeer het SSL-certificaat en de persoonlijke sleutel van de gebruiker naar het Windows-certificaatarchief.**

In het [Gebruiken van Aangepaste Certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/using-custom-certificates-dwb.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd) wordt u geleid om het SSL certificaat en de sleutel in de volgende folder te zetten:

```
< 
<filepath>
  DWB Install folder 
</filepath>>\Certificates\
```

De naam van het certificaat is `<Common Name>.pem` (bijvoorbeeld [!DNL Analytics Server 1.pem] (niet het [!DNL trust_ca_cert.pem] bestand).

Voordat het certificaat en de persoonlijke sleutel kunnen worden geïmporteerd, moeten ze zijn omgezet van . [!DNL pem] een indeling hebben in een [!DNL .pfx] indeling, zoals [!DNL pkcs12.pfx] ).

1. Open een opdrachtprompt of terminal en navigeer naar de map:

   ```
   <CommonName>.pem c: cd \<DWB Install folder \Certificates
   ```

1. Voer [!DNL openssl] de volgende argumenten uit (met de werkelijke [!DNL .pem] bestandsnaam):

   ```
   openssl pkcs12 -in "<Common Name>.pem" -export -out "<Common Name>.pfx"
   ```

   Druk desgevraagd op **Enter** om het invoeren van een exportwachtwoord over te slaan.

1. Voer [!DNL certmgr.msc] vanaf de vraag, het beginmenu of de opdrachtregel uit.
1. Open het **persoonlijke** certificaatarchief voor de huidige gebruiker.

   ![](assets/6_5_crypto_api_0.png)

1. Klik met de rechtermuisknop op **Certificaten** en klik op **Alle taken** > **Importeren**.

   Controleer of de optie **Huidige gebruiker** is geselecteerd en klik op **Volgende**.

   ![](assets/6_5_crypto_api_4.png)

1. Klik op **Bladeren** en selecteer het `<CommonName>.pfx` bestand dat u eerder hebt gemaakt. U zult het drop-down vakje van de dossieruitbreiding van een X.509 Certificaat in of **Persoonlijke Uitwisseling** van Informatie of in **Alle Dossiers** moeten veranderen om het te zien.

   Selecteer het bestand, klik op **Openen** en **Volgende**.

1. Voer geen wachtwoord in en controleer of alleen de opties **Markeren dat deze sleutel exporteerbaar** is en **Inclusief alle uitgebreide eigenschappen** zijn geselecteerd.

   ![](assets/6_5_crypto_api_3.png)

   Klik op **Volgende**.

1. Zorg ervoor dat Alle certificaten **plaatsen in de volgende opslag** wordt geselecteerd, en dat de vermelde certificaatopslag **Persoonlijk** is. (Als u een gevorderde gebruiker bent, kunt u een andere opslag op dit punt selecteren, maar u zult de configuratie later moeten veranderen.)

1. Klik op **Volgende** en vervolgens op **Voltooien**. Er wordt een dialoogvenster weergegeven waarin u wordt aangegeven dat het importeren is gelukt. Uw certificaat wordt weergegeven in de map Certificates in de winkel.

   >[!NOTE]
   >
   >Let vooral op de velden **Uitgegeven aan** en **Uitgegeven door** . U zult deze in de volgende stap nodig hebben.

**Stap 2: Bewerk het bestand Insight.cfg.**

Het [!DNL Insight.cfg] bestand moet worden bewerkt om Data Workbench de Windows-certificaatopslagfunctie te laten gebruiken. Voor elk serveritem in dit bestand moeten aanvullende parameters worden opgegeven. Als de parameters worden weggelaten, zal het werkstation aan het gebruiken van de bestaande certificaatconfiguratie in gebreke blijven. Als de parameters worden gespecificeerd maar onjuiste waarden hebben, zal het werkstation een foutenstaat ingaan en u zult naar het logboekdossier voor fouteninformatie moeten verwijzen.

1. Open het bestand **Insight.cfg** (in de installatiemap van **Insight** ).

1. De rol neer aan de serveringang die u wenst te vormen. Als u het Windows-certificaatarchief voor elke server wilt gebruiken, moet u deze wijzigingen aanbrengen in elke vermelding in de vector met [!DNL serverInfo] objecten.
1. Voeg deze parameters toe aan hun [!DNL Insight.cfg] bestand. U kunt dit vanuit het werkstation doen of handmatig door de volgende parameters aan het [!DNL serverInfo] object toe te voegen. (Gebruik spaties in plaats van tabtekens en maak geen andere typografische of syntaxisfouten in dit bestand. )

   ```
   SSL Use CryptoAPI = bool: true  
   SSL CryptoAPI Cert Name = string: <Common Name>  
   SSL CryptoAPI Cert Issuer Name = string: Visual Sciences,LLC  
   SSL CryptoAPI Cert Store Name = string: My 
   ```

   De Booleaanse waarde schakelt de functie in of uit. De certificaatnaam komt overeen met de naam van de **uitgever naar** in certificaatbeheer. De uitgeversnaam van het certificaat komt overeen met de naam **Uitgegeven door** en de **winkelnaam** moet overeenkomen met de opslagnaam van het certificaat.

   >[!NOTE]
   >
   >De naam &quot;Persoonlijk&quot;in de Manager van het Certificaat (certmgr.msc) verwijst eigenlijk naar de certificaatopslag genoemd **Mijn.** Als u het SSL-communicatiecertificaat en de sleutel (.PFX) naar het **persoonlijke** certificaatarchief importeert zoals aanbevolen, moet u daarom de **SSL CryptoAPI Cert Store Name** string instellen op &quot;My&quot;. Het instellen van deze parameter op &#39;Persoonlijk&#39; werkt niet. Dit is een eigenaardigheid van het Windows-certificaatarchief.

   Een volledige lijst van de vooraf bepaalde systeemopslag kan hier worden verkregen: [https://msdn.microsoft.com/en-us/library/windows/desktop/aa388136(v=vs.85).aspx](https://msdn.microsoft.com/en-us/library/windows/desktop/aa388136%28v=vs.85%29.aspx). Mogelijk bevat uw systeem extra certificaatopslagruimten. Als u een andere opslagplaats dan &quot;Persoonlijk&quot;(zoals **Mijn**) wenst te gebruiken, moet u de canonieke naam van de certificaatopslag verkrijgen en het verstrekken in het [!DNL Insight.cfg] dossier. (De naam van de systeemopslag &quot;Mijn&quot;wordt inconsistent bedoeld als &quot;Mijn&quot;en &quot;MIJN&quot;door de documentatie van Vensters. De parameter lijkt niet hoofdlettergevoelig te zijn.)

1. Nadat u deze parameters hebt toegevoegd en hebt gecontroleerd dat de waarden overeenkomen met de lijst in Windows Certificate Manager, slaat u het [!DNL Insight.cfg] bestand op.

U kunt het werkstation nu starten (of de verbinding met de server verbreken of opnieuw tot stand brengen). Data Workbench moet uw certificaat en sleutel laden uit het certificaatarchief en normaal verbinding maken.

## Logboekuitvoer {#section-a7ef8c9e90ef4bbabaa3cd51a2aca3ab}

Wanneer een certificaat niet wordt gevonden of ongeldig is, wordt dit foutbericht naar het [!DNL HTTP.log] bestand gegenereerd.

```
ERROR Fatal error: the cert could not be found!
```

>[!NOTE]
>
>U kunt het L4-logboekframework inschakelen door het [!DNL L4.cfg] bestand in te stellen (raadpleeg uw accountmanager om dit in te stellen).

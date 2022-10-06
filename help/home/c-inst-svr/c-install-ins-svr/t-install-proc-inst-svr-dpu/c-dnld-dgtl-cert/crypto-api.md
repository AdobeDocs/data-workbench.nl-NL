---
description: Met het Windows-certificaatarchief kunt u het certificaat en de persoonlijke sleutel van de client opslaan in het Windows-certificaatarchief voor SSL-communicatie met servers.
title: Windows-certificaatarchief
uuid: a8021295-375a-460b-8686-acf3bc43cd17
exl-id: 8613a941-6213-4bfa-9c35-dccc2acb6c17
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Windows-certificaatarchief{#windows-certificate-store}

{{eol}}

Met het Windows-certificaatarchief kunt u het certificaat en de persoonlijke sleutel van de client opslaan in het Windows-certificaatarchief voor SSL-communicatie met servers.

Het Windows-certificaatarchief voor de client is een nieuwe functie waarmee u het SSL-communicatiecertificaat en de persoonlijke sleutel kunt opslaan in het Windows-certificaatarchief in plaats van in `Insight/Certificates/<CertName>.pem` bestand. Het gebruik van het Windows-certificaatarchief heeft de voorkeur als u het certificaatarchief voor andere toepassingen gebruikt en het certificaatbeheer op één plaats wilt uitvoeren, of als u wilt genieten van het aanvullende Windows-auditlogboek dat door het Windows-certificaatarchief wordt geleverd.

>[!NOTE]
>
>Licentie met de licentieserver blijft behouden met behulp van de bestaande `<Common Name>.pem` en dat het certificaat dat is verkregen uit het certificaatarchief alleen wordt gebruikt voor communicatie met de servers die u opgeeft.

## Vereisten {#section-69b18600052145ff8e5299b7123e69c5}

1. U moet toegang hebben tot de [!DNL certmgr.msc] bestand met de mogelijkheid om een certificaat en sleutel te importeren in de **Persoonlijk** opslaan. (Dit zou voor de meeste gebruikers van Vensters moeten waar zijn.)

1. De gebruiker die de configuratie doet moet een exemplaar van hebben **OpenSSL** opdrachtregelprogramma.
1. De server en client moeten al zijn geconfigureerd voor het gebruik van een aangepast SSL-certificaat, zoals beschreven in [Aangepaste certificaten gebruiken](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/using-custom-certificates-dwb.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd), die instructies geven om het cliëntcertificaat in het het certificaatopslag van Vensters eerder op te slaan dan het op te slaan in **Certificaten** directory.

## Het Windows-certificaatarchief configureren {#section-3629802122e947d4b4f63e8b732cfe27}

Het Windows-certificaatarchief voor clients wordt als volgt ingeschakeld:

**Stap 1: Importeer het SSL-certificaat en de persoonlijke sleutel van de gebruiker naar het Windows-certificaatarchief.**

In [Aangepaste certificaten gebruiken](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/using-custom-certificates-dwb.md#concept-ee6a9b5015f84a0ba64a11428b0a72dd) u wordt opgedragen het SSL-certificaat en de sleutel in de volgende map te plaatsen:

```
< 
<filepath>
  DWB Install folder 
</filepath>>\Certificates\
```

De naam van het certificaat is `<Common Name>.pem` (zoals [!DNL Analytics Server 1.pem] (niet de [!DNL trust_ca_cert.pem] bestand.)

Voordat het certificaat en de persoonlijke sleutel kunnen worden geïmporteerd, moeten ze zijn omgezet van . [!DNL pem] opmaken naar een [!DNL .pfx] opmaak, zoals [!DNL pkcs12.pfx] ).

1. Open een opdrachtprompt of terminal en navigeer naar de map:

   ```
   <CommonName>.pem c: cd \<DWB Install folder \Certificates
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

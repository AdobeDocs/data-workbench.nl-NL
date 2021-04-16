---
description: Algemene informatie over digitale certificaten en procedures voor het downloaden en installeren van deze certificaten.
title: Digitale certificaten downloaden en installeren
uuid: ac484e96-21dc-4643-ae74-01ac957e30ee
exl-id: 8aae9b63-7df0-4725-9833-711246bbe746
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 0%

---

# Digitale certificaten downloaden en installeren{#downloading-and-installing-the-digital-certificates}

Algemene informatie over digitale certificaten en procedures voor het downloaden en installeren van deze certificaten.

* [Digitale certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-e48a776ef39042759d1dfb3444996d8b)
* [Door knooppunten vergrendelde certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-b3dc7dcf2aa3439cbe66b0461b42d485)
* [Huidige certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-15aabaa8625c46edaa7436e1f3fc29c5)
* [Digitale certificaten gebruiken op computers zonder internettoegang](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-809366329a7d4e198f95fe06c1f534fa)
* [Installatieprocedures voor digitale certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-19f31676aad344a98e26e4fca1fad03b)

## Digitale certificaten {#section-e48a776ef39042759d1dfb3444996d8b}

Adobe gebruikt X.509 digitale certificaten om de cliënt en servercomponenten te identificeren en voor authentiek te verklaren die omhoog een implementatie maken.

Wanneer u een servercomponent ( [!DNL Insight Server] of [!DNL Repeater]) installeert, moet u het digitale certificaat installeren dat Adobe voor de component heeft uitgegeven. Als u uw Adobe-toepassing naar een andere computer wilt migreren, moet u een nieuw certificaat van Adobe verkrijgen. Neem hiervoor contact op met de klantenservice van Adobe.

De algemene naam die op dit certificaat wordt weergegeven, identificeert de server door een opgegeven domeinnaam (bijvoorbeeld [!DNL vs001a.mycompany.com]). Wanneer een serverclient verbinding maakt met deze server, geeft de server dit certificaat als bewijs dat het inderdaad de server is die de client heeft aangevraagd.

Wanneer u een serverclient installeert (bijvoorbeeld [!DNL Insight] of [!DNL Report]), moet u het digitale certificaat installeren dat een benoemde persoon (bijvoorbeeld Jane Smith) toestaat om de geïnstalleerde clienttoepassing te gebruiken. Als u uw Adobe-toepassing naar een andere computer of een andere benoemde gebruiker moet migreren, moet u een nieuw certificaat van Adobe verkrijgen. Neem hiervoor contact op met de klantenservice van Adobe.

De clienttoepassing presenteert dit digitale certificaat om toegang te krijgen tot een servercomponent. Een beheerder van de servercomponent kan toegang tot servermiddelen beperken die op de gemeenschappelijke naam of organisatorische eenheidswaarden worden gebaseerd die in het certificaat van de cliënt verschijnen.

De X.509 digitale certificaten die met Adobe toepassingen worden geïnstalleerd laten ook zijn cliënt en servercomponenten toe om informatie over de Veilige Laag van Contactdozen (SSL) uit te wisselen. SSL beveiligt transmissies over HTTP gebruikend een publiek-en-privé zeer belangrijk encryptiesysteem. Adobe&#39;s implementatie van SSL ondersteunt 1024-bits RSA-sleutels en gebruikt een 128-bits RC4-versleutelingsalgoritme.

Naast beveiliging werken de digitale certificaten die u installeert ook als licentiecodes waarmee u de geïnstalleerde Adobe-software kunt uitvoeren. Een digitaal certificaat kan alleen correct functioneren als het is vergrendeld en actueel is, of als de toepassing niet wordt gestart.

## Tekenreekscodering {#section-8abe6b2d95704d38a04137d5c4602f0b}

Zie [String Encryption](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/string-encryption.md#concept-35da0b53650a4d7e82b240ad27f6d45a) voor het coderen van wachtwoorden.

## Niet-vergrendelde certificaten {#section-b3dc7dcf2aa3439cbe66b0461b42d485}

Een door knooppunten vergrendeld certificaat is een digitaal certificaat dat is geregistreerd op de computer waarop het is geïnstalleerd. Knooppuntvergrendeling koppelt een certificaat permanent aan een specifieke knooppunt-id (een waarde die een bepaalde computer uniek identificeert). Als u het certificaat wilt vergrendelen op een knooppunt, moet uw computer toegang hebben tot internet van de Adobe-licentieserver of een proxyserver die toegang heeft tot de licentieserver.

Als u een computer installeert die geen toegang heeft tot internet, moet u een speciaal vooraf vergrendeld certificaat verkrijgen en installeren, zoals beschreven in [Digitale certificaten gebruiken op computers zonder internettoegang](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-809366329a7d4e198f95fe06c1f534fa).

Als u op een computer installeert die tot Internet kan toegang hebben, wordt uw digitaal certificaat knoop-gesloten automatisch de eerste keer dat u uw product van de Adobe begint. Nadat het knooppunt-vergrendeld is, kan het certificaat niet op een andere computer worden gebruikt. Als u uw Adobe product naar een andere machine moet migreren, moet u een nieuw, niet-vergrendeld certificaat van Adobe verkrijgen.

## Huidige certificaten {#section-15aabaa8625c46edaa7436e1f3fc29c5}

Naast knooppuntvergrendeling moet een digitaal certificaat actueel zijn. Uw certificaat moet regelmatig opnieuw worden gevalideerd (gewoonlijk om de 30 dagen, maar kan afhankelijk van uw toestemming met Adobe variëren) om actueel te blijven. Als uw computer toegang tot internet heeft, is het proces voor opnieuw valideren volledig transparant. Uw Adobe-product maakt automatisch verbinding met de licentieserver en hervalideert het certificaat indien nodig. Als uw computer geen internettoegang heeft, moet u de bijgewerkte certificaten handmatig installeren, zoals beschreven in de volgende sectie.

## Digitale certificaten gebruiken op computers zonder internettoegang {#section-809366329a7d4e198f95fe06c1f534fa}

Als u een installatie uitvoert op een computer die geen toegang heeft tot internet, moet u een vooraf vergrendeld certificaat aanvragen voor de installatie van [!DNL Insight Server]. Een vooraf vergrendeld certificaat is een digitaal certificaat dat Adobe handmatig vergrendelt op de knooppuntidentificatie voor de computer.

Als u een vooraf vergrendeld certificaat wilt aanvragen, moet u de knooppuntidentificatie en uw certificaatnummer naar de klantenservice van Adobe sturen. Om de knoopherkenningsteken voor uw machine te verkrijgen, contacteer de Zorg van de Klant van Adobe om het nut van de Identifier van de Knoop van de Adobe te verzoeken. U kunt de knoopherkenningsteken van het alarm ook verkrijgen dat de software van de Adobe wanneer het probeert om met de Server van de Vergunning te verbinden en niet kan.

Wanneer u het vooraf vergrendelde certificaat ontvangt, installeert u dit zoals beschreven in de laatste twee stappen van [Digital Certificate Installation Procedures](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-19f31676aad344a98e26e4fca1fad03b). Wanneer het certificaat opnieuw moet worden gevalideerd, moet u een nieuw, gevalideerd certificaat downloaden van de licentieserver en opnieuw installeren op uw computer.

## Installatieprocedures voor digitale certificaten {#section-19f31676aad344a98e26e4fca1fad03b}

**Het digitale certificaat downloaden en installeren**

1. Open uw webbrowser op [https://aap.adobe.com](https://aap.adobe.com).

   >[!NOTE]
   >
   >Mogelijk wordt u in uw browser gevraagd om nu een digitaal certificaat voor te leggen. Als dit het geval is, klikt u gewoon op **[!UICONTROL Cancel]** om het dialoogvenster te sluiten.

1. Voer in het aanmeldingsscherm de **[!UICONTROL Account Name]** en **[!UICONTROL Password]** in die u van Adobe hebt ontvangen en klik vervolgens op **[!UICONTROL login]**.

1. Zoek het certificaat dat is uitgegeven voor uw [!DNL Insight Server] en klik vervolgens op het pictogram dat is gekoppeld aan dat certificaat.

   >[!NOTE]
   >
   >Noteer de algemene naam die aan dit certificaat is toegewezen. U gebruikt deze naam in een latere stap.

1. Wanneer ertoe aangezet om het certificaat te bewaren, klik **[!UICONTROL Save]**. (De naam van het bestand komt overeen met de algemene naam die aan het certificaat is gekoppeld.)
1. Download het bestand naar de map [!DNL Certificates] in de map waarin u [!DNL Insight Server] hebt geïnstalleerd. Deze map bevat al een certificaatbestand met de naam [!DNL trust_ca_cert.pem]. Dit certificaatbestand moet altijd aanwezig zijn.

1. Wijzig de naam van het gedownloade certificaatbestand in:

[!DNL server_cert.pem]

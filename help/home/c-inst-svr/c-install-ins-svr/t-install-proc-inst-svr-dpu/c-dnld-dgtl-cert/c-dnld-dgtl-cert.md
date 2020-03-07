---
description: Algemene informatie over digitale certificaten, en procedures om hen te downloaden en te installeren.
solution: Insight
title: De digitale certificaten downloaden en installeren
uuid: ac484e96-21dc-4643-ae74-01ac957e30ee
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De digitale certificaten downloaden en installeren{#downloading-and-installing-the-digital-certificates}

Algemene informatie over digitale certificaten, en procedures om hen te downloaden en te installeren.

* [Het begrip van Digitale Certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-e48a776ef39042759d1dfb3444996d8b)
* [Certificaten zonder noden](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-b3dc7dcf2aa3439cbe66b0461b42d485)
* [Huidige certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-15aabaa8625c46edaa7436e1f3fc29c5)
* [Digitale certificaten gebruiken op machines zonder internettoegang](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-809366329a7d4e198f95fe06c1f534fa)
* [Procedures voor de installatie van digitale certificaten](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-19f31676aad344a98e26e4fca1fad03b)

## Het begrip van Digitale Certificaten {#section-e48a776ef39042759d1dfb3444996d8b}

Adobe gebruikt X.509 digitale certificaten om de cliënt en servercomponenten te identificeren en voor authentiek te verklaren die omhoog een implementatie maken.

Wanneer u een servercomponent ( [!DNL Insight Server] of [!DNL Repeater]) installeert, moet u het digitale certificaat installeren dat Adobe voor de component heeft uitgegeven. Als u uw toepassing van Adobe aan een andere machine moet migreren, moet u een nieuw certificaat van Adobe verkrijgen. Om dit te doen, contacteer de Zorg van de Klant van Adobe.

De gemeenschappelijke naam die op dit certificaat verschijnt identificeert de server door een gespecificeerde domeinnaam (bijvoorbeeld, [!DNL vs001a.mycompany.com]). Wanneer een servercliënt met deze server verbindt, stelt de server dit certificaat als bewijs voor dat het, inderdaad, de server is die de cliënt vroeg.

Op dezelfde manier wanneer u een servercliënt (bijvoorbeeld, [!DNL Insight] of [!DNL Report]) installeert moet u het digitale certificaat installeren dat een genoemd individu (bijvoorbeeld, Jane Smith) machtigt om de geïnstalleerde cliënttoepassing te gebruiken. Als u uw toepassing van Adobe aan een andere machine of een andere genoemde gebruiker moet migreren, moet u een nieuw certificaat van Adobe verkrijgen. Om dit te doen, contacteer de Zorg van de Klant van Adobe.

De cliënttoepassing stelt dit digitale certificaat voor om tot een servercomponent toegang te krijgen. Een beheerder van de servercomponent kan toegang tot servermiddelen beperken die op de gemeenschappelijke naam of organisatorische eenheidswaarden worden gebaseerd die in het certificaat van de cliënt verschijnen.

De X.509 digitale certificaten die met de toepassingen van Adobe worden geïnstalleerd laten ook zijn cliënt en servercomponenten toe om informatie over de Veilige Laag van Contactdozen te ruilen (SSL). SSL beveiligt transmissies over HTTP gebruikend een openbaar-en-privé zeer belangrijk encryptiesysteem. De implementatie van Adobe van SSL steunt 1024 beetjeRSA sleutels en gebruikt een 128 beetjeRC4 encryptiealgoritme.

Naast veiligheid, functioneren de digitale certificaten die u installeert ook als vergunningssleutels die u toelaten om de geïnstalleerde software van Adobe in werking te stellen. Om behoorlijk te functioneren, moet een digitaal certificaat knoop-gesloten en huidig zijn, of de toepassing begint niet.

## String Encryption {#section-8abe6b2d95704d38a04137d5c4602f0b}

Zie de Encryptie [van het](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/string-encryption.md#concept-35da0b53650a4d7e82b240ad27f6d45a) Koord voor het coderen van wachtwoorden.

## Certificaten zonder noden {#section-b3dc7dcf2aa3439cbe66b0461b42d485}

Een knoop-gesloten certificaat is een digitaal certificaat dat aan de machine is geregistreerd waarop het geïnstalleerd is. Het sluiten van de knoop associeert permanent een certificaat met een specifiek knoopherkenningsteken (een waarde die uniek een bepaalde machine identificeert). Om knoopslot uw certificaat te sluiten, moet uw machine de toegang van Internet tot de Server van de Vergunning van Adobe of tot een volmachtsserver hebben die toegang tot de Server van de Vergunning heeft.

Als u op een machine installeert die tot Internet niet kan toegang hebben, moet u een speciaal vooraf gesloten certificaat verkrijgen en installeren zoals die in het [Gebruiken van Digitale Certificaten op Machines zonder de Toegang](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-809366329a7d4e198f95fe06c1f534fa)van Internet wordt beschreven.

Als u op een machine installeert die tot Internet kan toegang hebben, is uw digitaal certificaat knoop-gesloten automatisch de eerste keer dat u uw product van Adobe begint. Nadat het wordt knoop-gesloten, kan het certificaat niet op een andere machine worden gebruikt. Als u uw product van Adobe aan een andere machine moet migreren, moet u een nieuw, ontgrendeld certificaat van Adobe verkrijgen.

## Huidige certificaten {#section-15aabaa8625c46edaa7436e1f3fc29c5}

Naast het zijn knoop-gesloten, moet een digitaal certificaat huidig zijn. Om huidig te blijven, moet uw certificaat op een regelmatige basis (over het algemeen om de 30 dagen opnieuw worden bevestigd, maar kan afhankelijk van uw overeenkomst met Adobe variëren). Als uw machine de toegang van Internet heeft, is het herbevestigingsproces volledig transparant. Uw product van Adobe verbindt automatisch met de Server van de Vergunning en bevestigt het certificaat wanneer nodig opnieuw. Als uw machine geen toegang tot Internet heeft, moet u bijgewerkte certificaten manueel installeren zoals die in de volgende sectie wordt beschreven.

## Digitale certificaten gebruiken op machines zonder internettoegang {#section-809366329a7d4e198f95fe06c1f534fa}

Als u op een machine installeert die tot Internet niet kan toegang hebben, moet u een vooraf gesloten certificaat voor uw installatie van [!DNL Insight Server]vragen. Een pre-gesloten certificaat is een digitaal certificaat dat Adobe manueel aan het knoopherkenningsteken voor de machine sluit.

Om een vooraf gesloten certificaat aan te vragen, moet u het knoopherkenningsteken en uw certificaataantal naar de Zorg van de Klant van Adobe verzenden. Om het knoopherkenningsteken voor uw machine te verkrijgen, contacteer de Zorg van de Klant van Adobe om het nut van het Herkenningsteken van de Knoop van Adobe te verzoeken. U kunt ook het knoopherkenningsteken uit het alarm verkrijgen dat de de softwarekwesties van Adobe wanneer het probeert om met de Server van de Vergunning te verbinden en niet kan.

Wanneer u het vooraf vergrendelde certificaat ontvangt, installeert u het zoals beschreven in de laatste twee stappen van de [Digital Certificate Installation Procedures](../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-dnld-dgtl-cert/c-dnld-dgtl-cert.md#section-19f31676aad344a98e26e4fca1fad03b). Wanneer het certificaat opnieuw moet worden bevestigd, moet u een nieuw, bevestigd certificaat van de Server van de Vergunning downloaden en het opnieuw installeren op uw machine.

## Procedures voor de installatie van digitale certificaten {#section-19f31676aad344a98e26e4fca1fad03b}

**Om het digitale certificaat te downloaden en te installeren**

1. Open uw Webbrowser aan [https://aap.adobe.com](https://aap.adobe.com).

   >[!NOTE]
   >
   >Uw browser zou u kunnen ertoe aanzetten om een digitaal certificaat op dit punt voor te stellen. Als het, eenvoudig klik **[!UICONTROL Cancel]** om de dialoogdoos te verwerpen.

1. Voor het login scherm, ga de **[!UICONTROL Account Name]** en **[!UICONTROL Password]** die u van Adobe ontving in, dan klik **[!UICONTROL login]**.

1. Bepaal de plaats van het certificaat dat voor uw is uitgegeven [!DNL Insight Server], dan klik het pictogram verbonden aan dat certificaat.

   >[!NOTE]
   >
   >Maak een nota van de gemeenschappelijke naam die aan dit certificaat wordt toegewezen. U gebruikt deze naam in een recentere stap.

1. Wanneer ertoe aangezet om het certificaat te bewaren, klik **[!UICONTROL Save]**. (Merk op dat de naam van het dossier de gemeenschappelijke naam aanpast verbonden aan het certificaat.)
1. Download het dossier aan de [!DNL Certificates] omslag in de folder waar u installeerde [!DNL Insight Server]. Deze omslag bevat reeds een certificaatdossier genoemd [!DNL trust_ca_cert.pem]. Dit certificaatdossier moet altijd aanwezig zijn.

1. Noem het gedownloade certificaatdossier anders aan:

[!DNL server_cert.pem]


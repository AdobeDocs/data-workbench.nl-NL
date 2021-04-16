---
description: Adobe gebruikt X.509 digitale certificaten om de cliënt en servercomponenten te identificeren en voor authentiek te verklaren die omhoog een implementatie maken.
title: Digitale certificaten
uuid: a2d84e9a-16aa-4973-85da-303614a4ad7f
exl-id: 967e9d5b-7972-497e-8902-8db0eb304f27
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---

# Digitale certificaten{#understanding-digital-certificates}

Adobe gebruikt X.509 digitale certificaten om de cliënt en servercomponenten te identificeren en voor authentiek te verklaren die omhoog een implementatie maken.

Wanneer u [!DNL Report Server] installeert, moet u het digitale certificaat installeren dat een genoemde individu (bijvoorbeeld, Jane Smith) toestaat om de geïnstalleerde cliënttoepassing te gebruiken.

>[!NOTE]
>
>Als u [!DNL Report Server] aan een andere machine of een andere genoemde gebruiker moet migreren, moet u een nieuw certificaat van Adobe verkrijgen. Neem hiervoor contact op met de klantenservice van Adobe.

[!DNL Report Server] presenteert dit digitale certificaat om toegang te krijgen tot een servercomponent. Een beheerder van de servercomponent kan toegang tot servermiddelen beperken die op de gemeenschappelijke naam of organisatorische eenheidswaarden worden gebaseerd die in het certificaat van de cliënt verschijnen.

De X.509 digitale certificaten die met Adobe toepassingen worden geïnstalleerd laten ook zijn cliënt en servercomponenten toe om informatie over de Veilige Laag van Contactdozen (SSL) uit te wisselen. SSL beveiligt transmissies over HTTP gebruikend een publiek-en-privé zeer belangrijk encryptiesysteem. Adobe&#39;s implementatie van SSL ondersteunt 1024-bits RSA-sleutels en gebruikt een 128-bits RC4-versleutelingsalgoritme.

Het digitale certificaat dat u installeert, werkt niet alleen als beveiliging, maar ook als licentiecode waarmee u de geïnstalleerde [!DNL Report Server] kunt uitvoeren. Een digitaal certificaat kan alleen correct functioneren als het is vergrendeld en actueel is, of als de toepassing wordt gestart.

## Niet-vergrendelde certificaten {#section-3338f1558e7844888dced8f395888744}

Een door knooppunten vergrendeld certificaat is een digitaal certificaat dat is geregistreerd op de computer waarop het is geïnstalleerd. Knooppuntvergrendeling koppelt een certificaat permanent aan een specifieke knooppunt-id (een waarde die een bepaalde computer uniek identificeert). Als u het certificaat wilt vergrendelen op een knooppunt, moet uw computer toegang hebben tot internet van de Adobe-licentieserver of een proxyserver die toegang heeft tot de licentieserver.

Als u een computer installeert die geen toegang heeft tot internet, moet u een speciaal vooraf vergrendeld certificaat verkrijgen en installeren, zoals beschreven in [Digitale certificaten gebruiken op computers zonder internettoegang](../../../../home/c-rpt-oview/c-inst-rpt/c-install-dig-cert/c-underst-dig-cert.md#section-18cce05e2204407bb2b6b75deab9197d) op deze pagina.

Als u op een computer installeert die tot Internet kan toegang hebben, wordt uw digitaal certificaat knoop-gesloten automatisch de eerste keer dat u [!DNL Report Server] begint. Nadat het knooppunt-vergrendeld is, kan het certificaat niet op een andere computer worden gebruikt. Als u [!DNL Report Server] naar een andere machine moet migreren, moet u een nieuw, niet-vergrendeld certificaat van Adobe verkrijgen.

## Huidige certificaten {#section-b4053ab714514dfb97ea7f61bbb8da1e}

Naast knooppuntvergrendeling moet een digitaal certificaat actueel zijn. Uw certificaat moet regelmatig opnieuw worden gevalideerd (gewoonlijk om de 30 dagen, maar kan afhankelijk van uw overeenkomst met Adobe variëren) om actueel te blijven. Als uw computer toegang tot internet heeft, is het proces voor opnieuw valideren volledig transparant. [!DNL Report Server] maakt automatisch verbinding met de licentieserver en valideert het certificaat indien nodig opnieuw. Als uw computer geen internettoegang heeft, moet u de bijgewerkte certificaten handmatig installeren, zoals beschreven in de volgende sectie.

## Digitale certificaten gebruiken op computers zonder internettoegang {#section-18cce05e2204407bb2b6b75deab9197d}

Als u een installatie uitvoert op een computer die geen toegang heeft tot internet, moet u een vooraf vergrendeld certificaat aanvragen voor de installatie van [!DNL Report Server]. Een vooraf vergrendeld certificaat is een digitaal certificaat dat Adobe handmatig vergrendelt op de knooppuntidentificatie voor de computer.

Als u een vooraf vergrendeld certificaat wilt aanvragen, moet u de knooppuntidentificatie en uw certificaatnummer naar de klantenservice van Adobe sturen. Om de knoopherkenningsteken voor uw machine te verkrijgen, contacteer de Zorg van de Klant van Adobe om het Adobe [!DNL Node Identifier] nut te verzoeken. U kunt de knoopherkenningsteken van het alarm ook verkrijgen dat [!DNL Report Server] uitgeeft wanneer het probeert om met de Server van de Vergunning te verbinden en niet kan. Wanneer u het vooraf vergrendelde certificaat ontvangt, installeert u dit zoals beschreven in de laatste twee stappen van [Digital Certificate Installation Procedures](../../../../home/c-rpt-oview/c-inst-rpt/c-install-dig-cert/t-dig-cert-install-proc.md#task-5c4bb352ff534b40adc46dd053874e5d).

Wanneer het certificaat opnieuw moet worden gevalideerd, moet u een nieuw gevalideerd certificaat downloaden van de licentieserver en dit opnieuw op uw computer installeren (tenzij u akkoord gaat met Adobe, anders).

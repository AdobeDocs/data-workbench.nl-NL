---
description: Adobe gebruikt X.509 digitale certificaten om de cliënt en servercomponenten te identificeren en voor authentiek te verklaren die omhoog een implementatie maken.
solution: Analytics
title: Het begrip van Digitale Certificaten
topic: Data workbench
uuid: a2d84e9a-16aa-4973-85da-303614a4ad7f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het begrip van Digitale Certificaten{#understanding-digital-certificates}

Adobe gebruikt X.509 digitale certificaten om de cliënt en servercomponenten te identificeren en voor authentiek te verklaren die omhoog een implementatie maken.

Wanneer u installeert [!DNL Report Server], moet u het digitale certificaat installeren dat een genoemd individu (bijvoorbeeld, Jane Smith) machtigt om de geïnstalleerde cliënttoepassing te gebruiken.

>[!NOTE]
>
>Als u [!DNL Report Server] naar een andere machine of een andere genoemde gebruiker moet migreren, moet u een nieuw certificaat van Adobe verkrijgen. Om dit te doen, contacteer de Zorg van de Klant van Adobe.

[!DNL Report Server] stelt dit digitale certificaat voor om tot een servercomponent toegang te krijgen. Een beheerder van de servercomponent kan toegang tot servermiddelen beperken die op de gemeenschappelijke naam of organisatorische eenheidswaarden worden gebaseerd die in het certificaat van de cliënt verschijnen.

De X.509 digitale certificaten die met de toepassingen van Adobe worden geïnstalleerd laten ook zijn cliënt en servercomponenten toe om informatie over de Veilige Laag van Contactdozen te ruilen (SSL). SSL beveiligt transmissies over HTTP gebruikend een openbaar-en-privé zeer belangrijk encryptiesysteem. De implementatie van Adobe van SSL steunt 1024 beetjeRSA sleutels en gebruikt een 128 beetjeRC4 encryptiealgoritme.

Naast veiligheid, functioneert het digitale certificaat dat u installeert ook als vergunningssleutel die u toelaat om geïnstalleerd in werking te stellen [!DNL Report Server]. Om behoorlijk te functioneren, moet een digitaal certificaat knoop-gesloten en huidig zijn, of de toepassing zal niet beginnen.

## Certificaten zonder noden {#section-3338f1558e7844888dced8f395888744}

Een knoop-gesloten certificaat is een digitaal certificaat dat aan de machine is geregistreerd waarop het geïnstalleerd is. Het sluiten van de knoop associeert permanent een certificaat met een specifiek knoopherkenningsteken (een waarde die uniek een bepaalde machine identificeert). Om knoopslot uw certificaat te sluiten, moet uw machine de toegang van Internet tot de Server van de Vergunning van Adobe of tot een volmachtsserver hebben die toegang tot de Server van de Vergunning heeft.

Als u op een machine installeert die tot Internet niet kan toegang hebben, moet u een speciaal vooraf gesloten certificaat verkrijgen en installeren zoals die in het [Gebruiken van Digitale Certificaten op Machines zonder de Toegang](../../../../home/c-rpt-oview/c-inst-rpt/c-install-dig-cert/c-underst-dig-cert.md#section-18cce05e2204407bb2b6b75deab9197d) van Internet op deze pagina wordt beschreven.

Als u op een machine installeert die tot Internet kan toegang hebben, is uw digitaal certificaat knoop-gesloten automatisch de eerste keer dat u begint [!DNL Report Server]. Nadat het wordt knoop-gesloten, kan het certificaat niet op een andere machine worden gebruikt. Als u [!DNL Report Server] naar een andere machine moet migreren, moet u een nieuw, ontgrendeld certificaat van Adobe verkrijgen.

## Huidige certificaten {#section-b4053ab714514dfb97ea7f61bbb8da1e}

Naast het zijn knoop-gesloten, moet een digitaal certificaat huidig zijn. Om huidig te blijven, moet uw certificaat regelmatig opnieuw worden bevestigd, (over het algemeen om de 30 dagen, maar kan afhankelijk van uw overeenkomst met Adobe variëren). Als uw machine de toegang van Internet heeft, is het herbevestigingsproces volledig transparant. [!DNL Report Server] verbindt automatisch met de Server van de Vergunning en hervalideert het certificaat wanneer nodig. Als uw machine geen toegang tot Internet heeft, moet u bijgewerkte certificaten manueel installeren zoals die in de volgende sectie wordt beschreven.

## Digitale certificaten gebruiken op machines zonder internettoegang {#section-18cce05e2204407bb2b6b75deab9197d}

Als u op een machine installeert die tot Internet niet kan toegang hebben, moet u een vooraf gesloten certificaat voor uw installatie van [!DNL Report Server]vragen. Een pre-gesloten certificaat is een digitaal certificaat dat Adobe manueel aan het knoopherkenningsteken voor de machine sluit.

Om een vooraf gesloten certificaat aan te vragen, moet u het knoopherkenningsteken en uw certificaataantal naar de Zorg van de Klant van Adobe verzenden. Om het knoopherkenningsteken voor uw machine te verkrijgen, contacteer de Zorg van de Klant van Adobe om het [!DNL Node Identifier] nut van Adobe te verzoeken. U kunt ook het knoopherkenningsteken uit het alarm verkrijgen dat [!DNL Report Server] kwesties wanneer het probeert om met de Server van de Vergunning te verbinden en niet kan. Wanneer u het vooraf vergrendelde certificaat ontvangt, installeert u het zoals beschreven in de laatste twee stappen van de [Digital Certificate Installation Procedures](../../../../home/c-rpt-oview/c-inst-rpt/c-install-dig-cert/t-dig-cert-install-proc.md#task-5c4bb352ff534b40adc46dd053874e5d).

Wanneer het certificaat opnieuw moet worden bevestigd, moet u een nieuw bevestigd certificaat van de Server van de Vergunning downloaden en het opnieuw installeren op uw machine (tenzij uw overeenkomst met Adobe anders verklaart).

---
description: Het Portaal van het Rapport gebruikt de informatie in een configuratiedossier genoemd global.asa om gebruikerszittingen te initialiseren.
title: Het sessieconfiguratiebestand bewerken
uuid: c1bcd4d2-9bf5-425a-bda2-7f805983cdc6
exl-id: 98cf2e11-afb8-4530-aaa4-ea3c913effc1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# Het sessieconfiguratiebestand bewerken{#edit-the-session-configuration-file}

{{eol}}

Het Portaal van het Rapport gebruikt de informatie in een configuratiedossier genoemd global.asa om gebruikerszittingen te initialiseren.

Wanneer u [!DNL Report Portal], moet u dit bestand bewerken zoals aangegeven. De [!DNL global.asa] Het bestand bevindt zich in de map \*PortalName*\PortalASP\.

>[!NOTE]
>
>Wijzig geen andere parameters in dit configuratiebestand.

1. Open op de computer waarop IIS wordt uitgevoerd de [!DNL global.asa] bestand in een teksteditor, zoals Kladblok.
1. Optioneel. Gebruikers toegang geven tot [!DNL Report Portal] zonder verificatie wijzigt u de waarde van de parameter Session(&quot;In&quot;) in true. De standaardwaarde is false. Hiermee worden alle gebruikers geverifieerd die toegang proberen te krijgen [!DNL Report Portal].
1. Als uw [!DNL Report Portal] wordt geïnstalleerd op een ander station dan het station C, wijzigt u de waarde van de parameter Session(&quot;Drive&quot;) in de juiste stationslocatie.
1. Voor de parameter Session (&quot;DBPath&quot;) wijzigt u de waarde om het pad naar de database te weerspiegelen die de informatie bevat die nodig is voor verificatie [!DNL Report Portal] gebruikers. Plaats de stationsletter niet, maar zorg ervoor dat u een slash aan het einde toevoegt.

   Voorbeeld: [!DNL /Inetpub/wwwroot/Portal/data/]

1. Sla het bestand op.
1. Om te verifiëren dat [!DNL Report Portal] bestanden correct zijn geïnstalleerd en via de toegewezen virtuele map kunnen worden bereikt, opent u de volgende pagina in uw browser:

   https://*YourServerAddress*/*YourPortalName*

   Voorbeeld: [!DNL https://localhost/VisualReportPortal]

   Als de [!DNL Report Portal] ASPs is correct geïnstalleerd, zou u de poortlogin pagina moeten zien. Als u deze pagina niet ziet, verifieer dat ASPs op uw IIS wordt toegelaten en uw virtuele folderafbeeldingen tweemaal controleert.

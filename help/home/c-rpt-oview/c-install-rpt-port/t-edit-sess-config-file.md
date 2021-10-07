---
description: Het Portaal van het Rapport gebruikt de informatie in een configuratiedossier genoemd global.asa om gebruikerszittingen te initialiseren.
title: Het sessieconfiguratiebestand bewerken
uuid: c1bcd4d2-9bf5-425a-bda2-7f805983cdc6
exl-id: 98cf2e11-afb8-4530-aaa4-ea3c913effc1
source-git-commit: 79981e92dd1c2e552f958716626a632ead940973
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# Het sessieconfiguratiebestand bewerken{#edit-the-session-configuration-file}

Het Portaal van het Rapport gebruikt de informatie in een configuratiedossier genoemd global.asa om gebruikerszittingen te initialiseren.

Wanneer u [!DNL Report Portal] installeert, moet u dit dossier zoals aangewezen uitgeven. Het [!DNL global.asa] dossier verblijft in \*PortalName*\PortalASP\ folder.

>[!NOTE]
>
>Wijzig geen andere parameters in dit configuratiebestand.

1. Op de machine waar IIS loopt, open het [!DNL global.asa] dossier in een tekstredacteur zoals Blocnote.
1. Optioneel. Als u gebruikers toegang wilt geven tot [!DNL Report Portal] zonder verificatie, wijzigt u de waarde van de parameter Session(&quot;In&quot;) in true. De standaardwaarde is false. Hiermee worden alle gebruikers geverifieerd die toegang proberen te krijgen tot [!DNL Report Portal].
1. Als uw [!DNL Report Portal] op een aandrijving buiten C wordt geïnstalleerd, verander de waarde van de Sessie (&quot;Aandrijving&quot;) parameter in de correcte aandrijvingsplaats.
1. Voor de parameter Session (&quot;DBPath&quot;), verander de waarde om de weg aan het gegevensbestand te weerspiegelen dat de informatie nodig bevat om [!DNL Report Portal] gebruikers voor authentiek te verklaren. Plaats de stationsletter niet, maar zorg ervoor dat u een slash aan het einde toevoegt.

   Voorbeeld: [!DNL /Inetpub/wwwroot/Portal/data/]

1. Sla het bestand op.
1. Als u wilt controleren of de [!DNL Report Portal]-bestanden correct zijn geïnstalleerd en via de toegewezen virtuele map kunnen worden bereikt, opent u de volgende pagina in uw browser:

   https://*YourServerAddress*/*YourPortalName*

   Voorbeeld: [!DNL https://localhost/VisualReportPortal]

   Als [!DNL Report Portal] ASPs correct geïnstalleerd is, zou u de poortlogin pagina moeten zien. Als u deze pagina niet ziet, verifieer dat ASPs op uw IIS wordt toegelaten en uw virtuele folderafbeeldingen tweemaal controleert.

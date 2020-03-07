---
description: Het Portaal van het Rapport gebruikt de informatie in een configuratiedossier genoemd global.asa om gebruikerszittingen te initialiseren.
solution: Analytics
title: Het sessieconfiguratiebestand bewerken
topic: Data workbench
uuid: c1bcd4d2-9bf5-425a-bda2-7f805983cdc6
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het sessieconfiguratiebestand bewerken{#edit-the-session-configuration-file}

Het Portaal van het Rapport gebruikt de informatie in een configuratiedossier genoemd global.asa om gebruikerszittingen te initialiseren.

Wanneer u installeert [!DNL Report Portal], moet u dit dossier uitgeven zoals vermeld. Het [!DNL global.asa] dossier verblijft in \*PortalName*\PortalASP\ folder.

>[!NOTE]
>
>Verander geen andere parameters in dit configuratiedossier.

1. Voor de machine waar IIS loopt, open het [!DNL global.asa] dossier in een tekstredacteur zoals Blocnote.
1. Optioneel. Om gebruikers tot [!DNL Report Portal] zonder authentificatie toegang te laten, verander de de parameterwaarde van de Zitting (&quot;In&quot;) in waar. Het gebrek is vals, die alle gebruikers voor authentiek verklaart die proberen om tot toegang te hebben [!DNL Report Portal].
1. Als uw schijf op een ander station dan station C [!DNL Report Portal] is geïnstalleerd, wijzigt u de waarde van de parameter Session(&quot;Drive&quot;) in de juiste stationslocatie.
1. Voor de parameter van de Zitting (&quot;DBPath&quot;), verander de waarde om op de weg aan het gegevensbestand te wijzen dat de informatie nodig bevat om [!DNL Report Portal] gebruikers voor authentiek te verklaren. Neem de aandrijvingsbrief niet op, maar zorg ervoor om een het slepen schuine streep te omvatten.

   Voorbeeld: [!DNL /Inetpub/wwwroot/Portal/data/]

1. Sla het bestand op.
1. Om te verifiëren dat de [!DNL Report Portal] dossiers correct zijn geïnstalleerd en door hun aangewezen virtuele folder kunnen worden bereikt, open de volgende pagina in uw browser:

   http://*YourServerAddress*/*YourPortalName*

   Voorbeeld: [!DNL http://localhost/VisualReportPortal]

   Als [!DNL Report Portal] ASPs correct is geïnstalleerd, zou u de poortlogin pagina moeten zien. Als u deze pagina niet ziet, verifieer dat ASPs op uw IIS wordt toegelaten en controleer uw virtuele folderafbeeldingen tweemaal.


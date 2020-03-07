---
description: Nadat u uw experiment hebt opgesteld, zou u moeten bevestigen dat het experiment behoorlijk werkt.
solution: Insight,Analytics
title: Het experiment valideren
topic: Data workbench
uuid: 59769f5b-4175-479e-ad7d-7226e9c666af
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het experiment valideren{#validating-the-experiment}

Nadat u uw experiment hebt opgesteld, zou u moeten bevestigen dat het experiment behoorlijk werkt.

Zoals besproken in het [Wijzigen van de (Facultatieve)](../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expckurl-prm.md#concept-215bf86bab4e4ec0b0cc803ec48a8fcf)Paramter ExpCookieURL, kan de pagina die in de parameter ExpCookieURL in het [!DNL Sensor] configuratiedossier wordt gespecificeerd worden gebruikt om zich in een specifieke experimentgroep te plaatsen.

De standaard virtuele pagina is [!DNL /setcookie.htm], maar u moet de waarde gebruiken die u in de parameter ExpCookieURL plaatst.

## De testpagina aanvragen {#section-8aed3b48d47f4e6c8869c0216f8781b1}

Om een specifieke experimentatiegroep voor uw website te testen, moet uw browser worden geconfigureerd om cookies goed te keuren en u moet niet al een cookie voor deze website hebben.

Telkens als u een nieuwe groep wilt testen, zorg ervoor om uw koekjes voor de website te ontruimen.

Om zich in een specifieke groep binnen een specifiek experiment te plaatsen, verzoek om de testpagina met een vraagkoord in de volgende vorm:

[!DNL http://] *&lt;[!DNL sitename/?Experiment Name=Group Name]>*

Bijvoorbeeld:

[!DNL http://www.omniture.com/setcookie.htm?New_Homepage=index2]

Wanneer het virtuele verzoek URL naar de server wordt verzonden, [!DNL Sensor] identificeert u als lid van de gespecificeerde groep binnen het gespecificeerde experiment en richt u dan aan de wortel van de website opnieuw. U kunt nu aan de aangewezen plaats op de website navigeren om te bevestigen of de correcte inhoudsvertoningen voor dat experiment en groep.

Als u het volgende in uw browser moest typen, zou browser de homepage van de website tonen en u in de index2 groep binnen het experiment plaatsen New_Homepage:

[!DNL http://www.omniture.com/setcookie.htm?New_Homepage=index2]

Wanneer de bezoekers in de index2 groep om de homepage verzoeken, de &quot;Verzoek een Demo&quot;grafische verbindingsvertoningen hoger op de pagina, zoals in volgende grafisch verzoeken:

![](assets/TestPage.png)


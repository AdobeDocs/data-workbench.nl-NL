---
description: Nadat u uw experiment hebt opgesteld, zou u moeten bevestigen dat het experiment behoorlijk werkt.
solution: Analytics,Analytics
title: Het experiment valideren
uuid: 59769f5b-4175-479e-ad7d-7226e9c666af
exl-id: 6dfd01ca-288d-40fd-aad4-75a588902ebd
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Het experiment valideren{#validating-the-experiment}

Nadat u uw experiment hebt opgesteld, zou u moeten bevestigen dat het experiment behoorlijk werkt.

Zoals besproken in [Modifying the ExpCookieURL Paramter (Optional)](../../home/c-undst-ctrld-exp/t-en-ctrld-exp/c-mod-expckurl-prm.md#concept-215bf86bab4e4ec0b0cc803ec48a8fcf), kan de pagina die in de parameter ExpCookieURL in het [!DNL Sensor] configuratiedossier wordt gespecificeerd worden gebruikt om zich in een specifieke proefgroep te plaatsen.

De standaard virtuele pagina is [!DNL /setcookie.htm], maar u moet de waarde gebruiken die u in de parameter ExpCookieURL plaatst.

## Testpagina {#section-8aed3b48d47f4e6c8869c0216f8781b1} aanvragen

Als u een specifieke testgroep voor uw website wilt testen, moet uw browser zo zijn geconfigureerd dat cookies worden geaccepteerd en moet u nog geen cookie voor deze website hebben.

Elke keer dat u een nieuwe groep wilt testen, moet u de cookies voor de website wissen.

Als u uzelf in een specifieke groep in een specifiek experiment wilt plaatsen, vraagt u de testpagina aan met een queryreeks in de volgende vorm:

[!DNL http://] *&lt; [!DNL sitename/?Experiment Name=Group Name]>*

Bijvoorbeeld:

[!DNL http://www.omniture.com/setcookie.htm?New_Homepage=index2]

Wanneer het virtuele URL-verzoek naar de server wordt verzonden, identificeert [!DNL Sensor] u als lid van de opgegeven groep binnen het opgegeven experiment en leidt u vervolgens naar de hoofdmap van de website. U kunt nu naar de juiste locatie op de website navigeren om te controleren of de juiste inhoud voor dat experiment en die groep wordt weergegeven.

Als u het volgende in uw browser zou typen, zou browser de homepage van de website tonen en u in de index2 groep binnen het New_Homepage experiment plaatsen:

[!DNL http://www.omniture.com/setcookie.htm?New_Homepage=index2]

Wanneer bezoekers in de index2 groep de homepage aanvragen, wordt de grafische koppeling &quot;Verzoek om een demo&quot; hoger weergegeven op de pagina, zoals in de volgende afbeelding:

![](assets/TestPage.png)

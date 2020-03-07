---
description: Richtlijnen voor het specificeren van het outputformaat.
solution: Analytics
title: Uitvoerindeling
topic: Data workbench
uuid: 12086f14-bad1-4d27-82fb-533e877d0a04
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Uitvoerindeling{#output-format}

Richtlijnen voor het specificeren van het outputformaat.

* Elke metrische of afmetingsnaam moet met een percententeken (%) beginnen en eindigen.

   * %XYZ% specificeert het element van afmeting XYZ die aan het element van Niveau beantwoordt. Een fout wordt geproduceerd als de afmeting XYZ niet één-aan-één of één-aan-velen met Niveau is.
   * %=XYZ% specificeert de waarde van metrische of metrische formule XYZ voor het bepaalde element van Niveau.

* De namen van de afmetingen die twee woorden zijn of langer vereisen geen onderstreepingen.
* De metrische namen die twee woorden zijn of meer vereisen onderstreepingen.

>[!NOTE]
>
>Als u de sleutel van CTRL onderdrukt en binnen het [!DNL Output Format] gebied met de rechtermuisknop klikt, [!DNL Insert menu] verschijnt een. Dit menu bevat een lijst van speciale karakters (bijvoorbeeld, Lusje) die vaak als afbakeningen worden gebruikt.

Als u de gegevens van de zittingsduur voor uw segment wilt uitvoeren, moet u nieuwe metrisch tot stand brengen die op de metrische Duur van de Zitting wordt gebaseerd. Nieuwe metrisch, die voor gebruik slechts met het [!DNL Output Format] gebied van de segmentuitvoer is, laat Microsoft Excel toe om zittingen correct te interpreteren die minder dan één uur duren. Om een nieuwe metrische zittingsduur tot stand te brengen, open het [!DNL Session Duration.metric] dossier (van [!DNL Profile Manager]) en neem een pond teken (#) in het ftime koord op: [!DNL ftime = string: %#H:%M:%S]

Het pondteken zorgt ervoor dat een belangrijke &quot;0&quot;aan zittingsduur van minder dan 1 uur wordt toegevoegd. Dientengevolge, interpreteert Excel 0:53:21 als 53 minuten en 21 seconden. Sparen nieuwe metrisch met een verschillende naam en upload het aan het aangewezen profiel voor anderen aan gebruik door het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan te klikken en **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>* te klikken.

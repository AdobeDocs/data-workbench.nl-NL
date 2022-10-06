---
description: Richtlijnen voor het opgeven van de uitvoerindeling.
title: Uitvoerindeling
uuid: 12086f14-bad1-4d27-82fb-533e877d0a04
exl-id: e695eaf4-ebe5-4dd1-8191-8045021d6411
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Uitvoerindeling{#output-format}

{{eol}}

Richtlijnen voor het opgeven van de uitvoerindeling.

* Elke metrische naam of afmetingsnaam moet met een percentageteken (%) beginnen en eindigen.

   * %XYZ% geeft het element van afmeting XYZ aan dat overeenkomt met het element van Niveau. Er wordt een fout gegenereerd als dimensie XYZ niet een-op-een of een-op-een-op-een is met Niveau.
   * %=XYZ% geeft de waarde aan van de metrische of metrische formule XYZ voor het opgegeven element van Niveau.

* Voor namen van Dimension die twee woorden of langer zijn, is geen onderstrepingsteken nodig.
* Voor metrische namen die twee woorden of langer zijn, zijn onderstrepingstekens vereist.

>[!NOTE]
>
>Als u de Ctrl-toets ingedrukt houdt en met de rechtermuisknop klikt in het dialoogvenster [!DNL Output Format] veld, en [!DNL Insert menu] wordt weergegeven. Dit menu bevat een lijst met speciale tekens (bijvoorbeeld Tab) die vaak als scheidingstekens worden gebruikt.

Als u de gegevens van de zittingsduur voor uw segment wilt uitvoeren, moet u nieuwe metrisch tot stand brengen die op metrische waarde van de Duur van de Zitting wordt gebaseerd. De nieuwe metrisch, die slechts voor gebruik met [!DNL Output Format] in het veld voor segmentexport kunnen Microsoft Excel sessies van minder dan een uur correct interpreteren. Als u een nieuwe metrische sessieduur wilt maken, opent u de [!DNL Session Duration.metric] bestand (van de [!DNL Profile Manager]) en voeg een hekje (#) in het ftime koord in: [!DNL ftime = string: %#H:%M:%S]

Het hekje zorgt ervoor dat een voorloopteken &quot;0&quot; wordt toegevoegd aan sessieduur van minder dan 1 uur. Dientengevolge, interpreteert Excel 0:53:21 als 53 minuten en 21 seconden. Sla de nieuwe metrische gegevens op onder een andere naam en upload deze naar het juiste profiel voor anderen, zodat u deze kunt gebruiken door met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom en klikken **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

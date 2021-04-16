---
description: Richtlijnen voor het opgeven van de uitvoerindeling.
title: Uitvoerindeling
uuid: 12086f14-bad1-4d27-82fb-533e877d0a04
exl-id: e695eaf4-ebe5-4dd1-8191-8045021d6411
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Uitvoerindeling{#output-format}

Richtlijnen voor het opgeven van de uitvoerindeling.

* Elke metrische naam of afmetingsnaam moet met een percentageteken (%) beginnen en eindigen.

   * %XYZ% geeft het element van afmeting XYZ aan dat overeenkomt met het element van Niveau. Er wordt een fout gegenereerd als dimensie XYZ niet een-op-een of een-op-een-op-een is met Niveau.
   * %=XYZ% geeft de waarde aan van de metrische of metrische formule XYZ voor het opgegeven element van Niveau.

* Voor namen van Dimension die twee woorden of langer zijn, is geen onderstrepingsteken nodig.
* Voor metrische namen die twee woorden of langer zijn, zijn onderstrepingstekens vereist.

>[!NOTE]
>
>Als u de Ctrl-toets ingedrukt houdt en met de rechtermuisknop klikt in het veld [!DNL Output Format], wordt een [!DNL Insert menu] weergegeven. Dit menu bevat een lijst met speciale tekens (bijvoorbeeld Tab) die vaak als scheidingstekens worden gebruikt.

Als u de gegevens van de zittingsduur voor uw segment wilt uitvoeren, moet u nieuwe metrisch tot stand brengen die op metrische waarde van de Duur van de Zitting wordt gebaseerd. De nieuwe metrische waarde, die slechts voor gebruik met [!DNL Output Format] gebied van segmentuitvoer is, laat Microsoft Excel toe om zittingen correct te interpreteren die minder dan één uur duren. Als u een nieuwe metrische waarde voor de sessieduur wilt maken, opent u het [!DNL Session Duration.metric]-bestand (van [!DNL Profile Manager]) en voegt u een hekje (#) in de ftime-tekenreeks in: [!DNL ftime = string: %#H:%M:%S]

Het hekje zorgt ervoor dat een voorloopteken &quot;0&quot; wordt toegevoegd aan sessieduur van minder dan 1 uur. Het resultaat is dat Excel 0:53:21 interpreteert als 53 minuten en 21 seconden. Sla de nieuwe metrische gegevens op onder een andere naam en upload deze naar het juiste profiel voor anderen. Klik hiertoe met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

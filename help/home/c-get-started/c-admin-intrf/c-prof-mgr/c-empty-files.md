---
description: Als u geen toestemming hebt om bestanden uit een profiel te verwijderen of als u een bestand niet permanent wilt verwijderen, kunt u lege (nulbyte) bestanden gebruiken om bestanden te verbergen.
title: Een bestand verbergen door het te ledigen (nulbyte)
uuid: 82c1a5c9-1bbb-41c7-bee7-704f0a9ef87d
exl-id: d5841fb5-afae-4352-aded-01b0b2eb9f85
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Een bestand verbergen door het te ledigen (nulbyte){#hide-a-file-by-emptying-it-zero-byte}

{{eol}}

Als u geen toestemming hebt om bestanden uit een profiel te verwijderen of als u een bestand niet permanent wilt verwijderen, kunt u lege (nulbyte) bestanden gebruiken om bestanden te verbergen.

In de [!DNL Profile Manager], geeft een afbreekstreepje (-) in plaats van een vinkje in een kolom een bestand aan dat uit nul bytes bestaat.

![](assets/vis_ProfMgr_Zero-byte.png)

In tegenstelling tot andere methoden voor het verbergen van bestanden (zoals [!DNL order.txt], de parameter Show en de parameter Hidden), behandelt Data Workbench bestanden met byte nul als niet-bestaand. Bijvoorbeeld, als u nul-byte een afmeting die in een visualisatie of een metrische definitie is gebruikt, veroorzaakt de Data Workbench een fout voor die visualisatie of metrisch, respectievelijk.

Deze functionaliteit is om verschillende redenen nuttig, bijvoorbeeld wanneer u het volgende wilt doen:

* **Een bestand onbruikbaar maken** in Data Workbench zonder dat u de profielmachtigingen nodig hebt om het bestand te verwijderen.
* **Een metrische waarde, dimensie of filter verplaatsen** naar een andere locatie zonder dat u de profielmachtigingen nodig hebt om het bestand van de oorspronkelijke locatie te verwijderen.
* **Menuopdrachten verbergen.** De [!DNL Base] profiel heeft [!DNL Metric Legend] in de [!DNL Metric.vw] bestand. Stel dat uw bedrijf drie metrische legenda heeft gemaakt die u wilt weergeven in het submenu Legenda toevoegen > Metrisch. U kunt de [!DNL Base] profiel [!DNL Metric.vw] zodat alleen het nieuwe submenu en drie nieuwe metrische legenda worden weergegeven.

**Een bestand verbergen**

1. In de [!DNL Profile Manager]Open de benodigde mappen en submappen om te zoeken naar het bestand dat u op nul-byte wilt instellen.
1. Klik met de rechtermuisknop op het vinkje naast de naam van het bestand en klik op **[!UICONTROL Make Local]**.
1. Open het lokale bestand en verwijder de inhoud ervan.
1. Sla het bestand op en sluit het.

---
description: Met een padbrowser kunt u de volgorde analyseren waarin de elementen van een bepaalde dimensie zijn benaderd.
title: Padbrowsers
uuid: 548091dc-935f-41ac-b67c-39080988f1ea
exl-id: 563cf0e3-39d7-49b7-b808-b0233169fb1a
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# Padbrowsers{#path-browsers}

Met een padbrowser kunt u de volgorde analyseren waarin de elementen van een bepaalde dimensie zijn benaderd.

U maakt een padbrowser door een element van een dimensie naar een browserweergave met een leeg pad te slepen. Het element dat u naar de padbrowser sleept, wordt de basis van de padbrowser. In de padbrowser worden paden weergegeven die door de hoofdmap lopen, zodat u de reeks elementen kunt zien die voor en na de hoofdmap zijn geopend.

In de volgende padbrowser wordt de volgorde van films weergegeven die de kijkers hebben beoordeeld voor en na het classificeren van de film *De filmclip*, die de basis vormt van de padbrowser. Elke filmnaam is een element van de afmetingen van de Film, die in een dataset wordt bepaald die uit filmgegevens bestaat die filmnamen en kijkers&#39; classificaties van die films omvat.

![](assets/vis_PathBrowser_Movies.png)

U kunt wegbrowsers tot stand brengen om de opeenvolging te tonen waarin de elementen van om het even welke afmeting in uw dataset werden betreden. Als u bijvoorbeeld met websitegegevens werkt, kunt u een padbrowser maken met de volgorde van websitepagina&#39;s die voor en na de hoofdmap zijn geopend voor elke sessie waarin de hoofdmap is weergegeven of voor elke sitebezoeker die de hoofdmap heeft weergegeven.

![](assets/vis_PathBrowser_Pages.png)

Elke wegbrowser heeft een bijbehorende basisafmeting, groepsafmeting, niveauafmeting, en metrisch, die sleutels verstrekken om de gegevens te interpreteren die in wegbrowser worden getoond.

* **Basisafmetingen:** wanneer u een basiselement naar de padbrowser sleept, sleept u een element van de basisdimensie en zet u het neer. Alle andere elementen die in de paden voorkomen, zijn elementen van de basisdimensie. U kunt de basisdimensie wijzigen door een element van een andere dimensie naar de padbrowser te slepen.
* **De dimensie van het niveau:** Elke dimensie in uw dataset heeft een bijbehorende niveaudimensie (die ook als ouder wordt bedoeld). De niveaudimensie voor uw wegbrowser zou het zelfde moeten zijn als de niveaudimensie (of ouder) voor de de basisdimensie van uw wegbrowser. De niveaudimensie van een padbrowser is belangrijk om twee belangrijke redenen:

   * Als u een pad volgt van het ene element van de basisdimensie naar het volgende, gaat u van het ene element van de niveaudimensie naar het volgende. Stel dat u een padbrowser hebt gemaakt waarin pagina&#39;s van een website worden weergegeven. Elke pagina is een element van de pagina-afmeting en de niveauafmeting voor Pagina is Paginaweergave. Als u van de ene pagina naar de andere gaat, gaat u van de ene paginaweergave naar de andere.
   * Wanneer u een pad met basisdimensie-elementen selecteert in een padbrowser, selecteert u gegevens voor de corresponderende elementen van de niveaudimensie. De selectie bevat altijd de elementen van de niveaudimensie die betrekking hebben op de hoofdmap en wordt verfijnd door meer elementen aan het pad toe te voegen. Als u bijvoorbeeld een pad met pagina&#39;s selecteert, zoals Basis > A > B, selecteert u gegevens voor de paginaweergaven die zijn gekoppeld aan de hoofdpagina waarop de volgende pagina A staat en de volgende pagina B.

      Zie [Paden selecteren](../../../../home/c-get-started/c-analysis-vis/c-path-browsers/t-sel-paths.md#task-bf44d08c71954ef2adec4b82f840adeb) voor informatie over het selecteren van een pad in een padbrowser. Zie [Selecties maken in visualisaties](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746) voor informatie over selecties.
   >[!NOTE]
   >
   >De padbrowser negeert de elementen van de niveaudimensie zonder de bijbehorende basisdimensie-elementen. Deze situatie kan zich voordoen wanneer u een padbrowser maakt op basis van een proceskaart. Zie [Padbrowsers maken](../../../../home/c-get-started/c-analysis-vis/c-path-browsers/c-create-path-browsers.md#concept-e120de6a740d4b6f98dda9e2b638f6ff).

* **Groepsdimensie:** de groepsdimensie bepaalt hoe de elementen van de niveaudimensie worden gegroepeerd om de paden van een padbrowser te vormen. Specifiek, kunnen de elementen van de niveaudimensie verbonden aan één enkele weg in wegbrowser niet meer dan één element van een groepsdimensie overspannen.

   Om dit te begrijpen, overweeg een voorbeeld gebruikend Webgegevens. Stel dat de basis-, niveau- en groepsafmetingen voor de padbrowser respectievelijk Pagina, Paginaweergave en Sessie zijn. Eén pad in uw padbrowser toont de paginareeks A > B > C. De groepsdimensie (Sessie) geeft aan dat de paginaweergaven (elementen van de afmetingen Paginaweergave) die aan de paginareeks A > B > C zijn gekoppeld, tijdens elke sessie zijn opgetreden. Het is belangrijk om op te merken dat er meerdere sessies kunnen zijn waarin paginareeksen A > B > C werden weergegeven. Daarom vertegenwoordigt het pad met paginareeks A > B > C alle afzonderlijke sessies waarin de paginaweergaven voor die reeks plaatsvonden.

* **Metrisch**: De dikte van het pad dat naar een bepaald element leidt, is evenredig met de waarde van de metrische waarde voor dat element. Hogere paden geven hogere metrische waarden aan dan dunne paden.

Het label in de linkerbovenhoek van de padbrowser geeft de basis- en groepsafmetingen aan die in de visualisatie worden weergegeven. De naam van de niveaudimensie is niet zichtbaar in de browser van de weg visualisatie. Het label heeft de vorm &quot;Reeks van *naam van de basisdimensie*+s voor elke *naam van de groepsdimensie*.&quot; Bijvoorbeeld, vertelt de etiketReeks van Films voor elke Gebruiker dat de basisafmeting Film is en de groepsafmeting Gebruiker is.

![](assets/vis_PathBrowser_Movies.png)

Door met de rechtermuisknop op een element in de padbrowser te klikken, kunt u de naam zien van de metrische waarde die is gekoppeld aan de padbrowser en de waarde ervan voor dat element.

![](assets/vis_PathBrowser_RightClick.png)

>[!NOTE]
>
>U kunt de standaardafmetingen en de metrische waarde voor een padbrowser wijzigen. Zie [Browsers van paden configureren](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-path-brwsr.md#task-bbb3ddaa140a414f984b697c2b8202a3) voor instructies voor het configureren van de visualisatie van een padbrowser.

---
description: Een wegbrowser laat u toe om de opeenvolging te analyseren waarin de elementen van een bepaalde dimensie werden betreden.
solution: Analytics
title: Padbrowsers
topic: Data workbench
uuid: 548091dc-935f-41ac-b67c-39080988f1ea
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Padbrowsers{#path-browsers}

Een wegbrowser laat u toe om de opeenvolging te analyseren waarin de elementen van een bepaalde dimensie werden betreden.

U creeert wegbrowser door een element van een afmeting te slepen en te laten vallen op een lege wegbrowser visualisatie. Het element dat u sleept en op wegbrowser laat vallen wordt de wortel van wegbrowser. De weg browser toont wegen die door de wortel overgaan, toelatend u om de opeenvolging van elementen te zien die vóór en na de wortel werden betreden.

De volgende wegbrowser toont de opeenvolging van films die de kijkers vóór en na classificatie van de film *de Afbeelder* schatten, die de wortel van wegbrowser is. Elke filmnaam is een element van de afmeting van de Film, die in een dataset wordt bepaald die uit filmgegevens bestaat die film&#39; namen en kijkers&#39; classificaties van die films omvat.

![](assets/vis_PathBrowser_Movies.png)

U kunt wegbrowsers tot stand brengen om de opeenvolging te tonen waarin de elementen van om het even welke afmeting in uw dataset werden betreden. Bijvoorbeeld, als u met websitegegevens werkt, kunt u wegbrowser tot stand brengen die de opeenvolging van websitepagina&#39;s toont die vóór en na de wortel voor elke zitting werden betreden waarin de wortel of voor elke plaatsbezoeker werd bekeken die de wortel bekeken.

![](assets/vis_PathBrowser_Pages.png)

Elke wegbrowser heeft een bijbehorende basisafmeting, groepsafmeting, niveauafmeting, en metrisch, die sleutels verstrekken om de gegevens te interpreteren die in wegbrowser worden getoond.

* **Basisdimensie:** Wanneer u sleept en een wortelelement op wegbrowser laat vallen, sleept u en laat vallen een element van de basisdimensie. Alle andere elementen die in de wegen verschijnen zijn elementen van de basisdimensie. U kunt de basisafmeting veranderen door een element van een andere afmeting op wegbrowser te slepen en te laten vallen.
* **Niveaudimensie:** Elke dimensie in uw dataset heeft een bijbehorende niveaudimensie (die ook als ouder wordt bedoeld). De niveaudimensie voor uw wegbrowser zou het zelfde als de niveaudimensie (of ouder) voor de basisafmeting van uw wegbrowser moeten zijn. De het niveaudimensie van wegbrowser is belangrijk om twee belangrijke redenen:

   * Aangezien u een weg van één element van de basisdimensie aan volgende volgt, beweegt u zich van één element van de niveaudimensie aan volgende. Bijvoorbeeld, veronderstel dat u wegbrowser hebt gecreeerd die pagina&#39;s van een website toont. Elke pagina is een element van de dimensie van de Pagina, en de niveaudimensie voor Pagina is de Mening van de Pagina. Aangezien u zich van één pagina aan de volgende beweegt, beweegt u zich van één paginamening aan volgende.
   * Wanneer u een weg van de elementen van de basisafmeting binnen wegbrowser selecteert, selecteert u gegevens voor de overeenkomstige elementen van de niveauafmeting. De selectie omvat altijd de elementen van de niveaudimensie die op de wortel betrekking hebben, en het wordt verfijnd door meer elementen aan de weg toe te voegen. Bijvoorbeeld, wanneer u een weg van pagina&#39;s, zoals wortel > A > B selecteert, selecteert u gegevens voor de paginameningen verbonden aan de wortel waar de volgende pagina A is en de volgende pagina B is.

      Voor informatie over het selecteren van een weg in wegbrowser, zie het [Selecteren van Wegen](../../../../home/c-get-started/c-analysis-vis/c-path-browsers/t-sel-paths.md#task-bf44d08c71954ef2adec4b82f840adeb). Voor informatie over selecties, zie het [Maken Selecties in Visualisaties](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746).
   >[!NOTE]
   >
   >De wegbrowser negeert de elementen van de niveaudimensie zonder bijbehorende elementen van de basisafmeting. Deze situatie kan voorkomen wanneer u wegbrowser van een proceskaart creeert. Zie [het Creëren van Browsers](../../../../home/c-get-started/c-analysis-vis/c-path-browsers/c-create-path-browsers.md#concept-e120de6a740d4b6f98dda9e2b638f6ff)van de Weg.

* **Groepsdimensie:** De groepsdimensie bepaalt hoe de elementen van de niveaudimensie worden gegroepeerd om de wegen van wegbrowser te vormen. Specifiek, kunnen de elementen van de niveaudimensie verbonden aan één enkele weg in wegbrowser niet meer dan één element van een groepsdimensie overspannen.

   Om dit te begrijpen, overweeg een voorbeeld gebruikend Webgegevens. Veronderstel dat de basis, het niveau, en de groepsdimensies voor uw wegbrowser Pagina, de Mening van de Pagina, en Zitting, respectievelijk zijn. Één weg in uw wegbrowser toont de paginaopeenvolging A > B > C. De groepsafmeting (Zitting) vertelt u dat de paginameningen (elementen van de afmeting van de Mening van de Pagina) verbonden aan de paginaopeenvolging A > B > C tijdens om het even welke enige zitting voorkwam. Het is belangrijk om op te merken dat er veelvoudige zittingen zouden kunnen zijn waarin er paginameningen voor de paginaopeenvolging A > B > C. waren. Daarom vertegenwoordigt de weg die de paginasequentie A > B > C toont alle individuele zittingen waarin de paginameningen voor die opeenvolging voorkwamen.

* **Metrisch**: De dikte van de weg die tot een bepaald element leidt is proportioneel aan de waarde van metrisch voor dat element. De dikkere wegen wijzen op grotere metrische waarden dan dunner wegen.

Het etiket in de hoogste linkerhoek van wegbrowser noemt de basis en groepsafmetingen die in de visualisatie worden vertegenwoordigd. De naam van de niveaudimensie is niet zichtbaar in de wegbrowser visualisatie. Het etiket neemt de vorm &quot;Opeenvolging van naam *+s van de* basisafmeting voor elke naam *van de* groepsafmeting.&quot; Bijvoorbeeld, vertelt de etiketopeenvolging van Films voor elke Gebruiker u dat de basisafmeting Film is en de groepsafmeting Gebruiker is.

![](assets/vis_PathBrowser_Movies.png)

Door om het even welk element in wegbrowser met de rechtermuisknop aan te klikken, kunt u de naam van metrisch zien verbonden aan wegbrowser en zijn waarde voor dat element.

![](assets/vis_PathBrowser_RightClick.png)

>[!NOTE]
>
>U kunt de standaardafmetingen en metrisch voor wegbrowser veranderen. Voor instructies om een wegbrowser visualisatie te vormen, zie het [Vormen Browsers](../../../../home/c-get-started/c-intf-anlys-ftrs/t-config-path-brwsr.md#task-bbb3ddaa140a414f984b697c2b8202a3)van de Weg.


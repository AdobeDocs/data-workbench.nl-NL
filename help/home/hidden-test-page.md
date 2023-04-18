---
title: Verborgen testpagina
description: Deze pagina is verborgen in de zoekopdracht en in de inhoudsopgave
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
source-git-commit: fd815415e55e72ab01a1beee9b7ebed0432eded9
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 0%

---

# Verborgen testpagina

## Badges

Een badge is een gekleurd label dat wordt gebruikt als inhoudsindicator. U kunt bijvoorbeeld een badge toevoegen om een artikel te markeren als _Beta_ of een sectie als _Premium_. U kunt de kleur van een badge wijzigen en een URL en knopinfo koppelen.

[!BADGE Badge-voorbeeld]

Er zijn twee typen badges, elk met een verschillende syntaxis:

* **Metagegevens** - Geeft het symbool boven aan een pagina weer
* **Inline** - Geeft de badge weer waar de syntaxis zich bevindt

![badge-voorbeelden](assets/badge-examples.png "Badge-voorbeelden"){width="200" zoomable="yes"}

### Metagegevensbadges

Als u een badgesyntaxis toevoegt in metagegevens, wordt een symbool boven de paginatitel (H1) in het artikel geplaatst.

U kunt bijvoorbeeld badges benoemen met _badge1_ of _badge2_. Of u kunt creatiever zijn (zolang de naam begint met _badge_).

Voorbeelden van metagegevens:

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium:** In dit voorbeeld wordt een Premium-badge met een URL en knopinfo weergegeven.

* **badgeExam:** In dit voorbeeld wordt een donkere badge met een examen-id-nummer weergegeven.

#### Inline badges

Geef de badge-informatie op een eigen regel of in een kop, tabel of ander pagina-element op.

Hier volgt de syntaxis voor een inline badge met een bètalabel, blauwe kleur, URL en knopinfo:

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### Beschikbare badkleuren

Badges gebruiken kleuren die zijn gedefinieerd in Adobe-spectrum:

| Type | Badge |
|---|---|
| Informatief (standaard) | [!BADGE Beta]{type=Informative url="https://www.example.com"} |
| Positief | [!BADGE Nieuwe functie]{type=Positive url="https://www.example.com" tooltip="Ga naar voorbeeld.com"} |
| Negatief | [!BADGE Stopzetten]{type=negative tooltip="Deze functie is nu levenseinde"} |
| Neutraal | [!BADGE Misschien]{type=Neutral tooltip="Een rider viel van het paard..."} |
| Waarschuwing | [!BADGE Opgelet]{type=Caution tooltip="Gele status"} |

Syntaxisvoorbeelden

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### Voorschriften voor badges

* Er zijn slechts twee badges toegestaan in metagegevens. Deze regel is configureerbaar, dus laat ons weten of u een uitzondering nodig hebt.
* Alleen het badge-label is vereist. De `type`, `url`, en `tooltip` parameters zijn optioneel. De `type` bepaalt de kleur. De `url` Met deze parameter kunnen gebruikers op de badge klikken om een artikel of pagina te openen. De `tooltip` De parameter toont de tooltip tekst op mouseover.
* Een badge toevoegen aan de `TOC.md` het bestand geeft de badge op elk artikel in de handleiding weer. Als u een URL opgeeft om naar een artikel te gaan, moet u een hoofdkoppeling gebruiken (bijvoorbeeld `/help/guide/article.md`) geen relatieve koppeling (bijvoorbeeld `article.md`) voor artikelen in verschillende mappen.
* Een badge toevoegen aan `metadata-new.md` geeft de badge op elk artikel in een repo weer.
* Voor meta-gegevensbadges, zorg ervoor dat alle waarden in citaten worden verpakt. Voor inline badges moet u ervoor zorgen dat `url` en `tooltip` worden tussen aanhalingstekens geplaatst.
* Geldige tekstwaarden zijn *Informatief* (standaard, blauw), *Positief* (groen), *Negatief* (rood), *Neutraal* (donkergrijs), en *Waarschuwing* (geel).
* Badge-labels worden gelokaliseerd.
* Als er meerdere metagegevensbadges zijn opgegeven, worden badges in alfabetische volgorde weergegeven op basis van de badge-naam, zoals `badge1:` of `badgeWeb`.
* Als u de URL op een nieuw tabblad wilt openen, gebruikt u deze syntaxis:

   ```
   [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
   ```

   Gerenderd:

   [!BADGE Openen op nieuw tabblad]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Adobe.com openen op nieuw tabblad"}

## Tekstmarkering

Het Workfront-team heeft gevraagd gele markering te kunnen gebruiken om de voorvertoning van aanstaande functies aan te geven. Zo werkt het.

Voorbeeld:

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

Gerenderd:

Deze hele alinea mag NIET worden gemarkeerd. <span class="preview"> Dit woord is **vet** in een gemarkeerde zin.</span> Dit is slechts de laatste zin.

Als algemene regel geldt dat `<span class="preview">` om een alinea of tekst in een alinea te markeren en te gebruiken `<div class="preview">` voor meerdere alinea&#39;s en componenten.

## Syntaxis markeren voor codeblokken

Experience League ondersteunt syntaxismarkering voor codeblokken. Zorg ervoor dat u een taal opgeeft, zoals `java` na de openingsreeks tikken om ervoor te zorgen dat de syntaxis behoorlijk wordt benadrukt. Voor een lijst met geldige talen raadpleegt u [https://prismjs.com](https://prismjs.com/#supported-languages). Als er talen ontbreken, registreert u een jira-ticket.

### Regelnummering in codeblokken

Toevoegen `{line-numbers="true"}` na de taal om regelnummering in te schakelen.

Voorbeeld met regelnummers (&grave;&grave;&grave;`html {line-numbers="true"}`):

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**Nummering beginnen op regel _**

Toevoegen `start-number="n"` na de syntaxis van het regelnummer om de nummering te laten beginnen op een ander nummer dan 1.

Voorbeeld met nieuwe beginregel (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`):

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### Regelmarkering in codeblokken

Toevoegen `highlight="n"` na de syntaxis van het regelnummer om rijen binnen een codeblok te markeren. Opgeven `11-13, 16` worden de lijnen 11 tot en met 13 en 16 benadrukt.

Voorbeeld met lijnmarkering (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`):

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

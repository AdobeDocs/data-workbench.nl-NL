---
description: Reguliere expressies worden gebruikt voor alle zoekvelden in de werkbank met gegevens, inclusief de deelvensters met query-entiteiten.
title: Reguliere expressies
uuid: f3a0119d-6fac-4f63-8dca-4db32d2a737a
exl-id: 75841a70-e78a-429b-b00d-ac107b7a87aa
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1418'
ht-degree: 1%

---

# Gewone uitdrukkingen{#regular-expressions}

Reguliere expressies worden gebruikt voor alle zoekvelden in de werkbank met gegevens, inclusief de deelvensters met query-entiteiten.

* [Informatie over reguliere expressies](../../home/c-dataset-const-proc/c-reg-exp.md#section-cc9dc7293bb04fc0b41fe8acdee708f0)
* [Terminologie voor reguliere expressies](../../home/c-dataset-const-proc/c-reg-exp.md#section-80b0d54f731e448391532ab3eb3c525c)
* [Letterlijke overeenkomsten](../../home/c-dataset-const-proc/c-reg-exp.md#section-ec4497e3160c47ba9b828d939761b3e0)
* [Metatekens gebruiken](../../home/c-dataset-const-proc/c-reg-exp.md#section-e29a804336304ea1ba33d40d60139aa2)
* [Patroonextractie](../../home/c-dataset-const-proc/c-reg-exp.md#section-4389779653b64f6cb7c47615b25c1a79)

## Informatie over reguliere expressies {#section-cc9dc7293bb04fc0b41fe8acdee708f0}

Een reguliere expressie is een tekstpatroon, bestaande uit een combinatie van alfanumerieke tekens en speciale tekens, bekend als metatekens, die patronen zoeken en subtekenreeksen uit tekst extraheren. Reguliere expressies worden op grote schaal gebruikt in computerprogrammering en maken integraal deel uit van talen zoals Perl.

Om complexe tekenreekspatronen te identificeren en te extraheren, gebruikt de server van de gegevenswerkbank regelmatige uitdrukkingen in sommige transformaties en voorwaarden. Hierna volgt een korte handleiding voor reguliere expressies.

Deze bijlage is geen uitgebreide inleiding op reguliere expressies. Een bijzonder goede verwijzing is de publicatie van O&#39;Reilly *Mastering Regular Expressions, 2nd Edition* door Jeffrey E. F. Friedl.

## Terminologie voor reguliere expressies {#section-80b0d54f731e448391532ab3eb3c525c}

| Term | Definitie |
|---|---|
| Letterlijk | Een letterlijk teken is een teken dat we in een reguliere expressie gebruiken om een bepaalde reeks tekens te zoeken. Bijvoorbeeld, om product in [!DNL shop/products.html] te vinden, is het koordproduct letterlijk, of wat wij letterlijk zoeken in het koord. |
| Metateken | Een metateken is een speciaal teken dat een unieke interpretatie heeft in de context van reguliere expressies. De punt (.) is een metateken dat wordt gebruikt om aan om het even welk karakter aan te passen. |
| Escape-reeks | Een escapereeks is gewoon een manier om de reguliere-expressieengine te vertellen dat we een van de metatekens als letterlijk teken willen gebruiken. Escape-reeksen beginnen altijd met de backslash (`\`). Door de backslash (ook een metateken) vóór een metateken te plaatsen, interpreteert de engine voor de reguliere expressie het metateken zonder escape als letterlijk. Bijvoorbeeld, als u de metatekerperiode (`.`) wilt aanpassen, moet u een vluchtopeenvolging gebruiken. Nochtans, om één van de periodes in koord 168.196.0.11 aan te passen, kon u de regelmatige uitdrukking gebruiken die uit backslash en een periode (`\.`) bestaat. |
| Patroon | Dit is een korte terminologie voor de reguliere expressie. In wezen is een reguliere expressie een patroon dat u probeert af te stemmen op de doeltekenreeks. |
| Doeltekenreeks | Deze term verwijst naar de tekenreeks waarin we zoeken om het gewenste patroon te vinden. |

## Informatie over letterlijke overeenkomsten {#section-ec4497e3160c47ba9b828d939761b3e0}

Letterlijke overeenkomst neemt een letterlijke tekenreeks zonder escape-tekens en zoekt in de doeltekenreeks om te zien of het een subtekenreeks van de doeltekenreeks is.

In dit voorbeeld ziet u hoe letterlijke overeenkomst werkt. Overweeg een situatie waarin gegevens worden verzameld van websiteverkeer en het veld cs(reference) de volgende waarde bevat:

`http://www.abc.com/adventurenews/today.html?ad=123AZ45`

Om te bepalen of de verwijzer iemand vertegenwoordigt die op één van de advertenties klikte, moet u zien of de verwijzer de koordadvertentie bevat. U kon de letterlijke koordadvertentie eenvoudig gebruiken om het doelkoord te zoeken en te bepalen of een reclame werd gebruikt om het verkeer aan de plaats te leiden. Hoewel dit met de doeltekenreeks zou overeenkomen, zou deze op twee locaties overeenkomen en dus dubbelzinnig zijn en tot onjuiste positieven kunnen leiden.

De volgende URL bevat de tekenreeksadvertentie op twee verschillende plaatsen:

`http://www.abc.com/ad vertnews/today.html?ad =123AZ45`

Als u dus probeert vast te stellen welke sessies zijn gestart als gevolg van een bepaalde advertentiecampagne, is het duidelijk dat het gebruik van de letterlijke advertentie als reguliere expressie niet voldoende is. Als u de letterlijke waarde wijzigt in &quot;ad=&quot;, voorkomt u deze dubbelzinnigheid en resulteert de expressie in slechts één overeenkomst. Zelfs dit is misschien niet voldoende om te garanderen dat de verwijzende partij deel uitmaakte van de advertentiecampagne. Overweeg de volgende referentie:

`http://www.xyz.com/hello.html?pad=something`

U hebt geen controle over de URL&#39;s die anderen gebruiken om koppelingen naar de site te maken. Letterlijke overeenkomsten zijn te eenvoudig om sessies te zoeken die zijn gestart als gevolg van de advertentiecampagne. In de volgende sectie wordt besproken hoe u metatekens kunt gebruiken voor flexibelere en krachtigere overeenkomsten.

## Metatekens gebruiken {#section-e29a804336304ea1ba33d40d60139aa2}

Een metateken is een speciaal teken in een programma of gegevensveld dat informatie over andere tekens bevat.

| metateken | beschrijving |
|---|---|
| . (punt) | Komt overeen met één teken, bijvoorbeeld: `re:x.z` komt overeen met &quot;xyz&quot; of &quot;xxz&quot;. |
| * (ster) | Komt overeen met een of meer tekens, bijvoorbeeld: `re:Z*` komt overeen met &quot;ZZZ&quot;. |
| ? (jokerteken) | Komt overeen met 0 of 1 van de vorige expressie om minimale overeenkomsten af te dwingen, bijvoorbeeld: `xy?z` komt overeen met &quot;xy&quot; en &quot;xyz&quot;. |

Aanvullende reguliere expressies kunnen ook worden gebruikt om complexere zoekreeksen te maken.

**Lijsten, bereiken en OF**

Met letterlijke overeenkomsten kunt u één tekenreeks zoeken, maar met vierkante haken, streepjes en pijpen kunt u een lijst definiëren van de items die u wilt zoeken in de doeltekenreeks.

<table id="table_18B86955EC3748079E7C176273ADE92B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor dit metateken... </th> 
   <th colname="col2" class="entry"> De reguliere-expressieprocessor zal.. </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Vierkante haken ([ ]) </td> 
   <td colname="col2"> Pas een van de tekens binnen de vierkante haken aan met één tekenpositie. [AB] is bijvoorbeeld een instructie die ofwel overeenkomt met de letter A of de letter B, en [0123456789] staat voor elk teken in het bereik 0 tot en met 9. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Streepje (-) </td> 
   <td colname="col2"> <p>Overeenkomst met een tekenbereik. In plaats van [0123456789] te schrijven, zouden we dus gewoon [0-9] kunnen schrijven. </p> <p> Dit kan worden uitgebreid tot bereiken van tekens en meerdere bereiken binnen één set haakjes. [0-9A-C] komt bijvoorbeeld overeen met de tekens 0 tot en met 9 en A tot en met C. </p> <p> <p>Opmerking:  Als u op een streepje (-) wilt testen als letterlijk teken binnen de vierkante haakjes, moet het eerste of laatste streepje staan. [-0-9] test bijvoorbeeld op - en 0 tot en met 9. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pijp (|) </td> 
   <td colname="col2"> Kies een van de twee opties voor een bepaalde doeltekenreeks. Zo komt b|nat bijvoorbeeld overeen met bat of nat. </td> 
  </tr> 
 </tbody> 
</table>

Neem de volgende voorbeelden:

| Patroon | String | Overeenkomst |
|---|---|---|
| Win9`[58]` | OS=Win95 | Win95 |
| Win95 | 8 | OS=Win98 | Win98 |
| `[0-9]` | Mozilla/3.0 | 1 |
| Les`[A-Z]` | Les | Geen gelijke omdat laag-gecaased a niet in de waaier van bovenkast A door Z is. |

**Negatie**

Negatie is een manier om te zeggen dat je iets wilt zoeken behalve de opgegeven tekens. Het metateken van de negatie, de omtrek of het inlasteken (`^`), wordt gebruikt als eerste karakter binnen steunen om te zeggen dat u de gelijke om het even wat behalve de resterende karakters in de steunen zou willen zijn. Als u bijvoorbeeld een willekeurig teken maar een puntkomma (`;`) wilt afstemmen, schrijft u

[`^;`]

Dit komt overeen met elk willekeurig teken behalve de puntkomma.

**Plaatsing**

Om een gelijke aan het begin of eind van een doelkoord te dwingen, wordt één van twee metatekens gebruikt.

| Voor dit metateken... | De reguliere-expressieprocessor zal.. |
|---|---|
| Circumflex of Caret (`^`) | Komt overeen met het begin van de tekenreeks. Bijvoorbeeld, ^`[Tt]`hij zou het doelkoord &quot;het Begin&quot;aanpassen maar zou niet &quot;dit is het begin&quot;aanpassen.&quot; |
| Dollarteken (`$`) | Komt overeen met het einde van de tekenreeks. `[Ee]`nd$ komt bijvoorbeeld overeen met &quot;This is the end&quot;, maar komt niet overeen met &quot;The end is a special time&quot;. |

>[!NOTE]
>
>Wanneer de reguliere expressie ^ aan het begin en $ aan het einde bevat, moet de gehele doeltekenreeks overeenkomen met de reguliere expressie.

**Alles afstemmen**

De punt (.) is een speciaal metateken dat overeenkomt met elk willekeurig teken in de doeltekenreeks. De reguliere expressie `^…$` komt bijvoorbeeld overeen met elke doeltekenreeks die precies drie tekens lang is. De reguliere expressie &quot;...&quot; komt overeen met elke doeltekenreeks die ten minste drie tekens bevat.

**Herhaalde patronen**

Met metatekens voor herhaling kunt u een patroon meerdere keren afstemmen.

<table id="table_6A14333D6C264A48ADF1EBBAF687CADD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor dit metateken... </th> 
   <th colname="col2" class="entry"> De reguliere-expressieprocessor zal.. </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Vraagteken (?) </td> 
   <td colname="col2"> Geen instanties of één instantie van het teken direct voorafgaand aan het metateken (?). Het patroongebied komt bijvoorbeeld overeen met rood en gelezen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sterretje (*) </td> 
   <td colname="col2"> Komt overeen met nul of meer exemplaren van het teken dat onmiddellijk voorafgaat aan het metateken (*). Het patroon [0-9]* komt bijvoorbeeld overeen met een willekeurig aantal tekens 0 tot en met 9 (een willekeurig geheel getal). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Plus (+) </td> 
   <td colname="col2"> Komt overeen met een of meer exemplaren van het voorgaande teken of bereik. Het patroon drie+ komt bijvoorbeeld overeen met drie, maar niet doorheen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> {n} </td> 
   <td colname="col2"> <p>Komt exact overeen met het normale teken of bereik. Het volgende patroon komt overeen met telefoonnummers in de Verenigde Staten: <code>[0-9]{3}-[0-9]{3}-[0-9]{4}</code>. </p> <p> Hoewel het geen optimaal patroon is, wordt bepaald of de doeltekenreeks de juiste indeling heeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> {n,m} </td> 
   <td colname="col2"> Pas het voorgaande teken minstens in keer en hoogstens m aan. For example, fo{1,2}d would match fod and food but not foood. </td> 
  </tr> 
 </tbody> 
</table>

## Patroonextractie {#section-4389779653b64f6cb7c47615b25c1a79}

Patroonaanpassing is slechts een deel van de kracht van reguliere expressies. Reguliere expressies bieden ook een mechanisme voor het extraheren van belangrijke delen van een doeltekenreeks. Dit wordt gedaan door het gebruiken van linker en juiste haakjes. Deze extracties worden doorgaans gebruikt als invoer in een ander proces en worden benaderd via het gebruik van *%position%*, waarbij de positie een geheel getal is dat verwijst naar het aantal ronde haakjes waarvoor een overeenkomende set ronde haakjes is gevonden.

Bekijk de volgende voorbeelden van patroonextractie:

<table id="table_BC8D471B966844049FFFCDEC0F183941"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Patroon </th> 
   <th colname="col2" class="entry"> String </th> 
   <th colname="col3" class="entry"> Overeenkomst </th> 
   <th colname="col4" class="entry"> Extractie </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Win(9[58]) </td> 
   <td colname="col2"> OS=Win95 </td> 
   <td colname="col3"> Win95 </td> 
   <td colname="col4"> %1% = 95 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> (Win)(95|8) </td> 
   <td colname="col2"> OS=Win98 </td> 
   <td colname="col3"> Win98 </td> 
   <td colname="col4"> <p>%1% = Win </p> <p> %2% = 98 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Mozilla/([0-9]).([0-9]) </td> 
   <td colname="col2"> Mozilla/3.0 </td> 
   <td colname="col3"> Mozilla/3.03 </td> 
   <td colname="col4"> <p>%1% = 3 </p> <p> %2% = 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Les ([A-Z]) </td> 
   <td colname="col2"> Les </td> 
   <td colname="col3"> Geen overeenkomst omdat lower-cased a niet binnen de waaier van bovenkast A door Z is </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

---
description: De regelmatige uitdrukkingen worden gebruikt over alle de onderzoeksgebieden van de gegevenswerkbank met inbegrip van de panelen van de vraagentiteit.
solution: Analytics
title: Regelmatige expressies
topic: Data workbench
uuid: f3a0119d-6fac-4f63-8dca-4db32d2a737a
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Regelmatige expressies{#regular-expressions}

De regelmatige uitdrukkingen worden gebruikt over alle de onderzoeksgebieden van de gegevenswerkbank met inbegrip van de panelen van de vraagentiteit.

* [Ongeveer Regelmatige Uitdrukkingen](../../home/c-dataset-const-proc/c-reg-exp.md#section-cc9dc7293bb04fc0b41fe8acdee708f0)
* [Regelmatige expressieterminologie](../../home/c-dataset-const-proc/c-reg-exp.md#section-80b0d54f731e448391532ab3eb3c525c)
* [Over Letterlijke overeenstemming](../../home/c-dataset-const-proc/c-reg-exp.md#section-ec4497e3160c47ba9b828d939761b3e0)
* [Metacharacters gebruiken](../../home/c-dataset-const-proc/c-reg-exp.md#section-e29a804336304ea1ba33d40d60139aa2)
* [Patroonextractie](../../home/c-dataset-const-proc/c-reg-exp.md#section-4389779653b64f6cb7c47615b25c1a79)

## Ongeveer Regelmatige Uitdrukkingen {#section-cc9dc7293bb04fc0b41fe8acdee708f0}

Een regelmatige uitdrukking is een tekstpatroon, dat uit een combinatie alfanumerieke karakters en speciale karakters bestaat die als metacharacters worden bekend, die van patronen de plaats bepaalt en substrings uit tekst haalt. De regelmatige uitdrukkingen worden wijd gebruikt in computerprogrammering en zijn een integraal deel van talen zoals Perl.

Om complexe koordpatronen te identificeren en te halen, gebruikt de server van de gegevenswerkbank regelmatige uitdrukkingen in enkele transformaties en voorwaarden. Wat volgt is een korte gids voor regelmatige uitdrukkingen.

Deze bijlage is geen uitvoerige inleiding aan regelmatige uitdrukkingen. Een bijzonder goede verwijzing is de O&#39;Reilly publicatie *Mastering Regular Expressions, 2e Uitgave* door Jeffrey E. F. Friedl.

## Regelmatige expressieterminologie {#section-80b0d54f731e448391532ab3eb3c525c}

| Termijn | Definitie |
|---|---|
| Letterlijk | Een letterlijk is een karakter dat wij in een regelmatige uitdrukking gebruiken om van een specifieke opeenvolging van karakters de plaats te bepalen. Bijvoorbeeld, om product in te vinden [!DNL shop/products.html], is het koordproduct letterlijk, of wat wij letterlijk zoeken in het koord. |
| Metacharacter | Een metacharacter is een speciaal karakter dat een unieke interpretatie in de context van regelmatige uitdrukkingen heeft. Bijvoorbeeld, de periode (.) is een metacharacter die wordt gebruikt om het even welk karakter aan te passen. |
| Escape Sequence | Een vluchtsequentie is simpelweg een manier om de reguliere expressiemotor te vertellen dat we een van de metacharacters als letterlijk zouden willen gebruiken. De opeenvolgingen van de ontsnapping beginnen altijd met het backslash karakter (`\`). Door backslash (die ook een metacharacter is) voor een metacharacter te plaatsen, interpreteert de regelmatige uitdrukkingsmotor de ontsnapte metacharacter als letterlijk. Bijvoorbeeld, als u de metacharacterperiode (`.`) wilt aanpassen, moet u een vluchtopeenvolging gebruiken. Nochtans, om één van de periodes in koord 168.196.0.11 aan te passen, kon u de regelmatige uitdrukking gebruiken die uit een backslash en een periode (`\.`) bestaat. |
| Patroon | Dit is korte terminologie voor de regelmatige uitdrukking. In wezen, is een regelmatige uitdrukking een patroon u probeert om tegen het doelkoord aan te passen. |
| Doel-tekenreeks | Deze termijn verwijst naar het koord wij binnen zoeken om van het gewenste patroon de plaats te bepalen. |

## Over Letterlijke overeenstemming {#section-ec4497e3160c47ba9b828d939761b3e0}

De letterlijke aanpassing neemt een letterlijke koord zonder enige vluchtkarakters en kijkt in het doelkoord om te zien of is het een substring van het doelkoord.

In dit voorbeeld, ziet u hoe de letterlijke aanpassing werkt. Overweeg een situatie waarin de gegevens van websiteverkeer worden verzameld, en het cs(referrer) gebied bevat de volgende waarde:

`http://www.abc.com/adventurenews/today.html?ad=123AZ45`

Om te bepalen of de verwijzende persoon iemand vertegenwoordigt die op één van de reclame klikte, moet u zien of de verwijzende persoon de koordadvertentie bevat. U kon de letterlijke koordadvertentie eenvoudig gebruiken om het doelkoord te zoeken en te bepalen als een reclame werd gebruikt om het verkeer aan de plaats te leiden. Terwijl dit het doelkoord zou aanpassen, zou het in twee plaatsen aanpassen en is zo dubbelzinnig en kan tot valse positieven leiden.

Volgende URL bevat de koordadvertentie op twee verschillende plaatsen:

`http://www.abc.com/ad vertnews/today.html?ad =123AZ45`

Aldus, als u probeert om te bepalen welke zittingen als resultaat van een bepaalde reclamecampagne begonnen zijn, eenvoudig is het gebruiken van de letterlijke advertentie aangezien de regelmatige uitdrukking duidelijk niet voldoende is. Het veranderen van letterlijk in &quot;ad=&quot;zou deze dubbelzinnigheid elimineren en in de uitdrukking resulteren die slechts één enkele gelijke maakt. Zelfs dit is wellicht niet voldoende om te garanderen dat de verwijzende persoon deel uitmaakte van de reclamecampagne. Overweeg de volgende referentie:

`http://www.xyz.com/hello.html?pad=something`

U hebt geen controle over URLs die anderen kunnen gebruiken om verbindingen aan de plaats tot stand te brengen. De letterlijke aanpassing is een te eenvoudig mechanisme om van zittingen de plaats te bepalen die als resultaat van de reclamecampagne begonnen zijn. De volgende sectie bespreekt hoe u metacharacters voor flexibelere en krachtige aanpassing kunt gebruiken.

## Metacharacters gebruiken {#section-e29a804336304ea1ba33d40d60139aa2}

Een metacharacter is een speciaal karakter op een programma of een gegevensgebied dat informatie over andere karakters verstrekt.

| metacharacter | beschrijving |
|---|---|
| . (punt) | Komt overeen met één teken, bijvoorbeeld: komt overeen met &quot;xyz&quot; of &quot;xxz&quot;. `re:x.z` |
| * (ster) | Komt overeen met een of meer tekens, bijvoorbeeld: komt overeen met &quot;ZZZ&quot;. `re:Z*` |
| ? (jokerteken) | De gelijken 0 of 1 van vorige uitdrukking aan kracht minimum aanpassing, bijvoorbeeld: komt overeen met &quot;xy&quot; en &quot;xyz&quot;. `xy?z` |

De extra gemeenschappelijke regelmatige uitdrukkingen kunnen ook worden gebruikt om complexere onderzoekskoorden tot stand te brengen.

**Lijsten, Waaiers, en OF**

De letterlijke aanpassing laat u één enkel koord zoeken, maar de steunen, de streepjes, en de pijpen laten u een lijst van dingen bepalen om in het doelkoord te zoeken.

<table id="table_18B86955EC3748079E7C176273ADE92B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze metacharacter... </th> 
   <th colname="col2" class="entry"> De reguliere expressieprocessor zal... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Vierkante beugels ([ ]) </td> 
   <td colname="col2"> Pas om het even welke karakters binnen van de steun met één enkele karakterpositie aan. Bijvoorbeeld, is [AB] een instructie om of de brief A of de brief B aan te passen en [0123456789] zegt gelijke aan om het even welk karakter in waaier 0 tot 9. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Dash (-) </td> 
   <td colname="col2"> <p>Pas een waaier van karakters aan. In plaats van [0123456789] te schrijven, konden we dus gewoon [0-9] schrijven. </p> <p> Dit kan tot waaiers van karakters en veelvoudige waaiers binnen één reeks steunen worden uitgebreid. Bijvoorbeeld, [0-9A-c] past de karakters 0 door 9 en A aan C aan aan. </p> <p> <p>Opmerking:  Om voor een streepje (-) als letterlijk binnen de steunen te testen, moet het eerst of het laatst komen. Bijvoorbeeld, [-0-9] tests voor - en 0 tot 9. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Pijp (|) </td> 
   <td colname="col2"> Pas één van twee keuzen aan een bepaald doelkoord aan. Bijvoorbeeld, b|nat past of vleermuis of nat aan. </td> 
  </tr> 
 </tbody> 
</table>

Overweeg de volgende voorbeelden:

| Patroon | Koord | Aanpassen |
|---|---|---|
| Win9`[58]` | OS=Win95 | Win95 |
| Win95 | 8 | OS=Win98 | Win98 |
| `[0-9]` | Mozilla/3,0 | 3 |
| Lesson`[A-Z]` | Les | Geen gelijke omdat de laag-gehuurde a niet in de waaier van bovengehackte A door Z is. |

**Negatie**

Negatie is een manier om te zeggen dat je alles wilt aanpassen behalve de gegeven karakters. De negatie metacharacter, de omtrek of het inlasteken (`^`), wordt gebruikt als eerste karakter binnen steunen om te zeggen dat u de gelijke om het even wat behalve de resterende karakters in de steunen zou willen zijn. Bijvoorbeeld, om om het even welk karakter maar een puntkomma (`;`) aan te passen, zou u schrijven

[`^;`]

Dit zou om het even welk karakter behalve de puntkomma aanpassen.

**Positionering**

Om een gelijke aan het begin of het eind van een doelkoord te dwingen, wordt één van twee metacharacters gebruikt.

| Voor deze metacharacter... | De reguliere expressieprocessor zal... |
|---|---|
| Circumflex of Caret (`^`) | Pas aan tegen het begin van het koord. Bijvoorbeeld, zou ^`[Tt]`hij de doelkoord &quot;het Beginnen&quot;aanpassen maar zou niet &quot;dit is het begin&quot;aanpassen. |
| Dollar-teken (`$`) | Pas tegen het eind van het koord aan. Bijvoorbeeld, `[Ee]`en$ zou &quot;dit is het eind&quot;aanpassen maar niet &quot;het eind is een speciale tijd.&quot; aanpassen |

>[!NOTE]
>
>Wanneer de regelmatige uitdrukking ^ aan het begin en $ aan het eind bevat, moet het volledige doelkoord de regelmatige uitdrukking aanpassen.

**Alles afstemmen**

De periode (..) is een speciale metacharacter die om het even welk karakter in het doelkoord aanpast. Bijvoorbeeld, past de regelmatige uitdrukking om het even welk doelkoord aan dat precies drie lange karakters is. `^…$` De regelmatige uitdrukking &quot;...&quot;past om het even welk doelkoord aan dat minstens drie karakters bevat.

**Herhaalde patronen**

De metacharacters van de teratie laten u een patroon meer dan eens aanpassen.

<table id="table_6A14333D6C264A48ADF1EBBAF687CADD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze metacharacter... </th> 
   <th colname="col2" class="entry"> De reguliere expressieprocessor zal... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Vragenmerk (?) </td> 
   <td colname="col2"> Pas geen instanties of één geval van het karakter aan onmiddellijk voorafgaand aan metacharacter (?). Bijvoorbeeld, past het patroongebied?d rood en gelezen aan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Sterretje (*) </td> 
   <td colname="col2"> Pas nul of meer voorkomen van het karakter aan onmiddellijk voorafgaand aan het metacharacter (*). Bijvoorbeeld, past het patroon [0-9]* om het even welk aantal karakters 0 door 9 (om het even welk geheel) aan. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Plus (+) </td> 
   <td colname="col2"> Pas één of meerdere voorkomen van het voorafgaande karakter of de waaier aan. Bijvoorbeeld, zou het patroon drie+ drie maar niet door aanpassen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> {n} </td> 
   <td colname="col2"> <p>Pas precies het het werk karakter of de waaier in tijden aan. Het volgende patroon past de telefoonaantallen van de Verenigde Staten aan: [0-9] \ {3 \} - [0-9] \ {3 \} - [0-9] \ {4 \}. </p> <p> Terwijl niet een optimaal patroon, bepaalt het of het doelkoord in het juiste formaat is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> {n,m} </td> 
   <td colname="col2"> Pas het voorafgaande karakter minstens n keer en hoogstens m keer aan. Bijvoorbeeld, van {1.2} d zou voedsel en voedsel maar niet voedsel aanpassen. </td> 
  </tr> 
 </tbody> 
</table>

## Patroonextractie {#section-4389779653b64f6cb7c47615b25c1a79}

De aanpassing van het patroon is slechts een deel van de macht van regelmatige uitdrukkingen. De regelmatige uitdrukkingen verstrekken ook een mechanisme om zeer belangrijke gedeelten van een doelkoord te halen. Dit wordt gedaan door het gebruik van de linker en juiste haakjes. Deze extracties worden typisch gebruikt als input in een ander proces en door het gebruik van *%position%* betreden, waar de positie een geheel verwijst naar de telling waarvan reeks haakjes werd aangepast.

Overweeg de volgende voorbeelden van patroonextractie:

<table id="table_BC8D471B966844049FFFCDEC0F183941"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Patroon </th> 
   <th colname="col2" class="entry"> Koord </th> 
   <th colname="col3" class="entry"> Aanpassen </th> 
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
   <td colname="col2"> Mozilla/3,0 </td> 
   <td colname="col3"> Mozilla/3,03 </td> 
   <td colname="col4"> <p>%1% = 3 </p> <p> %2% = 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Les([A-Z]) </td> 
   <td colname="col2"> Les </td> 
   <td colname="col3"> Geen gelijke omdat de laag-cased a niet in de waaier van upper-cased A door Z is </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>


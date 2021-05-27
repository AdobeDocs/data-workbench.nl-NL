---
description: Tekst of expressies kunnen in elke cel van een werkblad worden ingevoerd.
title: Werken met gegevens in werkbladen
uuid: c2331fa5-aa07-4622-8f44-5124c22dffcb
exl-id: 40d9211b-8f5c-4051-8f93-638ffacf45bd
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Werken met gegevens in werkbladen{#work-with-data-in-worksheets}

Tekst of expressies kunnen in elke cel van een werkblad worden ingevoerd.

Alle expressies in een werkblad worden voorafgegaan door een gelijk teken (=), tenzij [!DNL eval( )] wordt gebruikt, dat de tekst in de cel waarnaar wordt verwezen als een expressie behandelt.

Voor een volledige lijst van metrische, afmeting, en de regels van de filtersyntaxis, zie [Syntaxis van de Taal van de Vraag](../../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f).

**Gegevens typen in een werkblad**

1. Klik tweemaal op een cel in het werkblad om de bewerkingsmodus te activeren. De geselecteerde cel wordt gemarkeerd.
1. Typ of plak de gewenste gegevens in de cel.

**Kopiëren en plakken van de ene cel naar de andere**

1. Klik met de rechtermuisknop op de cel die de gegevens bevat die u wilt kopiëren en klik op **[!UICONTROL Copy]**.
1. Klik met de rechtermuisknop op de cel waarin u de gekopieerde gegevens wilt plakken en klik op **[!UICONTROL Paste]**.

Data Workbench werkt automatisch de verwijzingen in de nieuwe cel bij om naar de aangewezen kolommen en de rijen te verwijzen.

**Kopiëren en plakken van een groep cellen naar een andere groep**

1. Selecteer de cellen die de gegevens bevatten die u wilt kopiëren.
1. Klik met de rechtermuisknop op de cellen die de gegevens bevatten die u wilt kopiëren en klik op **[!UICONTROL Copy]**.
1. Klik met de rechtermuisknop op de eerste cel waarin u de gekopieerde gegevens wilt plakken en klik op **[!UICONTROL Paste]**. De gegevens worden in de eerste cel en eronder geplakt.

Data Workbench werkt automatisch de verwijzingen in de nieuwe cel bij om naar de aangewezen kolommen en de rijen te verwijzen.

**Een kolom invoegen**

* Klik met de rechtermuisknop op een kolom en klik op **[!UICONTROL Insert Column]**. De nieuwe kolom wordt links van de geselecteerde kolom ingevoegd.

**Een kolom verwijderen**

* Klik met de rechtermuisknop op de kolom die u wilt verwijderen en klik op **[!UICONTROL Delete Column]**. De kolom wordt verwijderd.

**Een rij invoegen**

* Klik met de rechtermuisknop op een rij en klik op **[!UICONTROL Insert Row]**. De nieuwe rij wordt boven de geselecteerde rij ingevoegd.

**Een rij verwijderen**

* Klik met de rechtermuisknop op de rij die u wilt verwijderen en klik op **[!UICONTROL Delete Row]**. De rij wordt verwijderd.

**Een kolom vergroten of verkleinen**

1. Plaats de cursor in de kolomkoprij op de scheidingslijn rechts van de kolom waarvan u de grootte wilt wijzigen.
1. Klik en sleep naar rechts om de breedte van de kolom te vergroten of naar links om de breedte van de kolom te verkleinen.

**Een cel opmaken**

1. Klik met de rechtermuisknop op de cel en klik op **[!UICONTROL Format]**.

   ![](assets/mnu_Worksheet_Format.png)

1. Klik op de gewenste indeling in het menu met beschikbare opties:

<table id="table_5788E01E52CC44E7927A0D23760D9EDD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Menuoptie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Getal </p> </td> 
   <td colname="col2"> <p>Hiermee past u de geselecteerde numerieke notatie toe op uw gegevens, zoals tijd, datum, percentage of decimaal. </p> <p>Klik <span class="uicontrol"> Standaard</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Uitvullen </p> </td> 
   <td colname="col2"> <p>Hiermee vult u de gegevens in de cel uit op links, midden of rechts. De standaarduitvulling blijft behouden. </p> <p>Klik <span class="uicontrol"> Standaard</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kleur </p> </td> 
   <td colname="col2"> <p>Past de geselecteerde doopvontkleur op de gegevens binnen de cel toe. De standaardkleur van het lettertype is wit. </p> <p>Klik <span class="uicontrol"> Standaard</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Indicator </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u een metrische indicator met deze cel. Zie <a href="../../../home/c-get-started/c-analysis-vis/c-wksts/c-metric-ind.md#concept-f0e911b23b2c4e8da3e1ea7b9ae04183"> Metrische indicatoren maken</a> voor meer informatie. </p> <p>Klik <span class="uicontrol"> Standaard</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Invoercel </p> </td> 
   <td colname="col2"> <p>Hiermee maakt u van de geselecteerde cel een invoercel. Zie <a href="../../../home/c-get-started/c-analysis-vis/c-wksts/c-input-cells.md#concept-08cd2c05a28a43dd9f7698b37e23e590"> Invoercellen maken</a> voor meer informatie. </p> <p>Klik <span class="uicontrol"> Standaard</span> om het geselecteerde formatteren te verwijderen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sneltoetsen {#section-05301f4d2c60418e86902635a7aeee20}

Binnen aantekenvellen kunt u veel van de basis het uitgeven toetsenbordkortere weg gebruiken die u in om het even welke tekstredacteur, zoals Blocnote of Microsoft Word kunt gebruiken.

In de volgende tabel staan de standaardsneltoetsen die u kunt gebruiken bij het invoeren van gegevens in een werkblad.

<table id="table_8E6F73F253B3451CA1DE45EE4F4E69EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Sneltoets </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Pijltoetsen </p> </td> 
   <td colname="col2"> <p>U kunt van cel naar cel in het werkblad gaan met de toetsen Pijl-omhoog, Pijl-omlaag, Pijl-links en Pijl-rechts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F2 </p> </td> 
   <td colname="col2"> <p>Bewerk de cel door de cursor in de geselecteerde cel te plaatsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Enter </p> </td> 
   <td colname="col2"> <p>Voltooit het bewerken van de cel die u hebt geselecteerd. De cursor wordt uit de cel verwijderd en de celinhoud weerspiegelt uw bewerking. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Esc </p> </td> 
   <td colname="col2"> <p>Annuleer het bewerken van de cel die u hebt geselecteerd. De cursor wordt uit de cel verwijderd en de celinhoud wordt teruggezet naar de oorspronkelijke waarden voordat u begon met bewerken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verwijderen </p> </td> 
   <td colname="col2"> <p>Verwijder de inhoud van de cel(len). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+A </p> </td> 
   <td colname="col2"> <p>Selecteer de inhoud van de cel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+C </p> </td> 
   <td colname="col2"> <p>Kopieer de inhoud van de cel(len). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+X </p> <p>Shift+Delete </p> </td> 
   <td colname="col2"> <p>Kopieer en verwijder de inhoud van de cel(len). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+v </p> <p>Shift+Insert </p> </td> 
   <td colname="col2"> <p>Plak de inhoud van de cellen die u hebt gekopieerd in de geselecteerde cel(len). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+Z </p> </td> 
   <td colname="col2"> <p>Ongedaan maken typen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ctrl+Shift+z </p> </td> 
   <td colname="col2"> <p>Opnieuw typen. </p> </td> 
  </tr> 
 </tbody> 
</table>

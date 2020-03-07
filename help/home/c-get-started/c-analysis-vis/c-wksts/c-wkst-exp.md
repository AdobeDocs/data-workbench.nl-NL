---
description: Conceptuele informatie over aantekenveluitdrukkingen en het gebruiken van celverwijzingen.
solution: Analytics
title: Werkbladexpressies
topic: Data workbench
uuid: be57d6bd-3e13-4c90-9034-8e0f2b8315aa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Werkbladexpressies{#worksheet-expressions}

Conceptuele informatie over aantekenveluitdrukkingen en het gebruiken van celverwijzingen.

Het volgende aantekenvel verstrekt details over de bezoekers die de pagina bekijken van de Tovenaar van de Toepassing die op de online toepassingsvorm van de website van een bank wordt verstrekt.

![](assets/client-wkst.png)

* Kolom A bevat een lijst van de categorieën bezoekers die worden beoordeeld: bezoekers, doorverwezen bezoekers, en doorverwezen bezoekers van Referrer A.
* De kolom B toont het aantal bezoekers in elke categorie die de Apply nu pagina bekeken.
* De kolom C toont die bezoekers die zowel Apply nu als de pagina&#39;s van de Tovenaar van de Toepassing bekeken.
* De kolom D bevat de percentages van pas nu kijkers in de drie categorieën toe die ook de pagina van de Tovenaar van de Toepassing bekeken.

Het aantekenvel toont aan dat ongeveer 55 percent van de bezoekers van Referrer A die de Apply nu pagina bekeken ook de pagina van de Tovenaar van de Toepassing bekeken.

De volgende lijst verstrekt steekproefformules voor het aantekenvel in het vorige voorbeeld:

<table id="table_0F5EFDB58040465AB599E6BE93324822"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Worksheet-cel </th> 
   <th colname="col2" class="entry"> Formule </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>B2 </p> <p>Bezoekers die de pagina Nu toepassen hebben bekeken </p> </td> 
   <td colname="col2"> <p><span class="filepath"> =Bezoekers[Page="/applynow/default.asp"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>B3 </p> <p>Verwezen Bezoekers die de pagina Nu toepassen hebben bekeken </p> </td> 
   <td colname="col2"> <p><span class="filepath"> =Referred_Visitors[Page="/applynow/default.asp"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>B4 </p> <p>Verwezen Bezoekers van Referrer A die de Apply nu pagina bekeken </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> =Referred_Visitors[Page="/applynow/default.asp" </span> </p> <p> EN <span class="filepath"> Referrer="Ref A"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C2 </p> <p>Bezoekers die de Apply nu pagina en de pagina van de Tovenaar van de Toepassing bekeken </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> =Bezoekers[Page="/applynow/default.asp" </span> </p> <p> EN <span class="filepath"> Page="/applynow/appwizard.asp"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C3 </p> <p>Verwezen Bezoekers die de Apply nu pagina en de pagina van de Tovenaar van de Toepassing bekeken </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> =Referred_Visitors[Page="/applynow/default.asp" </span> </p> <p> EN <span class="filepath"> Page="/applynow/appwizard.asp"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>C4 </p> <p>Verwezen Bezoekers van Referrer A die de Apply nu pagina en de pagina van de Tovenaar van de Toepassing bekeken </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> =Referred_Visitors[Page="/applynow/default.asp"</span> </p> <p> EN <span class="filepath"> Page="/applynow/appwizard.asp"</span> </p> <p> EN <span class="filepath"> Referrer="Ref A"]</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D2 </p> <p>Percentage bezoekers die de Apply nu pagina en de pagina van de Tovenaar van de Toepassing bekeken </p> </td> 
   <td colname="col2"> <p><span class="filepath"> =C2/B2*100</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D3 </p> <p>Percentage van Verwezen Bezoekers die de Apply nu pagina en de pagina van de Tovenaar van de Toepassing bekeken </p> </td> 
   <td colname="col2"> <p><span class="filepath"> =C3/B3*100</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>D4 </p> <p>Percentage van Verwezen Bezoekers van Referrer A die de Apply nu pagina en de pagina van de Tovenaar van de Toepassing bekeken </p> </td> 
   <td colname="col2"> <p><span class="filepath"> =C4/B4*100</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Zoals met andere visualisaties, werken de aantekenvellen automatisch bij wanneer u een selectie in een andere visualisatie in de werkruimte maakt. Voor meer informatie over het maken van selecties, zie het [Maken Selecties in Visualisaties](../../../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746).

In het volgende voorbeeld van Webgegevens, zijn verscheidene dagen van zittingsgegevens geselecteerd in de zittingen door de visualisatie van de Dag. Het aantekenvel toont aan dat tijdens de geselecteerde tijd, ongeveer 69 percent van de bezoekers van Referrer A die de Apply nu pagina bekeken ook de pagina van de Tovenaar van de Toepassing bekeken. Zonder deze selectie (zoals aangetoond in het voorbeeld hierboven), bekeken ongeveer 55 percent van de bezoekers van Referrer A de Apply nu pagina evenals de pagina van de Tovenaar van de Toepassing.

![](assets/client-exp.png)

## Celverwijzingen gebruiken {#section-0004e315c9c94d359b1a8a39794ba555}

U kunt om het even welk koord, hetzij op zijn of binnen een andere uitdrukking in het aantekenvel, met een celverwijzing substitueren.

* **Eenvoudige celreferentie:** Cel A2 bevat de tekst Bezoekers, die als rubriek wordt gebruikt. Cel B2 bevat [!DNL eval(A1)], dat evalueert tot [!DNL =Visitors].

* **Referentie filtercel:** Cel A5 bevat de datum van gisteren. Cel B5 bevat [!DNL Bezoekers[ Day=A5 ]], die het aantal bezoekers gisteren evalueert.

* **Verbonden celreferentie:** De cel A5 bevat de datum van vandaag en cel A6 bevat de tijd 08:00 tot 08:59 van één uur. Cel B6 bevat [!DNL Bezoekers[ Hour=A5+&quot;+&quot;+A6 ]], die tot het aantal Bezoekers van vandaag tussen 8.00 en 9.00 uur evalueert.


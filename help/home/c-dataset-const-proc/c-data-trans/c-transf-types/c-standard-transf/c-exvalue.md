---
description: Als u met webgegevens werkt, kunt u de ExtractValue-transformatie gebruiken om een waarde te extraheren uit een queryreeks, cookie of vergelijkbaar gecodeerd veld in uw websitegegevens.
title: ExtractValue
uuid: 305827a2-04e6-421f-82cb-923d62b02e70
exl-id: 5bafe64f-081a-49ec-997e-68e8f6915a71
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# ExtractValue{#extractvalue}

{{eol}}

Als u met webgegevens werkt, kunt u de ExtractValue-transformatie gebruiken om een waarde te extraheren uit een queryreeks, cookie of vergelijkbaar gecodeerd veld in uw websitegegevens.

De namen die overeenkomen met de waarde die moet worden geëxtraheerd, kunnen in elk logbestandvermelding anders zijn.

<table id="table_D16A39BE035043628A4D6F7452952304"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Standaard </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Naam </td> 
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt hier elke naam invoeren. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Voorwaarde </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoernaam </td> 
   <td colname="col2"> <p>De naam of namen van de velden die uit de invoerquery moeten worden geëxtraheerd. </p> <p> <p>Opmerking: Als de Invoernaam een vector is (er zijn meerdere namen aanwezig), wordt slechts één waarde geëxtraheerd. </p> </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoerquery </td> 
   <td colname="col2"> De gecodeerde toewijzing (queryreeks, cookie enzovoort) waaruit de waarde moet worden geëxtraheerd. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoerwaarde </td> 
   <td colname="col2"> De naam van het veld dat wordt gebruikt om de geëxtraheerde gedecodeerde waarde vast te leggen. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

Als u een zoekfragment wilt extraheren, kunt u de hele woordgroep extraheren en desgewenst de woordgroep splitsen in zoektermen met een [!DNL Tokenize] transformatie. Voor informatie over de [!DNL Tokenize] transformatie, zie [Tokenize](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-tokenize.md#concept-f460aa5df3a7476e971af29cf5d9b32c).

In dit voorbeeld wordt een [!DNL ExtractValue] transformatie om waarden van het veld x-v-search-querynames uit cs(reference-query) te extraheren en op te slaan in het veld x-search-express.

![](assets/cfg_TransformationType_ExtractValue.png)

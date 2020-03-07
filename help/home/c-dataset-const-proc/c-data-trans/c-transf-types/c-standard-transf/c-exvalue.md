---
description: Als u met Webgegevens werkt, kunt u de transformatie gebruiken ExtractValue om een waarde uit een vraagkoord, koekje, of zo ook gecodeerd gebied in uw websitegegevens te halen.
solution: Analytics
title: ExtractValue
topic: Data workbench
uuid: 305827a2-04e6-421f-82cb-923d62b02e70
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# ExtractValue{#extractvalue}

Als u met Webgegevens werkt, kunt u de transformatie gebruiken ExtractValue om een waarde uit een vraagkoord, koekje, of zo ook gecodeerd gebied in uw websitegegevens te halen.

Merk op dat de naam(en) die overeenkomt (overeenkomen) met de waarde die moet worden geëxtraheerd, in elke logboekvermelding kan (kunnen) verschillen.

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
   <td colname="col2"> Beschrijvende naam van de transformatie. U kunt om het even welke naam hier ingaan. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Opmerkingen </td> 
   <td colname="col2"> Optioneel. Opmerkingen over de transformatie. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Toestand </td> 
   <td colname="col2"> De omstandigheden waaronder deze transformatie wordt toegepast. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoernaam </td> 
   <td colname="col2"> <p>De naam (namen) van de velden die uit de invoerquery moeten worden gehaald. </p> <p> <p>Opmerking:  Als de Naam van de Input een vector is (namelijk zijn er veelvoudige aanwezige namen), wordt slechts één waarde gehaald. </p> </p> </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Invoerquery </td> 
   <td colname="col2"> De gecodeerde afbeelding (vraagkoord, koekje, enzovoort) waarvan de waarde moet worden gehaald. </td> 
   <td colname="col3"></td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitgangswaarde </td> 
   <td colname="col2"> De naam van het veld dat wordt gebruikt om de geëxtraheerde gedecodeerde waarde vast te leggen. </td> 
   <td colname="col3"></td> 
  </tr> 
 </tbody> 
</table>

Als u een onderzoeksuitdrukking wilt halen, kunt u de volledige uitdrukking halen en, indien gewenst, de uitdrukking verdelen in onderzoekstermijnen gebruikend een [!DNL Tokenize] transformatie. Voor informatie over de [!DNL Tokenize] transformatie, zie [Tokenize](../../../../../home/c-dataset-const-proc/c-data-trans/c-transf-types/c-standard-transf/c-tokenize.md#concept-f460aa5df3a7476e971af29cf5d9b32c).

Dit voorbeeld vormt een [!DNL ExtractValue] transformatie om waarden van het x-v onderzoek-querynames gebied uit cs (verwijzing-vraag) te halen en hen op het x-onderzoek-uitdrukking gebied op te slaan.

![](assets/cfg_TransformationType_ExtractValue.png)


---
description: Bestanden die zijn opgenomen in het installatiepakket voor Data Workbench.
title: Bestanden die zijn opgenomen in het installatiepakket
uuid: 46cda536-ea71-4840-bd7f-3fe9e0242c33
exl-id: 086fb49c-d492-4670-938b-7ede70a7cd16
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# Bestanden die zijn opgenomen in het installatiepakket{#files-included-in-the-installation-package}

{{eol}}

Bestanden die zijn opgenomen in het installatiepakket voor Data Workbench.

De volgende directory&#39;s zijn opgenomen in het Insight-pakket.

## Programmabestanden {#section-ddb14bf42cdd4dc7a6b4310a5b4388e4}

Uitvoerbaar werkstation (**[!DNL Insight.exe]**) en ondersteunende bestanden worden standaard in deze map geïnstalleerd.

```
C:\Program Files\Adobe\Adobe Analytics\Data Workbench
```

<table id="table_56BAC85184A04E7680FBB4B36DE73285"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Map </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.exe </span> </b> </td> 
   <td colname="col2"> Het uitvoerbare bestand van de client Data Workbench. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> insight.ini </span> </b> </td> 
   <td colname="col2"> Taal en pad instellen voor de <span class="filepath"> Appdata </span> map. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.zbin </span> </b> </td> 
   <td colname="col2"> <p>De werkbank Gegevens ondersteunt nu een invoermethode-editor (IME) als een secundair tekstinvoerproces waarmee u internationale tekens van het toetsenbord kunt invoeren met behulp van een zwevend tekstvak. De werkbank voor gegevens biedt standaard ondersteuning voor Engels, maar u kunt ook andere bestanden laden die internationale talen ondersteunen, zoals een virtueel Chinees toetsenbord (Pinyin IME). </p> <p>Een nieuw woordenboekbestand <span class="filepath"> (Insight.zbin </span>) is vereist door de clienttoepassing ter ondersteuning van de IME. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> unins000.exe </span></b> </td> 
   <td colname="col2"> Uitvoeren om werkstation te verwijderen en bestanden te verwijderen. </td> 
  </tr> 
 </tbody> 
</table>

## AppData-bestanden {#section-afddeedf8d29451f996fa46b2dfe932c}

Gegevensbestanden (**[!DNL Insight.cfg]**, Profielen, certificaten, traceringslogbestanden en gebruikersbestanden) worden standaard opgeslagen in:

```
<filepath>
  C:\Users\<Winuser>\AppData\Adobe\Analytics\DataWorkbench\ 
</filepath>
```

<table id="table_DBA4DBB54C57409C8EC116C686A08560"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Map </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.cfg </span> </b> </td> 
   <td colname="col2"> Het configuratiebestand van de Data Workbench. Definieert parameters waarbinnen Data Workbench werkt. Zie <a href="../../../home/c-install-insight/install-setup/c-conn-isvr.md#concept-9f47b2cd7c12492693a2cf810cfc1d9e"> De verbinding met Insight Server configureren </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Basis </span> </b> </td> 
   <td colname="col2"> <p>Bevat de programmabestanden voor Data Workbench. </p> <p> <p>Opmerking: U moet deze bestanden niet verwijderen of wijzigen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Certificaten </span> </b> </td> 
   <td colname="col2"> Bevat het certificaatbestand, <span class="filepath"> trust_ca_cert.pem </span>en het benoemde digitale gebruikerscertificaat voor Data Workbench. Zie <a href="../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#concept-4c6a900074d4464fb6ec7862f7e54f10"> Het digitale certificaat downloaden en installeren </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Configuratie </span> </b> </td> 
   <td colname="col2"> Bevat de dossiers die voor de configuratie van het Werkstation worden gebruikt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Geografie </span></b> </td> 
   <td colname="col2"> Bestanden voor grafische rendering van geografische visualisaties. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Traceren </span></b> </td> 
   <td colname="col2"> Logbestanden die zijn gegenereerd op basis van het werkstation. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Profielen </span></b> </td> 
   <td colname="col2"> <i>AdobeSC</i>, <i>Predictieve analyse</i> en andere profielconfiguratiebestanden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> InsightSetup.exe </span></b> </td> 
   <td colname="col2"> De tovenaar van de opstelling om extra cliëntcomputers in te installeren <b> <span class="filepath"> Software/Insight </span></b> map. </td> 
  </tr> 
 </tbody> 
</table>

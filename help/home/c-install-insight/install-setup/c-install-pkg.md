---
description: Dossiers inbegrepen in het de installatiepakket van de Werkbank van Gegevens.
title: Bestanden die zijn opgenomen in het Installatiepakket
uuid: 46cda536-ea71-4840-bd7f-3fe9e0242c33
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bestanden die zijn opgenomen in het Installatiepakket{#files-included-in-the-installation-package}

Dossiers inbegrepen in het de installatiepakket van de Werkbank van Gegevens.

De volgende folders zijn inbegrepen in het pakket van het Inzicht.

## Programmabestanden {#section-ddb14bf42cdd4dc7a6b4310a5b4388e4}

Uitvoerbare (**[!DNL Insight.exe]**) en ondersteunende dossiers van het Werkstation worden geïnstalleerd door gebrek aan deze omslag.

```
C:\Program Files\Adobe\Adobe Analytics\Data Workbench
```

<table id="table_56BAC85184A04E7680FBB4B36DE73285"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Directoraat </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.exe </span></b> </td> 
   <td colname="col2"> Uitvoerbaar de cliënt van de Werkbank van Gegevens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> inzicht.ini </span></b> </td> 
   <td colname="col2"> Stel de taal en het pad in voor de map <span class="filepath"> Appdata </span> . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.zbin </span></b> </td> 
   <td colname="col2"> <p>De werkbank van gegevens steunt nu een Redacteur van de Methode van de Input (IME) als secundair proces van de tekstingang dat u toestaat om internationale karakters van uw toetsenbord in te gaan gebruikend een drijvend tekstvakje. De werkbank van gegevens zal Engels door gebrek steunen maar staat u ook toe om andere dossiers te laden om internationale talen, zoals een virtueel Chinees toetsenbord (Pinyin IME) te steunen. </p> <p>Een nieuw woordenboekdossier <span class="filepath"> (Insight.zbin </span>) wordt vereist door de cliënttoepassing om IME te steunen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> unins000.exe </span></b> </td> 
   <td colname="col2"> Kan werkstation verwijderen en bestanden verwijderen. </td> 
  </tr> 
 </tbody> 
</table>

## AppData-bestanden {#section-afddeedf8d29451f996fa46b2dfe932c}

De Dossiers van gegevens (**[!DNL Insight.cfg]**, Profielen, Certificaten, spoorlogboeken, en gebruikersdossiers) worden opgeslagen door gebrek aan:

```
<filepath>
  C:\Users\<Winuser>\AppData\Adobe\Analytics\DataWorkbench\ 
</filepath>
```

<table id="table_DBA4DBB54C57409C8EC116C686A08560"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Directoraat </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Insight.cfg </span></b> </td> 
   <td colname="col2"> Het de configuratiedossier van de Werkbank van Gegevens. Bepaalt parameters waarbinnen de Werkbank van Gegevens werkt. Zie het <a href="../../../home/c-install-insight/install-setup/c-conn-isvr.md#concept-9f47b2cd7c12492693a2cf810cfc1d9e"> Vormen van de Verbinding aan de Server van het Inzicht </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Basis </span></b> </td> 
   <td colname="col2"> <p>Bevat de programmadossiers voor de Werkbank van Gegevens. </p> <p> <p>Opmerking:  U zou geen van deze dossiers moeten verwijderen of veranderen. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Certificaten </span></b> </td> 
   <td colname="col2"> Bevat het certificaatdossier, <span class="filepath"> trust_ca_cert.pem </span>, en het genoemde gebruiker digitale certificaat voor de Werkbank van Gegevens. Zie <a href="../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#concept-4c6a900074d4464fb6ec7862f7e54f10"> Downloaden en installeren van het Digitale Certificaat </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Configuratie </span></b> </td> 
   <td colname="col2"> Bevat de dossiers die voor de configuratie van het Werkstation worden gebruikt. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Geografie </span></b> </td> 
   <td colname="col2"> Bestanden voor het grafisch weergeven van geografische visualisaties. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Spoor </span></b> </td> 
   <td colname="col2"> De dossiers van het logboek die van het Werkstation worden geproduceerd. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> Profielen </span></b> </td> 
   <td colname="col2"> <i>AdobeSC</i>, <i>Predictive Analytics</i> en andere dossiers van de profielconfiguratie. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b> <span class="filepath"> InsightSetup.exe </span></b> </td> 
   <td colname="col2"> De tovenaar van de opstelling om extra cliëntcomputers in de <b> omslag van de Software/van het Inzicht te installeren <span class="filepath"> </span></b> . </td> 
  </tr> 
 </tbody> 
</table>


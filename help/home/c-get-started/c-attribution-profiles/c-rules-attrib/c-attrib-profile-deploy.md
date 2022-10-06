---
description: Het kenmerk is een overgeërfd, kant-en-klare profiel. In combinatie met het Adobe SC-profiel en de gegevensfeed Analytics (SC/Insight) kan het profiel worden gebruikt om snel nieuwe attributiemodellen via digitale kanalen beschikbaar te maken.
title: Het kenmerkprofiel implementeren
uuid: acc4e92a-2af1-4993-bae7-015ece3da26c
exl-id: 287e1710-7e74-4904-b258-7b811ad484b7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---

# Het kenmerkprofiel implementeren{#deploying-the-attribution-profile}

{{eol}}

Het kenmerk is een overgeërfd, kant-en-klare profiel. In combinatie met het Adobe SC-profiel en de gegevensfeed Analytics (SC/Insight) kan het profiel worden gebruikt om snel nieuwe attributiemodellen via digitale kanalen beschikbaar te maken.

Nadat u het kenmerk op de primaire server hebt opgeslagen, zijn er twee extra stappen nodig om het profiel te integreren in het huidige profiel in het dialoogvenster [!DNL Profile] map: (1) Stel het bestand Profile.cfg in en (2) Declareer de vereiste velden.

## Het bestand Profile.cfg instellen {#section-7531cb865d994207baba692a6fc842d7}

Het kenmerk moet, net als alle profielen, worden toegevoegd aan het [!DNL profile.cfg] bestand. Omdat het kenmerk afhankelijk is van het Adobe SC-profiel, moet het Adobe SC-profiel eerst in het configuratiebestand worden vermeld voordat het kenmerk wordt gebruikt.

>[!NOTE]
>
>Deze stappen zullen een re-transformatie van de dataset vereisen.

1. Open de [!DNL profile.cfg] in uw map met aangepaste profielen. (Openen in [!DNL server\Profiles\(custom profile name)\profile.cfg].

1. Als het kenmerk niet in het configuratiebestand wordt vermeld, voegt u dit toe aan de lijst. ![](assets/new_profile_cfg.png)

1. Zorg ervoor dat de **[!UICONTROL Attribution]** tekenreeks wordt onder de **[!UICONTROL Adobe SC]** profieltekenreeks.

1. De bijgewerkte versie opslaan [!DNL profile.cfg] en sla het bestand vervolgens op de server op via Profielbeheer.

## De vereiste velden declareren {#section-23d4273af0c34b7a85ae3430e2c9350e}

Het kenmerk bevat vooraf gedefinieerde velden en met een reeks transformaties worden deze velden op nieuwe en nuttige manieren door uitgebreide afmetingen toegankelijk gemaakt. Om de meest directe waarde te bieden, hangt het kenmerk af van de velden die beschikbaar zijn met het Adobe SC-profiel.

<table id="table_97751B73CCAA4B96BB162641A178A68A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Standaardvariabelen </th> 
   <th colname="col2" class="entry"> Veldnaam en decoderingspositie (Adobe SC) </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Campaign </td> 
   <td colname="col2"> <p>x-campagne, #199 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Marketingkanalen </td> 
   <td colname="col2"> <p>x-va_near_detail, #162 </p> <p>x-va_instance_event, #163 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> De gebeurtenis Order </td> 
   <td colname="col2"> <p>x-order, #206 </p> <p>x-purchase aseid, #200 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Omzet </td> 
   <td colname="col2"> x-Revenue, #205 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Eenheden </td> 
   <td colname="col2"> <p>x-units, #204 </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Controleer of deze velden zijn gedeclareerd in de Decoderingsgroep die wordt gebruikt om de Adobe Analytics-gegevensbron te definiëren. De standaarddecoderingsgroep is beschikbaar onder [!DNL Dataset\Log Procesing\Decoding Instructions.cfg].
1. Controleer of deze velden zijn gedeclareerd in het dialoogvenster **[!UICONTROL Fields]** van de [!DNL SC Fields.cfg] bestand. Dit bestand bevindt zich onder [!DNL Dataset\Log Processing\SC Fields.cfg].

## Toevoegingen voor kenmerken en probleemoplossing {#section-168133a8a1a54e1281e532033878d246}

Aan het kenmerkprofiel is een configuratiebestand toegevoegd, [!DNL 0a_Marketing Channels.cfg], die de waarde van [!DNL x-va_closer_detail] in een nieuw veld [!DNL x-marketing-channel], wanneer de [!DNL x-va_instance_event] veld komt overeen met &quot;1&quot;. Beide [!DNL x-va_closer_detail] en [!DNL x-va_instant_event] worden standaard gedecodeerd en doorgegeven van decodering in de geïnstalleerde pakketten die beschikbaar zijn wanneer u een update uitvoert naar versie 6.2.

De [!DNL x-marketing-channel] het gebied wordt dan gebruikt in de Eenvoudige afmeting genoemd het Kanaal van de Marketing.

>[!IMPORTANT]
>
>Als u uw profielen hebt gewijzigd door voorheen ongebruikte velden die nu worden gebruikt, te verwijderen, moet u controleren of de [!DNL x-va_closer_detail] en [!DNL x-va_instance_event] velden worden gedecodeerd en doorgegeven voor gebruik.

Als velden ontbreken, krijgt u een bericht in uw gedetailleerde status:

```
<b>x-va_closer_detail</b> is not available
```

of

```
<b>x-va_instance_event</b> is not available
```

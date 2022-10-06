---
description: Configureer de tijdafmetingen voor een correcte weergave voor de landinstelling.
title: Dimension voor tijd lokaliseren
uuid: a2098522-bf05-4680-9b78-6fb284695a0a
exl-id: 950fe70b-a687-4b9c-b29f-555139740809
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Dimension voor tijd lokaliseren{#localizing-time-dimensions}

{{eol}}

Configureer de tijdafmetingen voor een correcte weergave voor de landinstelling.

U kunt de weergegeven tijdnotatie configureren op basis van de landinstelling in het dialoogvenster **[!DNL Standard Time Dimensions.cfg]** bestand (standaard aanwezig op **[!DNL Server/Profiles/`<my profile>`/Dataset/Transformation/Time/Standard Time Dimension.cfg]**).

In Noord-Amerika kunt u bijvoorbeeld de datum 3 mei 2015 uitdrukken als 3/5/15, of **`%m/%d/%y`**. In andere delen van de wereld kan dit echter worden geïnterpreteerd als `%d/%m/%y`, of 5 maart 2015 vanwege een dubbelzinnigheid in de waarden. Om deze situatie te vermijden, zou een beheerder het getoonde formaat kunnen willen veranderen om de verwachtingen van de gebruikers in een scène aan te passen.

## 1. Dimension voor standaardtijd overschrijven in Dimension voor standaardtijd.cfg {#section-7d0b24657bef4b15abb3cbea66cb617f}

Om deze eigenschap toe te laten, moet de beheerder de gebreken met voeten treden door of de bestaande tijddimensies uit te geven of door nieuwe tijddimensies met extra parameters te creëren.

Hierna volgt een voorbeeld van een gewijzigde tijddimensie.

De **Indeling** De waarden voor Week, Uur, Dag, Maand, en Uur van Dag worden geplaatst aan de gebreken in het voorbeeld.

>[!NOTE]
>
>Als deze lijnen worden weggelaten, zal het gedrag van de Data Workbench niet veranderen en de afmeting zal worden gecompileerd gebruikend de gebreken.

```
Transformation Include = TransformationInclude:  
  Extended Dimensions = vector: 1 items 
    0 = TimeDimensions:  
      Comments = Comment: 0 items 
      Dimensions = map:  
        Day = string: Day 
        Day of Week = string: Day of Week 
        Hour = string: Hour 
        Hour of Day = string: Hour of Day 
        Month = string: Month 
        Week = string: Week 
      Hidden = bool: false 
      Input Time (1970 epoch) = string: x-unixtime 
      Week Format = string:  
  %m/%d/%y
      Hour Format = string:  
  %x %H:%M 
      Day Format = string:  
  %x
      Month Format = string:  
  %b '%y
      Hour Of Day Format = string:  
  %#H:%M
      Name = string: Visit Time 
      Parent = string: Visit 
      Week Start Day = string: Mon 
  Transformations = vector: 0 items
```

![](assets/6_4_time_format.png)

## 2. Het bestand meta.cfg configureren {#section-5e077d3298dd48fda7f7bb16af9ea00c}

Bovendien, is het noodzakelijk voor de pakketbeheerder om deze parameters en hun gebreken aan profiel toe te voegen **[!DNL meta.cfg]** bestand. Op deze manier kunt u bestanden vanaf het werkstation bewerken.

Hier is een uittreksel van gevormd **[!DNL meta.cfg]** bestand.

```
dimensions = vector: 6 items 
  0 = Template: 
    ...
  ...
  5 = Template: 
    name = string: Time Dimensions 
    value = TimeDimensions: 
      Name = string:  
      Comments = Comment: 0 items 
      Hidden = bool: false 
       
  Week Format = string: %d/%m/%y 
       Hour Format = string: %x %H:%M 
       Day Format = string: %x 
       Month Format = string: %b '%y 
       Hour Of Day Format = string: %#H:%M</b> 
      Input Time (1970 epoch) = string:  
      Parent = string:  
      Week Start Day = string: Mon 
      Dimensions = map: 
        Hour of Day = string: Hour of Day 
        Day of Week = string: Day of Week 
        Hour = string: Hour 
        Day = string: Day 
        Week = string: Week 
        Month = string: Month
```

Hier is een voorbeeld van een **[!DNL meta.cfg]** bestand op het werkstation:

![](assets/dwb_time_format.png)

De beheerder kan dan in de **Bestandsbeheer** opent u het bestand of de bestanden waarin de tijdafmetingen zijn geconfigureerd (bijvoorbeeld **[!DNL Standard Time Dimensions.cfg]**) en bewerkt u deze in het werkstation.

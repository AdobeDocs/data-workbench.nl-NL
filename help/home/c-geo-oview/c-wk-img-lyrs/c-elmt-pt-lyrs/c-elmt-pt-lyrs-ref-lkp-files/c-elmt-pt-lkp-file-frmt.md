---
description: Informatie over de kolommen van de elementpuntlaag.
title: Opzoekbestandsindeling voor elementpunt
uuid: 3480b9f3-35cd-40b7-aac9-15a3e2f19c1c
exl-id: da81da9e-0567-4f3a-bc0d-ab6c5e4a23b7
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Bestandsindeling voor opzoeken van elementpunt{#element-point-lookup-file-format}

Informatie over de kolommen van de elementpuntlaag.

Het opzoekbestand van de elementpuntlaag moet ten minste de volgende drie kolommen bevatten:

* **[!DNL Key]kolom:** Deze kolom zou gemeenschappelijke zeer belangrijke gegevens moeten bevatten, die de server van de gegevenswerkbank toelaat om de gegevens in het raadplegingsdossier met dat in de dataset te verbinden. De [!DNL Key] kolom moet de eerste kolom in het raadplegingsdossier zijn. Elke rij in deze kolom identificeert een element van de dimensie.

* **[!DNL Longitude]kolom:** Deze kolom moet de lengtegraad bevatten voor elk gegevenspunt in de  [!DNL Key] kolom.

* **[!DNL Latitude]kolom:** Deze kolom moet de breedtegraad voor elk gegevenspunt in de  [!DNL Key] kolom bevatten.

* **[!DNL Name]kolom:** (Optioneel). Als u een naam wilt specificeren die op de kaart voor elk gegevenspunt moet worden getoond, kunt u een [!DNL Name] kolom in het raadplegingsdossier omvatten.

Elke rij in het opzoekbestand [!DNL Zip Points.txt] bevat een ZIP-code in de eerste kolom, gevolgd door de lengte, breedte en de bijbehorende plaatsnaam.

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```

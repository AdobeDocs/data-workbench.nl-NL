---
description: Informatie over de kolommen van de elementpuntlaag.
title: Opzoekbestandsindeling voor elementpunt
uuid: 3480b9f3-35cd-40b7-aac9-15a3e2f19c1c
exl-id: da81da9e-0567-4f3a-bc0d-ab6c5e4a23b7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Opzoekbestandsindeling voor elementpunt{#element-point-lookup-file-format}

{{eol}}

Informatie over de kolommen van de elementpuntlaag.

Het opzoekbestand van de elementpuntlaag moet ten minste de volgende drie kolommen bevatten:

* **[!DNL Key]kolom:** Deze kolom zou gemeenschappelijke zeer belangrijke gegevens moeten bevatten, die de server van de gegevenswerkbank toelaat om de gegevens in het raadplegingsdossier met dat in de dataset te verbinden. De [!DNL Key] de kolom moet de eerste kolom in het raadplegingsdossier zijn. Elke rij in deze kolom identificeert een element van de dimensie.

* **[!DNL Longitude]kolom:** Deze kolom moet de lengtegraad bevatten voor elk gegevenspunt in het dialoogvenster [!DNL Key] kolom.

* **[!DNL Latitude]kolom:** Deze kolom moet de breedtegraad bevatten voor elk gegevenspunt in het dialoogvenster [!DNL Key] kolom.

* **[!DNL Name]kolom:** (Optioneel). Als u een naam wilt opgeven die voor elk gegevenspunt op de kaart moet worden weergegeven, kunt u een [!DNL Name] in het opzoekbestand.

Elke rij in de [!DNL Zip Points.txt] Het opzoekbestand bevat een ZIP-code in de eerste kolom gevolgd door de lengte, breedtegraad en de naam van de desbetreffende stad.

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```

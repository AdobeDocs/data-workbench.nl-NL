---
description: Informatie over de de laagkolommen van het elementenpunt.
solution: Analytics
title: Bestandsindeling voor zoeken op element
topic: Data workbench
uuid: 3480b9f3-35cd-40b7-aac9-15a3e2f19c1c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bestandsindeling voor zoeken op element{#element-point-lookup-file-format}

Informatie over de de laagkolommen van het elementenpunt.

Het de raadplegingsdossier van de elementenpuntlaag moet minstens de volgende drie kolommen bevatten:

* **[!DNL Key]kolom:**Deze kolom zou gemeenschappelijke zeer belangrijke gegevens moeten bevatten, die de server van de gegevenswerkbank toelaat om de gegevens in het raadplegingsdossier met dat in de dataset te verbinden. De[!DNL Key]kolom moet de eerste kolom in het raadplegingsdossier zijn. Elke rij in deze kolom identificeert een element van de afmeting.

* **[!DNL Longitude]kolom:**Deze kolom zou de lengtegraad voor elk gegevenspunt in de[!DNL Key]kolom moeten bevatten.

* **[!DNL Latitude]kolom:**Deze kolom zou de breedtegraad voor elk gegevenspunt in de[!DNL Key]kolom moeten bevatten.

* **[!DNL Name]kolom:**(Facultatief). Als u een naam wilt specificeren die op de kaart voor elk gegevenspunt moet worden getoond, kunt u een[!DNL Name]kolom in het raadplegingsdossier omvatten.

Elke rij in het [!DNL Zip Points.txt] raadplegingsdossier bevat een Code van het PIT in de eerste kolom die door de lengtegraad, de breedtegraad, en de bijbehorende stadsnaam wordt gevolgd.

```
tude, and associated city name.
ZIP_CODE LATITUDE LONGITUDE NAME
00210 +43.005895 -071.013202 PORTSMOUTH, NH
00211 +43.005895 -071.013202 PORTSMOUTH, NH
...
```


---
description: Instructies voor het toevoegen van visual_sciences.dll aan de de bibliotheekweg van Tomcat.
title: Het bibliotheekpad van Java wijzigen
uuid: 1e1a2704-045a-4b35-aa43-1b5bae91dc32
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het bibliotheekpad van Java wijzigen{#modify-the-java-library-path}

Instructies voor het toevoegen van visual_sciences.dll aan de de bibliotheekweg van Tomcat.

1. Voor uw server van Vensters, navigeer aan de installatiefolder van Tomcat. (Tomcat > bin)
1. Onder bakomslag, looppas Tomcat9w.exe (gemeenschappelijke de dienstmanager van daemon).

In het lusje van Java, onder de opties van Java, voeg een nieuwe lijn toe:

```
-Djava.library.path=C:\Sensor directory
```

Waar C:\Sensor directory is the directory containing the visual_sciences.dll-bestand.

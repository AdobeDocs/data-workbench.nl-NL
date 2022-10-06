---
description: Instructies voor het toevoegen van visual_sciences.dll aan het bibliotheekpad van Tomcat.
title: Het pad naar de Java-bibliotheek wijzigen
uuid: 1e1a2704-045a-4b35-aa43-1b5bae91dc32
exl-id: bd853d95-3f44-4860-9965-c3210ec4adcf
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Het pad naar de Java-bibliotheek wijzigen{#modify-the-java-library-path}

{{eol}}

Instructies voor het toevoegen van visual_sciences.dll aan het bibliotheekpad van Tomcat.

1. Navigeer op uw Windows-server naar de Tomcat-installatiemap. (Tomcat > bin)
1. Voer Tomcat9w.exe onder de map bin uit (de algemene manager van de daemon-service).

Voeg op het tabblad Java onder Java-opties een nieuwe regel toe:

```
-Djava.library.path=C:\Sensor directory
```

Waar C:\Sensor directory is the directory containing the visual_sciences.dll.

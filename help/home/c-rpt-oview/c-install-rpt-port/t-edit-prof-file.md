---
description: Om de profielen te specificeren die u in het Portaal van het Rapport beschikbaar wilt zijn, moet u het profiel.xml- dossier vormen.
title: Het bestand Profiles.xml bewerken
uuid: 3640552b-bc46-4b4f-8524-e021b0ca2bfc
exl-id: 7a3900e4-e472-4295-80f7-ce755958bc18
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Het bestand Profiles.xml bewerken{#edit-the-profiles-xml-file}

{{eol}}

Om de profielen te specificeren die u in het Portaal van het Rapport beschikbaar wilt zijn, moet u het profiel.xml- dossier vormen.

De [!DNL profiles.xml] Het bestand bevindt zich in de map die u hebt opgegeven voor uitvoer. Standaard bevindt deze zich in de map \*PortalName*\PortalFiles\Output.

**Profielnamen toevoegen aan het bestand profiles.xml**

1. Open op de computer waarop IIS wordt uitgevoerd de [!DNL profiles.xml] bestand in een teksteditor, zoals Kladblok.
1. Een profielelement en tag toevoegen voor elk [!DNL Profile] in uw portaal, zoals in het volgende voorbeeld:

   ```
   <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
   <PROFILES>
     <PROFILE>
       <NAME>Product Sales</NAME>
     </PROFILE>
     <PROFILE>
       <NAME>Product Marketing</NAME>
     </PROFILE>
   </PROFILES>
   ```

1. Sla het bestand op en sluit het.

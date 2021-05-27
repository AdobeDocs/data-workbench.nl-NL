---
description: Om de profielen te specificeren die u in het Portaal van het Rapport beschikbaar wilt zijn, moet u het profiel.xml- dossier vormen.
title: Het bestand Profiles.xml bewerken
uuid: 3640552b-bc46-4b4f-8524-e021b0ca2bfc
exl-id: 7a3900e4-e472-4295-80f7-ce755958bc18
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Het bestand Profiles.xml bewerken{#edit-the-profiles-xml-file}

Om de profielen te specificeren die u in het Portaal van het Rapport beschikbaar wilt zijn, moet u het profiel.xml- dossier vormen.

Het [!DNL profiles.xml] dossier verblijft in de omslag u voor output hebt aangewezen. Door gebrek verblijft het in \*PortalName*\PortalFiles\Output folder.

**Profielnamen toevoegen aan het bestand profiles.xml**

1. Op de machine waar IIS loopt, open het [!DNL profiles.xml] dossier in een tekstredacteur zoals Blocnote.
1. Voeg een profielelement en markering voor elke [!DNL Profile] in uw portaal, zoals in het volgende voorbeeld toe:

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

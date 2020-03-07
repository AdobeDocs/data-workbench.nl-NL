---
description: Om de profielen te specificeren die u in het Portaal van het Rapport beschikbaar wilt zijn, moet u het profile.xml- dossier vormen.
solution: Analytics
title: Geef het Profiles.xml- Dossier uit
topic: Data workbench
uuid: 3640552b-bc46-4b4f-8524-e021b0ca2bfc
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Geef het Profiles.xml- Dossier uit{#edit-the-profiles-xml-file}

Om de profielen te specificeren die u in het Portaal van het Rapport beschikbaar wilt zijn, moet u het profile.xml- dossier vormen.

Het [!DNL profiles.xml] dossier verblijft in de omslag u voor output hebt aangewezen. Door gebrek verblijft het in \*PortalName*\PortalFiles\Output folder.

**Om profielnamen aan het profiel.xml- dossier toe te voegen**

1. Voor de machine waar IIS loopt, open het [!DNL profiles.xml] dossier in een tekstredacteur zoals Blocnote.
1. Voeg een profielelement en een markering voor elk [!DNL Profile] in uw portaal, zoals in het volgende voorbeeld toe:

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

1. Sparen en sluit het dossier.

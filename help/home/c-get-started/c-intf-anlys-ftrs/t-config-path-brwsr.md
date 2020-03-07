---
description: browsers van de weg kunnen worden gevormd om met om het even welke combinatie basisafmeting, groepsafmeting, niveauafmeting, en metrisch te werken die voor uw toepassing en dataset steek houdt.
solution: Analytics
title: Vorm een wegbrowser
topic: Data workbench
uuid: 1ba3fb6e-b76f-428f-b6ec-077669c3b305
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vorm een wegbrowser{#configure-a-path-browser}

browsers van de weg kunnen worden gevormd om met om het even welke combinatie basisafmeting, groepsafmeting, niveauafmeting, en metrisch te werken die voor uw toepassing en dataset steek houdt.

Nadat u wegbrowser vormt, is het vermeld met andere wegbrowsers in het [!DNL Add Visualization] menu.

1. In [!DNL Profile Manager], klik **[!UICONTROL Menu]**, dan klik **[!UICONTROL Add Visualization]** en **[!UICONTROL Path Browser]**.

   Minstens één [!DNL *.vw] - dossier verblijft in de Browser van de Weg folder.

1. Klik het vinkje voor het gewenste dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.
1. Klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. Geef de parameters van het dossier uit gebruikend het volgende steekproefdossier en de lijst als gidsen:

   ```
   window = simpleBorderWindow: 
     client = pathBrowser: 
       Left Path = vector: 0 items
       Map = ref: wdata/model/dim/base dimension name
       Map Group = ref: wdata/model/dim/group dimension name
       Map Level = ref: wdata/model/dim/level dimension name
       Metric = ref: wdata/model/metric/metric name
       Right Path = vector: 0 items
       size = v3d: (673, 279, 0)
     pos = v3d: (714, 143, 0)
     size = v3d: (673, 298, 0)
   ```

<table id="table_1DCCB4B24B554B72A781B304B5EB155E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Verstrek deze informatie... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><i>Naam van de basisdimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van de afmeting de waarvan elementen op wegbrowser verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam groepsdimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van de afmeting die bepaalt hoe de elementen van de niveauafmeting worden gegroepeerd om de wegen in wegbrowser te vormen. Specifiek, kunnen de elementen van de niveaudimensie verbonden aan één enkele weg in wegbrowser niet meer dan één element van een groepsdimensie overspannen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam dimensie niveau</i> </p> </td> 
   <td colname="col2"> <p>De naam van het niveau (ouder) van de basisdimensie de waarvan elementen u aan wegbrowser sleept. Aangezien u een weg van één element van de basisdimensie aan volgende volgt, beweegt u zich van één element van de niveaudimensie aan volgende. Wanneer u een weg van de elementen van de basisafmeting selecteert, selecteert u gegevens voor de overeenkomstige elementen van de niveauafmeting. De selectie omvat altijd de elementen van de niveaudimensie die op de wortel betrekking hebben, en het wordt verfijnd door meer elementen aan de weg toe te voegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Metrische naam</i> </p> </td> 
   <td colname="col2"> <p>De naam van metrisch de waarvan waarde voor een bepaald element proportioneel aan de dikte van de weg is die tot dat element leidt. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor meer informatie over de basisafmeting, de groepsafmeting, de niveauafmeting, en metrisch voor wegbrowser, zie Browsers van de [Weg](../../../home/c-get-started/c-analysis-vis/c-path-browsers/c-path-browsers.md#concept-f2e9fdafed6e49c2bd111ab425cd6e2b).

1. In Blocnote, klik **[!UICONTROL File]** > **[!UICONTROL Save As]** om het dossier met een nieuwe naam op te slaan die op de groepsdimensie wordt gebaseerd, d.w.z., de afmetingsnaam *.vw van de* Groep.

   Zorg ervoor dat u sparen het dossier aan de Browser van de Weg folder.

   >[!NOTE]
   >
   >Om ervoor te zorgen dat uw wegbrowser als [!DNL *.vw] dossier, in het [!DNL Save As] venster wordt opgeslagen, plaats sparen als type aan Alle Dossiers.

1. (Facultatief) om de veranderingen ter beschikking te stellen van alle gebruikers van het het werkprofiel, in het [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

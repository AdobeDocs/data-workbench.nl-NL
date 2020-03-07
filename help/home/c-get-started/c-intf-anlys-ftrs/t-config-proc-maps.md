---
description: De kaarten van het proces kunnen worden gevormd om met om het even welke combinatie basisafmeting, groepsafmeting, niveauafmeting, en metrisch te werken die voor uw toepassing en dataset steek houdt.
solution: Analytics
title: Vorm een proceskaart
topic: Data workbench
uuid: e629191e-48b9-4b58-b6aa-3705ff7b387e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Vorm een proceskaart{#configure-a-process-map}

De kaarten van het proces kunnen worden gevormd om met om het even welke combinatie basisafmeting, groepsafmeting, niveauafmeting, en metrisch te werken die voor uw toepassing en dataset steek houdt.

Nadat u een proceskaart vormt, is het vermeld met andere proceskaarten in [!DNL Add Visualization menu].

1. In [!DNL Profile Manager], klik **[!UICONTROL Menu]**, klik **[!UICONTROL Add Visualization]**, dan klik het type van type van proceskaart dat u (2D Metrische Kaart, 2D Kaart van het Proces, of 3D Kaart van het Proces) wilt vormen.

   Minstens één [!DNL *.vw] dossier verblijft in de folder.

1. Klik het vinkje voor het gewenste dossier met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.
1. Klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. Geef de parameters van het dossier uit gebruikend het volgende steekproefdossier en de lijst als gidsen:

   ```
   window = simpleBorderWindow: 
     client = processMap: 
       Traffic Metric = ref: wdata/model/metric/metric name
       center = v3d: (-0.741014, 0, 0.0639476)
       color_links = bool: true
       Map = PrefixDim: 
         Name = string: Map
         Base Dimension = ref: wdata/model/dim/base dimension name
         Element Prefixes = vector: 0 items
         Element Names = vector: 0 items
       Map Level = ref: wdata/model/dim/level dimension name
       Map Group = ref: wdata/model/dim/group dimension name
       node_label = vector<bool>: 
       node_positions = vector: 0 items
       quantify_links = int: 2
       range = double: 2.37386
       size = v3d: (430, 290, 0)
       xAxisMetric = ref: wdata/model/metric/metric name for metric map
     pos = v3d: (880, 595, 0)
     size = v3d: (430, 309, 0)
   ```

<table id="table_3F072DB1B68746C49DF9332718982EBE"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Voor deze parameter... </th> 
   <th colname="col2" class="entry"> Verstrek deze informatie... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><i>Metrische naam</i> </p> </td> 
   <td colname="col2"> <p>De naam van metrisch de waarvan waarde voor een bepaalde knoop aan de grootte van de knoop evenredig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam van de basisdimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van de afmeting de waarvan elementen als knopen op de proceskaart verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam dimensie niveau</i> </p> </td> 
   <td colname="col2"> <p>De naam van het niveau (ouder) van de basisdimensie de waarvan elementen u aan de proceskaart sleept. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam groepsdimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van de afmeting die bepaalt hoe de elementen van de niveauafmeting worden gegroepeerd om de verbindingen tussen knopen te vormen. Een verbinding tussen twee knopen kan niet meer dan één element van een groepsdimensie overspannen. Wanneer u een selectie maakt die op een knoop binnen een proceskaart wordt gebaseerd, selecteert u alle elementen van de groepsdimensie die die knoop impliceerde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Metrische naam voor metrische kaart</i> </p> </td> 
   <td colname="col2"> <p>Deze parameter is op 2D metrische slechts kaarten van toepassing. </p> <p>De naam van metrisch de waarvan waarde de horizontale positie van de knopen op de kaart bepaalt. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor meer informatie over de basisdimensie, groepsdimensie, niveaudimensie, en metrisch voor een proceskaart, zie de Kaarten van het [Proces](../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-proc-maps.md#concept-880aee224404429785b733a4e80d275e).

1. In Blocnote, klik **[!UICONTROL File]** > **[!UICONTROL Save As]** om het dossier met een nieuwe naam op te slaan die op de basisafmeting wordt gebaseerd, namelijk de afmetingsnaam *.vw van de* Basis.

   (Als u een 2D metrische kaart vormt, zou u het dossier met een naam moeten bewaren die op de metrische naam voor de metrische kaart wordt gebaseerd, namelijk de *Metrische naam voor metrische map*.vw.) Zorg ervoor dat u sparen het dossier aan de aangewezen folder van de proceskaart.

   >[!NOTE]
   >
   >Om ervoor te zorgen dat uw proceskaart als [!DNL *.vw] dossier, in het [!DNL Save As] venster wordt bewaard, plaats sparen als type aan Alle Dossiers.

1. (Facultatief) om de veranderingen ter beschikking te stellen van alle gebruikers van het het werkprofiel, in het [!DNL Profile Manager], klik het vinkje voor het dossier in de [!DNL User] kolom met de rechtermuisknop aan en klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

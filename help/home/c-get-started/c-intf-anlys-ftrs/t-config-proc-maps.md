---
description: De kaarten van het proces kunnen worden gevormd om met om het even welke combinatie basisdimensie, groepsdimensie, niveaudimensie, en metrisch te werken die voor uw toepassing en dataset zinvol is.
title: Een proceskaart configureren
uuid: e629191e-48b9-4b58-b6aa-3705ff7b387e
exl-id: 0b37e942-4596-45cc-bc31-db147626f4eb
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Een proceskaart configureren{#configure-a-process-map}

De kaarten van het proces kunnen worden gevormd om met om het even welke combinatie basisdimensie, groepsdimensie, niveaudimensie, en metrisch te werken die voor uw toepassing en dataset zinvol is.

Nadat u een proceskaart vormt, is het vermeld met andere proceskaarten in [!DNL Add Visualization menu].

1. Klik in [!DNL Profile Manager] op **[!UICONTROL Menu]**, klik op **[!UICONTROL Add Visualization]** en klik vervolgens op het type proceskaart dat u wilt configureren (2D-metrische kaart, 2D-proceskaart of 3D-proceskaart).

   Ten minste één [!DNL *.vw]-bestand bevindt zich in de map.

1. Klik met de rechtermuisknop op het vinkje voor het gewenste bestand en klik op **[!UICONTROL Make Local]**.
1. Klik met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. Bewerk de parameters van het bestand met behulp van het volgende voorbeeldbestand en de volgende tabel als hulplijnen:

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
   <th colname="col2" class="entry"> Deze informatie opgeven... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><i>Metrische naam</i> </p> </td> 
   <td colname="col2"> <p>De naam van metrisch de waarvan waarde voor een bepaalde knoop aan de grootte van de knoop evenredig is. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam van basisdimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van de dimensie waarvan de elementen als knopen op de proceskaart verschijnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam van niveaudimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van het niveau (ouder) van de basisdimensie waarvan elementen u aan de proceskaart sleept. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam van groepsdimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van de dimensie die bepaalt hoe de elementen van de niveaudimensie worden gegroepeerd om de verbindingen tussen knopen te vormen. Een verbinding tussen twee knooppunten kan niet meer dan één element van een groepsdimensie beslaan. Wanneer u een selectie maakt die op een knoop binnen een proceskaart wordt gebaseerd, selecteert u alle elementen van de groepsdimensie die dat knoop impliceert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Metrische naam voor metrische kaart</i> </p> </td> 
   <td colname="col2"> <p>Deze parameter is alleen van toepassing op 2D-metrische kaarten. </p> <p>De naam van metrisch waarvan waarde de horizontale positie van de knopen op de kaart bepaalt. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor meer informatie over de basisdimensie, groepsdimensie, niveaudimensie, en metrisch voor een proceskaart, zie [Proceskaarten](../../../home/c-get-started/c-analysis-vis/c-proc-maps/c-proc-maps.md#concept-880aee224404429785b733a4e80d275e).

1. Klik in Kladblok op **[!UICONTROL File]** > **[!UICONTROL Save As]** om het bestand op te slaan met een nieuwe naam op basis van de basisdimensie, dat wil zeggen *Naam van basisdimensie*.vw.

   (Als u een metrische kaart 2D vormt, zou u het dossier met een naam moeten opslaan die op de metrische naam voor de metrische kaart wordt gebaseerd, namelijk *Metrische naam voor metrische kaart*.vw.) Zorg ervoor dat u het bestand opslaat in de juiste map met proceskaarten.

   >[!NOTE]
   >
   >Om ervoor te zorgen dat uw proceskaart als [!DNL *.vw] dossier, in het [!DNL Save As] venster wordt bewaard, plaats sparen als type aan Alle Dossiers.

1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL User] en klikt u op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

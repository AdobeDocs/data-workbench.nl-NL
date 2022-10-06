---
description: Browsers van de weg kunnen worden gevormd om met om het even welke combinatie basisdimensie, groepsdimensie, niveaudimensie, en metrisch te werken die voor uw toepassing en dataset steek houdt.
title: Een padbrowser configureren
uuid: 1ba3fb6e-b76f-428f-b6ec-077669c3b305
exl-id: be6a68f7-e3e3-4207-a112-3a4fdd5c5f57
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Een padbrowser configureren{#configure-a-path-browser}

{{eol}}

Browsers van de weg kunnen worden gevormd om met om het even welke combinatie basisdimensie, groepsdimensie, niveaudimensie, en metrisch te werken die voor uw toepassing en dataset steek houdt.

Nadat u een wegbrowser vormt, is het vermeld met andere wegbrowsers in [!DNL Add Visualization] -menu.

1. In de [!DNL Profile Manager], klikt u op **[!UICONTROL Menu]** en klik vervolgens op **[!UICONTROL Add Visualization]** en **[!UICONTROL Path Browser]**.

   Ten minste één [!DNL *.vw] bestand bevindt zich in de map Path Browser.

1. Klik met de rechtermuisknop op het vinkje voor het gewenste bestand en klik op **[!UICONTROL Make Local]**.
1. Klik met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**.
1. Bewerk de parameters van het bestand met behulp van het volgende voorbeeldbestand en de volgende tabel als hulplijnen:

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
   <th colname="col2" class="entry"> Deze informatie opgeven... </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><i>Naam van basisdimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van de dimensie waarvan de elementen in de padbrowser worden weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam van groepsdimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van de dimensie die bepaalt hoe de elementen van de niveaudimensie worden gegroepeerd om de paden te vormen in een padbrowser. Specifiek, kunnen de elementen van de niveaudimensie verbonden aan één enkele weg in wegbrowser niet meer dan één element van een groepsdimensie overspannen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Naam van niveaudimensie</i> </p> </td> 
   <td colname="col2"> <p>De naam van het niveau (bovenliggend niveau) van de basisdimensie waarvan u de elementen naar de padbrowser sleept. Als u een pad volgt van het ene element van de basisdimensie naar het volgende, gaat u van het ene element van de niveaudimensie naar het volgende. Wanneer u een pad met basisdimensie-elementen selecteert, selecteert u gegevens voor de corresponderende elementen van de niveaudimensie. De selectie bevat altijd de elementen van de niveaudimensie die betrekking hebben op de hoofdmap en wordt verfijnd door meer elementen aan het pad toe te voegen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><i>Metrische naam</i> </p> </td> 
   <td colname="col2"> <p>De naam van de metrische waarde waarvan de waarde voor een bepaald element evenredig is met de dikte van het pad dat naar dat element leidt. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Voor meer informatie over de basisafmeting, groepsafmeting, niveauafmeting, en metrisch voor wegbrowser, zie [Padbrowsers](../../../home/c-get-started/c-analysis-vis/c-path-browsers/c-path-browsers.md#concept-f2e9fdafed6e49c2bd111ab425cd6e2b).

1. Klik in Kladblok op **[!UICONTROL File]** > **[!UICONTROL Save As]** om het bestand op te slaan onder een andere naam op basis van de groepsdimensie, dat wil zeggen: *Naam van groepsdimensie*.vw.

   Sla het bestand op in de map Path Browser.

   >[!NOTE]
   >
   >Om ervoor te zorgen dat uw padbrowser wordt opgeslagen als een [!DNL *.vw] in het [!DNL Save As] , stelt u Opslaan als type in op Alle bestanden.

1. (Optioneel) Als u de wijzigingen beschikbaar wilt maken voor alle gebruikers van het werkprofiel, gaat u naar [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL working profile name]**>*.

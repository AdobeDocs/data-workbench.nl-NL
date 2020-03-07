---
description: De Unlock parameter in het dossier van Insight.cfg van een gebruiker specificeert of die gebruiker toestemming heeft om gesloten werkruimten tijdelijk te openen voor het uitgeven.
solution: Analytics
title: De parameter voor ontgrendelen instellen
topic: Data workbench
uuid: db094e32-7d82-4f93-a492-a6bed33ae722
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De parameter voor ontgrendelen instellen{#set-the-unlock-parameter}

De Unlock parameter in het dossier van Insight.cfg van een gebruiker specificeert of die gebruiker toestemming heeft om gesloten werkruimten tijdelijk te openen voor het uitgeven.

Als de Unlock parameter reeds aanwezig in het [!DNL Insight.cfg] dossier van de gebruiker is, kunt u de parameter uitgeven gebruikend de Werkbank van Gegevens. Als het niet reeds aanwezig in het [!DNL Insight.cfg] dossier van de gebruiker is, moet u het aan het dossier toevoegen gebruikend een tekstredacteur, zoals Blocnote.

**Om een bestaande[!DNL Unlock]parameter in het Insight.cfg- dossier te plaatsen**

1. In een werkruimte, klik **[!UICONTROL Admin]** > met de rechtermuisknop aan **[!UICONTROL Client Configuration]**. Het [!DNL Insight.cfg] bestand wordt geopend.
1. Voor de Unlock parameter, typ of waar of vals. Waar laat de gebruiker toe om het even welke gesloten werkruimte tijdelijk te openen, terwijl vals niet.
1. Om uw configuratieveranderingen te bewaren, klik **[!UICONTROL Insight.cfg (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save as Insight.cfg]**.

**Om de parameter van de Ontgrendeling aan het Insight.cfg- dossier toe te voegen**

1. Navigeer aan uw de installatiefolder van de Werkbank van Gegevens en open het [!DNL Insight.cfg] dossier gebruikend een tekstredacteur, zoals Blocnote.
1. Voeg de parameter van de Ontgrendeling aan het eind van het dossier, zoals in het volgende voorbeeld toe:

[!DNL Unlock = bool: false]

1. Plaats de waarde aan of waar of vals. Waar laat de gebruiker toe om het even welke gesloten werkruimte tijdelijk te openen, terwijl vals niet.
1. Sparen en sluit het dossier.


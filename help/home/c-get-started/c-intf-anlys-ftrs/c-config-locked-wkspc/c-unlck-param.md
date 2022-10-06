---
description: Met de parameter Unlock in het bestand Insight.cfg van een gebruiker wordt opgegeven of die gebruiker gemachtigd is om vergrendelde werkruimten tijdelijk te ontgrendelen voor bewerking.
title: De ontgrendelingsparameter instellen
uuid: db094e32-7d82-4f93-a492-a6bed33ae722
exl-id: 5eda919f-4cfe-4692-9dbf-f7cf64fde1de
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# De ontgrendelingsparameter instellen{#set-the-unlock-parameter}

{{eol}}

Met de parameter Unlock in het bestand Insight.cfg van een gebruiker wordt opgegeven of die gebruiker gemachtigd is om vergrendelde werkruimten tijdelijk te ontgrendelen voor bewerking.

Als de parameter Ontgrendelen al aanwezig is in het deelvenster [!DNL Insight.cfg] kunt u de parameter bewerken met Data Workbench. Als dit nog niet het geval is in de [!DNL Insight.cfg] moet u het bestand toevoegen aan het bestand met een teksteditor, zoals Kladblok.

**Een bestaande [!DNL Unlock] parameter in het bestand Insight.cfg**

1. Klik in een werkruimte met de rechtermuisknop **[!UICONTROL Admin]** > **[!UICONTROL Client Configuration]**. De [!DNL Insight.cfg] wordt geopend.
1. Typ true of false voor de parameter Unlock. True stelt de gebruiker in staat om vergrendelde werkruimten tijdelijk te ontgrendelen, false niet.
1. Klik met de rechtermuisknop om uw configuratiewijzigingen op te slaan **[!UICONTROL Insight.cfg (modified)]** boven aan het venster en klik op **[!UICONTROL Save as Insight.cfg]**.

**De parameter Unlock toevoegen aan het bestand Insight.cfg**

1. Navigeer naar de installatiemap van uw Data Workbench en open de [!DNL Insight.cfg] bestand met een teksteditor, zoals Kladblok.
1. Voeg de parameter Ontgrendelen toe aan het einde van het bestand, zoals in het volgende voorbeeld:

[!DNL Unlock = bool: false]

1. Stel de waarde in op true of false. True stelt de gebruiker in staat om vergrendelde werkruimten tijdelijk te ontgrendelen, false niet.
1. Sla het bestand op en sluit het.

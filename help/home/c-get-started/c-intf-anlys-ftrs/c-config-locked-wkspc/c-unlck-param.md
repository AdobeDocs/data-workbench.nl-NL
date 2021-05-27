---
description: Met de parameter Unlock in het bestand Insight.cfg van een gebruiker wordt opgegeven of die gebruiker gemachtigd is om vergrendelde werkruimten tijdelijk te ontgrendelen voor bewerking.
title: De ontgrendelingsparameter instellen
uuid: db094e32-7d82-4f93-a492-a6bed33ae722
exl-id: 5eda919f-4cfe-4692-9dbf-f7cf64fde1de
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# De ontgrendelingsparameter instellen{#set-the-unlock-parameter}

Met de parameter Unlock in het bestand Insight.cfg van een gebruiker wordt opgegeven of die gebruiker gemachtigd is om vergrendelde werkruimten tijdelijk te ontgrendelen voor bewerking.

Als de parameter Ontgrendelen al aanwezig is in het bestand [!DNL Insight.cfg] van de gebruiker, kunt u de parameter bewerken met Data Workbench. Als het niet reeds in het [!DNL Insight.cfg] dossier van de gebruiker aanwezig is, moet u het aan het dossier toevoegen gebruikend een tekstredacteur, zoals Kladblok.

**Een bestaande  [!DNL Unlock] parameter instellen in het bestand Insight.cfg**

1. Klik in een werkruimte met de rechtermuisknop op **[!UICONTROL Admin]** > **[!UICONTROL Client Configuration]**. Het [!DNL Insight.cfg] dossier opent.
1. Typ true of false voor de parameter Unlock. True stelt de gebruiker in staat om vergrendelde werkruimten tijdelijk te ontgrendelen, false niet.
1. Als u de configuratiewijzigingen wilt opslaan, klikt u met de rechtermuisknop **[!UICONTROL Insight.cfg (modified)]** boven in het venster en klikt u op **[!UICONTROL Save as Insight.cfg]**.

**De parameter Unlock toevoegen aan het bestand Insight.cfg**

1. Navigeer naar de installatiemap van de Data Workbench en open het [!DNL Insight.cfg] dossier gebruikend een tekstredacteur, zoals Blocnote.
1. Voeg de parameter Ontgrendelen toe aan het einde van het bestand, zoals in het volgende voorbeeld:

[!DNL Unlock = bool: false]

1. Stel de waarde in op true of false. True stelt de gebruiker in staat om vergrendelde werkruimten tijdelijk te ontgrendelen, false niet.
1. Sla het bestand op en sluit het.

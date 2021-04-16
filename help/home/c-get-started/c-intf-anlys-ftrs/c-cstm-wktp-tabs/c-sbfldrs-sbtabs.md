---
description: Nieuwe tabbladen geven de submappen in de bijbehorende map standaard weer als hiërarchische submappen in plaats van als subtabbladen.
title: Submappen weergeven als subtabbladen
uuid: b4d7c6dd-d5ad-4b93-ba67-65a69e11eefc
exl-id: 6a05852b-3efc-4e71-9782-d4cc3a687a26
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# Submappen weergeven als subtabbladen{#display-subfolders-as-subtabs}

Nieuwe tabbladen geven de submappen in de bijbehorende map standaard weer als hiërarchische submappen in plaats van als subtabbladen.

U kunt submappen weergeven als subtabbladen (zoals in het volgende voorbeeld) door een [!DNL empty folder.useTabs]-bestand te plaatsen in de map *werkprofiel name*\Workspaces\*tabnaam* in de installatiemap van de Data Workbench.

In het volgende voorbeeld ziet u het tabblad [!DNL Custom] met vervolgkeuzemenu&#39;s.

![](assets/client-sub.png)

Als u een [!DNL empty folder.useTabs] dossier in de omslag van de Werkruimten \ van de Douane plaatst, tonen alle subfolders binnen de omslag van de Douane in [!DNL Worktop] als subtabs, zoals aangetoond in het volgende voorbeeld:

![](assets/client-sub2.png)

**Submappen weergeven als subtabbladen in het dialoogvenster[!DNL Worktop]**

>[!NOTE]
>
>De inhoud van de submap wordt alleen weergegeven als subtabs op elk directoryniveau als er een [!DNL Tab Name.useTabs]-bestand aanwezig is in plaats van hiërarchische vervolgkeuzelijsten.

1. Klik in [!DNL Profile Manager] op **[!UICONTROL Workspaces]** om de inhoud ervan weer te geven.
1. Klik in de kolom *werkprofielnaam* met de rechtermuisknop op het vinkje voor een van de [!DNL folder.useTabs] bestanden en klik op **[!UICONTROL Copy]**.
1. Klik met de rechtermuisknop in de kolom [!DNL User] voor de map Workspaces\*tab name* en klik op **[!UICONTROL Paste]**. De submappen op dat tabblad worden nu als subtabbladen weergegeven.
1. (Optioneel) Als u deze wijziging beschikbaar wilt maken voor alle gebruikers van het werkprofiel, klikt u met de rechtermuisknop op het witte vinkje voor het bestand [!DNL new folder.useTabs] in de kolom [!DNL User] en klikt u op **[!UICONTROL Save to]** > &lt; **[!UICONTROL working profile name]**>.

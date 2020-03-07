---
description: Nu het x-experimentgebied beschikbaar is, moet u een uitgebreide dimensie tot stand brengen om het x-experimentgebied in uw dataset te omvatten, die u toestaat om uw resultaten in Inzicht te bekijken.
solution: Insight,Analytics
title: Transformatie wijzigen.cfg
topic: Data workbench
uuid: c17e48db-8fd9-4640-b621-6963bb8223d7
translation-type: tm+mt
source-git-commit: 72761a57e4bb9f230581b2cd37bff04ba7be8e37

---


# Transformatie wijzigen.cfg{#modifying-transformation-cfg}

Nu het x-experimentgebied beschikbaar is, moet u een uitgebreide dimensie tot stand brengen om het x-experimentgebied in uw dataset te omvatten, die u toestaat om uw resultaten in Inzicht te bekijken.

Om dit te doen, moet u een nieuwe dimensie aan het [!DNL Transformation.cfg] dossier toevoegen.

Als u van plan bent om veelvoudige experimenten in werking te stellen, moet u ook een nieuwe Gespleten transformatie aan het [!DNL Transformation.cfg] dossier toevoegen. Deze Gespleten transformatie scheidt de verschillende experiment en groepnamen zodat de informatie gemakkelijker te interpreteren is. Om te vermijden opnieuw verwerkend uw gegevens als u extra experimenten op een recentere datum moest toevoegen, adviseert Adobe dat u de Gespleten transformatie toevoegt zelfs als u momenteel niet van plan bent om veelvoudige experimenten in werking te stellen.

De volgende procedure omvat de verwezenlijking van zowel de nieuwe Gespleten transformatie als de uitgebreide dimensie. Als u niet de Gespleten transformatie wilt toevoegen, sla eenvoudig stappen 5-7 over.

**Om Transformation.cfg te wijzigen**

1. In [!DNL Insight], open [!DNL Profile Manager] door binnen een werkruimte met de rechtermuisknop aan te klikken en **[!UICONTROL Admin]** > **[!UICONTROL Profile Manager]** te klikken, of door de werkruimte van het Beheer van het Profiel op de [!DNL Admin] tabel te openen.
1. In [!DNL Profile Manager], klik **[!UICONTROL Dataset]** om zijn inhoud te tonen.
1. Klik het vinkje naast met de rechtermuisknop aan [!DNL Transformation.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.
1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het [!DNL Transformation.cfg] venster wordt weergegeven.
1. Klik **[!UICONTROL Transformation]** om zijn inhoud te tonen.
1. Klik met de rechtermuisknop **[!UICONTROL Transformations]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Split]**.
1. Voltooi de nieuwe spleet op komma transformatie zoals aangetoond in het volgende voorbeeld:

   ![Stapgegevens](assets/New_split_transformation.png)

   >[!NOTE]
   >
   >U kunt om het even welke waarde op het gebied van de Naam ingaan.

1. Klik met de rechtermuisknop **[!UICONTROL Extended Dimensions]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL ManyToMany]**.
1. Voltooi de nieuwe dimensie zoals aangetoond in het volgende voorbeeld:

   ![Stapgegevens](assets/New_Dimension_controlled_experiment_groups.png)

   >[!NOTE]
   >
   >* U kunt om het even welke waarde op het gebied van de Naam ingaan.
   >* Als u de gespleten transformatie niet omvatte, moet u &quot;x-experiment&quot;op het [!DNL Input] gebied typen.


1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.
1. In [!DNL Profile Manager], klik het vinkje voor [!DNL Transformation.cfg] in de [!DNL User] kolom met de rechtermuisknop aan, dan klik **[!UICONTROL Save to]** > **[!UICONTROL profile name]** om de plaatselijk aangebrachte veranderingen in het het werk profiel te bewaren.

   >[!NOTE]
   >
   >De dataset begint onmiddellijk retransformerend.

   Voor meer informatie over [!DNL Transformation.cfg] en uitgebreide afmetingen, zie de Gids *van de Configuratie van de* Dataset.

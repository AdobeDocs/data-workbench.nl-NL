---
description: Het profiel Geography dat wordt geleverd bij Data WorkbenchGeography is een intern profiel dat aanvullende functionaliteit biedt voor uw Adobe-toepassing.
title: Het geografische profiel installeren
uuid: afc0699d-e58b-481b-a3f2-ab6d6998bdd8
exl-id: 9ab07fd4-d6e7-495e-ba34-04e53c9b0aa3
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Het profiel Geografie installeren{#installing-the-geography-profile}

Het profiel Geography dat wordt geleverd bij Data WorkbenchGeography is een intern profiel dat aanvullende functionaliteit biedt voor uw Adobe-toepassing.

Zoals bij alle andere interne profielen die door Adobe worden verstrekt, zou het [!DNL Geography] profiel niet moeten worden veranderd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Het profiel [!DNL Geography] bevat verschillende sets met transformatiegegevens, waaronder bestanden (in de map [!DNL Dataset\Transformation\Geography]) die geografische afmetingen definiëren. Hieronder volgt een lijst met transformatiegegevens met daarin bestanden van het profiel [!DNL Geography]:

* [!DNL City.cfg]
* [!DNL Coordinates.cfg]
* [!DNL Country.cfg]
* [!DNL DMA.cfg]
* [!DNL Domain.cfg]

Elk van de bestanden krijgt een naam voor de uitgebreide dimensie die wordt gedefinieerd. Een extra dossier, [!DNL IPLookup.cfg], bepaalt verscheidene geografische gegevensgebieden die worden gebruikt om dimensies in de andere transformatiedataset te bepalen omvat dossiers.

Voor informatie over transformatiedataset omvat dossiers, zie *de Gids van de Configuratie van de Dataset*.

**Het  [!DNL Geography] profiel installeren op de gegevenswerkbankserver**

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u een gegevenswerkbank hebt geïnstalleerd en een verbinding tot stand hebt gebracht tussen de gegevenswerkbank en de gegevenswerkbankserver waarop u de gegevenswerkbank [!DNL Geography] installeert. Als u dit niet hebt gedaan, zie *de Gids van de Gebruiker van de Data Workbench*.

1. Open de map Profielen in het bestand [!DNL .zip] dat u van Adobe hebt ontvangen.
1. Kopieer de map [!DNL Geography] naar de map Profiles in de installatiemap van de gegevenswerkbank op de server. U wilt uiteindelijk een [!DNL ...\Profiles\Geography]-map op uw gegevenswerkbankserver plaatsen, zoals in het volgende voorbeeld wordt getoond. De namen van de andere mappen in de map Profielen kunnen afwijken van de mappen die worden weergegeven.

   ![Stapinfo](assets/Geo_installProfiles_dir.png)

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor elk profiel bij te werken waarmee u gegevenswerkbank [!DNL Geography] wilt gebruiken.

   1. Open [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het venster [!DNL profile.cfg] verschijnt.

   1. Klik in het venster [!DNL profile.cfg] met de rechtermuisknop **[!UICONTROL Directories]** en klik **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Als u de nieuwe map wilt toevoegen aan het einde van de lijst met directory&#39;s, klikt u met de rechtermuisknop op het nummer of de naam van de laatste map in de lijst en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe map: [!DNL Geography].
   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de kolom [!DNL User] en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd (inclusief het profiel [!DNL Geography]), omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

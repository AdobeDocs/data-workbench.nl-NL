---
description: Het profiel Geography dat wordt geleverd bij Data WorkbenchGeography is een intern profiel dat aanvullende functionaliteit biedt voor uw Adobe-toepassing.
title: Het geografische profiel installeren
uuid: afc0699d-e58b-481b-a3f2-ab6d6998bdd8
exl-id: 9ab07fd4-d6e7-495e-ba34-04e53c9b0aa3
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 0%

---

# Het geografische profiel installeren{#installing-the-geography-profile}

{{eol}}

Het profiel Geography dat wordt geleverd bij Data WorkbenchGeography is een intern profiel dat aanvullende functionaliteit biedt voor uw Adobe-toepassing.

Net als bij alle andere interne profielen die door Adobe worden geleverd, worden de [!DNL Geography] mag niet worden gewijzigd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

De [!DNL Geography] Het profiel bevat verschillende bestanden met transformatiegegevens (in de map [!DNL Dataset\Transformation\Geography] map) die geografische afmetingen definiëren. Hieronder volgt een lijst met transformatiegegevens met daarin bestanden die worden geleverd bij de [!DNL Geography] profiel:

* [!DNL City.cfg]
* [!DNL Coordinates.cfg]
* [!DNL Country.cfg]
* [!DNL DMA.cfg]
* [!DNL Domain.cfg]

Elk van de bestanden krijgt een naam voor de uitgebreide dimensie die wordt gedefinieerd. Een extra bestand, [!DNL IPLookup.cfg], definieert verschillende geografische gegevensvelden die worden gebruikt om afmetingen te definiëren in de andere set met transformatiegegevens.

Voor informatie over transformatiedataset omvat dossiers, zie *Configuratie-handleiding voor gegevensset*.

**Als u het dialoogvenster [!DNL Geography] profiel op de gegevenswerkbankserver**

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u de gegevenswerkbank hebt geïnstalleerd en een verbinding tot stand hebt gebracht tussen de gegevenswerkbank en de gegevenswerkbankserver waarop u de gegevenswerkbank installeert [!DNL Geography]. Als u dit niet hebt gedaan, raadpleegt u de *Gebruikershandleiding voor Data Workbench*.

1. Open de map Profielen in het menu [!DNL .zip] bestand dat door Adobe aan u wordt geleverd.
1. Kopieer de [!DNL Geography] naar de map Profiles in de installatiemap van de gegevenswerkbank. U wilt eindigen met een [!DNL ...\Profiles\Geography] op uw gegevenswerkbankserver, zoals in het volgende voorbeeld wordt getoond. De namen van de andere mappen in de map Profielen kunnen afwijken van de mappen die worden weergegeven.

   ![Stapinfo](assets/Geo_installProfiles_dir.png)

1. Gebruik de volgende stappen om de [!DNL profile.cfg] bestand voor elk profiel waarmee u de gegevenswerkbank wilt gebruiken [!DNL Geography].

   1. Open de [!DNL Profile Manager].
   1. Klik met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.

   1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. De [!DNL profile.cfg] wordt weergegeven.

   1. In de [!DNL profile.cfg] venster, klik met de rechtermuisknop **[!UICONTROL Directories]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Als u de nieuwe map wilt toevoegen aan het einde van de lijst met mappen, klikt u met de rechtermuisknop op het nummer of de naam van de laatste map in de lijst en klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe map: [!DNL Geography].
   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die worden geleverd door Adobe (inclusief de [!DNL Geography] ), aangezien uw veranderingen worden beschreven wanneer u updates aan deze profielen installeert.

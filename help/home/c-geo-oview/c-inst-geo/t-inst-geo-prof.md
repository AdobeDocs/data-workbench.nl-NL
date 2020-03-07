---
description: Het profiel van de Geografie dat van gegevenswerkbankGeography wordt verstrekt is een intern profiel dat extra functionaliteit aan uw toepassing van Adobe verstrekt.
solution: Analytics
title: Het geografische profiel installeren
topic: Data workbench
uuid: afc0699d-e58b-481b-a3f2-ab6d6998bdd8
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het geografische profiel installeren{#installing-the-geography-profile}

Het profiel van de Geografie dat van gegevenswerkbankGeography wordt verstrekt is een intern profiel dat extra functionaliteit aan uw toepassing van Adobe verstrekt.

Zoals met alle andere interne profielen die door Adobe worden verstrekt, zou het [!DNL Geography] profiel niet moeten worden veranderd. Al aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert.

Het [!DNL Geography] profiel omvat verscheidene transformatiedataset dossiers (die in de [!DNL Dataset\Transformation\Geography] omslag worden gevestigd) die geografische afmetingen bepalen. Na is een lijst van de transformatiedataset omvat dossiers die van het [!DNL Geography] profiel worden voorzien:

* [!DNL City.cfg]
* [!DNL Coordinates.cfg]
* [!DNL Country.cfg]
* [!DNL DMA.cfg]
* [!DNL Domain.cfg]

Elk van de dossiers wordt genoemd voor de uitgebreide dimensie die het bepaalt. Een extra dossier, [!DNL IPLookup.cfg], bepaalt verscheidene geografische gegevensgebieden die worden gebruikt om afmetingen in de andere transformatiedataset te bepalen omvat dossiers.

Voor informatie over transformatiedataset omvat dossiers, zie de Gids *van de Configuratie van de* Dataset.

**Om het[!DNL Geography]profiel op de server van de gegevenswerkbank te installeren**

>[!NOTE]
>
>In de volgende installatie-instructies wordt ervan uitgegaan dat u een werkbank voor gegevens hebt geïnstalleerd en een verbinding hebt gemaakt tussen de werkbank voor gegevens en de server voor een werkbank voor gegevens waarop u een werkbank voor gegevens installeert [!DNL Geography]. Als u dit niet hebt gedaan, zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.

1. Open de omslag van Profielen van het [!DNL .zip] dossier dat aan u door Adobe wordt verstrekt.
1. Kopieer de [!DNL Geography] omslag aan de omslag van Profielen in uw de installatiefolder van de gegevenswerkbank. U wilt omhoog met een [!DNL ...\Profiles\Geography] omslag op uw server van de gegevenswerkbank zoals aangetoond in het volgende voorbeeld beëindigen. De namen van de andere omslagen binnen de omslag van Profielen kunnen van getoond verschillen.

   ![Stapgegevens](assets/Geo_installProfiles_dir.png)

1. Gebruik de volgende stappen om het [!DNL profile.cfg] dossier voor elk profiel bij te werken waarmee u gegevenswerkbank wilt gebruiken [!DNL Geography].

   1. Open de [!DNL Profile Manager].
   1. Klik het vinkje naast met de rechtermuisknop aan [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

   1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL from the workbench]**. Het [!DNL profile.cfg] venster wordt weergegeven.

   1. Klik in het [!DNL profile.cfg] venster met de rechtermuisknop **[!UICONTROL Directories]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

      Om de nieuwe folder aan het eind van de lijst van folders toe te voegen, klik het aantal of de naam van de laatste folder in de lijst met de rechtermuisknop aan en klik **[!UICONTROL Add new]** > **[!UICONTROL Directory]**.

   1. Typ de naam van de nieuwe folder: [!DNL Geography].
   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in de [!DNL Profile Manager], rechtsklik op het vinkje voor [!DNL profile.cfg] in de [!DNL User] kolom en klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*.

      >[!NOTE]
      >
      >Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe (inclusief het [!DNL Geography] profiel) worden geleverd, omdat uw wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.


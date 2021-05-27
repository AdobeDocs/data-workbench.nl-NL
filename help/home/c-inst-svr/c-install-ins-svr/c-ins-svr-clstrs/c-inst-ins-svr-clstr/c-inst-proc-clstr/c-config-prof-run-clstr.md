---
description: Wanneer u een datasetprofiel om op een cluster van de Server van het Inzicht vormt te lopen, delen alle machines in de cluster alle dossiers van de datasetconfiguratie voor dat profiel.
title: Een profiel configureren om op een cluster uit te voeren
uuid: e181d069-fb2f-4a71-a86f-bb9a48cfe059
exl-id: be8090fc-b3da-41c4-a5d4-c6eb85b8a84d
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---

# Het vormen van een Profiel om op een Cluster {#configuring-a-profile-to-run-on-a-cluster} te lopen

Wanneer u een datasetprofiel om op een cluster van de Server van het Inzicht vormt te lopen, delen alle machines in de cluster alle dossiers van de datasetconfiguratie voor dat profiel.

Daarom moeten de vermeldingen voor de parameters in deze bestanden van toepassing zijn op alle [!DNL Insight Servers] in de cluster. De locaties van de te lezen logbestanden, de opzoekbestanden die door [!DNL Insight Server] moeten worden gebruikt en de locatie van de gegevensuitvoer door [!DNL Insight Server] moeten bijvoorbeeld op alle computers in de cluster gelijk zijn.

U voert alle configuratietaken op master [!DNL Insight Server] van de cluster uit, die [!DNL Insight Server] is u gebruikt om uw configuratiedossiers uit te geven. Alle opgeslagen wijzigingen in het configuratiebestand die op de master [!DNL Insight Server] zijn aangebracht, worden automatisch gesynchroniseerd met de bestanden op de verwerking [!DNL Insight Servers] in de cluster.

Om een datasetprofiel op een [!DNL Insight Server] cluster in werking te stellen, moet u de volgende processen in de vermelde orde uitvoeren:

1. [Bepalen welke Insight Servers gebeurtenisgegevens verwerken](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-59b8e3f2b34f49739d544c8740a62fba)
1. [De verwerkingsservers opgeven in Profile.cfg](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9)
1. (Indien nodig) [De configuratiebestanden van de gegevensset wijzigen voor het profiel](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99bf9248e4e5483cb518f453b0a2f278)

## Bepalen welke Insight Servers gebeurtenisgegevens verwerken {#section-59b8e3f2b34f49739d544c8740a62fba}

Het is niet vereist dat alle [!DNL Insight Servers] in de gebeurtenisgegevens van het clusterproces. U kunt één [!DNL Insight Server] in de cluster als Eenheid van de Server van het Dossier aanwijzen die de brondossiers (VSL en logboekdossiers) opslaat en de dossiers aan alle Eenheden van de Gegevensverwerking (verwerkingsservers) in de cluster dient. Deze installatie biedt het voordeel van één gegevensopslagplaats voor gebeurtenissen en gebruikt de verwerkingskracht van alle verwerkingsservers in de cluster. De gegevensbestanden worden door de verwerkingsservers verdeeld en er wordt gegarandeerd dat hetzelfde bestand niet meer dan één keer wordt verwerkt.

Voor meer informatie over het aanwijzen van [!DNL Insight Server] om als Eenheid van de Server van het Dossier in werking te stellen, zie het hoofdstuk van het Dossier van de Configuratie van de Verwerking van het Logboek van de *Gids van de Configuratie van de Dataset*.

Als u besluit om brongegevensdossiers op elk van de verwerkingsservers eerder dan op één enkele Eenheid van de Server van het Dossier op te slaan, moet u de dossiers gelijkelijk onder de verwerkingsservers verdelen. Sla niet alle brondossiers van de dataset op elk van de verwerkingsservers op. Als meerdere kopieën van hetzelfde bestand beschikbaar zijn op meerdere verwerkingsservers, worden de gegevens meerdere keren gelezen (één keer per computer) en worden de gegevens scheefgetrokken.

Neem contact op met de Adobe Consulting voor hulp bij het bepalen welke [!DNL Insight Servers] logbestanden moet verwerken.

## De verwerkingsservers opgeven in Profile.cfg {#section-99664e072c21462f91fbafb6d893fcf9}

Geef in het bestand [!DNL profile.cfg] de verwerkingsservers op die de gegevens voor het profiel verwerken.

**Toegang tot het bestand profile.cfg**

U hebt toegang tot het profielconfiguratiebestand met de [!DNL Profile Manager] in [!DNL Insight].

1. Open [!DNL Profile Manager] terwijl u in uw gegevenssetprofiel werkt door met de rechtermuisknop in een werkruimte te klikken en **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Profile Manager]** te klikken of door de werkruimte Profielbeheer op het tabblad [!DNL Admin] te openen.

1. Klik in [!DNL Profile Manager] met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in de kolom [!DNL User].

1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het venster voor profielconfiguratie wordt weergegeven.

**Verwerkingsservers toevoegen**

1. Klik in het [!DNL profile.cfg]-bestand op **[!UICONTROL Profile]** en klik vervolgens op **[!UICONTROL Processing Servers]** om de inhoud ervan weer te geven.

1. Klik met de rechtermuisknop **[!UICONTROL Processing Servers]** en klik **[!UICONTROL Add new]** > **[!UICONTROL Processing Server]**.

1. Typ in de parameter Common Name de algemene naam voor de eerste verwerkingsserver in de cluster. Bijvoorbeeld: [!DNL server1.mycompany.com]
1. Herhaal stap 2 en 3 totdat u de algemene namen van alle verwerkingsservers in de cluster hebt toegevoegd.

   >[!NOTE]
   >
   >Als de master [!DNL Insight Server] gegevens verwerkt, moet u het ook toevoegen.

1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

1. Klik met de rechtermuisknop op het vinkje in de kolom [!DNL User] naast [!DNL profile.cfg]. Klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]**>*.

## Het wijzigen van de Dossiers van de Configuratie van de Dataset voor het Profiel {#section-99bf9248e4e5483cb518f453b0a2f278}

**Om de dossiers van de datasetconfiguratie te wijzigen**

Als u veranderingen in de dossiers van de datasetconfiguratie ( [!DNL Log Processing.cfg], [!DNL Transformation.cfg], dataset omvat dossiers, [!DNL Log Processing Mode.cfg], etc.) moet aanbrengen, doe dit slechts op master [!DNL Insight Server].

1. Open de bestanden die u wilt wijzigen:

   Voor instructies om tot de dossiers toegang te hebben, zie *de Gids van de Configuratie van de Dataset*.
1. Breng de gewenste wijzigingen aan. Zie *Gegevenssetconfiguratiehandleiding* voor meer informatie over de parameters in het configuratiebestand of de configuratiebestanden.
1. Sla het bestand op.

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik met de rechtermuisknop op het vinkje in de kolom [!DNL User] naast de bestandsnaam.
   1. Klik op **[!UICONTROL Save to]** en selecteer het gewenste profiel.

>[!NOTE]
>
>[!DNL Insight] gebruikers die tot een datasetprofiel toegang hebben dat op een cluster loopt identificeren slechts master  [!DNL Insight Server] in het  [!DNL Insight] configuratiedossier (  [!DNL insight.cfg]). Vanuit het perspectief van de [!DNL Insight] gebruiker, is het profiel toegankelijk op slechts één [!DNL Insight Server] (master [!DNL Insight Server]); echter, kunnen de vraagverzoeken van analisten aan om het even welk [!DNL Insight Servers] in de cluster worden geleid.

Een [!DNL Insight Server] cluster staat de gecentraliseerde opslag van [!DNL .vsl] logboekdossiers (van [!DNL Sensor]) op één [!DNL Insight Server] machine toe genoemd een Eenheid van de Server van het Dossier (FSU). Zie [Installatieprocedures voor een Insight Server FSU](../../../../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016) voor informatie over het installeren van een FSU. Voor informatie over het vormen van een FSU, zie *de Gids van de Configuratie van de Dataset*.

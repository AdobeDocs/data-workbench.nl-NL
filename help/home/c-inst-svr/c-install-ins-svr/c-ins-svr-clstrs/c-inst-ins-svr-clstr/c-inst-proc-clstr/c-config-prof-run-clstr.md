---
description: Wanneer u een datasetprofiel om op een cluster van de Server van het Inzicht vormt te lopen, delen alle machines in de cluster alle dossiers van de datasetconfiguratie voor dat profiel.
solution: Insight
title: Het vormen van een Profiel om op een Cluster te lopen
uuid: e181d069-fb2f-4a71-a86f-bb9a48cfe059
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen van een Profiel om op een Cluster te lopen{#configuring-a-profile-to-run-on-a-cluster}

Wanneer u een datasetprofiel om op een cluster van de Server van het Inzicht vormt te lopen, delen alle machines in de cluster alle dossiers van de datasetconfiguratie voor dat profiel.

Daarom moeten de ingangen voor de parameters in deze dossiers op allen [!DNL Insight Servers] in de cluster van toepassing zijn. Bijvoorbeeld, de plaatsen van de te lezen logboekdossiers, de raadplegingsdossiers die door moeten worden gebruikt, [!DNL Insight Server]en de plaats van de gegevensoutput door [!DNL Insight Server] moeten het zelfde op alle machines in de cluster zijn.

U voert alle configuratietaken op de meester van de cluster uit [!DNL Insight Server], die is [!DNL Insight Server] u gebruikt om uw configuratiedossiers uit te geven. Alle opgeslagen veranderingen van het configuratiedossier die op de meester worden aangebracht [!DNL Insight Server] worden gesynchroniseerd automatisch aan de dossiers op de verwerking [!DNL Insight Servers] in de cluster.

Om een datasetprofiel op een [!DNL Insight Server] cluster in werking te stellen, moet u de volgende processen in de vermelde orde uitvoeren:

1. [Bepalend welke de gebeurtenisgegevens van het Proces van de Servers van het Inzicht](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-59b8e3f2b34f49739d544c8740a62fba)
1. [Het specificeren van de Servers van de Verwerking in Profile.cfg](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9)
1. (Indien nodig) de Dossiers van de Configuratie van de Dataset voor het Profiel [wijzigen](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99bf9248e4e5483cb518f453b0a2f278)

## Bepalend welke de gebeurtenisgegevens van het Proces van de Servers van het Inzicht {#section-59b8e3f2b34f49739d544c8740a62fba}

Het wordt niet vereist dat allen [!DNL Insight Servers] in de de gebeurtenisgegevens van het clusterproces. U kunt één [!DNL Insight Server] in de cluster als Eenheid van de Server van het Dossier aanwijzen die de brondossiers (VSL en logboekdossiers) opslaat en de dossiers aan alle Eenheden van de Gegevensverwerking (verwerkingsservers) in de cluster dient. Deze instelling biedt het voordeel van één gebeurtenisgegevensopslagplaats en maakt gebruik van de verwerkingskracht van alle verwerkingsservers in het cluster. De verwerkingsservers verdelen de gegevensdossiers onder hen en waarborgen dat het zelfde dossier niet meer dan eens wordt verwerkt.

Voor meer informatie over het aanwijzen van een als Eenheid van de Server van het Dossier te lopen, zie het hoofdstuk van het Dossier van de Configuratie van de Verwerking van het Logboek van de Gids van de Configuratie van de [!DNL Insight Server] Dataset **.

Als u besluit om brongegevensdossiers op te slaan over elk van de verwerkingsservers eerder dan op één enkele Eenheid van de Server van het Dossier, moet u de dossiers onder de verwerkingsservers gelijk verdelen. Sla niet alle van de bron dataset dossiers op elk van de verwerkingsservers op. Als meerdere kopieën van hetzelfde bestand beschikbaar zijn voor meerdere verwerkingsservers, worden de gegevens meerdere malen gelezen (één keer per machine) en worden uw gegevens scheefgetrokken.

Voor hulp die bepaalt welke logboekdossiers [!DNL Insight Servers] zouden moeten verwerken, te contacteren gelieve het Raadplegen van Adobe.

## Het specificeren van de Servers van de Verwerking in Profile.cfg {#section-99664e072c21462f91fbafb6d893fcf9}

In het [!DNL profile.cfg] dossier, specificeer de verwerkingsservers die de gegevens voor het profiel verwerken.

**Om tot het profiel.cfg- dossier toegang te hebben**

U hebt toegang tot het dossier van de profielconfiguratie gebruikend [!DNL Profile Manager] binnen [!DNL Insight].

1. Terwijl het werken in uw datasetprofiel, open [!DNL Profile Manager] door binnen een werkruimte met de rechtermuisknop aan te klikken en **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Profile Manager]**, of door de werkruimte van het Beheer van het Profiel op de [!DNL Admin] tabel te openen.

1. Klik in het [!DNL Profile Manager]venster met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. Een vinkje voor dit dossier verschijnt in de [!DNL User] kolom.

1. Klik het pas gecreëerde vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het venster voor profielconfiguratie wordt weergegeven.

**Om de servers van de Verwerking toe te voegen**

1. In het [!DNL profile.cfg] dossier, klik **[!UICONTROL Profile]**, dan klik **[!UICONTROL Processing Servers]** om zijn inhoud te tonen.

1. Klik met de rechtermuisknop **[!UICONTROL Processing Servers]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Processing Server]**.

1. In de Gemeenschappelijke parameter van de Naam, typ de gemeenschappelijke naam voor de eerste verwerkingsserver in de cluster. Bijvoorbeeld: [!DNL server1.mycompany.com]
1. Herhaal Stappen 2 en 3 tot u de gemeenschappelijke namen van alle verwerkingsservers in de cluster hebt toegevoegd.

   >[!NOTE]
   >
   >Als de meester gegevens [!DNL Insight Server] verwerkt, moet u het eveneens toevoegen.

1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

1. Klik het vinkje in de [!DNL User] kolom naast met de rechtermuisknop aan [!DNL profile.cfg]. Klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]**>*.

## Het wijzigen van de Dossiers van de Configuratie van de Dataset voor het Profiel {#section-99bf9248e4e5483cb518f453b0a2f278}

**Om de dossiers van de datasetconfiguratie te wijzigen**

Als u veranderingen in de dossiers van de datasetconfiguratie moet aanbrengen ( [!DNL Log Processing.cfg], [!DNL Transformation.cfg], omvat de dataset dossiers, [!DNL Log Processing Mode.cfg], enzovoort), doe dit slechts op de meester [!DNL Insight Server].

1. Heb toegang tot de dossiers u wilt wijzigen:

   Voor instructies om tot de dossiers toegang te hebben, zie de Gids *van de Configuratie van de* Dataset.
1. Breng uw wijzigingen aan. Raadpleeg de *Dataset Configuration Guide* voor meer informatie over de parameters in de configuratiebestanden.
1. Sla het bestand op.

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik het vinkje in de [!DNL User] kolom naast het dossier met de rechtermuisknop aan - noem.
   1. Klik **[!UICONTROL Save to]** en selecteer het gewenste profiel.

>[!NOTE]
>
>[!DNL Insight] de gebruikers die tot een datasetprofiel toegang hebben dat op een cluster loopt identificeren slechts de meester [!DNL Insight Server] in het [!DNL Insight] configuratiedossier ( [!DNL insight.cfg]). Vanuit het perspectief van de [!DNL Insight] gebruiker, is het profiel toegankelijk op slechts één [!DNL Insight Server] (de meester [!DNL Insight Server]); nochtans, kunnen de vraagverzoeken van analisten aan om het even welke [!DNL Insight Servers] in de cluster worden geleid.

Een [!DNL Insight Server] cluster laat de gecentraliseerde opslag van [!DNL .vsl] logboekdossiers (van [!DNL Sensor]) op één enkele [!DNL Insight Server] machine toe genoemd een Eenheid van de Server van het Dossier (FSU). Voor informatie over het installeren van een FSU, zie de Procedures van de [Installatie voor een Server FSU](../../../../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016)van het Inzicht. Voor informatie over het vormen van een FSU, zie de Gids *van de Configuratie van de* Dataset.

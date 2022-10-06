---
description: Wanneer u een datasetprofiel om op een cluster van de Server van het Inzicht vormt te lopen, delen alle machines in de cluster alle dossiers van de datasetconfiguratie voor dat profiel.
title: Een profiel configureren om op een cluster uit te voeren
uuid: e181d069-fb2f-4a71-a86f-bb9a48cfe059
exl-id: be8090fc-b3da-41c4-a5d4-c6eb85b8a84d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---

# Een profiel configureren om op een cluster uit te voeren{#configuring-a-profile-to-run-on-a-cluster}

{{eol}}

Wanneer u een datasetprofiel om op een cluster van de Server van het Inzicht vormt te lopen, delen alle machines in de cluster alle dossiers van de datasetconfiguratie voor dat profiel.

Daarom moeten de vermeldingen voor de parameters in deze bestanden op alle [!DNL Insight Servers] in de cluster. Bijvoorbeeld de locaties van de te lezen logbestanden, de opzoekbestanden die moeten worden gebruikt door [!DNL Insight Server]en de locatie van de gegevensuitvoer door [!DNL Insight Server] moet op alle computers in de cluster gelijk zijn.

U voert alle configuratietaken op master cluster uit [!DNL Insight Server], die [!DNL Insight Server] u gebruikt om uw configuratiedossiers uit te geven. Alle wijzigingen in het opgeslagen configuratiebestand die zijn aangebracht op het master [!DNL Insight Server] automatisch worden gesynchroniseerd met de bestanden op de verwerking [!DNL Insight Servers] in de cluster.

Een gegevenssetprofiel uitvoeren op een [!DNL Insight Server] cluster, moet u de volgende processen in de vermelde orde uitvoeren:

1. [Bepalen welke Insight Servers gebeurtenisgegevens verwerken](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-59b8e3f2b34f49739d544c8740a62fba)
1. [De verwerkingsservers opgeven in Profile.cfg](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99664e072c21462f91fbafb6d893fcf9)
1. (Indien nodig) [Het wijzigen van de Dossiers van de Configuratie van de Dataset voor het Profiel](../../../../../../home/c-inst-svr/c-install-ins-svr/c-ins-svr-clstrs/c-inst-ins-svr-clstr/c-inst-proc-clstr/c-config-prof-run-clstr.md#section-99bf9248e4e5483cb518f453b0a2f278)

## Bepalen welke Insight Servers gebeurtenisgegevens verwerken {#section-59b8e3f2b34f49739d544c8740a62fba}

Het is niet verplicht dat alle [!DNL Insight Servers] in de clusterprocesgebeurtenisgegevens. U kunt er een aanwijzen [!DNL Insight Server] in de cluster als een eenheid van de Server van het Dossier die de brondossiers (VSL en logboekdossiers) opslaat en de dossiers aan alle Eenheden van de Gegevensverwerking (verwerkingsservers) in de cluster dient. Deze installatie biedt het voordeel van één gegevensopslagplaats voor gebeurtenissen en gebruikt de verwerkingskracht van alle verwerkingsservers in de cluster. De gegevensbestanden worden door de verwerkingsservers verdeeld en er wordt gegarandeerd dat hetzelfde bestand niet meer dan één keer wordt verwerkt.

Voor meer informatie over het toewijzen van een [!DNL Insight Server] om als Eenheid van de Server van het Dossier in werking te stellen, zie het hoofdstuk van het Dossier van de Configuratie van de Verwerking van het Logboek van *Configuratie-handleiding voor gegevensset*.

Als u besluit om brongegevensdossiers op elk van de verwerkingsservers eerder dan op één enkele Eenheid van de Server van het Dossier op te slaan, moet u de dossiers gelijkelijk onder de verwerkingsservers verdelen. Sla niet alle brondossiers van de dataset op elk van de verwerkingsservers op. Als meerdere kopieën van hetzelfde bestand beschikbaar zijn op meerdere verwerkingsservers, worden de gegevens meerdere keren gelezen (één keer per computer) en worden de gegevens scheefgetrokken.

Om te helpen bepalen welke [!DNL Insight Servers] Neem contact op met Adobe Consulting als u logbestanden wilt verwerken.

## De verwerkingsservers opgeven in Profile.cfg {#section-99664e072c21462f91fbafb6d893fcf9}

In de [!DNL profile.cfg] Geef de verwerkingsservers op die de gegevens voor het profiel verwerken.

**Toegang tot het bestand profile.cfg**

U opent het profielconfiguratiebestand met het [!DNL Profile Manager] in [!DNL Insight].

1. Tijdens het werken in uw datasetprofiel, open [!DNL Profile Manager] door met de rechtermuisknop in een werkruimte te klikken en te klikken **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Profile Manager]** of door de werkruimte Profielbeheer te openen in het dialoogvenster [!DNL Admin] tab.

1. In de [!DNL Profile Manager], klikt u met de rechtermuisknop op het vinkje naast [!DNL profile.cfg] en klik op **[!UICONTROL Make Local]**. Er wordt een vinkje voor dit bestand weergegeven in het dialoogvenster [!DNL User] kolom.

1. Klik met de rechtermuisknop op het nieuwe vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**. Het venster voor profielconfiguratie wordt weergegeven.

**Verwerkingsservers toevoegen**

1. In de [!DNL profile.cfg] bestand, klikt u op **[!UICONTROL Profile]** en klik vervolgens op **[!UICONTROL Processing Servers]** om de inhoud weer te geven.

1. Klikken met rechtermuisknop **[!UICONTROL Processing Servers]** en klik op **[!UICONTROL Add new]** > **[!UICONTROL Processing Server]**.

1. Typ in de parameter Common Name de algemene naam voor de eerste verwerkingsserver in de cluster. Bijvoorbeeld: [!DNL server1.mycompany.com]
1. Herhaal stap 2 en 3 totdat u de algemene namen van alle verwerkingsservers in de cluster hebt toegevoegd.

   >[!NOTE]
   >
   >Als de master [!DNL Insight Server] verwerkt gegevens, moet u het ook toevoegen.

1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster [!DNL User] kolom naast [!DNL profile.cfg]. Klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL dataset profile name]**>*.

## Het wijzigen van de Dossiers van de Configuratie van de Dataset voor het Profiel {#section-99bf9248e4e5483cb518f453b0a2f278}

**Om de dossiers van de datasetconfiguratie te wijzigen**

Als u veranderingen in de dossiers van de datasetconfiguratie moet aanbrengen ( [!DNL Log Processing.cfg], [!DNL Transformation.cfg], gegevensset met bestanden, [!DNL Log Processing Mode.cfg], enzovoort) alleen op master [!DNL Insight Server].

1. Open de bestanden die u wilt wijzigen:

   Zie voor instructies voor toegang tot de bestanden de *Configuratie-handleiding voor gegevensset*.
1. Breng de gewenste wijzigingen aan. Zie de *Configuratie-handleiding voor gegevensset* voor meer informatie over de parameters in het configuratiebestand of de configuratiebestanden.
1. Sla het bestand op.

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster [!DNL User] naast de bestandsnaam.
   1. Klikken **[!UICONTROL Save to]** en selecteert u het gewenste profiel.

>[!NOTE]
>
>[!DNL Insight] gebruikers die toegang hebben tot een gegevenssetprofiel dat op een cluster wordt uitgevoerd, identificeren alleen de master [!DNL Insight Server] in de [!DNL Insight] configuratiebestand ( [!DNL insight.cfg]). Vanuit het perspectief van de [!DNL Insight] gebruiker, is het profiel slechts op één [!DNL Insight Server] (de master [!DNL Insight Server]); echter, de vraagverzoeken van analisten kunnen aan om het even welk van [!DNL Insight Servers] in de cluster.

An [!DNL Insight Server] cluster maakt gecentraliseerde opslag van [!DNL .vsl] logbestanden (van [!DNL Sensor]) op één enkele [!DNL Insight Server] computer genoemd een Eenheid van de Server van het Dossier (FSU). Voor informatie over het installeren van een FSU raadpleegt u [Installatieprocedures voor een Insight Server FSU](../../../../../../home/c-inst-svr/c-install-ins-svr/t-inst-proc-fsu.md#task-e4a4a791b6694119ba45b36f3e573016). Voor informatie over het vormen van FSU, zie *Configuratie-handleiding voor gegevensset*.

---
description: Informatie over het vormen van de cluster op de HoofdServer van het Inzicht, bijwerkend het toegangsbeheerdossier voor een cluster, en meer.
solution: Insight
title: Het vormen van de HoofdServer van het Inzicht voor het Groeperen
uuid: c3ac38e3-79c5-4863-9156-194589a6bcbd
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het vormen van de HoofdServer van het Inzicht voor het Groeperen{#configuring-the-master-insight-server-for-clustering}

Informatie over het vormen van de cluster op de HoofdServer van het Inzicht, bijwerkend het toegangsbeheerdossier voor een cluster, en meer.

Om de cluster te vormen, voer de volgende stappen op de meester uit [!DNL Insight Server]:

* Voeg de verwerking [!DNL Insight Servers’] gemeenschappelijke namen en adressen aan het adresdossier toe.
* Voeg elk van [!DNL Insight Servers] aan de groep van de Servers van de Cluster in het [!DNL Access Control.cfg] dossier toe.

* Werk het [!DNL Synchronize.cfg] dossier in de Componenten voor de folder van de Servers van de Verwerking bij om aan de meester te richten [!DNL Insight Server].

* Indien nodig, wijzig het [!DNL Disk Files.cfg] dossier in de Componenten voor de folder van de Servers van de Verwerking om de plaats van het [!DNL temp.db] dossier op de verwerking te specificeren [!DNL Insight Servers].

Om deze stappen te voltooien, moet u de gemeenschappelijke namen (zoals die op de digitale certificaten voor het individu wordt gespecificeerd) en de IP adressen van elk [!DNL Insight Server][!DNL Insight Server] in de cluster kennen. Als u nog niet over deze gegevens beschikt, moet u deze eerst opvragen voordat u verdergaat.

>[!NOTE]
>
>De in dit punt beschreven procedures vereisen [!DNL Insight]. Als u niet hebt geïnstalleerd [!DNL Insight], volg de instructies in de **[!DNL Insight]Gids **van de Gebruiker alvorens te werk te gaan.

## Het toevoegen van de Servers van het Inzicht van de Verwerking aan het Dossier van het Adres {#section-2fe5298180164e8dbaa59ea6b6ff682d}

Gebruik de volgende procedure om de verwerking [!DNL Insight Servers’] gemeenschappelijke namen en IP adressen aan het adresdossier op de meester toe te voegen [!DNL Insight Server]. (Hoewel het adresdossier op de meester wordt gehandhaafd en wordt beheerd, wordt het gebruikt door allen [!DNL Insight Server][!DNL Insight Servers] in de cluster.)

>[!NOTE]
>
>Het volgende veronderstelt dat het adresdossier reeds voor de meester is gevormd [!DNL Insight Server]. Als u nog niet het hoofd- [!DNL Insight Server’s] IP-adres(sen) aan het adresbestand hebt toegevoegd, voltooit u de procedure die wordt beschreven in de [definitie van de netwerklocatie](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649) van de server voordat u begint.

**Om de verwerking[!DNL Insight Servers]aan het adresdossier toe te voegen**

1. Begin [!DNL Insight] en laad het profiel van de Configuratie (als het niet reeds open is) door de titelbar met de rechtermuisknop aan te klikken en te klikken **[!UICONTROL Switch Profile]** > **[!UICONTROL Configuration]**.

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.

1. Klik het pictogram van de meester met de rechtermuisknop aan **[!UICONTROL Insight Server]** en klik **[!UICONTROL Server Files]**.

1. In [!DNL Server Files Manager], open de folder van Adressen en doe het volgende om het [!DNL Insight Server’s] adresdossier te openen:

   1. Klik het vinkje in de kolom van de *servernaam* met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.

   1. Klik het vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de inhoud van de [!DNL Locations] structuur uit, dan breid NetworkLocation 0, Adressen, en AddressDefinition uit.
1. Doe het volgende een AddressDefinition aan NetworkLocation 0 voor elke verwerking [!DNL Insight Server] in de cluster toevoegen:

   1. Klik met de rechtermuisknop **[!UICONTROL AddressDefinition]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL Address Definition]**.

   1. In de parameter van de Naam, specificeer de verwerking [!DNL Insight Server’s] gemeenschappelijke naam.
   1. In de parameter van het Adres, specificeer het verwerkingsIP [!DNL Insight Server’s] adres.

      U kunt een asterisk als vervanging op het gebied van het Adres, zoals 10.10.116 gebruiken.*, om clustering te vereenvoudigen. Zie Toegangsniveaus [begrijpen](../../../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-undst-acc-lvls.md#concept-6b292edf79214750a8d0525097b8795a).

      Het volgende voorbeeld bepaalt een cluster die twee bevat [!DNL Insight Servers]:

      ![](assets/cfg_cluster_AddressDefinition1IP.png)

1. Als de servers met veelvoudige netwerken worden verbonden, herhaal Stap 6 om de verwerking [!DNL Insight Servers] aan NetworkLocations voor die netwerken toe te voegen.

   Het volgende voorbeeld toont een cluster van vier [!DNL Insight Servers] in bijlage aan twee netwerken (&quot;Collectief Intranet&quot;en &quot;Internet&quot;).

   ![](assets/cfg_cluster_AddressDefinition2IP.png)

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het bijwerken van het Dossier van het Toegangsbeheer voor een Cluster {#section-fce1367d92a445168c35e9ca506e7d6b}

Om [!DNL Insight Servers] in een cluster te gebruiken, moet elk [!DNL Insight Server] in de cluster (met inbegrip van de meester [!DNL Insight Server]) tot de de toegangsbeheergroep van de Servers van de Cluster behoren. De groep van de Servers van de Cluster identificeert de servers (door IP adres) die om aan de cluster worden toegestaan deel te nemen. Hoewel dit dossier op de meester wordt gehandhaafd en wordt beheerd, wordt het gebruikt door elk van [!DNL Insight Server][!DNL Insight Servers] in de cluster.

**Om het toegangsbeheerdossier uit te geven**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.

1. Klik het pictogram van de meester met de rechtermuisknop aan [!DNL Insight Server] en klik **[!UICONTROL Server Files]**.

1. In [!DNL Server Files Manager], open de folder van het Toegangsbeheer.
1. Doe het volgende het [!DNL Access Control.cfg] dossier openen:

   1. Klik het vinkje in de kolom van de *servernaam* met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.

   1. Klik het vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de structuur van de Groepen van het Toegangsbeheer uit, dan breid AccessGroup (de Servers van de Cluster) uit.
1. Voor elk [!DNL Insight Server] in de cluster (met inbegrip van de meester [!DNL Insight Server]), doe het volgende:

   1. Klik met de rechtermuisknop **[!UICONTROL Members]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL New Member]**.

   1. Specificeer het [!DNL Insight Server’s] IP adres (zijn numeriek IP adres, niet zijn naam). Als [!DNL Insight Servers] met veelvoudige netwerken wordt verbonden, zou dit AccessGroup slechts de interne adressen moeten bevatten die het [!DNL Insight Servers] gebruik voor inter-servermededeling binnen de cluster.

      Het volgende toont AccessGroup (de Servers van de Cluster) voor een cluster van vier [!DNL Insight Servers].

      ![](assets/cfg_cluster_AccessControlMembers.png)

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het vormen van het Dossier van de Synchronisatie {#section-d23e751771c84da6bab6a34a8db867bc}

U kunt de volgende procedure gebruiken om het centrale exemplaar van het [!DNL Synchronize.cfg] dossier te vormen. Het centrale exemplaar van dit dossier wordt gehandhaafd op de meester [!DNL Insight Server]. De verwerking [!DNL Insight Servers] in de cluster stelt mededeling met de meester in werking [!DNL Insight Server] om een bijgewerkt exemplaar van dit dossier terug te winnen.

Het [!DNL Synchronize.cfg] dossier specificeert de plaats van de meester [!DNL Insight Server]. Het identificeert ook de reeks administratieve dossiers die elk van de verwerking [!DNL Insight Servers] in de cluster van de meester terugwint [!DNL Insight Server]. De verwerking downloadt [!DNL Insight Servers] automatisch deze dossiers van de meester [!DNL Insight Server] wanneer zij beginnen. Zij winnen ook dynamisch bijgewerkte exemplaren van deze dossiers van de meester terug [!DNL Insight Server] wanneer de dossiers veranderen.

>[!NOTE]
>
>Hoewel u het [!DNL Synchronize.cfg] dossier op de meester vormt [!DNL Insight Server], gebruikt de meester [!DNL Insight Server] zelf niet dit dossier. U werkt dit dossier op de meester bij [!DNL Insight Server] zodat het behoorlijk wordt gevormd wanneer de verwerking het dossier [!DNL Insight Servers] terugwint.

**Om het Synchronize.cfg- dossier op de meester bij te werken[!DNL Insight Server]**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.

1. Klik het pictogram van de meester met de rechtermuisknop aan [!DNL Insight Server] en klik **[!UICONTROL Server Files]**.

1. In, open [!DNL Server Files Manager]de **[!UICONTROL Components]** voor de folder van de Servers van de Verwerking.

1. Doe het volgende openen [!DNL Synchronize.cfg]:

   1. Klik het vinkje in de kolom van de *servernaam* met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.

   1. Klik het [!DNL Temp] vinkje met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de componentenstructuur uit.
1. In de parameter van het Adres van de Server van de Cluster Primaire, specificeer het IP adres van de (primaire) meester **[!UICONTROL Insight Server]**.

   ![](assets/cfg_cluster_SyncFile_(CentralCopy).png)

   Om een logboek tot stand te brengen dat registreert telkens als de synchronisatie tussen de meester [!DNL Insight Server] [!DNL Insight Servers]en de verwerking voorkomt, zorg ervoor dat de Enable parameter van het Logboek van de Synchronisatie aan &quot;waar wordt geplaatst.&quot;

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. In [!DNL Server Files Manager], klik het vinkje voor het dossier in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het vormen van de Plaats van de Dataset (temp.db) {#section-5ec257a4b4c64fb58baec1f12119a822}

Voer de volgende procedure uit als u de verwerking [!DNL Insight Servers] (de dataset) in een folder of een aandrijving verschillend wilt handhaven dan de standaardplaats of als u [!DNL temp.db] [!DNL temp.db] over veelvoudige aandrijving wilt verdelen.

>[!NOTE]
>
>Omdat de verwerking [!DNL Insight Servers] allen het zelfde deelt [!DNL Disk Files.cfg], moeten zij allen de dossierplaats(en) steunen u in dit dossier specificeert. Bijvoorbeeld, als u [!DNL temp.db] aan E toewijst: aandrijving, moet elke verwerking [!DNL Insight Server] in het cluster E hebben: rijden.

**Om de plaats van temp.db te vormen**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.

1. Klik het pictogram van de meester met de rechtermuisknop aan [!DNL Insight Server] en klik **[!UICONTROL Server Files]**.

1. In [!DNL Server Files Manager], open de **[!UICONTROL Components for Processing Servers]** folder.

1. Doe het volgende openen [!DNL Disk Files.cfg]:

   1. Klik het vinkje in de kolom van de *servernaam* met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.

   1. Klik het vinkje in de [!DNL Temp]kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de structuur DiskSpaceManagerComponent uit, dan breid de lijst van de Dossiers van de Schijf uit.
1. Geef ingang 0 uit om de plaats van het [!DNL temp.db] dossier te veranderen.
1. Als u [!DNL temp.db] over veelvoudige aandrijving wilt verdelen, gebruik de hieronder stappen om een extra ingang voor elke extra aandrijving tot stand te brengen.

   1. Klik met de rechtermuisknop **[!UICONTROL Disk Files]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL Disk File]**.

   1. In de nieuwe ingang, specificeer de plaats waar u wilt [!DNL temp.db] geschreven.
   De volgende shows [!DNL temp.db] die over vier aandrijving worden geschreven.

   ![](assets/cfg_diskfiles_exampleNewValues.png)

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. In [!DNL Server Files Manager], klik het vinkje voor het dossier in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.


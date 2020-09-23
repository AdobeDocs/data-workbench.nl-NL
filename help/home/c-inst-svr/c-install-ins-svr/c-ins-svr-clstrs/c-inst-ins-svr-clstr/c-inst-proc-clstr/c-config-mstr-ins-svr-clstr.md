---
description: Informatie over het vormen van de cluster op de Master Server van het Inzicht, het bijwerken van het dossier van de toegangscontrole voor een cluster, en meer.
solution: Analytics
title: Het vormen van de Master Server van het Inzicht voor het Groeperen
uuid: c3ac38e3-79c5-4863-9156-194589a6bcbd
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%

---


# Het vormen van de Master Server van het Inzicht voor het Groeperen{#configuring-the-master-insight-server-for-clustering}

Informatie over het vormen van de cluster op de Master Server van het Inzicht, het bijwerken van het dossier van de toegangscontrole voor een cluster, en meer.

Voer de volgende stappen uit op het master [!DNL Insight Server]:

* Voeg de [!DNL Insight Servers’] gebruikelijke namen en adressen voor de verwerking toe aan het adresbestand.
* Voeg alle bestanden toe [!DNL Insight Servers] aan de groep Clusterservers in het [!DNL Access Control.cfg] bestand.

* Werk het [!DNL Synchronize.cfg] bestand in de map Components for Processing Servers bij om naar het master bestand te verwijzen [!DNL Insight Server].

* Wijzig zo nodig het [!DNL Disk Files.cfg] bestand in de map Components for Processing Servers om de locatie van het [!DNL temp.db] bestand op de verwerking op te geven [!DNL Insight Servers].

Om deze stappen te voltooien, moet u de gemeenschappelijke namen (zoals gespecificeerd op de digitale certificaten voor het individu [!DNL Insight Server]) en de IP adressen van elk [!DNL Insight Server] in de cluster kennen. Als u deze gegevens nog niet hebt, vraagt u deze op voordat u verdergaat.

>[!NOTE]
>
>De in dit punt beschreven procedures vereisen [!DNL Insight]. Als u niet hebt geïnstalleerd [!DNL Insight], volgt u de instructies in de **[!DNL Insight]gebruikershandleiding** voordat u verdergaat.

## De servers van het Inzicht van de Verwerking aan het Dossier van het Adres toevoegen {#section-2fe5298180164e8dbaa59ea6b6ff682d}

Gebruik de volgende procedure om de verwerking [!DNL Insight Servers’] gemeenschappelijke namen en IP adressen aan het adresdossier op master toe te voegen [!DNL Insight Server]. (Hoewel het adresdossier op master wordt gehandhaafd en wordt beheerd, wordt het gebruikt door al [!DNL Insight Server][!DNL Insight Servers] in de cluster.)

>[!NOTE]
>
>Het volgende veronderstelt dat het adresdossier reeds voor master is gevormd [!DNL Insight Server]. Als u nog niet het master [!DNL Insight Server’s] IP adres(sen) aan het adresdossier hebt toegevoegd, voltooi de procedure die in het [Bepalen van de Plaats](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649) van het Netwerk van de Server wordt beschreven alvorens u begint.

**De verwerking toevoegen[!DNL Insight Servers]aan het adresbestand**

1. Start [!DNL Insight] en laad het configuratieprofiel (als dit nog niet geopend is) door met de rechtermuisknop op de titelbalk te klikken en op **[!UICONTROL Switch Profile]** > **[!UICONTROL Configuration]** te klikken.

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het master pictogram **[!UICONTROL Insight Server]** en klik op **[!UICONTROL Server Files]**.

1. Open in de [!DNL Server Files Manager]map Adressen de map en voer de volgende handelingen uit om het [!DNL Insight Server’s] adresbestand te openen:

   1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* en klik op **[!UICONTROL Make Local]**.

   1. Klik met de rechtermuisknop op het vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de inhoud van de [!DNL Locations] structuur uit, dan breid NetworkLocation 0, Adressen, en AddressDefinition uit.
1. Doe het volgende een AddressDefinition aan NetworkLocation 0 voor elke verwerking [!DNL Insight Server] in de cluster toevoegen:

   1. Klik met de rechtermuisknop **[!UICONTROL AddressDefinition]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL Address Definition]**.

   1. Geef in de parameter Name de [!DNL Insight Server’s] algemene naam voor de verwerking op.
   1. In de parameter van het Adres, specificeer het verwerkingsIP [!DNL Insight Server’s] adres.

      U kunt een asterisk als vervanging op het gebied van het Adres, zoals 10.10.116 gebruiken.*, om clustering te vereenvoudigen. Zie Toegangsniveaus [begrijpen](../../../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-undst-acc-lvls.md#concept-6b292edf79214750a8d0525097b8795a).

      In het volgende voorbeeld wordt een cluster gedefinieerd die twee componenten bevat [!DNL Insight Servers]:

      ![](assets/cfg_cluster_AddressDefinition1IP.png)

1. Als de servers met veelvoudige netwerken worden verbonden, herhaal Stap 6 om de verwerking [!DNL Insight Servers] aan NetworkLocations voor die netwerken toe te voegen.

   Het volgende voorbeeld toont een cluster van vier in bijlage aan twee netwerken (&quot;Collectief Intranet&quot;en &quot;Internet&quot;). [!DNL Insight Servers]

   ![](assets/cfg_cluster_AddressDefinition2IP.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het toegangscontrolebestand voor een cluster bijwerken {#section-fce1367d92a445168c35e9ca506e7d6b}

Om [!DNL Insight Servers] in een cluster te gebruiken, moet elk [!DNL Insight Server] in de cluster (met inbegrip van master [!DNL Insight Server]) tot de de toegangsbeheergroep van de Servers van de Cluster behoren. De groep van de Servers van de Cluster identificeert de servers (door IP adres) die aan de cluster mogen deelnemen. Hoewel dit bestand op het master systeem wordt onderhouden en beheerd, wordt het door alle [!DNL Insight Server][!DNL Insight Servers] componenten in het cluster gebruikt.

**Het toegangsbeheerbestand bewerken**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het master pictogram [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.

1. Open in de [!DNL Server Files Manager]map Access Control (Toegangsbeheer).
1. Ga als volgt te werk om het [!DNL Access Control.cfg] bestand te openen:

   1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* en klik op **[!UICONTROL Make Local]**.

   1. Klik met de rechtermuisknop op het vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de structuur van de Groepen van het Toegangsbeheer uit, dan breid AccessGroup (de Servers van de Cluster) uit.
1. Ga als volgt te werk voor elke [!DNL Insight Server] cluster (inclusief de master [!DNL Insight Server]):

   1. Klik met de rechtermuisknop **[!UICONTROL Members]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL New Member]**.

   1. Geef het [!DNL Insight Server’s] IP-adres op (het numerieke IP-adres, niet de naam). Als het [!DNL Insight Servers] met veelvoudige netwerken wordt verbonden, zou dit AccessGroup slechts de interne adressen moeten bevatten die het [!DNL Insight Servers] gebruik voor inter-servermededeling binnen de cluster.

      Het volgende toont AccessGroup (de Servers van de Cluster) voor een cluster van vier [!DNL Insight Servers].

      ![](assets/cfg_cluster_AccessControlMembers.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het synchronisatiebestand configureren {#section-d23e751771c84da6bab6a34a8db867bc}

U kunt de volgende procedure gebruiken om het centrale exemplaar van het [!DNL Synchronize.cfg] dossier te vormen. Het centrale exemplaar van dit dossier wordt gehandhaafd op het master [!DNL Insight Server]. De verwerking [!DNL Insight Servers] in de cluster initieert communicatie met de master [!DNL Insight Server] om een bijgewerkte kopie van dit bestand op te halen.

In het [!DNL Synchronize.cfg] bestand wordt de locatie van het master bestand opgegeven [!DNL Insight Server]. Het identificeert ook de reeks administratieve dossiers die elk van de verwerking [!DNL Insight Servers] in de cluster van master terugwint [!DNL Insight Server]. De verwerking downloadt deze bestanden [!DNL Insight Servers] automatisch van de master [!DNL Insight Server] server wanneer deze worden gestart. Ook worden bijgewerkte kopieën van deze bestanden dynamisch opgehaald uit het master bestand [!DNL Insight Server] wanneer de bestanden worden gewijzigd.

>[!NOTE]
>
>Hoewel u het [!DNL Synchronize.cfg] dossier op master vormt [!DNL Insight Server], gebruikt master [!DNL Insight Server] zelf niet dit dossier. U werkt dit bestand op het master systeem bij, [!DNL Insight Server] zodat het op de juiste wijze wordt geconfigureerd wanneer de verwerking het bestand [!DNL Insight Servers] ophaalt.

**Het bestand Synchronize.cfg in het master bestand bijwerken[!DNL Insight Server]**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het master pictogram [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.

1. Open in [!DNL Server Files Manager]de map **[!UICONTROL Components]** for Processing Servers.

1. Ga als volgt te werk om te openen [!DNL Synchronize.cfg]:

   1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* en klik op **[!UICONTROL Make Local]**.

   1. Klik met de rechtermuisknop op het [!DNL Temp] vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de componentenstructuur uit.
1. In de parameter van het Adres van de Server van de Cluster Primaire, specificeer het IP adres van master (primair) **[!UICONTROL Insight Server]**.

   ![](assets/cfg_cluster_SyncFile_CentralCopy.png)

   Om een logboek tot stand te brengen dat registreert telkens als de synchronisatie tussen master [!DNL Insight Server] en de verwerking voorkomt [!DNL Insight Servers], zorg ervoor dat de Enable parameter van het Logboek van de Synchronisatie aan &quot;waar&quot; wordt geplaatst.

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik [!DNL Server Files Manager]in met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het vormen van de Plaats van de Dataset (temp.db) {#section-5ec257a4b4c64fb58baec1f12119a822}

Voer de volgende procedure uit als u de verwerking [!DNL Insight Servers] (de dataset) in een folder of aandrijving verschillend wilt handhaven dan de standaardplaats of als u [!DNL temp.db] [!DNL temp.db] over veelvoudige aandrijving wilt verdelen.

>[!NOTE]
>
>Omdat de verwerking [!DNL Insight Servers] allemaal hetzelfde is [!DNL Disk Files.cfg], moeten ze allemaal de bestandslocatie(s) ondersteunen die u in dit bestand opgeeft. Als u bijvoorbeeld toewijst [!DNL temp.db] aan de E: -station, moet elke verwerking [!DNL Insight Server] in de cluster een E hebben: rijden.

**De locatie van temp.db configureren**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het master pictogram [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.

1. Open de [!DNL Server Files Manager]map in de **[!UICONTROL Components for Processing Servers]** map.

1. Ga als volgt te werk om te openen [!DNL Disk Files.cfg]:

   1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* en klik op **[!UICONTROL Make Local]**.

   1. Klik met de rechtermuisknop op het vinkje in de [!DNL Temp]kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Vouw de structuur DiskSpaceManagerComponent uit en vouw vervolgens de lijst Schijfbestanden uit.
1. Bewerk item 0 om de locatie van het [!DNL temp.db] bestand te wijzigen.
1. Als u wilt distribueren [!DNL temp.db] over meerdere stations, gebruikt u de onderstaande stappen om een extra ingang te maken voor elk extra station.

   1. Klik met de rechtermuisknop **[!UICONTROL Disk Files]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL Disk File]**.

   1. Geef in het nieuwe item de locatie op waar u wilt [!DNL temp.db] schrijven.
   In het volgende voorbeeld ziet u hoe u over vier stations [!DNL temp.db] schrijft.

   ![](assets/cfg_diskfiles_exampleNewValues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik [!DNL Server Files Manager]in met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.


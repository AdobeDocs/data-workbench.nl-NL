---
description: Informatie over het vormen van de cluster op de Master Server van het Inzicht, het bijwerken van het dossier van de toegangscontrole voor een cluster, en meer.
title: Het vormen van de Master Server van het Inzicht voor het Groeperen
uuid: c3ac38e3-79c5-4863-9156-194589a6bcbd
exl-id: 28126ba4-6d81-4ca4-895c-4e8b1a54a693
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 0%

---

# Het vormen van de Master Server van het Inzicht voor het Groeperen{#configuring-the-master-insight-server-for-clustering}

{{eol}}

Informatie over het vormen van de cluster op de Master Server van het Inzicht, het bijwerken van het dossier van de toegangscontrole voor een cluster, en meer.

Om de cluster te vormen, voer de volgende stappen op master uit [!DNL Insight Server]:

* De verwerking toevoegen [!DNL Insight Servers’] gemeenschappelijke namen en adressen aan het adresdossier.
* Alle opties toevoegen [!DNL Insight Servers] naar de groep van de Servers van de Cluster in [!DNL Access Control.cfg] bestand.

* Werk de [!DNL Synchronize.cfg] bestand in de map Components for Processing Servers om naar het master bestand te verwijzen [!DNL Insight Server].

* Indien nodig wijzigt u de [!DNL Disk Files.cfg] bestand in de directory Components for Processing Servers om de locatie van de [!DNL temp.db] bestand op de verwerking [!DNL Insight Servers].

Als u deze stappen wilt voltooien, moet u de algemene namen weten (zoals opgegeven op de digitale certificaten voor de afzonderlijke [!DNL Insight Server]) en de IP-adressen van elk [!DNL Insight Server] in de cluster. Als u deze gegevens nog niet hebt, vraagt u deze op voordat u verdergaat.

>[!NOTE]
>
>De in dit punt beschreven procedures vereisen [!DNL Insight]. Als u niet hebt geïnstalleerd [!DNL Insight]volgt u de instructies in de **[!DNL Insight]Handboek** voordat u verdergaat.

## De servers van het Inzicht van de Verwerking aan het Dossier van het Adres toevoegen {#section-2fe5298180164e8dbaa59ea6b6ff682d}

Gebruik de volgende procedure om de verwerking toe te voegen [!DNL Insight Servers’] gemeenschappelijke namen en IP adressen aan het adresdossier op master [!DNL Insight Server]. (Hoewel het adresdossier op master wordt gehandhaafd en wordt beheerd [!DNL Insight Server]wordt gebruikt door alle [!DNL Insight Servers] in de cluster.)

>[!NOTE]
>
>Het volgende veronderstelt dat het adresdossier reeds voor master is gevormd [!DNL Insight Server]. Als u nog geen master [!DNL Insight Server’s] IP adres(sen) aan het adresdossier, voltooi de in [De netwerklocatie van de server definiëren](../../../../../../home/c-inst-svr/c-install-ins-svr/t-install-proc-inst-svr-dpu/c-svrs-ntwk-loc/c-svrs-ntwk-loc.md#concept-87dd2aa3448c415ca1285bc445a8c649) voordat u begint.

**De verwerking toevoegen [!DNL Insight Servers] naar het adresbestand**

1. Start [!DNL Insight] en laad het configuratieprofiel (als dit nog niet geopend is) door met de rechtermuisknop op de titelbalk te klikken en op **[!UICONTROL Switch Profile]** > **[!UICONTROL Configuration]**.

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van het master **[!UICONTROL Insight Server]** en klik op **[!UICONTROL Server Files]**.

1. In de [!DNL Server Files Manager], opent u de directory Adressen en gaat u als volgt te werk om de [!DNL Insight Server’s] adresbestand:

   1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom en klik op **[!UICONTROL Make Local]**.

   1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. De inhoud van het dialoogvenster [!DNL Locations] structuur, dan breid NetworkLocation 0, Adressen, en AddressDefinition uit.
1. Doe het volgende een AddressDefinition aan NetworkLocation 0 voor elke verwerking toevoegen [!DNL Insight Server] in de cluster:

   1. Klikken met rechtermuisknop **[!UICONTROL AddressDefinition]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL Address Definition]**.

   1. Geef in de parameter Name de verwerking op [!DNL Insight Server’s] algemene naam.
   1. In de parameter van het Adres, specificeer de verwerking [!DNL Insight Server’s] IP-adres.

      U kunt een asterisk als vervanging op het gebied van het Adres, zoals 10.10.116 gebruiken.&#42;, om clustering te vereenvoudigen. Zie [Toegangsniveaus](../../../../../../home/c-inst-svr/c-admin-inst-svr/c-config-acs-ctrl/c-undst-acc-lvls.md#concept-6b292edf79214750a8d0525097b8795a).

      In het volgende voorbeeld wordt een cluster gedefinieerd die twee [!DNL Insight Servers]:

      ![](assets/cfg_cluster_AddressDefinition1IP.png)

1. Als de servers met veelvoudige netwerken worden verbonden, herhaal Stap 6 om de verwerking toe te voegen [!DNL Insight Servers] aan NetworkLocations voor die netwerken.

   In het volgende voorbeeld wordt een cluster van vier [!DNL Insight Servers] verbonden aan twee netwerken (&quot;Collectief Intranet&quot;en &quot;Internet&quot;).

   ![](assets/cfg_cluster_AddressDefinition2IP.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het toegangscontrolebestand voor een cluster bijwerken {#section-fce1367d92a445168c35e9ca506e7d6b}

Te gebruiken [!DNL Insight Servers] in een cluster, elk [!DNL Insight Server] in de cluster (inclusief de master [!DNL Insight Server]) moet tot de de toegangsbeheergroep van de Servers van de Cluster behoren. De groep van de Servers van de Cluster identificeert de servers (door IP adres) die aan de cluster mogen deelnemen. Hoewel dit bestand op het master [!DNL Insight Server], wordt het gebruikt door alle [!DNL Insight Servers] in de cluster.

**Het toegangsbeheerbestand bewerken**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van het master [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.

1. In de [!DNL Server Files Manager], opent u de directory Toegangsbeheer.
1. Ga als volgt te werk om de [!DNL Access Control.cfg] bestand:

   1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom en klik op **[!UICONTROL Make Local]**.

   1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de structuur van de Groepen van het Toegangsbeheer uit, dan breid AccessGroup (de Servers van de Cluster) uit.
1. Voor elke [!DNL Insight Server] in de cluster (inclusief de master [!DNL Insight Server]), doet u het volgende:

   1. Klikken met rechtermuisknop **[!UICONTROL Members]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL New Member]**.

   1. Geef de [!DNL Insight Server’s] IP adres (zijn numeriek IP adres, niet zijn naam). Als de [!DNL Insight Servers] worden verbonden met veelvoudige netwerken, zou dit AccessGroup slechts de interne adressen moeten bevatten die [!DNL Insight Servers] gebruiken voor communicatie tussen servers binnen de cluster.

      Het volgende toont AccessGroup (de Servers van de Cluster) voor een cluster van vier [!DNL Insight Servers].

      ![](assets/cfg_cluster_AccessControlMembers.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het synchronisatiebestand configureren {#section-d23e751771c84da6bab6a34a8db867bc}

U kunt de volgende procedure gebruiken om het centrale exemplaar van te vormen [!DNL Synchronize.cfg] bestand. Het centrale exemplaar van dit dossier wordt gehandhaafd op master [!DNL Insight Server]. De verwerking [!DNL Insight Servers] in de cluster communicatie met de master [!DNL Insight Server] om een bijgewerkte kopie van dit bestand op te halen.

De [!DNL Synchronize.cfg] bestand geeft de locatie van het master [!DNL Insight Server]. Het identificeert ook de reeks administratieve dossiers die elk van de verwerking [!DNL Insight Servers] in de cluster wordt opgehaald uit de master [!DNL Insight Server]. De verwerking [!DNL Insight Servers] Deze bestanden automatisch downloaden van de master [!DNL Insight Server] wanneer ze beginnen. Ook worden bijgewerkte kopieën van deze bestanden dynamisch opgehaald uit de master [!DNL Insight Server] wanneer de bestanden veranderen.

>[!NOTE]
>
>Hoewel u vormt [!DNL Synchronize.cfg] bestand op de master [!DNL Insight Server], de master [!DNL Insight Server] zelf gebruikt dit bestand niet. U werkt dit bestand bij op het master [!DNL Insight Server] zodat het behoorlijk wordt gevormd wanneer de verwerking [!DNL Insight Servers] Haal het bestand op.

**Het bestand Synchronize.cfg in het master bestand bijwerken[!DNL Insight Server]**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van het master [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.

1. In [!DNL Server Files Manager], opent u de **[!UICONTROL Components]** voor het verwerken van de map Servers.

1. Ga als volgt te werk om te openen [!DNL Synchronize.cfg]:

   1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom en klik op **[!UICONTROL Make Local]**.

   1. Klik met de rechtermuisknop op de knop [!DNL Temp] vinkje en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Breid de componentenstructuur uit.
1. In de parameter van het Adres van de Server van de Cluster Primaire, specificeer het IP adres van master (primair) **[!UICONTROL Insight Server]**.

   ![](assets/cfg_cluster_SyncFile_CentralCopy.png)

   Om een logboek te creëren dat registreert telkens als de synchronisatie tussen master voorkomt [!DNL Insight Server] en de verwerking [!DNL Insight Servers], zorg ervoor dat de Enable parameter van het Logboek van de Synchronisatie aan &quot;waar wordt geplaatst.&quot;

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

## Het vormen van de Plaats van de Dataset (temp.db) {#section-5ec257a4b4c64fb58baec1f12119a822}

Voer de volgende procedure uit als u de verwerking wilt uitvoeren [!DNL Insight Servers] handhaven [!DNL temp.db] (de dataset) in een folder of een aandrijving verschillend dan de standaardplaats of als u wilt verdelen [!DNL temp.db] op meerdere stations.

>[!NOTE]
>
>Omdat de verwerking [!DNL Insight Servers] allen delen het zelfde [!DNL Disk Files.cfg], moeten zij allen de dossierplaats(en) steunen u in dit dossier specificeert. Als u bijvoorbeeld [!DNL temp.db] aan de E: aandrijving, elke verwerking [!DNL Insight Server] in de cluster moet een E zijn: rijden.

**De locatie van temp.db configureren**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.

1. Klik met de rechtermuisknop op het pictogram van het master [!DNL Insight Server] en klik op **[!UICONTROL Server Files]**.

1. In de [!DNL Server Files Manager], opent u de **[!UICONTROL Components for Processing Servers]** directory.

1. Ga als volgt te werk om te openen [!DNL Disk Files.cfg]:

   1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom en klik op **[!UICONTROL Make Local]**.

   1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster [!DNL Temp]kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.

1. Vouw de structuur DiskSpaceManagerComponent uit en vouw vervolgens de lijst Schijfbestanden uit.
1. Item 0 bewerken om de locatie van de [!DNL temp.db] bestand.
1. Als u wilt distribueren [!DNL temp.db] voor meerdere stations gebruikt u de onderstaande stappen om een extra ingang te maken voor elk extra station.

   1. Klikken met rechtermuisknop **[!UICONTROL Disk Files]** en klik op **[!UICONTROL Add New]** > **[!UICONTROL Disk File]**.

   1. Geef in het nieuwe item de locatie op waar u wilt [!DNL temp.db] geschreven.
   De volgende shows [!DNL temp.db] geschreven over vier stations.

   ![](assets/cfg_diskfiles_exampleNewValues.png)

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

---
description: Informatie over de ruimte van de controlegebeurtenisgegevens en het veranderen van de logboekfolder voor de gegevens van de Sensor.
solution: Insight
title: Bewaking van gebeurtenisgegevensruimte
uuid: e514e8fb-e735-4003-ab21-17470c73af37
translation-type: tm+mt
source-git-commit: 25366087936dfa5e31c5921aac400535ec259f2e

---


# Bewaking van gebeurtenisgegevensruimte{#monitoring-event-data-space}

Informatie over de ruimte van de controlegebeurtenisgegevens en het veranderen van de logboekfolder voor de gegevens van de Sensor.

**Aanbevolen frequentie:** Om de 5-10 minuten

[!DNL Insight Server] slaat één logboekdossier per [!DNL Sensor] per dag op of de Eenheid van de Gegevensverwerking of van de Server van het Dossier, afhankelijk van uw configuratie op. De grootte van de logboekdossiers en de hoeveelheid ruimte van de gegevensopslag die voor hen wordt vereist hangt van vele variabelen, met inbegrip van, bijvoorbeeld, het aantal websites af die worden geregistreerd en het aantal verzoeken uw Webservers per seconde ontvangen.

Een typische installatie van [!DNL Insight Server] (of een [!DNL Insight Server] cluster) kan veelvoudige terabytes van gegevens opslaan, veronderstellend dat de implementatie de hardware gebruikt die door Adobe voor de [!DNL Insight Server] machine(s) wordt geadviseerd.

Typisch, blijven alle logboekgegevens aanwezig op de [!DNL Insight Server] machine. Als het noodzakelijk wordt om meer ruimte van de gegevensopslag beschikbaar te maken op de machine, kunt u alle - behalve de het logboekdossiers van de huidigste dag naar een andere machine of gegevensopslagmiddel (zip aandrijving, band, etc.) verplaatsen. Het bewegen van de gegevens vereist u niet om op te houden [!DNL Insight Server], en het beïnvloedt niet de functionaliteit beschikbaar in om het even welk [!DNL Insights] die met [!DNL Insight Server] en het werken met ononderbroken gegevens kan worden verbonden. Op voorwaarde dat u geen analysedataset verwerkt of opnieuw verwerkt, behoudt u toegang tot alle vorige gegevens en de nieuwe gegevens blijven beschikbaar in [!DNL Insight]. Als u verwerkt of een analysedataset opnieuw verwerkt, kunt u niet tot de gegevens toegang hebben tot de verwerking volledig is.

Door gebrek, worden de gebeurtenisgegevens die door worden geproduceerd [!DNL Sensor] en aan [!DNL Insight Server] worden overgebracht opgeslagen in de [!DNL Logs] omslag binnen de [!DNL Insight Server] installatiefolder. Het Communicatie configuratiedossier, [!DNL Communications.cfg], specificeert de plaats van de dossiers van het logboek van gebeurtenisgegevens die langs worden gelezen [!DNL Insight Server].

**Om de logboekfolder voor[!DNL Sensor]gegevens te veranderen**

1. In [!DNL Insight], op het [!DNL Admin] > [!DNL Dataset and Profile] lusje, klik de **[!UICONTROL Servers Manager]** duimnagel om de werkruimte van de Manager van Servers te openen.
1. Klik het pictogram van het pictogram met de rechtermuisknop aan [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In [!DNL Server Files Manager], klik **[!UICONTROL Components]** om zijn inhoud te bekijken. Het [!DNL Communications.cfg] dossier wordt gevestigd binnen deze folder.
1. Klik het vinkje in de kolom van de *servernaam* voor met de rechtermuisknop aan [!DNL Communications.cfg] en klik **[!UICONTROL Make Local]**. Een vinkje verschijnt in de [!DNL Temp] kolom voor [!DNL Communications.cfg].
1. Klik het pas gecreëerde vinkje in de [!DNL Temp] kolom met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In het [!DNL Communications.cfg] venster, klik **[!UICONTROL component]** om zijn inhoud te bekijken.
1. In het [!DNL Communications.cfg] venster, klik **[!UICONTROL Servers]** om zijn inhoud te bekijken. Verscheidene types van servers kunnen verschijnen: Bestandsservers, logboekservers, IP-servers, statusservers, servers verzenden of servers repliceren.
1. Vind LoggingServer, die is waar zijn logboekdossiers [!DNL Sensor] [!DNL Insight Server]schrijft die langs moeten worden verwerkt, en zijn aantal klikken om het menu te bekijken.

   ![Stapgegevens](assets/cfg_communications_examplevalues_logging.png)

   De standaardlogboekfolder is de [!DNL Logs] omslag binnen de [!DNL Insight Server] installatiefolder.

1. Geef de parameter van de Folder van het Logboek uit om op de gewenste plaats van de logboekdossiers te wijzen.

   >[!NOTE]
   >
   >Wijzig geen andere parameters voor LoggingServer.

   ![](assets/cfg_communicates_logslocalpath_egvalues.png)

   Verscheidene FileServers kunnen onder de knoop van Servers worden vermeld, zodat kunt u de inhoud van vele van hen (door hun aantallen in de [!DNL Servers] lijst te klikken) moeten bekijken om de server met een Lokale Weg van Logboeken te vinden \ om worden gewijzigd.

1. Geef de Lokale Weg uit om op de gewenste plaats van de [!DNL .vsl] dossiers te wijzen.

   >[!NOTE]
   >
   >Wijzig geen andere parameters voor FileServer.

   Hoewel de plaats van de logboekdossiers in het [!DNL Communications.cfg] dossier is veranderd, kunt u deze dossiers aan de folder van Logboeken van in kaart brengen [!DNL Server Files Manager] door /Logs/ als URI voor FileServer te specificeren.

1. Sparen uw veranderingen in de server door het volgende te doen:

   1. Klik **[!UICONTROL (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.


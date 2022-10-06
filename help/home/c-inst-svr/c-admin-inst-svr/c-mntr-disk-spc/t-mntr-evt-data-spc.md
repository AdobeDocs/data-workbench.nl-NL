---
description: Informatie over het controleren van de ruimte van gebeurtenisgegevens en het veranderen van de logboekfolder voor de gegevens van de Sensor.
title: Gegevensruimte van gebeurtenissen controleren
uuid: e514e8fb-e735-4003-ab21-17470c73af37
exl-id: 1016d00f-e0a0-47f1-a600-528c4811fcf6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# Gegevensruimte van gebeurtenissen controleren{#monitoring-event-data-space}

{{eol}}

Informatie over het controleren van de ruimte van gebeurtenisgegevens en het veranderen van de logboekfolder voor de gegevens van de Sensor.

**Aanbevolen frequentie:** Elke 5-10 minuten

[!DNL Insight Server] één logbestand opslaan per [!DNL Sensor] per dag op of de Eenheid van de Gegevensverwerking of van de Server van het Dossier, afhankelijk van uw configuratie. De grootte van de logbestanden en de hoeveelheid gegevensopslagruimte die voor deze bestanden nodig is, zijn afhankelijk van vele variabelen, zoals het aantal websites dat wordt geregistreerd en het aantal aanvragen dat uw webservers per seconde ontvangen.

Een standaardinstallatie van [!DNL Insight Server] (of [!DNL Insight Server] cluster) kan meerdere terabytes aan gegevens opslaan, ervan uitgaande dat de implementatie de hardware gebruikt die door Adobe voor de [!DNL Insight Server] machine(s).

Doorgaans blijven alle loggegevens aanwezig op het tabblad [!DNL Insight Server] machine. Als het nodig is om meer opslagruimte voor gegevens beschikbaar te maken op de computer, kunt u alle logbestanden van de meest recente dag verplaatsen naar een andere computer of een ander opslagmedium (ZIP-station, tape enzovoort). Als u de gegevens verplaatst, hoeft u niet te stoppen [!DNL Insight Server]en heeft geen invloed op de functionaliteit die in [!DNL Insights] die verbonden kunnen zijn met [!DNL Insight Server] en het werken met ononderbroken gegevens. Op voorwaarde dat u een analysetgegevensset niet verwerkt of opnieuw verwerkt, behoudt u toegang tot alle vorige gegevens en blijven de nieuwe gegevens beschikbaar in [!DNL Insight]. Als u een dataset van de analyse verwerkt of opnieuw verwerkt, kunt u tot de gegevens niet toegang hebben tot tot de verwerking volledig is.

Standaard worden gebeurtenisgegevens geproduceerd door [!DNL Sensor] en verzonden aan [!DNL Insight Server] wordt opgeslagen in het dialoogvenster [!DNL Logs] in de [!DNL Insight Server] installatiemap. Het Communicatie configuratiedossier, [!DNL Communications.cfg], geeft de locatie op van logbestanden met gebeurtenisgegevens die worden gelezen door [!DNL Insight Server].

**De logmap wijzigen voor [!DNL Sensor] data**

1. In [!DNL Insight]over de [!DNL Admin] > [!DNL Dataset and Profile] klikt u op de knop **[!UICONTROL Servers Manager]** om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het dialoogvenster [!DNL Insight Server] u wilt vormen en klikken **[!UICONTROL Server Files]**.
1. In de [!DNL Server Files Manager], klikt u op **[!UICONTROL Components]** om de inhoud te bekijken. De [!DNL Communications.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster *servernaam* kolom voor [!DNL Communications.cfg] en klik op **[!UICONTROL Make Local]**. Er verschijnt een vinkje in het dialoogvenster [!DNL Temp] kolom voor [!DNL Communications.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in het dialoogvenster [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. In de [!DNL Communications.cfg] venster, klikt u op **[!UICONTROL component]** om de inhoud te bekijken.
1. In de [!DNL Communications.cfg] venster, klikt u op **[!UICONTROL Servers]** om de inhoud te bekijken. Er kunnen verschillende typen servers worden weergegeven: Bestandsservers, Logging Servers, Init Servers, Statusservers, Send Servers of Replicate Servers.
1. Vind LoggingServer, die is waar [!DNL Sensor] schrijft zijn logboekdossiers die door moeten worden verwerkt [!DNL Insight Server]en klik op het nummer ervan om het menu weer te geven.

   ![Stapinfo](assets/cfg_communications_examplevalues_logging.png)

   De standaardlogmap is [!DNL Logs] in de [!DNL Insight Server] installatiemap.

1. Geef de parameter van de Folder van het Logboek uit om op de gewenste plaats van de logboekdossiers te wijzen.

   >[!NOTE]
   >
   >Wijzig geen andere parameters voor LoggingServer.

   ![](assets/cfg_communicates_logslocalpath_egvalues.png)

   Verschillende FileServers kunnen onder het knooppunt Servers worden vermeld, dus u moet mogelijk de inhoud van veel hiervan bekijken (door op de nummers in het knooppunt [!DNL Servers] lijst) om de server te zoeken met een lokaal te wijzigen pad naar logbestanden.

1. Het lokale pad bewerken om de gewenste locatie van het [!DNL .vsl] bestanden.

   >[!NOTE]
   >
   >Wijzig geen andere parameters voor FileServer.

   Hoewel de locatie van de logbestanden is gewijzigd in het dialoogvenster [!DNL Communications.cfg] bestand, kunt u deze bestanden toewijzen aan de map Logs van het dialoogvenster [!DNL Server Files Manager] door /Logs/ als URI voor FileServer te specificeren.

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klikken met rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

   1. In de [!DNL Server Files Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

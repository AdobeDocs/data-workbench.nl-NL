---
description: Informatie over het controleren van de ruimte van gebeurtenisgegevens en het veranderen van de logboekfolder voor de gegevens van de Sensor.
title: Gegevensruimte van gebeurtenissen controleren
uuid: e514e8fb-e735-4003-ab21-17470c73af37
exl-id: 1016d00f-e0a0-47f1-a600-528c4811fcf6
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# Bewaking van gebeurtenisgegevensruimte{#monitoring-event-data-space}

Informatie over het controleren van de ruimte van gebeurtenisgegevens en het veranderen van de logboekfolder voor de gegevens van de Sensor.

**Aanbevolen frequentie:** elke 5-10 minuten

[!DNL Insight Server] slaat één logboekdossier per  [!DNL Sensor] per dag op of de Eenheid van de Gegevensverwerking of van de Server van het Dossier, afhankelijk van uw configuratie. De grootte van de logbestanden en de hoeveelheid gegevensopslagruimte die voor deze bestanden nodig is, zijn afhankelijk van vele variabelen, zoals het aantal websites dat wordt geregistreerd en het aantal aanvragen dat uw webservers per seconde ontvangen.

Een standaardinstallatie van [!DNL Insight Server] (of een [!DNL Insight Server] cluster) kan veelvoudige terabytes van gegevens opslaan, veronderstellend dat de implementatie de hardware gebruikt die door Adobe voor [!DNL Insight Server] machine(s) wordt geadviseerd.

Doorgaans blijven alle loggegevens aanwezig op de [!DNL Insight Server]-computer. Als het nodig is om meer opslagruimte voor gegevens beschikbaar te maken op de computer, kunt u alle logbestanden van de meest recente dag verplaatsen naar een andere computer of een ander opslagmedium (ZIP-station, tape enzovoort). Als u de gegevens verplaatst, hoeft u [!DNL Insight Server] niet te stoppen en heeft dit geen invloed op de functionaliteit die beschikbaar is in [!DNL Insights] die mogelijk is verbonden met [!DNL Insight Server] en werken met doorlopende gegevens. Op voorwaarde dat u een analysetgegevensset niet verwerkt of opnieuw verwerkt, behoudt u toegang tot alle vorige gegevens en blijven nieuwe gegevens beschikbaar in [!DNL Insight]. Als u een dataset van de analyse verwerkt of opnieuw verwerkt, kunt u tot de gegevens niet toegang hebben tot tot de verwerking volledig is.

Standaard worden gebeurtenisgegevens die door [!DNL Sensor] worden geproduceerd en naar [!DNL Insight Server] worden verzonden, opgeslagen in de map [!DNL Logs] in de installatiemap [!DNL Insight Server]. Het Communicatie configuratiedossier, [!DNL Communications.cfg], specificeert de plaats van de dossiers van het logboek van gebeurtenisgegevens die door [!DNL Insight Server] worden gelezen.

**De logmap voor  [!DNL Sensor] gegevens wijzigen**

1. Klik in [!DNL Insight] op het tabblad [!DNL Admin] > [!DNL Dataset and Profile] op de miniatuur **[!UICONTROL Servers Manager]** om de werkruimte Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van de [!DNL Insight Server] die u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in [!DNL Server Files Manager] op **[!UICONTROL Components]** om de inhoud ervan weer te geven. Het [!DNL Communications.cfg]-bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *servernaam* voor [!DNL Communications.cfg] en klik op **[!UICONTROL Make Local]**. In de kolom [!DNL Temp] wordt een vinkje weergegeven voor [!DNL Communications.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de kolom [!DNL Temp] en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het venster [!DNL Communications.cfg] op **[!UICONTROL component]** om de inhoud ervan weer te geven.
1. Klik in het venster [!DNL Communications.cfg] op **[!UICONTROL Servers]** om de inhoud ervan weer te geven. Er kunnen verschillende typen servers worden weergegeven: Bestandsservers, Logging Servers, Init Servers, Statusservers, Send Servers of Replicate Servers.
1. Zoek de LoggingServer, waar [!DNL Sensor] zijn logboekdossiers schrijft die door [!DNL Insight Server] moeten worden verwerkt, en zijn aantal klikken om het menu te bekijken.

   ![Stapinfo](assets/cfg_communications_examplevalues_logging.png)

   De standaardlogmap is de map [!DNL Logs] in de installatiemap [!DNL Insight Server].

1. Geef de parameter van de Folder van het Logboek uit om op de gewenste plaats van de logboekdossiers te wijzen.

   >[!NOTE]
   >
   >Wijzig geen andere parameters voor LoggingServer.

   ![](assets/cfg_communicates_logslocalpath_egvalues.png)

   Meerdere FileServers kunnen onder de knoop van Servers worden vermeld, zodat kunt u de inhoud van vele van hen (door hun aantallen in de [!DNL Servers] lijst te klikken) moeten bekijken om de server met een Lokale Weg van Logs te vinden \ om worden gewijzigd.

1. Bewerk het lokale pad om de gewenste locatie van de [!DNL .vsl]-bestanden weer te geven.

   >[!NOTE]
   >
   >Wijzig geen andere parameters voor FileServer.

   Hoewel de locatie van de logbestanden is gewijzigd in het [!DNL Communications.cfg]-bestand, kunt u deze bestanden toewijzen aan de map Logs van de [!DNL Server Files Manager] door /Logs/ op te geven als de URI voor de FileServer.

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik **[!UICONTROL Save]**.

   1. Klik in [!DNL Server Files Manager] met de rechtermuisknop op het vinkje voor het bestand in de kolom [!DNL Temp] en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.

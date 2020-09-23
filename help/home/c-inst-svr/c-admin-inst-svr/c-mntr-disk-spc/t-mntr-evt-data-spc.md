---
description: Informatie over het controleren van de ruimte van gebeurtenisgegevens en het veranderen van de logboekfolder voor de gegevens van de Sensor.
solution: Analytics
title: Gegevensruimte van gebeurtenissen controleren
uuid: e514e8fb-e735-4003-ab21-17470c73af37
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---


# Gegevensruimte van gebeurtenissen controleren{#monitoring-event-data-space}

Informatie over het controleren van de ruimte van gebeurtenisgegevens en het veranderen van de logboekfolder voor de gegevens van de Sensor.

**Aanbevolen frequentie:** Elke 5-10 minuten

[!DNL Insight Server] slaat één logboekdossier per [!DNL Sensor] per dag op of de Eenheid van de Gegevensverwerking of van de Server van het Dossier, afhankelijk van uw configuratie. De grootte van de logbestanden en de hoeveelheid gegevensopslagruimte die voor deze bestanden nodig is, zijn afhankelijk van vele variabelen, zoals het aantal websites dat wordt geregistreerd en het aantal aanvragen dat uw webservers per seconde ontvangen.

Een standaardinstallatie van [!DNL Insight Server] (of een [!DNL Insight Server] cluster) kan meerdere terabytes aan gegevens opslaan, ervan uitgaande dat de implementatie de hardware gebruikt die door Adobe voor de [!DNL Insight Server] machine(s) wordt aanbevolen.

Doorgaans blijven alle loggegevens op de [!DNL Insight Server] computer aanwezig. Als het nodig is om meer opslagruimte voor gegevens beschikbaar te maken op de computer, kunt u alle logbestanden van de meest recente dag verplaatsen naar een andere computer of een ander opslagmedium (ZIP-station, tape enzovoort). Als u de gegevens verplaatst, hoeft u niet te stoppen [!DNL Insight Server]en heeft dit geen invloed op de functionaliteit die beschikbaar is in [!DNL Insights] bestanden die zijn verbonden met [!DNL Insight Server] en werken met ononderbroken gegevens. Op voorwaarde dat u een analysetgegevensset niet verwerkt of opnieuw verwerkt, behoudt u toegang tot alle vorige gegevens en blijven de nieuwe gegevens beschikbaar in [!DNL Insight]. Als u een dataset van de analyse verwerkt of opnieuw verwerkt, kunt u tot de gegevens niet toegang hebben tot tot de verwerking volledig is.

Standaard worden gebeurtenisgegevens die door [!DNL Sensor] en naar [!DNL Insight Server] worden verzonden, opgeslagen in de [!DNL Logs] map in de [!DNL Insight Server] installatiemap. Het Communicatie configuratiedossier, [!DNL Communications.cfg], specificeert de plaats van de dossiers van het logboek van gebeurtenisgegevens die door worden gelezen [!DNL Insight Server].

**De logmap voor[!DNL Sensor]gegevens wijzigen**

1. Klik in [!DNL Insight]het tabblad [!DNL Admin] > op de [!DNL Dataset and Profile] **[!UICONTROL Servers Manager]** miniatuur om de werkruimte van Servers Manager te openen.
1. Klik met de rechtermuisknop op het pictogram van het [!DNL Insight Server] object dat u wilt configureren en klik op **[!UICONTROL Server Files]**.
1. Klik in de [!DNL Server Files Manager]werkruimte **[!UICONTROL Components]** om de inhoud weer te geven. Het [!DNL Communications.cfg] bestand bevindt zich in deze map.
1. Klik met de rechtermuisknop op het vinkje in de kolom *Servernaam* voor [!DNL Communications.cfg] en klik op **[!UICONTROL Make Local]**. In de [!DNL Temp] kolom voor [!DNL Communications.cfg].
1. Klik met de rechtermuisknop op het nieuwe vinkje in de [!DNL Temp] kolom en klik op **[!UICONTROL Open]** > **[!UICONTROL in Insight]**.
1. Klik in het [!DNL Communications.cfg] venster **[!UICONTROL component]** om de inhoud weer te geven.
1. Klik in het [!DNL Communications.cfg] venster **[!UICONTROL Servers]** om de inhoud weer te geven. Er kunnen verschillende typen servers worden weergegeven: Bestandsservers, Logging Servers, Init Servers, Statusservers, Send Servers of Replicate Servers.
1. Vind LoggingServer, die is waar zijn logboekdossiers [!DNL Sensor] schrijft door worden verwerkt, [!DNL Insight Server]en zijn aantal klikken om het menu te bekijken.

   ![Stapinfo](assets/cfg_communications_examplevalues_logging.png)

   De standaardlogmap is de [!DNL Logs] map in de [!DNL Insight Server] installatiemap.

1. Geef de parameter van de Folder van het Logboek uit om op de gewenste plaats van de logboekdossiers te wijzen.

   >[!NOTE]
   >
   >Wijzig geen andere parameters voor LoggingServer.

   ![](assets/cfg_communicates_logslocalpath_egvalues.png)

   Meerdere FileServers kunnen onder de knoop van Servers worden vermeld, zodat kunt u de inhoud van vele van hen (door hun aantallen in de [!DNL Servers] lijst te klikken) moeten bekijken om de server met een Lokale Weg van Logs te vinden \ om worden gewijzigd.

1. Bewerk het lokale pad om de gewenste locatie van de [!DNL .vsl] bestanden weer te geven.

   >[!NOTE]
   >
   >Wijzig geen andere parameters voor FileServer.

   Hoewel de locatie van de logbestanden is gewijzigd in het [!DNL Communications.cfg] bestand, kunt u deze bestanden toewijzen aan de map Logs van het bestand [!DNL Server Files Manager] door /Logs/ op te geven als de URI voor de FileServer.

1. Sla de wijzigingen op de server op door het volgende te doen:

   1. Klik met de rechtermuisknop **[!UICONTROL (modified)]** boven in het venster en klik op **[!UICONTROL Save]**.

   1. Klik in het [!DNL Server Files Manager]dialoogvenster met de rechtermuisknop op het vinkje voor het bestand in de [!DNL Temp] kolom en selecteer **[!UICONTROL Save to]** > *&lt;**[!UICONTROL server name]**>*.


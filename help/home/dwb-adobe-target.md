---
description: Integreer Data Workbench met Adobe Target. Gegevenssegmenten exporteren en exportbestanden automatisch vullen.
title: Integratie van Data Workbench met Adobe Target
exl-id: e7c41e7a-aae6-4b5c-8b14-7ae97b62d70b
source-git-commit: 4ab43bfbad96096fb2cebd77a8be8fa6d49fa7dc
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# Integratie van Data Workbench met Adobe Target

{{eol}}

De integratie van de Data Workbench van Adobe met Adobe Target werd gemakkelijker met de eigenschappen van de Data Workbench om gegevenssegmenten uit te voeren en automatisch uitvoerdossiers te bevolken.

De Data Workbench van Adobe verstrekt gesloten-loopintegratie met Adobe Target voor het delen van gegevens en het produceren van rapporten. Binnen Data Workbench kunt u populaties voor zinvolle segmenten analyseren gebruikend alle beschikbare gegevens, met inbegrip van off-line omzettingen door kanalen zoals telefoon, een opslag, etc.

Bijvoorbeeld, zoekt een bezoeker naar schoenen op uw website maar zet niet om. In plaats daarvan downloadt de bezoeker een coupon voor 20 procent van zijn volgende aankoop en koopt hij een shirt in je winkel. Met behulp van Data Workbench kunt u die gegevens verzamelen en die profielgegevens vervolgens weer naar Target duwen om te tonen dat de bezoeker een shirt offline heeft gekocht. Vervolgens kunt u een campagne starten die een koppeling aanbiedt aan die bezoeker, terwijl Target normaal gesproken zou proberen schoenen opnieuw op de markt te brengen voor die bezoeker.

## Data Workbench instellen met Adobe Target

1. Klik met de rechtermuisknop op de koptekst in het dialoogvenster [!UICONTROL Detail Table] venster.

   ![](assets/insight-to-tnt.png)

1. Selecteren **[!UICONTROL New Target Export]** en voert u de naam in van een nieuw exportbestand onder de **[!UICONTROL Save As]** in het menu.

1. Klik op **[!UICONTROL Save Export File]**.

   Er wordt een venster met een exportsjabloon geopend.

   Alle Adobe Target-gegevens worden automatisch ingevuld. Het bouwt omhoog de parameterlijst op wat u in de segmentuitvoer zet. Als de bewerking is voltooid, stuurt Data Workbench de gegevens naar de Adobe Target-server.

   **Opmerking:** Het sjabloonbestand moet door de [!UICONTROL Profile Architect]. De [!UICONTROL Client Name], [!UICONTROL Domain Postfix], [!UICONTROL Mbox Host], en [!UICONTROL Mbox Name] moet worden ingevoerd. Als u meerdere sites hebt, vult u meerdere sjablonen in en slaat u deze op de server op. De sjablonen in Profielbeheer bevinden zich in `Context\FileNew\Detail Table\Export\Copy`.

   ![](assets/insight-to-tnt1.png)

1. Geef de [!UICONTROL mboxPC] queryparameter.

   Als de naam van het kenmerk Data Workbench iets anders is dan [!UICONTROL mboxPC], moet u de aangewezen Parameter van de Vraag uitgeven en het anders noemen aan _mboxPC_.

   ![](assets/insight-to-tnt2.png)

   Wanneer u het exportbestand opslaat op de server, wordt het exporteren gestart. Wanneer de [!UICONTROL TnTSend.exe] de toepassing start en begint met het verzenden van gegevens naar de Target-account.

## Data Workbench voor doel configureren

Voer de volgende taken uit in Adobe Target:

Data Workbench geeft gebruikersprofielen door aan Adobe Target. Om voor de uitvoer naar Doel te vormen, moet u opstelling en zijn API toelaten en verstrekken **[!UICONTROL clientname]** en **[!UICONTROL domain postfix]** parameters voor het exportconfiguratiebestand (`export.cfg`).

Een nieuwe Booleaanse optie die **[!UICONTROL Oneshot]** is toegevoegd aan segmentexportbestanden. Deze optie is opgenomen in het sjabloonbestand dat met het nieuwe profiel wordt gedistribueerd. Indien [!UICONTROL Oneshot] is ingesteld op _true_ en de `.export` bestand wordt hernoemd naar `.export.done-TIMESTAMP` nadat de uitvoer is voltooid, ervoor zorgen dat het segment nooit meer dan één keer wordt uitgevoerd. Dit is belangrijk bij het exporteren naar Adobe Target.

**Opmerking:** Een vraag van Data Workbench aan Adobe Target telt als [!UICONTROL mbox] vraag, die één vraag voor elk verzonden profiel vereist. Dientengevolge, stijgen de kosten als de veelvoudige vraag tussen de twee oplossingen wordt vereist.

Een onvolledige configuratie veroorzaakt het volgende foutenbericht in het logboek:

```
TNT-040615-133212-Adobe-Target-Product-Test.log:
TnT Configuration left out these empty fields:
ClientName,MboxHost,MboxName
```

## Adobe Target for Data Workbench configureren

In Adobe Target is geen speciale configuratie nodig voor een klant om profielgegevens te verzenden. De profielinformatie voor een gebruiker wordt typisch overgegaan in het regelmatige [!UICONTROL mbox] verzoek, en de servers zullen de profielparameters voor een gerichte campagneopstelling als standaardfunctionaliteit zonder enige extra opstelling ter beschikking stellen.

Adobe Target heeft ingebouwde Data Workbench-integratie, die van de pagina van de Details van de Cliënt van de Super-gebruiker kan worden toegelaten. Als u deze optie inschakelt, worden segmenten die worden gedeeld vanuit de Data Workbench in Adobe Target, gemarkeerd.

## HTTP-logboekrapportage instellen in ExportIntegration.exe

Lange rapportage reduceren tot [!UICONTROL HTTP.log] wanneer u [!UICONTROL ExportIntegration.exe] om Adobe Target-integratiebestanden te exporteren.

Een nieuwe [!UICONTROL httpLoggingEI.cfg] configuratiebestand (bevindt zich op `server\Admin\Export\httpLoggingEI.cfg`) kunt u uitgebreide logboekregistratie tot de [!UICONTROL HTTP.log] bestand voor het exporteren van gegevens met [!UICONTROL ExportIntegration.exe]. Dit staat u toe om verbose verzoek/reactieregistreren tegen te houden.

Verboden logboekregistratie is al vastgelegd in [!UICONTROL TnTSend.log] bestanden.

_Waar_ plaatst uitgebreide registreren, en _Onwaar_ stopt uitgebreide logboekregistratie naar [!UICONTROL HTTP.log] bestand.

Bij de instelling Onwaar wordt alleen een waarschuwingsbericht verzonden naar de [!UICONTROL HTTP.log] bestand (Info-inhoud niet verzonden).

---
description: Integreer Data Workbench met Adobe Target. Gegevenssegmenten exporteren en exportbestanden automatisch vullen.
title: Integratie van Data Workbench met Adobe Target
exl-id: e7c41e7a-aae6-4b5c-8b14-7ae97b62d70b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---

# Integratie van Data Workbench met Adobe Target

De integratie van de Data Workbench van Adobe met Adobe Target werd gemakkelijker met de eigenschappen van de Data Workbench om gegevenssegmenten uit te voeren en automatisch uitvoerdossiers te bevolken.

De Data Workbench van Adobe verstrekt gesloten-loopintegratie met Adobe Target voor het delen van gegevens en het produceren van rapporten. Binnen Data Workbench kunt u populaties voor zinvolle segmenten analyseren gebruikend alle beschikbare gegevens, met inbegrip van off-line omzettingen door kanalen zoals telefoon, een opslag, etc.

Bijvoorbeeld, zoekt een bezoeker naar schoenen op uw website maar zet niet om. In plaats daarvan downloadt de bezoeker een coupon voor 20 procent van zijn volgende aankoop en koopt hij een shirt in je winkel. Met behulp van Data Workbench kunt u die gegevens verzamelen en die profielgegevens vervolgens weer naar Target duwen om te tonen dat de bezoeker een shirt offline heeft gekocht. U kunt dan een campagne richten die een verbinding aan die bezoeker aanbiedt, wanneer normaal Target zou kunnen proberen om schoenen aan die bezoeker opnieuw op de markt te brengen.

## Data Workbench instellen met Adobe Target

1. Klik met de rechtermuisknop op de koptekst in het venster [!UICONTROL Detail Table].

   ![](assets/insight-to-tnt.png)

1. Selecteer **[!UICONTROL New Target Export]** en voer de naam van een nieuw exportbestand in onder de opdracht **[!UICONTROL Save As]** in het menu.

1. Klik op **[!UICONTROL Save Export File]**.

   Er wordt een venster met een exportsjabloon geopend.

   Alle Adobe Target-gegevens worden automatisch ingevuld. Het bouwt omhoog de parameterlijst op wat u in de segmentuitvoer zet. Als de bewerking is voltooid, stuurt Data Workbench de gegevens naar de Adobe Target-server.

   **Opmerking:** het sjabloonbestand moet door de  [!UICONTROL Profile Architect]gebruiker worden geconfigureerd. De [!UICONTROL Client Name], [!UICONTROL Domain Postfix], [!UICONTROL Mbox Host], en [!UICONTROL Mbox Name] moeten worden ingegaan. Als u meerdere sites hebt, vult u meerdere sjablonen in en slaat u deze op de server op. De sjablonen van Profielbeheer bevinden zich in `Context\FileNew\Detail Table\Export\Copy`.

   ![](assets/insight-to-tnt1.png)

1. Geef de queryparameter [!UICONTROL mboxPC] op.

   Als de naam van het attribuut van de Data Workbench iets buiten [!UICONTROL mboxPC] is, moet u de aangewezen Parameter van de Vraag uitgeven en het anders noemen aan _mboxPC_.

   ![](assets/insight-to-tnt2.png)

   Wanneer u het exportbestand opslaat op de server, wordt het exporteren gestart. Als de [!UICONTROL TnTSend.exe]-toepassing is voltooid, wordt het verzenden van gegevens naar de Target-account gestart en gestart.

## Data Workbench voor doel configureren

Voer de volgende taken uit in Adobe Target:

Data Workbench geeft gebruikersprofielen door aan Adobe Target. Om voor de uitvoer aan Doel te vormen, moet u opstelling en zijn API toelaten en **[!UICONTROL clientname]** en **[!UICONTROL domain postfix]** parameters voor het dossier van de de uitvoerconfiguratie (`export.cfg`) verstrekken.

Er is een nieuwe booleaanse optie met de naam **[!UICONTROL Oneshot]** toegevoegd om exportbestanden te segmenteren. Deze optie is opgenomen in het sjabloonbestand dat met het nieuwe profiel wordt gedistribueerd. Als [!UICONTROL Oneshot] is ingesteld op _true_, wordt de naam van het `.export`-bestand gewijzigd in `.export.done-TIMESTAMP` nadat het exporteren is voltooid, zodat het segment nooit meer dan één keer wordt geëxporteerd. Dit is belangrijk bij het exporteren naar Adobe Target.

**Nota:** Een vraag van Data Workbench aan Adobe Target telt als  [!UICONTROL mbox] vraag, die één vraag voor elk verzonden profiel vereist. Dientengevolge, stijgen de kosten als de veelvoudige vraag tussen de twee oplossingen wordt vereist.

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

Lange rapportage reduceren tot [!UICONTROL HTTP.log] wanneer u [!UICONTROL ExportIntegration.exe] gebruikt om Adobe Target-integratiebestanden te exporteren.

Met een nieuw [!UICONTROL httpLoggingEI.cfg]-configuratiebestand (dat zich bevindt op `server\Admin\Export\httpLoggingEI.cfg`) kunt u uitgebreide logboekregistratie reduceren naar het [!UICONTROL HTTP.log]-bestand voor wanneer u gegevens exporteert met [!UICONTROL ExportIntegration.exe]. Dit staat u toe om verbose verzoek/reactieregistreren tegen te houden.

Bol registreren wordt al vastgelegd in [!UICONTROL TnTSend.log] bestanden.

__ Truesets uitgebreide registreren, en  __ Falsestops verbose registreren aan  [!UICONTROL HTTP.log] dossier.

Bij de instelling Onwaar wordt alleen een waarschuwingsbericht verzonden naar het bestand [!UICONTROL HTTP.log] (Info-inhoud niet verzonden).

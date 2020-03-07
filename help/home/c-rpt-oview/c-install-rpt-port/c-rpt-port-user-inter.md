---
description: De reeksen van het rapport moeten op een specifieke manier worden gevormd om rapporten te veroorzaken die behoorlijk door het Portaal van het Rapport tonen.
solution: Analytics
title: Pas het PortaalGebruikersinterface van het Rapport aan
topic: Data workbench
uuid: d1ea88e2-7b9e-4b1e-a826-dbe7c2e75976
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Pas het PortaalGebruikersinterface van het Rapport aan{#customize-the-report-portal-user-interface}

De reeksen van het rapport moeten op een specifieke manier worden gevormd om rapporten te veroorzaken die behoorlijk door het Portaal van het Rapport tonen.

Het gebruikersinterface voor [!DNL Report Portal] wordt ontworpen om een lusje voor elke rapportvastgestelde omslag te tonen die in de outputfolder verschijnt en in het [!DNL profiles.xml] dossier, evenals het ingebouwde [!DNL Admin] lusje vermeld is, dat aan het te tonen [!DNL TopNavigation.xml] dossier moet worden toegevoegd. Voor meer informatie over het tonen van het ingebouwde [!DNL Admin] lusje, zie het [Verbinden van een Omslag van de Output met een Lusje in de Gebruiker..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee).

![](assets/report_portal_home.png)

* [Zorgen dat Uw Reeksen van het Rapport compatibel met het Portaal van het Rapport zijn..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706)
* [Het verbinden van een Omslag van de Output aan een Lusje in de Gebruiker..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee)

## Zorgen dat Uw Reeksen van het Rapport compatibel met het Portaal van het Rapport zijn {#section-2b141e5d198a4bbea455699126c24706}

Een rapportreeks bepaalt een geplande baan voor [!DNL Report]. Het bestaat uit twee posten:

* Een omslag die de inzameling van werkruimten bepaalt die u als rapporten wilt [!DNL Report] produceren.
* Een configuratiedossier ( [!DNL Report.cfg]).

Onder andere, vertelt het [!DNL Report.cfg] dossier [!DNL Report] wanneer om de rapporten te produceren en waar te om de outputdossiers te bewaren. De reeksen van het rapport verblijven in de omslag van Rapporten op de server van de gegevenswerkbank. Een profiel kan om het even welk aantal rapportreeksen tonen.

Om verenigbaarheid met te verzekeren, moet uw rapportreeksen aan de volgende vereisten voldoen: [!DNL Report Portal]

* De outputfolder voor uw rapportreeksen moet een gevormd [!DNL profiles.xml] dossier bevatten.
* Elke rapportreeks moet een top-level rapport omvatten genoemd &quot;*ReportSetName* Summiere,&quot;waar *ReportSetName* de naam van de rapportreeks aanpast. Bijvoorbeeld, [!DNL Profile Manager] toont het volgende twee rapportreeksen, &quot;Huis&quot;en &quot;Verkeer.&quot; Merk op dat elke rapportreeks een samenvattend rapport ( [!DNL Home Summary.vw] [!DNL Traffic Summary.vw]en, respectievelijk) bepaalt.

![](assets/rptPort_scrn_RptSets.png)

In [!DNL Report Portal], verschijnt het summiere rapport op het lusje van de rapportreeks. Het summiere rapport kan om het even welke werkruimte, venster, of visualisatie bevatten u kiest.

* Het summiere rapport moet het enige rapport in de top-level omslag voor een rapportreeks zijn. Alle andere rapporten moeten in subfolders worden geplaatst. Als u andere rapporten in de top-level omslag plaatst, kunt u hen niet door het portaal bekijken.

## Het verbinden van een Omslag van de Output aan een Lusje in het Gebruikersinterface {#section-3f6bc47d37ed448e871f4f685f46acee}

Om de lusjes te specificeren die u wilt tonen, moet u een [!DNL Report Portal] [!DNL TopNavigation.xml] dossier voor elk profiel vormen. Dit dossier bepaalt welke rapportreeksen als lusjes in het gebruikersinterface voor een bepaald profiel, evenals de orde van die lusjes verschijnen. Het [!DNL TopNavigation.xml] dossier verblijft in de omslag \*PortalName*\PortalFiles\Core\TopNav\*profileName*.

**Om het TopNavigation.xml- dossier uit te geven**

1. Voor de machine waar IIS loopt, open het [!DNL TopNavigation.xml] dossier in een tekstredacteur zoals Blocnote.
1. Geef de lijst van `<TopNav>` elementen uit zodat het de namen en de orde van de rapportreeksen bepaalt de waarvan output u, zoals in het volgende voorbeeld wilt tonen [!DNL Report Portal] :

   ```
   <?xml version="1.0" encoding="UTF-8" standalone="no" ?>
   <TOPNAV_ELEMENTS>
   <TOPNAV>
       <NAME>Monthly Web</NAME>
     </TOPNAV>
     <TOPNAV>
       <NAME>Weekly Web</NAME>
     </TOPNAV>
   <TOPNAV> 
         <NAME>Admin</NAME> 
     </TOPNAV>
   </TOPNAV_ELEMENTS>
   ```

   >[!NOTE]
   >
   >Het [!DNL Admin] lusje is een ingebouwd lusje dat extra functionaliteit verstrekt. Als u het niet in het [!DNL TopNavigation.xml] dossier omvat, toont dit lusje niet en zijn functionaliteit is niet beschikbaar.

1. In \*PortalName*\PortalFiles\Core\TopNav\ folder, creeer een omslag voor uw volgende profiel.
1. Kopieer het [!DNL TopNavigation.xml] dossier van de eerste profielomslag en kleef het in de nieuwe omslag.
1. Bewerk het bestand [!DNL TopNavigation.xml] indien nodig en sla het op.
1. Herhaal Stappen 3-5 voor alle andere profielen beschikbaar in uw portaal.


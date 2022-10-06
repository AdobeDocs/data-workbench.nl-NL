---
description: De reeksen van het rapport moeten op een specifieke manier worden gevormd om rapporten te produceren die behoorlijk door het Portaal van het Rapport tonen.
title: Pas het Portaalgebruikersinterface van het Rapport aan
uuid: d1ea88e2-7b9e-4b1e-a826-dbe7c2e75976
exl-id: 1f7c807d-d896-448f-b9dd-9fe6a68ef27e
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Pas het Portaalgebruikersinterface van het Rapport aan{#customize-the-report-portal-user-interface}

{{eol}}

De reeksen van het rapport moeten op een specifieke manier worden gevormd om rapporten te produceren die behoorlijk door het Portaal van het Rapport tonen.

De gebruikersinterface voor [!DNL Report Portal] is ontworpen om een tabblad weer te geven voor elke rapportsetmap die wordt weergegeven in de uitvoerdirectory en wordt vermeld in de [!DNL profiles.xml] en de ingebouwde [!DNL Admin] , die moet worden toegevoegd aan de [!DNL TopNavigation.xml] bestand dat moet worden weergegeven. Voor meer informatie over het weergeven van de ingebouwde [!DNL Admin] tab, zie [Een uitvoermap koppelen aan een tabblad in de gebruiker...](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee).

![](assets/report_portal_home.png)

* [Ervoor zorgen dat uw rapportsets compatibel zijn met Report Portal...](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706)
* [Een uitvoermap koppelen aan een tabblad in de gebruiker...](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-3f6bc47d37ed448e871f4f685f46acee)

## Ervoor zorgen dat uw rapportsets compatibel zijn met Report Portal {#section-2b141e5d198a4bbea455699126c24706}

Een rapportset definieert een geplande taak voor [!DNL Report]. Het bestaat uit twee posten:

* Een map die de verzameling werkruimten definieert die u wilt [!DNL Report] om als rapporten te produceren.
* Een configuratiebestand ( [!DNL Report.cfg]).

De [!DNL Report.cfg] bestand vertelt [!DNL Report] wanneer de rapporten moeten worden gegenereerd en waar de uitvoerbestanden moeten worden opgeslagen. Rapportsets bevinden zich in de map Rapporten op de gegevenswerkbankserver. Een profiel kan om het even welk aantal rapportreeksen tonen.

Om verenigbaarheid met [!DNL Report Portal], moet uw rapportreeksen aan de volgende vereisten voldoen:

* De outputfolder voor uw rapportreeksen moet gevormd bevatten [!DNL profiles.xml] bestand.
* Elke rapportset moet een rapport op hoofdniveau met de naam &quot;*ReportSetName* Samenvatting&quot; *ReportSetName* komt overeen met de naam van de rapportset. Het volgende wordt bijvoorbeeld [!DNL Profile Manager] toont twee rapportreeksen, &quot;Huis&quot;en &quot;Verkeer.&quot; Merk op dat elke rapportreeks een samenvattingsrapport bepaalt ( [!DNL Home Summary.vw] en [!DNL Traffic Summary.vw], respectievelijk).

![](assets/rptPort_scrn_RptSets.png)

In [!DNL Report Portal], verschijnt het samenvattingsrapport op het lusje van de rapportreeks. Het samenvattingsrapport kan elke gewenste werkruimte, elk gewenst venster of elke gewenste visualisatie bevatten.

* Het samenvattingsrapport moet het enige rapport zijn in de map op het hoogste niveau voor een rapportset. Alle andere rapporten moeten in subfolders worden geplaatst. Als u andere rapporten in de top-level omslag plaatst, kunt u hen niet door het portaal bekijken.

## Een uitvoermap koppelen aan een tabblad in de gebruikersinterface {#section-3f6bc47d37ed448e871f4f685f46acee}

De gewenste tabbladen opgeven [!DNL Report Portal] om te tonen, moet u vormen [!DNL TopNavigation.xml] bestand voor elk profiel. Dit dossier bepaalt welke rapportreeksen als lusjes in het gebruikersinterface voor een bepaald profiel, evenals de orde van die lusjes verschijnen. De [!DNL TopNavigation.xml] Het bestand bevindt zich in de map \*PortalName*\PortalFiles\Core\TopNav\*profileName*.

**Het bestand TopNavigation.xml bewerken**

1. Open op de computer waarop IIS wordt uitgevoerd de [!DNL TopNavigation.xml] bestand in een teksteditor, zoals Kladblok.
1. De lijst met `<TopNav>` elementen zodat het de namen en de orde van de rapportreeksen bepaalt waarvan output u wilt [!DNL Report Portal] om weer te geven, zoals in het volgende voorbeeld:

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
   >De [!DNL Admin] tab is een ingebouwde tab die aanvullende functionaliteit biedt. Als u deze niet opneemt in het dialoogvenster [!DNL TopNavigation.xml] wordt op dit tabblad niet weergegeven en is de functionaliteit ervan niet beschikbaar.

1. Maak in de map \*PortalName*\PortalFiles\Core\TopNav\ folder een map voor uw volgende profiel.
1. Kopieer de [!DNL TopNavigation.xml] in de eerste profielmap en plak deze in de nieuwe map.
1. Bewerk de [!DNL TopNavigation.xml] Sla het bestand op, indien nodig.
1. Herhaal stap 3-5 voor alle andere profielen beschikbaar in uw portaal.

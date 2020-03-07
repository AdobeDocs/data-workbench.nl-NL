---
description: Normaal, beantwoordt de server van de Werkbank van Gegevens inkomende gebruikersvragen aangezien zij worden ontvangen, en blijft resultaten en updates in real time verstrekken tot de gebruiker niet meer om hen verzoekt.
solution: Analytics
title: Zoekwachtrij
topic: Data workbench
uuid: 4d64bc89-b664-4532-9f17-be11812d36d4
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Zoekwachtrij{#query-queue}

Normaal, beantwoordt de server van de Werkbank van Gegevens inkomende gebruikersvragen aangezien zij worden ontvangen, en blijft resultaten en updates in real time verstrekken tot de gebruiker niet meer om hen verzoekt.

Soms, vooral op systemen met vele gebruikers van de Werkbank van Gegevens, vereist het aantal actieve vragen meer systeemmiddelen dan beschikbaar bij de server zijn. [!DNL Query Queue] staat de server toe om sommige vragen tijdelijk op greep te plaatsen tot de middelen noodzakelijk om antwoorden te verstrekken beschikbaar worden. De eigenschappen [!DNL Query Queue] verstrekken ook om vragen voorrang te geven die op een verscheidenheid van parameters worden gebaseerd, zodat in het geval van middelgeschil, de hoog-prioritaire vragen eerst worden beantwoord.

De vragen van één enkele cliënt of rapportserver worden geplaatst in een bos en gepland als eenheid. U kunt middelmonitors vormen om de hoeveelheid bepaalde systeemmiddelen te beperken die door vragen worden gebruikt. Wanneer de gecontroleerde middelen het plannen van een andere vraagsteller toestaan, is de hoogst-prioritaire bos gepland. De gebruikers de van wie vragen nog niet gepland zijn, wegens middelbeperkingen, ontvangen geen fout maar meegedeeld dat hun vragen een rij worden gevormd, en de gebruiker kan blijven aan de lokale steekproef werken.

De standaardconfiguratie omvat een eenvoudige configuratie voor [!DNL Query Queue], maar verlaat het gehandicapt. De beheerders kunnen toelaten of onbruikbaar maken [!DNL Query Queue], middelmonitors vormen om te bepalen hoeveel van diverse middelen voor het vragen worden gebruikt, en vormen complex prioritization beleid voor verschillende gebruikers.

**Om het dossier te vormen Server.cfg voor[!DNL Query Queuing]**

1. Open [!DNL Server.cfg] door te klikken **[!UICONTROL Admin]** > **[!UICONTROL Profile Manager]** > **[!UICONTROL Dataset]**.
1. Klik met de rechtermuisknop **[!UICONTROL Server.cfg]** en maak het lokaal voor het uitgeven.
1. Breid uit [!DNL Query Queue].

   ![](assets/queryqueue1.png)

1. Vorm de volgende parameters:

   * **Gebruikersgroepen:** Laat u beleid, gebruikers, en de rijprioriteit vormen. Zie Gebruikersgroepen [van de Rij van de](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-user-grps.md#concept-5555f51402ed49419c067d61738474c1) Vraag voor definities.

   * **Actief:** (Vector) laat of maakt het toe onbruikbaar [!DNL Query Queue]. De geldige waarden zijn waar of vals. Standaard het plaatsen is vals.

   * **Standaardgebruikersgroep:** (Koord) Type een naam van de gebruikersgroep waaraan de gebruikers worden toegevoegd, als zij niet vermeld in om het even welke gebruikersgroep zijn.
   * **Bronnenmonitoren:** (Vector) klik met de rechtermuisknop om een middelmonitor toe te voegen. U kunt specificeren of het [!DNL Query Queue] monitorgeheugen of het aantal vragen. Klik met de rechtermuisknop **[!UICONTROL Resource Monitor]** om de Monitor van de Begroting van het Geheugen of Aantal de Monitor van Vragen te kiezen. Zie de Monitoren [van het Middel van de Rij van de](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-res-mon.md#concept-0840967b228c4d5ba3b59b4b2759f325) Vraag voor meer informatie.

   * **Onaanraakbare prioriteit:** (Int) specificeert dat de trossen met een prioriteit groter dan of gelijk aan deze waarde nooit aan het plannen van hogere prioritaire bunches worden voorrang gegeven. Gebruikt samen met [!DNL Memory Budget Monitor] beschreven in de Lijst [van de Parameters van de](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-user-grps.md#concept-5555f51402ed49419c067d61738474c1)Gebruikersgroep.


---
description: Normaal, beantwoordt de server van de Data Workbench inkomende gebruikersvragen aangezien zij worden ontvangen, en blijft resultaten en updates in real time verstrekken tot de gebruiker hen niet meer verzoekt.
title: Query-wachtrij
uuid: 4d64bc89-b664-4532-9f17-be11812d36d4
exl-id: 5d9b20bf-9396-4016-beed-cee8f533f3ea
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Query-wachtrij{#query-queue}

{{eol}}

Normaal, beantwoordt de server van de Data Workbench inkomende gebruikersvragen aangezien zij worden ontvangen, en blijft resultaten en updates in real time verstrekken tot de gebruiker hen niet meer verzoekt.

Soms, vooral op systemen met vele gebruikers van de Data Workbench, vereist het aantal actieve vragen meer systeemmiddelen dan bij de server beschikbaar zijn. [!DNL Query Queue] staat de server toe om sommige vragen tijdelijk op greep te plaatsen tot de middelen noodzakelijk om antwoorden te verstrekken beschikbaar worden. De [!DNL Query Queue] verstrekt ook eigenschappen om vragen voorrang te geven die op een verscheidenheid van parameters worden gebaseerd, zodat in het geval van middelgeschil, de hoog-prioritaire vragen eerst worden beantwoord.

De vragen van één enkele cliënt of rapportserver worden geplaatst in een bos en gepland als eenheid. U kunt middelmonitors vormen om de hoeveelheid bepaalde systeemmiddelen te beperken die door vragen worden gebruikt. Wanneer de gecontroleerde middelen het plannen van een andere vraagsteller toestaan, is de hoogst-prioritaire bos gepland. De gebruikers de waarvan vragen nog niet gepland zijn, wegens middelbeperkingen, ontvangen geen fout maar worden meegedeeld dat hun vragen een rij worden gevormd, en de gebruiker kan aan de lokale steekproef blijven werken.

De standaardconfiguratie bevat een eenvoudige configuratie voor de [!DNL Query Queue], maar laat het uitgeschakeld. Beheerders kunnen de [!DNL Query Queue], configureert u middelenmonitoren om te bepalen hoeveel van de verschillende bronnen worden gebruikt voor het opvragen en configureert u een complex prioriteitsbeleid voor verschillende gebruikers.

**Het bestand Server.cfg configureren voor[!DNL Query Queuing]**

1. Openen [!DNL Server.cfg] door te klikken **[!UICONTROL Admin]** > **[!UICONTROL Profile Manager]** > **[!UICONTROL Dataset]**.
1. Klikken met rechtermuisknop **[!UICONTROL Server.cfg]** en deze lokaal maken voor bewerken.
1. Uitbreiden [!DNL Query Queue].

   ![](assets/queryqueue1.png)

1. Configureer de volgende parameters:

   * **Gebruikersgroepen:** Hiermee kunt u beleid, gebruikers en de prioriteit van de wachtrij configureren. Zie [Gebruikersgroepen Query-wachtrij](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-user-grps.md#concept-5555f51402ed49419c067d61738474c1) voor definities.

   * **Actief:** (Vector) Schakelt het [!DNL Query Queue]. Geldige waarden zijn true of false. De standaardinstelling is false.

   * **Standaardgebruikersgroep:** (Tekenreeks) Typ een naam van de gebruikersgroep waaraan gebruikers worden toegevoegd, als deze niet in een gebruikersgroep staan.
   * **Bronmonitoren:** (Vector) Klik met de rechtermuisknop om een bronmonitor toe te voegen. U kunt opgeven of de [!DNL Query Queue] controleert geheugen of het aantal vragen. Klikken met rechtermuisknop **[!UICONTROL Resource Monitor]** om de Monitor van de Begroting van het Geheugen of Aantal Monitor van Vragen te kiezen. Zie [Bronnen voor query-wachtrij](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-res-mon.md#concept-0840967b228c4d5ba3b59b4b2759f325) voor meer informatie .

   * **Onaanraakbare prioriteit:** (Int) Geeft aan dat bunches met een prioriteit die groter is dan of gelijk is aan deze waarde, nooit worden voorspeld bij het plannen van hosprioriteitsbunches. Wordt gebruikt in combinatie met de [!DNL Memory Budget Monitor] in de [Parameters gebruikersgroep, tabel](../../../../home/c-get-started/c-admin-intrf/c-query-que/c-query-que-user-grps.md#concept-5555f51402ed49419c067d61738474c1).

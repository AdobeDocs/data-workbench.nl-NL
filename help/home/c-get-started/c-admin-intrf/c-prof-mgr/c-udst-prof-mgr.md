---
description: De map en bestandsnamen die in de implementatie zijn opgenomen, worden links in Profielbeheer weergegeven.
title: Profielbeheer
uuid: c3a19a56-c96b-4661-b656-b845feba4b6f
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 0%

---


# Profielbeheer{#profile-manager}

De map en bestandsnamen die in de implementatie zijn opgenomen, worden links in Profielbeheer weergegeven.

De profielen waaruit de toepassing bestaat, worden weergegeven als de afzonderlijke kolommen in de [!DNL Profile Manager]. Deze profielen bevatten meerdere overgeërfde profielen en één werkprofiel.

>[!NOTE]
>
>Uw werkprofiel (of een datasetprofiel of een rol-specifiek profiel) is het profiel dat u laadt wanneer u Data Workbench opent.

De vinkjes (en de kleuren ervan) geven de profielmap(pen) aan op de Data Workbench-server en de Data Workbench-computer waarin elk bestand zich bevindt, of meerdere kopieën van een bestand bestaan en of deze meerdere kopieën dezelfde datum en tijd hebben als gewijzigd. Deze bestanden worden tijdens het downloaden van profielen gesynchroniseerd tussen de Data Workbench-server en de Data Workbench-computers.

Hier volgt een voorbeeld [!DNL Profile Manager] voor een HBX implementatie:

![](assets/client-prof.png)

Vanuit het menu [!DNL Profile Manager] kunt u elk van de andere managers openen (bijvoorbeeld [!DNL Dimensions Manager] of [!DNL Reports Manager]), die alleen bepaalde delen van [!DNL Profile Manager] weergeven. U kunt ook nieuwe profielmanagers tot stand brengen. Zie [Nieuwe profielmanagers maken](../../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-prof-files-mgrs/c-new-prof-mgrs.md#concept-0021e006523e4d538aaa16322731d9d3).

Een vinkje naast een bestandsnaam in een bepaalde kolom geeft aan dat een bestand met die naam zich in de map bevindt die in die kolom (profiel) staat. Als u in de [!DNL Profile Manager] naar rechts gaat, hebben de bestanden voorrang op de bestanden aan de linkerkant. Elk overgeërfd profiel bouwt dus voort op de profielen aan de linkerkant in [!DNL Profile Manager]. Als u bijvoorbeeld een bestand hebt met dezelfde naam en op dezelfde locatie in het [!DNL Base]-profiel (kolom) en in het [!DNL User]-profiel (kolom), wordt het bestand in het [!DNL User]-profiel gebruikt in plaats van het bestand in het [!DNL Base]-profiel.

## Zoeken naar profielen {#section-91f873f1d7ed4fd6a5f3c3ac08cfa623}

Met Data Workbench 5.5 is een zoekveld toegevoegd om de vereiste profielen te zoeken in [!DNL Profile Manager].

![](assets/client-prof2.png)

De volgende typen kolommen worden weergegeven in de [!DNL Profile Manager]:

* De kolommen *overgeërfde profielnaam* bevatten vinkjes voor dossiers die in elke profielomslag verblijven. Geërfde profielen omvatten interne profielen die door Adobe worden verstrekt evenals om het even welke bedrijf-specifieke of rol-specifieke profielen die u creeert en handhaaft. In het bovenstaande voorbeeld omvatten de interne profielen Basis, Verkeer, Waarde, Marketing, enzovoort. Het interne [!DNL Base] profiel, dat de basisbouwstenen en configuratieinformatie nodig bevat om uw toepassing van de Adobe in werking te stellen, wordt voorzien van elke implementatie. De andere interne profielen bevatten elementen (werkruimten, metriek, afgeleide dimensies, etc.) met betrekking tot bepaalde soorten informatie, zoals Webverkeer of marketing. Adobe biedt alleen profielen die geschikt zijn voor het type gegevens dat u analyseert en voor uw branche.

   >[!NOTE]
   >
   >Intern profiel (opgegeven door Adobe) kan standaard niet worden gewijzigd. Alle aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert. Als u een nieuwe toepassing bouwt en een intern profiel moet veranderen, moet u de Modify Interne parameter van Profielen in het [!DNL Insight.cfg] dossier veranderen. Zie [De Parameters van de Configuratie van het Inzicht](../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b) voor meer informatie. Neem voordat u dit doet contact op met de Adobe Consulting Services.

* De kolom *werkprofielnaam*, die altijd de kolom naast elkaar is, bevat vinkjes voor bestanden die zich in de map van het huidige werkprofiel bevinden. In het bovenstaande voorbeeld is het werkprofiel Dataset. Uw werkprofiel is of een datasetprofiel of een rol-specifiek profiel. De bestanden in deze map hebben voorrang op bestanden met dezelfde naam in een overgenomen profielmap.
* De kolom [!DNL User], die altijd de laatste kolom is, bevat vinkjes voor bestanden en mappen die zich als lokale bestanden in de map User\*profile name* bevinden. De mappenstructuur van de map Gebruiker bootst de structuur van het werkprofiel na en elke map met een gebruikersprofiel\*profielnaam* bevat lokale kopieën van de werkruimten, meetgegevens, afmetingen en configuratiebestanden voor dat specifieke profiel. Deze lokale kopieën hebben voorrang op bestanden met dezelfde namen in een overgeërfde map of werkprofielmap. De bestanden in de kolom [!DNL User] zijn gemaakt en alleen opgeslagen in de map User\*profile name*, of ze bevinden zich in een intern profiel of in een werkprofiel en in de map User\*profile name*. De bestanden in elke map kunnen al dan niet identiek zijn en hebben mogelijk dezelfde datum en tijd als gewijzigd.

   >[!NOTE]
   >
   >
   >    
   >    
   >    * Om te voorkomen dat u uw gegevensset alleen lokaal wijzigt, negeert de server van de Data Workbench de lokale kopieën van het [!DNL profile.cfg]-bestand en alle bestanden in de mappen Gegevensset of Exporteren in de map Gebruiker\*profielnaam*. Genegeerde bestanden worden aangegeven met een rode achtergrond in de kolom [!DNL User] en de waarschuwing &quot;Genegeerd in gebruikersmap&quot; in het contextmenu. Als u de wijzigingen die u aanbrengt in uw lokale kopieën van deze bestanden wilt implementeren, moet u deze opslaan in uw werkprofiel zodat ze kunnen worden gesynchroniseerd met de Data Workbench-server. Zie [Bestanden publiceren naar uw werkprofiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9) voor stappen om bestanden op te slaan in uw werkprofiel.
      >    
      >    
   * Een afbreekstreepje (-) in plaats van een vinkje in een kolom geeft een leeg (nulbyte) bestand aan. Data Workbench behandelt bestanden met een lengte van nul bytes als niet bestaand, zodat u deze kunt gebruiken om bestanden die in een profiel aan de linkerkant zijn opgenomen, te verbergen. Zie [Bestanden verbergen met lege bestanden (nulbyte)](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491).


## Bestandsversies {#section-225d732246b94cbe87acdfa9c881d6af} bepalen

Zoals vermeld in de vorige sectie, zijn de controlemerken in [!DNL Profile Manager] kleur-gecodeerd zodat u gemakkelijk kunt identificeren waar een dossier verblijft en of de veelvoudige exemplaren van een dossier op verschillende tijden werden gewijzigd.

Als een bestand of samengevouwen map precies hetzelfde is als het bestand of de map aan de linkerkant, heeft het bestand of de map dezelfde kleurcontrole als het bestand of de map in die kolom (profiel). Als het van om het even welk dossier of folder aan zijn linkerzijde verschillend is, of het dossier of de folder slechts in [!DNL User] kolom bestaat, is het vinkje wit.

![](assets/vis_ProfMgr_LocalFiles.png)

De [!DNL Profile Manager] in het bovenstaande voorbeeld geeft het volgende aan:

* Een wit vinkje voor het [!DNL A New Metric.metric] dossier verschijnt slechts in [!DNL User] kolom, die erop wijst dat u slechts een lokaal exemplaar van dat dossier-het niet gepubliceerd (of geupload) aan de server van de Data Workbench voor andere gebruikers van de Data Workbench om hebt toegang.

* Er worden vinkjes voor de bestandsnaam [!DNL Average Score.metric] weergegeven in de kolommen Films en [!DNL User]. Het vinkje in de kolom [!DNL User] is de zelfde kleur als het vinkje in de kolom van Films, die erop wijst dat het lokale exemplaar van het dossier de zelfde Gewijzigde datum en tijd zoals het dossier in de omslag van Films heeft.

* Er worden vinkjes voor de bestandsnaam [!DNL Average Score Error.metric] weergegeven in de kolommen Films en [!DNL User]. Het vinkje in de kolom [!DNL User] is wit, wat erop wijst dat de lokale kopie van het dossier een verschillende Gewijzigde datum of tijd heeft dan het dossier in de omslag van Films.


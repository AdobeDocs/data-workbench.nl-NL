---
description: De omslag en de dossiernamen inbegrepen in uw implementatie worden getoond op de linkerkant van de Manager van het Profiel.
solution: Analytics
title: Profielbeheer
topic: Data workbench
uuid: c3a19a56-c96b-4661-b656-b845feba4b6f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Profielbeheer{#profile-manager}

De omslag en de dossiernamen inbegrepen in uw implementatie worden getoond op de linkerkant van de Manager van het Profiel.

De profielen die omhoog uw toepassing maken worden getoond als individuele kolommen in [!DNL Profile Manager]. Deze profielen omvatten veelvoudige geërfte profielen en één enkel werkend profiel.

>[!NOTE]
>
>Uw het werk profiel (of een datasetprofiel of een rol-specifiek profiel) is het profiel dat u wanneer u de Werkbank van Gegevens opent laadt.

De vinkjes (en hun kleuren) geven de profielmap(en) aan op de server van de Werkbank van Gegevens en de computers van de Werkbank waarin elk bestand zich bevindt, of er meerdere kopieën van een bestand bestaan en of die meerdere kopieën dezelfde datum en tijd hebben als de gewijzigde versies. Deze dossiers zijn gesynchroniseerd tussen de server van de Werkbank van Gegevens en de computers van de Werkbank van Gegevens tijdens profieldownload.

Hierna volgt een voorbeeld [!DNL Profile Manager] voor een HBX-implementatie:

![](assets/client-prof.png)

Van het [!DNL Profile Manager] menu, kunt u om het even welke andere managers (bijvoorbeeld, [!DNL Dimensions Manager] of [!DNL Reports Manager]) openen, die slechts bepaalde gedeelten van tonen [!DNL Profile Manager]. U kunt ook nieuwe profielmanagers maken. Zie Profielbeheer [maken](../../../../home/c-get-started/c-intf-anlys-ftrs/c-cstm-prof-files-mgrs/c-new-prof-mgrs.md#concept-0021e006523e4d538aaa16322731d9d3).

Een vinkje naast een dossier - noem in een bepaalde kolom wijst erop dat een dossier door die naam in de omslag verblijft die in die kolom (profiel) wordt genoemd. Aangezien u zich aan het recht in beweegt, [!DNL Profile Manager]nemen de dossiers belangrijkheid over die aan de linkerzijde, dat wil zeggen, bouwt elk geërfd profiel op de profielen aan zijn linkerzijde in [!DNL Profile Manager]. Bijvoorbeeld, als u een dossier van de zelfde naam en in de zelfde plaats in het [!DNL Base] profiel (kolom) en in het [!DNL User] profiel (kolom) hebt, wordt het dossier in het [!DNL User] profiel gebruikt in plaats van het dossier in het [!DNL Base] profiel.

## Zoeken naar profielen {#section-91f873f1d7ed4fd6a5f3c3ac08cfa623}

Met Data Workbench 5.5 is een zoekveld toegevoegd om de gewenste profielen in het veld te vinden [!DNL Profile Manager].

![](assets/client-prof2.png)

De volgende types van kolommen verschijnen in [!DNL Profile Manager]:

* De *geërfte kolommen van de profielnaam* bevatten controletekens voor dossiers die in elke profielomslag verblijven. De ingegane profielen omvatten interne profielen die door Adobe worden verstrekt evenals om het even welke bedrijf-specifieke of rol-specifieke profielen die u creeert en handhaaft. In het voorbeeld hierboven, omvatten de interne profielen Basis, Verkeer, Waarde, Marketing, etc. Het interne [!DNL Base] profiel, dat de basisbouwstenen en configuratieinformatie nodig bevat om uw toepassing van Adobe in werking te stellen, wordt voorzien van elke implementatie. De andere interne profielen bevatten elementen (werkruimten, metriek, afgeleide afmetingen, etc.) met betrekking tot bepaalde soorten informatie, zoals Webverkeer of marketing. Adobe verstrekt slechts die profielen die voor het type van gegevens aangewezen zijn u analyseert en voor uw industrie.

   >[!NOTE]
   >
   >Door gebrek, kunnen de interne profielen (die verstrekt door Adobe) niet worden veranderd. Al aanpassing moet in uw dataset of rol-specifieke profielen of andere profielen voorkomen die u creeert. Als u een nieuwe toepassing bouwt en een intern profiel moet veranderen, moet u de Modify Interne parameter van Profielen in het [!DNL Insight.cfg] dossier veranderen. Zie de Parameters [van de Configuratie van het](../../../../home/c-get-started/c-insght-config-param.md#concept-14da97d0756348e885c08ca9e866074b) Inzicht voor meer informatie. Alvorens dit te doen, contacteer de Raadplegende Diensten van Adobe.

* De kolom van de naam *van het* werkende profiel, die altijd de volgende-aan-laatste kolom is, bevat controletekens voor dossiers die in de omslag van het huidige het werkprofiel verblijven. In het voorbeeld hierboven, is het het werk profiel Dataset. Uw het werk profiel is of een datasetprofiel of een rol-specifiek profiel. De dossiers in deze omslag nemen belangrijkheid over om het even welke dossiers met de zelfde namen in om het even welke geërfte profielomslag.
* De [!DNL User] kolom, die altijd de laatste kolom is, bevat vinkjes voor bestanden en mappen die zich als lokale bestanden bevinden in de map User\*profile name*. De folderstructuur van de omslag van de Gebruiker bootst dat van het het werk profiel na, en elke omslag van de Naam* van het Profiel van de Gebruiker \*bevat lokale exemplaren van de werkruimten, metriek, afmetingen, en configuratiedossiers voor dat bepaalde profiel. Deze lokale exemplaren nemen belangrijkheid over om het even welke dossiers met de zelfde namen in om het even welke geërfte of werkende profielomslag. De bestanden in de [!DNL User] kolom zijn gemaakt en alleen opgeslagen in de map User\*profile name* of in een intern of werkprofiel en in de map User\*profile name*. De dossiers in elke omslag kunnen of kunnen niet identiek zijn en kunnen niet de zelfde Gewijzigde datum en de tijd hebben.

   >[!NOTE]
   >
   >
   >    
   >    
   >    * Om te vermijden veranderend uw dataset slechts plaatselijk, negeert de server van de Werkbank van Gegevens de lokale exemplaren van het [!DNL profile.cfg] dossier en om het even welke dossiers in de omslagen van de Dataset of van de Uitvoer in de Gebruiker \*profiel naam* omslag. De genegeerde dossiers worden geïdentificeerd door een rode achtergrond in de [!DNL User] kolom en een &quot;Ontbroken in de folder van de Gebruiker&quot;waarschuwing in het contextmenu. Om de veranderingen uit te voeren u in uw lokale exemplaren van deze dossiers aanbrengt, moet u hen aan uw werkend profiel bewaren zodat zij met de server van de Werkbank van Gegevens kunnen worden gesynchroniseerd. Voor stappen om dossiers aan uw het werk profiel op te slaan, zie het [Publiceren Dossiers aan Uw het Werk Profiel](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/t-pub-files-wkg-prof.md#task-a0106e010c834d16bd60eef4721b6af9).
      >    
      >    
   * Een koppelteken (-) in plaats van een vinkje in een kolom identificeert een leeg (nul-byte) dossier. De Werkbank van gegevens behandelt nul-bytedossiers als niet-bestaand, die u toelaat om hen te gebruiken om dossiers te verbergen inbegrepen in een profiel aan de linkerzijde. Zie Bestanden [verbergen met lege bestanden (nul-byte)](../../../../home/c-get-started/c-admin-intrf/c-prof-mgr/c-empty-files.md#concept-e776fac9e5904bed8c13b9d5eb17c491).


## Bestandsversies bepalen {#section-225d732246b94cbe87acdfa9c881d6af}

Zoals vermeld in de vorige sectie, [!DNL Profile Manager] zijn de controletekens in kleur-gecodeerd zodat u kunt gemakkelijk identificeren waar een dossier verblijft en of de veelvoudige exemplaren van een dossier op verschillende tijden werden gewijzigd.

Als een dossier of een doen ineenstorten folder precies het zelfde als het dossier of de folder aan zijn linkerzijde is, heeft het het zelfde teken van de kleurencontrole zoals het dossier of de folder in die kolom (profiel). Als het van om het even welk dossier of folder aan zijn linkerzijde verschillend is, of het dossier of de folder bestaan slechts in de [!DNL User] kolom, is het vinkje wit.

![](assets/vis_ProfMgr_LocalFiles.png)

De [!DNL Profile Manager] afbeelding in het bovenstaande voorbeeld geeft het volgende aan:

* Een wit vinkje voor het [!DNL A New Metric.metric] dossier verschijnt slechts in de [!DNL User] kolom, die erop wijst dat u slechts een lokaal exemplaar van dat dossier-het niet (of geupload) aan de server van de Werkbank van Gegevens voor andere gebruikers van de Werkbank van Gegevens aan toegang hebt gepubliceerd.

* De tekens van de controle voor het [!DNL Average Score.metric] dossier - de naam verschijnen in de Films en de [!DNL User] kolommen. Het vinkje in de [!DNL User] kolom is de zelfde kleur als het vinkje in de kolom van Films, die erop wijst dat het lokale exemplaar van het dossier de zelfde Gewijzigde datum en de tijd zoals het dossier in de omslag van Films heeft.

* De tekens van de controle voor het [!DNL Average Score Error.metric] dossier - de naam verschijnen in de Films en de [!DNL User] kolommen. Het vinkje in de [!DNL User] kolom is wit, wat erop wijst dat het lokale exemplaar van het dossier een verschillende Gewijzigde datum of een tijd dan het dossier in de omslag van Films heeft.


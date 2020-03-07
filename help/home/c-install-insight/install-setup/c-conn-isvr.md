---
description: Nadat u uw software van het Inzicht en digitaal certificaat hebt geïnstalleerd, moet u Inzicht beginnen en zijn verbinding aan de Server van het Inzicht vormen.
title: Het vormen van de Verbinding aan de Server van het Inzicht
uuid: 8ba13da6-8749-49fe-a29e-dac3906f71b8
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Het vormen van de Verbinding aan de Server van het Inzicht{#configuring-the-connection-to-insight-server}

Nadat u uw software van het Inzicht en digitaal certificaat hebt geïnstalleerd, moet u Inzicht beginnen en zijn verbinding aan de Server van het Inzicht vormen.

>[!NOTE]
>
>In sommige gevallen, kan de verbinding aan de Server van het Inzicht pre-gevormd zijn door de Raadplegende Diensten van Adobe of uw systeembeheerder. Zo ja, dan hoeft u deze taak niet te voltooien.

Wanneer u Inzicht voor het eerst begint, verbindt het automatisch met de Server van de Vergunning van Adobe om uw digitaal certificaat te registreren. Om het registratieproces met succes te voltooien, moet uw computer met Internet worden verbonden wanneer u de volgende stappen uitvoert.

>[!NOTE]
>
>Als u reeds, een vooraf gesloten certificaat zoals beschreven in het [Downloaden van en het Installeren van het Digitale Certificaat](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#topic-fed3b44e472c4e4ca6dd5852af14cdb9)hebt gevraagd gedownload en geïnstalleerd, zal het Inzicht niet proberen om met de Server van de Vergunning te verbinden en u zult geen fout ontvangen.

**Om de verbinding aan de Server van het Inzicht te vormen**

Wanneer het werken in een gegroepeerd milieu, zou het Inzicht moeten worden gevormd om tot de hoofdserver van het Inzicht toegang te hebben om synchronisatiekwesties te vermijden. In Inzicht kunt u informatie over de verwerking [!DNL Insight Servers] in uw cluster bekijken gebruikend het [!DNL Related Servers] menupunt in de Manager [van](https://docs.adobe.com/content/help/en/data-workbench/using/client/admin-ui/c-svrs-mgr.html)Servers.

1. Inzicht starten.
1. Op de [!DNL Worktop], klik **[!UICONTROL Admin]**, dan **[!UICONTROL First Steps]**.

1. Klik de **[!UICONTROL Configure Connection to Servers]** duimnagel.

   Het [!DNL Servers Manager], het [!DNL Insight.cfg] dossier, en de instructies voor het vormen van uw [!DNL Insight.cfg]dossier worden getoond.

1. Klik in het [!DNL Insight.cfg] venster met de rechtermuisknop **[!UICONTROL Servers]** en klik op **[!UICONTROL Add new child]** > **[!UICONTROL Server]**.

   ![](assets/cfg_Workstation_AddChild.png)

1. Voltooi of wijzig de serverparameters om Inzicht van toegang tot uw hoofdServer van het Inzicht te voorzien. Voor gedetailleerde beschrijvingen van de parameters in het dossier Insight.cfg, zie de parameters [van de](https://docs.adobe.com/content/help/en/data-workbench/using/client/c-insght-config-param.html)Configuratie.

   ![](assets/cfg_Workstation_AddServer.png)

1. Herhaal Stap 4 en Stap 5 voor elke Server van het Inzicht waaraan u een verbinding wilt vormen.
1. Om uw configuratieveranderingen te bewaren, klik **[!UICONTROL Insight.cfg (modified)]** bij de bovenkant van het venster met de rechtermuisknop aan en klik **[!UICONTROL Save as Insight.cfg]**.

   Het inzicht probeert om met het [!DNL Insight Server(s)] gebruiken van de montages te verbinden die u hebt gespecificeerd. Als een verbinding wordt gevestigd, verschijnt een groene knoop in de [!DNL Servers Manager] zoals aangetoond op de volgende pagina.

   ![](assets/vis_SysStat_RedGreenDots.png)

   * **Groen:** Wijst erop dat de verbinding aan de Server van het Inzicht actief is.
   * **Licht rood:** Wijst op een potentieel probleem met de server, zoals een afvoer op serververwerking, hoog geheugengebruik, of lage schijfruimte.
   * **Rood:** Wijst erop dat de verbinding aan de Server van het Inzicht niet actief is.
   Als het Inzicht niet kan verbinden gebruikend de gespecificeerde montages, verschijnt een rode knoop in [!DNL Servers Manager]. Als dit gebeurt, zie het Oplossen van problemen van de [Verbinding](../../../home/c-install-insight/install-setup/t-conn-trbsh.md#task-034e588c5ce04c4a8f6d0097364d3b2b).

<!--
c_dir_crt_setup.xml
-->

Wanneer u een te gebruiken profiel selecteert, wordt de profielinformatie (met inbegrip van verwante gegevens en om het even welke specifieke die werkruimten of visualisaties voor het profiel worden bepaald) gedownload aan uw computer. Aangezien u elk profiel downloadt, leidt het Inzicht tot een omslag binnen de installatiefolder gebruikend de profielnaam.

Bijvoorbeeld, als u een profiel genoemd Verkoop selecteert, verschijnt een omslag genoemd Verkoop in uw folder van het Inzicht. Deze omslag bevat de metriek, de afmetingen, de werkruimten, en de visualisaties die in het profiel van de Verkoop worden bepaald. Na de aanvankelijke lading van het profiel, kan het profiel worden gebruikt wanneer het werken offline. Zie [offline en online](https://docs.adobe.com/content/help/en/data-workbench/using/client/c-off-on.html)werken.

Bovendien wanneer u met de Server van het Inzicht voor het eerst van het Inzicht verbindt, leidt de Server van het Inzicht tot de volgende folders in de de installatiefolder van het Inzicht.

* **[!DNL Trace]directory:**Binnen de[!DNL Trace]folder is het het logboekdossier van het Inzicht ([!DNL insight.log]). Wanneer de grootte van het[!DNL Insight.log]dossier 100 MB bereikt, wordt het dossier anders genoemd aan[!DNL insight-1.log]. Als een dossier van de naam[!DNL insight-1.log]reeds bestaat, dan[!DNL insight-1.log]wordt anders genoemd aan[!DNL insight-2.log], etc., met een maximum van[!DNL insight-9.log]. Het dossier bevat[!DNL insight.log]altijd de meest recente logboekinformatie, en[!DNL insight-max.log]bevat oudste.

* **[!DNL User]directory:**Binnen de[!DNL User]folder zijn omslagen die aan elk profiel beantwoorden dat aan datum wordt gebruikt, en binnen elke profielomslag zijn omslagen genoemd[!DNL Work]en[!DNL Workspaces]. De folder`User\*profile name*\Workspaces`is de standaardplaats waarin de de werkruimtedossiers van het Inzicht worden opgeslagen.`User\*profile name*\Work`is de standaardplaats waarin de visualisaties van het Inzicht en ander douanewerk dat door de gebruiker van het Inzicht wordt uitgevoerd worden bewaard.

De volgende lijst maakt een lijst van de standaardplaatsen van algemeen betreden componenten.

<table id="table_0254A8C25AF5400F89F87A242746D07E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Onderdeel </th> 
   <th colname="col2" class="entry"> Directorylocatie </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Opgeslagen visualisaties </p> </td> 
   <td colname="col2"> <p><i>Insight</i>\User\<i>profielnaam</i>\Work\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Opgeslagen <span class="wintitle"> werkruimten</span> </p> </td> 
   <td colname="col2"> <p><i>Inzicht</i>\User\<i>profielnaam</i>\Workspaces\<i>tabbladNaam</i>\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Opgeslagen<span class="filepath"> .png</span> -bestanden </p> </td> 
   <td colname="col2"> <p><i>Insight</i>\User\<i>profielnaam</i>\Work\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gegevenscache </p> </td> 
   <td colname="col2"> <p><i>Insight</i>\User\Cache.db </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="filepath"> Insight.log</span> -bestand </p> </td> 
   <td colname="col2"> <p><i>Insight</i>\Trace\ </p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
c_config_file_ent.xml
-->

U kunt door zeer belangrijke naam, zeer belangrijk type, of waarde zoeken om van een ingang snel de plaats te bepalen, om de behoefte te verwijderen om door uitgebreide, grote dossiers voor genestelde informatie te scrollen. U kunt van afmetingsnamen, servernamen, etc. de plaats bepalen. Het volgende voorbeeld toont gelijken voor een onderzoek op de uitdrukkingskaart.

![](assets/cfg_search.PNG)

Typ een onderzoeksuitdrukking in dit gebied om van de gegevens de plaats te bepalen. Afhankelijk van het succes van een gelijke, verandert de kleur van het gebied. De gelijken worden getoond benadrukte en de niet-gelijken worden verduisterd. Als er geen gelijken zijn, wordt de achtergrond van het onderzoeksgebied rood. Wanneer u drukt ga binnen, breidt de config boom elke plaats uit waar er een gelijke is en doet ineenstorten waar er geen gelijke is.

U kunt regelmatige uitdrukkingen op het [!DNL Search] gebied ook gebruiken. Bijvoorbeeld, kunt u gebruiken re: [!DNL *Zitten.*]voor elke vermelding die het woord &quot;zip&quot; bevat.

Om een onderzoek te ontruimen, druk **[!UICONTROL Escape]**.

---
description: Nadat u uw software van het Inzicht en digitaal certificaat hebt geïnstalleerd, moet u Insight beginnen en zijn verbinding aan de Server van het Inzicht vormen.
title: De verbinding met Insight Server configureren
uuid: 8ba13da6-8749-49fe-a29e-dac3906f71b8
exl-id: 6a87e972-069a-435c-9bac-23b20f165ebb
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# De verbinding met Insight Server configureren{#configuring-the-connection-to-insight-server}

{{eol}}

Nadat u uw software van het Inzicht en digitaal certificaat hebt geïnstalleerd, moet u Insight beginnen en zijn verbinding aan de Server van het Inzicht vormen.

>[!NOTE]
>
>In sommige gevallen, kan de verbinding aan de Server van het Inzicht pre-gevormd door de Raadgevende Diensten van Adobe of uw systeembeheerder zijn geweest. Zo ja, dan hoeft u deze taak niet uit te voeren.

Wanneer u Insight voor het eerst start, wordt er automatisch verbinding gemaakt met de Adobe-licentieserver om uw digitale certificaat te registreren. Om het registratieproces met succes te voltooien, moet uw computer met Internet worden verbonden wanneer u de volgende stappen uitvoert.

>[!NOTE]
>
>Als u al een vooraf vergrendeld certificaat hebt aangevraagd, gedownload en geïnstalleerd, zoals beschreven in [Het digitale certificaat downloaden en installeren](../../../home/c-install-insight/install-setup/c-dgtl-crtf.md#topic-fed3b44e472c4e4ca6dd5852af14cdb9), Insight zal niet proberen verbinding te maken met de licentieserver en u ontvangt geen fout.

**Om de verbinding aan de Server van het Inzicht te vormen**

Wanneer het werken in een gegroepeerd milieu, zou het Inzicht moeten worden gevormd om tot de master Server van het Inzicht toegang te hebben om synchronisatiekwesties te vermijden. In Insight kunt u informatie over de verwerking bekijken [!DNL Insight Servers] in uw cluster met de [!DNL Related Servers] menu-item in het dialoogvenster [Serverbeheer](https://experienceleague.adobe.com/docs/data-workbench/using/client/admin-ui/c-svrs-mgr.html).

1. Start Insight.
1. Op de [!DNL Worktop], klikt u op **[!UICONTROL Admin]** vervolgens **[!UICONTROL First Steps]**.

1. Klik op de knop **[!UICONTROL Configure Connection to Servers]** miniatuur.

   De [!DNL Servers Manager]de [!DNL Insight.cfg] en instructies voor het configureren van uw [!DNL Insight.cfg]worden weergegeven.

1. In de [!DNL Insight.cfg] venster, klik met de rechtermuisknop **[!UICONTROL Servers]** en klik op **[!UICONTROL Add new child]** > **[!UICONTROL Server]**.

   ![](assets/cfg_Workstation_AddChild.png)

1. Voltooi of wijzig de serverparameters om het Inzicht van toegang tot uw master Server van het Inzicht te voorzien. Voor gedetailleerde beschrijvingen van de parameters in het Insight.cfg- dossier, zie [Configuratieparameters](https://experienceleague.adobe.com/docs/data-workbench/using/client/c-insght-config-param.html).

   ![](assets/cfg_Workstation_AddServer.png)

1. Herhaal Stap 4 en Stap 5 voor elke Server van het Inzicht waaraan u een verbinding wilt vormen.
1. Klik met de rechtermuisknop om uw configuratiewijzigingen op te slaan **[!UICONTROL Insight.cfg (modified)]** boven aan het venster en klik op **[!UICONTROL Save as Insight.cfg]**.

   Inzicht probeert verbinding te maken met de [!DNL Insight Server(s)] met de opgegeven instellingen. Als een verbinding tot stand is gebracht, wordt een groen knooppunt weergegeven in het dialoogvenster [!DNL Servers Manager] zoals weergegeven op de volgende pagina.

   ![](assets/vis_SysStat_RedGreenDots.png)

   * **Groen:** Geeft aan dat de verbinding met de Insight Server actief is.
   * **Lichtrood:** Geeft een mogelijk probleem met de server aan, zoals een leegloop bij de serververwerking, een hoog geheugengebruik of een gebrek aan schijfruimte.
   * **Rood:** Geeft aan dat de verbinding met de Insight Server niet actief is.

   Als Insight geen verbinding kan maken met de opgegeven instellingen, wordt een rood knooppunt weergegeven in het dialoogvenster [!DNL Servers Manager]. Als dit gebeurt, zie [Verbindingsproblemen oplossen](../../../home/c-install-insight/install-setup/t-conn-trbsh.md#task-034e588c5ce04c4a8f6d0097364d3b2b).

<!--
c_dir_crt_setup.xml
-->

Wanneer u een te gebruiken profiel selecteert, worden de profielgegevens (inclusief verwante gegevens en eventuele specifieke werkruimten of visualisaties die voor het profiel zijn gedefinieerd) gedownload naar de computer. Tijdens het downloaden van elk profiel maakt Insight een map in de installatiemap met de profielnaam.

Als u bijvoorbeeld een profiel met de naam Verkoop selecteert, wordt een map met de naam Verkoop weergegeven in de map Insight. Deze map bevat de metriek, afmetingen, werkruimten en visualisaties die zijn gedefinieerd in het verkoopprofiel. Nadat het profiel voor het eerst is geladen, kunt u het profiel gebruiken wanneer u offline werkt. Zie [Offline en online werken](https://experienceleague.adobe.com/docs/data-workbench/using/client/c-off-on.html).

Bovendien wanneer u voor het eerst van het Inzicht met de Server van het Inzicht verbindt, leidt de Server van het Inzicht tot de volgende folders in de de installatiemap van het Inzicht.

* **[!DNL Trace]map:** Binnen de [!DNL Trace] directory is het Logbestand Insight ( [!DNL insight.log]). Wanneer de grootte van de [!DNL Insight.log] bestand bereikt 100 MB, wordt de naam van het bestand gewijzigd in [!DNL insight-1.log]. Als een bestand met de naam [!DNL insight-1.log] bestaat al [!DNL insight-1.log] is hernoemd naar [!DNL insight-2.log], enzovoort, met een maximum van [!DNL insight-9.log]. Het bestand [!DNL insight.log] bevat altijd de meest recente logboekinformatie, en [!DNL insight-max.log] bevat de oudste.

* **[!DNL User]map:** Binnen de [!DNL User] map zijn mappen die overeenkomen met elk profiel dat tot nu toe is gebruikt. Elke profielmap bevat mappen met de naam [!DNL Work] en [!DNL Workspaces]. De map `User\*profile name*\Workspaces` is de standaardlocatie waar de bestanden in de Insight-werkruimte worden opgeslagen. `User\*profile name*\Work` is de standaardplaats waarin de visualisaties van het Inzicht en ander douanewerk die door de gebruiker van het Inzicht worden uitgevoerd worden bewaard.

In de volgende tabel worden de standaardlocaties van veelgebruikte componenten weergegeven.

<table id="table_0254A8C25AF5400F89F87A242746D07E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Component </th> 
   <th colname="col2" class="entry"> Maplocatie </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Opgeslagen visualisaties </p> </td> 
   <td colname="col2"> <p><i>Inzicht</i>\Gebruiker\<i>profielnaam</i>\Work\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Opgeslagen <span class="wintitle"> Werkruimten</span> </p> </td> 
   <td colname="col2"> <p><i>Inzicht</i>\Gebruiker\<i>profielnaam</i>\Workspaces\<i>tabnaam</i>\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Opgeslagen<span class="filepath"> .png</span> bestanden </p> </td> 
   <td colname="col2"> <p><i>Inzicht</i>\Gebruiker\<i>profielnaam</i>\Work\ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gegevenscache </p> </td> 
   <td colname="col2"> <p><i>Inzicht</i>\User\Cache.db </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="filepath"> Insight.log</span> file </p> </td> 
   <td colname="col2"> <p><i>Inzicht</i>\Trace\ </p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
c_config_file_ent.xml
-->

U kunt zoeken op sleutelnaam, sleuteltype, of waarde om snel van een ingang de plaats te bepalen, om de behoefte te verwijderen om door uitgebreide, grote dossiers voor genestelde informatie te scrollen. U kunt afmetingsnamen, servernamen, enzovoort opzoeken. In het volgende voorbeeld worden overeenkomsten voor een zoekopdracht op de woordkaart getoond.

![](assets/cfg_search.PNG)

Typ een zoekterm in dit veld om de gegevens te zoeken. Afhankelijk van het succes van een overeenkomst, verandert de kleur van het gebied. Overeenkomsten worden gemarkeerd weergegeven en niet-overeenkomende items worden grijs weergegeven. Als er geen overeenkomsten zijn, wordt de achtergrond van het zoekveld rood. Wanneer u binnengaan drukt, breidt de config boom elke plaats uit waar er een gelijke is en doet ineenstorten waar er geen gelijke is.

U kunt ook reguliere expressies gebruiken in het dialoogvenster [!DNL Search] veld. U kunt bijvoorbeeld het volgende gebruiken: [!DNL *ZIP.*] voor elke vermelding die het woord &quot;zip&quot; bevat.

Als u een zoekopdracht wilt wissen, drukt u op **[!UICONTROL Escape]**.

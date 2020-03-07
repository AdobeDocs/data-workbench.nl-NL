---
description: Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 5.0) in kaart te brengen.
solution: Analytics
title: Het Portaal van het Rapport van de afbeelding aan een Virtuele Folder (IIS 5.0)
topic: Data workbench
uuid: 9514c33e-c139-4cc2-97c2-8b241522c44d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het Portaal van het Rapport van de afbeelding aan een Virtuele Folder (IIS 5.0){#mapping-report-portal-to-a-virtual-directory-iis}

Stappen om het Portaal van het Rapport aan een virtuele folder (IIS 5.0) in kaart te brengen.

1. Op de machine waar [!DNL Report Portal] wordt geïnstalleerd, begin Manager IIS gebruikend of **[!UICONTROL Start]** > **[!UICONTROL Control Panel]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]** of **[!UICONTROL Start]** > **[!UICONTROL Administrative Tools]** > **[!UICONTROL Internet Information Services]**.

1. Selecteer **[!UICONTROL Local Machine]** > **[!UICONTROL Web Sites]** > **[!UICONTROL Default Web Site]**.

1. Klik met de rechtermuisknop **[!UICONTROL Default Web Site]** en selecteer **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**.

1. Wanneer het [!DNL Virtual Directory Wizard] opent, klik **[!UICONTROL Next]**.

1. Voltooi de volgende stappen om de wortel virtuele folder voor te bepalen [!DNL Report Portal]:

   1. Wanneer ertoe aangezet voor een alias, typ de naam van [!DNL Report Portal], dan klik **[!UICONTROL Next]**. Bijvoorbeeld, als u &quot;Portaal&quot;als naam van uw wilt gebruiken, wijs het alias &quot;Portaal&quot;aan de virtuele folder toe [!DNL Report Portal]. Klik **[!UICONTROL Next]** wanneer gebeëindigd.

   1. Wanneer u wordt gevraagd naar het fysieke pad, bladert u naar de *&lt;**[!UICONTROL PortalName]**>* directory en selecteert u deze en klikt u op **[!UICONTROL \PortalASP]** **[!UICONTROL Next]**.

      Voorbeeld: [!DNL C:\Inetpub\wwwroot\Portal\PortalASP]

   1. Wanneer ertoe aangezet voor toestemmingen, verifieer dat de volgende opties worden toegelaten:

      * **[!UICONTROL Read]**
      * **[!UICONTROL Run scripts (such as ASP)]**
   1. Klik **[!UICONTROL Next]**, dan klik **[!UICONTROL Finish]**. De virtuele folder die u creeerde verschijnt onder de StandaardWebsite zoals aangetoond in het volgende voorbeeld.
   ![](assets/RptPort_scrn_VirDirManual.png)

1. Klik met de rechtermuisknop op de virtuele map die u zojuist hebt gemaakt en selecteer **[!UICONTROL New]** > **[!UICONTROL Virtual Directory]**.

1. Gebruik de [!DNL Virtual Directory] tovenaar om een alias voor elk van de volgende fysieke folders tot stand te brengen. Het doen van dit leidt tot een aangewezen genoemde virtuele folder voor elk van deze fysieke middelen.

<table id="table_B2E04423C20F40CAA8EDA3FCBA210AA2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Creeer dit alias. . . </th> 
   <th colname="col2" class="entry"> Voor deze fysieke bron. . . </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> Kern </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\Core </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Core</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> CSS </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\CSS </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\CSS</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> HTC </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\HTC </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\HTC</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Afbeeldingen </td> 
   <td colname="col2"> <p>\<i>PortalName</i>\PortalFiles\Images </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Images</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Uitvoer </td> 
   <td colname="col2"> <p>Fysieke plaats van de folder waarin de Server <span class="keyword"> van het</span> Rapport de output voor uw rapportreeksen bewaart. De outputomslag kan overal worden gevestigd, kan om het even wat worden genoemd, en bevat een subfolder voor elke rapportreeks. </p> <p>Dit moet de zelfde folder zijn die u in de parameter van de Wortel van de Output in het <span class="filepath"> Report.cfg</span> - dossier voor een rapportreeks specificeert. Voor meer informatie, zie het <a href="../../../../home/c-rpt-oview/c-admin-rpt/c-config-rpt-files.md#concept-cf4b95344fcb4c8c877db91e5f1d345d"> Vormen Dossiers</a>Report.cfg. </p> <p>De standaardplaats is \<i>PortalName</i>\PortalFiles\Output. </p> <p>Voorbeeld: <span class="filepath"> C:\Inetpub\wwwroot\Portal\PortalFiles\Output</span> </p> <p>Het <i>PortalName</i>\PortalFiles\Output directory contains the <span class="filepath"> profile.xml</span> - dossier, dat moet worden bewogen aan de outputfolder die u voor dit alias specificeert. </p> <p>Het is kritiek dat het attribuut van de <span class="wintitle"> Weg</span> behoorlijk wordt geplaatst. </p> </td> 
  </tr> 
 </tbody> 
</table>

1. Wanneer u wordt gebeëindigd, verifieer dat IIS zes nieuwe virtuele folders toont. Zorg ervoor dat de folderstructuur één ouderomslag (met de zelfde naam zoals uw portaal) en vijf subfolders zoals hieronder getoond heeft.

   ![](assets/rptPort_scrn_VirDirs_Installed.png)

1. Wanneer gebeëindigd, ga het Dossier [van de Configuratie van de Zitting](../../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7) uitgeven om met het installatieproces verder te gaan.


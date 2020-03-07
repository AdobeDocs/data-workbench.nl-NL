---
description: Stappen om bestaande Report.cfg- dossiers uit te geven gebruikend Desktop of een tekstredacteur.
solution: Analytics
title: Bestaande Report.cfg-bestanden bewerken
topic: Data workbench
uuid: 494b9eef-42f3-4ed9-8b43-f5c09af33f2e
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Bestaande Report.cfg-bestanden bewerken{#editing-existing-report-cfg-files}

Stappen om bestaande Report.cfg- dossiers uit te geven gebruikend Desktop of een tekstredacteur.

>[!NOTE]
>
>* U moet online werken om [!DNL Report.cfg] dossiers uit te geven. Om online te werken, van [!DNL Worktop], klik de titelbar met de rechtermuisknop aan en klik **[!UICONTROL Work Online]**.
   >
   >
* Als de **[!UICONTROL Allow Report Regeneration]** parameter in het [!DNL Report.cfg] dossier aan wordt geplaatst, [!DNL True]wanneer u veranderingen in dat dossier aanbrengt en dat dossier terug naar de server opslaat, [!DNL Report] produceert automatisch de rapporten in die reeks opnieuw. Hoewel het de rapporten regenereert, verzendt het niet de rapporten via e-mail opnieuw. Voor stappen om dit te doen, zie het [Terugkomen Rapporten door E-mail](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/t-res-rpts-email.md#task-b0a21f1c925f4e5d82560581ae4cf607).
>



U kunt het bestaan uitgeven [!DNL Report.cfg] van [!DNL Worktop] of een tekstredacteur gebruiken.

Het uitgeven van een [!DNL Report.cfg] dossier dat het [!DNL Reports] lusje van [!DNL Worktop] gebruikt laat u toe om slechts die parameters, vectoren, en vectorpunten uit te geven die reeds in het dossier bestaan. Als u een parameter of een vector aan het dossier moet toevoegen, moet u het uitgeven gebruikend een tekstredacteur, zoals Blocnote.

* [Om een bestaand Report.cfg uit te geven die de Desktop gebruikt](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-7bce3bca006149c79be7678430f21945)
* [Om een bestaand Report.cfg uit te geven die een tekstredacteur gebruikt](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-06f3d2a8d7f34bc2841180caf10a1eb7)

## Om een bestaand Report.cfg uit te geven die de Desktop gebruikt {#section-7bce3bca006149c79be7678430f21945}

>[!NOTE]
>
>U moet online werken om uit te geven [!DNL Report.cfg] van [!DNL Worktop].

1. In gegevenswerkbank, op het [!DNL Reports] lusje, selecteer subfolder (lusje of drop-down subdirectory) voor de rapportreeks die u wilt vormen.
1. Klik op **[!UICONTROL Report.cfg]**. De parameters van [!DNL Report.cfg] voor dit rapport plaatsen vertoning.

1. Geef de configuratieparameters uit zoals gewenst. Voor informatie over deze parameters, zie Parameters [Report.cfg](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
1. Sparen het dossier door **[!UICONTROL Report.cfg (modified)]** bij de bovenkant van de parameters met de rechtermuisknop aan te klikken en **[!UICONTROL Save to]***&lt; **[!UICONTROL server location]**>*te klikken.

## Om een bestaand Report.cfg uit te geven die een tekstredacteur gebruikt {#section-06f3d2a8d7f34bc2841180caf10a1eb7}

1. Open het [!DNL Reports Manager] door binnen een werkruimte met de rechtermuisknop te klikken en te klikken **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Reports Manager]**.

1. Klik de omslag voor uw rapportreeks.
1. Klik het vinkje naast het [!DNL Report.cfg] voor deze rapportreeks met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.

1. In de [!DNL User] kolom, klik het vinkje naast [!DNL Report.cfg] voor deze rapportreeks met de rechtermuisknop aan en klik **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL Report.cfg] bestand wordt geopend.

   De steekproef [!DNL Report.cfg] die in [vormt de Reeks](../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0) van het Rapport wordt getoond bevat slechts de parameters inbegrepen in het [!DNL Report.cfg] dossier door gebrek. Het volgende voorbeeld omvat alle parameters beschikbaar voor het [!DNL Report.cfg] dossier dat u als modellen voor uw parameteringangen kunt gebruiken:

   ```
   Attachments = vector: 1 items
     0 = Attachment:
       FileName = string: c:\\myimage.jpg
       Content Type = string: image/jpeg
   Alert Threshold = int: 0
   Allow Report Regeneration = bool: true
   Color Set = int: 1
   Command To Execute = string: 
   Default Excel Template = string: 
   Dimension Name = string: 
   Email Only If Perfect = bool: false
   End Date = string: 
   Every = string: month
   Excel Watchdog Timeout (seconds) = double: 300.0
   Filter Formula = string: 
   Gamma Correction = double: 1
   Hide Logos = bool: false
   Lookup File = string: 
   Mail Report = MailReport: 
     Body XSL Template = string: 
     Recipients = vector: 0 items
     SMTP Server = SmtpServerInfo: 
       Address = string: 
       Password = string: 
       User = string: 
     Sender Address = string: 
     Sender Name = string: 
     Subject = string: 
   Notification Only = bool: false
   Output Root = string: 
   Report Types = vector: 3 items
     0 = string: thumbnail
     1 = string: png
     2 = string: excel
   Start Date = string: 7/1/06 19:16 EDT
   Thumbnail X = int: 240
   Thumbnail Y = int: 180
   Top N Metric = string: 
   Top N Value = int: 0
   Use Local Sample Only = bool: false
   Workspace Path = string: 
   ```

1. Geef de configuratieparameters uit zoals gewenst. Voor informatie over deze parameters, zie Parameters [Report.cfg](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
1. Sparen en sluit het dossier.
1. Klik in het [!DNL Reports Manager]venster met de rechtermuisknop op het vinkje in de [!DNL User] kolom voor het [!DNL Report.cfg] bestand en selecteer **[!UICONTROL Save to]***&lt; **[!UICONTROL profile name]**>*.


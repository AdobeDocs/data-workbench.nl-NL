---
description: Stappen om bestaande Report.cfg- dossiers uit te geven gebruikend Desktop of een tekstredacteur.
title: Bestaand Report.cfg-bestanden bewerken
uuid: 494b9eef-42f3-4ed9-8b43-f5c09af33f2e
exl-id: 69038c0c-bb01-4e61-aad6-1be0bdec8a6d
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Bestaand Report.cfg-bestanden bewerken{#editing-existing-report-cfg-files}

{{eol}}

Stappen om bestaande Report.cfg- dossiers uit te geven gebruikend Desktop of een tekstredacteur.

>[!NOTE]
>
>* U moet online werken om te kunnen bewerken [!DNL Report.cfg] bestanden. Als u online wilt werken, kiest u [!DNL Worktop], klikt u met de rechtermuisknop op de titelbalk en klikt u op **[!UICONTROL Work Online]**.
>
>* Als de **[!UICONTROL Allow Report Regeneration]** in de [!DNL Report.cfg] bestand is ingesteld op [!DNL True], wanneer u wijzigingen in dat bestand aanbrengt en dat bestand weer op de server opslaat, [!DNL Report] genereert automatisch de rapporten in die set opnieuw. Hoewel de rapporten opnieuw worden gegenereerd, worden de rapporten niet via e-mail opnieuw verzonden. Ga voor meer informatie naar [Rapporten terugsturen via e-mail](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/t-res-rpts-email.md#task-b0a21f1c925f4e5d82560581ae4cf607).
>


U kunt een bestaande [!DNL Report.cfg] van de [!DNL Worktop] of met een teksteditor.

Een [!DNL Report.cfg] bestand met de [!DNL Reports] tabblad van het dialoogvenster [!DNL Worktop] kunt u alleen die parameters, vectoren en vectoritems bewerken die al in het bestand staan. Als u een parameter of een vector aan het dossier moet toevoegen, moet u het uitgeven gebruikend een tekstredacteur, zoals Blocnote.

* [Om een bestaand Report.cfg uit te geven gebruikend de Desktop](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-7bce3bca006149c79be7678430f21945)
* [Een bestaand Report.cfg bewerken met een teksteditor](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-06f3d2a8d7f34bc2841180caf10a1eb7)

## Om een bestaand Report.cfg uit te geven gebruikend de Desktop {#section-7bce3bca006149c79be7678430f21945}

>[!NOTE]
>
>U moet online werken om de [!DNL Report.cfg] van de [!DNL Worktop].

1. Op de werkbank Gegevens, op de [!DNL Reports] selecteert u de submap (tab of vervolgkeuzelijst) voor de rapportset die u wilt configureren.
1. Klik op **[!UICONTROL Report.cfg]**. De parameters van de [!DNL Report.cfg] voor deze rapportreeks vertoning.

1. Bewerk de configuratieparameters naar wens. Voor informatie over deze parameters raadpleegt u [Report.cfg-parameters](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
1. Sla het bestand op door met de rechtermuisknop te klikken **[!UICONTROL Report.cfg (modified)]** boven aan de parameters en klik op **[!UICONTROL Save to]***&lt; **[!UICONTROL server location]**>*.

## Een bestaand Report.cfg bewerken met een teksteditor {#section-06f3d2a8d7f34bc2841180caf10a1eb7}

1. Open de [!DNL Reports Manager] door met de rechtermuisknop in een werkruimte te klikken en te klikken **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Reports Manager]**.

1. Klik de omslag voor uw rapportreeks.
1. Klik met de rechtermuisknop op het vinkje naast het pictogram [!DNL Report.cfg] voor deze rapportset en klik op **[!UICONTROL Make Local]**.

1. In de [!DNL User] kolom, klikt u met de rechtermuisknop op het vinkje naast [!DNL Report.cfg] voor deze rapportset en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. De [!DNL Report.cfg] wordt geopend.

   Het voorbeeld [!DNL Report.cfg] getoond in [De rapportset configureren](../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0) bevat alleen de parameters die zijn opgenomen in de [!DNL Report.cfg] bestand standaard. In het volgende voorbeeld worden alle parameters opgenomen die beschikbaar zijn voor de [!DNL Report.cfg] bestand dat u als model kunt gebruiken voor parameteritems:

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

1. Bewerk de configuratieparameters naar wens. Voor informatie over deze parameters raadpleegt u [Report.cfg-parameters](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
1. Sla het bestand op en sluit het.
1. In de [!DNL Reports Manager], klikt u met de rechtermuisknop op het vinkje in het dialoogvenster [!DNL User] kolom voor de [!DNL Report.cfg] bestand en selecteer **[!UICONTROL Save to]***&lt; **[!UICONTROL profile name]**>*.

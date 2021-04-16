---
description: Stappen om bestaande Report.cfg- dossiers uit te geven gebruikend Desktop of een tekstredacteur.
title: Bestaand Report.cfg-bestanden bewerken
uuid: 494b9eef-42f3-4ed9-8b43-f5c09af33f2e
exl-id: 69038c0c-bb01-4e61-aad6-1be0bdec8a6d
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Bestaand Report.cfg- Dossiers{#editing-existing-report-cfg-files} uitgeven

Stappen om bestaande Report.cfg- dossiers uit te geven gebruikend Desktop of een tekstredacteur.

>[!NOTE]
>
>* U moet online werken om [!DNL Report.cfg] dossiers uit te geven. Als u online wilt werken, klikt u in de [!DNL Worktop] met de rechtermuisknop op de titelbalk en klikt u op **[!UICONTROL Work Online]**.
   >
   >
* Als de parameter **[!UICONTROL Allow Report Regeneration]** in het [!DNL Report.cfg] dossier aan [!DNL True] wordt geplaatst, wanneer u veranderingen in dat dossier aanbrengt en dat dossier terug naar de server opslaat, [!DNL Report] automatisch regenereert de rapporten in die reeks. Hoewel de rapporten opnieuw worden gegenereerd, worden de rapporten niet via e-mail opnieuw verzonden. Voor stappen om dit te doen, zie [Resending Reports door Email](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/t-res-rpts-email.md#task-b0a21f1c925f4e5d82560581ae4cf607).

>



U kunt een bestaande [!DNL Report.cfg] van [!DNL Worktop] of het gebruiken van een tekstredacteur uitgeven.

Als u een [!DNL Report.cfg]-bestand bewerkt met het tabblad [!DNL Reports] van [!DNL Worktop], kunt u alleen die parameters, vectoren en vectoritems bewerken die al in het bestand staan. Als u een parameter of een vector aan het dossier moet toevoegen, moet u het uitgeven gebruikend een tekstredacteur, zoals Blocnote.

* [Om een bestaand Report.cfg uit te geven gebruikend de Desktop](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-7bce3bca006149c79be7678430f21945)
* [Een bestaand Report.cfg bewerken met een teksteditor](../../../../home/c-rpt-oview/c-work-rpt-sets/c-edit-ex-rpt-files/c-edit-ex-rpt-files.md#section-06f3d2a8d7f34bc2841180caf10a1eb7)

## Om een bestaand Report.cfg uit te geven gebruikend de Desktop {#section-7bce3bca006149c79be7678430f21945}

>[!NOTE]
>
>U moet online werken om [!DNL Report.cfg] van [!DNL Worktop] uit te geven.

1. In gegevenswerkbank, op [!DNL Reports] lusje, selecteer subfolder (lusje of drop-down subdirectory) voor de rapportreeks die u wilt vormen.
1. Klik op **[!UICONTROL Report.cfg]**. De parameters van [!DNL Report.cfg] voor dit rapport plaatsen vertoning.

1. Bewerk de configuratieparameters naar wens. Voor informatie over deze parameters, zie [Parameters Report.cfg](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
1. Sla het bestand op door met de rechtermuisknop op **[!UICONTROL Report.cfg (modified)]** boven aan de parameters te klikken en op **[!UICONTROL Save to]***&lt; **[!UICONTROL server location]***te klikken.

## Om een bestaand Report.cfg uit te geven gebruikend een tekstredacteur {#section-06f3d2a8d7f34bc2841180caf10a1eb7}

1. Open [!DNL Reports Manager] door met de rechtermuisknop in een werkruimte te klikken en **[!UICONTROL Admin]** > **[!UICONTROL Profile]** > **[!UICONTROL Reports Manager]** te klikken.

1. Klik de omslag voor uw rapportreeks.
1. Klik het vinkje naast [!DNL Report.cfg] voor deze rapportreeks met de rechtermuisknop aan en klik **[!UICONTROL Make Local]**.

1. Klik in de kolom [!DNL User] met de rechtermuisknop op het vinkje naast [!DNL Report.cfg] voor deze rapportset en klik op **[!UICONTROL Open]** > **[!UICONTROL in Notepad]**. Het [!DNL Report.cfg] dossier opent.

   Het voorbeeld [!DNL Report.cfg] in [Configureer de rapportset](../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/t-config-rpt-set.md#task-cfb2fd0c28bc48c2acdd582fe0d670d0) bevat standaard alleen de parameters die in het [!DNL Report.cfg]-bestand zijn opgenomen. Het volgende voorbeeld omvat alle parameters beschikbaar voor het [!DNL Report.cfg] dossier dat u als modellen voor uw parameteringangen kunt gebruiken:

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

1. Bewerk de configuratieparameters naar wens. Voor informatie over deze parameters, zie [Parameters Report.cfg](../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).
1. Sla het bestand op en sluit het.
1. Klik in [!DNL Reports Manager] met de rechtermuisknop op het vinkje in de kolom [!DNL User] voor het bestand [!DNL Report.cfg] en selecteer **[!UICONTROL Save to]***&lt; **[!UICONTROL profile name]**>*.

---
description: De Werkbank van gegevens verstrekt een opstellingstovenaar om de werkstation (cliënt) toepassing te installeren.
title: Wizard Werkstation instellen
uuid: e2bf6606-e7ba-439f-b50c-118706ab5b7d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Wizard Werkstation instellen{#workstation-setup-wizard}

De Werkbank van gegevens verstrekt een opstellingstovenaar om de werkstation (cliënt) toepassing te installeren.

## Het installeren van het Werkstation dat de Tovenaar van de Opstelling gebruikt {#section-58da9bb6196c46eab3b54146913fdcb8}

Lanceer uitvoerbaar de installatietovenaar en loop door elke stap om het programma van de werkstationcliënt te installeren. Na installatie van het werkstation kunt u verbinding maken met servers en profielen.

1. Dubbelklik op het uitvoerbare uitvoerbare werkstationinstallatieprogramma.
1. Klik **ja** om het programma toe te staan om op Vensters te installeren.
1. Selecteer een **Taal** voor de opstellingstovenaar.

   De tovenaar zal openen:

   ![](assets/6_4_workstation_wizard.png)

1. Klik **daarna** op het **Onthaal aan de dialoog van de Tovenaar** van de Opstelling van de Werkbank van Gegevens.

1. Selecteer deze optie om een **nieuwe installatie** te installeren of een bestaande installatie te **upgraden of te repareren** .

   **De nieuwe Installatie** beschrijft om het even welke eerder geïnstalleerde dossiers.

   **De verbetering** werkt uw Werkstation aan de recentste versie bij of laat u een bestaande installatie herstellen. De Werkbank van gegevens zal geïnstalleerde **dossiers vergelijken Insight.exe** en zal de Tovenaar van de Opstelling van het Werkstation in werking stellen als een nieuwere versie van de cliënt beschikbaar is.

1. Selecteer installatielocatie:

   **Typisch** installeert aan een standaardomslag en een plaats.

   * De dossiers van het programma worden opgeslagen door gebrek aan:

      ```
      C:\Program Files\Adobe\Adobe Analytics\Data Workbench
      ```

   * De Dossiers van gegevens (profielen, certificaten, spoorlogboeken, en gebruikersdossiers) worden opgeslagen door gebrek aan:

      ```
      C:\Users\<username>\AppData\Local\Adobe\Adobe Analytics\Data Workbench\
      ```

      >[!IMPORTANT]
      >
      >Een generisch ***Insight.cfg*** - dossier zonder serverdetails zal aanvankelijk worden geïnstalleerd. Men adviseert dat u het onlangs geïnstalleerde dossier ***Insight.cfg*** gebruikt en het aanpast eerder dan het bewegen van een dossier van een vorige installatie. Omdat de weg voor het installeren van het werkstation is veranderd, wordt de toevoeging van doopvonten, de verwijdering van de Omslag *van de* Gebruiker, en de verwijdering van *TraceFileComponent * geadviseerd.

1. (facultatief) Selecteer** Aangepast** om het taalpakket en de locatie van het programma en de gegevensbestanden te kiezen.
1. Selecteer plaats voor **kortere weg in het Menu** van het Begin.

   ![](assets/6_4_workstation_wizard_folder.png)

   Klik **creëren geen omslag** van het Menu van het Begin om geen kortere weg op het Menu van het Begin van Vensters te installeren.

1. Klik op **Volgende.** Een samenvatting van geselecteerde wegen en talen van de dossierplaats zal tonen. Klik op **Installeren.**

1. Zoek het **Data Workbench Certificate**.

   Als de opstellingstovenaar niet het certificaat van de Werkbank van Gegevens tijdens installatie kan vinden, zal het een dialoog openen om aan de plaats van het certificaat te doorbladeren (een **.pem** dossier dat door gebrek in de omslag van de **Certificaten** van de cliënt wordt gevestigd), of **Skip** te klikken om het certificaat na installatie te vinden.

   Klik **installeren** na de plaats van het certificaat.

1. Nadat de opstellingstovenaar volledig is en de Werkbank van Gegevens geïnstalleerd, klik **Afwerking** om opstelling te voltooien.

   >[!NOTE]
   >
   >De standaardlogboekplaats voor de Tovenaar van de Opstelling van het Werkstation in **[!DNL C:\Users\&quot;<userName>\AppData\Local\Temp.]**

   Selecteer checkbox van de toepassing **van de** Lancering om de werkbank na opstelling te openen.

1. **Vorm verbindingen** aan servers in **[!DNL Insight.cfg]** dossier.

   Na installatie van het werkstation, zal de Verbeterde werkruimte van de Ervaring van de Configuratie van het Werkstation met extra informatie over het [ingaan van de informatie](/help/home/c-get-started/c-insght-config-param.md) van de serververbinding in het *Insight.cfg* - dossier en een optie openen om een profiel van drop-down te selecteren. U kunt de verbindingsstatus aan uw servers ook bekijken.

   ![](assets/6_4_workstation_install_conf_conn.png)

## Installatiemappen {#section-b5ea5a3b3ecb4622aef713972f3f8ebd}

De de omslagstructuur van de Werkbank van Gegevens heeft twee installatielocaties:

* **De Dossiers** van het programma **Insight.exe** en het steunen van cliëntdossiers (**Insight.ini**) worden nu gevestigd door gebrek bij

   ```
   C:\Program Files\Adobe\Analytics\DataWorkbench
   ```

* De map **Appdata** .

   **Insight.cfg**, de profielen, de certificaten, de spoorlogboeken, en de gebruikersdossiers worden nu gevestigd door gebrek bij

   ```
   C:\Users\<Winuser>\AppData\Adobe\Analytics\DataWorkbench\ 
   ```

   U kunt de weg voor de omslag **Appdata** in het `Insight.ini` dossier plaatsen:

   ```
   [InitialSettings] 
   AppDataFolder=C:\Users\mhiatt\AppData\Local\Adobe\Adobe Analytics\Data Workbench\ 
   Locale=en-us
   ```

## Het werkstation verwijderen {#section-5ce2e233fe4348469ef1b3c451dd5b70}

De Werkbank van gegevens omvat nu uitvoerbaar om het werkstation (dat door gebrek bij **`Program Files\Adobe\Adobe Analytics\Data Workbench\ unins000.exe`**) wordt gevestigd te desinstalleren.

Start en volg stappen om de gegevenswerkstationbestanden van uw harde schijf te verwijderen.

>[!NOTE]
>
>U kunt uitvoerbaar **unins000.exe** van de omslag lanceren, gebruikend de kortere weg van de Werkbank **van de Gegevens van de** Desinstallatie van het Menu van het Begin, of van **[!UICONTROL Control Panel]** > **[!UICONTROL Program and Features]**.

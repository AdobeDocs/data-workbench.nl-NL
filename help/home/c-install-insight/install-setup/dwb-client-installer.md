---
description: Data Workbench biedt een installatiewizard om de workstationtoepassing (client) te installeren.
title: Wizard Werkstation instellen
uuid: e2bf6606-e7ba-439f-b50c-118706ab5b7d
exl-id: bfd9f2ad-282a-4be8-9f66-53e045648ef1
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 0%

---

# Wizard Werkstation instellen{#workstation-setup-wizard}

{{eol}}

Data Workbench biedt een installatiewizard om de workstationtoepassing (client) te installeren.

## Het werkstation installeren met de wizard Setup {#section-58da9bb6196c46eab3b54146913fdcb8}

Start het uitvoerbare bestand van de installatiewizard en doorloop elke stap om het clientprogramma van het werkstation te installeren. Nadat u het werkstation hebt geïnstalleerd, kunt u verbinding maken met servers en profielen.

1. Dubbelklik op het uitvoerbare bestand van het installatieprogramma van het werkstation.
1. Klikken **Ja** om het programma in Windows te laten installeren.
1. Selecteer een **Taal** voor de installatiewizard.

   De wizard wordt geopend:

   ![](assets/6_4_workstation_wizard.png)

1. Klikken **Volgende** op de **Welkom bij de wizard Data Workbench instellen** .

1. Selecteer om een **Nieuwe installatie** of aan **Upgrade of herstel** een bestaande installatie.

   **Nieuwe installatie** Hiermee overschrijft u eerder geïnstalleerde bestanden.

   **Upgrade** werkt uw Werkstation aan de recentste versie bij of laat u een bestaande installatie herstellen. Data Workbench vergelijkt geïnstalleerde **Insight.exe** en voer de Tovenaar van de Opstelling van het Werkstation in als een nieuwere versie van de cliënt beschikbaar is.

1. Selecteer installatielocatie:

   **Normaal** wordt geïnstalleerd in een standaardmap en -locatie.

   * Programmabestanden worden standaard opgeslagen in:

      ```
      C:\Program Files\Adobe\Adobe Analytics\Data Workbench
      ```

   * Gegevensbestanden (profielen, certificaten, traceringslogbestanden en gebruikersbestanden) worden standaard opgeslagen in:

      ```
      C:\Users\<username>\AppData\Local\Adobe\Adobe Analytics\Data Workbench\
      ```

      >[!IMPORTANT]
      >
      >Een generiek ***Insight.cfg*** bestand zonder servergegevens wordt in eerste instantie geïnstalleerd. U wordt aangeraden de zojuist geïnstalleerde ***Insight.cfg*** en aanpassen in plaats van een bestand te verplaatsen van een vorige installatie. Omdat het pad voor de installatie van het werkstation is gewijzigd, moet u de toevoeging van lettertypen en de verwijdering van het *Gebruikersmap* en het verwijderen van de *TraceFileComponent * wordt aanbevolen.

1. (optioneel) Selecteer **Aangepast** om het taalpakket en de locatie van het programma en gegevensbestanden te kiezen.
1. Selecteer locatie voor **sneltoetsen in het menu Start**.

   ![](assets/6_4_workstation_wizard_folder.png)

   Klikken **Geen map voor menu Start maken** om geen kortere weg op het Menu van het Begin van Vensters te installeren.

1. Klikken **Volgende.** Er wordt een overzicht weergegeven van de paden en talen van de geselecteerde bestandslocatie. Klikken **Installeren.**

1. Zoek de **Certificaat van Data Workbench**.

   Als de installatiewizard het Data Workbench-certificaat niet kan vinden tijdens de installatie, wordt een dialoogvenster geopend waarin u naar de locatie van het certificaat kunt bladeren (een **.pem** bestand bevindt zich standaard in de client **Certificaten** map) of klik op **Overslaan** om het certificaat na installatie te vinden.

   Klikken **Installeren** nadat u het certificaat hebt gevonden.

1. Nadat de installatiewizard is voltooid en de Data Workbench is geïnstalleerd, klikt u op **Voltooien** om de installatie te voltooien.

   >[!NOTE]
   >
   >De standaardlogboekplaats voor de Tovenaar van de Opstelling van het Werkstation bij  `C:\Users\<userName>\AppData\Local\Temp`.

   Selecteer **Toepassing starten** Schakel het selectievakje in om de werkbank na installatie te openen.

1. **Verbindingen configureren** naar servers in **[!DNL Insight.cfg]** bestand.

   Na installatie van het werkstation wordt de werkruimte Verbeterde werkstationconfiguratie geopend met aanvullende informatie over [invoeren, serververbindingsgegevens](/help/home/c-get-started/c-insght-config-param.md) in de *Insight.cfg* en een optie om een profiel te selecteren in de vervolgkeuzelijst. U kunt de verbindingsstatus ook weergeven op uw servers.

   ![](assets/6_4_workstation_install_conf_conn.png)

## Installatiemappen {#section-b5ea5a3b3ecb4622aef713972f3f8ebd}

De de omslagstructuur van de Data Workbench heeft twee installatielocaties:

* **Programmabestanden** De **Insight.exe** en ondersteunende clientbestanden (**Insight.ini**) bevindt zich nu standaard op

   ```
   C:\Program Files\Adobe\Analytics\DataWorkbench
   ```

* De **Appdata** map.

   **Insight.cfg**, profielen, certificaten, traceringslogbestanden en gebruikersbestanden bevinden zich nu standaard op

   ```
   C:\Users\<Winuser>\AppData\Adobe\Analytics\DataWorkbench\ 
   ```

   U kunt het pad instellen voor de **Appdata** in de `Insight.ini` bestand:

   ```
   [InitialSettings] 
   AppDataFolder=C:\Users\mhiatt\AppData\Local\Adobe\Adobe Analytics\Data Workbench\ 
   Locale=en-us
   ```

## Het werkstation verwijderen {#section-5ce2e233fe4348469ef1b3c451dd5b70}

Data Workbench bevat nu een uitvoerbaar bestand om het werkstation te verwijderen (standaard op **`Program Files\Adobe\Adobe Analytics\Data Workbench\ unins000.exe`**).

Start en voer de stappen uit om de Data Workbench Workstation-bestanden van de vaste schijf te verwijderen.

>[!NOTE]
>
>U kunt de opdracht **unins000.exe** uitvoerbaar vanuit de map, met de **Data Workbench verwijderen** sneltoets in menu Start of vanuit **[!UICONTROL Control Panel]** > **[!UICONTROL Program and Features]**.

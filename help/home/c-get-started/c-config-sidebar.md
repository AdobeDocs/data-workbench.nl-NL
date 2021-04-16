---
description: De zijbalk biedt toegang tot regelmatig gebruikte functies en behoudt de visualisatie wanneer u tussen werkruimten beweegt.
title: De zijbalk configureren
uuid: 0d2f0b9a-56a9-4f27-aaa6-1f9bf7fcab2d
exl-id: 75ccc869-8ced-4beb-b3d7-ed7febe347f9
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# De zijbalk configureren{#configure-the-sidebar}

De zijbalk biedt toegang tot regelmatig gebruikte functies en behoudt de visualisatie wanneer u tussen werkruimten beweegt.

Beheerders kunnen een zijbalk aanpassen om deze geschikt te maken voor verschillende gebruikersgroepen en vervolgens de zijbalk met een profiel implementeren.

De zijbalk is ideaal als u filters en lokale overschrijvingen wilt bijhouden. Als u liever de zijbalk niet gebruikt, kunt u deze verbergen.

## Visualisaties toevoegen aan het zijpaneel {#section-666f70a405db4f8d8eaffa567ffcac06}

1. Start Data Workbench.
1. Klik in de zijbalk op **[!UICONTROL Add]** > *&lt;**[!UICONTROL item]**>*. Bijvoorbeeld [!DNL Selections Panel], [!DNL Filters Panel], of [!DNL Table].

   De volgende zijbalkdeelvensters zijn beschikbaar in de standaardinstallatie van Data Workbench. Mogelijk zijn meer items beschikbaar in uw specifieke profiel:

   * **Deelvenster Selecties:** Hiermee kunt u begrijpen welke selecties actief zijn in de huidige werkruimte. De [!DNL Selections Panel] wordt bijgewerkt wanneer u een nieuwe selectie maakt. U kunt selecties wissen door op **[!UICONTROL x]** te klikken. Zie [Selecties maken in visualisaties](../../home/c-get-started/c-vis/c-sel-vis/c-sel-vis.md#concept-012870ec22c7476e9afbf3b8b2515746) voor informatie over het selecteren van gegevens.
   * **Deelvenster Filters:** Hiermee kunt u opgeslagen filters eenvoudig laden en toepassen. U kunt meerdere filters laden en elk filter afzonderlijk in- of uitschakelen door op het selectievakje naast het filter te klikken. Zie [Editors filteren](../../home/c-get-started/c-analysis-vis/c-filter-editors/c-filter-editors.md#concept-2f343ecbed8240f18b0c1f1eccef11e3).
   * **Deelvenster Lokaal overschrijven:in** dit deelvenster wordt weergegeven welke maateenheden, afmetingen en filters in het profiel zijn gewijzigd in uw persoonlijke kopie van het profiel. Hierdoor wordt u gewaarschuwd voor mogelijke verschillen tussen de manier waarop gegevens op uw client worden weergegeven en die van andere gebruikers. Wanneer u wijzigingen in metrische vorm, in afmetingen of in een filter opslaat op de server, wordt de overschrijving verwijderd uit [!DNL Local Overrides panel]. Als u op een overschrijving klikt en vervolgens **[!UICONTROL Revert to Server]** klikt, wordt de lokale overschrijving verwijderd en wordt het item teruggezet naar de gedeelde versie.
   * **Metrische legenda:** voegt een metrische legenda toe. [!DNL Metric legends] kunt u basislijnmetriek zien met betrekking tot uw profiel en statistieken met betrekking tot de dataset (of tot de huidige selectie, als gemaakt). Zie [Metrische legenda](../../home/c-get-started/c-analysis-vis/c-legends/c-metric-leg.md#concept-e7195bc8f7844ae295bda3a88b028d5b).
   * **Kleurlegenda:** voegt een legenda toe. U kunt kleurcode-visualisaties op metriek, zoals Omzetting en Behoud, en gebruiken hen in bijna elke [!DNL Workspace]. Door bedrijfsmetriek aan kleuren te koppelen, kunt u gemakkelijk anomalieën, uitzonderingen en trends opsporen. Zie [Kleurlegenda](../../home/c-get-started/c-analysis-vis/c-legends/c-color-leg.md#concept-f84d51dc0d6547f981d0642fc2d01358).
   * **Tekstannotatie:** voegt een notitievenster toe. [!DNL Text annotations] Dit zijn vensters waarin u willekeurige tekst kunt invoeren om beschrijvende informatie of opmerkingen aan een  [!DNL Workspace]document toe te voegen. Zie [Werken met tekstannotaties](../../home/c-get-started/c-analysis-vis/c-annots/c-text-annots.md#concept-55b4aa3e0c58470b8e3c9d452e12a777).
   * **Tabel:** voegt een tabel toe. Een tabel kan een of meer metriek in een of meer dimensies van gegevens weergeven. Zie [Tabellen](../../home/c-get-started/c-analysis-vis/c-tables/c-tables.md#concept-c632cb8ad9724f90ac5c294d52ae667f).
   * **Openen:** Opent een opgeslagen bestand.

## Deelvenster Zijbalk openen {#section-cbc8e57491854274a577d47a48c306b8}

U kunt een bestand voor sidebar-visualisatie openen vanaf een opgeslagen locatie of vanaf het klembord.

1. Klik in de zijbalk op **[!UICONTROL Add]** > **[!UICONTROL Open]**.
1. Klik op **[!UICONTROL File]** om het [!DNL .vw]-bestand te zoeken van het deelvenster dat u wilt toevoegen of klik op **[!UICONTROL Last Closed Window]**, dat de visualisatie vanaf het klembord ophaalt.

   Daarnaast kunt u op **[!UICONTROL From Clipboard]** klikken om een visualisatie te plakken die naar het klembord is gekopieerd. Zie [Een zijpaneel kopiëren](../../home/c-get-started/c-config-sidebar.md#section-720ae057632a4b8dbb94412e06a370b1).

## Een deelvenster Zijbalk {#section-720ae057632a4b8dbb94412e06a370b1} kopiëren

1. Klik met de rechtermuisknop op de bovenste rand van het deelvenster en klik vervolgens op **[!UICONTROL Copy]** > **[!UICONTROL Window]**.
1. Als u het deelvenster wilt plakken, klikt u op **[!UICONTROL Add]** > **[!UICONTROL Open]** > **[!UICONTROL From Clipboard]**.

## Een zijpaneel opslaan {#section-fb19936b12704fb0a4c592abb579db1d}

Klik in een zijpaneel met de rechtermuisknop op de titelbalk en klik op **[!UICONTROL Save]**.

Op dezelfde manier kunt u een opgeslagen zijbalkvisualisatie openen. Data Workbench slaat de visualisatie op als een [!DNL .vw]-bestand op de locatie die u opgeeft.

## Terugkeren naar de standaardzijbalk {#section-4d14b8771ad747bba799876267f24831}

Klik in de zijbalk op **[!UICONTROL Options]** > **[!UICONTROL Revert]**.

Wanneer u Data Workbench sluit, slaat het systeem de huidige zijbalkconfiguratie in het [!DNL sidebar.vw] dossier in het gebruikersprofiel op. Wanneer u Data Workbench opent, laadt het systeem het [!DNL sidebar.vw] dossier van het gebruikersprofiel, eerder dan een ouderprofiel.

U kunt terugkeren naar een standaardzijbalk of eerder opgeslagen zijbalk, waardoor de zijbalk uit het gebruikersprofiel wordt verwijderd en de zijbalk opnieuw wordt geladen uit het bovenliggende profiel. Beheerders kunnen de standaardzijbalk (bovenliggend item) vervangen door een lokale zijbalk door deze te uploaden vanaf [!DNL Profile Manager].

## Het bestand Meer status-deelvensters aanpassen {#section-8d502f3b59cc4331966edec05e896ce1}

Systeembeheerders kunnen formules maken in de [!DNL More Status Panel.vw]. Hierdoor worden contextafhankelijke woorden geplaatst rondom metrische waarden en waarden van dimensies, en worden de resultaten weergegeven in de [!DNL More Status panel] op de zijbalk.

Als u de [!DNL More Status panel] in het zijpaneel wilt weergeven, klikt u op de pijlen in het volgende voorbeeld.

![](assets/more_status_panel_arrows.png)

De volgende procedure toont een eenvoudig voorbeeld van hoe te om tot een aangepaste status te leiden die u vertelt hoeveel dagen in een dataset zijn:

1. Klik in [!DNL Profile Manager] op **[!UICONTROL Sidebar\]**.

1. Maak in de kolom [!DNL Base_5_3*] een lokale kopie van het bestand [!DNL More Status Panel.vw].

   Klik hiertoe met de rechtermuisknop op het vinkje en klik op **[!UICONTROL Make Local]**.

1. Open het [!DNL More Status Panel.vw] dossier in [!DNL .vw] [!DNL Editor] of in Blocnote.

   ![](assets/more_status_panel_file.png)

1. Vul de velden [!DNL Context] en [!DNL Items] in [!DNL Editor] in. Zie [Syntaxis van de Taal van de vraag](../../home/c-get-started/c-qry-lang-syntx/c-qry-lang-syntx.md#concept-15d1d3f5164a47d49468c5acb7299d9f) voor richtlijnen over syntaxis.

1. Sla het bestand op.

   De waarden in het voorgaande voorbeeld resulteren in een statusformule die als volgt wordt weergegeven:

   ![](assets/more_status_panel.png)

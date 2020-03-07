---
description: Het dossier van de opstelling insight.zbin om de taal van de cliënttoepassing te plaatsen.
title: Lokaal taalgebruik instellen
uuid: 97baf281-32fd-4df0-81a6-c2c7126b053c
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Lokaal taalgebruik instellen{#setting-up-localized-languages}

Het dossier van de opstelling insight.zbin om de taal van de cliënttoepassing te plaatsen.

## Werk de servercomponenten van de gegevenswerkbank bij {#section-5d07a081befc4eaa8fdf7fea904e0d48}

De beheerder moet deze taken eerst voltooien om deze servercomponenten bij te werken:

1. **Update aan de server van de gegevenswerkbank 6.x.** U moet de server van de gegevenswerkbank voor localisatie bijwerken door het [!DNL base\localization\*.zbin] dossier bij te werken. Dit [!DNL insight.zbin] bestand wordt vervolgens naar de client gekopieerd.

   Een [!DNL insight.zbin] dossier is inbegrepen in de installatieomslag naast het [!DNL insight.exe] dossier. Als u met een server verbindt die u niet van taal-specifieke [!DNL .zbin] dossiers voorziet, dan zal de gegevenswerkbank te werk gaan om dit dossier te gebruiken.

   Het back- [!DNL insight.zbin] upbestand kan in elke taal worden geleverd. Dientengevolge, als u gegevenswerkbank in Chinees gebruikt en met een server verbindt die deze taal niet steunt, dan zal uw cliënt van de gegevenswerkbank nog in het Chinees zijn, zelfs als de server uw basisprofiel verandert en uw [!DNL .zbin] dossiers uit de [!DNL Base/Localization] omslag verwijdert.

1. **Werk de server van het gegevenswerkbankrapport bij.** De [!DNL insight.zbin] bij de wortelomslag van het rapportserver van de gegevenswerkbank zal in het Engels door gebrek zijn. Als beheerder, zult u worden vereist om het [!DNL .zbin] - dossier van het bijgewerkte pakket van de rapportserver te selecteren en te kopiëren en het te plaatsen in de wortelfolder van de het rapportserver van de gegevenswerkbank. Als de cliënt, vereist de rapportserver ook de juiste argumenten voor de geselecteerde taal, zoals [!DNL Insight.exe -zh-cn]

   1. Stop de diensten van de rapportserver.
   1. Kopieer de [!DNL Localization] omslag van het nieuwe pakket van de rapportserver.
   1. Van de [!DNL Localization] omslag, kopieer het [!DNL Insight.zbin] dossier en plaats het in de wortelfolder van de rapportserver waar [!DNL Insight.exe] wordt gevestigd.

   1. Voeg om het even welke vereiste argumenten, zoals toe [!DNL insight.exe -zh-cn]
   1. Start de rapportserver opnieuw.

## Update de cliënt van de gegevenswerkbank {#section-9653d3fcaf2a4337a97b685857e7aeac}

Na het bijwerken van de server, volg deze stappen om elke cliënt bij te werken.

1. Om ervoor te zorgen wordt de cliënt niet bijgewerkt van de server tijdens deze update, plaats uw [!DNL Insight.cfg] argument aan Vals.

   ```
   Update Software = bool: false
   ```

1. Start de client opnieuw.
1. Navigeer naar het profiel Software en Docs (SoftDocs-profiel) en download het vereiste **[!UICONTROL insight.zbin]** bestand van het clientpakket: [!DNL Software\Insight Client\Insight_6.1.zip]

1. Verplaats het [!DNL insight.zbin] dossier naar de omslag waar [!DNL insight.exe] wordt gevestigd.

1. Om ervoor te zorgen dat de cliëntdossiers nu van de server worden bijgewerkt, verander het [!DNL Insight.cfg] dossierargument in Waar worden bijgewerkt:

   ```
   Update Software = bool: true
   ```

   I

   >[!NOTE]
   >
   >Uw cliënt zal met de server synchroniseren en u zult een bericht zien verklarend dat het bijwerkt. Aan het eind van de download, zult u een bericht krijgen vragend of wilt u uw cliënt opnieuw beginnen.

1. Klik op **OK** om de client opnieuw te starten.

Als u het volgende bericht krijgt, dan betekent het dat het [!DNL zbin] dossier niet in de zelfde plaats werd geplaatst zoals het [!DNL Insight.exe].

```
Insight Terminated: The backup dictionary file insight.zbin 
is missing.
```

**Gelokaliseerde plasmaschermen**

De werkbank van gegevens zoekt de volgende dossiers van het welkomstscherm:

* Engels (standaard): [!DNL Base/Images/<version_product> Splash.png]
* Chinees (bij aanvang met -zh-cn): [!DNL Base/Images/<version_product> Splash zh-cn.png].

Als een welkomstscherm wordt gevraagd maar ontbreekt, zal de gegevenswerkbank tot het Engelse welkomstscherm door gebrek toegang hebben.

<!-- <a id="section_91AE5EF234C14652A7B04082A22629AB"></a> -->


---
description: Stel het bestand info.zbin in om de taal van de clienttoepassing in te stellen.
title: Gelokaliseerde talen instellen
uuid: 7735e183-7ba3-4e11-bfe2-7f87e4c55fc8
exl-id: bb57887f-f213-48a4-9a10-8da7ea33eda5
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Gelokaliseerde talen instellen{#setting-up-localized-languages}

Stel het bestand info.zbin in om de taal van de clienttoepassing in te stellen.

## De onderdelen {#section-5d07a081befc4eaa8fdf7fea904e0d48} van de gegevenswerkbench-server bijwerken

De beheerder moet deze taken eerst voltooien om deze servercomponenten bij te werken:

1. **Bijwerken naar gegevenswerkbankserver 6.x.** U moet de gegevenswerkbankserver bijwerken voor lokalisatie door het  [!DNL base\localization\*.zbin] bestand bij te werken. Dit [!DNL insight.zbin]-bestand wordt vervolgens naar de client gekopieerd.

   Er wordt een [!DNL insight.zbin]-bestand in de installatiemap opgenomen naast het [!DNL insight.exe]-bestand. Als u verbinding maakt met een server die u geen taalspecifieke [!DNL .zbin]-bestanden biedt, wordt dit bestand verder gebruikt in de werkbank.

   Het back-upbestand [!DNL insight.zbin] kan in elke taal worden geleverd. Als u gegevensworkbench gebruikt in het Chinees en verbinding maakt met een server die deze taal niet ondersteunt, is de gegevensworkbench-client dus nog steeds Chinees, zelfs als de server uw basisprofiel wijzigt en uw [!DNL .zbin]-bestanden verwijdert uit de map [!DNL Base/Localization].

1. **Werk de server van het gegevenswerkbankrapport bij.** De  [!DNL insight.zbin] hoofdmap van de rapportserver van de gegevenswerkbank wordt standaard in het Engels weergegeven. Als beheerder, zult u het [!DNL .zbin] dossier van het bijgewerkte pakket van de rapportserver moeten selecteren en kopiëren en het in de wortelfolder van de server van het gegevenswerkbankrapport plaatsen. Net als de client vereist de rapportserver ook de juiste argumenten voor de geselecteerde taal, zoals [!DNL Insight.exe -zh-cn]

   1. Stop de diensten van de rapportserver.
   1. Kopieer de map [!DNL Localization] uit het nieuwe serverpakket voor rapporten.
   1. Kopieer het [!DNL Localization]-bestand vanuit de map [!DNL Insight.zbin] en plaats het in de hoofdmap van de rapportserver op de locatie van [!DNL Insight.exe].

   1. Voeg eventueel vereiste argumenten toe, zoals [!DNL insight.exe -zh-cn]
   1. Start de rapportserver opnieuw.

## De gegevensworkbench-client {#section-9653d3fcaf2a4337a97b685857e7aeac} bijwerken

Nadat u de server hebt bijgewerkt, voert u de volgende stappen uit om elke client bij te werken.

1. Om ervoor te zorgen dat de client tijdens deze update niet van de server wordt bijgewerkt, stelt u het argument [!DNL Insight.cfg] in op Onwaar.

   ```
   Update Software = bool: false
   ```

1. Start de client opnieuw.
1. Navigeer naar het profiel Software en Docs (SoftDocs-profiel) en download het vereiste **[!UICONTROL insight.zbin]**-bestand uit het clientpakket: [!DNL Software\Insight Client\Insight_6.1.zip]

1. Verplaats het [!DNL insight.zbin]-bestand naar de map waarin [!DNL insight.exe] zich bevindt.

1. Om ervoor te zorgen dat de cliëntdossiers nu van de server worden bijgewerkt, verander het [!DNL Insight.cfg] dossierargument in Waar:

   ```
   Update Software = bool: true
   ```

   I

   >[!NOTE]
   >
   >De client wordt gesynchroniseerd met de server. Er wordt een bericht weergegeven dat de client wordt bijgewerkt. Aan het einde van het downloaden ontvangt u een bericht met de vraag of u de client opnieuw wilt starten.

1. Klik **OK** om de client opnieuw te starten.

Als u het volgende bericht krijgt, dan betekent het dat het [!DNL zbin] dossier niet in de zelfde plaats werd geplaatst zoals [!DNL Insight.exe].

```
Insight Terminated: The backup dictionary file insight.zbin 
is missing.
```

**Gelokaliseerde welkomstschermen**

De werkbank van gegevens zoekt de volgende dossiers van het splash scherm:

* Engels (standaard): [!DNL Base/Images/<version_product> Splash.png]
* Chinees (wanneer begonnen met -zh-cn): [!DNL Base/Images/<version_product> Splash zh-cn.png].

Als een welkomstscherm wordt aangevraagd maar ontbreekt, heeft de werkbank voor gegevens standaard toegang tot het Engelstalige welkomstscherm.

<!-- <a id="section_91AE5EF234C14652A7B04082A22629AB"></a> -->

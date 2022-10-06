---
description: Stel het bestand info.zbin in om de taal van de clienttoepassing in te stellen.
title: Gelokaliseerde talen instellen
uuid: 97baf281-32fd-4df0-81a6-c2c7126b053c
exl-id: 29624b3a-e26a-48a9-9dcc-21ba829c34d4
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Gelokaliseerde talen instellen{#setting-up-localized-languages}

{{eol}}

Stel het bestand info.zbin in om de taal van de clienttoepassing in te stellen.

## De servercomponenten van de gegevenswerkbank bijwerken {#section-5d07a081befc4eaa8fdf7fea904e0d48}

De beheerder moet deze taken eerst voltooien om deze servercomponenten bij te werken:

1. **Bijwerken naar gegevenswerkbankserver 6.x.** U moet de gegevensworkbench-server bijwerken voor lokalisatie door het [!DNL base\localization\*.zbin] bestand. Dit [!DNL insight.zbin] wordt vervolgens naar de client gekopieerd.

   An [!DNL insight.zbin] het bestand is opgenomen in de installatiemap naast de map [!DNL insight.exe] bestand. Als u verbinding maakt met een server die u geen taalspecifieke [!DNL .zbin] bestanden, dan wordt dit bestand gebruikt in de werkbank voor gegevens.

   De back-up [!DNL insight.zbin] bestand kan in elke taal worden opgegeven. Dientengevolge, als u de werkbank van gegevens in Chinees gebruikt en met een server verbindt die deze taal niet steunt, dan zal uw cliënt van de gegevenswerkbank nog in het Chinees zijn, zelfs als de server uw basisprofiel verandert en uw verwijdert [!DNL .zbin] bestanden van de [!DNL Base/Localization] map.

1. **Werk de server van het gegevenswerkbankrapport bij.** De [!DNL insight.zbin] in de hoofdmap van de rapportserver van de gegevenswerkbank wordt standaard de Engelse taal gebruikt. Als beheerder moet u de [!DNL .zbin] dossier van het bijgewerkte pakket van de rapportserver en plaats het in de wortelfolder van de server van het gegevenswerkbankrapport. Zoals de cliënt, vereist de rapportserver ook de juiste argumenten voor de geselecteerde taal, zoals [!DNL Insight.exe -zh-cn]

   1. Stop de diensten van de rapportserver.
   1. Kopieer de [!DNL Localization] van het nieuwe pakket van de rapportserver.
   1. Van de [!DNL Localization] map, kopieert u de [!DNL Insight.zbin] en plaats het in de wortelfolder van de rapportserver waar [!DNL Insight.exe] bevindt.

   1. Voeg eventueel vereiste argumenten toe, zoals [!DNL insight.exe -zh-cn]
   1. Start de rapportserver opnieuw.

## De gegevensworkbench-client bijwerken {#section-9653d3fcaf2a4337a97b685857e7aeac}

Nadat u de server hebt bijgewerkt, voert u de volgende stappen uit om elke client bij te werken.

1. Om ervoor te zorgen dat de client tijdens deze update niet van de server wordt bijgewerkt, stelt u uw [!DNL Insight.cfg] argument naar False.

   ```
   Update Software = bool: false
   ```

1. Start de client opnieuw.
1. Navigeer naar het profiel Software en Docs (SoftDocs-profiel) en download de vereiste **[!UICONTROL insight.zbin]** bestand van het clientpakket: [!DNL Software\Insight Client\Insight_6.1.zip]

1. Verplaats de [!DNL insight.zbin] bestand naar de map waarin [!DNL insight.exe] bevindt.

1. Om ervoor te zorgen dat de clientbestanden nu worden bijgewerkt vanaf de server, wijzigt u de [!DNL Insight.cfg] bestandsargument naar True:

   ```
   Update Software = bool: true
   ```

   I

   >[!NOTE]
   >
   >De client wordt gesynchroniseerd met de server. Er wordt een bericht weergegeven dat de client wordt bijgewerkt. Aan het einde van het downloaden ontvangt u een bericht met de vraag of u de client opnieuw wilt starten.

1. Klikken **OK** om de client opnieuw te starten.

Als u het volgende bericht krijgt, dan betekent het het [!DNL zbin] bestand is niet op dezelfde locatie geplaatst als [!DNL Insight.exe].

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

---
description: U kunt rapporten dynamisch voor de afmetingselementen produceren die u in een raadplegingsdossier of voor een bepaald aantal afmetingselementen, zoals voor de gebruikers met de 10 hoogste ordetellingen specificeert.
solution: Analytics
title: Dynamisch het Produceren Rapporten
topic: Data workbench
uuid: 87174fb5-e72f-4758-8e9d-1aaa784c1898
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Dynamisch het Produceren Rapporten{#dynamically-generating-reports}

U kunt rapporten dynamisch voor de afmetingselementen produceren die u in een raadplegingsdossier of voor een bepaald aantal afmetingselementen, zoals voor de gebruikers met de 10 hoogste ordetellingen specificeert.

>[!NOTE]
>
>Adobe ontmoedigt de verwezenlijking van dynamische rapportreeksen voor dagelijkse (of frequentere) rapportgeneratie. De dynamische rapportgeneratie kan middel-intensief zijn als u rapporten met grote of complexe vragen vormt.

* [Rapporten over dimensieelement van bestanden opzoeken](../../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-dyn-gen-rpts.md#section-a5e8f38af06c42b4bfddec4bafbf03d6)
* [Top Dimension-elementrapporten](../../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-dyn-gen-rpts.md#section-d8d75a6dfadd407bb18d6f32d70ebf8f)

## Rapporten over dimensieelement van bestanden opzoeken {#section-a5e8f38af06c42b4bfddec4bafbf03d6}

Om een rapport te vormen dat wordt geplaatst om dynamisch te produceren en (naar keuze) rapporten voor de elementen van een afmeting te verdelen die in een raadplegingsdossier wordt gespecificeerd, specificeer de volgende parameters in het [!DNL Report.cfg] dossier:

* [!DNL Dimension Name]
* [!DNL Lookup File]

Voor gedetailleerde beschrijvingen van deze parameters, zie Parameters [Report.cfg](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

**Om een dynamische rapportreeks te creëren die een raadplegingsdossier gebruikt**

1. Creeer een dossier van de twee-kolomraadpleging voor een bepaalde afmeting. Dit dossier moet twee lusje-afgebakende kolommen, zonder een kopbalrij bevatten.

   * Kolom 1 zou een lijst van afmetingselementen moeten bevatten.
   * Kolom 2 zou de e-mailadressen van de rapportontvangers moeten bevatten. Een verslag voor een bepaald element in kolom 1 wordt naar het e-mailadres (de e-mailadressen) op dezelfde rij in kolom 2 verzonden. U kunt veelvoudige e-mailadressen ingaan door hen met komma&#39;s (geen ruimten) te scheiden.

      >[!NOTE]
      >
      >
      >    
      >    
      >    * Als de rapporten niet per e-mail moeten worden verzonden, kan kolom 2 leeg zijn maar moet bestaan.
      >    * Dit dossier kan lege lijnen bevatten.




1. Optioneel. Om het e-mailen van rapporten toe te laten, moet u het volgende in de [!DNL Mail Report] sectie van het [!DNL Report.cfg] dossier voor die bepaalde rapportreeks doen:

   * In de parameter van de Server SMTP, maak een lijst van de aangewezen server SMTP die moet worden gebruikt om rapporten via e-mail te verdelen.
   * In de parameter Ontvangers, maak een lijst minstens één e-mailadres om de rapporten toe te laten om via e-mail worden verspreid. De rapporten worden niet gepost aan het adres vermeld-u plaatst deze parameter slechts om de rapporten toe te laten om worden gemaild. Dit kan een bogusadres zijn, maar het moet in een toelaatbaar formaat (bijvoorbeeld, [!DNL jsmith@company.com]) zijn.

1. Sparen het raadplegingsdossier aan de omslag van de rapportreeks.
1. Open het [!DNL Report.cfg] dossier voor de rapportreeks.
1. In de parameter van de Naam van de Dimensie, typ de naam van de afmeting waarvoor u een rapport dynamisch wilt produceren.
1. In de parameter van het Dossier van de Raadpleging, typ de plaats en de naam van het raadplegingsdossier die de afmetingselementen bevatten die u in het rapport en de ontvankelijke e e-mailadressen wilt.
1. Herhaal deze stappen voor extra rapportreeksen.

>[!NOTE]
>
>De dynamische rapporten worden niet per e-mail aan ontvangers tot de volledige rapportreeks volledig is.

## Top Dimension-elementrapporten {#section-d8d75a6dfadd407bb18d6f32d70ebf8f}

Om een rapport te vormen dat wordt geplaatst om rapporten voor de hoogste afmetingselementen dynamisch te produceren, die door gespecificeerde metrisch tellen, specificeer de volgende parameters in het [!DNL Report.cfg] dossier te produceren:

* Naam dimensie
* Bovenste N metrisch
* Beste N-waarde
* (Facultatief) de Filter van de Vraag van de Preload

Voor gedetailleerde beschrijvingen van deze parameters, zie Parameters [Report.cfg](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

**Om een dynamisch rapport te creëren dat voor de hoogste elementen wordt geplaatst**

1. Open het [!DNL Report.cfg] dossier van de rapportreeks.
1. In de parameter van de Naam van de Dimensie, typ de naam van de afmeting waarvoor u een rapportreeks dynamisch wilt produceren.
1. In de Hoogste Metrische parameter van N, typ de naam van metrisch waardoor u de afmeting wilt sorteren.
1. In de Hoogste parameter van de Waarde van N, typ het aantal afmetingselementen die u in de rapportreeks wilt.
1. (Facultatief) in de Preload parameter van de Filter van de Vraag, typ de naam van de gewenste filter.
1. Herhaal deze stappen voor extra rapportreeksen.
1. Voor informatie over het gebruiken van een dynamische titelvisualisatie met uw rapport, zie de Gids van de Gebruiker van de Werkbank van *Gegevens*.


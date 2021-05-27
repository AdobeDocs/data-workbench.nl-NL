---
description: U kunt rapporten dynamisch voor de afmetingselementen produceren die u in een raadplegingsdossier of voor een bepaald aantal afmetingselementen specificeert, zoals voor de gebruikers met de 10 hoogste orde tellingen.
title: Rapporten dynamisch genereren
uuid: 87174fb5-e72f-4758-8e9d-1aaa784c1898
exl-id: c14d93cd-212d-44a1-aff9-652e5c4fbda0
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# Rapporten dynamisch genereren{#dynamically-generating-reports}

U kunt rapporten dynamisch voor de afmetingselementen produceren die u in een raadplegingsdossier of voor een bepaald aantal afmetingselementen specificeert, zoals voor de gebruikers met de 10 hoogste orde tellingen.

>[!NOTE]
>
>Adobe ontmoedigt het creëren van dynamische rapportreeksen voor dagelijkse (of frequentere) rapportgeneratie. De dynamische rapportgeneratie kan middel-intensief zijn als u rapporten met grote of complexe vragen vormt.

* [Dimension-elementrapporten opzoeken](../../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-dyn-gen-rpts.md#section-a5e8f38af06c42b4bfddec4bafbf03d6)
* [Top Dimension Element Reports](../../../../../home/c-rpt-oview/c-work-rpt-sets/t-create-rpt-set/t-config-rpt-set/c-dyn-gen-rpts.md#section-d8d75a6dfadd407bb18d6f32d70ebf8f)

## Rapporten {#section-a5e8f38af06c42b4bfddec4bafbf03d6} Dimension-element opzoeken

Om een rapport te vormen dat wordt geplaatst om (naar keuze) rapporten voor de elementen van een afmeting dynamisch te produceren en te verdelen die in een raadplegingsdossier wordt gespecificeerd, specificeer de volgende parameters in [!DNL Report.cfg] dossier:

* [!DNL Dimension Name]
* [!DNL Lookup File]

Voor gedetailleerde beschrijvingen van deze parameters, zie [Parameters Report.cfg](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

**Een dynamische rapportset maken met een opzoekbestand**

1. Maak een opzoekbestand met twee kolommen voor een bepaalde dimensie. Dit bestand moet twee tabgescheiden kolommen bevatten, zonder koptekstrij.

   * Kolom 1 moet een lijst met dimensie-elementen bevatten.
   * Kolom 2 moet de e-mailadressen van de rapportontvangers bevatten. Een rapport voor een bepaald element in kolom 1 wordt naar het e-mailadres of de e-mailadressen in dezelfde rij in kolom 2 verzonden. U kunt meerdere e-mailadressen invoeren door deze te scheiden met komma&#39;s (geen spaties).

      >[!NOTE]
      >
      >
      >    
      >    
      >    * Als rapporten niet per e-mail moeten worden verstuurd, kan kolom 2 leeg zijn, maar moet deze bestaan.
      >    * Dit bestand kan lege regels bevatten.




1. Optioneel. Als u de e-mail van rapporten wilt inschakelen, moet u het volgende doen in de sectie [!DNL Mail Report] van het [!DNL Report.cfg] dossier voor die bepaalde rapportreeks:

   * In de parameter van de Server SMTP, maak een lijst van de aangewezen server SMTP die moet worden gebruikt om rapporten via e-mail te verspreiden.
   * Geef in de parameter Ontvangers ten minste één e-mailadres op, zodat de rapporten via e-mail kunnen worden verspreid. De rapporten worden niet gemaild aan het vermelde adres-u plaatst deze parameter slechts om de rapporten toe te staan om worden gemaild. Dit kan een misleidend adres zijn, maar het moet in een toelaatbare formaat (bijvoorbeeld, [!DNL jsmith@company.com]) zijn.

1. Sla het opzoekbestand op in de map van de rapportset.
1. Open het [!DNL Report.cfg] dossier voor de rapportreeks.
1. In de parameter van de Naam van Dimension, typ de naam van de afmeting waarvoor u een rapport dynamisch wilt produceren.
1. In de parameter van het Dossier van de Opzoekopdracht, typ de plaats en de naam van het raadplegingsdossier die de afmetingselementen bevatten die u in het rapport en de ontvankelijke e-mailadressen wilt.
1. Herhaal deze stappen voor extra rapportreeksen.

>[!NOTE]
>
>De dynamische rapporten worden niet naar ontvangers gemaild tot de volledige rapportreeks volledig is.

## Bovenste Dimension-elementrapporten {#section-d8d75a6dfadd407bb18d6f32d70ebf8f}

Om een rapport te vormen dat wordt geplaatst om rapporten voor de hoogste afmetingselementen dynamisch te produceren, die door gespecificeerde metrisch tellen, specificeer de volgende parameters in het [!DNL Report.cfg] dossier:

* Naam dimensie
* Bovenste N metrisch
* Bovenste N-waarde
* (Optioneel) Vooraf laden van queryfilter

Voor gedetailleerde beschrijvingen van deze parameters, zie [Parameters Report.cfg](../../../../../home/c-rpt-oview/c-rpt-param-ref/c-rpt-param.md#concept-838e59d72d3f4cb29ee15f5c7eb0ceff).

**Een dynamische rapportset maken voor de bovenste elementen**

1. Open het [!DNL Report.cfg] dossier van de rapportreeks.
1. In de parameter van de Naam van de Dimension, typ de naam van de afmeting waarvoor u een rapportreeks dynamisch wilt produceren.
1. Typ in de parameter Metrisch boven-N de naam van de metrische waarde waarmee u de dimensie wilt sorteren.
1. In de Bovenste parameter van de Waarde N, typ het aantal afmetingselementen die u in de rapportreeks wilt.
1. (Optioneel) Typ in de parameter Query-filter vooraf laden de naam van het gewenste filter.
1. Herhaal deze stappen voor extra rapportreeksen.
1. Voor informatie over het gebruiken van een dynamische titelvisualisatie met uw rapport, zie *de Gids van de Gebruiker van de Data Workbench*.

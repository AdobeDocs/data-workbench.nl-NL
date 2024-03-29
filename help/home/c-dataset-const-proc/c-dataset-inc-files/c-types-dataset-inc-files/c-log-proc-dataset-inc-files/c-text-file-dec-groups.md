---
description: Voor de verwerking van logbestanden als logbronnen is de definitie van een decoder vereist in het bestand Include-bestand van de gegevensset voor de logbestandverwerking om velden met gegevens uit de logbestandvermeldingen te extraheren.
title: Decoderingsgroepen tekstbestand
uuid: 3ff9700b-4f34-4098-8827-6856897bdb28
exl-id: e9f6e02e-7150-455f-96f0-f34d98cc31b7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Decoderingsgroepen tekstbestand{#text-file-decoder-groups}

{{eol}}

Voor de verwerking van logbestanden als logbronnen is de definitie van een decoder vereist in het bestand Include-bestand van de gegevensset voor de logbestandverwerking om velden met gegevens uit de logbestandvermeldingen te extraheren.

Voor het definiëren van decoderingsgroepen voor tekstbestanden voor logbestandslogbronnen is kennis vereist van de structuur en inhoud van het logbestand, de gegevens die moeten worden geëxtraheerd en de velden waarin die gegevens worden opgeslagen. Deze sectie bevat basisbeschrijvingen van de parameters die u voor decoders kunt opgeven, maar de manier waarop u een decoder gebruikt, is afhankelijk van het logbestand dat de brongegevens bevat.

Voor informatie over formaatvereisten voor de bronnen van het logboekdossier, zie [Logbestanden](../../../../../home/c-dataset-const-proc/c-log-proc-config-file/c-log-sources.md#concept-3d4fb817c057447d90f166b1183b461e). Neem contact op met Adobe voor hulp bij het definiëren van decoders voor tekstbestanden.

Een decoderingsgroep voor tekstbestanden kan het volgende bevatten:

* [Decoders voor reguliere expressies](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#section-67aca2c1f008404da7f845a64abec97c)
* [Gescheiden decoders](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-text-file-dec-groups.md#section-7e0a23decdbc4c75ae750a42446997a6)

## Decoders voor reguliere expressies {#section-67aca2c1f008404da7f845a64abec97c}

Een decoder voor reguliere expressies identificeert complexe tekenreekspatronen binnen de logitems in een logbestand en extraheert deze patronen als gegevensvelden. Voor elke decoder moet het aantal velden gelijk zijn aan het aantal vastgelegde subpatronen in de reguliere expressie. Het gedeelte van de regel dat overeenkomt met het subpatroon voor de n-de vastlegging, wordt toegewezen aan het nde veld voor die regel.

**Een reguliere-expressiedecoder toevoegen aan een decoderingsgroep voor een tekstbestand**

1. Open de [!DNL Log Processing Dataset Include] bestand zoals beschreven in [Bestaande gegevensset met include-bestanden bewerken](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077) en voeg een decoderingsgroep voor tekstbestanden toe. Zie de tabelvermelding [Decoderingsgroepen](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab).

1. Klikken met rechtermuisknop **[!UICONTROL Decoders]** onder de zojuist gemaakte decodergroep klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Regular Expression]**.

1. Geef de volgende informatie op:

   * **Velden:** Lijst met velden in het logbestand. Als een van de hier gedefinieerde velden moet worden doorgegeven aan de transformatiefase van de constructie van de gegevensset, moeten die velden worden vermeld in de parameter Fields van een van de [!DNL Log Processing Dataset Include] bestanden voor de gegevensset. Aangepaste veldnamen moeten beginnen met &quot;x-&quot;.

   * **Naam:** Optionele id voor de decoder.
   * **Reguliere expressie:** Wordt gebruikt om de gewenste velden uit elke regel in het bestand te extraheren.

1. Herhaal stap 4 en 5 voor alle andere decoders die u aan de groep wilt toevoegen.
1. Als u de [!DNL Log Processing Dataset Include] bestand, klik met de rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom. Klikken **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

>[!NOTE]
>
>Een bepaald logbestand kan meerdere decoders voor reguliere expressies bevatten. De volgorde waarin u de decoders definieert, is belangrijk: de eerste decoder die overeenkomt met een regel in het logbestand is de decoder die wordt gebruikt om die regel te decoderen.

In dit voorbeeld wordt het gebruik van een decoder voor reguliere expressies geïllustreerd om gegevensvelden uit een met tabs gescheiden tekstbestand te extraheren. U kunt hetzelfde resultaat bereiken door een gescheiden decoder met een tabscheidingsteken te definiëren.

![](assets/cfg_LogProcessingInclude_RegExpDecoder.png)

Voor meer informatie over reguliere-expressiedecoders, waaronder terminologie en syntaxis, raadpleegt u [Reguliere expressies](../../../../../home/c-dataset-const-proc/c-reg-exp.md#concept-070077baa419475094ef0469e92c5b9c).

## Gescheiden decoders {#section-7e0a23decdbc4c75ae750a42446997a6}

Een gescheiden decoder decodeert een logbestand waarvan de velden worden gescheiden door één teken. Het aantal velden moet overeenkomen met het aantal kolommen in het gescheiden bestand. niet alle velden hoeven echter een naam te krijgen . Als een veld leeg blijft, wordt de kolom nog steeds vereist in het logbestand, maar wordt deze genegeerd door de decoder.

**Een gescheiden decoder toevoegen aan een decoderingsgroep voor tekstbestanden**

1. Open de [!DNL Log Processing Dataset Include] bestand zoals beschreven in [Bestaande gegevensset met include-bestanden bewerken](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-work-dataset-inc-files/t-edit-ex-dataset-inc-files.md#task-456c04e38ebc425fb35677a6bb6aa077) en voeg een decoderingsgroep voor tekstbestanden toe. Zie de tabelvermelding [Decoderingsgroepen](../../../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab).

1. Klikken met rechtermuisknop **[!UICONTROL Decoders]** onder de zojuist gemaakte decodergroep klikt u op **[!UICONTROL Add new]** > **[!UICONTROL Delimited]**.

1. Geef de volgende informatie op:

   * **Velden:** Lijst met velden in het logbestand. Als een van de hier gedefinieerde velden moet worden doorgegeven aan de transformatiefase van de constructie van de gegevensset, moeten die velden worden vermeld in de parameter Fields van een van de [!DNL Log Processing Dataset Include] bestanden voor de gegevensset. Aangepaste veldnamen moeten beginnen met &quot;x-&quot;.

   * **Scheidingsteken:** Teken dat wordt gebruikt om velden in het uitvoerbestand van elkaar te scheiden.

1. Herhaal stap 4 en 5 voor alle andere decoders die u aan de groep wilt toevoegen.
1. Als u de [!DNL Log Processing Dataset Include] bestand, klik met de rechtermuisknop **[!UICONTROL (modified)]** boven aan het venster en klik op **[!UICONTROL Save]**.

1. Om de plaatselijk aangebrachte veranderingen van kracht te maken, in [!DNL Profile Manager]klikt u met de rechtermuisknop op het vinkje voor het bestand in het dialoogvenster [!DNL User] kolom, klik vervolgens op **[!UICONTROL Save to]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de profielnaam de naam is van het gegevenssetprofiel of het overgeërfde profiel waartoe de gegevensset include-bestand behoort.

>[!NOTE]
>
>Sla het gewijzigde configuratiebestand niet op in een van de interne profielen die door Adobe worden geleverd, omdat de wijzigingen worden overschreven wanneer u updates voor deze profielen installeert.

Dit voorbeeld illustreert het gebruik van een gescheiden decoder om gegevensvelden te extraheren uit een kommagescheiden tekstbestand met gegevens over films.

![](assets/cfg_LogProcessingInclude_DelimitedDecoder.png)

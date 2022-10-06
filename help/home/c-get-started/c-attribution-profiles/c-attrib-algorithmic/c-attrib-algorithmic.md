---
description: Best Fit Attribution is een machine-leert benadering om attributiewaarden over de verschillende kanalen van een succesvolle omzettingsgebeurtenis toe te wijzen. Data Workbench evalueert automatisch bijdragen aan succes over een periode per kanaal, en bouwt dan een attributiemodel dat op de daadwerkelijke interactiepatronen van uw klanten wordt gebaseerd.
title: Kenmerk best passend
uuid: 0c51beb3-8f74-4f8e-9722-0c885140c8ce
exl-id: 225a54d0-370c-4274-8a87-dc287bbb8201
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 0%

---

# Kenmerk best passend{#best-fit-attribution}

{{eol}}

Best Fit Attribution is een machine-leert benadering om attributiewaarden over de verschillende kanalen van een succesvolle omzettingsgebeurtenis toe te wijzen. Data Workbench evalueert automatisch bijdragen aan succes over een periode per kanaal, en bouwt dan een attributiemodel dat op de daadwerkelijke interactiepatronen van uw klanten wordt gebaseerd.

**[!UICONTROL Best Fit Attribution]** Hiermee kunt u de interacties (of aanrakingen) vergelijken die hebben bijgedragen tot een geslaagde verkoop, e-mailaanmelding of andere prestatie-indicatoren. De attributieanalyse wijst automatisch gewicht aan de belangrijkste aanrakingen toe en verstrekt een attributiemodel per kanaal dat op uw gegevens wordt gebaseerd en aan uw markt en interne protocollen reageert.

![](assets/attrib_windows_5.png)

Als een klant bijvoorbeeld uw site bezoekt via een organische zoekopdracht, voert u een campagne en meldt u zich vervolgens aan voor een e-mail, [Op regels gebaseerde Attributie](/help/home/c-get-started/c-attribution-profiles/c-rules-attrib/c-rules-attrib.md) zou de eerste aanraking of laatste aanraking identificeren, of zou succesattributie gelijkmatig over alle aanraakpunten verdelen gebruikend vooraf ingestelde attributiemodellen. Wanneer op regels gebaseerde attributie door de gebruiker wordt bepaald, plaatst de attributen Best Fit waarden door een algoritme door de waarschijnlijkheid van een omzetting als functie van de waargenomen aanrakingspunten te berekenen.

>[!NOTE]
>
>Uitvoeren **Kenmerk best passend** in Data Workbench, moet u uw servercertificaat bijwerken ( [!DNL .pem file]) ter ondersteuning van Adobe Analytics Premium. U moet ook toevoegen **Premium** naar uw aangepaste [!DNL Profile.cfg] voor de cliënt en ontvangt nieuwe certificaten van Adobe ClientCare voor Server en de Server van het Rapport.

## Basisinstelling {#section-db597eaee462412ea7280d1426366c61}

Zie [Een kenmerk best passend maken maken](../../../../home/c-get-started/c-attribution-profiles/c-attrib-algorithmic/c-attrib-building.md#concept-fede6fc4f592475fa8b351b1765a522d) voor stapsgewijze instructies.

**Metrische waarde voor succes instellen**
Bepaal metrisch die een succesgebeurtenis vertegenwoordigen.

![](assets/attrib_windows_1.png)

De succesmetrische waarde is vaak *Orders*, hoewel u Data Workbench kunt gebruiken om een zeer gecompliceerde succesmetrische waarde samen met het Venster van het Succes te bepalen.

**De aanraakmeting instellen** (optioneel)

Identificeer interacties om bij te houden die tot een succesvolle omzetting leidden, dan plaats metrisch van de Aanraking waarover de attributie zal worden berekend.

>[!NOTE]
>
>Het instellen van een aanraakmeting is alleen vereist als u deze gebruikt om Kanaalmetriek af te leiden van het slepen en neerzetten van Dimension-elementen in plaats van bestaande kanaalmetriek te gebruiken.

Als u geen metrische definitie voor campagnes of kanalen hebt, maar afmetingen die kanalen vertegenwoordigen hebben, kan Beste Aanpasbare Attributie hen voor u automatisch bouwen die op metrisch van de Aanraking wordt gebaseerd.

Met de set Touch Metric bijvoorbeeld als *Hits* en een dimensie krijgen die *Mediatype* met elementen die *E-mail*, *Persbericht*, *Ad afdrukken*, en *Sociale media* resulteert de visualisatie in Kanaalwaarden van het formulier [!DNL Hits where Media Type = Email] wanneer u het element of de elementen naar de visualisatie sleept.

![](assets/attrib_windows_2.png)

De Touch-parameter bepaalt vervolgens de toewijzing van toewijzingsscores om marketinginteracties te identificeren die van invloed zijn op succes, zodat u marketingtips kunt kwalificeren voor de populatie die in het venster Succes is geïdentificeerd. U kunt metrisch instellen, zoals *Paginaweergaven* of *Hits* of gebruik aangepaste aanraakmetriek die specifiek is voor uw behoeften.

In veel gevallen moet het venster Touch het venster Success bevatten om een lange aanlooptijd in de verkoopcyclus te evalueren.

**Stel de maatstaf voor inkomsten in.**

U kunt ervoor kiezen om inkomsten te identificeren tussen aanraakpunten door een geschikte inkomstenmaatstaf in te stellen. Indien gespecificeerd, zal het model de verdeling van opbrengst over de inputkanalen tonen. ![](assets/attrib_windows_6.png)

U kunt een opbrengstmetrische met muntgegevenstypes plaatsen om succes over alle hoogste vastgestelde en geanalyseerde aanraakpunten toe te wijzen. Deze maatstaf verdeelt de eindverkoopopbrengst en verdeelt deze op basis van de door het algoritme toegewezen weging.

**Stel de opties Succesvol en Touch Windows in.**

Het venster van het Succes bepaalt de bevolking te onderzoeken en de periode voor succesvolle gebeurtenissen, die u toestaan om op de vensters van tijd en breedte van bevolking te wijzen om voor de analyse door een werkruimteselectie te overwegen. De **Succes** window bepaalt de periode en de bevolking om op succesgebeurtenissen te onderzoeken. De **Aanraken** window specificeert de historische tijdspanne om voor kanaalinteractie te onderzoeken die tot de succesgebeurtenissen leiden.

>[!NOTE]
>
>Het instellen van een aanraakmetrisch is alleen vereist als u cijfers voor succes automatisch probeert te maken door dimensie-elementen naar de visualisatie te slepen.

U kunt een dag, maand, jaar, of om het even welk beschikbaar tijdkader plaatsen om uw evaluatie van succes te beperken en gebeurtenissen over de verkoopcyclus te raken of voor specifieke publiek dat uw plaats ingaat. Door vensters te maken om de toewijzing te beperken, kunt u uw analyse toespitsen op de relevante tijdsperiodes voor uw specifieke behoeften.

![](assets/attrib_windows_4.png)

In veel gevallen wilt u dat het venster Touch het venster Success bevat, zodat u de analyse kunt uitbreiden over een lange doorlooptijd die is gebaseerd op uw verkoopvenster. Of u kunt aanrakingen afzonderlijk van de succesgebeurtenis volgen en analyseren.

**Selecteer de kanalen.**

Bij het invoeren van kanalen hebt u twee mogelijkheden.

**Voeg de optie Metrisch aanraken toe en voeg Dimension-elementen toe aan de kanalen**

In veel gevallen zult u de bovenste aanraakpunten willen splitsen op dimensie-elementen om specifieke kanalen te definiëren. Gebaseerd op de elementwaarden, zal Best Fit Attribution automatisch de hoogste uitvoerders selecteren en zal hen op percentage rangschikken en hen in een grafiekvisualisatie tonen.

![](assets/attrib_windows_7.png)

Een attributiemodel wordt samengesteld door te tekenen op de bezoekers die tijdens het venster Succes met elkaar hebben gewerkt en de kanaalaanrakingen te bekijken tijdens het aanraakvenster die al dan niet tot een geslaagde gebeurtenis hebben geleid.

## Omlaag splitsen op kanalen {#section-a30592b84bc84f57bd2b988824e852d4}

Bij het invoeren van kanalen hebt u twee opties:

* Voeg een **Touch Metric** en vervolgens toevoegen **Dimension Elements** voor de Kanalen.

   **of**

* Creeer metriek die filter voor de kanaalelementen die u wilt evalueren.

**Optie 1: Een touch-metrisch toevoegen en Dimension-elementen toevoegen voor kanalen**.

Dit is de gemakkelijkere aanpak. Met kenmerk Aanpassen aan maakt u de meetgegevens automatisch om de kenmerken te evalueren. In het onderstaande voorbeeld is de Touch Metric ***Hits*** en Kanalen zijn: ***Campagnes weergeven***, ***E-mailcampagnes***, en ***SEM-campagnes***.

Met deze methode maakt u een maateenheid op de achtergrond voor het evalueren van de toewijzing via de kanalen (maar u ziet nooit de automatisch gegenereerde metrische waarde en deze wordt niet opgeslagen). In het onderstaande voorbeeld worden drie metriek gemaakt waarbij Hits voor elk van de drie kanalen wordt gefilterd (bijvoorbeeld *Campagnes weergeven*, *E-mailcampagnes*, en *SEM-campagnes*). Dit is het gemakkelijkst omdat u de maatstaven voor u laat maken met kenmerk Best Fit.

![](assets/attrib_touch_add_dims.png)

**Optie 2: Een metrisch object maken**.

In de tweede optie, creeert en bewaart u de metriek voor de kanalen die u door een specifiek kanaal wilt evalueren te filtreren. Een voorbeeld van zo metrisch wordt getoond hieronder.

![](assets/attrib_create_metric.png)

Vervolgens kunt u in plaats van een aanraakmetrisch element en Dimension-element voor de kanalen in te voeren op de menubalk in de visualisatie klikken en **Invoer** > **Kanaal toevoegen** en selecteer vervolgens de maatstaven die u hebt gemaakt.

![](assets/attrib_results_2.png)

Zie het voorbeeld van de tweede methode hieronder. U ziet dat de resultaten van beide opties identiek zijn.

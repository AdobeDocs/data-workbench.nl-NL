---
description: Het maskeren verwijst naar het selecteren van een ondergroep van uw gegevens of een ondergroep van de elementen in een afmeting.
solution: Analytics
title: Maskergegevens
topic: Data workbench
uuid: 81b5f4e0-826c-4803-9169-66a424a4ea9f
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Maskergegevens{#mask-data}

Het maskeren verwijst naar het selecteren van een ondergroep van uw gegevens of een ondergroep van de elementen in een afmeting.

U maskeert of verbergt die elementen die u niet inbegrepen in de analyse wilt.

De Werkbank van gegevens verstrekt twee methodes om afmetingselementen te maskeren. De eerste methode wendt de opties aan beschikbaar in het [!DNL Mask] menu. Gebruikend de [!DNL Mask] menuopties, kunt u uw muis gebruiken om die elementen te selecteren om te tonen of te maskeren, of u kunt top-gerangschikte elementen tonen wanneer u de gegevens door metrisch sorteert. De tweede methode om afmetingselementen te maskeren wendt een onderzoek aan.

**Om gegevens te maskeren**

1. Klik een element of het etiket van de gewenste afmeting met de rechtermuisknop aan en klik **[!UICONTROL Mask]**.

   ![](assets/mnu_Table_Mask.png)

1. Klik op een van de volgende opties:

   * **[!UICONTROL Show all]**
   * **[!UICONTROL Show selected only]**
   * **[!UICONTROL Hide selected]**
   * **[!UICONTROL Show top > 5, 10, 25, 50, 100]**, of **[!UICONTROL 500]** van de getoonde die elementen door metrisch worden gesorteerd
   * **[!UICONTROL Show top > All Positive]** om slechts waarden te tonen groter dan nul (0)
   * **[!UICONTROL Display “X more”]** om het aantal momenteel gemaskeerde elementen te tonen
   * **[!UICONTROL At least one >]***&lt; **[!UICONTROL countable dimension name]**>*(alleen beschikbaar bij werken met een denormale dimensie)

      Wanneer het werken met een denormale afmeting, laat deze optie u toe om een afmeting door een telbare afmeting te maskeren. Wanneer geselecteerd, toont de lijst slechts die elementen die minstens één element van de telbare dimensie hebben die u selecteerde. De lijst toont tot 1.023 elementen.

>[!NOTE]
>
>Omdat Adobe gegevens in willekeurige orde [!DNL Platform] verwerkt, wanneer minstens één het maskeren in meer dan 1.023 elementen resulteert, hebben de gemeenschappelijkere en grotere elementen een grotere kans om in de lijst worden omvat.

Wanneer u door toont bovenkant of minstens één maskeert, door gebrek beantwoordt de orde in de lijst aan de waarden zoals die door de selectie op dat ogenblik worden beïnvloed. Als u later de selectie verandert, verandert de orde niet van de originele orde tenzij de lijst wordt geresorteerd of u Dynamische Selectie toelaat. Wanneer u klikt **[!UICONTROL Mask]** > **[!UICONTROL Dynamic Selection]**, wordt de lijst opnieuw geplaatst telkens als u de selectie verandert.

**Om gegevens te maskeren die een onderzoek gebruiken**

* U kunt gegevens maskeren met een van de volgende zoekopties:

   * Klik een element of het etiket van de gewenste afmeting met de rechtermuisknop aan, klik **[!UICONTROL Mask]**, dan in het [!DNL Search] doostype de uitdrukking waarvoor u wilt zoeken.

      ![](assets/mnu_Table_MaskSearch.png)

   * Klik een element of het etiket van de gewenste afmeting met de rechtermuisknop aan, klik **[!UICONTROL Mask]** > **[!UICONTROL Display search bar]**, dan in de onderzoeksdoos die in de cel van het afmetingsetiket toont, typ de uitdrukking waarvoor u wilt zoeken.

      ![](assets/vis_Table_Mask_searchBar.png)

      Aangezien u een onderzoeksuitdrukking typt, werkt de Werkbank van Gegevens de afmeting bij om op gelijken te wijzen.

Om het maskeren tijdens een onderzoek verder te beperken, kunt u om het even welke volgende methodes gebruiken:

* U kunt &quot;re:&quot;in de [!DNL search] doos of de bar typen om de onderzoeksuitdrukking te hebben die als regelmatige uitdrukking wordt geïnterpreteerd. U kunt om het even welke syntaxis gebruiken verbonden aan regelmatige uitdrukkingen in uw onderzoeksuitdrukking. Voor meer informatie over regelmatige uitdrukkingen, zie het Regelmatige bijlage van de Uitdrukking in de Gids *van de Configuratie van de* Dataset.
* U kunt het $ symbool als eerste karakter in uw onderzoekskoord typen om uitdrukkingen te vinden die met het koord beginnen u inging, of als laatste karakter om uitdrukkingen te vinden die met het koord beëindigen u inging.
* U kunt een ruimte als eerste karakter in uw onderzoekskoord typen om het even welke woorden binnen een uitdrukking te vinden die met het koord beginnen u inging, of als laatste karakter om het even welke woorden binnen een uitdrukking te vinden die met het koord beëindigde u inging.

Na zijn voorbeelden van verschillende manieren om een lijst te maskeren gebruikend het koord &quot;op&quot;in een onderzoek:

* Het typen &quot;op&quot;toont elke uitdrukking die het koord &quot;op&quot;overal in de uitdrukking bevat: &quot;**** online bankieren&quot;, &quot;**** contact opnemen met kopers&quot;, &quot;**gouden** munten&quot;, &quot;bank **** online&quot;, &quot;gouden **** opties&quot; en &quot;zilveren **miljard**&quot;.
* Het typen &quot;$on&quot;toont elke uitdrukking die met het koord &quot;op&quot;begint:

   &quot;**** online bankieren&quot; en &quot;**on**-line betaling&quot;.

* Het typen &quot;op$&quot;toont elke uitdrukking die met het koord &quot;op&quot;beëindigt:

   &quot;zilveren **edelmetaal**&quot; en &quot;gouden **optie**&quot;.

* Het typen &quot;op&quot;toont elke uitdrukking die een woord bevat dat met het koord &quot;op&quot;begint:

   &quot;**** online bankieren&quot; en &quot;bank **** online&quot;.

* Het typen &quot;op&quot;toont elke uitdrukking die een woord bevat dat met het koord &quot;op&quot;beëindigt:

   &quot;**gouden** munten&quot; en &quot;zilveren **edelmetaal**&quot;.

* Het gebruiken &quot;op&quot;toont elke uitdrukking die het koord &quot;op&quot;als woord bevat:

   &quot;**on** line banking&quot; en &quot;bank **on** line&quot;.


---
description: Maskeren verwijst naar het selecteren van een subset van uw gegevens of een subset van de elementen in een dimensie.
title: Maskergegevens
uuid: 81b5f4e0-826c-4803-9169-66a424a4ea9f
exl-id: 3029e08e-827f-40d7-b5a1-45630876a097
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# Maskergegevens{#mask-data}

{{eol}}

Maskeren verwijst naar het selecteren van een subset van uw gegevens of een subset van de elementen in een dimensie.

U maskeert of verbergt de elementen die u niet in de analyse wilt opnemen.

Data Workbench biedt twee methoden voor het maskeren van dimensie-elementen. Bij de eerste methode worden de opties gebruikt die beschikbaar zijn in het dialoogvenster [!DNL Mask] -menu. Met de [!DNL Mask] kunt u de muis gebruiken om de elementen te selecteren die u wilt tonen of maskeren, of u kunt de elementen op de hoogste positie tonen wanneer u de gegevens op metrische basis sorteert. De tweede methode voor het maskeren van dimensie-elementen maakt gebruik van een zoekopdracht.

**Gegevens maskeren**

1. Klik met de rechtermuisknop op een element of het label van de gewenste dimensie en klik op **[!UICONTROL Mask]**.

   ![](assets/mnu_Table_Mask.png)

1. Klik op een van de volgende opties:

   * **[!UICONTROL Show all]**
   * **[!UICONTROL Show selected only]**
   * **[!UICONTROL Hide selected]**
   * **[!UICONTROL Show top > 5, 10, 25, 50, 100]**, of **[!UICONTROL 500]** van de weergegeven elementen, gesorteerd op metrisch
   * **[!UICONTROL Show top > All Positive]** alleen waarden groter dan nul (0) weergeven
   * **[!UICONTROL Display “X more”]** om het aantal momenteel gemaskerde elementen weer te geven
   * **[!UICONTROL At least one >]***&lt; **[!UICONTROL countable dimension name]**>*(alleen beschikbaar wanneer u werkt met een denormale dimensie)

      Wanneer het werken met een denormale afmeting, laat deze optie u toe om een afmeting door een telbare afmeting te maskeren. Wanneer geselecteerd, toont de lijst slechts die elementen die minstens één element van de telbare afmeting hebben die u selecteerde. De tabel bevat maximaal 1023 elementen.

>[!NOTE]
>
>Omdat de Adobe [!DNL Platform] verwerkt gegevens in willekeurige volgorde, wanneer ten minste één maskering resulteert in meer dan 1023 elementen, hebben de meer gangbare en grotere elementen een grotere kans om in de tabel te worden opgenomen.

Wanneer u maskeert door Bovenzijde tonen of minstens één, door gebrek beantwoordt de orde in de lijst aan de waarden zoals die door de selectie op dat ogenblik worden beïnvloed. Als u de selectie later wijzigt, verandert de volgorde niet in de oorspronkelijke volgorde, tenzij de tabel opnieuw wordt gesorteerd of u Dynamische selectie inschakelt. Wanneer u op **[!UICONTROL Mask]** > **[!UICONTROL Dynamic Selection]** De tabel wordt telkens opnieuw gesorteerd wanneer u de selectie wijzigt.

**Gegevens maskeren met een zoekopdracht**

* U kunt gegevens maskeren met een van de volgende zoekopties:

   * Klik met de rechtermuisknop op een element of het label van de gewenste dimensie en klik op **[!UICONTROL Mask]** en vervolgens in de [!DNL Search] Typ de woordgroep waarnaar u wilt zoeken.

      ![](assets/mnu_Table_MaskSearch.png)

   * Klik met de rechtermuisknop op een element of het label van de gewenste dimensie en klik op **[!UICONTROL Mask]** > **[!UICONTROL Display search bar]** Typ vervolgens in het zoekvak dat wordt weergegeven in de cel met het dimensielabel de woordgroep waarnaar u wilt zoeken.

      ![](assets/vis_Table_Mask_searchBar.png)

      Terwijl u een zoekfrase typt, wordt de Data Workbench aangepast aan de overeenkomsten.

Als u het maskeren tijdens een zoekopdracht verder wilt beperken, kunt u een van de volgende methoden gebruiken:

* U kunt &quot;re:&quot; typen in het dialoogvenster [!DNL search] vak of balk om de zoekuitdrukking als een reguliere expressie te laten interpreteren. U kunt elke syntaxis gebruiken die is gekoppeld aan reguliere expressies in uw zoekfragment. Zie de sectie Reguliere expressie in de *Configuratie-handleiding voor gegevensset*.
* U kunt het $ symbool als eerste karakter in uw onderzoekstekenreeks typen om uitdrukkingen te vinden die met het koord beginnen u inging, of als laatste karakter om uitdrukkingen te vinden die met het koord beëindigen u inging.
* U kunt een spatie typen als het eerste teken in de zoektekenreeks om te zoeken naar woorden binnen een woordgroep die begint met de tekenreeks die u hebt ingevoerd, of als het laatste teken om woorden te zoeken binnen een woordgroep die eindigt met de tekenreeks die u hebt ingevoerd.

Hier volgen voorbeelden van verschillende manieren om een tabel te maskeren met de tekenreeks &quot;on&quot; in een zoekopdracht:

* Wanneer u &quot;on&quot; typt, wordt elke woordgroep met de tekenreeks &quot;on&quot; overal in de woordgroep weergegeven: &quot;**op** line banking,&quot; c **op** tact kopers, &quot; bulli **op** munten&quot;, &quot;bank **op** lijn,&quot; &quot;gouden opti **op** s,&quot; en &quot;zilverbollen **op**.&quot;
* Wanneer u &quot;$on&quot; typt, wordt elke woordgroep weergegeven die begint met de tekenreeks &quot;on&quot;:

   &quot;**op** line banking&quot; en &quot;**op**-line betaling.&quot;

* Als u &quot;on$&quot; typt, wordt elke woordgroep weergegeven die eindigt met de tekenreeks &quot;on&quot;:

   &quot;zilverbollen **op**&quot; en &quot;goudopti **op**.&quot;

* Als u &quot;on&quot; typt, wordt elke woordgroep weergegeven die een woord bevat dat begint met de tekenreeks &quot;on&quot;:

   &quot;**op** line banking&quot; en &quot;bank&quot; **op** lijn.&quot;

* Als u &quot;on&quot; typt, wordt elke woordgroep weergegeven die een woord bevat dat eindigt met de tekenreeks &quot;on&quot;:

   &quot;bulli **op** munten&quot; en &quot;zilverbollen&quot;**op**.&quot;

* Als u &quot;on&quot; gebruikt, wordt elke woordgroep met de tekenreeks &quot;on&quot; weergegeven als een woord:

   &quot;**op** line banking&quot; en &quot;bank&quot; **op** lijn.&quot;

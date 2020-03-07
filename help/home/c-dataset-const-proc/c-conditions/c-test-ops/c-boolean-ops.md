---
description: De verrichtingen Van Boole combineren de resultaten van de testverrichtingen, die als kinderen van de verrichtingen van Boole functioneren.
solution: Analytics
title: Booleaanse bewerkingen
topic: Data workbench
uuid: 01143bc2-c867-434c-8028-86d4708e8b80
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Booleaanse bewerkingen{#boolean-operations}

De verrichtingen Van Boole combineren de resultaten van de testverrichtingen, die als kinderen van de verrichtingen van Boole functioneren.

Voor informatie over de testverrichtingen, zie de Verrichtingen van de [Test](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-ops.md#concept-c4bf6cb9e7a94cc7ac49ca9b0b1a2144). Wanneer u een [!DNL boolean] verrichting bepaalt, kunt u nul of meer kinderen voor de verrichting bepalen.

**Om een kindvoorwaarde aan een verrichting toe te voegen Van Boole**

1. Klik met de rechtermuisknop op de naam of het nummer dat overeenkomt met de [!DNL Boolean] bewerking.
1. Klik **[!UICONTROL Add new child]** en kies één van de beschikbare voorwaardentypes om toe te voegen.
1. Herhaal stappen 1 en 2 tot u alle gewenste kindvoorwaarden voor de [!DNL Boolean] verrichting hebt toegevoegd.

   >[!NOTE]
   >
   >Wanneer u de naam of het aantal met de rechtermuisknop aanklikt dat aan een [!DNL Boolean] verrichting beantwoordt, ziet u de [!DNL Add new sibling] menuoptie. Een sibling is een andere voorwaarde bij de zelfde relatieve positie in de voorwaardenhiërarchie zoals de [!DNL Boolean] verrichting die u met de rechtermuisknop aanklikte. Het toevoegen van een nieuw sibling voor een [!DNL Boolean] verrichting is het zelfde als toevoegend een nieuwe voorwaarde door de [!DNL Condition] of [!DNL Log Entry Condition] parameter met de rechtermuisknop aan te klikken.

**Om een kindvoorwaarde uit een verrichting te verwijderen Van Boole:**

1. Klik de naam van de kindvoorwaarde of het aantal met de rechtermuisknop aan die aan de kindvoorwaarde beantwoorden die u uit de [!DNL Boolean] verrichting wilt verwijderen.
1. Klik op **[!UICONTROL Remove]** &lt;* **[!UICONTROL #number]***>, waarbij het nummer overeenkomt met de onderliggende voorwaarde die u wilt verwijderen.

In deze sectie worden de volgende voorwaarden besproken:

* [en](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a14dba4b07cc4ab9aeb20868f773db7c)
* [Geen](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-7e48b61266aa43ecbc48b979bf5e939b)
* [of](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a3aa0f56b6234f2680fa81939228326b)

## en {#section-a14dba4b07cc4ab9aeb20868f773db7c}

De [!DNL And] voorwaarde kan nul of meer kindvoorwaarden hebben en keert waar terug wanneer geen van zijn kindknopen vals terugkeren.

De [!DNL And] voorwaarde vormt de wortelverrichting van al voorwaarde het testen binnen de server van de gegevenswerkbank. Als de [!DNL And] voorwaarde geen kinderen bevat, evalueert de voorwaarde aan waar en de bijbehorende verrichtingsopbrengst. Dit is waarom de acties die slechts de [!DNL And] voorwaarde als voorwaardentest hebben altijd uitvoeren en waarom het als wortel voor alle voorwaardentests wordt gebruikt.

Dit voorbeeld toont aan hoe een [!DNL And] voorwaarde wordt gebruikt om ervoor te zorgen dat de [!DNL Copy] transformatie voorkomt wanneer slechts zowel de datum van de logboekingang in het jaar 2006 voorkwam en dat de gevraagde pagina was [!DNL /products/purchase.asp].

![](assets/cfg_Condition_AndCondition.png)

## Geen {#section-7e48b61266aa43ecbc48b979bf5e939b}

De [!DNL Neither] voorwaarde kan nul of meer kindvoorwaarden hebben en vals terugkeren als om het even welke van zijn kindvoorwaarden aan waar evalueren. Als de [!DNL Neither] aandoening geen kinderen bevat, kan geen van zijn kinderen terugkeren waar. Dientengevolge, evalueert de [!DNL Neither] voorwaarde aan waar.

Het volgende voorbeeld toont een [!DNL Neither] voorwaarde met twee [!DNL Range] voorwaarden als zijn kinderen. Zoals gedefinieerd, omvat de [!DNL Neither] voorwaarde geen logboekvermeldingen die plaatsvonden tussen 1 januari 2007 en 10 januari 2007 of in de periode van 12 januari 2007 tot 14 januari 2007. Een dergelijke voorwaarde zou kunnen worden gebruikt als de voorwaarde [!DNL Log Entry Condition] om transacties uit een dataset te elimineren gedurende perioden waarin er een bekend probleem met de verzamelde gegevens was.

![](assets/cfg_Condition_NeitherCondition.png)

## of {#section-a3aa0f56b6234f2680fa81939228326b}

De [!DNL Or] voorwaarde kan nul of meer kindvoorwaarden hebben en keert waar terug als minstens één van zijn kindvoorwaarden aan waar evalueren. Als de [!DNL Or] aandoening geen kinderen bevat, kan geen van zijn kinderen terugkeren waar. Dientengevolge, evalueert de [!DNL Or] voorwaarde aan vals.

Dit voorbeeld toont de [!DNL Or] aandoening met een [!DNL String Match] aandoening en een [!DNL Range] aandoening als zijn kinderen. Aan de [!DNL Or] voorwaarde wordt voldaan slechts als de logboekingang de [!DNL x-hasproblem] waarde heeft die aan ja wordt geplaatst of de logboekingang kwam tijdens de tijdwaaier januari 1, 2007, aan 10 Januari voor, 2007.

![](assets/cfg_Condition_OrCondition.png)


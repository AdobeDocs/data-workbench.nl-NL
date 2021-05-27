---
description: De verrichtingen Van Boole combineren de resultaten van de testverrichtingen, die als kinderen van de booleaanse verrichtingen functioneren.
title: Booleaanse bewerkingen
uuid: 01143bc2-c867-434c-8028-86d4708e8b80
exl-id: 5b01e614-5603-43ff-9be4-aa329cca1645
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Booleaanse bewerkingen{#boolean-operations}

De verrichtingen Van Boole combineren de resultaten van de testverrichtingen, die als kinderen van de booleaanse verrichtingen functioneren.

Zie [Bewerkingen testen](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-ops.md#concept-c4bf6cb9e7a94cc7ac49ca9b0b1a2144) voor informatie over de testbewerkingen. Wanneer u een [!DNL boolean] verrichting bepaalt, kunt u nul of meer kinderen voor de verrichting bepalen.

**Een onderliggende voorwaarde toevoegen aan een Booleaanse bewerking**

1. Klik met de rechtermuisknop op de naam of het nummer dat overeenkomt met de bewerking [!DNL Boolean].
1. Klik op **[!UICONTROL Add new child]** en kies een van de beschikbare voorwaardetypen die u wilt toevoegen.
1. Herhaal stap 1 en 2 totdat u alle gewenste onderliggende voorwaarden voor de bewerking [!DNL Boolean] hebt toegevoegd.

   >[!NOTE]
   >
   >Als u met de rechtermuisknop op de naam of het nummer klikt dat overeenkomt met een bewerking [!DNL Boolean], wordt de menuoptie [!DNL Add new sibling] weergegeven. Een sibling is een andere voorwaarde bij de zelfde relatieve positie in de voorwaardenhiërarchie zoals [!DNL Boolean] verrichting die u met de rechtermuisknop aanklikte. Het toevoegen van een nieuw sibling voor een [!DNL Boolean] verrichting is het zelfde als het toevoegen van een nieuwe voorwaarde door de [!DNL Condition] of [!DNL Log Entry Condition] parameter met de rechtermuisknop aan te klikken.

**Een onderliggende voorwaarde verwijderen uit een Booleaanse bewerking:**

1. Klik met de rechtermuisknop op de naam van de onderliggende voorwaarde of het nummer dat overeenkomt met de onderliggende voorwaarde die u wilt verwijderen uit de bewerking [!DNL Boolean].
1. Klik **[!UICONTROL Remove]** &lt;* **[!UICONTROL #number]***>, waarbij het getal het getal is dat overeenkomt met de onderliggende voorwaarde die u wilt verwijderen.

In deze sectie worden de volgende voorwaarden besproken:

* [en](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a14dba4b07cc4ab9aeb20868f773db7c)
* [Geen](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-7e48b61266aa43ecbc48b979bf5e939b)
* [of](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a3aa0f56b6234f2680fa81939228326b)

## en {#section-a14dba4b07cc4ab9aeb20868f773db7c}

De voorwaarde [!DNL And] kan nul of meer kindvoorwaarden hebben en keert waar terug wanneer geen van zijn kindknopen vals terugkeren.

De voorwaarde [!DNL And] vormt de basisbewerking van alle voorwaarde die wordt getest op de gegevenswerkbankserver. Als de voorwaarde [!DNL And] geen kinderen bevat, evalueert de voorwaarde aan waar en de bijbehorende verrichting gaat te werk. Daarom worden handelingen die alleen de voorwaarde [!DNL And] als voorwaarde hebben, altijd uitgevoerd en wordt deze als basis voor alle voorwaardetests gebruikt.

In dit voorbeeld wordt getoond hoe een voorwaarde [!DNL And] wordt gebruikt om ervoor te zorgen dat de transformatie [!DNL Copy] plaatsvindt wanneer alleen de datum van de logbestandvermelding in 2006 is opgetreden en dat de gevraagde pagina [!DNL /products/purchase.asp] is.

![](assets/cfg_Condition_AndCondition.png)

## Geen {#section-7e48b61266aa43ecbc48b979bf5e939b}

De voorwaarde [!DNL Neither] kan nul of meer kindvoorwaarden hebben en keert vals terug als om het even welk van zijn kindvoorwaarden aan waar evalueren. Als de voorwaarde [!DNL Neither] geen kinderen bevat, kan geen van zijn kinderen waar terugkeren. Het resultaat is dat de voorwaarde [!DNL Neither] true oplevert.

In het volgende voorbeeld wordt een voorwaarde [!DNL Neither] met twee voorwaarden [!DNL Range] getoond als onderliggende voorwaarden. Zoals gedefinieerd, sluit de [!DNL Neither] voorwaarde logingangen uit die tussen 1 Januari, 2007 en 10 Januari, 2007 of tijdens de periode 12 Januari, 2007, tot 14 Januari, 2007 optraden. Een dergelijke voorwaarde zou als [!DNL Log Entry Condition] kunnen worden gebruikt om transacties uit een dataset tijdens periodes te elimineren waarin er een bekend probleem met de verzamelde gegevens was.

![](assets/cfg_Condition_NeitherCondition.png)

## Of {#section-a3aa0f56b6234f2680fa81939228326b}

De voorwaarde [!DNL Or] kan nul of meer kindvoorwaarden hebben en keert waar terug als minstens één van zijn kindvoorwaarden aan waar evalueert. Als de voorwaarde [!DNL Or] geen kinderen bevat, kan geen van zijn kinderen waar terugkeren. Als gevolg hiervan levert de voorwaarde [!DNL Or] false op.

In dit voorbeeld wordt de voorwaarde [!DNL Or] met een voorwaarde [!DNL String Match] en een voorwaarde [!DNL Range] als onderliggende voorwaarde getoond. Aan de voorwaarde [!DNL Or] wordt alleen voldaan als voor het logbestand de waarde [!DNL x-hasproblem] is ingesteld op ja of als de logbestandvermelding is opgetreden tijdens het tijdsbereik van 1 januari 2007 tot 10 januari 2007.

![](assets/cfg_Condition_OrCondition.png)

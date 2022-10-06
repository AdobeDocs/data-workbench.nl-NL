---
description: De verrichtingen Van Boole combineren de resultaten van de testverrichtingen, die als kinderen van de booleaanse verrichtingen functioneren.
title: Booleaanse bewerkingen
uuid: 01143bc2-c867-434c-8028-86d4708e8b80
exl-id: 5b01e614-5603-43ff-9be4-aa329cca1645
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Booleaanse bewerkingen{#boolean-operations}

{{eol}}

De verrichtingen Van Boole combineren de resultaten van de testverrichtingen, die als kinderen van de booleaanse verrichtingen functioneren.

Voor informatie over de testbewerkingen raadpleegt u [Bewerkingen testen](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-test-ops.md#concept-c4bf6cb9e7a94cc7ac49ca9b0b1a2144). Wanneer u een [!DNL boolean] kunt u nul of meer onderliggende items voor de bewerking definiëren.

**Een onderliggende voorwaarde toevoegen aan een Booleaanse bewerking**

1. Klik met de rechtermuisknop op de naam of het nummer dat overeenkomt met de [!DNL Boolean] bewerking.
1. Klikken **[!UICONTROL Add new child]** en kiest u een van de beschikbare voorwaardetypen die u wilt toevoegen.
1. Herhaal stap 1 en 2 totdat u alle gewenste onderliggende voorwaarden voor de [!DNL Boolean] bewerking.

   >[!NOTE]
   >
   >Als u met de rechtermuisknop op de naam of het nummer klikt dat overeenkomt met een [!DNL Boolean] bewerking, ziet u de [!DNL Add new sibling] menuoptie. Een verwant is een andere voorwaarde op dezelfde relatieve positie in de voorwaardenhiërarchie als de [!DNL Boolean] bewerking waarop u met de rechtermuisknop hebt geklikt. Een nieuw item op hetzelfde niveau toevoegen voor een [!DNL Boolean] bewerking is hetzelfde als het toevoegen van een nieuwe voorwaarde door met de rechtermuisknop op de [!DNL Condition] of [!DNL Log Entry Condition] parameter.

**Een onderliggende voorwaarde verwijderen uit een Booleaanse bewerking:**

1. Klik met de rechtermuisknop op de naam van de onderliggende voorwaarde of op het nummer dat overeenkomt met de onderliggende voorwaarde die u uit de voorwaarde wilt verwijderen [!DNL Boolean] bewerking.
1. Klikken **[!UICONTROL Remove]** &lt;* **[!UICONTROL #number]***>, waarbij het getal het nummer is dat overeenkomt met de onderliggende voorwaarde die u wilt verwijderen.

In deze sectie worden de volgende voorwaarden besproken:

* [en](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a14dba4b07cc4ab9aeb20868f773db7c)
* [Geen](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-7e48b61266aa43ecbc48b979bf5e939b)
* [of](../../../../home/c-dataset-const-proc/c-conditions/c-test-ops/c-boolean-ops.md#section-a3aa0f56b6234f2680fa81939228326b)

## en {#section-a14dba4b07cc4ab9aeb20868f773db7c}

De [!DNL And] De voorwaarde kan nul of meer kindvoorwaarden hebben en keert waar terug wanneer geen van zijn kindknopen vals terugkeren.

De [!DNL And] De voorwaarde vormt de wortelverrichting van al voorwaarde het testen binnen de server van de gegevenswerkbank. Als de [!DNL And] voorwaarde bevat geen kinderen, evalueert de voorwaarde aan waar en de bijbehorende verrichting gaat te werk. Daarom hebben acties die alleen [!DNL And] De voorwaarde als voorwaardetest voert altijd uit en waarom het als wortel voor alle voorwaardetests wordt gebruikt.

In dit voorbeeld wordt getoond hoe een [!DNL And] voorwaarde wordt gebruikt om ervoor te zorgen dat [!DNL Copy] er vindt een transformatie plaats wanneer alleen de datum van de logbestandvermelding in het jaar 2006 plaatsvond en de gevraagde pagina [!DNL /products/purchase.asp].

![](assets/cfg_Condition_AndCondition.png)

## Geen {#section-7e48b61266aa43ecbc48b979bf5e939b}

De [!DNL Neither] De voorwaarde kan nul of meer kindvoorwaarden hebben en keert vals terug als om het even welk van zijn kindvoorwaarden aan waar evalueren. Als de [!DNL Neither] voorwaarde bevat geen kinderen, geen van zijn kinderen kan waar terugkeren. Als gevolg hiervan [!DNL Neither] condition levert true op.

In het volgende voorbeeld wordt een [!DNL Neither] voorwaarde met twee [!DNL Range] de toestand van de kinderen. Zoals gedefinieerd, wordt de [!DNL Neither] De voorwaarde sluit logitems uit die zich tussen 1 januari 2007 en 10 januari 2007 of in de periode van 12 januari 2007 tot 14 januari 2007 hebben voorgedaan. Een dergelijke voorwaarde kan worden gebruikt als de [!DNL Log Entry Condition] om transacties uit een gegevensset te verwijderen tijdens perioden waarin zich een bekend probleem met de verzamelde gegevens heeft voorgedaan.

![](assets/cfg_Condition_NeitherCondition.png)

## of {#section-a3aa0f56b6234f2680fa81939228326b}

De [!DNL Or] De voorwaarde kan nul of meer kindvoorwaarden hebben en keert waar terug als minstens één van zijn kindvoorwaarden aan waar evalueert. Als de [!DNL Or] voorwaarde bevat geen kinderen, geen van zijn kinderen kan waar terugkeren. Als gevolg hiervan [!DNL Or] voorwaarde levert false op.

In dit voorbeeld wordt het [!DNL Or] voorwaarde met een [!DNL String Match] voorwaarde en [!DNL Range] staat als de onderliggende. De [!DNL Or] alleen aan de voorwaarde wordt voldaan als de logbestandvermelding de [!DNL x-hasproblem] waarde ingesteld op ja of de logbestandvermelding is opgetreden in het tijdsbereik van 1 januari 2007 tot 10 januari 2007.

![](assets/cfg_Condition_OrCondition.png)

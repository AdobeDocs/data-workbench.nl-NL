---
description: De werkbank voor gegevens ondersteunt nu de IME (Input Method Editor) als secundair tekstinvoerproces voor internationale talen.
title: De Invoermethode-editor installeren
uuid: 2a4dc6de-9dd7-4280-b410-fb88a135fe45
exl-id: 3fcc58f5-29a9-427e-831a-44d527614b56
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# De Invoermethode-editor installeren{#installing-the-input-method-editor}

{{eol}}

De werkbank voor gegevens ondersteunt nu de IME (Input Method Editor) als secundair tekstinvoerproces voor internationale talen.

Met IME&#39;s kunt u internationale tekens invoeren met behulp van verschillende methoden die geschikt zijn voor uw lokale taal. De werkbank Gegevens biedt een invoerdialoogvenster waarin u de gewenste IME voor tekstvelden kunt openen en gebruiken.

>[!NOTE]
>
>Voor de gegevenswerkbank 6.1-release wordt alleen het virtuele vereenvoudigde Chinese toetsenbord ondersteund. Het invoeren van andere talen via de IME kan leiden tot onverwacht gedrag.

## Een IME gebruiken {#section-5f008d75a7b24119ab6aebc55454f927}

De functie voor het invoeren van zwevende IME-tekst gebruiken:

1. Klikken **[!UICONTROL Alt + Space]** voor een tekstinvoergebied.
1. Voer waarden in met behulp van de IME van uw systeem.
1. Sluit het dialoogvenster voor invoer door het **[!UICONTROL Enter]** of op de toets **[!UICONTROL OK]** knop.

   Het dialoogvenster verdwijnt en de tekens verschijnen in het geselecteerde veld.

**Het bestand Insight.cfg bijwerken**

Als u de IME wilt gebruiken, moet u de [!DNL Insight.cfg] bestand met deze instelling:

```
Localized IME = bool: true
```

Als deze instelling niet bestaat in het configuratiebestand, drukt u op **[!UICONTROL Alt + Space]** zal de IME-functie niet inschakelen.

**Inzicht starten in een andere taal:** Voor een betere ondersteuning van gelokaliseerde elementen, zoals een welkomstscherm, en voor de ondersteuning van meerdere talen in de toekomst, zijn in de werkbank voor gegevens opdrachtregelargumenten vereist waarmee de te laden taal wordt geïdentificeerd. De standaardtaal is Engels.

Voor het starten van een gegevenswerkbank in het Chinees moet u een oproep doen [!DNL Insight.exe] met het argument &quot;-zh-cn&quot;:

```
Insight.exe -zh-cn
```

(Deze opdrachtregelargumenten zijn niet hoofdlettergevoelig.)

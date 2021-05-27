---
description: De werkbank voor gegevens ondersteunt nu de IME (Input Method Editor) als secundair tekstinvoerproces voor internationale talen.
title: De Invoermethode-editor installeren
uuid: 2a4dc6de-9dd7-4280-b410-fb88a135fe45
exl-id: 3fcc58f5-29a9-427e-831a-44d527614b56,0bdc7d95-b49a-4ca5-9fde-9c1ce2cd14ec,e4e1c016-0544-434a-b82e-fdd2a4af316c
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# De Invoermethode-editor installeren{#installing-the-input-method-editor}

De werkbank voor gegevens ondersteunt nu de IME (Input Method Editor) als secundair tekstinvoerproces voor internationale talen.

Met IME&#39;s kunt u internationale tekens invoeren met behulp van verschillende methoden die geschikt zijn voor uw lokale taal. De werkbank Gegevens biedt een invoerdialoogvenster waarin u de gewenste IME voor tekstvelden kunt openen en gebruiken.

>[!NOTE]
>
>Voor de gegevenswerkbank 6.1-release wordt alleen het virtuele vereenvoudigde Chinese toetsenbord ondersteund. Het invoeren van andere talen via de IME kan leiden tot onverwacht gedrag.

## IME {#section-5f008d75a7b24119ab6aebc55454f927} gebruiken

De functie voor het invoeren van zwevende IME-tekst gebruiken:

1. Klik **[!UICONTROL Alt + Space]** voor om het even welk gebied van de tekstinput.
1. Voer waarden in met behulp van de IME van uw systeem.
1. Sluit het invoerdialoogvenster door de **[!UICONTROL Enter]**-toets te selecteren of op de **[!UICONTROL OK]**-knop te klikken.

   Het dialoogvenster verdwijnt en de tekens verschijnen in het geselecteerde veld.

**Het bestand Insight.cfg bijwerken**

Als u de IME wilt gebruiken, moet u het [!DNL Insight.cfg]-bestand met deze instelling bijwerken:

```
Localized IME = bool: true
```

Als deze instelling niet bestaat in het configuratiebestand en u op **[!UICONTROL Alt + Space]** drukt, wordt de IME-functie niet geactiveerd.

**Beginnend Inzicht in een andere taal:** om gelokaliseerde activa zoals een splash scherm beter te steunen en veelvoudige talen in de toekomst te steunen, vereist de werkbank van gegevens bevel-lijn argumenten die de te laden taal identificeren. De standaardtaal is Engels.

Voor het starten van een gegevenswerkbank in het Chinees moet u [!DNL Insight.exe] aanroepen met het argument &quot;-zh-cn&quot;:

```
Insight.exe -zh-cn
```

(Deze opdrachtregelargumenten zijn niet hoofdlettergevoelig.)

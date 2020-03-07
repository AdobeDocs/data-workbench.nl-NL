---
description: De werkbank van gegevens steunt nu de Redacteur van de Methode van de Input (IME) als secundair proces van de tekstingang voor internationale talen.
solution: Analytics
title: Het installeren van de Redacteur van de Methode van de Input
topic: Data workbench
uuid: 2a4dc6de-9dd7-4280-b410-fb88a135fe45
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het installeren van de Redacteur van de Methode van de Input{#installing-the-input-method-editor}

De werkbank van gegevens steunt nu de Redacteur van de Methode van de Input (IME) als secundair proces van de tekstingang voor internationale talen.

IMEs staat u toe om internationale karakters in te gaan gebruikend een verscheidenheid van methodes die voor uw lokale taal worden aangepast. De werkbank van gegevens verstrekt een vakje van de inputdialoog dat u toestaat om uw gewenste IME voor tekstgebieden te openen en te gebruiken.

>[!NOTE]
>
>Voor de 6.1-release van de gegevenswerkbank wordt alleen het virtuele vereenvoudigde Chinese toetsenbord ondersteund. Het invoeren van andere talen door IME zou in onverwacht gedrag kunnen resulteren.

## Een IME gebruiken {#section-5f008d75a7b24119ab6aebc55454f927}

Om de drijvende IME eigenschap van de tekstinput te gebruiken:

1. Klik **[!UICONTROL Alt + Space]** voor om het even welk gebied van de tekstinput.
1. Ga waarden in gebruikend IME van uw systeem.
1. Sluit de invoerdialoog door de **[!UICONTROL Enter]** sleutel te selecteren of de **[!UICONTROL OK]** knoop te klikken.

   De dialoog zal verdwijnen en de karakters zullen dan op het geselecteerde gebied verschijnen.

**Het bijwerken van het dossier Insight.cfg**

Om IME aan te wenden, moet u het [!DNL Insight.cfg] dossier met dit het plaatsen bijwerken:

```
Localized IME = bool: true
```

Als dit het plaatsen niet in het configuratiedossier bestaat, dan zal het drukken niet de eigenschap IME in dienst nemen. **[!UICONTROL Alt + Space]**

**Inzicht starten in een andere taal:** Om gelokaliseerde activa zoals een welkomstscherm beter te steunen en veelvoudige talen in de toekomst te steunen, vereist de gegevenswerkbank bevel-lijn argumenten die de te laden taal identificeren. De standaardtaal is Engels.

De beginnende gegevenswerkbank in het Chinees vereist u om [!DNL Insight.exe] met het &quot;-zh-cn&quot;argument aan te halen:

```
Insight.exe -zh-cn
```

(Deze argumenten van de bevellijn zijn niet gevoelig geval.)

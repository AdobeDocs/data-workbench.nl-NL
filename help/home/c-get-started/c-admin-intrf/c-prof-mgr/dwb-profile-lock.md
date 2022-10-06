---
description: Het bestand Internal.cfg dat in Profielbeheer wordt toegepast, voorkomt dat gebruikers uw aangepaste profielen wijzigen met de managers Profiel, Dimension, Rapporten, Werkruimten, Metriek en Filters.
title: Profielen vergrendelen in het werkstation
uuid: 6b65d7c1-dade-4c6e-9d59-09693e62f3f5
exl-id: 2604ceea-0e55-4ae7-a286-e5257e974a64
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Profielen vergrendelen in het werkstation{#locking-profiles-in-the-workstation}

{{eol}}

Het bestand Internal.cfg dat in Profielbeheer wordt toegepast, voorkomt dat gebruikers uw aangepaste profielen wijzigen met de managers Profiel, Dimension, Rapporten, Werkruimten, Metriek en Filters.

U kunt voorkomen dat profielbestanden worden gewijzigd en overschreven wanneer u de beheerprogramma&#39;s gebruikt door de **[!DNL Internal.cfg]** naar uw aangepaste profiel in Profielbeheer. Met dit configuratiebestand wordt voorkomen dat gebruikers meerdere bestanden overschrijven wanneer ze in de beheerprogramma&#39;s werken (die via het **Beheer** > **Profiel** ).

**Profielen vergrendelen in Profielbeheer**

1. Klik met de rechtermuisknop in de werkruimte **Beheer** > **Profielbeheer**.

1. In de **Profielbeheer**, klikt u met de rechtermuisknop **[!DNL Context > Internal.cfg]** en **Lokaal maken**.

1. Klik met de rechtermuisknop op het vinkje in **Gebruiker** kolom en opslaan naar een `<custom profile>`.

![](assets/dwb_lock_profiles.png)

**Opmerking**: Alleen wijzigingen in profielbestanden door de beheerders zijn niet mogelijk bij het opslaan van het dialoogvenster **[!DNL Internal.cfg]** naar een aangepast profiel in Profielbeheer. U kunt werkruimten nog steeds vanaf de werkbalk op de server opslaan met de opdracht **Opslaan op server** gebruiken.

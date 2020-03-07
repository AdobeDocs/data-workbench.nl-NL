---
description: Het bestand Internal.cfg dat in Profielbeheer wordt toegepast, voorkomt wijzigingen door gebruikers in uw aangepaste profielen door de managers Profielen, Afmetingen, Rapporten, Werkruimten, Metriek en Filters.
title: Profielen vergrendelen in het werkstation
uuid: 6b65d7c1-dade-4c6e-9d59-09693e62f3f5
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Profielen vergrendelen in het werkstation{#locking-profiles-in-the-workstation}

Het bestand Internal.cfg dat in Profielbeheer wordt toegepast, voorkomt wijzigingen door gebruikers in uw aangepaste profielen door de managers Profielen, Afmetingen, Rapporten, Werkruimten, Metriek en Filters.

U kunt voorkomen dat profielbestanden worden gewijzigd en overschreven wanneer u de managers gebruikt door het **[!DNL Internal.cfg]** bestand op te slaan in uw aangepaste profiel in Profielbeheer. Dit configuratiedossier verhindert gebruikers veelvoudige dossiers te beschrijven wanneer het werken in de managers (die van **Admin** worden betreden > het menu van het **Profiel** ).

**Profielen vergrendelen in Profielbeheer**

1. In de werkruimte, klik **Admin** met de rechtermuisknop aan > **Profielbeheer**.

1. In de **Manager** van het Profiel, klik met de rechtermuisknop aan **[!DNL Context > Internal.cfg]** en **maak Lokaal**.

1. Klik controleteken in de kolom van de **Gebruiker** met de rechtermuisknop aan en bewaar aan een `<custom profile>`.

![](assets/dwb_lock_profiles.png)

**Opmerking**: Alleen wijzigingen in profielbestanden door de beheerders worden voorkomen wanneer u de bestanden opslaat **[!DNL Internal.cfg]** in een aangepast profiel in Profielbeheer. U kunt werkruimten aan de server van de werktop nog bewaren gebruikend **sparen aan server** bevel.

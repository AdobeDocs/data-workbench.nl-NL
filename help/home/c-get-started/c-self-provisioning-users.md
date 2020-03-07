---
description: Gebruik Werkstation om uw gebruikers van de Werkbank van Gegevens te beheren.
title: Zelfvoorziening van gebruikers
uuid: e3c10bc4-2fa0-4368-9952-e38a4794aee9
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Zelfvoorziening van gebruikers{#self-provisioning-of-users}

Gebruik Werkstation om uw gebruikers van de Werkbank van Gegevens te beheren.

U kunt Werkstation gebruiken om met de Server van de Werkbank van Gegevens te verbinden door opstelling het vereiste certificaat van Adobe. Dit certificaat verleent hulp in zowel SSL mededeling als vergunning om de vergunning gegeven middelen en de eigenschappen te gebruiken. In op certificaat-gebaseerde authentificatie, moet u veelvoudige certificaten verwerven en oprichten voor het gebruiken van het Werkstation op veelvoudige machines. Ook, worden de gebruikerslevering en de rechten beheerd door Adobe en u moet Adobe voor nieuwe certificaten of certificaatintrekking contacteren.

Beginnend in DWB 6.7, steunt het Werkstation gebruikersauthentificatie door gebruikersbenaming en wachtwoord.

Terwijl de op certificaat-gebaseerde authentificatie/vergunning nog voor uw opstelling zal werken, wordt het hoogst geadviseerd om aan de nieuwere op geloofsbrieven-gebaseerde authentificatie te migreren. In de nieuwere benadering, verifiëren uw gebruikers van het Werkstation zich door het Systeem van het Beheer van de Identiteit van Adobe (IMS). Alvorens zij het Werkstation kunnen gebruiken, moeten zij toegang tot de eigenschappen door de Console [](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html) Admin door de beheerder van de organisatie worden gegeven.

Het nieuwe authentificatie en gebruikersleveringsmodel helpt in:

* Self-provisioning van gebruikers en groepen via Admin Console. U moet geen Adobe contacteren om, vergunningsrechten voor gebruikers toe te voegen te verwijderen of te wijzigen.
* Toegang hebbend tot Werkstation van veelvoudige machines zonder de configuratiestaat te verliezen door het programma te openen gebruikend geloofsbrieven. Het lokale geheime voorgeheugen wordt geschrapt op logout, is het huidige profiel gesloten, en het profiel van de Configuratie wordt actief.

## Aan de slag

Alvorens u begint, contacteer Adobe om uw organisatie in de Console toe te voegen Admin. Afhankelijk van de diensten u hebt gekocht, zal Adobe voorziening de organisatie voor u. Bijvoorbeeld, kunnen de organisaties toegang tot de dienst van de Attributie hebben of Beta bouwt, of allebei. Zodra een organisatie wordt gevormd, kan de organisatiebeheerder gebruikers en groepen toevoegen. Zie Cloud-gebruikers en -producten [](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html) beheren in Experience Cloud voor meer informatie. De organisatiebeheerder kan gebruiksbeperkingen voor verschillende gebruikers afhankelijk van hun rollen ook vormen. Bijvoorbeeld, niet-pre-versiegebruikers hebben geen toegang tot Beta nodig bouwt.

Elke provisioned gebruiker die aan deze organisatie door de Console Admin wordt toegevoegd zal toegang hebben om de Werkbank van Gegevens te gebruiken. De sub-diensten kunnen slechts voor elke gebruiker afhankelijk van hun producttoegang worden toegelaten of worden onbruikbaar gemaakt. Wanneer een gebruiker van certificaat aan IMS wordt bevorderd, zullen alle lokale gegevens aan de nieuwe IMS gebruikersfolder worden gekopieerd.

>[!NOTE]
>
>Een zitting duurt 6 uur op Server en 23 uur op Cliënt tenzij het toegangsteken wordt verfrist. Wanneer het teken wordt verfrist, kunt u Cliënt gebruiken zonder opnieuw het programma te openen.

Minstens één Configuratie van het Niveau van het Product moet in Console Admin door de beheerder worden gecreeerd alvorens toegang tot om het even welke gebruiker te verlenen.

Het booleense **Gebruik IMS** van de vlag kan aan reserve [!DNL Insight.cfg] aan certificaatwijze worden toegevoegd. Voor informatie bij het vormen van het Toegangsbeheer voor gebruikers IMS, zie het [Bijwerken van het Dossier](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/install-servers/insight-server-dpu/c-updt-accss-ctrl-file.html)van het Toegangsbeheer.

## Conflictoplossing

Wanneer een gebruiker aan veelvoudige machines met de zelfde rekening IMS op het zelfde profiel het programma wordt geopend, en op off-line wijze op één van de machines is, `.conflict` kan een vorm vormen en een pop-up venster zal u informeren. Dit komt voor wanneer er een verschil in inhoud met om het even welke dossiers (werkruimten, afmetingen, filters, enz.) is gesynchroniseerd op beide machines in [!DNL User\Profile\] op server en cliënt. Er wordt een back-up gemaakt in het `.conflict` bestand en er gaan geen gegevens verloren. Een booleense vlag in [!DNL Insight.cfg] geeft u de capaciteit om dit conflict pop-up onbruikbaar te maken.

Vlag: Conflictmeldingen

Dit is van toepassing op werkruimten, metriek, afmeting, enz. in de Omslag van de Gebruiker.

---
description: Gebruik Workstation om de gebruikers van uw Data Workbench te beheren.
title: Zelfinrichting van gebruikers
uuid: e3c10bc4-2fa0-4368-9952-e38a4794aee9
exl-id: fba916bf-66a1-4b69-a1c0-cad5b27bbbba
source-git-commit: 232117a8cacaecf8e5d7fcaccc5290d6297947e5
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Zelfinrichting van gebruikers{#self-provisioning-of-users}

Gebruik Workstation om de gebruikers van uw Data Workbench te beheren.

U kunt Werkstation gebruiken om met de Server van de Data Workbench te verbinden door het vereiste certificaat van Adobe te plaatsen. Dit certificaat is een hulpmiddel bij zowel SSL-communicatie als bij het gebruik van de gelicentieerde bronnen en functies. In op certificaat-gebaseerde authentificatie, moet u veelvoudige certificaten voor het gebruiken van het Werkstation op veelvoudige machines verkrijgen en opstelling. Ook, worden de gebruikerslevering en de toestemmingen beheerd door Adobe en u moet Adobe voor nieuwe certificaten of certificaatintrekking contacteren.

Vanaf DWB 6.7 ondersteunt het werkstation gebruikersverificatie via gebruikersnaam en wachtwoord.

Terwijl de op certificaat-gebaseerde authentificatie/vergunning nog voor uw opstelling zal werken, wordt het hoogst geadviseerd om aan de nieuwere op geloofsbrieven-gebaseerde authentificatie te migreren. In de nieuwere benadering, verifiëren uw gebruikers van het Werkstation zich door het Systeem van Adobe Identity Management (IMS). Alvorens zij het Werkstation kunnen gebruiken, moeten zij toegang tot de eigenschappen door [Admin Console](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html) door de beheerder van de organisatie worden verleend.

Het nieuwe verificatie- en gebruikersinrichtingsmodel helpt bij:

* Zelf-levering van gebruikers en groepen door Admin Console. U hoeft geen contact op te nemen met Adobe om licentierechten voor gebruikers toe te voegen, te verwijderen of te wijzigen.
* Toegang tot Werkstation van veelvoudige machines zonder de configuratiestaat te verliezen door het programma te openen gebruikend geloofsbrieven. Het lokale cachegeheugen wordt verwijderd bij het afmelden, het huidige profiel wordt gesloten en het configuratieprofiel wordt actief.

## Aan de slag

Neem voordat u begint contact op met Adobe om uw organisatie in de Admin Console toe te voegen. Afhankelijk van de services die u hebt aangeschaft, zal Adobe u de organisatie ter beschikking stellen. Bijvoorbeeld, kunnen de organisaties toegang tot de dienst van de Attributie hebben of Beta bouwt, of allebei. Zodra een organisatie wordt gevormd, kan de organisatiebeheerder gebruikers en groepen toevoegen. Zie [Gebruikers en producten van Experience Cloud beheren](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html) in Experience Cloud voor meer informatie. De organisatiebeheerder kan gebruiksbeperkingen voor verschillende gebruikers afhankelijk van hun rollen ook vormen. Gebruikers die niet vooraf release ontvangen, hebben bijvoorbeeld geen toegang nodig tot de bètabuilds.

Elke provisioned gebruiker die aan deze organisatie door de Admin Console wordt toegevoegd zal toegang hebben om de Data Workbench te gebruiken. De subservices kunnen alleen voor elke gebruiker worden in- of uitgeschakeld, afhankelijk van de toegang tot het product. Wanneer een gebruiker van certificaat aan IMS wordt bevorderd, zullen alle lokale gegevens naar de nieuwe IMS gebruikersfolder worden gekopieerd.

>[!NOTE]
>
>Een sessie duurt 6 uur op de server en 23 uur op de client, tenzij het toegangstoken wordt vernieuwd. Wanneer het token is vernieuwd, kunt u Client gebruiken zonder u opnieuw aan te melden.

Ten minste één configuratie op productniveau moet door de beheerder in Admin Console worden gemaakt voordat gebruikers toegang kunnen krijgen.

De booleaanse markering **Gebruik IMS** kan aan [!DNL Insight.cfg] worden toegevoegd om aan fallback aan certificaatwijze. Voor informatie bij het vormen van Toegangsbeheer voor gebruikers IMS, zie [Bijwerken van het Dossier van het Toegangsbeheer](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/install-servers/insight-server-dpu/c-updt-accss-ctrl-file.html).

## Conflict oplossen

Wanneer een gebruiker op veelvoudige machines met de zelfde rekening IMS op het zelfde profiel wordt het programma geopend, en offline wijze op één van de machines is, kan een `.conflict` vormen en een pop-up venster zal u op de hoogte brengen. Dit gebeurt wanneer de inhoud van bestanden verschilt (werkruimten, afmetingen, filters, enz.) gesynchroniseerd op beide computers in [!DNL User\Profile\] op server en client. Er wordt een back-up gemaakt in het `.conflict`-bestand en er gaan geen gegevens verloren. Een booleaanse vlag in [!DNL Insight.cfg] geeft u de capaciteit om dit conflict pop-up onbruikbaar te maken.

Markering: Conflictmeldingen

Dit is van toepassing op werkruimten, metriek, dimensie, enz. in de map Gebruiker.

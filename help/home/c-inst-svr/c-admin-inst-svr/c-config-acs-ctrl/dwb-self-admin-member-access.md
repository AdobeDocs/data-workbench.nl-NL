---
description: De beheerders kunnen werkstationgebruikers de gedeeltelijke capaciteit geven om toegangsbeheer voor douanegroepen te beheren.
title: Gebruikersbeheer van toegang groepslid
uuid: c31128f9-1094-4337-9bf6-96401278df33
exl-id: 6d2a0f19-a33c-49f6-a470-c95d2c1532c7
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# Gebruikersbeheer van toegang groepslid{#user-administration-of-group-member-access}

{{eol}}

De beheerders kunnen werkstationgebruikers de gedeeltelijke capaciteit geven om toegangsbeheer voor douanegroepen te beheren.

**Zelf-beleid van de toegang van het groepslid** verleent rechten aan niet-beheerders om leden toe te voegen en te schrappen in een douanegroep. De beheerder maakt een **Gebruikerslijst** bestand en groepstoegang instellen in het dialoogvenster [Toegangsbeheer.cfg](https://experienceleague.adobe.com/docs/data-workbench/using/server-admin-install/admin-dwb-server/access-control/c-config-acs-ctrl.html) bestand voor de nieuwe groepsleden.

**Toegang tot de Servers Manager**

Het instellen van de **[!DNL User List]** en synchroniseren met de **[!DNL Communications.cfg]** bestand is voltooid in het dialoogvenster **Serverbeheer** werkruimte.

1. Klik op de knop **Beheer** tab > **Gegevensset en profiel** tab.

1. Open de **Serverbeheer** werkruimte.
1. Klikken met rechtermuisknop >*uw servernaam*> in het diagram en selecteer **Bestanden**.

   De serverbestanden worden geopend in een tabel met kolommen *Bestand*, *`<server name>`*, en *Temperatuur*.

1. **Lokaal maken** door met de rechtermuisknop in de serverkolom van een serverbestand te klikken (voor deze functie) **[!DNL Access Control]** en **[!DNL Components/Communications.cfg)]**.

   Er verschijnt een wit vinkje in het dialoogvenster **Temperatuur** kolom. U kunt deze bewerken in de map Temperatuur. Klik vervolgens met de rechtermuisknop op het vinkje en **Opslaan naar** de server. (Wordt rood wanneer deze wordt gesynchroniseerd met de server).

## Een bestand met de naam User List.cfg maken {#section-c25bcaf34f4546e6b8b65f5e7f69ac09}

De beheerder moet een **[!DNL User List.cfg]** in het **[!DNL Access Control]** map.

1. Klik met de rechtermuisknop** rij Toegangsbeheer** in de **Temperatuur** kolom en selecteer **Openen** > **Map**. ![](assets/6_4_workstation_groups_3.png)

   De map Access Control in het dialoogvenster **Temperatuur** map wordt weergegeven met één aanbieding **[!DNL Access Control.cfg]** bestand.

1. Nog een tekstbestand toevoegen aan deze map en deze een naam geven **[!DNL User List.cfg]** (naast de **[!DNL Access Control.cfg]**).

1. Voeg de volgende parameters toe aan de **[!DNL User List.cfg]** bestand.

Het gebruikerslijstbestand moet een vector bevatten van **AccessGroup** objecten en elk **AccessGroup** object moet een naam en een vector met tekenreeksen hebben, die **Leden**.

```
Access Control Groups = vector: 1 items 
  0 = AccessGroup:  
    Name = string: Group 1 
    Members = vector: 1 items 
      0 = string: CN:Joe User
```

U kunt dit vervolgens bewerken en toevoegen in de werkstationweergave van de **[!DNL User List.cfg]**bestand.

![](assets/6_4_workstation_groups_4.png)

Hier zijn de meest fundamentele parameters om aan toe te voegen **[!DNL User List.cfg]** bestand. De leden kunnen dan in de mening van het Werkstation worden toegevoegd.

```
Access Control Groups = vector: 1 items 
  0 = AccessGroup:  
    Name = string:  
    Members = vector: 0 items
```

>[!IMPORTANT]
>
>Zoals bij alle **[!DNL .cfg]** als u handmatig een bestand bewerkt, moet u de spaties gebruiken in plaats van de tabs en de witruimte en syntaxis zorgvuldig in acht nemen. Er is een fout opgetreden in dit bestand *Adobe Insight Server* om het bestand Gebruikerslijst te negeren.

De **Naam** veld in elk **Toegangsgroep** wordt verwezen binnen de [!DNL Access Control.cfg] bestand.

>[!NOTE]
>
>Alleen geldige leden met voorvoegsels van directoryservices, zoals **GN:** of **OU:** worden geaccepteerd en mogen geen jokerteken bevatten (&#42;).

## Het bestand Communications.cfg instellen {#section-9d6f05ba81c14f15be63e361533459e8}

Een beheerder laat deze eigenschap eerst toe door te openen **[!DNL Components]>[!DNL Communications.cfg]** bestand en een nieuwe sleutel met de naam toevoegen **[!DNL Access Control User List File]**. De tekenreekswaarde van deze sleutel is het pad waar dit nieuwe bestand zich bevindt.

1. Klik in de serverbestanden op **Componenten** en klik met de rechtermuisknop op het vinkje in de serverkolom. Klikken **Lokaal maken**.

   Er verschijnt een wit vinkje in het dialoogvenster **Temperatuur** kolom.

1. Klik met de rechtermuisknop op het vinkje in het dialoogvenster **Temperatuur** kolom en selecteer **Openen** > **in werkstation**.

1. In de **Communication.cfg** bestand, klik met de rechtermuisknop **component** en selecteert u **Aangepaste sleutel toevoegen.** ![](assets/6_4_workstation_groups.png)

1. Typ de **Naam** als *Gebruikerslijstbestand toegangsbeheer* en instellen **Van type** als *String*.

   >[!NOTE]
   >
   >U kunt het nieuwe lijstbestand niet maken als een pad. Om dit te verhelpen, moet u het dossier opslaan, het openen in een redacteur (Blocnote), en &quot;Koord&quot;veranderen in &quot;Weg&quot;:

   Voor:

   ```
   component = CommServer:  
     Access Control File = Path: Access Control\\Access Control.cfg 
     Access Control User List File =  
    <string>: Access Control\\User List.cfg
   ```

   Na:

   ```
   component = CommServer:  
     Access Control File = Path: Access Control\\Access Control.cfg 
     Access Control User List File =  
    <Path>: Access Control\\User List.cfg
   ```

1. Sla de **[!DNL Communications.cfg]** en (indien nodig) sla het bestand op de server op. Dit zal componenten in de server opnieuw beginnen om ervoor te zorgen u geen fouten hebt gemaakt die konden verhinderen **[!DNL Communications.cfg]** bestand wordt geparseerd.
1. Als uw systeem verwerkingsservers bevat, wijzigt u het configuratiebestand in het dialoogvenster **[!DNL Components for Processing Servers.cfg]** bestand.
1. Klikken met rechtermuisknop **[!DNL Communications.cfg]** en opslaan op de server.

De beheerder van de Data Workbench kan nu bevestigen dat de beoogde gebruiker(s) toegang heeft tot het bestand met de gebruikerslijst en de gebruikers in staat stelt de groep te beheren. De gebruiker(s) kunnen het bestand Gebruikerslijst openen, bewerken en zo nodig GN- of OU-leden toevoegen en verwijderen.

## Het bestand Access Control.cfg synchroniseren {#section-ca6da453dfb4432bb40b86ef15ede872}

De beheerder kan vervolgens de **[!DNL Access Control.cfg]** en voeg verwijzingen in naar de groep(en) die door de *Gebruikerslijst* bestand.

De verwijzingen naar de groep(en) moeten net als elk ander lid worden ingevoegd, maar met de volgende syntaxis:

```
$(Group Name)
```

Waar &quot;Groepsnaam&quot; overeenkomt met wat is gedefinieerd in het gebruikerslijstbestand, inclusief spaties. ![](assets/6_4_workstation_groups_2.png)

Op dit punt kan de beheerder van de Data Workbench bevestigen dat de uitgezochte groepsgebruikers toegang tot het dossier van de gebruikerslijst hebben. De geselecteerde gebruikers kunnen vervolgens het dialoogvenster **[!DNL User List.cfg]** bestand maken, bewerken en zo nodig CN- of OU-leden toevoegen en verwijderen.

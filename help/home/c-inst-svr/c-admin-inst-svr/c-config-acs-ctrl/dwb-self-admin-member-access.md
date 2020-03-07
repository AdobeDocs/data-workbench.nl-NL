---
description: De beheerders kunnen werkstationgebruikers de gedeeltelijke capaciteit geven om toegangsbeheer voor douanegroepen te beheren.
title: Gebruikersbeheer van Groepsledentoegang
uuid: c31128f9-1094-4337-9bf6-96401278df33
translation-type: tm+mt
source-git-commit: cb3ca4b3b993f5f04f6b6cee25850600ff3d8986

---


# Gebruikersbeheer van Groepsledentoegang{#user-administration-of-group-member-access}

De beheerders kunnen werkstationgebruikers de gedeeltelijke capaciteit geven om toegangsbeheer voor douanegroepen te beheren.

**Het zelf-beleid van de toegang** van het groepslid geeft rechten aan niet-beheerders om leden in een douanegroep toe te voegen en te schrappen. De beheerder leidt tot een dossier van de Lijst **van de** Gebruiker en plaatst - de groepstoegang in het dossier van [Access Control.cfg](https://docs.adobe.com/content/help/en/data-workbench/using/server-admin-install/admin-dwb-server/access-control/c-config-acs-ctrl.html) voor de nieuwe groepsleden.

**Toegang tot de Servers Manager**

De vestiging van het **[!DNL User List]** dossier en het synchroniseren van het met het **[!DNL Communications.cfg]** dossier wordt gedaan in de werkruimte van de Manager **van** Servers.

1. Klik op het tabblad **Beheerder** > **Dataset en Profiel** op het werkblad.

1. Open de **werkruimte van de Manager** van Servers.
1. Klik met de rechtermuisknop >*uw servernaam*> in het diagram en selecteer **Bestanden**.

   De serverdossiers zullen in een lijst met kolommen *Dossier*, *`<server name>`*, en *Temp* openen.

1. **Maak Lokaal** door in de serverkolom van een serverdossier met de rechtermuisknop aan te klikken (voor deze eigenschap **[!DNL Access Control]** en **[!DNL Components/Communications.cfg)]**.

   Een wit vinkje zal in de kolom van **Temperatuur** verschijnen. U kunt in de omslag van Temperaturen uitgeven. Klik vervolgens met de rechtermuisknop op het vinkje en **sla op de server op** . (Het wordt rood wanneer samengevoegd met server).

## Creeer een dossier van de Gebruiker List.cfg {#section-c25bcaf34f4546e6b8b65f5e7f69ac09}

De beheerder moet een **[!DNL User List.cfg]** dossier in de **[!DNL Access Control]** omslag tot stand brengen.

1. Klik met de rechtermuisknop op de rij toegangsbeheer*** in de kolom **Temp** en selecteer **Openen** > **Map**. ![](assets/6_4_workstation_groups_3.png)

   De omslag van het Toegangsbeheer in de omslag van **Temperaturen** zal een lijst van één enkel **[!DNL Access Control.cfg]** dossier openen.

1. Voeg een ander tekstdossier aan deze omslag toe en noem het **[!DNL User List.cfg]** (naast **[!DNL Access Control.cfg]**).

1. Voeg de volgende parameters aan het **[!DNL User List.cfg]** dossier toe.

Het dossier van de Lijst van de Gebruiker zou een vector van voorwerpen **AccessGroup** moeten bevatten, en elk voorwerp **AccessGroup** zou een naam en een vector van koorden moeten hebben genoemd **Leden**.

```
Access Control Groups = vector: 1 items 
  0 = AccessGroup:  
    Name = string: Group 1 
    Members = vector: 1 items 
      0 = string: CN:Joe User
```

U kunt gebruikers dit in de mening van het Werkstation van het **[!DNL User List.cfg]**dossier dan uitgeven en toevoegen.

![](assets/6_4_workstation_groups_4.png)

Hier zijn de meest fundamentele parameters om aan het **[!DNL User List.cfg]** dossier toe te voegen. De leden kunnen dan in de mening van het Werkstation worden toegevoegd.

```
Access Control Groups = vector: 1 items 
  0 = AccessGroup:  
    Name = string:  
    Members = vector: 0 items
```

>[!IMPORTANT]
>
>Zoals met om het even welk **[!DNL .cfg]** dossier dat u manueel uitgeeft, zorg ervoor om ruimten in plaats van lusjes te gebruiken en aandacht te besteden aan whitespace en de syntaxis. Een fout in dit dossier zal de Server *van het Inzicht van* Adobe veroorzaken om het dossier van de Lijst van de Gebruiker te negeren.

Het gebied van de **Naam** in elke Groep **van de** Toegang zal binnen het [!DNL Access Control.cfg] dossier van verwijzingen worden voorzien.

>[!NOTE]
>
>Slechts geldige leden met de prefixen van de folderdienst, zoals **CN:** of **OU:** worden goedgekeurd, en deze kunnen geen vervangingskarakter (*) bevatten.

## Opstelling het Communications.cfg- dossier {#section-9d6f05ba81c14f15be63e361533459e8}

Een beheerder laat eerst deze eigenschap door het **[!DNL Components]>[!DNL Communications.cfg]**- dossier te openen toe en een nieuwe sleutel met de naam toe te voegen **[!DNL Access Control User List File]**. De koordwaarde van deze sleutel is de weg waar dit nieuwe dossier zal worden gevestigd.

1. Van de serverdossiers, klik **Componenten** en klik het controleteken in de serverkolom met de rechtermuisknop aan. Klik **maken Lokaal**.

   Een wit vinkje zal in de kolom van **Temperatuur** verschijnen.

1. Klik het controleteken in de kolom van **Temperaturen** met de rechtermuisknop aan en selecteer **Open** > **in Werkstation**.

1. In het **Communication.cfg** - dossier, klik **component** met de rechtermuisknop aan en uitgezocht **voeg de Sleutel van de Douane toe.** ![](assets/6_4_workstation_groups.png)

1. Typ de **Naam** als Dossier *van de Lijst van de Gebruiker van het* Toegangsbeheer en reeks **van Type** als *Koord*.

   >[!NOTE]
   U kunt niet het nieuwe lijstdossier als Weg tot stand brengen. Om dit te verhelpen, moet u het dossier bewaren, het openen in een redacteur (Blocnote), en &quot;Koord&quot;veranderen in &quot;Weg&quot;:

   Vóór:

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

1. Sparen het **[!DNL Communications.cfg]** dossier en (indien nodig) bewaar het aan de server. Dit zal componenten in de server opnieuw beginnen om ervoor te zorgen u geen fouten hebt gemaakt die konden verhinderen het **[!DNL Communications.cfg]** dossier wordt ontleed.
1. Als uw systeem verwerkingsservers omvat, wijzig het configuratiedossier in het **[!DNL Components for Processing Servers.cfg]** dossier.
1. Klik met de rechtermuisknop **[!DNL Communications.cfg]** en sla deze op de server op.

De beheerder van de gegevenswerkbank kan nu bevestigen dat de beoogde gebruiker(s) toegang heeft (hebben) tot het bestand van de gebruikerslijst en de gebruikers toestaan de groep te beheren. De gebruiker(s) kan (kunnen) het bestand Gebruikerslijst openen, bewerken en zo nodig GN- of OU-leden toevoegen en verwijderen.

## Het Access Control.cfg-bestand synchroniseren {#section-ca6da453dfb4432bb40b86ef15ede872}

De beheerder kan vervolgens de verwijzingen naar de groep(en) die door het **[!DNL Access Control.cfg]** gebruikerslijstbestand *is (zijn) gedefinieerd, bewerken* en invoegen.

De verwijzingen naar de groep(en) moeten net als alle andere leden worden ingevoegd, maar met de volgende syntaxis:

```
$(Group Name)
```

Waar de &quot;Naam van de Groep&quot;aanpast wat in het dossier van de gebruikerslijst, met inbegrip van witte ruimten wordt bepaald. ![](assets/6_4_workstation_groups_2.png)

Op dit punt kan de beheerder van de Werkbank van Gegevens bevestigen dat de uitgezochte groepsgebruikers toegang tot het dossier van de gebruikerslijst hebben. De uitgezochte gebruikers kunnen het **[!DNL User List.cfg]** dossier dan openen, het uitgeven, en GN of OU leden toevoegen en verwijderen zoals nodig.

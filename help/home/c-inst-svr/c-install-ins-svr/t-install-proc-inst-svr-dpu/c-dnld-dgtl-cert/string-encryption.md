---
description: Codeer wachtwoorden en andere koorden wanneer het communiceren tussen de cliënt en de server.
title: String Encryption
uuid: b2ec6a10-136c-4694-a425-04dbb41d43d1
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# String Encryption{#string-encryption}

Codeer wachtwoorden en andere koorden wanneer het communiceren tussen de cliënt en de server.

Wanneer het communiceren tussen de cliënt van de Werkbank van Gegevens (werkstation) en server, kunt u een parameter van de Waarde (zoals een wachtwoord) met het Type van *EncryptedString* bewaren. Dit verbergt de parameter en bewaart het koord aan de Credentiële Opslag *van* Vensters op de server met de overeenkomstige teruggekeerde sleutel. Dit slaat hoofdzakelijk geloofsbrieven op die in uitvoer worden gebruikt maar kan worden gebruikt om het even welke parameter te coderen.

* Een nieuwe omslag werd toegevoegd bij Server \**EncryptStrings**.

   Dit is waar u het configuratiedossier plaatst om koorden te coderen.

* Een nieuw configuratiedossier werd toegevoegd in Server\Component\**EncryptedStrings.cfg**.

   ```
   component = EncryptionComponent:
     Path = Path: EncryptStrings\\*.cfg
   ```

   Dit dossier opinieert de omslag van de *Server*\*EncryptStrings* voor de dossiers van de encryptieconfiguratie.

**Om een koord** te coderen:

1. Creeer een **EncryptedStrings.cfg** - configuratiedossier voor een koord met deze reeks gebieden:

   ```
   Names = vector: 1 items
    0 = NameEncryptValuePair:
     EncryptValue = EncryptedString: // left empty as input then output will be filled by server
     Name = string: // Name for identifier 
     Value = string: // Value to be encrypted
   ```

   * *Waarde* - Dit gebied bevat het duidelijke tekstkoord dat moet worden gecodeerd.

      Dit is alleen servercodering. De *waarde* die wordt geplaatst wordt gecodeerd slechts op de servercomputer.

   * *Naam* - Dit gebied bevat een waarde die het gecodeerde koord identificeert.
   * *EncryptValue* - Dit gebied zal leeg in het dossier van de inputconfiguratie worden verlaten. De gecodeerde waarde zal op dit gebied zijn teruggekeerd.
   U kunt veelvoudige waarden **NameEncryptValuePair** voor verschillende gebieden voor encryptie toevoegen.

   >[!NOTE]
   >
   >Alle lege gebieden van de Waarde zullen worden verwijderd.

1. Sla het bestand **EncryptedStrings.cfg** op in de map Server\**EncryptStrings**.

**Uitvoerbestand**

Een outputdossier zal met de zelfde naam worden geproduceerd zoals het inputdossier met &lt;*filename*>.*gecodeerde* uitbreiding. Bijvoorbeeld, als het inputdossier *sample.cfg* wordt genoemd dan zal het outputdossier *sample.cfg.encrypted* worden genoemd.

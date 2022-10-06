---
description: Codeer wachtwoorden en andere koorden wanneer het communiceren tussen de cliënt en de server.
title: String Encryption
uuid: b2ec6a10-136c-4694-a425-04dbb41d43d1
exl-id: 43696ff1-3153-4d85-b9a9-c2752dd2c29a
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# String Encryption{#string-encryption}

{{eol}}

Codeer wachtwoorden en andere koorden wanneer het communiceren tussen de cliënt en de server.

Wanneer het communiceren tussen de cliënt van de Data Workbench (werkstation) en de server, kunt u een parameter van de Waarde (zoals een wachtwoord) met het Type van opslaan *EncryptedString*. Hierdoor wordt de parameter verborgen en wordt de tekenreeks opgeslagen in de *Windows Credential Store* op de server met de corresponderende geretourneerde sleutel. Dit slaat hoofdzakelijk geloofsbrieven op die in uitvoer worden gebruikt maar kan worden gebruikt om het even welke parameter te coderen.

* Een nieuwe map is toegevoegd op de server\**EncryptStrings**.

   Hier stelt u het configuratiebestand zo in dat tekenreeksen worden gecodeerd.

* Een nieuw configuratiebestand is toegevoegd op de server\Component\**EncryptedStrings.cfg**.

   ```
   component = EncryptionComponent:
     Path = Path: EncryptStrings\\*.cfg
   ```

   Dit bestand pollt de *Server*\*EncryptStrings* omslag voor de dossiers van de encryptieconfiguratie.

**Een tekenreeks coderen**:

1. Een **EncryptedStrings.cfg** configuratiebestand voor een tekenreeks met deze velden ingesteld:

   ```
   Names = vector: 1 items
    0 = NameEncryptValuePair:
     EncryptValue = EncryptedString: // left empty as input then output will be filled by server
     Name = string: // Name for identifier 
     Value = string: // Value to be encrypted
   ```

   * *Waarde* - Dit veld bevat de tekenreeks zonder opmaak die moet worden gecodeerd.

      Dit is alleen servercodering. De *Waarde* instelling wordt alleen op de servercomputer gecodeerd.

   * *Naam* - Dit veld bevat een waarde die de gecodeerde tekenreeks identificeert.
   * *EncryptValue* - Dit veld blijft leeg in het invoerconfiguratiebestand. De gecodeerde waarde wordt in dit veld geretourneerd.

   U kunt meerdere **NameEncryptValuePair** waarden voor verschillende velden voor versleuteling.

   >[!NOTE]
   >
   >Alle lege waardevelden worden verwijderd.

1. Sla de **EncryptedStrings.cfg** bestand naar de server\**EncryptStrings** map.

**Uitvoerbestand**

Er wordt een uitvoerbestand gegenereerd met dezelfde naam als het invoerbestand met een &lt;*filename*>.*gecodeerd* extensie. Als het invoerbestand bijvoorbeeld een naam heeft *sample.cfg* dan krijgt het uitvoerbestand een naam *sample.cfg.encrypted*.

---
description: Tijdens opwerking, reconstrueert de server van de gegevenswerkbank uw dataset aangezien u in de dossiers van de Configuratie van de Dataset van de Verwerking en van de Transformatie van het Logboek hebt gespecificeerd.
solution: Analytics
title: Inzicht in opwerking en heromzetting
topic: Data workbench
uuid: 0253bc8c-8883-41eb-8a9f-e0685613ff5c
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Inzicht in opwerking en heromzetting{#understanding-reprocessing-and-retransformation}

Tijdens opwerking, reconstrueert de server van de gegevenswerkbank uw dataset aangezien u in de dossiers van de Configuratie van de Dataset van de Verwerking en van de Transformatie van het Logboek hebt gespecificeerd.

Om dit te doen, moet de server van de gegevenswerkbank (InsightServer64.exe) zowel de fase van de logboekverwerking als de transformatiefase van datasetconstructie voltooien. Wanneer de logboekverwerking eindigt, brengt het transformatie teweeg om automatisch voor te komen, maar de transformatie kan ook onafhankelijk van logboekverwerking voorkomen.

Tijdens de fase van de logboekverwerking, hebben de gebruikers van de gegevenswerkbank geen toegang tot de gegevens in de dataset. Tijdens de transformatiefase, hebben de gebruikers van de gegevenswerkbank toegang tot bijgewerkte gegevens, maar de gegevens worden bemonsterd in plaats van volledig. De analyse van gegevens kan tijdens transformatie verdergaan, maar de vragen zullen slechts zo snel voltooien aangezien de transformatie voorkomt.

## Opwerking {#section-92f1e46bf1534b3dba39e9493190b8ab}

Telkens als u één van de volgende taken, logboekverwerking, en daarom transformatie voltooit, komt automatisch voor om uw dataset te reconstrueren aangezien u in de dossiers van de datasetconfiguratie hebt gespecificeerd:

* Voeg een nieuwe gegevensbron toe.
* Voeg een nieuwe server van de gegevenswerkbank aan uw cluster in het [!DNL Profile.cfg] dossier toe.
* Wijzig het [!DNL Cluster.cfg] bestand.
* Verander het [!DNL Log Processing.cfg] dossier of een [!DNL Log Processing Dataset Include] dossier, met inbegrip van maar niet beperkt tot het volgende:

   * Een nieuwe parameter toevoegen
   * Een transformatie wijzigen
   * Verander de parameters van de Tijd van het Begin of van de Tijd van het Eind

* Upgrade uw [!DNL Insight Server.exe] bestand.

U kunt ook opwerking op elk ogenblik in werking stellen door om het even welk karakter of combinatie karakters in de Reprocess parameter van het [!DNL Log Processing.cfg] dossier in te gaan en het dossier op te slaan.

>[!NOTE]
>
>Voor opwerking om voor te komen, moet de parameter van de Pauze in het [!DNL Log Processing Mode.cfg] dossier aan vals worden geplaatst. De standaardwaarde van deze parameter is vals, zodat kan het veranderen van de parameter niet worden vereist. Voor meer informatie over [!DNL Log Processing Mode.cfg], zie de [Extra Dossiers](/help/home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md)van de Configuratie.

## Hervorming {#section-02446744549940ada8eba0573ec5575f}

Telkens als u om het even welke informatie in het [!DNL Transformation.cfg] dossier of in een [!DNL Transformation Dataset Include] dossier, zoals verandering een transformatie verandert of een nieuwe afmeting bepaalt, komt de transformatie automatisch voor.

Telkens als u raadplegingsdossiers verandert die in het [!DNL Transformation.cfg] dossier of in een [!DNL Transformation Dataset Include] dossier van verwijzingen worden voorzien (met inbegrip van raadplegingsdossiers voor [!DNL Categorize], [!DNL FlatFileLookup], en [!DNL ODBCLookup] transformaties), moet u transformatie in werking stellen door om het even welk karakter of combinatie karakters in de parameter van het Herproces van het [!DNL Transformation.cfg] dossier in te gaan en het dossier te bewaren.

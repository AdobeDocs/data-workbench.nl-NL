---
description: Tijdens het opnieuw verwerken, reconstrueert de server van de gegevenswerkbank uw dataset zoals u in de dossiers van de Configuratie van de Dataset van de Verwerking van het Logboek en van de Transformatie hebt gespecificeerd.
title: Inzicht in opwerking en heromzetting
uuid: 0253bc8c-8883-41eb-8a9f-e0685613ff5c
exl-id: 12c69935-a981-492c-9124-71f6f06ff77b
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Inzicht in opwerking en wederomzetting{#understanding-reprocessing-and-retransformation}

Tijdens het opnieuw verwerken, reconstrueert de server van de gegevenswerkbank uw dataset zoals u in de dossiers van de Configuratie van de Dataset van de Verwerking van het Logboek en van de Transformatie hebt gespecificeerd.

Om dit te doen, moet de server van de gegevenswerkbank (InsightServer64.exe) zowel de fase van de logboekverwerking als de transformatiefase van datasetbouw voltooien. Wanneer de logboekverwerking eindigt, teweegbrengt het transformatie automatisch voor te komen, maar de transformatie kan ook onafhankelijk van logboekverwerking voorkomen.

Tijdens de fase van de logboekverwerking, hebben de gebruikers van de gegevenswerkbank geen toegang tot de gegevens in de dataset. Tijdens de transformatiefase hebben de gebruikers van de gegevenswerkbank wel toegang tot actuele gegevens, maar worden de gegevens gesampled in plaats van voltooid. De analyse van gegevens kan tijdens transformatie verdergaan, maar de vragen zullen slechts zo snel voltooien aangezien de transformatie voorkomt.

## Opwerking {#section-92f1e46bf1534b3dba39e9493190b8ab}

Telkens als u één van de volgende taken voltooit, logboekverwerking, en daarom transformatie, komt automatisch voor om uw dataset te reconstrueren zoals u in de dossiers van de datasetconfiguratie hebt gespecificeerd:

* Voeg een nieuwe gegevensbron toe.
* Voeg een nieuwe server van de gegevenswerkbank aan uw cluster in het [!DNL Profile.cfg] dossier toe.
* Wijzig het bestand [!DNL Cluster.cfg].
* Wijzig het [!DNL Log Processing.cfg]-bestand of een [!DNL Log Processing Dataset Include]-bestand, inclusief maar niet beperkt tot het volgende:

   * Een nieuwe parameter toevoegen
   * Een transformatie wijzigen
   * De parameters Begintijd of Eindtijd wijzigen

* Voer een upgrade uit op uw [!DNL Insight Server.exe]-bestand.

U kunt de opwerking ook op elk gewenst moment starten door een willekeurig teken of een willekeurige combinatie van tekens in te voeren in de parameter Opnieuw verwerken van het bestand [!DNL Log Processing.cfg] en het bestand op te slaan.

>[!NOTE]
>
>Opwerking is alleen mogelijk als de parameter Pauze in het bestand [!DNL Log Processing Mode.cfg] is ingesteld op false. De standaardwaarde van deze parameter is false, dus het wijzigen van de parameter is mogelijk niet vereist. Voor meer informatie over [!DNL Log Processing Mode.cfg], zie [Extra Dossiers van de Configuratie](/help/home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md).

## Hertransformatie {#section-02446744549940ada8eba0573ec5575f}

Telkens wanneer u informatie wijzigt in het [!DNL Transformation.cfg]-bestand of in een [!DNL Transformation Dataset Include]-bestand, zoals een transformatie wijzigen of een nieuwe dimensie definiëren, vindt de transformatie automatisch plaats.

Elke keer dat u opzoekbestanden wijzigt waarnaar wordt verwezen in het [!DNL Transformation.cfg]-bestand of in een [!DNL Transformation Dataset Include]-bestand (inclusief opzoekbestanden voor [!DNL Categorize]-, [!DNL FlatFileLookup]- en [!DNL ODBCLookup]-transformaties), moet u de transformatie starten door een teken of combinatie van tekens in de parameter Opnieuw verwerken van het [!DNL Transformation.cfg]-bestand in te voeren en het bestand op te slaan.

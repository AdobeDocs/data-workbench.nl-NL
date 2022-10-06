---
description: Tijdens het opnieuw verwerken, reconstrueert de server van de gegevenswerkbank uw dataset zoals u in de dossiers van de Configuratie van de Dataset van de Verwerking van het Logboek en van de Transformatie hebt gespecificeerd.
title: Inzicht in opwerking en heromzetting
uuid: 0253bc8c-8883-41eb-8a9f-e0685613ff5c
exl-id: 12c69935-a981-492c-9124-71f6f06ff77b
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Inzicht in opwerking en heromzetting{#understanding-reprocessing-and-retransformation}

{{eol}}

Tijdens het opnieuw verwerken, reconstrueert de server van de gegevenswerkbank uw dataset zoals u in de dossiers van de Configuratie van de Dataset van de Verwerking van het Logboek en van de Transformatie hebt gespecificeerd.

Om dit te doen, moet de server van de gegevenswerkbank (InsightServer64.exe) zowel de fase van de logboekverwerking als de transformatiefase van datasetbouw voltooien. Wanneer de logboekverwerking eindigt, teweegbrengt het transformatie automatisch voor te komen, maar de transformatie kan ook onafhankelijk van logboekverwerking voorkomen.

Tijdens de fase van de logboekverwerking, hebben de gebruikers van de gegevenswerkbank geen toegang tot de gegevens in de dataset. Tijdens de transformatiefase hebben de gebruikers van de gegevenswerkbank wel toegang tot actuele gegevens, maar worden de gegevens gesampled in plaats van voltooid. De analyse van gegevens kan tijdens transformatie verdergaan, maar de vragen zullen slechts zo snel voltooien aangezien de transformatie voorkomt.

## Opwerking {#section-92f1e46bf1534b3dba39e9493190b8ab}

Telkens als u één van de volgende taken voltooit, logboekverwerking, en daarom transformatie, komt automatisch voor om uw dataset te reconstrueren zoals u in de dossiers van de datasetconfiguratie hebt gespecificeerd:

* Voeg een nieuwe gegevensbron toe.
* Voeg een nieuwe gegevenswerkbankserver toe aan uw cluster in de [!DNL Profile.cfg] bestand.
* Wijzig de [!DNL Cluster.cfg] bestand.
* Wijzig de [!DNL Log Processing.cfg] of een [!DNL Log Processing Dataset Include] bestand, met inbegrip van, maar niet beperkt tot:

   * Een nieuwe parameter toevoegen
   * Een transformatie wijzigen
   * De parameters Begintijd of Eindtijd wijzigen

* Upgrade uw [!DNL Insight Server.exe] bestand.

U kunt de opwerking ook op elk gewenst moment starten door een willekeurig teken of een willekeurige combinatie van tekens in te voeren in de parameter Opnieuw verwerken van het dialoogvenster [!DNL Log Processing.cfg] en het bestand opslaan.

>[!NOTE]
>
>Voor opwerking, de parameter van de Pauze in [!DNL Log Processing Mode.cfg] bestand moet op false worden ingesteld. De standaardwaarde van deze parameter is false, dus het wijzigen van de parameter is mogelijk niet vereist. Meer informatie over [!DNL Log Processing Mode.cfg], zie [Aanvullende configuratiebestanden](/help/home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md).

## Hertransformatie {#section-02446744549940ada8eba0573ec5575f}

Elke keer dat u gegevens wijzigt in het dialoogvenster [!DNL Transformation.cfg] of in een [!DNL Transformation Dataset Include] transformatie wordt automatisch uitgevoerd, bijvoorbeeld wanneer u een transformatie wijzigt of een nieuwe dimensie definieert.

Elke keer dat u opzoekbestanden wijzigt waarnaar wordt verwezen in het dialoogvenster [!DNL Transformation.cfg] of in een [!DNL Transformation Dataset Include] bestand (inclusief opzoekbestanden voor [!DNL Categorize], [!DNL FlatFileLookup], en [!DNL ODBCLookup] transformaties), moet u transformatie initiëren door een willekeurig teken of een willekeurige combinatie van tekens in te voeren in de parameter Opnieuw verwerken van het dialoogvenster [!DNL Transformation.cfg] en het bestand opslaan.

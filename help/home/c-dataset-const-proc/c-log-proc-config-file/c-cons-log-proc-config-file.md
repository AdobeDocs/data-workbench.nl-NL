---
description: Conceptuele informatie om te overwegen wanneer het uitgeven van het dossier van het Logboek Processing.cfg.
solution: Analytics
title: Overwegingen voor het dossier van de Configuratie van de Verwerking van het Logboek
topic: Data workbench
uuid: 2ccedf63-12d9-40e9-912a-aee030191b1e
translation-type: tm+mt
source-git-commit: 27600561841db3705f4eee6ff0aeb8890444bbc9

---


# Overwegingen voor het dossier van de Configuratie van de Verwerking van het Logboek{#considerations-for-the-log-processing-configuration-file}

Conceptuele informatie om te overwegen wanneer het uitgeven van het dossier van het Logboek Processing.cfg.

* De dossiers van gegevens zouden niet tussen folders moeten worden bewogen nadat de bronnen voor een dataset zijn bepaald. De enige extra bestanden die een directory zou moeten ontvangen, zijn pas gecreëerde bestanden die het resultaat zijn van de gegevenswerkbankserver die gegevens van de sensor(en) ontvangt.
* Het veranderen van om het even welke parameters in dit dossier vereist opwerking van alle gegevens. De parameter van de Pauze in het [!DNL Log Processing Mode.cfg] dossier moet aan vals worden geplaatst voor opwerking om voor te komen. (Merk op dat de standaardwaarde van deze parameter vals is, zodat kan het veranderen van de parameter niet worden vereist.) Voor informatie over het [!DNL Log Processing Mode.cfg] dossier, zie de [Extra Dossiers](../../../home/c-dataset-const-proc/c-add-config-files/c-add-config-files.md#concept-1afef4f88f1e467ab4326875fd1d3004)van de Configuratie.

* Als u de gegevens opnieuw verwerkt, kunt u de parameter van de Voortgang van de Verwerking van het Logboek in gegevenswerkbank controleren [!DNL Processing Legend].

   Voor informatie over het opnieuw verwerken van uw gegevens, zie [Verwerking en Herschikking](../../../home/c-dataset-const-proc/c-reproc-retrans/c-unst-reproc-retrans.md). Zie [Verwerkingslegger](../../../home/c-get-started/c-admin-intrf/c-pro-lgd.md#concept-233e27c9c84c426f8c178a27cc7ff828).

* Het [!DNL Log Processing.cfg] dossier kan door veelvoudige datasetprofielen worden gedeeld. De transformaties die in het [!DNL Log Processing.cfg] dossier worden bepaald worden toegepast op alle datasetprofielen die dit configuratiedossier delen.

   >[!NOTE]
   >
   >Adobe adviseert bepalende transformaties voor de logboekverwerking in één of meerdere [!DNL dataset include] dossiers van de logboekverwerking. Voor informatie, zie de Dataset van de Verwerking van het [Logboek omvatten Dossiers](../../../home/c-dataset-const-proc/c-dataset-inc-files/c-types-dataset-inc-files/c-log-proc-dataset-inc-files/c-log-proc-dataset-inc-files.md#concept-999475a22519432e98844622ca95b6ab).

* U kunt om het even welke hierboven beschreven parameters aan het [!DNL Log Processing.cfg] dossier toevoegen door het dossier in Blocnote te openen en uit te geven. Om het even welke veranderingen u aanbrengt en opslaat verschijnen wanneer u het dossier in gegevenswerkbank heropent. Wanneer het toevoegen van een nieuwe parameter, gebruik de Ruimtesleutel (niet de sleutel van het Lusje) om twee (2) ruimten rechts van het vorige rubriekniveau te kartelen.

   Om het even welke fouten die tijdens de fase van de logboekverwerking van het proces van de datasetconstructie voor een datasetprofiel voorkomen worden getoond in de [!DNL Profiles] knoop van de [!DNL Detailed Status] interface in gegevenswerkbank. Voor informatie over de [!DNL Detailed Status] interface, zie de Gids *van de Gebruiker van de Werkbank van* Gegevens.


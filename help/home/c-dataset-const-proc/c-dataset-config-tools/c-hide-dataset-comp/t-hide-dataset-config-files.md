---
description: Als u geen configuratiedossier van een intern of ander geërft profiel wilt erven (namelijk wilt u de instructies in het dossier worden genegeerd tijdens de aanleg van de dataset), maar u wilt niet het dossier wijzigen, kunt u een leeg (nul-byte) dossier met de zelfde naam tot stand brengen en het dossier in een ander profiel opslaan.
title: Gegevenssetconfiguratiebestanden verbergen
uuid: eb33cf54-e067-4af2-a10e-7ffe43910e4f
exl-id: 327847d1-421a-4ed1-9a5f-2491765a34bd
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Gegevenssetconfiguratiebestanden verbergen{#hiding-dataset-configuration-files}

{{eol}}

Als u geen configuratiedossier van een intern of ander geërft profiel wilt erven (namelijk wilt u de instructies in het dossier worden genegeerd tijdens de aanleg van de dataset), maar u wilt niet het dossier wijzigen, kunt u een leeg (nul-byte) dossier met de zelfde naam tot stand brengen en het dossier in een ander profiel opslaan.

**Aan nul-byte een dossier van de datasetconfiguratie**

1. In de [!DNL Profile Manager]Open de benodigde mappen en submappen om te zoeken naar het bestand dat u op nul-byte wilt instellen.
1. Klik met de rechtermuisknop op het vinkje naast de naam van het bestand en klik op **[!UICONTROL Make Local]**.
1. Open het lokale bestand in een teksteditor, zoals Kladblok, en verwijder de inhoud ervan.
1. Sla het bestand op en sluit het.
1. In de [!DNL Profile Manager], slaat u het bestand met een byte van nul op in een profiel rechts van het profiel waarin het oorspronkelijke bestand zich bevindt. (U wilt dat het bestand met een byte van nul voorrang heeft op het oorspronkelijke bestand.)

   In de [!DNL Profile Manager]Een koppelteken (-) in plaats van een vinkje geeft in een kolom het bestand met een lengte van nul bytes aan, zoals in het onderstaande voorbeeld wordt getoond.

   ![](assets/vis_ProfileManager_ZeroByteFile.png)

Wanneer u uw dataset opnieuw verwerkt, bevat de dataset niet de datasetcomponenten die het originele dossier bepaalt.

>[!NOTE]
>
>Als u nul-byte een configuratiedossier dat een uitgebreide afmeting bepaalt die in een visualisatie of een metrische definitie wordt gebruikt, produceert de werkbank van gegevens een fout voor die visualisatie of metrisch, respectievelijk.

U kunt ook bestanden met een nulbyte gebruiken om een metrische waarde, dimensie of filter naar een andere locatie in het profiel te verplaatsen of om menu-items te verbergen. Zie voor meer informatie de *Gebruikershandleiding voor Data Workbench*.

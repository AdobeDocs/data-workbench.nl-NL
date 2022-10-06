---
description: Data Workbench downloadt profielen naar uw computer.
title: Profielen
uuid: 8ea36138-9839-40e5-89e2-4b120f1dd7aa
exl-id: a140f549-448c-4e34-8eae-ad154fa01f1f
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Profielen{#profiles}

{{eol}}

Data Workbench downloadt profielen naar uw computer.

Als u een profiel voor het eerst laadt, moet u een netwerkverbinding hebben met de [!DNL Data Workbench server] en werken online, zodat de Data Workbench de benodigde bestanden kan downloaden van de [!DNL Data Workbench server].

Het downloaden van het profiel kan enkele minuten duren. U moet niet met het profiel beginnen te werken tot het Geheime voorgeheugen van Gegevens begint te vullen, maar u moet niet wachten tot het volledig is. U kunt de voortgang van de gegevenscache, de voortgang van de profielsynchronisatie en de datum en tijd van de laatst verwerkte gegevens bijhouden door de statusbalken te bekijken terwijl het profiel wordt geladen.

>[!NOTE]
>
>U ziet geen gegevens in visualisaties die u toevoegt tot het gegevensgeheime voorgeheugen begint te vullen.

De volgende keer dat u het profiel laadt, worden updates van het profiel en de bijbehorende gegevens alleen gedownload als u een netwerkverbinding hebt met de [!DNL Data Workbench server] en werken online. Als u offline werkt, worden het profiel en de bijbehorende gegevens geladen vanuit de cache van uw computer. In dit geval bekijkt u de versie van het profiel en de gegevens die de laatste keer zijn gedownload dat u online met het profiel hebt gewerkt. Voor meer informatie over online of offline werken raadpleegt u [Offline werken en online werken](../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54).

Wanneer u uw profiel moet wijzigen (met de opdracht [!DNL Profile Manager] of de [!DNL Server Files Manager]), moet u online werken om ervoor te zorgen dat u over de meest actuele versie van het profiel beschikt. Voor meer informatie over de [!DNL Profile Manager] en de [!DNL Server Files Manager], zie [Administratieve interfaces](../../home/c-get-started/c-admin-intrf/c-admin-intrf.md#concept-855c1a91e1a948969fab592adca15f74).

Als u geen toegang kunt krijgen tot een profiel of een profiel niet kunt laden, moet u mogelijk het volgende bevestigen:

* U hebt een netwerkverbinding met de [!DNL Data Workbench server] computer waarop het profiel zich bevindt.
* U hebt de juiste machtigingen om toegang te krijgen tot het profiel.

Neem voor hulp contact op met de systeembeheerder.

## Profielen laden of schakelen {#section-c50499d7d8084d7cadfada52df33f5f4}

1. Start Data Workbench.
1. Klik op de zijbalk op de naam van het profiel en klik op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*, waarbij *profielnaam* Dit is het profiel waarmee u wilt werken.

   ![](assets/sidebar_profile.png)

Als dit de eerste keer is dat u het geselecteerde profiel laadt, kan het enkele minuten duren voordat voldoende gegevens zijn gedownload om een visualisatie te vullen.

## Een profiel openen in een cluster {#section-189a0ac04a8f46099c11c0f4f77b6dbb}

Gebruikers van Data Workbench die toegang krijgen tot een profiel dat wordt uitgevoerd op een

De servercluster van de werkbank van gegevens identificeert slechts de master Server van de Data Workbench in het configuratiedossier van de Data Workbench ( [!DNL Insight.cfg]). Vanuit het perspectief van de gebruiker van de Data Workbench, is het profiel toegankelijk op slechts één Server van de Data Workbench (de master Server van de Data Workbench). Nochtans, kunnen de vraagverzoeken van analisten aan om het even welke Servers van de Data Workbench in de cluster worden geleid.

Voor meer informatie over profielen die op een cluster van de Server van de Data Workbench lopen, zie *Handleiding voor installatie en beheer van serverproducten*.

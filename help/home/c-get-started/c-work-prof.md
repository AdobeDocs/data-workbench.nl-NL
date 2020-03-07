---
description: De Werkbank van gegevens downloadt profielen aan uw machine.
title: Profielen
uuid: 8ea36138-9839-40e5-89e2-4b120f1dd7aa
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Profielen{#profiles}

De Werkbank van gegevens downloadt profielen aan uw machine.

Als u een profiel voor het eerst laadt, moet u een netwerkverbinding aan hebben [!DNL Data Workbench server] en online werken zodat de Werkbank van Gegevens de noodzakelijke dossiers van kan downloaden [!DNL Data Workbench server].

Het downloaden van het profiel kan enkele minuten in beslag nemen. U zou niet met het profiel moeten beginnen te werken tot het Geheime voorgeheugen van Gegevens begint te vullen, maar u moet niet wachten tot het volledig is. U kunt de vooruitgang van het gegevensgeheime voorgeheugen, de vooruitgang van de profielsynchronisatie, en de datum en de tijd van de onlangs verwerkte gegevens volgen, door de statusbars te bekijken aangezien het profiel laadt.

>[!NOTE]
>
>U ziet geen gegevens in visualisaties die u toevoegt tot het gegevensgeheime voorgeheugen begint te vullen.

De volgende keer dat u het profiel laadt, worden de updates aan het profiel en zijn gegevens gedownload slechts als u een netwerkverbinding aan hebt [!DNL Data Workbench server] en online werkt. Als u offline werkt, worden het profiel en zijn gegevens geladen van het geheime voorgeheugen van uw machine. In dit geval, bekijkt u de versie van het profiel en de gegevens die de laatste keer werd gedownload dat u online met het profiel werkte. Voor meer informatie over het werken online tegenover off-line, zie het [Werk Off-line en Online](../../home/c-get-started/c-off-on.md#concept-cef8758ede044b18b3558376c5eb9f54).

Wanneer u uw profiel (het gebruiken van [!DNL Profile Manager] of [!DNL Server Files Manager]) moet veranderen, zou u online moeten werken om ervoor te zorgen dat u de meest bijgewerkte versie van het profiel hebt. Voor meer informatie over [!DNL Profile Manager] en [!DNL Server Files Manager], zie [Administratieve Interfaces](../../home/c-get-started/c-admin-intrf/c-admin-intrf.md#concept-855c1a91e1a948969fab592adca15f74).

Als u geen toegang hebt tot een profiel of een profiel niet kunt laden, moet u het volgende bevestigen:

* U hebt een netwerkverbinding met het [!DNL Data Workbench server] systeem waarop het profiel zich bevindt.
* U hebt de aangewezen toestemmingen om tot het profiel toegang te hebben.

Voor hulp, contacteer uw systeembeheerder.

## Profielen voor laden of schakelen {#section-c50499d7d8084d7cadfada52df33f5f4}

1. De werkbank van Gegevens van de lancering.
1. Klik in de zijbalk op de profielnaam en klik op **[!UICONTROL Switch Profile]** > *&lt;**[!UICONTROL profile name]**>*, waarbij de *profielnaam* het profiel is waarmee u wilt werken.

   ![](assets/sidebar_profile.png)

Als dit de eerste keer is dat u het geselecteerde profiel laadt, kan het enkele minuten duren voordat u voldoende gegevens downloadt om een visualisatie te bevolken.

## Toegang tot een profiel op een cluster {#section-189a0ac04a8f46099c11c0f4f77b6dbb}

De gebruikers van de Werkbank van gegevens die tot een profiel toegang hebben dat op een

De de servercluster van de werkbank van gegevens identificeert slechts de server van de hoofdwerkbank van Gegevens in het de configuratiedossier van de Werkbank van Gegevens ( [!DNL Insight.cfg]). Vanuit het perspectief van de gebruiker van de Werkbank van Gegevens, is het profiel toegankelijk op slechts één Server van de Werkbank van Gegevens (de hoofdserver van de Werkbank van Gegevens). Nochtans, kunnen de vraagverzoeken van analisten aan om het even welke Servers van de Werkbank van Gegevens in de cluster worden geleid.

Voor meer informatie over profielen die op een cluster van de Server van de Werkbank van Gegevens lopen, zie de Gids *van de Installatie en van het Beleid van de Producten van de* Server.

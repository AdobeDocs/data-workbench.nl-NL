---
description: U kunt Profielbeheer gebruiken om bestanden te downloaden die u wilt wijzigen.
title: Lokale bestanden in het gebruikersprofiel wijzigen
uuid: 839417d1-34db-4b14-a103-8f5297af55b7
exl-id: 187d67a1-e436-4bfd-87ad-17b6c70dbee4
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Lokale bestanden wijzigen in het gebruikersprofiel{#modify-local-files-in-the-user-profile}

U kunt Profielbeheer gebruiken om bestanden te downloaden die u wilt wijzigen.

U kunt een bestand downloaden om het bestaande lokale bestand te overschrijven met de oorspronkelijke versie van het bestand of bestanden te openen, weer te geven en te wijzigen die niet toegankelijk zijn via de werkruimtemenu&#39;s.

**Een bestand downloaden**

1. Open in [!DNL Profile Manager] de benodigde mappen en submappen om te zoeken naar het bestand dat u wilt downloaden.
1. Klik met de rechtermuisknop op het vinkje naast de naam van het bestand en klik op **[!UICONTROL Make Local]**.

   >[!NOTE]
   >
   >Configuratie ( [!DNL .cfg]), dimensie ( [!DNL .dim]) en metrische ( [!DNL .metric]) dossiers kunnen direct in een profielomslag worden uitgegeven en aan de server worden bewaard zonder hen lokaal te maken en hen afzonderlijk op te slaan aan de server. Klik met de rechtermuisknop op het vinkje naast de naam van het bestand en klik op **[!UICONTROL Open]** > **in werkstation**.

Nadat het bestand naar de lokale computer is gedownload, wordt een vinkje weergegeven in de kolom [!DNL User]. Hiermee wordt aangegeven dat een lokale kopie van het bestand zich in de map Gebruiker\*profielnaam* op uw computer bevindt. Het vinkje heeft dezelfde kleur als het vinkje in de kolom *profielnaam*. Dit geeft aan dat het lokale bestand dezelfde datum en tijd heeft als het bestand in de map *profile name*.

**Het bestand wijzigen**

1. Klik met de rechtermuisknop op het vinkje naast de bestandsnaam in de kolom [!DNL User].
1. Klik op een van de volgende menuopties, afhankelijk van de manier waarop u het bestand wilt bewerken:

   * **[!UICONTROL Open]** >  **[!UICONTROL in workstation]** als u een  [!DNL .vw] bestand of een  [!DNL .cfg] bestand in een werkruimte bewerkt.

   * **Open**  > **in vw. Editor **als u een .vw-bestand bewerkt om nieuwe parameters toe te voegen.

   * **[!UICONTROL Open]** >  **[!UICONTROL In Notepad]** als u een tekstbestand opent of nieuwe parameters aan een  [!DNL .cfg] bestand wilt toevoegen.

   * **[!UICONTROL Open]** >  **[!UICONTROL folder]** als u de map wilt openen waarin het bestand zich op uw computer bevindt

1. Bewerk het bestand naar wens en sla het bestand op.

Let er in [!DNL Profile Manager] op dat het vinkje in de kolom [!DNL User] voor het bestand dat u hebt bewerkt, van kleur is gewijzigd. Dit geeft aan dat het lokale bestand nu verschilt van de versie in de map *profile name*. Indien nodig kunt u de gereviseerde versie van het bestand publiceren naar het profiel voor gebruik door andere gebruikers die met dit profiel werken.

---
description: Een snelle handleiding voor de minimale stappen die nodig zijn om historische gegevensfeeds te valideren en in te stellen.
title: Historische gegevensfeeds valideren
uuid: 83d2d48b-0966-4f4e-9c9c-60473c4546b2
exl-id: 5a5e2cca-2fab-48a0-b58d-a8c46114b9a0
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Historische gegevensfeeds valideren{#validating-historical-data-feeds}

{{eol}}

Een snelle handleiding voor de minimale stappen die nodig zijn om historische gegevensfeeds te valideren en in te stellen.

## Validatiestappen voor consistentie van gegevensfeeds {#section-777b2c627a354627a02feb9461e23038}

1. Aanmelden bij *droogte* (https://oasis.omniture.com/drteeth/)
1. Ga naar SiteCatalyst Admin -> Definitie gegevensfeed (nieuw)
1. Naar serverlocatie springen (bijv. Dallas, Londen..) Afhankelijk van waar uw organisatie zich bevindt.
1. Verstrek RSID en selecteer het type van voer Inzicht en klik op *zoeken*.

   ![](assets/dwb_impl_historical.png)

1. Identificeer de daadwerkelijke voedernaam voor uw cliënt.
1. Klik op Historie in de sectie Handelingen. ![](assets/dwb_impl_historical1.png)

   Controleer het statusveld op fouten. Als de status van een feed fout is, selecteert u de feed en klikt u op Opnieuw verwerken. Als er een fout is opgetreden voor meerdere aanvragen, stuurt u een e-mail naar *`dataworkbench@adobe.com`* met Feed ID en Report Suit details om opnieuw te verwerken.

1. Na de validatie worden de logbestanden in de onbewerkte map van de NAS-locatie gecontroleerd.

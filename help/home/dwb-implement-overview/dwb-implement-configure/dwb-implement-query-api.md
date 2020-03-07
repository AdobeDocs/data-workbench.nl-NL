---
description: Een snelle gids voor vestiging een Vraag API.
title: Query API Setup
uuid: 521f06a4-65ee-4206-b769-4c1ce6e5fe7d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Query API Setup{#query-api-setup}

Een snelle gids voor vestiging een Vraag API.

Volg de volgende stappen voor vestiging de Vraag API:

1. Vraag API Certificate Acquisition

   Verzend een E-mail naar het Team van Tech Ops van Adobe E-mail - `Dataworkbench@adobe.com`.

   Gelieve te verstrekken de naam van CN u voor de Vraag API wilt gebruiken ( verstrek een generische naam zoals `<Client>` Vraag API).

   >[!NOTE]
   >
   >De technische Ops zullen het certificaat produceren en het uploaden in een URL. Gelieve te laten de Adviseurs van Adobe weten na het ontvangen van het bericht van Tech Ops over succesvolle generatie van het kaartje zodat het kaartje aan u door hen terug zal worden verzonden.

1. Het downloaden van en het Extracteren van de Stunnel API. Ontvang het api-stunnel dossier van uw consultant.

   Zorg ervoor Perl op uw systeem geïnstalleerd is.

   In de gehaalde omslag (de omslagweg waar u het dossier kopieert), kopieer uw certificaat van de Vraag API binnen de *stunnel* omslag.

1. Vorm Stunnel.conf

   Er zou een dossier moeten zijn genoemd *stunnel.conf* binnen de omslag van de *Stunnel* (waar u uw certificaat kopieerde).

   Geef het dossier in Blocnote uit.

   ![](assets/dwb_impl_API1.png)

   Verander de parameters als volgt: ![](assets/dwb_impl_API2.png)

   Twee parameters moeten in dit dossier worden veranderd.

   * *Cert* = de naam op uw certificaat. In dit voorbeeld is het Aadhithiya Ramani QAPI Client.pem.
   * *Verbind* =The servernaam voor uw belangrijkste DPU.

1. Het kopiëren van *Query.pm*.

   Het *Query.pm* - dossier zal in de Omslag van het Inzicht API beschikbaar zijn.

   Kopieer het bestand *Query.pm* en plak het in de map Perl Library (meestal is het *C:\Perl64\lib *, maar controleer waar Perl op uw computer is geïnstalleerd).

1. Wijzig het *api-http.pl* - dossier

   Het api-http.pl- dossier zal in de api-stunnel omslag beschikbaar zijn.

   Slechts één te wijzigen parameter

   *Mijn $profile* = de profielnaam waarvoor u de Vraag API vormt.

1. Installeer de Vraag API.

   Open de opdrachtprompt in uw systeem als &quot;Beheerder&quot; en navigeer naar de directory waar u de *stunnel* hebt gewonnen zoals getoond: ![](assets/dwb_impl_API3.png)

   Stel het volgende bevel in werking *.\ stunnel - installeer*. ![](assets/dwb_impl_API4.png)

   Na het uitvoeren van het bevel zal een venster opklappen verklarend dat de *stunnel* geïnstalleerd is.

   >[!NOTE]
   >
   >Na het uitvoeren van het bevel zal een venster opklappen verklarend dat de *stunnel* geïnstalleerd is.

1. Het testen van de de stunnel van de Vraag API configuratie

   De definitieve stap van dit proces zal de configuratie van de Vraag API zijn te testen. In de bevelherinnering die u voor het installeren van de api-stunnel folder gebruikte. ![](assets/dwb_impl_API5.png)

   Stel het Perl manuscript beschikbaar in die omslag in werking gebruikend volgende bevel* perl api-http.pl*. ![](assets/dwb_impl_API6.png)

   Na het runnen van het manuscript zouden de resultaten als het hieronder ontsproten scherm moeten zijn (de datumtijd en de waarden in het resultaat zullen afhankelijk van tijd en andere parameters in het profiel variëren waarop u de Vraag API (in stap 6) hebt gevormd. ![](assets/dwb_impl_API7.png)


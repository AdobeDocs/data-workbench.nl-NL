---
description: Een snelle handleiding voor het instellen van een query-API.
title: Query API instellen
uuid: 521f06a4-65ee-4206-b769-4c1ce6e5fe7d
exl-id: 8b9dace8-4dad-434c-aec3-2f6ca872a5f6
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Query API instellen{#query-api-setup}

{{eol}}

Een snelle handleiding voor het instellen van een query-API.

Voer de volgende stappen uit om de API voor zoekopdrachten in te stellen:

1. Vraag-API-certificaatovername

   Stuur een e-mail naar het TechOps-team van Adobe - `Dataworkbench@adobe.com`.

   Geef de GN-naam op die u voor de API voor query wilt gebruiken. Geef een algemene naam op, bijvoorbeeld `<Client>` Query-API).

   >[!NOTE]
   >
   >Tech Ops genereert het certificaat en uploadt het in een URL. Laat het de consultants van de Adobe weten na het ontvangen van het bericht van Tech Ops over het succesvol genereren van het ticket, zodat het ticket naar u wordt teruggestuurd.

1. Het downloaden en uitpakken van het API-werkstation. Ontvang het api-stunnel-bestand van uw consultant.

   Controleer of Perl op uw computer is geïnstalleerd.

   Kopieer in de uitgepakte map (het mappad waar u het bestand kopieert) het API-certificaat van de query in het *stunnel* map.

1. Vorm Stunnel.conf

   Er moet een bestand met de naam *stunnel.conf* binnen *Stunnel* map (waar u het certificaat hebt gekopieerd).

   Bewerk het bestand in Kladblok.

   ![](assets/dwb_impl_API1.png)

   Wijzig de parameters als volgt: ![](assets/dwb_impl_API2.png)

   In dit bestand moeten twee parameters worden gewijzigd.

   * *Cert* = De naam op het certificaat. In dit voorbeeld is het Aadhithiya Ramani QAPI Client.pem.
   * *Verbinden* =De servernaam voor uw belangrijkste DPU.

1. De *Query.pm*.

   De *Query.pm* Het bestand is beschikbaar in de Insight API-map.

   Kopieer de *Query.pm* bestand en plak het bestand in uw Perl Library-map (meestal *C:\Perl64\lib *, maar controleer waar de Perl op uw computer is geïnstalleerd).

1. De *api-http.pl* file

   Het bestand api-http.pl is beschikbaar in de map api-stunnel.

   Slechts één te wijzigen parameter

   *Mijn $profiel* = De profielnaam waarvoor u de Vraag API vormt.

1. Installeer de API voor query.

   Open de opdrachtregel in uw systeem als &quot;Beheerder&quot; en navigeer naar de map waar u de opdrachtregel hebt uitgepakt *stunnel* zoals weergegeven: ![](assets/dwb_impl_API3.png)

   Voer de volgende opdracht uit *.\stunnel-install*. ![](assets/dwb_impl_API4.png)

   Na het uitvoeren van het bevel zal een venster verschijnen verklarend dat *stunnel* is geïnstalleerd.

   >[!NOTE]
   >
   >Na het uitvoeren van het bevel zal een venster verschijnen verklarend dat *stunnel* is geïnstalleerd.

1. De stunnel-configuratie van de Query API testen

   De laatste stap van dit proces is het testen van de API-configuratie van de query. In de opdrachtprompt die u hebt gebruikt voor de installatie van de api-stunnel-directory. ![](assets/dwb_impl_API5.png)

   Voer het Perl-script uit dat beschikbaar is in die map met de volgende opdracht* perl api-http.pl*. ![](assets/dwb_impl_API6.png)

   Na het in werking stellen van het manuscript zouden de resultaten als hieronder schermafbeelding moeten zijn (de datumtijd en de waarden in het resultaat zullen afhankelijk van de tijd en andere parameters in het profiel variëren waarop u de Vraag API (in stap 6) hebt gevormd. ![](assets/dwb_impl_API7.png)

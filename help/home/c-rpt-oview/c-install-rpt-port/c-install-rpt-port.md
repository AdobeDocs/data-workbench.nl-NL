---
description: Om het Portaal van het Rapport te gebruiken, moet u een reeks pagina's van de toepassingsserver (ASPs) op IIS installeren en vormen.
title: Het rapportportaal installeren
uuid: 6aeb6038-b0b0-48b9-a020-bc9dfd703c43
exl-id: c6f140d4-a4fe-48e2-bbcd-b43efb2387dd
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Het rapportportaal installeren{#installing-the-report-portal}

{{eol}}

Om het Portaal van het Rapport te gebruiken, moet u een reeks pagina&#39;s van de toepassingsserver (ASPs) op IIS installeren en vormen.

**Voordat u begint**

De procedures in dit hoofdstuk beschrijven hoe te installeren en te vormen [!DNL Report Portal]. Om deze procedures te voltooien, moet u:

* Microsoft IIS installeren en de versie ervan kennen.
* Ken de namen van de rapportreeksen waarvan rapporten door worden getoond [!DNL Report Portal].
* Weet de locatie van de map waarin [!DNL Report Server] Slaat de output voor deze rapportreeksen op. Zorg ervoor dat de IIS-toepassingsserver toegang heeft tot deze map.

>[!NOTE]
>
>* Te bekijken met [!DNL Report Portal], moeten rapporten specifieke naamgevingsconventies volgen. Daarnaast moet de map waarin rapporten worden opgeslagen een voorgeschreven structuur hebben. Zie voor een beschrijving van deze eisen [Ervoor zorgen dat uw rapportsets compatibel zijn met Report Portal...](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706).
>
>* Wachtwoorden in rapportportaal zijn nu compatibel met AES-256 bits. Als de bevordering aan Portaal 2.0 van het Rapport, vergroot de Grootte van het Gebied voor Wachtwoord van 50 tot 150 in **users.mdb** database. Het veld moet groter worden om wachtwoorden met bijgewerkte versleuteling te kunnen bevatten.
>* Als u aan Portaal 2.0 van het Rapport bevordert, vergroot de Grootte van het Gebied voor **Wachtwoord** veld van 50 tot 150 in de database users.mdb. Het veld moet groter worden om wachtwoorden met bijgewerkte versleuteling te kunnen bevatten.
>* Het Portaal van het Rapport kenmerkt nu sterkere het hakken algoritmen met het zouten steun. Als u een upgrade uitvoert naar **Report Portal 2.1**, voegt u een nieuw tekstveld toe, *PasswordSalt* met een veldgrootte van 20 tekens in [!DNL users.mdb]database. Dit veld is vereist voor het opslaan van de salt van het wachtwoord.
>


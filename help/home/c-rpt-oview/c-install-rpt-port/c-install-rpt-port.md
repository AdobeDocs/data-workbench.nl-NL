---
description: Om het Portaal van het Rapport te gebruiken, moet u een reeks pagina's van de toepassingsserver (ASPs) op IIS installeren en vormen.
title: Het rapportportaal installeren
uuid: 6aeb6038-b0b0-48b9-a020-bc9dfd703c43
exl-id: c6f140d4-a4fe-48e2-bbcd-b43efb2387dd
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Het Portaal van het Rapport installeren{#installing-the-report-portal}

Om het Portaal van het Rapport te gebruiken, moet u een reeks pagina&#39;s van de toepassingsserver (ASPs) op IIS installeren en vormen.

**Voordat u begint**

De procedures in dit hoofdstuk beschrijven hoe te om [!DNL Report Portal] te installeren en te vormen. Om deze procedures te voltooien, moet u:

* Microsoft IIS geïnstalleerd hebben en zijn versie kennen.
* Weet de namen van de rapportreeksen waarvan rapporten door [!DNL Report Portal] worden getoond.
* Weet de plaats van de folder waarin [!DNL Report Server] de output voor deze rapportreeksen bewaart. Zorg ervoor dat de IIS-toepassingsserver toegang heeft tot deze map.

>[!NOTE]
>
>* Om te kunnen worden weergegeven met [!DNL Report Portal], moeten rapporten specifieke naamgevingsconventies volgen. Daarnaast moet de map waarin rapporten worden opgeslagen een voorgeschreven structuur hebben. Voor een beschrijving van deze vereisten, zie [Zorgen dat Uw Reeksen van het Rapport met het Portaal van het Rapport compatibel zijn..](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706).
   >
   >
* Wachtwoorden in rapportportaal zijn nu compatibel met AES-256 bits. Als de bevordering aan Portaal 2.0 van het Rapport, vergroot de Grootte van het Gebied voor het gebied van het Wachtwoord van 50 tot 150 in **users.mdb** gegevensbestand. Het veld moet groter worden om wachtwoorden met bijgewerkte versleuteling te kunnen bevatten.
>* Als u aan Portaal 2.0 van het Rapport bevordert, verhoog de Grootte van het Gebied voor het **Wachtwoord** gebied van 50 tot 150 in user.mdb- gegevensbestand. Het veld moet groter worden om wachtwoorden met bijgewerkte versleuteling te kunnen bevatten.
>* Het Portaal van het Rapport kenmerkt nu sterkere het hakken algoritmen met het zouten steun. Als u aan **Portaal 2.1** van het Rapport bevordert, voeg een nieuw gebied van de Tekst, *PasswordSalt* met gebiedsgrootte van 20 karakters in [!DNL users.mdb]gegevensbestand toe. Dit veld is vereist voor het opslaan van de salt van het wachtwoord.

>



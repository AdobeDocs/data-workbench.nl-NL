---
description: Om het Portaal van het Rapport te gebruiken, moet u een reeks pagina's van de toepassingsserver (ASPs) op IIS installeren en vormen.
solution: Analytics
title: Het portaal van het Rapport installeren
topic: Data workbench
uuid: 6aeb6038-b0b0-48b9-a020-bc9dfd703c43
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# Het portaal van het Rapport installeren{#installing-the-report-portal}

Om het Portaal van het Rapport te gebruiken, moet u een reeks pagina&#39;s van de toepassingsserver (ASPs) op IIS installeren en vormen.

**Voordat u begint**

De procedures in dit hoofdstuk beschrijven om te installeren en te vormen [!DNL Report Portal]. Om deze procedures te voltooien, moet u:

* Heb Microsoft IIS geïnstalleerd en ken zijn versie.
* Ken de namen van de rapportreeksen de waarvan rapporten langs worden getoond [!DNL Report Portal].
* Ken de plaats van de folder waarin de output voor deze rapportreeksen [!DNL Report Server] bewaart. Zorg ervoor dat de IIS toepassingsserver toegang tot deze folder heeft.

>[!NOTE]
>
>* Om worden bekeken gebruikend [!DNL Report Portal], moeten de rapporten specifieke noemende overeenkomsten volgen. Bovendien, moet de folder waarin de rapporten worden bewaard een voorgeschreven structuur volgen. Voor een beschrijving van deze vereisten, zie het [Zorgen dat Uw Reeksen van het Rapport met het Portaal van het Rapport compatibel zijn...](../../../home/c-rpt-oview/c-install-rpt-port/c-rpt-port-user-inter.md#section-2b141e5d198a4bbea455699126c24706).
   >
   >
* De wachtwoorden in rapportportaal zijn nu volgzaam AES-256 beetje. Als de bevordering aan Portaal 2.0 van het Rapport, verhoog de Grootte van het Gebied voor het gebied van het Wachtwoord van 50 tot 150 in het **user.mdb** - gegevensbestand. Het verhogen van de gebiedsgrootte wordt vereist om wachtwoorden met bijgewerkte encryptie aan te passen.
>* Als u bevordert om Portaal 2.0 te melden, verhoog de Grootte van het Gebied voor het gebied van het **Wachtwoord** van 50 tot 150 in user.mdb- gegevensbestand. Het verhogen van de gebiedsgrootte wordt vereist om wachtwoorden met bijgewerkte encryptie aan te passen.
>* Het Portaal van het Rapport kenmerkt nu sterkere het hakken algoritmen met het zouten steun. Als u bevordert om Portaal 2.1 **te** Rapport, voeg een nieuw gebied van de Tekst, *PasswordSalt* met gebiedsgrootte van 20 karakters in [!DNL users.mdb]gegevensbestand toe. Dit gebied wordt vereist om het wachtwoordzout op te slaan.
>




---
description: Gebruikers moeten over een geldig account beschikken en een accountnaam en wachtwoord opgeven wanneer zij het rapportportaal openen.
solution: Analytics
title: Aanvullende accounts definiëren
topic: Data workbench
uuid: 5ad98b52-267c-4c36-b43a-ae6ad415de8e
translation-type: tm+mt
source-git-commit: e4f2c653c00c21180b14bf67cc116d832bddd028

---


# Aanvullende accounts definiëren

Gebruikers moeten over een geldig account beschikken en een accountnaam en wachtwoord opgeven wanneer zij het rapportportaal openen.

Gebruikersverificatie is standaard ingeschakeld in [!DNL Report Portal].

De lijst met geldige accounts voor [!DNL Report Portal] wordt bijgehouden in het databasebestand, [!DNL portal.mdb]. [!DNL Report Portal] wordt geïnstalleerd met één account met beheerdersrechten:

* Accountnaam: test
* Wachtwoord: user

>[!NOTE]
>
>Om veiligheidsredenen raadt Adobe u aan het wachtwoord voor dit account te wijzigen nadat u het hebt geïnstalleerd [!DNL Report Portal].

Als u gebruikersaccounts wilt toevoegen aan [!DNL Report Portal] of gegevens wilt wijzigen die betrekking hebben op bestaande accounts, gebruikt u het [!DNL Admin] tabblad in de [!DNL Report Portal] gebruikersinterface.

Telkens wanneer u een nieuwe account toevoegt of een bestaande account bewerkt, wordt een bevestigingse-mail verzonden zoals opgegeven in het [!DNL email.asp] bestand in de map \*PortalName*\PortalASP. Zie Het bestand [Email.asp](../../../home/c-rpt-oview/c-install-rpt-port/t-email-file.md#task-d9f4f306d38e435aa7effab3d94f690b)bewerken voor meer informatie.

Zie [Werken met accounts](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d)voor stappen om extra gebruikers toe te voegen.

>[!NOTE]
>
>Naar keuze, kunt u gebruikersauthentificatie onbruikbaar maken en anonieme toegang tot toestaan [!DNL Report Portal]. Voor stappen om dit te doen, zie de informatie over de Sessie (&quot;In&quot;) parameter in [geef het Dossier](../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7)van de Configuratie van de Zitting uit.


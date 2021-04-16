---
description: Gebruikers moeten over een geldig account beschikken en een accountnaam en wachtwoord opgeven wanneer zij het rapportportaal openen.
title: Aanvullende accounts definiëren
uuid: 5ad98b52-267c-4c36-b43a-ae6ad415de8e
exl-id: 1f267217-a389-431a-ba49-9a9eead0ae83
translation-type: tm+mt
source-git-commit: d9df90242ef96188f4e4b5e6d04cfef196b0a628
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Aanvullende accounts definiëren

Gebruikers moeten over een geldig account beschikken en een accountnaam en wachtwoord opgeven wanneer zij het rapportportaal openen.

Gebruikersverificatie wordt standaard ingeschakeld in [!DNL Report Portal].

De lijst met geldige accounts voor [!DNL Report Portal] wordt bijgehouden in het databasebestand [!DNL portal.mdb]. [!DNL Report Portal] wordt geïnstalleerd met één account met beheerdersrechten:

* Accountnaam: test
* Wachtwoord: user

>[!NOTE]
>
>Om veiligheidsredenen raadt Adobe u aan het wachtwoord voor dit account te wijzigen nadat u [!DNL Report Portal] hebt geïnstalleerd.

Als u gebruikersaccounts wilt toevoegen aan [!DNL Report Portal] of informatie met betrekking tot bestaande accounts wilt wijzigen, gebruikt u het tabblad [!DNL Admin] in de gebruikersinterface [!DNL Report Portal].

Telkens wanneer u een nieuwe account toevoegt of een bestaande account bewerkt, wordt een bevestigingse-mail verzonden zoals opgegeven in het bestand [!DNL email.asp] in de map \*PortalName*\PortalASP. Zie [Het bestand Email.asp](../../../home/c-rpt-oview/c-install-rpt-port/t-email-file.md#task-d9f4f306d38e435aa7effab3d94f690b) bewerken voor meer informatie.

Zie [Werken met accounts](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d) voor stappen om extra gebruikers toe te voegen.

>[!NOTE]
>
>Naar keuze, kunt u gebruikersauthentificatie onbruikbaar maken en anonieme toegang tot [!DNL Report Portal] verlenen. Voor stappen om dit te doen, zie de informatie over de Sessie (&quot;In&quot;) parameter in [geef het Dossier van de Configuratie van de Zitting](../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7) uit.

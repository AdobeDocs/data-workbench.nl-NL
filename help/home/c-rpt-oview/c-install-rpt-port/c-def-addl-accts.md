---
description: Gebruikers moeten over een geldig account beschikken en een accountnaam en wachtwoord opgeven wanneer zij het rapportportaal openen.
title: Aanvullende accounts definiëren
uuid: 5ad98b52-267c-4c36-b43a-ae6ad415de8e
exl-id: 1f267217-a389-431a-ba49-9a9eead0ae83
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Aanvullende accounts definiëren

{{eol}}

Gebruikers moeten over een geldig account beschikken en een accountnaam en wachtwoord opgeven wanneer zij het rapportportaal openen.

Gebruikersverificatie is standaard ingeschakeld in [!DNL Report Portal].

De lijst met geldige accounts voor [!DNL Report Portal] wordt bijgehouden in het databasebestand, [!DNL portal.mdb]. [!DNL Report Portal] wordt geïnstalleerd met één account met beheerdersrechten:

* Accountnaam: test
* Wachtwoord: user

>[!NOTE]
>
>Om veiligheidsredenen raadt Adobe u aan het wachtwoord voor dit account te wijzigen nadat u het hebt geïnstalleerd [!DNL Report Portal].

Gebruikersaccounts toevoegen aan [!DNL Report Portal] of gegevens met betrekking tot bestaande accounts wijzigen, gebruikt u de [!DNL Admin] op het tabblad [!DNL Report Portal] gebruikersinterface.

Telkens wanneer u een nieuwe account toevoegt of een bestaande account bewerkt, wordt een bevestigingsbericht verzonden zoals opgegeven in het dialoogvenster [!DNL email.asp] in de map \*PortalName*\PortalASP. Zie voor meer informatie [Het bestand Email.asp bewerken](../../../home/c-rpt-oview/c-install-rpt-port/t-email-file.md#task-d9f4f306d38e435aa7effab3d94f690b).

Voor stappen om extra gebruikers toe te voegen, zie [Werken met accounts](../../../home/c-rpt-oview/c-admin-rpt/c-work-accts/c-work-accts.md#concept-c933a1940bda4a3489d61d8af315e45d).

>[!NOTE]
>
>U kunt gebruikersverificatie desgewenst uitschakelen en anonieme toegang toestaan tot [!DNL Report Portal]. Zie de informatie over de parameter Session(&quot;In&quot;) in het gedeelte [Het sessieconfiguratiebestand bewerken](../../../home/c-rpt-oview/c-install-rpt-port/t-edit-sess-config-file.md#task-cf11c3a780bd4936afd3f64a6b30afc7).

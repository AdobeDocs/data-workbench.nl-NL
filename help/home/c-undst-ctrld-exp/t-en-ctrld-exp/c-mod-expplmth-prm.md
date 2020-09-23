---
description: 'null'
solution: Analytics,Analytics
title: De parameter ExpPartialMatch wijzigen (optioneel)
topic: Data workbench
uuid: 15ed33cc-5ec8-45b2-a4eb-d1941962ca9d
translation-type: tm+mt
source-git-commit: 34cdcfc83ae6bb620706db37228e200cff43ab2c
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# De parameter ExpPartialMatch wijzigen (optioneel){#modifying-the-exppartialmatch-parameter-optional}

Als u gecontroleerde experimenten wilt toelaten om uw volledige website of een volledige subdirectory van uw website aan een andere plaats opnieuw in kaart te brengen, kunt u de parameter ExpPartialMatch in het [!DNL txlogd.conf] dossier aan &quot;op.&quot;plaatsen De standaardwaarde is &quot;uit&quot;.

Hieronder ziet u een voorbeeld van de parameter ExpPartialMatch:

[!DNL ExpPartialMatch off]

Wees zeer voorzichtig wanneer u deze parameter instelt op &quot;on&quot;, omdat dit kan leiden tot een onbedoelde hertoewijzing van uw gehele website.

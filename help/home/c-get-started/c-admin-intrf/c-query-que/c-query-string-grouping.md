---
description: Met Tekenreeksgroepering voor query kunt u een groot aantal velden samenvoegen.
title: Groepering queryreeks
uuid: 7dc5ba71-984f-4899-99d2-f79b57fb616d
exl-id: 4052cf7e-abdf-4e16-9f42-521c4e719786
source-git-commit: b1dda69a606a16dccca30d2a74c7e63dbd27936c
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Groepering queryreeks{#query-string-grouping}

{{eol}}

Met Tekenreeksgroepering voor query kunt u een groot aantal velden samenvoegen.

De Groepering van het Koord van de vraag is specifiek voor elk profiel, maar werkt goed in transformaties zoals aangetoond in dit voorbeeld:

1. Maak de paren die u wilt bundelen door een aangepast configuratiebestand toe te voegen ( [!DNL E:\...\Dataset\Log Processing\SC Fields.cfg]) en voegt vervolgens het transformatietype toe *BuildNameValuePair* als parameter.

   ```
   2 = BuildNameValuePair:  
         Comments = Comment: 0 items 
         Condition = AndCondition: 0 items 
         Delimiter = string:  
         Input Columns = vector: 1 items 
           0 = Column:  
             Column Name = string: e100 
             Field Name = string: x-cust100 
             ...  
     (all the fields you wish to build)
             Name = string: Custom Events 
             Output = string: x-event-list       
   ```

1. Maak een nieuw bestand om de gecondenseerde gegevens uit te pakken naar de velden die u wilt gebruiken door een aangepast configuratiebestand toe te voegen ( [!DNL E:\...\Dataset\Transformation\SC Fields Transformation.cfg]) en voegt vervolgens het transformatietype toe *ExtractNameValueParen* als parameter.

   ```
   2 = ExtractNameValuePairs:  
         Comments = Comment: 0 items 
         Condition = AndCondition: 0 items 
         Delimiter = string:  
         Input Field = string: x-event-list 
         Name = string: Custom Events 
         Output Columns = vector: 1 items 
           0 = Column:  
             Column Name = string: e100 
             Field Name = string: x-cust100 
             ...  
     (all the fields you wish to extract) 
             Name = string: Custom Events 
             Output = string: x-event-list   
   ```

## Andere toepassingen {#section-cc5d2b0c9e194fc88a5a18a06ef22f5e}

Als u vele gebieden met douanevars, steunen, en variabelen hebt, tijdens logboekverwerking kunt u een paar van de naamwaarde bouwen om gebieden in een rapport te combineren. U kunt bijvoorbeeld benoemde-waardeparen samenstellen in gecombineerde velden om de [!DNL tempDB] bestandsgrootte.

![](assets/query_string_grouping.png)

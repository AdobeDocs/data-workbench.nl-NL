---
description: De Groepering van het Koord van de vraag laat u een groot aantal gebieden samen integreren.
title: De Groepering van het Koord van de vraag
uuid: 7dc5ba71-984f-4899-99d2-f79b57fb616d
translation-type: tm+mt
source-git-commit: aec1f7b14198cdde91f61d490a235022943bfedb

---


# De Groepering van het Koord van de vraag{#query-string-grouping}

De Groepering van het Koord van de vraag laat u een groot aantal gebieden samen integreren.

De Groepering van het Koord van de vraag is specifiek voor elk profiel, maar de werken goed in transformaties zoals aangetoond in dit voorbeeld:

1. Creeer de paren u wenst om te bundelen door een dossier van de douaneconfiguratie ( [!DNL E:\...\Dataset\Log Processing\SC Fields.cfg]) toe te voegen en dan het Type van Transformatie toe te voegen *BuildNameValuePair* als parameter.

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

1. Creeer een nieuw dossier voor het halen van de gecondenseerde gegevens in de gebieden u wenst te gebruiken door een dossier van de douaneconfiguratie ( [!DNL E:\...\Dataset\Transformation\SC Fields Transformation.cfg]) toe te voegen en dan het Type van Transformatie toe te voegen *ExtractNamePairs* als parameter.

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

Als u vele gebieden met douanevars, steunen, en variabelen hebt, tijdens logboekverwerking kunt u een paar van de naamwaarde bouwen om gebieden in een rapport te combineren. Bijvoorbeeld, kunt u genoemde-waardeparen in gecombineerde gebieden bouwen om de [!DNL tempDB] dossiergrootte te verminderen.

![](assets/query_string_grouping.png)

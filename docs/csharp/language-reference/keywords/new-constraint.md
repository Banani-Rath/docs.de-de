---
title: "new-Einschr&#228;nkung (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "new constraint-Schlüsselwort [C#]"
ms.assetid: 58850b64-cb97-4136-be50-1f3bc7fc1da9
caps.latest.revision: 20
caps.handback.revision: 20
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# new-Einschr&#228;nkung (C#-Referenz)
Die `new`\-Einschränkung gibt an, dass jedes Typargument in einer generischen Klassendeklaration einen öffentlichen parameterlosen Konstruktor besitzen muss.  Der Typ darf nicht abstrakt sein, um die new\-Einschränkung zu verwenden.  
  
## Beispiel  
 Wenden Sie `new`\-Einschränkung auf einen Typparameter an, wenn die generische Klasse wie im folgenden Beispiel neue Instanzen des Typs erstellt:  
  
 [!CODE [csrefKeywordsOperator#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#5)]  
  
## Beispiel  
 Wenn Sie die `new()`\-Einschränkung mit anderen Einschränkungen verwenden, muss sie zuletzt angegeben werden:  
  
 [!CODE [csrefKeywordsOperator#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#6)]  
  
 Weitere Informationen finden Sie unter [Einschränkungen für Typparameter](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md).  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 <xref:System.Collections.Generic>   
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Operatorschlüsselwörter](../../../csharp/language-reference/keywords/operator-keywords.md)   
 [Generika](../../../csharp/programming-guide/generics/index.md)
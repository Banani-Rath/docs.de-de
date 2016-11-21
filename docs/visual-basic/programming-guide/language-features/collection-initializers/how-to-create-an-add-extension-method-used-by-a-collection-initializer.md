---
title: "How to: Create an Add Extension Method Used by a Collection Initializer (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "collection initializers [Visual Basic]"
ms.assetid: f64b52c7-8b11-4410-93a6-cb3aeebcc772
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Create an Add Extension Method Used by a Collection Initializer (Visual Basic)
Wenn Sie eine Auflistung mithilfe eines Auflistungsinitialisierers erstellen, sucht der Visual Basic\-Compiler nach einer `Add`\-Methode des Auflistungstyps, für den die Parameter der `Add`\-Methode mit den Typen der Werte im Auflistungsinitialisierer übereinstimmen.  Diese `Add`\-Methode wird verwendet, um die Auflistung mit den Werten des Auflistungsinitialisierers aufzufüllen.  
  
 Wenn keine entsprechende `Add`\-Methode vorhanden ist und Sie den Code für die Auflistung nicht ändern können, können Sie eine Erweiterungsmethode namens `Add` hinzufügen, die die Parameter akzeptiert, die für den Auflistungsinitialisierer erforderlich sind.  Diese Aktion müssen Sie bei der Verwendung von Auflistungsinitialisierern für generische Auflistungen normalerweise ausführen.  
  
## Beispiel  
 Im folgenden Beispiel wird gezeigt, wie dem generischen <xref:System.Collections.Generic.List%601>\-Typ eine Erweiterungsmethode hinzugefügt wird, damit ein Auflistungsinitialisierer zum Hinzufügen von Objekten des Typs `Employee` verwendet werden kann.  Die Erweiterungsmethode ermöglicht es Ihnen, die gekürzte Auflistungsinitialisierersyntax zu verwenden.  
  
 [!CODE [VbVbalrCollectionInitializersHowTo1#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1#1)]  
  
 [!CODE [VbVbalrCollectionInitializersHowTo1#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1#2)]  
  
 [!CODE [VbVbalrCollectionInitializersHowTo1#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCollectionInitializersHowTo1#3)]  
  
## Siehe auch  
 [Collection Initializers](../../../../visual-basic/programming-guide/language-features/collection-initializers/index.md)   
 [How to: Create a Collection Used by a Collection Initializer](../../../../visual-basic/programming-guide/language-features/collection-initializers/how-to-create-a-collection-used-by-a-collection-initializer.md)
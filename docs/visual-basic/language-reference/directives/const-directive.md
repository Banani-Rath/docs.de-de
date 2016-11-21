---
title: "#Const Directive | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vb.#Const"
  - "#vb.Const"
  - "#Const"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "#Const directive"
  - "conditional compilation, directives"
  - "Const directive (#Const)"
  - "Visual Basic compiler, compiler directives"
  - "constants, Const directive"
  - "constants, declaring"
  - "Const statement [Visual Basic], directive (#Const)"
  - "declaring constants, #const directive"
ms.assetid: 707669e5-23f9-4f17-8622-a0d534429386
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# #Const Directive
Definiert Konstanten für die bedingte Kompilierung in Visual Basic.  
  
## Syntax  
  
```  
#Const constname = expression  
```  
  
## Teile  
 `constname`  
 Erforderlich.  Der Name der Konstanten, die definiert wird.  
  
 `expression`  
 Erforderlich.  Literalzeichen, andere Konstanten für die bedingte Kompilierung oder jede Kombination, die alle arithmetischen oder logischen Operatoren außer `Is` enthalten kann.  
  
## Hinweise  
 Konstanten für die bedingte Kompilierung sind immer **Private** für die Datei, in der sie enthalten sind.  Public\-Compilerkonstanten können nicht mit der `#Const`\-Direktive erstellt werden. Sie werden ausschließlich mithilfe der Benutzeroberfläche oder mit der `/define`\-Compileroption erstellt.  
  
 Als `expression` dürfen nur Konstanten für die bedingte Kompilierung und Literalzeichen angegeben werden.  Bei einer mit `Const` definierten Standardkonstante wird ein Fehler ausgegeben.  Mit dem `#Const`\-Schlüsselwort definierte Konstanten sind entsprechend nur für die bedingte Kompilierung einzusetzen.  Es gibt auch nicht definierte Konstanten mit dem Wert `Nothing`.  
  
## Beispiel  
 In diesem Beispiel wird die `#Const`\-Direktive verwendet.  
  
 [!CODE [VbVbalrConditionalComp#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrConditionalComp#3)]  
  
## Siehe auch  
 [\/define](../../../visual-basic/reference/command-line-compiler/define.md)   
 [\#If...Then...\#Else Directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md)   
 [Const Statement](../../../visual-basic/language-reference/statements/const-statement.md)   
 [Conditional Compilation](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)   
 [If...Then...Else Statement](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
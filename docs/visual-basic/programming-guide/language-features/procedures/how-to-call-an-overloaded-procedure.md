---
title: "How to: Call an Overloaded Procedure (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
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
  - "Visual Basic code, procedures"
  - "procedures, overloading"
  - "procedures, calling"
  - "procedures, multiple versions"
  - "procedure calls, overloaded"
ms.assetid: 3bb331fb-f6bc-406f-9ca0-9609b497014c
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Call an Overloaded Procedure (Visual Basic)
Der Vorteil der Prozedurüberladung liegt in der Flexibilität des Aufrufs.  Der Aufrufcode kann die Informationen abrufen, die er an die Prozedur übergeben muss, und dann unabhängig davon, welche Argumente übergeben werden, denselben Prozedurnamen verwenden.  
  
### So rufen Sie eine Prozedur auf, für die mehrere Versionen definiert sind  
  
1.  Legen Sie im Aufrufcode fest, welche Daten an die Prozedur übergeben werden sollen.  
  
2.  Schreiben Sie den Prozeduraufruf auf die übliche Weise, und geben Sie dabei die Daten in der Argumentliste an.  Stellen Sie sicher, dass die Argumente zur Parameterliste einer der Versionen passen, die für die Prozedur definiert sind.  
  
3.  Sie müssen nicht festlegen, welche Version der Prozedur aufgerufen werden soll.  [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] übergibt die Steuerung der Version, zu der die angegebene Argumentliste passt.  
  
     Im folgenden Beispiel wird die in [How to: Define Multiple Versions of a Procedure](../../../../visual-basic/programming-guide/language-features/procedures/how-to-define-multiple-versions-of-a-procedure.md) deklarierte `post`\-Prozedur aufgerufen.  Es wird die Kundenkennung abgerufen und dann ermittelt, ob es sich dabei um einen Wert vom Typ `String` oder `Integer` handelt. Anschließend wird in beiden Fällen die gleiche Prozedur aufgerufen.  
  
     [!CODE [VbVbcnProcedures#56](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#56)]  
  
     [!CODE [VbVbcnProcedures#57](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#57)]  
  
## Siehe auch  
 [Procedures](../../../../visual-basic/programming-guide/language-features/procedures/index.md)   
 [Procedure Parameters and Arguments](../../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)   
 [Procedure Overloading](../../../../visual-basic/programming-guide/language-features/procedures/procedure-overloading.md)   
 [Troubleshooting Procedures](../../../../visual-basic/programming-guide/language-features/procedures/troubleshooting-procedures.md)   
 [How to: Define Multiple Versions of a Procedure](../../../../visual-basic/programming-guide/language-features/procedures/how-to-define-multiple-versions-of-a-procedure.md)   
 [How to: Overload a Procedure that Takes Optional Parameters](../../../../visual-basic/programming-guide/language-features/procedures/how-to-overload-a-procedure-that-takes-optional-parameters.md)   
 [How to: Overload a Procedure that Takes an Indefinite Number of Parameters](../../../../visual-basic/programming-guide/language-features/procedures/how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)   
 [Considerations in Overloading Procedures](../../../../visual-basic/programming-guide/language-features/procedures/considerations-in-overloading-procedures.md)   
 [Overload Resolution](../../../../visual-basic/programming-guide/language-features/procedures/overload-resolution.md)   
 [Overloads](../../../../visual-basic/language-reference/modifiers/overloads.md)
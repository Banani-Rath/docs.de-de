---
title: "const (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "const_CSharpKeyword"
  - "const"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "const-Schlüsselwort [C#]"
ms.assetid: 79eb447c-117b-4418-933f-97c50aa472db
caps.latest.revision: 28
caps.handback.revision: 28
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# const (C#-Referenz)
Sie verwenden das `const`\-Schlüsselwort, um ein konstantes Feld oder eine konstante lokale Variable zu deklarieren.  Konstante Felder und lokale Felder sind keine Variablen und können daher nicht geändert werden.  Konstanten können Nummern, boolesche Werte, Zeichenfolgen oder ein NULL\-Verweis sein.  Erstellen Sie keine Konstante, um Informationen darzustellen, von denen Sie ausgehen, dass sie sich einmal ändern.  Verwenden Sie beispielsweise kein konstantes Feld, um den Preis einer Dienstleistung, einer Produktversionsnummer oder den Markennamen eines Unternehmens zu speichern.  Diese Werte können sich im Laufe der Zeit ändern, und da Compiler Konstanten weitergeben, muss anderer Code, der mit Ihren Bibliotheken kompiliert wird, neu kompiliert werden, damit die Änderungen sichtbar werden.  Weitere Informationen finden Sie auch unter dem [readonly](../../../csharp/language-reference/keywords/readonly.md)\-Schlüsselwort.  Beispiel:  
  
```  
  
      const int x = 0;  
public const double gravitationalConstant = 6.673e-11;  
private const string productName = "Visual C#";  
```  
  
## Hinweise  
 Der Typ einer Konstantendeklaration gibt den Typ der Member an, die durch die Deklaration eingeführt werden.  Der Initialisierer einer konstanten lokalen Variable oder eines konstanten Felds muss ein konstanter Ausdruck sein, der implizit in den Zieltyp konvertiert werden kann.  
  
 Ein konstanter Ausdruck ist ein Ausdruck, der während der Kompilierung vollständig ausgewertet werden kann.  Daher sind `string` und ein NULL\-Verweis die einzig möglichen Werte für Verweistypkonstanten.  
  
 In der Konstantendeklaration können mehrere Konstanten deklariert werden, z. B.:  
  
```  
public const double x = 1.0, y = 2.0, z = 3.0;  
```  
  
 Der `static`\-Modifizierer ist in einer Konstantendeklaration nicht zulässig.  
  
 Eine Konstante kann wie folgt einen Teil eines konstanten Ausdrucks darstellen:  
  
```  
public const int c1 = 5;  
public const int c2 = c1 + 100;  
```  
  
> [!NOTE]
>  Das [readonly](../../../csharp/language-reference/keywords/readonly.md)\-Schlüsselwort unterscheidet sich vom `const`\-Schlüsselwort.  Ein `const`\-Feld kann nur bei der Deklaration des Felds initialisiert werden.  Ein `readonly`\-Feld kann entweder bei der Deklaration oder in einem Konstruktor initialisiert werden.  Daher können `readonly`\-Felder abhängig vom verwendeten Konstruktor über unterschiedliche Werte verfügen.  Außerdem ist ein `const`\-Feld eine Kompilierzeitkonstante, während ein `readonly`\-Feld für Laufzeitkonstanten verwendet werden kann, wie in der folgenden Codezeile: `public static readonly uint l1 = (uint)DateTime.Now.Ticks;`.  
  
## Beispiel  
 [!CODE [csrefKeywordsModifiers#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#5)]  
  
## Beispiel  
 In diesem Beispiel wird das Verwenden von Konstanten als lokale Variablen demonstriert.  
  
 [!CODE [csrefKeywordsModifiers#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsModifiers#6)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [Modifizierer](../../../csharp/language-reference/keywords/modifiers.md)   
 [readonly](../../../csharp/language-reference/keywords/readonly.md)
---
title: "Overrides (Visual Basic) | Microsoft Docs"
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
  - "Overrides"
  - "vb.Overrides"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "properties [Visual Basic], redefining"
  - "procedures, overriding"
  - "procedures, redefining"
  - "overriding"
  - "Overrides keyword"
  - "overriding, Overrides keyword"
  - "properties [Visual Basic], overriding"
ms.assetid: 9f5e6144-ce10-465e-842b-1a8f8760af90
caps.latest.revision: 18
caps.handback.revision: 18
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Overrides (Visual Basic)
Gibt an, dass eine Eigenschaft oder Prozedur eine Eigenschaft oder Prozedur mit dem gleichen Namen überschreibt, die von einer Basisklasse geerbt wurde.  
  
## Hinweise  
  
## Regeln  
  
-   **Deklarationskontext.** Sie können `Overrides` nur in einer Eigenschaft oder einer Prozedurdeklarationsanweisung verwenden.  
  
-   **Kombinierte Modifizierer.** Sie können `Overrides` nicht zusammen mit `Shadows` oder `Shared` in derselben Deklaration angeben.  Da ein überschreibendes Element implizit überschreibbar ist, können Sie `Overridable` nicht mit `Overrides` kombinieren.  
  
-   **Übereinstimmende Signaturen.** Die Signatur dieser Deklaration muss genau mit der *Signatur* der Eigenschaft oder Prozedur übereinstimmen, die von der Deklaration überschrieben wird.  Das bedeutet, dass die Anzahl, die Reihenfolge und die Datentypen der Parameter in den Parameterlisten gleich sein müssen.  
  
     Neben der Signatur müssen auch die folgenden Elemente der überschreibenden Deklaration genau übereinstimmen:  
  
    -   Die Zugriffsebene  
  
    -   Der Rückgabetyp, falls vorhanden  
  
-   **Generische Signaturen.** Bei einer generischen Prozedur umfasst die Signatur die Anzahl der Typparameter.  Daher muss die überschreibende Deklaration auch in dieser Hinsicht mit der Basisklassenversion übereinstimmen.  
  
-   **Zusätzliche Übereinstimmung.** Diese Deklaration muss nicht nur in Bezug auf die Signatur, sondern auch in folgenden Punkten mit der Basisklassenversion übereinstimmen:  
  
    -   Zugriffsebenenmodifizierer \(z. B. [Public](../../../visual-basic/language-reference/modifiers/public.md)\)  
  
    -   Übergabemechanismus jedes Parameters \([ByVal](../../../visual-basic/language-reference/modifiers/byval.md) oder [ByRef](../../../visual-basic/language-reference/modifiers/byref.md)\)  
  
    -   Einschränkungslisten für jeden Typparameter einer generischen Prozedur  
  
-   **Shadowing und Überschreiben.** Sowohl das Shadowing als auch das Überschreiben definieren ein geerbtes Element neu, es gibt jedoch bedeutende Unterschiede zwischen den beiden Vorgehensweisen.  Weitere Informationen finden Sie unter [Shadowing in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md).  
  
 Beim Verwenden von `Overrides` fügt der Compiler implizit `Overloads` hinzu, sodass Ihre Bibliotheks\-APIs leichter mit C\# verwendet werden können.  
  
 Der `Overrides`\-Modifizierer kann in folgenden Kontexten verwendet werden:  
  
 [Function\-Anweisung](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Property\-Anweisung](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Sub\-Anweisung](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## Siehe auch  
 [MustOverride](../../../visual-basic/language-reference/modifiers/mustoverride.md)   
 [NotOverridable](../../../visual-basic/language-reference/modifiers/notoverridable.md)   
 [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md)   
 [Stichwörter](../../../visual-basic/language-reference/keywords/index.md)   
 [Shadowing in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)   
 [Generische Typen in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)   
 [Type List](../../../visual-basic/language-reference/statements/type-list.md)
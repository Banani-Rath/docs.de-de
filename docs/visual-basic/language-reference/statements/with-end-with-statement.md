---
title: "With...End With Statement (Visual Basic) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vb.With"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "With keyword"
  - "loop structures, and With...End With statements"
  - "execution, on object"
  - "instructions, repeating"
  - "With...End With statements"
  - "With statement"
  - "With statement, nesting"
  - "objects [Visual Basic], accessing"
  - "With block"
  - "End keyword, With...End With statements"
ms.assetid: 340d5fbb-4f43-48ec-a024-80843c137817
caps.latest.revision: 34
caps.handback.revision: 34
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# With...End With Statement (Visual Basic)
Führt eine Reihe von Anweisungen aus, die wiederholt auf ein einzelnes Objekt oder eine einzelne Struktur verweisen, sodass die Anweisungen mittels vereinfachter Syntax auf Member des Objekts oder der Struktur zugreifen können.  Wenn Sie eine Struktur verwenden, können Sie nur die Werte von Membern lesen oder Methoden aufrufen; Sie erhalten eine Fehlermeldung, wenn Sie versuchen, Werte zu Membern einer Struktur zuzuweisen, die in einer `With...End With`\-Anweisung verwendet wird.  
  
## Syntax  
  
```  
With objectExpression  
    [ statements ]  
End With  
```  
  
## Teile  
  
|||  
|-|-|  
|Ausdruck|Definition|  
|`objectExpression`|Erforderlich.  Ein Ausdruck, der zu einem Objekt ausgewertet wird.  Der Ausdruck kann von beliebiger Komplexität sein und wird nur einmal ausgewertet.  Der Ausdruck kann einen beliebigen Datentyp ergeben, u. a. auch einen elementaren Datentyp.|  
|`statements`|Optional.  Eine oder mehrere Anweisungen zwischen `With` und `End With`, die auf Member eines Objekts verweisen können, das durch die Auswertung von `objectExpression` erstellt wird.|  
|`End With`|Erforderlich.  Beendet die Definition des `With`\-Blocks.|  
  
## Hinweise  
 Bei Verwendung von `With...End With` können Sie eine Reihe von Anweisungen für ein angegebenes Objekt ausführen, ohne den Namen des Objekts mehrmals angeben zu müssen.  Innerhalb eines `With`\-Anweisungsblocks können Sie bei der Angabe eines Member des Objekts mit einem Punkt beginnen, als ob das `With`\-Anweisungsobjekt dem Member vorausgehen würde.  
  
 Wenn Sie beispielsweise mehrere verschiedene Eigenschaften eines einzelnen Objekts ändern möchten, fügen Sie die Anweisungen für die Eigenschaftenzuweisungen in den `With...End With`\-Block ein. Sie müssen dann nicht in jeder Eigenschaftenzuweisung auf das Objekt verweisen, sondern es genügt ein einziger Verweis auf das Objekt.  
  
 Wenn der Code auf dasselbe Objekt in mehreren Anweisungen zugreift, bietet die `With`\-Anweisung folgende Vorteile:  
  
-   Sie müssen einen komplexen Ausdruck nicht mehrmals auswerten oder das Ergebnis einer temporären Variablen zuweisen, auch wenn Sie mehrmals auf die Member des Ausdrucks verweisen möchten.  
  
-   Der Code wird lesbarer, da wiederkehrende qualifizierende Ausdrücke vermieden werden.  
  
 Der Datentyp `objectExpression` kann ein beliebiger Klassen\- oder Strukturtyp und sogar ein elementarer Visual Basic\-Typ sein, z. B. `Integer`.  Wenn `objectExpression` kein Objekt liefert, können Sie nur die Werte der Member lesen oder Methoden aufrufen; Sie erhalten eine Fehlermeldung, wenn Sie versuchen, Werte zu Membern einer Struktur zuzuweisen, die in einer `With...End With`\-Anweisung verwendet wird.  Denselben Fehler würden Sie erhalten, wenn Sie eine Methode aufrufen, die eine Struktur zurückgegeben hat und unmittelbar auf einen Wert zugreifen und diesen einem Member des Funktionsergebnisses zuweisen, z. B. `GetAPoint().x = 1`.  Das Problem in beiden Fällen besteht darin, dass die Struktur nur in der Aufrufliste vorhanden ist und es in solchen Fällen keine Möglichkeit für einen Member einer geänderten Struktur gibt, Daten so an eine Position zu schreiben, dass die Änderung durch anderen Code im Programm berücksichtigt werden kann.  
  
 `objectExpression` wird nach Eintragung in den Block einmal ausgewertet.  Es gibt keine Möglichkeit, `objectExpression` aus dem `With`\-Block heraus neu zuzuweisen.  
  
 In einem `With`\-Block können Sie nur auf die Methoden und Eigenschaften des angegebenen Objekts zugreifen, ohne sie zu qualifizieren.  Sie können zwar auch Methoden und Eigenschaften anderer Objekte verwenden, diese müssen Sie jedoch mit dem Objektnamen qualifizieren.  
  
 Sie können eine `With...End With`\-Anweisung in eine andere einfügen.  Geschachtelte `With...End With`\-Anweisungen sind möglicherweise unübersichtlich, wenn die Objekte, auf die verwiesen wird, aus dem Kontext heraus nicht nachvollziehbar sind.  Sie müssen einen vollqualifizierten Verweis auf ein Objekt angeben, das sich in einem äußeren `With`\-Block befindet, wenn aus einem inneren `With`\-Block auf das Objekt verwiesen wird.  
  
 Sie können von außerhalb eines Blocks keine Verzweigung in einen `With`\-Anweisungsblock vornehmen.  
  
 Sofern der Block keine Schleife enthält, werden die Anweisungen nur einmal ausgeführt.  Sie können verschiedene Arten von Steuerungsstrukturen schachteln.  Weitere Informationen finden Sie unter [Nested Control Structures](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md).  
  
> [!NOTE]
>  Das `With`\-Schlüsselwort kann auch in Objektinitialisierern verwendet werden.  Weitere Informationen und Beispiele finden Sie unter [Object Initializers: Named and Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md) und [Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).  
>   
>  Wenn Sie einen `With`\-Block nur zum Initialisieren der Eigenschaften oder Felder eines soeben instanziierten Objekts verwenden, sollten Sie stattdessen einen Objektinitialisierer verwenden.  
  
## Beispiel  
 Im folgenden Beispiel führt jeder `With`\-Block eine Reihe von Anweisungen für ein einzelnes Objekt aus.  
  
 [!CODE [VbVbalrWithStatement#2](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrwithstatement#2)]  
  
## Beispiel  
 Im folgenden Beispiel werden `With…End With`\-Anweisungen geschachtelt.  In der geschachtelten `With`\-Anweisung verweist die Syntax auf das innere Objekt.  
  
 [!CODE [VbVbalrWithStatement#1](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrwithstatement#1)]  
  
## Siehe auch  
 <xref:System.Collections.Generic.List%601>   
 [Nested Control Structures](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)   
 [Object Initializers: Named and Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)   
 [Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
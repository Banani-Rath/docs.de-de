---
title: "Comments in Code (Visual Basic) | Microsoft Docs"
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
  - "Uncomment button"
  - "REM statement"
  - "comments, in code"
  - "comments, Visual Basic code"
  - "Comment button"
  - "buttons, Uncomment"
  - "buttons, Comment"
  - "code comments, Visual Basic"
  - "Visual Basic code, comments"
  - "comments"
  - "code comments"
ms.assetid: 90136fba-22eb-49f9-ba81-63db629b4a47
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Comments in Code (Visual Basic)
Wenn Sie die Codebeispiele lesen, werden Sie oft auf das Kommentarsymbol \(`'`\) stoßen.  Dieses Symbol weist den [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler an, den darauf folgenden Text, also den *Kommentar*, zu ignorieren.  Kommentare sind kurze, erläuternde Hinweise, die dem Code zum Zwecke der besseren Verständlichkeit hinzugefügt werden.  
  
 Es gilt als guter Programmierstil, alle Prozeduren mit einem kurzen Kommentar zu beginnen, der die Funktionsmerkmale der Prozedur \(ihre Aufgabe\) beschreibt.  Dies ist zu Ihrem eigenen Nutzen und zum Nutzen jeder anderen Person, die den Code liest.  Dabei ist es sinnvoll, die Einzelheiten der Implementierung, d. h., wie die Prozedur funktioniert, von den Kommentaren abzugrenzen, in denen die funktionalen Eigenschaften beschrieben werden.  Falls Sie in einem Kommentar Einzelheiten der Implementierung beschreiben, denken Sie daran, diese entsprechend zu aktualisieren, wenn Sie die Funktion ändern.  
  
 Kommentare können nach einer Anweisung in der gleichen Zeile eingefügt werden oder eine ganze Zeile belegen.  Beide Fälle werden im folgenden Code veranschaulicht:  
  
 [!CODE [VbVbcnConventions#16](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnConventions#16)]  
  
 Wenn der Kommentar mehr als eine Zeile beansprucht, verwenden Sie das Kommentarsymbol in jeder neuen Zeile, wie im folgenden Beispiel veranschaulicht.  
  
 [!CODE [VbVbcnConventions#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnConventions#17)]  
  
## Richtlinien für Kommentare  
 Die folgende Tabelle enthält allgemeine Richtlinien für die verschiedenen Arten von Kommentaren, die einem Codeabschnitt vorangestellt werden können.  Diese Richtlinien sind als Empfehlungen gedacht, da [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] keine Regeln für das Hinzufügen von Kommentaren erzwingt.  Wenden Sie diese Empfehlungen so an, wie sie für Sie und andere Leser am sinnvollsten sind.  
  
|||  
|-|-|  
|Kommentartyp|Kommentarbeschreibung|  
|Zweck|Hier wird beschrieben, was die Prozedur bewirkt \(nicht, wie sie dies bewirkt\).|  
|Annahmen|Listet alle externen Variablen, Steuerelemente, offenen Dateien und andere Elemente auf, auf die die Prozedur zugreift.|  
|Effekte|Hier werden die einzelnen betroffenen externen Variablen, Steuerelemente oder Dateien sowie deren Auswirkungen genannt \(falls dies nicht offensichtlich ist\).|  
|Eingaben|Gibt den Zweck des Arguments an.|  
|Rückgabe|Erläutert die von der Prozedur zurückgegebenen Werte.|  
  
 Beachten Sie Folgendes:  
  
-   Vor jeder wichtigen Variablendeklaration sollte ein Kommentar stehen, der Sinn und Zweck der deklarierten Variablen beschreibt.  
  
-   Variablen, Steuerelemente und Prozeduren sollten so klar benannt werden, dass Kommentare nur für komplexe Implementierungsdetails erforderlich sind.  
  
-   Auf eine Zeilenfortsetzungszeichenfolge darf nicht in der gleichen Zeile ein Kommentar folgen.  
  
 Sie können Kommentarsymbole für einen Codeblock hinzufügen bzw. entfernen, indem Sie eine oder mehrere Codezeilen markieren und auf der Symbolleiste **Bearbeiten** auf die Schaltflächen **Auswahl kommentieren** \(![VisualBasicWinAppCodeEditorCommentButton](../../../visual-basic/programming-guide/program-structure/media/vacommentbutton.png "vaCommentButton")\) bzw. **Auswahlkommentar löschen** \(![VisualStudioWinAppProjectUncommentButton](../../../visual-basic/programming-guide/program-structure/media/vauncommentbutton.png "vaUncommentButton")\) klicken.  
  
> [!NOTE]
>  Sie können Code auch Kommentare hinzufügen, indem Sie vor dem betreffenden Text das `REM`\-Schlüsselwort einfügen.  Das `'`\-Symbol und die Schaltflächen **Auswahl kommentieren**\/**Auswahlkommentar löschen** sind jedoch einfacher zu verwenden und beanspruchen weniger Platz auf dem Bildschirm und Speicherplatz.  
  
## Siehe auch  
 [Dokumentieren von Code mit XML\-Kommentaren](http://msdn.microsoft.com/magazine/dd722812.aspx)   
 [How to: Create XML Documentation](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)   
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)   
 [Programmstruktur und Codekonventionen](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)   
 [REM Statement](../../../visual-basic/language-reference/statements/rem-statement.md)
---
title: "How to: Initialize an Array Variable in Visual Basic | Microsoft Docs"
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
  - "variables [Visual Basic], initializing"
  - "arrays [Visual Basic], variables"
  - "arrays [Visual Basic], initializing"
  - "arrays [Visual Basic], declaring"
ms.assetid: aadd7a60-7ca4-4608-b986-091f19e7fc10
caps.latest.revision: 42
caps.handback.revision: 42
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Initialize an Array Variable in Visual Basic
Sie initialisieren eine Arrayvariable, in dem Sie ein Arrayliteral in einer `New`\-Klausel einfügen und die Anfangswerte des Arrays angeben.  Sie können den Typ angeben oder ihn von den Werten im Arrayliteral ableiten lassen.  Weitere Informationen zum Ableiten des Typs finden Sie unter "Auffüllen eines Arrays mit Anfangswerten" in [Arrays](../../../../visual-basic/programming-guide/language-features/arrays/index.md).  
  
### So initialisieren Sie eine Arrayvariable mit einem Arrayliteral  
  
-   Geben Sie die Elementwerte in der `New`\-Klausel oder beim Zuweisen des Arraywerts in geschweiften Klammern \(`{}`\) an.  Im folgenden Beispiel werden mehrere Möglichkeiten veranschaulicht, wie Variablen so deklariert, erstellt und initialisiert werden können, dass sie ein Array mit Elementen vom Typ `Char` enthalten.  
  
     [!CODE [VbVbalrArrays#16](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrArrays#16)]  
  
     Nach der Ausführung jeder Anweisung hat das erstellte Array die Länge 3, wobei die Elemente von Index 0 bis Index 2 die Anfangswerte enthalten.  Wenn Sie sowohl die Obergrenze als auch die Werte angeben, müssen Sie für jedes Element von Index 0 bis zur Obergrenze einen Wert einfügen.  
  
     Beachten Sie, dass Sie keine Indexobergrenze angeben müssen, wenn Elementwerte in einem Arrayliteral bereitgestellt werden.  Wenn keine Obergrenze angegeben wird, wird die Größe des Arrays anhand der Anzahl der Werte im Arrayliteral abgeleitet.  
  
### So initialisieren Sie eine mehrdimensionale Arrayvariable mit Arrayliteralen  
  
-   Schachteln Sie Werte in geschweiften Klammern \(`{}`\) in geschweiften Klammern.  Stellen Sie sicher, dass alle geschachtelten Arrayliterale als Arrays des gleichen Typs und mit derselben Länge abgeleitet werden.  Im folgenden Codebeispiel werden mehrere Beispiele für die Initialisierung mehrdimensionaler Arrays veranschaulicht.  
  
     [!CODE [VbVbalrArrays#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrArrays#17)]  
  
-   Sie können die Arraygrenzen explizit angeben oder diese Angabe auslassen, sodass der Compiler die Arraygrenzen von den Werten im Arrayliteral ableitet.  Wenn Sie sowohl die Obergrenzen als auch die Werte vorgeben, müssen Sie in jeder Dimension für jedes Element von Index 0 bis zur Obergrenze einen Wert angeben.  Im folgenden Beispiel werden mehrere Möglichkeiten veranschaulicht, wie Variablen so deklariert, erstellt und initialisiert werden können, dass sie ein zweidimensionales Array mit Elementen vom Typ `Short` enthalten.  
  
     [!CODE [VbVbalrArrays#18](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrArrays#18)]  
  
     Nach der Ausführung jeder Anweisung enthält das erstellte Array sechs initialisierte Elemente mit den Indizes `(0,0)`, `(0,1)`, `(0,2)`, `(1,0)`, `(1,1)` und `(1,2)`.  Jede Arrayposition enthält den Wert `10`.  
  
-   Im folgenden Beispiel wird ein mehrdimensionales Array durchlaufen.  Fügen Sie den Code in einer Windows\-Konsolenanwendung, die in Visual Basic geschrieben wurde, in die `Sub Main()`\-Methode ein.  Die letzten Kommentare zeigen die Ausgabe an.  
  
     [!CODE [VbVbalrArrays#31](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrArrays#31)]  
  
### So initialisieren Sie eine verzweigte Arrayvariable mit Arrayliteralen  
  
-   Schachteln Sie Objektwerte in geschweiften Klammern \(`{}`\).  Sie können zwar auch Arrayliterale schachteln, die Arrays von verschiedener Länge angeben, stellen Sie jedoch bei einem verzweigten Array sicher, dass die geschachtelten Arrayliterale in runden Klammern \(`()`\) eingeschlossen sind.  Durch die Klammern wird die Auswertung der geschachtelten Arrayliterale erzwungen, und die erhaltenen Arrays werden als Anfangswerte des verzweigten Arrays verwendet.  Im folgenden Codebeispiel werden zwei Beispiele für die Initialisierung verzweigter Arrays veranschaulicht.  
  
     [!CODE [VbVbalrArrays#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrArrays#19)]  
  
-   Im folgenden Beispiel wird ein verzweigtes Array durchlaufen.  Fügen Sie den Code in einer Windows\-Konsolenanwendung, die in Visual Basic geschrieben wurde, in die `Sub Main()`\-Methode ein.  Die letzten Kommentare im Code zeigen die Ausgabe an.  
  
     [!CODE [VbVbalrArrays#32](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrArrays#32)]  
  
## Siehe auch  
 [Arrays](../../../../visual-basic/programming-guide/language-features/arrays/index.md)   
 [Troubleshooting Arrays](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)
---
title: "Main() und Befehlszeilenargumente (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "CS5001"
  - "main_CSharpKeyword"
  - "Main"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Argumente [C#], Befehlszeile"
  - "C#-Sprache, Befehlszeilenargumente"
  - "Befehlszeile [C#], Argumente"
  - "Befehlszeilenargumente [C#], Main-Methode"
  - "Main-Methode [C#]"
ms.assetid: 73a17231-cf96-44ea-aa8a-54807c6fb1f4
caps.latest.revision: 30
caps.handback.revision: 30
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Main() und Befehlszeilenargumente (C#-Programmierhandbuch)
Die `Main`\-Methode ist der Einstiegspunkt einer C\#\-Konsolenanwendung oder einer Windows\-Anwendung.  \(Für Bibliotheken und Dienste ist keine `Main`\-Methode als Einstiegspunkt erforderlich.\).  Wenn die Anwendung gestartet wird, ist die `Main`\-Methode die erste Methode, die aufgerufen wird.  
  
 Es kann nur einen Einstiegspunkt in einem C\#\-Programm geben.  Wenn mehrere Klassen vorliegen, die eine `Main`\-Methode aufweisen, müssen Sie Ihr Programm mit der **\/main**\-Compileroption kompilieren, um festzulegen, welche `Main`\-Methode als Einstiegspunkt verwendet werden soll.  Weitere Informationen hierzu finden Sie unter [\/main \(Specify Location of Main Method\)](../../../csharp/language-reference/compiler-options/main-compiler-option.md).  
  
 [!CODE [csProgGuideMain#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideMain#17)]  
  
## Übersicht  
  
-   Die `Main`\-Methode ist der Einstiegspunkt eines EXE\-Programms. Dies ist der Punkt, an dem die Programmsteuerung beginnt und endet.  
  
-   `Main` wird in einer Klasse oder einer Struktur deklariert.  `Main` muss [statisch](../../../csharp/language-reference/keywords/static.md) sein und darf nicht [Öffentlich](../../../csharp/language-reference/keywords/public.md) sein.  \(Im Beispiel oben erhält sie den Standardzugriff [private](../../../csharp/language-reference/keywords/private.md).\) Die einschließende Klasse oder die Struktur muss nicht statisch sein.  
  
-   `Main` kann entweder einen `void`\-Rückgabetyp oder einen `int`\-Rückgabetyp aufweisen.  
  
-   Die `Main`\-Methode kann mit oder ohne einen `string[]`\-Parameter deklariert werden, der Befehlszeilenargumente enthält.  Wenn Sie [!INCLUDE[vsprvs](../../../csharp/includes/vsprvs_md.md)] zum Erstellen von Windows Forms\-Anwendungen verwenden, können Sie den Parameter manuell hinzufügen oder anderenfalls die <xref:System.Environment>\-Klasse zum Abrufen der Befehlszeilenargumente verwenden.  Parameter werden als nullbasierte Befehlszeilenargumente gelesen. Im Gegensatz zu C und C\+\+ wird der Name des Programms nicht als Erstes Befehlszeilenargument behandelt.  
  
## In diesem Abschnitt  
  
-   [Befehlszeilenargumente](../../../csharp/programming-guide/main-and-command-args/command-line-arguments.md)  
  
-   [Gewusst wie: Anzeigen von Befehlszeilenargumenten](../../../csharp/programming-guide/main-and-command-args/how-to-display-command-line-arguments.md)  
  
-   [Gewusst wie: Zugreifen auf Befehlszeilenargumente mithilfe von foreach](../../../csharp/programming-guide/main-and-command-args/how-to-access-command-line-arguments-using-foreach.md)  
  
-   [Main\(\)\-Rückgabewerte](../../../csharp/programming-guide/main-and-command-args/main-return-values.md)  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [Command\-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Methoden](../../../csharp/programming-guide/classes-and-structs/methods.md)   
 [Einblicke in ein C\#\-Programm](../../../csharp/programming-guide/inside-a-program/index.md)   
 [\<paveover\>C\# Sample Applications](http://msdn.microsoft.com/de-de/9a9d7aaa-51d3-4224-b564-95409b0f3e15)
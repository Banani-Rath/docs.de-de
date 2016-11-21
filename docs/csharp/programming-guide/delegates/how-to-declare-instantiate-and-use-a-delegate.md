---
title: "Gewusst wie: Deklarieren, Instanziieren und Verwenden von Delegaten (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Delegaten [C#], Deklarieren und Instanziieren von"
ms.assetid: 61c4895f-f785-48f8-8bfe-db73b411c4ae
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Deklarieren, Instanziieren und Verwenden von Delegaten (C#-Programmierhandbuch)
In C\# 1.0 und höher können Delegaten wie im folgenden Beispiel gezeigt deklariert werden.  
  
 [!CODE [csProgGuideDelegates#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#13)]  
  
 [!CODE [csProgGuideDelegates#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#14)]  
  
 C\# 2.0 bietet eine einfachere Möglichkeit zum Schreiben dieser Deklaration, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csProgGuideDelegates#32](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#32)]  
  
 In C\# 2.0 und höher kann auch eine anonyme Methode verwendet werden, um einen [Delegaten](../../../csharp/language-reference/keywords/delegate.md) zu deklarieren und initialisieren, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csProgGuideDelegates#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#15)]  
  
 In C\# 3.0 und höher können Delegaten auch mit einem Lambda\-Ausdruck deklariert und instanziiert werden, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csProgGuideDelegates#31](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#31)]  
  
 Weitere Informationen finden Sie unter [Lambda\-Ausdrücke](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md).  
  
 Im folgenden Beispiel wird verdeutlicht, wie Sie einen Delegaten deklarieren, instanziieren und verwenden.  In der `BookDB`\-Klasse ist eine Buchhandlungsdatenbank gekapselt, die eine Buchtiteldatenbank enthält.  Sie stellt eine `ProcessPaperbackBooks`\-Methode zur Verfügung, durch die alle Taschenbücher in der Datenbank gefunden und für jedes Taschenbuch ein Delegat aufgerufen wird.  Der verwendete `delegate`\-Typ hat den Namen `ProcessBookDelegate`.  Die `Test`\-Klasse verwendet diese Klasse, um die Buchtitel und Durchschnittspreise der Taschenbücher auszugeben.  
  
 Die Verwendung von Delegaten beinhaltet eine sinnvolle Trennung der Funktionalitäten von Buchhandlungsdatenbank und Clientcode.  Der Clientcode weiß nicht, wie die Bücher archiviert werden oder wie der Buchhandlungscode Taschenbücher sucht.  Der Buchhandlungscode wiederum weiß nicht, wie ein Taschenbuchtitel weiterverarbeitet wird, nachdem er gefunden wurde.  
  
## Beispiel  
 [!CODE [csProgGuideDelegates#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#12)]  
  
## Robuste Programmierung  
  
-   Deklarieren von Delegaten  
  
     Mit der folgenden Anweisung wird ein neuer Delegattyp deklariert.  
  
     [!CODE [csProgGuideDelegates#16](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#16)]  
  
     Durch die einzelnen Delegattypen werden Anzahl und Typen von Argumenten sowie Rückgabewerte von Methoden beschrieben, die gekapselt können.  Sobald neue Argumenttypen oder ein neuer Rückgabewerttyp erforderlich ist, muss ein neuer Delegattyp deklariert werden.  
  
-   Instanziieren von Delegaten  
  
     Nachdem ein Delegattyp deklariert wurde, muss ein Delegatobjekt erstellt und mit einer bestimmten Methode verknüpft werden.  Im vorherigen Beispiel übergeben Sie dazu die `PrintTitle`\-Methode an die `ProcessPaperbackBooks`\-Methode, wie im folgenden Beispiel gezeigt:  
  
     [!CODE [csProgGuideDelegates#17](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#17)]  
  
     Hierdurch wird ein neues Delegatobjekt erstellt, das mit der [static](../../../csharp/language-reference/keywords/static.md)\-Methode verknüpft ist `Test.PrintTitle`.  Auf ähnliche Weise wird die nicht statische `AddBookToTotal`\-Methode für das `totaller`\-Objekt wie im folgenden Beispiel übergeben:  
  
     [!CODE [csProgGuideDelegates#18](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#18)]  
  
     In beiden Fällen wird ein neues Delegatobjekt an die `ProcessPaperbackBooks`\-Methode übergeben.  
  
     Nach der Erstellung eines Delegaten wird die mit diesem verknüpfte Methode nicht mehr geändert. Delegatobjekte sind unveränderlich.  
  
-   Aufrufen von Delegaten  
  
     Nachdem ein Delegatobjekt erstellt wurde, wird es normalerweise an anderen Code übergeben, durch den der Delegat aufgerufen wird.  Ein Delegatobjekt wird über seinen Namen aufgerufen. Auf den Namen folgen \(in Klammern gesetzte\) Argumente, die an den Delegaten übergeben werden sollen.  Es folgt ein Beispiel für einen Delegataufruf:  
  
     [!CODE [csProgGuideDelegates#19](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDelegates#19)]  
  
     Ein Delegat kann entweder \(wie in diesem Beispiel\) synchron oder mithilfe der `BeginInvoke`\-Methode und der `EndInvoke`\-Methode asynchron aufgerufen werden.  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Ereignisse](../../../csharp/programming-guide/events/index.md)   
 [Delegaten](../../../csharp/programming-guide/delegates/index.md)
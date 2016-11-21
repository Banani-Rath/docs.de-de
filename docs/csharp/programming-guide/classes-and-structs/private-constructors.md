---
title: "Private Konstruktoren (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "C#-Sprache, Private Konstruktoren"
  - "Private Konstruktoren [C#]"
ms.assetid: 29eeaa7d-8d81-453c-94b9-0e2800172621
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Private Konstruktoren (C#-Programmierhandbuch)
Ein privater Konstruktor ist ein spezieller Instanzkonstruktor.  Er wird meistens für Klassen verwendet, die nur statische Member enthalten.  Wenn eine Klasse über einen oder mehrere private und keine öffentlichen Konstruktoren verfügt, können andere Klassen \(außer geschachtelte Klassen\) keine Instanzen dieser Klasse erstellen.  Beispiele:  
  
 [!CODE [csProgGuideObjects#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#11)]  
  
 Die Deklaration des leeren Konstruktors verhindert die automatische Erstellung eines Standardkonstruktors.  Beachten Sie, dass bei nicht erfolgter Verwendung eines Zugriffsmodifizierers mit dem Konstruktor dieser standardmäßig weiterhin privat ist.  Der [private](../../../csharp/language-reference/keywords/private.md)\-Modifizierer wird jedoch in der Regel verwendet, um explizit festzulegen, dass die Klasse nicht instanziiert werden kann.  
  
 Mithilfe von privaten Konstruktoren kann das Erstellen von Instanzen einer Klasse verhindert werden, wenn keine Instanzfelder oder Instanzmethoden vorhanden sind, wie es beispielsweise bei <xref:System.Math> der Fall ist, oder wenn eine Methode zum Erstellen einer Instanz einer Klasse aufgerufen wird.  Wenn alle Methoden in der Klasse statisch sind, sollten Sie in Betracht ziehen, die gesamte Klasse statisch zu machen.  Weitere Informationen finden Sie unter [Statische Klassen und statische Klassenmember](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).  
  
## Beispiel  
 Im Folgenden sehen Sie ein Beispiel für eine Klasse, die einen privaten Konstruktor verwendet.  
  
 [!CODE [csProgGuideObjects#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#12)]  
  
 Beachten Sie, dass das Auskommentieren der folgenden Anweisung aus dem Beispiel einen Fehler verursacht, da auf den Konstruktor aufgrund seiner Sicherheitsebene nicht zugegriffen werden kann:  
  
 [!CODE [csProgGuideObjects#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#13)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Klassen und Strukturen](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Konstruktoren](../../../csharp/programming-guide/classes-and-structs/constructors.md)   
 [Destruktoren](../../../csharp/programming-guide/classes-and-structs/destructors.md)   
 [Private](../../../csharp/language-reference/keywords/private.md)   
 [public](../../../csharp/language-reference/keywords/public.md)
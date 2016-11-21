---
title: "How to: Create XML Documentation in Visual Basic | Microsoft Docs"
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
  - "XML comments"
  - "XML documentation, creating"
ms.assetid: 27b5b06c-09b9-496a-8245-f9542d846230
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Create XML Documentation in Visual Basic
In diesem Beispiel wird veranschaulicht, wie dem Code XML\-Dokumentationskommentare hinzugefügt werden.  
  
 [!INCLUDE[note_settings_general](../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### So erstellen Sie eine XML\-Dokumentation für einen Typ oder einen Member  
  
1.  Bewegen Sie den Cursor im **Code\-Editor** in die Zeile über dem Typ oder Member, zu dem eine Dokumentation erstellt werden soll.  
  
2.  Geben Sie `'''` \(drei einfache Anführungszeichen\) ein.  
  
     Im **Code\-Editor** wird ein XML\-Skelett für den Typ oder Member hinzugefügt.  
  
3.  Fügen Sie beschreibende Informationen zwischen den entsprechenden Tags hinzu.  
  
    > [!NOTE]
    >  Wenn Sie zusätzliche Zeilen innerhalb des XML\-Dokumentationsblocks hinzufügen, muss jede Zeile mit `'''` anfangen.  
  
4.  Fügen Sie weiteren Code hinzu, in dem der Typ oder der Member mit den neuen XML\-Dokumentationskommentaren verwendet wird.  
  
     IntelliSense zeigt den Text aus dem \< summary \>\-Tag für den Typ oder den Member an.  
  
5.  Kompilieren Sie den Code, um eine XML\-Datei zu generieren, die die Dokumentationskommentare enthält.  Weitere Informationen finden Sie unter [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md).  
  
## Siehe auch  
 [Documenting Your Code with XML](../../../visual-basic/programming-guide/program-structure/documenting-your-code-with-xml.md)   
 [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)   
 [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md)
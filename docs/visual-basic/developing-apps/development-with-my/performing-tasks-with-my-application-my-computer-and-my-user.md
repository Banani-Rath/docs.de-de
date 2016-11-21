---
title: "Performing Tasks with My.Application, My.Computer, and My.User (Visual Basic) | Microsoft Docs"
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
  - "My.Application object, developing applications"
  - "rapid application development (RAD), My.Application"
  - "rapid application development (RAD), My.Computer"
  - "rapid application development (RAD), My.User"
  - "My.Computer object, developing applications"
  - "My.User object, developing applications"
ms.assetid: c8af61bd-4dd3-4a0f-9af5-795b594b240b
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Performing Tasks with My.Application, My.Computer, and My.User (Visual Basic)
Die drei zentralen `My`\-Objekte, die Zugriff auf Informationen und häufig verwendete Funktionen bereitstellen, sind `My.Application` \(<xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>\), `My.Computer` \(<xref:Microsoft.VisualBasic.Devices.Computer>\) und `My.User` \(<xref:Microsoft.VisualBasic.ApplicationServices.User>\).  Mit diesen Objekten können Sie auf Informationen zugreifen, die sich auf die aktuelle Anwendung, den Computer, auf dem die Anwendung installiert ist, sowie auf den aktuellen Benutzer der Anwendung beziehen.  
  
## My.Application, My.Computer und My.User  
 Die folgenden Beispiele veranschaulichen das Abrufen von Informationen mit `My`.  
  
 [!CODE [VbVbcnMy#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#1)]  
  
 [!CODE [VbVbcnMy#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#2)]  
  
 Neben dem Abrufen von Informationen ermöglichen die Member, die von diesen drei Objekten bereitgestellt werden, die Ausführung von Methoden mit dem jeweiligen Objekt.  So können Sie z. B. auf eine Vielzahl an Methoden zur Manipulation von Dateien zugreifen oder die Registrierung mithilfe von `My.Computer` aktualisieren.  
  
 Datei\-E\/A\-Operationen sind mit `My` wesentlich einfacher und schneller, da es eine Reihe von Methoden und Eigenschaften für die Bearbeitung von Dateien, Verzeichnissen und Laufwerken enthält.  Mit dem <xref:Microsoft.VisualBasic.FileIO.TextFieldParser>\-Objekt können Sie große strukturierte Dateien lesen, die Felder mit Begrenzungen oder Felder mit fester Breite enthalten.  In diesem Beispiel wird der `reader` von `TextFieldParser` geöffnet und zum Lesen von `C:\TestFolder1\test1.txt` verwendet.  
  
 [!CODE [VbVbalrTextFieldParser#23](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTextFieldParser#23)]  
  
 Mit `My.Application` können Sie die Kultur für die Anwendung ändern.  Das folgende Beispiel veranschaulicht den Aufruf dieser Methode.  
  
 [!CODE [VbVbcnMy#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnMy#3)]  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>   
 <xref:Microsoft.VisualBasic.Devices.Computer>   
 <xref:Microsoft.VisualBasic.ApplicationServices.User>   
 [How My Depends on Project Type](../../../visual-basic/developing-apps/development-with-my/how-my-depends-on-project-type.md)
---
title: "/nowin32manifest (Visual Basic) | Microsoft Docs"
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
  - "/nowin32manifest compiler option [Visual Basic]"
  - "nowin32manifest compiler option [Visual Basic]"
  - "-nowin32manifest compiler option [Visual Basic]"
ms.assetid: c0528aae-83b3-4425-99f0-19448e9843e3
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# /nowin32manifest (Visual Basic)
Weist den Compiler an, kein Anwendungsmanifest in die ausführbare Datei einzubetten.  
  
## Syntax  
  
```  
/nowin32manifest  
```  
  
## Hinweise  
 Wenn Sie diese Option verwenden, unterliegt die Anwendung der Virtualisierung unter Windows Vista, es sei denn, Sie stellen ein Anwendungsmanifest in einer Win32\-Ressourcendatei oder bei einem späteren Buildschritt bereit.  Weitere Informationen über Virtualisierung finden Sie unter [ClickOnce Deployment on Windows Vista](/visual-studio/deployment/clickonce-deployment-on-windows-vista).  
  
 Weitere Informationen über das Erstellen von Manifesten finden Sie unter [\/win32manifest](../../../visual-basic/reference/command-line-compiler/win32manifest.md).  
  
## Siehe auch  
 [Visual Basic Command\-Line Compiler](../../../visual-basic/reference/command-line-compiler/index.md)   
 [Seite "Anwendung", Projekt\-Designer \(Visual Basic\)](/visual-studio/ide/reference/application-page-project-designer-visual-basic)
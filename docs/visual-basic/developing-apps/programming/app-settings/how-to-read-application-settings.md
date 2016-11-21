---
title: "How to: Read Application Settings in Visual Basic | Microsoft Docs"
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
  - "reading application settings"
  - "My.Settings object, reading application settings"
  - "application settings, reading"
ms.assetid: eb3428ef-115e-49a8-a878-e0613183fee0
caps.latest.revision: 12
caps.handback.revision: 12
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Read Application Settings in Visual Basic
Sie können eine Benutzereinstellung lesen, indem Sie auf die zugehörige Eigenschaft im `My.Settings`\-Objekt zugreifen.  
  
 Das `My.Settings`\-Objekt macht alle Einstellungen als Eigenschaft verfügbar.  Der Eigenschaftenname entspricht dem Namen der Einstellung, und der Eigenschaftentyp entspricht dem Typ der Einstellung.  Der **Bereich** einer Einstellung bestimmt, ob die zugehörige Eigenschaft schreibgeschützt ist: Die Eigenschaft für eine Einstellung mit dem Bereich **Anwendung** ist schreibgeschützt, während die Eigenschaft für eine Einstellung mit dem Bereich **Benutzer** Lese\-\/Schreibzugriff ermöglicht.  Weitere Informationen finden Sie unter [My.Settings Object](../../../../visual-basic/language-reference/objects/my-settings-object.md).  
  
## Beispiel  
 In diesem Beispiel wird der Wert der `Nickname`\-Einstellung angezeigt.  
  
 [!CODE [VbVbalrMyResources#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#14)]  
  
 Damit dieses Beispiel ausgeführt werden kann, muss die Anwendung über die `Nickname`\-Einstellung vom Typ `String` verfügen.  Weitere Informationen finden Sie unter [Verwalten von Anwendungseinstellungen \(.NET\)](/visual-studio/ide/managing-application-settings-dotnet).  
  
## Siehe auch  
 [My.Settings Object](../../../../visual-basic/language-reference/objects/my-settings-object.md)   
 [How to: Change User Settings in Visual Basic](../../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)   
 [How to: Persist User Settings in Visual Basic](../../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)   
 [How to: Create Property Grids for User Settings in Visual Basic](../../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)   
 [Verwalten von Anwendungseinstellungen \(.NET\)](/visual-studio/ide/managing-application-settings-dotnet)
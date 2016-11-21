---
title: "My.Settings Object | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "My.MySettingsProperty.Settings"
  - "My.Settings"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "My.Settings object"
ms.assetid: 41f30dc1-202a-4273-b9b7-5728941f996c
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# My.Settings Object
Stellt Eigenschaften und Methoden für den Zugriff auf die Einstellungen der Anwendung bereit.  
  
## Hinweise  
 Das `My.Settings`\-Objekt bietet Zugriff auf die Anwendungseinstellungen und ermöglicht es, die Eigenschafteneinstellungen und andere Informationen über die Anwendung dynamisch zu speichern und abzurufen.  Weitere Informationen finden Sie unter [Verwalten von Anwendungseinstellungen \(.NET\)](/visual-studio/ide/managing-application-settings-dotnet).  
  
## Eigenschaften  
 Die Eigenschaften des `My.Settings`\-Objekts ermöglichen den Zugriff auf die Einstellungen der Anwendung.  Um Einstellungen hinzuzufügen oder zu entfernen, verwenden Sie den **Einstellungs\-Designer**.  
  
 Jede Einstellung verfügt über **Name**, **Typ**, **Bereich** und **Wert**, und diese Einstellungen bestimmen, wie die Eigenschaft für den Zugriff auf die einzelnen Einstellungen im `My.Settings`\-Objekt dargestellt wird:  
  
-   **Name** bestimmt den Namen der Eigenschaft.  
  
-   **Typ** bestimmt den Typ der Eigenschaft.  
  
-   **Bereich** gibt an, ob die Eigenschaft schreibgeschützt ist.  Wenn der Wert **Anwendung** lautet, ist die Eigenschaft schreibgeschützt, und wenn der Wert **Benutzer** lautet, weist die Eigenschaft Lese\-\/Schreibzugriff auf.  
  
-   **Wert** ist der Standardwert der Eigenschaft.  
  
## Methoden  
  
|||  
|-|-|  
|Methode|Beschreibung|  
|`Reload`|Lädt die Benutzereinstellungen mit den letzten gespeicherten Werten erneut.|  
|`Save`|Speichert die aktuellen Benutzereinstellungen.|  
  
 Das `My.Settings`\-Objekt stellt auch erweiterte Eigenschaften und Methoden bereit, die von der <xref:System.Configuration.ApplicationSettingsBase>\-Klasse geerbt werden.  
  
## Aufgaben  
 In der folgenden Tabelle werden Beispiele für Aufgaben mit dem `My.Settings`\-Objekt aufgeführt.  
  
|||  
|-|-|  
|To|Siehe|  
|Lesen einer Anwendungseinstellung|[How to: Read Application Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)|  
|Ändern einer Benutzereinstellung|[How to: Change User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)|  
|Beibehalten von Benutzereinstellungen|[How to: Persist User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)|  
|Erstellen eines Eigenschaftenrasters für Benutzereinstellungen|[How to: Create Property Grids for User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)|  
  
## Beispiel  
 In diesem Beispiel wird der Wert der `Nickname`\-Einstellung angezeigt.  
  
 [!CODE [VbVbalrMyResources#14](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyResources#14)]  
  
 Damit dieses Beispiel ausgeführt werden kann, muss die Anwendung über die `Nickname`\-Einstellung vom Typ `String` verfügen.  
  
## Siehe auch  
 <xref:System.Configuration.ApplicationSettingsBase>   
 [How to: Read Application Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-read-application-settings.md)   
 [How to: Change User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-change-user-settings.md)   
 [How to: Persist User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-persist-user-settings.md)   
 [How to: Create Property Grids for User Settings in Visual Basic](../../../visual-basic/developing-apps/programming/app-settings/how-to-create-property-grids-for-user-settings.md)   
 [Verwalten von Anwendungseinstellungen \(.NET\)](/visual-studio/ide/managing-application-settings-dotnet)
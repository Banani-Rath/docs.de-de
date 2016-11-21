---
title: "How to: Check Connection Status in Visual Basic | Microsoft Docs"
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
  - "Web connections"
  - "IsAvailable property, about IsAvailable"
  - "connections, checking status"
  - "connection status"
ms.assetid: 4d9ee8ab-9a6f-4279-ace4-b75afc976a74
caps.latest.revision: 26
caps.handback.revision: 26
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Check Connection Status in Visual Basic
Mithilfe der <xref:Microsoft.VisualBasic.Devices.Network.IsAvailable%2A>\-Eigenschaft kann bestimmt werden, ob ein Computer über eine funktionierende Netzwerk\- oder Internetverbindung verfügt.  
  
 [!INCLUDE[note_settings_general](../../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### So überprüfen Sie, ob ein Computer über eine funktionierende Verbindung verfügt  
  
-   Ermitteln Sie, ob die `IsAvailable`\-Eigenschaft `True` oder `False` ist.  Im folgenden Code wird der Status der Eigenschaft überprüft und ausgegeben:  
  
     [!CODE [VbResourceTasks#3](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#3)]  
  
     Dieses Codebeispiel ist auch als IntelliSense\-Codeausschnitt verfügbar.  Sie finden das Element in der Codeausschnittauswahl unter **Connectivity and Networking**.  Weitere Informationen finden Sie unter [Codeausschnitte](/visual-studio/ide/code-snippets).  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.Devices.Network?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Devices.Network.IsAvailable%2A>
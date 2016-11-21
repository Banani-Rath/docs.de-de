---
title: "Some subkeys cannot be deleted | Microsoft Docs"
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
ms.assetid: 14562137-af43-4972-84c1-a380a90f7d6c
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Some subkeys cannot be deleted
Es wurde versucht, einen Registrierungsschlüssel zu löschen, doch der Vorgang ist fehlgeschlagen, weil einige Unterschlüssel nicht gelöscht werden können.  Die Ursache hierfür sind i. d. R. fehlende Berechtigungen.  
  
### So beheben Sie diesen Fehler  
  
-   Stellen Sie sicher, dass Sie über ausreichende Berechtigungen zum Löschen der angegebenen Unterschlüssel verfügen.  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.MyServices.RegistryProxy?displayProperty=fullName>   
 <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%2A>   
 <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%2A>   
 <xref:System.Security.Permissions.RegistryPermission>
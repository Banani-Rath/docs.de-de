---
title: "Lesen von der und Schreiben in die Registrierung mithilfe des Microsoft.Win32-Namespaces (Visual Basic) | Microsoft Docs"
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
  - "Registrierung, Visual Basic"
ms.assetid: 4a0dcce0-c27b-4199-baa8-ee4528da6a56
caps.latest.revision: 20
caps.handback.revision: 20
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Lesen von der und Schreiben in die Registrierung mithilfe des Microsoft.Win32-Namespaces (Visual Basic)
Obwohl `My.Computer.Registry` alle Ihre Basisanforderungen beim Programmieren der Registrierung abdecken soll, können Sie alternativ die Klassen <xref:Microsoft.Win32.Registry> und <xref:Microsoft.Win32.RegistryKey> im <xref:Microsoft.Win32>\-Namespace von [!INCLUDE[dnprdnshort](../../../../csharp/getting-started/includes/dnprdnshort_md.md)] verwenden.  
  
## Schlüssel in der Registry\-Klasse  
 Die <xref:Microsoft.Win32.Registry>\-Klasse stellt die Basisregistrierungsschlüssel bereit, die für den Zugriff auf Unterschlüssel und deren Werte verwendet werden können. Die Basisschlüssel selbst sind schreibgeschützt. In der folgenden Tabelle werden die sieben Schlüssel, die von der <xref:Microsoft.Win32.Registry>\-Klasse verfügbar gemacht werden, aufgelistet und beschrieben.  
  
|**Taste**|**Beschreibung**|  
|---------------|----------------------|  
|<xref:Microsoft.Win32.Registry.ClassesRoot>|Definiert die Typen von Dokumenten und die diesen Typen zugeordneten Eigenschaften.|  
|<xref:Microsoft.Win32.Registry.CurrentConfig>|Enthält Informationen zur Hardwarekonfiguration, die nicht spezifisch sind.|  
|<xref:Microsoft.Win32.Registry.CurrentUser>|Enthält Informationen über die aktuellen Benutzereinstellungen, z.B. Umgebungsvariablen.|  
|<xref:Microsoft.Win32.Registry.DynData>|Enthält dynamische Registrierungsdaten, z.B. solche, die von virtuellen Gerätetreibern verwendet werden.|  
|<xref:Microsoft.Win32.Registry.LocalMachine>|Enthält fünf Unterschlüssel \(Hardware, SAM, Security, Software und System\), die die Konfigurationsdaten für den lokalen Computer enthalten.|  
|<xref:Microsoft.Win32.Registry.PerformanceData>|Enthält Informationen zur Leistung für Softwarekomponenten.|  
|<xref:Microsoft.Win32.Registry.Users>|Enthält Informationen zu den Standardeinstellungen für Benutzer.|  
  
> [!IMPORTANT]
>  Es ist sicherer, Daten in den Schlüssel für den aktuellen Benutzer \(<xref:Microsoft.Win32.Registry.CurrentUser>\) statt in den Schlüssel für den lokalen Computer \(<xref:Microsoft.Win32.Registry.LocalMachine>\) zu schreiben. Eine Bedingung, die in der Regel als „squatting“ bezeichnet wird, tritt auf, wenn der Schlüssel, den Sie erstellen, zuvor von einem anderen, möglicherweise böswilligen Prozess erstellt wurde. Um dies zu vermeiden, verwenden Sie eine Methode, z.B. <xref:Microsoft.Win32.RegistryKey.GetValue%2A>, die `Nothing` zurückgibt, wenn der Schlüssel nicht bereits vorhanden ist.  
  
## Lesen eines Werts aus der Registrierung  
 Der folgende Code zeigt, wie eine Zeichenfolge aus HKEY\_CURRENT\_USER gelesen wird.  
  
 [!CODE [VbResourceTasks#20](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#20)]  
  
 Der folgende Code liest, erhöht, und schreibt dann eine Zeichenfolge in HKEY\_CURRENT\_USER.  
  
 [!CODE [VbResourceTasks#21](../CodeSnippet/VS_Snippets_VBCSharp/VbResourceTasks#21)]  
  
## Siehe auch  
 <xref:System.SystemException>   
 <xref:System.ApplicationException>   
 <xref:Microsoft.VisualBasic.MyServices.RegistryProxy>   
 [Try...Catch...Finally Statement](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)   
 [Reading from and Writing to the Registry](../../../../visual-basic/developing-apps/programming/computer-resources/reading-from-and-writing-to-the-registry.md)   
 [Security and the Registry](../../../../visual-basic/developing-apps/programming/computer-resources/security-and-the-registry.md)
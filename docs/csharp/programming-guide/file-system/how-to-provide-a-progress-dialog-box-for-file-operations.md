---
title: "Gewusst wie: Bereitstellen eines Statusdialogfelds f&#252;r Dateioperationen (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Status (Dialogfeld) [C#]"
ms.assetid: 01b71fe7-8178-4dc8-aeb1-12053be7b51c
caps.latest.revision: 15
caps.handback.revision: 15
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Bereitstellen eines Statusdialogfelds f&#252;r Dateioperationen (C#-Programmierhandbuch)
Sie können ein Standarddialogfeld bereitstellen, das den Verlauf bei Dateivorgängen in Windows anzeigt, wenn Sie die Methode <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile%28System.String%2CSystem.String%2CMicrosoft.VisualBasic.FileIO.UIOption%29> im <xref:Microsoft.VisualBasic?displayProperty=fullName>\-Namespace verwenden.  
  
 [!INCLUDE[note_settings_general](../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### So fügen Sie einen Verweis in Visual Studio hinzu  
  
1.  Wählen Sie in der Menüleiste die Optionen **Projekt** und **Verweis hinzufügen** aus.  
  
     Das Dialogfeld **Verweis\-Manager** wird angezeigt.  
  
2.  Wählen Sie im Bereich **Assemblys** die Option **Framework** aus, wenn sie nicht bereits ausgewählt ist.  
  
3.  Aktivieren Sie in der Namensliste das Kontrollkästchen **Microsoft.VisualBasic**, und schließen Sie dann das Dialogfeld durch Auswählen der Schaltfläche **OK**.  
  
## Beispiel  
 Im folgenden Code wird das von `sourcePath` angegebene Verzeichnis in das von `destinationPath` angegebene Verzeichnis kopiert.  Mit diesem Code wird auch ein Standarddialogfeld bereitgestellt, in dem die geschätzte Zeit angezeigt wird, die bis zum Abschluss des Vorgangs verbleibt.  
  
 [!CODE [csFilesandFolders#11](../CodeSnippet/VS_Snippets_VBCSharp/csFilesAndFolders#11)]  
  
## Siehe auch  
 [Das Dateisystem und die Registrierung](../../../csharp/programming-guide/file-system/file-system-and-the-registry.md)
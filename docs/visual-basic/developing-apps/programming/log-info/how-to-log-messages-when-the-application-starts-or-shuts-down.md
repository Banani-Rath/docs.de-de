---
title: "Gewusst wie: Protokollieren von Meldungen beim Starten oder Beenden der Anwendung (Visual Basic) | Microsoft Docs"
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
  - "Ereignisprotokolle, Herunterfahren"
  - "My.Application.Log-Objekt, Protokollierung"
  - "Startup-Ereignis"
  - "Ereignisprotokolle, Start"
  - "Shutdown-Ereignis"
  - "My.Log-Objekt, Protokollierung"
ms.assetid: 67624d05-cddf-48b7-8c36-5c99baa4c621
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Gewusst wie: Protokollieren von Meldungen beim Starten oder Beenden der Anwendung (Visual Basic)
Sie können die Objekte `My.Application.Log` und `My.Log` verwenden, um Informationen über Ereignisse zu protokollieren, die in Ihrer Anwendung auftreten. Dieses Beispiel zeigt die Verwendung der `My.Application.Log.WriteEntry`\-Methode mit den Ereignissen `Startup` und `Shutdown` zum Erfassen von Ablaufverfolgungsinformationen.  
  
### Zugriff auf den Code des Ereignishandlers der Anwendung  
  
1.  Ein Projekt auswählen in **Projektmappen\-Explorer**. Klicken Sie im Menü **Projekt** auf **Eigenschaften**.  
  
2.  Klicken Sie auf die Registerkarte **Anwendung**.  
  
3.  Klicken Sie auf die Schaltfläche **Anwendungsereignisse anzeigen** um den Code\-Editor zu öffnen.  
  
     Dadurch wird die Datei "ApplicationEvents.vb" geöffnet.  
  
### Protokollieren von Meldungen beim Starten der Anwendung  
  
1.  Öffnen Sie die Datei "ApplicationEvents.vb" im Code\-Editor. Wählen Sie im Menü **Allgemein** den Eintrag **MyApplication\-Ereignisse** aus.  
  
2.  Wählen Sie im Menü **Deklarationen** den Eintrag **Start** aus.  
  
     Die Anwendung löst das Ereignis <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup> aus, bevor die Hauptanwendung ausgeführt wird.  
  
3.  Fügen Sie die Methode `My.Application.Log.WriteEntry` zum `Startup`\-Ereignishandler hinzu.  
  
     [!CODE [VbVbalrMyApplicationLog#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#1)]  
  
### Protokollieren von Meldungen beim Herunterfahren der Anwendung  
  
1.  Öffnen Sie die Datei "ApplicationEvents.vb" im Code\-Editor. Wählen Sie im Menü **Allgemein** den Eintrag **MyApplication\-Ereignisse** aus.  
  
2.  Wählen Sie im Menü **Deklarationen** den Eintrag **Herunterfahren** aus.  
  
     Die Anwendung löst das <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown>\-Ereignis aus, wenn der Hauptthread der Anwendung ausgeführt wird, jedoch bevor er heruntergefahren wird.  
  
3.  Fügen Sie dem `Shutdown`\-Ereignishandler die Methode `My.Application.Log.WriteEntry` hinzu.  
  
     [!CODE [VbVbalrMyApplicationLog#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#2)]  
  
## Beispiel  
 Sie können den **Projekt\-Designer** verwenden, um auf die Anwendungsereignisse im Code\-Editor zuzugreifen. Weitere Informationen finden Sie unter [Seite "Anwendung", Projekt\-Designer \(Visual Basic\)](/visual-studio/ide/reference/application-page-project-designer-visual-basic).  
  
 [!CODE [VbVbalrMyApplicationLog#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#3)]  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>   
 [Seite "Anwendung", Projekt\-Designer \(Visual Basic\)](/visual-studio/ide/reference/application-page-project-designer-visual-basic)   
 [Arbeiten mit Anwendungsprotokollen](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)
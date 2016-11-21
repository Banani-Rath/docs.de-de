---
title: "How to: Log Exceptions in Visual Basic | Microsoft Docs"
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
  - "exceptions, logging"
  - "exceptions, tracking"
ms.assetid: a26c60e2-ae39-444a-aebb-33eccadc0eeb
caps.latest.revision: 19
caps.handback.revision: 19
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Log Exceptions in Visual Basic
Sie können das `My.Application.Log`\-Objekt und das `My.Log`\-Objekt verwenden, um Informationen über in der Anwendung auftretende Ausnahmen zu protokollieren.  In diesen Beispielen wird gezeigt, wie mithilfe der `My.Application.Log.WriteException`\-Methode sowohl explizit abgefangene als auch unbehandelte Ausnahmen protokolliert werden können.  
  
 Verwenden Sie für das Protokollieren von Ablaufverfolgungsdaten die `My.Application.Log.WriteEntry`\-Methode.  Weitere Informationen finden Sie unter <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>  
  
### So protokollieren Sie eine behandelte Ausnahme  
  
1.  Erstellen Sie die Methode, die die Ausnahmeinformationen generiert.  
  
     [!CODE [VbVbalrMyApplicationLog#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#9)]  
  
2.  Verwenden Sie einen `Try...Catch`\-Block, um die Ausnahme abzufangen.  
  
     [!CODE [VbVbalrMyApplicationLog#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#6)]  
  
3.  Setzen Sie den Code, der eine Ausnahme generieren könnte, in den `Try`\-Block.  
  
     Heben Sie die Auskommentierung der Codezeilen `Dim` und `MsgBox` auf, um eine <xref:System.NullReferenceException>\-Ausnahme zu verursachen.  
  
     [!CODE [VbVbalrMyApplicationLog#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#7)]  
  
4.  Verwenden Sie im `Catch`\-Block die `My.Application.Log.WriteException`\-Methode, um die Ausnahmeinformationen zu schreiben.  
  
     [!CODE [VbVbalrMyApplicationLog#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#8)]  
  
     Im folgenden Beispiel wird der vollständige Code für die Protokollierung einer behandelten Ausnahme gezeigt.  
  
     [!CODE [VbVbalrMyApplicationLog#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#10)]  
  
### So protokollieren Sie eine nicht behandelte Ausnahme  
  
1.  Wählen Sie im **Projektmappen\-Explorer** ein Projekt aus.  Klicken Sie im Menü **Projekt** auf **Eigenschaften**.  
  
2.  Klicken Sie auf die Registerkarte **Anwendung**.  
  
3.  Klicken Sie auf die Schaltfläche **Anwendungsereignisse anzeigen**, um den Code\-Editor zu öffnen.  
  
     Daraufhin wird die Datei ApplicationEvents.vb geöffnet.  
  
4.  Öffnen Sie die Datei ApplicationEvents.vb im Code\-Editor.  Klicken Sie im Menü **Allgemein** auf **MyApplication\-Ereignisse**.  
  
5.  Klicken Sie im Menü **Deklarationen** auf **UnhandledException**.  
  
     Die Anwendung löst vor dem Ausführen der Hauptanwendung das <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException>\-Ereignis aus.  
  
6.  Fügen Sie im `UnhandledException`\-Ereignishandler die `My.Application.Log.WriteException`\-Methode hinzu.  
  
     [!CODE [VbVbalrMyApplicationLog#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#4)]  
  
     Im folgenden Beispiel wird der vollständige Code für die Protokollierung eines Ausnahmefehlers an.  
  
     [!CODE [VbVbalrMyApplicationLog#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#5)]  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>   
 <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>   
 [Arbeiten mit Anwendungsprotokollen](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)   
 [Gewusst wie: Schreiben von Protokollmeldungen](../../../../visual-basic/developing-apps/programming/log-info/how-to-write-log-messages.md)   
 [Exemplarische Vorgehensweise: Bestimmen, wohin "My.Application.Log" Informationen schreibt](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-determining-where-my-application-log-writes-information.md)   
 [Exemplarische Vorgehensweise: Ändern des Ortes, in den "My.Application.Log" Informationen schreibt](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md)
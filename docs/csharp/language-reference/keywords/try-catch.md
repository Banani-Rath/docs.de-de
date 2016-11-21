---
title: "try-catch (C#-Referenz) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "try"
  - "try_CSharpKeyword"
  - "catch"
  - "catch_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "catch-Schlüsselwort [C#]"
  - "try-catch-Anweisung [C#]"
ms.assetid: cb5503c7-bfa1-4610-8fc2-ddcd2e84c438
caps.latest.revision: 45
caps.handback.revision: 43
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# try-catch (C#-Referenz)
Die try\-catch\-Anweisung besteht aus einem `try`\-Block gefolgt von einer oder mehreren `catch`\-Klauseln, die Handler für verschiedene Ausnahmen angeben.  
  
## Hinweise  
 Wenn eine Ausnahme ausgelöst wird, sucht die Common Language Runtime \(CLR\) nach der `catch`\-Anweisung, die diese Ausnahme behandelt.  Wenn die derzeit ausgeführte Methode keinen solchen `catch`\-Block enthält, betrachtet die CLR die Methode, die die aktuelle Methode aufgerufen hat, dann die vorhergehende in der Aufrufliste usw.  Wenn kein `catch`\-Block gefunden wird, zeigt die CLR dem Benutzer eine Meldung über eine nicht behandelte Ausnahme an und beendet die Ausführung des Programms.  
  
 Der `try` \-Block enthält den überwachten Code, der möglicherweise die Ausnahme verursacht.  Der Block wird ausgeführt, bis eine Ausnahme ausgelöst wird, oder bis er erfolgreich abgeschlossen wird.  Beispielsweise löst der folgende Versuch, ein `null`\-Objekt umzuwandeln, die <xref:System.NullReferenceException>\-Ausnahme aus:  
  
```c#  
object o2 = null;  
try  
{  
    int i2 = (int)o2;   // Error  
}  
```  
  
 Zwar kann die `catch`\-Klausel ohne Argumente verwendet werden, um jeden beliebigen Ausnahmetyp abfangen, dies wird jedoch nicht empfohlen.  Im Allgemeinen sollten Sie nur solche Ausnahmen abfangen, bei denen Sie wissen, wie die Wiederherstellung durchgeführt wird.  Daher sollten Sie immer ein von <xref:System.Exception?displayProperty=fullName> abgeleitetes Objektargument angeben, zum Beispiel:  
  
```c#  
catch (InvalidCastException e)   
{  
}  
```  
  
 Es ist möglich, mehrere spezifische `catch`\-Klauseln in derselben try\-catch\-Anweisung zu verwenden.  In diesem Fall ist die Reihenfolge der `catch`\-Klauseln wichtig, da die `catch`\-Klauseln nacheinander überprüft werden.  Fangen Sie spezifischere Ausnahmen vor den weniger spezifischen ab.  Der Compiler erzeugt einen Fehler, wenn Sie Ihre catch\-Blöcke so anordnen, dass ein neuerer Block nie erreicht werden kann.  
  
 Die Verwendung von `catch`\-Argumenten ist eine Möglichkeit zum Filtern der Ausnahmen, die Sie behandeln möchten.  Sie können auch einen Prädikatausdruck verwenden, der die Ausnahme weiter untersucht, um zu entscheiden, ob Sie sie behandeln möchten.  Wenn der Prädikatausdruck „false“ zurückgibt, wird die Suche nach einem Ausnahmehandler fortgesetzt.  
  
```c#  
Catch (ArgumentException e) if (e.ParamName == “…”)  
{  
}  
```  
  
 Ausnahmefilter sind dem Abfangen und erneuten Auslösen vorzuziehen \(siehe nachfolgende Erläuterung\), da der Filter den Stapel nicht beschädigt.  Wenn ein späterer Handler den Stapel löscht, können Sie feststellen, wo die Ausnahme ursprünglich herkam, und nicht nur die letzte Stelle, an der sie erneut ausgelöst wurde.  Filterausdrücke für Ausnahmen werden häufig zu Protokollierungszwecken eingesetzt.  Sie können eine Prädikatfunktion erstellen, die immer „false“ zurückgibt und außerdem Ausgaben in ein Protokoll schreibt, und Sie können Ausnahmen protokollieren, wenn sie auftreten, ohne sie zu behandeln und erneut auszulösen.  
  
 Eine [throw](../../../csharp/language-reference/keywords/throw.md)\-Anweisung kann in einem `catch`\-Block verwendet werden, um die von der `catch`\-Anweisung abgefangene Ausnahme erneut auszulösen.  Im folgenden Beispiel werden Quellinformationen aus einer <xref:System.IO.IOException>\-Ausnahme extrahiert, anschließend wird die Ausnahme in der übergeordneten Methode ausgelöst.  
  
```c#  
catch (FileNotFoundException e)  
{  
    // FileNotFoundExceptions are handled here.  
}  
catch (IOException e)  
{  
    // Extract some information from this exception, and then   
    // throw it to the parent method.  
    if (e.Source != null)  
        Console.WriteLine("IOException source: {0}", e.Source);  
    throw;  
}  
```  
  
 Sie können eine Ausnahme abfangen und eine andere Ausnahme auslösen.  Wenn Sie dies tun, geben Sie die abgefangene Ausnahme als innere Ausnahme an, wie im folgenden Beispiel gezeigt.  
  
```c#  
catch (InvalidCastException e)   
{  
    // Perform some action here, and then throw a new exception.  
    throw new YourCustomException("Put your error message here.", e);  
}  
```  
  
 Sie können eine Ausnahme auch erneut auslösen, wenn eine angegebene Bedingung erfüllt ist, wie im folgenden Beispiel gezeigt.  
  
```c#  
  
catch (InvalidCastException e)  
{  
    if (e.Data == null)  
    {  
        throw;  
    }  
    else  
    {  
        // Take some action.  
    }  
 }  
```  
  
 Initialisieren Sie innerhalb eines `try`\-Blocks nur Variablen, die auch in diesem deklariert sind.  Andernfalls kann eine Ausnahme auftreten, bevor die Ausführung des Blocks abgeschlossen ist.  Beispiel: Im folgenden Codebeispiel wird die `n`\-Variable innerhalb des `try`\-Blocks initialisiert.  Beim Versuch, diese Variable außerhalb des `try`\-Blocks in der `Write(n)`\-Anweisung zu verwenden, wird ein Compilerfehler generiert.  
  
```c#  
static void Main()   
{  
    int n;  
    try   
    {  
        // Do not initialize this variable here.  
        n = 123;  
    }  
    catch  
    {  
    }  
    // Error: Use of unassigned local variable 'n'.  
    Console.Write(n);  
}  
```  
  
 Weitere Informationen zu „catch“ finden Sie unter [try\-catch\-finally](../../../csharp/language-reference/keywords/try-catch-finally.md).  
  
## Ausnahmen in asynchronen Methoden  
 Eine asynchrone Methode wird mit einem [async](../../../csharp/language-reference/keywords/async.md)\-Modifizierer gekennzeichnet und enthält in der Regel eine oder mehrere await\-Ausdrücke oder \-Anweisungen.  Ein await\-Ausdruck wendet den [await](../../../csharp/language-reference/keywords/await.md)\-Operator auf eine <xref:System.Threading.Tasks.Task> oder <xref:System.Threading.Tasks.Task%601> an.  
  
 Wenn ein `await`\-Ausdruck in der asynchchronen Methode erreicht wird, wird die Ausführung der Methode angehalten, bis die erwartete Aufgabe abgeschlossen ist.  Wenn die Aufgabe abgeschlossen ist, kann die Ausführung in der Methode fortgesetzt werden.  Weitere Informationen finden Sie unter [Asynchrone Programmierung mit Async und Await](../Topic/Asynchronous%20Programming%20with%20Async%20and%20Await%20\(C%23%20and%20Visual%20Basic\).md) und [Ablaufsteuerung in asynchronen Programmen](../Topic/Control%20Flow%20in%20Async%20Programs%20\(C%23%20and%20Visual%20Basic\).md).  
  
 Die abgeschlossene Aufgabe, auf die `await` angewendet wird, kann sich aufgrund einer unbehandelten Ausnahme in der Methode, die die Aufgabe zurückgibt, in einem fehlerhaften Zustand befinden.  Das Warten auf die Aufgabe löst eine Ausnahme aus.  Eine Aufgabe kann auch in einem abgebrochenen Zustand enden, wenn der asynchrone Prozess, der sie zurückgibt, abgebrochen wird.  Das Warten auf eine abgebrochene Aufgabe löst eine `OperationCanceledException` aus.  Weitere Informationen zum Abbrechen eines asynchronen Prozesses finden Sie unter [Feinabstimmung der Async\-Anwendung](../Topic/Fine-Tuning%20Your%20Async%20Application%20\(C%23%20and%20Visual%20Basic\).md).  
  
 Um die Ausnahme abzufangen, warten Sie in einem `try`\-Block auf die Aufgabe, und fangen Sie die Ausnahme im zugehörigen `catch`\-Block ab.  Ein Beispiel hierfür finden Sie im Abschnitt „Beispiel“.  
  
 Eine Aufgabe kann sich in einem fehlerhaften Zustand befinden, da mehrere Ausnahmen in der erwarteten asynchronen Methode aufgetreten sind.  Beispielsweise kann die Aufgabe das Ergebnis eines Aufrufs an <xref:System.Threading.Tasks.Task.WhenAll%2A?displayProperty=fullName> sein.  Wenn Sie auf eine solche Aufgabe warten, wird nur eine der Ausnahmen abgefangen, und Sie können nicht vorhersagen, welche Ausnahme abgefangen wird.  Ein Beispiel hierfür finden Sie im Abschnitt „Beispiel“.  
  
## Beispiel  
 Im folgenden Beispiel enthält der `try`\-Block einen Aufruf der `ProcessString`\-Methode, die eine Ausnahme verursachen kann.  Die `catch`\-Klausel enthält den Ausnahmehandler, der lediglich eine Meldung auf dem Bildschirm anzeigt.  Wenn die `throw`\-Anweisung aus `MyMethod` heraus aufgerufen wird, sucht das System nach der `catch`\-Anweisung und zeigt die Meldung `Exception caught` an.  
  
 [!CODE [csrefKeywordsExceptions#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsExceptions#2)]  
  
## Beispiel  
 Im folgenden Beispiel werden zwei catch\-Blöcke verwendet, und die spezifischste Ausnahme, die an erster Stelle steht, wird abgefangen.  
  
 Um die allgemeinste Ausnahme abzufangen, können Sie die throw\-Anweisung in `ProcessString` durch die folgende Anweisung ersetzen: `throw new Exception()`.  
  
 Wenn Sie den allgemeinsten catch\-Block im Beispiel an erster Stelle platzieren, wird die folgende Fehlermeldung angezeigt: `A previous catch clause already catches all exceptions of this or a super type ('System.Exception')`.  
  
 [!CODE [csrefKeywordsExceptions#3](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsExceptions#3)]  
  
## Beispiel  
 Im folgenden Beispiel wird die Ausnahmebehandlung für asynchrone Methoden veranschaulicht.  Um eine von einer asynchronen Aufgabe ausgelöste Ausnahme abzufangen, platzieren Sie den `await`\-Ausdruck in einem `try`\-Block, und fangen Sie die Ausnahme in einem `catch`\-Block ab.  
  
 Heben Sie die Auskommentierung der Zeile `throw new Exception` im Beispiel auf, um die Ausnahmebehandlung zu veranschaulichen.  Die `IsFaulted`\-Eigenschaft der Aufgabe wird auf `True` festgelegt, die `Exception.InnerException`\-Eigenschaft der Aufgabe auf die Ausnahme, und die Ausnahme wird im `catch`\-Block abgefangen.  
  
 Heben Sie die Auskommentierung der Zeile `throw new OperationCancelledException` auf, um zu veranschaulichen, was beim Abbrechen eines asynchronen Prozesses passiert.  Die `IsCanceled`\-Eigenschaft der Aufgabe wird auf `true` festgelegt, und die Ausnahme wird im `catch`\-Block abgefangen.  Unter bestimmten Bedingungen, die für dieses Beispiel nicht gelten, wird die `IsFaulted`\-Eigenschaft der Aufgabe auf `true` und `IsCanceled` auf `false` festgelegt.  
  
 [!CODE [csAsyncExceptions#2](../CodeSnippet/VS_Snippets_VBCSharp/csasyncexceptions#2)]  
  
## Beispiel  
 Das folgende Beispiel veranschaulicht die Behandlung von Ausnahmen in Fällen, in denen mehrere Aufgaben zu mehreren Ausnahmen führen können.  Der `try`\-Block wartet auf die Aufgabe, die von einem Aufruf von <xref:System.Threading.Tasks.Task.WhenAll%2A?displayProperty=fullName> zurückgegeben wird.  Die Aufgabe ist abgeschlossen, wenn die drei Aufgaben abgeschlossen sind, auf die WhenAll angewendet wird.  
  
 Jede der drei Aufgaben löst eine Ausnahme aus.  Der `catch`\-Block iteriert durch die Ausnahmen, die in der `Exception.InnerExceptions`\-Eigenschaft der Aufgabe stehen, die von <xref:System.Threading.Tasks.Task.WhenAll%2A?displayProperty=fullName> zurückgegeben wurde.  
  
 [!CODE [csAsyncExceptions#4](../CodeSnippet/VS_Snippets_VBCSharp/csasyncexceptions#4)]  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [C\#\-Schlüsselwörter](../../../csharp/language-reference/keywords/index.md)   
 [try\-, throw\- und catch\-Anweisungen \(C\+\+\)](/visual-cpp/cpp/try-throw-and-catch-statements-cpp)   
 [Ausnahmebehandlungsanweisungen](../../../csharp/language-reference/keywords/exception-handling-statements.md)   
 [throw](../../../csharp/language-reference/keywords/throw.md)   
 [try\-finally](../../../csharp/language-reference/keywords/try-finally.md)   
 [Gewusst wie: Explizites Auslösen von Ausnahmen](../Topic/How%20to:%20Explicitly%20Throw%20Exceptions.md)
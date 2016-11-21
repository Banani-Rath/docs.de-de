---
title: "Methoden (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "C#-Sprache, Methoden"
  - "Methoden [C#]"
ms.assetid: cc738f07-e8cd-4683-9585-9f40c0667c37
caps.latest.revision: 41
caps.handback.revision: 41
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Methoden (C#-Programmierhandbuch)
Eine Methode ist ein Codeblock, der eine Reihe von Anweisungen enthält. Ein Programm bewirkt die Ausführung der Anweisungen, indem die Methode aufgerufen wird und alle erforderlichen Methodenargumente angegeben werden. In C\# werden alle Anweisungen im Kontext einer Methode ausgeführt. Die Main\-Methode ist der Einstiegspunkt jeder C\#\-Anwendung und wird von der Common Language Runtime \(CLR\) aufgerufen, wenn das Programm gestartet wird.  
  
> [!NOTE]
>  In diesem Thema werden benannte Methoden erläutert. Informationen zu anonymen Funktionen finden Sie unter [Anonyme Funktionen](../../../csharp/programming-guide/statements-expressions-operators/anonymous-functions.md).  
  
## Methodensignaturen  
 Methoden werden in einer [Klasse](../../../csharp/language-reference/keywords/class.md) oder [Struktur](../../../csharp/language-reference/keywords/struct.md) deklariert, indem die Zugriffsebene wie z. B. `public` oder `private`, optionale Modifizierer wie z. B. `abstract` oder `sealed`, der Rückgabewert, der Name der Methode und die Methodenparameter angegeben werden. Diese Teile bilden zusammen die Signatur der Methode.  
  
> [!NOTE]
>  Ein Rückgabetyp einer Methode ist nicht Teil der Signatur der Methode, wenn es um die Methodenüberladung geht. Er ist jedoch Teil der Methodensignatur, wenn die Kompatibilität zwischen einem Delegaten und der Methode bestimmt wird, auf die dieser verweist.  
  
 Methodenparameter werden in Klammern eingeschlossen und durch Kommas getrennt. Leere Klammern geben an, dass für die Methode keine Parameter erforderlich sind. Diese Klasse enthält drei Methoden:  
  
 [!CODE [csProgGuideObjects#40](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#40)]  
  
## Methodenzugriff  
 Das Aufrufen einer Methode für ein Objekt ähnelt dem Zugreifen auf ein Feld. Fügen Sie nach dem Objektnamen einen Punkt, den Namen der Methode und Klammern hinzu. Argumente werden innerhalb der Klammern aufgelistet und durch Kommas getrennt. Die Methoden der `Motorcycle`\-Klasse können also wie im folgenden Beispiel gezeigt aufgerufen werden:  
  
 [!CODE [csProgGuideObjects#41](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#41)]  
  
## Methodenparameter und Argumente  
 Die Methodendefinition gibt die Namen und Typen aller ggf. erforderlichen Parameter an. Wenn aufrufender Code die Methode aufruft, werden für jeden Parameter konkrete Werte bereitgestellt, die als Argumente bezeichnet werden. Die Argumente müssen mit dem Parametertyp kompatibel sein, aber der im aufrufenden Code verwendete Name des Arguments \(sofern vorhanden\) muss nicht mit dem in der Methode definierten Parameternamen identisch sein. Zum Beispiel:  
  
 [!CODE [csProgGuideObjects#74](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#74)]  
  
## Übergeben als Verweis und Übergeben als Wert  
 Wenn ein Werttyp an eine Methode übergeben wird, wird anstelle des eigentlichen Objekts standardmäßig eine Kopie übergeben. Änderungen am Argument haben daher keine Auswirkungen auf die ursprüngliche Kopie in der aufrufenden Methode. Sie können einen Werttyp als Verweis übergeben, indem Sie das ref\-Schlüsselwort verwenden. Weitere Informationen finden Sie unter [Übergeben von Werttypparametern](../../../csharp/programming-guide/classes-and-structs/passing-value-type-parameters.md). Eine Liste der integrierten Werttypen finden Sie unter [Tabelle der Werttypen](../../../csharp/language-reference/keywords/value-types-table.md).  
  
 Wenn ein Objekt eines Verweistyps an eine Methode übergeben wird, wird ein Verweis auf das Objekt übergeben. Das heißt, die Methode erhält nicht das Objekt selbst, sondern ein Argument, das den Speicherort des Objekts angibt. Wenn Sie einen Member des Objekts unter Verwendung dieses Verweises ändern, wird die Änderung im Argument in der aufrufenden Methode berücksichtigt, selbst wenn Sie das Objekt als Wert übergeben.  
  
 Sie erstellen einen Verweistyp mithilfe des `class`\-Schlüsselworts, wie im folgenden Beispiel gezeigt.  
  
 [!CODE [csProgGuideObjects#42](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#42)]  
  
 Wenn Sie jetzt ein Objekt, das auf diesem Typ basiert, an eine Methode übergeben, wird ein Verweis auf das Objekt übergeben. Das folgende Beispiel übergibt ein Objekt des `SampleRefType`\-Typs an die `ModifyObject`\-Methode.  
  
 [!CODE [csProgGuideObjects#75](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#75)]  
  
 Das Beispiel entspricht im Wesentlichen dem vorherigen Beispiel und übergibt ein Argument als Wert an eine Methode. Aber da ein Verweistyp verwendet wird, unterscheidet sich das Ergebnis. Die Änderung, die in `ModifyObject` am `value`\-Feld des Parameters \(`obj`\) vorgenommen wird, ändert auch das `value`\-Feld des Arguments \(`rt`\) in der `TestRefType`\-Methode. Die `TestRefType`\-Methode zeigt 33 als Ausgabe an.  
  
 Weitere Informationen zum Übergeben von Verweistypen als Verweis und als Wert finden Sie unter [Übergeben von Verweistypparametern](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md) und [Verweistypen](../../../csharp/language-reference/keywords/reference-types.md).  
  
## Rückgabewerte  
 Methoden können einen Wert an die aufrufende Funktion \(den Aufrufer\) zurückgeben. Wenn der Rückgabetyp – der vor dem Methodennamen aufgeführte Typ – nicht `void` ist, kann die Methode den Wert mithilfe des `return`\-Schlüsselworts zurückgeben. Eine Anweisung mit der `return`\-Schlüsselwort, gefolgt von einem Wert, der dem Rückgabetyp entspricht, gibt diesen Wert an den Methodenaufrufer zurück. Das `return`\-Schlüsselwort beendet außerdem die Ausführung der Methode. Wenn der Rückgabetyp `void` ist, ist eine `return`\-Anweisung ohne Wert immer noch nützlich, um die Ausführung der Methode zu beenden. Ohne das `return`\-Schlüsselwort wird die Ausführung der Methode beendet, wenn das Ende des Codeblocks erreicht ist. Methoden mit einem anderen Rückgabetyp als „void“ müssen das `return`\-Schlüsselwort verwenden, um einen Wert zurückzugeben. Die folgenden beiden Methoden verwenden z. B. das `return`\-Schlüsselwort, um ganze Zahlen zurückzugeben:  
  
 [!CODE [csProgGuideObjects#44](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#44)]  
  
 Um einen von einer Methode zurückgegebenen Wert zu verwenden, kann die aufrufende Methode den Methodenaufruf selbst an jeder Stelle verwenden, an der ein Wert des gleichen Typs ausreichend ist. Sie können den Rückgabewert auch einer Variablen zuweisen. Beispielsweise wird mit den folgenden beiden Codebeispiele das gleiche Ergebnis erzielt:  
  
 [!CODE [csProgGuideObjects#45](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#45)]  
  
 [!CODE [csProgGuideObjects#46](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#46)]  
  
 Die Verwendung einer lokalen Variablen, in diesem Fall `result`, zum Speichern eines Werts ist optional. Es kann die Lesbarkeit des Codes verbessern, oder es kann notwendig sein, wenn Sie den ursprünglichen Wert des Arguments für den gesamten Gültigkeitsbereich der Methode speichern müssen.  
  
 Die Rückgabe eines mehrdimensionalen Arrays von einer Methode M, die den Inhalt des Arrays ändert, ist nicht erforderlich, wenn die aufrufende Funktion das Array an M übergeben hat. Sie können das resultierende Array von M für den funktionalen Fluss von Werten oder zu stilistischen Zwecken zurückgeben, erforderlich ist dies aber nicht.  Sie müssen das geänderte Array nicht zurückgeben, weil C\# alle Verweistypen als Wert übergibt und der Wert eines Arrayverweises der Zeiger auf das Array ist. In der Methode M sind Änderungen am Inhalt des Arrays durch beliebigen Code beobachtbar, der einen Verweis auf das Array enthält, wie im folgenden Beispiel gezeigt.  
  
```c#  
static void Main(string[] args) { int[,] matrix = new int[2, 2]; FillMatrix(matrix); // matrix is now full of -1 } public static void FillMatrix(int[,] matrix) { for (int i = 0; i < matrix.GetLength(0); i++) { for (int j = 0; j < matrix.GetLength(1); j++) { matrix[i, j] = -1; } } }  
  
```  
  
 Weitere Informationen finden Sie unter [return](../../../csharp/language-reference/keywords/return.md).  
  
## Asynchrone Methoden  
 Mithilfe der Async\-Funktion können Sie asynchrone Methoden aufrufen, ohne explizite Rückrufe verwenden oder den Code manuell über mehrere Methoden oder Lambda\-Ausdrücke teilen zu müssen. Die Async\-Funktion wurde in [!INCLUDE[vs_dev11_long](../../../csharp/includes/vs_dev11_long_md.md)] eingeführt.  
  
 Wenn Sie eine Methode mit dem [async](../../../csharp/language-reference/keywords/async.md)\-Modifizierer kennzeichnen, können Sie den [await](../../../csharp/language-reference/keywords/await.md) Operator in der Methode verwenden. Wenn ein await\-Ausdruck in der asynchronen Methode erreicht wird, wird die Steuerung an den Aufrufer zurückgegeben, und die Ausführung der Methode wird angehalten, bis die erwartete Aufgabe abgeschlossen ist. Wenn die Aufgabe abgeschlossen ist, kann die Ausführung in der Methode fortgesetzt werden.  
  
> [!NOTE]
>  Eine asynchrone Methode wird an den Aufrufer zurückgegeben, wenn sie entweder auf das erste erwartete Objekt trifft, das noch nicht abgeschlossen wurde, oder das Ende der asynchronen Methode erreicht.  
  
 Eine asynchrone Methode kann den Rückgabetyp <xref:System.Threading.Tasks.Task%601>, <xref:System.Threading.Tasks.Task> oder „void“ haben. Der void\-Rückgabetyp wird hauptsächlich zum Definieren von Ereignishandlern verwendet, bei denen ein void\-Rückgabetyp erforderlich ist. Auf eine asynchrone Methode, die „void“ zurückgibt, kann nicht gewartet werden, und der Aufrufer einer Methode mit void\-Rückgabe kann keine Ausnahmen auffangen, die die Methode auslöst.  
  
 Im folgenden Beispiel ist `DelayAsync` eine asynchrone Methode mit dem Rückgabetyp <xref:System.Threading.Tasks.Task%601>.`DelayAsync` enthält eine `return`\-Anweisung, die eine ganze Zahl zurückgibt. Aus diesem Grund muss die Methodendeklaration von `DelayAsync` den Rückgabetyp `Task<int>` haben. Da der Rückgabetyp `Task<int>` ist, ergibt die Auswertung des `await`\-Ausdrucks in `DoSomethingAsync` eine ganze Zahl, wie die folgende Anweisung veranschaulicht: `int result = await delayTask`.  
  
 Die `startButton_Click`\-Methode ist ein Beispiel für eine asynchrone Methode mit void\-Rückgabetyp. Da `DoSomethingAsync` eine asynchrone Methode ist, muss die Aufgabe für den Aufruf von `DoSomethingAsync` abgewartet werden, wie in der folgenden Anweisung dargestellt: `await DoSomethingAsync();`. Die `startButton_Click`\-Methode muss mit dem `async`\-Modifizierer definiert werden, da die Methode über einen `await`\-Ausdruck verfügt.  
  
 [!CODE [csAsyncMethod#2](../CodeSnippet/VS_Snippets_VBCSharp/csasyncmethod#2)]  
  
 Mit einer asynchronen Methode können keine [ref](../../../csharp/language-reference/keywords/ref.md)\- oder [out](../../../csharp/language-reference/keywords/out.md)\-Parameter deklariert, jedoch Methoden aufgerufen werden, die solche Parameter aufweisen.  
  
 Weitere Informationen zu asynchronen Methoden finden Sie unter [Asynchrone Programmierung mit Async und Await](../Topic/Asynchronous%20Programming%20with%20Async%20and%20Await%20\(C%23%20and%20Visual%20Basic\).md), [Ablaufsteuerung in asynchronen Programmen](../Topic/Control%20Flow%20in%20Async%20Programs%20\(C%23%20and%20Visual%20Basic\).md) und [Asynchrone Rückgabetypen](../Topic/Async%20Return%20Types%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Ausdruckstextdefinitionen  
 Es gibt häufig Methodendefinitionen, die einfach direkt das Ergebnis eines Ausdrucks zurückgeben oder eine einzige Anweisung als Text der Methode aufweisen.  Es ist eine Syntaxabkürzung zur Definition solcher Methoden mithilfe von `=>` verfügbar:  
  
```c#  
public Point Move(int dx, int dy) => new Point(x + dx, y + dy); public void Print() => Console.WriteLine(First + " " + Last); // Works with operators, properties, and indexers too. public static Complex operator +(Complex a, Complex b) => a.Add(b); public string Name => First + " " + Last; public Customer this[long id] => store.LookupCustomer(id);  
```  
  
 Wenn die Methode `void` zurückgibt oder es sich um eine asynchrone Methode handelt, muss der Text der Methode ein Anweisungsausdruck sein \(wie bei Lambdas\).  Eigenschaften und Indexer müssen schreibgeschützt sein. Verwenden Sie darüber hinaus nicht das `get`\-Accessorschlüsselwort.  
  
## Iteratoren  
 Ein Iterator führt eine benutzerdefinierte Iteration durch eine Auflistung durch, z. B. eine Liste oder ein Array. Ein Iterator verwendet die [yield return](../../../csharp/language-reference/keywords/yield.md)\-Anweisung, um jedes Element einzeln nacheinander zurückzugeben. Wenn eine [yield return](../../../csharp/language-reference/keywords/yield.md)\-Anweisung erreicht wird, wird die aktuelle Position im Code gespeichert. Wenn der Iterator das nächste Mal aufgerufen wird, wird die Ausführung von dieser Position neu gestartet.  
  
 Sie rufen einen Iterator im Clientcode mithilfe einer [foreach](../../../csharp/language-reference/keywords/foreach-in.md) Anweisung auf.  
  
 Der Rückgabetyp eines Iterators kann <xref:System.Collections.IEnumerable>, <xref:System.Collections.Generic.IEnumerable%601>, <xref:System.Collections.IEnumerator> oder <xref:System.Collections.Generic.IEnumerator%601> sein.  
  
 Weitere Informationen finden Sie unter [Iteratoren](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md).  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Klassen und Strukturen](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Zugriffsmodifizierer](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)   
 [Statische Klassen und statische Klassenmember](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md)   
 [Vererbung](../../../csharp/programming-guide/classes-and-structs/inheritance.md)   
 [Abstrakte und versiegelte Klassen und Klassenmember](../../../csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members.md)   
 [params](../../../csharp/language-reference/keywords/params.md)   
 [return](../../../csharp/language-reference/keywords/return.md)   
 [out](../../../csharp/language-reference/keywords/out.md)   
 [ref](../../../csharp/language-reference/keywords/ref.md)   
 [Übergeben von Parametern](../../../csharp/programming-guide/classes-and-structs/passing-parameters.md)
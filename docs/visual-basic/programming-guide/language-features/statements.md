---
title: "Statements in Visual Basic | Microsoft Docs"
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
  - "variables [Visual Basic], declaring"
  - "colons (:)"
  - "constants, defining"
  - "underlines"
  - "constants, statements"
  - "blue underline"
  - "procedures, statements"
  - "variables [Visual Basic], assigning"
  - "line breaks, in code"
  - "executable statements"
  - "variables [Visual Basic], defining"
  - "statements [Visual Basic], about statements"
ms.assetid: fcfdee1a-82b7-4846-98f7-9ca3f5160089
caps.latest.revision: 30
caps.handback.revision: 30
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Statements in Visual Basic
Eine Anweisung in [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] ist eine vollständige Instruktion.  Sie kann Schlüsselwörter, Operatoren, Variablen, Konstanten und Ausdrücke enthalten.  Jede Anweisung gehört zu einer der folgenden Kategorien:  
  
-   **Deklarationsanweisungen**, die eine Variable, Konstante oder Prozedur benennen und auch einen Datentyp angeben können.  
  
-   **Ausführbare Anweisungen**, die Aktionen starten.  Diese Anweisungen rufen eine Methode oder Funktion auf und können Codeblöcke in einer Schleife durchlaufen oder sich in Codeblöcke verzweigen.  Zu ausführbaren Anweisungen zählen **Zuweisungsanweisungen**, die einer Variablen oder Konstanten einen Wert oder einen Ausdruck zuweisen.  
  
 In diesem Thema werden die einzelnen Kategorien beschrieben.  Darüber hinaus wird erläutert, wie mehrere Anweisungen in einer einzigen Zeile kombiniert werden und wie eine Anweisung über mehrere Zeilen fortgesetzt wird.  
  
## Deklarationsanweisungen  
 Mit Deklarationsanweisungen benennen und definieren Sie Prozeduren, Variablen, Eigenschaften, Arrays und Konstanten.  Wenn Sie ein Programmierelement deklarieren, können Sie auch seinen Datentyp, seine Zugriffsebene und seinen Gültigkeitsbereich definieren.  Weitere Informationen finden Sie unter [Declared Element Characteristics](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md).  
  
 Das folgende Beispiel enthält drei Deklarationen:  
  
 [!CODE [VbVbalrStatements#80](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#80)]  
  
 Die erste Deklaration ist die `Sub`\-Anweisung.  Zusammen mit der entsprechenden `End Sub` \-Anweisung deklariert sie eine Prozedur mit dem Namen `applyFormat`.  Sie gibt außerdem an, dass `applyFormat` `Public` ist. Dies bedeutet, dass jeder Code auf sie zugreifen und sie aufrufen kann.  
  
 Die zweite Deklaration ist die `Const`\-Anweisung, die die Konstante `limit` deklariert und den `Integer`\-Datentyp sowie den Wert 33 angibt.  
  
 Die dritte Deklaration ist die `Dim`\-Anweisung, die die Variable `thisWidget` deklariert.  Der Datentyp ist ein bestimmtes Objekt, und zwar ein aus der `Widget`\-Klasse erstelltes Objekt.  Sie können eine Variable als beliebigen elementaren Datentyp oder als beliebigen Objekttyp deklarieren, der in der verwendeten Anwendung verfügbar gemacht wird.  
  
### Anfangswerte  
 Beim Ausführen von Code, der eine Deklarationsanweisung enthält, reserviert [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] den für das deklarierte Element erforderlichen Speicher.  Wenn das Element einen Wert enthält, wird es von [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] mit dem Standardwert für seinen Datentyp initialisiert.  Weitere Informationen finden Sie in [Dim Statement](../../../visual-basic/language-reference/statements/dim-statement.md) unter "Verhalten".  
  
 Sie können einer Variablen in ihrer Deklaration einen Anfangswert zuweisen, wie im folgenden Beispiel veranschaulicht.  
  
 [!CODE [VbVbalrStatements#81](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#81)]  
  
 Wenn es sich bei der Variablen um eine Objektvariable handelt, können Sie beim Deklarieren eine Instanz ihrer Klasse explizit erstellen, indem Sie das [New Operator](../../../visual-basic/language-reference/operators/new-operator.md)\-Schlüsselwort verwenden, wie im folgenden Beispiel veranschaulicht.  
  
 [!CODE [VbVbalrStatements#82](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#82)]  
  
 Beachten Sie, dass der Anfangswert, den Sie in einer Deklarationsanweisung angeben, erst einer Variablen zugewiesen wird, wenn ihre Deklarationsanweisung ausgeführt wird.  Bis zu diesem Zeitpunkt enthält die Variable den Standardwert für ihren Datentyp.  
  
## Ausführbare Anweisungen  
 Eine ausführbare Anweisung führt eine Aktion aus.  Sie kann eine Prozedur aufrufen, an eine andere Stelle im Code verzweigen, verschiedene Anweisungen durchlaufen oder einen Ausdruck auswerten.  Eine Zuweisungsanweisung ist eine besondere Variante einer ausführbaren Anweisung.  
  
 Im folgenden Beispiel wird eine `If...Then...Else`\-Steuerungsstruktur verwendet, um je nach dem Wert einer Variablen verschiedene Codeblöcke auszuführen.  In jedem Codeblock wird eine `For...Next`\-Schleife mit einer festgelegten Anzahl von Wiederholungen ausgeführt.  
  
 [!CODE [VbVbalrStatements#83](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#83)]  
  
 Die `If`\-Anweisung im vorherigen Beispiel überprüft den Wert des Parameters `clockwise`.  Wenn der Wert `True` ist, wird die `spinClockwise`\-Methode von `aWidget` aufgerufen.  Wenn der Wert `False` ist, wird die `spinCounterClockwise`\-Methode von `aWidget` aufgerufen.  Die `If...Then...Else`\-Steuerungsstruktur endet mit `End If`.  
  
 Die `For...Next`\-Schleife in jedem Block wiederholt den Aufruf der entsprechenden Methode mit einer Häufigkeit, die dem Wert des `revolutions`\-Parameters entspricht.  
  
## Zuweisungsanweisungen  
 Zuweisungsanweisungen führen Zuweisungsoperationen aus. Bei diesen wird ein Wert auf der rechten Seite des Zuweisungsoperators \(`=`\) in dem Element auf der linken Seite gespeichert, wie im folgenden Beispiel veranschaulicht.  
  
 [!CODE [VbVbalrStatements#73](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#73)]  
  
 Im vorherigen Beispiel speichert die Zuweisungsanweisung den Literalwert 42 in der Variablen `v`.  
  
### Geeignete Programmierelemente  
 Das Programmierelement auf der linken Seite des Zuweisungsoperators muss einen Wert akzeptieren und speichern können.  Es muss daher eine Variable oder Eigenschaft sein, die nicht [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md) ist, oder es muss ein Arrayelement sein.  Im Kontext einer Zuweisungsanweisung wird ein solches Element zuweilen als *l\-Wert* \("linker Wert"\) bezeichnet.  
  
 Der Wert auf der rechten Seite des Zuweisungsoperators wird durch einen Ausdruck generiert, der aus einer beliebigen Kombinationen von Literalen, Konstanten, Variablen, Eigenschaften, Arrayelementen, anderen Ausdrücken und Funktionsaufrufen bestehen kann.  Dies wird anhand des folgenden Beispiels veranschaulicht:  
  
 [!CODE [VbVbalrStatements#74](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#74)]  
  
 Im vorherigen Beispiel wird dem Wert in der Variablen `z` der Wert in der Variablen `y` hinzugefügt, und anschließend wird der durch den Aufruf der Funktion `findResult` zurückgegebene Wert hinzugefügt.  Der Gesamtwert dieses Ausdrucks wird dann in der Variablen `x` gespeichert.  
  
### Datentypen in Zuweisungsanweisungen  
 Außer numerischen Wert kann der Zuweisungsoperator auch `String`\-Werte zuweisen, wie im folgenden Beispiel veranschaulicht.  
  
 [!CODE [VbVbalrStatements#75](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#75)]  
  
 Sie können auch `Boolean`\-Werte zuweisen, entweder mit einem `Boolean`\-Literal oder einem `Boolean`\-Ausdruck, wie im folgenden Beispiel veranschaulicht.  
  
 [!CODE [VbVbalrStatements#76](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#76)]  
  
 Ebenso können Sie Programmierelementen vom Datentyp `Char`, `Date` oder `Object` entsprechende Werte zuweisen.  Sie können auch einem Element, das als Element der Klasse deklariert ist, aus der diese Instanz erstellt wurde, eine Objektinstanz zuweisen.  
  
### Verbundzuweisungsanweisungen  
 *Verbundzuweisungsanweisungen* führen zunächst eine Operation für einen Ausdruck aus, bevor Sie diesen einem Programmierelement zuweisen.  Im folgenden Beispiel wird der Operator `+=` veranschaulicht, der den Wert der Variablen auf der linken Seite des Operators um den Wert des Ausdrucks auf der rechten Seite erhöht.  
  
 [!CODE [VbVbalrStatements#77](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#77)]  
  
 Im vorherigen Beispiel wird dem Wert von `n` 1 hinzugefügt und anschließend dieser neue Wert in `n` gespeichert.  Dies ist die Kurzform der folgenden Anweisung:  
  
 [!CODE [VbVbalrStatements#78](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#78)]  
  
 Eine Vielzahl von Verbundzuweisungsoperationen können mit Operatoren dieses Typs ausgeführt werden.  Eine Liste dieser Operatoren und weitere Informationen über sie finden Sie unter [Assignment Operators](../../../visual-basic/language-reference/operators/assignment-operators.md).  
  
 Der Verkettungszuweisungsoperator \(`&=`\) eignet sich zum Hinzufügen einer Zeichenfolge am Ende einer bereits vorhandenen Zeichenfolge, wie im folgenden Beispiel veranschaulicht.  
  
 [!CODE [VbVbalrStatements#79](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#79)]  
  
### Typkonvertierungen in Zuweisungsanweisungen  
 Der Datentyp des Werts, den Sie einer Variablen, einer Eigenschaft oder einem Arrayelement zuweisen, muss dem jeweiligen Zielelement entsprechen.  Versuchen Sie grundsätzlich, einen Wert mit demselben Datentyp wie der Datentyp des Zielelements zu generieren.  Einige Typen können jedoch während der Zuweisung in einen anderen Typ konvertiert werden.  
  
 Informationen über das Konvertieren von Datentypen finden Sie unter [Type Conversions in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md).  Kurz gesagt, [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] konvertiert den Wert eines bestimmten Typs automatisch in einen beliebigen anderen Typ, zu dem der ursprüngliche Typ erweitert werden kann.  Eine *erweiternde Konvertierung* wird zur Laufzeit immer erfolgreich und ohne Datenverlust ausgeführt.  [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] konvertiert z. B. einen `Integer`\-Wert ggf. in `Double`, da `Integer` zu `Double` erweitert wird.  Weitere Informationen finden Sie unter [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md).  
  
 *Einschränkende Konvertierungen* \(Konvertierungen, die keine erweiternden Konvertierungen sind\) können zur Laufzeit fehlschlagen oder mit Datenverlust ausgeführt werden.  Sie können eine einschränkende Konvertierung explizit ausführen, indem Sie eine Typkonvertierungsfunktion verwenden, oder Sie können den Compiler alle Konvertierungen implizit ausführen lassen, indem Sie `Option Strict Off` festlegen.  Weitere Informationen finden Sie unter [Implicit and Explicit Conversions](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md).  
  
## Anordnen mehrerer Anweisungen in einer Zeile  
 Sie können mehrere Anweisungen in einer Zeile durch einen Doppelpunkt \(`:`\) trennen.  Dies wird anhand des folgenden Beispiels veranschaulicht:  
  
 [!CODE [VbVbalrStatements#70](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#70)]  
  
 Dies ist jedoch nur selten sinnvoll, da durch diese Syntaxform der Code schwer leserlich und schwer zu pflegen ist.  Daher empfiehlt es sich, nur eine Anweisung pro Zeile zu verwenden.  
  
## Fortsetzen einer Anweisung über mehrere Zeilen  
 Eine Anweisung passt normalerweise in eine Zeile. Wenn sie jedoch zu lang ist, können Sie die Anweisung in der nächsten Zeile fortsetzen. Verwenden Sie dazu ein Zeilenfortsetzungszeichen, das aus einem Leerzeichen vor einem Unterstrich \(`_`\) gefolgt von einem Wagenrücklauf besteht.  Im folgenden Beispiel wird die ausführbare `MsgBox`\-Anweisung über zwei Zeilen fortgesetzt.  
  
 [!CODE [VbVbalrStatements#71](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#71)]  
  
### Implizite Zeilenfortsetzung  
 In vielen Fällen können Sie eine Anweisung ohne Angabe eines Unterstrichs \(\_\) in der nächsten Zeile fortsetzen.  In der folgenden Tabelle sind die Syntaxelemente aufgeführt, mit denen eine Anweisung implizit in der nächsten Codezeile fortgesetzt wird.  
  
|||  
|-|-|  
|Syntaxelement|Beispiel|  
|Nach einem Komma \(`,`\).|[!CODE [VbVbalrLineContinuation#1](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#1)]|  
|Nach einer öffnenden runden Klammer \(`(`\) oder vor einer schließenden runden Klammer \(`)`\).|[!CODE [VbVbalrLineContinuation#2](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#2)]|  
|Nach einer öffnenden geschweiften Klammer \(`{`\) oder vor einer schließenden geschweiften Klammer \(`}`\).|[!CODE [VbVbalrLineContinuation#3](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#3)]<br /><br /> Weitere Informationen finden Sie unter [Object Initializers: Named and Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md) und [Collection Initializers](../../../visual-basic/programming-guide/language-features/collection-initializers/index.md).|  
|Nach dem Beginn eines eingebetteten Ausdrucks \(`<%=`\) oder vor dem Ende eines eingebetteten Ausdrucks \(`%>`\) in einem XML\-Literal.|[!CODE [VbVbalrLineContinuation#4](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#4)]<br /><br /> Weitere Informationen finden Sie unter [Embedded Expressions in XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).|  
|Nach dem Verkettungsoperator \(`&`\).|[!CODE [VbVbcnConventions#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnConventions#9)]<br /><br /> Weitere Informationen finden Sie unter [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md).|  
|Nach Zuweisungsoperatoren \(`=`, `&=`, `:=`, `+=`, `-=`, `*=`, `/=`, `\=`, `^=`, `<<=`, `>>=`\).|[!CODE [VbVbalrLineContinuation#5](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#5)]<br /><br /> Weitere Informationen finden Sie unter [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md).|  
|Nach binären Operatoren \(`+`, `-`, `/`, `*`, `Mod`, `<>`, `<`, `>`, `<=`, `>=`, `^`, `>>`, `<<`, `And`, `AndAlso`, `Or`, `OrElse`, `Like`, `Xor`\) in einem Ausdruck.|[!CODE [VbVbalrLineContinuation#7](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#7)]<br /><br /> Weitere Informationen finden Sie unter [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md).|  
|Nach dem `Is`\-Operator und dem `IsNot`\-Operator.|[!CODE [VbVbalrLineContinuation#8](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#8)]<br /><br /> Weitere Informationen finden Sie unter [Operators Listed by Functionality](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md).|  
|Nach einem Memberqualifiziererzeichen \(`.`\) und vor dem Membernamen.  Nach einem Memberqualifiziererzeichen müssen Sie jedoch ein Zeilenfortsetzungszeichen \(\_\) einschließen, wenn Sie die `With`\-Anweisung verwenden oder Werte in der Initialisierungsliste für einen Typ angeben.  Es empfiehlt sich, die Zeile nach dem Zuweisungsoperator \(z. B. `=`\) zu umbrechen, wenn Sie `With`\-Anweisungen oder Objektinitialisierungslisten verwenden.|[!CODE [VbVbalrLineContinuation#5](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#5)]<br />[!CODE [VbVbalrLineContinuation#14](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#14)]<br /><br /> Weitere Informationen finden Sie unter [With...End With Statement](../../../visual-basic/language-reference/statements/with-end-with-statement.md) und [Object Initializers: Named and Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md).|  
|Nach einem XML\-Achseneigenschaften\-Qualifizierer \(`.` oder `.@` oder `...`\).  Sie müssen jedoch ein Zeilenfortsetzungszeichen \(\_\) einschließen, wenn Sie bei Verwendung des `With`\-Schlüsselworts einen Memberqualifizierer angeben.|[!CODE [VbVbalrLineContinuation#9](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#9)]<br /><br /> Weitere Informationen finden Sie unter [XML Axis Properties](../../../visual-basic/language-reference/xml-axis/xml-axis-properties.md).|  
|Nach einem Kleiner\-als\-Zeichen \(\<\) oder vor einem Größer\-als\-Zeichen \(`>`\), wenn Sie ein Attribut angeben.  Außerdem nach einem Größer\-als\-Zeichen \(`>`\), wenn Sie ein Attribut angeben.  Sie müssen jedoch ein Zeilenfortsetzungszeichen \(\_\) einschließen, wenn Sie Attribute auf Assemblyebene oder Modulebene angeben.|[!CODE [VbVbalrLineContinuation#10](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#10)]<br /><br /> Weitere Informationen finden Sie unter [Attribute](../Topic/Attributes%20\(C%23%20and%20Visual%20Basic\).md).|  
|Vor und nach Abfrageoperatoren \(`Aggregate`, `Distinct`, `From`, `Group By`, `Group Join`, `Join`, `Let`, `Order By`, `Select`, `Skip`, `Skip While`, `Take`, `Take While`, `Where`, `In`, `Into`, `On`, `Ascending` und `Descending`\).  Zeilen zwischen den Schlüsselwörtern von Abfrageoperatoren, die sich aus mehreren Schlüsselwörtern \(`Order By`, `Group Join`, `Take While` und `Skip While`\) zusammensetzen, dürfen nicht umbrochen werden.|[!CODE [VbVbalrLineContinuation#11](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#11)]<br /><br /> Weitere Informationen finden Sie unter [Queries](../../../visual-basic/language-reference/queries/queries.md).|  
|Nach dem `In`\-Schlüsselwort in einer `For Each`\-Anweisung.|[!CODE [VbVbalrLineContinuation#12](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#12)]<br /><br /> Weitere Informationen finden Sie unter [For Each...Next\-Anweisung](../../../visual-basic/language-reference/statements/for-each-next-statement.md).|  
|Nach dem `From`\-Schlüsselwort in einem Auflistungsinitialisierer.|[!CODE [VbVbalrLineContinuation#13](../CodeSnippet/VS_Snippets_VBCSharp/vbvbalrlinecontinuation#13)]<br /><br /> Weitere Informationen finden Sie unter [Collection Initializers](../../../visual-basic/programming-guide/language-features/collection-initializers/index.md).|  
  
## Hinzufügen von Kommentaren  
 Quellcode ist nicht immer selbsterklärend, selbst nicht für den Programmierer, der ihn geschrieben hat.  Daher verwenden die meisten Programmierer eingebettete Kommentare, um den Code zu dokumentieren.  Kommentare im Code dienen zur Erläuterung einer Prozedur oder zur Angabe bestimmter Anweisungen für andere Personen, die den Code lesen oder damit arbeiten.  In [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] werden Kommentare während der Kompilierung ignoriert und haben keine Auswirkung auf den kompilierten Code.  
  
 Kommentarzeilen beginnen mit einem Apostroph \(`'`\) oder `REM` vor einem Leerzeichen.  Sie können an beliebiger Stelle im Code, außer in einer Zeichenfolge, hinzugefügt werden.  Wenn Sie einen Kommentar an eine Anweisung anhängen möchten, fügen Sie nach der Anweisung einen Apostroph oder `REM` ein, und geben Sie danach den Kommentar ein.  Kommentare können auch in eine separate Zeile geschrieben werden.  Im folgenden Beispiel werden diese Möglichkeiten veranschaulicht.  
  
 [!CODE [VbVbalrStatements#72](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#72)]  
  
## Überprüfen von Kompilierungsfehlern  
 Wenn nach der Eingabe einer Codezeile die Zeile mit einer blauen Wellenlinie unterstrichen ist \(möglicherweise wird auch eine Fehlermeldung angezeigt\), enthält die Anweisung einen Syntaxfehler.  Sie müssen den Fehler in der Anweisung finden \(indem Sie in der Aufgabenliste nachschauen oder mit der Maus auf den Fehler zeigen und die Fehlermeldung lesen\) und korrigieren.  Solange nicht alle Syntaxfehler im Code behoben sind, kann das Programm nicht ordnungsgemäß kompiliert werden.  
  
## Verwandte Abschnitte  
  
|||  
|-|-|  
|Begriff|Definition|  
|[Assignment Operators](../../../visual-basic/language-reference/operators/assignment-operators.md)|Enthält Links zu Sprachreferenzseiten, die Zuweisungsoperatoren, z. B. `=`, `*=` und `&=`, beschreiben.|  
|[Operators and Expressions](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)|Beschreibt, wie Elemente mit Operatoren kombiniert werden, um neue Werte zu erhalten.|  
|[Gewusst wie: Umbrechen und Zusammenfassen von Anweisungen in Code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)|Veranschaulicht, wie eine einzelne Anweisung auf mehrere Zeilen verteilt wird und wie mehrere Anweisungen in einer Zeile platziert werden.|  
|[How to: Label Statements](../../../visual-basic/programming-guide/program-structure/how-to-label-statements.md)|Beschreibt das Bezeichnen einer Codezeile.|
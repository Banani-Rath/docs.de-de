---
title: "Typen (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Werttypen [C#]"
  - "Verweistypen [C#]"
  - "Typen [C#]"
  - "C#-Sprache, Datentypen"
  - "Allgemeines Typsystem [C#]"
  - "Datentypen [C#]"
  - "C#-Sprache, Typen"
  - "Starke Typisierung [C#]"
ms.assetid: f782d7cc-035e-4500-b1b1-36a9881130ad
caps.latest.revision: 53
caps.handback.revision: 53
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Typen (C#-Programmierhandbuch)
## Typen, Variablen und Werte  
 C\# ist eine stark typisierte Sprache.  Jede Variable und jede Konstante verfügt über einen Typ, genau wie jeder Ausdruck, der zu einem Wert ausgewertet wird.  Jede Methodensignatur gibt für jeden Eingabeparameter und den Rückgabewert einen Typ an.  In der .NET Framework\-Klassenbibliothek sind integrierte numerische Typen sowie komplexere Typen definiert, die eine große Anzahl logischer Konstrukte darstellen, z. B. das Dateisystem, Netzwerkverbindungen, Auflistungen und Arrays von Objekten sowie Datumsangaben.  In einem typischen C\#\-Programm werden Typen aus der Klassenbibliothek sowie benutzerdefinierte Typen verwendet, die die Konzepte für das Problemfeld des Programms modellieren.  
  
 Folgende Informationen können in einem Typ gespeichert sein:  
  
-   Der Speicherplatz, den eine Variable des Typs erfordert  
  
-   Die maximalen und minimalen Werte, die diese darstellen kann  
  
-   Die enthaltenen Member \(Methoden, Felder, Ereignisse usw.\)  
  
-   Der Basistyp, von dem geerbt wird  
  
-   Die Position, an der der Arbeitsspeicher für Variablen zur Laufzeit belegt wird  
  
-   Die Arten von zulässigen Vorgängen  
  
 Der Compiler verwendet Typinformationen, um sicherzustellen, dass alle im Code ausgeführten Vorgänge *typsicher* sind.  Wenn Sie z. B. eine Variable vom Typ [int](../../../csharp/language-reference/keywords/int.md) deklarieren, können Sie mit dem Compiler die Variable für Additions\- und Subtraktionsvorgänge verwenden.  Wenn Sie dieselben Vorgänge für eine Variable vom Typ [bool](../../../csharp/language-reference/keywords/bool.md) ausführen möchten, generiert der Compiler einen Fehler, wie im folgenden Beispiel dargestellt:  
  
 [!CODE [csProgGuideTypes#42](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#42)]  
  
> [!NOTE]
>  C\- und C\+\+\-Entwickler sollten beachten, dass in C\# [bool](../../../csharp/language-reference/keywords/bool.md) nicht in [int](../../../csharp/language-reference/keywords/int.md) konvertiert werden kann.  
  
 Der Compiler bettet die Typinformationen als Metadaten in die ausführbare Datei ein.  Die Common Language Runtime \(CLR\) verwendet diese Metadaten zur Laufzeit, um die Typsicherheit zu gewährleisten, wenn Speicherplatz belegt und freigegeben wird.  
  
### Angeben von Typen in Variablendeklarationen  
 Wenn Sie eine Variable oder Konstante in einem Programm deklarieren, müssen Sie ihren Typ festlegen oder das [var](../../../csharp/language-reference/keywords/var.md)\-Schlüsselwort verwenden, damit der Typ vom Compiler abgeleitet wird.  Im folgenden Beispiel werden einige Variablendeklarationen dargestellt, die sowohl integrierte numerische Typen als auch komplexe benutzerdefinierte Typen verwenden:  
  
 [!CODE [csProgGuideTypes#36](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#36)]  
  
 Die Methodenparameter\- und Rückgabewerttypen werden in der Methodensignatur angegeben.  Die folgende Signatur zeigt eine Methode, für die ein [int](../../../csharp/language-reference/keywords/int.md) als Eingabeargument benötigt wird und die eine Zeichenfolge zurückgibt:  
  
 [!CODE [csProgGuideTypes#35](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#35)]  
  
 Nachdem eine Variable deklariert wurde, kann sie nicht erneut mit einem neuen Typ deklariert werden. Außerdem kann ihr kein Wert zugewiesen werden, der nicht mit dem deklarierten Typ kompatibel ist.  Zum Beispiel können Sie nicht eine [int](../../../csharp/language-reference/keywords/int.md) deklarieren und dieser dann den booleschen Wert [true](../../../csharp/language-reference/keywords/true-literal.md) zuweisen.  Werte können jedoch in andere Typen konvertiert werden, z. B., wenn diese neuen Variablen zugewiesen oder als Methodenargumente übergeben werden.  Eine *Typkonvertierung*, die keinen Datenverlust verursacht, wird automatisch vom Compiler ausgeführt.  Eine Konvertierung, die möglicherweise Datenverlust verursacht, erfordert eine *Umwandlung* in den Quellcode.  
  
 Weitere Informationen finden Sie unter [Umwandlung und Typkonvertierungen](../../../csharp/programming-guide/types/casting-and-type-conversions.md).  
  
## Integrierte Typen  
 C\# liefert einen Standardsatz mit integrierten numerischen Typen zur Darstellung von ganzen Zahlen, Gleitkommawerten, booleschen Ausdrücken, Textzeichen, Dezimalwerten und anderen Datentypen.  Es gibt auch integrierte `string`\-Typen und `object`\-Typen.  Diese können Sie in jedem C\#\-Programm verwenden.  Weitere Informationen über die integrierten Typen finden Sie unter [Referenztabellen für Typen](../../../csharp/language-reference/keywords/reference-tables-for-types.md).  
  
## Benutzerdefinierte Typen  
 Sie verwenden die Konstrukte [struct](../../../csharp/language-reference/keywords/struct.md), [class](../../../csharp/language-reference/keywords/class.md), [interface](../../../csharp/language-reference/keywords/interface.md) und [enum](../../../csharp/language-reference/keywords/enum.md), um eigene benutzerdefinierte Typen zu erstellen.  Die .NET Framework\-Klassenbibliothek ist eine Auflistung benutzerdefinierter, von Microsoft bereitgestellter Typen, die Sie in Ihren eigenen Anwendungen verwenden können.  Standardmäßig sind die am häufigsten verwendeten Typen in der Klassenbibliothek in jedem C\#\-Programm verfügbar.  Andere stehen nur zur Verfügung, wenn Sie ausdrücklich einen Projektverweis auf die Assembly hinzufügen, in der diese definiert sind.  Wenn der Compiler über einen Verweis auf die Assembly verfügt, können Sie Variablen \(und Konstanten\) des in dieser Assembly deklarierten Typs im Quellcode deklarieren.  Weitere Informationen finden Sie in der Dokumentation zur [.NET Framework\-Klassenbibliothek](http://go.microsoft.com/fwlink/?LinkID=217856).  
  
## Das allgemeine Typsystem  
 Mit zwei grundlegenden Punkten über das System der Typen in [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] sollten Sie vertraut sein:  
  
-   Es unterstützt das Prinzip der Vererbung.  Typen können von anderen Typen abgeleitet werden, die als *Basistypen* bezeichnet werden.  Der abgeleitete Typ erbt \(mit einigen Beschränkungen\) die Methoden, Eigenschaften und anderen Member des Basistyps.  Der Basistyp kann wiederum von einem anderen Typ abgeleitet sein. In diesem Fall erbt der abgeleitete Typ die Member beider Basistypen in der Vererbungshierarchie.  Alle Typen, einschließlich integrierter numerischer Typen, z. B. <xref:System.Int32?displayProperty=fullName> \(C\#\-Schlüsselwort: [int](../../../csharp/language-reference/keywords/int.md)\), werden letztendlich von einem einzelnen Basistyp abgeleitet, nämlich <xref:System.Object?displayProperty=fullName> \(C\#\-Schlüsselwort: [object](../../../csharp/language-reference/keywords/object.md)\).  Diese einheitliche Typhierarchie wird als [Allgemeines Typsystem](../../../standard/base-types/common-type-system.md) \(CTS\) bezeichnet.  Weitere Informationen zur Vererbung in C\# finden Sie unter [Vererbung](../../../csharp/programming-guide/classes-and-structs/inheritance.md).  
  
-   Jeder Typ im CTS ist als *Werttyp* oder *Referenztyp* definiert.  Dies betrifft auch alle benutzerdefinierten Typen in der .NET Framework\-Klassenbibliothek und Ihre eigenen benutzerdefinierten Typen.  Typen, die Sie mithilfe des [struct](../../../csharp/language-reference/keywords/struct.md)\-Schlüsselworts definieren, sind Werttypen. Alle integrierten numerischen Typen sind `structs`.  Typen, die Sie mithilfe des [class](../../../csharp/language-reference/keywords/class.md)\-Schlüsselworts definieren, sind Referenztypen.  Für Referenztypen und Werttypen gelten unterschiedliche Kompilierzeitregeln und ein anderes Laufzeitverhalten.  
  
 In der folgenden Abbildung wird die Beziehung zwischen Werttypen und Referenztypen im CTS dargestellt.  
  
 ![Wert&#45; und Verweistypen](../../../csharp/programming-guide/types/media/valuetypescts.png "ValueTypesCTS")  
Werttypen und Referenztypen im CTS  
  
> [!NOTE]
>  Wie Sie sehen, sind die am häufigsten verwendeten Typen alle im <xref:System>\-Namespace organisiert.  Jedoch ist es für den Namespace, in dem ein Typ enthalten ist, unerheblich, ob es sich um einen Werttyp oder einen Referenztyp handelt.  
  
### Werttypen  
 Werttypen werden von <xref:System.ValueType?displayProperty=fullName> abgeleitet, was wiederum von <xref:System.Object?displayProperty=fullName> abgeleitet wird.  Typen, die von <xref:System.ValueType?displayProperty=fullName> abgeleitet werden, weisen ein besonderes Verhalten in der CLR auf.  Werttypvariablen enthalten die zugehörigen Werte direkt, d. h., der Speicher wird inline in dem Kontext belegt, in dem die Variable deklariert ist.  Für Werttypvariablen erfolgt keine getrennte Heapzuordnung oder ein Mehraufwand für die Garbage Collection.  
  
 Zwei Kategorien von Werttypen sind verfügbar: [struct](../../../csharp/language-reference/keywords/struct.md) und [enum](../../../csharp/language-reference/keywords/enum.md).  
  
 Die integrierten numerischen Typen sind Strukturen und verfügen über Eigenschaften und Methoden, auf die Sie zugreifen können:  
  
```c#  
// Static method on type Byte.  
byte b = Byte.MaxValue;  
```  
  
 Sie deklarieren diese jedoch und weisen ihnen Werte zu, als wären es einfache, nicht aggregierte Typen:  
  
```c#  
byte num = 0xA;  
int i = 5;  
char c = 'Z';  
```  
  
 Werttypen sind *versiegelt* \(sealed\). Dies bedeutet z. B., dass Sie keinen Typ von <xref:System.Int32?displayProperty=fullName> ableiten können und dass eine Struktur nicht von einer benutzerdefinierten Klasse oder Struktur erben kann, weil eine Struktur nur von <xref:System.ValueType?displayProperty=fullName> erben kann.  Eine Struktur kann jedoch eine oder mehrere Schnittstellen implementieren.  Sie können einen Strukturtyp in einen Schnittstellentyp umwandeln. Dadurch wird ein *Boxing*\-Vorgang gestartet, mit dem die Struktur von einem Referenztypobjekt im verwalteten Heap umschlossen wird.  Boxing\-Vorgänge werden auch ausgeführt, wenn Sie einen Werttyp an eine Methode übergeben, die <xref:System.Object?displayProperty=fullName> als Eingabeparameter akzeptiert.  Weitere Informationen finden Sie unter [Boxing und Unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md).  
  
 Sie können das [struct](../../../csharp/language-reference/keywords/struct.md)\-Schlüsselwort verwenden, um eigene benutzerdefinierte Werttypen zu erstellen.  In der Regel wird eine Struktur als Container für einen kleinen Satz verwandter Variablen verwendet, wie im folgenden Beispiel dargestellt:  
  
 [!CODE [csProgGuideObjects#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideObjects#1)]  
  
 Weitere Informationen über Strukturen finden Sie unter [Strukturen](../../../csharp/programming-guide/classes-and-structs/structs.md).  Weitere Informationen über Werttypen im [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] finden Sie unter [Allgemeines Typsystem](../../../standard/base-types/common-type-system.md).  
  
 Die andere Kategorie von Werttypen ist [enum](../../../csharp/language-reference/keywords/enum.md).  Eine Enumeration definiert einen Satz benannter ganzzahliger Konstanten.  So enthält z. B. die <xref:System.IO.FileMode?displayProperty=fullName>\-Enumeration in der .NET Framework\-Klassenbibliothek einen Satz benannter ganzzahliger Konstanten, die festlegen, wie eine Datei geöffnet werden soll.  Die Definition erfolgt wie im folgenden Beispiel:  
  
 [!CODE [csProgGuideTypes#44](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#44)]  
  
 Die `System.IO.FileMode.Create`\-Konstante besitzt den Wert 2.  Der Name ist jedoch für Personen, die den Quellcode lesen, viel aussagekräftiger. Aus diesem Grund ist es besser, anstelle von Konstantenliteralen Enumerationen zu verwenden.  Weitere Informationen finden Sie unter <xref:System.IO.FileMode?displayProperty=fullName>.  
  
 Alle Enumerationen erben von <xref:System.Enum?displayProperty=fullName>, was wiederum von <xref:System.ValueType?displayProperty=fullName> erbt.  Alle Regeln, die für Strukturen gelten, gelten auch für Enumerationen.  Weitere Informationen über Enumerationen finden Sie unter [Enumerationstypen](../../../csharp/programming-guide/enumeration-types.md).  
  
### Verweistypen  
 Ein Typ, der als [Klasse](../../../csharp/language-reference/keywords/class.md), [Delegat](../../../csharp/language-reference/keywords/delegate.md), Array oder [Schnittstelle](../../../csharp/language-reference/keywords/interface.md) definiert ist, ist ein *Referenztyp*.  Wenn Sie eine Variable für einen Referenztyp deklarieren, enthält die Variable zunächst den Wert [NULL](../../../csharp/language-reference/keywords/null.md), bis Sie explizit eine Instanz des Objekts mithilfe des Operators [new](../../../csharp/language-reference/keywords/new.md) erstellen oder ihr ein Objekt zuweisen, das an anderer Stelle mithilfe des folgenden Operators erstellt wurde: `new, as shown in the following example:`  
  
```c#  
MyClass mc = new MyClass();  
MyClass mc2 = mc;  
```  
  
 Eine Schnittstelle muss zusammen mit einem Klassenobjekt initialisiert werden, von dem sie implementiert wird.  Wenn `IMyInterface` von `MyClass` implementiert wird, erstellen Sie eine Instanz von `IMyInterface`, wie im folgenden Beispiel dargestellt:  
  
```c#  
IMyInterface iface = new MyClass();  
```  
  
 Beim Erstellen des Objekts wird der Speicher im verwalteten Heap belegt. Die Variable enthält lediglich einen Verweis auf den Speicherort des Objekts.  Für Typen im verwalteten Heap ist Mehraufwand erforderlich, wenn sie zugewiesen werden und wenn sie von der automatischen Speicherverwaltungsfunktion der CLR freigegeben werden, was als *Garbage Collection* bezeichnet wird.  Die Garbage Collection ist jedoch auch stark optimiert. In den meisten Szenarien führt sie nicht zu einem Leistungsproblem.  Weitere Informationen über die Garbage Collection finden Sie unter [Automatische Speicherverwaltung](../Topic/Automatic%20Memory%20Management.md).  
  
 Alle Arrays sind Referenztypen, selbst wenn ihre Elemente Werttypen sind.  Arrays werden implizit von der <xref:System.Array?displayProperty=fullName>\-Klasse abgeleitet. Sie deklarieren und verwenden diese jedoch mit der vereinfachten, von C\# bereitgestellten Syntax, wie im folgenden Beispiel dargestellt:  
  
 [!CODE [csProgGuideTypes#45](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#45)]  
  
 Referenztypen bieten volle Vererbungsunterstützung.  Wenn Sie eine Klasse erstellen, können Sie von einer anderen Schnittstelle oder Klasse erben, die nicht als [versiegelt](../../../csharp/language-reference/keywords/sealed.md) definiert ist. Andere Klassen können von Ihrer Klasse erben und die virtuellen Methoden überschreiben.  Weitere Informationen zum Erstellen eigener Klassen finden Sie unter [Klassen und Strukturen](../../../csharp/programming-guide/classes-and-structs/index.md).  Weitere Informationen zur Vererbung und zu virtuellen Methoden finden Sie unter [Vererbung](../../../csharp/programming-guide/classes-and-structs/inheritance.md).  
  
## Typen von Literalwerten  
 In C\# erhalten Literalwerte einen Typ vom Compiler.  Sie können festlegen, wie ein numerisches Literal eingegeben werden soll, indem Sie am Ende der Zahl einen Buchstaben anfügen.  Um z. B. anzugeben, dass der Wert 4.56 als Gleitkommazahl behandelt werden soll, fügen Sie nach der Zahl `4.56f` ein "f" oder "F" an:  Wenn kein Buchstabe angefügt wird, leitet der Compiler einen Typ für das Literal ab.  Weitere Informationen darüber, welche Typen mit Buchstabensuffixen angegeben werden können, finden Sie auf den Referenzseiten für einzelne Typen unter [Werttypen](../../../csharp/language-reference/keywords/value-types.md).  
  
 Da Literale typisiert sind und alle Typen letztlich von <xref:System.Object?displayProperty=fullName> abgeleitet werden, können Sie Code der folgenden Art erstellen und kompilieren:  
  
 [!CODE [csProgGuideTypes#37](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#37)]  
  
## Generische Typen  
 Ein Typ kann mit einem oder mehreren *Typparametern* deklariert werden, die als Platzhalter für den eigentlichen Typ verwendet werden \(den *konkreten Typ*\), der vom Clientcode beim Erstellen einer Instanz des Typs bereitgestellt wird.  Solche Typen werden als *generische Typen* bezeichnet.  Beispielsweise besitzt der .NET Framework\-Typ <xref:System.Collections.Generic.List%601?displayProperty=fullName> einen Typparameter, dem üblicherweise der Name *T* gegeben wird.  Beim Erstellen einer Instanz des Typs geben Sie die Objekte an, die die Liste enthalten soll, z. B. string:  
  
<CodeContentPlaceHolder>4</CodeContentPlaceHolder>  
 Die Verwendung des Typparameters ermöglicht die Wiederverwendung der Klasse für beliebige Elementtypen, ohne die einzelnen Elemente in [object](../../../csharp/language-reference/keywords/object.md) konvertieren zu müssen.  Generische Auflistungsklassen werden als *stark typisierte Auflistungen* bezeichnet, weil der Compiler den jeweiligen Typ der Elemente in der Auflistung kennt und zur Kompilierzeit einen Fehler auslösen kann, wenn Sie beispielsweise versuchen, dem `strings`\-Objekt im vorherigen Beispiel eine ganze Zahl hinzuzufügen.  Weitere Informationen finden Sie unter [Generika](../../../csharp/programming-guide/generics/index.md).  
  
## Implizite Typen, anonyme Typen und Typen, die NULL\-Werte zulassen  
 Wie bereits zuvor erläutert, können Sie eine lokale Variable \(jedoch keine Klassenmember\) implizit eingeben, indem Sie das [var](../../../csharp/language-reference/keywords/var.md)\-Schlüsselwort verwenden.  Die Variable erhält weiterhin zur Kompilierzeit einen Typ, aber der Typ wird vom Compiler bereitgestellt.  Weitere Informationen finden Sie unter [Implizit typisierte lokale Variablen](../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md).  
  
 In einigen Fällen ist es unpraktisch, einen benannten Typ für einfache Sätze verwandter Werte zu erstellen, die nicht außerhalb von Methodengrenzen gespeichert oder übergeben werden sollen.  Sie können für diesen Zweck *anonyme Typen* erstellen.  Weitere Informationen finden Sie unter [Anonyme Typen](../../../csharp/programming-guide/classes-and-structs/anonymous-types.md).  
  
 Gewöhnliche Werttypen können den Wert [NULL](../../../csharp/language-reference/keywords/null.md) nicht aufweisen.  Sie können jedoch auf NULL festlegbare Werttypen erstellen, indem Sie nach dem Typ ein `?` anfügen.  Zum Beispiel ist `int?` ein `int`\-Typ, der auch den Wert [NULL](../../../csharp/language-reference/keywords/null.md) aufweisen kann.  Im CTS sind Typen, die NULL\-Werte zulassen, Instanzen vom generischen Strukturtyp <xref:System.Nullable%601?displayProperty=fullName>.  Typen, die NULL\-Werte zulassen, sind besonders hilfreich, wenn Sie Daten an und aus Datenbanken übergeben, in denen die numerischen Werte NULL sein können.  Weitere Informationen finden Sie unter [Typen, die NULL\-Werte zulassen](../../../csharp/programming-guide/nullable-types/index.md).  
  
## Verwandte Abschnitte  
 Weitere Informationen finden Sie unter den folgenden Themen:  
  
-   [Umwandlung und Typkonvertierungen](../../../csharp/programming-guide/types/casting-and-type-conversions.md)  
  
-   [Boxing und Unboxing](../../../csharp/programming-guide/types/boxing-and-unboxing.md)  
  
-   [Verwenden von dynamischen Typen](../../../csharp/programming-guide/types/using-type-dynamic.md)  
  
-   [Werttypen](../../../csharp/language-reference/keywords/value-types.md)  
  
-   [Verweistypen](../../../csharp/language-reference/keywords/reference-types.md)  
  
-   [Klassen und Strukturen](../../../csharp/programming-guide/classes-and-structs/index.md)  
  
-   [Anonyme Typen](../../../csharp/programming-guide/classes-and-structs/anonymous-types.md)  
  
-   [Generika](../../../csharp/programming-guide/generics/index.md)  
  
-   [Variablen und Ausdrücke](http://go.microsoft.com/fwlink/?LinkId=221228) im Buch zum [Einstieg in Visual C\# 2010](http://go.microsoft.com/fwlink/?LinkId=221214)  
  
## C\#\-Programmiersprachenspezifikation  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## Siehe auch  
 [C\#\-Referenz](../../../csharp/language-reference/index.md)   
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Konvertierung von XML\-Datentypen](../Topic/Conversion%20of%20XML%20Data%20Types.md)   
 [Tabelle ganzzahliger Typen](../../../csharp/language-reference/keywords/integral-types-table.md)
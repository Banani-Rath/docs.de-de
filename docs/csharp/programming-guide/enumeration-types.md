---
title: "Enumerationstypen (C#-Programmierhandbuch) | Microsoft Docs"
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
  - "Bitflags [C#]"
  - "Die Programmiersprache C#, Enumerationen"
  - "Enumerationen [C#]"
  - "Enumerationen [C#]"
ms.assetid: 64a9b731-9e3c-4336-8a09-018db2aa10b7
caps.latest.revision: 17
caps.handback.revision: 17
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Enumerationstypen (C#-Programmierhandbuch)
Ein Enumerationstyp \(auch als Enumeration bezeichnet\) bietet eine effiziente Möglichkeit, einen Satz benannter integraler Konstanten zu definieren, die einer Variablen zugewiesen werden können.  Angenommen, Sie müssen eine Variable definieren, deren Wert einen Wochentag darstellt.  Es gibt nur sieben sinnvolle Werte, die diese Variable speichern kann.  Um diese Werte zu definieren, können Sie einen Enumerationstyp verwenden, der durch die Verwendung des [enum](../../csharp/language-reference/keywords/enum.md)\-Schlüsselworts deklariert wird.  
  
 [!CODE [csProgGuideEnums#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEnums#1)]  
  
 Der zugrunde liegende Standardtyp aller Elemente in der Enumeration lautet [int](../../csharp/language-reference/keywords/int.md).  Sie können mit einem Doppelpunkt einen anderen ganzzahligen numerischen Typ angeben, wie im vorherigen Beispiel dargestellt.  Eine vollständige Liste möglicher Typen finden Sie in [Enumeration \(C\#\-Referenz\)](../../csharp/language-reference/keywords/enum.md).  
  
 Sie können die zugrunde liegenden numerischen Werte überprüfen, indem Sie dem zugrunde liegenden Typ, wie im folgenden Beispiel gezeigt umwandeln.  
  
```c#  
Days today = Days.Monday;  
int dayNumber =(int)today;  
Console.WriteLine("{0} is day number #{1}.", today, dayNumber);  
  
Months thisMonth = Months.Dec;  
byte monthNumber = (byte)thisMonth;  
Console.WriteLine("{0} is month number #{1}.", thisMonth, monthNumber);  
  
// Output:  
// Monday is day number #1.  
// Dec is month number #11.  
```  
  
 Im Folgenden werden die Vorteile beschrieben, die mit der Verwendung eines Enumerations\- statt eines numerischen Typs einhergehen:  
  
-   Sie geben eindeutig für Clientcode an, welche Werte für die Variable gültig sind.  
  
-   In [!INCLUDE[vsprvs](../../csharp/includes/vsprvs_md.md)] führt IntelliSense die definierten Werte auf.  
  
 Wenn Sie keine Werte für die Elemente in der Enumeratorliste angeben, werden die Werte automatisch um 1 erhöht.  Im vorhergehenden Beispiel hat `Days.Sunday` den Wert 0, `Days.Monday` den Wert 1 usw.  Wenn Sie ein neues `Days`\-Objekt erstellen, weist es den Standardwert `Days.Sunday` \(0\) auf, wenn Sie ihm nicht ausdrücklich einen Wert zuweisen.  Wenn Sie eine Enumeration erstellen, wählen Sie den Standardwert aus, der am logischsten ist und weisen Sie ihm den Wert Null zu.  Auf diese Weise erhalten alle Enumerationen diesen Standardwert, wenn ihnen nicht ausdrücklich beim Erstellen ein Wert zugewiesen wird.  
  
 Falls die Variable `meetingDay` vom Typ `Days` ist, können Sie ihr \(ohne eine explizite Umwandlung\) lediglich einen der von `Days` definierten Werte zuweisen.  Und wenn sich der Besprechungstag ändert, können Sie `meetingDay` einen neuen Wert von `Days` zuweisen:  
  
 [!CODE [csProgGuideEnums#4](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEnums#4)]  
  
> [!NOTE]
>  Es ist möglich, `meetingDay` einen beliebigen ganzzahligen Wert zuzuweisen.  Zum Beispiel erzeugt diese Codezeile keinen Fehler: `meetingDay = (Days) 42`.  Sie sollten dies jedoch nicht tun, weil die damit einhergehende Erwartung darin besteht, dass eine Enumerationsvariable nur einen der vom Enumerator definierten Werte enthält.  Einer Variablen eines Enumerationstyps einen willkürlich gewählten Wert zuzuweisen, führt zu einem hohen Fehlerrisiko.  
  
 Sie können den Elementen in der Enumeratorliste, die einen Enumerationstyp aufweisen, beliebige Werte zuweisen und auch berechnete Werte verwenden:  
  
 [!CODE [csProgGuideEnums#3](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEnums#3)]  
  
## Enumerationstypen als Bitflags  
 Sie können einen Enumerationstyp verwenden, um Bitflags zu definieren. Dadurch kann eine Instanz des Enumerationstyps eine Kombination aus den Werten speichern, die in der Enumeratorliste definiert sind.  \(Selbstverständlich sind einige Kombinationen möglicherweise im Programmcode nicht sinnvoll oder zulässig.\)  
  
 Sie erstellen eine Bitflagenumeration, indem Sie das <xref:System.FlagsAttribute?displayProperty=fullName>\-Attribut anwenden und die Werte entsprechend definieren, damit biweise `AND`\-Operationen, `OR`\-Operationen, `NOT`\-Operationen und `XOR`\-Operationen durchgeführt werden können.  Fügen Sie in eine Bitflagenumeration eine benannte Konstante mit dem Wert Null ein, was "Es sind keine Flags festelegt" bedeutet. Weisen Sie einem Flag nicht den Wert Null zu, falls dies nicht "Es sind keine Flags festgelegt" bedeutet.  
  
 Im folgenden Beispiel wird eine andere Version der `Days`\-Enumeration mit dem Namen `Days2` definiert.  `Days2` weist das `Flags`\-Attribut auf, und jedem Wert wird die nächste höhere Potenz von 2 zugewiesen.  So können Sie eine `Days2`\-Variable mit dem Wert `Days2.Tuesday` und `Days2.Thursday` erstellen.  
  
 [!CODE [csProgGuideEnums#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEnums#2)]  
  
 Um ein Flag für einen Enumerator festzulegen, verwenden Sie den bitweisen `OR`\-Operator, wie im folgenden Beispiel dargestellt:  
  
 [!CODE [csProgGuideEnums#6](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEnums#6)]  
  
 Um zu ermittln, ob ein bestimmtes Flag festgelegt ist, verwenden Sie eine bitweise `AND`\-Operation, wie im folgenden Beispiel dargestellt:  
  
 [!CODE [csProgGuideEnums#7](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEnums#7)]  
  
 Weitere Informationen zum Definieren von Enumerationstypen mit dem <xref:System.FlagsAttribute?displayProperty=fullName>\-Attribut finden Sie unter <xref:System.Enum?displayProperty=fullName>.  
  
## Verwenden der System.Enum\-Methoden zur Ermittlung und Behandlung von Enumerationswerten  
 Alle Enumerationen sind Instanzen des <xref:System.Enum?displayProperty=fullName>\-Typs.  Sie können von <xref:System.Enum?displayProperty=fullName> keine neuen Klassen ableiten. Sie können jedoch seine Methoden verwenden, um Informationen darüber zu erhalten und Werte in einer Enumerationsinstanz zu bearbeiten.  
  
 [!CODE [csProgGuideEnums#5](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideEnums#5)]  
  
 Weitere Informationen hierzu finden Sie unter <xref:System.Enum?displayProperty=fullName>.  
  
 Sie können für eine Enumeration auch eine neue Methode erstellen, indem Sie die Erweiterungsmethode verwenden.  Weitere Informationen finden Sie unter [Gewusst wie: Erstellen einer neuen Methode für eine Enumeration](../../csharp/programming-guide/classes-and-structs/how-to-create-a-new-method-for-an-enumeration.md).  
  
## Enthaltenes Buchkapitel  
 [Weitere Informationen zu Variablen](http://go.microsoft.com/fwlink/?LinkId=221230) in [Visual C\-2010 Anfang](http://go.microsoft.com/fwlink/?LinkId=221214)  
  
## Siehe auch  
 <xref:System.Enum?displayProperty=fullName>   
 [C\#\-Programmierhandbuch](../../csharp/programming-guide/index.md)   
 [enum](../../csharp/language-reference/keywords/enum.md)
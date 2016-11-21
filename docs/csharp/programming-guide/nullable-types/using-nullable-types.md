---
title: "Verwenden von auf NULL festlegbaren Typen (C#&#160;Programmierhandbuch) | Microsoft Docs"
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
  - "Typen, die NULL-Werte zulassen [C#], Informationen über Typen, die NULL-Werte zulassen"
ms.assetid: 0bacbe72-ce15-4b14-83e1-9c14e6380c28
caps.latest.revision: 31
caps.handback.revision: 31
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Verwenden von auf NULL festlegbaren Typen (C#&#160;Programmierhandbuch)
Typen, die auf NULL festgelegt werden können, können alle Werte des zugrunde liegenden Typs und einen zusätzlichen [null](../../../csharp/language-reference/keywords/null.md)\-Wert darstellen.  Typen, die auf NULL festgelegt werden können, werden auf zwei verschiedene Arten deklariert:  
  
 `System.Nullable<T> variable`  
  
 \- oder \-  
  
 `T?  variable`  
  
 `T` ist der zugrunde liegende Typ des Nullable\-Typs.  `T` kann ein beliebiger Wert einschließlich `struct` sein; es kann kein Verweistyp sein.  
  
 Nehmen Sie als Beispiel für das Einsatzgebiet eines Typs, der auf NULL festgelegt werden kann, eine boolesche Variable. Sie kann zwei Werte annehmen: true und false.  Es gibt keinen Wert, der "nicht definiert" angibt.  In vielen Programmieranwendungen, besonders bei Datenbankinteraktionen, können Variablen in einem nicht definierten Zustand existieren.  Ein Feld in einer Datenbank kann z. B. den Wert true oder false enthalten, aber es kann auch überhaupt keinen Wert enthalten.  Auf ähnliche Weise können Referenztypen auf `null` festgelegt werden, um anzugeben, dass sie nicht initialisiert sind.  
  
 Diese Ungleichheit kann zu zusätzlichem Programmiereraufwand führen – beispielsweise zusätzliche Variablen zum Speichern von Zustandsinformationen, spezielle Werte usw.  Der Modifizierer für Typen, die auf NULL festgelegt werden können, ermöglicht in C\# das Erstellen von Werttypvariablen, die einen nicht definierten Wert angeben.  
  
## Beispiele von Typen, die auf NULL festgelegt werden können  
 Jeder Werttyp kann als Grundlage für einen Typ verwenden werden, der auf NULL festgelegt werden kann.  Beispiele:  
  
 [!CODE [csProgGuideTypes#4](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#4)]  
  
## Die Member der Typen, die auf NULL festgelegt werden können  
 Jede Instanz eines auf NULL festlegbaren Typs besitzt zwei öffentliche schreibgeschützte Eigenschaften:  
  
-   `HasValue`  
  
     `HasValue` ist vom Typ `bool`.  Sie wird auf `true` festgelegt, wenn die Variable einen Wert ungleich NULL enthält.  
  
-   `Value`  
  
     `Value` hat denselben Typ wie der zugrunde liegende Typ.  Wenn `HasValue` den Wert `true` hat, enthält `Value` einen sinnvollen Wert.  Wenn `HasValue` den Wert `false` hat, löst das Zugreifen auf `Value` eine <xref:System.InvalidOperationException> aus.  
  
 In diesem Beispiel wird mit dem `HasValue`\-Member getestet, ob die Variable einen Wert enthält, bevor versucht wird, diese anzuzeigen.  
  
 [!CODE [csProgGuideTypes#5](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#5)]  
  
 Dieser Test kann auch wie in folgendem Beispiel ausgeführt werden:  
  
 [!CODE [csProgGuideTypes#6](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#6)]  
  
## Explizite Konvertierungen  
 Ein auf NULL festlegbarer Typ kann in einen regulären Typ umgewandelt werden. Dies kann entweder explizit mit einer Umwandlung oder mit der `Value`\-Eigenschaft erfolgen.  Beispiele:  
  
 [!CODE [csProgGuideTypes#7](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#7)]  
  
 Wenn eine benutzerdefinierte Konvertierung zwischen zwei Datentypen festgelegt wird, kann dieselbe Konvertierung auch für auf NULL festlegbare Versionen dieser Datentypen verwendet werden.  
  
## Implizite Konvertierungen  
 Eine Variable eines auf NULL festlegbaren Typs kann mit dem Schlüsselwort `null` auf NULL festgelegt werden, wie im folgenden Beispiel gezeigt:  
  
 [!CODE [csProgGuideTypes#8](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#8)]  
  
 Die Konvertierung von einem gewöhnlichen Typ in einen auf NULL festlegbaren Typ ist implizit.  
  
 [!CODE [csProgGuideTypes#9](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#9)]  
  
## Operatoren  
 Die vordefinierten unären und binären Operatoren sowie alle für Werttypen vorhandenen benutzerdefinierten Operatoren können auch von auf NULL festlegbaren Typen verwendet werden.  Diese Operatoren generieren einen NULL\-Wert, wenn die Operanden auf NULL festgelegt sind. Ansonsten verwendet der Operand den enthaltenen Wert, um das Ergebnis zu berechnen.  Beispiele:  
  
 [!CODE [csProgGuideTypes#10](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#10)]  
  
 Wenn Sie Vergleiche mit Typen ausführen, die NULL\-Werte zulassen, und der Wert eines Typs NULL ist, der Wert des anderen Typs jedoch nicht, werden alle Vergleiche außer `!=` \(ungleich\) als `false` ausgewertet.  Daher sollt keinesfalls angenommen werden, dass wenn ein bestimmter Vergleich `false` zurückgibt, im entgegengesetzten Fall `true` zurückgegeben wird.  Im folgenden Beispiel ist 10 weder größer als noch kleiner als noch gleich NULL.  Nur `num1 != num2` wird als `true` ausgewertet.  
  
 [!CODE [csProgGuideTypes#11](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#11)]  
  
 Ein Gleichheitsvergleich zweier Typen, die NULL\-Werte zulassen und beide NULL sind, wird als `true` ausgewertet.  
  
## Der ??Operator  
 Der Operator `??` definiert einen Standardwert, der zurückgegeben wird, wenn ein auf NULL festlegbarer Typ einem Typ zugewiesen wird, der nicht auf NULL festgelegt werden kann.  
  
 [!CODE [csProgGuideTypes#12](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#12)]  
  
 Dieser Operator kann auch mit mehreren auf NULL festlegbaren Typen verwendet werden.  Beispiele:  
  
 [!CODE [csProgGuideTypes#13](../CodeSnippet/VS_Snippets_VBCSharp/CsProgGuideTypes#13)]  
  
## Der bool?\-type  
 Der auf NULL festlegbare `bool?`\-Typ kann drei verschiedene Werte enthalten: [true](../../../csharp/language-reference/keywords/true.md), [false](../../../csharp/language-reference/keywords/false.md) und [null](../../../csharp/language-reference/keywords/null.md).  Weitere Informationen zur Umwandlung von einem bool?\-Typ  in einen bool\-Typ finden Sie unter [Gewusst wie: Sichere Umwandlung von bool? in bool](../../../csharp/programming-guide/nullable-types/how-to-safely-cast-from-bool-to-bool.md).  
  
 Auf NULL festlegbare boolesche Typen entsprechen den in SQL verwendeten Variablen vom Typ Boolean.  Um sicherzustellen, dass die von `&` erstellten Ergebnisse und  `|` Operatoren sind mit dem booleschen Typ mit drei Werten in SQL konsistent. Die folgenden vordefinierten Operatoren werden bereitgestellt:  
  
 `bool?  operator &(bool?  x, bool?  y)`  
  
 `bool?  operator |(bool?  x, bool?  y)`  
  
 Die Ergebnisse dieser Operatoren sind in der folgenden Tabelle aufgeführt:  
  
|X|y|x&y|x&#124;y|  
|-------|-------|---------|--------------|  
|true|true|true|true|  
|true|false|false|true|  
|true|null|null|true|  
|false|true|false|true|  
|false|false|false|false|  
|false|null|false|null|  
|null|true|null|true|  
|null|false|false|null|  
|null|null|null|null|  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [Typen, die NULL\-Werte zulassen](../../../csharp/programming-guide/nullable-types/index.md)   
 [Boxing von Typen, die NULL\-Werte zulassen](../../../csharp/programming-guide/nullable-types/boxing-nullable-types.md)   
 [Nullable Value Types](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
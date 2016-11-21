---
title: "Type of optional value for optional parameter &lt;parametername&gt; is not CLS-compliant | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "BC40042"
  - "vbc40042"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "BC40042"
ms.assetid: 1d6eae29-4ad3-4434-bde4-a53b6051adf5
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Type of optional value for optional parameter &lt;parametername&gt; is not CLS-compliant
Eine Prozedur ist als `<CLSCompliant(True)>` markiert, deklariert jedoch einen [Optional](../../../visual-basic/language-reference/modifiers/optional.md)\-Parameter mit einem nicht kompatiblen Typ als Standardwert.  
  
 Damit eine Prozedur mit der [Sprachenunabhängigkeit und sprachunabhängige Komponenten](../Topic/Language%20Independence%20and%20Language-Independent%20Components.md) \(CLS\) kompatibel ist, darf sie nur CLS\-kompatible Typen verwenden.  Dies gilt für die Parametertypen, den Rückgabetyp und die Typen aller ihrer lokalen Variablen.  Dies gilt auch für die Standardwerte optionaler Parameter.  
  
 Die folgenden [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Datentypen sind nicht CLS\-kompatibel:  
  
-   [SByte Data Type](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [UInteger Data Type](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [ULong Data Type](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [UShort Data Type](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 Wenn Sie das <xref:System.CLSCompliantAttribute>\-Attribut auf ein Programmierelement anwenden, legen Sie den `isCompliant`\-Parameter des Attributs auf `True` oder auf `False` fest, um die Kompatibilität bzw. Nichtkompatibilität anzugeben.  Es gibt keinen Standardwert für diesen Parameter, und Sie müssen einen Wert angeben.  
  
 Wenn Sie <xref:System.CLSCompliantAttribute> auf ein Element nicht anwenden, wird dieses als nicht kompatibel betrachtet.  
  
 Standardmäßig ist diese Meldung eine Warnung.  Informationen über das Ausblenden von Warnungen bzw. über die Behandlung von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](/visual-studio/ide/configuring-warnings-in-visual-basic).  
  
 **Fehler\-ID:** BC40042  
  
### So beheben Sie diesen Fehler  
  
-   Wenn der optionale Parameter als Standardwert diesen speziellen Typ aufweisen muss, entfernen Sie <xref:System.CLSCompliantAttribute>.  Die Prozedur kann nicht CLS\-kompatibel sein.  
  
-   Wenn die Prozedur CLS\-kompatibel sein muss, ändern Sie den Typ dieses Standardwerts in den ähnlichsten CLS\-kompatiblen Typ.  Möglicherweise können Sie z. B. `Integer` anstelle von `UInteger` verwenden, wenn Sie den Wertebereich über 2.147.483.647 nicht benötigen.  Wenn Sie den erweiterten Bereich benötigen, können Sie `UInteger` durch `Long` ersetzen.  
  
-   Wenn Sie Verbindungen mit Automatisierungs\- oder COM\-Objekten verwenden, beachten Sie, dass einige Typen über andere Datenbreiten als in [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] verfügen.  Beispielsweise umfasst `int` in anderen Umgebungen oft 16 Bits.  Wenn Sie eine 16\-Bit\-Ganzzahl von einer solchen Komponente akzeptieren, deklarieren Sie sie im verwalteten [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Code als `Short` und nicht als `Integer`.  
  
## Siehe auch  
 [\<PAVE OVER\> Writing CLS\-Compliant Code](http://msdn.microsoft.com/de-de/4c705105-69a2-4e5e-b24e-0633bc32c7f3)
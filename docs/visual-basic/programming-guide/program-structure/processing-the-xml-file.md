---
title: "Processing the XML File (Visual Basic) | Microsoft Docs"
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
  - "XML comments, parsing [Visual Basic]"
ms.assetid: 78a15cd0-7708-4e79-85d1-c154b7a14a8c
caps.latest.revision: 16
caps.handback.revision: 16
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Processing the XML File (Visual Basic)
Für jedes Konstrukt, das zum Generieren von Dokumentation gekennzeichnet ist, wird vom Compiler eine ID\-Zeichenfolge generiert.  \(Informationen zum Kennzeichnen des Codes finden Sie unter [XML Comment Tags](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md).\) Das Konstrukt wird von der ID\-Zeichenfolge eindeutig identifiziert.  Programme, von denen die XML\-Datei verarbeitet wird, können das entsprechende [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)]\-Metadaten\-\/Reflektionselement mithilfe der ID\-Zeichenfolge identifizieren.  
  
 Die XML\-Datei enthält keine hierarchische Darstellung des Codes. Es handelt sich um eine unstrukturierte Liste mit einer generierten ID für jedes Element.  
  
 Die folgenden Regeln werden vom Compiler beim Generieren der ID\-Zeichenfolgen beachtet:  
  
-   Die Zeichenfolge darf keine Leerräume enthalten.  
  
-   Der erste Teil der ID\-Zeichenfolge kennzeichnet die Art des zu identifizierenden Members durch ein einzelnes Zeichen, gefolgt von einem Doppelpunkt.  Die folgenden Membertypen werden verwendet.  
  
|||  
|-|-|  
|Zeichen|Beschreibung|  
|N|\-Namespace<br /><br /> Einem Namespace können keine Dokumentationskommentare hinzugefügt werden. Sie können jedoch CREF\-Verweise hinzufügen, falls diese unterstützt werden.|  
|T|Typ: `Class`, `Module`, `Interface`, `Structure`, `Enum`, `Delegate`|  
|F|Feld: `Dim`|  
|P|Eigenschaft: `Property` \(einschließlich Standardeigenschaften\)|  
|M|Methode: `Sub`, `Function`, `Declare`, `Operator`|  
|E|Ereignis: `Event`|  
|\!|Fehlerzeichenfolge<br /><br /> Der verbleibende Teil der Zeichenfolge enthält Fehlerinformationen.  Vom [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler werden Fehlerinformationen für Links generiert, die nicht aufgelöst werden können.|  
  
-   Beim zweiten Teil von `String` handelt es sich um den vollqualifizierten Namen des Elements, beginnend mit dem Stamm des Namespaces.  Der Name des Elements, der bzw. die einschließende\(n\) Typ\(en\) und der Namespace sind durch Punkte getrennt.  Wenn der Name des Elements selbst Punkte enthält, werden sie durch ein Nummernzeichen \(\#\) ersetzt.  Es wird vorausgesetzt, dass kein Element ein Nummernzeichen direkt im Namen aufweist.  Der vollqualifizierte Name des `String`\-Konstruktors würde beispielsweise `System.String.#ctor` lauten.  
  
-   Wenn es sich bei Eigenschaften und Methoden um Argumente der Methode handelt, folgt die in Klammern eingeschlossene Argumentliste.  Wenn keine Argumente vorhanden sind, werden keine Klammern verwendet.  Die Argumente werden durch Kommas voneinander getrennt.  Die Codierung jedes Arguments erfolgt genauso wie die Codierung in einer [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)]\-Signatur:  
  
## Beispiel  
 Im folgenden Codebeispiel wird die Generierung der ID\-Zeichenfolgen für eine Klasse und deren Member dargestellt:  
  
 [!CODE [VbVbcnXmlDocComments#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnXmlDocComments#10)]  
  
## Siehe auch  
 [\/doc](../../../visual-basic/reference/command-line-compiler/doc.md)   
 [How to: Create XML Documentation](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)
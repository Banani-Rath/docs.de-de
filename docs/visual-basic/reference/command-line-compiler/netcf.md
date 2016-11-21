---
title: "/netcf | Microsoft Docs"
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
  - "/netcf"
  - "netcf"
dev_langs: 
  - "VB"
helpviewer_keywords: 
  - "-netcf compiler option [Visual Basic]"
  - "netcf compiler option [Visual Basic]"
  - "/netcf compiler option [Visual Basic]"
ms.assetid: db7cfa59-c315-401c-a59b-0daf355343d6
caps.latest.revision: 18
caps.handback.revision: 18
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# /netcf
Legt fest, dass der Compiler [!INCLUDE[Compact](../../../visual-basic/reference/command-line-compiler/includes/compact_md.md)] als Zielplattform verwendet.  
  
## Syntax  
  
```  
/netcf  
```  
  
## Hinweise  
 Die `/netcf`\-Option bewirkt, dass der [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Compiler auf [!INCLUDE[Compact](../../../visual-basic/reference/command-line-compiler/includes/compact_md.md)] statt auf das vollständige [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] abzielt.  Die Sprachfunktionalität, die nur im vollständigen [!INCLUDE[dnprdnshort](../../../csharp/getting-started/includes/dnprdnshort_md.md)] verfügbar ist, wird deaktiviert.  
  
 Die `/netcf`\-Option ist für die Verwendung mit [\/sdkpath](../../../visual-basic/reference/command-line-compiler/sdkpath.md) vorgesehen.  Die Sprachfeatures, die durch `/netcf` deaktiviert werden, sind die Sprachfeatures, die in den durch `/sdkpath` verwendeten Dateien nicht verfügbar sind.  
  
> [!NOTE]
>  Die `/netcf`\-Option ist innerhalb der Entwicklungsumgebung von Visual Studio nicht verfügbar, sondern nur bei der Kompilierung über die Befehlszeile.  Die `/netcf`\-Option wird festgelegt, wenn ein [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Geräteprojekt geladen wird.  
  
 Die `/netcf`\-Option ändert die folgenden Sprachfeatures:  
  
-   Das [End \<keyword\> Statement](../../../visual-basic/language-reference/statements/end-keyword-statement.md)\-Schlüsselwort, das die Ausführung eines Programms beendet, wird deaktiviert.  Das folgende Programm wird kompiliert und ausgeführt, wenn `/netcf` nicht angegeben wurde. Bei der Angabe von `/netcf` schlägt es aber während der Kompilierung fehl.  
  
     [!CODE [VbVbalrCompiler#34](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#34)]  
  
-   Alle Formen des späten Bindens werden deaktiviert.  Fehler beim Kompilieren werden generiert, wenn bekannte Szenarios für spätes Binden festgestellt werden.  Das folgende Programm wird kompiliert und ausgeführt, wenn `/netcf` nicht angegeben wurde. Bei der Angabe von `/netcf` schlägt es aber während der Kompilierung fehl.  
  
     [!CODE [VbVbalrCompiler#35](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#35)]  
  
-   Die Modifizierer [Auto](../../../visual-basic/language-reference/modifiers/auto.md), [Ansi](../../../visual-basic/language-reference/modifiers/ansi.md) und [Unicode](../../../visual-basic/language-reference/modifiers/unicode.md) werden deaktiviert.  Die Syntax der [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md)\-Anweisung wird in `Declare Sub|Function name Lib "library" [Alias "alias"] [([arglist])]` geändert.  Das folgende Codebeispiel veranschaulicht, wie sich `/netcf` auf eine Kompilierung auswirkt.  
  
     [!CODE [VbVbalrCompiler#36](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrCompiler#36)]  
  
-   Bei Verwendung von Visual Basic 6.0\-Schlüsselwörtern, die aus [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] entfernt wurden, werden andere Fehler generiert als bei Angabe von `/netcf`.  Dies hat Auswirkungen auf die Fehlermeldungen für die folgenden Schlüsselwörter:  
  
    -   `Open`  
  
    -   `Close`  
  
    -   `Put`  
  
    -   `Print`  
  
    -   `Write`  
  
    -   `Input`  
  
    -   `Lock`  
  
    -   `Unlock`  
  
    -   `Seek`  
  
    -   `Width`  
  
    -   `Name`  
  
    -   `FreeFile`  
  
    -   `EOF`  
  
    -   `Loc`  
  
    -   `LOF`  
  
    -   `Line`  
  
## Beispiel  
 Mit dem folgenden Code wird `Myfile.vb` mit [!INCLUDE[Compact](../../../visual-basic/reference/command-line-compiler/includes/compact_md.md)] kompiliert. Dabei werden die Versionen von Mscorlib.dll und Microsoft.VisualBasic.dll verwendet, die sich im Standardinstallationsverzeichnis von [!INCLUDE[Compact](../../../visual-basic/reference/command-line-compiler/includes/compact_md.md)] auf Laufwerk C befinden.  In der Regel verwenden Sie die neueste Version von [!INCLUDE[Compact](../../../visual-basic/reference/command-line-compiler/includes/compact_md.md)].  
  
```  
vbc /netcf /sdkpath:"c:\Program Files\Microsoft Visual Studio .NET 2003\CompactFrameworkSDK\v1.0.5000\Windows CE " myfile.vb  
```  
  
## Siehe auch  
 [Visual Basic Command\-Line Compiler](../../../visual-basic/reference/command-line-compiler/index.md)   
 [Beispiele für Kompilierungsbefehlszeilen](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)   
 [\/sdkpath](../../../visual-basic/reference/command-line-compiler/sdkpath.md)
---
title: "/define (C# Compiler Options) | Microsoft Docs"
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
  - "/define"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "-define compiler option [C#]"
  - "/define compiler option [C#]"
  - "-d compiler option [C#]"
  - "define compiler option [C#]"
  - "/d compiler option [C#]"
  - "d compiler option [C#]"
ms.assetid: f17d7b4d-82d0-4133-8563-68cced1cac6e
caps.latest.revision: 21
caps.handback.revision: 21
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# /define (C# Compiler Options)
Die Option **\/define** definiert `name` als Symbol in allen Quellcodedateien Ihres Programms.  
  
## Syntax  
  
```  
/define:name[;name2]  
```  
  
## Argumente  
 `name`, `name2`  
 Der Name eines oder mehrerer Symbole, die Sie definieren möchten.  
  
## Hinweise  
 Die Option **\/define** hat dieselbe Auswirkung wie die Verwendung eines [\#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md)\-Präprozessordirektiven, außer dass die Compileroption für alle Dateien im Projekt gültig ist.  Ein Symbol bleibt in einer Quelldatei definiert, bis eine [\#undef](../../../csharp/language-reference/preprocessor-directives/preprocessor-undef.md)\-Direktive in der Quelldatei die Definition entfernt.  Wenn Sie die Option \/define verwenden, hat eine `#undef`\-Direktive in einer Datei keinerlei Auswirkung auf andere Quellcodedateien im Projekt.  
  
 Sie können die durch diese Option erstellten Symbole in Verbindung mit [\#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md), [\#else](../../../csharp/language-reference/preprocessor-directives/preprocessor-else.md), [\#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) und [\#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) verwenden, um Quelldateien bedingt zu kompilieren.  
  
 **\/d** ist die Kurzform von **\/define**.  
  
 Sie können mehrere Symbole mit **\/define** definieren, indem Sie die Symbolnamen jeweils durch ein Semikolon oder Komma voneinander trennen.  Beispiel:  
  
```  
/define:DEBUG;TUESDAY  
```  
  
 Der C\# \-Compiler selbst definiert keine Symbole oder Makros, die Sie im Quellcode verwenden können. Alle Symboldefinitionen müssen benutzerdefiniert sein.  
  
> [!NOTE]
>  Anders als in Programmiersprachen wie C\+\+ ist es in C\# bei Verwendung von `#define` nicht zulässig, einem Symbol einen Wert zuzuweisen.  Beispielsweise kann `#define` nicht zum Erstellen eines Makros oder zum Definieren einer Konstante verwendet werden.  Falls Sie eine Konstante definieren müssen, verwenden Sie eine `enum`\-Variable.  Wenn Sie ein C\+\+\-übliches Makro erstellen möchten, erwägen Sie Alternativen wie Generika.  Da Makros sehr fehleranfällig sind, ist ihre Verwendung in C\# nicht zugelassen. Es stehen jedoch sicherere Alternativen zur Verfügung.  
  
### So legen Sie diese Compileroption in der Visual Studio\-Entwicklungsumgebung fest  
  
1.  Öffnen Sie die **Eigenschaften**\-Seite des Projekts.  
  
2.  Geben Sie auf der Registerkarte **Erstellen** im Feld **Symbole für bedingte Kompilierung** das zu definierende Symbol ein.  Wenn Sie z. B. das folgende Codebeispiel verwenden, geben Sie im Textfeld einfach `xx` ein.  
  
 Informationen zum programmgesteuerten Festlegen dieser Compileroption finden Sie unter <xref:VSLangProj80.CSharpProjectConfigurationProperties3.DefineConstants%2A>.  
  
## Beispiel  
  
```  
// preprocessor_define.cs  
// compile with: /define:xx  
// or uncomment the next line  
// #define xx  
using System;  
public class Test   
{  
    public static void Main()   
    {  
        #if (xx)   
            Console.WriteLine("xx defined");  
        #else  
            Console.WriteLine("xx not defined");  
        #endif  
    }  
}  
```  
  
## Siehe auch  
 [C\# Compiler Options](../../../csharp/language-reference/compiler-options/index.md)   
 [Gewusst wie: Ändern von Projekteigenschaften und Konfigurationseinstellungen](http://msdn.microsoft.com/de-de/e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)
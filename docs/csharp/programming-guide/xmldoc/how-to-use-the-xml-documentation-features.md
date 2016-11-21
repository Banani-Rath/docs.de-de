---
title: "Gewusst wie: Verwenden der XML-Dokumentationsfeatures (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "C#-Sprache, XML-Dokumentationsfeatures"
  - "XML-Dokumentation [C#]"
ms.assetid: 8f33917b-9577-4c9a-818a-640dbbb0b399
caps.latest.revision: 19
caps.handback.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Verwenden der XML-Dokumentationsfeatures (C#-Programmierhandbuch)
Im folgenden Beispiel wird eine grundlegende Übersicht über eines Typs, der dokumentiert wurde.  
  
## Beispiel  
 [!CODE [csProgGuideDocComments#15](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#15)]  
  
  **\/\/diese XML\-Datei wurde mit dem vorherigen Codebeispiel generiert.  \<?xml version\="1.0"?\>**  
**\<doc\>**  
 **\<assembly\>**  
 **\<name\> xmlsample\<\/name\>**  
 **\<\/assembly\>**  
 **\<members\>**  
 **\<member name\="T:SomeClass"\>**   
 **\<summary\>**  
 **An dieser Stelle steht in der Dokumentation die Zusammenfassung auf Klassenebene.\<\/summary\>**  
 **\<remarks\>**  
 **Mit dem \<remarks\>\-Tag können einem Typ oder Member**   
 **tag\<\/remarks\> durch die Hinweise**  
 **\<\/member\>**  
 **\<member name\="F:SomeClass.m\_Name"\>**   
 **\<summary\>**  
 **Speicher für den Namen property\<\/summary\>**  
 **\<\/member\>**  
 **\<member name\="M:SomeClass.\#ctor"\>**   
 **\<summary\> Die Klasse constructor.\<\/summary\>**   
 **\<\/member\>**  
 **\<member name\="M:SomeClass.SomeMethod\(System.String\)"\>**   
 **\<summary\>**  
 **Beschreibung von SomeMethod.\<\/summary\>**  
 **\<param name\="s"\> Beschreibung der Parameter für here\<\/param\> geht s**  
 **\<seealso cref\="T:System.String"\>**  
 **Sie können mit dem cref\-Attribut für jedes Tag auf einen Typ oder Member verweisen,**   
 **und der Compiler überprüft, ob der Verweis vorhanden ist.  \<\/seealso\>**  
 **\<\/member\>**  
 **\<member name\="M:SomeClass.SomeOtherMethod"\>**   
 **\<summary\>**  
 **Eine andere Methode.  \<\/summary\>**  
 **\<returns\>**  
 **Mit dem \<returns\>\-Tag werden Rückgabeergebnisse beschrieben.\<\/returns\>**  
 **\<seealso cref\="M:SomeClass.SomeMethod\(System.String\)"\>**   
 **Beachten Sie die Verwendung des cref Attribut eine bestimmte Methode zu verweisen \<\/seealso\>**  
 **\<\/member\>**  
 **\<member name\="M:SomeClass.Main\(System.String\[\]\)"\>**   
 **\<summary\>**  
 **Der Einstiegspunkt für die Anwendung.  \<\/summary\>**  
 **\<param name\="args"\> Eine Liste der Befehlszeile arguments\<\/param\>**  
 **\<\/member\>**  
 **\<member name\="P:SomeClass.Name"\>**   
 **\<summary\>**  
 **Name\-Eigenschaft \<\/summary\>**  
 **\<value\>**  
 **Ein Werts tag wird verwendet, um die Eigenschaft zu beschreiben value\<\/value\>**  
 **\<\/member\>**  
 **\<\/members\>**  
**\<\/doc\>**    
## Kompilieren des Codes  
 Zum Kompilieren des Beispiels geben Sie die folgende Befehlszeile ein:  
  
 `csc XMLsample.cs /doc:XMLsample.xml`  
  
 Dadurch wird die XML\-Datei XMLsample.xml, die Sie anzeigen können oder indem Sie im Browser den TYPE\-Befehl verwenden.  
  
## Robuste Programmierung  
 Die XML\-Dokumentation beginnt mit drei Schrägstrichen \(\/\/\/\).  Wenn Sie ein neues Projekt erstellen, fügen der Assistent einige Zeilen in Starter \/\/\/\-.  Die Verarbeitung dieser Kommentare unterliegt einigen Beschränkungen:  
  
-   Die Dokumentation muss regelkonformes XML aufweisen.  Wenn das XML nicht wohl geformt ist, wird eine Warnung ausgegeben, und die Dokumentationsdatei enthält einen Kommentar, der besagt, dass ein Fehler aufgetreten ist.  
  
-   Der Entwickler kann auch eigene Tagsets entwickeln.  Es gibt eine Reihe empfohlener Tags \(finden Sie weiterführende Literatur\-Abschnitt\).  Einige der empfohlenen Tags haben eine besondere Bedeutung:  
  
    -   Das \<param\>\-Tag wird zur Beschreibung von Parametern verwendet.  Bei Verwendung dieses Tags stellt der Compiler sicher, dass der Parameter vorhanden ist und dass alle Parameter in der Dokumentation beschrieben werden.  Falls die Überprüfung fehlschlägt, gibt der Compiler eine Warnung aus.  
  
    -   Das `cref`\-Attribut kann an jedes Tag angefügt werden, um einen Verweis auf ein Codeelement bereitzustellen.  Der Compiler überprüft, ob dieses Codeelement vorhanden ist.  Falls die Überprüfung fehlschlägt, gibt der Compiler eine Warnung aus.  Bei der Suche nach einem im `cref`\-Attribut beschriebenen Typ beachtet der Compiler etwaige `using`\-Anweisungen.  
  
    -   Das \<summary\>\-Tag wird innerhalb von Visual Studio von IntelliSense verwendet, um zusätzliche Informationen über einen Typ oder einen Member anzuzeigen.  
  
        > [!NOTE]
        >  Die XML\-Datei enthält keine genauen Informationen über den Typ und die Member enthält \(z. B. keine Typinformationen\).  Um vollständige Informationen zu einem Typ oder Member zu erhalten, muss die Dokumentationsdatei in Verbindung mit der Reflektion des aktuellen Typs oder Members verwendet werden.  
  
## Siehe auch  
 [C\#\-Programmierhandbuch](../../../csharp/programming-guide/index.md)   
 [\/doc \(Process Documentation Comments\)](../../../csharp/language-reference/compiler-options/doc-compiler-option.md)   
 [XML\-Dokumentationskommentare](../../../csharp/programming-guide/xmldoc/xml-documentation-comments.md)
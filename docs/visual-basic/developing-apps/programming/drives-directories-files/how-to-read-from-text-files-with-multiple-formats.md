---
title: "How to: Read From Text Files with Multiple Formats in Visual Basic | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
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
  - "TextFieldParser object, reading from a file"
  - "TextFieldType enumeration"
  - "My.Computer.FileSystem.WriteAllText method, parsing structured text files"
  - "WriteAllText method, parsing structured text files"
  - "PeekChars method, determining format of text"
  - "reading text files, multiple formats"
  - "I/O [Visual Basic], reading text files"
  - "text files, reading"
ms.assetid: 8d185eb2-79ca-42cd-95a7-d3ff44a5a0f8
caps.latest.revision: 17
caps.handback.revision: 17
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Read From Text Files with Multiple Formats in Visual Basic
Mit dem <xref:Microsoft.VisualBasic.FileIO.TextFieldParser>\-Objekt können strukturierte Textdateien, z. B. Protokolle, leicht und effizient analysiert werden.  Sie können eine Datei mit mehreren Formaten mithilfe der `PeekChars`\-Methode verarbeiten, um das Format der jeweiligen Zeile zu bestimmen, während Sie die Datei analysieren.  
  
### So lesen Sie aus einer Textdatei mit mehreren Formaten  
  
1.  Fügen Sie dem Projekt eine Textdatei mit dem Namen "testfile.txt" hinzu.  Fügen Sie der Textdatei folgenden Inhalt hinzu:  
  
    ```  
    Err  1001 Cannot access resource.  
    Err  2014 Resource not found.  
    Acc  10/03/2009User1      Administrator.  
    Err  0323 Warning: Invalid access attempt.  
    Acc  10/03/2009User2      Standard user.  
    Acc  10/04/2009User2      Standard user.  
    ```  
  
2.  Definieren Sie das erwartete Format und das für das Erfassen eines Fehlers verwendete Format.  Der letzte Eintrag in jedem Array lautet "\-1", daher wird für das letzte Feld eine variable Breite angenommen.  Dies ist der Fall, wenn der letzte Eintrag im Array kleiner oder gleich 0 \(null\) ist.  
  
     [!CODE [VbFileIORead#4](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#4)]  
  
3.  Erstellen Sie ein neues <xref:Microsoft.VisualBasic.FileIO.TextFieldParser>\-Objekt, und definieren Sie Breite und Format.  
  
     [!CODE [VbFileIORead#5](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#5)]  
  
4.  Durchlaufen Sie die Zeilen, und testen Sie das Format vor dem Lesen.  
  
     [!CODE [VbFileIORead#6](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#6)]  
  
5.  Geben Sie Fehler auf der Konsole aus.  
  
     [!CODE [VbFileIORead#7](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#7)]  
  
## Beispiel  
 Im Folgenden ist ein vollständiges Beispiel aus der Datei `testfile.txt` aufgeführt.  
  
 [!CODE [VbFileIORead#8](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#8)]  
  
## Robuste Programmierung  
 Unter den folgenden Bedingungen kann eine Ausnahme ausgelöst werden:  
  
-   Eine Zeile kann nicht mit dem angegebenen Format analysiert werden \(<xref:Microsoft.VisualBasic.FileIO.MalformedLineException>\).  In der Ausnahmemeldung wird die Nummer der Zeile angegeben, die die Ausnahme verursacht hat. Der in der Zeile enthaltene Text wird der <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine%2A>\-Eigenschaft zugewiesen.  
  
-   Die angegebene Datei ist nicht vorhanden \(<xref:System.IO.FileNotFoundException>\).  
  
-   Es besteht eine teilweise vertrauenswürdige Situation, in der der Benutzer nicht über ausreichende Berechtigungen für den Zugriff auf die Datei verfügt.  \(<xref:System.Security.SecurityException>\).  
  
-   Der Pfad ist zu lang \(<xref:System.IO.PathTooLongException>\).  
  
-   Der Benutzer verfügt nicht über ausreichende Berechtigungen für den Zugriff auf die Datei \(<xref:System.UnauthorizedAccessException>\).  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser?displayProperty=fullName>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.PeekChars%2A>   
 <xref:Microsoft.VisualBasic.FileIO.MalformedLineException>   
 <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.EndOfData%2A>   
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.TextFieldType%2A>   
 [How to: Read From Comma\-Delimited Text Files](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)   
 [How to: Read From Fixed\-width Text Files](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-fixed-width-text-files.md)   
 [Parsing Text Files with the TextFieldParser Object](../../../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)
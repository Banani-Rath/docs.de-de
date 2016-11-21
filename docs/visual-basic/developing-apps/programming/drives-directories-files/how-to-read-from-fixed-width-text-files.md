---
title: "How to: Read From Fixed-width Text Files in Visual Basic | Microsoft Docs"
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
  - "fixed-width text file"
  - "reading text files, fixed-width"
  - "files, parsing"
  - "text files, tasks"
  - "text files, reading"
ms.assetid: 99be5692-967a-4e85-993e-cd18139a5a69
caps.latest.revision: 24
caps.handback.revision: 24
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Read From Fixed-width Text Files in Visual Basic
Mit dem `TextFieldParser`\-Objekt können strukturierte Textdateien, z. B. Protokolle, leicht und effizient analysiert werden.  
  
 Die `TextFieldType`\-Eigenschaft definiert, ob es sich bei der analysierten Datei um eine Datei mit Trennzeichen oder um eine Datei mit Textfeldern fester Breite handelt.  In einer Textdatei mit fester Breite kann das Feld am Ende über eine variable Breite verfügen.  Legen Sie für ein Feld eine Breite von kleiner oder gleich 0 \(null\) fest, wenn das Feld am Ende über eine variable Breite verfügen soll.  
  
### So analysieren Sie eine Textdatei mit fester Breite  
  
1.  Erstellen Sie einen neuen `TextFieldParser`.  Im folgenden Code wird ein `TextFieldParser` mit dem Namen `Reader` erstellt und die Datei `test.log` geöffnet.  
  
     [!CODE [VbFileIORead#9](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#9)]  
  
2.  Definieren Sie die `TextFieldType`\-Eigenschaft als `FixedWidth`, und geben Sie die Breite und das Format an.  Im Beispiel werden die Textspalten wie folgt definiert: die erste Spalte ist 5 Zeichen breit, die zweite 10, die dritte 11 und die vierte Spalte weist eine variable Breite auf.  
  
     [!CODE [VbFileIORead#10](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#10)]  
  
3.  Die Felder in der Datei werden durchlaufen.  Falls eine beschädigte Zeile gefunden wird, wird ein Fehler gemeldet und die Analyse fortgesetzt.  
  
     [!CODE [VbFileIORead#11](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#11)]  
  
4.  Der `While`\-Block und der `Using`\-Block werden mit `End While` und `End Using` geschlossen.  
  
     [!CODE [VbFileIORead#12](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#12)]  
  
## Beispiel  
 In diesem Beispiel wird aus der Datei `test.log` gelesen.  
  
 [!CODE [VbFileIORead#13](../CodeSnippet/VS_Snippets_VBCSharp/VbFileIORead#13)]  
  
## Robuste Programmierung  
 Unter den folgenden Bedingungen kann eine Ausnahme ausgelöst werden:  
  
-   Eine Zeile kann nicht mit dem angegebenen Format analysiert werden \(<xref:Microsoft.VisualBasic.FileIO.MalformedLineException>\).  In der Ausnahmemeldung wird die Nummer der Zeile angegeben, die die Ausnahme verursacht hat. Der in der Zeile enthaltene Text wird der <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.ErrorLine%2A>\-Eigenschaft zugewiesen.  
  
-   Die angegebene Datei ist nicht vorhanden \(<xref:System.IO.FileNotFoundException>\).  
  
-   Es besteht eine teilweise vertrauenswürdige Situation, in der der Benutzer nicht über ausreichende Berechtigungen für den Zugriff auf die Datei verfügt.  \(<xref:System.Security.SecurityException>\).  
  
-   Der Pfad ist zu lang \(<xref:System.IO.PathTooLongException>\).  
  
-   Der Benutzer verfügt nicht über ausreichende Berechtigungen für den Zugriff auf die Datei \(<xref:System.UnauthorizedAccessException>\).  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser?displayProperty=fullName>   
 [How to: Read From Comma\-Delimited Text Files](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)   
 [How to: Read From Text Files with Multiple Formats](../../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-text-files-with-multiple-formats.md)   
 [Parsing Text Files with the TextFieldParser Object](../../../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)   
 [Walkthrough: Manipulating Files and Directories in Visual Basic](../../../../visual-basic/developing-apps/programming/drives-directories-files/walkthrough-manipulating-files-and-directories.md)   
 [Troubleshooting: Reading from and Writing to Text Files](../../../../visual-basic/developing-apps/programming/drives-directories-files/troubleshooting-reading-from-and-writing-to-text-files.md)   
 [Problembehandlung bei Ausnahmen: Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException](../Topic/Troubleshooting%20Exceptions:%20Microsoft.VisualBasic.FileIO.TextFieldParser.MalformedLineException.md)
---
title: "Walkthrough: Defining Classes (Visual Basic) | Microsoft Docs"
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
  - "execution, ending"
  - "objects [Visual Basic], initializing"
  - "Initialize event"
  - "files, closing"
  - "programs, quitting"
  - "code, exiting"
  - "objects [Visual Basic], creating"
  - "program termination"
  - "classes [Visual Basic], walkthroughs"
  - "class modules, walkthroughs"
  - "Terminate event"
  - "execution, stopping"
ms.assetid: 07018828-2d49-4cf5-a44b-19fb15d9efea
caps.latest.revision: 21
caps.handback.revision: 21
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Walkthrough: Defining Classes (Visual Basic)
In dieser exemplarischen Vorgehensweise wird demonstriert, wie Klassen definiert werden, die zum Erstellen von Objekten verwendet werden können.  Darüber hinaus werden das Hinzufügen von Eigenschaften und Methoden zur neuen Klasse und die Initialisierung von Objekten erläutert.  
  
 [!INCLUDE[note_settings_general](../../../../csharp/language-reference/compiler-messages/includes/note_settings_general_md.md)]  
  
### So definieren Sie eine Klasse  
  
1.  Erstellen Sie ein Projekt, indem Sie im Menü **Datei** auf **Neues Projekt** klicken.  Das Dialogfeld **Neues Projekt** wird angezeigt.  
  
2.  Wählen Sie Windows\-Anwendung aus der Liste mit [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]\-Projektvorlagen aus, um das neue Projekt anzuzeigen.  
  
3.  Fügen Sie dem Projekt eine neue Klasse hinzu, indem Sie im Menü **Projekt** auf **Klasse hinzufügen** klicken.  Das Dialogfeld **Neues Element hinzufügen** wird angezeigt.  
  
4.  Wählen Sie die Vorlage **Klasse** aus.  
  
5.  Nennen Sie die neue Klasse `UserNameInfo.vb`, und klicken Sie dann auf **Hinzufügen**, um den Code für die neue Klasse anzuzeigen.  
  
     [!CODE [VbVbalrOOP#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#5)]  
  
    > [!NOTE]
    >  Mit dem **Code\-Editor** von [!INCLUDE[vbprvb](../../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)] können Sie dem Startformular eine Klasse hinzufügen, indem Sie das `Class`\-Schlüsselwort und anschließend den Namen der neuen Klasse eingeben.  Der **Code\-Editor** fügt automatisch eine entsprechende `End Class`\-Anweisung hinzu.  
  
6.  Definieren Sie ein privates Feld für die Klasse, indem Sie den folgenden Code zwischen die Anweisungen `Class` und `End Class` einfügen:  
  
     [!CODE [VbVbalrOOP#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#7)]  
  
     Die Deklaration des Felds als `Private` bedeutet, dass es nur innerhalb der Klasse verwendet werden kann.  Um von außerhalb einer Klasse auf Felder zugreifen zu können, können Sie Zugriffsmodifizierer verwenden. Diese ermöglichen einen erweiterten Zugriff, z. B. `Public`.  Weitere Informationen finden Sie unter [Access Levels in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
7.  Definieren Sie für die Klasse eine Eigenschaft, indem Sie den folgenden Code hinzufügen:  
  
     [!CODE [VbVbalrOOP#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#8)]  
  
8.  Definieren Sie für die Klasse eine Methode, indem Sie den folgenden Code hinzufügen:  
  
     [!CODE [VbVbalrOOP#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#9)]  
  
9. Definieren Sie für die neue Klasse einen parametrisierten Konstruktor, indem Sie eine Prozedur mit der Bezeichnung `Sub New` hinzufügen:  
  
     [!CODE [VbVbalrOOP#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#10)]  
  
     Der `Sub New`\-Konstruktor wird automatisch aufgerufen, wenn ein auf dieser Klasse basierendes Objekt erstellt wird.  Dieser Konstruktor legt den Wert des Felds fest, das den Benutzernamen enthält.  
  
### So erstellen Sie eine Schaltfläche zum Test der Klasse  
  
1.  Ändern Sie den Modus des Startformulars auf Entwurfsmodus, indem Sie im **Projektmappen\-Explorer** mit der rechten Maustaste auf den Formularnamen und anschließend auf **Ansicht\-Designer** klicken.  Das Startformular für Windows\-Anwendungsprojekte erhält standardmäßig die Bezeichnung Form1.vb.  Daraufhin wird das Hauptformular angezeigt.  
  
2.  Fügen Sie dem Hauptformular eine Schaltfläche hinzu, und doppelklicken Sie darauf, um den Code für den `Button1_Click`\-Ereignishandler anzuzeigen.  Fügen Sie zum Aufrufen der Testprozedur den folgenden Code hinzu:  
  
     [!CODE [VbVbalrOOP#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#12)]  
  
### So führen Sie die Anwendung aus  
  
1.  Drücken Sie F5, um die Anwendung auszuführen.  Klicken Sie im Formular auf die Schaltfläche, um die Testprozedur aufzurufen.  Es wird die Meldung angezeigt, dass der ursprüngliche `UserName` "MOORE, BOBBY" lautet, da von der Prozedur die `Capitalize`\-Methode des Objekts aufgerufen wurde.  
  
2.  Klicken Sie auf **OK**, um das Meldungsfeld zu schließen.  Die `Button1 Click`\-Prozedur ändert den Wert der `UserName`\-Eigenschaft und zeigt die Meldung an, dass der neue Wert für `UserName` "Worden, Joe" ist.  
  
## Siehe auch  
 [Objektorientiertes Programmieren](../Topic/Object-Oriented%20Programming%20\(C%23%20and%20Visual%20Basic\).md)   
 [Objects and Classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
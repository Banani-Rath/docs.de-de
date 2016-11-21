---
title: "How to: Draw Lines with the LineShape Control (Visual Studio) | Microsoft Docs"
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
  - "LineShape control"
  - "lines, drawing"
ms.assetid: 83e71b4e-aa76-4f9b-b547-8704309fd1e5
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Draw Lines with the LineShape Control (Visual Studio)
Mit dem <xref:Microsoft.VisualBasic.PowerPacks.LineShape>\-Steuerelement können Sie sowohl zur Entwurfszeit als auch zur Laufzeit horizontale, vertikale oder diagonale Linien auf einem Formular oder Container zeichnen.  
  
 **Hinweis** Auf Ihrem Computer werden möglicherweise andere Namen oder Speicherorte für die Benutzeroberflächenelemente von Visual Studio angezeigt als in den folgenden Anweisungen.  Die von Ihnen verwendete Visual Studio\-Edition und die Einstellungen legen diese Elemente fest.  Weitere Informationen finden Sie unter [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/de-de/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### So zeichnen Sie zur Entwurfszeit eine Linie  
  
1.  Ziehen Sie das <xref:Microsoft.VisualBasic.PowerPacks.LineShape>\-Steuerelement von der Registerkarte **Visual Basic PowerPacks** in der **Toolbox** in ein Formular\- oder Containersteuerelement.  
  
2.  Ziehen Sie die Handles für die Größenanpassung und die Position, um die Größe der Linie festzulegen und deren Position zu bestimmen.  
  
     Sie können Größe und Position der Linie auch festlegen, indem Sie die Eigenschaften `X1`, `X2`, `Y1` und `Y2` im Fenster **Eigenschaften** ändern.  
  
3.  Legen Sie im Fenster **Eigenschaften** ggf. weitere Eigenschaften fest, z. B. `BorderStyle` oder `BorderColor`, um die Darstellung der Linie zu ändern.  
  
### So zeichnen Sie zur Laufzeit eine Linie  
  
1.  Klicken Sie im Menü **Projekt** auf **Verweis hinzufügen**.  
  
2.  Wählen Sie im Dialogfeld **Verweis hinzufügen** die Option **Microsoft.VisualBasic.PowerPacks.VS** aus, und klicken Sie dann auf **OK**.  
  
3.  Fügen Sie im **Code\-Editor** am Anfang des Moduls eine `Imports`\-Anweisung oder eine `using`\-Anweisung hinzu:  
  
    ```vb#  
    Imports Microsoft.VisualBasic.PowerPacks  
    ```  
  
    ```c#  
    using Microsoft.VisualBasic.PowerPacks;  
    ```  
  
4.  Fügen Sie in einer `Event`\-Prozedur den folgenden Code hinzu:  
  
     [!CODE [VbPowerPacksLine#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksLine#1)]  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.PowerPacks.LineShape>   
 [Introduction to the Line and Shape Controls](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-line-and-shape-controls-visual-studio.md)   
 [How to: Draw Shapes with the OvalShape and RectangleShape Controls](../../../visual-basic/developing-apps/windows-forms/how-to-draw-shapes-with-the-ovalshape-and-rectangleshape-controls.md)
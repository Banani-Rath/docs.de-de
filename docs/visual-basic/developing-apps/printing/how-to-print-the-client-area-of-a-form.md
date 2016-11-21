---
title: "Gewusst wie: Drucken des Clientbereichs eines Formulars (Visual Basic) | Microsoft Docs"
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
  - "Clientbereich, Drucken"
ms.assetid: c06c9c0e-bc07-48cd-9596-e29a2ff96236
caps.latest.revision: 15
caps.handback.revision: 15
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Gewusst wie: Drucken des Clientbereichs eines Formulars (Visual Basic)
Mithilfe der <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm>\-Komponente können Sie schnell ein Bild eines Formulars drucken, ohne eine <xref:System.Drawing.Printing.PrintDocument>\-Komponente zu verwenden. Die folgende Vorgehensweise zeigt, wie nur der Clientbereich eines Formulars gedruckt wird, ohne Titelleiste, Rahmen und Scrollleisten.  
  
 Die PowerPack\-Steuerelemente sind nicht mehr in Visual Studio enthalten, Sie können sie jedoch aus dem [Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=25169) herunterladen.  
  
### So drucken Sie den Clientbereich eines Formulars  
  
1.  Klicken Sie in der **Toolbox** auf die Registerkarte **Visual Basic PowerPacks**, und ziehen Sie dann die <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm>\-Komponente auf das Formular.  
  
     Die <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm>\-Komponente wird der Komponentenleiste hinzugefügt.  
  
2.  Legen Sie im Fenster **Eigenschaften** die Eigenschaft <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A> auf <xref:System.Drawing.Printing.PrintAction> fest.  
  
3.  Fügen Sie den folgenden Code in den passenden Ereignishandler ein \(z.B. in den `Click`\-Ereignishandler für eine **Drucken**\-`Button`\).  
  
    ```  
    PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.ClientAreaOnly)  
    ```  
  
    > [!NOTE]
    >  Unter einigen Betriebssystemen werden von den <xref:System.Drawing.Graphics>\-Methoden gezeichnete Text\- oder Grafikelemente möglicherweise nicht ordnungsgemäß gedruckt. Verwenden Sie in diesem Fall diese kompatible Druckmethode: `PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption CompatibleModeClientAreaOnly).`  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction%2A>   
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.Print%2A>   
 [PrintForm Component](../../../visual-basic/developing-apps/printing/printform-component.md)   
 [Gewusst wie: Drucken von Client\- und Nicht\-Client\-Bereichen eines Formulars](../../../visual-basic/developing-apps/printing/how-to-print-client-and-non-client-areas-of-a-form.md)   
 [Gewusst wie: Drucken eines bildlauffähigen Formulars](../../../visual-basic/developing-apps/printing/how-to-print-a-scrollable-form.md)
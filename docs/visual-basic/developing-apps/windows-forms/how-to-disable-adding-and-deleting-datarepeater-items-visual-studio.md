---
title: "How to: Disable Adding and Deleting DataRepeater Items (Visual Studio) | Microsoft Docs"
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
  - "DataRepeater, disabling delete"
  - "DataRepeater, disabling add"
ms.assetid: 298d8f60-ddfe-4361-ab66-cf76d0df5220
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# How to: Disable Adding and Deleting DataRepeater Items (Visual Studio)
Benutzer können standardmäßig Elemente in einem <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>\-Steuerelement hinzufügen und löschen.  Wenn <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> den Fokus hat, können Benutzer durch Drücken von STRG\+N ein neues Element hinzufügen, oder sie verwenden die Schaltfläche **AddNewItem** im <xref:System.Windows.Forms.BindingNavigator>\-Steuerelement.  Wenn <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> den Fokus hat, können Benutzer durch Drücken der ENTF\-TASTE ein Element löschen, oder sie verwenden die Schaltfläche **DeleteItem** im <xref:System.Windows.Forms.BindingNavigator>\-Steuerelement.  
  
 Sie können das Hinzufügen und\/oder Löschen zur Entwurfszeit oder zur Laufzeit deaktivieren.  
  
### So deaktivieren Sie das Hinzufügen und Löschen zur Entwurfszeit  
  
1.  Wählen Sie im Windows Forms\-Designer das <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>\-Steuerelement aus.  
  
    > [!NOTE]
    >  Wählen Sie den unteren Bereich des Steuerelements aus.  Wenn Sie den Elementvorlagenbereich auswählen, werden andere Eigenschaften angezeigt.  
  
2.  Legen Sie im Eigenschaftenfenster die <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToAddItems%2A>\-Eigenschaft auf **False** fest.  
  
3.  Legen Sie die <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToDeleteItems%2A>\-Eigenschaft auf **False** fest.  
  
4.  Wählen Sie im Windows Forms\-Designer das <xref:System.Windows.Forms.BindingNavigator>\-Steuerelement aus, und klicken Sie anschließend auf die Schaltfläche **AddNewItem** \(Schaltfläche mit dem Pluszeichen\).  
  
5.  Legen Sie im Eigenschaftenfenster die <xref:System.Windows.Forms.ToolBarButton.Enabled%2A>\-Eigenschaft auf **False** fest.  
  
6.  Wählen Sie im Windows Forms\-Designer das <xref:System.Windows.Forms.BindingNavigator>\-Steuerelement aus, und klicken Sie anschließend auf die Schaltfläche **DeleteItem** \(Schaltfläche mit dem roten X\).  
  
7.  Legen Sie im Eigenschaftenfenster die <xref:System.Windows.Forms.ToolBarButton.Enabled%2A>\-Eigenschaft auf **False** fest.  
  
8.  Wählen Sie in der Komponentenleiste die <xref:System.Windows.Forms.BindingSource> aus, an die <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> gebunden ist.  
  
9. Legen Sie im Eigenschaftenfenster die <xref:System.Windows.Forms.BindingSource.AllowNew%2A>\-Eigenschaft auf **False** fest.  
  
10. Doppelklicken Sie im Windows Forms\-Designer auf die Schaltfläche **DeleteItem**, um den Code\-Editor zu öffnen.  
  
11. Wählen Sie in der Dropdownliste **Ereignisse** das `BindingNavigatorDeleteItem_EnabledChanged`\-Ereignis aus.  
  
12. Fügen Sie dem `BindingNavigatorDeleteItem_EnabledChanged`\-Ereignishandler folgenden Code hinzu:  
  
     [!CODE [VbPowerPacksDataRepeaterDisableAddDelete#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterDisableAddDelete#1)]  
  
    > [!NOTE]
    >  Dieser Schritt ist erforderlich, da <xref:System.Windows.Forms.BindingSource> die **DeleteItem**\-Schaltfläche bei jeder Änderung des aktuellen Datensatzes aktiviert.  
  
### So deaktivieren Sie das Hinzufügen und Löschen zur Laufzeit  
  
1.  Doppelklicken Sie im Windows Forms\-Designer auf das Formular, um den Code\-Editor zu öffnen.  
  
2.  Fügen Sie folgenden Code zum `Form_Load`\-Ereignis hinzu:  
  
     [!CODE [VbPowerPacksDataRepeaterDisableAddDelete#2](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterDisableAddDelete#2)]  
  
3.  Fügen Sie dem `BindingNavigatorDeleteItem_EnabledChanged`\-Ereignishandler folgenden Code hinzu:  
  
     [!CODE [VbPowerPacksDataRepeaterDisableAddDelete#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterDisableAddDelete#1)]  
  
    > [!NOTE]
    >  Dieser Schritt ist erforderlich, da <xref:System.Windows.Forms.BindingSource> die **DeleteItem**\-Schaltfläche bei jeder Änderung des aktuellen Datensatzes aktiviert.  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>   
 [Introduction to the DataRepeater Control](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)   
 [Troubleshooting the DataRepeater Control](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
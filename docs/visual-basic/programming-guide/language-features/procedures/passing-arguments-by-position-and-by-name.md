---
title: "Passing Arguments by Position and by Name (Visual Basic) | Microsoft Docs"
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
  - "arguments [Visual Basic], passing by name"
  - "procedures, arguments"
  - ":= passing arguments"
  - "procedure arguments"
  - "Visual Basic code, procedures"
  - "named arguments, passing arguments"
  - "arguments [Visual Basic], passing by position"
  - "Function procedures, passing arguments"
  - "named parameters, passing arguments"
  - "named arguments"
  - "passing parameters, named parameter arguments"
  - "passing parameters, by position"
  - "procedures, calling"
  - "named parameters"
  - "Sub procedures, passing arguments"
  - "argument passing"
  - "passing parameters, by name"
  - "argument passing, by position"
  - "arguments [Visual Basic], listing by name"
ms.assetid: 1ad7358f-1da9-48da-a95b-f3c7ed41eff3
caps.latest.revision: 13
caps.handback.revision: 13
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Passing Arguments by Position and by Name (Visual Basic)
Wenn Sie eine `Sub`\- oder `Function`\-Prozedur aufrufen, können Sie Argumente *durch die Position* übergeben, d. h. in der Reihenfolge, in der sie in der Prozedurdefinition aufgeführt werden, oder *durch Namen* unabhängig von der Position.  
  
 Bei der Übergabe eines Arguments durch Namen geben Sie den deklarierten Namen des Arguments, gefolgt von einem Doppelpunkt, einem Gleichheitszeichen \(`:=`\) und dem Argumentwert an.  Benannte Argumente können in beliebiger Reihenfolge angegeben werden.  
  
 Die `Sub`\-Prozedur im folgenden Beispiel übernimmt z. B. drei Argumente:  
  
 [!CODE [VbVbcnProcedures#41](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#41)]  
  
 Bei Aufrufen dieser Prozedur können Sie die Argumente durch Position, durch Namen oder unter Verwendung beider Methoden bereitstellen.  
  
## Übergeben von Argumenten durch Position  
 Die `studentInfo` \-Prozedur kann, wie im folgenden Beispiel gezeigt, mit durch Position übergebenen, durch Kommas getrennten Argumenten aufgerufen werden:  
  
 [!CODE [VbVbcnProcedures#42](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#42)]  
  
 Wenn Sie ein optionales Argument in einer positionellen Argumentliste auslassen, müssen Sie seinen Platz mit einem Komma freihalten.  Im folgenden Beispiel wird `studentInfo` ohne das `age` \-Argument aufgerufen:  
  
 [!CODE [VbVbcnProcedures#43](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#43)]  
  
## Übergeben von Argumenten durch Namen  
 Die `studentInfo` \-Prozedur kann auch, wie im folgenden Beispiel gezeigt, mit durch Namen übergebenen, durch Kommas getrennten Argumenten aufgerufen werden:  
  
 [!CODE [VbVbcnProcedures#44](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#44)]  
  
## Mischen von Argumenten durch Position und durch Namen  
 In ein und demselben Prozeduraufruf können Sie Argumente sowohl durch Position als auch durch Namen angeben, wie im folgenden Beispiel gezeigt:  
  
 [!CODE [VbVbcnProcedures#45](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#45)]  
  
 Im vorhergehenden Beispiel muss der Platz des ausgelassenen `age` \-Arguments nicht durch ein zusätzliches Komma freigehalten werden, da `birth` durch Namen übergeben wird.  
  
 Wenn Sie Argumente durch Position und durch Namen angeben, müssen alle positionellen Argumente zuerst aufgeführt werden.  Sobald Sie ein Argument durch Namen angeben, müssen auch alle darauf folgenden Argumente durch Namen übergeben werden.  
  
## Angeben optionaler Argumente durch Namen  
 Argumente durch Namen zu übergeben ist vor allem dann sinnvoll, wenn eine Prozedur mit mehr als einem optionalen Argument aufgerufen wird.  Bei der Angabe von Argumenten durch Namen müssen fehlende positionelle Argumente nicht durch aufeinander folgende Kommas gekennzeichnet werden.  Außerdem erleichtert die Argumentübergabe durch Namen den Überblick über die übergebenen und die weggelassenen Argumente.  
  
## Beschränkungen bei der Bereitstellung von Argumenten durch Namen  
 Auch bei der Argumentübergabe durch Namen müssen erforderliche Argumente eingegeben werden.  Weggelassen werden dürfen nur optionale Argumente.  
  
 Parameterarrays können nicht durch Namen übergeben werden,  da für Parameterarrays beim Aufrufen der Prozedur eine unbestimmte Anzahl von durch Trennzeichen getrennten Argumenten bereitgestellt wird und der Compiler einem Namen immer nur ein Argument zuordnen kann.  
  
## Siehe auch  
 [Procedures](../../../../visual-basic/programming-guide/language-features/procedures/index.md)   
 [Procedure Parameters and Arguments](../../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)   
 [How to: Pass Arguments to a Procedure](../../../../visual-basic/programming-guide/language-features/procedures/how-to-pass-arguments-to-a-procedure.md)   
 [Passing Arguments by Value and by Reference](../../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)   
 [Optional Parameters](../../../../visual-basic/programming-guide/language-features/procedures/optional-parameters.md)   
 [Parameter Arrays](../../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md)   
 [Optional](../../../../visual-basic/language-reference/modifiers/optional.md)   
 [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md)
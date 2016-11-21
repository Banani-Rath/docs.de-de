---
title: "Playing Sounds (Visual Basic) | Microsoft Docs"
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
  - "system sounds, playing"
  - "system sounds"
  - "playing sounds, Visual Basic"
  - "sound loops"
  - "My.Computer.Audio object, tasks"
  - "sounds, playing"
  - "sounds, background"
  - "playing sounds"
ms.assetid: f0d9e4ab-57c7-47b6-86d3-99ff07078040
caps.latest.revision: 21
caps.handback.revision: 21
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Playing Sounds (Visual Basic)
Das `My.Computer.Audio`\-Objekt stellt Methoden für die Wiedergabe von Sounds bereit.  
  
## Sounds wiedergeben  
 Während der Soundwiedergabe im Hintergrund kann die Anwendung anderen Code ausführen.  Die `My.Computer.Audio.Play`\-Methode erlaubt jeweils nur die Wiedergabe eines einzelnen Hintergrundsounds. Bei Wiedergabe eines neuen Hintergrundsounds wird der vorherige Hintergrundsound beendet.  Sie können auch einen Sound wiedergeben und warten, bis er beendet wird.  
  
 Im folgenden Beispiel gibt die `My.Computer.Audio.Play`\-Methode einen Sound abgespielt.  Wenn `AudioPlayMode.WaitToComplete` angegeben ist, wartet `My.Computer.Audio.Play`, bis der Sound beendet wird, bevor der aufrufende Code weiter ausgeführt wird.  Wenn Sie dieses Beispiel verwenden möchten, sollten Sie sicherstellen, dass der Dateiname auf eine WAV\-Audiodatei auf dem Computer befindet  
  
 [!CODE [VbVbalrMyComputer#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#15)]  
  
 Im folgenden Beispiel gibt die `My.Computer.Audio.Play`\-Methode einen Sound abgespielt.  Wenn Sie dieses Beispiel verwenden möchten, sollten Sie sicherstellen, dass die Anwendungsressourcen eine WAV\-Audiodatei enthalten, das Waterfall benannt ist.  
  
 [!CODE [VbVbalrMyComputer#16](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#16)]  
  
## Schleifungssounds wiedergeben  
 Im folgenden Beispiel gibt die `My.Computer.Audio.Play`\-Methode den angegebenen Sound im Hintergrund wieder, wenn `PlayMode.BackgroundLoop` angegeben wird.  Wenn Sie dieses Beispiel verwenden möchten, sollten Sie sicherstellen, dass der Dateiname eine WAV\-Audiodatei angibt, der auf Ihrem Computer befindet.  
  
 [!CODE [VbVbalrMyComputer#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#11)]  
  
 Im folgenden Beispiel gibt die `My.Computer.Audio.Play`\-Methode den angegebenen Sound im Hintergrund wieder, wenn `PlayMode.BackgroundLoop` angegeben wird.  Wenn Sie dieses Beispiel verwenden möchten, sollten Sie sicherstellen, dass die Anwendungsressourcen eine WAV\-Audiodatei enthalten, das Waterfall benannt ist.  
  
 [!CODE [VbVbalrMyComputer#12](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#12)]  
  
 Das vorangehende Codebeispiel ist auch als IntelliSense\-Codeausschnitt verfügbar.  Sie finden das Element in der Codeausschnittauswahl unter **Windows Forms Applications \> Sound**.  Weitere Informationen finden Sie unter [Codeausschnitte](/visual-studio/ide/code-snippets).  
  
 Wenn eine Anwendung eine Soundschleife wiedergibt, sollte diese im Allgemeinen irgendwann angehalten werden.  
  
## Das Beenden der Wiedergabe von Sounds im Hintergrund  
 Verwenden Sie die `My.Computer.Audio.Stop`\-Methode, um die gegenwärtig von der Anwendung im Hintergrund wiedergegebene Soundschleife zu beenden.  
  
 Wenn eine Anwendung eine Soundschleife wiedergibt, sollte diese im Allgemeinen irgendwann angehalten werden.  
  
 Im folgenden Beispiel wird beendet, der einen Sound im Hintergrund wiedergibt.  
  
 [!CODE [VbVbalrMyComputer#18](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#18)]  
  
 Das vorangehende Codebeispiel ist auch als IntelliSense\-Codeausschnitt verfügbar.  Sie finden das Element in der Codeausschnittauswahl unter **Windows Forms Applications \> Sound**.  Weitere Informationen finden Sie unter [Codeausschnitte](/visual-studio/ide/code-snippets).  
  
## Systemsounds wiedergeben  
 Verwenden Sie die `My.Computer.Audio.PlaySystemSound`\-Methode, um den angegebenen Systemsound wiederzugeben.  
  
 Die `My.Computer.Audio.PlaySystemSound`\-Methode akzeptiert als Parameter einen der freigegebenen Member der <xref:System.Media.SystemSound>\-Klasse.  Der Systemsound <xref:System.Media.SystemSounds.Asterisk%2A> weist i. d. R. auf Fehler hin.  
  
 Im folgenden Beispiel wird die `My.Computer.Audio.PlaySystemSound`\-Methode, um einen Systemsound wiederzugeben.  
  
 [!CODE [VbVbalrMyComputer#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyComputer#17)]  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.Devices.Audio>   
 <xref:Microsoft.VisualBasic.Devices.Audio.Play%2A>   
 <xref:Microsoft.VisualBasic.Devices.Audio.PlaySystemSound%2A>   
 <xref:Microsoft.VisualBasic.Devices.Audio.Stop%2A>   
 <xref:Microsoft.VisualBasic.AudioPlayMode>
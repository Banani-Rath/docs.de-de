---
title: "Der Verbindungstimeout-Wert muss gr&#246;&#223;er als 0 sein. | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbrNetwork_BadConnectionTimeout"
ms.assetid: 15ac09a7-47f0-44f3-9e84-5bd10bd07450
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Der Verbindungstimeout-Wert muss gr&#246;&#223;er als 0 sein.
Wenn Dateien mit dem [My.Computer.Network Object](../../visual-basic/language-reference/objects/my-computer-network-object.md) hochgeladen und heruntergeladen werden, müssen Sie einen `connectionTimeout`\-Wert angeben, der größer ist als `0`.  
  
### So beheben Sie diesen Fehler  
  
-   Geben Sie einen `connectionTimeout`\-Wert an, der größer ist als `0`.  
  
## Siehe auch  
 [My.Computer.Network.UploadFile\-Methode](http://msdn.microsoft.com/de-de/5505ea3e-3dbd-460b-9f8f-62c84c0a4de6)   
 [My.Computer.Network.DownloadFile\-Methode](http://msdn.microsoft.com/de-de/aeb7ed8f-1ac9-4242-ae57-9f35914eb329)   
 [How to: Upload a File](../../visual-basic/developing-apps/programming/computer-resources/how-to-upload-a-file.md)   
 [How to: Download a File](../../visual-basic/developing-apps/programming/computer-resources/how-to-download-a-file.md)   
 [Netzwerkoperationen in .NET Framework mit Visual Basic](http://msdn.microsoft.com/de-de/c5379021-44ef-4d6a-acf5-e951fdcab6b2)
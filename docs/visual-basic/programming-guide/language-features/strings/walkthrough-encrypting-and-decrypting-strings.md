---
title: "Walkthrough: Encrypting and Decrypting Strings in Visual Basic | Microsoft Docs"
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
  - "encryption, strings"
  - "strings [Visual Basic], encrypting"
  - "decryption, strings"
  - "strings [Visual Basic], decrypting"
ms.assetid: 1f51e40a-2f88-43e2-a83e-28a0b5c0d6fd
caps.latest.revision: 18
caps.handback.revision: 18
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Walkthrough: Encrypting and Decrypting Strings in Visual Basic
In dieser exemplarischen Vorgehensweise wird gezeigt, wie die <xref:System.Security.Cryptography.DESCryptoServiceProvider>\-Klasse zum Verschlüsseln und Entschlüsseln von Zeichenfolgen mithilfe der CSP \(Cryptographic Service Provider\)\-Version des <xref:System.Security.Cryptography.TripleDES> \(Triple Data Encryption Standard\)\-Algorithmus verwendet wird.  Der erste Schritt besteht im Erstellen einer einfachen Wrapperklasse, die den 3DES\-Algorithmus kapselt und die gespeicherten Daten als Base\-64\-codierte Zeichenfolge speichert.  Anschließend wird dieser Wrapper verwendet, um private Benutzerdaten in einer Textdatei mit öffentlichem Zugriff sicher zu speichern.  
  
 Mithilfe von Verschlüsselung können Sie vertrauliche Benutzerdaten \(z. B. Kennwörter\) schützen und Anmeldeinformationen für unbefugte Benutzer unlesbar machen.  Dies kann den Diebstahl der Identität eines berechtigten Benutzers verhindern, sodass die Daten des Benutzers geschützt werden und Nichtleugnung ermöglicht wird.  Mit Verschlüsselung können auch die Daten eines Benutzers vor dem Zugriff durch unbefugte Benutzer geschützt werden.  
  
 Weitere Informationen finden Sie unter [Kryptografische Dienste](../Topic/Cryptographic%20Services.md).  
  
> [!IMPORTANT]
>  Der Rijndael\-Algorithums \(jetzt als AES, Advanced Encryption Standard, bezeichnet\) und der 3DES \(Triple Data Encryption Standard\)\-Algorithmus bieten mehr Sicherheit als DES, da sie rechenintensiver sind.  Weitere Informationen finden Sie unter <xref:System.Security.Cryptography.DES> und <xref:System.Security.Cryptography.Rijndael>.  
  
### So erstellen Sie den Verschlüsselungswrapper  
  
1.  Erstellen Sie die `Simple3Des`\-Klasse, um die Verschlüsselungs\- und Entschlüsselungsmethode zu kapseln.  
  
     [!CODE [VbVbalrStrings#38](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#38)]  
  
2.  Fügen Sie einen Import des Kryptografienamespaces am Anfang der Datei hinzu, die die `Simple3Des`\-Klasse enthält.  
  
     [!CODE [VbVbalrStrings#77](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#77)]  
  
3.  In der `Simple3Des`\-Klasse fügen Sie ein privates Feld hinzu, um den 3DES\-Kryptografiedienstanbieter zu speichern.  
  
     [!CODE [VbVbalrStrings#39](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#39)]  
  
4.  Fügen Sie eine private Methode hinzu, die aus dem Hash des angegebenen Schlüssels ein Bytearray mit einer bestimmten Länge erstellt.  
  
     [!CODE [VbVbalrStrings#41](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#41)]  
  
5.  Fügen Sie einen Konstruktor hinzu, um den 3DES\-Kryptografiedienstanbieter zu initialisieren.  
  
     Der `key`\-Parameter steuert `EncryptData`\-Methode und die `DecryptData`\-Methode.  
  
     [!CODE [VbVbalrStrings#40](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#40)]  
  
6.  Fügen Sie eine öffentliche Methode hinzu, die eine Zeichenfolge verschlüsselt.  
  
     [!CODE [VbVbalrStrings#42](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#42)]  
  
7.  Fügen Sie eine öffentliche Methode hinzu, die eine Zeichenfolge entschlüsselt.  
  
     [!CODE [VbVbalrStrings#43](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#43)]  
  
     Die Wrapperklasse kann jetzt zum Schützen von Benutzerdaten verwendet werden.  In diesem Beispiel wird sie verwendet, um private Benutzerdaten in einer Textdatei mit öffentlichem Zugriff sicher zu speichern.  
  
### So testen Sie den Verschlüsselungswrapper  
  
1.  Fügen Sie in einer eigenen Klasse eine Methode hinzu, die die `EncryptData`\-Methode des Wrappers zum Verschlüsseln einer Zeichenfolge und zum Schreiben der Zeichenfolge in den Ordner Eigene Dateien des Benutzers verwendet.  
  
     [!CODE [VbVbalrStrings#78](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#78)]  
  
2.  Fügen Sie eine Methode hinzu, die die verschlüsselte Zeichenfolge aus dem Ordner Eigene Dokumente des Benutzers liest und sie mit der `DecryptData`\-Methode des Wrappers entschlüsselt.  
  
     [!CODE [VbVbalrStrings#79](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#79)]  
  
3.  Fügen Sie Benutzeroberflächencode hinzu, um die `TestEncoding`\-Methode und die `TestDecoding`\-Methode aufzurufen.  
  
4.  Führen Sie die Anwendung aus.  
  
     Beachten Sie beim Testen der Anwendung, dass die Daten nicht entschlüsselt werden, wenn Sie das falsche Kennwort angeben.  
  
## Siehe auch  
 <xref:System.Security.Cryptography>   
 <xref:System.Security.Cryptography.DESCryptoServiceProvider>   
 <xref:System.Security.Cryptography.DES>   
 <xref:System.Security.Cryptography.TripleDES>   
 <xref:System.Security.Cryptography.Rijndael>   
 [Kryptografische Dienste](../Topic/Cryptographic%20Services.md)
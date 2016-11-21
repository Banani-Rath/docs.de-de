---
title: "Gewusst wie: Implementieren einer einfachen Klasse mit automatisch implementierten Eigenschaften (C#-Programmierhandbuch) | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "Automatisch implementierte Eigenschaften [C#]"
  - "Eigenschaften [C#], Automatisch implementiert"
ms.assetid: 1dc5a8ad-a4f7-4f32-8506-3fc6d8c8bfed
caps.latest.revision: 11
caps.handback.revision: 11
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# Gewusst wie: Implementieren einer einfachen Klasse mit automatisch implementierten Eigenschaften (C#-Programmierhandbuch)
In diesem Beispiel wird das Erstellen einer unveränderlichen einfachen Klasse gezeigt, die nur zum Kapseln einer Reihe von automatisch implementierten Eigenschaften dient.  Verwenden Sie diese Konstruktart anstelle einer Struktur, wenn Sie eine Verweistypsemantik verwenden müssen.  
  
 Für das Erstellen einer unveränderlichen Eigenschaft gibt es zwei Möglichkeiten.  Sie können deklarieren, dass der [set](../../../csharp/language-reference/keywords/set.md)\-Accessor [privat](../../../csharp/language-reference/keywords/private.md) ist.  Die Eigenschaft kann nur im Typ festgelegt werden. Kunden können sie jedoch nicht verändern.  Sie können stattdessen einfach den [get](../../../csharp/language-reference/keywords/get.md)\-Accessor deklarieren. Dieser macht die Eigenschaft mit Ausnahme im Konstruktor des Typs überall unveränderlich.  
  
 Beim Deklarieren eines privaten `set`\-Accessors können Sie einen Objektinitialisierer nicht verwenden, um die Eigenschaft zu initialisieren.  Sie müssen eine Konstruktor oder eine Factorymethode verwenden.  
  
## Beispiel  
 Im folgenden Beispiel werden zwei Möglichkeiten für die Implementierung einer unveränderlichen Klasse gezeigt, die über automatisch implementierte Eigenschaften verfügt.  Mit beiden Möglichkeiten wird jeweils eine der Eigenschaften mit einer privaten `set` und eine der Eigenschaft mit einer `get` deklariert.  Die erste Klasse verwendet einen Konstruktor nur zum Initialisieren der Eigenschaften, und die zweite Klasse verwendet eine statische Factorymethode, die einen Konstruktor aufruft.  
  
```c#  
// This class is immutable. After an object is created,   
    // it cannot be modified from outside the class. It uses a   
    // constructor to initialize its properties.   
    class Contact  
    {  
        // Read-only properties.   
        public string Name { get; }  
        public string Address { get; private set; }  
  
        // Public constructor.   
        public Contact(string contactName, string contactAddress)  
        {  
            Name = contactName;  
            Address = contactAddress;                 
        }  
    }  
  
    // This class is immutable. After an object is created,   
    // it cannot be modified from outside the class. It uses a   
    // static method and private constructor to initialize its properties.      
    public class Contact2  
    {  
        // Read-only properties.   
        public string Name { get; private set; }  
        public string Address { get; }  
  
        // Private constructor.   
        private Contact2(string contactName, string contactAddress)  
        {  
            Name = contactName;  
            Address = contactAddress;                 
        }  
  
        // Public factory method.   
        public static Contact2 CreateContact(string name, string address)  
        {  
            return new Contact2(name, address);  
        }  
    }  
  
    public class Program  
    {   
        static void Main()  
        {  
            // Some simple data sources.   
            string[] names = {"Terry Adams","Fadi Fakhouri", "Hanying Feng",   
                              "Cesar Garcia", "Debra Garcia"};  
            string[] addresses = {"123 Main St.", "345 Cypress Ave.", "678 1st Ave",  
                                  "12 108th St.", "89 E. 42nd St."};  
  
            // Simple query to demonstrate object creation in select clause.   
            // Create Contact objects by using a constructor.   
            var query1 = from i in Enumerable.Range(0, 5)  
                        select new Contact(names[i], addresses[i]);  
  
            // List elements cannot be modified by client code.   
            var list = query1.ToList();  
            foreach (var contact in list)  
            {  
                Console.WriteLine("{0}, {1}", contact.Name, contact.Address);  
            }  
  
            // Create Contact2 objects by using a static factory method.   
            var query2 = from i in Enumerable.Range(0, 5)  
                         select Contact2.CreateContact(names[i], addresses[i]);  
  
            // Console output is identical to query1.   
            var list2 = query2.ToList();  
  
            // List elements cannot be modified by client code.   
            // CS0272:   
            // list2[0].Name = "Eugene Zabokritski";   
  
            // Keep the console open in debug mode.  
            Console.WriteLine("Press any key to exit.");  
            Console.ReadKey();                  
        }  
    }  
  
/* Output:  
    Terry Adams, 123 Main St.  
    Fadi Fakhouri, 345 Cypress Ave.  
    Hanying Feng, 678 1st Ave  
    Cesar Garcia, 12 108th St.  
    Debra Garcia, 89 E. 42nd St.  
*/  
  
```  
  
 Der Compiler erstellt Unterstützungsfelder für jede automatisch implementierte Eigenschaft.  Es ist nicht möglich, über den Quellcode direkt auf die Felder zuzugreifen.  
  
## Siehe auch  
 [Eigenschaften](../../../csharp/programming-guide/classes-and-structs/properties.md)   
 [struct](../../../csharp/language-reference/keywords/struct.md)   
 [Objekt\- und Auflistungsinitialisierer](../../../csharp/programming-guide/classes-and-structs/object-and-collection-initializers.md)
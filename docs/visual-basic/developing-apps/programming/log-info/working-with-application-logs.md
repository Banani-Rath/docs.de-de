---
title: "Arbeiten mit Anwendungsprotokollen in Visual Basic | Microsoft Docs"
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
  - "Protokolle, Anwendung"
  - "Anwendungsereignisprotokolle, Visual Basic"
  - "Anwendungsereignisprotokolle"
ms.assetid: 2581afd1-5791-4bc4-86b2-46244e9fe468
caps.latest.revision: 21
caps.handback.revision: 21
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# Arbeiten mit Anwendungsprotokollen in Visual Basic
Mithilfe der `My.Applicaton.Log`\- und `My.Log`\-Objekte ist es einfach, Protokollierungs\- und Ablaufverfolgungsinformationen in Protokolle zu schreiben.  
  
## Protokollierung von Meldungen  
 Zuerst wird der Schweregrad der Meldung mithilfe der <xref:System.Diagnostics.TraceSource.Switch%2A>\-Eigenschaft der <xref:Microsoft.VisualBasic.Logging.Log.TraceSource%2A>\-Eigenschaft des Protokolls überprüft. Standardmäßig werden nur Meldungen vom Schweregrad "Information" und höher an die Nachverfolgungslistener übergeben, die in der `TraceListener`\-Auflistung des Protokolls angegeben sind. Anschließend vergleicht jeder Listener den Schweregrad der Meldung mit der Eigenschaft <xref:System.Diagnostics.TraceSource.Switch%2A> des Listeners. Wenn der Schweregrad der Meldung ausreichend hoch ist, schreibt der Listener die Meldung.  
  
 Im folgenden Diagramm ist dargestellt, wie eine in die `WriteEntry`\-Methode geschriebene Meldung an die `WriteLine`\-Methoden der Ablaufverfolgungslistener des Protokolls übergeben wird:  
  
 ![Aufruf von "Log" für "My"](../../../../visual-basic/developing-apps/programming/log-info/media/mylogcall.png "MyLogCall")  
  
 Das Verhalten von Protokoll und Ablaufverfolgungslistener lässt sich durch Ändern der Konfigurationsdatei der Anwendung ändern. Das folgende Diagramm stellt die Entsprechung zwischen den Teilen des Protokolls und der Konfigurationsdatei dar.  
  
 ![Konfiguration von "Log" für "My"](../../../../visual-basic/developing-apps/programming/log-info/media/mylogconfig.png "MyLogConfig")  
  
## Protokollspeicherorte von Meldungen  
 Wenn die Assembly keine Konfigurationsdatei aufweist, schreiben die Objekte `My.Application.Log` und `My.Log` in die Debugausgabe der Anwendung \(mithilfe der <xref:System.Diagnostics.DefaultTraceListener>\-Klasse\). Darüber hinaus schreibt das `My.Application.Log`\-Objekt in die Protokolldatei der Assembly \(mithilfe der <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener>\-Klasse\), während das `My.Log`\-Objekt in die Ausgabe der ASP.NET\-Webseite schreibt \(mithilfe der <xref:System.Web.WebPageTraceListener>\-Klasse\).  
  
 Die Debugausgabe kann beim Ausführen der Anwendung im Debugmodus im Fenster [!INCLUDE[vsprvs](../../../../csharp/includes/vsprvs_md.md)] **Ausgabe** angezeigt werden. Klicken Sie zum Öffnen des Fensters **Ausgabe** auf das Menüelement **Debug**, zeigen Sie auf **Fenster**, und klicken Sie dann auf **Ausgabe**. Wählen Sie im Fenster **Ausgabe**  im Feld **Ausgabe anzeigen von** den Wert **Debug** aus.  
  
 Standardmäßig schreibt `My.Application.Log` die Protokolldatei in den Pfad für die Anwendungsdaten des Benutzers. Diesen Pfad können Sie aus der Eigenschaft <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener.FullLogFileName%2A> des <xref:Microsoft.VisualBasic.Logging.Log.DefaultFileLogWriter%2A>\-Objekts abrufen. Das Format des Pfades ist wie folgt:  
  
 `BasePath`\\`CompanyName`\\`ProductName`\\`ProductVersion`  
  
 Ein typischer Wert für `BasePath` ist etwa dieser:  
  
 C:\\Dokumente und Einstellungen\\`username`\\Anwendungsdaten  
  
 Die Werte von `CompanyName`, `ProductName` und `ProductVersion` stammen aus den Assemblyinformationen der Anwendung. Der Name der Protokolldatei hat die Form "*AssemblyName*.log", wobei *AssemblyName* der Dateiname der Assembly ohne Erweiterung ist. Wenn mehr als eine Protokolldatei erforderlich ist, etwa wenn die ursprüngliche Protokolldatei zu dem Zeitpunkt, da die Anwendung versucht, in es zu schreiben, nicht verfügbar ist, hat der Name der Protokolldatei die Form "*AssemblyName*\-*iteration*.log", wobei `iteration` ein positiver `Integer` ist.  
  
 Sie können das Standardverhalten außer Kraft setzen, indem Sie die Konfigurationsdateien des Computers und der Anwendung hinzufügen oder ändern. Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Ändern des Ortes, in den "My.Application.Log" Informationen schreibt](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-changing-where-my-application-log-writes-information.md).  
  
## Konfigurieren von Protokolleinstellungen  
 Die Standardimplementierung des `Log`\-Objekts funktioniert ohne Anwendungskonfigurationsdatei, "app.config". Um die Standardwerte zu ändern, müssen Sie eine Konfigurationsdatei mit den neuen Einstellungen hinzufügen. Weitere Informationen finden Sie unter [Walkthrough: Filtering My.Application.Log Output](../../../../visual-basic/developing-apps/programming/log-info/walkthrough-filtering-my-application-log-output.md).  
  
 Die Protokollkonfigurationsabschnitte befinden sich im `<system.diagnostics>`\-Knoten im `<configuration>`\-Hauptknoten der app.config\-Datei. Die Protokollinformationen sind in mehreren Knoten definiert:  
  
-   Die Listener für das `Log`\-Objekt sind in dem `<sources>`\-Knoten mit dem Namen "DefaultSource" definiert.  
  
-   Der Schweregradfilter für das `Log`\-Objekt ist in dem `<switches>`\-Knoten mit dem Namen "DefaultSwitch" definiert.  
  
-   Die Protokolllistener sind im `<sharedListeners>`\-Knoten definiert.  
  
 Beispiele für `<sources>`\-, `<switches>`\- und `<sharedListeners>`\-Knoten sind im folgenden Code dargestellt:  
  
```  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="DefaultSource" switchName="DefaultSwitch">  
        <listeners>  
          <add name="FileLog"/>  
        </listeners>  
      </source>  
    </sources>  
    <switches>  
      <add name="DefaultSwitch" value="Information" />  
    </switches>  
    <sharedListeners>  
      <add name="FileLog"  
        type="Microsoft.VisualBasic.Logging.FileLogTraceListener,  
          Microsoft.VisualBasic, Version=8.0.0.0, Culture=neutral,   
          PublicKeyToken=b03f5f7f11d50a3a, processorArchitecture=MSIL"  
        initializeData="FileLogWriter"  
      />  
    </sharedListeners>  
  </system.diagnostics>  
</configuration>  
```  
  
## Ändern der Protokolleinstellungen nach der Bereitstellung  
 Beim Entwickeln einer Anwendung werden deren Konfigurationseinstellungen in der app.config\-Datei gespeichert, wie in den Beispielen oben dargestellt. Nach dem Bereitstellen der Anwendung kann das Protokoll durch Bearbeiten der Konfigurationsdatei weiterhin konfiguriert werden. In einer Windows\-basierten Anwendung ist der Name dieser Datei "*applicationName*.exe.config", und sie muss sich im gleichen Ordner wie die Programmdatei befinden. Für eine Webanwendung ist dies die "Web.config"\-Datei, die dem Projekt zugeordnet ist.  
  
 Wenn die Anwendung den Code, der eine Instanz einer Klasse erstellt, zum ersten Mal ausführt, prüft sie die Konfigurationsdatei auf Informationen zum Objekt. Für das `Log`\-Objekt geschieht das beim ersten Zugriff auf das `Log`\-Objekt. Das System durchsucht die Konfigurationsdatei für jedes Objekt nur ein Mal – wenn die Anwendung das Objekt erstmalig erstellt. Daher müssen Sie ggf. die Anwendung erneut starten, damit die Änderungen wirksam werden.  
  
 In einer bereitgestellten Anwendung aktivieren Sie Ablaufverfolgungscode, indem Sie Schalterobjekte neu konfigurieren, bevor die Anwendung gestartet wird. Üblicherweise umfasst dies das Aktivieren oder Deaktivieren der Schalterobjekte oder Ändern der Ablaufverfolgungsebenen und dann das Neustarten Ihrer Anwendung.  
  
## Sicherheitsüberlegungen  
 Berücksichtigen Sie beim Schreiben von Daten in das Protokoll folgende Punkte:  
  
-   **Vermeiden Sie die Preisgabe von Benutzerinformationen**. Stellen Sie sicher, dass die Anwendung nur genehmigte Informationen in das Protokoll schreibt. Beispielsweise kann es akzeptabel sein, dass ein Anwendungsprotokoll Benutzernamen enthält, in keinem Fall jedoch Benutzerkennwörter.  
  
-   **Achten Sie auf sichere Protokollspeicherorte**. Jedes Protokoll, das möglicherweise vertrauliche Informationen enthält, sollte an einem sicheren Ort gespeichert werden.  
  
-   **Vermeiden Sie irreführende Informationen**. Im Allgemeinen sollte die Anwendung alle von einem Benutzer eingegeben Daten überprüfen, bevor Sie sie verwendet. Dies umfasst auch das Schreiben von Daten in das Anwendungsprotokoll.  
  
-   **Vermeiden Sie Dienstverweigerung**. Wenn die Anwendung zu viele Informationen in das Protokoll schreibt, kann das Protokolls voll werden, oder die Suche nach wichtigen Informationen gestaltet sich schwierig.  
  
## Siehe auch  
 <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=fullName>   
 [Logging Information from the Application](../../../../visual-basic/developing-apps/programming/log-info/logging-information-from-the-application.md)
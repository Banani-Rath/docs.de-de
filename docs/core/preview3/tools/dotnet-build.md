---
title: Dotnet-build-Befehl | .NET Core SDK
description: "Der dotnet-build-Befehl erstellt ein Projekt und alle seine Abhängigkeiten."
keywords: dotnet-build, CLI, CLI-Befehl, .NET Core
author: mairaw
manager: wpickett
ms.date: 10/13/2016
ms.topic: article
ms.prod: .net-core
ms.technology: .net-core-technologies
ms.devlang: dotnet
ms.assetid: 70285a83-4103-4617-be8b-d0e1e9a4a91d
translationtype: Human Translation
ms.sourcegitcommit: 1a84c694945fe0c77468eb77274ab46618bccae6
ms.openlocfilehash: 04c4d77b31bf4a1bdb425d837c490440e7312e57

---

#<a name="dotnet-build"></a>dotnet-build

## <a name="name"></a>Name 
dotnet-build – Erstellt ein Projekt und alle seine Abhängigkeiten 

## <a name="synopsis"></a>Übersicht

`dotnet build [--help] [--output]  [--framework]  
    [--configuration]  [--runtime] [--version-suffix]
    [--build-profile]  [--no-incremental] [--no-dependencies]
    [<project>]`

## <a name="description"></a>Beschreibung

Der Befehl `dotnet build` erstellt aus mehreren Quelldateien eines Quellprojekts und seinen Abhängigkeiten eine Binärdatei. Standardmäßig ist die resultierende Binärdatei in Intermediate Language (IL) und hat eine DLL-Erweiterung. 
`dotnet build` ergibt auch eine `\*.deps`-Datei, die beschreibt, wie der Host die Anwendung auszuführen hat.  

Zum Erstellen muss eine Ressourcendatei vorhanden sein (eine Datei, die alle Abhängigkeiten Ihrer Anwendung auflistet). Das bedeutet, dass Sie [`dotnet restore`](dotnet-restore.md) vor dem Erstellen von Code ausführen müssen.

Vor Beginn jeder Kompilierung analysiert das Verb `build` das Projekt und seine Abhängigkeiten für inkrementelle Sicherheitskontrollen.
Wenn alle Überprüfungen erfolgreich sind, wird das Erstellen mit der inkrementellen Kompilierung des Projekts und seine Abhängigkeiten fortgesetzt. Anderenfalls wird wieder die nicht inkrementelle Kompilierung verwendet. Über ein Profilflag können Benutzer wählen, zusätzliche Informationen zu erhalten, wie sie ihre Buildzeiten verbessern können.

Um eine ausführbare Anwendung statt einer Bibliothek zu erstellen, müssen Sie die `<OutputType>`-Eigenschaft festlegen:

```xml
<PropertyGroup>
    <OutputType>Exe</OutputType>
</PropertyGroup>
```

## <a name="options"></a>Optionen

`-h|--help`

Druckt eine kurze Hilfe für den Befehl.  

`-o|--output <OUTPUT_DIRECTORY>`

Verzeichnis, in dem die erstellten Binärdateien platziert werden. Sie müssen außerdem `--framework` definieren, wenn Sie diese Option angeben.

`-f|--framework <FRAMEWORK>`

Kompilierungen für ein bestimmtes Framework. Das Framework muss in der [Projektdatei](csproj.md) definiert werden.

`-c|--configuration [Debug|Release]`

Definiert eine Konfiguration für die Erstellung.  Wenn kein Wert angegeben ist, wird als Standardwert `Debug` verwendet.

`-r|--runtime [RUNTIME_IDENTIFIER]`

Ziellaufzeit für die Erstellung. Eine Liste der Runtime-IDs (RIDs) finden Sie unter [RID-Katalog](../../rid-catalog.md). 

`--version-suffix [VERSION_SUFFIX]`

Definiert, durch was `*` im Versionsfeld der Projektdatei ersetzt werden soll. Das Format entspricht den NuGet-Versionsrichtlinien. 

`--build-profile`

Druckt die inkrementellen Sicherheitsüberprüfungen, die Benutzer durchführen müssen, damit die inkrementelle Kompilierung automatisch aktiviert wird.

`--no-incremental`

Markiert den Build als unsicher für inkrementelle Builds. Deaktiviert die inkrementelle Kompilierung und erzwingt eine komplette Neuerstellung des Abhängigkeitsdiagramms des Projekts.

`--no-dependencies`

Ignoriert Verweise zwischen Projekten und erstellt nur das zum Erstellen angegebene Stammprojekt.

## <a name="examples"></a>Beispiele

Erstellt ein Projekt und seine Abhängigkeiten:

`dotnet build`

Erstellt ein Projekt und seine Abhängigkeiten mithilfe der Release-Konfiguration:

`dotnet build --configuration Release`

Erstellt ein Projekt und seine Abhängigkeiten für eine bestimmte Laufzeit (in diesem Beispiel Ubuntu 16.04):

`dotnet build --runtime ubuntu.16.04-x64`



<!--HONumber=Nov16_HO3-->



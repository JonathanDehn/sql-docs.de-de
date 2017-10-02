---
title: Aufrufen ProcessASDatabase | Microsoft Docs
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 66d5d154-88ce-4c2e-b1ef-e2d2f6fb1c44
caps.latest.revision: 11
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: f8e83493ed934a3f9bf32a1cef35969f04996223
ms.contentlocale: de-de
ms.lasthandoff: 09/01/2017

---
# <a name="invoke-processasdatabase"></a>Invoke-ProcessASDatabase

[!INCLUDE[ssas-appliesto-sqlas-all-aas](../../includes/ssas-appliesto-sqlas-all-aas.md)]

  Führt den **Process** -Vorgang für eine bestimmte **Database** mit einem bestimmten **ProcessType** oder **RefreshType** durch, je nach dem zugrunde liegenden Metadatentyp.  
  
 Verwenden Sie **ProcessType** für eine Datenbank mit mehrdimensionalen Metadaten (einschließlich tabellarischer Datenbanken mit Kompatibilitätsgrad 1050, 1100 oder 1103).  
  
 Verwenden Sie **RefreshType** für tabellarische Datenbanken mit Kompatibilitätsgrad 1200 oder höher.  

>[!NOTE] 
>In diesem Artikel möglicherweise veraltete Informationen und Beispiele enthalten. Verwenden Sie das Cmdlet "Get-Help", für die aktuelle.
  
## <a name="syntax"></a>Syntax  
 `Invoke-ProcessASDatabase [-DatabaseName] <string> [-RefreshType] <RefreshType> {Full | ClearValues | Calculate |     DataOnly | Automatic | Add | Defragment} [-Server <string>] [-Credential <pscredential>] [-WhatIf] [-Confirm]     [<CommonParameters>]`  
  
 `Invoke-ProcessASDatabase [-DatabaseName] <string> [-ProcessType] <ProcessType> {ProcessFull | ProcessAdd |     ProcessUpdate | ProcessIndexes | ProcessData | ProcessDefault | ProcessClear | ProcessStructure |     ProcessClearStructureOnly | ProcessScriptCache | ProcessRecalc | ProcessDefrag} [-Server <string>] [-Credential     <pscredential>] [-WhatIf] [-Confirm]  [<CommonParameters>]`  
  
## <a name="description"></a>Description  
 Das Cmdlet **Invoke-ProcessASDatabase** verarbeitet eine Datenbank auf der Ebene, die Sie angeben. Wenn Sie **RefreshType** bei tabellarischen Datenbanken mit Kompatibilitätsgrad 1200 beispielsweise auf **Vollständig** festlegen, werden vorhandene Daten durch alle neuen Daten überschrieben.  
  
 Der Verarbeitungstyp (mehrdimensional) oder der Aktualisierungstyp (tabellarisch) ist erforderlich und kann vor oder nach den Datenbank- und Serverparametern angegeben werden:  
  
-   Informationen zum mehrdimensionalen Verarbeitungstyp finden Sie unter [Verarbeiten von Optionen und Einstellungen &#40;Analysis Services&#41;](../../analysis-services/multidimensional-models/processing-options-and-settings-analysis-services.md).  
  
-   Informationen zum tabellarischen Verarbeitungstyp finden Sie unter [Verarbeiten von Datenbank, Tabelle oder Partition &#40;Analysis Services&#41;](../../analysis-services/tabular-models/process-database-table-or-partition-analysis-services.md).  
  
## <a name="parameters"></a>Parameter  
  
### <a name="-databasename-string"></a>DatabaseName - \<Zeichenfolge >  
 Gibt die tabellarische oder mehrdimensionale Datenbank an, die verarbeitet werden soll.  
  
|||  
|-|-|  
|Erforderlich?|true|  
|Position?|0|  
|Standardwert||  
|Pipelineeingabe akzeptieren?|false|  
|Platzhalterzeichen akzeptieren?|false|  
  
### <a name="-servermicrosoftanalysissevicesserver"></a>-Server\<Microsoft.AnalysisSevices.Server >  
 Gibt optional die Serverinstanz an, mit der eine Verbindung hergestellt werden soll, wenn Sie nicht das **SQLAS** -Anbieterverzeichnis für den Kontext verwenden.  
  
|||  
|-|-|  
|Erforderlich?|false|  
|Position?|benannt|  
|Standardwert||  
|Pipelineeingabe akzeptieren?|false|  
|Platzhalterzeichen akzeptieren?|false|  
  
### <a name="-refreshtype-microsoftanalysisservicesrefreshtype"></a>-RefreshType \<Microsoft.AnalysisServices.RefreshType >  
 Gibt den Prozesstyp für eine tabellarische Datenbank an.  Gültige Werte sind „Full“, „ClearValues“, „Calculate“, „DataOnly“, „Automatic“, „Add“ und „Defragment“. Beschreibungen und einen Leitfaden finden Sie unter [Verarbeiten von Datenbank, Tabelle oder Partition &#40;Analysis Services&#41;](../../analysis-services/tabular-models/process-database-table-or-partition-analysis-services.md).  
  
|||  
|-|-|  
|Erforderlich?|true|  
|Position?|1|  
|Standardwert||  
|Pipelineeingabe akzeptieren?|false|  
|Platzhalterzeichen akzeptieren?|false|  
  
### <a name="-processtype-microsoftanalysisservicesprocesstype"></a>Der ProcessType - \<Microsoft.AnalysisServices.ProcessType >  
 Gibt den Prozesstyp für eine mehrdimensionale Datenbank oder eine tabellarische Datenbank mit einem Kompatibilitätsgrad von 1050–1103 an. Gültige Werte sind: ProcessFull, ProcessAdd, ProcessUpdate, ProcessIndexes, ProcessData, ProcessDefault, ProcessClear, ProcessStructure, ProcessClearStructureOnly, ProcessScriptCache oder ProcessRecalc. Beschreibungen und einen Leitfaden finden Sie unter [Verarbeiten von Optionen und Einstellungen &#40;Analysis Services&#41;](../../analysis-services/multidimensional-models/processing-options-and-settings-analysis-services.md).  
  
|||  
|-|-|  
|Erforderlich?|true|  
|Position?|1|  
|Standardwert||  
|Pipelineeingabe akzeptieren?|false|  
|Platzhalterzeichen akzeptieren?|false|  
  
### <a name="-credential"></a>-Credential  
 Wenn dieser Parameter angegeben wird, werden der übergebene Benutzername bzw. das übergebene Kennwort verwendet, um eine Verbindung mit der Analysis Services-Instanz herzustellen. Wenn keine Anmeldeinformationen angegeben sind, wird das Windows-Standardkonto des Benutzers verwendet, der das Skript ausführt.  
  
|||  
|-|-|  
|Erforderlich?|false|  
|Position?|benannt|  
|Standardwert||  
|Pipelineeingabe akzeptieren?|false|  
|Platzhalterzeichen akzeptieren?|false|  
  
## <a name="-whatif"></a>-Whatif  
 Verwenden Sie diesen Parameter, um Informationen über die Auswirkungen des Vorgangs zu erhalten, bevor er ausgeführt wird.  
  
|||  
|-|-|  
|Erforderlich?|false|  
|Position?|benannt|  
|Standardwert||  
|Pipelineeingabe akzeptieren?|false|  
|Platzhalterzeichen akzeptieren?|false|  
  
## <a name="-confirm"></a>-Confirm  
 Verwenden Sie diesen Parameter, um den Vorgang interaktiv mit "Ja" oder "Nein" zu bestätigen, bevor er ausgeführt wird.  
  
|||  
|-|-|  
|Erforderlich?|false|  
|Position?||  
|Standardwert||  
|Pipelineeingabe akzeptieren?||  
|Platzhalterzeichen akzeptieren?|false|  
  
## <a name="example-1-sqlas-provider"></a>Beispiel 1 (SQLAS-Anbieter)  
 In diesem Beispiel wird der **SQLAS** -Anbieter verwendet, um den Kontext für die Liste der Datenbanken auf einer Standardinstanz festzulegen.  Wenn Sie den Inhalt des Verzeichnisses „Datenbanken“ auflisten, werden alle Datenbanken zusammen mit ihrem Verarbeitungsstatus und Lese-/Schreibmodus angezeigt.  
  
 Sie können **Invoke-ProcessASDatabase** über den Datenbankordner ausführen, indem Sie lediglich den Datenbanknamen angeben.  
  
```  
PS > import-module SQLPS -DisableNameChecking  
PS  SQL Server > cd sqlas\ssas-srv-01\default\databases  
PS SQLSERVER:\sqlas\ssas-srv-01\default\databases> dir  
. . . .  
PS SQLSERVER:\sqlas\ssas-srv-01\default\databases> Invoke-ProcessASDatabase "adventureworks"  
  
```  
  
 Je nach Datenbanktyp werden Sie dazu aufgefordert, **RefreshType** oder **ProcessType**anzugeben.  
  
 Nachweis für die Verarbeitung ist das Vorhandensein eines Auswirkungsobjekts in der Rückgabeanweisung: Microsoft.AnalysisServices.Tabular.ObjectImpact.  
  
 Beachten Sie, dass Objektzustandsinformationen manchmal zwischengespeichert werden. Wenn Sie daher nach dem erfolgreichen Abschluss der Verarbeitung den Inhalt eines Verzeichnisses auflisten, behält der Datenbankzustand den ursprünglichen Deskriptor „nicht verarbeitet“ bei. Dies ist irreführend, denn sofern die Objektauswirkung zurückgegeben wurde, wurde die Datenbank eigentlich verarbeitet.  
  
 Sie können überprüfen, ob die Verarbeitung erfolgreich war, indem Sie auf der Eigenschaftenseite der Datenbank in Management Studio eine neue Sitzung starten oder indem Sie den Verarbeitungsstatus von einem Datenbankobjekt zurückgeben (über [Microsoft.AnalysisServices.ProcessableMajorObject.LastProcessed](https://msdn.microsoft.com/library/microsoft.analysisservices.processablemajorobject.lastprocessed.aspx)).  
  
## <a name="example-2"></a>Beispiel 2  
 Dieses Beispiel zeigt den gleichen Vorgang nur mit Cmdlet, ohne Anbieter. Zusätzliche Parameter sind erforderlich, um den Server und den Prozesstyp anzugeben.  
  
```  
PS > import-module SQLPS -DisableNameChecking  
PS  SQL Server >  Invoke-ProcessASDatabase -databasename "AdventureWorks" -server '\\server-name\instancename' –ProcessType "ProcessFull"  
  
```  
  
  
  
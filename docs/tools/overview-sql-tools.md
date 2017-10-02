---
title: "SQL-Tools und Hilfsprogramme für SQLServer, Azure SQL-Datenbank und SQL Datawarehouse | Microsoft Docs"
ms.custom: 
ms.date: 08/25/2017
ms.prod: sql-server-2017
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 
caps.latest.revision: 0
author: stevestein
ms.author: sstein
manager: craigg
ms.translationtype: MT
ms.sourcegitcommit: 21f0cfd102a6fcc44dfc9151750f1b3c936aa053
ms.openlocfilehash: eccbe54c561e009858f6192126abc57e3399082c
ms.contentlocale: de-de
ms.lasthandoff: 08/28/2017

---
# <a name="tools-and-utilities-for-azure-sql-database-sql-server-and-sql-data-warehouse"></a>Tools und Hilfsprogramme für Azure SQL-Datenbank, SQL Server und SQL Data Warehouse

[!INCLUDE[tsql-appliesto-ss2008-all_md](../includes/tsql-appliesto-ss2008-all-md.md)]  

![](../includes/media/sql-database-tools.png)Dieser Artikel enthält eine Liste der verfügbaren Tools zum Arbeiten mit SQL Server, Azure SQL-Datenbank, SQL Data Warehouse und SQL Server-basierten Anwendungen. 

Wenn Sie direkt im und Erstellen von Tabellen, Start springen Ausführen von Abfragen, im Grunde entwerfen und verwalten Sie die Datenbank aus, klicken Sie dann [ **SQL Server Management Studio (SSMS)** ](../ssms/download-sql-server-management-studio-ssms.md) ist sehr wahrscheinlich die Werkzeug. SSMS ist kostenlos und unter Windows ausgeführt wird.

Wenn Sie Linux oder MacOS ausführen, versuchen Sie es [Visual Studio Code](https://code.visualstudio.com/) mit der [ **Mssql für Visual Studio Code** ](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql) Erweiterung. Diese Tools sind für die Entwicklung von Microsoft SQL Server, Azure SQL-Datenbank und SQL Data Warehouse mit einem umfangreichen Satz an Funktionen und sind auch frei. Finden Sie unter [verwenden Visual Studio-Code zum Erstellen und Ausführen von Transact-SQL-Skripts für SQL Server](../linux/sql-server-linux-develop-use-vscode.md).


## <a name="sql-tools"></a>SQL-tools 
 
| Tool | Description |
|:--|:--|
| [SQL Server Management Studio (SSMS)](../ssms/download-sql-server-management-studio-ssms.md) | Verwenden Sie SQL Server Management Studio (SSMS), um Abfragen, Entwerfen und Verwalten Ihrer SQL Server, Azure SQL-Datenbank und Azure SQL Data Warehouse. |
| [SQL Server Data Tools (SSDT)](../ssdt/download-sql-server-data-tools-ssdt.md) | Umwandeln von Visual Studio in einer leistungsstarken Entwicklungsumgebung für SQL Server, Azure SQL-Datenbank und Azure SQL Data Warehouse. |
| [Visual Studio-Code](https://code.visualstudio.com/)| Visual Studio-Code funktioniert unter Linux, Mac OS und Windows. Installieren Sie nach der Installation von Visual Studio-Code, der [Mssql-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql) zum Entwickeln von Microsoft SQL Server, Azure SQL-Datenbank und SQL Data Warehouse. |
| [Configuration Manager](../tools/configuration-manager/sql-server-configuration-manager-help.md) | Verwenden Sie SQL Server Configuration Manager, zum Konfigurieren von SQL Server-Dienste und Netzwerkkonnektivität.|
| [SQL Server Migration Assistant](../ssma/sql-server-migration-assistant.md) | Verwenden Sie SQL Server Migration Assistant zur Automatisierung der Datenbankmigration zu SQL Server aus Microsoft Access, DB2, MySQL, Oracle und Sybase.|
| [Distributed Replay](../tools/distributed-replay/install-distributed-replay-overview.md) | Verwenden Sie die Distributed Replay-Funktion können Sie das Bewerten der Auswirkungen zukünftiger Upgrades von SQL Server. Verwenden des Distributed Replay auch Bewerten der Auswirkungen von Hardware- und Betriebssystemupgrades sowie SQL Server-Computer optimieren. |
| [ssbdiagnose](../tools/ssbdiagnose/ssbdiagnose-utility-service-broker.md) | Die Ssbdiagnose (Hilfsprogramm) meldet Probleme in Service Broker-Konversationen oder die Konfiguration von Service Broker-Dienste. |


## <a name="sql-command-prompt-utilities"></a>SQL-Eingabeaufforderungs-Hilfsprogramme

  Eingabeaufforderungs-Hilfsprogramme versetzen Sie in die Lage, [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] -Vorgänge einem Skript hinzuzufügen. Die folgende Tabelle enthält eine Liste der Eingabeaufforderung-Hilfsprogramme, die im Lieferumfang von [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)]enthalten sind.  
  
|**Hilfsprogramm**|**Beschreibung**|**Installiert in**|  
|-----------------|---------------------|----------------------|  
|[bcp (Hilfsprogramm)](../tools/bcp-utility.md)|Wird verwendet, um Daten in einem benutzerdefinierten Format zwischen einer [!INCLUDE[msCoName](../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] -Instanz und einer Datendatei zu kopieren.|\<*Laufwerk*: > \Programme Dateien\\[!INCLUDE[msCoName](../includes/msconame-md.md)][!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)]\Client SDK\ODBC\110\Tools\Binn|  
|[dta (Hilfsprogramm)](../tools/dta/dta-utility.md)|Wird verwendet, um eine Arbeitsauslastung zu analysieren und Empfehlungen zu physischen Entwurfsstrukturen auszugeben, um die Serverleistung für diese Arbeitsauslastung zu optimieren.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[dtexec (Hilfsprogramm)](../integration-services/packages/dtexec-utility.md)|Wird verwendet, um ein [!INCLUDE[ssISnoversion](../includes/ssisnoversion-md.md)] -Paket zu konfigurieren und auszuführen. Unter dem Namen **DTExecUI**steht eine Version dieses Hilfsprogramms mit Benutzeroberfläche zur Verfügung, über die das Paketausführungsprogramm aufgerufen wird.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]DTS\Binn|  
|[dtutil (Hilfsprogramm)](../integration-services/dtutil-utility.md)|Wird für die Verwaltung von SSIS-Paketen verwendet.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]DTS\Binn|  
|[Bereitstellen von Modelllösungen mit dem Bereitstellungshilfsprogramm](../analysis-services/multidimensional-models/deploy-model-solutions-with-the-deployment-utility.md)|Wird verwendet, um [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)] -Projekte für [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)]-Instanzen bereitzustellen.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn\VShell\Common7\IDE|  
|[MSSQL-Skripter (öffentliche Vorschau)](https://blogs.technet.microsoft.com/dataplatforminsider/2017/05/17/try-new-sql-server-command-line-tools-to-generate-t-sql-scripts-and-monitor-dynamic-management-views/)|Zum Generieren von CREATE "und" Einfügen von T-SQL-Skripts für Datenbankobjekte in SQL Server, Azure SQL-Datenbank und Azure SQL Data Warehouse verwendet.|Finden Sie in unserem [GitHub-Repository](https://github.com/Microsoft/sql-xplat-cli) für Download und Nutzungsinformationen.| 
|[Osql (Hilfsprogramm)](../tools/osql-utility.md)|Ermöglicht es Ihnen, [!INCLUDE[tsql](../includes/tsql-md.md)] -Anweisungen, Systemprozeduren und Skriptdateien an der Eingabeaufforderung einzugeben.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[Profiler-Hilfsprogramm](../tools/profiler-utility.md)|Wird verwendet, um [!INCLUDE[ssSqlProfiler](../includes/sssqlprofiler-md.md)] von der Eingabeaufforderung zu starten.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[Hilfsprogramm RS.exe &#40;SSRS&#41;](../reporting-services/tools/rs-exe-utility-ssrs.md)|Wird verwendet, um Skripts für die Verwaltung von [!INCLUDE[ssRSnoversion](../includes/ssrsnoversion-md.md)] -Berichtsservern auszuführen.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[rsconfig-Hilfsprogramm &#40;SSRS&#41;](../reporting-services/tools/rsconfig-utility-ssrs.md)|Wird zum Konfigurieren einer Berichtsserververbindung verwendet.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[rskeymgmt-Hilfsprogramm &#40;SSRS&#41;](../reporting-services/tools/rskeymgmt-utility-ssrs.md)|Wird für die Verwaltung von Verschlüsselungsschlüsseln auf einem Berichtsserver verwendet.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[sqlagent90 (Anwendung)](../tools/sqlagent90-application.md)|Wird verwendet, um den [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] -Agent von der Eingabeaufforderung zu starten.|\<Laufwerk >: \Programme\Microsoft SQL Server\\<*Instance_name*> \MSSQL\Binn|  
|[sqlcmd (Hilfsprogramm)](../tools/sqlcmd-utility.md)|Ermöglicht es Ihnen, [!INCLUDE[tsql](../includes/tsql-md.md)] -Anweisungen, Systemprozeduren und Skriptdateien an der Eingabeaufforderung einzugeben.|\<*Laufwerk*: > \Programme Dateien\\[!INCLUDE[msCoName](../includes/msconame-md.md)][!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)]\Client SDK\ODBC\110\Tools\Binn|  
|[SQLdiag (Hilfsprogramm)](../tools/sqldiag-utility.md)|Wird zum Sammeln von Diagnoseinformationen für den [!INCLUDE[msCoName](../includes/msconame-md.md)] -Kundenservice und -support verwendet.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[Anwendung sqllogship](../tools/sqllogship-application.md)|Wird von Anwendungen zum Ausführen von Sicherungs-, Kopier- und Wiederherstellungsvorgängen und zugeordneten Cleanups für eine Protokollversandkonfiguration verwendet, ohne Sicherungs-, Kopier- und Wiederherstellungsaufträge auszuführen.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[SqlLocalDB-Hilfsprogramm](../tools/sqllocaldb-utility.md)|Ein Ausführungsmodus von [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] , der speziell für Programmentwickler konzipiert wurde.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[sqlmaint (Hilfsprogramm)](../tools/sqlmaint-utility.md)|Wird verwendet, um Datenbank-Wartungspläne auszuführen, die in früheren Versionen von [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)]erstellt wurden.|\<Laufwerk >: \Programme\Microsoft SQL Server\MSSQL13. MSSQLSERVER\MSSQL\Binn|  
|[sqlps (Hilfsprogramm)](../tools/sqlps-utility.md)|Wird zum Ausführen von PowerShell-Befehlen und -Skripts verwendet. Lädt und registriert den [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] PowerShell-Anbieter sowie cmdlets.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn|  
|[sqlservr](../tools/sqlservr-application.md)|Wird verwendet, um eine Instanz von [!INCLUDE[ssDE](../includes/ssde-md.md)] zur Problembehandlung von der Eingabeaufforderung aus zu starten und zu beenden.|\<Laufwerk >: \Programme\Microsoft SQL Server\MSSQL13. MSSQLSERVER\MSSQL\Binn|  
|[Ssms-Hilfsprogramm](../tools/sql-server-management-studio/ssms-utility.md)|Wird verwendet, um [!INCLUDE[ssManStudioFull](../includes/ssmanstudiofull-md.md)] von der Eingabeaufforderung zu starten.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]Tools\Binn\VSShell\Common7\IDE|  
|[tablediff (Hilfsprogramm)](../tools/tablediff-utility.md)|Wird verwendet, um Daten in zwei Tabellen im Hinblick auf Nichtkonvergenz zu vergleichen, was im Rahmen der Problembehandlung in einer Replikationstopologie hilfreich sein kann.|[!INCLUDE[ssInstallPathVar](../includes/ssinstallpathvar-md.md)]COM|  

## <a name="sql-command-prompt-utilities-syntax-conventions"></a>SQL-Eingabeaufforderungs-Hilfsprogramme geltende Syntaxkonventionen  
  
|**Konvention**|**Syntaxelemente**|  
|--------------------|------------------|  
|GROSSBUCHSTABEN|Anweisungen und Ausdrücke, die auf Betriebssystemebene verwendet werden.|  
|`monospace`|Beispielbefehle und Programmcode.|  
|*Kursiv*|Vom Benutzer angegebene Parameter.|  
|**Fett**|Befehle, Parameter und sonstige Syntaxelemente, die genau wie angezeigt eingegeben werden müssen.|  



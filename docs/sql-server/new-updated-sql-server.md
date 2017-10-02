---
title: "Aktualisiert – Dokumentation zu SQL Server | Microsoft-Dokumentation"
description: "Codeausschnitte anzeigen aktualisierter Inhalt in zuletzt geänderten Dokumentation für SQL Server."
services: na
documentationcenter: 
author: MightyPen
manager: jhubbard
editor: BYHAM
ms.service: na
ms.topic: updart-autogen
ms.technology: database-engine
ms.custom: UpdArt.exe
ms.workload: sql-server
ms.tgt_pltfrm: na
ms.devlang: na
ms.date: 09/11/2017
ms.author: genemi
ms.translationtype: HT
ms.sourcegitcommit: a6aeda8e785fcaabef253a8256b5f6f7a842a324
ms.openlocfilehash: 7f1c64e11e1bec44a558cec10c3d1f90f4951dfd
ms.contentlocale: de-de
ms.lasthandoff: 09/21/2017

---
# <a name="new-and-recently-updated-sql-server-docs"></a>Neu und zuletzt kürzlich aktualisiert: Dokumentation zu SQL Server Data Tools



Beinahe jeden Tag aktualisiert Microsoft einige der vorhandenen Artikel auf der Dokumentationswebsite [Docs.Microsoft.com](http://docs.microsoft.com/). In diesem Artikel werden Auszüge aus den zuletzt aktualisierten Artikeln wiedergegeben. Links zu den neuen Artikel werden ggf. ebenfalls aufgeführt.

Dieser Artikel wurde im Rahmen eines Programms erstellt, das in regelmäßigen Abständen erneut ausgeführt wird. Gelegentlich kann ein Auszug mit falscher Formatierung oder als Markdown aus dem Quellartikel angezeigt werden. Bilder werden hier nie wiedergegeben.

Neueste Updates werden für den folgenden Datumsbereich und Themenbereich gemeldet:



- *Datumsbereich des Updates*: &nbsp; **18.07.2017** &nbsp; –bis– &nbsp; **11.09.2017**
- *Themenbereich*: &nbsp; **SQL Server**




&nbsp;

## <a name="new-articles-created-recently"></a>Neue Artikel, die vor kurzem erstellt wurden

Die folgenden Links leiten Sie zu den neuen Artikeln weiter, die erst kürzlich erstellt wurden.


1. [SQL Server 2008 R2 SP2 Release Notes](sql-server-2008-r2-sp2-release-notes.md)
2. [Versionsanmerkungen zu SQL Server 2012](sql-server-2012-release-notes.md)
3. [SQL Server 2012 SP1 Release Notes](sql-server-2012-sp1-release-notes.md)
4. [SQL Server 2012 SP2 Release Notes](sql-server-2012-sp2-release-notes.md)
5. [Versionsanmerkungen zu SQL Server 2012 SP3](sql-server-2012-sp3-release-notes.md)
6. [SQL Server 2014 Release Notes](sql-server-2014-release-notes.md)
7. [Help Viewer und Offlineinhalt für SQL Server](sql-server-help-installation.md)



&nbsp;

## <a name="updated-articles-with-excerpts"></a>Aktualisierte Artikel mit Auszügen

In diesem Abschnitt werden die Auszüge der Updates aus den Artikeln dargestellt, die vor Kurzem umfassend aktualisiert wurden.

Die Auszüge hier werden getrennt vom richtigen semantischen Kontext angezeigt. Darüber hinaus wird ein Auszug manchmal getrennt von der wichtigen Markdownsyntax wiedergegeben, die ihn im ursprünglichen Artikel umgibt. Aus diesem Grund sind diese Auszüge nur allgemeine Anleitungen. Anhand dieser Auszüge sollen Sie nur entscheiden können, ob Sie sich die Zeit nehmen und den eigentlichen Artikel besuchen möchten.

Kopieren Sie aus diesem und anderen Gründen auf gar keinen Fall Code aus diesen Auszügen, und gehen Sie bei keinem Textauszug von einer 100-prozentigen Richtigkeit der Informationen aus. Besuchen Sie stattdessen den eigentlichen Artikel.





&nbsp;

<a name="compactupdatedlist"/>

## <a name="compact-list-of-articles-updated-recently"></a>Kompakte Liste der Artikel, die vor Kurzem aktualisiert wurden

Diese kompakte Liste enthält Links zu den aktualisierten Artikeln, die im Abschnitt Auszüge aufgeführt sind.

1. [Neuerungen in SQL Server 2016](#TitleNum_1)




&nbsp;

&nbsp;

<a name="TitleNum_1"/>

### <a name="1-nbsp-whats-new-in-sql-server-2016what-s-new-in-sql-server-2016md"></a>1. &nbsp;[Neuerungen in SQL Server 2016](what-s-new-in-sql-server-2016.md)

*Aktualisiert: 20170908* &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 

<!-- Source markdown line 34.  ms.author= "craigg".  -->

&nbsp;


<!-- git diff --ignore-all-space --unified=0 e5bc0c05f120289f09a535400a4d521e4113ae55 0607d0a9af1c9a8dd9d3d7b0606895ff23bbffdc  (PR=0  ,  Filename=what-s-new-in-sql-server-2016.md  ,  Dirpath=docs\sql-server\  ,  MergeCommitSha40=b97cc9723d563b19c85661f5ad7049a96fc904ff) -->



- Laden Sie die **kostenlose** [**SQL Server 2016 Developer-Edition**](https://www.microsoft.com/en-us/cloud-platform/sql-server-editions-developers) herunter.
- Laden Sie die neueste Version von [SQL Server Management Studio (SSMS)](/sql-docs/docs/ssms/download-sql-server-management-studio-ssms) herunter.
- Sie haben ein Azure-Konto? Starten Sie einen [virtuellen Computer mit vorinstalliertem SQL Server 2016](https://azure.microsoft.com/marketplace/partners/microsoft/sqlserver2016sp1standardwindowsserver2016/).

**SQL Server 2016-Datenbankmodul**

- Sie können jetzt während der Installation und Einrichtung von SQL Server **mehrere tempDB**-Datenbankdateien konfigurieren.
- Der neue **Abfragespeicher** speichert Abfragetexte, Ausführungspläne und Leistungsmetriken in der Datenbank und ermöglicht so eine einfache Leistungsüberwachung und Behebung von Leistungsproblemen. Ein Dashboard zeigt an, welche Abfragen am längsten dauern und am meisten Arbeitsspeicher- oder CPU-Ressourcen verbrauchen.
- **Temporale Tabellen** sind Verlaufstabellen, in denen alle Datenänderungen erfasst werden, einschließlich Datum und Uhrzeit.
- Die neue integrierte **JSON-Unterstützung** in SQL Server unterstützt Import-, Export-, Analyse- und Speichervorgänge in JSON.
- Das neue **PolyBase**-Abfragemodul integriert SQL Server mit externen Daten in Hadoop oder Azure Blob Storage. Sie können Daten importieren und exportieren sowie Abfragen ausführen.
- Mit dem neuen **Stretch Database**-Feature können Sie Daten aus einer lokalen SQL Server-Datenbank dynamisch und sicher in einer Azure SQL-Datenbank in der Cloud archivieren. SQL Server fragt automatisch sowohl die lokalen Daten als auch die Remotedaten in den verknüpften Datenbanken ab.
- **In-Memory-OLTP:**
    - Unterstützt jetzt die Einschränkungen FOREIGN KEY, UNIQUE und CHECK sowie die nativen kompilierten gespeicherte Prozeduren OR, NOT, SELECT DISTINCT, OUTER JOIN und Unterabfragen in SELECT.
    - Unterstützt Tabellen mit einer Größe von bis zu 2 TB (bisheriger Maximalwert: 256 GB).
    - Bietet Erweiterungen des ColumnStore-Index für die Sortierung und die Unterstützung von Always On-Verfügbarkeitsgruppen.
- Neue Sicherheitsfeatures:
    - **Always Encrypted:** Wenn dieses Feature aktiviert ist, kann nur die Anwendung, die über den Verschlüsselungsschlüssel verfügt, auf die verschlüsselten sensiblen Daten in einer SQL Server 2016-Datenbank zugreifen. Der Schlüssel wird nie an SQL Server übergeben.







## <a name="similar-articles"></a>Ähnliche Artikel

<!--  HOW TO:
    Refresh this file's line items with the latest 'Count-in-Similars*' content.
    Then run Run-533-*.BAT
-->

Dieser Abschnitt enthält sehr ähnliche Artikel für zuletzt aktualisierte Artikel in anderen Themenbereichen innerhalb des gleichen GitHub-Repositorys: [MicrosoftDocs/sql-docs-pr](https://github.com/MicrosoftDocs/sql-docs/).

#### <a name="subject-areas-which-do-have-new-or-recently-updated-articles"></a>Themenbereiche, die über neue oder kürzlich aktualisierte Artikel verfügen

- [New + Updated (3+12): **Advanced Analytics for SQL** docs (Neu + Aktualisiert (3+12): Dokumentation zu Advanced Analytics für SQL)](../advanced-analytics/new-updated-advanced-analytics.md)
- [Neu und aktualisiert (5+0): **Herstellen einer Verbindung mit SQL** – Dokumentation](../connect/new-updated-connect.md)
- [Neu und aktualisiert (5+1): **Datenbankmodul für SQL** – Dokumentation](../database-engine/new-updated-database-engine.md)
- [Neu und aktualisiert (19+82): **Integration Services für SQL** – Dokumentation](../integration-services/new-updated-integration-services.md)
- [Neu und aktualisiert (1+8): **Linux für SQL** – Dokumentation](../linux/new-updated-linux.md)
- [Neu und aktualisiert (12+1): **Relationale Datenbanken für SQL** – Dokumentation](../relational-databases/new-updated-relational-databases.md)
- [Neu und aktualisiert (0+1): **Reporting Services für SQL** – Dokumentation](../reporting-services/new-updated-reporting-services.md)
- [Neu und aktualisiert (7+1): **Microsoft SQL Server** – Dokumentation](../sql-server/new-updated-sql-server.md)
- [Neu und aktualisiert (1+1): **SQL Server Data Tools (SSDT)** – Dokumentation](../ssdt/new-updated-ssdt.md)
- [Neu und aktualisiert (0+2): **SQL Server Migration Assistant (SSMA)** – Dokumentation](../ssma/new-updated-ssma.md)
- [Neu und aktualisiert (1+4): **SQL Server Management Studio (SSMS)** – Dokumentation](../ssms/new-updated-ssms.md)
- [Neu und aktualisiert (4+1): **Transact-SQL** – Dokumentation](../t-sql/new-updated-t-sql.md)
- [New + Updated (0+1): **Tools for SQL** docs (Neu + Aktualisiert (0+1): Dokumentation zu Tools für SQL)](../tools/new-updated-tools.md)

#### <a name="subject-areas-which-have-no-new-or-recently-updated-articles"></a>Themenbereiche, die über keine neuen oder kürzlich aktualisierten Artikel verfügen

- [New + Updated (0+0): **ActiveX Data Objects (ADO) for SQL** docs (Neu + Aktualisiert (0+0): ActiveX Data Objects (ADO) für SQL-Dokumente)](../ado/new-updated-ado.md)
- [New + Updated (0+0): **Analysis Services for SQL** docs (Neu + Aktualisiert (0+0): Dokumentation zu Analysis Services für SQL)](../analysis-services/new-updated-analysis-services.md)
- [New + Updated (0+0): **Data Quality Services for SQL** docs (Neu + Aktualisiert (0+0): Data Quality Services für SQL-Dokumente)](../data-quality-services/new-updated-data-quality-services.md)
- [New + Updated (0+0): **Data Mining Extensions (DMX) for SQL** docs (Neu + Aktualisiert (0+0): Data Mining-Erweiterungen (DMX) für SQL)](../dmx/new-updated-dmx.md)
- [New + Updated (0+0): **Master Data Services (MDS) for SQL** docs (Neu + Aktualisiert (0+0): Dokumentation zu Master Data Services (MDS) für SQL)](../master-data-services/new-updated-master-data-services.md)
- [New + Updated (0+0): **Multidimensional Expressions (MDX) for SQL** docs (Neu + Aktualisiert (0+0): Mehrdimensionale Ausdrücke für SQL)](../mdx/new-updated-mdx.md)
- [New + Updated (0+0): **ODBC (Open Database Connectivity) for SQL** docs (Neu + Aktualisiert (0+0): Open Database Connectivity für SQL-Dokumente)](../odbc/new-updated-odbc.md)
- [New + Updated (0+0): **PowerShell for SQL** docs (Neu + Aktualisiert (0+0): PowerShell für SQL-Dokumente)](../powershell/new-updated-powershell.md)
- [New + Updated (0+0): **Samples for SQL** docs (Neu + Aktualisiert (0+0): Beispiele für SQL-Dokumente)](../sample/new-updated-sample.md)
- [New + Updated (0+0): **XQuery for SQL** docs (Neu + Aktualisiert (0+0): XQuery für SQL-Dokumente)](../xquery/new-updated-xquery.md)



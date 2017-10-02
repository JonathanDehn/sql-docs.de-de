---
title: "Aktualisiert – Dokumentation zu relationalen Datenbanken | Microsoft-Dokumentation"
description: "Zeigen Sie Codeausschnitte von aktualisierten Inhalten in der zuletzt geänderten Dokumentation zu relationale Datenbanken an."
services: na
documentationcenter: 
author: MightyPen
manager: jhubbard
editor: BYHAM
ms.service: na
ms.topic: updart-autogen
ms.technology: database-engine
ms.custom: UpdArt.exe
ms.workload: relational-databases
ms.tgt_pltfrm: na
ms.devlang: na
ms.date: 09/11/2017
ms.author: genemi
ms.translationtype: HT
ms.sourcegitcommit: 15080827744c19120a8474f3142004c4af7a4064
ms.openlocfilehash: ee7d66bcd8720234f4aec97d24ce16ed21888a3c
ms.contentlocale: de-de
ms.lasthandoff: 09/13/2017

---
# <a name="new-and-recently-updated-relational-databases-docs"></a>Neu und zuletzt aktualisiert: Dokumentation zu relationalen Datenbanken



Beinahe jeden Tag aktualisiert Microsoft einige der vorhandenen Artikel auf der Dokumentationswebsite [Docs.Microsoft.com](http://docs.microsoft.com/). In diesem Artikel werden Auszüge aus den zuletzt aktualisierten Artikeln wiedergegeben. Links zu den neuen Artikel werden ggf. ebenfalls aufgeführt.

Dieser Artikel wurde im Rahmen eines Programms erstellt, das in regelmäßigen Abständen erneut ausgeführt wird. Gelegentlich kann ein Auszug mit falscher Formatierung oder als Markdown aus dem Quellartikel angezeigt werden. Bilder werden hier nie wiedergegeben.

Neueste Updates werden für den folgenden Datumsbereich und Themenbereich gemeldet:



- *Datumsbereich des Updates*: &nbsp; **18.07.2017** &nbsp; –bis– &nbsp; **11.09.2017**
- *Themenbereich:* &nbsp; **Relationale Datenbanken**




&nbsp;

## <a name="new-articles-created-recently"></a>Neue Artikel, die vor kurzem erstellt wurden

Die folgenden Links leiten Sie zu den neuen Artikeln weiter, die erst kürzlich erstellt wurden.


1. [Importieren von Daten aus Excel in SQL Server oder Azure SQL-Datenbank](import-export/import-data-from-excel-to-sql.md)
2. [Troubleshoot PolyBase Kerberos connectivity (Problembehandlung: PolyBase-Kerberos-Konnektivität)](polybase/polybase-troubleshoot-connectivity.md)
3. [Transparente Datenverschlüsselung (TDE)](security/encryption/transparent-data-encryption.md)
4. [Transparent Data Encryption für Azure SQL-Datenbank und Data Warehouse](security/encryption/transparent-data-encryption-azure-sql.md)
5. [Transparent Data Encryption mit Bring Your Own Key-Unterstützung für Azure SQL-Datenbank und Data Warehouse](security/encryption/transparent-data-encryption-byok-azure-sql.md)
6. [PowerShell: Aktivieren von Transparent Data Encryption mithilfe Ihres eigenen Schlüssels aus Azure Key Vault](security/encryption/transparent-data-encryption-byok-azure-sql-configure.md)
7. [Rotieren einer Transparent Data Encryption-Schutzvorrichtung (TDE) mithilfe von PowerShell](security/encryption/transparent-data-encryption-byok-azure-sql-key-rotation.md)
8. [Entfernen einer TDE-Schutzvorrichtung (Transparent Data Encryption) mithilfe von PowerShell](security/encryption/transparent-data-encryption-byok-azure-sql-remove-tde-protector.md)
9. [SQL Server Shared Management Objects (SMO) License Terms (Lizenzbedingungen für SQL Server Shared Management Objects (SMO))](server-management-objects-smo/smo-license-terms.md)
10. [sys.external_libraries (Transact-SQL)](system-catalog-views/sys-external-libraries-transact-sql.md)
11. [sys.external_library_files (Transact-SQL)](system-catalog-views/sys-external-library-files-transact-sql.md)
12. [sp_rxPredict](system-stored-procedures/sp-rxpredict-transact-sql.md)



&nbsp;

## <a name="updated-articles-with-excerpts"></a>Aktualisierte Artikel mit Auszügen

In diesem Abschnitt werden die Auszüge der Updates aus den Artikeln dargestellt, die vor Kurzem umfassend aktualisiert wurden.

Die Auszüge hier werden getrennt vom richtigen semantischen Kontext angezeigt. Darüber hinaus wird ein Auszug manchmal getrennt von der wichtigen Markdownsyntax wiedergegeben, die ihn im ursprünglichen Artikel umgibt. Aus diesem Grund sind diese Auszüge nur allgemeine Anleitungen. Anhand dieser Auszüge sollen Sie nur entscheiden können, ob Sie sich die Zeit nehmen und den eigentlichen Artikel besuchen möchten.

Kopieren Sie aus diesem und anderen Gründen auf gar keinen Fall Code aus diesen Auszügen, und gehen Sie bei keinem Textauszug von einer 100-prozentigen Richtigkeit der Informationen aus. Besuchen Sie stattdessen den eigentlichen Artikel.





&nbsp;

<a name="compactupdatedlist"/>

## <a name="compact-list-of-articles-updated-recently"></a>Kompakte Liste der Artikel, die vor Kurzem aktualisiert wurden

Diese kompakte Liste enthält Links zu den aktualisierten Artikeln, die im Abschnitt Auszüge aufgeführt sind.

1. [Automatische Optimierung](#TitleNum_1)




&nbsp;

&nbsp;

<a name="TitleNum_1"/>

### <a name="1-nbsp-automatic-tuningautomatic-tuningautomatic-tuningmd"></a>1. &nbsp; [Automatische Optimierung](automatic-tuning/automatic-tuning.md)

*Aktualisiert: 16.08.2017* &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 

<!-- Source markdown line 64.  ms.author= "jovanpop".  -->

&nbsp;


<!-- git diff --ignore-all-space --unified=0 be765a1acf9bdfd5485520d16160677583e81f8e 135d926227094374e6ec5484e7babee625b44bb2  (PR=2860  ,  Filename=automatic-tuning.md  ,  Dirpath=docs\relational-databases\automatic-tuning\  ,  MergeCommitSha40=e4a6157cb56c6db911406585f841046a431eef99) -->



**Automatische Korrektur der Planauswahl**


„..!NCLUDE-NotShown--ssde_md--../../includes/ssde_md.md)]“ kann automatisch zum letzten bekannten geeigneten Plan wechseln, unabhängig davon, wann die Regression der Planauswahl erkannt wurde.

„![SQL plan choice correction--media/force-last-good-plan.png „SQL-Korrektur der Planauswahl“)

..!NCLUDE-NotShown--ssde_md--../../includes/ssde_md.md)]“ erkennt automatisch alle potenziellen Regressionen von Planauswahlen, einschließlich des Plans, der statt des falschen Plans verwendet werden soll.
Wenn „..!NCLUDE-NotShown--ssde_md--../../includes/ssde_md.md)]“ für den letzten bekannten geeigneten Plan gilt, wird die Leistung des erzwungenen Plans automatisch überwacht. Wenn der erzwungene Plan nicht besser als der zurückgestellte Plan ist, wird der neue Plan nicht mehr erzwungen und „..!NCLUDE-NotShown--ssde_md--../../includes/ssde_md.md)]“ kompiliert einen neuen Plan. Wenn „..!NCLUDE-NotShown--ssde_md--../../includes/ssde_md.md)]“ bestätigt, dass der erzwungene Plan besser als der zurückgestellte ist, wird der erzwungene Plan bis zu einer Neukompilierung (z.B. bei der nächsten Statistik oder Schemaänderung) beibehalten, die besser als der zurückgestellte Plan ist.

**Aktivieren der automatischen Korrektur der Planauswahl**


Sie können die automatische Optimierung pro Datenbank aktivieren und angeben, dass der letzte geeignete Plan erzwungen werden soll, wenn eine Regression der Planänderung erkannt wird. Die automatische Optimierung wird durch folgenden Befehl aktiviert:

```
ALTER DATABASE current
SET AUTOMATIC_TUNING ( FORCE_LAST_GOOD_PLAN = ON );
```
Wenn Sie diese Option aktivieren, erzwingt „..!NCLUDE-NotShown--ssde_md--../../includes/ssde_md.md)]“ automatisch jede Empfehlung, bei der der geschätzte CPU-Gewinn größer als 10 Sekunden ist oder bei der die Anzahl von Fehlern im neuen Plan höher als die Anzahl von Fehlern im empfohlenen Plan ist. Außerdem wird überprüft, ob der erzwungene Plan besser als der aktuelle ist.

**Alternative – manuelle Korrektur der Planauswahl**


Ohne die automatische Optimierung müssen Benutzer ihr System regelmäßig überwachen und nach zurückgestellten Abfragen suchen. Wenn Pläne zurückgestellt wurden, sollte der Benutzer diese finden.







## <a name="similar-articles"></a>Ähnliche Artikel

<!--  HOW TO:
    Refresh this file's line items with the latest 'Count-in-Similars*' content.
    Then run Run-533-*.BAT
-->

Dieser Abschnitt enthält sehr ähnliche Artikel für zuletzt aktualisierte Artikel in anderen Themenbereichen innerhalb des gleichen GitHub-Repositorys: [MicrosoftDocs/sql-docs-pr](https://github.com/MicrosoftDocs/sql-docs/).

#### <a name="subject-areas-which-do-have-new-or-recently-updated-articles"></a>Themenbereiche, die über neue oder kürzlich aktualisierte Artikel verfügen

- [New + Updated (3+12): **Advanced Analytics for SQL** docs (Neu + Aktualisiert (3+12): Dokumentation zu Advanced Analytics für SQL)](../advanced-analytics/new-updated-advanced-analytics.md)
- [New + Updated (5+0): **Connect to SQL** docs (Neu + Aktualisiert (1+2): Dokumentation zur Herstellung einer Verbindung mit SQL)](../connect/new-updated-connect.md)
- [New + Updated (5+1): **Database Engine for SQL** docs (Neu + Aktualisiert (6+0): Dokumentation zum Datenbankmodul für SQL)](../database-engine/new-updated-database-engine.md)
- [New + Updated (19+82): **Integration Services for SQL** docs (Neu + Aktualisiert (0+0): Dokumentation zu SSIS für SQL)](../integration-services/new-updated-integration-services.md)
- [New + Updated (1+8): **Linux for SQL** docs (Neu + Aktualisiert (13+2): Dokumentation zu Linux für SQL)](../linux/new-updated-linux.md)
- [New + Updated (12+1): **Relational Databases for SQL** docs (Neu + Aktualisiert (8+4): Dokumentation zu relationalen Datenbanken für SQL)](../relational-databases/new-updated-relational-databases.md)
- [New + Updated (0+1): **Reporting Services for SQL** docs (Neu + Aktualisiert (0+0): Dokumentation zu Reporting Services für SQL)](../reporting-services/new-updated-reporting-services.md)
- [New + Updated (7+1): **Microsoft SQL Server** docs (Neu + Aktualisiert (2+2): Dokumentation zu Microsoft SQL Server)](../sql-server/new-updated-sql-server.md)
- [New + Updated (1+1): **SQL Server Data Tools (SSDT)** docs (Neu + Aktualisiert (0+0): Dokumentation zu SQL Server Data Tools (SSDT))](../ssdt/new-updated-ssdt.md)
- [New + Updated (0+2): **SQL Server Migration Assistant (SSMA)** docs (Neu + Aktualisiert (0+0): SQL Server Migration Assistant-Dokumente (SSMA))](../ssma/new-updated-ssma.md)
- [New + Updated (1+4): **SQL Server Management Studio (SSMS)** docs (Neu + Aktualisiert (0+1): Dokumentation zu SQL Server Management Studio (SSMS))](../ssms/new-updated-ssms.md)
- [New + Updated (4+1): **Transact-SQL** docs (Neu + Aktualisiert (1+0): Dokumentation zu Transact-SQL)](../t-sql/new-updated-t-sql.md)
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



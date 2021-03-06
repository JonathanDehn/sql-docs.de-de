---
title: Verwenden von SSMS zum Verwalten von SQLServer on Linux | Microsoft Docs
description: ''
author: rothja
ms.author: jroth
manager: craigg
ms.date: 05/21/2018
ms.topic: article
ms.prod: sql
ms.component: ''
ms.suite: sql
ms.technology: linux
ms.assetid: b2fcf858-21c3-462a-8d49-50c85647d092
ms.custom: sql-linux
ms.openlocfilehash: 2b6293e7c0d80eb1ebe02d6cd03f17626d793c05
ms.sourcegitcommit: b5ab9f3a55800b0ccd7e16997f4cd6184b4995f9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/23/2018
---
# <a name="use-sql-server-management-studio-on-windows-to-manage-sql-server-on-linux"></a>Verwenden von SQL Server Management Studio unter Windows zum Verwalten von SQL Server on Linux

[!INCLUDE[appliesto-ss-xxxx-xxxx-xxx-md-linuxonly](../includes/appliesto-ss-xxxx-xxxx-xxx-md-linuxonly.md)]

Dieser Artikel führt [SQL Server Management Studio (SSMS)](../ssms/sql-server-management-studio-ssms.md) und führt Sie durch ein paar häufige Aufgaben. SSMS ist eine Windows-Anwendung, daher SSMS verwenden, wenn Sie einen Windows-Computer verfügen, der mit einer SQL Server-Remoteinstanz unter Linux eine Verbindung herstellen können.

> [!TIP]
> Wenn Sie nicht für die Ausführung von SSMS auf einen Windows-Computer verfügen, sollten Sie die neue [SQL Server Operationen Studio](../sql-operations-studio/index.md). Es stellt ein grafisches Tool zum Verwalten von SQL Server und auf Linux- und Windows ausgeführt wird.

[SQL Server Management Studio (SSMS)](../ssms/sql-server-management-studio-ssms.md) ist Teil einer Suite von SQL-Tools, die Microsoft-Angebote kostenlos für Entwicklung und Verwaltung Anforderungen freizugeben. SSMS ist eine integrierte Umgebung zugreifen, konfigurieren, verwalten, verwalten und entwickeln aller Komponenten von SQL Server. Sie können mit SQL Server auf einer beliebigen Plattform sowohl lokal ausgeführten, in Docker-Containern und in der Cloud verbinden. Herstellen einer Verbindung auch mit Azure SQL-Datenbank und Azure SQL Data Warehouse. SSMS kombiniert eine umfassende Gruppe grafischer Tools mit einer Reihe umfassender Skript-Editoren, um Entwicklern und Administratoren mit verschiedenem Kenntnisstand den Zugriff auf SQL Server zu ermöglichen.

SSMS bietet eine Breite Palette von Funktionen zur Entwicklung und Verwaltung für SQL Server, Tools, einschließlich:

- Konfigurieren Sie, überwachen Sie und verwalten Sie einzelne oder mehrere Instanzen von SQL Server
- bereitstellen, überwachen und aktualisieren Sie die Datenebenen-Komponenten wie z. B. Datenbanken und Data Warehouses
- Sichern und Wiederherstellen von Datenbanken
- Erstellen und T-SQL-Abfragen und Skripts ausführen und die Ergebnisse anzuzeigen
- Generieren von T-SQL-Skripts für Datenbankobjekte
- Anzeigen und Bearbeiten von Daten in Datenbanken
- Visuell zu entwerfen, T-SQL-Abfragen und Datenbankobjekte, z. B. Sichten, Tabellen und gespeicherten Prozeduren

Finden Sie unter [neuerungen SSMS?](../ssms/sql-server-management-studio-ssms.md) für Weitere Informationen über SSMS.

## <a name="install-the-newest-version-of-sql-server-management-studio-ssms"></a>Installieren Sie die neueste Version von SQL Server Management Studio (SSMS)

Bei der Arbeit mit SQL Server sollten Sie immer die neueste Version von SQL Server Management Studio (SSMS) verwenden. Die neueste Version von SSMS wird laufend aktualisiert und optimiert und arbeitet zurzeit mit SQLServer 2017 on Linux. Zum Herunterladen und installieren Sie die neueste Version, finden Sie unter [Herunterladen von SQL Server Management Studio](../ssms/download-sql-server-management-studio-ssms.md). Um auf dem neuesten Stand zu bleiben, die neueste Version von SSMS werden Sie aufgefordert, wenn eine neue Version für den download verfügbaren vorhanden ist.

> [!NOTE]
> Lesen Sie vor dem Verwenden von SSMS zum Verwalten von Linux, die [bekannte Probleme](sql-server-linux-release-notes.md) für SSMS unter Linux.

## <a name="connect-to-sql-server-on-linux"></a>Herstellen einer Verbindung mit SQLServer on Linux

Verwenden Sie die folgenden grundlegenden Schritte zum Herstellen einer Verbindung aus:

1. Starten Sie SSMS, geben Sie **Microsoft SQL Server Management Studio** in Windows-Suchfeld ein, und klicken Sie dann auf den desktop-app.

    ![SQL Server Management Studio](./media/sql-server-linux-manage-ssms/ssms.png)

1. In der **Verbindung mit Server herstellen** Fenster, geben Sie die folgenden Informationen (wenn SSMS bereits ausgeführt wird, klicken Sie auf **verbinden > Datenbankmodul** öffnen die **Verbindung mit Server herstellen** Fenster):

   | Einstellung | Description |
   |-----|-----|
   | **Servertyp** | Der Standardwert ist-Datenbankmoduls. Ändern Sie diesen Wert nicht. |
   | **Servername** | Geben Sie den Namen des Ziel-Linux SQL Server-Computer oder die IP-Adresse ein. |
   | **Authentifizierung** | Verwenden Sie für SQL Server 2017 unter Linux **SQL Server-Authentifizierung**. |
   | **Anmeldename** | Geben Sie den Namen eines Benutzers mit Zugriff auf eine Datenbank auf dem Server (z. B. die Standardeinstellung **SA** Konto während des Setups erstellt). |
   | **Kennwort** | Geben Sie das Kennwort für den angegebenen Benutzer (für die **SA** Konto Sie dies beim Setup erstellt wurde). |

    ![SQL Server Management Studio: Eine Verbindung mit SQL-Datenbankserver](./media/sql-server-linux-manage-ssms/connect.png)

1. Klicken Sie auf **Verbinden**.

    > [!TIP]
    > Wenn Sie einen Verbindungsfehler erhalten, versuchen Sie zunächst das Problem aus der Fehlermeldung zu ermitteln. Überprüfen Sie anschließend die [Empfehlungen zur Verbindungsproblembehandlung](sql-server-linux-troubleshooting-guide.md#connection).
 
1. Nach einer erfolgreichen verbindungsherstellung mit SQL Server **Objekt-Explorer** wird geöffnet, und Sie können jetzt die Datenbank für administrative Aufgaben oder Abfragen von Daten zugreifen.

## <a name="run-transact-sql-queries"></a>Ausführen von Transact-SQL-Abfragen

Nachdem Sie eine Verbindung mit dem Server herstellen, können Sie mit einer Datenbank verbinden und Ausführen von Transact-SQL-Abfragen. Transact-SQL-Abfragen können für nahezu jede Task "Datenbank" verwendet werden.

1. In **Objekt-Explorer**, navigieren Sie in die Zieldatenbank auf dem Server. Erweitern Sie z. B. **Systemdatenbanken** zur Bearbeitung der **master** Datenbank.

1. Mit der rechten Maustaste in der Datenbank, und wählen Sie dann **neue Abfrage**.

1. In das Abfragefenster ein Schreiben einer Transact-SQL-Abfrage zurück auf die Namen aller Datenbanken auf dem Server.

   ```sql
   SELECT [Name]
   FROM sys.Databases
   ```

   Wenn Sie zum Schreiben von Abfragen nicht vertraut sind, finden Sie unter [Schreiben von Transact-SQL-Anweisungen](../t-sql/tutorial-writing-transact-sql-statements.md).

1. Klicken Sie auf die **Execute** Schaltfläche, um die Abfrage auszuführen und die Ergebnisse anzuzeigen.

   ![Erfolg. Herstellen einer Verbindung mit SQL-Datenbankserver: SQL Server Management Studio](./media/sql-server-linux-manage-ssms/execute-query.png)

Obwohl es beinahe jede Verwaltungsaufgabe mit Transact-SQL-Abfragen möglich ist, ist SSMS ein grafisches Tool, mit der, einfacher zu verwalten, SQL Server. Die folgenden Abschnitte enthalten einige Beispiele für die Verwendung der grafischen Benutzeroberfläche.

## <a name="create-and-manage-databases"></a>Erstellen und Verwalten von Datenbanken

Während einer Verbindung mit der *master* Datenbank, Sie können Datenbanken auf dem Server erstellen und ändern oder Löschen vorhandener Datenbanken. Die folgenden Schritte beschreiben, wie Sie verschiedene allgemeine Datenbankverwaltungsaufgaben über Management Studio ausführen. Um diese Aufgaben ausführen, stellen Sie sicher, dass Sie verbunden sind, die *master* Datenbank mit der prinzipalanmeldung auf Serverebene, die Sie beim Einrichten einer Verbindung mit SQL Server-2017 unter Linux erstellt haben.

### <a name="create-a-new-database"></a>Erstellen einer neuen Datenbank

1. Starten Sie SSMS aus, und verbinden Sie Ihre Server in SQL Server-2017 unter Linux

2. Objekt-Explorer mit der Maustaste auf die *Datenbanken* Ordner, und klicken Sie dann auf * neue Datenbank... "

3. In der *neue Datenbank* Dialogfeld, geben Sie einen Namen für die neue Datenbank, und klicken Sie dann auf *OK*

Die neue Datenbank wird auf dem Server wurde erfolgreich erstellt. Wenn Sie lieber eine neue Datenbank mit T-SQL zu erstellen, finden Sie unter [CREATE DATABASE (SQL Server Transact-SQL)](../t-sql/statements/create-database-sql-server-transact-sql.md).

### <a name="drop-a-database"></a>Löschen einer Datenbank

1. Starten Sie SSMS aus, und verbinden Sie Ihre Server in SQL Server-2017 unter Linux

2. Erweitern Sie im Objekt-Explorer die *Datenbanken* Ordner, um eine Liste aller Datenbanken auf dem Server anzuzeigen.

3. Klicken Sie im Objekt-Explorer mit der rechten Maustaste auf die Datenbank, die Sie löschen möchten, und klicken Sie dann auf *löschen*

4. In der *Objekt löschen* Dialogfeld Kontrollkästchen *bestehende Verbindungen schließen* , und klicken Sie dann auf *OK*

Die Datenbank wird vom Server wurde erfolgreich gelöscht. Wenn Sie eine Datenbank mit T-SQL löschen möchten, finden Sie unter [DROP DATABASE (SQL Server Transact-SQL)](../t-sql/statements/drop-database-transact-sql.md).

## <a name="use-activity-monitor-to-see-information-about-sql-server-activity"></a>Mit dem Aktivitätsmonitor Informationen zu SQL Server-Aktivitäten finden Sie unter

Die [Aktivitätsmonitor](../relational-databases/performance-monitor/activity-monitor.md) Tool ist in SQL Server Management Studio (SSMS) erstellt und zeigt Informationen zu SQL Server-Prozesse und Auswirkungen diese Prozesse auf die aktuelle Instanz von SQL Server.

1. Starten Sie SSMS aus, und verbinden Sie Ihre Server in SQL Server-2017 unter Linux

1. Klicken Sie im Objekt-Explorer mit der Maustaste die *Server* Knoten, und klicken Sie dann auf *Aktivitätsmonitor*

Aktivitätsmonitor zeigt erweiterbare und reduzierbare Bereichen mit den folgenden Informationen an:

- Übersicht
- Prozesse
- Ressourcenwartevorgänge
- Datendatei-e/a
- Aktuelle wertvolle Abfragen
- Aktuelle ressourcenintensive Abfragen

Wenn ein Bereich erweitert wird, fragt der Aktivitätsmonitor die Instanz nach Informationen. Wenn ein Bereich reduziert wird, werden sämtliche Abfrageaktivitäten für diesen Bereich angehalten. Sie können einen oder mehrere Bereiche erweitern, zur gleichen Zeit um unterschiedliche Aktivitätstypen für die Instanz anzuzeigen.

## <a name="see-also"></a>Siehe auch
- [Was ist SSMS?](../ssms/sql-server-management-studio-ssms.md)
- [Exportieren Sie und importieren Sie eine Datenbank mit SSMS](sql-server-linux-migrate-ssms.md)
- [Lernprogramm: SQL Server Management Studio](../ssms/tutorials/tutorial-sql-server-management-studio.md)
- [Lernprogramm: Schreiben von Transact-SQL-Anweisungen](../t-sql/tutorial-writing-transact-sql-statements.md)
- [Überwachen der Serverleistung und -aktivität](../relational-databases/performance/server-performance-and-activity-monitoring.md)

---
title: Verwalten von SQLServer on Linux | Microsoft Docs
description: "Dieses Thema enthält Links zu allgemeinen Verwaltungsaufgaben und Tools für SQL Server auf dem Linux ausgeführt wird."
author: rothja
ms.author: jroth
manager: jhubbard
ms.date: 03/17/2017
ms.topic: article
ms.prod: sql-linux
ms.technology: database-engine
ms.assetid: 6bd8eb0b-593d-467e-87ea-ab1c4dbcd1ea
ms.custom: H1Hack27Feb2017
ms.translationtype: MT
ms.sourcegitcommit: a6aeda8e785fcaabef253a8256b5f6f7a842a324
ms.openlocfilehash: 5f7c0f61cf9f441c56529ddaaddc96a0c318ce59
ms.contentlocale: de-de
ms.lasthandoff: 09/21/2017

---
# <a name="choose-the-right-tool-to-manage-sql-server-on-linux"></a>Wählen Sie das richtige Tool zum Verwalten von SQL Server on Linux

[!INCLUDE[tsql-appliesto-sslinux-only](../includes/tsql-appliesto-sslinux-only.md)]

Es gibt verschiedene Methoden zum Verwalten von SQL Server 2017 RC2 unter Linux. Im folgende Abschnitt bieten einen schnellen Überblick über unterschiedliche Management-Tools und Techniken mit Zeigern auf Weitere Ressourcen.

## <a name="mssql-conf"></a>MSSQL-conf 
Die **Mssql-Conf** Tool konfiguriert die SQL Server unter Linux. Weitere Informationen finden Sie unter [konfigurieren Sie SQL Server unter Linux mit Mssql-Conf](sql-server-linux-configure-mssql-conf.md).

## <a name="transact-sql"></a>Transact-SQL

Nahezu jede Option in einem Clienttool ausführen kann auch mit Transact-SQL-Anweisungen ausgeführt werden. SQL Server bietet [dynamische Verwaltungssichten (DMVs)](/sql-docs/docs/relational-databases/system-dynamic-management-views/system-dynamic-management-views) Status und Konfiguration von SQL Server-Abfrage. Es gibt auch [Transact-SQL-Befehle](https://msdn.microsoft.com/library/bb510741.aspx) Datenbankverwaltungsaufgaben. Sie können diese Befehle in jedem Clienttool ausführen, die eine Verbindung mit SQL Server herstellen und Ausführen von Transact-SQL-Abfragen unterstützt. Beispiele hierfür sind [Sqlcmd](sql-server-linux-setup-tools.md), [Visual Studio Code](sql-server-linux-develop-use-vscode.md), und [SQL Server Management Studio](sql-server-linux-manage-ssms.md).

## <a name="sql-server-management-studio-on-windows"></a>SQL Server Management Studio unter Windows

SQL Server Management Studio (SSMS) ist eine Windows-Anwendung, die eine grafische Benutzeroberfläche bereitstellt, für die Verwaltung von SQL Server. Obwohl es zurzeit nur unter Windows ausgeführt wird, können es Sie Ihre Linux SQL Server-Instanzen herstellen. Weitere Informationen zur Verwendung von SSMS zum Verwalten von SQL Server finden Sie unter [Verwenden von SSMS zum Verwalten von SQL Server on Linux](sql-server-linux-manage-ssms.md).

## <a name="powershell"></a>PowerShell

PowerShell bietet eine umfangreiche befehlszeilenumgebung zum Verwalten von SQL Server on Linux. Weitere Informationen finden Sie unter [Verwenden von PowerShell zum Verwalten von SQL Server on Linux](sql-server-linux-manage-powershell.md).

## <a name="next-steps"></a>Nächste Schritte

Weitere Informationen zu SQL Server unter Linux finden Sie unter [SQL Server on Linux](sql-server-linux-overview.md).
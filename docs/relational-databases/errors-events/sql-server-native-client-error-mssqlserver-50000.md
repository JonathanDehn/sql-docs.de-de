---
title: MSSQLSERVER_50000 | Microsoft-Dokumentation
ms.custom: ''
ms.date: 04/04/2017
ms.prod: sql
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.reviewer: ''
ms.suite: sql
ms.technology: supportability
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- 50000 [SQL Server Native Client setup error]
ms.assetid: 5426d87a-d5d9-4984-b211-b07d69e834a2
caps.latest.revision: 16
author: MashaMSFT
ms.author: mathoma
manager: craigg
monikerRange: '>= aps-pdw-2016 || = azuresqldb-current || = azure-sqldw-latest || >= sql-server-2016 || = sqlallproducts-allversions'
ms.openlocfilehash: a67941c3eb21b0029a84aa3c2abbe79b34aa38d3
ms.sourcegitcommit: ee661730fb695774b9c483c3dd0a6c314e17ddf8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2018
---
# <a name="sql-server-native-client-error-mssqlserver50000"></a>SQL Server-Fehler beim nativen Client MSSQLSERVER_50000
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
[!INCLUDE[SNAC_Deprecated](../../includes/snac-deprecated.md)]

    
## <a name="details"></a>Details  
  
|||  
|-|-|  
|Produktname|SQL Server|  
|Produktversion|11.0|  
|Ereignis-ID|50000|  
|Ereignisquelle|SETUP|  
|Komponente|[!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client|  
|Symbolischer Name||  
|Meldungstext|Netzwerkfehler beim Lesen der Datei '% * ls'.|  
  
## <a name="explanation"></a>Erklärung  
 Es wurde versucht, [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client auf einem Computer zu installieren (oder zu aktualisieren), auf dem [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client bereits installiert ist und die vorhandene Installation über eine MSI-Datei ausgeführt wurde, die ursprünglich den Namen sqlncli.msi hatte und dann umbenannt wurde.  
  
## <a name="user-action"></a>Benutzeraktion  
 Um diesen Fehler zu beheben, deinstallieren Sie die vorhandene Version von [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client. Um den Fehler zu verhindern, installieren Sie [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Native Client über eine MSI-Datei, die nicht sqlncli.msi heißt.  
  
## <a name="internal-only"></a>Nur intern  
  

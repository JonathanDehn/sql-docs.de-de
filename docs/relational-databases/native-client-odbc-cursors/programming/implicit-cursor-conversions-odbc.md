---
title: Implizite Cursorkonvertierung (ODBC) | Microsoft Docs
ms.custom: 
ms.date: 03/06/2017
ms.prod: sql-non-specified
ms.prod_service: database-engine, sql-database, sql-data-warehouse, pdw
ms.service: 
ms.component: native-client-odbc-cursors
ms.reviewer: 
ms.suite: sql
ms.technology: docset-sql-devref
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- ODBC cursors, implicit cursor conversions
- implicit cursor conversions
- cursors [ODBC], implicit cursor conversions
ms.assetid: fe29a58d-8448-4512-9ffd-b414784ba338
caps.latest.revision: "33"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: Inactive
ms.openlocfilehash: a661774e9be2311a0c7d113356b2fab5a775ba72
ms.sourcegitcommit: 44cd5c651488b5296fb679f6d43f50d068339a27
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2017
---
# <a name="implicit-cursor-conversions-odbc"></a>Implizite Cursorkonvertierung (ODBC)
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]
[!INCLUDE[SNAC_Deprecated](../../../includes/snac-deprecated.md)]

  Anwendungen können über einen Cursortyp anfordern [SQLSetStmtAttr](../../../relational-databases/native-client-odbc-api/sqlsetstmtattr.md) und führen Sie dann eine SQL-Anweisung, die von Servercursorn des angeforderten Typs nicht unterstützt wird. Ein Aufruf von **SQLExecute** oder **SQLExecDirect** SQL_SUCCESS_WITH_INFO zurückgegeben und **SQLGetDiagRec** zurückgibt:  
  
```  
szSqlState = "01S02", *pfNativeError = 0,  
szErrorMsg="[Microsoft][SQL Server Native Client] Cursor type changed"  
```  
  
 Kann die Anwendung bestimmen, welche Art von Cursor jetzt durch den Aufruf verwendet wird **SQLGetStmtOption** auf SQL_CURSOR_TYPE gesetzt. Die Cursortypkonvertierung gilt nur für eine Anweisung. Das nächste **SQLExecDirect** oder **SQLExecute** erfolgt mithilfe der ursprünglichen anweisungscursoreinstellungen.  
  
## <a name="see-also"></a>Siehe auch  
 [Details zum Programmieren von Cursorn &#40; ODBC &#41;](../../../relational-databases/native-client-odbc-cursors/programming/cursor-programming-details-odbc.md)  
  
  
---
title: Katalogfunktionen in ODBC | Microsoft Docs
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- drivers
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- catalog functions [ODBC], listed
- functions [ODBC], catalog functions
ms.assetid: 4f28f557-7eca-4905-aa6d-45a6cf501a66
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 74b86dfd62a12938d18b4aa11a8d0502db50da13
ms.contentlocale: de-de
ms.lasthandoff: 09/09/2017

---
# <a name="catalog-functions-in-odbc"></a>In ODBC-Katalogfunktionen
ODBC enthält die folgenden Katalogfunktionen:  
  
|Funktion|Description|  
|--------------|-----------------|  
|**SQLTables**|Gibt eine Liste der Kataloge, Schemas, Tabellen und Tabellentypen in der Datenquelle zurück.|  
|**SQLColumns**|Gibt eine Liste der Spalten in einer oder mehreren Tabellen zurück.|  
|**SQLStatistics**|Gibt eine Liste der Statistiken zu einer einzelnen Tabelle zurück. Außerdem gibt eine Liste der Indizes dieser Tabelle zugeordnet.|  
|**SQLSpecialColumns**|Gibt eine Liste der Spalten, die eine Zeile in einer einzelnen Tabelle eindeutig identifiziert. Außerdem gibt eine Liste der Spalten in dieser Tabelle, die automatisch aktualisiert werden.|  
|**SQLPrimaryKeys**|Gibt eine Liste der Spalten, die den Primärschlüssel einer Tabelle zu erstellen.|  
|**SQLForeignKeys**|Gibt eine Liste von Fremdschlüsseln in einer einzelnen Tabelle oder eine Liste von Fremdschlüsseln in anderen Tabellen, die auf einer einzelnen Tabelle verweisen.|  
|**SQLTablePrivileges**|Gibt eine Liste von Berechtigungen, die einer oder mehreren Tabellen zugeordnet.|  
|**SQLColumnPrivileges**|Gibt eine Liste von Berechtigungen, die eine oder mehrere Spalten in einer einzelnen Tabelle zugeordnet.|  
|**SQLProcedures**|Gibt eine Liste der Verfahren in der Datenquelle zurück.|  
|**SQLProcedureColumns**|Gibt eine Liste der Eingabe-und Ausgabeparameter, der Rückgabewert und die Spalten im Resultset einer einzelnen Prozedur zurück.|  
|**SQLGetTypeInfo**|Gibt eine Liste der SQL-Datentypen, die von der Datenquelle unterstützt. Diese Datentypen werden in der Regel verwendet, **CREATE TABLE** und **ALTER TABLE** Anweisungen.|  
  
 Da **SQLTables**, **SQLColumns**, **SQLStatistics**, und **SQLSpecialColumns** entsprechen der Open Group-CLI und **SQLGetTypeInfo** entspricht dem ISO-92-CLI, die sie von den meisten-Treibern implementiert werden. Die verbleibenden Katalogfunktionen sind in der ODBC-Konformitätsgrad.  
  
 Dieser Abschnitt enthält die folgenden Themen.  
  
-   [Daten, die von Katalogfunktionen zurückgegeben werden.](../../../odbc/reference/develop-app/data-returned-by-catalog-functions.md)  
  
-   [Argumente im Katalogfunktionen](../../../odbc/reference/develop-app/arguments-in-catalog-functions.md)  
  
-   [Schema-Ansichten](../../../odbc/reference/develop-app/schema-views.md)
---
title: SESSION_USER (Transact-SQL) | Microsoft Docs
ms.custom: 
ms.date: 03/06/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- SESSION_USER_TSQL
- SESSION_USER
dev_langs:
- TSQL
helpviewer_keywords:
- usernames [SQL Server]
- current user names
- sessions [SQL Server], user names
- displaying user names
- viewing user names
- SESSION_USER function
ms.assetid: 3dbe8532-31b6-4862-8b2a-e58b00b964de
caps.latest.revision: 26
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 88b9d27bfc084e341712c374c54098984c0f3e95
ms.contentlocale: de-de
ms.lasthandoff: 09/01/2017

---
# <a name="sessionuser-transact-sql"></a>SESSION_USER (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all_md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  SESSION_USER gibt den Benutzernamen im Kontext der aktuellen Datenbank zurück.  
  
 ![Themenlinksymbol](../../database-engine/configure-windows/media/topic-link.gif "Topic link icon") [Transact-SQL Syntax Conventions (Transact-SQL-Syntaxkonventionen)](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
SESSION_USER  
```  
  
## <a name="return-types"></a>Rückgabetypen  
 **vom Datentyp nvarchar(128)**  
  
## <a name="remarks"></a>Hinweise  
 Verwenden Sie SESSION_USER mit DEFAULT-Einschränkungen in der CREATE TABLE- oder ALTER TABLE-Anweisung oder als beliebige Standardfunktion. SESSION_USER kann in eine Tabelle eingefügt werden, wenn kein Standardwert angegeben wird. Diese Funktion akzeptiert keine Argumente. SESSION_USER kann in Abfragen verwendet werden.  
  
 Wird SESSION_USER nach einem Kontextwechsel aufgerufen, gibt SESSION_USER den Benutzernamen des Kontexts zurück, dessen Identität angenommen wurde.  
  
## <a name="examples"></a>Beispiele  
  
### <a name="a-using-sessionuser-to-return-the-user-name-of-the-current-session"></a>A. Verwenden von SESSION_USER zur Rückgabe des Benutzernamens der aktuellen Sitzung  
 Im folgenden Beispiel wird eine Variable als Datentyp `nchar` deklariert, ihr der aktuelle Wert von `SESSION_USER` zugewiesen und die Variable dann mit einer Textbeschreibung ausgegeben.  
  
```  
DECLARE @session_usr nchar(30);  
SET @session_usr = SESSION_USER;  
SELECT 'This session''s current user is: '+ @session_usr;  
GO  
```  
  
 Wenn `Surya` Sitzungsbenutzer ist, sieht das Resultset folgendermaßen aus:  
  
 `--------------------------------------------------------------`  
  
 `This session's current user is: Surya`  
  
 `(1 row(s) affected)`  
  
### <a name="b-using-sessionuser-with-default-constraints"></a>B. Verwenden von SESSION_USER mit DEFAULT-Einschränkungen  
 Im folgenden Beispiel wird eine Tabelle erstellt, die `SESSION_USER` als `DEFAULT`-Einschränkung für den Namen der Person verwendet, die den Empfang einer Lieferung aufzeichnet.  
  
```  
USE AdventureWorks2012;  
GO  
CREATE TABLE deliveries3  
(  
 order_id int IDENTITY(5000, 1) NOT NULL,  
 cust_id  int NOT NULL,  
 order_date smalldatetime NOT NULL DEFAULT GETDATE(),  
 delivery_date smalldatetime NOT NULL DEFAULT   
    DATEADD(dd, 10, GETDATE()),  
 received_shipment nchar(30) NOT NULL DEFAULT SESSION_USER  
);  
GO  
```  
  
 Der Tabelle hinzugefügte Datensätze werden mit dem Benutzernamen des aktuellen Benutzers versehen. Im folgenden Beispiel wird der Empfang von Lieferungen von `Wanida`, `Sylvester` und `Alejandro` überprüft. Dies kann durch Wechseln des Benutzerkontexts mithilfe von `EXECUTE AS` emuliert werden.  
  
```  
EXECUTE AS USER = 'Wanida'  
INSERT deliveries3 (cust_id)  
VALUES (7510);  
INSERT deliveries3 (cust_id)  
VALUES (7231);  
REVERT;  
EXECUTE AS USER = 'Sylvester'  
INSERT deliveries3 (cust_id)  
VALUES (7028);  
REVERT;  
EXECUTE AS USER = 'Alejandro'  
INSERT deliveries3 (cust_id)  
VALUES (7392);  
INSERT deliveries3 (cust_id)  
VALUES (7452);  
REVERT;  
GO  
```  
  
 In der folgenden Abfrage werden alle Informationen aus der `deliveries3`-Tabelle ausgewählt.  
  
```  
SELECT order_id AS 'Order #', cust_id AS 'Customer #',   
   delivery_date AS 'When Delivered', received_shipment   
   AS 'Received By'  
FROM deliveries3  
ORDER BY order_id;  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
 `Order #   Customer #  When Delivered       Received By`  
  
 `--------  ----------  -------------------  -----------`  
  
 `5000      7510        2005-03-16 12:02:14  Wanida`  
  
 `5001      7231        2005-03-16 12:02:14  Wanida`  
  
 `5002      7028        2005-03-16 12:02:14  Sylvester`  
  
 `5003      7392        2005-03-16 12:02:14  Alejandro`  
  
 `5004      7452        2005-03-16 12:02:14  Alejandro`  
  
 `(5 row(s) affected)`  
  
## <a name="examples-includesssdwfullincludessssdwfull-mdmd-and-includesspdwincludessspdw-mdmd"></a>Beispiele: [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] und[!INCLUDE[ssPDW](../../includes/sspdw-md.md)]  
  
### <a name="c-using-sessionuser-to-return-the-user-name-of-the-current-session"></a>"C:" Verwenden von SESSION_USER zur Rückgabe des Benutzernamens der aktuellen Sitzung  
 Im folgende Beispiel gibt den Sitzungsbenutzer für die aktuelle Sitzung zurück.  
  
```  
SELECT SESSION_USER;  
```  
  
## <a name="see-also"></a>Siehe auch  
 [ALTER TABLE &#40;Transact-SQL&#41;](../../t-sql/statements/alter-table-transact-sql.md)   
 [CREATE TABLE &#40;Transact-SQL&#41;](../../t-sql/statements/create-table-transact-sql.md)   
 [CURRENT_TIMESTAMP &#40; Transact-SQL &#41;](../../t-sql/functions/current-timestamp-transact-sql.md)   
 [CURRENT_USER &#40; Transact-SQL &#41;](../../t-sql/functions/current-user-transact-sql.md)   
 [SYSTEM_USER &#40; Transact-SQL &#41;](../../t-sql/functions/system-user-transact-sql.md)   
 [Systemfunktionen &#40;Transact-SQL&#41;](../../relational-databases/system-functions/system-functions-for-transact-sql.md)   
 [Benutzer &#40; Transact-SQL &#41;](../../t-sql/functions/user-transact-sql.md)   
 [USER_NAME &#40; Transact-SQL &#41;](../../t-sql/functions/user-name-transact-sql.md)  
  
  


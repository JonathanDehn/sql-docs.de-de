---
title: Benutzer (Transact-SQL) | Microsoft Docs
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
- USER
- USER_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- usernames [SQL Server]
- system-supplied usernames [SQL Server]
- USER function
- users [SQL Server], database names
- names [SQL Server], database users
- database usernames [SQL Server]
ms.assetid: 82bbbd94-870c-4c43-9ed9-d9abc767a6be
caps.latest.revision: 24
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 5230769c1e41d5831d77c3711c9b5c4a215414cb
ms.contentlocale: de-de
ms.lasthandoff: 09/01/2017

---
# <a name="user-transact-sql"></a>USER (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-all_md](../../includes/tsql-appliesto-ss2008-all-md.md)]

  Ermöglicht das Einfügen eines vom System bereitgestellten Werts für den Datenbankbenutzernamen des aktuellen Benutzers in eine Tabelle, wenn kein Standardwert angegeben ist.  
  
 ![Themenlinksymbol](../../database-engine/configure-windows/media/topic-link.gif "Topic link icon") [Transact-SQL Syntax Conventions (Transact-SQL-Syntaxkonventionen)](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
USER  
```  
  
## <a name="return-types"></a>Rückgabetypen  
 **char**  
  
## <a name="remarks"></a>Hinweise  
 USER bietet die gleiche Funktionalität wie die USER_NAME-Systemfunktion.  
  
 Verwenden Sie die USER-Funktion mit DEFAULT-Einschränkungen in der CREATE TABLE- oder ALTER TABLE-Anweisung oder als beliebige Standardfunktion.  
  
 USER gibt immer den Namen des aktuellen Kontexts zurück. Wenn USER nach einer EXECUTE AS-Anweisung aufgerufen wird, wird der Name des Kontexts zurückgegeben, dessen Identität angenommen wurde.  
  
 Greift ein Windows-Prinzipal über die Mitgliedschaft in einer Gruppe auf die Datenbank zu, gibt USER den Namen des Windows-Prinzipals statt des Namens der Gruppe zurück.  
  
## <a name="examples"></a>Beispiele  
  
### <a name="a-using-user-to-return-the-database-user-name"></a>A. Verwenden von USER zum Zurückgeben des Datenbankbenutzernamens  
 Im folgenden Beispiel wird eine Variable als `char`-Datentyp deklariert, ihr wird der aktuelle Wert von USER zugewiesen, und anschließend wird die Variable mit einer Textbeschreibung gedruckt.  
  
```  
DECLARE @usr char(30)  
SET @usr = user  
SELECT 'The current user''s database username is: '+ @usr  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
 `-----------------------------------------------------------------------`  
  
 `The current user's database username is: dbo`  
  
 `(1 row(s) affected)`  
  
### <a name="b-using-user-with-default-constraints"></a>B. Verwenden von USER mit DEFAULT-Einschränkungen  
 Im folgenden Beispiel wird eine Tabelle mit `USER` als `DEFAULT`-Einschränkung für den Verkäufer in einer Zeile mit Verkaufszahlen erstellt.  
  
```  
USE AdventureWorks2012;  
GO  
CREATE TABLE inventory22  
(  
 part_id int IDENTITY(100, 1) NOT NULL,  
 description varchar(30) NOT NULL,  
 entry_person varchar(30) NOT NULL DEFAULT USER   
)  
GO  
INSERT inventory22 (description)  
VALUES ('Red pencil')  
INSERT inventory22 (description)  
VALUES ('Blue pencil')  
INSERT inventory22 (description)  
VALUES ('Green pencil')  
INSERT inventory22 (description)  
VALUES ('Black pencil')  
INSERT inventory22 (description)  
VALUES ('Yellow pencil')  
GO  
```  
  
 Im Folgenden wird die Abfrage zur Auswahl aller Informationen aus der `inventory22`-Tabelle aufgeführt:  
  
```  
SELECT * FROM inventory22 ORDER BY part_id;  
GO  
```  
  
 Im Folgenden wird das Resultset aufgeführt (beachten Sie den `entry-person`-Wert):  
  
 `part_id     description                    entry_person`  
  
 `----------- ------------------------------ -------------------------`  
  
 `100         Red pencil                     dbo`  
  
 `101         Blue pencil                    dbo`  
  
 `102         Green pencil                   dbo`  
  
 `103         Black pencil                   dbo`  
  
 `104         Yellow pencil                  dbo`  
  
 `(5 row(s) affected)`  
  
### <a name="c-using-user-in-combination-with-execute-as"></a>C. Verwenden von USER in Kombination mit EXECUTE AS  
 Im folgenden Beispiel wird das Verhalten von `USER` bei Aufruf in einer Sitzung mit Identitätswechsel gezeigt.  
  
```  
SELECT USER;  
GO  
EXECUTE AS USER = 'Mario';  
GO  
SELECT USER;  
GO  
REVERT;  
GO  
SELECT USER;  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
 `DBO`  
  
 `Mario`  
  
 `DBO`  
  
## <a name="examples-includesssdwfullincludessssdwfull-mdmd-and-includesspdwincludessspdw-mdmd"></a>Beispiele: [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] und[!INCLUDE[ssPDW](../../includes/sspdw-md.md)]  
  
### <a name="d-using-user-to-return-the-database-user-name"></a>D. Verwenden von USER zum Zurückgeben des Datenbankbenutzernamens  
 Im folgenden Beispiel wird eine Variable als `char`-Datentyp deklariert, ihr wird der aktuelle Wert von USER zugewiesen, und anschließend wird die Variable mit einer Textbeschreibung gedruckt.  
  
```  
DECLARE @usr char(30)  
SET @usr = user  
SELECT 'The current user''s database username is: '+ @usr  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
 `-----------------------------------------------------------------------`  
  
 `The current user's database username is: dbo`  
  
 `(1 row(s) affected)`  
  
## <a name="see-also"></a>Siehe auch  
 [ALTER TABLE &#40;Transact-SQL&#41;](../../t-sql/statements/alter-table-transact-sql.md)   
 [CREATE TABLE &#40;Transact-SQL&#41;](../../t-sql/statements/create-table-transact-sql.md)   
 [CURRENT_TIMESTAMP &#40; Transact-SQL &#41;](../../t-sql/functions/current-timestamp-transact-sql.md)   
 [CURRENT_USER &#40; Transact-SQL &#41;](../../t-sql/functions/current-user-transact-sql.md)   
 [Sicherheitsfunktionen &#40;Transact-SQL&#41;](../../t-sql/functions/security-functions-transact-sql.md)   
 [SESSION_USER &#40; Transact-SQL &#41;](../../t-sql/functions/session-user-transact-sql.md)   
 [SYSTEM_USER &#40; Transact-SQL &#41;](../../t-sql/functions/system-user-transact-sql.md)   
 [USER_NAME &#40; Transact-SQL &#41;](../../t-sql/functions/user-name-transact-sql.md)  
  
  


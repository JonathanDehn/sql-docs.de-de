---
title: FILE_ID (Transact-SQL) | Microsoft Docs
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- FILE_ID
- FILE_ID_TSQL
dev_langs:
- TSQL
helpviewer_keywords:
- IDs [SQL Server], files
- file IDs [SQL Server]
- FILE_ID function
- names [SQL Server], files
- identification numbers [SQL Server], files
- file names [SQL Server], FILE_ID
ms.assetid: 6a7382cf-a360-4d62-b9d2-5d747f56f076
caps.latest.revision: 34
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 2544da5cb252b27f42a82e1fa400d7c28f503f20
ms.contentlocale: de-de
ms.lasthandoff: 09/01/2017

---
# <a name="fileid-transact-sql"></a>FILE_ID (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx_md](../../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Gibt die Datei-ID für den angegebenen logischen Dateinamen in der aktuellen Datenbank zurück.  
  
> [!IMPORTANT]  
>  [!INCLUDE[ssNoteDepFutureAvoid](../../includes/ssnotedepfutureavoid-md.md)]Verwendung [FILE_IDEX](../../t-sql/functions/file-idex-transact-sql.md) stattdessen.  
  
 ![Themenlinksymbol](../../database-engine/configure-windows/media/topic-link.gif "Topic link icon") [Transact-SQL Syntax Conventions (Transact-SQL-Syntaxkonventionen)](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)  
  
## <a name="syntax"></a>Syntax  
  
```  
  
FILE_ID ( file_name )  
```  
  
## <a name="arguments"></a>Argumente  
 *Dateiname*  
 Ist ein Ausdruck vom Typ **Sysname** , die den Namen der Datei, für die die Datei-ID zurückgegeben darstellt  
  
## <a name="return-types"></a>Rückgabetypen  
 **smallint**  
  
## <a name="remarks"></a>Hinweise  
 *File_name* entspricht dem logischen Dateinamen in der Spalte "Name" in den Katalogsichten Sys. master_files oder Sys. database_files angezeigt.  
  
 In [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] ist die Volltextkatalogen zugewiesene Dateikennzeichnungsnummer größer als 32767. Da der Rückgabetyp der FILE_ID-Funktion ist **"smallint"**, diese Funktion kann nicht für volltextdateien verwendet werden. Verwendung [FILE_IDEX](../../t-sql/functions/file-idex-transact-sql.md) stattdessen.  
  
## <a name="examples"></a>Beispiele  
 Im folgenden Beispiel wird die Datei-ID für die Datei `AdventureWorks_Data` zurückgegeben.  
  
```tsql  
USE AdventureWorks2012;  
GO  
SELECT FILE_ID('AdventureWorks2012_Data')AS 'File ID';  
GO  
```  
  
 [!INCLUDE[ssResult](../../includes/ssresult-md.md)]  
  
```  
File ID   
-------   
1  
(1 row(s) affected)  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Als veraltet markierte Funktionen des Datenbankmoduls in SQL Server 2016](../../database-engine/deprecated-database-engine-features-in-sql-server-2016.md)   
 [File_name &#40; Transact-SQL &#41;](../../t-sql/functions/file-name-transact-sql.md)   
 [Metadatenfunktionen &#40; Transact-SQL &#41;](../../t-sql/functions/metadata-functions-transact-sql.md)   
 [sys.database_files &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-database-files-transact-sql.md)   
 [sys.master_files &#40;Transact-SQL&#41;](../../relational-databases/system-catalog-views/sys-master-files-transact-sql.md)  
  
  
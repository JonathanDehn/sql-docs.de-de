---
title: DATEFROMPARTS (Transact-SQL) | Microsoft Docs
ms.custom: 
ms.date: 07/29/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- DATEFROMPARTS_TSQL
- DATEFROMPARTS
dev_langs:
- TSQL
helpviewer_keywords:
- DATEFROMPARTS function
ms.assetid: 5b885376-87aa-41f1-9e18-04987aead250
caps.latest.revision: 16
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 876522142756bca05416a1afff3cf10467f4c7f1
ms.openlocfilehash: 3365c40b5bc4fb57a8e09cc97e706a16fbd709ec
ms.contentlocale: de-de
ms.lasthandoff: 09/01/2017

---
# <a name="datefromparts-transact-sql"></a>DATEFROMPARTS (Transact-SQL)
[!INCLUDE[tsql-appliesto-ss2012-all_md](../../includes/tsql-appliesto-ss2012-all-md.md)]

Gibt eine **Datum** Wert für den angegebenen Werten für Jahr, Monat und Tag.
  
![Themenlinksymbol](../../database-engine/configure-windows/media/topic-link.gif "Topic link icon") [Transact-SQL Syntax Conventions (Transact-SQL-Syntaxkonventionen)](../../t-sql/language-elements/transact-sql-syntax-conventions-transact-sql.md)
  
## <a name="syntax"></a>Syntax  
  
```sql
DATEFROMPARTS ( year, month, day )  
```  
  
## <a name="arguments"></a>Argumente  
*Jahr*  
Ganzzahliger Ausdruck, der ein Jahr angibt.
  
*Monat*  
Ganzzahliger Ausdruck, der einen Monat angibt (von 1 bis 12).
  
*Tag*  
Ganzzahliger Ausdruck, der einen Tag angibt.
  
## <a name="return-types"></a>Rückgabetypen
**Datum**
  
## <a name="remarks"></a>Hinweise  
**DATEFROMPARTS** gibt eine **Datum** Wert mit den Datumsteil legen Sie auf den angegebenen Werten für Jahr, Monat und Tag und den Zeitbereich, der auf den Standardwert festgelegt. Wenn die Argumente nicht gültig sind, wird ein Fehler ausgelöst. Wenn erforderliche Argumente den Wert NULL haben, wird NULL zurückgegeben.
  
Diese Funktion kann remote auf [!INCLUDE[ssSQL11](../../includes/sssql11-md.md)]-Servern oder höher ausgeführt werden. Eine Remoteausführung auf Servern mit einer Version unter [!INCLUDE[ssSQL11](../../includes/sssql11-md.md)] ist nicht möglich.
  
## <a name="examples"></a>Beispiele  
Das folgende Beispiel veranschaulicht die **DATEFROMPARTS** Funktion.
  
```sql
SELECT DATEFROMPARTS ( 2010, 12, 31 ) AS Result;  
```  
  
[!INCLUDE[ssResult](../../includes/ssresult-md.md)]
  
```sql
Result  
----------------------------------  
2010-12-31  
  
(1 row(s) affected)  
```  
  
## <a name="examples-includesssdwfullincludessssdwfull-mdmd-and-includesspdwincludessspdw-mdmd"></a>Beispiele: [!INCLUDE[ssSDWfull](../../includes/sssdwfull-md.md)] und[!INCLUDE[ssPDW](../../includes/sspdw-md.md)]  
Das folgende Beispiel veranschaulicht die **DATEFROMPARTS** Funktion.
  
```sql
SELECT DATEFROMPARTS ( 2010, 12, 31 ) AS Result;  
```  
  
[!INCLUDE[ssResult](../../includes/ssresult-md.md)]
  
```sql
Result  
----------------------------------  
2010-12-31  
  
(1 row(s) affected)  
```  
  
## <a name="see-also"></a>Siehe auch
[date &#40;Transact-SQL&#41;](../../t-sql/data-types/date-transact-sql.md)
  
  


---
title: Erstellen von Volltextsuchabfragen (Visual Database Tools) | Microsoft-Dokumentation
ms.custom: 
ms.date: 01/19/2017
ms.prod: sql-non-specified
ms.reviewer: 
ms.suite: 
ms.technology:
- tools-ssms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- CONTAINS predicate (Transact-SQL)
- queries [full-text search], creating
- full-text queries [SQL Server], creating
ms.assetid: 537fa556-390e-4c88-9b8e-679848d94abc
caps.latest.revision: 5
author: stevestein
ms.author: sstein
manager: jhubbard
translationtype: Human Translation
ms.sourcegitcommit: 2edcce51c6822a89151c3c3c76fbaacb5edd54f4
ms.openlocfilehash: 3c7f13f234c595c494e22a1bb0888899a40df51b
ms.lasthandoff: 04/11/2017

---
# <a name="create-full-text-search-queries-visual-database-tools"></a>Erstellen von Volltextsuchabfragen (Visual Database Tools)
In Volltextsuchen werden mit dem CONTAINS-Prädikat Zeilen gefunden, die in einer bestimmten Spalte den angegebenen Text enthalten. Volltextsuchen sind nur bei Spalten möglich, die aktive Volltextindizes haben. Wenn Sie versuchen, die CONTAINS-Klausel in einer Spalte zu verwenden, für die es zurzeit keinen aktiven Volltextindex gibt, wird ein Fehler angezeigt. Weitere Informationen zu Volltextindizes und der CONTAINS-Klausel finden Sie unter [Volltextsuche (SQL Server)](http://msdn.microsoft.com/en-us/a0ce315d-f96d-4e5d-b4eb-ff76811cab75) und [CONTAINS (Transact-SQL)](http://msdn.microsoft.com/en-us/996c72fc-b1ab-4c96-bd12-946be9c18f84).  
  
### <a name="to-create-a-full-text-search-query"></a>So erstellen Sie eine Volltextsuchabfrage  
  
1.  Öffnen Sie im Projektmappen-Explorer eine Abfrage, oder erstellen Sie eine neue Abfrage.  
  
2.  Verwenden Sie in der WHERE-Klausel der Abfrage die CONTAINS-Funktion, um eine Volltextspalte zu durchsuchen.  
  
## <a name="see-also"></a>Siehe auch  
[Unterstützte Abfragetypen &amp;#40;Visual Database Tools&amp;#41;](../../ssms/visual-db-tools/supported-query-types-visual-database-tools.md)  
[Themen zur Vorgehensweise: Entwerfen von Abfragen und Sichten &amp;#40;Visual Database Tools&amp;#41;](../../ssms/visual-db-tools/design-queries-and-views-how-to-topics-visual-database-tools.md)  
[Ausführen grundlegender Vorgänge mit Abfragen &amp;#40;Visual Database Tools&amp;#41;](../../ssms/visual-db-tools/perform-basic-operations-with-queries-visual-database-tools.md)  
  

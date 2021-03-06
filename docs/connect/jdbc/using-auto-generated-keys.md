---
title: Verwenden von automatisch generierten Schlüsseln | Microsoft Docs
ms.custom: ''
ms.date: 01/19/2017
ms.prod: sql
ms.prod_service: connectivity
ms.reviewer: ''
ms.suite: sql
ms.technology: connectivity
ms.tgt_pltfrm: ''
ms.topic: conceptual
ms.assetid: 55a062c7-45ce-40e3-9a6f-4a0f4da4e2a6
caps.latest.revision: 18
author: MightyPen
ms.author: genemi
manager: craigg
ms.openlocfilehash: be2799c9d1b4eae52dc2ede364b88099175f1adf
ms.sourcegitcommit: 1740f3090b168c0e809611a7aa6fd514075616bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="using-auto-generated-keys"></a>Verwenden von automatisch generierten Schlüsseln
[!INCLUDE[Driver_JDBC_Download](../../includes/driver_jdbc_download.md)]

  Die [!INCLUDE[jdbcNoVersion](../../includes/jdbcnoversion_md.md)] unterstützt die optionalen JDBC 3.0-APIs für das Abrufen automatisch generierter Zeilen-IDs. Der Hauptwert dieser Funktion besteht darin, eine Möglichkeit zu bieten, IDENTITY-Werte einer Anwendung zur Verfügung zu stellen, die eine Datenbanktabelle aktualisiert, ohne dass eine Abfrage und ein zweiter Roundtrip zum Server notwendig sind.  
  
 Da [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] unterstützt keine Pseudospalten der Unterstützung für den Bezeichner, Updates, die die automatisch generierten Schlüssel-Funktion verwenden, müssen ausgeführt werden, für eine Tabelle, die eine Identitätsspalte enthält. [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] können nur eine einzelne Identitätsspalte pro Tabelle. Das Resultset zurückgegebenes [GetGeneratedKeys](../../connect/jdbc/reference/getgeneratedkeys-method-sqlserverstatement.md) Methode der [SQLServerStatement](../../connect/jdbc/reference/sqlserverstatement-class.md) -Klasse hat nur eine Spalte mit dem Namen generated_keys. Wenn generierte Schlüssel für eine Tabelle ohne IDENTITY-Spalte angefordert werden, gibt der JDBC-Treiber ein leeres Resultset zurück.  
  
 Erstellen Sie beispielsweise die folgende Tabelle in der [!INCLUDE[ssSampleDBnormal](../../includes/sssampledbnormal_md.md)] -Beispieldatenbank:  
  
```  
CREATE TABLE TestTable   
   (Col1 int IDENTITY,   
    Col2 varchar(50),   
    Col3 int);  
```  
  
 Im folgenden Beispiel wird eine offene Verbindung mit dem [!INCLUDE[ssSampleDBnormal](../../includes/sssampledbnormal_md.md)] -Beispieldatenbank an die Funktion übergeben, eine SQL­Anweisung erstellt, die Daten der Tabelle hinzugefügt und die Anweisung wird ausgeführt, und der Wert der IDENTITY-Spalte wird angezeigt.  
  
 [!code[JDBC#UsingAutoGeneratedKeys1](../../connect/jdbc/codesnippet/Java/using-auto-generated-keys_1.java)]  
  
## <a name="see-also"></a>Siehe auch  
 [Verwenden von Anweisungen mit dem JDBC-Treiber](../../connect/jdbc/using-statements-with-the-jdbc-driver.md)  
  
  

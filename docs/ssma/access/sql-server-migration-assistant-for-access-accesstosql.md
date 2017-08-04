---
title: "SQL Server Migration Assistant für Access (AccessToSQL) | Microsoft Docs"
ms.prod: sql-non-specified
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.technology:
- sql-ssma
ms.tgt_pltfrm: 
ms.topic: article
applies_to:
- Azure SQL Database
- SQL Server
ms.assetid: 40c1eb02-26b2-44ba-969d-6c430c61c281
caps.latest.revision: 22
author: sabotta
ms.author: carlasab
manager: lonnyb
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: eabbda81defc597d99b82a928a1ca69baedb6328
ms.contentlocale: de-de
ms.lasthandoff: 08/02/2017

---
# <a name="sql-server-migration-assistant-for-access-accesstosql"></a>SQL Server Migration Assistant für Access (AccessToSQL)
[!INCLUDE[msCoName](../../includes/msconame_md.md)][!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] Migration Assistant (SSMA) for Access ist ein Tool zur Migration von Datenbanken von [!INCLUDE[msCoName](../../includes/msconame_md.md)] Zugriff auf die Versionen 97 bis 2010 [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] 2005 / [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] 2008 / [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] 2012 / [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] 2014 / [!INCLUDE[msCoName](../../includes/msconame_md.md)] [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] 2016 / [!INCLUDE[msCoName](../../includes/msconame_md.md)] SQL Azure. SSMA für Access konvertiert den Zugriff auf Datenbankobjekte zu [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] oder SQL Azure-Datenbankobjekte, lädt die Objekte in [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] oder SQL Azure, und klicken Sie dann Migrieren von Daten aus den Zugriff auf [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] oder SQL Azure.  
  
In dieser Dokumentation erläutert die SSMA für Access, enthält schrittweise Anleitungen zum Migrieren von Access-Datenbanken zu [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] oder SQL Azure, und enthält Informationen zu Problemen, die nach der Migration auftreten können.  
  
## <a name="contents"></a>Inhalt  
  
|Abschnitt|Description|  
|-----------|---------------|  
|[Was ist neu in SSMA für Access](http://msdn.microsoft.com/en-us/a24d3fc0-6911-4bfa-828a-197abf222e02)|Listet die Änderungen an SSMA-Versionen.|  
|[Installieren von SQL Server Migration Assistant für Access](http://msdn.microsoft.com/en-us/dd50eebd-75df-4e0d-8c4d-88b511aae4c7)|Enthält Informationen zu den Voraussetzungen für die Installation von SSMA das Verfahren zum Installieren und lizenzieren SSMA und einen Link auf die neueste Version.|  
|[Erste Schritte mit SQL Server Migration Assistant für Access & #40; AccessToSQL & #41;](../../ssma/access/getting-started-with-sql-server-migration-assistant-for-access-accesstosql.md)|Führt SSMA und seine Benutzeroberfläche.|  
|[Access-Datenbanken vorbereitet für die Migration.](http://msdn.microsoft.com/en-us/9b80a9e0-08e7-4b4d-b5ec-cc998d3f5114)|Beschreibt, wie die Access-Datenbanken für die Konvertierung in Vorbereiten [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)] SQL Azure.|  
|[Migrieren von Access-Datenbanken zu SQLServer](http://msdn.microsoft.com/en-us/76a3abcf-2998-4712-9490-fe8d872c89ca)|Bietet eine Übersicht über den Konvertierungsprozess und detaillierte Informationen zu jedem Schritt im Prozess an.|  
|[Verknüpfen von Access-Anwendungen mit SQLServer](http://msdn.microsoft.com/en-us/82374ad2-7737-4164-a489-13261ba393d4)|Beschreibt, wie die vorhandenen Access-Anwendungen mit [!INCLUDE[ssNoVersion](../../includes/ssnoversion_md.md)].|  
|[Referenz zur Benutzeroberfläche](http://msdn.microsoft.com/en-us/af24c303-4a41-449b-9c86-d6558a97e839)|Enthält die Dokumentation für SSMA-Dialogfelder.|  
|[Arbeiten mit SSMA für Access-Konsole](http://msdn.microsoft.com/en-us/ef94e843-9f88-45a2-86c4-a0af268738c4)|Dokumentation für die SSMA-Konsolenanwendung enthalten|  
|[Informationsquellen für SSMA für Access](http://go.microsoft.com/fwlink/?LinkID=708538&clcid=0x409)|Enthält Informationen über die zusätzliche Informationsquellen.|  
  

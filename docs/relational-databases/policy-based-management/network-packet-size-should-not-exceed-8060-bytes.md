---
title: "Netzwerkpaketgröße darf 8060 Bytes nicht überschreiten | Microsoft-Dokumentation"
ms.custom: 
ms.date: 03/14/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- database-engine
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Best Practices [Database Engine]
ms.assetid: 86db5da1-afe4-4fbb-8bf8-33cedc7e4361
caps.latest.revision: 8
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.translationtype: Human Translation
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: cb2e255e501d739ddfe8f822c7c62b212aa14db8
ms.contentlocale: de-de
ms.lasthandoff: 06/22/2017

---
# <a name="network-packet-size-should-not-exceed-8060-bytes"></a>Netzwerkpaketgröße darf 8060 Bytes nicht überschreiten
  Wenn der für sp_configure 'Netzwerkpaketgröße' angegebene Wert oder die Netzwerkpaketgröße eines angemeldeten Benutzers 8060 Bytes überschreitet, führt [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] verschiedene Speicherbelegungsvorgänge aus. Dies kann zu einer Zunahme des virtuellen Adressraums führen, der nicht für den Pufferpool reserviert ist.  
  
## <a name="best-practices-recommendations"></a>Empfehlungen zu Best Practices  
 Die Netzwerkpaketgröße sollte 8060 Bytes nicht überschreiten.  
  
## <a name="for-more-information"></a>Weitere Informationen  
 [Microsoft Knowledge Base-Artikel 903002](http://go.microsoft.com/fwlink/?linkid=117749)  
  
## <a name="see-also"></a>Siehe auch  
 [Überwachen und Erzwingen von Best Practices mit der richtlinienbasierten Verwaltung](../../relational-databases/policy-based-management/monitor-and-enforce-best-practices-by-using-policy-based-management.md)  
  
  
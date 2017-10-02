---
title: Anbietereigenschaft (ADO) | Microsoft Docs
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
apitype: COM
f1_keywords:
- Connection15::get_Provider
- Connection15::PutProvider
- Connection15::put_Provider
- Connection15::GetProvider
- Connection15::Provider
helpviewer_keywords:
- Provider property [ADO]
ms.assetid: 0ff70e72-0061-4ffc-90fb-e3ea23129bb2
caps.latest.revision: 11
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 1839d8bc9c954d3f5ceeafca2b604304801f643f
ms.contentlocale: de-de
ms.lasthandoff: 09/09/2017

---
# <a name="provider-property-ado"></a>Anbietereigenschaft (ADO)
Gibt den Namen des Anbieters für einen [Verbindung](../../../ado/reference/ado-api/connection-object-ado.md) Objekt.  
  
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte  
 Legt fest oder gibt einen **Zeichenfolge** Wert, der Name des Anbieters angibt.  
  
## <a name="remarks"></a>Hinweise  
 Verwenden der **Anbieter** Eigenschaft so festlegen oder den Namen des Anbieters für eine Verbindung zurückgeben. Diese Eigenschaft kann auch festgelegt werden, durch den Inhalt der der ["ConnectionString"](../../../ado/reference/ado-api/connectionstring-property-ado.md) Eigenschaft oder die *"ConnectionString"* Argument der [öffnen](../../../ado/reference/ado-api/open-method-ado-connection.md) Methode; allerdings angeben eines Anbieters in mehreren Orten beim Aufrufen der **öffnen** Methode kann unvorhersehbare Folgen haben. Wenn kein Anbieter angegeben wird, wird die Eigenschaft MSDASQL standardmäßig ([Microsoft OLE DB-Anbieter für ODBC](../../../ado/guide/appendixes/microsoft-ole-db-provider-for-odbc.md)).  
  
 Die **Anbieter** Eigenschaft ist Lese-/Schreibzugriff auf, wenn die Verbindung ist geschlossen und Read-only, wenn er geöffnet ist. Die Einstellung wird wirksam, bis Sie öffnen Sie entweder die **Verbindung** Objekt oder den Zugriff der [Eigenschaften](../../../ado/reference/ado-api/properties-collection-ado.md) Auflistung von der **Verbindung** Objekt. Wenn die Einstellung nicht gültig ist, tritt ein Fehler auf.  
  
## <a name="applies-to"></a>Gilt für  
 [Verbindungsobjekt (ADO)](../../../ado/reference/ado-api/connection-object-ado.md)  
  
## <a name="see-also"></a>Siehe auch  
 [Anbieter und DefaultDatabase-Eigenschaften-Beispiel (VB)](../../../ado/reference/ado-api/provider-and-defaultdatabase-properties-example-vb.md)   
 [Anbieter und DefaultDatabase-Eigenschaften-Beispiel (VB)](../../../ado/reference/ado-api/provider-and-defaultdatabase-properties-example-vb.md)   
 [Microsoft OLE DB-Anbieter für ODBC](../../../ado/guide/appendixes/microsoft-ole-db-provider-for-odbc.md)   
 [Anhang A: Anbieter](../../../ado/guide/appendixes/appendix-a-providers.md)

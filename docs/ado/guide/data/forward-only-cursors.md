---
title: "Vorwärtscursor | Microsoft Docs"
ms.prod: sql-non-specified
ms.technology:
- drivers
ms.custom: 
ms.date: 01/19/2017
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- cursors [ADO], forward-only
- forward-only cursors [ADO]
ms.assetid: 2b1e062f-3294-4a6f-8241-a17045c4df18
caps.latest.revision: 5
author: MightyPen
ms.author: genemi
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f7e6274d77a9cdd4de6cbcaef559ca99f77b3608
ms.openlocfilehash: 121e8eec0b95f66b6e034f1f77d78c7d88fd5184
ms.contentlocale: de-de
ms.lasthandoff: 09/09/2017

---
# <a name="forward-only-cursors"></a>Vorwärtscursor
Der übliche Standardnamespace Cursortyp, bezeichnet einen Cursor Vorwärtscursor (oder nicht scrollfähige) kann über das Resultset nur vorwärts bewegen. Ein Vorwärtscursor unterstützt keine Bildläufe (die Möglichkeit, im Resultset vorwärts und rückwärts zu bewegen); Es unterstützt nur das Abrufen von Zeilen vom Anfang bis zum Ende des Resultsets. Mit einigen Vorwärtscursor (z. B. mit der SQL Server-Cursorbibliothek), werden alle INSERT-, Update- und Delete-Anweisungen, die aktuelle Benutzer (oder anderer Benutzer ausgeführt werden), dass Zeilen im Resultset auswirken angezeigt werden, wenn die Zeilen abgerufen werden. Da sich der Cursor nicht rückwärts gescrollt werden kann, sind jedoch Änderungen an Zeilen in der Datenbank vorgenommen wurden, nachdem die jeweilige Zeile abgerufen wurde nicht über den Cursor sichtbar.  
  
 Nachdem die Daten für die aktuelle Zeile verarbeitet wurde, werden die Ressourcen, die zum Speichern dieser Daten verwendet wurden von der Vorwärtscursor frei. Vorwärtscursor sind dynamisch, was bedeutet, dass alle Änderungen erkannt werden, bei der Verarbeitung der aktuellen Zeile in der Standardeinstellung. Dies bietet schnellere Cursor öffnende und ermöglicht die Resultsets an den zugrunde liegenden Tabellen vorgenommenen Updates anzuzeigen.  
  
 Während Vorwärtscursor rückwärts-scrollen nicht unterstützt werden, kann Ihre Anwendung auf den Anfang des Resultsets durch Schließen und erneutes Öffnen des Cursors zurück. Dies ist eine effektive Möglichkeit für kleine Mengen von Daten arbeiten. Als Alternative können konnte die Anwendung das Resultset einmal gelesen, die Daten lokal zwischengespeichert und navigieren Sie dann auf den lokalen Datencache.  
  
 Wenn Ihre Anwendung einen Bildlauf durch das Resultset nicht erforderlich ist, ist der Vorwärtscursor die beste Möglichkeit zum Abrufen von Daten schnell und mit minimalem Aufwand. Verwenden Sie die **AdOpenForwardOnly CursorTypeEnum** um anzugeben, dass Sie einen Vorwärtscursor in ADO verwenden möchten.  
  
## <a name="see-also"></a>Siehe auch  
 [Statische Cursor](../../../ado/guide/data/static-cursors.md)   
 [KEYSET-Cursor](../../../ado/guide/data/keyset-cursors.md)   
 [Dynamische Cursor](../../../ado/guide/data/dynamic-cursors.md)
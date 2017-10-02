---
title: "Neuanordnen von Spalten (MDS-Add-In für Excel) | Microsoft-Dokumentation"
ms.custom: 
ms.date: 03/01/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- master-data-services
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: ac00462e-c0f7-4b8d-86f2-d9eda2598a15
caps.latest.revision: 7
author: smartysanthosh
ms.author: nagavo
manager: craigg
ms.translationtype: HT
ms.sourcegitcommit: 0b832a9306244210e693bde7c476269455e9b6d8
ms.openlocfilehash: fe262e2c5ad6a0a5853868ce0cc2f89284d6ea8c
ms.contentlocale: de-de
ms.lasthandoff: 09/07/2017

---
# <a name="reorder-columns-mds-add-in-for-excel"></a>Neuanordnen von Spalten (MDS-Add-In für Excel)
  In [!INCLUDE[ssMDSshort](../../includes/ssmdsshort-md.md)][!INCLUDE[ssMDSXLS](../../includes/ssmdsxls-md.md)]können Sie Spalten durch das Filtern der Liste vor dem Laden neu anordnen.  
  
 Wenn Sie Attribute im Dialogfeld **Filter** neu anordnen, werden die Daten mit der neuen Reihenfolge in Excel geladen. Wenn Sie jedoch die Attributdaten das nächste Mal filtern, wird die Reihenfolge des ursprünglichen Entwurfs wiederhergestellt. Um die Reihenfolge permanent zu ändern, sollte ein Administrator die Reihenfolge im Bereich **Systemverwaltung** von Master Data Manager ändern. Weitere Informationen finden Sie unter [Change the Order of Attributes](../../master-data-services/change-the-order-of-attributes.md).  
  
## <a name="prerequisites"></a>Erforderliche Komponenten  
 So führen Sie diese Prozedur aus  
  
-   Sie müssen über die Berechtigung für den Zugriff auf den Funktionsbereich **Explorer** verfügen.  
  
### <a name="to-reorder-mds-managed-columns"></a>So ordnen Sie von MDS verwaltete Spalten neu an  
  
1.  Öffnen Sie Excel, und stellen Sie auf der Registerkarte **Masterdaten** eine Verbindung mit einem MDS-Repository her. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit einem MDS-Repository &#40;MDS-Add-In für Excel&#41;](../../master-data-services/microsoft-excel-add-in/connect-to-an-mds-repository-mds-add-in-for-excel.md).  
  
2.  Wählen Sie im Bereich **Master Data Explorer** ein Modell und eine Version aus. Die Liste der Entitäten wird aufgefüllt.  
  
    -   Wenn der Bereich **Master Data Explorer** nicht sichtbar ist, klicken Sie in der Gruppe **Verbinden und Laden** auf **Explorer anzeigen**.  
  
    -   Wenn der Bereich **Master Data Explorer** deaktiviert ist, liegt dies daran, dass das vorhandene Blatt bereits von MDS verwaltete Daten enthält. Um den Bereich zu aktivieren, öffnen Sie ein neues Arbeitsblatt.  
  
3.  Klicken Sie im Bereich **Master Data Explorer** auf eine Entität.  
  
4.  Klicken Sie in der Gruppe **Verbinden und Laden** auf **Filtern**.  
  
5.  Klicken Sie im Dialogfeld **Filtern** im Abschnitt **Spalten** in der Liste der Attribute auf das Attribut, das Sie bewegen möchten.  
  
6.  Klicken Sie rechts von der Liste auf den **Nach oben** - oder **Nach unten** -Pfeil, um das Attribut im Arbeitsblatt nach links und rechts zu verschieben.  
  
7.  Wiederholen Sie Schritt 7 für jedes Attribut, bis die Reihenfolge von oben nach unten die Reihenfolge von links nach rechts darstellt, die Sie im Arbeitsblatt wünschen.  
  
8.  Klicken Sie auf **Daten laden**. Das Blatt wird mit von MDS verwalteten Daten aufgefüllt, und die Spalten werden in der angegebenen Reihenfolge angezeigt.  
  
## <a name="see-also"></a>Siehe auch  
 [Overview: Exporting Data to Excel &#40;MDS Add-in for Excel&#41; (Übersicht: Exportieren von Daten nach Excel (MDS-Add-in für Excel))](../../master-data-services/microsoft-excel-add-in/overview-exporting-data-to-excel-mds-add-in-for-excel.md)  
  
  
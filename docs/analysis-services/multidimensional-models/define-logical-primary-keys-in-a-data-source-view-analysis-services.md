---
title: Definieren logischer Primärschlüssel in einer Datenquellensicht (Analysis Services) | Microsoft Docs
ms.date: 05/02/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: multidimensional-models
ms.topic: conceptual
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: 90684f55414fa9e3f0d68a8ec90884fdae4d2c0a
ms.sourcegitcommit: c12a7416d1996a3bcce3ebf4a3c9abe61b02fb9e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2018
---
# <a name="define-logical-primary-keys-in-a-data-source-view-analysis-services"></a>Definieren logischer Primärschlüssel in einer Datenquellensicht (Analysis Services)
[!INCLUDE[ssas-appliesto-sqlas](../../includes/ssas-appliesto-sqlas.md)]
  Der Datenquellensicht-Assistent und der Datenquellensicht-Designer definieren automatisch einen Primärschlüssel für eine Tabelle, die einer Datenquellensicht basierend auf der zugrunde liegenden Datenbanktabelle hinzugefügt wird.  
  
 Es kann jedoch zeitweise erforderlich sein, einen Primärschlüssel manuell in der Datenquellensicht zu definieren. Aus Leistungs- oder Entwurfsgründen haben Tabellen in einer Datenquelle z. B. möglicherweise keine explizit definierten Primärschlüsselspalten. In benannten Abfragen und Sichten kann die Primärschlüsselspalte einer Tabelle ebenfalls fehlen. Wenn für eine Tabelle, Sicht oder benannte Abfrage kein physischer Primärschlüssel definiert ist, können Sie im Datenquellensicht-Designer manuell einen logischen Primärschlüssel für die Tabelle, Sicht oder benannte Abfrage definieren.  
  
## <a name="set-a-logical-primary-key"></a>Festlegen eines logischen Primärschlüssels  
 Primärschlüssel werden in [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] benötigt, um Datensätze in Tabellen eindeutig zu identifizieren, um Schlüsselspalten in Dimensionstabellen zu identifizieren und um Beziehungen zwischen Tabellen, Sichten und benannten Abfragen zu unterstützen. Diese Beziehungen werden verwendet, um Abfragen zum Abrufen von Daten und Metadaten aus zugrunde liegenden Datenquellen zu erstellen und um erweiterte Business Intelligence-Funktionen zu nutzen.  
  
 Jede Spalte kann für den logischen Primärschlüssel verwendet werden, einschließlich einer benannten Berechnung. Wenn Sie einen logischen Primärschlüssel erstellen, wird eine eindeutige Einschränkung in der Datenquellensicht erstellt und als Primärschlüsseleinschränkung markiert. Jeder andere in der ausgewählten Tabelle festgelegte, vorhandene logische Primärschlüssel wird gelöscht.  
  
1.  Öffnen Sie in [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)]das Projekt, oder stellen Sie eine Verbindung mit der Datenbank her, das bzw. die die Datenquellensicht enthält, in der Sie einen logischen Primärschlüssel festlegen möchten.  
  
2.  Erweitern Sie im Projektmappen-Explorer den Ordner **Datenquellensichten** und doppelklicken Sie anschließend auf die Datenquellensicht.  
  
     Um nach einer Tabelle oder Sicht zu suchen, können Sie die Option **Tabelle suchen** verwenden, indem Sie entweder auf das Menü **Datenquellensicht**  klicken oder mit der rechten Maustaste auf einen offenen Bereich im Bereich **Tabellen** oder **Diagramm** klicken.  
  
3.  Klicken Sie im Bereich **Tabellen** oder **Diagramm** mit der rechten Maustaste auf die Spalte(n), mit denen Sie einen logischen Primärschlüssel definierten möchten, und klicken Sie anschließend auf **Logischen Primärschlüssel festlegen**.  
  
     Die Option zum Festlegen eines logischen Primärschlüssels steht nur für Tabellen zur Verfügung, die keinen Primärschlüssel aufweisen.  
  
     Beachten Sie, dass die Primärschlüsselspalten nach dem Festlegen des Schlüssels mit einem Schlüsselsymbol gekennzeichnet sind.  
  
## <a name="see-also"></a>Siehe auch  
 [Datenquellsichten in mehrdimensionalen Modellen](../../analysis-services/multidimensional-models/data-source-views-in-multidimensional-models.md)   
 [Definieren von benannten Berechnungen in einer Datenquellensicht & #40; Analysis Services & #41;](../../analysis-services/multidimensional-models/define-named-calculations-in-a-data-source-view-analysis-services.md)  
  
  

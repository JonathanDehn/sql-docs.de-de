---
title: "Veröffentlichungsinformationen, Agents (Transaktionsveröffentlichung) | Microsoft-Dokumentation"
ms.custom: 
ms.date: 03/07/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- replication
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- sql13.rep.monitor.publicationinfo.downlevelagents.tran.f1
ms.assetid: 38ef2f54-53bb-4053-876d-86f8f06a4519
caps.latest.revision: 23
author: BYHAM
ms.author: rickbyh
manager: jhubbard
ms.translationtype: Human Translation
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: a1e666793719f1a277fffe23d02d4a6630585f61
ms.contentlocale: de-de
ms.lasthandoff: 06/22/2017

---
# <a name="publication-information-agents-transactional-publication"></a>Veröffentlichungsinformationen, Agents (Transaktionsveröffentlichung)
  Auf der Registerkarte **Agents** werden Zusammenfassungsinformationen zu den Agents für die ausgewählte Veröffentlichung angezeigt. Die Informationen auf dem Momentaufnahme-Agent und dem Protokolllese-Agent werden für alle Transaktionsveröffentlichungen angezeigt. Die Informationen auf dem Warteschlangenlese-Agent werden für solche Transaktionsveröffentlichungen, die für Abonnements mit verzögertem Update über eine Warteschlange verfügbar sind.  
  
## <a name="options"></a>Optionen  
 Ausführliche Informationen und eine Liste der Aufträge für einen Agent können Sie anzeigen, indem Sie mit der rechten Maustaste in die Zeile des jeweiligen Agents klicken und ein Kontextmenü auswählen. Wenn Sie die Anzeige der Daten im Raster ändern möchten, klicken Sie mit der rechten Maustaste auf das Raster, und klicken Sie anschließend auf eine der folgenden Optionen:  
  
-   **Sortieren**: Sortieren Sie nach einer oder mehreren Spalten im Dialogfeld **Spalten sortieren** .  
  
-   **Anzuzeigende Spalten auswählen**: Wählen Sie die anzuzeigenden Spalten sowie die Reihenfolge aus, in der diese im Dialogfeld **Spalten auswählen** angezeigt werden sollen.  
  
-   **Filtern**: Filtern Sie Zeilen im Raster auf Grundlage der Spaltenwerte im Dialogfeld **Filtereinstellungen** .  
  
-   **Filter löschen**: Löschen Sie alle Filtereinstellungen für das Raster.  
  
 Filtereinstellungen sind rasterspezifisch. Die Spaltenauswahl und -sortierung wird auf alle Raster desselben Typs angewendet, z. B. das Veröffentlichungsraster für jeden Verleger.  
  
 **Status**  
 Die Status der einzelnen Replikations-Agents, die der Veröffentlichung zugeordnet sind. In der folgenden Liste sind die möglichen Statuswerte aufgeführt:  
  
-   Fehler  
  
-   Fehlgeschlagener Befehl wird wiederholt  
  
-   Wird nicht ausgeführt  
  
-   Wird ausgeführt  
  
-   Abgeschlossen  
  
 **Agent**  
 Die Namen der einzelnen Replikations-Agents, die der Veröffentlichung zugeordnet sind. Der Verteilungs-Agent ist den Abonnements dieser Veröffentlichung zugeordnet. Weitere Informationen finden Sie unter [Anzeigen von Informationen und Ausführen von Aufgaben für die einem Abonnement zugeordneten Agent &#40;Replication Monitor&#41;](../../relational-databases/replication/monitor/view-information-and-perform-tasks-for-subscription-agents.md).  
  
 **Letzte Startzeit**  
 Zeitpunkt, zu dem der Agent zuletzt gestartet wurde.  
  
 **Dauer**  
 Zeitdauer, für die der Agent ausgeführt wurde. Dieser Wert gibt entweder die verstrichene Zeit eines zurzeit ausgeführten Agents oder die Gesamtzeit des zuvor ausgeführten Agents an.  
  
 **Letzte Aktion**  
 Die letzte Aktion, die bei der letzten Ausführung des Agents ausgeführt wurde.  
  
## <a name="see-also"></a>Siehe auch  
 [Starten des Replikationsmonitors](../../relational-databases/replication/monitor/start-the-replication-monitor.md)   
 [Anzeigen von Informationen und Ausführen von Aufgaben für eine Veröffentlichung &#40;Replication Monitor&#41;](../../relational-databases/replication/monitor/view-information-and-perform-tasks-for-a-publication-replication-monitor.md)   
 [Anzeigen von Informationen und Ausführen von Aufgaben für die einer Veröffentlichung zugeordneten Agents &#40;Replikationsmonitor&#41;](../../relational-databases/replication/monitor/view-information-and-perform-tasks-for-publication-agents.md)   
 [Überwachen der Replikation](../../relational-databases/replication/monitor/monitoring-replication-overview.md)  
  
  
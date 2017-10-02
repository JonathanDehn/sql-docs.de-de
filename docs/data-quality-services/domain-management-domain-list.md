---
title: "Domänenverwaltung: Domänenliste | Microsoft-Dokumentation"
ms.custom: 
ms.date: 11/08/2011
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- data-quality-services
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- sql13.dqs.dm.domainlist.f1
ms.assetid: 8df305f0-97ea-4226-811b-979ed862e1f0
caps.latest.revision: 13
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.translationtype: HT
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: 83b1db3be39a5472fd422f23955eff9bafb5265f
ms.contentlocale: de-de
ms.lasthandoff: 09/09/2017

---
# <a name="domain-management-domain-list"></a>Domänenverwaltung: Domänenliste
  In diesem Thema werden die Steuerelemente in der Liste „Domänen“ auf der Seite **Domänenverwaltung** in [!INCLUDE[ssDQSnoversion](../includes/ssdqsnoversion-md.md)] (DQS) beschrieben. Verwenden Sie diesen Bereich, um eine Domäne auszuwählen, für die Verwaltungsvorgänge ausgeführt werden sollen. Der gleiche Bereich wird für alle Seiten im Registerkartenformat auf der Seite **Domänenverwaltung** verwendet.  
  
## <a name="options"></a>Optionen  
  
### <a name="domains-list"></a>Domänenliste  
 **Domäne**  
 Diese Liste enthält alle Domänen in der Wissensdatenbank. Vorgänge, die Sie auf den Seiten im Registerkartenformat im rechten Bereich ausführen, werden auf die in der Liste ausgewählte Domäne angewendet. Weitere Informationen finden Sie unter  
  
 **Erstellen einer Verbunddomäne**  
 Erstellen Sie eine neue Verbunddomäne in der Wissensdatenbank. Durch diesen Befehl wird das Dialogfeld **Verbunddomäne erstellen** angezeigt. Sie rufen den Befehl auf, indem Sie mit der rechten Maustaste auf eine Domäne klicken oder indem Sie auf das Symbol oberhalb der Domänenliste klicken. Weitere Informationen finden Sie unter [Create a Composite Domain](../data-quality-services/create-a-composite-domain.md).  
  
 **Erstellen einer Domäne**  
 Erstellen Sie eine neue Domäne in der Wissensdatenbank. Durch diesen Befehl wird das Dialogfeld **Domäne erstellen** angezeigt. Sie rufen den Befehl auf, indem Sie mit der rechten Maustaste auf eine Domäne klicken oder indem Sie auf das Symbol oberhalb der Domänenliste klicken. Weitere Informationen finden Sie unter [Create a Domain](../data-quality-services/create-a-domain.md).  
  
 **Kopie der ausgewählten Domäne erstellen**  
 Erstellen Sie eine genaue Kopie der ausgewählten Domäne, und fügen Sie sie der Wissensdatenbank hinzu. Der Name entspricht dem Namen der kopierten Domäne mit dem Zusatz „ ‑ Kopie“. Sie rufen den Befehl auf, indem Sie mit der rechten Maustaste auf eine Domäne klicken und **Kopie erstellen**auswählen oder indem Sie auf das Symbol oberhalb der Domänenliste klicken. Er ist für Verbunddomänen nicht verfügbar.  
  
 **Domäne aus Datendatei importieren**  
 Importieren Sie eine Domäne aus einer DQS-Datei. Durch diesen Befehl wird das Dialogfeld **Aus Datendatei importieren** angezeigt, in dem Sie das Dateisystem durchsuchen und eine DQS-Datei für eine einzelne Domäne oder eine Verbunddomäne auswählen können. Sie rufen den Befehl auf, indem Sie auf das Symbol oberhalb der Domänenliste klicken. Weitere Informationen finden Sie unter [Import a Domain from a .dqs File](../data-quality-services/import-a-domain-from-a-dqs-file.md).  
  
 **Domäne löschen**  
 Löschen Sie die ausgewählte Domäne aus der Wissensdatenbank. Durch diesen Befehl wird das Dialogfeld **SQL Server Data Quality Services** aufgerufen. Wenn Sie auf **Ja**klicken, werden die Domäne und all zugehörigen Daten dauerhaft gelöscht. Sie rufen den Befehl auf, indem Sie mit der rechten Maustaste auf eine Domäne klicken oder indem Sie auf das Symbol oberhalb der Domänenliste klicken.  
  
 **Erstellen einer verknüpften Domäne**  
 Erstellen Sie eine Domäne, die mit der ausgewählten Domäne verknüpft ist. Durch diesen Befehl wird das Dialogfeld **Domäne erstellen** angezeigt. Sie rufen diesen Befehl auf, indem Sie mit der rechten Maustaste auf eine Domäne klicken und **Verknüpfte Domäne erstellen** auswählen. Die Domäne, zu der Sie eine Verknüpfung herstellen, wird im Dialogfeld „Domäne erstellen“ angezeigt. Dieser Befehl ist für Verbunddomänen nicht verfügbar. Es gibt keinen Befehl, mit dem die Verknüpfung von zwei Domänen aufgehoben werden kann. Hierzu müssen Sie die verknüpfte Domäne löschen. Es kann keine verknüpfte Domäne für eine andere verknüpfte Domäne erstellt werden. Weitere Informationen finden Sie unter [Create a Linked Domain](../data-quality-services/create-a-linked-domain.md).  
  
 Eine verknüpfte Domäne weist die gleichen Werte auf wie die Domäne, mit der sie verknüpft ist. Nur der Name und die Eigenschaften der Domänen unterscheiden sich. Wenn Sie eine Domänenregel, einen Domänenwert, eine Verweisdatenverknüpfung oder eine begriffsbasierte Beziehung in der Domäne ändern, mit der eine andere Domäne verknüpft ist, ändert sich auch die Domänenregel, der Domänenwert, die Verweisdatenverknüpfung bzw. die begriffsbasierte Beziehung in der verknüpften Domäne. Ebenso gilt, dass bei Änderung eines Werts in der verknüpften Domäne der Wert in der Domäne, mit der diese verknüpft ist, ebenfalls geändert wird.  
  
 **Wissensdatenbank exportieren**  
 Exportieren Sie die gesamte Wissensdatenbank in eine DQS-Datei. Durch diesen Befehl wird das Dialogfeld **In Datendatei exportieren** aufgerufen. Sie rufen diesen Befehl auf, indem Sie oben auf der Seite oder im Kontextmenü der Domänen im Domänenlistenbereich unter **Exportieren** auf **Daten der Wissensdatenbank exportieren** klicken. Weitere Informationen finden Sie unter [Export a Knowledge Base to a .dqs File](../data-quality-services/export-a-knowledge-base-to-a-dqs-file.md).  
  
 **Domäne exportieren**  
 Exportieren Sie die Domäne in eine DQS-Datei. Durch diesen Befehl wird das Dialogfeld **In Datendatei exportieren** aufgerufen. Sie rufen diesen Befehl über das Menü **Exportieren** in der Menüleiste am oberen Rand der Seite auf, oder klicken Sie mit der rechten Maustaste in den Domänenlistenbereich. Weitere Informationen finden Sie unter [Export a Domain to a .dqs File](../data-quality-services/export-a-domain-to-a-dqs-file.md).  
  
  
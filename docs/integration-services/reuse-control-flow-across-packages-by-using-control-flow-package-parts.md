---
title: Wiederverwenden der Ablaufsteuerung in Paketen mithilfe von Ablaufsteuerungs-Paketteile | Microsoft Docs
ms.custom:
- SQL2016_New_Updated
ms.date: 03/01/2017
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- integration-services
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- sql13.dts.designer.toolboxcontrolflowtemplate.f1
- sql13.dts.designer.addcopyexistingtemplate.f1
- sql13.dts.designer.addcopyexistingpackagepart.f1
- sql13.dts.designer.packagepart.general.f1
ms.assetid: 1edc91d9-1fab-4fe5-aed3-6f581fe32c18
caps.latest.revision: 14
author: douglaslMS
ms.author: douglasl
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: f3481fcc2bb74eaf93182e6cc58f5a06666e10f4
ms.openlocfilehash: 3dfe873284d448a53d4c094b622a5411261039e3
ms.contentlocale: de-de
ms.lasthandoff: 08/03/2017

---
# <a name="reuse-control-flow-across-packages-by-using-control-flow-package-parts"></a>Wiederverwenden der Ablaufsteuerung für Pakete mithilfe von Ablaufsteuerungs-Paketteilen
  Sie können einen häufig verwendeten Ablaufsteuerungstask oder Container in einer eigenständigen Teiledatei (einer DTSXP-Datei) speichern und in einem oder mehreren Paketen unter Verwendung von Ablaufsteuerungs-Paketteilen mehrmalig wiederverwenden. Die Wiederverwendbarkeit erleichtert das Design und die Verwaltung von SSIS-Paketen.  
  
## <a name="create-a-new-control-flow-package-part"></a>Erstellen eines neuen Ablaufsteuerungs-Paketteils  
 Erweitern Sie im Projektmappen-Explorer den Ordner **Paketteile** , um einen neuen Ablaufsteuerungs-Paketteil zu erstellen. Klicken Sie mit der rechten Maustaste auf **Ablaufsteuerung** , und wählen Sie **Neuer Ablaufsteuerungs-Paketteil**aus.  
  
 ![Erstellen eine neuen ablaufsteuerungsvorlage](../integration-services/media/control-flow-templates-create-new.png "erstellen eine neuen ablaufsteuerungsvorlage")  
  
 Eine neue Teiledatei mit der Erweiterung „.dtsxp“ wird im Ordner **Paketteile | Ablaufsteuerung** erstellt. Gleichzeitig wird ein neues Element mit dem gleichen Namen zur SSIS-Toolbox hinzugefügt. (Das Toolboxelement wird nur angezeigt, wenn in Visual Studio ein Projekt geöffnet ist, das den Teil enthält.)  
  
 ![Steuern Sie die Vorlagen der ablaufsteuerung in Toolbox](../integration-services/media/control-flow-templates-in-toolbox.png "steuern Sie die Vorlagen der ablaufsteuerung in Toolbox")  
  
## <a name="design-a-control-flow-package-part"></a>Entwerfen eines Ablaufsteuerungs-Paketteils  
 Zum Öffnen des Paketteil-Editors, doppelklicken Sie im Projektmappen-Explorer auf die Teiledatei. Sie können den Teil genau wie ein Paket entwerfen.  
  
 ![Schritt 1 von Control Flow Vorlagenentwurf](../integration-services/media/control-flow-template-design-step-1.png "Schritt 1 von Control Flow Vorlagenentwurf")  
  
 ![Schritt 2 von Control Flow Vorlagenentwurf](../integration-services/media/control-flow-template-design-step-2.png "Schritt2 des Control Flow Vorlagenentwurf")  
  
 Für Ablaufsteuerungs-Paketteile gelten die folgenden Einschränkungen.  
  
-   Ein Teil kann nur einen Task oder Container der obersten Ebene enthalten. Wenn Sie mehrere Tasks oder Container hinzufügen möchten, fügen Sie diese in einen Sequenzcontainer ein.  
  
-   Sie können einen Teil nicht direkt im Designer ausführen oder debuggen .  
  
## <a name="add-an-existing-control-flow-package-part-to-a-package"></a>Hinzufügen eines vorhandenen Ablaufsteuerungs-Paketteils zu einem Paket  
 Teile, die im aktuellen Integration Services-Projekt oder in einem anderen Projekt gespeichert wurden, können wiederverwendet werden.  
  
-   Zum Wiederverwenden eines Teils, der zum aktuellen Projekt gehört, ziehen Sie ihn mit Drag & Drop aus der Toolbox.  
  
-   Zum Wiederverwenden eines Teils, der zu einem anderen Projekt gehört, verwenden Sie den Befehl **Vorhandenen Ablaufsteuerungs-Paketteil hinzufügen** .  
  
### <a name="drag-and-drop-a-control-flow-package-part"></a>Verschieben eines Ablaufsteuerungs-Paketteils mit Drag & Drop  
 Wenn Sie einen Teil in einem Projekt wiederverwenden möchten, verschieben Sie das Teilelement einfach mit Drag & Drop wie einen beliebigen anderen Task oder Container aus der Toolbox. Sie können den Teil per Drag & Drop mehrere Male in ein Paket verschieben, um die Logik an mehreren Orten im Paket wiederzuverwenden. Mit dieser Methode können Sie einen Teil wiederverwenden, der zum aktuellen Projekt gehört.  
  
 ![Hinzufügen eine ablaufsteuerungsvorlage zu einem Paket](../integration-services/media/control-flow-templates-add-to-package.png "hinzufügen eine ablaufsteuerungsvorlage zu einem Paket")  
  
 ![Paket mit mehreren Vorlagen der ablaufsteuerung](../integration-services/media/control-flow-templates-in-package.png "Paket mit mehreren Vorlagen der ablaufsteuerung")  
  
 Beim Speichern des Pakets wird vom SSIS-Designer überprüft, ob das Paket Teileinstanzen enthält.  
  
-   Ist dies der Fall, generiert der Designer eine neue .dtsx.designer-Datei mit allen Informationen über die Teile.  
  
-   Wenn das Paket keine Teile verwendet werden alle zuvor erstellten .dtsx.designer-Dateien für das Paket (d. h. alle .dtsx.designer-Dateien, die den gleichen Namen wie das Paket haben) vom Designer gelöscht.  
  
 ![Projektmappen-Explorer mit Vorlagen der ablaufsteuerung](../integration-services/media/control-flow-templates-in-solution-explorer.png "Projektmappen-Explorer mit Vorlagen der ablaufsteuerung")  
  
### <a name="add-a-copy-of-an-existing-control-flow-package-part-or-a-reference-to-an-existing-part"></a>Hinzufügen einer Kopie eines vorhandenen Ablaufsteuerungs-Paketteils oder eines Verweises auf einen vorhandenen Teil  
 Erweitern Sie im Projektmappen-Explorer den Ordner **Paketteile** , um einem Paket im Dateisystem eine Kopie eines vorhandenen Teils hinzuzufügen. Klicken Sie mit der rechten Maustaste auf **Ablaufsteuerung** , und wählen Sie **Vorhandenen Ablaufsteuerungs-Paketteil hinzufügen**aus.  
  
 ![Hinzufügen einer neuen Vorlagen der ablaufsteuerung aus dem Menü](../integration-services/media/control-flow-templates-add-from-menu.png "fügen Sie einen neuen Vorlagen der ablaufsteuerung aus dem Menü hinzu")  
  
 ![Kopieren von vorhandenen Vorlagen-Dialogfelds "hinzufügen"](../integration-services/media/control-flow-templates-add-copy-dialog.png "Kopie des vorhandenen Vorlagen hinzufügen (Dialogfeld)")  
  
 **Optionen**  
  
 **Paketteilpfad**  
 Geben Sie den Pfad der Teildatei ein, oder klicken Sie auf die Schaltfläche „Durchsuchen (...)“, und suchen Sie die Teildatei, die Sie kopieren oder auf die Sie verweisen möchten.  
  
 **Als Verweis hinzufügen**  
 -   Ist diese Option ausgewählt, wird der Teil dem Integration Services-Projekt als Verweis hinzugefügt. Wählen Sie diese Option aus, wenn Sie auf eine einzige Kopie einer Teiledatei in mehreren Integration Services-Projekten verweisen möchten.  
  
-   Ist die Option deaktiviert, wird eine Kopie der Teiledatei zum Projekt hinzugefügt.  
  
## <a name="configure-a-control-flow-package-part"></a>Konfigurieren eines Ablaufsteuerungs-Paketteils  
 Verwenden Sie das Dialogfeld **Paketteilkonfiguration**  , um Ablaufsteuerungs-Paketteile zu konfigurieren, nachdem Sie sie zur Ablaufsteuerung eines Pakets hinzugefügt haben.  
  
#### <a name="to-open-the-package-part-configuration-dialog-box"></a>So öffnen Sie das Dialogfeld „Paketteilkonfiguration“  
  
1.  Um eine Teileinstanz zu konfigurieren, doppelklicken Sie in der Ablaufsteuerung auf die Teileinstanz. Oder klicken Sie mit der rechten Maustaste auf die Teileinstanz, und wählen Sie **Bearbeiten**aus. Das Dialogfeld **Paketteilkonfiguration** wird geöffnet.  
  
2.  Konfigurieren Sie die Eigenschaften und Verbindungs-Manager für die Teileinstanz.  
  
### <a name="properties-tab"></a>Eigenschaften (Registerkarte)  
 Verwenden Sie die Registerkarte **Eigenschaften** im Dialogfeld **Paketteilkonfiguration**  , um die Eigenschaften des Teils festzulegen.  
  
 ![Registerkarte "Eigenschaften" des Dialogfelds ist die Vorlagenkonfiguration](../integration-services/media/template-configuration-properties-tab.png "Registerkarte "Eigenschaften" des Dialogfelds ist die Vorlagenkonfiguration")  
  
 In der Strukturansichthierarchie im linken Fensterbereich werden alle konfigurierbaren Eigenschaften der Teileinstanz aufgeführt.  
  
-   Wird eine Option deaktiviert, wird die Eigenschaft für die Teileinstanz nicht konfiguriert. Für die Teileinstanz wird der Standardwert für die Eigenschaft verwendet, der im Ablaufsteuerungs-Paketteil definiert ist.  
  
-   Wird eine Option aktiviert, überschreibt der eingegebene oder ausgewählte Wert den Standardwert.  
  
 Die Tabelle im rechten Fensterbereich enthält die zu konfigurierenden Eigenschaften.  
  
-   **Eigenschaftspfad**. Der Eigenschaftspfad des Eigenschaft.  
  
-   **Eigenschaftstyp**. Der Datentyp der Eigenschaft.  
  
-   **Wert**. Der konfigurierte Wert. Dieser Wert überschreibt den Standardwert.  
  
### <a name="connection-managers-tab"></a>Registerkarte „Verbindungs-Manager“  
 Auf der Registerkarte **Verbindungs-Manager** im Dialogfeld **Paketteilkonfiguration**  können Sie die Eigenschaften der Verbindungs-Manager für die Teileinstanz festlegen.  
  
 ![Verbindungs-Manager-Registerkarte des Dialogfelds ist die Vorlagenkonfiguration](../integration-services/media/template-configuration-connection-managers-tab.png "Registerkarte "Verbindungs-Manager" des Dialogfelds ist die Vorlagenkonfiguration")  
  
 Die Tabelle im linken Fensterbereich enthält alle Verbindungs-Manager, die im Ablaufsteuerungsteil definiert sind. Wählen Sie den Verbindungs-Manager aus, den Sie konfigurieren möchten.  
  
 Die Liste im rechten Fensterbereich enthält die Eigenschaften des ausgewählten Verbindungs-Managers.  
  
-   **Festgelegt**. Aktiviert, wenn die Eigenschaft für die Teileinstanz konfiguriert wurde.  
  
-   **Eigenschaftsname**. Der Name der Eigenschaft.  
  
-   **Wert**. Der konfigurierte Wert. Dieser Wert überschreibt den Standardwert.  
  
## <a name="delete-a-control-flow-part"></a>Löschen eines Ablaufsteuerungsteils  
 Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf einen Teil, und wählen Sie anschließend **Löschen**aus. Klicken Sie auf **OK** , um den Löschvorgang zu bestätigen, oder klicken Sie auf **Abbrechen** , um den Teil beizubehalten.  
  
 Wenn Sie einen Teil aus einem Projekt löschen, wird er endgültig aus dem Dateisystem entfernt und kann nicht wiederhergestellt werden.  
  
> [!NOTE]  
>  Wenn Sie einen Teil aus einem Integration Services-Projekt entfernen, ihn aber in anderen Projekten weiter verwenden möchten, wählen Sie anstelle der Option **Löschen**  die Option **Aus Projekt ausschließen** aus.  
  
## <a name="package-parts-are-a-design-time-feature-only"></a>Paketteile sind eine reine Entwurfszeitfunktion  
 Paketteile sind eine reine Entwurfszeitfunktion. Im SSIS-Designer können Sie Teile erstellen, öffnen, speichern und aktualisieren sowie Teileinstanzen zu einem Paket hinzufügen, darin konfigurieren oder daraus löschen. In der SSIS-Laufzeit werden die Teile jedoch ignoriert. Nachfolgend wird erläutert, wie der Designer diese Trennung erreicht.  
  
-   Der Designer speichert Instanzen von Paketteilen mit den konfigurierten Eigenschaften in einer .dtsx.designer-Datei.  
  
-   Beim Speichern der .dtsx.designer-Datei durch den Designer wird gleichzeitig der Inhalt aus den Teilen extrahiert, auf die diese Datei verweist, und die Teileinstanzen im Paket werden durch den Inhalt der Teile ersetzt.  
  
-   Schließlich wird der gesamte Inhalt, der keine Teileinformationen mehr enthält, zurück in die DTSX-Paketdatei gespeichert. Dies ist die Datei, die von der SSIS-Laufzeit ausgeführt wird.  
  
 Das folgende Diagramm veranschaulicht die Beziehung zwischen Teilen („DTSXP-Dateien), dem SSIS-Designer und der SSIS-Laufzeit.  
  
 ![Datenfluss-Vorlagendateien und den Fluss steuern](../integration-services/media/control-flow-templates-intro.png "Flow-Vorlagendateien und den Fluss steuern")  
  
  
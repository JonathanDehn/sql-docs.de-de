---
title: Azure Blob-Quelle | Microsoft Docs
ms.custom:
- SQL2016_New_Updated
ms.date: 07/25/2016
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- integration-services
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- sql13.dts.designer.afpblobsrc.f1
- sql14.dts.designer.afpblobsrc.f1
ms.assetid: 80645c5c-88c8-4fb0-8607-de1bb7bffcbb
caps.latest.revision: 12
author: douglaslMS
ms.author: douglasl
manager: jhubbard
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: 752f199d4555163fee9bbc7b1cbcda9e69b638aa
ms.contentlocale: de-de
ms.lasthandoff: 08/03/2017

---
# <a name="azure-blob-source"></a>Azure-Blob-Quelle
  Die **Azure-Blobquelle** ermöglicht es einem SSIS-Paket, Daten aus einem Azure-Blob zu lesen. Die unterstützten Dateiformate sind CSV und AVRO.
  
  Um den Editor für die Azure-Blobquelle aufzurufen, ziehen Sie die **Azure-Blobquelle** auf den Datenfluss-Designer, und doppelklicken Sie darauf, um den Editor zu öffnen.  
  
 Die **Azure Blob-Quelle** ist eine Komponente von der [SQL Server Integration Services (SSIS) Feature Pack für Azure](../../integration-services/azure-feature-pack-for-integration-services-ssis.md).  
  
1.  Geben Sie für den **Azure Storage-Verbindungs-Manager** einen vorhandenen Azure Storage-Verbindungs-Manager an, oder erstellen Sie einen neuen, der auf ein Azure-Speicherkonto verweist.  
  
2.  Geben Sie im Feld **Blobcontainername** den Namen des Blobcontainers an, der die Quelldateien enthält.  
  
3.  Geben Sie im Feld **Blobname** den Pfad für das Blob an.  
  
4.  Geben Sie im Feld **Blobdateiformat** das gewünschte Blobformat an.  
  
5.  Wenn es sich um das CSV-Dateiformat handelt, geben Sie den Wert für das **Spaltentrennzeichen** ein. Aktivieren Sie außerdem **Spaltennamen in der ersten Datenzeile** , wenn die erste Zeile in der Datei Spaltennamen enthält.  
  
6.  Nachdem Sie die Verbindungsinformationen angegeben haben, wechseln Sie zur Seite **Spalten** , um Quellspalten zu den Zielspalten für den SSIS-Datenfluss zuzuordnen.  
  
  

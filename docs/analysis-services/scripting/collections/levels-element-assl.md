---
title: Level-Element (ASSL) | Microsoft Docs
ms.date: 05/03/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: assl
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: d327d4525a179191cfc1889ebf0035522860efaf
ms.sourcegitcommit: c12a7416d1996a3bcce3ebf4a3c9abe61b02fb9e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2018
---
# <a name="levels-element-assl"></a>Levels-Element (ASSL)
[!INCLUDE[ssas-appliesto-sqlas](../../../includes/ssas-appliesto-sqlas.md)]
  Enthält die Auflistung der [Ebene](../../../analysis-services/scripting/objects/level-element-assl.md) Elemente in einem [Hierarchie](../../../analysis-services/scripting/objects/hierarchy-element-assl.md) Element.  
  
## <a name="syntax"></a>Syntax  
  
```xml  
  
<Hierarchy>  
      ...  
   <Levels>  
      <Level>...</Level>  
   </Levels>  
   ...  
</Hierarchy>  
```  
  
## <a name="element-characteristics"></a>Elementmerkmale  
  
|Merkmal|Beschreibung|  
|--------------------|-----------------|  
|Datentyp und -länge|Keine|  
|Standardwert|Keine|  
|Kardinalität|0-1: Optionales Element, das nur einmal auftreten kann.|  
  
## <a name="element-relationships"></a>Elementbeziehungen  
  
|Beziehung|Element|  
|------------------|-------------|  
|Übergeordnete Elemente|[Hierarchie](../../../analysis-services/scripting/objects/hierarchy-element-assl.md)|  
|Untergeordnete Elemente|[Ebene](../../../analysis-services/scripting/objects/level-element-assl.md)|  
  
## <a name="remarks"></a>Hinweise  
 Das entsprechende Element im Objektmodell von Analysis Management Objects (AMO) ist <xref:Microsoft.AnalysisServices.LevelCollection>.  
  
## <a name="see-also"></a>Siehe auch  
 [Schemaauflistungen & #40; ASSL & #41;](../../../analysis-services/scripting/collections/collections-assl.md)  
  
  

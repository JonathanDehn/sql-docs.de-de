---
title: RequestType-Element (XMLA) | Microsoft Docs
ms.date: 05/08/2018
ms.prod: sql
ms.technology: analysis-services
ms.custom: xmla
ms.topic: reference
ms.author: owend
ms.reviewer: owend
author: minewiskan
manager: kfile
ms.openlocfilehash: 63c1a838d74745b5ef51f73b51e34c95e08a81ff
ms.sourcegitcommit: 808d23a654ef03ea16db1aa23edab496b73e5072
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2018
ms.locfileid: "34577622"
---
# <a name="requesttype-element-xmla"></a>RequestType-Element (XMLA)
[!INCLUDE[ssas-appliesto-sqlas-aas](../../../includes/ssas-appliesto-sqlas-aas.md)]
  Bestimmt den Typ des vom zurückgegebenen Metadaten der [Discover](../../../analysis-services/xmla/xml-elements-methods-discover.md) Methode.  
  
## <a name="syntax"></a>Syntax  
  
```xml  
  
<Discover>  
   ...  
   <RequestType>...</RequestType>  
   ...  
</Discover>  
```  
  
## <a name="element-characteristics"></a>Elementmerkmale  
  
|Merkmal|Description|  
|--------------------|-----------------|  
|Datentyp und -länge|Zeichenfolge (Enumeration)|  
|Standardwert|InclusionThresholdSetting|  
|Cardinality|1-1: Erforderliches Element, das nur einmal auftritt.|  
  
## <a name="element-relationships"></a>Elementbeziehungen  
  
|Beziehung|Element|  
|------------------|-------------|  
|Übergeordnete Elemente|[Ermitteln](../../../analysis-services/xmla/xml-elements-methods-discover.md)|  
|Untergeordnete Elemente|InclusionThresholdSetting|  
  
## <a name="remarks"></a>Hinweise  
 Das **RequestType** -Element bestimmt das Schemarowset, von dem die **Discover** -Methode Daten zurückgibt. Diese Enumeration ist auf den Namen der von Analysis Services unterstützten Schemarowsets beschränkt. Weitere Informationen zu Schemarowsets finden Sie unter [Analysis Services-Schemarowsets](../../../analysis-services/schema-rowsets/analysis-services-schema-rowsets.md).  
  
> [!NOTE]  
>  Das **RequestType** -Element listet nur Schemarowsetnamen auf. Ein Fehler tritt auf, wenn die Schemarowset-GUID verwendet wird.  
  
## <a name="see-also"></a>Siehe auch
 [Eigenschaften &#40;XMLA&#41;](../../../analysis-services/xmla/xml-elements-properties/xml-elements-properties.md)  
  
  

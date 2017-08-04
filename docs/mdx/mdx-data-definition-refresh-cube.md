---
title: REFRESH CUBE-Anweisung (MDX) | Microsoft Docs
ms.custom: 
ms.date: 03/02/2016
ms.prod: sql-server-2016
ms.reviewer: 
ms.suite: 
ms.technology:
- analysis-services
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- Cube
- REFRESH CUBE
- REFRESH_CUBE
- REFRESH
dev_langs:
- kbMDX
helpviewer_keywords:
- cubes [Analysis Services], cache
- refreshing cache
- REFRESH CUBE statement
- cache [Analysis Services]
ms.assetid: b8c087fb-5d17-4b13-b7cf-9929e9aab35c
caps.latest.revision: 31
author: Minewiskan
ms.author: owend
manager: erikre
ms.translationtype: MT
ms.sourcegitcommit: 1419847dd47435cef775a2c55c0578ff4406cddc
ms.openlocfilehash: ce57b2384e8cf28dae218dec5f09b756b8cd61c6
ms.contentlocale: de-de
ms.lasthandoff: 08/02/2017

---
# <a name="mdx-data-definition---refresh-cube"></a>MDX-Datendefinition - CUBE aktualisieren
[!INCLUDE[tsql-appliesto-ss2008-xxxx-xxxx-xxx_md](../includes/tsql-appliesto-ss2008-xxxx-xxxx-xxx-md.md)]

  Aktualisiert den Clientcache für einen Cube.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
REFRESH CUBECube_Name   
```  
  
## <a name="arguments"></a>Argumente  
 *Cube_Name*  
 Ein gültiger Zeichenfolgenausdruck, der einen Cubenamen bereitstellt.  
  
## <a name="remarks"></a>Hinweise  
 Bei Clientanwendungen, die Verbindung mit einer Instanz von [!INCLUDE[msCoName](../includes/msconame-md.md)] [!INCLUDE[ssNoVersion](../includes/ssnoversion-md.md)] [!INCLUDE[ssASnoversion](../includes/ssasnoversion-md.md)], diese Anweisung bewirkt, dass den Arbeitsspeicher der Clientanwendung mit dem Server synchronisiert werden zwischengespeichert. Erkennung und Update erfolgen zwar normalerweise automatisch, die zeitlichen Abstände hängen aber von den Einstellungen der Clientverbindungszeichenfolge ab. Die REFRESH CUBE-Anweisung aktualisiert die Daten sofort.  
  
 Bei Clientanwendungen, die eine Verbindung zu einem lokalen Cube besitzen, veranlasst die REFRESH CUBE-Anweisung die Neuerstellung der lokalen Cubedatei.  
  
> [!IMPORTANT]  
>  Auf dem Server gespeicherte benannte Mengen werden nicht aktualisiert.  
  
## <a name="see-also"></a>Siehe auch  
 [MDX-Datendefinitionsanweisungen &#40; MDX &#41;](../mdx/mdx-data-definition-statements-mdx.md)  
  
  

---
title: Referencia de reglas de rendimiento | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 59fc9424-76ca-4365-ae47-bb14a736c9c2
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a8f96819c5d6f8e2be1c7f92e53ebbb29d075886
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47580432"
---
# <a name="performance-rules-reference"></a>Referencia de reglas de rendimiento
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [referencia de las reglas de rendimiento](https://docs.microsoft.com/visualstudio/profiling/performance-rules-reference).  
  
Las reglas de rendimiento de las herramientas de generación de perfiles proporcionan advertencias adicionales e información sobre el rendimiento de la aplicación. Las reglas de rendimiento analizan los datos en un proceso de generación de perfiles recopilados de orígenes como los contadores de rendimiento de procesador y de Windows. Los mensajes de regla aparecen en la ventana Salida de error del entorno de desarrollo integrado de [!INCLUDE[vs_current_short](../includes/vs-current-short-md.md)]. Los mensajes se muestran con uno de los siguientes niveles de regla:  
  
|||  
|-|-|  
|**Error**|Pocas reglas generan mensajes de error, dado que la mayoría de los problemas de rendimiento no son errores propiamente dichos. Un mensaje de error puede indicar que no es posible recopilar datos de generación de perfiles.|  
|**Advertencia**|Las advertencias indican un área de la aplicación que puede ser una fuente de problemas de rendimiento o que podría beneficiarse de las optimizaciones.|  
|**Información**|Los mensajes de información indican que el análisis de una condición de regla no alcanzó el umbral para generar un mensaje de error o que la información en el mensaje es útil, pero no refleja un problema de rendimiento.|  
  
## <a name="in-this-section"></a>En esta sección  
 [Reglas de rendimiento por identificador](../profiling/performance-rules-by-id.md)  
  
 Las reglas de rendimiento de las herramientas de generación de perfiles se organizan en cuatro categorías:  
  
|||  
|-|-|  
|[Reglas de rendimiento de uso de .NET Framework](../profiling/dotnet-framework-usage-performance-rules.md)|Reglas que le ayudarán a utilizar .NET Framework de forma más eficaz.|  
|[Reglas de rendimiento de memoria y paginación](../profiling/memory-and-paging-performance-rules.md)|Reglas que analizan el comportamiento de paginación y la memoria administrada de la aplicación.|  
|[Reglas de uso de herramientas de generación de perfiles](../profiling/profiling-tools-usage-rules.md)|Reglas que le ayudarán a utilizan las herramientas de generación de perfiles de forma más eficaz.|  
|[Reglas de rendimiento de la supervisión de recursos](../profiling/resource-monitoring-performance-rules.md)|Mensajes de información sobre el uso del procesador y la memoria en un proceso de generación de perfiles.|



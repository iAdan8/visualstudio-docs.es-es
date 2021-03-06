---
title: Apagar | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: a1e37500-4ad1-4670-9737-3d9a20536386
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: b9b8848399ea88b5f4ce7ebf30f970e2091e6406
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2019
ms.locfileid: "54784604"
---
# <a name="shutdown"></a>Apagar
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La opción **Apagar** espera a que termine o se desasocie cualquier proceso del que se generaron perfiles actualmente y, después, desactiva el generador de perfiles y cierra el archivo de datos de generación de perfiles. La opción **Apagar** debe ser el último comando de una ejecución de generación de perfiles.  
  
 Si no se especifica un parámetro de tiempo de espera, la opción **Apagar** esperará indefinidamente. Si se especifica un parámetro de tiempo de espera, la opción vuelve tras el número de segundos especificado sin desactivar el generador de perfiles ni cerrar el archivo de datos.  
  
 La opción **Apagar** debe ser la única especificada en la línea de comandos.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
VSPerfCmd.exe /Shutdown[:Timeout]  
```  
  
#### <a name="parameters"></a>Parámetros  
 `Timeout`  
 -   (Opcional) Si se especifica, la opción vuelve tras el número de segundos especificado sin desactivar el generador de perfiles ni cerrar el archivo de datos de generación de perfiles.  
  
## <a name="see-also"></a>Vea también  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Generar perfiles para aplicaciones independientes](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Generar perfiles para aplicaciones web ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Generar perfiles de servicios](../profiling/command-line-profiling-of-services.md)

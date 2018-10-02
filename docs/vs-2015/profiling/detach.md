---
title: Desasociar | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: d9d1b52c-7f28-467d-b1e0-512afc4e46c9
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 56ad870d4638607ad03b60b33bb7d648dbbca424
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47577445"
---
# <a name="detach"></a>Desasociar
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [Detach](https://docs.microsoft.com/visualstudio/profiling/detach).  
  
La opción **Desasociar** de VSPerfCmd.exe desconecta el generador de perfiles de los procesos especificados o de todos los procesos si no se especifica ninguno. Se debe haber inicializado la generación de perfiles mediante el método de muestreo.  
  
 La generación de perfiles que se ha iniciado con las opciones **Iniciar** o **Adjuntar** se puede desconectar con **Desasociar**. El generador de perfiles se puede volver a adjuntar mediante los comandos **Adjuntar** subsiguientes.  
  
 **Desasociar** no cierra el archivo de datos de generación de perfiles. Use la opción **Cierre** para finalizar la generación de perfiles y cerrar el archivo de datos.  
  
> [!NOTE]
>  Si la opción **Start** se ha especificado con la opción **CrossSession**, en cualquier llamada a **VSPerfCmd /Attach** o a **VSPerfCmd /Detach** también se debe especificar **CrossSession**.  
  
## <a name="syntax"></a>Sintaxis  
  
```  
VSPerfCmd.exe /Detach[:PIDs|ProcessNames]  
```  
  
#### <a name="parameters"></a>Parámetros  
 `PIDs|ProcessNames`  
 `PID`: identificador del sistema numérico de uno o varios procesos.  
  
 `ProcessNames`: nombre del proceso. Si se ejecutan varias instancias del proceso designado, los resultados son imprevisibles.  
  
 Separe varios procesos con comas.  
  
 Si no se especifica ningún proceso, el generador de perfiles se desasocia de todos los procesos para los que se generan perfiles.  
  
## <a name="valid-options"></a>Opciones válidas  
 Las opciones siguientes de **VSPerfCmd** se pueden combinar con la opción **Adjuntar** en una sola línea de comandos.  
  
 **CrossSession**  
 Habilita la generación de perfiles de aplicaciones en las sesiones que no sean la sesión de inicio. Es obligatorio si la opción **Start** se ha especificado con la opción **CrossSession**.  
  
## <a name="example"></a>Ejemplo  
 En este ejemplo, el comando **Desasociar** suspende la generación de perfiles y el comando **Cierre** cierra el archivo de datos del generador de perfiles.  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe  
;REM Excercise the application  
VSPerfCmd.exe /Detach  
VSPerfCmd.exe /Shutdown  
```  
  
## <a name="see-also"></a>Vea también  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Generar perfiles para aplicaciones independientes](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Generar perfiles para aplicaciones web ASP.NET](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Generar perfiles de servicios](../profiling/command-line-profiling-of-services.md)



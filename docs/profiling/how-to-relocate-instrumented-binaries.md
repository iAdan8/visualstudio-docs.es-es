---
title: Procedimiento Cambiar la ubicación de binarios instrumentados | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.property.binaries
helpviewer_keywords:
- binaries, instrumented
- instrumentation, instrumented binaries
- instrumented binaries and relocating
- profiling tools, instrumented binaries
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 394ac9b7f3a1a72485c8b435c776ca98c7c9fdb4
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/25/2019
ms.locfileid: "54963468"
---
# <a name="how-to-relocate-instrumented-binaries"></a>Procedimiento Reubicar archivos binarios instrumentados

Durante la instrumentación, se insertan análisis en el binario para medir el rendimiento de la aplicación. Si opta por reubicar el binario instrumentado, se instrumenta una copia del binario original y se coloca en la ubicación especificada. Esta opción es útil si no desea que el generador de perfiles cambie el nombre del binario original. Si el binario no se reubica, se sobrescribe su versión original.

## <a name="to-relocate-instrumented-binary"></a>Para reubicar un binario instrumentado

1. En el **Explorador de rendimiento**, haga clic con el botón derecho del mouse en la sesión de rendimiento y, después, haga clic en **Propiedades**.

2. En **Páginas de propiedades**, haga clic en las propiedades de **Binario** .

3. Active la casilla **Reubicar archivos binarios instrumentados** .

4. Especifique la ubicación del binario instrumentado.

## <a name="see-also"></a>Vea también

[Configuración de sesiones de rendimiento](../profiling/configuring-performance-sessions.md)  
[VSInstr](../profiling/vsinstr.md)

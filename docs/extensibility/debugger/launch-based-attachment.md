---
title: Adjunto basado en Inicio | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, launching
- debug engines, attaching to programs
ms.assetid: 362f00ac-1909-4a3a-bacb-c0ceb5549816
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f4a967b48f7c904ecc22d0b3ea077ae5cecd2625
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56718968"
---
# <a name="launch-based-attachment"></a>Adjunto basado en Inicio
Basado en el lanzamiento de los datos adjuntos a un programa son automático. Cuando se inicia el proceso que hospeda el programa mediante el SDM, basado en el lanzamiento de los datos adjuntos siguen una ruta de acceso similar a la del método manual de los datos adjuntos. Para obtener información, consulte [adjuntar al programa](../../extensibility/debugger/attaching-to-the-program.md).

## <a name="the-attaching-process"></a>El proceso de asociación
 La diferencia principal es la secuencia de eventos siguiendo el **adjuntar** llamar, como sigue:

1.  Enviar una **IDebugEngineCreateEvent2** objeto event para el SDM. Para obtener más información, consulte [enviar eventos](../../extensibility/debugger/sending-events.md).

2.  Llame a la `IDebugProgram2::GetProgramId` método en el **IDebugProgram2** interfaz se pasa a la **adjuntar** método.

3.  Enviar una **IDebugProgramCreateEvent2** objeto de evento para notificar el SDM que local **IDebugProgram2** objeto se creó para representar el programa a la DE.

4.  Enviar una [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) objeto de evento para notificar el SDM que se crea un nuevo subproceso para el proceso que se inicia.

## <a name="see-also"></a>Vea también
- [Enviar los eventos necesarios](../../extensibility/debugger/sending-the-required-events.md)
- [Habilitar un programa que se desea depurar](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)
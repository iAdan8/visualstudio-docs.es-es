---
title: (Visual Studio SDK) de control de excepciones | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], exception handling
ms.assetid: 7279dc16-db14-482c-86b8-7b3da5a581d2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b580a4774cfe06f81e2d9798ef6cf949afe8c1c8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56710856"
---
# <a name="exception-handling-visual-studio-sdk"></a>Control de excepciones (Visual Studio SDK)
El siguiente describe el proceso que se produce cuando se produzcan excepciones.

## <a name="exception-handling-process"></a>Proceso de control de excepciones

1.  Cuando se produce una excepción por primera vez, pero antes de se controla mediante el controlador de excepciones en el programa que se está depurando, el motor de depuración (DE) envía un [IDebugExceptionEvent2](../../extensibility/debugger/reference/idebugexceptionevent2.md) el Administrador de depuración de sesión (SDM) como un evento de detención. El `IDebugExceptionEvent2` se envía si sólo la configuración de la excepción (especificado en el cuadro de diálogo de excepciones en el paquete de depuración) especifica que el usuario desea detener las notificaciones de excepciones de primera oportunidad.

2.  Las llamadas SDM [IDebugExceptionEvent2::GetException](../../extensibility/debugger/reference/idebugexceptionevent2-getexception.md) para obtener la propiedad de excepción.

3.  Las llamadas de paquete de depuración [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md) para determinar qué opciones se presentan al usuario.

4.  El paquete de depuración pide al usuario controlar la excepción abriendo un cuadro de diálogo de excepciones de primera oportunidad.

5.  Si el usuario decide continuar, se llama el SDM [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md).

    -   Si el método devuelve S_OK, llama a [IDebugExceptionEvent2::PassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-passtodebuggee.md).

         O bien

         Si el método devuelve S_FALSE, el programa que se está depurando se proporciona una segunda oportunidad para controlar la excepción.

6.  Si el programa que se está depurando no tiene ningún controlador para una excepción de la segunda oportunidad, envía la DE un `IDebugExceptionEvent2` en el SDM como **EVENT_SYNC_STOP**.

7.  El paquete de depuración pide al usuario controlar la excepción abriendo un cuadro de diálogo de excepciones de primera oportunidad.

8.  Las llamadas de paquete de depuración [IDebugExceptionEvent2::CanPassToDebuggee](../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md) para determinar qué opciones se presentan al usuario.

9. El paquete de depuración pide al usuario controlar la excepción abriendo un cuadro de diálogo de excepción de segunda oportunidad.

10. Si el método devuelve S_OK, llama a `IDebugExceptionEvent2::PassToDebuggee`.

## <a name="see-also"></a>Vea también
- [Llamar a los eventos del depurador](../../extensibility/debugger/calling-debugger-events.md)
---
title: Contexto de código | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], contexts
ms.assetid: 65e4d37a-086b-426e-9394-a3534967fd59
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 114537976561e72a9b1922c41d94ffa5e7ce613b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56714550"
---
# <a name="code-context"></a>Contexto de código
En [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] depuración, un **contexto del código**:

-   Proporciona una abstracción de una posición en el código tal y como se sabe que el motor de depuración (DE). Para la mayoría de las arquitecturas de tiempo de ejecución en la actualidad, un contexto de código puede considerarse como una dirección en la secuencia de instrucciones de un programa. Para los idiomas no tradicionales, donde no se puede representar código por instrucciones, se puede representar un contexto de código por otros medios.

-   Describe la posición actual en la secuencia de ejecución del programa que está depurando.

-   Existe solo cuando se ha detenido un programa en un punto de interrupción.

-   Tiene un contexto de documento asociado.

-   Se implementa mediante un [IDebugCodeContext2](../../extensibility/debugger/reference/idebugcodecontext2.md) interfaz.

## <a name="see-also"></a>Vea también
- [Contexto de documento](../../extensibility/debugger/document-context.md)
- [Contextos de depurador](../../extensibility/debugger/debugger-contexts.md)
---
title: m_stateflags (campo) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- m_stateFlags field, Task class [.NET Framework debug engines]
ms.assetid: 82b20efc-08f2-4cd2-91f6-4e01e3da906b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b6766fa98d6141005ed88d623ef8608035593a2a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56704597"
---
# <a name="mstateflags-field"></a>m_stateFlags field
Almacena información sobre el estado actual de la <xref:System.Threading.Tasks.Task> objeto.

 **Espacio de nombres:** <xref:System.Threading.Tasks?displayProperty=fullName>

 **Ensamblado:** mscorlib (en *mscorlib.dll*)

 Dado que no se puede obtener acceso a este miembro interno de .NET Framework, la sintaxis siguiente se proporciona el lenguaje intermedio en común (CIL).

## <a name="syntax"></a>Sintaxis

```csharp
.field assembly int32 modreq(System.Runtime.CompilerServices.IsVolatile) m_stateFlags
```

## <a name="remarks"></a>Comentarios
 Normalmente, se utiliza el <xref:System.Threading.Tasks.Task.Status%2A?displayProperty=fullName> propiedad para tener acceso a este valor.

 Este miembro puede ser cualquier combinación de los siguientes valores:

-   [TASK_STATE_EXECUTED](../../extensibility/debugger/task-state-executed-field.md)

-   [TASK_STATE_FAULTED](../../extensibility/debugger/task-state-faulted-field.md)

-   [TASK_STATE_CANCELED](../../extensibility/debugger/task-state-canceled-field.md)

-   [TASK_STATE_WAITING_ON_CHILDREN](../../extensibility/debugger/task-state-waiting-on-children-field.md)

-   [TASK_STATE_RAN_TO_COMPLETION](../../extensibility/debugger/task-state-ran-to-completion-field.md)

## <a name="see-also"></a>Vea también
- [Clase de tarea: miembros internos](../../extensibility/debugger/task-class-internal-members.md)
---
title: 'TaskScheduler Class: miembros internos | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- TaskScheduler class [.NET Framework debug engines]
- debug engines, TaskScheduler class [.NET Framework]
ms.assetid: 87f1c969-0217-4464-8907-7609c1bf61d3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cf7b693c058cd69ab2dcb79be787cf5a16d8f8a0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56696160"
---
# <a name="taskscheduler-class---internal-members"></a>TaskScheduler Class: miembros internos
En este artículo se describe los miembros internos de la <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName> clase que le ayudarán a implementar un depurador personalizado. Para obtener información general acerca de esta clase, vea el <xref:System.Threading.Tasks.TaskScheduler> artículo de referencia.

 **Espacio de nombres:** <xref:System.Threading.Tasks?displayProperty=fullName>

 **Ensamblado:** mscorlib (en *mscorlib.dll*)

 Dado que no se puede obtener acceso a estos miembros internos de .NET Framework, la sintaxis siguiente se proporciona el lenguaje intermedio en común (CIL).

## <a name="syntax"></a>Sintaxis

```csharp
.class public abstract auto ansi beforefieldinit System.Threading.Tasks.TaskScheduler
       extends System.Object
```

## <a name="members"></a>Miembros

### <a name="methods"></a>Métodos

|Name|Descripción|
|----------|-----------------|
|[GetScheduledTasksForDebugger](../../extensibility/debugger/getscheduledtasksfordebugger-method.md)|Recupera una matriz de todas las tareas programadas.|
|[GetTaskSchedulersForDebugger](../../extensibility/debugger/gettaskschedulersfordebugger-method.md)|Recupera una matriz de todos los <xref:System.Threading.Tasks.TaskScheduler> objetos que están activos actualmente.|

## <a name="remarks"></a>Comentarios

## <a name="see-also"></a>Vea también
- <xref:System.Threading.Tasks.TaskScheduler?displayProperty=fullName>
- [Parámetros internos de extensiones paralelas para .NET Framework](../../extensibility/debugger/parallel-extension-internals-for-the-dotnet-framework.md)
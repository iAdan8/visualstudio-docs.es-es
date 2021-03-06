---
title: IDebugMemoryContext2::Compare | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugMemoryContext2::Compare
helpviewer_keywords:
- IDebugMemoryContext2::Compare method
- Compare method
ms.assetid: c51b5128-848e-4d8e-b2e9-1161339763c3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ed8f7f778e0dfd55e9db175c4e279c92b72e427e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56721916"
---
# <a name="idebugmemorycontext2compare"></a>IDebugMemoryContext2::Compare
Compara cada contexto en la matriz especificada de la manera indicada por las marcas de comparación, devolviendo un índice del primer contexto que coincida con el contexto de memoria.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Compare( 
   CONTEXT_COMPARE        compare,
   IDebugMemoryContext2** rgpMemoryContextSet,
   DWORD                  dwMemoryContextSetLen,
   DWORD*                 pdwMemoryContext
);
```

```csharp
int Compare(
   enum_CONTEXT_COMPARE   compare,
   IDebugMemoryContext2[] rgpMemoryContextSet,
   uint                   dwMemoryContextSetLen,
   out uint               pdwMemoryContext
);
```

#### <a name="parameters"></a>Parámetros
 `compare`

 [in] Un valor de la [CONTEXT_COMPARE](../../../extensibility/debugger/reference/context-compare.md) enumeración que determina el tipo de comparación.

 `rgpMemoryContextSet`

 [in] Una matriz de referencias a la [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md) objetos que se va a comparar.

 `dwMemoryContextSetLen`

 [in] El número de contextos en los `rgpMemoryContextSet` matriz.

 `pdwMemoryContext`

 [out] Devuelve el índice del primer contexto de memoria que satisface la comparación.

## <a name="return-value"></a>Valor devuelto
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve un código de error. Devuelve `E_COMPARE_CANNOT_COMPARE` si no se pueden comparar los dos contextos.

## <a name="remarks"></a>Comentarios
 Un motor de depuración (DE) no tiene que admitir todos los tipos de comparaciones, pero debe admitir al menos `CONTEXT_EQUAL`, `CONTEXT_LESS_THAN`, `CONTEXT_GREATER_THAN` y `CONTEXT_SAME_SCOPE`.

## <a name="see-also"></a>Vea también
- [IDebugMemoryContext2](../../../extensibility/debugger/reference/idebugmemorycontext2.md)
- [CONTEXT_COMPARE](../../../extensibility/debugger/reference/context-compare.md)
---
title: IEnumDebugPorts2::Clone | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugPorts2::Clone
helpviewer_keywords:
- IEnumDebugPorts2::Clone
ms.assetid: d5ce77e8-bb99-409a-98fa-20fe5a0de25e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 572d338fb010db9d0ff4aaaeefa5c692b2262e29
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56681704"
---
# <a name="ienumdebugports2clone"></a>IEnumDebugPorts2::Clone
Devuelve una copia de la enumeración actual como un objeto independiente.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Clone(
   IEnumDebugPorts2** ppEnum
);
```

```csharp
int Clone(
   out IEnumDebugPorts2 ppEnum
);
```

#### <a name="parameters"></a>Parámetros
 `ppEnum`

 [out] Devuelve una copia de esta enumeración como un objeto independiente.

## <a name="return-value"></a>Valor devuelto
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve un código de error.

## <a name="remarks"></a>Comentarios
 La copia de la enumeración tiene el mismo estado que el original en el momento en que se llama a este método. Sin embargo, los Estados de la copia y el original son independientes y se pueden cambiar de forma individual.

## <a name="see-also"></a>Vea también
- [IEnumDebugPorts2](../../../extensibility/debugger/reference/ienumdebugports2.md)
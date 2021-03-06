---
title: IDebugAlias2::GetAppDomainId | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- GetAppDomainId
- IDebugAlias2::GetAppDomainId
ms.assetid: 23581aaa-5a53-4859-b264-eca49fc44bcd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 890e215c7e575e67a4360717851bab538966f419
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56715055"
---
# <a name="idebugalias2getappdomainid"></a>IDebugAlias2::GetAppDomainId
Recupera el identificador del dominio de aplicación.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT GetAppDomainId (
   ULONG32* pappDomainId
);
```

```csharp
int GetAppDomainId (
   out uint pappDomainId
);
```

#### <a name="parameters"></a>Parámetros
 `pappDomainId`

 [out] Devuelve el identificador de dominio de aplicación.

## <a name="return-value"></a>Valor devuelto
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve un código de error.

## <a name="remarks"></a>Comentarios
 Se crea un nuevo dominio de aplicación y de los cambios de identificador de dominio de aplicación cada vez que se reinicie la aplicación.

## <a name="see-also"></a>Vea también
- [IDebugAlias2](../../../extensibility/debugger/reference/idebugalias2.md)
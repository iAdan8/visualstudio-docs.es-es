---
title: IDebugCustomViewer::DisplayValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCustomViewer::DisplayValue
helpviewer_keywords:
- IDebugCustomViewer::DisplayValue
ms.assetid: 7a538248-5ced-450e-97cd-13fabe35fb1c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8734d97dfc8bcd7be2b12ce657071597deaea7a8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/22/2019
ms.locfileid: "56717928"
---
# <a name="idebugcustomviewerdisplayvalue"></a>IDebugCustomViewer::DisplayValue
Este método se llama para mostrar el valor especificado.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT DisplayValue(
   HWND             hwnd,
   DWORD            dwID,
   IUnknown *       pHostServices,
   IDebugProperty3* pDebugProperty);
);
```

```csharp
int DisplayValue(
   IntPtr          hwnd,
   uint            dwID,
   object          pHostServices,
   IDebugProperty3 pDebugProperty
);
```

#### <a name="parameters"></a>Parámetros
 `hwnd`

 [in] Ventana primaria

 `dwID`

 [in] Identificador de los visores personalizados que admiten más de un tipo.

 `pHostServices`

 [in] Reservado. Siempre se establece en null.

 `pDebugProperty`

 [in] Interfaz que puede usarse para recuperar el valor que se mostrará.

## <a name="return-value"></a>Valor devuelto
 Si es correcto, devuelve `S_OK`; en caso contrario, devuelve el código de error.

## <a name="remarks"></a>Comentarios
 La visualización es "modal" en que este método crea la ventana es necesaria, mostrar el valor, esperar la entrada y cerrar la ventana, todos antes de devolver al llamador. Esto significa que el método debe controlar todos los aspectos de mostrar el valor de propiedad, desde la creación de una ventana de salida a la espera de entrada del usuario, para destruir la ventana.

 Que se pueden cambiar el valor en el determinado [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) objeto, puede usar el [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3-setvalueasstringwitherror.md) método, si el valor se puede expresar como una cadena. En caso contrario, es necesario crear una interfaz personalizada, exclusivo para el evaluador de expresiones de esta implementación `DisplayValue` método, en el mismo objeto que implementa el `IDebugProperty3` interfaz. Esta interfaz personalizada podría proporcionar métodos para cambiar los datos de un tamaño arbitrario o complejidad.

## <a name="see-also"></a>Vea también
- [IDebugCustomViewer](../../../extensibility/debugger/reference/idebugcustomviewer.md)
- [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)
- [SetValueAsStringWithError](../../../extensibility/debugger/reference/idebugproperty3-setvalueasstringwitherror.md)
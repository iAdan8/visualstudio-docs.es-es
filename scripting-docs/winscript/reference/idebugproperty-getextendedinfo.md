---
title: IDebugProperty::GetExtendedInfo | Documentos de Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugProperty.GetExtendedInfo
apilocation:
- scrobj.dll
helpviewer_keywords:
- IDebugProperty::GetExtendedInfo
ms.assetid: a989ade5-16d5-4ee6-8d8a-8dcbfad24034
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6dc3fc90b8f5fa465715bc4b9466da472cbbb580
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "54086546"
---
# <a name="idebugpropertygetextendedinfo"></a>IDebugProperty::GetExtendedInfo
Obtiene información de la propiedad extendida.  
  
## <a name="syntax"></a>Sintaxis  
  
```cpp
HRESULT GetExtendedInfo (  
   ULONG  cInfos,  
   GUID*  rgguidExtendedInfo,  
   VARIANT* pExtendedInfo  
);  
```  
  
#### <a name="parameters"></a>Parámetros  
 `cInfos`  
 [in] Recuento de objetos de información extendida.  
  
 `rgguidExtendedInfo`  
 [in] Una matriz de `GUID`s se pasa por lo que se pueden recuperar varios elementos de información ampliada al mismo tiempo.  
  
 `pExtendedInfo`  
 [out] Devuelve una matriz de `VARIANT`s que puede usarse para recuperar la información de la propiedad extendida.  
  
## <a name="return-value"></a>Valor devuelto  
 Devuelve un válidas `HRESULT`, normalmente `S_OK`.  
  
## <a name="remarks"></a>Comentarios  
 Esta interfaz obtiene información de este objeto extendida. La API existe solo con el fin de recuperar la información que no se presta a que se va a recuperar mediante el uso de `IDebugProperty::GetPropertyInfo`).  
  
## <a name="see-also"></a>Vea también  
 [IDebugProperty (Interfaz)](../../winscript/reference/idebugproperty-interface.md)
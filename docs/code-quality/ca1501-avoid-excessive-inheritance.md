---
title: 'CA1501: Evitar una herencia excesiva'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1501
- AvoidExcessiveInheritance
helpviewer_keywords:
- AvoidExcessiveInheritance
- CA1501
ms.assetid: 9e934746-1a4d-492a-91e4-085201abafa4
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: bc51b4c84ca38c0fb4e5837e3bcdf1f28a045747
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55947489"
---
# <a name="ca1501-avoid-excessive-inheritance"></a>CA1501: Evitar una herencia excesiva

|||
|-|-|
|TypeName|AvoidExcessiveInheritance|
|Identificador de comprobación|CA1501|
|Categoría|Microsoft.Maintainability|
|Cambio problemático|Problemático|

## <a name="cause"></a>Motivo
 Un tipo tiene más de cuatro niveles de profundidad en su jerarquía de herencia.

## <a name="rule-description"></a>Descripción de la regla
 Las jerarquías de tipos con demasiados niveles de anidación pueden resultar difíciles de seguir, comprender y mantener. Esta regla limita analysis a jerarquías en el mismo módulo.

## <a name="how-to-fix-violations"></a>Cómo corregir infracciones
 Para corregir una infracción de esta regla, derive el tipo de un tipo base que es menos profundo en la jerarquía de herencia o eliminar algunos de los tipos base intermedios.

## <a name="when-to-suppress-warnings"></a>Cuándo Suprimir advertencias
 Es seguro suprimir una advertencia de esta regla. Sin embargo, el código sea más difícil de mantener. Tenga en cuenta que, dependiendo de la visibilidad de tipos base, resolver las infracciones de esta regla podría crear cambios importantes. Por ejemplo, la eliminación de tipos bases públicos es un cambio importante.

## <a name="example"></a>Ejemplo
 El ejemplo siguiente muestra un tipo que infringe la regla.

 [!code-csharp[FxCop.Maintainability.ExcessiveInheritance#1](../code-quality/codesnippet/CSharp/ca1501-avoid-excessive-inheritance_1.cs)]
 [!code-vb[FxCop.Maintainability.ExcessiveInheritance#1](../code-quality/codesnippet/VisualBasic/ca1501-avoid-excessive-inheritance_1.vb)]
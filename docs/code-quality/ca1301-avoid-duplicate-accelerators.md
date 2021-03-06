---
title: 'CA1301: Evitar los aceleradores duplicados'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1301
- AvoidDuplicateAccelerators
helpviewer_keywords:
- CA1301
- AvoidDuplicateAccelerators
ms.assetid: 20570a00-864b-459c-a1fa-a6e9db5f1001
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f82163b1c377df4c8c7fcbba07672312153dad9b
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/08/2019
ms.locfileid: "55916549"
---
# <a name="ca1301-avoid-duplicate-accelerators"></a>CA1301: Evitar los aceleradores duplicados

|||
|-|-|
|TypeName|AvoidDuplicateAccelerators|
|Identificador de comprobación|CA1301|
|Categoría|Microsoft.Globalization|
|Cambio problemático|Poco problemático|

## <a name="cause"></a>Motivo
 Extiende un tipo <xref:System.Windows.Forms.Control?displayProperty=fullName> y contiene dos o más controles de nivel superior que tienen claves de acceso idénticas que se almacenan en un archivo de recursos.

## <a name="rule-description"></a>Descripción de la regla

Una clave de acceso, también conocido como un acelerador, permite el acceso mediante teclado a un control mediante la **Alt** clave. Cuando varios controles tienen la misma clave de acceso, el comportamiento de la clave de acceso no está bien definido. El usuario no pueda obtener acceso al control deseado mediante el uso de la clave de acceso, y puede habilitarse un control diferente al que está diseñado.

La implementación actual de esta regla omite los elementos de menú. Sin embargo, los elementos de menú en el mismo submenú no deberían tener teclas de acceso idénticas.

## <a name="how-to-fix-violations"></a>Cómo corregir infracciones
 Para corregir una infracción de esta regla, definir teclas de acceso único para todos los controles.

## <a name="when-to-suppress-warnings"></a>Cuándo Suprimir advertencias
 No suprima las advertencias de esta regla.

## <a name="example"></a>Ejemplo
 El ejemplo siguiente muestra un formulario mínimo que contiene dos controles que tienen claves de acceso idénticas. Las claves se almacenan en un archivo de recursos que no se muestra. Sin embargo, sus valores se mostrarán en la comentada out `checkBox.Text` líneas. El comportamiento de aceleradores duplicados puede examinarse intercambiando el `checkBox.Text` líneas con sus homólogos comentadas. Sin embargo, en este caso, el ejemplo no generará una advertencia de la regla.

 [!code-csharp[FxCop.Globalization.AvoidDuplicateAccels#1](../code-quality/codesnippet/CSharp/ca1301-avoid-duplicate-accelerators_1.cs)]

## <a name="see-also"></a>Vea también

- <xref:System.Resources.ResourceManager?displayProperty=fullName>
- [Recursos de aplicaciones de escritorio](/dotnet/framework/resources/index)
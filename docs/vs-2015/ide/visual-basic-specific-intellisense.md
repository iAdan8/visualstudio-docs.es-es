---
title: Opciones de IntelliSense específicas de Visual Basic | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- IntelliSense [Visual Basic]
- IntelliSense [Visual Studio], Visual Basic
ms.assetid: 4dec8753-05e5-4f74-b304-5f8c4ed8723b
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: 9bae55b10695ba73fec86d7ab63943e3440e3f05
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47581579"
---
# <a name="visual-basic-specific-intellisense"></a>Opciones de IntelliSense específicas de Visual Basic
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [Visual Basic-Specific IntelliSense](https://docs.microsoft.com/visualstudio/ide/visual-basic-specific-intellisense).  
  
El editor de código fuente de Visual Basic ofrece las siguientes características de IntelliSense:  
  
-   Sugerencias de sintaxis  
  
     Las sugerencias de sintaxis muestran la sintaxis de la instrucción que está escribiendo. Es útil para instrucciones como [Declare](http://msdn.microsoft.com/library/d3f21fb0-b804-4c99-97ed-583b23894cf1).  
  
## <a name="automatic-completion"></a>Finalización automática  
  
-   Finalización de varias palabras clave  
  
     Por ejemplo, si escribe `goto` y un espacio, IntelliSense mostrará una lista de las etiquetas definidas en un menú desplegable. Otras palabras clave admitidas son `Exit`, `Implements`, `Option` y `Declare`.  
  
-   Finalización de `Enum` y `Boolean`  
  
     Si una instrucción va a hacer referencia a un miembro de una enumeración, IntelliSense mostrará una lista de los miembros de `Enum`. Si una instrucción va a hacer referencia a un `Boolean`, IntelliSense mostrará un menú desplegable con los valores true y false.  
  
 La finalización se puede desactivar de forma predeterminada al anular la selección de **Lista de miembros automática** en la página de propiedades **General** de la carpeta **Visual Basic**.  
  
 Puede invocar manualmente la finalización al invocar Lista de miembros, Palabra completa o ALT+FLECHA DERECHA. Para obtener más información, vea [Usar IntelliSense](../ide/using-intellisense.md).  
  
## <a name="intellisense-in-zone"></a>IntelliSense en zona  
 IntelliSense en zona ayuda a los desarrolladores de Visual Basic que necesitan implementar aplicaciones a través de [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] y están restringidos a configuraciones de confianza parcial. Esta característica:  
  
-   Le permite elegir los permisos con los que se ejecutará la aplicación.  
  
-   Muestra las API de la zona elegida como disponibles en Lista de miembros y las API que requieren permisos adicionales como no disponibles.  
  
 Para más información, vea [Code Access Security for ClickOnce Applications](../deployment/code-access-security-for-clickonce-applications.md) (Seguridad de acceso del código para aplicaciones ClickOnce).  
  
## <a name="see-also"></a>Vea también  
 [Usar IntelliSense](../ide/using-intellisense.md)



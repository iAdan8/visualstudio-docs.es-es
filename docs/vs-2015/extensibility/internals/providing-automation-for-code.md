---
title: Provisión de automatización de código | Documentos de Microsoft
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- CodeModel object
ms.assetid: 21cb3e63-f25c-404b-bc1d-a32ad0fdd4d5
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 456927337331c15b3392b03175d83f2a63f87e77
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47565621"
---
# <a name="providing-automation-for-code"></a>Provisión de automatización para código
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [proporcionar automatización para código](https://docs.microsoft.com/visualstudio/extensibility/internals/providing-automation-for-code).  
  
No es necesario crear un modelo de automatización para el código. El SDK del entorno no proporciona un ejemplo para hacerlo. Para obtener información sobre los modelos de código, vea el <xref:EnvDTE.CodeModel> objeto.  
  
 Para implementar un modelo de código, debe implementar las interfaces que están determinadas por la estructura de datos interna. Los objetos que se deben derivar de la `IDispatch` clase.  
  
 Los objetos que se amplían, <xref:EnvDTE.CodeModel> y <xref:EnvDTE.FileCodeModel>, están disponibles desde el <xref:EnvDTE.Project> de objetos y el aspecto siguiente:  
  
 <xref:EnvDTE.Project.CodeModel%2A>  
  
 <xref:EnvDTE.ProjectItem.FileCodeModel%2A>  
  
 Puede optar por implementar simplemente el `CodeModel` o `FileCodeModel` interfaz en el objeto que se devuelve desde su `Project` y <xref:EnvDTE.ProjectItem> objetos. Proporciona funcionalidad de esta interfaz que sea adecuada para el sistema del proyecto.  
  
 Si desea agregar características, como métodos o propiedades, que no están disponibles en el estándar `CodeModel` y `FileCodeModel` interfaces, cree su propia interfaz que hereda de la norma. No olvide documentó con el sistema del proyecto para que los usuarios finales para buscar lo sepa. Devolver la interfaz estándar, pero el usuario puede llamar a la `QueryInterface` método o la conversión a la interfaz si se sabe que existe.  
  
## <a name="see-also"></a>Vea también  
 [Información general del modelo de automatización](../../extensibility/internals/automation-model-overview.md)

---
title: Registrar y anular el registro de VSPackages | Microsoft Docs
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
- registration, VSPackages
- VSPackages, registering
ms.assetid: e25e7a46-6a55-4726-8def-ca316f553d6b
caps.latest.revision: 36
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 8995bbb47f9a65a101256029a28313768a0b04ab
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47575650"
---
# <a name="registering-and-unregistering-vspackages"></a>Registro y anulación del registro de VSPackages
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [registrar y anular el registro de VSPackages](https://docs.microsoft.com/visualstudio/extensibility/registering-and-unregistering-vspackages).  
  
Usar atributos para registrar un VSPackage, pero  
  
## <a name="registering-a-vspackage"></a>Registrar un VSPackage  
 Puede usar atributos para controlar el registro de VSPackages administrados. Toda la información de registro se encuentra en un archivo .pkgdef. Para obtener más información sobre el registro de archivo, consulte [utilidad CreatePkgDef](../extensibility/internals/createpkgdef-utility.md).  
  
 El código siguiente muestra cómo utilizar los atributos de registro estándar para registrar el VSPackage.  
  
```csharp  
[PackageRegistration(UseManagedResourcesOnly = true)]  
[Guid("0B81D86C-0A85-4f30-9B26-DD2616447F95")]  
public sealed class BasicPackage : Package  
{. . .}  
```  
  
## <a name="unregistering-an-extension"></a>Anular el registro de una extensión  
 Si ha estado experimentando con una gran cantidad de VSPackages diferentes y eliminarlos de la instancia experimental, puede ejecutar simplemente el **restablecer** comando. Busque **restablecer la instancia Experimental de Visual Studio** en la página de inicio del equipo, o ejecute este comando desde la línea de comandos:  
  
```vb  
<location of Visual Studio 2015 install>\"Microsoft Visual Studio 14.0\VSSDK\VisualStudioIntegration\Tools\Bin\CreateExpInstance.exe" /Reset /VSInstance=14.0 /RootSuffix=Exp  
```  
  
 Si desea desinstalar una extensión que ha instalado en su instancia de desarrollo de Visual Studio, vaya a **herramientas / extensiones y actualizaciones**, busque la extensión y haga clic en **desinstalar**.  
  
 Si por algún motivo, ninguno de estos métodos es correcta al desinstalar la extensión, puede anular el registro del ensamblado de VSPackage desde la línea de comandos como sigue:  
  
```  
<location of Visual Studio 2015 install>\"Microsoft Visual Studio 14.0\VSSDK\VisualStudioIntegration\Tools\Bin\regpkg” /unregister <pathToVSPackage assembly>  
```  
  
## <a name="see-also"></a>Vea también  
 [VSPackages](../extensibility/internals/vspackages.md)

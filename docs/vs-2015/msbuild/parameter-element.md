---
title: Elemento Parameter | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Parameter element [MSBuild]
- <Parameter> element [MSBuild]
ms.assetid: b273afff-b500-4e97-8cfd-31f39fa64a51
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d76991809f5793ec150fa71aa4a30456f096ec44
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47576901"
---
# <a name="parameter-element"></a>Parameter (Elemento)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [elemento Parameter](https://docs.microsoft.com/visualstudio/msbuild/parameter-element).  
  
  
Contiene información sobre un parámetro específico para una tarea que se genera mediante `UsingTask``TaskFactory`.  El nombre del elemento es el nombre del parámetro.  Para más información, consulte [Elemento UsingTask (MSBuild)](../msbuild/usingtask-element-msbuild.md).  
  
 \<Project>  
 \<UsingTask>  
 \<ParameterGroup>  
 \<Parameter>  
  
## <a name="syntax"></a>Sintaxis  
  
```  
<ParameterGroup ParameterType="SystemType"  
    Output="true/false"  
    Required="true/false" />  
```  
  
## <a name="attributes-and-elements"></a>Atributos y elementos  
 En las siguientes secciones se describen los atributos, los elementos secundarios y los elementos primarios.  
  
### <a name="attributes"></a>Atributos  
  
|Atributo|Descripción|  
|---------------|-----------------|  
|`ParameterType`|Atributo opcional.<br /><br /> El tipo .NET del parámetro, por ejemplo, "System.String".|  
|`Output`|Atributo Boolean opcional.<br /><br /> Si es `true`, este parámetro es un parámetro de salida para la tarea. De forma predeterminada, el valor es `false`.|  
|`Required`|Atributo Boolean opcional.<br /><br /> Si es `true`, este parámetro es un parámetro necesario para la tarea. De forma predeterminada, el valor es `false`.|  
  
### <a name="child-elements"></a>Elementos secundarios  
 Ninguno.  
  
### <a name="parent-elements"></a>Elementos primarios  
  
|Elemento|Descripción|  
|-------------|-----------------|  
|[ParameterGroup](../msbuild/parametergroup-element.md)|Contiene una lista opcional de parámetros que estarán presentes en la tarea generada por `UsingTask``TaskFactory`.|  
  
## <a name="example"></a>Ejemplo  
 El ejemplo siguiente muestra cómo usar el elemento `Parameter`.  
  
```  
<UsingTask TaskName="MyTask" AssemblyName="My.Assembly" TaskFactory="MyTaskFactory">  
       <ParameterGroup>  
              <Parameter1 ParameterType="System.String" Required="False" Output="False"/>  
              <Parameter2 ParameterType="System.Int" Required="True" Output="False"/>  
             ...  
</ParameterGroup>  
       <TaskBody Evaluate="true">  
      ... Task factory-specific data ...  
       </TaskBody>  
</UsingTask>  
```  
  
## <a name="see-also"></a>Vea también  
 [Tareas](../msbuild/msbuild-tasks.md)   
 [Referencia de tareas](../msbuild/msbuild-task-reference.md)   
 [Referencia de esquemas de archivo del proyecto](../msbuild/msbuild-project-file-schema-reference.md)



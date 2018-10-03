---
title: Evaluación de expresiones en modo de interrupción | Microsoft Docs
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
- break mode, expression evaluation
- debugging [Debugging SDK], expression evaluation
- expression evaluation, break mode
ms.assetid: 34fe5b58-15d5-4387-a266-72120f90a4b6
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a74119edfb390dab0a8ce0fddd96046ca80ad92d
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/22/2018
ms.locfileid: "47582966"
---
# <a name="expression-evaluation-in-break-mode"></a>Evaluación de expresiones en el modo de interrupción
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

La versión más reciente de este tema puede encontrarse en [evaluación de expresiones en modo de interrupción](https://docs.microsoft.com/visualstudio/extensibility/debugger/expression-evaluation-in-break-mode).  
  
El siguiente describe el proceso que se produce cuando el depurador está en modo de interrupción y debe llevar a cabo la evaluación de expresiones.  
  
## <a name="expression-evaluation-process"></a>Proceso de evaluación de expresión  
 Estos son los pasos básicos para evaluar una expresión:  
  
1.  El Administrador de depuración de la sesión (SDM) llama a [IDebugStackFrame2::GetExpressionContext](../../extensibility/debugger/reference/idebugstackframe2-getexpressioncontext.md) para obtener una interfaz de contexto de expresión [IDebugExpressionContext2](../../extensibility/debugger/reference/idebugexpressioncontext2.md).  
  
2.  A continuación, llama el SDM [IDebugExpressionContext2::ParseText](../../extensibility/debugger/reference/idebugexpressioncontext2-parsetext.md) con la cadena que se va a analizar.  
  
3.  Si ParseText no devuelve S_OK, se devuelve el motivo del error.  
  
     -en caso contrario-  
  
     Si ParseText devuelva S_OK, el SDM, a continuación, puede llamar [IDebugExpression2::EvaluateSync](../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) o [IDebugExpression2::EvaluateAsync](../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) para obtener un valor final de la expresión analizada.  
  
    -   En el caso de uso `IDebugExpression2::EvaluateSync`, la interfaz de devolución de llamada especificada se utiliza para comunicar el proceso de evaluación en curso. Se devuelve el valor final en un [IDebugProperty2](../../extensibility/debugger/reference/idebugproperty2.md) interfaz.  
  
    -   En el caso de uso `IDebugExpression2::EvaluateAsync`, la interfaz de devolución de llamada especificada se utiliza para comunicar el proceso de evaluación en curso. Una vez completada la evaluación, EvaluateAsync envía un [IDebugExpressionEvaluationCompleteEvent2](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2.md) interfaz a través de la devolución de llamada. Con esta interfaz de eventos, se puede obtener el valor final con [GetResult](../../extensibility/debugger/reference/idebugexpressionevaluationcompleteevent2-getresult.md).  
  
## <a name="see-also"></a>Vea también  
 [Llamada a eventos del depurador](../../extensibility/debugger/calling-debugger-events.md)

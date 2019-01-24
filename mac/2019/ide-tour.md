---
title: Paseo por Visual Studio para Mac
description: Visual Studio para Mac proporciona un entorno de desarrollo integrado para compilar aplicaciones .NET en macOS, incluidos sitios web de ASP.NET Core y proyectos de Xamarin para iOS, Android, Mac y Xamarin.Forms.
author: conceptdev
ms.author: crdun
ms.date: 11/03/2018
ms.assetid: 7DC64A52-AA41-4F3A-A8A1-8A20BCD81CC7
ms.openlocfilehash: 54b3c3ac265f00ba0fb5a9d95e65ed3913eb5c9c
ms.sourcegitcommit: 5a65ca6688a2ebb36564657d2d73c4b4f2d15c34
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/15/2019
ms.locfileid: "54315843"
---
# <a name="visual-studio-2019-for-mac-preview-tour"></a>Paseo por la versión preliminar de Visual Studio 2019 para Mac

> [!NOTE]
> Visual Studio 2019 para Mac [ya está disponible](installation.md) para su instalación y pruebas.

Visual Studio para Mac convierte el IDE centrado en dispositivos móviles de Xamarin, Xamarin Studio, en un entorno de desarrollo con un enfoque de primero móvil, primero en la nube en el equipo Mac. Esta herramienta para desarrolladores permite utilizar la eficacia de .NET para crear aplicaciones para todas las plataformas que exigen los usuarios.

La experiencia de usuario (UX) de Visual Studio para Mac es similar a la de su equivalente de Windows, pero con una sensación de macOS nativo. La creación, la apertura y el desarrollo de una aplicación son experiencias familiares para cualquiera que haya usado anteriormente Visual Studio en Windows. Además, Visual Studio para Mac emplea muchas de las eficaces herramientas que convierten a su equivalente de Windows en un IDE tan eficaz. La plataforma de compilador Roslyn se usa para la refactorización e IntelliSense. El sistema del proyecto y el motor de compilación usan MSBuild y el editor de código fuente es compatible con los paquetes de TextMate. Usa los mismos motores de depuración para las aplicaciones .NET Core y Xamarin y los mismos diseñadores para Xamarin.iOS y Xamarin.Android.

En este artículo se analizan varias secciones de Visual Studio para Mac y se ofrece una visión general de algunas de las características que lo convierten en una herramienta eficaz para crear aplicaciones multiplataforma.

## <a name="ide-tour"></a>Paseo por el IDE

Visual Studio para Mac se organiza en varias secciones para administrar archivos de aplicación y configuraciones, crear código de aplicación y depurar.

## <a name="new-start-window"></a>Nueva ventana de inicio

Al iniciar la versión preliminar de Visual Studio 2019 para Mac, los nuevos usuarios verán una ventana de inicio de sesión. Inicie sesión con una cuenta Microsoft para activar una licencia de pago, si tiene una, o haga clic en el vínculo para consultar las suscripciones de Azure. Puede presionar **Omitir** e iniciar sesión más adelante en el elemento de menú **Visual Studio > Iniciar sesión**:

![Inicio de sesión en su cuenta Microsoft](media/ide-tour-2019-start-signin.png)

Los usuarios que hayan iniciado sesión verán la nueva _ventana de inicio_, en la que se muestra una lista de proyectos recientes y botones para abrir un proyecto existente o crear uno:

![Elección entre proyectos recientes o creación de uno nuevo](media/ide-tour-2019-start-projects.png)

## <a name="solutions-and-projects"></a>Soluciones y proyectos

En la imagen siguiente, se muestra Visual Studio para Mac con una aplicación cargada:

![Visual Studio para Mac con una aplicación cargada](media/ide-tour-image17.png)

En las secciones siguientes se proporciona una introducción a las áreas principales de Visual Studio para Mac.

## <a name="solution-pad"></a>Panel de solución

El Panel de solución organiza los proyectos de una solución:

![Proyectos organizados en el Panel de solución](media/ide-tour-image18.png)

Aquí es donde se organizan los archivos por el código fuente, los recursos, la interfaz de usuario y las dependencias en proyectos específicos de plataforma.

Para más información sobre el uso de proyectos y soluciones en Visual Studio para Mac, consulte el artículo [Proyectos y soluciones](/visualstudio/mac/projects-and-solutions).

## <a name="assembly-references"></a>Referencias de ensamblado

Las referencias de ensamblado de cada proyecto están disponibles en la carpeta Referencias:

![Carpeta Referencias del Panel de solución](media/ide-tour-image19.png)

Se pueden agregar otras referencias con el cuadro de diálogo **Editar referencias**. Para mostrarlo, haga doble clic en la carpeta Referencias o seleccione **Editar referencias** en las acciones del menú contextual:

![Cuadro de diálogo Editar referencias](media/ide-tour-image20.png)

Para más información sobre el uso de referencias en Visual Studio para Mac, consulte el artículo [Administrar referencias en un proyecto](/visualstudio/mac/managing-references-in-a-project).

## <a name="dependencies--packages"></a>Dependencias o paquetes

Todas las dependencias externas usadas en la aplicación se almacenan en la carpeta Dependencias o Paquetes, según si el usuario se encuentra en un proyecto de .Net Core o de Xamarin.iOS/Xamarin.Android. Normalmente se proporcionan en forma de NuGet.

NuGet es el administrador de paquetes más popular para el desarrollo de .NET. Con NuGet de Visual Studio, puede buscar paquetes fácilmente y agregarlos al proyecto o la aplicación.

Para agregar una dependencia a la aplicación, haga clic con el botón derecho en la carpeta Dependencias o Paquetes y seleccione **Agregar paquetes**:

![Adición de un paquete NuGet](media/ide-tour-image21.png)

En el artículo [Incluir un paquete NuGet en el proyecto](/visualstudio/mac/nuget-walkthrough) puede encontrar información sobre el uso de un paquete NuGet en una aplicación.

## <a name="refactoring"></a>Refactorización

Visual Studio para Mac proporciona dos formas útiles de refactorizar el código: acciones contextuales y análisis de código fuente. Puede obtener más información sobre ellas en el artículo [Refactorización](/visualstudio/mac/refactoring).

## <a name="debugging"></a>Depuración

Visual Studio para Mac tiene un depurador nativo que proporciona compatibilidad de depuración con aplicaciones Xamarin.iOS, Xamarin.Mac y Xamarin.Android. Visual Studio para Mac usa Mono Soft Debugger, que está implementado en el entorno de ejecución Mono, lo que permite al IDE depurar código administrado en todas las plataformas. Para más información sobre la depuración, visite el artículo [Depuración](/visualstudio/mac/debugging).

El depurador contiene visualizadores completos para tipos especiales, como cadenas, colores, direcciones URL, además de tamaños, coordenadas y curvas Bézier.

Para más información sobre las visualizaciones de datos del depurador, vea el artículo [Visualizaciones de datos](/visualstudio/mac/data-visualizations).

## <a name="version-control"></a>Control de versiones

Visual Studio para Mac se integra con los sistemas de control de código fuente Git y Subversion. Los proyectos con control de código fuente se reconocen por la rama que aparece junto al nombre de la solución:

![Nombre de rama para indicar que se trata de un proyecto con control de código fuente](media/ide-tour-image22.png)

Los archivos con cambios sin confirmar tienen una anotación en sus iconos en el Panel de solución, como se muestra en la imagen siguiente:

![Archivos sin confirmar en el Panel de solución](media/ide-tour-image23.png)

Para más información sobre el uso del control de versiones en Visual Studio, consulte el artículo [Control de versiones](/visualstudio/mac/version-control).

## <a name="next-steps"></a>Pasos siguientes

- [Instalación de Visual Studio para Mac](installation.md)
- [Revisión de las cargas de trabajo disponibles](/visualstudio/mac/workloads/)

## <a name="see-also"></a>Vea también

- [IDE de Visual Studio (en Windows)](/visualstudio/ide/visual-studio-ide)
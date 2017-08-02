---
title: "Símbolos para la depuración en modo mixto de Python/C++ para Visual Studio | Microsoft Docs"
ms.custom: 
ms.date: 4/4/2017
ms.prod: visual-studio-dev15
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-python
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: be5fdf2f-b55f-488a-9772-58adfe07a7ab
caps.latest.revision: 1
author: kraigb
ms.author: kraigb
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Human Translation
ms.sourcegitcommit: adf122a478b29674dc2924dcf7d42972a5a3f52e
ms.openlocfilehash: b8bf362f506255c09468934f01a7beeef3a632dd
ms.lasthandoff: 04/10/2017

---

# <a name="installing-debugging-symbols-for-python-interpreters"></a>Instalación de símbolos de depuración para intérpretes de Python

Para proporcionar una experiencia de depuración completa, el [depurador en modo mixto de Python](debugging-mixed-mode.md) en Visual Studio necesita analizar numerosas estructuras de datos internas en el intérprete de Python que se va a usar. El propio intérprete necesita símbolos de depuración para esta tarea. Para python27.dll, por ejemplo, el archivo de símbolos correspondiente es python27.pdb; para python36.dll, el archivo de símbolos es python36.pdb. Cada versión del intérprete también proporciona archivos de símbolos para diferentes módulos.

Con Visual Studio 2017, los intérpretes "Python 3" y "Anaconda 3" instalan automáticamente sus símbolos respectivos y Visual Studio los encontrará automáticamente. Para Visual Studio 2015 y versiones anteriores, o al usar otros intérpretes, será necesario descargar los símbolos por separado y, después, apuntar Visual Studio a ellos a través del cuadro de diálogo **Herramientas > Opciones** en la pestaña **Depuración > Símbolos**. Estos pasos se detallan en las secciones siguientes.

Es posible que Visual Studio le solicite los símbolos cuando los necesite, normalmente al iniciar una sesión de depuración en modo mixto. En este caso, muestra un cuadro de diálogo con dos opciones:

- **Abrir cuadro de diálogo de configuración de símbolos** abre el cuadro de diálogo **Opciones** en la pestaña **Depuración > Símbolos**.
- **Descargar símbolos para el intérprete** abre esta página de documentación actual, en cuyo caso, seleccione **Herramientas > Opciones** y navegue hasta la pestaña **Depuración > Símbolos** para continuar.

    ![Solicitud de símbolos del depurador en modo mixto](~/python/media/mixed-mode-debugging-symbols-required.png)

## <a name="downloading-symbols"></a>Descargar símbolos

- Python 3.5 y versiones posteriores: adquiera los símbolos de depuración a través del programa de instalación de Python. Seleccione **Instalación personalizada**, haga clic en **Siguiente** para acceder a **Opciones avanzadas** y después active las casillas **Download debugging symbols** (Descargar símbolos de depuración) y **Download debug binaries** (Descargar archivos binarios de depuración):

    ![Instalador de Python 3.x que incluye símbolos de depuración](~/python/media/mixed-mode-debugging-symbols-installer35.png)

    Los archivos de símbolos (`.pdb`) se encuentran en la carpeta raíz de la instalación (los archivos de símbolos para módulos individuales también se encuentran en la carpeta `DLLs`). Por este motivo, Visual Studio los encontrará automáticamente y no se necesita realizar ningún paso adicional.

- Python 3.4.x y versiones anteriores: los símbolos están disponibles como archivos .zip que se pueden descargar desde las [distribuciones oficiales](#official-distributions) o [Enthought Canopy](#enthought-canopy), como se indica a continuación. Después de descargarlos, extraiga los archivos en una carpeta local para continuar, como una carpeta `Symbols` dentro de la carpeta de Python.

    > [!Important]
    > Los símbolos difieren entre compilaciones menores de Python y entre las compilaciones de 32 y 64 bits, por lo que querrá que las versiones coincidan. Para comprobar el intérprete que se va a usar, expanda el *nodo* **Entornos de Python** en el proyecto en el Explorador de soluciones y anote el nombre del entorno. Después, cambie a la *ventana* **Entornos de Python** y anote la ubicación de la instalación. Luego, abra una ventana de comandos en esa ubicación e inicie `python.exe`, que muestra la versión exacta y si es de 32 o 64 bits.

- Para otras distribuciones de Python de terceros, como ActiveState Python: póngase en contacto con los autores de la distribución para solicitarles los símbolos. En el caso de WinPython, incorpora el intérprete de Python estándar sin cambios, así que use los símbolos de la distribución oficial para el número de versión correspondiente.

## <a name="pointing-visual-studio-to-the-symbols"></a>Apuntar Visual Studio a los símbolos

Si ha descargado los símbolos por separado, siga estos pasos para hacer que Visual Studio sea consciente de ellos. Si ha instalado los símbolos a través del instalador de Python 3.5 o una versión posterior, Visual Studio los encontrará automáticamente.

1. Seleccione el menú **Herramientas > Opciones** y después vaya a **Depuración > Símbolos**.
    
1. Haga clic en el botón Agregar de la barra de herramientas (descrito a continuación), escriba la carpeta donde ha expandido los símbolos descargados (que es donde se encuentra `python.pdb`, por ejemplo `c:\python34\Symbols`, como se muestra a continuación) y haga clic en **Aceptar**. 

    ![Opciones de símbolos para el depurador en modo mixto](~/python/media/mixed-mode-debugging-symbols.png)

1. Durante una sesión de depuración, es posible que Visual Studio también le pida la ubicación de un archivo de origen para el intérprete de Python. Si por ejemplo los ha descargado desde [python.org/downloads](https://www.python.org/downloads), entonces también puede apuntar hacia ellos.

> [!Note]
> Las características de almacenamiento en caché de símbolos que se muestran en el cuadro de diálogo se usan para crear una caché local de símbolos obtenidos de un origen en línea. Estas características no son necesarias con los símbolos del intérprete de Python, dado que ya se habrán descargado de forma local. En cualquier caso, consulte [Specify Symbols and Source Files in the Visual Studio Debugger](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md) (Especificar símbolos y archivos de origen en el depurador de Visual Studio) para obtener más detalles.

## <a name="official-distributions"></a>Distribuciones oficiales

| Versión de Python | Descargas | 
| --- | --- | 
| 3.5 y versiones posteriores | Instale los símbolos mediante el programa de instalación de Python. | 
| 3.4.4 | [32 bits](https://www.python.org/ftp/python/3.4.4/python-3.4.4-pdb.zip) - [64 bits](https://www.python.org/ftp/python/3.4.4/python-3.4.4.amd64-pdb.zip) |
| 3.4.3 | [32 bits](https://www.python.org/ftp/python/3.4.3/python-3.4.3-pdb.zip) - [64 bits](https://www.python.org/ftp/python/3.4.3/python-3.4.3.amd64-pdb.zip) |
| 3.4.2 | [32 bits](https://www.python.org/ftp/python/3.4.2/python-3.4.2-pdb.zip) - [64 bits](https://www.python.org/ftp/python/3.4.2/python-3.4.2.amd64-pdb.zip) |
| 3.4.1 | [32 bits](https://www.python.org/ftp/python/3.4.1/python-3.4.1-pdb.zip) - [64 bits](https://www.python.org/ftp/python/3.4.1/python-3.4.1.amd64-pdb.zip) |
| 3.4.0 | [32 bits](https://www.python.org/ftp/python/3.4.0/python-3.4.0-pdb.zip) - [64 bits](https://www.python.org/ftp/python/3.4.0/python-3.4.0.amd64-pdb.zip) |
| 3.3.5 | [32 bits](http://www.python.org/ftp/python/3.3.5/python-3.3.5-pdb.zip) - [64 bits](http://www.python.org/ftp/python/3.3.5/python-3.3.5.amd64-pdb.zip) |
| 3.3.4 | [32 bits](http://python.org/ftp/python/3.3.4/python-3.3.4-pdb.zip) - [64 bits](http://python.org/ftp/python/3.3.4/python-3.3.4.amd64-pdb.zip) |
| 3.3.3 | [32 bits](http://python.org/ftp/python/3.3.3/python-3.3.3-pdb.zip) - [64 bits](http://python.org/ftp/python/3.3.3/python-3.3.3.amd64-pdb.zip) |
| 3.3.2 | [32 bits](http://python.org/ftp/python/3.3.2/python-3.3.2-pdb.zip) - [64 bits](http://python.org/ftp/python/3.3.2/python-3.3.2.amd64-pdb.zip) |
| 3.3.1 | [32 bits](http://python.org/ftp/python/3.3.1/python-3.3.1-pdb.zip) - [64 bits](http://python.org/ftp/python/3.3.1/python-3.3.1.amd64-pdb.zip) |
| 3.3.0 | [32 bits](http://python.org/ftp/python/3.3.0/python-3.3.0-pdb.zip) - [64 bits](http://python.org/ftp/python/3.3.0/python-3.3.0.amd64-pdb.zip) |
| 2.7.11 | [32 bits](https://www.python.org/ftp/python/2.7.11/python-2.7.11-pdb.zip) - [64 bits](https://www.python.org/ftp/python/2.7.11/python-2.7.11.amd64-pdb.zip) |
| 2.7.10 | [32 bits](https://www.python.org/ftp/python/2.7.10/python-2.7.10-pdb.zip) - [64 bits](https://www.python.org/ftp/python/2.7.10/python-2.7.10.amd64-pdb.zip) |
| 2.7.9 | [32 bits](https://www.python.org/ftp/python/2.7.9/python-2.7.9-pdb.zip) - [64 bits](https://www.python.org/ftp/python/2.7.9/python-2.7.9.amd64-pdb.zip) |
| 2.7.8 | [32 bits](https://www.python.org/ftp/python/2.7.8/python-2.7.8-pdb.zip) - [64 bits](https://www.python.org/ftp/python/2.7.8/python-2.7.8.amd64-pdb.zip) |
| 2.7.7 | [32 bits](https://www.python.org/ftp/python/2.7.7/python-2.7.7-pdb.zip) - [64 bits](https://www.python.org/ftp/python/2.7.7/python-2.7.7.amd64-pdb.zip) |
| 2.7.6 | [32 bits](http://python.org/ftp/python/2.7.6/python-2.7.6-pdb.zip) - [64 bits](http://python.org/ftp/python/2.7.6/python-2.7.6.amd64-pdb.zip) |
| 2.7.5 | [32 bits](http://python.org/ftp/python/2.7.5/python-2.7.5-pdb.zip) - [64 bits](http://python.org/ftp/python/2.7.5/python-2.7.5.amd64-pdb.zip) |
| 2.7.4 | [32 bits](http://python.org/ftp/python/2.7.4/python-2.7.4-pdb.zip) - [64 bits](http://python.org/ftp/python/2.7.4/python-2.7.4.amd64-pdb.zip) |
| 2.7.3 | [32 bits](http://python.org/ftp/python/2.7.3/python-2.7.3-pdb.zip) - [64 bits](http://python.org/ftp/python/2.7.3/python-2.7.3.amd64-pdb.zip) |
| 2.7.2 | [32 bits](http://python.org/ftp/python/2.7.2/python-2.7.2-pdb.zip) - [64 bits](http://python.org/ftp/python/2.7.2/python-2.7.2.amd64-pdb.zip) |
| 2.7.1 | [32 bits](http://python.org/ftp/python/2.7.1/python-2.7.1-pdb.zip) - [64 bits](http://python.org/ftp/python/2.7.1/python-2.7.1.amd64-pdb.zip) |


## <a name="enthought-canopy"></a>Enthought Canopy

Enthought Canopy ofrece símbolos para sus archivos binarios, a partir de la versión 1.2. Se instalan automáticamente junto con la distribución, pero tendrá que agregar manualmente la carpeta que los contiene en la ruta de acceso a los símbolos, como se ha descrito anteriormente. Si se trata de una instalación por usuario típica de Canopy, los símbolos se encuentran en `%UserProfile%\AppData\Local\Enthought\Canopy\User\Scripts` para la versión de 64 bits y en `%UserProfile%\AppData\Local\Enthought\Canopy32\User\Scripts` para la versión de 32 bits.

Enthought Canopy 1.1 y las versiones anteriores y Enthought Python Distribution (EPD) no proporcionan símbolos para el intérprete y, por tanto, no son compatibles con la depuración en modo mixto.
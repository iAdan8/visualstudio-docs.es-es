---
title: Accesibilidad
description: 
author: asb3993
ms.author: amburns
ms.date: 08/15/2017
ms.topic: article
ms.assetid: 2C4AAC2E-3B4A-4496-8BE0-1F5A7F81D1CA
ms.translationtype: HT
ms.sourcegitcommit: f6c7e290f0abc2c32456e076420a7695ae868ba6
ms.openlocfilehash: e0d893f155982ecd95f25ebdab768e810005b167
ms.contentlocale: es-es
ms.lasthandoff: 09/07/2017

---

# <a name="accessibility"></a>Accesibilidad

Además de las características y utilidades de macOS, Visual Studio para Mac tiene las características siguientes, por lo que es más accesible para personas con discapacidades:

- Ampliación de texto de los paneles de soluciones y de editores
- Opciones de tamaño de texto en los editores
- Personalización de colores en los editores
- Personalización de métodos abreviados de teclado
- Completado de código para métodos y parámetros 

Para más información acerca de las características de accesibilidad de macOS, consulte el [sitio web de Apple](https://www.apple.com/accessibility/mac/).

## <a name="using-accessibility-features-in-visual-studio-for-mac"></a>Uso de las características de accesibilidad de Visual Studio para Mac

De forma predeterminada, las características de accesibilidad de Visual Studio para Mac están desactivadas. Para habilitarlas, siga estos pasos:

1. Vaya a **Visual Studio > Preferencias > Otros > Accesibilidad**.

2. Active la casilla **Enable Accessibility** (Habilitar accesibilidad), como se muestra en el diagrama siguiente:

    ![Casilla para habilitar la accesibilidad](media/accessibility-image1.png)

3. Presione el botón **Reinicie Visual Studio** para que las características de accesibilidad surtan efecto.


Como alternativa, puede usar la línea de comandos para habilitar las características de accesibilidad. Para ello, especifique el comando siguiente en el terminal: 

```bash
defaults write com.microsoft.visual-studio com.monodevelop.AccessibilityEnabled 1 
```

Después de activar la accesibilidad, debe reiniciar Visual Studio.

## <a name="how-to-use-keyboard-navigation"></a>Uso de la navegación mediante el teclado

Se puede habilitar la navegación mediante el teclado mediante el establecimiento de la opción de acceso de teclado completo en **Preferencias del sistema > Teclado > Accesos directos** en **Todos los controles**:

  ![Panel de preferencias del sistema en macOS](media/accessibility-image2.png)

Si se establece el acceso de teclado completo, se activa en el rectángulo de foco. Después, se pueden seleccionar los controles mediante:
- Presione la tecla tabulador para avanzar por los controles
- Presione Mayús-Tab para retroceder por los controles
- Teclas de dirección para desplazarse entre los controles en la dirección de las flechas. 

Al presionar la barra espaciadora, se activa el control con el foco.

## <a name="how-to-enable-and-use-voice-over"></a>Habilitación y utilización de VoiceOver

Para activar o desactivar VoiceOver, presione **Cmd + F5**

Para navegar por los comandos de VoiceOver de la interfaz de usuario, use los comandos siguientes:

- Nueva el cursor de VoiceOver entre los controles: **Ctrl + Alt + tecla de dirección izquierda/tecla de dirección derecha**

VoiceOver lee el nombre de los controles, algunos detalles sobre ellos y lo que se puede hacer con ellos. 

- Especifique los grupos y controles (por ejemplo, Panel de solución, el cuadro de herramientas y otros paneles): **Ctrl + Alt + Mayús + flecha abajo**

Cuando esté dentro de un control, puede usar **Ctrl + Alt + Teclas de dirección** para desplazarse por él. 
 
Para más información sobre el uso de VoiceOver en macOS, consulte las guías siguientes:

- [Getting Started with VoiceOver](https://help.apple.com/voiceover/info/guide/10.12/) (Introducción a VoiceOver)
- [VoiceOver commands in macOS](http://lab.dotjay.com/notes/voiceover-commands/) (Comandos de VoiceOver en macOS)

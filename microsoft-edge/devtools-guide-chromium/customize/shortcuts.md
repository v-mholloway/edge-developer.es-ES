---
description: Personalice los métodos abreviados de teclado, incluidos los accesos directos que coincidan Visual Studio Code.
title: Personalizar métodos abreviados de teclado en DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, custom, shortcuts, teclado, visual studio code
ms.openlocfilehash: d2b02531c8608ca4cee787c75f9e7f0a268918546030848b20ab2050c3411c7e
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11799710"
---
# <a name="customize-keyboard-shortcuts-in-devtools"></a>Personalizar métodos abreviados de teclado en DevTools  

En la página **Accesos directos** de **Configuración,** puede ver los accesos directos definidos para Microsoft Edge DevTools, definir su propio acceso directo para una acción específica o usar un ajuste preestablecido para que coincida con los métodos abreviados predeterminados de Microsoft Visual Studio Code.

Para obtener un artículo en el que se enumeran todas las opciones de acceso directo predeterminadas, [vea Microsoft Edge DevTools keyboard shortcuts][DevToolsShortcuts].  Vea también [Personalizar DevTools][DevToolsCustomizeSettings].


## <a name="match-keyboard-shortcuts-from-visual-studio-code"></a>Coincidencia de métodos abreviados de teclado Visual Studio Code

Para hacer coincidir el método abreviado de teclado en el Microsoft Edge DevTools para una acción equivalente en Visual Studio Code:

1.  [Abra DevTools][DevtoolsOpenMain], por ejemplo, seleccionando `F12` .
1.  Abra [Configuración][DevToolsCustomizeSettings], como seleccionando el icono de engranaje en la barra de herramientas principal o seleccionando `Shift` + `?` .  
1.  Seleccione la **página Configuración de accesos directos.**
1.  En la parte superior derecha, en la lista desplegable Coincidencia **de accesos directos** de preestablecida, **seleccione** Visual Studio Code en lugar **de DevTools (predeterminado).**
    
    :::image type="complex" source="../media/match-keyboard-shortcuts-visual-studio-code.msft.png" alt-text="Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio Code" lightbox="../media/match-keyboard-shortcuts-visual-studio-code.msft.png":::
       Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio Code  
    :::image-end:::  
    
Por ejemplo, para pausar o continuar ejecutando un script en Visual Studio Code, seleccione `F5` .  Pero con el valor **preestablecido DevTools (Predeterminado),** para pausar o continuar ejecutando un script, seleccione `F8` .  Al cambiar el valor preestablecido **a Visual Studio Code,** ahora también seleccionas `F5` en DevTools, al igual que en Visual Studio Code.

### <a name="see-also"></a>Consulte también

* [Microsoft Visual Studio Código][VisualStudioCode]
* [Visual Studio Code métodos abreviados de teclado para Windows][VisualStudioCodeShortcutsKeyboardWindows] (archivo PDF)


## <a name="edit-the-keyboard-shortcut-for-a-devtools-action"></a>Editar el método abreviado de teclado para una acción DevTools

1.  [Abra DevTools][DevtoolsOpenMain], por ejemplo, seleccionando `F12` .
1.  Abra [Configuración][DevToolsCustomizeSettings], como seleccionando el icono de engranaje en la barra de herramientas principal o seleccionando `Shift` + `?` .  
1.  Seleccione la **página Configuración de accesos directos.**
1.  Seleccione la acción que desea personalizar.  Por ejemplo, en la sección **Depurador,** seleccione la **acción Pausar la** ejecución del script.  
1.  Seleccione el **icono Editar** \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Seleccione la acción que desea personalizar en la página Accesos directos de Configuración" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Seleccione la acción que desea personalizar en la página **Accesos directos** **de Configuración**
    :::image-end:::  
    
1.  Para enlazar las teclas de método abreviado a la acción, asegúrese de que el cuadro de texto situado junto a la acción tenga el foco y, a continuación, use el teclado para seleccionar las teclas de método abreviado.  
1.  Para enlazar más de una combinación de métodos abreviados a una acción, seleccione Agregar un acceso directo, asegúrese de que el cuadro de texto situado junto a la acción tenga el foco y, **a**continuación, use el teclado para seleccionar las teclas de método abreviado.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Seleccione las claves que desea asignar a la acción" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Seleccione las claves que desea asignar a la acción  
    :::image-end:::  
    
1.  Para guardar el nuevo método abreviado de teclado, seleccione la marca de verificación \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) de la marca de verificación.
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Seleccione el icono de marca de verificación para guardar el nuevo método abreviado de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Seleccione el icono de marca de verificación para guardar el nuevo método abreviado de teclado  
    :::image-end:::  
    
1.  Seleccione el nuevo método abreviado de teclado para desencadenar la acción en DevTools.  
    
En la **página Accesos directos,** el icono **Método** abreviado de teclado personalizado \( ![ CustomKeyboardShortcut \) muestra los ](../media/custom-keyboard-shortcut-icon.msft.png) métodos abreviados de teclado personalizados.  Para restablecer todos los accesos directos, **seleccione Restaurar accesos directos predeterminados.**  

Mientras edita los métodos abreviados de teclado para una acción, para descartar los cambios, seleccione el icono X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).  Para quitar accesos directos para una acción específica, seleccione el icono Eliminar **acceso directo** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).  

> [!NOTE]
> Si un método abreviado de teclado está asignado actualmente a una acción, se te bloquea que no lo guardes en otra acción.  En su lugar, elimine el método abreviado de teclado de la acción anterior y, a continuación, agrégrelo a la nueva acción.  

<!-- links -->  
[DevToolsCustomizeSettings]: ./index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abrir Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  
<!-- external links -->
[VisualStudioCode]: https://code.visualstudio.com "Microsoft Visual Studio Código"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Métodos abreviados de teclado para Windows | Microsoft Visual Studio Código"  

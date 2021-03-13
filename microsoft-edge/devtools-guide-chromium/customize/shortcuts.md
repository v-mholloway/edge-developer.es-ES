---
description: Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código
title: Personalizar los métodos abreviados de teclado en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, custom, shortcuts, teclado, visual studio code
ms.openlocfilehash: ec48b075ff6741e0905e963993e7ca4e5dabe714
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408298"
---
# <a name="customize-keyboard-shortcuts-in-the-microsoft-edge-devtools"></a>Personalizar los métodos abreviados de teclado en Microsoft Edge DevTools  

La **página Accesos directos** de [Configuración][DevToolsCustomizeSettings] proporciona una lista de métodos abreviados de teclado en [DevTools][DevToolsShortcuts] y características [para personalizar los métodos abreviados](#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code).  Para navegar a la página **Accesos directos,** siga estos pasos.  

1.  [Abra DevTools][DevtoolsOpenMain].  
1.  Abra [Configuración][DevToolsCustomizeSettings].
    *   Seleccione `Shift` + `?` .  
1.  Vaya a la **página Accesos directos.**  
    
    :::image type="complex" source="../media/settings-shortcuts.msft.png" alt-text="La página Accesos directos en Configuración" lightbox="../media/settings-shortcuts.msft.png":::
       La **página Accesos directos** en **Configuración**  
    :::image-end:::  
    
## <a name="match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code"></a>Coincidencia de métodos abreviados de teclado en DevTools con Microsoft Visual Studio Code  

Para hacer coincidir el método abreviado de teclado en Microsoft Edge DevTools para una acción equivalente en [Visual Studio Code][VisualStudioCode], siga estos pasos.  

1.  Vaya a la [página web Accesos directos.](#customize-keyboard-shortcuts-in-the-microsoft-edge-devtools)  
1.  Elija el **menú desplegable Coincidencia de accesos directos** de la lista desplegable preestablecido y cambie **DevTools (predeterminado)** **a Visual Studio code**.  
    
    :::image type="complex" source="../media/match-keyboard-shortcuts-visual-studio-code.msft.png" alt-text="Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código" lightbox="../media/match-keyboard-shortcuts-visual-studio-code.msft.png":::
       Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código  
    :::image-end:::  
    
Por ejemplo, para pausar o continuar ejecutando un script [en Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows], seleccione `F5` .  Con el **valor preestablecido DevTools (predeterminado),** para pausar o continuar ejecutando un script, seleccione `F8` .  Al cambiar el valor preestablecido **a Visual Studio Code**, ahora también selecciona , al igual que en Visual Studio `F5` [Code][VisualStudioCodeShortcutsKeyboardWindows].  

## <a name="edit-keyboard-shortcuts-for-any-action-in-the-devtools"></a>Editar métodos abreviados de teclado para cualquier acción en DevTools  

Para personalizar el método abreviado de teclado de una acción específica en DevTools, siga estos pasos.  

1.  Vaya a la [página web Accesos directos.](#customize-keyboard-shortcuts-in-the-microsoft-edge-devtools)  
1.  Elija la acción que desea personalizar.  Por ejemplo, en la sección **Depurador,** busque y seleccione la **acción Pausar la** ejecución del script.  
1.  Elija el **icono Editar** \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Elija la acción que desea personalizar en la página Accesos directos de Configuración" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Elija la acción que desea personalizar en la página [Accesos directos](#customize-keyboard-shortcuts-in-the-microsoft-edge-devtools) de [Configuración][DevToolsCustomizeSettings]  
    :::image-end:::  
    
1.  Para enlazar las teclas de método abreviado a la acción, asegúrese de que el cuadro de texto situado junto a la acción tenga el foco y, a continuación, use el teclado para seleccionar las teclas de método abreviado.  
1.  Para enlazar más de una combinación de métodos abreviados a una acción, elija Agregar un acceso directo, asegúrese de que el cuadro de texto situado junto a la acción tenga el foco y, **a**continuación, use el teclado para seleccionar las teclas de método abreviado.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Seleccione las claves que desea asignar a la acción" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Seleccione las claves que desea asignar a la acción  
    :::image-end:::  
    
1.  Para guardar el nuevo método abreviado de teclado, elija la marca de verificación \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) icono.
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado  
    :::image-end:::  
    
1.  Seleccione el nuevo método abreviado de teclado para desencadenar la acción en DevTools.  
    
En la [página Accesos directos,](#customize-keyboard-shortcuts-in-the-microsoft-edge-devtools) el icono **Método** abreviado de teclado personalizado \( ![ CustomKeyboardShortcut \) muestra los ](../media/custom-keyboard-shortcut-icon.msft.png) métodos abreviados de teclado personalizados.  Para restablecer todos los accesos directos, elija **Restaurar métodos abreviados predeterminados.**  

Mientras edita los métodos abreviados de teclado para una acción, para descartar los cambios, elija el icono X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).  Para quitar accesos directos para una acción específica, elija el icono Eliminar **acceso directo** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).  

> [!NOTE]
> Si un método abreviado de teclado está asignado actualmente a una acción, se te bloquea que no lo guardes en otra acción.  En su lugar, elimine el método abreviado de teclado de la acción anterior y, a continuación, agrégrelo a la nueva acción.  

<!-- links -->  

[DevToolsCustomizeSettings]: ./index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCode]: https://code.visualstudio.com "Microsoft Visual Studio Code"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio métodos abreviados de teclado de código para Windows | Microsoft Visual Studio Code"  

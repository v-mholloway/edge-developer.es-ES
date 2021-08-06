---
description: Una lista de las características de prueba de accesibilidad en Microsoft Edge DevTools.
title: Características de prueba de accesibilidad en DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: db386e9c4bf3f94e2f607a356acafdceb040f0833ac5f5f0cb9cc2655e5d63c1
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802606"
---
# <a name="accessibility-testing-features-in-devtools"></a>Características de prueba de accesibilidad en DevTools

Para probar la accesibilidad de las páginas web, primero haga una lista de comprobación de los aspectos de accesibilidad que se probarán y, a continuación, use las características de DevTools pertinentes para comprobar cada aspecto.

| Aspecto de accesibilidad que se debe comprobar | Característica de DevTools | Artículo o subpartida |
|---|---|---|
| Comprobar que las imágenes tienen texto alternativo | **La** herramienta Issues > **Sección de accesibilidad** del informe | [Comprobar que las imágenes tienen texto alternativo](test-issues-tool.md#verify-that-images-have-alt-text) |
| Comprobar la compatibilidad con teclado | **Inspeccionar** la sección > **accesibilidad** de superposición | [Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar sobre la página web](test-inspect-tool.md) |
| Comprobar la compatibilidad con teclado | `Tab`, `Shift+Tab` y las `Enter` claves | [Comprobar la compatibilidad con el teclado usando las teclas Tab y Enter](test-tab-enter-keys.md) |
| Comprobar la compatibilidad con el teclado: compruebe que el foco está indicado | **Herramienta Inspeccionar,** **pestaña Estilos** y **Herramienta Orígenes** | [Analizar la falta de indicación del foco del teclado en un menú lateral](test-analyze-no-focus-indicator.md) |
| Comprobar la compatibilidad con el teclado: compruebe que los botones de formulario se pueden usar con el teclado | **Inspeccionar** herramienta, **árbol DOM en** la herramienta **Elementos** y pestaña **Escuchas de** eventos | [Analizar la falta de compatibilidad con teclado en un formulario](test-analyze-no-keyboard-support.md) |
| Comprobar la compatibilidad con el teclado: comprobar `Tab` el orden de las teclas | **Herramienta Elementos** > **pestaña Accesibilidad >** Visor de pedidos de **origen** | [Probar la compatibilidad con teclado con el Visor de pedidos de origen](test-tab-key-source-order-viewer.md) |
| Compruebe que el texto tiene suficiente contraste (automáticamente, para toda la página) | **La** herramienta Issues > **Sección de accesibilidad** del informe | [Comprobar que los colores de texto tienen suficiente contraste](test-issues-tool.md#verify-that-text-colors-have-enough-contrast) |
| Comprobar que el texto tiene suficiente contraste | **Herramienta** Elementos > **de estilos >** **Selector de color** | [Probar el contraste de color de texto con el Selector de colores](color-picker.md) |
| Comprobar que el texto tiene suficiente contraste | **Inspeccionar** la sección accesibilidad **>** herramienta de superposición > **fila Contraste** | [Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar sobre la página web](test-inspect-tool.md) |
| Compruebe que el texto tiene suficiente contraste: en el estado de puntero | **La** herramienta Elements > **styles tab** > Toggle **Element State** | [Comprobar la accesibilidad de todos los estados de elementos](test-inspect-states.md) |
| Compruebe que el texto tiene suficiente contraste: con el tema oscuro (modo oscuro) y el tema claro | **Herramienta** de representación > emular la característica **multimedia CSS prefers-color-scheme** | [Comprobar si hay problemas de contraste con el tema oscuro y el tema claro](test-dark-mode.md) |
| Comprobar la compatibilidad con el lector de pantalla: compruebe que los campos de entrada tienen etiquetas | **La** herramienta Issues > **Sección de accesibilidad** del informe | [Comprobar que los campos de entrada tienen etiquetas](test-issues-tool.md#verify-that-input-fields-have-labels) |
| Comprobar la compatibilidad con el lector de pantalla | **Inspeccionar** la sección > **accesibilidad** de la superposición > **nombre** y **rol** | [Usar la herramienta Inspeccionar para detectar problemas de accesibilidad al pasar sobre la página web](test-inspect-tool.md) |
| Comprobar la compatibilidad con el lector de pantalla | **Herramienta Elementos** > **pestaña Accesibilidad >** **Árbol de accesibilidad** | [Compruebe el árbol de accesibilidad para obtener compatibilidad con el](test-accessibility-tree.md)teclado y el lector de pantalla y pruebe la [accesibilidad con la pestaña Accesibilidad](accessibility-tab.md) |
| Comprobar que la página web es utilizable por personas con ceguera de color | **Lista desplegable** > herramientas de representación **Emular deficiencias** de visión | [Verificar si las personas con daltonismo pueden utilizar la página](test-color-blindness.md) |
| Comprobar que la página web es utilizable con la visión borrosa | **Lista desplegable** > herramientas de representación **Emular deficiencias** de visión | [Verificar si la página se puede utilizar con la visión borrosa](test-blurred-vision.md) |
| Comprobar que la página web se puede usar con la animación de la interfaz de usuario desactivada (movimiento reducido) | **La** herramienta de > **emular la característica multimedia CSS prefiere el movimiento reducido** | [Verificar si la página se puede usar con la animación de la interfaz de usuario desactivada](test-reduced-ui-motion.md) |
| Comprobar que el diseño de la página web es utilizable cuando es estrecho | **Herramienta de emulación de** dispositivos | [Compruebe que el diseño de la página web es utilizable cuando es estrecho](accessibility-testing-in-devtools.md#verify-that-the-webpage-layout-is-usable-when-narrow)y Emular dispositivos móviles [en Microsoft Edge DevTools](../device-mode/index.md) |


## <a name="see-also"></a>Consulte también

*   [Información general sobre las pruebas de accesibilidad con DevTools][DevtoolsAccessibilityAccessibilitytestingindevtools]
*   [Navegar Microsoft Edge DevTools con tecnología de asistencia][DevtoolsAccessibilityNavigation]
*   [Pruebas de accesibilidad][DevtoolsAccessibilityTest]
*   [Principios y procedimientos recomendados de accesibilidad][MDNAccessibility]
*   [Lector de pantalla][MDNScreenReader]


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->  
[DevtoolsAccessibilityTest]: ../../accessibility/test.md "Pruebas de accesibilidad | Microsoft Docs"
[DevtoolsAccessibilityAccessibilitytestingindevtools]: accessibility-testing-in-devtools.md "Información general sobre las pruebas de accesibilidad con DevTools | Microsoft Docs"
[DevtoolsAccessibilityNavigation]: ./navigation.md "Navegue Microsoft Edge DevTools con tecnología de asistencia | Microsoft Docs"  
<!-- external -->
[MDNAccessibility]: https://developer.mozilla.org/docs/Web/Accessibility "Accesibilidad | MDN"  
[MDNScreenReader]: https://developer.mozilla.org/docs/Glossary/Screen_reader "Lector de pantalla | MDN"  

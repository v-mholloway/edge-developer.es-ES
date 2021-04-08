---
description: Conozca las herramientas para desarrolladores de Microsoft Edge (Chromium)
title: Introducción a Microsoft Edge (Chromium) Developer Tools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 3d91b0754f84579d770940503cf4a252e3926416
ms.sourcegitcommit: fa8bedfc83fbd1c4ce7bda8c69586c4f24007beb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "11481473"
---
# <a name="microsoft-edge-chromium-developer-tools-overview"></a>Introducción a Microsoft Edge (Chromium) Developer Tools  

Al instalar Microsoft Edge, obtiene un explorador. Además, obtiene una forma eficaz de inspeccionar, depurar e incluso crear proyectos web.  Las herramientas para desarrolladores que se suministran con el explorador se basan en las herramientas del proyecto de código abierto Chromium, por lo que es posible que ya esté familiarizado con las herramientas.  Para que las descripciones sean más cortas en este artículo, ahora se `Microsoft Edge Developer Tools` `DevTools` denominan .  

Use DevTools para revisar y obtener más información sobre las siguientes tareas de desarrollo.  

*   [Inspeccione y cambie la página web actual][DevtoolsGuideDomIndex] en directo en el explorador.  
*   [Emula el comportamiento del producto en diferentes dispositivos][DevtoolsGuideDeviceModeIndex] y simula un entorno móvil completo con diferentes condiciones de red.  
*   [Inspeccionar, ajustar y cambiar los estilos de los][DevtoolsGuideInspectStylesEditFonts] elementos de la página web mediante herramientas en directo con una interfaz visual.  
*   [Depure su JavaScript][DevtoolsGuideJavascriptIndex] mediante la depuración de puntos de interrupción y con la [consola en directo][DevtoolsGuideConsoleIndex].  
*   Encuentre [problemas de accesibilidad, rendimiento, compatibilidad][DevtoolsGuideIssuesIndex] y seguridad en sus productos y aprenda a usar DevTools para corregir cada uno de ellos.  
*   [Inspeccione el tráfico de red][DevtoolsGuideNetworkIndex] y revise la ubicación de los problemas.  
*   [Inspeccione dónde el explorador almacenaba el contenido][DevtoolsGuideStorageSessionstorage] en varios formatos.  
*   [Evalúe el rendimiento][DevtoolsGuideEvaluatePerformanceIndex] del producto para encontrar problemas [de memoria y][DevtoolsGuideMemoryProblemsIndex] de [representación.][DevtoolsGuideRenderingToolsIndex]  
*   [Use un entorno de desarrollo][DevtoolsGuideSourcesIndex] para sincronizar los cambios en [DevTools con el sistema de archivos][DevtoolsGuideWorkspacesIndex] y invalidar los [archivos][DevtoolsGuideJavascriptOverrides] de la web.  
    
<!-- Is the link meant to be local or session storage for "inspect where the browser stored content"? -->  

Y mucho más.  Todo se inicia al abrir DevTools y personalizar cada herramienta según sus necesidades.  

## <a name="open-the-devtools"></a>Abrir devTools  

Para abrir y explorar DevTools, use una de las siguientes acciones.  

*   Mantenga el mouse en cualquier elemento de la página web, abra el menú contextual \(clic con el botón secundario\) y, a continuación, elija **Inspeccionar**.  Esta acción abre la **herramienta** Elementos.  
*   Seleccione `F12` .  
*   Selecciona `Ctrl` + `Shift` + `I` en Windows/Linux o `Command` + `Option` + `I` en macOS.  
    
:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-inspect.msft.png" alt-text="Elija Inspeccionar en el menú contextual de cualquier elemento" lightbox="./media/devtools-intro-inspect.msft.png":::  
         Elija **Inspeccionar** en el menú contextual de cualquier elemento  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-inspect-devtools-open.png" alt-text="DevTools se abre con el elemento seleccionado resaltado" lightbox="./media/devtools-intro-inspect-devtools-open.png":::  
         DevTools se abre con el elemento seleccionado resaltado  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

Hay dos formas principales de interactuar con DevTools.
*   Usar el mouse  
*   [Métodos abreviados de teclado][DevtoolsGuideShortcutsIndex].  Los métodos abreviados de teclado proporcionan una forma rápida de acceder a la funcionalidad y son necesarios para la accesibilidad.  El equipo de Microsoft Edge DevTools trabaja duro para que todas las herramientas estén disponibles con el teclado y las tecnologías de asistencia, como los lectores de pantalla.  Para obtener más información acerca de cómo abrir las diferentes características de DevTools, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsGuideOpenIndex].  

## <a name="dock-the-devtools-in-your-browser"></a>Acoplar las DevTools en el explorador  

Al abrir DevTools, se acopla a la izquierda del explorador.  Para cambiar la ubicación acoplada de DevTools, realice las siguientes acciones.  

1.  Elija el **botón Personalizar y controlar DevTools** \( `...` \).  
1.  A la derecha de **Placement de DevTools con relación** a la página \( Dock**side**\), elija una opción **dock side.**  
    
Para obtener más información, vaya a Cambiar la ubicación [de Microsoft Edge DevTools (Undock, Dock To Bottom, Dock To Left).][DevtoolsGuideCustomizePlacement]  

:::image type="complex" source="./media/devtools-intro-docking-menu.msft.png" alt-text="Captura de pantalla del menú lateral Dock en DevTools" lightbox="./media/devtools-intro-docking-menu.msft.png":::  
   Captura de pantalla del menú lateral Dock en DevTools  
:::image-end:::  

En **dock side**, elija cualquiera de las siguientes opciones de diseño.  

*   **Desacoplar en una ventana independiente**.   Te ayuda a trabajar con varios monitores o si necesitas trabajar en una aplicación de pantalla completa.  
*   **Acoplar a la izquierda** **o Acoplar a la derecha.**  Te ayuda a mantener devTools en paralelo con el producto web y es excelente cuando emulas dispositivos móviles.  Las **opciones Acoplar a izquierda** y **Acoplar** a la derecha funcionan mejor con pantallas de alta resolución.  Para obtener más información acerca de los dispositivos de emulación, vaya [a Emular dispositivos móviles en Microsoft Edge DevTools][DevtoolsGuideDeviceModeIndex].  
*   **Acoplar a la parte inferior**.  Le ayuda cuando no tiene suficiente espacio para mostrar horizontalmente o desea depurar texto largo en dom o **consola.**  
    
:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-docking-left.msft.png" alt-text="Elija Acoplar a la izquierda" lightbox="./media/devtools-intro-docking-left.msft.png":::  
         Elija **Acoplar a la izquierda**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-bottom.msft.png" alt-text="Elija Acoplar a la parte inferior" lightbox="media/devtools-intro-docking-bottom.msft.png":::  
         Elija **Acoplar a la parte inferior**  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  
:::row:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-right.msft.png" alt-text="Elija Acoplar a la derecha" lightbox="media/devtools-intro-docking-right.msft.png":::  
         Elija **Acoplar a la derecha**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-own-window.msft.png" alt-text="Elegir Desacoplar en una ventana independiente" lightbox="media/devtools-intro-docking-own-window.msft.png":::  
         Elegir **Desacoplar en una ventana independiente**  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

## <a name="learn-about-the-core-tools"></a>Obtenga información sobre las herramientas principales  

DevTools le ofrece una cantidad increíble de energía para inspeccionar, depurar y cambiar el producto web que se muestra actualmente en el explorador.  La mayoría de las herramientas muestran los cambios en directo.  Las actualizaciones en directo hacen que las herramientas sea increíblemente útiles para refinar la apariencia y la navegación o la funcionalidad de un proyecto web sin necesidad de actualizarlo o compilarlo.  DevTools también le permite cambiar productos de terceros basados en web en su equipo.  

DevTools creció durante un período de varios años.  Puede suponer que DevTools es difícil de aprender cuando abre por primera vez cualquiera de las herramientas.  El siguiente texto presenta rápidamente las distintas partes.  La barra de herramientas principal ofrece algunas secciones y las secciones se ordenan de izquierda a derecha.  

:::image type="complex" source="./media/devtools-intro-menu-bar.msft.png" alt-text="Captura de pantalla de la barra de menús de DevTools con etiquetas que explican las distintas secciones.  En orden: Inspeccionar herramienta, Herramienta de emulación de dispositivo, Grupo de pestañas Herramientas, Errores de JavaScript, Problemas, Configuración, Comentarios, Personalizar y Cerrar." lightbox="./media/devtools-intro-menu-bar.msft.png":::  
   Captura de pantalla de la barra de menús de DevTools con etiquetas que explican las distintas secciones.  En orden: Inspeccionar herramienta, Herramienta de emulación de dispositivo, Grupo de pestaña Herramientas, Errores de JavaScript, Problemas, Configuración, Comentarios, Personalizar y Cerrar.  
:::image-end:::  

*   La herramienta Inspeccionar le permite elegir un elemento en la página web actual.  Después de activarlo, puede mover el mouse sobre diferentes partes de la página web para obtener información detallada sobre el elemento y una superposición de color para mostrar las dimensiones, el relleno y el margen.  
    
    :::image type="complex" source="./media/devtools-intro-inspect-tool.msft.png" alt-text="Captura de pantalla de la herramienta de inspección con el primer titular de este artículo elegido" lightbox="./media/devtools-intro-inspect-tool.msft.png":::  
       Captura de pantalla de la herramienta de inspección con el primer titular de este artículo elegido  
    :::image-end:::  
    
*   La [herramienta Emulación de dispositivos][DevtoolsGuideDeviceModeIndex] muestra el producto web actual en un modo de dispositivo emulado.  La **herramienta emulación de** dispositivos te permite ejecutar y probar cómo reacciona el producto al cambiar el tamaño del explorador.  También te ofrece una estimación del diseño y el comportamiento de un dispositivo móvil.  
    
    :::image type="complex" source="./media/devtools-intro-device-emulation.msft.png" alt-text="Captura de pantalla de la pantalla DevTools de este artículo en un teléfono móvil emulado" lightbox="./media/devtools-intro-device-emulation.msft.png":::  
       Captura de pantalla de la pantalla DevTools de este artículo en un teléfono móvil emulado  
    :::image-end:::  
    
*   El grupo de pestañas Herramientas es un grupo de pestañas que representan distintas herramientas que se usan en distintos escenarios.  Puede personalizar cada una de las herramientas y cada herramienta puede cambiar en función del contexto.  Para abrir un menú desplegable de más herramientas, elija el botón **Más pestañas** \( `>>` \).  Cada una de las herramientas se presenta más adelante en la siguiente sección.  
*   Junto al grupo de pestañas Herramientas hay un error opcional y emite accesos directos.  Los accesos directos se muestran cuando se producen errores o problemas de JavaScript en la página web actual.  El botón Abrir consola para ver **# errors, # warnings** \(**JavaScript Errors**\) muestra un círculo rojo seguido del número `X` de errores de JavaScript.  Para abrir la [consola y][DevtoolsGuideConsoleIndex] obtener información sobre el error, elija el botón Errores **de JavaScript.**  El **botón Abrir problemas para ver # issues** \(**Issues**\) es un icono de mensaje azul seguido del número de problemas.  Para abrir la [herramienta Problemas,][DevtoolsGuideIssuesIndex] elija **el botón** Problemas.  
*   El **botón** Configuración muestra un icono de engranaje.  Para abrir la página web Configuración **de** DevTools, elija el **botón** Configuración.  La **página web** Configuración muestra un menú para cambiar **** **Preferencias,** activar Experimentos y mucho más.  
*   El **botón Enviar comentarios** muestra torso con una burbuja de chat junto a él.  Para abrir el cuadro **de diálogo** Enviar comentarios, elija el **botón Enviar** comentarios.  El **cuadro de diálogo** Enviar comentarios te permite escribir información para describir lo que sucedió e incluye automáticamente una captura de pantalla.  Úselo para conectarse con el equipo de DevTools para informar de problemas, problemas o sugerir ideas.  
*   El **botón Personalizar y controlar Devtools** \( `...` \) abre un menú desplegable.  Le permite definir dónde acoplar DevTools, buscar, abrir diferentes herramientas y mucho más.  
    
En el grupo de pestaña Herramientas, puede abrir las distintas herramientas que están disponibles en DevTools.  En la siguiente lista se describen las herramientas más usadas en DevTools.  

*   **Bienvenido**.  Incluye información sobre las nuevas características de DevTools, cómo ponerse en contacto con el equipo y proporciona información sobre determinadas características.  
*   **Elementos**.  Permite editar o inspeccionar HTML y CSS.  Puede editar ambos en la herramienta y mostrar los cambios en directo en el explorador.  
*   [Consola][DevtoolsGuideConsoleIndex].  Permite mostrar y filtrar mensajes de registro.  Los mensajes de registro son registros automatizados del explorador, como solicitudes de red y registros generados por el desarrollador.  También puede ejecutar JavaScript directamente en la **consola** en el contexto de la ventana o marco actual.  
*   [Sources][DevtoolsGuideSourcesIndex].  Un editor de código y un depurador de JavaScript.  Puede editar proyectos, mantener fragmentos de código y depurar el proyecto actual.  
*   [Red][DevtoolsGuideNetworkIndex].  Permite supervisar e inspeccionar solicitudes o respuestas desde la red y la memoria caché del explorador.  Puede filtrar solicitudes y respuestas para ajustarse a sus necesidades y simular diferentes condiciones de red.  También hay disponibles otras herramientas especializadas, como **Rendimiento,** **Memoria,** **Aplicación,** **Seguridad**y **Auditorías.**  

## <a name="power-tip-use-the-command-menu"></a>Sugerencia de encendido: usar el menú de comandos  

DevTools proporciona muchas características y funcionalidades para usar con el producto web.  Accede a las distintas partes de DevTools de muchas maneras, pero la forma más rápida de acceder a las características que necesitas es usar el menú de comandos.  Para obtener más información, vaya a Ejecutar comandos con el menú Comando [de Microsoft Edge DevTools][DevtoolsGuideCommandMenuIndex].  Para abrir el menú de comandos, complete una de las siguientes acciones.  

*   Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).  
*   Elija **Personalizar y controlar DevTools** \( `...` \) y, a continuación, elija **Ejecutar comando**.  

:::image type="complex" source="./media/devtools-intro-command-menu.msft.png" alt-text="Captura de pantalla del menú de comandos en DevTools" lightbox="./media/devtools-intro-command-menu.msft.png":::  
Captura de pantalla del menú de comandos en DevTools  
:::image-end:::  

El menú de comandos permite escribir comandos para mostrar, ocultar o ejecutar características en DevTools.  Con el menú de comandos abierto, escriba la palabra **cambios**y, a continuación, elija **Drawer Show Changes**.  Se **abre** la herramienta Cambios, que resulta útil al editar CSS, pero es difícil de encontrar en la interfaz de usuario de DevTools.  

:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-command-menu-show-changes.msft.png" alt-text="El menú Comando muestra las opciones después de escribir los cambios" lightbox="./media/devtools-intro-command-menu-show-changes.msft.png":::  
         El menú Comando muestra las opciones después de escribir `changes`  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-showing-changes.msft.png" alt-text="DevTools con la herramienta Cambios abierta" lightbox="./media/devtools-intro-showing-changes.msft.png":::  
         DevTools con la **herramienta Cambios** abierta  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

## <a name="customize-the-devtools"></a>Personalizar las DevTools  

DevTools se puede personalizar para satisfacer sus necesidades o la forma en que trabaja.  Para cambiar la configuración, complete una de las siguientes acciones.  

*   Elija **Configuración** \(el icono de engranaje en la parte superior derecha\)  
*   Seleccione `F1` o `?` .  
    
En la **sección Preferencias,** puede cambiar varias partes de DevTools.  Por ejemplo, puede **** usar la opción Coincidir con el idioma del explorador para usar el mismo idioma en las DevTools que se usan en el explorador.  Para otro ejemplo, use la **configuración Theme** para cambiar el tema de DevTools.  

:::image type="complex" source="media/devtools-intro-all-settings.msft.png" alt-text="Captura de pantalla de toda la configuración de DevTools" lightbox="./media/devtools-intro-all-settings.msft.png":::  
   Captura de pantalla de toda la configuración de DevTools  
:::image-end:::  

También puede cambiar la configuración de las características avanzadas, incluidas las siguientes características.    

*   [Áreas de trabajo][DevtoolsGuideWorkspacesIndex].  
*   Filtrar código de biblioteca con **la lista omitir**.  
*   Define los **dispositivos** que quieres incluir en el modo de simulación y prueba del dispositivo.  Para obtener más información, vaya [a Emular dispositivos móviles en Microsoft Edge DevTools][DevtoolsGuideDeviceModeIndex].  
*   Elija un perfil **de limitación de** red.  
*   Definir ubicaciones **simuladas**.  
*   Personalizar los métodos abreviados de teclado.  Para usar los mismos métodos abreviados en DevTools que Visual Studio code, complete las siguientes acciones.  
    1.  Elija **Match shortcuts from preset**.  
    1.  Elija **Visual Studio code**.  
        
    :::image type="complex" source="./media/devtools-intro-match-keys.msft.png" alt-text="Captura de pantalla de todos los métodos abreviados de teclado y el menú para que coincidan con cada uno de los accesos directos en Visual Studio código" lightbox="./media/devtools-intro-match-keys.msft.png":::  
       Captura de pantalla de todos los métodos abreviados de teclado y el menú para que coincidan con cada uno de los accesos directos en Visual Studio código  
    :::image-end:::  
    
## <a name="try-experimental-features"></a>Probar características experimentales  

El equipo de DevTools proporciona nuevas características como experimentos en DevTools.  Para obtener la lista completa de experimentos, **** vaya a Configuración de DevTools y, a continuación, elija **Experimentos**.  Puede activar o desactivar cada uno de los experimentos.  Ayuda a decidir cuál de los experimentos es valioso para ti.  Para obtener más información sobre los experimentos, vaya a [Características experimentales][DevtoolsGuideExperimentalFeaturesIndex].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Si quieres obtener una vista previa de las características más recientes que llegan a [DevTools,][DevtoolsGuideWhatsNew202102Devtools]descarga [Microsoft Edge Canary,][MicrosoftedgeinsiderDownload]que se compila por la noche.  

## <a name="see-also"></a>Consulte también  

*   [DevtoolsGuide para principiantes: Introducción a HTML y DOM][DevtoolsGuideBeginnersHtml]  
*   [Protocolo DevTools de Microsoft Edge (Chromium)][DevtoolsProtocolIndex]  
    
<!-- links -->  

[DevtoolsGuideBeginnersHtml]: ./beginners/html.md "DevTools para principiantes: Introducción a HTML y el dom | Microsoft Docs"  
[DevtoolsGuideCommandMenuIndex]: ./command-menu/index.md "Ejecute comandos con el menú Comando de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideConsoleIndex]: ./console/index.md "Información general de la consola | Microsoft Docs"  
[DevtoolsGuideCustomizePlacement]: ./customize/placement.md "Cambiar la ubicación de Microsoft Edge DevTools (Undock, Dock to Bottom, Dock to Left) | Microsoft Docs"  
[DevtoolsGuideDeviceModeIndex]: ./device-mode/index.md "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideDomIndex]: ./dom/index.md "Introducción a ver y cambiar el dom | Microsoft Docs"  
[DevtoolsGuideEvaluatePerformanceIndex]: ./evaluate-performance/index.md "Introducción al análisis del rendimiento en tiempo de ejecución | Microsoft Docs"  
[DevtoolsGuideExperimentalFeaturesIndex]: ./experimental-features/index.md "Características experimentales | Microsoft Docs"  
[DevtoolsGuideMemoryProblemsIndex]: ./memory-problems/index.md "Corregir problemas de memoria | Microsoft Docs"  
[DevtoolsGuideInspectStylesEditFonts]: ./inspect-styles/edit-fonts.md "Editar estilos y opciones de fuente CSS en el panel Estilos | Microsoft Docs"  
[DevtoolsGuideIssuesIndex]: ./issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideJavascriptIndex]: ./javascript/index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideJavascriptOverrides]: ./javascript/overrides.md "Invalidar recursos de página web con copias locales mediante Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideNetworkIndex]: ./network/index.md "Inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideOpenIndex]: ./open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideRenderingToolsIndex]: ./rendering-tools/index.md "Analizar el rendimiento en tiempo de ejecución | Microsoft Docs"  
[DevtoolsGuideShortcutsIndex]: ./shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideSourcesIndex]: ./sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
[DevtoolsGuideStorageSessionstorage]: ./storage/sessionstorage.md "Ver y editar el almacenamiento de sesiones con Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideWhatsNew202102Devtools]: ./whats-new/2021/02/devtools.md "Novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsGuideWorkspacesIndex]: ./workspaces/index.md "Editar archivos con áreas de trabajo | Microsoft Docs"  
[DevtoolsProtocolIndex]: ../devtools-protocol-chromium/index.md "Información general del protocolo DevTools de Microsoft Edge (Chromium) | Microsoft Docs"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Complementos de Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensiones | Chrome Web Store"  

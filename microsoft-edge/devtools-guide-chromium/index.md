---
description: Conozca las herramientas de Microsoft Edge (Chromium) para desarrolladores
title: Microsoft Edge Información general sobre herramientas para desarrolladores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 0ed8cea6b39e7f0fcac87df5efbe89831a4ec24c
ms.sourcegitcommit: 3d1b23679e8b61cdebe6c014247925adc04d132c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "11920836"
---
# <a name="microsoft-edge-developer-tools-overview"></a>Microsoft Edge Información general sobre herramientas para desarrolladores  

Al instalar Microsoft Edge (Chromium), obtiene un explorador. Además, el explorador le servirá para inspeccionar, depurar y crear proyectos web de forma eficaz.  Las herramientas para desarrolladores que se suministran con el explorador se basan en las herramientas del proyecto de código abierto Chromium, por lo que es posible que ya las conozca.  Para que las descripciones sean más cortas en este artículo, ahora se `Microsoft Edge Developer Tools` `DevTools` denominan .  

Utilice DevTools para revisar y obtener más información sobre las siguientes tareas de desarrollo.  

*   [Inspeccionar y cambiar la página web actual][DevtoolsGuideDomIndex] en el explorador al momento.  
*   [Emular el comportamiento de un producto en diferentes dispositivos][DevtoolsGuideDeviceModeIndex] y simular un entorno móvil completo con diferentes condiciones de red.  
*   [Inspeccionar, ajustar y cambiar los estilos de los elementos][DevtoolsGuideInspectStylesEditFonts] en la página web al momento mediante herramientas integradas en una interfaz visual.  
*   [Depurar JavaScript][DevtoolsGuideJavascriptIndex] utilizando la depuración de puntos de interrupción y la [consola activa][DevtoolsGuideConsoleIndex].  
*   Encontrar en sus productos [problemas de accesibilidad, rendimiento, compatibilidad y seguridad][DevtoolsGuideIssuesIndex] y aprender a usar DevTools para corregirlos.  
*   [Inspeccionar el tráfico de red][DevtoolsGuideNetworkIndex] y ver dónde se encuentran los problemas.  
*   [Examinar dónde almacena el explorador el contenido][DevtoolsGuideStorageSessionstorage] en diversos formatos.  
*   [Evaluar el rendimiento][DevtoolsGuideEvaluatePerformanceIndex] del producto para encontrar [problemas de memoria][DevtoolsGuideMemoryProblemsIndex] y de[representación][DevtoolsGuideRenderingToolsIndex].  
*   [Usar un entorno de desarrollo][DevtoolsGuideSourcesIndex] para [sincronizar los cambios en DevTools con el sistema de archivos][DevtoolsGuideWorkspacesIndex] e [invalidar los archivos][DevtoolsGuideJavascriptOverrides] de la web.  
    
<!-- Is the link meant to be local or session storage for "inspect where the browser stored content"? -->  

Y muchas otras cosas.  Lo primero es abrir DevTools y personalizar cada herramienta según sus necesidades.  

## <a name="open-the-devtools"></a>Abrir DevTools  

Para abrir y explorar DevTools, use cualquiera de las siguientes acciones.  

*   Mantenga el mouse sobre cualquier elemento de la página web, abra el menú contextual \(haga clic con el botón secundario\) y, a continuación, seleccione **Inspeccionar**.  Se abrirá la herramienta **Elementos**.  
*   Seleccione `F12`.  
*   Seleccione `Ctrl` + `Shift` + `I` en Windows/Linux o `Command` + `Option` + `I` en macOS.  
    
:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-inspect.msft.png" alt-text="Seleccione Inspeccionar en el menú contextual de cualquier elemento" lightbox="./media/devtools-intro-inspect.msft.png":::  
         Seleccione **Inspeccionar** en el menú contextual de cualquier elemento  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-inspect-devtools-open.png" alt-text="DevTools se abrirá con el elemento seleccionado resaltado" lightbox="./media/devtools-intro-inspect-devtools-open.png":::  
         DevTools se abrirá con el elemento seleccionado resaltado  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

Hay dos formas principales de interactuar con DevTools.
*   Use el mouse.  
*   Con [Métodos abreviados de teclado][DevtoolsGuideShortcutsIndex].  Los métodos abreviados de teclado son una forma rápida de acceder a las funcionalidades y son necesarios para la accesibilidad.  El equipo de Microsoft Edge DevTools está continuamente trabajando para que se pueda acceder a todas las herramientas desde el teclado y con tecnologías de asistencia como los lectores de pantalla.  Para obtener más información sobre cómo abrir las diferentes características de DevTools, vaya a [métodos abreviados de teclado de Microsoft Edge DevTools][DevtoolsGuideOpenIndex].  

## <a name="dock-the-devtools-in-your-browser"></a>Acoplar DevTools en el explorador  

Al abrir DevTools, se acopla a la izquierda del explorador.  Para cambiar la ubicación de DevTools, realice las siguientes acciones.  

1.  Seleccione el **botón Personalizar y controlar devTools** \( `...` \).  
1.  A la derecha de **Ubicación de DevTools con respecto a la página** \(**Acoplar**\), elija una de las opciones de **Acoplar**.  
    
Para obtener más información, vaya a Cambiar la ubicación [de DevTools (Undock, Dock To bottom, Dock To left).][DevtoolsGuideCustomizePlacement]  

:::image type="complex" source="./media/devtools-intro-docking-menu.msft.png" alt-text="Captura de pantalla del menú lateral de Acoplar en DevTools" lightbox="./media/devtools-intro-docking-menu.msft.png":::  
   Captura de pantalla del menú lateral de Acoplar en DevTools  
:::image-end:::  

En **Acoplar**, elija una de las siguientes opciones de diseño.  

*   **Desacoplar en una ventana independiente**.   Le facilita el trabajo cuando utiliza varios monitores o aplicaciones en pantalla completa.  
*   **Acoplar a la izquierda** o **Acoplar a la derecha**.  Mantiene DevTools en paralelo con el producto web y funciona estupendamente al emular dispositivos móviles.  Las opciones **Acoplar a la izquierda** y **Acoplar a la derecha** funcionan a pleno rendimiento con pantallas de alta resolución.  Para obtener más información sobre los dispositivos de emulación, vaya a [Emular dispositivos móviles en Microsoft Edge DevTools][DevtoolsGuideDeviceModeIndex].  
*   **Acoplar en la parte inferior**.  Le permite solucionar la falta de espacio horizontal o depurar un texto largo en DOM o en la **Consola**.  
    
:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-docking-left.msft.png" alt-text="Seleccione Acoplar a la izquierda" lightbox="./media/devtools-intro-docking-left.msft.png":::  
         Seleccione **Acoplar a la izquierda**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-bottom.msft.png" alt-text="Seleccione Acoplar a la parte inferior" lightbox="media/devtools-intro-docking-bottom.msft.png":::  
         Seleccione **Acoplar a la parte inferior**  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  
:::row:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-right.msft.png" alt-text="Seleccione Acoplar a la derecha" lightbox="media/devtools-intro-docking-right.msft.png":::  
         Seleccione **Acoplar a la derecha**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="media/devtools-intro-docking-own-window.msft.png" alt-text="Seleccionar Desacoplar en una ventana independiente" lightbox="media/devtools-intro-docking-own-window.msft.png":::  
         Seleccionar **Desacoplar en una ventana independiente**  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

## <a name="learn-about-the-core-tools"></a>Obtenga información sobre las herramientas principales  

DevTools le concede la capacidad de inspeccionar, depurar y modificar el producto web que se muestra en el explorador.  La mayoría de herramientas muestran los cambios al instante.  Las actualizaciones en tiempo real hacen que las herramientas sean de gran utilidad a la hora de refinar la apariencia, navegación o la funcionalidad de un proyecto web sin tener que estar actualizando o compilando.  DevTools también le permite modificar en su equipo productos web de terceros.  

DevTools ha ido creciendo a lo largo de los años.  Al principio podría parecer que las herramientas de DevTools son difíciles de utilizar.  Aquí le explicaremos rápidamente sus distintos componentes.  La barra de herramientas principal contiene algunas secciones que se ordenan de izquierda a derecha.  

:::image type="complex" source="./media/devtools-intro-menu-bar.msft.png" alt-text="Captura de pantalla de la barra de menús de DevTools con etiquetas que explican las distintas secciones.  En orden: Inspeccionar herramienta, Herramienta de emulación de dispositivo, Grupo de pestañas de Herramientas, Errores de JavaScript, Problemas, Configuración, Comentarios, Personalizar y Cerrar." lightbox="./media/devtools-intro-menu-bar.msft.png":::  
   Captura de pantalla de la barra de menús de DevTools con etiquetas que explican las distintas secciones.  En orden: Inspeccionar herramienta, Herramienta de emulación de dispositivo, Grupo de pestañas de Herramientas, Errores de JavaScript, Problemas, Configuración, Comentarios, Personalizar y Cerrar.  
:::image-end:::  

*   La herramienta Inspeccionar permite seleccionar un elemento de la página web actual.  Después de activarlo, puedes mover el mouse sobre diferentes partes de la página web para obtener información detallada sobre el elemento y una superposición de color para mostrar las dimensiones, el relleno y el margen.  
    
    :::image type="complex" source="./media/devtools-intro-inspect-tool.msft.png" alt-text="La herramienta Inspeccionar junto al primer título de este artículo" lightbox="./media/devtools-intro-inspect-tool.msft.png":::  
       La herramienta Inspeccionar junto al primer título de este artículo  
    :::image-end:::  
    
*   La herramienta [Emulación de dispositivos][DevtoolsGuideDeviceModeIndex] permite visualizar el producto web en un dispositivo emulado.  La herramienta ** Emulación de dispositivos** también permite comprobar cómo se comporta un producto al cambiar el tamaño del explorador.  Asimismo, le ofrece una idea aproximada del diseño y del comportamiento en un dispositivo móvil.  
    
    :::image type="complex" source="./media/devtools-intro-device-emulation.msft.png" alt-text="Captura de pantalla de las DevTools de este artículo en la emulación de un teléfono móvil" lightbox="./media/devtools-intro-device-emulation.msft.png":::  
       Captura de pantalla de las DevTools de este artículo en la emulación de un teléfono móvil  
    :::image-end:::  
    
*   La barra de herramientas principal contiene pestañas para las herramientas que se usan en varios escenarios.  Puede personalizar cada una de las herramientas y cada herramienta puede cambiar en función del contexto.  Para mostrar una herramienta que se encuentra en una pestaña oculta, seleccione el botón **Más pestañas** \( `>>` \).   Para agregar una herramienta a la barra de herramientas principal o a la barra de herramientas del cajón, seleccione el **botón Más herramientas** ( `+` ).  Cada herramienta se presenta a continuación.  
*   Junto al grupo de pestañas de Herramientas hay accesos directos opcionales a errores y problemas.  Los accesos directos se muestran cuando se producen errores o problemas de JavaScript en la página web.  El botón Abrir consola para ver **# errors, # warnings** \(**JavaScript Errors**\) muestra un círculo rojo con un , seguido del `X` número de errores de JavaScript.  Para abrir la [consola y][DevtoolsGuideConsoleIndex] obtener información sobre el error, seleccione el botón Errores **de JavaScript.**  El botón **Abrir problemas para ver # problemas** \(**Problemas**\) muestra un icono azul seguido del número de problemas.  Para abrir la [herramienta Problemas,][DevtoolsGuideIssuesIndex] seleccione el **botón** Problemas.  
*   El botón de **Configuración** muestra un icono de engranaje.  Para abrir devTools **Configuración** página web, seleccione el **botón Configuración** página web.  La página web de **Configuración** muestra un menú para modificar **Preferencias**, activar  **Experimentos** y muchas cosas más.  
*   El **botón Enviar comentarios** muestra un torso con una burbuja de chat junto a él.  Para abrir el **cuadro de diálogo** Enviar comentarios, seleccione el botón **Enviar** comentarios.  El cuadro de diálogo **Enviar comentarios** permite informar de lo que haya sucedido e incluye automáticamente una captura de pantalla.  Úselo para conectarse con el equipo de DevTools e informar de problemas y errores o hacer sugerencias.  
*   El **botón Personalizar y controlar DevTools** \( `...` \) abre un menú desplegable.  Le permite decidir dónde acoplar las DevTools, buscar y abrir diferentes herramientas y muchas cosas más.  
    
En el grupo de pestañas de Herramientas puede abrir las distintas herramientas disponibles en DevTools.  En la siguiente lista podrá ver las herramientas de DevTools más utilizadas.  

*   **Bienvenido**.  Aquí podrá informarse sobre las nuevas características de DevTools, cómo ponerse en contacto con el equipo y el funcionamiento de ciertas características.  
*   **Elementos**.  Permite editar o inspeccionar HTML y CSS.  Puede editar ambos mediante esta herramienta y ver los cambios en el explorador en tiempo real.  
*   [Consola][DevtoolsGuideConsoleIndex].  Permite mostrar y filtrar los mensajes de registro.  Los mensajes de registro son registros automatizados del explorador, como solicitudes de red y registros generados por el desarrollador.  Puede ejecutar JavaScript directamente en la **Consola** dentro del contexto de la ventana o marco actuales.  
*   [Orígenes][DevtoolsGuideSourcesIndex].  Un editor de códigos y depurador de JavaScript.  Puede usarlo para editar proyectos, mantener fragmentos de código y depurar el proyecto actual.  
*   [Red][DevtoolsGuideNetworkIndex].  Le permite supervisar e inspeccionar solicitudes o respuestas de la red y de la memoria caché del explorador.  Puede utilizarlo para filtrar solicitudes y respuestas que se ajusten a sus necesidades y simular diferentes condiciones de red.  También tiene disponibles otras herramientas especializadas como **Rendimiento**, **Memoria**, **Aplicación**, **Seguridad** y **Auditorías**.  

## <a name="power-tip-use-the-command-menu"></a>Sugerencia: utilice el menú de comandos  

DevTools proporciona muchas características y funcionalidades que puede utilizar en su producto web.  Puede acceder a las distintas funcionalidades de DevTools de varias maneras, pero la forma más rápida es utilizando el menú de comandos.  Para obtener más información, vaya a [Ejecutar comandos con el menú de comandos de DevTools de Microsoft Edge][DevtoolsGuideCommandMenuIndex].  Para abrir el menú de comandos, realice una de las siguientes acciones.  

*   Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).  
*   Seleccione **Personalizar y controlar DevTools** \( `...` \) y, a continuación, seleccione **Ejecutar comando**.  

:::image type="complex" source="./media/devtools-intro-command-menu.msft.png" alt-text="Captura de pantalla del menú de comandos de DevTools" lightbox="./media/devtools-intro-command-menu.msft.png":::  
Captura de pantalla del menú de comandos de DevTools  
:::image-end:::  

El menú de comandos le permite introducir comandos para mostrar, ocultar o ejecutar características en DevTools.  Con el menú de comandos abierto, escriba la palabra **cambios**y, a continuación, **seleccione Cajón: Mostrar cambios**.  Se **abre** la herramienta Cambios, que resulta útil al editar CSS, pero es difícil de encontrar en la interfaz de usuario de DevTools.  

:::row:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-command-menu-show-changes.msft.png" alt-text="Al escribir la palabra cambios, el menú Comando le mostrará las opciones" lightbox="./media/devtools-intro-command-menu-show-changes.msft.png":::  
         Al escribir la palabra, el menú Comando le mostrará las opciones `changes`  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::  
      :::image type="complex" source="./media/devtools-intro-showing-changes.msft.png" alt-text="DevTools con la herramienta de Cambios abierta" lightbox="./media/devtools-intro-showing-changes.msft.png":::  
         DevTools con la herramienta de **Cambios** abierta  
      :::image-end:::  
   :::column-end:::  
:::row-end:::  

## <a name="customize-the-devtools"></a>Personalizar las herramientas de DevTools  

DevTools se puede personalizar para satisfacer sus necesidades y favorecer su forma de trabajo.  Para cambiar la configuración, realice una de las siguientes acciones.  

*   Seleccione **Configuración** \(el icono de engranaje en la parte superior derecha\)  
*   Seleccione `F1` o `?`.  
    
En la sección de **Preferencias** puede realizar varios cambios en DevTools.  Por ejemplo, la opción de **Emparejar con el idioma del explorador** le permite utilizar el mismo idioma del explorador en DevTools.  La opción de **Tema** le permite cambiar el tema de DevTools.  

:::image type="complex" source="media/devtools-intro-all-settings.msft.png" alt-text="Captura de pantalla de la configuración de DevTools" lightbox="./media/devtools-intro-all-settings.msft.png":::  
   Captura de pantalla de la configuración de DevTools  
:::image-end:::  

También puede cambiar la configuración de las características avanzadas, incluidas las siguientes características.    

*   [Áreas de trabajo][DevtoolsGuideWorkspacesIndex].  
*   **Lista de omitidos** para filtrar código de biblioteca.  
*   **Dispositivos** para añadir dispositivos en el modo de simulación y prueba de dispositivos.  Para más información vaya a [Emular dispositivos móviles en Microsoft Edge DevTools][DevtoolsGuideDeviceModeIndex].  
*   Perfil de **Limitación** de red.  
*   **Ubicaciones** para definir ubicaciones simuladas.  
*   Personalizar **métodos abreviados de teclado**.  Por ejemplo, para usar los mismos métodos abreviados en DevTools que Visual Studio Code seleccione Coincidencia **de accesos directos**de la configuración  >  **Visual Studio Code**.  
        
    :::image type="complex" source="./media/devtools-intro-match-keys.msft.png" alt-text="Captura de pantalla de los métodos abreviados de teclado y del menú para que coincidan con los de Visual Studio Code" lightbox="./media/devtools-intro-match-keys.msft.png":::  
       Captura de pantalla de los métodos abreviados de teclado y del menú para que coincidan con los de Visual Studio Code  
    :::image-end:::  
    
## <a name="try-experimental-features"></a>Probar características experimentales  

El equipo de DevTools proporciona nuevas características experimentales.  Para obtener la lista completa de experimentos, vaya a la página DevTools **Configuración**y, a continuación, **seleccione Experimentos**.  Todos los experimentos pueden activarse o desactivarse.  Esto le ayudará a ver qué experimentos le son de mayor utilidad.  Para obtener más información sobre los experimentos, vaya a [Características experimentales][DevtoolsGuideExperimentalFeaturesIndex].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Para obtener una vista previa de las [características más recientes de DevTools][DevtoolsGuideWhatsNew202102Devtools]descargue [Microsoft Edge Canary][MicrosoftedgeinsiderDownload], que se compila todas las noches.  

## <a name="see-also"></a>Vea también  

*   [DevTools para principiantes: Introducción html y dom][DevtoolsGuideBeginnersHtml]  
*   [Protocolo de Microsoft Edge (Chromium) DevTools][DevtoolsProtocolIndex]  
    
<!-- links -->  

[DevtoolsGuideBeginnersHtml]: ./beginners/html.md "DevTools para principiantes: introducción utilizando HTML y DOM | Microsoft Docs"  
[DevtoolsGuideCommandMenuIndex]: ./command-menu/index.md "Ejecute comandos con el menú de comandos de DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsGuideConsoleIndex]: ./console/index.md "Información general de la Consola | Microsoft Docs"  
[DevtoolsGuideCustomizePlacement]: ./customize/placement.md "Cambiar la ubicación de DevTools (Undock, Dock To bottom, Dock To left) | Microsoft Docs"  
[DevtoolsGuideDeviceModeIndex]: ./device-mode/index.md "Emulación de dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideDomIndex]: ./dom/index.md "Cómo ver y cambiar el DOM | Microsoft Docs"  
[DevtoolsGuideEvaluatePerformanceIndex]: ./evaluate-performance/index.md "Introducción al análisis del rendimiento en tiempo de ejecución | Microsoft Docs"  
[DevtoolsGuideExperimentalFeaturesIndex]: ./experimental-features/index.md "Características experimentales | Microsoft Docs"  
[DevtoolsGuideMemoryProblemsIndex]: ./memory-problems/index.md "Corregir problemas de memoria | Microsoft Docs"  
[DevtoolsGuideInspectStylesEditFonts]: ./inspect-styles/edit-fonts.md "Editar estilos y opciones de fuente de CSS en el panel Estilos | Microsoft Docs"  
[DevtoolsGuideIssuesIndex]: ./issues/index.md "Buscar y solucionar problemas con la herramienta Problemas | Microsoft Docs"  
[DevtoolsGuideJavascriptIndex]: ./javascript/index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideJavascriptOverrides]: ./javascript/overrides.md "Invalidar recursos de página web con copias locales utilizando Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideNetworkIndex]: ./network/index.md "Inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideOpenIndex]: ./open/index.md "Abrir Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideRenderingToolsIndex]: ./rendering-tools/index.md "Analizar el rendimiento en tiempo de ejecución | Microsoft Docs"  
[DevtoolsGuideShortcutsIndex]: ./shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideSourcesIndex]: ./sources/index.md "Información general sobre la herramienta Orígenes | Microsoft Docs"  
[DevtoolsGuideStorageSessionstorage]: ./storage/sessionstorage.md "Ver y editar el almacenamiento de sesiones con Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideWhatsNew202102Devtools]: ./whats-new/2021/02/devtools.md "Novedades de DevTools (Microsoft Edge 90) | Microsoft Docs"  
[DevtoolsGuideWorkspacesIndex]: ./workspaces/index.md "Editar archivos utilizando Áreas de trabajo | Microsoft Docs"  
[DevtoolsProtocolIndex]: ../devtools-protocol-chromium/index.md "Información general del Protocolo de Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Complementos de Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensiones | Chrome Web Store"  

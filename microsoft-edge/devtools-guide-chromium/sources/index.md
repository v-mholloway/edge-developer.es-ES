---
description: Use la herramienta Orígenes para ver, modificar y depurar JavaScript devuelto por el servidor e inspeccionar los recursos que conste la página web actual.  Para usar la herramienta Orígenes como entorno de desarrollo, agregue archivos de origen a un área de trabajo.
title: Introducción a la herramienta Sources
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c162ccb21c5a3d55ecbdf1fd71ad729f34338c2e
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519587"
---
# <a name="sources-tool-overview"></a>Introducción a la herramienta Sources  

Use la **herramienta Orígenes** para ver, modificar y depurar código JavaScript front-end e inspeccionar los recursos que formaban la página web actual.  La **herramienta Orígenes** tiene tres paneles:  

| Panel | Acciones |
|---|---|
| **Panel Navegador** | Navegue entre los recursos que se devuelven desde el servidor para crear la página web actual.  Seleccione archivos, imágenes y otros recursos y vea sus rutas de acceso.  Opcionalmente, configure un área de trabajo local para guardar los cambios directamente en los archivos de origen. |
| **Panel editor** | Ver JavaScript, HTML, CSS y otros archivos que se devuelven desde el servidor.  Realice ediciones experimentales en JavaScript o CSS.  Los cambios se conservan hasta actualizar la página o se conservan después de la actualización de la página si se guarda en un archivo local con áreas de trabajo. Al usar áreas de trabajo o invalidaciones, también puede editar archivos HTML. |
| **Panel depurador** | Use el depurador de JavaScript para establecer puntos de interrupción, pausar la ejecución de JavaScript y realizar un paso por el código, incluidas las modificaciones que haya realizado, mientras observa las expresiones de JavaScript que especifique.  Observe y cambie manualmente los valores de las variables que están dentro del ámbito de la línea de código actual. |

En la siguiente **** figura se muestra el panel Navegador resaltado con un cuadro rojo en la esquina superior **** izquierda de DevTools, el **panel Editor** resaltado en la parte superior derecha y el panel Depurador resaltado en la parte inferior.  En el lado izquierdo se encuentra la parte principal de la ventana del explorador, que muestra la página web en gris porque el depurador está pausado en un punto de interrupción:

:::image type="complex" source="../media/sources-panes-narrow-layout.msft.png" alt-text="Los paneles de la herramienta Orígenes, en diseño estrecho" lightbox="../media/sources-panes-narrow-layout.msft.png":::
   Los paneles de la herramienta Orígenes, en diseño estrecho  
:::image-end:::  

Cuando DevTools es ancho, el panel **Depurador** se coloca a la derecha e incluye **Scope** y **Watch:**  

:::image type="complex" source="../media/sources-panes-wide-layout.msft.png" alt-text="Navegar, ver, editar y depurar JavaScript devuelto por el servidor" lightbox="../media/sources-panes-wide-layout.msft.png":::
   Navegar, ver, editar y depurar JavaScript devuelto por el servidor  
:::image-end:::  

Para maximizar el tamaño de la herramienta Orígenes, desasoye DevTools en una ventana independiente y, opcionalmente, mueva la ventana DevTools a un monitor independiente.  Consulte [Cambiar la ubicación de Microsoft Edge DevTools (Undock, Dock to bottom, Dock to left).][DevToolsCustomizePlacement]

Para cargar la página web de demostración de depuración que se muestra anteriormente, consulta [El enfoque básico para usar un depurador](#the-basic-approach-to-using-a-debugger), a continuación.

## <a name="using-the-navigator-pane-to-select-files"></a>Uso del panel Navegador para seleccionar archivos

Use el **panel** Navegador (a la izquierda) para navegar entre los recursos que se devuelven desde el servidor para construir la página web actual.  Seleccione archivos, imágenes y otros recursos y vea sus rutas de acceso.  

:::image type="complex" source="../media/navigator-pane.msft.png" alt-text="Panel Navegador" lightbox="../media/navigator-pane.msft.png":::
   Panel **Navegador**
:::image-end:::  

Para obtener acceso a las pestañas ocultas del panel Navegador, seleccione ![ Más pestañas ](../media/more-tabs-icon.msft.png) ( Más**pestañas**).

Las siguientes subsecciones abarcan el panel Navegador:
*   [Uso de la pestaña Página para explorar los recursos que crean la página web actual](#using-the-page-tab-to-explore-resources-that-construct-the-current-webpage)
*   [Uso de la pestaña Sistema de archivos para definir un área de trabajo local](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [Uso de la pestaña Invalidaciones para invalidar archivos de servidor con archivos locales](#using-the-overrides-tab-to-override-server-files-with-local-files)
*   [Uso de la pestaña Scripts de contenido para extensiones de Microsoft Edge](#using-the-content-scripts-tab-for-microsoft-edge-extensions)
*   [Uso de la pestaña Fragmentos de código para ejecutar fragmentos de código JavaScript en cualquier página](#using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage)
*   [Uso del menú comando para abrir archivos](#using-the-command-menu-to-open-files)

### <a name="using-the-page-tab-to-explore-resources-that-construct-the-current-webpage"></a>Uso de la pestaña Página para explorar los recursos que crean la página web actual

Use la **pestaña Página** **del** panel Navegador para explorar el sistema de archivos que se devuelve desde el servidor para crear la página web actual.  Seleccione un archivo JavaScript para verlo, editarlo y depurarlo.  La **pestaña** Página enumera todos los recursos que la página ha cargado.

:::image type="complex" source="../media/sources-page-tab.msft.png" alt-text="La pestaña Página del panel Navegador de la herramienta Orígenes" lightbox="../media/sources-page-tab.msft.png":::
   La **pestaña Página** del panel **Navegador** de la herramienta **Orígenes**
:::image-end:::  

Para mostrar un archivo en el **panel Editor,** seleccione un archivo en la **pestaña** Página.  Para una imagen, se muestra una vista previa de la imagen.  

Para mostrar la dirección URL o la ruta de acceso de un recurso, mantenga el puntero sobre el recurso.

Para cargar un archivo en una nueva pestaña del explorador o para mostrar otras acciones, haga clic con el botón secundario en el nombre del archivo.
   
#### <a name="icons-in-the-page-tab"></a>Iconos en la pestaña Página

La **pestaña** Página usa los siguientes iconos:
*   El **icono de** ventana, junto con la etiqueta , representa el marco del documento `top` principal, que es un marco [HTML][W3CHtml4Frames].  
*   El **icono de** nube representa un [origen][HtmlstandardOrigin].  
*   El **icono de** carpeta representa un directorio.
*   El **icono de** página representa un recurso.  
    
#### <a name="group-files-by-folder-or-as-a-flat-list"></a>Agrupar archivos por carpeta o como una lista plana

La **pestaña** Página muestra archivos o recursos agrupados por servidor y directorio, o como una lista plana.

Para cambiar la forma en que se agrupan los recursos:

1.  Junto a las pestañas del panel Navegador (a la izquierda), seleccione **el botón ...** (**Más**opciones ).  Aparece un menú.
1.  Seleccione o desactive la **opción Agrupar por** carpeta.  

### <a name="using-the-filesystem-tab-to-define-a-local-workspace"></a>Uso de la pestaña Sistema de archivos para definir un área de trabajo local

Use la pestaña Sistema **** **de** archivos del panel Navegador para agregar archivos a un área de trabajo, de modo que los cambios realizados en DevTools se guarden en el sistema de archivos local.

Un archivo que está en un área de trabajo se indica mediante un punto verde junto al nombre del archivo, en DevTools. 

:::image type="complex" source="../media/sources-filesystem-tab.msft.png" alt-text="Ficha Sistema de archivos para un área de trabajo" lightbox="../media/sources-filesystem-tab.msft.png":::
   Ficha **Sistema de** archivos para un área de trabajo
:::image-end:::  

De forma predeterminada, al editar un archivo en la **herramienta Orígenes,** los cambios se descartan al actualizar la página web.  La **herramienta Orígenes** funciona con una copia de los recursos front-end devueltos por el servidor web.  Al modificar estos archivos front-end devueltos por el servidor, los cambios no persisten, ya que no ha cambiado los archivos de origen.  También debe aplicar las ediciones en el código fuente real y, a continuación, volver a implementar en el servidor.

En cambio, al usar un área de trabajo, los cambios realizados en el código front-end se conservan al actualizar la página web.  Con un área de trabajo, al editar el código front-end devuelto por el servidor, la herramienta Orígenes también aplica las ediciones al código fuente local.  A continuación, para que otros usuarios vean los cambios, solo necesita volver a implementar los archivos de origen cambiados en el servidor.

Las áreas de trabajo funcionan bien cuando el código JavaScript devuelto por el servidor es el mismo que el código fuente de JavaScript local.  Las áreas de trabajo no funcionan tan bien cuando el flujo de trabajo implica transformaciones en el código fuente, como la minificación o la compilación [de TypeScript.][TypescriptlangMain]  

Para obtener más información, vea el tutorial [Editar archivos con áreas de trabajo.][DevtoolsGuideChromiumWorkspacesIndex]

### <a name="using-the-overrides-tab-to-override-server-files-with-local-files"></a>Uso de la pestaña Invalidaciones para invalidar archivos de servidor con archivos locales

Use la **pestaña Invalidaciones** del panel **Navegador** para invalidar los activos de página (como imágenes) con archivos de una carpeta local.

Los elementos de esta pestaña invalidan lo que el servidor envía al explorador, incluso después de que el servidor haya enviado los activos.  

:::image type="complex" source="../media/overrides-tab.msft.png" alt-text="La pestaña Invalidaciones del panel Navegador" lightbox="../media/overrides-tab.msft.png":::
   La **pestaña Invalidaciones** del **panel** Navegador
:::image-end:::  

La **característica Invalidaciones** es similar a Workspaces.  Usa Invalidaciones cuando quieras experimentar con los cambios en una página web y debes mantener los cambios después de actualizar la página web, pero no te importa asignar los cambios al código fuente de la página web.  

Un archivo que reemplaza un archivo devuelto por el servidor se indica mediante un punto púrpura junto al nombre del archivo, en DevTools.

#### <a name="see-also"></a>Consulte también

*   [Invalidar recursos de página web con copias locales con Microsoft Edge DevTools][DevtoolsJavascriptOverrides]

*   [Asignar código preprocesado al código fuente][DevToolsJavaScriptSourceMaps]

### <a name="using-the-content-scripts-tab-for-microsoft-edge-extensions"></a>Uso de la pestaña Scripts de contenido para extensiones de Microsoft Edge

Use la **pestaña Scripts de** contenido del panel **Navegador** para ver los scripts de contenido cargados por una extensión de Microsoft Edge que haya instalado. 

:::image type="complex" source="../media/content-scripts-tab.msft.png" alt-text="La pestaña Scripts de contenido del panel Navegador" lightbox="../media/content-scripts-tab.msft.png":::
   La **pestaña Scripts de contenido** del **panel** Navegador
:::image-end:::  

Cuando el depurador entra en el código que no reconoce, es posible que desee marcar ese código como código de biblioteca, para evitar entrar en ese código.  Vea [Marcar scripts de contenido como código de biblioteca][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].

#### <a name="see-also"></a>Consulte también

*   [Scripts de contenido][MDNContentScripts]
*   [Crear un tutorial de extensión, parte 2][ExtensionsChromiumGetstartPart2ContentScripts]

### <a name="using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage"></a>Uso de la pestaña Fragmentos de código para ejecutar fragmentos de código JavaScript en cualquier página web

Use la **pestaña Fragmentos** de código del panel **Navegador** para crear y guardar fragmentos de código javaScript, de modo que pueda ejecutar fácilmente estos fragmentos de código en cualquier página web.

:::image type="complex" source="../media/snippet.msft.png" alt-text="Fragmento de código que inserta la biblioteca jQuery en una página web" lightbox="../media/snippet.msft.png":::
   Fragmento de código que inserta la biblioteca jQuery en una página web  
:::image-end:::  

Por ejemplo, supongamos que escribe con frecuencia el siguiente código en la consola **,** para insertar la biblioteca jQuery en una página para que pueda ejecutar comandos jQuery desde la **consola**:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

En su lugar, puede guardar este código en un **fragmento** de código y, a continuación, ejecutarlo fácilmente siempre que lo necesite.  Cuando selecciona `Ctrl` + `S` \(Windows/Linux\) o `Command` + `S` \(macOS\), DevTools guarda **** el fragmento de código en el sistema de archivos.  

Hay varias maneras de ejecutar un fragmento de código:
*   En el **panel Navegador,** seleccione la pestaña **Fragmentos** de código y, a continuación, seleccione el archivo de fragmentos de código para abrirlo.  A continuación, en la parte inferior del panel Editor, seleccione **Ejecutar** \( ![ El botón Ejecutar ](../media/run-snippet-icon.msft.png) \).  
*   Cuando DevTools tenga el foco, seleccione `Ctrl` + `P` \(Windows/Linux\) o `Command` + `P` [][DevToolsCommandMenuIndex]\(macOS\) `!` para abrir el menú comando y, a continuación, escriba . 

Los fragmentos de código son similares a los bookmarklets.

#### <a name="see-also"></a>Consulte también

*   [Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptSnippets]

### <a name="using-the-command-menu-to-open-files"></a>Uso del menú comando para abrir archivos

Para abrir un archivo, además **** de usar el panel Navegador de la herramienta **Orígenes,** puede usar el menú comando desde cualquier lugar dentro de DevTools.

*   Desde cualquier lugar de DevTools, selecciona `Ctrl` + `P` en Windows/Linux o `Command` + `P` en macOS.  Aparece el menú Comando y enumera todos los recursos que se encuentran en las pestañas del **panel** Navegador de la **herramienta** Orígenes.  
*   O bien, junto a **** las pestañas del panel Navegador de la herramienta **Orígenes,** seleccione **el botón ...** (**Más**opciones ) y, a continuación, seleccione **Abrir archivo**.  

Para mostrar y seleccionar de una lista de todos los archivos .js, escriba `.js` .

:::image type="complex" source="../media/sources-command-menu-to-open-file.msft.png" alt-text="Abrir un archivo mediante el menú comando" lightbox="../media/sources-command-menu-to-open-file.msft.png":::
   Abrir un archivo mediante el menú comando
:::image-end:::

Si escribe `?` , el menú de comandos muestra varios comandos, incluidos **... Abrir archivo**.  Si selecciona borrar `Backspace` el menú comando, se muestra una lista de archivos.

Para obtener más información, vea [Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge][DevToolsCommandMenuIndex].

## <a name="using-the-editor-pane-to-view-or-edit-files"></a>Uso del panel Editor para ver o editar archivos

Use el **panel Editor** para ver los archivos front-end que se devuelven desde el servidor para redactar la página web actual, incluidos los archivos JavaScript, HTML, CSS e imagen.  Al editar los archivos front-end en el **panel Editor,** DevTools actualiza la página web para ejecutar el código modificado.  

:::image type="complex" source="../media/editor-pane.msft.png" alt-text="El panel Editor de la herramienta Orígenes" lightbox="../media/editor-pane.msft.png":::
   El **panel Editor** de la herramienta **Orígenes**  
:::image-end:::

El **panel Editor** tiene el siguiente nivel de compatibilidad para varios tipos de archivo:

| Tipo de archivo | Acciones admitidas |
|---|---|
| JavaScript | Ver, editar y depurar. |
| CSS | Ver y editar. |
| HTML | Ver y editar. |
| Imágenes | Ver. |

De forma predeterminada, las ediciones se descartan al actualizar la página web.  Para obtener información sobre cómo guardar los cambios en el sistema de archivos, consulte [Using the Filesystem tab to define a local Workspace](#using-the-filesystem-tab-to-define-a-local-workspace), arriba.

Las siguientes subsecciones abarcan el panel Editor:
*   [Edición de un archivo JavaScript](#editing-a-javascript-file)
*   [Reformatear un archivo JavaScript minificado con pretty-print](#reformatting-a-minified-javascript-file-with-pretty-print)
*   [Asignación de código minificado al código fuente para mostrar código legible](#mapping-minified-code-to-your-source-code-to-show-readable-code)
*   [Transformaciones del código fuente al código front-end compilado](#transformations-from-source-code-to-compiled-front-end-code)
*   [Edición de un archivo CSS](#editing-a-css-file)
*   [Edición de un archivo HTML](#editing-an-html-file)
*   [Ir a una función o número de línea](#going-to-a-line-number-or-function)
*   [Mostrar archivos de origen al usar una herramienta diferente](#displaying-source-files-when-using-a-different-tool)

### <a name="editing-a-javascript-file"></a>Edición de un archivo JavaScript

Para editar un archivo JavaScript en DevTools, use el **panel Editor,** dentro de la **herramienta** Orígenes.

:::image type="complex" source="../media/editing-js-in-editor-pane.msft.png" alt-text="Edición de JavaScript en el panel Editor" lightbox="../media/editing-js-in-editor-pane.msft.png":::
   Edición de JavaScript en el **panel Editor**  
:::image-end:::

Para cargar un archivo en el panel Editor, use la pestaña **Página** en **el** panel Navegador (a la izquierda).  O bien, use el **menú comando**, como se muestra a continuación: en la parte superior derecha de DevTools, seleccione Personalizar y **controlar DevTools** \( \) y, a continuación, `...` seleccione Abrir **archivo**.

#### <a name="save-and-undo"></a>Guardar y deshacer

Para que los cambios de JavaScript entren en vigor, seleccione `Ctrl` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\).  

Si cambia un archivo, aparecerá un asterisco junto al nombre del archivo.
*   Para guardar los cambios, `Ctrl` + `S` selecciona en Windows/Linux o `Command` + `S` en macOS.
*   Para deshacer un cambio, selecciona `Ctrl` + `Z` en Windows/Linux o `Command` + `Z` en macOS.

De forma predeterminada, las ediciones se descartan al actualizar la página web.  Para obtener más información acerca de cómo guardar los cambios en el sistema de archivos local, vea [Editar archivos con áreas de trabajo.][DevtoolsGuideChromiumWorkspacesIndex]

#### <a name="find-and-replace"></a>Buscar y reemplazar

Para buscar texto en el archivo actual, seleccione el **panel Editor** para darle el foco y, a continuación, seleccione en `Ctrl` + `F` Windows/Linux o `Command` + `F` en macOS.  

:::image type="complex" source="../media/find-replace.msft.png" alt-text="Buscar y reemplazar, en el panel Editor de la herramienta Orígenes" lightbox="../media/find-replace.msft.png":::
   **Buscar** y **reemplazar**, en el **panel Editor** de la **herramienta** Orígenes
:::image-end:::

Para buscar y reemplazar texto, seleccione el botón **Reemplazar** (**A-\>B**) a la izquierda **del** cuadro de texto Buscar. El **botón Reemplazar** (**A-\>B**) aparece al ver un archivo editable.

#### <a name="showing-the-changes-you-made"></a>Mostrar los cambios realizados

Para revisar los cambios realizados en un archivo, haga clic con el botón secundario en el **panel Editor** y, a continuación, seleccione **Modificaciones locales**.

El **cajón** se abre en la parte inferior de DevTools y muestra los cambios en la **pestaña** Cambios.

:::image type="complex" source="../media/local-modifications.msft.png" alt-text="Mostrar modificaciones locales, en la pestaña Cambios del cajón" lightbox="../media/local-modifications.msft.png":::
   Mostrar **modificaciones locales**, en la pestaña **Cambios** del **cajón**
:::image-end:::

#### <a name="changes-inside-a-function-take-effect"></a>Los cambios dentro de una función tienen efecto

DevTools no vuelve a ejecutar un script, por lo que los únicos cambios de JavaScript que tienen efecto son los cambios que se realicen dentro de las funciones.  Por ejemplo, en la siguiente figura, agregamos el siguiente código al JavaScript que devuelve el servidor:  
*   Se agregó la instrucción `console.log('A')` fuera de cualquier función.  
*   Se agregó la instrucción `console.log('B')` dentro de una `onClick` función.  
A continuación, guardamos los cambios, introdujmos números en el formulario y, a continuación, seleccionamos el botón de formulario para enviar el formulario.  

Después de enviar el formulario, , que está en el ámbito global, no se ejecuta, pero , dentro de una función, se ejecuta, lo que da como resultado `console.log('A')` `console.log('B')` a la `onClick` `B` consola:

:::image type="complex" source="../media/edit-js.msft.png" alt-text="JavaScript de ámbito global no se vuelve a ejecutar" lightbox="../media/edit-js.msft.png":::
   JavaScript de ámbito global no se vuelve a ejecutar  
:::image-end:::

### <a name="reformatting-a-minified-javascript-file-with-pretty-print"></a>Reformatear un archivo JavaScript minificado con pretty-print

Para usar pretty-print para volver a formatear un **** archivo para que sea legible, seleccione el botón De impresión bastante \( Formato \), que se muestra como llaves, en la parte inferior del ![ ](../media/format-icon.msft.png) panel Editor.  O bien, si **aparece un botón De impresión** bastante en la parte superior del panel Editor, puede seleccionar ese botón.

:::image type="complex" source="../media/minified.msft.png" alt-text="El botón De impresión bastante" lightbox="../media/minified.msft.png":::
   El **botón De impresión** bastante  
:::image-end:::  

El archivo reformateado aparece en una pestaña nueva, con `:formatted` anexado al nombre del archivo.  El código reformateado es de solo lectura.  

:::image type="complex" source="../media/pretty-printed.msft.png" alt-text="Un archivo JavaScript bastante impreso (reformateado)" lightbox="../media/pretty-printed.msft.png":::
   Un archivo JavaScript bastante impreso (reformateado)  
:::image-end:::  

Para hacer que el archivo reformateado se desplace al código que seleccione en el archivo minificado: 
1.   Si la pestaña de archivo reformateado está abierta, cierre.  
1.   Seleccione algún código en el archivo minificado en el panel Editor.
1.   Seleccione el **botón Imprimir** bastante.
El código con formato aparece en una pestaña nueva y se desplaza hasta el código seleccionado.

Para obtener más información, [vea Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].  

### <a name="mapping-minified-code-to-your-source-code-to-show-readable-code"></a>Asignación de código minificado al código fuente para mostrar código legible

Los mapas de origen de los preprocesadores hacen que DevTools cargue los archivos de origen de JavaScript originales, además de los archivos JavaScript minificados y transformados que devuelve el servidor.  A continuación, puede ver los archivos de origen originales mientras establece puntos de interrupción y atraviesa el código.  Mientras tanto, Microsoft Edge está ejecutando el código minificado.  

En el **panel Editor,** si hace clic con el botón secundario en un archivo JavaScript y luego selecciona Agregar mapa de **origen,** aparecerá un cuadro emergente, con un cuadro de texto Dirección **URL** de mapa de origen y un **botón** Agregar.

El enfoque de asignación de origen mantiene el código front-end legible y depurable incluso después de combinarlo, minificarlo o compilarlo.
Para obtener más información, vea [Map preprocessed code to source code][DevToolsJavaScriptSourceMaps].

### <a name="transformations-from-source-code-to-compiled-front-end-code"></a>Transformaciones del código fuente al código front-end compilado

Si usa un marco que transforma los archivos JavaScript, como React, el Código JavaScript de origen local puede ser diferente al JavaScript front-end que devuelve el servidor.  En este escenario no se admiten áreas de trabajo, pero en este escenario se admite la asignación de código fuente.  

En un entorno de desarrollo, el servidor puede incluir los mapas de origen y el original `.ts` o los archivos de `.jsx` React.  La **herramienta Orígenes** muestra estos archivos, pero no permite editar estos archivos.  Cuando se establecen puntos de interrupción y se usa el depurador, DevTools muestra el original o los archivos, pero en realidad se hace un paso a través de la versión minificada de los `.ts` `.jsx` archivos JavaScript.

En este escenario, la herramienta **Orígenes** es útil para inspeccionar y realizar un paso a través del JavaScript front-end transformado que se devuelve desde el servidor.  Use el depurador para definir expresiones Watch y use la Consola para escribir expresiones de JavaScript para manipular datos que están dentro del ámbito.

### <a name="editing-a-css-file"></a>Edición de un archivo CSS

Hay dos formas de editar CSS en DevTools:
*   En la **herramienta Elementos,** se trabaja con una configuración CSS a la vez, a través de controles de interfaz de usuario.  Este enfoque se recomienda en la mayoría de los casos.  Para obtener más información, vea [Edit CSS font styles and settings in the Styles pane][DevToolsInspectStylesEditFonts].
*   En la **herramienta Orígenes,** se usa un editor de texto.

La herramienta Orígenes admite la edición directa de un archivo CSS.  Por ejemplo, si edita el archivo CSS desde el tutorial Editar archivos con áreas de [trabajo][DevtoolsGuideChromiumWorkspacesIndex] para que coincidan con la regla de estilo siguiente, el elemento de la parte superior izquierda de la página web representado `H1` cambia a verde:

```css
h1 {
  color: green;
}  
```

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS en el panel Editor para cambiar el color del texto del encabezado H1 a verde" lightbox="../media/edit-css.msft.png":::
   Editar CSS en el **panel Editor** para cambiar el color del texto del encabezado `H1` a verde  
:::image-end:::  

Los cambios CSS se llevan a efecto inmediatamente; no es necesario guardar manualmente los cambios.

#### <a name="see-also"></a>Consulte también

*   [Editar estilos y opciones de fuente CSS en el panel Estilos][DevToolsInspectStylesEditFonts]

*   [DevTools para principiantes: Introducción a CSS][DevToolsBeginnersCss] - tutorial

### <a name="editing-an-html-file"></a>Edición de un archivo HTML

Hay dos formas de editar HTML en DevTools:  
*   En la **herramienta Elementos,** se trabaja con un elemento HTML a la vez, a través de controles de interfaz de usuario.  
*   En la **herramienta Orígenes,** se usa un editor de texto.  

:::image type="complex" source="../media/sources-html-editor.msft.png" alt-text="El editor HTML de la herramienta Orígenes" lightbox="../media/sources-html-editor.msft.png":::
   El editor HTML de la **herramienta Orígenes**
:::image-end:::  

A diferencia de un archivo JavaScript o CSS, un archivo HTML devuelto por el servidor web no se puede editar directamente en la herramienta Orígenes.  Para editar un archivo HTML con el Editor de la herramienta Orígenes, el archivo HTML debe estar en un área de trabajo o en la pestaña **Invalidaciones.**  Vea estas subsecciones del artículo actual:
*   [Uso de la pestaña Sistema de archivos para definir un área de trabajo local](#using-the-filesystem-tab-to-define-a-local-workspace)
*   [Uso de la pestaña Invalidaciones para invalidar archivos de servidor con archivos locales](#using-the-overrides-tab-to-override-server-files-with-local-files)
    
Para guardar los cambios, `Ctrl` + `S` selecciona en Windows/Linux o `Command` + `S` en macOS.  Un archivo editado está marcado por un asterisco.  

Para buscar texto, selecciona `Ctrl` + `F` en Windows/Linux o `Command` + `F` en macOS.

Para deshacer una edición, selecciona `Ctrl` + `Z` en Windows/Linux o `Command` + `Z` en macOS.

Para ver otros comandos al editar un archivo HTML, en el panel Editor, haga clic con el botón secundario en el archivo HTML.

También puede editar HTML mediante un editor HTML, en lugar de DevTools.  Por ejemplo, el artículo [DevTools para principiantes:][DevToolsBeginnersHtml] Introducción a HTML y dom usa un sitio web que permite la edición HTML dentro de la página web.

### <a name="going-to-a-line-number-or-function"></a>Ir a una función o número de línea

Para ir a un número de línea o símbolo (como un nombre de función) en el archivo que está abierto en el panel Editor, puede usar el menú Comando, en lugar de desplazarse por el archivo.

1.   En el **panel Navegador,** seleccione los puntos suspensivos (...) (**Más opciones**) y, a continuación, seleccione Abrir **archivo**.  Aparece el menú comando.  
1.   Escriba uno de los siguientes caracteres:  

| Carácter | Nombre del comando | Propósito |
|---|---|---|
| \: | **Ir a la línea** | Vaya a un número de línea. |
| \@ | **Ir al símbolo** | Vaya a una función.  Al escribir , el menú comando enumera las funciones que se encuentran en el archivo JavaScript que `@` está abierto en el panel Editor. |
   
Para obtener más información, vea [Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge][DevToolsCommandMenuIndex].

### <a name="displaying-source-files-when-using-a-different-tool"></a>Mostrar archivos de origen al usar una herramienta diferente

El lugar principal para ver los archivos de origen en DevTools está dentro de la **herramienta** Orígenes.  Pero a veces es necesario tener acceso a otras herramientas, como **Elementos** o **Consola,** mientras se ven o editan los archivos de origen.  Use la **herramienta Orígenes rápidos** en el [cajón][DevtoolsCustomizeIndexDrawer].

1.  Seleccione una herramienta que no sea **la herramienta Orígenes,** como la **herramienta Elementos.**  
1.  Seleccione `Ctrl` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).  Se abre el menú comando.  
1.  Escriba `Quick Source` y, a continuación, **seleccione Mostrar origen rápido**.  En la parte inferior de la ventana DevTools, aparece el cajón, con el panel **Origen rápido** seleccionado.  El **panel Origen rápido** contiene el último archivo que editó en la herramienta **Orígenes,** dentro de una versión compacta del editor de código DevTools.  
1.  Seleccione `Ctrl` + `P` \(Windows, Linux\) o `Command` + `P` \(macOS\) para abrir el **cuadro de diálogo Abrir** archivo.  

## <a name="using-the-debugger-pane-to-debug-javascript-code"></a>Uso del panel Depurador para depurar código JavaScript

Use el depurador de JavaScript para pasar por el código JavaScript devuelto por el servidor. El depurador incluye el **panel Depurador,** junto con los puntos de interrupción que se establecen en líneas de código en el **panel Editor.**

Con el depurador, se pasa por el código mientras se observan las expresiones de JavaScript especificadas.  Observe y cambie manualmente los valores de las variables y muestre automáticamente qué variables están en el ámbito de la instrucción actual.

:::image type="complex" source="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png" alt-text="El panel Depurador de la herramienta Orígenes  " lightbox="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png":::
   El **panel Depurador** de la herramienta **Orígenes**  
:::image-end:::  

El depurador admite acciones de depuración estándar, como:  
*   Establecer puntos de interrupción para pausar el código.
*   Paso a paso por el código.
*   Visualización y edición de propiedades y variables.
*   Ver los valores de las expresiones de JavaScript.
*   Visualización de la pila de llamadas (la secuencia de llamadas de función hasta ahora).

El depurador de DevTools está diseñado para que se vea, se sienta y funcione como el depurador en [Visual Studio Code][CodeVisualStudioComDocsEditorDebugging] y el depurador [en Visual Studio][DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger].

Las subsecciones siguientes cubren la depuración:
*   [El enfoque básico para usar un depurador](#the-basic-approach-to-using-a-debugger)
*   [Ventajas de watch y scope sobre console.log del depurador](#advantages-of-the-debuggers-watch-and-scope-over-consolelog)
*   [Depurar desde Visual Studio código directamente](#debug-from-visual-studio-code-directly)
*   [Artículos sobre depuración](#articles-about-debugging)

### <a name="the-basic-approach-to-using-a-debugger"></a>El enfoque básico para usar un depurador

Para solucionar problemas de código JavaScript, puede insertar `console.log()` instrucciones en el panel **Editor.**  Otro enfoque más eficaz es usar el depurador de Microsoft Edge DevTools.  En realidad, el uso de un depurador puede ser más sencillo que , una vez que estés `console.log()` familiarizado con el enfoque del depurador.

Para usar un depurador en una página web, normalmente se establece un punto de interrupción y, a continuación, se envía un formulario desde la página web, de la siguiente manera:

1.  Abra la página web en una nueva pestaña del explorador.  Por ejemplo, abra esta página web de formulario en una nueva [pestaña: Demo: Get Started Debugging JavaScript with Microsoft Edge (Chromium) DevTools][DevtoolsGlitchMeDebugJsGetStarted].

1.  Seleccione `F12` para abrir la ventana **DevTools** y, a continuación, seleccione la **pestaña** Orígenes.

1.  En el **panel Navegador** (a la izquierda), seleccione la pestaña **Página** y, a continuación, seleccione el archivo JavaScript, como `get-started.js` .

1.  En el **panel Editor,** seleccione un número de línea cerca de una línea de código sospechosa para establecer un punto de interrupción en esa línea.  En la figura siguiente, se establece un punto de interrupción en la línea `var sum = addend1 + addend2;` .

1.  En la página web, escriba valores y envíe el formulario.  Por ejemplo, escriba números, como y, a continuación, seleccione el botón `5` `1` Agregar número **1 y Número 2**.  

    El depurador ejecuta el código JavaScript y, a continuación, se pausa en el punto de interrupción.  El depurador está ahora en modo pausado, por lo que puede inspeccionar los valores de las propiedades que están en el ámbito y pasar por el código.

    :::image type="complex" source="../media/sources-paused-breakpoint-highlights.msft.png" alt-text="Introducción al modo pausado del depurador" lightbox="../media/sources-paused-breakpoint-highlights.msft.png":::
        Introducción al modo pausado del depurador  
    :::image-end:::  

    En la figura anterior, agregamos las expresiones Watch y , y hemos pasado dos `sum` líneas más allá del punto de `typeof sum` interrupción.

1.  Examine los valores del **panel Ámbito,** que muestra todas las variables o propiedades que están dentro del ámbito del punto de interrupción actual y sus valores.  O bien, agregue expresiones en el **panel** Ver.  Estas expresiones son las mismas expresiones que escribiría en una `console.log` instrucción para depurar el código.  Para ejecutar comandos de JavaScript para manipular datos en el contexto actual, use la **consola**.  Para abrir la consola, seleccione `Esc` .  

1.  Pase por el código mediante los controles de la parte superior del panel **Depurador,** como **Step** ( `F9` ).

#### <a name="see-also"></a>Consulte también

*   [Introducción a la depuración de JavaScript:][DevtoolsGuideChromiumJavascriptIndex] un tutorial con una página web sencilla y existente que contiene algunos controles de formulario.

### <a name="advantages-of-the-debuggers-watch-and-scope-over-consolelog"></a>Ventajas del depurador \'s Watch and Scope over console\.log

Estos tres enfoques son equivalentes:

*   Agregar temporalmente las instrucciones `console.log(sum)` y `console.log(typeof sum)` en el código, donde está en `sum` el ámbito.
*   Emitir las instrucciones y en el panel Consola de DevTools, cuando el depurador se pausa `sum` donde está en el `console.log(typeof sum)` **** `sum` ámbito.
*   Establecer las **expresiones** Watch `sum` y en el panel `typeof sum` **Depurador.**

Cuando la variable está en el ámbito y su valor se muestra automáticamente en la sección Ámbito del panel Depurador, y también se sobrelada en el panel Editor donde `sum` `sum` se **** **** `sum` calcula.  Por lo tanto, probablemente no tendría que definir una expresión Watch para `sum` .

El depurador proporciona una pantalla y un entorno más enriquecidos y flexibles que una `console.log` instrucción.  Por ejemplo, en el depurador, al pasar por el código, puede mostrar y cambiar los valores de todas las propiedades y variables definidas actualmente.  También puede emitir instrucciones JavaScript en **la consola,** como cambiar los valores de una matriz que está dentro del ámbito.  (Para mostrar la consola, seleccione **Esc**.)

Los puntos de interrupción y las expresiones watch se conservan al actualizar la página web.

### <a name="debug-from-visual-studio-code-directly"></a>Depurar desde Visual Studio código directamente

Para usar el depurador más completo de Visual Studio Code en lugar del depurador DevTools, use la extensión **Microsoft Edge Tools for VS Code** para Visual Studio Code.

:::image type="complex" source="../media/microsoft-edge-tools-for-vs-code-extension.msft.png" alt-text="La extensión Herramientas de Microsoft Edge para VS Code para Visual Studio código" lightbox="../media/microsoft-edge-tools-for-vs-code-extension.msft.png":::
   La **extensión Herramientas de Microsoft Edge para VS Code** para Visual Studio código  
:::image-end:::  

Esta extensión proporciona acceso a los **elementos** **y** herramientas de red de Microsoft Edge DevTools, desde Microsoft Visual Studio Code.  

Para obtener más información, [vea Visual Studio de][DevToolsVSCodeIndex] código y la página GitHub Readme, Microsoft Edge Developer Tools for Visual Studio [Code][GithubMicrosoftVscodeEdgeDevtools].

### <a name="articles-about-debugging"></a>Artículos sobre depuración

Los siguientes artículos abarcan el **panel Depurador** y los puntos de interrupción:

*   [Introducción a la depuración de JavaScript en Microsoft Edge DevTools:][DevtoolsGuideChromiumJavascriptIndex] un tutorial (con capturas de pantalla), con un proyecto simple y existente.

*   [Usar las características][DevToolsJavaScriptReference] del depurador: cómo usar el depurador para establecer puntos de interrupción, pasar por el código, ver y modificar valores de variables, ver expresiones de JavaScript y ver la pila de llamadas.

*   [Pausar el código con puntos de interrupción:][DevToolsJavaScriptBreakpoints] cómo establecer puntos de interrupción básicos y especializados en el depurador.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsBeginnersCss]: ../beginners/css.md "DevTools para principiantes: Introducción a CSS | Microsoft Docs"
[DevToolsBeginnersHtml]: ../beginners/html.md "DevTools para principiantes: Introducción a HTML y el dom | Microsoft Docs"
[DevToolsCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Drawer: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de Microsoft Edge DevTools (Undock, Dock to bottom, Dock to left) | Microsoft Docs"
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar archivos con áreas de trabajo | Microsoft Docs"  
[DevToolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos y opciones de fuente CSS en el panel Estilos | Microsoft Docs"
[DevToolsJavaScriptBreakpoints]: ../javascript/breakpoints.md "Pausa el código con puntos de interrupción | Microsoft Docs"
[DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]: ../javascript/guides/mark-content-scripts-library-code.md "Marcar scripts de contenido como código de biblioteca | Microsoft Docs"
[DevtoolsJavascriptOverrides]: ../javascript/overrides.md "Invalidar recursos de página web con copias locales mediante Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavaScriptReference]: ../javascript/reference.md "Usar las características del depurador | Microsoft Docs"
[DevToolsJavaScriptReferenceReformat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Volver a formatear un archivo JavaScript minificado con pretty-print: use las características del depurador | Microsoft Docs"
[DevToolsJavaScriptSourceMaps]: ../javascript/source-maps.md "Asignar código preprocesado al código fuente | Microsoft Docs"
[DevToolsVSCodeIndex]: ../../visual-studio-code/index.md "Visual Studio introducción al código | Microsoft Docs"
[ExtensionsChromiumGetstartPart2ContentScripts]: ../../extensions-chromium/getting-started/part2-content-scripts.md "Crear un tutorial de extensión Parte 2 | Microsoft Docs"
<!-- external: -->
[CodeVisualStudioComDocsEditorDebugging]: https://code.visualstudio.com/docs/editor/debugging "Depuración: Visual Studio código | Microsoft Docs"
[DMCVisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]: https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger "Navegue por el código con el Visual Studio depurador | Microsoft Docs"
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Herramientas para desarrolladores de Microsoft Edge para Visual Studio código | GitHub"
[DevtoolsGlitchMeDebugJsGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Demostración: Introducción a la depuración de JavaScript con Microsoft Edge (Chromium) DevTools | Microsoft Docs"
[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origen | Estándar HTML"  
[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Fotogramas | W3C"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de contenido | MDN"  
[TypescriptlangMain]: https://www.typescriptlang.org "TypeScript"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/sources) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

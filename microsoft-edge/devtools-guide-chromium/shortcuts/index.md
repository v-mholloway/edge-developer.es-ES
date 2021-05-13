---
description: La documentación canónica para Microsoft Edge métodos abreviados de teclado de DevTools.
title: Microsoft Edge Métodos abreviados de teclado de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f2b10bc763073632975248cd5a9caa523702e869
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565102"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="microsoft-edge-devtools-keyboard-shortcuts"></a>Microsoft Edge Métodos abreviados de teclado de DevTools  

Este artículo es una referencia de los métodos abreviados de teclado en Microsoft Edge DevTools.

También puede encontrar accesos directos en la información sobre herramientas.  Mantenga el mouse sobre un elemento de interfaz de usuario de DevTools para mostrar la información sobre herramientas.  Si el elemento tiene un acceso directo, la información sobre herramientas lo incluye.

## <a name="keyboard-shortcuts-for-opening-devtools"></a>Métodos abreviados de teclado para abrir DevTools  

Para abrir DevTools, seleccione los siguientes métodos abreviados de teclado mientras el cursor está centrado en la ventanilla del explorador.

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Abra el panel que usó por última vez | `F12` o `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Abrir la **herramienta Consola** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Abrir la **herramienta** Elementos | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` o `Command`+`Option`+`C` |  

## <a name="global-keyboard-shortcuts"></a>Métodos abreviados de teclado globales  

Los siguientes métodos abreviados de teclado están disponibles en la mayoría de los paneles DevTools, si no todos.

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Mostrar **Configuración** | `?` or `F1` | `?` o `Function`+`F1` |  
| Centrar el panel siguiente | `Control`+`]` | `Command`+`]` |  
| Centrar el panel anterior | `Control`+`[` | `Command`+`[` |  
| Vuelva a la posición [de acoplamiento que][DevtoolsCustomizeIndexPlacement] usó por última vez.  Si DevTools ha estado en la posición predeterminada para toda la sesión, este acceso directo desacopla DevTools en una ventana independiente | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Alternar [emulación de dispositivo][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Alternar **el modo de elemento Inspect** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Abrir el [menú de comandos][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Alternar el [cajón][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Actualización normal | `F5` o `Control`+`R` | `Command`+`R` |  
| Actualización dura | `Control`+`F5` o `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Busque texto en el panel actual.  No se admite en las **herramientas auditorías,** **aplicaciones**y **seguridad** | `Control`+`F` | `Command`+`F` |  
| Abre la **pestaña Búsqueda** en [el][DevtoolsCustomizeIndexDrawer]cajón, que le permite buscar texto en todos los recursos cargados | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Abrir un archivo en la **herramienta Orígenes** | `Control`+`O` o `Control`+`P` | `Command`+`O` o `Command`+`P` |  
| Acercar | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Alejar | `Control`+`-` | `Command`+`-` |  
| Restaurar el nivel de zoom predeterminado | `Control`+`0` | `Command`+`0` |  
| Ejecutar fragmento de código | Seleccione `Control` + `O` para abrir el [menú comando][DevtoolsCommandMenuIndex], escriba seguido del nombre del script y, a `!` continuación, seleccione `Enter` | Seleccione `Command` + `O` para abrir el [menú comando][DevtoolsCommandMenuIndex], escriba seguido del nombre del script y, a `!` continuación, seleccione `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## <a name="elements-tool-keyboard-shortcuts"></a>Métodos abreviados de teclado de la herramienta Elements  

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Deshacer cambio | `Control`+`Z` | `Command`+`Z` |  
| Cambio de rehacer | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Seleccione el elemento anterior / debajo del elemento seleccionado actualmente | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Expanda el nodo seleccionado actualmente.  Si el nodo ya está expandido, este acceso directo selecciona el elemento debajo de él | `Right Arrow` | `Right Arrow` |  
| Contraiga el nodo seleccionado actualmente.  Si el nodo ya está contraído, este acceso directo selecciona el elemento encima de él | `Left Arrow` | `Left Arrow` |  
| Expandir o contraer el nodo seleccionado actualmente y todos los elementos secundarios | Hold `Control` + `Alt` , a continuación, elija el **icono de** flecha junto al nombre del elemento | Hold `Option` , a continuación, elija el **icono de** flecha junto al nombre del elemento |  
| Alternar **el modo Editar atributos** en el elemento seleccionado actualmente | `Enter` | `Enter` |  
| Seleccione el atributo siguiente o anterior después de entrar en el **modo Editar atributos** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Ocultar el elemento seleccionado actualmente | `H` | `H` |  
| Alternar **editar como modo HTML** en el elemento seleccionado actualmente | `Function`+`F2` | `F2` |  

### <a name="styles-panel-keyboard-shortcuts"></a>Métodos abreviados de teclado del panel Estilos  

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Navegue a la línea donde se declara un valor de propiedad | Hold `Control` y, a continuación, seleccione el valor de la propiedad | Hold `Command` y, a continuación, seleccione el valor de la propiedad |  
| Recorrer las representaciones RBGA, HSLA y Hex de un valor de color | Hold `Shift` y, a continuación, elija el **cuadro Vista previa** de color junto al valor | Hold `Shift` y, a continuación, elija el **cuadro Vista previa** de color junto al valor |  
| Seleccione la siguiente o anterior propiedad o valor | Elija un nombre o valor de propiedad y, a continuación, seleccione `Tab` / `Shift`+`Tab` | Elija un nombre o valor de propiedad y, a continuación, seleccione `Tab` / `Shift`+`Tab` |  
| Incrementar o disminuir un valor de propiedad en 0,1 | Elija un valor y, a continuación, seleccione `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Elija un valor y, a continuación, `Option` + `Up Arrow` seleccione / Opción+Flecha abajo |  
| Incrementar o disminuir un valor de propiedad en 1 | Elija un valor y, a continuación, seleccione `Up Arrow` / `Down Arrow` | Elija un valor y, a continuación, seleccione `Up Arrow` / `Down Arrow` |  
| Incrementar o disminuir un valor de propiedad en 10 | Elija un valor y, a continuación, seleccione `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Elija un valor y, a continuación, seleccione `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Incrementar o disminuir un valor de propiedad en 100 | Elija un valor y, a continuación, seleccione `Control`+`Up Arrow` / `Control`+`Down Arrow` | Elija un valor y, a continuación, seleccione `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## <a name="sources-tool-keyboard-shortcuts"></a>Métodos abreviados de teclado de la herramienta Sources  

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Pause script runtime \(if currently running\) or resume \(if currently paused\) | `F8` o `Control`+`\` | `F8` o `Command`+`\` |  
| Paso a paso sobre la siguiente llamada de función | `F10` o `Control`+`'` | `F10` o `Command`+`'` |  
| Paso a siguiente llamada de función | `F11` o `Control`+`;` | `F11` o `Command`+`;` |  
| Salir de la función actual | `Shift`+`F11` o `Control`+`Shift`+`;` | `Shift`+`F11` o `Command`+`Shift`+`;` |  
| Continuar con una [línea de código específica mientras está en pausa][DevtoolsJavascriptBreakpointsLOC] | Hold `Control` y, a continuación, elija la línea de código | Hold `Command` y, a continuación, elija la línea de código |  
| Seleccione el marco de llamada debajo / encima del marco seleccionado actualmente | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Guardar cambios en modificaciones locales | `Control`+`S` | `Command`+`S` |  
| Guardar todos los cambios | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Navegar a la línea | `Control`+`G` | `Control`+`G` |  
| Vaya a un número de línea del archivo abierto actualmente | Seleccione `Control` + `O` para abrir el menú [comando][DevtoolsCommandMenuIndex], escriba `:` seguido del número de línea y, a continuación, seleccione `Enter` | Seleccione `Command` + `O` para abrir el menú [comando][DevtoolsCommandMenuIndex], escriba `:` seguido del número de línea y, a continuación, seleccione `Enter` |  
| Vaya a una columna del archivo actualmente abierto \(por ejemplo, línea 5, columna 9\) | Seleccione para abrir el menú comando , escriba , a continuación, el número de línea, luego otro , a `Control` + `O` continuación, el número de columna [][DevtoolsCommandMenuIndex] `:` `:` y, a continuación, seleccione `Enter` | Seleccione para abrir el menú comando , escriba , a continuación, el número de línea, luego otro , a `Command` + `O` continuación, el número de columna [][DevtoolsCommandMenuIndex] `:` `:` y, a continuación, seleccione `Enter` |  
| Vaya a una declaración de función, si el archivo actual es HTML o un script.  <br />  Vaya a un conjunto de reglas, si el archivo actual es una hoja de estilos.  | Seleccione , escriba el nombre del conjunto de reglas `Control` + `Shift` + `O` o declaración, o selecciónelo en la lista de opciones | Seleccione , escriba el nombre del conjunto de reglas `Command` + `Shift` + `O` o declaración, o selecciónelo en la lista de opciones |  
| Cerrar la pestaña activa | `Alt`+`W` | `Option`+`W` |  

### <a name="code-editor-keyboard-shortcuts"></a>Métodos abreviados de teclado del Editor de código  

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Eliminar todos los caracteres de la última palabra, hasta el cursor | `Control`+`Delete` | `Option`+`Delete` |  
| Agregar o quitar un [punto de interrupción de línea de código][DevtoolsJavascriptBreakpointsLOC] | Centrar el cursor en la línea y, a continuación, seleccionar `Control`+`B` | Centrar el cursor en la línea y, a continuación, seleccionar `Command`+`B` |  
| Navegar a corchetes de coincidencia | `Control`+`M` | `Control`+`M` |  
| Alternar comentario de línea única.  Si se seleccionan varias líneas, DevTools agrega un comentario al inicio de cada línea | `Control`+`/` | `Command`+`/` |  
| Active o desactive la siguiente aparición de cualquier palabra en la que esté el cursor.  Cada aparición se resalta simultáneamente | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## <a name="performance-tool-keyboard-shortcuts"></a>Métodos abreviados de teclado de la herramienta de rendimiento  

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Iniciar o detener la grabación | `Control`+`E` | `Command`+`E` |  
| Guardar grabación | `Control`+`S` | `Command`+`S` |  
| Cargar grabación | `Control`+`O` | `Command`+`O` |  

## <a name="memory-tool-keyboard-shortcuts"></a>Métodos abreviados de teclado de la herramienta de memoria  

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Iniciar o detener la grabación | `Control`+`E` | `Command`+`E` |  

## <a name="console-tool-keyboard-shortcuts"></a>Métodos abreviados de teclado de la herramienta de consola  

| Acción | Windows\/Linux | macOS |  
|:--- |:--- |:--- |  
| Aceptar sugerencia de autocompletar | `Right Arrow` or `Tab` | `Right Arrow` or `Tab` |  
| Rechazar sugerencia de autocompletar | `Escape` | `Escape` |  
| Obtener instrucción anterior | `Up Arrow` | `Up Arrow` |  
| Obtener siguiente instrucción | `Down Arrow` | `Down Arrow` |  
| Centrar la **consola** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Borrar la **consola** | `Control`+`L` | `Command`+`K` o `Option`+`L` |  
| Forzar una entrada de varias líneas.  Este acceso directo es en su mayoría innecesario, ya que DevTools debe detectar escenarios de varias líneas de forma predeterminada | `Shift`+`Enter` | `Command`+`Return` |  
| Ejecutar | `Enter` | `Return` |  
| Expandir todas las subpropiedades de un objeto que se registran en la consola | Mantenga `Alt` y, a **continuación, elija Expandir** \( Expandir ![ ](../media/expand-icon.msft.png) \) | Mantenga `Alt` y, a **continuación, elija Expandir** \( Expandir ![ ](../media/expand-icon.msft.png) \) |  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Drawer: personalice Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexPlacement]: ../customize/index.md#change-devtools-placement "Cambiar ubicación de DevTools: personalizar Microsoft Edge devTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../device-mode/index.md "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLOC]: ../javascript/breakpoints.md#line-of-code-breakpoints "Puntos de interrupción de línea de código: cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/shortcuts) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
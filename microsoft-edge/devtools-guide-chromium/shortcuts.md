---
description: La documentación canónica de los métodos abreviados de teclado de Microsoft Edge DevTools.
title: Métodos abreviados de teclado de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 78e96fa3ae927a8aee24dfc18d4fa6ee515556a8
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125345"
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
   limitations under the License. -->

# Métodos abreviados de teclado de Microsoft Edge DevTools  

Este artículo es una referencia de los métodos abreviados de teclado en Microsoft Edge DevTools.

También puede encontrar métodos abreviados en la información sobre herramientas. Pase el puntero sobre un elemento de la interfaz de usuario de DevTools para mostrar la información sobre herramientas. Si el elemento tiene un acceso directo, la información sobre herramientas lo incluye.

## Métodos abreviados de teclado para abrir DevTools  

Para abrir DevTools, seleccione los siguientes métodos abreviados de teclado mientras el cursor se centra en la ventanilla del explorador.

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Abrir el panel que usó en último lugar | `F12` ni `Control`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Abrir el panel de **consola** | `Control`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Abrir el panel **elementos** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` ni `Command`+`Option`+`C` |  

## Métodos abreviados de teclado globales  

Los siguientes métodos abreviados de teclado están disponibles en la mayoría de los paneles DevTools.

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Mostrar **configuración** | `?` o `F1` | `?` ni `Function`+`F1` |  
| Centrar el panel siguiente | `Control`+`]` | `Command`+`]` |  
| Centrarse en el panel anterior | `Control`+`[` | `Command`+`[` |  
| Vuelva a la [posición de acoplamiento][DevtoolsCustomizeIndexPlacement] que usó por última vez.  Si DevTools se encontraba en la posición predeterminada para toda la sesión, este método abreviado se desacopla DevTools en una ventana independiente. | `Control`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Activar o desactivar [emulación de dispositivo][DevtoolsDeviceModeIndex] | `Control`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Alternar **inspeccionar modo de elemento** | `Control`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Abrir el [menú de comandos][DevtoolsCommandMenuIndex] | `Control`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Activar o desactivar el [cajón][DevtoolsCustomizeIndexDrawer] | `Escape` | `Escape` |  
| Recarga normal | `F5` ni `Control`+`R` | `Command`+`R` |  
| Recarga de disco | `Control`+`F5` ni `Control`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Buscar texto en el panel actual.  No es compatible con los paneles **Auditoría**, **aplicación**y **seguridad** | `Control`+`F` | `Command`+`F` |  
| Abre la pestaña **Buscar** en el [cajón][DevtoolsCustomizeIndexDrawer], que le permite buscar texto en todos los recursos cargados. | `Control`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Abrir un archivo en el panel **orígenes** | `Control`+`O` ni `Control`+`P` | `Command`+`O` ni `Command`+`P` |  
| Acercar | `Control`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Alejar | `Control`+`-` | `Command`+`-` |  
| Restaurar el nivel de zoom predeterminado | `Control`+`0` | `Command`+`0` |  
| Ejecutar fragmento de código | Seleccione `Control` + `O` para abrir el [menú de comandos][DevtoolsCommandMenuIndex], escriba `!` seguido por el nombre del script y, a continuación, seleccione `Enter` | Seleccione `Command` + `O` para abrir el [menú de comandos][DevtoolsCommandMenuIndex], escriba `!` seguido por el nombre del script y, a continuación, seleccione `Enter` |  

<!-- TODO: make a bug about this UIPlacement link being ambiguous.  -->  
<!-- TODO: Link "Inspect Element Mode" when a good section exists.  -->  

## Métodos abreviados de teclado del panel elementos  

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Deshacer el cambio | `Control`+`Z` | `Command`+`Z` |  
| Rehacer cambiar | `Control`+`Y` | `Command`+`Shift`+`Z` |  
| Seleccionar el elemento por encima o por debajo del elemento seleccionado | `Up Arrow` / `Down Arrow` | `Up Arrow` / `Down Arrow` |  
| Expandir el nodo seleccionado actualmente. Si el nodo ya está expandido, este método abreviado de teclado selecciona el elemento situado debajo de él. | `Right Arrow` | `Right Arrow` |  
| Contraer el nodo seleccionado actualmente. Si el nodo ya está contraído, este método abreviado de teclado selecciona el elemento situado encima de él. | `Left Arrow` | `Left Arrow` |  
| Expandir o contraer el nodo seleccionado actualmente y todos los elementos secundarios | `Control` + `Alt` En espera y, a continuación, elija el icono de **flecha** junto al nombre del elemento. | `Option`En espera y, a continuación, elija el icono de **flecha** junto al nombre del elemento. |  
| Activar o desactivar modificar el modo de **atributos** en el elemento seleccionado actualmente | `Enter` | `Enter` |  
| Seleccionar el atributo siguiente o anterior después de especificar el modo **Editar atributos** | `Tab` / `Shift`+`Tab` | `Tab` / `Shift`+`Tab` |  
| Ocultar el elemento seleccionado actualmente | `H` | `H` |  
| Activar o desactivar **Editar como modo html** en el elemento seleccionado actualmente | `Function`+`F2` | `F2` |  

### Métodos abreviados de teclado del panel estilos  

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Ir a la línea donde se declara un valor de propiedad | Espera `Control` y, después, seleccione el valor de la propiedad | Espera `Command` y, después, seleccione el valor de la propiedad |  
| Recorrer las representaciones RBGA, HSLA y hexadecimales de un valor de color | Espera `Shift` y, a continuación, elija el cuadro **vista previa de color** junto al valor. | Espera `Shift` y, a continuación, elija el cuadro **vista previa de color** junto al valor. |  
| Seleccionar el valor o la propiedad siguiente/anterior | Elija un nombre de propiedad o valor y, a continuación, seleccione `Tab` / `Shift`+`Tab` | Elija un nombre de propiedad o valor y, a continuación, seleccione `Tab` / `Shift`+`Tab` |  
| Aumentar o disminuir el valor de una propiedad por 0,1 | Elija un valor y, a continuación, seleccione `Alt`+`Up Arrow` / `Alt`+`Down Arrow` | Elija un valor y, a continuación, seleccione `Option` + `Up Arrow` /opción + flecha abajo |  
| Aumentar o disminuir un valor de propiedad en 1 | Elija un valor y, a continuación, seleccione `Up Arrow` / `Down Arrow` | Elija un valor y, a continuación, seleccione `Up Arrow` / `Down Arrow` |  
| Aumentar o disminuir el valor de una propiedad en 10 | Elija un valor y, a continuación, seleccione `Shift`+`Up Arrow` / `Shift`+`Down Arrow` | Elija un valor y, a continuación, seleccione `Shift`+`Up Arrow` / `Shift`+`Down Arrow` |  
| Aumentar o disminuir el valor de una propiedad por 100 | Elija un valor y, a continuación, seleccione `Control`+`Up Arrow` / `Control`+`Down Arrow` | Elija un valor y, a continuación, seleccione `Command`+`Up Arrow` / `Command`+`Down Arrow` |  

## Métodos abreviados de teclado del panel orígenes  

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| PAUSE script Runtime \ (si se está ejecutando \) o resume \ (si está en pausa \) | `F8` ni `Control`+`\` | `F8` ni `Command`+`\` |  
| Paso a paso por la siguiente llamada de función | `F10` ni `Control`+`'` | `F10` ni `Command`+`'` |  
| Ir a la siguiente llamada de función | `F11` ni `Control`+`;` | `F11` ni `Command`+`;` |  
| Salir de la función actual | `Shift`+`F11` ni `Control`+`Shift`+`;` | `Shift`+`F11` ni `Command`+`Shift`+`;` |  
| Ir a una [línea de código específica mientras está en pausa][DevtoolsJavascriptBreakpointsLOC] | Espera `Control` y, a continuación, elige la línea de código | Espera `Command` y, a continuación, elige la línea de código |  
| Seleccionar el marco de llamada debajo o encima del fotograma seleccionado actualmente | `Control`+`.` / `Control`+`,` | `Control`+`.` / `Control`+`,` |  
| Guardar los cambios en las modificaciones locales | `Control`+`S` | `Command`+`S` |  
| Guardar todos los cambios | `Control`+`Alt`+`S` | `Command`+`Option`+`S` |  
| Ir a la línea | `Control`+`G` | `Control`+`G` |  
| Ir a un número de línea del archivo abierto actualmente | Seleccione `Control` + `O` para abrir el [menú de comandos][DevtoolsCommandMenuIndex], escriba `:` seguido por el número de línea y, a continuación, seleccione `Enter` | Seleccione `Command` + `O` para abrir el [menú de comandos][DevtoolsCommandMenuIndex], escriba `:` seguido por el número de línea y, a continuación, seleccione `Enter` |  
| Ir a una columna del archivo abierto actualmente \ (por ejemplo, línea 5, columna 9 \) | Seleccione `Control` + `O` para abrir el [menú de comandos][DevtoolsCommandMenuIndex], escriba `:` , luego el número de línea y, a continuación `:` , el número de columna y, después, seleccione `Enter` | Seleccione `Command` + `O` para abrir el [menú de comandos][DevtoolsCommandMenuIndex], escriba `:` , luego el número de línea y, a continuación `:` , el número de columna y, después, seleccione `Enter` |  
| Ir a una declaración de función si el archivo actual es HTML o un script. <br /> Ir a un conjunto de reglas si el archivo actual es una hoja de estilos. | Seleccione `Control` + `Shift` + `O` y, a continuación, escriba el nombre del conjunto de reglas o la declaración, o selecciónelo en la lista de opciones. | Seleccione `Command` + `Shift` + `O` y, a continuación, escriba el nombre del conjunto de reglas o la declaración, o selecciónelo en la lista de opciones. |  
| Cerrar la pestaña activa | `Alt`+`W` | `Option`+`W` |  

### Métodos abreviados de teclado del editor de código  

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Eliminar todos los caracteres de la última palabra, hasta el cursor | `Control`+`Delete` | `Option`+`Delete` |  
| Agregar o quitar un [punto de interrupción de línea de código][DevtoolsJavascriptBreakpointsLOC] | Centre el cursor en la línea y, a continuación, seleccione `Control`+`B` | Centre el cursor en la línea y, a continuación, seleccione `Command`+`B` |  
| Ir al corchete coincidente | `Control`+`M` | `Control`+`M` |  
| Activar o desactivar los comentarios de una sola línea. Si se seleccionan varias líneas, DevTools agregar un comentario al principio de cada línea | `Control`+`/` | `Command`+`/` |  
| Seleccione/anular la selección de la siguiente aparición de cualquier palabra en la que se encuentra el cursor. Cada ocurrencia se resalta simultáneamente | `Control`+`D` / `Control`+`U` | `Command`+`D` / `Command`+`U` |  

## Métodos abreviados de teclado del panel de rendimiento  

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Iniciar o detener grabación | `Control`+`E` | `Command`+`E` |  
| Guardar grabación | `Control`+`S` | `Command`+`S` |  
| Cargar grabación | `Control`+`O` | `Command`+`O` |  

## Métodos abreviados de teclado del panel memoria  

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Iniciar o detener grabación | `Control`+`E` | `Command`+`E` |  

## Métodos abreviados de teclado del panel de consola  

| Acción | Windows \/Linux | macOS |  
|:--- |:--- |:--- |  
| Aceptar sugerencia de autocompletar | `Right Arrow` o `Tab` | `Right Arrow` o `Tab` |  
| Rechazar sugerencia de autocompletar | `Escape` | `Escape` |  
| Obtener la instrucción anterior | `Up Arrow` | `Up Arrow` |  
| Instrucción GET NEXT | `Down Arrow` | `Down Arrow` |  
| Centrar la **consola** | `Control`+ `` ` `` | `Control`+`` ` `` |  
| Borrar la **consola** | `Control`+`L` | `Command`+`K` ni `Option`+`L` |  
| Forzar una entrada con varias líneas.  Este acceso directo es principalmente innecesario porque DevTools debería detectar escenarios de varias líneas de forma predeterminada | `Shift`+`Enter` | `Command`+`Return` |  
| Ejecutar | `Enter` | `Return` |  
| Expandir todas las subpropiedades de un objeto que se han registrado en la consola | Espera `Alt` y, a continuación, elija **expandir** \ ( ![ expandir ][ImageExpandIcon] \) | Espera `Alt` y, a continuación, elija **expandir** \ ( ![ expandir ][ImageExpandIcon] \) |  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ./media/expand-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: ./customize/index.md#drawer "Cajón-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomizeIndexPlacement]: ./customize/index.md#change-devtools-placement "Cambiar la ubicación de DevTools: personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsDeviceModeIndex]: ./device-mode/index.md "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsJavascriptBreakpointsLOC]: ./javascript/breakpoints.md#line-of-code-breakpoints "Puntos de interrupción de línea de código: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft docs"  

<!--[201705ReleaseNotesContinue]: whats-new/2017/05/devtools-release-notes#continue  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/shortcuts) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  

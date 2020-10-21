---
description: Guía para navegar por Microsoft Edge DevTools usando tecnología de asistencia como lectores de pantalla.
title: Navegar por Microsoft Edge DevTools con tecnología de asistencia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f4ec63a0d432925b7db99ce695db66dd61f8bcf1
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125296"
---
<!-- Copyright Rob Dodson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# Navegar por Microsoft Edge DevTools con tecnología de asistencia  

El siguiente artículo pretende ayudar a los usuarios que principalmente dependen de la tecnología de asistencia, como los lectores de pantalla, acceder y usar [Microsoft Edge DevTools][MicrosoftEdgeDevtoolsMain].  [Microsoft Edge DevTools][MicrosoftEdgeDevtoolsMain] es un conjunto de herramientas para desarrolladores web integrado en el explorador Microsoft Edge.  Si está buscando características de DevTools relacionadas con la mejora de la accesibilidad de una página web, consulte [referencia de accesibilidad][DevtoolsAccessibilityReference].  

La accesibilidad de DevTools es un trabajo en curso.  Algunos paneles y pestañas funcionan mejor con la tecnología de asistencia que otros.  Esta guía le guiará a través de los paneles que son los problemas específicos más accesibles y resaltados que puede encontrarse durante el proceso.  

## Introducción  

Antes de comenzar, ayuda a tener un modelo mental de estructurar la interfaz de usuario de DevTools.  DevTools se divide en una serie de paneles que se organizan en un [Tablist Aria][W3CWaiAriaTablist].  

Por ejemplo:  

*   El panel **elementos** le permite [ver y cambiar nodos DOM] [DevtoolsDomIndexNavigateDomTreeKeyboard] o [CSS][DevtoolsCssIndex].  
*   El [Panel de consola][DevtoolsConsoleIndex] le permite leer registros de JavaScript y objetos de edición en vivo.  

Dentro del área de contenido de cada panel hay varias herramientas diferentes, a menudo denominadas fichas o paneles en la documentación.  
Por ejemplo, el panel **elementos** contiene pestañas adicionales para inspeccionar detectores de eventos, el árbol de accesibilidad y mucho más.  La distinción entre las pestañas y los paneles es algo arbitrario.  El único motivo por el que puedes ver un término u otro es mantener la coherencia con el resto de la documentación oficial de DevTools.  

## Accesos rápidos de teclado  

La [referencia de métodos abreviados de teclado de DevTools] [DevtoolsShortcuts] es una Cheatsheet útil.  Asegúrese de marcarlo y hacer referencia a él mientras explora los distintos paneles.  

## Abrir DevTools  

Para empezar, vaya a [Open Microsoft Edge DevTools] [DevtoolsOpen].  Hay varias maneras de abrir DevTools, ya sea mediante métodos abreviados de teclado o elementos de menú.  

## Navegar entre paneles  

### Navegar por el teclado  

*   Con DevTools abierto, selecciona `Control` + `]` \ (Windows, Linux \) o `Command` + `]` \ (MacOS \) para centrar la atención en el siguiente panel.  
*   Seleccione `Control` + `[` \ (Windows, Linux \) o `Command` + `[` \ (MacOS \) para centrarse en el panel anterior.  
*   También se puede usar `Shift` + `Tab` para mover el foco a la [Tablist Aria][W3CWaiAriaTablist] de un panel y usar las teclas de dirección para cambiar los paneles, aunque es más rápido usar los métodos abreviados mencionados anteriormente.  

**Problemas conocidos**  

*   Algunos paneles, como los paneles de **consola** y **rendimiento** , pueden mover el foco al área de contenido del panel tan pronto como se active cada panel.  Esto puede dificultar la navegación por las teclas de dirección.  
*   Se anuncia el nombre del panel seleccionado, pero solo después de que haya leído el contenido centrado en el panel.  Esto puede resultar muy fácil de perder.  

### Navegar por el menú de comandos  

Para centrar un panel específico, use el [menú de comandos][DevtoolsCommandMenuIndex]:  

1.  Con DevTools abierto, seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.  
    El **menú comando** es un ComboBox de autocompletar de búsqueda.  
1.  Escriba el nombre del panel que desea abrir y, después, use el `Down Arrow` teclado para desplazarse a la opción correcta.  
1.  Seleccione `Enter` para ejecutar un comando.  

Complete las siguientes acciones para abrir el panel **elementos** .  

1.  Abrir el **menú de comandos**.  
1.  Escriba `E` a continuación `L` .  La opción **Panel > Mostrar elementos** está seleccionada.  
1.  Seleccione `Enter` para ejecutar el comando que abre el panel.  

Abrir un panel de esta forma dirige el foco al contenido del panel.  En el caso del panel **elementos** , el foco se mueve al **árbol DOM**.  

## Panel elementos  

### Inspeccionar un elemento de la página  

1.  Vaya al elemento que desea inspeccionar usando el cursor en el lector de pantalla.  
1.  Simular un clic con el botón secundario del mouse con un mouse en el elemento para abrir el menú contextual.  
1.  Elija la opción **inspeccionar** .  Esto [abre el panel de elementos y se centra en el elemento del árbol DOM] [DevtoolsDomIndexViewDomNodes].  

El **árbol DOM** se coloca como un [árbol Aria][W3CWaiAriaTree].  Para obtener un ejemplo, vaya a [navegar por el **árbol DOM** con un teclado] [DevtoolsDomIndexNavigateDomTreeKeyboard].  

### Copiar el código de un elemento en el árbol DOM  

1.  Con el foco en un nodo del **árbol DOM**, coloque el puntero sobre el nodo y abra el menú contextual \ (haga clic con el botón derecho \).  
1.  Expanda la opción **copiar** .  
1.  Elija **copiar outerHTML**.  

**Problemas conocidos**  

*   La **copia outerHTML** a menudo no selecciona el nodo actual, sino que selecciona el nodo primario.  Sin embargo, el contenido del elemento aún debe estar en el outerHTML copiado.  

### Modificar los atributos de un elemento en el árbol DOM  

*   Con el foco en un nodo del **árbol DOM**, seleccione `Enter` esta para que sea editable.  
*   Seleccione `Tab` para moverse entre los valores de atributo.  Cuando escuche "Space", se encuentra dentro de una entrada de texto vacía y puede escribir un nuevo valor de atributo.  
*   Seleccione `Control` + `Enter` \ (Windows, Linux \) o `Command` + `Enter` \ (MacOS \) para aceptar el cambio y oír todo el contenido del elemento.  

**Problemas conocidos**  

*   Cuando escribes en la entrada de texto, no obtienes Comentarios.  Si hace un error ortográfico y usa las teclas de dirección para explorar la entrada, tampoco recibirá Comentarios.  La manera más sencilla de comprobar su trabajo es aceptar el cambio y, a continuación, escuchar que se anuncie todo el elemento.  

### Editar el código HTML de un elemento en el árbol DOM  

*   Con el foco en un nodo del **árbol DOM**, seleccione `Enter` esta para que sea editable.  
*   Seleccione `Tab` para moverse entre los valores de atributo.  Al oír el nombre del elemento, por ejemplo, `h2` se encuentra dentro de una entrada de texto y puede cambiar el tipo de elemento.  
*   Seleccione `Control` + `Enter` \ (Windows, Linux \) o `Command` + `Enter` \ (MacOS \) para aceptar el cambio.  

Por ejemplo, cuando escribe `h3` y selecciona `Control` + `Enter` \ (Windows, Linux \) o `Command` + `Enter` \ (MacOS \), las etiquetas iniciales y finales del cambio de `h3` elemento.  

## Pestañas del panel elementos  

El panel **elementos** contiene pestañas adicionales para inspeccionar cosas como la CSS aplicada a un elemento o al lugar relevante en el árbol de accesibilidad.  

*   Con el foco en un nodo del **árbol DOM**, seleccione `Tab` hasta que escuche que el panel **estilos** está seleccionado.  
*   Use el `Right Arrow` para explorar otras pestañas disponibles.  

El **árbol DOM** convierte los elementos con `href` atributos en vínculos activables, por lo que es posible que tenga que seleccionar `Tab` más de una vez para llegar al panel **estilos** .  

**Problemas conocidos**  

Las pestañas **puntos de interrupción** y **propiedades** de Dom no son accesibles desde el teclado.  

### Panel estilos  

En el panel **estilos** , busque controles para filtrar estilos, alternar Estados de elementos \ (como [: activo][MDNActive] y [: enfoque][MDNFocus]\), alternar clases y agregar nuevas clases.  También hay una herramienta de inspección de estilo eficaz para explorar y modificar los estilos aplicados actualmente al elemento que se encuentra en el **árbol DOM**.  

El concepto clave que se debe comprender sobre el panel **estilos** es que solo muestra los estilos para el nodo seleccionado en ese momento en el **árbol DOM**.  Por ejemplo, supongamos que ha terminado de inspeccionar los estilos de un `<header>` nodo y ahora desea ver los estilos de un `<footer>` nodo.  Para ello, primero debe seleccionar el `<footer>` nodo en el **árbol DOM**.  Es posible que le resulte más rápido usar [el flujo de trabajo para inspeccionar](#inspect-an-element-on-the-page) un nodo que se encuentra en la general del `footer` nodo \ (como un vínculo dentro del pie de página \), que se centra en el **árbol DOM**y, a continuación, usar el teclado para navegar hasta el nodo exacto en el que esté interesado.  

#### Navegar por el panel estilos  

Puesto que todas las herramientas de estilo se conectan de una forma u otra al panel **estilos** , tiene sentido convertirse primero en experto en esta herramienta.  

*   Con el foco en el panel **estilos** , seleccione `Tab` para mover el foco dentro y explorar el contenido.  
*   Seleccione `Tab` hasta que el primer estilo se active.  Si está usando un lector de pantalla, este primer estilo se anuncia como `element.style {}` .  
*   Seleccione `Down Arrow` para desplazarse por la lista de estilos en orden de especificidad.  Un lector de pantalla anuncia cada estilo empezando por el nombre del archivo CSS, el número de línea en el que aparece el estilo y el nombre del estilo.  Por ejemplo, `main.css:233 .card__img {}`.  
*   Seleccione `Enter` para inspeccionar un estilo de forma más detallada.  El foco comienza en una versión editable del nombre de estilo.  
*   Seleccione `Tab` esta opciones para desplazarse entre las versiones editables de cada propiedad de CSS y los valores correspondientes.  Al final de cada bloque de estilo hay un campo de texto editable en blanco que puede usar para agregar propiedades de CSS adicionales.  
*   Puede seleccionar `Tab` desplazarse por la lista de estilos, o bien, seleccionar `Escape` para salir del modo y volver a navegar por las teclas de dirección.  

Para obtener más métodos abreviados, vaya a [Referencia del teclado del panel de estilos] [DevtoolsShortcutsStylesPaneKeyboard].  

**Problemas conocidos**  

*   Si usa el campo de texto editable **filtro** , ya no podrá navegar por la lista de estilos.  

#### Alternar estado del elemento  

Para alternar el estado de un elemento, como `:active` o `:focus` :  

1.  Vaya al panel **estilos** y seleccione `Tab` hasta que el botón **Estado del elemento de alternancia** tenga el foco.  
1.  Seleccione `Enter` esta opciones para expandir la colección de Estados de elementos.  Los Estados de los elementos se presentan como un grupo de casillas de verificación.  
1.  Seleccione `Tab` hasta el primer estado, `:active` , tiene el foco.  
1.  Seleccione `Space` esta opción para habilitarlo.  Si el elemento seleccionado actualmente en el árbol DOM tiene un `:active` estilo, ahora se aplica.  
1.  Espera `Tab` para explorar todos los Estados disponibles.  

#### Agregar una clase existente  

Junto al botón de **Estado del elemento de alternancia** se encuentra el botón clases de **elementos** .  Para mover el foco a la imagen, seleccione `Tab` y seleccione `Enter` .  El foco se mueve a un campo de texto de edición denominado **Agregar nueva clase**.  

El botón **clases de elementos** se usa principalmente para agregar clases existentes a un elemento.  Por ejemplo, si la hoja de estilos contiene una clase auxiliar denominada `.clearfix` , puede seleccionar `.` dentro del campo editar texto para ver una lista de sugerencias de clases y usar el `Down Arrow` para buscar la `.clearfix` sugerencia.  O bien, escriba el nombre de la clase y seleccione la `Enter` aplicación.  

#### Agregar una nueva regla de estilo  

Junto al botón **clases de elementos** se encuentra el botón **nueva regla de estilo** .  Para mover el foco a la imagen, seleccione `Tab` y seleccione `Enter` .  El foco se mueve a un campo de texto editable dentro del inspector de estilo.  El contenido de texto inicial del campo es el nombre de etiqueta del elemento que está seleccionado en el **árbol DOM**.  
Puede escribir el nombre de la clase que desee en este campo y, a continuación, seleccionar `Tab` para asignarle propiedades de CSS.  

### Pestaña calculada  

Con el foco en la pestaña **calculada** , seleccione `Tab` para mover el foco dentro y explorar el contenido.  En la pestaña **calculada** hay controles para explorar qué propiedades de CSS se aplican realmente a un elemento en orden de especificidad.  

<!--todo: add computed tab section when available  -->  

#### Explorar todos los estilos calculados  

Seleccione `Tab` hasta llegar a la colección de estilos calculados.  Se presentan como un [árbol Aria][W3CWaiAriaTree].  Al expandir un control ListBox, se revela qué selectores CSS están aplicando el estilo calculado.  Estos selectores están organizados por especificidad.  Un lector de pantalla anuncia el valor calculado, que actualmente coincide con el selector de CSS, el nombre de archivo de la hoja de estilos que contiene el selector y el número de línea del selector.  

**Problemas conocidos**  

*   Si usa el campo de texto de **filtro** , ya no podrá inspeccionar estilos.  

### Pestaña detectores de eventos  

Desde el panel **elementos** , puede inspeccionar las escuchas de eventos que se aplican a un elemento mediante la pestaña **detectores de eventos** .  Con el foco en el panel **estilos** , seleccione el `Right Arrow` para ir a la pestaña **detectores de eventos** .  

#### Explorar detectores de eventos  

Los detectores de eventos se presentan como un [árbol Aria][W3CWaiAriaTree].  Puede usar las teclas de dirección para desplazarse.  Un lector de pantalla anuncia el nombre del objeto DOM al que está asociada la escucha de eventos, así como el nombre de archivo en el que se define el agente de escucha de eventos y el número de línea.  

### Panel Accesibilidad  

Con el foco en el panel **accesibilidad** , seleccione `Tab` para mover el foco dentro y explorar el contenido.  En el [panel Accesibilidad][DevtoolsAccessibilityReference] , hay controles para explorar el árbol de accesibilidad, los atributos de Aria que se aplican a un elemento y las propiedades de accesibilidad calculadas.  

#### Árbol de accesibilidad  

El **árbol de accesibilidad** se presenta como un [árbol Aria][W3CWaiAriaTree] , donde cada uno `treeitem` corresponde a un elemento en el Dom.  El árbol anuncia el rol calculado para el nodo seleccionado.  Elementos genéricos como `div` y `span` se anuncian como "GenericContainer" en el árbol.  Use las teclas de dirección para desplazarse por el árbol y explorar las relaciones de elementos primarios y secundarios.  

**Problemas conocidos**  

*   Es posible que el tipo de [árbol Aria][W3CWaiAriaTree] usado por el panel de **accesibilidad** no se exponga correctamente en Microsoft Edge para lectores de pantalla de MacOS como VoiceOver.  Suscríbase al [problema de cromo #868480][ChromiumIssues868480] para estar informado sobre el progreso de este problema.  
*   Cada uno de los **atributos de Aria** y las secciones de **propiedades calculadas** se marcan como un [árbol Aria][W3CWaiAriaTree], pero en este momento no hay administración de foco y no funciona el teclado.  

## Panel auditorías  

El panel **Auditoría** debe ejecutar una serie de pruebas en un sitio para comprobar problemas comunes relacionados con el rendimiento, la accesibilidad, la SEO y un número de otras categorías.  

### Configurar y ejecutar una auditoría  

1.  Cuando se abre por primera vez el panel **auditorías** , el foco se coloca en el botón **Ejecutar auditoría** al final del formulario.  De forma predeterminada, el formulario está configurado para ejecutar auditorías de todas las categorías con emulación móvil en una conexión 3G simulada.  
1.  Use `Shift` + `Tab` o desplácese hacia atrás en el modo de exploración para cambiar la configuración de auditoría.  
1.  Cuando esté listo para ejecutar la auditoría, vuelva al botón **Ejecutar auditoría** y seleccione `Enter` .  
1.  El foco se mueve a una ventana modal con un botón **Cancelar** que le permite salir de la auditoría.  Es posible que oiga una serie de earcons mientras se ejecuta la auditoría y se actualiza la página varias veces.  

**Problemas conocidos**  

*   Las diferentes secciones del formulario de configuración no se marcan actualmente con un `fieldset` elemento.  Puede ser más fácil encontrarlos en el modo de exploración para averiguar qué controles están asociados con cada sección.  
*   No hay ningún anuncio de Earcon ni de región en vivo cuando la auditoría termina de ejecutarse.  Generalmente, tarda unos 30 segundos, después de los cuales debería poder navegar a los resultados.  Usar el modo de exploración puede ser la manera más fácil de alcanzar los resultados.  

### Navegar por el informe de auditoría  

El informe de auditoría se organiza en secciones que corresponden a cada una de las categorías de auditoría.  El informe se abre con una lista de puntuaciones para cada categoría.  Estas puntuaciones también son vínculos que se pueden usar para saltar a las secciones correspondientes.  Dentro de cada sección se incluyen `details` elementos expansibles, que contienen información relacionada con auditorías pasadas o fallidas.  De forma predeterminada, solo se muestran las auditorías con errores.  Cada sección termina con un `details` elemento final que contiene todas las auditorías pasadas.  

Para ejecutar una nueva auditoría, use `Shift` + `Tab` para salir del informe y busque el botón **realizar una auditoría** .  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsAccessibilityReference]: ./reference.md "Referencia de accesibilidad | Microsoft docs"  
[DevtoolsAccessibilityReferencePane]: reference.md#the-accessibility-pane "Panel Accesibilidad-referencia de accesibilidad | Microsoft docs"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft docs"  
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /Dom/index.MD # View-Dom-Nodes "ver nodos DOM: empieza a ver y cambiar DOM | Microsoft docs "  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /Dom/index.MD # navegación-el-Dom-Tree-by-a-Keyboard "navegue por el árbol DOM con un teclado: Introducción a la visualización y cambio del DOM | Microsoft docs "  
[DevtoolsOpen]: .. /open.md "abrir Microsoft Edge DevTools | Microsoft docs "  
[DevtoolsShortcuts]: .. /shortcuts.md "métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft docs "  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /Shortcuts.MD # Styles-panel-teclado de accesos directos "métodos abreviados de teclado del panel de estilos-Microsoft Edge DevTools métodos abreviados de teclado | Microsoft docs "  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problema 868480: exponer árboles de ARIA como tablas en la accesibilidad de Mac"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Nuevo problema: MicrosoftDocs/Edge-Developer | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ": activo | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ": Focus | MDN"  

[MonorailChromiumIssues]: https://crbug.com "Problemas-cromo-monorail"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "Tablist (función): aplicaciones de Internet enriquecidas accesibles (WAI-ARIA) 1,1 | RELATIVA"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "árbol (función): aplicaciones de Internet enriquecidas accesibles (WAI-ARIA) 1,1 | RELATIVA"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) y está creada por [Rob Dodson][RobDodson] \ (colaborador, Google webfundamentals \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[RobDodson]: https://developers.google.com/web/resources/contributors/robdodson  

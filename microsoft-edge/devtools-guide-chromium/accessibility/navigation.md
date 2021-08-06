---
description: Una guía para navegar por Microsoft Edge DevTools con tecnología de asistencia como lectores de pantalla.
title: Navegar Microsoft Edge DevTools con tecnología de asistencia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: e120507d05b95f857dbc27d8151fe460405aba714004f3685a76d8fd41583c81
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802631"
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
# <a name="navigate-microsoft-edge-devtools-with-assistive-technology"></a>Navegar Microsoft Edge DevTools con tecnología de asistencia  

Este artículo ayuda a los usuarios que dependen principalmente de la tecnología de asistencia, como los lectores de [pantalla, Microsoft Edge DevTools][MicrosoftEdgeDevtoolsMain].  DevTools es un conjunto de herramientas de desarrollador web integradas en el Microsoft Edge web.  

Para ver las características de DevTools relacionadas con la mejora de la accesibilidad de una página web, vea [Accessibility-testing features in DevTools][DevtoolsAccessibilityReference] and [Overview of accessibility testing using DevTools](accessibility-testing-in-devtools.md).

La accesibilidad de DevTools es un trabajo en curso.  Algunas herramientas y pestañas funcionan mejor con tecnología de asistencia que otras.  Esta guía le guiará por las herramientas y pestañas que son las más accesibles y resalta los problemas específicos que puede encontrar en el camino.  

## <a name="overview"></a>Información general  

DevTools se divide en una serie de herramientas.  (Dentro del **menú comando,** las herramientas se denominan _paneles_.)  Las herramientas se organizan en una lista de [pestañas de ARIA][W3CWaiAriaTablist] en la barra de herramientas principal y en la barra de herramientas del cajón.

A continuación se muestran ejemplos de herramientas:

*   La **herramienta Elementos** permite [ver y cambiar nodos DOM][DevtoolsDomIndexNavigateDomTreeKeyboard] o [CSS][DevtoolsCssIndex].  
*   La **herramienta Consola** permite leer los registros de JavaScript y los objetos de edición en directo.  Para obtener más información, vaya [a Usar la consola][DevtoolsConsoleIndex].

Dentro de cada herramienta, hay uno o más conjuntos de pestañas.  Por ejemplo, la **herramienta Elementos** contiene un conjunto de pestañas que incluyen **Styles**, **Event Listeners**y **Accessibility**.

## <a name="keyboard-shortcuts"></a>Accesos rápidos de teclado  

[Referencia de métodos abreviados de teclado de DevTools][DevtoolsShortcuts] es una hoja de trucos útil.  Asegúrese de marcarlo y volver a consultarlo a medida que explora las diferentes herramientas.

## <a name="open-devtools"></a>Abrir DevTools  

Para empezar, vaya a [Abrir Microsoft Edge DevTools][DevtoolsOpen].  Hay varias formas de abrir DevTools, ya sea mediante métodos abreviados de teclado o elementos de menú.  

## <a name="navigate-between-tools"></a>Navegar entre herramientas

### <a name="navigate-by-keyboard"></a>Navegar por teclado  

*   Con DevTools abierto, seleccione `Control` + `]` \(Windows, Linux\) o `Command` + `]` \(macOS\) para mover el foco a la siguiente herramienta de la barra de herramientas principal.
*   Seleccione `Control` + `[` \(Windows, Linux\) o `Command` + `[` \(macOS\) para mover el foco a la herramienta anterior en la barra de herramientas principal.
*   Seleccione o repita hasta que el foco se mueva a las pestañas de la barra de herramientas principal o de la barra de herramientas del cajón y, a continuación, use las teclas de flecha para `Tab` `Shift` + `Tab` moverse entre las herramientas.

**Problemas conocidos**  

*   Algunas herramientas, como las **** herramientas **consola** y rendimiento, pueden mover el foco al área de contenido de la herramienta en cuanto se selecciona la herramienta.  Esto puede dificultar la navegación por teclas de flecha.  
*   El nombre de la herramienta seleccionada se anuncia, pero solo después de anunciar el contenido centrado en la herramienta.  Esta secuencia de anuncios puede facilitar la pérdida del nombre de la herramienta.

### <a name="navigate-by-command-menu"></a>Navegar por menú de comandos  

Para seleccionar una herramienta específica, use el [menú comando][DevtoolsCommandMenuIndex].  En el menú comando, una herramienta se denomina _panel_.

1.  Con DevTools abierto, seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para **** abrir el menú de comandos .  
    El **menú de comandos** es un cuadro combinado de autocompletar de búsqueda aproximada.  
1.  Escriba el nombre de un panel (herramienta) y, a continuación, use el teclado para navegar a `Down Arrow` la opción correcta.  
1.  Seleccione `Enter` para ejecutar un comando.  

Para abrir la **herramienta** Elementos:

1.  Abra el **Menú de comandos**.  
1.  Escriba `E` a `L` continuación .  La **opción Panel > Mostrar elementos** está seleccionada.  
1.  Seleccione `Enter`.  

Abrir una herramienta de esta manera pone el foco en el área de contenido de la herramienta.  En el caso de la **herramienta Elementos,** el foco se mueve al **árbol DOM**.

## <a name="elements-tool"></a>Herramienta Elementos

### <a name="inspect-an-element-on-the-page"></a>Inspeccionar un elemento de la página  

1.  Navegue hasta el elemento que desea inspeccionar con el cursor en el lector de pantalla.  
1.  Simule un clic con el botón derecho en el elemento para abrir el menú contextual.  
1.  Elija la **opción Inspeccionar.**  Esto [abre la herramienta Elementos y centra el elemento en el árbol DOM][DevtoolsDomIndexViewDomNodes].  

El **árbol DOM** se establece como un árbol [ARIA.][W3CWaiAriaTree]  Para obtener un ejemplo, vaya a [Navegar por el árbol **DOM** con un teclado][DevtoolsDomIndexNavigateDomTreeKeyboard].  

### <a name="copy-the-code-for-an-element-in-the-dom-tree"></a>Copiar el código de un elemento en el árbol DOM  

1.  Con el foco en un nodo en el árbol **DOM**, mantenga el mouse en el nodo y abra el menú contextual \(hacer clic con el botón secundario\).  
1.  Expanda la **opción** Copiar.  
1.  Elija **Copiar outerHTML**.  

**Problemas conocidos**  

*   **Copiar outerHTML** a menudo no selecciona el nodo actual, sino que selecciona el nodo primario.  Sin embargo, el contenido del elemento todavía debe estar en el outerHTML copiado.  

### <a name="modify-the-attributes-of-an-element-in-the-dom-tree"></a>Modificar los atributos de un elemento en el árbol DOM  

*   Con el foco en un nodo en el árbol **DOM,** seleccione `Enter` para hacerlo editable.  
*   Seleccione `Tab` para moverse entre los valores de atributo.  Cuando oiga "espacio" está dentro de una entrada de texto vacía y puede escribir un nuevo valor de atributo.  
*   Seleccione `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\) para aceptar el cambio y escuchar todo el contenido del elemento.  

**Problemas conocidos**  

*   Cuando escribes en la entrada de texto, no obtienes comentarios.  Si haces un error tipográfico y usas las teclas de flecha para explorar la entrada, tampoco recibes comentarios.  La forma más sencilla de comprobar el trabajo es aceptar el cambio y, a continuación, escuchar todo el elemento que se va a anunciar.  

### <a name="edit-the-html-of-an-element-in-the-dom-tree"></a>Editar el CÓDIGO HTML de un elemento en el árbol DOM  

*   Con el foco en un nodo en el árbol **DOM,** seleccione `Enter` para hacerlo editable.  
*   Seleccione `Tab` para moverse entre los valores de atributo.  Cuando oiga el nombre del elemento, por ejemplo, , está dentro de una entrada de texto y puede cambiar el `h2` tipo del elemento.  
*   Seleccione `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\) para aceptar el cambio.  

Por ejemplo, al escribir y seleccionar `h3` `Control` + `Enter` \(Windows, Linux\) o `Command` + `Enter` \(macOS\), `h3` cambian las etiquetas de inicio y finalización del elemento.  

## <a name="tabs-in-the-elements-tool"></a>Pestañas en la herramienta Elementos

La **herramienta Elementos** contiene pestañas adicionales para inspeccionar elementos como el CSS aplicado a un elemento o el lugar relevante en el árbol de accesibilidad.  

*   Con el foco en un nodo en el **árbol DOM,** seleccione hasta que oiga `Tab` que la pestaña **Estilos** está seleccionada.  
*   Use la `Right Arrow` para explorar otras pestañas disponibles.

El **árbol DOM** convierte los elementos con atributos en vínculos seleccionables, por lo que es posible que deba seleccionar más de una vez para llegar al panel `href` `Tab` **Estilos.**  

**Problemas conocidos**  

Las **pestañas Puntos de interrupción DOM** y **Propiedades** no son accesibles con teclado.  

### <a name="styles-pane"></a>Panel Estilos  

En el **panel Estilos,** busque controles para filtrar estilos, cambiar los estados de elemento \(como [:active][MDNActive] y [:focus][MDNFocus]\), alternar clases y agregar nuevas clases.  También hay una herramienta de inspección de estilos eficaz para explorar y modificar los estilos aplicados actualmente al elemento que está en el foco en el **árbol DOM**.  

El concepto clave para comprender acerca del panel **Estilos** es que solo muestra estilos para el nodo seleccionado actualmente en el **árbol DOM**.  Por ejemplo, supongamos que ha terminado de inspeccionar los estilos de un nodo y ahora desea ver los `<header>` estilos de un `<footer>` nodo.  Para ello, primero debe seleccionar el `<footer>` nodo en el árbol **DOM**.  Es posible que sea [](#inspect-an-element-on-the-page) más rápido usar el flujo de trabajo Inspeccionar para inspeccionar un nodo que se encuentra en las proximidades generales del nodo \(como un vínculo dentro del pie de página\), que centra el árbol DOM y, a continuación, use el teclado para navegar al nodo exacto en el que está `footer` interesado. ****  

#### <a name="navigate-the-styles-pane"></a>Navegar por el panel Estilos  

Dado que todas las herramientas de estilo se conectan de una forma u otra al panel **Estilos,** tiene sentido convertirse primero en un experto en esta herramienta.  

*   Con el foco en el **panel Estilos,** seleccione `Tab` para mover el foco dentro y explorar el contenido.  
*   Seleccione `Tab` hasta que el primer estilo se active.  Si usa un lector de pantalla, este primer estilo se anuncia como `element.style {}` .  
*   Seleccione `Down Arrow` esta opción para navegar por la lista de estilos por orden de especificidad.  Un lector de pantalla anuncia cada estilo empezando por el nombre del archivo CSS, el número de línea en el que aparece el estilo y el nombre del estilo.  Por ejemplo, `main.css:233 .card__img {}`.  
*   Seleccione `Enter` para inspeccionar un estilo con más detalle.  El foco comienza en una versión editable del nombre del estilo.  
*   Seleccione `Tab` para moverse entre las versiones editables de cada propiedad CSS y los valores correspondientes.  Al final de cada bloque de estilos hay un campo de texto editable en blanco que puede usar para agregar propiedades CSS adicionales.  
*   Puedes seguir seleccionando para desplazarte por la lista de estilos o seleccionar salir del modo y volver a navegar por `Tab` `Escape` las teclas de flecha.  

Para obtener accesos directos adicionales, vaya a [Referencia del teclado del panel Estilos][DevtoolsShortcutsStylesPaneKeyboard].  

**Problemas conocidos**  

*   Si usa el **campo Filtrar** texto editable, ya no podrá navegar por la lista de estilos.  

#### <a name="toggle-element-state"></a>Estado del elemento Toggle  

Para alternar el estado de un elemento, como `:active` o `:focus` :  

1.  Vaya al panel **Estilos y** seleccione hasta que el botón Alternar estado `Tab` **del** elemento tenga el foco.  
1.  Seleccione `Enter` para expandir la colección de estados de elemento.  Los estados del elemento se presentan como un grupo de casillas.  
1.  Seleccione `Tab` hasta que el primer estado, , tenga el `:active` foco.  
1.  Seleccione `Space` esta opción para habilitarla.  Si el elemento seleccionado actualmente en el árbol DOM tiene un `:active` estilo, ahora se aplica.  
1.  Espera `Tab` para explorar todos los estados disponibles.  

#### <a name="add-an-existing-class"></a>Agregar una clase existente  

Junto al botón **Alternar estado del** elemento, se encuentra el botón Clases **de** elementos.  Para mover el foco a él, seleccione `Tab` y, a continuación, seleccione `Enter` .  El foco se mueve a un campo de texto de edición con la **etiqueta Agregar nueva clase**.  

El **botón Clases de** elementos se usa principalmente para agregar clases existentes a un elemento.  Por ejemplo, si la hoja de estilos contenía una clase auxiliar denominada , puede seleccionar dentro del campo editar texto para mostrar una lista de sugerencias de clases y usar la para buscar `.clearfix` `.` la `Down Arrow` `.clearfix` sugerencia.  O escriba el nombre de la clase usted mismo y `Enter` seleccione aplicarlo.  

#### <a name="add-a-new-style-rule"></a>Agregar una nueva regla de estilo  

Junto al botón **Clases de elementos** se encuentra el botón Nueva regla **de** estilo.  Para mover el foco a él, seleccione `Tab` y, a continuación, seleccione `Enter` .  El foco se mueve a un campo de texto editable dentro del inspector de estilos.  El contenido de texto inicial del campo es el nombre de etiqueta del elemento seleccionado en el **árbol DOM**.  
Puede escribir cualquier nombre de clase que desee en este campo y, a continuación, seleccionar `Tab` para asignarle propiedades CSS.  

### <a name="computed-tab"></a>Pestaña calculada  

Con el foco en **la pestaña** Calculado, seleccione para mover el foco dentro y explorar `Tab` el contenido.  Dentro de **la pestaña** Calculado hay controles para explorar qué propiedades CSS se aplican realmente a un elemento por orden de especificidad.  

<!--todo: add Computed tab section when available  -->  

#### <a name="explore-all-computed-styles"></a>Explorar todos los estilos calculados  

Seleccione `Tab` hasta llegar a la colección de estilos calculados.  Se presentan como un [árbol de ARIA.][W3CWaiAriaTree]  Al expandir un cuadro de lista, se revelan los selectores CSS que aplican el estilo calculado.  Estos selectores se organizan por especificidad.  Un lector de pantalla anuncia el valor calculado, el selector CSS que coincide actualmente, el nombre de archivo de la hoja de estilos que contiene el selector y el número de línea del selector.  

**Problemas conocidos**  

*   Si usa el **campo de** texto Filtrar, ya no podrá inspeccionar estilos.  

### <a name="event-listeners-tab"></a>Pestaña Escuchas de eventos  

Para inspeccionar los agentes de escucha de eventos que se aplican a un elemento, seleccione la herramienta **Elementos** y, a continuación, seleccione la pestaña **Escuchas** de eventos (agrupada con la **pestaña** Estilos).

#### <a name="explore-event-listeners"></a>Explorar escuchas de eventos  

Los agentes de escucha de eventos se presentan como un [árbol de ARIA.][W3CWaiAriaTree]  Puede usar las teclas de flecha para navegar por ellas.  Un lector de pantalla anuncia el nombre del objeto DOM al que está adjunta la escucha de eventos, así como el nombre de archivo donde se define el agente de escucha de eventos y el número de línea.  

### <a name="accessibility-tab"></a>Pestaña Accesibilidad

Seleccione la `Tab` tecla para moverse dentro de la pestaña **Accesibilidad** de la **herramienta** Elementos.

La **pestaña Accesibilidad** está cerca de la **pestaña Estilos.** En la pestaña Accesibilidad, hay controles para explorar el árbol de accesibilidad, los atributos ARIA aplicados a un elemento y las propiedades de accesibilidad calculadas.  Para obtener más información, vaya [a Probar accesibilidad mediante la pestaña Accesibilidad][DevtoolsAccessibilityTab].

#### <a name="accessibility-tree"></a>Árbol de accesibilidad  

El **árbol de accesibilidad** se presenta como un árbol [ARIA][W3CWaiAriaTree] donde cada uno corresponde `treeitem` a un elemento del DOM.  El árbol anuncia el rol calculado para el nodo seleccionado.  Los elementos genéricos `div` como y `span` se anuncian como "GenericContainer" en el árbol.  Use las teclas de flecha para recorrer el árbol y explorar las relaciones primario-secundario.  

**Problemas conocidos**  

*   Es posible que el tipo **** de árbol [ARIA][W3CWaiAriaTree] usado por la pestaña Accesibilidad no se exponga correctamente en Microsoft Edge lectores de pantalla de macOS como VoiceOver.  [Suscríbete Chromium problema #868480][ChromiumIssues868480] para estar informado sobre el progreso en este problema.  
*   Cada una de las **** secciones **Atributos de ARIA** y Propiedades calculadas se marcan como un árbol de [ARIA,][W3CWaiAriaTree]pero cada una de ellas no tiene actualmente administración de focos y no funciona con el teclado.  

## <a name="lighthouse-tool"></a>Herramienta Faro

**Lighthouse** ejecuta una serie de pruebas en un sitio para comprobar si hay problemas comunes relacionados con el rendimiento, la accesibilidad, el SEO y varias otras categorías.  

### <a name="configure-and-generate-a-report"></a>Configurar y generar un informe

1.  Cuando la **herramienta Faro** se abre por primera vez en DevTools, el foco se coloca en el botón **Generar informe.**  De forma predeterminada, el formulario está configurado para ejecutar informes para todas las categorías mediante emulación móvil en una conexión 3G simulada.  
1.  Para cambiar la configuración del informe, úse el foco en la configuración de Faro o vuelva `Shift` + `Tab` al modo Examinar. ****  
1.  Cuando esté listo para ejecutar el informe, vuelva al botón **Generar informe** y seleccione `Enter` .  
1.  El foco se mueve a una ventana modal con **un botón Cancelar** que te permite salir de la auditoría.  Es posible que oiga una serie de earcons mientras la auditoría se ejecuta y actualiza la página varias veces.  

**Problemas conocidos**  

*   Las distintas secciones del formulario de configuración no están marcadas actualmente con un `fieldset` elemento.  Puede ser más fácil navegar por ellos en el modo Examinar para averiguar qué controles están asociados con cada sección.  
*   Cuando la auditoría haya terminado de ejecutarse, no hay ningún anuncio de región viva o de earcon.  Por lo general, la auditoría tarda unos 30 segundos, después de lo cual debería poder navegar hasta los resultados.  El uso del modo Examinar puede ser la forma más sencilla de llegar a los resultados.  

### <a name="navigate-the-lighthouse-report"></a>Navegar por el informe de Faro  

El informe de Faro se organiza en secciones que corresponden a cada una de las categorías de auditoría.  El informe se abre con una lista de puntuaciones para cada categoría.  Estas puntuaciones también son vínculos que puede usar para pasar a las secciones correspondientes.  Dentro de cada sección hay elementos `details` expandibles, que contienen información relacionada con auditorías pasadas o con errores.  De forma predeterminada, solo se muestran las auditorías con errores.  Cada sección termina con un elemento final `details` que contiene todas las auditorías pasadas.  

Para ejecutar una nueva auditoría, `Shift` + `Tab` úselo para salir del informe y seleccione el **botón Generar** informe.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  
[DevtoolsAccessibilityReference]: reference.md "Características de prueba de accesibilidad en DevTools | Microsoft Docs"  
[DevtoolsAccessibilityTab]: accessibility-tab.md "Probar la accesibilidad con la pestaña Accesibilidad | Microsoft Docs"  
[MicrosoftEdgeDevtoolsMain]: ../../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el Microsoft Edge de comandos DevTools | Microsoft Docs"  
[DevtoolsConsoleIndex]: ../console/index.md "Descripción general de la consola | Microsoft Docs"  
[DevtoolsCssIndex]: ../css/index.md "Introducción Con vista y cambio de CSS | Microsoft Docs"  
<!--[DevtoolsCssReferenceViewAppliedElement]: ../css/reference.md#view-only-the-css-that-is-actually-applied-to-an-element "CSS Reference - View only the CSS that is actually applied to an element | Microsoft Docs"  -->  
<!--[DevtoolsDomIndex]: ../dom/index.md "Get started with viewing and changing the DOM | Microsoft Docs"  -->  
[DevtoolsDomIndexViewDomNodes]: .. /dom/index.md#view-dom-nodes "Ver nodos DOM: introducción a la visualización y cambio del dom | Microsoft Docs"  
[DevtoolsDomIndexNavigateDomTreeKeyboard]: .. /dom/index.md#navigate-the-dom-tree-with-a-keyboard "Navigate the DOM Tree with a keyboard- Get started with viewing and changing the DOM | Microsoft Docs"  
[DevtoolsOpen]: .. /open/index.md "Abrir Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcuts]: .. /shortcuts/index.md "Microsoft Edge DevTools Keyboard Shortcuts | Microsoft Docs"  
[DevtoolsShortcutsStylesPaneKeyboard]: .. /shortcuts/index.md#styles-panel-keyboard-shortcuts "Styles panel keyboard shortcuts - Microsoft Edge DevTools Keyboard Shortcuts | Microsoft Docs"  

[ChromiumIssues868480]: https://bugs.chromium.org/p/chromium/issues/detail?id=868480 "Problema 868480: exponer árboles ARIA como tablas en la accesibilidad de Mac"  

[GithubEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Docs%20Feedback%5D "Nuevo problema: MicrosoftDocs/edge-developer | GitHub"  

[MDNActive]: https://developer.mozilla.org/docs/Web/CSS/:active ":active | MDN"  
[MDNFocus]: https://developer.mozilla.org/docs/Web/CSS/:focus ":focus | MDN"  

[MonorailChromiumIssues]: https://crbug.com "Problemas - chromium - Monorail"  

[W3CWaiAriaTablist]: https://www.w3.org/TR/wai-aria-1.1/#tablist "tablist (rol): aplicaciones de Internet enriquecciones accesibles (WAI-ARIA) 1.1 | W3C"  
[W3CWaiAriaTree]: https://www.w3.org/TR/wai-aria-1.1/#tree "árbol (rol): aplicaciones de Internet enriquecciones accesibles (WAI-ARIA) 1.1 | W3C"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/navigation) y es creado por [Rob Dodson][RobDodson] \(Contributor, Google WebFundamentals\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[RobDodson]: https://developers.google.com/web/resources/contributors#rob-dodson  

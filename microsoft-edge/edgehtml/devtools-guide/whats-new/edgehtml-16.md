---
description: Características agregadas a Microsoft Edge DevTools en Windows 10 Fall Creators Update (EdgeHTML 16)
title: DevTools en EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, edgehtml 16
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2d24b6851e843f491e470b18ccc18d559ed5533d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235982"
---
# DevTools en Windows 10 Fall Creators Update (EdgeHTML 16)

Con esta versión comenzamos un esfuerzo importante de refactorización de DevTools para mejorar la solidez y el rendimiento, además de agregar un conjunto de nuevas características que puede comenzar a usar hoy. 

Estas son las características de Microsoft Edge DevTools que se incluían en [Windows 10 Fall Creators Update](/windows/uwp/whats-new/windows-10-build-16299) ([EdgeHTML 16](https://aka.ms/devguide_edgehtml_16)).

## Escuchas de eventos antecesores 

El panel **eventos** ahora agrega la opción de ver las escuchas de eventos registradas en cualquier antecesor del elemento seleccionado actualmente (en el panel **elementos** ), además de las del propio elemento. Además, ahora puede agrupar la escucha de eventos en un *evento* o *elemento*. 

![Panel inspección de detector de eventos](../media/elements_ancestor_events.png)

## Puntos de interrupción de mutación DOM

Ahora puede establecer puntos de interrupción de mutación de DOM para que se interrumpan en el depurador cada vez que cambie un nodo de elemento seleccionado. Desde el panel **elementos** , RT: haga clic en cualquier elemento de la vista de árbol DOM y seleccione una o varias de las siguientes opciones:

 - Interrupción en el nodo quitada
 - Interrupción en subárbol modificada
 - Interrupción en el atributo modificado

Puede administrar los puntos de interrupción de mutación desde el panel de **puntos de interrupción Dom** en los paneles **elementos** o **depuración** .

![Panel de puntos de interrupción DOM](../media/elements_dom_breakpoints.png)

## Compatibilidad con reglas en CSS

Las reglas de CSS "en" (@) ahora se representan entre otras declaraciones de regla CSS en el panel **estilos** , incluidas `@keyframes` las reglas de animación (actualmente limitadas a solo lectura), `@supports` consultas de características y `@media` consultas.

![Inspección de CSS en las reglas del panel estilo de DevTools](../media/elements_at_rules.png)

## Panel fuentes CSS

`@font-face`Las reglas CSS ahora tienen su propio panel **fuentes** dedicadas en el que se muestra dónde se carga la fuente (*local* o de *red*) y el número de caracteres que la usan. Si se carga una fuente desde la red, DevTools mostrará la regla que la importó junto con su alias y tipo de fuente.

![Información de fuente CSS](../media/elements_fonts.png)

## Compatibilidad con los seudoelementos CSS

Ahora, el panel **estilos** agrupa los seudoelementos bajo sus propios títulos y ya no muestra su contenido como tachado.

**Antes:**
<br>
![El contenido generado estaba tachado anteriormente](../media/gc_before.png)

**Después:**
<br>
![El contenido generado ya no se muestra con tachado.](../media/gc_after.png)

## Mejoras en la consola

El panel de **consola** ha reversión de la experiencia del usuario para mejorar la facilidad de uso y ofrece una experiencia de IntelliSense más rápida y eficaz.

**Antes:** 
![ Consola anterior](../media/console_old.png)

**Después de:** 
![ Nueva consola](../media/console_new.png)

También agregamos estas mejoras:

 -  `Shift + Enter`Se usa para agregar una línea adicional a un comando antes de ejecutarla `Enter` . (Anteriormente había un cambio en el botón de alternancia de *modo multilínea o de línea única* ).

 - Se admiten las siguientes API nuevas:
    - método [ **Console. Table (**_Object_*_)_* ](../console/console-api.md#organizing-log-output)
    - [ **getEventListeners (**_objeto_*_)_* ](../console/command-line.md#event-listeners) comando
    - comando [ **Keys (**_objeto_*_)_* ](../console/command-line.md#object-inspection)
    - comando [ **valores (**_objeto_*_)_* ](../console/command-line.md#object-inspection)
    - Selector de [ **$x (**_expresión XPath_*_)_* ](../console/command-line.md#dom-selectors)

 - El parámetro de formato [**% c ()**](../console/console-api.md#logging-custom-messages) ahora es compatible

## Mejoras en la depuración

Además de un conjunto de características nuevas para depurar los [trabajos de servicio y la caché de PWA](#progressive-web-app-debugging), el depurador agregó estas características:

### Depuración consolidada para recursos compartidos

Incluso cuando se hace referencia varias veces a un recurso, como un archivo cargado desde CDN, en todo el código, DevTools le proporcionará una única instancia de depuración para ese archivo, donde podrá establecer puntos de interrupción comunes, que se alcanzarán sin importar dónde se hace referencia al archivo. (Anteriormente se consideró que cada referencia de script se asignaba a un conjunto separado de puntos de interrupción).

### Editar en vivo de JavaScript con *la edición activada-inactiva*

Ahora puede editar su JavaScript en vivo durante una sesión de depuración. Esta característica estaba disponible experimentalmente (detrás de una marca) en la versión [anterior](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (*Windows 10 Creators Update*) y ahora es una característica permanente. Simplemente seleccione cualquier archivo de script en el panel **depuración** , edite, haga clic en **Guardar** (o `Ctrl+S` ) para probar los cambios la próxima vez que se ejecute esa sección de código. 

![El depurador le permite modificar el script en vivo y comparar los cambios](../media/debugger_edit_buttons.png) 

Haga clic en el botón **comparar documento con el original** para ver las diferencias de los cambios que ha realizado.

![Vista de diferencias del código editado en el depurador](../media/debugger_edit_code.png) 

Ten en cuenta las siguientes limitaciones:

- La edición de script solo funciona en archivos *. js* externos (y no incrustados `<script>` en *. html*)
- Las modificaciones se guardan en memoria y se vacían al volver a cargar el documento, por lo que no podrá ejecutar modificaciones dentro de un `DOMContentLoaded` controlador, por ejemplo
- Por el momento, no hay ninguna forma (como una opción **Guardar como** ) para guardar las modificaciones en el disco desde DevTools

## Accesos directos

Ahora puedes iniciar DevTools en el panel de la última `Ctrl+Shift+I` versión () o directamente en la consola ( `Ctrl+Shift+J` ) como lo harías en otros navegadores principales.

## Depuración de aplicaciones web progresivas

Pruebe el soporte experimental para las aplicaciones web progresivas (PWAs) en Microsoft Edge y DevTools seleccionando la opción **Habilitar trabajos de servicio** de `about:flags` (y reiniciando Microsoft Edge). Si un sitio hace uso de **trabajadores del servicio** o de la API de **caché** , rellenará las entradas en el panel de **depuración** para cada origen, de forma similar a cómo funciona el almacenamiento web y la inspección de cookies.

Al hacer clic en una entrada de trabajador de servicio específica, se abrirá la **visión general**de los trabajadores del servicio, donde puede administrar el registro de trabajadores del servicio para el ámbito determinado y exigir una notificación de inserción de prueba. También puede **detener** / el**Inicio** de trabajos de servicio individuales e **inspeccionarlos** desde una ventana de depurador independiente:

![Panel de información general del trabajo del servicio](../media/debugger_sw_overview.png)

Tenga en cuenta lo siguiente sobre la depuración de los trabajos de servicios:

 - La depuración de un trabajador de servicio iniciará una nueva instancia de la DevTools independiente de las herramientas de la página porque los trabajos de servicio se pueden compartir entre varias pestañas. 
 - Los [elementos](../elements.md) y los paneles de [emulación](../emulation.md) no están presentes en el depurador de trabajo de servicios, dado que los trabajadores del servicio se ejecutan en segundo plano y no controlan directamente el front-end de la aplicación.
 - En este momento, el tráfico de red de un trabajador de servicio solo se notifica desde la instancia de depuración de DevTools para ese trabajo, y no desde la instancia central de la página.

Al hacer clic en una entrada de caché específica, se abrirá el administrador de **caché** , donde puede inspeccionar y, opcionalmente, eliminar entradas de caché (pares clave/valor de*solicitud* y *respuesta* ).

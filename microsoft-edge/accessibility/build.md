---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Recorra la forma en que las mejores prácticas y las aplicaciones de Internet enriquecidas accesibles (ARIA) pueden reunirse para crear un sitio web accesible.
title: Accesibilidad-compilación
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, Edge, desarrollo web, ARIA, desarrollador, UIA, automatización de la interfaz de usuario
ms.custom: seodec18
ms.openlocfilehash: 4412fef6bb78b5a393ccafd5a2cfa79aba223141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572946"
---
# Creación de sitios web accesibles
La web está rellenada con sitios web dinámicos y complejos, aplicaciones e interfaces de usuario generadas con una combinación de HTML, CSS y JavaScript.  Sin embargo, cuando se diseñan y se crean sin problemas de accesibilidad, los usuarios que dependen de las tecnologías de [asistencia](https://webaim.org/articles/motor/assistive) para explorar la web son difíciles de usar. La creación de sitios web que sean accesibles para personas con discapacidades requiere información semántica acerca de la interfaz de usuario. Esto permite que las tecnologías de asistencia, como los lectores de pantalla, transmitan la información necesaria para ayudar a las personas con una amplia variedad de funciones a usar el sitio Web.

Visita [HTML5Accessibility](https://html5accessibility.com) para obtener información sobre qué nuevas características de HTML5 son compatibles con Microsoft Edge.

## Cómo funciona la accesibilidad

Las tecnologías de asistencia agregan capacidades que los equipos no suelen tener. Por ejemplo, un usuario con deficiencias visuales puede usar su teclado en combinación con tecnología de asistencia, como un lector de pantalla, en lugar de usar directamente el explorador con el mouse y la pantalla. Para las aplicaciones de las plataformas de Microsoft y en la web, la tecnología de asistencia interactúa con la automatización de la [interfaz de usuario](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)de Microsoft, un modelo de objetos específico de la aplicación, como el modelo de objetos de documento (dom) en Microsoft Edge, o una combinación de estos.

Para los desarrolladores web, determinados elementos HTML se asignan a objetos de automatización de la interfaz de usuario, por lo que al seleccionarlos, el desarrollador puede usar las propiedades y los eventos de accesibilidad integrados en esos elementos. Al desarrollar su sitio web, normalmente solo debe preocuparse de asegurarse de que la API esté escrita correctamente en (o que se especifique el elemento apropiado), para que la aplicación sea accesible. Para obtener más información [, consulta Aria y la automatización de la interfaz de usuario en Microsoft Edge](./build/ARIA-and-UI-Automation.md) .  Para obtener información sobre las aplicaciones de la plataforma universal de Windows (UWP) accesibles, consulta el tema [accesibilidad](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) en el centro de desarrollo de Windows.

Muchos de los problemas de accesibilidad comunes con el contenido dinámico se pueden resolver mediante una buena práctica de programación y la documentación de [WCAG 2,0](https://go.microsoft.com/fwlink/p/?LinkID=24629) incluye muchas técnicas y procedimientos recomendados para ayudarle a crear aplicaciones web dinámicas más accesibles. Sin embargo, incluso cuando se codifica correctamente, el contenido dinámico no es necesariamente accesible. [Las aplicaciones de Internet enriquecidas accesibles (Aria)](#aria) ayudan a solucionar este problema.  

Para obtener más información sobre accesibilidad web, consulte la [Introducción a la accesibilidad web](https://www.w3.org/WAI/intro/accessibility.php) de la [iniciativa de accesibilidad para web](https://www.w3.org/WAI/) (WAI).

## ARIA
La especificación de [aplicaciones de Internet enriquecidas accesibles](https://www.w3.org/TR/wai-aria/) (Aria) por la [iniciativa de accesibilidad web](https://www.w3.org/WAI/) de W3C's define como una sintaxis para hacer que el contenido Web dinámico y las interfaces de usuario personalizadas sean accesibles para todas las personas. ARIA extiende el código HTML mediante atributos adicionales (roles, propiedades y Estados) que están diseñados para transmitir la semántica personalizada. Los exploradores usan estos atributos para pasar el estado y la función de los controles a la API de accesibilidad.

### Roles, propiedades y Estados
Los roles de ARIA se establecen en los elementos que usan el [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) atributo para proporcionar tecnologías de asistencia y información sobre las API de accesibilidad sobre el elemento. Por ejemplo, el `<li>` elemento siguiente está asignado `role="menuitem"` para indicar que es un elemento de un menú.

``` html
<li role="menuitem">Home</li>
```

Los Estados y las propiedades de ARIA son atributos prefijos de Aria que proporcionan información específica sobre un objeto para ayudar en la definición de la naturaleza de los roles. Las propiedades son atributos que son esenciales para la naturaleza de un objeto, como [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) y [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . Cambiar una propiedad afecta al significado del objeto. En el ejemplo siguiente, la propiedad `aria-haspopup="true"` se establece en un `<li>` elemento de menú para indicar que tiene un elemento emergente.

``` html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Los Estados no cambian la naturaleza del objeto, pero representan información asociada al objeto o a la interacción del usuario con el objeto, como [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) o [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Por ejemplo, el estado del `aria-checked="false"` ejemplo siguiente representa que la casilla no está marcada.

``` html
<div role="checkbox" aria-checked="false">Accept</div>
```

Vaya al [modelo de roles](https://www.w3.org/TR/wai-aria-1.1/#roles) de W3C para ver una lista completa de los roles, las propiedades y los Estados.

Para obtener más información sobre ARIA, vea ARIA en la sección de [recursos](#resources) .

## Recursos

### Conceptos básicos sobre accesibilidad
#### [El proyecto A11Y](http://a11yproject.com/)
El proyecto A11Y es un esfuerzo basado en la comunidad para facilitar la accesibilidad Web. Consulte [el sitio del proyecto A11Y](https://a11yproject.com/) para obtener información sobre los principios de accesibilidad básicos, su patrón accesible y la [biblioteca](https://a11yproject.com/patterns)widget, y sus [recursos](http://a11yproject.com/resources.html) sobre el software de accesibilidad, los blogs, los libros y las herramientas.

#### [Iniciativa de accesibilidad para web (WAI)](https://w3.org/WAI/)
La iniciativa de accesibilidad web de W3C's (WAI) es un esfuerzo para ayudarle a mejorar la accesibilidad de la Web. Su sitio proporciona una variedad de recursos para [empezar a usar la accesibilidad web](https://www.w3.org/WAI/gettingstarted/Overview.html), [diseñar la inclusión](https://www.w3.org/WAI/users/Overview.html), [tutoriales y presentaciones](https://www.w3.org/WAI/train.html), entre otras.

### Blogs de accesibilidad
#### [El grupo Paciello Group](https://www.paciellogroup.com/blog/)
El grupo Paciello Group ofrece asesoramiento y soluciones tecnológicas a organizaciones de todo el mundo para garantizar que sus clientes llegan a todas las audiencias de manera eficaz y eficaz, mientras cumplen los estándares gubernamentales e internacionales. Su blog cubre temas como procedimientos recomendados de accesibilidad para Web, herramientas de accesibilidad y tendencias de accesibilidad.

#### [Simple accesible](http://simplyaccessible.com/articles/)
Simplemente accesible es un equipo de especialistas en accesibilidad que proporciona aprendizaje de accesibilidad, consultoría y más para cambiar la percepción de la accesibilidad en la Web. En la sección de [artículos](http://simplyaccessible.com/articles/) se describen los procedimientos recomendados para accesibilidad web, diseño accesible y mucho más.

#### [Grupo de la Jesús SSB (SSB)](http://www.ssbbartgroup.com/blog/)
El grupo SSB Jesús es una empresa de accesibilidad digital que apoya a sus clientes en el desarrollo e implementación de productos y servicios accesibles. Su blog aborda temas como procedimientos recomendados de ARIA, tendencias de accesibilidad, seminarios por Web, etc.

### Ejemplos accesibles
#### [Ally. js: Tutoriales](http://allyjs.io/tutorials/)
Biblioteca de JavaScript para ayudar a las aplicaciones web modernas a tener dificultades de accesibilidad, simplificando la accesibilidad.

#### [Ejemplos de Heydonworks-ARIA](http://heydonworks.com/practical_aria_examples/)
Ejemplos prácticos de ARIA para mejorar la accesibilidad de la aplicación

#### [Ejemplos de OpenAjax](http://oaa-accessibility.org/)
El sitio web de OpenAjax Alliance es un excelente recurso para verificar las reglas de WAI-ARIA y proporciona una serie de ejemplos de implementaciones de WAI-ARIA.

#### [Modos](http://a11yproject.com/patterns.html)
[El proyecto A11Y](http://a11yproject.com/) ofrece una biblioteca de widgets y patrones accesibles, como menús, botones, información sobre herramientas, etc.

### Técnicas de accesibilidad & herramientas
#### [Accesibilidad: crear iconos de extensión accesibles para Microsoft Edge](../extensions/guides/accessibility.md)
Obtén orientación sobre cómo crear iconos de extensiones accesibles para Microsoft Edge.

#### [Nombre accesible y descripción: cálculo y asignaciones 1,1](https://www.w3.org/TR/accname-1.1/)
Este documento de asignación del W3C explica cómo los exploradores determinan el nombre y las descripciones de los objetos accesibles de los idiomas de contenido web y los exponen en las API de accesibilidad.

#### [Recursos de evaluación de accesibilidad](https://www.w3.org/WAI/eval/Overview.html)
Recursos de evaluación de accesibilidad es un recurso de varias páginas que describe los diferentes enfoques para evaluar los sitios web para accesibilidad.

#### [Pruebas de compatibilidad con tecnología de asistencia](http://www.powermapper.com/tests/)
Resultados de la prueba que muestran cómo se comportan diferentes tipos de contenido y estándares en las tecnologías de asistencia (AT) como los lectores de pantalla.

#### [Crear sitios web accesibles ahora es mucho más fácil](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)
Este mensaje de blog de herramientas y desarrollo web de .NET describe el [Comprobador de accesibilidad web](https://go.microsoft.com/fwlink/p/?linkid=841539)de extensiones de Visual Studio.

#### [Asignaciones básicas de API de accesibilidad 1,1](https://www.w3.org/TR/core-aam-1.1/)
Este documento de asignación del W3C explica cómo se expone la semántica de los lenguajes de contenido web a las API de accesibilidad.  

#### [Comprobaciones fáciles: una primera revisión de accesibilidad web](https://www.w3.org/WAI/eval/preliminary.html)
Una serie de comprobaciones rápidas por el WAI que le ayudan a evaluar la accesibilidad de una página web.

#### [Cómo cumplir con las WCAG 2,0](https://www.w3.org/WAI/WCAG20/quickref/)
Referencia rápida a los requisitos de accesibilidad de contenido web (WCAG) 2,0 (criterios de éxito) y técnicas.

#### [Asignaciones de API de accesibilidad de HTML 1,0](https://www.w3.org/TR/html-aam-1.0/)
Este documento de las asignaciones del consorcio W3C explica cómo los atributos y elementos HTML 5.1 se asignan a las API de accesibilidad de la plataforma.


#### [Sugerencias rápidas](http://a11yproject.com/#Quick-tips)
Una lista de sugerencias de desarrollo rápido para la web para accesibilidad mediante [el proyecto A11Y](http://a11yproject.com/).

#### [Exploración del sitio](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)
La herramienta de exploración del sitio del centro de desarrollo de Microsoft Edge busca bibliotecas no actualizadas, problemas de diseño y problemas de accesibilidad.

#### [Técnicas para WCAG 2,0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)
Técnicas del W3C que proporcionan instrucciones para los desarrolladores web en las [directrices de accesibilidad de contenido Web de reunión (WCAG) 2,0](https://w3.org/TR/WCAG20/) criterios de éxito.

#### [Sugerencias sobre el desarrollo para accesibilidad web](https://w3.org/WAI/gettingstarted/tips/developing.html)
Sugerencias de W3C sobre el desarrollo de contenido web que sea más accesible para personas con discapacidades.

#### [Prácticas de creación de WAI-ARIA 1,1](http://w3c.github.io/aria-practices/)
Un documento de W3C que proporciona a los lectores comprensión de cómo usar WAI-ARIA 1,1 y recomienda métodos para hacer que los widgets, la navegación y los comportamientos sean accesibles mediante los roles WAI-ARIA, los Estados y las propiedades.

#### [Directrices y técnicas WAI](https://w3.org/WAI/guid-tech.html)
Una serie de pautas y estándares de accesibilidad de web desarrollados por el WAI.  

#### [Lista herramientas de evaluación de accesibilidad web](https://www.w3.org/WAI/ER/tools/index.html)
Una lista de herramientas de evaluación de accesibilidad web para determinar si los sitios web cumplen con las directrices de accesibilidad.

#### [Perspectivas de accesibilidad web: Explore el impacto y las ventajas para todos los usuarios](https://w3.org/WAI/perspectives/)
Una serie de vídeos a corto plazo de W3C sobre el impacto de la accesibilidad y los beneficios para todos.

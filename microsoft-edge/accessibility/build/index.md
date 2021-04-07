---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Consulte cómo los procedimientos recomendados y las aplicaciones accesibles de Internet enriquecida (ARIA) se pueden unir para crear un sitio web accesible.
title: Crear | Accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, edge, desarrollo web, ARIA, desarrollador, UIA, Automatización de la interfaz de usuario
ms.custom: seodec18
ms.openlocfilehash: 3bc16450a3a64c06d290d1d3e112a9b2faecbe14
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480156"
---
# <a name="building-accessible-websites"></a>Creación de sitios web accesibles

La web está llena de sitios web dinámicos y complejos, aplicaciones e interfaces de usuario creadas con una combinación de HTML, CSS y JavaScript.  Sin embargo, cuando se diseñan y se construyen sin accesibilidad [](https://webaim.org/articles/motor/assistive) en mente, estos sitios web complejos son difíciles de usar por las personas que dependen de tecnologías de asistencia para navegar por la web. La creación de sitios web accesibles para personas con discapacidades requiere información semántica sobre la interfaz de usuario. Esto permite que las tecnologías de asistencia, como los lectores de pantalla, transmitan la información necesaria para ayudar a las personas con una variedad de capacidades a usar el sitio web.

Visite [HTML5Accessibility para](https://html5accessibility.com) obtener información sobre las nuevas características html5 que microsoft Edge admite de forma compatible.

## <a name="how-accessibility-works"></a>Cómo funciona la accesibilidad

Las tecnologías de asistencia agregan funcionalidades que los equipos no suelen tener. Por ejemplo, un usuario con discapacidad visual puede usar su teclado en combinación con tecnología de asistencia, como un lector de pantalla, en lugar de usar directamente el explorador con el mouse y la pantalla. Para las aplicaciones en plataformas de Microsoft y en la web, la tecnología de asistencia interactúa con [Automatización](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)de la interfaz de usuario de Microsoft, un modelo de objetos específico de la aplicación como el Modelo de objetos de documento (DOM) en Microsoft Edge o una combinación de estos.

Para los desarrolladores web, determinados elementos HTML se asignan a objetos de automatización de la interfaz de usuario, por lo que al seleccionar esos elementos HTML, el desarrollador puede usar las propiedades de accesibilidad y los eventos integrados en esos elementos. Durante el desarrollo del sitio web, normalmente solo debe preocuparse por asegurarse de que la API se escribe correctamente en (o que se especifica el elemento adecuado) para que la aplicación sea accesible. Consulta [ARIA y automatización de la interfaz de usuario en Microsoft Edge](./ARIA-and-UI-Automation.md) para obtener más información.  Para obtener información sobre las aplicaciones accesibles de la Plataforma universal de Windows (UWP), ve al tema [Accesibilidad](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) en el Centro de desarrollo de Windows.

Muchos problemas comunes de accesibilidad con contenido dinámico se pueden solucionar mediante una buena práctica de codificación, y la documentación de [WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) incluye muchas técnicas y procedimientos recomendados para ayudarle a crear aplicaciones web dinámicas más accesibles. Sin embargo, incluso cuando se codifica correctamente, el contenido dinámico no es necesariamente accesible. [Las aplicaciones de Internet enriquecciones accesibles (ARIA)](#aria) ayudan a solucionar este problema.  

Para obtener más información sobre la accesibilidad web, consulte [introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php) by the [Web Accessibility Initiative (WAI).](https://www.w3.org/WAI)

## <a name="aria"></a>ARIA

La [especificación Aplicaciones](https://www.w3.org/TR/wai-aria/) de Internet enriquecidas accesibles (ARIA) de la Iniciativa de accesibilidad [web](https://www.w3.org/WAI/) de W3C define como una sintaxis para hacer que el contenido web dinámico y las interfaces de usuario personalizadas puedan ser accesibles para todas las personas. ARIA amplía HTML mediante atributos adicionales (roles, propiedades y estados) diseñados para transmitir semántica personalizada. Estos atributos los usan los exploradores para pasar el estado y el rol de los controles a la API de accesibilidad.

### <a name="roles-properties-and-states"></a>Roles, propiedades y estados

Los roles de ARIA se establecen en elementos que usan el atributo para proporcionar tecnologías de asistencia e información sobre las API de [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) accesibilidad sobre el elemento. Por ejemplo, el elemento siguiente se asigna para indicar `<li>` que es un elemento de un `role="menuitem"` menú.

```html
<li role="menuitem">Home</li>
```

Los estados y propiedades de ARIA son atributos con prefijo aria que proporcionan información específica sobre un objeto para ayudar a formar la definición de la naturaleza de los roles. Las propiedades son atributos esenciales para la naturaleza de un objeto, como [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) y [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) . Cambiar una propiedad afecta al significado del objeto. En el ejemplo siguiente, la propiedad se establece en un elemento de menú para indicar `aria-haspopup="true"` que tiene un elemento `<li>` emergente.

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```

Los estados no cambian la naturaleza del objeto, sino que representan información asociada con el objeto o la interacción del usuario con el objeto, like [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) o [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) . Por ejemplo, el estado `aria-checked="false"` del ejemplo siguiente indica que la casilla no está activada.

```html
<div role="checkbox" aria-checked="false">Accept</div>
```

Vaya a [El modelo de roles](https://www.w3.org/TR/wai-aria-1.1/#roles) de W3C para ver una lista completa de roles, propiedades y estados.

Para obtener más información sobre ARIA, vaya a ARIA en la [sección](#resources) Recursos.

## <a name="assistive-technology-compatibility-testing"></a>Pruebas de compatibilidad de tecnología de asistencia  

Comprobar que el sitio web que está creando funciona con tecnologías de asistencia reales es la mejor manera de garantizar una buena experiencia para los usuarios con discapacidades.  Dado que muchas tecnologías de asistencia usan el teclado, probar la accesibilidad del teclado de su sitio web es un buen lugar para empezar.  [Las pruebas de][W3cPerspectiveVideosKeyboard] compatibilidad de teclado validan que los usuarios tienen acceso a todos los controles interactivos sin necesidad de un mouse.  Microsoft [Accessibility Insights para Web][AccessibilityinsightsWebOverview] es una extensión de explorador para Microsoft Edge y Chrome que le guía y revela varios problemas comunes.  

Una vez que estás seguro de que tu sitio web funciona bien con un teclado, pruébalo con otras tecnologías de asistencia, como lectores de pantalla.  Se destapan problemas en lo siguiente.

*   Html, ARIA y CSS.  
*   Nivel de compatibilidad de una tecnología de asistencia para una característica o técnica.  
    
Diferentes exploradores pueden asignar elementos a las API de accesibilidad de la plataforma de forma diferente que Microsoft Edge.  Al crear la interfaz, es importante tener en cuenta cada diferencia.  

WebAIM realiza encuestas con [][WebaimProjectsLowvisionsurvey2] lector de pantalla y usuarios de baja visión que le ayudan a decidir qué tecnologías de asistencia y exploradores desea probar. [][WebaimProjectsScreenreadersurvey8]  

### <a name="learning-how-to-test"></a>Aprender a probar  

Las tecnologías de asistencia son herramientas sofisticadas.  No supongas que puedes comenzar inmediatamente las pruebas con una tecnología de asistencia sin aprender primero cómo funciona.  Aprender a probar con un lector de pantalla tiene una curva de aprendizaje especialmente empinada.  Un usuario de lector de pantalla principiante puede asumir que se ha producido un error de lector de pantalla mientras el problema está relacionado con el uso incorrecto del lector de pantalla.  

Para obtener más información sobre cómo aprender a probar con tecnologías de asistencia, vaya a [Pruebas][WebaimArticlesScreenreaderTesting] con lectores de pantalla en WebAIM.  

### <a name="testing-locally"></a>Probar localmente  

La mayoría de los dispositivos incluyen tecnología de asistencia integrada en el sistema operativo.  Microsoft Windows incluye el lector [de pantalla del Narrador][MicrosoftSupport22798] de Windows y [la Lupa de Windows][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].  Las tecnologías de asistencia de terceros como [NVDA,][NvaccessAboutNvda] [FreedomscientificSoftwareJaws]y [ZoomText][FreedomscientificSoftwareZoomtext] están disponibles para su descarga.  Apple macOS incluye el lector [de pantalla VoiceOver.][AppleAccessibilityMacVision]  Además, iOS, Android y Linux admiten una variedad de tecnologías de asistencia.  

### <a name="testing-in-virtual-machines-and-emulators"></a>Pruebas en máquinas virtuales y emuladores  

En macOS, si quieres probar con una tecnología de asistencia solo disponible para Windows, como Windows Narrator o NVDA, crea una máquina virtual de Windows.  Las máquinas virtuales con Microsoft Edge \(EdgeHTML\) e IE están disponibles para VirtualBox y VMWare en la página de descarga [Máquinas virtuales][MicrosoftDeveloperEdgeVms].  

[Android Studio incluye][AndroidDeveloperSdkInstallingStudioHtml] un emulador que permite probar tecnologías de asistencia en [el Conjunto de accesibilidad de Android.][GooglePlayStoreAndroidAccessibilitySuite]  Sigue las instrucciones para [configurar un][AndroidDeveloperDevicesManagingAvdsHtml] dispositivo virtual e [iniciar][AndroidDeveloperDevicesEmulatorHtml]el emulador y, a continuación, instala [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite] desde la Tienda GooglePlay.  

> [!NOTE]
> El simulador de iOS no incluye actualmente VoiceOver.  

### <a name="cloud-based-testing-tools"></a>Herramientas de prueba basadas en la nube  

Si una tecnología de asistencia no está disponible en el sistema operativo o no es posible instalar una en una máquina virtual o emulador, las herramientas de prueba de tecnología de asistencia basadas en la nube son lo siguiente mejor.  

*   [Assistiv Labs (comercial)][AssistivlabsMain] le permite probar manualmente con tecnologías de asistencia a través de cualquier explorador web moderno.  Elige una tecnología de asistencia y un explorador y te conecta con una máquina virtual, un emulador o un dispositivo real con el que puedes interactuar.  

## <a name="resources"></a>Recursos

### <a name="accessibility-basics"></a>Conceptos básicos de accesibilidad

#### [<a name="the-a11y-project"></a>El proyecto A11Y](http://a11yproject.com/)

The A11Y Project is a community-driven effort to make web accessibility easier. Consulte el sitio del proyecto [A11Y](https://a11yproject.com/) para obtener información sobre los principios [](http://a11yproject.com/resources.html) básicos de accesibilidad, su patrón accesible y su biblioteca de [widgets,](https://a11yproject.com/patterns)y sus recursos en software de accesibilidad, blogs, libros y herramientas.

#### [<a name="web-accessibility-initiative-wai"></a>Iniciativa de accesibilidad web (WAI)](https://w3.org/WAI/)

The W3C Web Accessibility Initiative (WAI) is an effort to help improve the accessibility of the web. Su sitio proporciona una variedad de recursos para Introducción a la accesibilidad [web,](https://www.w3.org/WAI/gettingstarted/Overview.html)diseño para la [inclusión,](https://www.w3.org/WAI/users/Overview.html)tutoriales y [presentaciones,](https://www.w3.org/WAI/train.html)etc.

### <a name="accessibility-blogs"></a>Blogs de accesibilidad

#### [<a name="the-paciello-group"></a>Grupo Paciello](https://www.paciellogroup.com/blog/)

El Grupo Paciello proporciona soluciones de consultoría y tecnología a organizaciones de todo el mundo para garantizar que sus clientes lleguen a todas las audiencias de forma eficaz y eficaz, al tiempo que se reúnen con los estándares gubernamentales e internacionales. Su blog trata temas como procedimientos recomendados de accesibilidad web, herramientas de accesibilidad y tendencias de accesibilidad.

#### [<a name="simply-accessible"></a>Simplemente accesible](http://simplyaccessible.com/articles/)

Simply Accessible es un equipo de especialistas en accesibilidad que ofrece cursos de accesibilidad, consultoría y mucho más para cambiar la percepción de accesibilidad en la web. En [la sección](http://simplyaccessible.com/articles/) Artículos se deba a los procedimientos recomendados para la accesibilidad web, el diseño accesible y mucho más.

#### [<a name="ssb-bart-group-ssb"></a>Grupo de SSB BART (SSB)](http://www.ssbbartgroup.com/blog/)

SSB BART Group es una firma de accesibilidad digital que ayuda a sus clientes a desarrollar e implementar productos y servicios accesibles. Su blog aborda temas como procedimientos recomendados de ARIA, tendencias de accesibilidad, seminarios web y mucho más.

### <a name="accessible-examples"></a>Ejemplos accesibles

#### [<a name="allyjs---tutorials"></a>ally.js: tutoriales](http://allyjs.io/tutorials/)

Biblioteca de JavaScript para ayudar a las aplicaciones web modernas con problemas de accesibilidad al facilitar la accesibilidad.

#### [<a name="heydonworks---aria-examples"></a>Heydonworks: ejemplos de ARIA](http://heydonworks.com/practical_aria_examples/)

Ejemplos prácticos de ARIA para mejorar la accesibilidad de la aplicación

#### [<a name="openajax-examples"></a>Ejemplos de OpenAjax](http://oaa-accessibility.org/)

El sitio web de OpenAjax Alliance es un recurso excelente para comprobar las reglas de WAI-ARIA y proporciona varios ejemplos de implementaciones de WAI-ARIA.

#### [<a name="patterns"></a>Patrones](http://a11yproject.com/patterns.html)

[The A11Y Project](http://a11yproject.com/) offers a library of accessible widgets and patterns like menus, buttons, tooltips, and more.

### <a name="accessibility-techniques--tools"></a>Herramientas de & accesibilidad

#### [<a name="accessibility-creating-accessible-extension-icons-for-microsoft-edge"></a>Accesibilidad: creación de iconos de extensión accesibles para Microsoft Edge](/archive/microsoft-edge/legacy/developer/extensions/guides/accessibility)

Obtenga instrucciones sobre cómo crear iconos de extensiones accesibles para Microsoft Edge.

#### [<a name="accessible-name-and-description-computation-and-mappings-11"></a>Nombre y descripción accesibles: cálculo y asignaciones 1.1](https://www.w3.org/TR/accname-1.1/)

En este documento de asignación de W3C se explica cómo los exploradores determinan el nombre y las descripciones de objetos accesibles desde lenguajes de contenido web y los exponen en las API de accesibilidad.

#### [<a name="accessibility-evaluation-resources"></a>Recursos de evaluación de accesibilidad](https://www.w3.org/WAI/eval/Overview.html)

Recursos de evaluación de accesibilidad es un recurso de varias páginas del W3C que describe diferentes enfoques para evaluar sitios web para la accesibilidad.

#### [<a name="assistive-technology-compatibility-tests"></a>Pruebas de compatibilidad de tecnología de asistencia](http://www.powermapper.com/tests/)

Resultados de pruebas que muestran cómo se comportan los distintos tipos de contenido y estándares en tecnologías de asistencia (AT) como lectores de pantalla.

#### [<a name="building-accessible-websites-just-got-a-lot-easier"></a>Crear sitios web accesibles es mucho más fácil](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)

Esta entrada de blog .NET Web Development and Tools describe el Visual Studio [extensión Web Accessibility Checker](https://go.microsoft.com/fwlink/p/?linkid=841539).

#### [<a name="core-accessibility-api-mappings-11"></a>Asignaciones de API de accesibilidad principales 1.1](https://www.w3.org/TR/core-aam-1.1/)

Este documento de asignación W3C explica cómo la semántica de los lenguajes de contenido web se expone a las API de accesibilidad.  

#### [<a name="easy-checks--a-first-review-of-web-accessibility"></a>Comprobaciones fáciles: una primera revisión de la accesibilidad web](https://www.w3.org/WAI/eval/preliminary.html)

Una serie de comprobaciones rápidas de la WAI que le ayudan a garantizar la accesibilidad de una página web.

#### [<a name="how-to-meet-wcag-20"></a>Cómo conocer WCAG 2.0](https://www.w3.org/WAI/WCAG20/quickref/)

Una referencia rápida a los requisitos y técnicas de las Directrices de accesibilidad de contenido web (WCAG) 2.0 (criterios de éxito).

#### [<a name="html-accessibility-api-mappings-10"></a>Asignaciones de LA API de accesibilidad HTML 1.0](https://www.w3.org/TR/html-aam-1.0/)

En este documento de asignaciones W3C se explica cómo se asignan elementos y atributos HTML5.1 a las API de accesibilidad de la plataforma.

#### [<a name="quick-tips"></a>Sugerencias rápidas](http://a11yproject.com/#Quick-tips)

Una lista de sugerencias de desarrollo web rápido para la accesibilidad [de The A11Y Project](http://a11yproject.com/).

#### [<a name="site-scan"></a>Examen del sitio](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)

La herramienta Examen del sitio en el Centro de desarrollo de Microsoft Edge comprueba si hay bibliotecas des actualizadas, problemas de diseño y problemas de accesibilidad.

#### [<a name="techniques-for-wcag-20"></a>Técnicas para WCAG 2.0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)

Técnicas de W3C que proporcionan instrucciones para desarrolladores web sobre cómo cumplir los criterios de éxito de las Directrices de accesibilidad de contenido web [(WCAG) 2.0.](https://w3.org/TR/WCAG20/)

#### [<a name="tips-on-developing-for-web-accessibility"></a>Sugerencias sobre el desarrollo de la accesibilidad web](https://w3.org/WAI/gettingstarted/tips/developing.html)

Sugerencias de W3C sobre el desarrollo de contenido web más accesible para personas con discapacidades.

#### [<a name="wai-aria-authoring-practices-11"></a>Procedimientos de creación de WAI-ARIA 1.1](http://w3c.github.io/aria-practices/)

Un documento del W3C que proporciona a los lectores información sobre cómo usar WAI-ARIA 1.1 y recomienda métodos para que los widgets, la navegación y los comportamientos puedan ser accesibles mediante roles, estados y propiedades de WAI-ARIA.

#### [<a name="wai-guidelines-and-techniques"></a>Directrices y técnicas de WAI](https://w3.org/WAI/guid-tech.html)

Una serie de directrices y estándares de accesibilidad web desarrollados por el WAI.  

#### [<a name="web-accessibility-evaluation-tools-list"></a>Lista de herramientas de evaluación de accesibilidad web](https://www.w3.org/WAI/ER/tools/index.html)

Una lista de herramientas de evaluación de accesibilidad web para ayudar a determinar si los sitios web cumplen las directrices de accesibilidad.

#### [<a name="web-accessibility-perspectives-explore-the-impact-and-benefits-for-everyone"></a>Perspectivas de accesibilidad web: explorar el impacto y las ventajas para todos](https://w3.org/WAI/perspectives/)

Una serie de vídeos situacionales breves de W3C sobre el impacto de la accesibilidad y las ventajas para todos.

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Máquinas virtuales | Desarrollador de Microsoft Edge"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Guía completa del narrador | Soporte técnico de Microsoft"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Usa lupa para que las cosas en la pantalla sean más fáciles de ver | Soporte técnico de Microsoft"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Accessibility Insights for Web | Accessibility Insights"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Crear y administrar dispositivos virtuales | Desarrolladores de Android"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Ejecutar aplicaciones en el emulador de Android | Desarrolladores de Android"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Descargar Android Studio | Desarrolladores de Android"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Accesibilidad a la visión: Mac | manzana"  

[AssistivlabsMain]: https://assistivlabs.com "Laboratorios Assistiv"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "JAWS® | Freedom Scientific"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText | Freedom Scientific"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Android Accessibility Suite | GooglePlay Store"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "Acerca de nvda | NV Access"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Compatibilidad de teclado | W3C"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Encuesta de usuarios con visión baja \#2 resultados | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Encuesta de usuario del lector de pantalla \#8 resultados | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Pruebas con lectores de pantalla | WebAIM"  

---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Consulte cómo los procedimientos recomendados y las aplicaciones accesibles de Internet enriquecida (ARIA) se pueden unir para crear un sitio web accesible.
title: Crear | Accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, edge, desarrollo web, ARIA, desarrollador, UIA, Automatización de la interfaz de usuario
ms.custom: seodec18
ms.openlocfilehash: 5754e6198888d54412dd7d5616c812400fee8a0180685ceda8f1f4e609541b39
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11800163"
---
# <a name="building-accessible-websites"></a>Creación de sitios web accesibles  

La web está llena de sitios web dinámicos y complejos, aplicaciones e interfaces de usuario creadas con una combinación de HTML, CSS y JavaScript.  Sin embargo, cuando se diseñan y se construyen sin accesibilidad [](https://webaim.org/articles/motor/assistive) en mente, estos sitios web complejos son difíciles de usar por las personas que dependen de tecnologías de asistencia para navegar por la web.  La creación de sitios web accesibles para personas con discapacidades requiere información semántica sobre la interfaz de usuario.  Esto permite que las tecnologías de asistencia, como los lectores de pantalla, transmitan la información necesaria para ayudar a las personas con una variedad de capacidades a usar el sitio web.  

Visite [HTML5Accessibility para](https://html5accessibility.com) obtener información sobre las nuevas características html5 que son compatibles de forma Microsoft Edge.  

## <a name="how-accessibility-works"></a>Cómo funciona la accesibilidad  

Las tecnologías de asistencia agregan funcionalidades que los equipos no suelen tener.  Por ejemplo, un usuario con discapacidad visual puede usar su teclado en combinación con tecnología de asistencia, como un lector de pantalla, en lugar de usar directamente el explorador con el mouse y la pantalla.  Para las aplicaciones en plataformas de Microsoft y en la web, la tecnología de asistencia interactúa con [La](/windows/win32/winauto/uiauto-specandcommunitypromise)automatización de la interfaz de usuario de Microsoft, un modelo de objetos específico de la aplicación, como el modelo de objetos de documento \(DOM\) en Microsoft Edge, o una combinación de estos.  

Para los desarrolladores web, determinados elementos HTML se asignan a objetos de automatización de la interfaz de usuario, por lo que al seleccionar esos elementos HTML, el desarrollador puede usar las propiedades de accesibilidad y los eventos integrados en esos elementos.  Durante el desarrollo de su sitio web, normalmente solo debe preocuparse de asegurarse de que la API se escribe correctamente en \(o que se especifica el elemento adecuado\), para que la aplicación sea accesible.  Consulte [ARIA y automatización de la interfaz de usuario en Microsoft Edge](./aria-and-ui-automation.md) para obtener más información.  Para obtener información sobre las aplicaciones accesibles de la Plataforma Windows universal \(UWP\), ve al tema [Accesibilidad](/windows/uwp/design/accessibility/accessibility) en el Windows Centro de desarrollo.  

Muchos problemas comunes de accesibilidad con contenido dinámico se pueden solucionar mediante una buena práctica de codificación, y la documentación de [WCAG 2.0](https://www.w3.org/TR/WCAG20) incluye muchas técnicas y procedimientos recomendados para ayudarle a crear aplicaciones web dinámicas más accesibles.  Sin embargo, incluso cuando se codifica correctamente, el contenido dinámico no es necesariamente accesible.  [Las aplicaciones de Internet enriquecciones accesibles (ARIA)](#aria) ayudan a solucionar este problema.  

Para obtener más información sobre la accesibilidad web, consulte [introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php) by the [Web Accessibility Initiative (WAI).](https://www.w3.org/WAI)  

## <a name="aria"></a>ARIA  

La especificación Aplicaciones de Internet enriquecidas [accesibles (ARIA)](https://www.w3.org/TR/wai-aria) de la Iniciativa de accesibilidad [web](https://www.w3.org/WAI) de W3C define como una sintaxis para hacer que el contenido web dinámico y las interfaces de usuario personalizadas puedan ser accesibles para todas las personas.  ARIA amplía HTML mediante atributos adicionales \(roles, propiedades y estados\) diseñados para transmitir semántica personalizada.  Estos atributos los usan los exploradores para pasar el estado y el rol de los controles a la API de accesibilidad.  

### <a name="roles-properties-and-states"></a>Roles, propiedades y estados  

Los roles de ARIA se establecen en elementos que usan el [atributo role](https://developer.mozilla.org/docs/Web/HTML/Reference) para proporcionar información sobre las API de accesibilidad y tecnologías de asistencia sobre el elemento.  Por ejemplo, el elemento siguiente se asigna para indicar `<li>` que es un elemento de un `role="menuitem"` menú.  

```html
<li role="menuitem">Home</li>
```  

Los estados y propiedades de ARIA son atributos con prefijo aria que proporcionan información específica sobre un objeto para ayudar a formar la definición de la naturaleza de los roles.  Las propiedades son atributos que son esenciales para la naturaleza de un objeto, como [aria-readonly](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y [aria-haspopup](https://developer.mozilla.org/docs/Web/Accessibility/ARIA).  Cambiar una propiedad afecta al significado del objeto.  En el ejemplo siguiente, la propiedad se establece en un elemento de menú para indicar `aria-haspopup="true"` que tiene un elemento `<li>` emergente.  

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```  

Los estados no cambian la naturaleza del objeto, sino que representan información asociada con el objeto o la interacción del usuario con el objeto, como [aria-hidden](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) o [aria-checked](https://developer.mozilla.org/docs/Web/Accessibility/ARIA).  Por ejemplo, el estado `aria-checked="false"` del ejemplo siguiente indica que la casilla no está activada.  

```html
<div role="checkbox" aria-checked="false">Accept</div>
```  

Vaya a [El modelo de roles](https://www.w3.org/TR/wai-aria-1.1#roles) de W3C para ver una lista completa de roles, propiedades y estados.  

Para obtener más información sobre ARIA, vaya a ARIA en la [sección](#resources) Recursos.  

## <a name="assistive-technology-compatibility-testing"></a>Pruebas de compatibilidad de tecnología de asistencia  

Comprobar que el sitio web que está creando funciona con tecnologías de asistencia reales es la mejor manera de garantizar una buena experiencia para los usuarios con discapacidades.  Dado que muchas tecnologías de asistencia usan el teclado, probar la accesibilidad del teclado de su sitio web es un buen lugar para empezar.  [Las pruebas de][W3cPerspectiveVideosKeyboard] compatibilidad de teclado validan que los usuarios tienen acceso a todos los controles interactivos sin necesidad de un mouse.  Microsoft [Accessibility Ideas web][AccessibilityinsightsWebOverview] es una extensión de explorador para Microsoft Edge y Chrome que le guía y revela varios problemas comunes.  

Una vez que estás seguro de que tu sitio web funciona bien con un teclado, pruébalo con otras tecnologías de asistencia, como lectores de pantalla.  Se destapan problemas en lo siguiente.  

*   Html, ARIA y CSS.  
*   Nivel de compatibilidad de una tecnología de asistencia para una característica o técnica.  
    
Diferentes exploradores pueden asignar elementos a las API de accesibilidad de la plataforma de forma diferente que Microsoft Edge.  Al crear la interfaz, es importante tener en cuenta cada diferencia.  

WebAIM realiza encuestas con [][WebaimProjectsLowvisionsurvey2] lector de pantalla y usuarios de baja visión que le ayudan a decidir qué tecnologías de asistencia y exploradores desea probar. [][WebaimProjectsScreenreadersurvey8]  

### <a name="learning-how-to-test"></a>Learning Cómo probar  

Las tecnologías de asistencia son herramientas sofisticadas.  No supongas que puedes comenzar inmediatamente las pruebas con una tecnología de asistencia sin aprender primero cómo funciona.  Learning probar con un lector de pantalla tiene una curva de aprendizaje especialmente empinada.  Un usuario de lector de pantalla principiante puede asumir que se ha producido un error de lector de pantalla mientras el problema está relacionado con el uso incorrecto del lector de pantalla.  

Para obtener más información sobre cómo aprender a probar con tecnologías de asistencia, vaya a [Pruebas][WebaimArticlesScreenreaderTesting] con lectores de pantalla en WebAIM.  

### <a name="testing-locally"></a>Probar localmente  

La mayoría de los dispositivos incluyen tecnología de asistencia integrada en el sistema operativo.  Microsoft Windows incluye el lector de pantalla [Windows narrador][MicrosoftSupport22798] y [Windows lupa][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].  Las tecnologías de asistencia de terceros como [NVDA,][NvaccessAboutNvda] [FreedomscientificSoftwareJaws]y [ZoomText][FreedomscientificSoftwareZoomtext] están disponibles para su descarga.  Apple macOS incluye el lector [de pantalla VoiceOver.][AppleAccessibilityMacVision]  Además, iOS, Android y Linux admiten una variedad de tecnologías de asistencia.  

### <a name="testing-in-virtual-machines-and-emulators"></a>Pruebas en máquinas virtuales y emuladores  

En macOS, si quieres probar con una tecnología de asistencia solo disponible para Windows, como Windows Narrador o NVDA, crea una Windows virtual.  Las máquinas virtuales con Microsoft Edge \(EdgeHTML\) e IE están disponibles para VirtualBox y VMWare en la página de descarga [Máquinas virtuales][MicrosoftDeveloperEdgeVms].  

[Android Studio incluye][AndroidDeveloperSdkInstallingStudioHtml] un emulador que permite probar tecnologías de asistencia en [el Conjunto de accesibilidad de Android.][GooglePlayStoreAndroidAccessibilitySuite]  Sigue las instrucciones para [configurar un][AndroidDeveloperDevicesManagingAvdsHtml] dispositivo virtual e [iniciar][AndroidDeveloperDevicesEmulatorHtml]el emulador y, a continuación, instala [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite] desde la Tienda GooglePlay.  

> [!NOTE]
> El simulador de iOS no incluye actualmente VoiceOver.  

### <a name="cloud-based-testing-tools"></a>Herramientas de prueba basadas en la nube  

Si una tecnología de asistencia no está disponible en el sistema operativo o no es posible instalar una en una máquina virtual o emulador, las herramientas de prueba de tecnología de asistencia basadas en la nube son lo siguiente mejor.  

*   [Assistiv Labs (comercial)][AssistivlabsMain] le permite probar manualmente con tecnologías de asistencia a través de cualquier explorador web moderno.  Elige una tecnología de asistencia y un explorador y te conecta con una máquina virtual, un emulador o un dispositivo real con el que puedes interactuar.  

## <a name="resources"></a>Recursos  

### <a name="accessibility-basics"></a>Conceptos básicos de accesibilidad  

#### <a name="the-a11y-project"></a>El archivo A11Y Project  

[El A11Y Project](http://a11yproject.com) es un esfuerzo basado en la comunidad para facilitar la accesibilidad web.  Consulte El sitio [de Project A11Y](https://a11yproject.com) para obtener información sobre los principios básicos [](http://a11yproject.com/resources.html) de accesibilidad, su patrón accesible y su biblioteca de [widgets,](https://a11yproject.com/patterns)y sus recursos en software de accesibilidad, blogs, libros y herramientas.  

#### <a name="web-accessibility-initiative-wai"></a>Iniciativa de accesibilidad web (WAI)  

The W3C [Web Accessibility Initiative (WAI)](https://w3.org/WAI) is an effort to help improve the accessibility of the web.  Su sitio proporciona una variedad de recursos para Introducción a la accesibilidad [web,](https://www.w3.org/WAI/gettingstarted/Overview.html)diseño para la [inclusión,](https://www.w3.org/WAI/users/Overview.html)tutoriales y [presentaciones,](https://www.w3.org/WAI/train.html)etc.  

### <a name="accessibility-blogs"></a>Blogs de accesibilidad  

#### <a name="tpgi-llc"></a>TPGi, LLC  

[TPGi, LLC](https://www.tpgi.com/blog) proporciona soluciones de consultoría y tecnología a organizaciones de todo el mundo para garantizar que sus clientes lleguen a todas las audiencias de forma eficaz y eficiente, al tiempo que se reúnen con los estándares gubernamentales e internacionales.  Su blog trata temas como procedimientos recomendados de accesibilidad web, herramientas de accesibilidad y tendencias de accesibilidad.  

#### <a name="simply-accessible"></a>Simplemente accesible  

[Simply Accessible](http://simplyaccessible.com/articles) es un equipo de especialistas en accesibilidad que ofrece cursos de accesibilidad, consultoría y mucho más para cambiar la percepción de accesibilidad en la web.  En [la sección](http://simplyaccessible.com/articles) Artículos se deba a los procedimientos recomendados para la accesibilidad web, el diseño accesible y mucho más.  

#### <a name="level-access"></a>Acceso de nivel  

[Level Access](https://www.levelaccess.com/blog) es una firma de accesibilidad digital que da soporte a sus clientes en el desarrollo e implementación de productos y servicios accesibles.  Su blog aborda temas como procedimientos recomendados de ARIA, tendencias de accesibilidad, seminarios web y mucho más.  

### <a name="accessible-examples"></a>Ejemplos accesibles  

#### <a name="allyjs---tutorials"></a>ally.js: tutoriales  

Biblioteca de JavaScript para ayudar a las aplicaciones web modernas con problemas de accesibilidad al facilitar la accesibilidad.  Para obtener más información, vaya [ aally.js - Tutoriales](http://allyjs.io/tutorials).  

#### <a name="openajax-examples"></a>Ejemplos de OpenAjax  

El [sitio web de OpenAjax Alliance](http://oaa-accessibility.org) es un recurso excelente para comprobar las reglas de WAI-ARIA y proporciona varios ejemplos de implementaciones de WAI-ARIA.  

#### <a name="patterns"></a>Patrones  

[El A11Y Project](http://a11yproject.com) una biblioteca de widgets y patrones accesibles, como menús, botones, información sobre herramientas y mucho más.  Para obtener más información, vaya a [Patrones](http://a11yproject.com/patterns.html).  

### <a name="accessibility-techniques--tools"></a>Herramientas de & accesibilidad

#### <a name="accessibility--creating-accessible-extension-icons-for-microsoft-edge"></a>Accesibilidad: crear iconos de extensión accesibles para Microsoft Edge  

Obtenga instrucciones sobre cómo crear iconos de extensiones accesibles para Microsoft Edge.  Para obtener más información, vaya a [Accesibilidad: Crear iconos de extensión accesibles para Microsoft Edge](/archive/microsoft-edge/legacy/developer/extensions/guides/accessibility).  

#### <a name="accessible-name-and-description-computation-and-mappings-11"></a>Nombre y descripción accesibles: cálculo y asignaciones 1.1  

En este documento de asignación de W3C se explica cómo los exploradores determinan el nombre y las descripciones de objetos accesibles desde lenguajes de contenido web y los exponen en las API de accesibilidad.  Para obtener más información, vaya [a Accessible Name and Description: Computation and Mappings 1.1](https://www.w3.org/TR/accname-1.1).  

#### <a name="accessibility-evaluation-resources"></a>Recursos de evaluación de accesibilidad  

Recursos de evaluación de accesibilidad es un recurso de varias páginas del W3C que describe diferentes enfoques para evaluar sitios web para la accesibilidad.  Para obtener más información, vaya [a Recursos de evaluación de accesibilidad](https://www.w3.org/WAI/eval/Overview.html).  

#### <a name="assistive-technology-compatibility-tests"></a>Pruebas de compatibilidad de tecnología de asistencia  

Resultados de pruebas que muestran cómo se comportan los distintos tipos de contenido y estándares en tecnologías de asistencia \(AT\) como lectores de pantalla.  Para obtener más información, vaya [a Pruebas de compatibilidad de tecnología de asistencia](http://www.powermapper.com/tests).  

#### <a name="building-accessible-websites-just-got-a-lot-easier"></a>Crear sitios web accesibles es mucho más fácil  

Esta entrada de blog .NET Web Development and Tools describe el Visual Studio [extensión Web Accessibility Checker](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.WebAccessibilityChecker).  Para obtener más información, vaya a Creación de sitios web accesibles [que son mucho más fáciles.](https://devblogs.microsoft.com/aspnet/building-accessible-websites-just-got-a-lot-easier)  

#### <a name="core-accessibility-api-mappings-11"></a>Asignaciones de API de accesibilidad principales 1.1  

Este documento de asignación W3C explica cómo la semántica de los lenguajes de contenido web se expone a las API de accesibilidad.  Para obtener más información, vaya a [Core Accessibility API Mappings 1.1](https://www.w3.org/TR/core-aam-1.1).  

#### <a name="easy-checks--a-first-review-of-web-accessibility"></a>Comprobaciones fáciles: una primera revisión de la accesibilidad web  

Una serie de comprobaciones rápidas de la WAI que le ayudan a garantizar la accesibilidad de una página web.  Para obtener más información, vaya [a Comprobaciones fáciles: una primera revisión de la accesibilidad web.](https://www.w3.org/WAI/eval/preliminary.html)  

#### <a name="how-to-meet-wcag-20"></a>Cómo conocer WCAG 2.0  

Una referencia rápida a las directrices de accesibilidad de contenido web \(WCAG\) 2.0 requisitos \(criterios de éxito\) y técnicas.  Para obtener más información, vaya [a How to Meet WCAG 2.0](https://www.w3.org/WAI/WCAG20/quickref).  

#### <a name="html-accessibility-api-mappings-10"></a>Asignaciones de LA API de accesibilidad HTML 1.0  

En este documento de asignaciones W3C se explica cómo se asignan elementos y atributos HTML5.1 a las API de accesibilidad de la plataforma.  Para obtener más información, vaya a [Asignaciones de la API de accesibilidad HTML 1.0](https://www.w3.org/TR/html-aam-1.0).  

#### <a name="quick-tips"></a>Quick Sugerencias

Una lista de sugerencias de desarrollo web rápido para la accesibilidad [de The A11Y Project](http://a11yproject.com).  Para obtener más información, vaya [a Quick Sugerencias](http://a11yproject.com#Quick-tips).  

#### <a name="site-scan"></a>Examen del sitio  

La herramienta Examen del sitio en Microsoft Edge Dev del centro de búsqueda busca bibliotecas des actualizadas, problemas de diseño y problemas de accesibilidad.  Para obtener más información, vaya a [Examen del sitio](https://developer.microsoft.com/microsoft-edge/tools).  

#### <a name="techniques-for-wcag-20"></a>Técnicas para WCAG 2.0  

Técnicas de W3C que proporcionan instrucciones para desarrolladores web sobre cómo cumplir los criterios de éxito de las Directrices de accesibilidad de contenido web [(WCAG) 2.0.](https://w3.org/TR/WCAG20)  Para obtener más información, vaya [a Técnicas para WCAG 2.0](https://www.w3.org/TR/WCAG20-TECHS/Overview.html).  

#### <a name="tips-on-developing-for-web-accessibility"></a>Sugerencias desarrollo de accesibilidad web  

Sugerencias de W3C sobre el desarrollo de contenido web que sea más accesible para las personas con discapacidades.  Para obtener más información, vaya [a Sugerencias en Desarrollo de accesibilidad web](https://w3.org/WAI/gettingstarted/tips/developing.html).  

#### <a name="wai-aria-authoring-practices-11"></a>Procedimientos de creación de WAI-ARIA 1.1  

Un documento del W3C que proporciona a los lectores información sobre cómo usar WAI-ARIA 1.1 y recomienda métodos para que los widgets, la navegación y los comportamientos puedan ser accesibles mediante roles, estados y propiedades de WAI-ARIA.  Para obtener más información, vaya [a WAI-ARIA Authoring Practices 1.1](http://w3c.github.io/aria-practices).  

#### <a name="wai-guidelines-and-techniques"></a>Directrices y técnicas de WAI  

Una serie de directrices y estándares de accesibilidad web desarrollados por el WAI.  Para obtener más información, vaya a [Directrices y técnicas de WAI](https://w3.org/WAI/guid-tech.html).  

#### <a name="web-accessibility-evaluation-tools-list"></a>Lista de herramientas de evaluación de accesibilidad web  

Una lista de herramientas de evaluación de accesibilidad web para ayudar a determinar si los sitios web cumplen las directrices de accesibilidad.  Para obtener más información, vaya a [Lista de herramientas de evaluación de accesibilidad web](https://www.w3.org/WAI/ER/tools/index.html).  

#### <a name="web-accessibility-perspectives-explore-the-impact-and-benefits-for-everyone"></a>Perspectivas de accesibilidad web: explorar el impacto y las ventajas para todos  

Una serie de vídeos situacionales breves de W3C sobre el impacto de la accesibilidad y las ventajas para todos.  Para obtener más información, vaya a [Perspectivas de accesibilidad web: Explorar el impacto y las ventajas para todos.](https://w3.org/WAI/perspectives)  

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Máquinas virtuales | Microsoft Edge Programador"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Guía completa del narrador | Soporte técnico de Microsoft"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Usa lupa para que las cosas en la pantalla sean más fáciles de ver | Soporte técnico de Microsoft"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Accesibilidad Ideas web | Accesibilidad Ideas"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Crear y administrar dispositivos virtuales | Desarrolladores de Android"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Ejecutar aplicaciones en el Emulator | Desarrolladores de Android"  
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

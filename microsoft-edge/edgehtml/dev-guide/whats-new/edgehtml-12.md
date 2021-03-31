---
description: Esta página proporciona una descripción general de las novedades de EdgeHTML 12.
title: Nuevas características y API de EdgeHTML 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a96d75ff7decf2c6efdfee3be94736707fea5a6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236247"
---
# Novedades de EdgeHTML 12  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge presenta EdgeHTML, un nuevo motor "vivo" diseñado con interoperabilidad en su centro, para asegurar que siempre obtendrás la última y mejor plataforma web de Windows.  Microsoft Edge presenta un salto limpio desde el pasado, gratis desde el código heredado necesario para admitir controles ActiveX, objetos de ayuda del explorador \(BHO \) y otras prácticas de desarrollo web de bygone.  Además, Microsoft Edge ofrece compatibilidad nativa con PDF.  A partir de IE11, los modos de documento heredado han quedado obsoletos y, con Microsoft Edge, la infraestructura de explorador para admitirlos no existe.  Consulta el [IEBlog](/archive/blogs/ie/living-on-the-edge-our-next-step-in-interoperability) para obtener más información.  

Estos son los cambios que se han enviado con EdgeHTML 12 en la versión inicial de [Windows 10](https://blogs.windows.com/windowsexperience/2015/07/28/windows-10-free-upgrade-available-in-190-countries) \(07/2015, compilación 10240 \).  Para obtener información general sobre los cambios en el explorador general de Microsoft Edge, vea [un salto del pasado: el nacimiento del nuevo motor de representación Web de Microsoft](https://blogs.windows.com/msedgedev/2015/02/26) y [un salto del pasado, parte 2: diga adiós a ActiveX, VBScript, attachEvent...](https://blogs.windows.com/msedgedev/2015/05/06)  

Este es el vínculo permanente de la siguiente lista de cambios:  [https://aka.ms/devguide_edgehtml_12](./edgehtml-12.md) .  

## Nuevas características  

### Directiva de seguridad de contenido 1,0  

Microsoft Edge ahora implementa la Directiva de seguridad de contenido \(CSP \) 1,0.  El estándar de seguridad de CSP permite a los desarrolladores de web controlar los recursos \(script, CSS, complementos, imágenes, etc. \) que una página determinada puede recuperar o ejecutar con el fin de evitar ataques de scripting entre sitios \(XSS \), Clickjacking y otros ataques de inserción de código que buscan ejecutar contenido malintencionado en el contexto de una página web de confianza.  Consulte la [Directiva de seguridad de contenido](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Content_Security_Policy) para obtener más información sobre CSP en Microsoft Edge.  

### Efectos de filtro  

Microsoft Edge ofrece una manera sencilla de agregar efectos visuales a los elementos.  Con la `filter` propiedad puede Agregar desenfoques, ajustar el brillo, agregar una sombra, cambiar la opacidad y mucho más a un elemento.  Con puramente CSS, puede aplicar varios efectos de filtro a un elemento y animar los filtros.  Para obtener más información, consulte [filtro de efectos](https://developer.mozilla.org/docs/Web/CSS/filter).  

### JavaScript  

La compatibilidad con JavaScript varía ligeramente entre la versión final de Internet Explorer \(IE11 \) y Microsoft Edge.  Las nuevas características de Edge incluyen:  

:::row:::
   :::column span="1":::
      **Extractos**  
   :::column-end:::
   :::column span="2":::
      [clase](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/class) \(experimental \), [para... de](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/for...of)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Objeto**  
   :::column-end:::
   :::column span="2":::
      [Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise), [proxy](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Proxy), [símbolo](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Symbol), [WeakSet](/scripting/javascript/reference/weakset-object-javascript)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Funciones**  
   :::column-end:::
   :::column span="2":::
      [Acosh](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/acosh), [codePointAt](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/codepointat), [fromCodePoint](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/fromcodepoint), [hypot](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/hypot), [imul](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Math/imul), [isInteger](/scripting/javascript/reference/number-isinteger-function-number-javascript), [isNaN](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number/isnan), [raw](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/raw)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Métodos**  
   :::column-end:::
   :::column span="2":::
      [incluye](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/includes), [Keys](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) \(matriz \), [repite](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) \(cadena \), [valores](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/values) \(matriz \)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Otras características**  
   :::column-end:::
   :::column span="2":::
      [Funciones](https://developer.mozilla.org/docs/Learn/JavaScript/Building_blocks/Functions) \(experimental \), [generadores](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators),  [iteradores](https://developer.mozilla.org/docs/Web/JavaScript/Guide/Iterators_and_generators), [ `y` indicador de expresiones regulares](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) \(experimental \), [cadenas de plantilla](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Template_literals), caracteres de escape de puntos de [código Unicode](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Lexical_grammar#String_literals)  
   :::column-end:::
:::row-end:::  

Para obtener una comparación de la compatibilidad de JavaScript en Internet Explorer, Microsoft Edge y las aplicaciones de Microsoft Store, consulte [información de versión de JavaScript](./javascript-version-information.md).  

### Capturas multimedia y secuencias  

Microsoft Edge presenta compatibilidad con las API de captura de contenido multimedia y secuencias basadas en la especificación [W3C multimedia Capture and streams](https://w3c.github.io/mediacapture-main/getusermedia.html) .  Estas API de JavaScript permiten a las páginas Web acceder a dispositivos de captura multimedia, como cámaras Web o micrófonos, con permiso del usuario.  Al usar las API de captura y secuencias de contenido multimedia, puedes crear escenarios como capturar una foto con una cámara web o capturar un mensaje de voz de un micrófono.  Más información sobre la captura multimedia en Microsoft Edge en el [blog para desarrolladores de Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/13).  

### Nuevo elemento HTML y atributos  

*   `meter` Element  
*   `picture` Element  
*   `template` Element  
*   `image` elemento: `srcset` y `sizes` atributos \( [publicación del blog](https://blogs.windows.com/msedgedev/2015/06/08)de Microsoft Edge Developer \)  
*   `selectionDirection` attribute  
*   `input type=time` y `input type=datetime-local`  

### API de RTC de objeto  

Object Real-Time Communications \(ORTC \) permite que los medios \(audio y/o video \) se transmitan \(enviados y recibidos \) en tiempo real directamente entre exploradores Web, dispositivos móviles y servidores a través de las API nativas de JavaScript.  Consulta el tema de la guía de desarrollo [API de RTC](https://ortc.org) para obtener más información sobre ORTC en Microsoft Edge.  

### Vista de lectura  

Microsoft Edge ofrece una vista de lectura para obtener una experiencia de lectura más fluida y simplificada de las páginas web sin la distracción de contenido no relacionado u otro contenido secundario de la página.  La vista de lectura se puede activar o desactivar desde la vista de lectura \(icono de libro \) en la barra de direcciones o con `Ctrl` + `Shift` + `R` .  Para obtener más información, visita la [vista de lectura](../browser-features/reading-view.md) .  

### Búsqueda de detección de proveedor  

La barra de direcciones de Microsoft Edge está integrada en la integración de búsqueda enriquecida, incluidas las sugerencias de búsqueda, los resultados de la web, el historial de exploración y los favoritos.  Microsoft Edge sigue la especificación de [OpenSearch 1,1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) para descubrir y usar proveedores de búsqueda web.  Si eres un proveedor de búsqueda, Obtén [más](../browser-features/search-provider-discovery.md) información sobre cómo asegurarte de que Microsoft Edge sea compatible con tu servicio.  

### Compatibilidad con las API de WebKit  

Para mejorar la compatibilidad, Microsoft Edge admite una variedad de `-webkit-` API prefijas.  Para obtener una lista completa de `-webkit-` las API admitidas, use el [Catálogo de API](https://developer.microsoft.com/microsoft-edge/platform/catalog/?page=1&q=webkit).  

### Audio Web  

Microsoft Edge presenta compatibilidad con la especificación de la [API de audio Web de W3C](https://webaudio.github.io/web-audio-api) .  El audio web es una API de JavaScript de alto nivel para procesar y sintetizar el audio en aplicaciones web con el fin de ofrecer experiencias de audio y música enriquecidas.  Si bien el `audio` elemento HTML5 permite la reproducción de audio de transmisión por secuencias básica, la API de audio web ofrece un conjunto de API que permiten reproducir varios sonidos con una sincronización estrecha y aplicar ganancias, fundidos, transiciones y efectos básicos en audio mezclado.  Más información sobre [audio web] (.. /multimedia/web-audio.MD en la guía para desarrolladores y en el [blog para desarrolladores de Microsoft Edge](https://blogs.windows.com/msedgedev/2015/05/19).  

### Controlador Web  

La [API Webdriver de W3C](https://w3.org/TR/webdriver) es una plataforma e interfaz independiente del idioma y Protocolo de conexión que permite a los programas o las secuencias de comandos controlar el comportamiento de un explorador Web.  Webdriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.  Esto es diferente de las pruebas unitarias de JavaScript porque Webdriver tiene acceso a la funcionalidad e información que JavaScript ejecuta en el explorador, y puede simular con más precisión los eventos de usuario o los eventos de nivel de sistema operativo.  Webdriver también puede administrar las pruebas en varias ventanas, pestañas y páginas web en una sola sesión de prueba.  Para obtener más información sobre cómo empezar a usar Webdriver para Microsoft Edge, consulte [Webdriver](../../webdriver/index.md).  

## Nuevas API en EdgeHTML 12  

Esta es la lista completa de las API nuevas de EdgeHTML 12.  Se muestran en el formato de `[interface name].[api name]` .  

 > [!NOTE] 
 > Muchas de estas API estaban disponibles en IE11.  Los datos siguientes de EdgeHTML 12 se ofrecen como una línea base para comparar la versión inicial de EdgeHTML con versiones posteriores.  

<iframe height='580' scrolling='no' title='Nuevas API en EdgeHTML 12' src='//codepen.io/MicrosoftEdgeDocumentation/embed/pPOwby/?height=580&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulta las <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/pPOwby/'> nuevas API de Pen en EdgeHTML 12 de </a> docs Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) en <a href='https://codepen.io'> CodePen </a> .</iframe>  

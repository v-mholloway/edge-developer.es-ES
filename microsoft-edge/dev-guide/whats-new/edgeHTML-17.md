---
title: Nuevas características y API en EdgeHTML 17
description: Esta guía proporciona una descripción general de las características y los estándares para desarrolladores incluidos en EdgeHTML 17.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 0fc7dda532866e8970003bce2febb7e46fbbc459
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941940"
---
# Novedades de EdgeHTML 17  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

A continuación se ofrece una lista de las características nuevas y actualizadas que se incluyen en la plataforma Web [EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/04/30) , como parte de la [actualización del 2018 de abril de Windows 10](https://blogs.windows.com/windowsexperience/2018/04/27) (04/2018, compilación 17134 \).  Para obtener información sobre los cambios en las compilaciones específicas de [Windows Insider](https://insider.windows.com) Preview, vea el registro de cambios de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) y las novedades [de EdgeHTML](../whats-new.md).  

Este es el vínculo permanente de la siguiente lista de cambios: [https://aka.ms/devguide_edgehtml_17](./edgehtml-17.md) .  

## Características nuevas y actualizadas  

### Roles, Estados y eventos de ARIA 1,1  

EdgeHTML 17 agrega compatibilidad con los roles, los Estados y las propiedades de la [especificación de aplicaciones de Internet enriquecidas accesibles (WAI-ARIA) 1,1](https://w3.org/TR/wai-aria-1.1), incluidos la [fuente](https://www.w3.org/TR/wai-aria-1.1#feed), el [formato](https://www.w3.org/TR/wai-aria-1.1#form), [Aria-haspopup](https://w3.org/TR/wai-aria-1.1#aria-haspopup), [Aria-marcador](https://w3.org/TR/wai-aria-1.1#aria-placeholder)y muchos más; Busque una [lista completa de las actualizaciones de Aria en el registro de cambios](https://developer.microsoft.com/microsoft-edge/platform/changelog/desktop/17134/?compareWith=16299).  Con esta actualización, EdgeHTML 17 ahora es compatible con todos los roles y atributos definidos en WAI-ARIA 1,1.  Consulte los documentos de [accesibilidad](../../accessibility.md) para obtener más información sobre la accesibilidad en Microsoft Edge.  

### Enmascaramiento de CSS  

EdgeHTML 17 incluye soporte experimental para [enmascaramiento de CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking).  La implementación parcial introduce las propiedades [máscara de CSS, imagen](https://developer.mozilla.org/docs/Web/CSS/mask-image) y [tamaño de máscara](https://developer.mozilla.org/docs/Web/CSS/mask-size) .  Active la bandera "habilitar máscaras CSS" en acerca de: marcas para experimentar.  

### Transformaciones CSS en elementos SVG  

EdgeHTML 17 ahora es compatible con las transformaciones de CSS en elementos SVG y atributos de presentación.  Esto permite manipular visualmente los elementos SVG, como girar, escalar, mover, sesgar o traducir.  

### Extensions  

Microsoft Edge ahora es compatible con la [API de notificaciones](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) que muestra notificaciones de extensiones.  Los desarrolladores de extensiones ahora pueden crear diferentes tipos de notificaciones \ (básico, lista, imagen, etc.) que admiten la interacción completa del usuario.  Las notificaciones también se registran automáticamente en el centro de actividades.  Visita el [ejemplo de notificaciones](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/notifications/notifications) sobre cómo usar esta API en tu extensión.  

EdgeHTML 17 ahora también admite el `Tabs.reload()` método como parte de la clase API de las pestañas estándar.  En la actualización de 2018 de abril de, los usuarios ahora pueden elegir permitir que se ejecuten las extensiones durante la exploración de InPrivate.  

Para obtener más información sobre las actualizaciones de las extensiones de esta versión, vaya a las características de publicación de blog [nuevas para las extensiones de la actualización de 2018 de abril de Windows 10](https://blogs.windows.com/msedgedev/2018/05/24).  

### DevTools  

Esta versión de la DevTools se envía de dos maneras: como las tradicionales \ ( `F12` \) herramientas integradas para Microsoft Edge y la vista previa como una aplicación independiente de [Windows 10](../../devtools-guide/whats-new/edgehtml-17.md#microsoft-edge-devtools-app-preview) de Microsoft Store.  

:::image type="complex" source="../../devtools-protocol/media/microsoft-edge-devtools.png" alt-text="Aplicación de DevTools de Microsoft Edge" lightbox="../../devtools-protocol/media/microsoft-edge-devtools.png":::
   Aplicación de DevTools de Microsoft Edge  
:::image-end:::  

Las herramientas también se han actualizado con varias características principales, entre las que se incluyen la compatibilidad básica para la [depuración remota](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol) \ (a través de nuestro nuevo [Protocolo de DevTools](../../devtools-guide/whats-new/edgehtml-17.md#devtools-protocol)\), [características de depuración de PWA](../../devtools-guide/whats-new/edgehtml-17.md#pwa-debugging), administración de la caché de [IndexedDB](../../devtools-guide/whats-new/edgehtml-17.md#indexeddb-inspection), [acoplamiento vertical](../../devtools-guide/whats-new/edgehtml-17.md#docking-to-the-right-in-microsoft-edge) y mucho más. También hemos continuado el [esfuerzo de refactorización](./edgehtml-16.md) general de la última versión, como parte de las inversiones continuas en rendimiento y confiabilidad.  

Para obtener más información [, visita DevTools en la actualización más reciente de Windows 10 (EdgeHTML 17)](../../devtools-guide/whats-new/edgehtml-17.md) .  

### JavaScript  

Con EdgeHTML 17, el motor de JavaScript de Chakra introduce mejoras de rendimiento en varias áreas clave:  

:::row:::
   :::column span="1":::
      **Superficie de memoria más eficiente**  
   :::column-end:::
   :::column span="2":::
      *   \ (Volver a \) aplazar el análisis de [funciones](https://github.com/Microsoft/ChakraCore/pull/4105) y [métodos de flecha en literales de objeto](https://github.com/Microsoft/ChakraCore/pull/4136)  
      *   [Refactorización de código de bytes RegExp](https://github.com/Microsoft/ChakraCore/pull/3915)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Integrado de JavaScript más rápido**
   :::column-end:::
   :::column span="2":::
      *   [Uso compartido de tipos para Object. Create](https://github.com/Microsoft/ChakraCore/pull/3901)  
      *   [Caché en línea polimórfico para objeto. asignar](https://github.com/Microsoft/ChakraCore/pull/3792)  
      *   [Optimizaciones de JSON. Parse/stringify](https://github.com/Microsoft/ChakraCore/pull/4077)  
      *   [Rescribir los iteradores de matriz en JavaScript y más rápido para... del](https://github.com/Microsoft/ChakraCore/pull/4095)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Ensamblado Web**
   :::column-end:::
   :::column span="2":::
      *   [Soporte técnico de Inling](https://github.com/Microsoft/ChakraCore/pull/3681)  
   :::column-end:::
:::row-end:::  

Consulta el [rendimiento mejorado de JavaScript y Webassembly en el EdgeHTML 17](https://blogs.windows.com/msedgedev/2018/06/19) para obtener todos los detalles.  

### Elemento multimedia

EdgeHTML 17 incluye actualizaciones a [HTMLMediaElement](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) , entre las que se incluyen:  

*   El nuevo `preload` atributo del [`<media>`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) elemento indica qué datos se deben cargar previamente.
*   La adición del [`setSinkId()`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/setSinkId) método y la [`sinkId`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/sinkId) propiedad permite que los programadores seleccionen el dispositivo de salida de audio.  
    
    > [!NOTE]
    > Esto aún no está disponible en RTC.  
    
### API de captura multimedia  

Microsoft Edge ahora admite la captura de pantalla en RTC a través de la [API de captura multimedia](https://w3c.github.io/mediacapture-screen-share).  Esta característica permite a las páginas web capturar la salida del dispositivo de visualización de un usuario, que suele usarse para difundir un escritorio con la presentación o las reuniones virtuales sin complementos.  

### Aplicaciones web progresivas  

A partir de EdgeHTML 17, los trabajos de servicio y las notificaciones de inserción están habilitados de forma predeterminada \ (Obtenga más información sobre estas características en el trabajo del servicio de entrada de blog [: va más allá de la página](https://blogs.windows.com/msedgedev/2017/12/19)).  Esto completa el conjunto de tecnologías \ (incluidas las API de captura de red y de inserción y caché \) que establece la base técnica de las aplicaciones web progresivas \ (PWAs \) en Windows 10.  

PWAs son simplemente aplicaciones web que se han [mejorado progresivamente](https://en.wikipedia.org/wiki/Progressive_enhancement) con características nativas de la aplicación en plataformas de soporte y motores de explorador, como la instalación, la pantalla de inicio y las notificaciones de inserción.  En Windows 10 con el motor Microsoft Edge \ (EdgeHTML \), PWAs disfruta de la ventaja agregada de ejecutar independientemente la ventana del explorador como aplicaciones para la [plataforma universal de Windows](/windows/uwp/get-started/whats-a-uwp) .  

Más allá de PWAs, los trabajadores del servicio y la API de caché permiten a los desarrolladores interceptar solicitudes de red y responder desde la caché.  Un sitio web no debe ser ni siquiera una aplicación web completa que aproveche la memoria caché de trabajos de servicio para la confiabilidad y el rendimiento de carga de página tined, así como la capacidad de ofrecer una experiencia sin conexión durante períodos de ausencia de Internet o de mala calidad.  

Vaya a nuestras [aplicaciones web progresivas en documentos de Windows](../../progressive-web-apps-edgehtml/index.md) para obtener más información sobre los trabajos de servicio y detalles sobre PWAs en Windows 10.  

### Seguridad Web  

EdgeHTML 17 introduce compatibilidad con la integridad de Subrecursos \ (SRI \).  La integridad de los [Subrecursos](https://developer.mozilla.org/docs/Web/Security/Subresource_Integrity) es una característica de seguridad que permite a los exploradores comprobar que los recursos recuperados \ (como imágenes, scripts, fuentes, etc. \) se entregan sin manipulación inesperada.  

Agregue un `integrity` atributo que contenga una representación de hash criptográfica del recurso que espera cargar en la página web en un `<script>` `<link>` elemento o, como en el ejemplo siguiente.  Después, Microsoft Edge comparará el recurso solicitado con el valor hash definido en el `integrity` atributo.  Si no coinciden, Microsoft Edge no ejecutará el recurso y devolverá un error a la red.  

```html
<script src="https://example.com/example-framework.js" 
        integrity="sha384-Li9vy3DqF8tnTXuiaAJuML3ky+er10rcgNR/VqsVpcw+ThHmYcwiB1pbOxEbzJr7" 
        crossorigin="anonymous"></script>
```  

También novedades de EdgeHTML 17, el encabezado de solicitud de [actualización de solicitudes inseguras](https://developer.mozilla.org/docs/Web/HTTP/Headers/Upgrade-Insecure-Requests) permite a los exploradores solicitar una experiencia de navegación segura.  Este encabezado indica al servidor que el explorador admite la actualización de solicitudes no seguras y el usuario debe redirigirse a una versión segura del sitio, si está disponible.  

### Fuentes de variables
La compatibilidad completa con las fuentes variables \ (incluyendo CSS [Font-VARIATION-Settings](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings) y [Font-Optical-Sizing](https://developer.mozilla.org/docs/Web/CSS/font-variation-settings)\) está disponible en EdgeHTML 17.  Las fuentes variables permiten a los programadores alcanzar el aspecto de tipos de letra aparentemente diferentes con una sola fuente mediante el ajuste de varios ejes, lo que reduce la necesidad de varios archivos de fuentes y mejora el rendimiento.  

Únase a nosotros en [una expedicion para obtener información sobre qué fuentes variables proporcionan diseñadores y desarrolladores web](https://developer.microsoft.com/microsoft-edge/testdrive/demos/variable-fonts), y cómo usarlas en su sitio.  Y Obtén más información sobre las fuentes de variables en la entrada de blog, lo [que aporta tipografía expresiva a Microsoft Edge con fuentes variables](https://blogs.windows.com/msedgedev/2018/03/13).  

<iframe height='456' scrolling='no' title='Ejemplos de vale mareas variable' src='//codepen.io/MSEdgeDev/embed/dmYvWg/?height=456&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulte los ejemplos de vale de mareas de la <a href='https://codepen.io/MSEdgeDev/pen/dmYvWg/'> variable de lápiz </a> de MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='https://codepen.io'> CodePen </a> .</iframe>  

## Nuevas API en EdgeHTML 17  

Esta es la lista completa de las API nuevas en EdgeHTML 17.  Se muestran en el formato de `[interface name].[api name]` .  

> [!NOTE] 
> A pesar de que las siguientes API están expuestas en el DOM, el comportamiento end-to-end de algunos podría estar aún en desarrollo.  Consulta el  [Estado de la plataforma de Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para la compatibilidad de características de Word oficial.  

<iframe height='580' scrolling='no' title='Nuevas API en EdgeHTML 17' src='//codepen.io/MSEdgeDev/embed/pLxgdj/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulta las <a href='https://codepen.io/MSEdgeDev/pen/pLxgdj/'> nuevas API de Pen en EdgeHTML 17 de </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='https://codepen.io'> CodePen </a> .</iframe>  

> [!TIP]
> Hemos [colaborado](https://blogs.windows.com/msedgedev/2017/10/18) con otros exploradores y la comunidad web en la adopción de [documentos web de MDN](https://developer.mozilla.org) como lugar definitivo para la documentación útil, no sesgada y independiente del explorador para las tecnologías web basadas en estándares actuales y emergentes.  Puede encontrar detalles sobre la compatibilidad con la API de EdgeHTML directamente en cada página de la [biblioteca de referencia Web de MDN](https://developer.mozilla.org/docs/Web).  Visita el estado de la [plataforma](https://developer.microsoft.com/microsoft-edge/status) de Microsoft Edge para obtener las características más recientes compatibles con Microsoft Edge.  

## Versiones anteriores de EdgeHTML  

[EdgeHTML 13/Windows compilación 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)  

[EdgeHTML 14/Windows compilación 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)  

[EdgeHTML 15/Windows compilación 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)  

[EdgeHTML 16/Windows compilación 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)  

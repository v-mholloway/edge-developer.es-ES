---
description: En esta guía se proporciona información general sobre las características y estándares del desarrollador incluidos en EdgeHTML 16.
title: Nuevas características y API en EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, web development, html, css, javascript, developer
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399200"
---
# <a name="whats-new-in-edgehtml-16"></a>Novedades de EdgeHTML 16  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Esta es una lista de las características nuevas y actualizadas que se incluyen en la plataforma web [EdgeHTML 16,](https://blogs.windows.com/msedgedev/2017/10/17) como parte de [windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, compilación 16299\).  Para ver los cambios en compilaciones específicas de Windows Insider Preview, consulta el Registro de cambios de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) y Novedades [de EdgeHTML](../whats-new.md).  

Este es el vínculo permanente para la siguiente lista de cambios:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .  

## <a name="new-and-updated-features"></a>Características nuevas y actualizadas  

### <a name="css-grid-layout"></a>Diseño de cuadrícula CSS  

Microsoft Edge ahora admite la implementación sin prefijo del diseño [de cuadrícula CSS](https://www.w3.org/TR/css-grid-1).  [Diseño de](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) cuadrícula define un sistema de diseño basado en cuadrícula bidimensional que permite más fluidez de diseño que posible con el posicionamiento mediante floats o scripts.  En el ejemplo siguiente se usa el diseño de cuadrícula CSS para crear la estructura de una página web básica.  

<iframe height='303' scrolling='no' title='Diseño de cuadrícula CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Vea el diseño de <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> cuadrícula CSS del lápiz por </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) en </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

### <a name="css-object-fit-and-object-position"></a>Ajuste de objeto CSS y posición de objeto  

EdgeHTML 16 presenta compatibilidad con las propiedades CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) y [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Estas propiedades controlan la posición y el tamaño del contenido reemplazado dentro del cuadro de contenido.  

### <a name="developer-tools"></a>Herramientas de desarrollo  

En esta versión, iniciamos un gran esfuerzo de refactorización de Microsoft Edge DevTools para mejorar la robustez y el rendimiento, y también agregamos un montón de nuevas características que puedes empezar a usar hoy en las compilaciones de [Windows Insider.](https://insider.windows.com)  Echa un vistazo a [la guía de Microsoft Edge DevTools](../whats-new.md) para obtener más información sobre lo que ha cambiado.  

### <a name="javascript"></a>JavaScript  

[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) se basa en optimizaciones de rendimiento de Javascript de versiones anteriores al expandir la capacidad del motor Decácrate para aplazar o volver a aplazar funciones, usar cachés en línea polimórficas y optimizar funciones con `try` / `finally` bloques.  

Además, las características vistas previamente en EdgeHTML 15 ahora son estables y están habilitadas de forma predeterminada:  

#### <a name="new-features"></a>Nuevas características  

Activado de forma predeterminada  

*   [WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)  
*   [Memoria compartida y atómicos](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a>API de solicitud de pago  

La [API de](../windows-integration/payment-request-api.md) solicitud de pago es un estándar abierto entre exploradores que permite a los exploradores actuar como intermediarios entre comerciantes, consumidores y métodos de pago \(como tarjetas de crédito\) que los consumidores han almacenado en la nube.  La API de EdgeHTML 16 se ha actualizado para que coincida con la última especificación de la [API](https://w3c.github.io/payment-request) de solicitud de pago de W3C.  Esto incluye:  

*   Compatibilidad con el `canMakePayment()` método  
*   Compatibilidad con la `requestId` propiedad  
*   Compatibilidad con la `id` propiedad  
*   El valor predeterminado del `complete()` parámetro del método `result` cambió de " " a "unknown"  

### <a name="service-workers"></a>Trabajos de servicio  

[Los trabajadores](https://www.w3.org/TR/service-workers-1) de servicio son scripts controlados por eventos que se ejecutan en segundo plano de una página web.  Los trabajadores del servicio solo habilitan la funcionalidad que anteriormente solo está disponible con aplicaciones nativas, como interceptar y controlar solicitudes de la red, administrar y administrar la sincronización en segundo plano, el almacenamiento local y las notificaciones push.  La compatibilidad con el trabajador de servicio aún está en desarrollo, pero puede probar su PWA en Microsoft Edge con nuestro soporte técnico experimental del trabajador de servicio habilitando la característica de trabajador de servicio en `about:flags` .  

### <a name="webvr"></a>WebVR  

WebVR para Microsoft Edge ha agregado compatibilidad con controladores [de movimiento.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)  Estos controladores tienen una posición precisa en el espacio, lo que permite una interacción detallada con objetos digitales en la realidad virtual.  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Controladores de movimiento" lightbox="../media/MotionControllers.jpg":::
   Controladores de movimiento  
:::image-end:::  

WebVR también se ha optimizado para admitir dos tipos diferentes de experiencias.  

**Equipos con Windows Mixed Reality:** equipos de escritorio y portátiles con gráficos integrados.  Cuando se conecta a estos dispositivos, nuestros auriculares envolventes se ejecutarán a 60 fotogramas por segundo.  
**Equipos Windows Mixed Reality Ultra:** equipos de escritorio y portátiles con gráficos discretos.  Cuando se conecta a estos dispositivos, nuestros auriculares envolventes se ejecutarán a 90 fotogramas por segundo.  

Ambas configuraciones admitirán las mismas experiencias envolventes de vídeo y juegos.  

Para obtener más información acerca de las próximas actualizaciones de Windows Mixed Reality, consulta la entrada de blog de actualización de días festivos de [Windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)  

Para obtener guías y demostraciones, dirígete a [la Guía para desarrolladores de WebVR.](/microsoft-edge/webvr)  

 > [!NOTE] 
 > Dado que la especificación webVR todavía está en desarrollo, la implementación de Microsoft Edge puede cambiar más adelante hacia abajo.  

## <a name="new-apis-in-edgehtml-16"></a>Nuevas API en EdgeHTML 16  

Esta es la lista completa de nuevas API en EdgeHTML 16.  Se enumeran con el formato `[interface name].[api name]` de .

> [!NOTE] 
> Aunque las siguientes API se exponen en el DOM, el comportamiento de extremo a extremo de algunas puede estar todavía en desarrollo.  Consulte Estado de [la plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) para obtener información oficial sobre la compatibilidad con características.  

---  

<iframe height='559' scrolling='no' title='Nuevas API en EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Vea las API nuevas del lápiz <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> en EdgeHTML 16 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) en </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

---  

## <a name="previous-edgehtml-releases"></a>Versiones anteriores de EdgeHTML  

[EdgeHTML 12 / Windows build 10240 (7/2015)](./edgehtml-12.md)  

[EdgeHTML 13 / Windows build 10586 (11/2015)](./edgehtml-13.md)  

[EdgeHTML 14 / Compilación de Windows 14393 (8/2016)](./edgehtml-14.md)  

[EdgeHTML 15 / Windows build 15063 (4/2017)](./edgehtml-15.md)  

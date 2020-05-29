---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Esta guía proporciona una descripción general de las características y los estándares del desarrollador que se incluyen en Microsoft Edge.
title: Guía para desarrolladores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 36c5e6530ff584a97e4b42910757495362a1960d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572983"
---
# Novedades de EdgeHTML 16

A continuación se ofrece una lista de las características nuevas y actualizadas que se incluyen en la plataforma Web [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17/edgehtml-16-fall-creators-update/) , como parte de [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update/) (10/2017, compilación 16299). Para obtener información sobre los cambios en las compilaciones específicas de Windows Insider Preview, vea el registro de cambios de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog/) y las novedades [de EdgeHTML](../whats-new.md).

Este es el vínculo permanente de la siguiente lista de cambios: [https://aka.ms/devguide_edgehtml_16](https://aka.ms/devguide_edgehtml_16) .

## Características nuevas y actualizadas

### Diseño de cuadrícula CSS

Microsoft Edge ahora es compatible con la implementación no prefijada de [diseño de cuadrícula CSS](https://www.w3.org/TR/css-grid-1/). [Diseño de cuadrícula](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) define un sistema de diseño basado en cuadrícula bidimensional que permite más fluidez de diseño que el que se puede realizar con el posicionamiento mediante flotadores o secuencias de comandos. En el siguiente ejemplo se usa el diseño de cuadrícula CSS para crear la estructura de una página web básica.


<iframe height='303' scrolling='no' title='Diseño de cuadrícula CSS' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Consulta el <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> diseño de cuadrícula CSS de lápiz </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='https://codepen.io'> CodePen </a> .
</iframe>


### CSS `object-fit` y `object-position`

EdgeHTML 16 introduce compatibilidad con propiedades de CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) y [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .  Estas propiedades controlan la posición y el tamaño del contenido reemplazado en el cuadro de contenido.  

### Herramientas de desarrollo

Esta versión comenzamos un importante esfuerzo de Microsoft Edge para refactorizar DevTools para mejorar la solidez y el rendimiento, además de agregar un conjunto de nuevas características que puede comenzar a usar hoy en las compilaciones de [Windows Insider](https://insider.windows.com/) .  Consulte la [Guía de DevTools Microsoft Edge](../../devtools-guide/whats-new.md) para obtener más información sobre lo que ha cambiado.

### JavaScript

[EdgeHTML 16 desarrolla](https://blogs.windows.com/msedgedev/2017/10/31/optimizations-webassembly-sharedarraybuffer-atomics-edgehtml-16/#FodxEPHxR4WkbtyA.97) las optimizaciones de rendimiento de JavaScript de versiones anteriores expandiendo la capacidad del motor de Chakra para aplazar o volver a aplazar funciones, usar memorias caché polimórficos en línea y optimizar funciones con bloques *try/finally* .

Además, características que aparecen en la primera vista previa de la EdgeHTML 15 ahora son estables y habilitadas de forma predeterminada:

#### Características nuevas (activada de forma predeterminada)

* [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP ([demostración](https://webassembly.org/demo/))
* [Memoria compartida y atómicas](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

### API de solicitud de pago

La [API de solicitud de pago](../windows-integration/payment-request-api.md) es un estándar entre exploradores abierto que permite que los exploradores actúen como intermediario entre comerciantes, consumidores y formas de pago (por ejemplo, tarjetas de crédito) que los consumidores han almacenado en la nube.  La API de EdgeHTML 16 se ha actualizado para coincidir con la última especificación de [API de solicitud de pago](https://w3c.github.io/payment-request/) de W3C. Esto incluye:
* Compatibilidad con el `canMakePayment()` método
* Compatibilidad con la `requestId` propiedad
* Compatibilidad con la `id` propiedad
* El valor predeterminado del `complete()` parámetro del método `result` ha cambiado de "" a "desconocido".

### Trabajadores de servicio

Los [trabajadores del servicio](https://www.w3.org/TR/service-workers-1/) son scripts controlados por eventos que se ejecutan en el fondo de una página web. Los trabajadores de servicio habilitan la funcionalidad anteriormente solo disponible con aplicaciones nativas, como interceptar y administrar solicitudes de la red, administrar y controlar la sincronización en segundo plano, el almacenamiento local y las notificaciones Push. El soporte técnico para el servicio de trabajo de servicio aún está en desarrollo, pero puede probar su PWA en Microsoft Edge con nuestro soporte técnico de trabajo de servicio experimental habilitando la característica de trabajo de servicio en **About: flags**.

### WebVR
WebVR para Microsoft Edge ha agregado compatibilidad con [los controladores de movimiento](https://developer.microsoft.com/windows/mixed-reality/motion_controllers). Estos controladores tienen una posición precisa en el espacio, lo que permite una interacción minuciosa con objetos digitales en realidad virtual.

![Controladores de movimiento](../media/MotionControllers.jpg)

WebVR también se ha optimizado para admitir dos tipos diferentes de experiencias.

Equipos de escritorio y portátiles **Windows Mixed Reality** con gráficos integrados.  Cuando esté conectado a estos dispositivos, nuestros auriculares con micrófono tan solo se ejecutarán a 60 fotogramas por segundo.  
**Windows Mixed Reality ultra PCS** : computadoras de escritorio y portátiles con gráficos discretos. Cuando esté conectado a estos dispositivos, nuestros auriculares con micrófono tan solo se ejecutarán a 90 fotogramas por segundo.   

Ambas configuraciones soportarán el mismo video y las experiencias de juego. 

Para obtener más información sobre las próximas actualizaciones de Windows Mixed Reality, consulta la entrada de blog de actualización de festividades de [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update/) . 

Para obtener guías y demostraciones, vaya a la [Guía para desarrolladores de WebVR](https://docs.microsoft.com/microsoft-edge/webvr/).

 > [!NOTE] 
 > Puesto que la especificación de WebVR aún está en desarrollo, la implementación de Microsoft Edge puede cambiar más adelante en la línea.

## Nuevas API en EdgeHTML 16

Esta es la lista completa de las API nuevas de EdgeHTML 16. Se muestran en el formato **[nombre de la interfaz]. [ nombre de la API]**.

> [!NOTE] 
> A pesar de que las siguientes API están expuestas en el DOM, el comportamiento end-to-end de algunos podría estar aún en desarrollo. Consulta el [Estado de la plataforma de Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) para la compatibilidad de características de Word oficial.

<iframe height='559' scrolling='no' title='Nuevas API en EdgeHTML 16' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'>Consulta las <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> nuevas API de Pen en EdgeHTML 16 de </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='https://codepen.io'> CodePen </a> .</iframe></p>

<h2 id="previous-edgehtml-releases">Versiones anteriores de EdgeHTML</h2>
<p><a href="https://aka.ms/devguide_edgehtml_12" data-raw-source="[EdgeHTML 12 / Windows build 10240 (7/2015)](https://aka.ms/devguide_edgehtml_12)">EdgeHTML 12/Windows compilación 10240 (7/2015)</a>

[EdgeHTML 13/Windows compilación 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows compilación 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows compilación 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)

---
description: Todo sobre las mejoras del trabajador de servicio y cómo usar cada una de ellas.
title: Mejoras del trabajador de servicio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, service worker, PWA
ms.openlocfilehash: 2f32155d1d28d1e65ad29abfe58a414f3e3c6ed7
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387283"
---
# <a name="service-worker-improvements"></a>Mejoras del trabajador de servicio  

En este artículo se le enseña acerca [][MdnServiceWorkerApi] de las mejoras de las herramientas de desarrollo para trabajar con los trabajadores de servicio y las solicitudes de red que pasan por cada uno de ellos.  Las **mejoras del trabajador de servicio** se encuentran en las herramientas **Red,** **Aplicación** **y** Orígenes.  Las mejoras simplifican las siguientes tareas.  

*   Depuración basada en las escalas de tiempo del trabajador de servicio.  
    *   El inicio de una solicitud y la duración del arranque.  
    *   Actualizar al registro del trabajador de servicio.  
    *   Tiempo de ejecución de una solicitud mediante el [controlador de eventos fetch.][MdnFetchEvent]  
    *   Tiempo de ejecución de todos los eventos de captura para cargar un cliente.  
*   Explore los detalles en tiempo de ejecución de los controladores de eventos de captura, instale controladores de eventos y active controladores de eventos.  
*   Paso a paso hacia dentro y fuera del controlador de eventos de captura con [información de script de página](#sources).  
    
Las experiencias abarcan tres herramientas de desarrollador diferentes.  

1.  La [herramienta Red.](#network)  Elija una solicitud de red que se ejecute a través de un trabajador de servicio y obtenga acceso a la escala de tiempo correspondiente del trabajador de servicio en la **herramienta Timing.**  
1.  La [herramienta Aplicación.](#application)  Para depurar los trabajadores del servicio, vaya a la **herramienta Trabajadores de** servicio.  
1.  La [herramienta Orígenes.](#sources)  Obtener acceso a la información de script de página al acceder a controladores de eventos de captura.  
    
## <a name="network"></a>Red  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Escala de tiempo de trabajo de servicio en la herramienta Red" lightbox="../media/sw-network-timeline.msft.png":::
   Vista de red  
:::image-end:::  

Para obtener acceso a las características de depuración de trabajadores de servicio en la **herramienta Red,** realice una de las siguientes acciones.  

*   Accede directamente a la **herramienta Red.**  
*   Se inició en **la herramienta Aplicación.**  
    
### <a name="request-routing"></a>Enrutamiento de solicitudes  

Para facilitar la visualización del enrutamiento de solicitudes, las escalas de tiempo ahora muestran el inicio del trabajador de servicio y los eventos `respondWith` de captura.  Para depurar y visualizar una solicitud de red que pasó a través de un trabajador de servicio, realice las siguientes acciones.  

1.  Elija la solicitud de red que ha pasado por un trabajador de servicio.  
1.  Abra la **herramienta Temporización.**  
    
### <a name="fetch-events"></a>Eventos de captura  

Para obtener más información sobre los eventos de captura, elija la flecha `respondWith` desplegable situada a la izquierda del archivo `respondWith` .  Para obtener más información acerca de la solicitud **original** y **la respuesta recibida,** use las flechas desplegables correspondientes.  

## <a name="application"></a>Aplicación  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Vista Aplicación" lightbox="../media/sw-application-timeline.msft.png":::
   Vista Aplicación  
:::image-end:::  

### <a name="service-worker-update-timeline"></a>Escala de tiempo de actualización del trabajador de servicio  

El Microsoft Edge DevTools agregó una escala de tiempo en la **herramienta Aplicación** para reflejar el ciclo de vida de actualización del trabajador del servicio.  Muestra los eventos de instalación y activación.  Cada uno de los eventos tiene una flecha desplegable correspondiente para darle más detalles.  

### <a name="request-routing-and-fetch-events"></a>Eventos de enrutamiento y captura de solicitudes  

Ahora puede acceder a las escalas de tiempo del trabajador de servicio a través **de la herramienta Red** en el cajón de la consola.  La característica beneficia el rendimiento, minimiza la duplicación de la interfaz de usuario y crea una experiencia de depuración más completa.  

1.  Abra el trabajador de servicio que está depurando.  
1.  Elija el **botón Red** para abrir la experiencia de enrutamiento [de solicitudes.](#network)  
1.  Use los desplegables **respondWith** para obtener información sobre la solicitud de evento y la respuesta.  

La **herramienta Red** muestra las solicitudes de red que pasaron por el trabajador de servicio que está depurando.  El filtro automático es una forma de restringir la exploración.

## <a name="sources"></a>Orígenes  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Vista DOM" lightbox="../media/sw-sources.msft.png":::
   Vista DOM  
:::image-end:::  

Para encontrar más información sobre la pila, establezca un punto de interrupción en el controlador de captura.  Los detalles llevan a dónde se solicita el recurso en el script de página.  Cuando el depurador se detiene dentro de un controlador de captura, se muestra una información de pila combinada en el panel a la derecha.  Después de eso, puede moverse en los marcos de la pila.  

### <a name="future-work"></a>Trabajo futuro  

El Microsoft Edge de DevTools planea desarrollar aún más los detalles de la memoria caché y están investigando más formas de mejorar la experiencia de depuración del trabajador del servicio para desarrolladores de [aplicaciones web][MdnProgressiveWebApps] progresivas.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Aplicaciones web progresivas (PWA) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Api de trabajo de servicio | MDN"  

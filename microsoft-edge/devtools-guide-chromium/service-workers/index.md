---
description: Todo sobre las mejoras de los trabajadores de servicios y cómo usar cada una de ellas.
title: Mejoras de los trabajos de servicio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, trabajo de servicios, PWA
ms.openlocfilehash: 4e1b43235ccd7b108d2aadd1c803aa3276fa1265
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190049"
---
# Mejoras de los trabajos de servicio  

Este artículo le enseña acerca de las mejoras en los [trabajadores de servicios][MdnServiceWorkerApi] y las solicitudes de red que pasan por cada uno de ellos.  Las **mejoras** de los trabajos de servicio se encuentran en las herramientas **red**, **aplicaciones**y **fuentes** .  Las mejoras incluyen las siguientes tareas.  

*   Depurar en función de escalas de tiempo de trabajo de servicio.  
    *   El inicio de una solicitud y la duración del bootstrap.  
    *   Actualice el registro de trabajadores del servicio.  
    *   El motor en tiempo de ejecución de una solicitud mediante el controlador de [eventos fetch][MdnFetchEvent] .  
    *   El motor en tiempo de ejecución de todos los eventos fetch para cargar un cliente.  
*   Explore los detalles de tiempo de ejecución de los controladores de eventos de Fetch, instale controladores de eventos y Active controladores de eventos.  
*   Ir hacia dentro y fuera del controlador de eventos de Fetch con [información de script de página](#sources).  

Las experiencias abarcan tres herramientas de desarrollador diferentes.  

1.  La herramienta [red](#network) .  Elija una solicitud de red que se ejecute a través de un trabajador de servicio y obtenga acceso a la escala de tiempo correspondiente del trabajo de servicio en la herramienta **intervalos** .  
1.  La herramienta de [aplicación](#application) .  Para depurar los trabajos de servicio, vaya a la herramienta de **trabajos de servicio** .  
1.  La herramienta [orígenes](#sources) .  Obtenga acceso a la información de script de página al entrar en los controladores de eventos de Fetch.  

## Red  

:::image type="complex" source="../media/sw-network-timeline.msft.png" alt-text="Escala de tiempo de trabajo del servicio en la herramienta red" lightbox="../media/sw-network-timeline.msft.png":::
   Vista de red  
:::image-end:::  

Para obtener acceso a las características de depuración de trabajos de servicio de la herramienta **red** , complete una de las siguientes acciones.  

*   Acceso directo en la herramienta **red** .  
*   Se inició en la herramienta de **aplicación** .  
    
### Enrutamiento de solicitudes  

Para facilitar la visualización del enrutamiento de solicitudes, las escalas de tiempo ahora muestran los eventos inicio de trabajo de servicio y `respondWith` captura.  Para depurar y visualizar una solicitud de red que pasó a través de un trabajo de servicio, complete las siguientes acciones.  

1.  Elija la solicitud de red que pasó a un trabajador de servicio.  
1.  Abrir la herramienta **intervalos** .  
    
### Eventos fetch  

Para obtener más información sobre los `respondWith` eventos de captura, elija la flecha de lista desplegable a la izquierda de la `respondWith` .  Para obtener más información sobre la **solicitud original** y la **respuesta recibida**, use las flechas desplegables correspondientes.  

## Aplicación  

:::image type="complex" source="../media/sw-application-timeline.msft.png" alt-text="Vista de aplicación" lightbox="../media/sw-application-timeline.msft.png":::
   Vista de aplicación  
:::image-end:::  

### Escala de tiempo de actualización de trabajo del servicio  

El equipo de DevTools Microsoft Edge agregó una escala de tiempo en la herramienta de **aplicaciones** para reflejar el ciclo de vida de actualización del trabajador de servicio.  Muestra los eventos de instalación y activación.  Cada uno de los eventos tiene una flecha desplegable correspondiente para obtener más información.  

### Solicitar eventos de enrutamiento y búsqueda  

Ahora puede acceder a las escalas de tiempo de los trabajos de servicio a través de la herramienta de **red** en el cajón de la consola.  La característica beneficia el rendimiento, minimiza la duplicación de la interfaz de usuario y crea una experiencia de depuración más completa.  

1.  Abra el trabajador de servicio que está depurando.  
1.  Haga clic en el botón **red** para abrir la [experiencia de enrutamiento](#network)de la solicitud.  
1.  Use los menús desplegables **respondWith** para obtener información de solicitud y respuesta de evento.  

La herramienta **red** muestra las solicitudes de red que pasaron por el trabajo de servicio que está depurando.  El filtro automático es una forma de restringir la exploración.

## Orígenes  

:::image type="complex" source="../media/sw-sources.msft.png" alt-text="Vista DOM" lightbox="../media/sw-sources.msft.png":::
   Vista DOM  
:::image-end:::  

Para obtener más información sobre la pila, establezca un punto de interrupción en el controlador de captura.  Los detalles conducen a la ubicación del recurso en la secuencia de comandos de la página.  Cuando el depurador se detiene en un controlador de captura, se muestra la información de la pila combinada en el panel de la derecha.  Después de eso, puede desplazarse por los marcos de pila.  

### Trabajo futuro  

El equipo de Microsoft Edge DevTools planea seguir desarrollando el detalle de la caché y está investigando más formas de mejorar la experiencia de depuración de los trabajos de servicio para los programadores de [aplicaciones web progresivas][MdnProgressiveWebApps] .  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MdnFetchEvent]: https://developer.mozilla.org/docs/Web/API/FetchEvent "FetchEvent | MDN"  
[MdnProgressiveWebApps]: https://developer.mozilla.org/docs/Web/Progressive_web_apps "Aplicaciones web progresivas (PWAs) | MDN"  
[MdnServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API de trabajo de servicio | MDN"  

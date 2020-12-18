---
description: Usar el panel de trabajo de servicio para administrar y depurar los trabajos de servicio
title: DevTools-depurador-trabajadores de servicio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, depuración, depuración, PWA, trabajo del servicio, API de caché
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 99592f787da8bcf89d2e16231aa3f39047b4fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236364"
---
# Trabajos de servicio

El panel de **trabajos de servicio** tiene herramientas para administrar y depurar los trabajos de servicio para su sitio, lo que le ayudará a:

 - Obtener una visión general de todos los trabajos de servicio asociados a su sitio y detalles de su ámbito y estado
 - **Actualizar** y administrar (**eliminar**) el registro de trabajadores del servicio para el ámbito especificado
 - **Insertar** una notificación de prueba
 - **Detener** / **Iniciar** trabajadores de servicio individuales y
 - **Inspeccionar** el trabajador del servicio seleccionado en una ventana independiente del depurador

![Panel de información general del trabajo del servicio](./media/service_worker.png)

Tenga en cuenta lo siguiente sobre la depuración de los trabajos de servicios en Edge DevTools:

 - La depuración de un trabajador de servicio iniciará una nueva instancia de la DevTools independiente de las herramientas de la página porque los trabajos de servicio se pueden compartir entre varias pestañas.
 - Los [**elementos**](./elements.md) y los paneles de [**emulación**](./emulation.md) no están presentes en el depurador de trabajo de servicios, dado que los trabajadores del servicio se ejecutan en segundo plano y no controlan directamente el front-end de la aplicación.
 - En la actualidad, el tráfico de red de un trabajador de servicio solo se notifica desde la instancia de depuración de DevTools para ese trabajo, y no desde la instancia del depurador para la página en sí.
 - Para simular una **inserción** desde la DevTools, tendrá que agregar un detector de eventos de *inserción* al trabajador del servicio para observar su efecto. El siguiente ejemplo imprimirá "probar mensaje push de DevTools" en la **consola**de trabajo del servicio.

   ```JavaScript
   self.addEventListener('push', function(event){
       console.log(event.data.text());
   });
   ```

Estas son algunas de las cosas generales que debe tener en cuenta al usar los trabajos de servicio:

- **Solo HTTPS.** Los trabajos del servicio no funcionan en HTTP; tendrá que usar HTTPS. Sin embargo, puede registrar trabajadores de servicio `localhost` para fines de prueba.

- **No se permite el acceso a DOM.** Al igual que con los trabajadores web, no obtienes acceso al modelo de objetos de la página. Esto significa que si necesita cambiar algo sobre la página, tendrá que usar [`postMessage`](https://developer.mozilla.org/docs/Web/API/Worker/postMessage) desde el trabajo de servicio hasta la página para poder controlar los cambios de Dom en la página.

- **Se ejecuta de forma independiente de la página.** Dado que estas secuencias de comandos no están vinculadas a la duración de una página, es importante comprender que no comparten el mismo contexto que la página. Aparte de no tener acceso al DOM (como se indicó anteriormente), no tendrá acceso a las mismas variables disponibles en la página.

- **Invalida la caché de la *aplicación*.** Se omitirá la caché de la aplicación cuando se estén usando los trabajos del servicio. La API de trabajo de servicios está pensada para suplantar completamente la caché de aplicaciones al otorgar un control granular al desarrollador web.

  - **La secuencia de comandos no puede estar en CDN.** El archivo JavaScript para el trabajo de servicio no se puede hospedar en una red de distribución de contenido (CDN), debe estar en el mismo dominio que la página. Sin embargo, si lo desea, puede importar scripts desde su red CDN.

- **Puede finalizar en cualquier momento.** Los trabajadores del servicio están diseñados para ser de corta duración y su vida útil está vinculado a eventos. En particular, los trabajadores del servicio tienen un límite de tiempo en el que deben finalizar la ejecución de los controladores de eventos. En otros casos, el explorador o el sistema operativo pueden elegir finalizar un trabajador de servicio que afecte al consumo de la batería, la CPU o la memoria. En cualquier caso, evite depender de variables globales en el script de trabajo de servicio en caso de que se use una instancia de trabajo de servicio diferente en un evento subsiguiente que se esté controlando.

- **Solo se permiten solicitudes asincrónicas.** Las XHR sincrónicas no se permiten aquí. Ni es localStorage, por lo que es mejor usar IndexedDB y la nueva API de cachés descrita anteriormente.

- **El trabajo del servicio para el ámbito es 1:1.** Solo podrá tener un trabajador de servicio por ámbito. Esto significa que si intenta registrar un trabajador de servicio diferente para un ámbito que ya tiene un trabajo de servicio, ese trabajo de servicio se actualizará.

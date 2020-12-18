---
description: Garantizar que el contenido multimedia de su sitio se comparará como se pretendía
title: 'Directivas de reproducción automática: Guía de desarrollo'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, multimedia, vídeo, audio, reproducción automática
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 85b91a8b87d73d6fccc6eac2aa64513f283d7f21
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236188"
---
# Directivas de reproducción automática  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge proporciona a los clientes la posibilidad de personalizar sus preferencias de navegación en sitios web con sonido de reproducción automática con el fin de minimizar las distracciones en la web y ahorrar ancho de banda.  Además, Microsoft Edge elimina automáticamente la reproducción automática de los elementos multimedia en las pestañas de fondo.  

Los usuarios pueden personalizar el comportamiento de los medios con controles de reproducción automática [globales](#global-media-autoplay-settings) y [por sitio](#per-site-media-autoplay-settings) , que proporcionan las siguientes opciones:  

*   `Allow`  El valor predeterminado y continuará reproduciendo vídeos cuando una pestaña se visualiza por primera vez en primer plano, a la discreción del sitio.  

*   `Limit`  Restringe la reproducción automática para que solo funcione cuando se silencian los vídeos, de modo que los usuarios nunca se sorprendan por sonido.  Una vez que el usuario hace clic en cualquier lugar de la página, la reproducción automática se vuelve a habilitar y seguirá estando permitida dentro de ese dominio en esa pestaña.  

*   `Block`  Evite sautoplay en todos los sitios hasta que los usuarios interactúen directamente con el contenido multimedia.  

## Configuración de la reproducción automática de multimedia global  

Los usuarios pueden controlar el comportamiento predeterminado de reproducción automática de todos los sitios en **Configuración avanzada**  >  **reproducción automática de multimedia**.  

:::image type="complex" source="../media/autoplay_global.png" alt-text="Configuración de la reproducción automática de multimedia global" lightbox="../media/autoplay_global.png":::
   Configuración de la reproducción automática de multimedia global  
:::image-end:::  

## Configuración de reproducción automática multimedia por sitio  

Los usuarios pueden controlar el comportamiento de la reproducción automática en función de cada sitio en la sección **permisos de sitios web** del panel información del sitio Web.  Para encontrar esta configuración, haga clic en el icono de información o en el icono de candado situado en el lado izquierdo de la barra de direcciones y haga clic en **configuración de multimedia de reproducción automática** para comenzar.  

La configuración por sitio invalida la configuración global.  Por ejemplo, si un usuario tiene su configuración global establecida en `Allow` pero cambia una configuración por sitio a `Block` , la reproducción automática se bloqueará para ese sitio.  

:::image type="complex" source="../media/autoplay_per-site.png" alt-text="Configuración de reproducción automática multimedia por sitio" lightbox="../media/autoplay_per-site.png":::
   Configuración de reproducción automática multimedia por sitio  
:::image-end:::  

## Procedimientos recomendados para desarrolladores web  

A continuación se explica cómo garantizar una buena experiencia de usuario con elementos multimedia hospedados en su sitio:  

*   Supongamos que cada uso de un elemento multimedia retiene un movimiento de usuario para iniciar la reproducción \ (a medida que los usuarios pueden bloquear la reproducción automática en cualquier momento \) y planificar según corresponda.  Las directivas de reproducción automática global y por sitio se aplican a todos los `<audio>` `<video>` elementos y, independientemente de cómo se usan en su sitio.  

*   Asegúrate de que los controles multimedia estén siempre presentes tanto en los medios del sitio como en el contenido de Active Directory.  Esto proporcionará a los usuarios la posibilidad de reiniciar la reproducción si la reproducción automática está bloqueada en la página.  

*   Evalúe cómo la reproducción automática puede influir en la experiencia de los usuarios en su sitio web y considere la posibilidad de usar la reproducción automática para minimizar la reproducción de archivos multimedia no deseados.  Si la reproducción automática es una parte crucial de su experiencia, considere la posibilidad de usar contenido silenciado para iniciar y permitir que el usuario reactive el audio.  Para el contenido silenciado en la reproducción automática, el origen de audio debe estar silenciado o no se puede establecer.  En caso contrario, el elemento no se considerará silenciado.  

*   A menos que sea absolutamente necesario hacer lo contrario, use los controles de explorador nativos para la reproducción de contenido multimedia.  Esto asegurará una experiencia coherente para los usuarios.  Si está creando controles personalizados en su lugar, asegúrese de que los controles multimedia estén siempre presentes y de que los controles respondan correctamente a la supresión de reproducción automática.  

### Delegación de iframe  

La reproducción automática en una `<iframe>` heredará el permiso de reproducción automática de la Página principal, independientemente del origen del contenido.  En un escenario de lista de reproducción en el que cada archivo multimedia está hospedado por un iframe independiente, el usuario solo necesita iniciar la reproducción una vez para toda la lista de reproducción.  

### Detectar cuándo está permitida la reproducción automática  

Puede ajustar los controles de reproducción para que muestren el estado correcto cuando se bloquea la reproducción automática examinando la promesa devuelta por la `play()` función en el elemento multimedia:  

```javascript
var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}
```  

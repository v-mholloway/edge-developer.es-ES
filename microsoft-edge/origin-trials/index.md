---
ms.assetid: ''
description: Experimentos con seguridad durante un período de tiempo fijo y proporciona comentarios sobre las nuevas características de las plataformas.
title: Pruebas de Origen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, pruebas de origen, desarrollador
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846531"
---
# Usar pruebas de origen en Microsoft Edge  

Los programadores pueden usar pruebas de origen para probar las API experimentales en sitios activos durante un período de tiempo limitado.  Al usar las pruebas de origen, los usuarios de Microsoft Edge que visitan su sitio pueden ejecutar código que usa las API experimentales.  Para obtener acceso a las API experimentales de cada equipo de usuario, no es necesario ir a `edge://flags` y activar las marcas de características.  Para obtener más información, consulte [API experimentales][DeveloperMicrsoftEdgeOriginTrials].  Además, puede proporcionar comentarios sobre el diseño de la API, sus casos de uso o su experiencia con las API para ingenieros del explorador y la comunidad estándar Web.  

## Empezar a usar las pruebas de origen  

Para obtener más información sobre las API experimentales disponibles en Microsoft Edge, consulta la [consola de desarrollo de pruebas de origen de Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials].  Asegúrese de revisar los requisitos de versión mínima de Microsoft Edge y la fecha de finalización de la prueba para evaluar la idoneidad del uso de las API experimentales en su sitio Web.  

> [!NOTE]
> Un experimento puede finalizar antes de lo planeado si se produce alguna de las situaciones siguientes.  
> *   Un incidente de seguridad importante.  
> *   Si se recopilan los comentarios suficientes que indican que es necesario un rediseño importante para satisfacer las necesidades de los programadores de Internet.  
> En cualquiera de los casos, se envía una notificación por correo electrónico a todos los desarrolladores actualmente inscritos en el experimento.  

### Registrarse para una prueba de una API experimental  

Siga estos pasos para registrar una prueba de una API experimental.  

1.  Visite la página de la [consola de desarrollo de versiones de prueba de Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .  
1.  Elija el botón registrar en cualquiera de los experimentos disponibles.  
1.  Inicia sesión en la consola del desarrollador con tu nombre de usuario y contraseña de GitHub.  
1.  Elija **autorizar MicrosoftEdge**.  
1.  Complete el formulario.  
    
    > [!NOTE]
    > Para inscribir uno o todos los subdominios, elija establecer la `Do you need to match all subdomains for the provided origin?` configuración en `Yes` .  Por ejemplo, `https://dev.contoso.com` es un solo dominio y `https://*.contoso.com` usa un carácter comodín para representar todos los subdominios.  
    
    > [!IMPORTANT]
    > No se permiten los siguientes formatos de origen.  
    > *   Especificar una subcarpeta en el origen.  Por ejemplo: `https://contoso.com/path/subfolder`  
    > 
    > *   Usar un origen con parámetros de cadena de consulta.  Por ejemplo: `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  Elija **Aceptar y registrar**.  

### Aplicar tu token  

Se genera un token de forma instantánea y se muestra en la página de la [consola de desarrollador de Microsoft Edge de origen][DeveloperMicrsoftEdgeOriginTrials] .  Para empezar a usar la versión de prueba en su sitio web, use uno de los métodos siguientes para aplicar el token a la página.  

*   Agregue el `origin-trial` valor de atributo y el token a la `meta` etiqueta en todas las páginas que usen la API experimental.  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   Agregar `Origin-Trial` al encabezado de respuesta HTTP del servidor.  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> Tu token es válido durante 6 semanas.  Antes de que finalice el período de prueba, te enviaremos recordatorio por correo electrónico que te pidan tus comentarios y te pidan que consideres la posibilidad de renovar la prueba antes de que venza el token.  

### No participar en un experimento  

Para no participar en un experimento, usa uno de los siguientes métodos para quitar tu token.  

*   Quite la `meta` etiqueta de todas las páginas que usaron la API experimental.  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   Quitar `Origin-Trial` del encabezado de respuesta HTTP del servidor.  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### Detectar características experimentales y proporcionar un respaldo  

Cuando uses las API experimentales, asegúrate de proporcionar una experiencia laboral a todos los visitantes de tu sitio Web.  Los visitantes pueden usar exploradores que no sean compatibles con las API experimentales que agregó al código.  Además, si tu token vence antes de renovarlo, la API experimental ya no está disponible, lo que puede provocar errores.  Para evitar esta situación, asegúrese de que detecta las características disponibles en el explorador.  Para obtener más información, consulte implementación de la [detección de características][MDNImplementingFeatureDetection].

### Guía básica para orígenes permitidos  

El portal de versiones de prueba de Microsoft Edge solo admite orígenes habilitados para SSL, lo que significa que los sitios web deben tener HTTPS correctamente implementados para registrarse en un experimento.  En el futuro, se planean los siguientes orígenes seguros.  

*   Regístrate `http://localhost` como el origen de tus experimentos.  Para usar `http://localhost` hoy, vaya a `edge://flags` y establezca el experimento en **habilitado**.  
*   Use extensiones con `extensions://` orígenes con prefijo para inscribirse en experimentos.  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Prueba de Microsoft Edge origen consola de desarrollador | Microsoft docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementación de la detección de características | MDN"  

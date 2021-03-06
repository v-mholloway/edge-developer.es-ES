---
ms.assetid: ''
description: Experimente de forma segura durante un período de tiempo fijo y proporcione comentarios sobre las nuevas características de la plataforma.
title: Pruebas de origen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desarrollo web, html, css, pruebas de origen, desarrollador
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397548"
---
# <a name="use-origin-trials-in-microsoft-edge"></a>Usar pruebas de origen en Microsoft Edge  

Los desarrolladores pueden usar las pruebas de Origin para probar api experimentales en sitios en directo durante un período de tiempo limitado.  Al usar las pruebas de origen, los usuarios de Microsoft Edge que visitan el sitio pueden ejecutar código que usa API experimentales.  Para obtener acceso a las API experimentales en cada equipo de usuario, no es necesario ir a y activar `edge://flags` las marcas de características.  Para obtener más información, vaya a [API experimentales][DeveloperMicrsoftEdgeOriginTrials].  Además, puede proporcionar comentarios sobre el diseño de la API, los casos de uso o la experiencia con las API para ingenieros de exploradores y la comunidad estándar web.  

## <a name="get-started-using-origin-trials"></a>Introducción al uso de pruebas de Origin  

Para obtener más información acerca de las API experimentales disponibles en Microsoft Edge, vaya a [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].  Asegúrese de revisar los requisitos mínimos de versión de Microsoft Edge y la fecha de finalización de la prueba para evaluar la idoneidad de usar las API experimentales en su sitio web.  

> [!NOTE]
> Un experimento puede finalizar antes de lo planeado si se produce alguna de las siguientes situaciones.  
> *   Un incidente de seguridad importante.  
> *   Si se recopilan suficientes comentarios que indican que se necesita un rediseño importante para satisfacer las necesidades de los desarrolladores web.  
> En cualquier caso, se envía un correo electrónico de notificación a todos los desarrolladores inscritos actualmente en el experimento.  

### <a name="register-for-a-trial-of-an-experimental-api"></a>Registrarse para una prueba de una API experimental  

Siga estos pasos para registrarse para una prueba de una API experimental.  

1.  Visite la [página Microsoft Edge Origin Trials Developer Console.][DeveloperMicrsoftEdgeOriginTrials]  
1.  Elija el botón Registrar en cualquiera de los experimentos disponibles.  
1.  Inicie sesión en la Consola de desarrolladores con su nombre de usuario y contraseña de GitHub.  
1.  Elija **Autorizar MicrosoftEdge**.  
1.  Complete el formulario.  
    
    > [!NOTE]
    > Para inscribir un único o todos los subdominios, elija establecer la `Do you need to match all subdomains for the provided origin?` configuración en `Yes` .  Por ejemplo, `https://dev.contoso.com` es un dominio único y usa un `https://*.contoso.com` comodín para representar todos los subdominios.  
    
    > [!IMPORTANT]
    > No se permiten los siguientes formatos de origen.  
    > *   Especificación de una subcarpeta en el origen.  Por ejemplo: `https://contoso.com/path/subfolder`  
    > 
    > *   Uso de un origen con parámetros de cadena de consulta.  Por ejemplo: `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  Elija **ACEPTAR y REGISTRAR**.  
    
### <a name="apply-your-token"></a>Aplicar el token  

Un token se genera instantáneamente y se muestra en la página De pruebas de [Microsoft Edge Origin Developer Console.][DeveloperMicrsoftEdgeOriginTrials]  Para empezar a usar la prueba en su sitio web, use cualquiera de los siguientes métodos para aplicar el token a la página.  

*   Agregue el `origin-trial` valor de atributo y el token a la etiqueta en cada página que use la API `meta` experimental.  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   Agregue `Origin-Trial` al encabezado de respuesta HTTP del servidor.  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> El token es válido durante 6 semanas.  Antes de que finalice la prueba, se le enviarán correos electrónicos de aviso que le pedirán sus comentarios y le pedirán que considere la posibilidad de renovar la prueba antes de que expire el token.  

### <a name="opt-out-of-an-experiment"></a>No participar en un experimento  

Para no participar en un experimento, use uno de los siguientes métodos para quitar el token.  

*   Quite la `meta` etiqueta de todas las páginas que usaron la API experimental.  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   Quite `Origin-Trial` del encabezado de respuesta HTTP del servidor.  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a>Detectar características experimentales y proporcionar una reserva  

Al usar API experimentales, asegúrese de proporcionar una experiencia de trabajo a todos los visitantes de su sitio web.  Los visitantes pueden usar exploradores que no admiten las API experimentales que agregó al código.  Además, si el token expira antes de renovarlo, la API experimental ya no está disponible, lo que puede provocar errores.  Para evitar esta situación, asegúrese de detectar las características disponibles en el explorador.  Para obtener más información, vaya [a Implementar la detección de características][MDNImplementingFeatureDetection].

### <a name="roadmap-for-allowed-origins"></a>Guía básica para orígenes permitidos  

El portal de pruebas de origen de Microsoft Edge actualmente solo admite orígenes habilitados para SSL, lo que significa que los sitios web deben tener HTTPS correctamente implementado para registrar un experimento.  En el futuro, se planean los siguientes orígenes seguros.  

*   Registrarse `http://localhost` como origen de los experimentos.  Para usarlo `http://localhost` hoy, vaya a `edge://flags` y establezca el experimento en **Habilitado**.  
*   Use extensiones con `extensions://` orígenes con prefijo para inscribirse en experimentos.  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials Developer Console | Microsoft Docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementación de la detección de características | MDN"  

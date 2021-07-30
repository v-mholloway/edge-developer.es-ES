---
description: Microsoft Edge (Chromium) y Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/27/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs, visual studio, depurador
ms.openlocfilehash: b7f2837d1d659ad9bf396d7de61efbcdeb6fe982
ms.sourcegitcommit: 613c4c5325177560f9e814ead1a802531f92b8ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/29/2021
ms.locfileid: "11709235"
---
# <a name="visual-studio"></a>Visual Studio  

Microsoft [Visual Studio][MicrosoftVisualstudioVs] es un entorno de desarrollo integrado \(IDE\).   Úselo para editar, depurar, compilar y publicar sus aplicaciones web.  Es un programa enriquecido con características que se puede usar para muchos aspectos del desarrollo web.  Más allá del editor y depurador estándar que proporcionan la mayoría de los identificadores, Visual Studio incluye las siguientes características para facilitar el proceso de desarrollo.  

*   Compiladores  
*   Herramientas de finalización de código  
*   Diseñadores gráficos  
*   Muchos más  
    
Si aún no está usando Visual Studio, vaya [a Descargar Visual Studio][MicrosoftVisualstudioDownloads] para descargarlo.  

Actualmente, Visual Studio 2019 admite la depuración de JavaScript en Microsoft Edge para su ASP.NET Framework y ASP.NET Core aplicaciones.  Complete los siguientes pasos para usar Visual Studio para depurar Microsoft Edge.  

## <a name="launch-microsoft-edge"></a>Iniciar Microsoft Edge  

Visual Studio crear la aplicación ASP.NET y ASP.NET Core, iniciar un servidor web, iniciar Microsoft Edge y conectar el depurador de Visual Studio con un solo botón.  

El flujo de trabajo simplificado permite depurar JavaScript que se ejecuta en Microsoft Edge directamente desde el IDE.  

### <a name="create-a-new-aspnet-core-web-app"></a>Crear una nueva aplicación ASP.NET Core web  

1.  Abra Visual Studio 2019 y **seleccione Crear un nuevo proyecto**.  

1.  En el cuadro de búsqueda de la siguiente pantalla, escriba **react**.  

1.  Seleccione **ASP.NET Core con React.js** de la lista de plantillas y, a continuación, **Siguiente**.  

:::image type="complex" source="./media/create-new-project.png" alt-text="Crear una nueva ASP.NET Core web con React.js" lightbox="./media/create-new-project.png":::
   Crear una nueva ASP.NET Core web con React.js  
:::image-end:::  

Esta **React.js** especifica cómo integrar React.js con una ASP.NET Core aplicación.  

### <a name="launch-microsoft-edge-from-visual-studio"></a>Inicie Microsoft Edge desde Visual Studio  

Con el proyecto creado, use Visual Studio para depurar JavaScript.  

1.  Abra `ClientApp/src/components/Counter.js` .  

1.  Selecciona el desplegable junto al botón **verde Reproducir** y **IIS Express**.  
    
    :::image type="complex" source="./media/vs-dropdown.png" alt-text="La lista desplegable junto al botón verde Reproducir y IIS Express" lightbox="./media/vs-dropdown.png":::
       La lista desplegable junto al botón **verde Reproducir** y **IIS Express**  
    :::image-end:::  

1.  Seleccione **Depuración de scripts**  >  **habilitada**.  

    :::image type="complex" source="./media/enable-script-debugging.png" alt-text="Activar la depuración de scripts en Visual Studio" lightbox="./media/enable-script-debugging.png":::
       Activar la depuración de scripts en Visual Studio  
    :::image-end:::  

1.  En el mismo desplegable, seleccione **Explorador web** > el canal de vista previa de Microsoft Edge que desea que Visual Studio inicie, como Microsoft Edge Canary, Dev o Beta.  Si aún no usa uno de los canales de vista Microsoft Edge, vaya a Descargar [Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] para descargar uno.  

    :::image type="complex" source="./media/set-web-browser.png" alt-text="Seleccione el canal de vista Microsoft Edge que desea Visual Studio iniciar" lightbox="./media/set-web-browser.png":::
       Seleccione el canal de vista Microsoft Edge que desea Visual Studio iniciar  
    :::image-end:::  

1.  Selecciona el botón **verde Reproducir.**  Visual Studio compila la aplicación, inicia el servidor web, inicia Microsoft Edge y navega al puerto especificado en `https://localhost:44362/` `launchSettings.json` .  

    :::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge inicia desde Visual Studio" lightbox="./media/edge-launch.png":::
       Microsoft Edge inicia desde Visual Studio  
    :::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a>Depurar JavaScript que se ejecuta en Microsoft Edge  

Vuelva a Visual Studio para establecer un punto de interrupción.  

1.  In `Counter.js` , set a breakpoint on Line 13 by selecting the gutter next to the line.  

    :::image type="complex" source="./media/set-breakpoint.png" alt-text="Seleccione el canal situado junto a la línea 13 en Counter.js para establecer un punto de interrupción en Visual Studio" lightbox="./media/set-breakpoint.png":::
       Seleccione el canal situado junto a la línea 13 para establecer un punto de `Counter.js` interrupción en Visual Studio  
    :::image-end:::  

1.  Vuelva a la instancia de Microsoft Edge que Visual Studio iniciado.  

1.  Seleccione **Contador** en el menú de navegación en la parte superior de la página web y, a continuación, **seleccione Incrementar**.  

    :::image type="complex" source="./media/edge-counter.png" alt-text="La página Contador de nuestra aplicación ASP.NET Core web" lightbox="./media/edge-counter.png":::
       La página Contador de nuestra aplicación ASP.NET Core web  
    :::image-end:::  

1.  El depurador de JavaScript de Visual Studio alcanza el punto de interrupción establecido en `Counter.js` .  Visual Studio pausa el tiempo de ejecución del JavaScript que se ejecuta en Microsoft Edge y puede pasar por el script línea por línea.  

    :::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio pausa la ejecución de JavaScript en Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
       Visual Studio pausa la ejecución de JavaScript en Microsoft Edge  
    :::image-end:::  

El ejemplo era solo una pequeña demostración de la funcionalidad disponible en Visual Studio.  Para obtener más información acerca de la funcionalidad de Visual Studio 2019, vaya [a Visual Studio documentación][VisualStudioWindowsIndex].  

## <a name="attach-to-microsoft-edge"></a>Adjuntar a Microsoft Edge  

Anteriormente, se iniciaba Microsoft Edge desde Visual Studio.  Como alternativa, puede adjuntar el depurador de Visual Studio a una instancia de Microsoft Edge que ya se está ejecutando, como se muestra a continuación.  

1.  En primer lugar, asegúrese de que no hay instancias en ejecución de Microsoft Edge.  

1.  Desde la línea de comandos, ejecute el siguiente comando.  

    ```console
    start msedge --remote-debugging-port=9222
    ```  

1.  En Visual Studio, seleccione **Depurar**  >  **adjuntar al proceso** o `Ctrl` + `Alt` + `P` .  

    :::image type="complex" source="./media/attach-to-process.png" alt-text="Seleccione Adjuntar al proceso en Visual Studio" lightbox="./media/attach-to-process.png":::
       Seleccione **Adjuntar al proceso** en Visual Studio  
    :::image-end:::  

1.  En el cuadro de diálogo Adjuntar al **proceso,** establezca Tipo de **conexión** en **Websocket del protocolo de devtools de Chrome (sin autenticación).**  

1.  En el **cuadro de texto Conexión de** destino, escriba y seleccione `http://localhost:9222/` `Enter` .  

1.  Revise la lista de pestañas abiertas que tiene en Microsoft Edge en la sección **Procesos disponibles.**  

    :::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Configurar el cuadro de diálogo Adjuntar al proceso en Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
       Configurar el **cuadro de diálogo Adjuntar** al proceso en Visual Studio  
    :::image-end:::  

1.  Elija la pestaña que desea depurar de la lista y, a continuación, **seleccione Adjuntar**.  

1.  En el **cuadro de diálogo** Seleccionar tipo de código, seleccione **JavaScript (Microsoft Edge - Chromium)** y **seleccione Aceptar**.  

El Visual Studio está conectado a Microsoft Edge.  Puede pausar la ejecución de JavaScript, establecer puntos de interrupción y ver instrucciones directamente en la ventana `console.log()` Depurar salida en Visual Studio.  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a>Getting in touch with the Microsoft Visual Studio team  

Los Microsoft Visual Studio y Microsoft Edge quieren obtener más información sobre cómo trabajar con JavaScript en Visual Studio.  Para enviar sus comentarios, seleccione **el** icono Enviar comentarios en Visual Studio o @VisualStudio [y @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].  

:::image type="complex" source="./media/feedback-icon.png" alt-text="El icono Enviar comentarios en Visual Studio" lightbox="./media/feedback-icon.png":::
   El **icono Enviar comentarios** en Visual Studio  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio documentación | Microsoft Docs"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Descargar Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet to @VisualStudio and @EdgeDevTools | Twitter"  

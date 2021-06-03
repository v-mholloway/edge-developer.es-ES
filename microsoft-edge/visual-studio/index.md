---
description: Microsoft Edge (Chromium) y Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs, visual studio, depurador
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387274"
---
# <a name="visual-studio"></a>Visual Studio  

Microsoft [Visual Studio][MicrosoftVisualstudioVs] es un entorno de desarrollo integrado \(IDE\).   Úselo para editar, depurar, compilar y publicar sus aplicaciones web.  Es un programa completo de características que puede usarse para muchos aspectos del desarrollo web.  Más allá del editor y depurador estándar que proporcionan la mayoría de los identificadores, Visual Studio incluye las siguientes características para facilitar el proceso de desarrollo.  

*   compiladores  
*   herramientas de finalización de código  
*   diseñadores gráficos  
*   muchos más  
    
Si aún no está usando Visual Studio, vaya [a Descargar Visual Studio][MicrosoftVisualstudioDownloads] para descargarlo.  

Actualmente, Visual Studio 2019 admite la depuración de JavaScript en Microsoft Edge para su ASP.NET Framework y ASP.NET Core aplicaciones.  Complete los siguientes pasos para usar Visual Studio para depurar Microsoft Edge.  

## <a name="launch-microsoft-edge"></a>Iniciar Microsoft Edge  

Visual Studio completa el siguiente flujo de trabajo con un solo botón.  

1.  Crea la aplicación ASP.NET y ASP.NET Core aplicación.  
1.  Inicia el servidor web.  
1.  Inicia Microsoft Edge.  
1.  Conecta el depurador Visual Studio.  
    
El flujo de trabajo simplificado permite depurar JavaScript que se ejecutan en Microsoft Edge directamente desde el IDE.  

### <a name="create-a-new-aspnet-core-web-app"></a>Crear una nueva aplicación ASP.NET Core web  

Abra Visual Studio 2019 y elija **Crear un nuevo proyecto**.  En la siguiente pantalla, elija **ASP.NET Core aplicación web**  >  **Siguiente**.  

:::image type="complex" source="./media/create-new-project.png" alt-text="Crear una nueva ASP.NET Core web" lightbox="./media/create-new-project.png":::
   Crear una nueva ASP.NET Core web  
:::image-end:::  

Proporcione un **Project nombre para** el nuevo proyecto y elija **Crear**.  Para los fines del ejemplo, elijaReact.js** como ** plantilla y elija **Crear**.  La **React.js** especifica cómo integrar React.js con una ASP.NET Core aplicación.  

### <a name="launch-microsoft-edge-from-visual-studio"></a>Inicie Microsoft Edge desde Visual Studio  

Después de crear el proyecto, abra `ClientApp/src/components/Counter.js` .  Ahora, para usar Visual Studio para depurar JavaScript, elija el desplegable junto al botón **verde Reproducir** y **IIS Express**.  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="La lista desplegable junto al botón verde Reproducir y IIS Express" lightbox="./media/vs-dropdown.png":::
   La lista desplegable junto al botón **verde Reproducir** y **IIS Express**  
:::image-end:::  

Elija **Depuración de scripts**  >  **habilitada**.  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Activar la depuración de scripts en Visual Studio" lightbox="./media/enable-script-debugging.png":::
   Activar la depuración de scripts en Visual Studio  
:::image-end:::  

En el mismo desplegable, elija **Explorador web** > el canal de vista previa de Microsoft Edge que desea que Visual Studio inicie, como Microsoft Edge Canary, Dev o Beta.  Si aún no usa uno de los canales de vista Microsoft Edge, vaya a Descargar [Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] para descargar uno.  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Elija el canal de vista previa Microsoft Edge que desea que Visual Studio inicie" lightbox="./media/set-web-browser.png":::
   Elija el canal de vista previa Microsoft Edge que desea que Visual Studio inicie  
:::image-end:::  

> [!NOTE]
> Si elige Microsoft Edge \(EdgeHTML\), Visual Studio la inicia en lugar de Microsoft Edge \(Chromium\).  [Instale uno][MicrosoftedgeinsiderDownload] de los canales de vista previa de Microsoft Edge o asegúrese de que la versión de Microsoft Edge instalada en el equipo sea Microsoft Edge \(Chromium\) y no Microsoft Edge \(EdgeHTML\).  

Ahora que Visual Studio está configurado correctamente, elija el botón **verde Reproducir.**  Visual Studio compila la aplicación, inicia el servidor web, inicia Microsoft Edge y navega al puerto especificado en `https://localhost:44362/` `launchSettings.json` .  

:::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge inicia desde Visual Studio" lightbox="./media/edge-launch.png":::
   Microsoft Edge inicia desde Visual Studio  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a>Depurar JavaScript que se ejecuta en Microsoft Edge  

Vuelva a Visual Studio.  In `Counter.js` , to set a breakpoint on Line 13, choose the gutter next to the line.  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Elija el canal situado junto a la línea 13 en Counter.js para establecer un punto de interrupción en Visual Studio" lightbox="./media/set-breakpoint.png":::
   Elija el canal situado junto a la línea 13 para establecer un punto de `Counter.js` interrupción en Visual Studio  
:::image-end:::  

Ahora vuelva a la instancia de Microsoft Edge que Visual Studio iniciado.  Elija en **Contador** en navmenu a la izquierda de la página web.  Ahora elija **Increment**.  

:::image type="complex" source="./media/edge-counter.png" alt-text="La página Contador de nuestra aplicación ASP.NET Core web" lightbox="./media/edge-counter.png":::
   La página Contador de nuestra aplicación ASP.NET Core web  
:::image-end:::  

El depurador de JavaScript de Visual Studio alcanza el punto de interrupción establecido en `Counter.js` .  Visual Studio pausa el tiempo de ejecución del JavaScript que se ejecuta en Microsoft Edge y puede pasar por el script línea por línea.  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio pausa la ejecución de JavaScript en Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
   Visual Studio pausa la ejecución de JavaScript en Microsoft Edge  
:::image-end:::  

El ejemplo era solo una pequeña demostración de la funcionalidad disponible en Visual Studio.  Para obtener más información acerca de la funcionalidad de Visual Studio 2019, vaya [a Visual Studio documentación][VisualStudioWindowsIndex].  

## <a name="attach-to-microsoft-edge"></a>Adjuntar a Microsoft Edge  

Anteriormente, tenías que iniciar Microsoft Edge desde Visual Studio.  Ahora, puede adjuntar el depurador de Visual Studio a una instancia de Microsoft Edge.  

En primer lugar, asegúrese de que no hay instancias en ejecución de Microsoft Edge.  Ahora, desde la línea de comandos, ejecute el siguiente comando.  

```console
start msedge –remote-debugging-port=9222
```  

Desde Visual Studio, abra el menú **Depurar** y elija **Adjuntar al proceso** o seleccione `Ctrl` + `Alt` + `P` .  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Elija Adjuntar al proceso en Visual Studio" lightbox="./media/attach-to-process.png":::
   Elija **Adjuntar al proceso** en Visual Studio  
:::image-end:::  

En el **cuadro de diálogo** Adjuntar a proceso, establezca Tipo de **conexión** en **Websocket del protocolo de devtools de Chrome (sin autenticación).**  En el **cuadro de texto Conexión de** destino, escriba y seleccione `http://localhost:9222/` `Enter` .  Revise la lista de pestañas abiertas que tiene en Microsoft Edge en el cuadro de diálogo Adjuntar **al** proceso.  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Configurar el cuadro de diálogo Adjuntar al proceso en Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   Configurar el **cuadro de diálogo Adjuntar** al proceso en Visual Studio  
:::image-end:::  

Elija **Seleccionar...** > la casilla situada junto a **JavaScript (Microsoft Edge – Chromium).**  Para agregar pestañas, vaya a nuevas pestañas, cierre pestañas **** y muestre los cambios reflejados en el cuadro de diálogo Adjuntar al proceso, elija el **botón** Actualizar.  Elija la pestaña que desea depurar y elija **Adjuntar**.  

El Visual Studio está conectado a Microsoft Edge.  Puede pausar la ejecución de JavaScript, establecer puntos de interrupción y revisar instrucciones directamente en la ventana `console.log()` Depurar salida en Visual Studio.  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a>Getting in touch with the Microsoft Visual Studio team  

Los Microsoft Visual Studio y Microsoft Edge quieren obtener más información sobre cómo trabajar con JavaScript en Visual Studio.  Para enviar sus comentarios, elija el icono **Enviar** comentarios en Visual Studio o @VisualStudio [y @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].  

:::image type="complex" source="./media/feedback-icon.png" alt-text="El icono Enviar comentarios en Visual Studio" lightbox="./media/feedback-icon.png":::
   El **icono Enviar comentarios** en Visual Studio  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio documentación | Microsoft Docs"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Descargar Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet to @VisualStudio and @EdgeDevTools | Twitter"  

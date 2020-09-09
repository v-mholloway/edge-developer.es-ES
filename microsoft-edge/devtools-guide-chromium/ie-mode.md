---
description: IE mode and the Microsoft Edge (cromo) DevTools
title: Modo Internet Explorer y DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, ie11, Internet Explorer 11, modo IE
ms.openlocfilehash: b059cae3ff48a45fe92cbf69e37ad692e329b200
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "11003979"
---
# Modo Internet Explorer y DevTools  

En este artículo se describe cómo el modo de Internet Explorer \ (modo IE \) se integra con el DevTools de Microsoft Edge \ (cromo \).  

## Descripción del modo IE  

El modo IE permite a las empresas especificar una lista de sitios web que solo funcionan en Internet Explorer 11.  Al navegar a estos sitios web en Microsoft Edge \ (cromo \), se ejecuta una instancia de Internet Explorer 11 y se representa el sitio en una pestaña.  La funcionalidad permite a las empresas administrar la compatibilidad con tecnologías que actualmente no son compatibles con ningún explorador web moderno.  La compatibilidad con las siguientes tecnologías está incluida en el modo IE.  

*   Modos de documento de IE  
*   Controles ActiveX  
*   otros componentes heredados  

En el modo IE, el proceso de representación se basa en Internet Explorer 11.  El administrador de procesos de Microsoft Edge \ (cromo \) controla la duración del proceso de representación.  Está limitado a la duración de la pestaña de un sitio \ (o aplicación \).  Cuando se representa una tabulación en modo IE, aparece un distintivo en la barra de direcciones de la pestaña específica.  

:::image type="complex" source="./media/ie-mode-badge.msft.png" alt-text="Distintivo de modo IE en la barra de direcciones" lightbox="./media/ie-mode-badge.msft.png":::
   Distintivo de modo IE en la barra de direcciones  
:::image-end:::  

El modo IE está disponible actualmente en Windows 10 versión 1903 \ (May 2019 Update \), pero pronto estará disponible para todas las plataformas de Windows compatibles.  

## Iniciar DevTools en una pestaña en modo IE  

Si está intentando ver el modo de documento de un sitio web en modo IE, elija el distintivo en la barra de direcciones.  

:::image type="complex" source="./media/ie-mode-badge-doc-mode.msft.png" alt-text="Ver el modo de documento con distintivo de modo IE" lightbox="./media/ie-mode-badge-doc-mode.msft.png":::
   Ver el modo de documento con distintivo de modo IE  
:::image-end:::  

Si una pestaña está usando el modo IE, la DevTools no funciona y se producen las siguientes condiciones.

*   Si seleccionas `F12` o seleccionas `Ctrl` + `Shift` + `I` , se inicia una instancia en blanco de la DevTools de Microsoft Edge \ (cromo \) y se muestra el siguiente mensaje.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Si abre un menú contextual \ (haga clic con el botón derecho \) y elige **Ver origen**, se inicia el Bloc de notas.  
*   Si abre un menú contextual \ (haga clic con el botón derecho \), el **elemento inspeccionar** no está visible.  

El motivo por el que una serie de herramientas de DevTools \ (como las herramientas de **rendimiento** y **red** \) no funciona es el motor de representación cambia de cromo a Internet Explorer 11 en modo IE.  Para proporcionar comentarios, navegue para [ponerse en contacto con el equipo de Microsoft Edge DevTools](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

:::image type="complex" source="./media/ie-mode-devtools.msft.png" alt-text="DevTools iniciado en modo IE" lightbox="./media/ie-mode-devtools.msft.png":::
   DevTools iniciado en modo IE  
:::image-end:::  

Para probar su sitio web basado en Internet Explorer 11 \ (o aplicación \) en el modo Internet Explorer 11 e IE, realice los siguientes pasos.  

1.  Abra Internet Explorer 11.  
    *   En Windows 10, busque el acceso directo para Internet Explorer 11.
        1.  **Menú Inicio**  >  **Accesorios**  >  de Windows **Internet Explorer 11**.  
    *   En Windows 7, busque Internet Explorer 11.
        1.  **Menú Inicio**  >  **Internet Explorer 11**.  
1.  En Internet Explorer 11, abra la misma página web.  
1.  Inicie Internet Explorer DevTools.  
    *   Seleccione `F12` .  
    *   Mantenga el puntero sobre cualquier lugar, abra un menú contextual \ (haga clic con el botón derecho \) y elija **Inspeccionar elemento**.  Para obtener más información sobre cómo usar estas herramientas, vaya a [usar las herramientas de desarrollo F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].  

## Depuración remota y modo IE  

Inicia Microsoft Edge \ (cromo \) con la depuración remota activada desde la interfaz de la línea de comandos.  Visual Studio, el código Visual Studio y otras herramientas de desarrollo suelen ejecutar un comando para iniciar Microsoft Edge.  El siguiente comando inicia Microsoft Edge con el puerto de depuración remota establecido en `9222` .  

```shell
start msedge --remote-debugging-port=9222
```  

Después de iniciar Microsoft Edge \ (cromo \) con un argumento de línea de comandos, el modo IE no está disponible.  Aún puede navegar a sitios web \ (o aplicaciones \) que, de lo contrario, se mostrarán en modo IE. El contenido del sitio web \ (o aplicación \) se representa con cromo, no con Internet Explorer 11.  Espere que las partes de las páginas que dependen de IE11, como los controles ActiveX, no se representen correctamente.  La tarjeta de identificación de modo de IE no aparece en la barra de direcciones.  

El modo IE no está disponible hasta que se cierra completamente y se reinicie Microsoft Edge \ (cromo \).  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Usar las herramientas de desarrollo F12 | Microsoft docs"  
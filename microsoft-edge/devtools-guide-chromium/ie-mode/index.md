---
description: Modo IE y el Microsoft Edge (Chromium) DevTools
title: Modo internet Explorer y DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, ie11, internet explorer 11, es el modo ie
ms.openlocfilehash: c744e13a8d0de3b425247faa1513c2f08edbf325fb9a084c4c5dc54c7059059f
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11799625"
---
# <a name="internet-explorer-mode-and-the-devtools"></a>Modo internet Explorer y DevTools  

En este artículo se describe cómo se integra el modo de Internet Explorer \(modo IE\) con el Microsoft Edge \(Chromium\) DevTools.  

## <a name="understanding-ie-mode"></a>Descripción del modo IE  

El modo IE permite a las empresas especificar una lista de sitios web que solo funcionan en Internet Explorer 11.  Al navegar a estos sitios web en Microsoft Edge \(Chromium\), una instancia de Internet Explorer 11 se ejecuta y representa el sitio en una pestaña.  La funcionalidad permite a las empresas administrar la compatibilidad con tecnologías que actualmente no son compatibles con ningún explorador web moderno.  La compatibilidad con las siguientes tecnologías se incluye en el modo IE.  

*   Modos de documento de IE  
*   Controles ActiveX  
*   otros componentes heredados  

En el modo IE, el proceso de representación se basa en Internet Explorer 11.  El Microsoft Edge de procesos \(Chromium\) controla la duración del proceso de representación.  Está restringido a la duración de la pestaña de un sitio específico \(o app\).  Cuando una pestaña se representa en modo IE, aparece un distintivo en la barra de direcciones de la pestaña específica.  

:::image type="complex" source="../media/ie-mode-badge.msft.png" alt-text="Distintivo de modo IE en la barra de direcciones" lightbox="../media/ie-mode-badge.msft.png":::
   Distintivo de modo IE en la barra de direcciones  
:::image-end:::  

Actualmente, el modo IE está disponible en Windows 10 Versión 1903 \(Actualización de mayo de 2019\), pero pronto llegará a todas las plataformas Windows compatibles.  

## <a name="launching-the-devtools-on-a-tab-in-ie-mode"></a>Iniciar DevTools en una pestaña en modo IE  

Si intenta ver el modo de documento de un sitio web en modo IE, elija el distintivo en la barra de direcciones.  

:::image type="complex" source="../media/ie-mode-badge-doc-mode.msft.png" alt-text="Ver el modo de documento con el distintivo de modo IE" lightbox="../media/ie-mode-badge-doc-mode.msft.png":::
   Ver el modo de documento con el distintivo de modo IE  
:::image-end:::  

Si una pestaña usa el modo IE, las DevTools no funcionan y se producen las siguientes condiciones.

*   Si selecciona o selecciona , se inicia una instancia en blanco de la Microsoft Edge `F12` `Ctrl` + `Shift` + `I` \(Chromium\) DevTools muestra el siguiente mensaje.  
    
    ```text
    Developer Tools are not available in Internet Explorer mode.  To debug the page, open it in Internet Explorer 11.
    ```  
    
*   Si abre un menú contextual \(clic con el botón derecho\) y elige **Ver**origen , Bloc de notas se inicia.  
*   Si abre un menú contextual \(clic con el botón secundario\), **el elemento Inspect** no está visible.  

El motivo por el que varias de las herramientas de DevTools \(like the **Network** and **Performance** tools\) no funcionan es que el motor de representación cambia de Chromium a Internet Explorer 11 en modo IE.  Para proporcionar comentarios, vaya a [Getting in touch with the Microsoft Edge DevTools team](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

:::image type="complex" source="../media/ie-mode-devtools.msft.png" alt-text="DevTools se inicia en modo IE" lightbox="../media/ie-mode-devtools.msft.png":::
   DevTools se inicia en modo IE  
:::image-end:::  

Para probar el sitio web basado en Internet Explorer 11 \(o app\) en modo Internet Explorer 11 e IE, siga estos pasos.  

1.  Abra Internet Explorer 11.  
    *   En Windows 10, busque el acceso directo para Internet Explorer 11.
        1.  **Menú Inicio**  >  **Windows accesorios**  >  **Internet Explorer 11**.  
    *   En Windows 7, busque Internet Explorer 11.
        1.  **Menú Inicio**  >  **Internet Explorer 11**.  
1.  En Internet Explorer 11, abra la misma página web.  
1.  Inicie Internet Explorer DevTools.  
    *   Seleccione `F12`.  
    *   Mantenga el mouse en cualquier lugar, abra un menú contextual \(clic con el botón derecho\) y elija **Inspeccionar elemento**.  Para obtener más información acerca de cómo usar esas herramientas, vaya a Uso de las herramientas para [desarrolladores F12][PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326].  

Si Internet Explorer 11 no está disponible, como en Windows 11, puede usar IEChooser para iniciar las DevTools de Internet Explorer para depurar el contenido de las pestañas del modo IE. Para usar IEChooser, siga estos pasos.

1.  Abra IEChooser.
    1. Abrir el cuadro de diálogo Ejecutar Por ejemplo, presione `Windows logo key`  +  `R` .
    2. Escriba `%systemroot%\system32\f12\IEChooser.exe` y, a continuación, **seleccione Aceptar**.
2.  En IEChooser, seleccione la entrada para la pestaña Modo IE.


## <a name="remote-debugging-and-ie-mode"></a>Depuración remota y modo IE  

Inicie Microsoft Edge \(Chromium\) con la depuración remota activada desde la interfaz de línea de comandos.  Microsoft Visual Studio, Microsoft Visual Studio code y otras herramientas de desarrollo normalmente ejecutan un comando para iniciar Microsoft Edge.  El siguiente comando inicia Microsoft Edge con el puerto de depuración remota establecido en `9222` .  

```shell
start msedge --remote-debugging-port=9222
```  

Después de iniciar Microsoft Edge \(Chromium\) mediante un argumento de línea de comandos, el modo IE no está disponible.  Todavía puede navegar a sitios web \(o aplicaciones\) que de lo contrario se muestran en modo IE.  El contenido del sitio web \(or app\) se representa Chromium, no Internet Explorer 11.  Espere que las partes de las páginas web que dependen de IE11, como los ActiveX, no se representen correctamente.  El distintivo de modo IE no aparece en la barra de direcciones.  

El modo IE permanece no disponible hasta que se cierra completamente y se reinicia Microsoft Edge \(Chromium\).  


## <a name="replacing-internet-explorer-automation"></a>Reemplazo de la automatización de Internet Explorer  

Si tiene una aplicación existente que usa el objeto [InternetExplorer][InternetExplorerObject] para automatizar Internet Explorer 11, pero la aplicación de escritorio de Internet Explorer 11 no está disponible, la aplicación no funcionará.  Internet Explorer 11 se retirará el 15 de junio de 2022.  Para obtener más información, vaya [a El futuro de Internet Explorer en Windows 10 está en Microsoft Edge][BlogsWindowsExperienceFutureOfIEEdge].  Microsoft Edge \(Chromium\) no admite la automatización del modo IE a través del objeto, por lo que las aplicaciones que dependen de este objeto tendrán que actualizarse con una de las `InternetExplorer` alternativas recomendadas a continuación.  Las aplicaciones que usan el control [WebBrowser][WebBrowserControl] seguirán funcionando y no se verán afectadas por la eliminación de Internet Explorer 11.

Si la aplicación de automatización no requiere el modo IE para que el contenido del sitio web \(o app\) funcione correctamente, se recomienda actualizar la aplicación para que use Microsoft Edge \(Chromium\) en lugar de Internet Explorer 11.  Muchas herramientas de automatización disponibles admiten Microsoft Edge \(Chromium\), incluidos WebDriver y Playwright.  Para obtener más información sobre cómo automatizar Microsoft Edge \(Chromium\) con WebDriver, vaya a [WebDriver overview][WebDriverIndex].  Para obtener más información sobre el uso de Playwright, vaya a [Introducción a Playwright][PlaywrightIndex].

Las aplicaciones que requieren el modo IE para que el contenido del sitio web \(o app\) funcione correctamente debe usar el `WebBrowser` control.  El control usa la plataforma Internet Explorer (MSHTML/Trident) para representar contenido web y funcionará incluso si la aplicación de escritorio de `WebBrowser` Internet Explorer 11 no está disponible.


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[PlaywrightIndex]: ../../playwright/index.md "Playwright: Microsoft Edge desarrollo | Microsoft Docs"
[BlogsWindowsExperienceFutureOfIEEdge]: https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge/ "El futuro de Internet Explorer en Windows 10 está en Microsoft Edge | Windows Blog de experiencia"
[PreviousVersionsWindowsInternetExplorerDeveloperSamplesbg182326]: /previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85) "Uso de las herramientas de desarrollo de F12 | Microsoft Docs"  

[WebDriverIndex]: ../../webdriver-chromium/index.md "Usar WebDriver (Chromium) para la automatización de pruebas: Microsoft Edge desarrollo | Microsoft Docs"  

[InternetExplorerObject]: /previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85) "Objeto InternetExplorer (Windows) | Microsoft Docs"
[WebBrowserControl]: /previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85) "Control WebBrowser (Internet Explorer) | Microsoft Docs"

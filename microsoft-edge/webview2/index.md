---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: Vista previa de Microsoft Edge 2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b1ec0c43b57fb107490ddb34b330bb6ec378ac41
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655175"
---
# Microsoft Edge WebView2 (versión preliminar para desarrolladores)

El control Microsoft Edge WebView2 permite hospedar contenido web en la aplicación con [Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/) como motor de representación.

El control WebView2 está actualmente en Developer Preview, durante el cual puedes establecer un prototipo de tus soluciones y compartir tus comentarios con nosotros para dar forma a la API estable futura. Es probable que se produzcan cambios importantes a medida que evolucionemos la API durante la versión preliminar y, cuando esto suceda, tendrá que actualizar el explorador de WebView2 y el explorador de Microsoft Edge (cromo). Los cambios importantes se anotarán en las notas de la [versión](./releasenotes.md) del SDK. Esto se bloqueará a medida que WebView2 se aproxime a la versión beta y estable.

## Plataformas compatibles

Una vista previa para desarrolladores está disponible para Win32 C/C++, Windows Forms y WPF en .NET Framework 4.6.2 o versiones posteriores, .NET Core 3,0 o posterior en Windows 10, Windows 8,1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012/2012R2 y Windows Server 2008 R2. [Aquí](https://docs.microsoft.com/uwp/toolkits/winui3/)está disponible una versión Alpha para WinUI 3,0.

## Tareas iniciales

Para compilar y probar la aplicación con el control WebView2, debe tener instalado tanto [Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download/) como el [SDK de WebView2](https://aka.ms/webviewnuget) . Seleccione una de las siguientes opciones para empezar.

* [Introducción a Win32 C/C++](./gettingstarted/win32.md)
* [Introducción a WPF](./gettingstarted/wpf.md)
* [Introducción a Windows Forms](./gettingstarted/winforms.md)

Envíenos comentarios en nuestro repositorio de [comentarios de WebView2](https://aka.ms/webviewfeedback) .

## Ejemplos de WebView2

El repositorio de [muestras de WebView2](https://github.com/MicrosoftEdge/WebView2Samples) contiene ejemplos que muestran todas las características del SDK de WebView2 y sus patrones de uso de API. A medida que agreguemos más características al SDK de WebView2, actualizaremos periódicamente nuestras aplicaciones de ejemplo.

## Distribución de aplicaciones

El control WebView2 usa el explorador Microsoft Edge (cromo). Al distribuir la aplicación, es importante asegurarse de que el explorador Edge está instalado en todos los equipos de usuario en los que se ejecutará la aplicación. También debe tener en cuenta la versión y el canal instalados, por ejemplo, estable, beta, dev o Canarias. El controlador de WebView2 usará la versión más estable del explorador cuando se instala en un equipo.

### Futuros cambios planeados

Reconocemos que es posible que el explorador Edge no esté disponible en todos los equipos de usuario que su aplicación tenga que ejecutar, o que el control del proceso de instalación del navegador perimetral puede resultar difícil. Para asegurarse de que su aplicación se ejecutará en todas las máquinas, independientemente del estado de instalación del explorador cliente Microsoft Edge, publicaremos el tiempo de ejecución de Microsoft Edge WebView2. Actualizaremos WebView2 para buscar la versión estable del motor en tiempo de ejecución antes de buscar las versiones preliminares del explorador instalado.

También reconocemos que algunos desarrolladores de aplicaciones operan en entornos restringidos y, por tanto, pretenden admitir dos opciones de distribución, hoja perenne y versión fija.

Perenne es el modelo de distribución recomendado para la mayoría de los programadores. En este modo, Microsoft administrará totalmente las actualizaciones para el tiempo de ejecución de WebView2 sin ningún esfuerzo adicional de la aplicación. Con este modelo de autoactualización, puedes tener la seguridad de que tu aplicación está aprovechando las últimas características y actualizaciones de seguridad de contenido web hospedado.

Para entornos limitados, también admitimos un modelo de distribución de versiones fijo. En este modelo, la aplicación seleccionará y empaquetará una versión específica de WebView2. Las actualizaciones de la versión de WebView serán responsabilidad de la aplicación y serán independientes de cualquier mecanismo de actualización de Microsoft administrado. Debe elegir este modelo si es crucial poder tener un control absoluto sobre la versión del explorador y las horas de actualización de su aplicación.

## Microsoft Edge WebView2 Runtime

El tiempo de ejecución de Microsoft Edge WebView2 es un empaquetado de los binarios del explorador optimizados para su uso por parte de WebView2 aplicaciones. Funcionará de forma independiente o en paralelo con la instalación del explorador perimetral del cliente. Una única instalación del tiempo de ejecución admitirá cualquier cantidad de aplicaciones WebView2. La instalación del motor en tiempo de ejecución no aparecerá como una instalación de explorador para el usuario final, es decir, sin accesos directos de escritorio, entradas del menú Inicio o registro de protocolo.

Una aplicación que usa WebView2 debe garantizar la instalación de Microsoft Edge WebView2 se ha producido el tiempo de ejecución. En el momento de la instalación de la aplicación, debe comprobar el estado de instalación actual, que se puede determinar mediante [GetAvailableCoreWebView2BrowserVersionString](./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring). Si el tiempo de ejecución de WebView2 no está disponible, deberías encadenar el instalador de tiempo de ejecución de Microsoft Edge WebView2 al flujo de instalación.

## SDK de Microsoft Edge WebView2

Para usar WebView2 dentro de tu aplicación, tendrás que instalar y hacer referencia al [SDK de WebView2](https://aka.ms/webviewnuget) en tu aplicación. Nuestras versiones de NuGet contendrán tanto una versión como una versión preliminar. La versión de lanzamiento contiene las API públicas que actualmente pretendemos publicar para la disponibilidad general.

La versión preliminar contendrá [API experimentales](./reference/win32/0-9-488-reference-webview2.md#experimental)adicionales. Estas son las API y la funcionalidad que estamos evaluando y deseamos que se [envíen comentarios](https://aka.ms/webviewfeedback) antes de promocionarlos a la versión de lanzamiento.

## Desarrollo de versiones futuras

Para el desarrollo, es posible que quieras dirigirte a beta, dev o Canarias para garantizar que tu aplicación funcione con las próximas versiones o para aprovechar las características futuras. Todos los canales prepublicados son proporcionados por el navegador Microsoft Edge de cliente instalado. Para dirigirte a uno de estos canales, asegúrate de que el explorador Edge instalado en tu equipo de desarrollo sea el canal que deseas. Los programadores pueden usar una clave del registro o una variable de entorno para cambiar el WebView2 de la versión más estable que se encuentra a la menos estable. Vea más detalles en [CreateCoreWebView2EnvironmentWithOptions](./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).

## Depurar WebView2

### DevTools

Puede usar [las herramientas de desarrollador de Microsoft Edge (cromo)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium) para depurar el contenido web que se muestra en WebView, como lo haría en el explorador. Mientras el foco está en la ventana WebView, presione `F12` o presione `Ctrl`  +  `Shift`  +  `I` , o haga clic con el botón derecho en + elegir `Inspect` para abrir las herramientas de desarrollador.

:::image type="complex" source="./media/f12.png" alt-text="F12":::
   F12
:::image-end:::  

<!--![F12](./media/f12.png)  -->  

**Nota Cuando se depura la aplicación en Visual Studio con el depurador nativo adjunto, se `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollador. Use `Ctrl`  +  `Shift`  +  `I` , o haga clic con el botón derecho + `Inspect` para evitar posibles conflictos de teclas de cambio.**

### Visual Studio

Puede usar el depurador de scripts en Visual Studio 2019 (versión mínima 16,4 Preview 2) para depurar el script en WebView2 directamente desde el IDE. Asegúrese de que el componente **diagnóstico de JavaScript** en el **desarrollo de escritorio con** la carga de trabajo de C++ está instalado.

:::image type="complex" source="./media/vs-js-diagnostics.jpg" alt-text="Diagnósticos de JavaScript de Visual Studio":::
   Diagnósticos de JavaScript de Visual Studio
:::image-end:::  

<!--![vs-js-diagnostics](./media/vs-js-diagnostics.jpg)  -->  

Haga clic con el botón secundario en el proyecto y seleccione **propiedades**. En **propiedades de configuración**  >  **depurando**  >  el**tipo de depurador**, elija la opción **JavaScript (WebView2)** para habilitar la depuración de script WebView2. Más información para seguir pronto.

:::image type="complex" source="./media/vs-script-debugger.jpg" alt-text="Depurador de scripts de Visual Studio":::
   Depurador de scripts de Visual Studio
:::image-end:::  

<!--![vs-script-debugger](./media/vs-script-debugger.jpg)  -->  

### Visual Studio Code

También puedes usar código de Visual Studio para depurar el script en el WebView2 directamente desde el IDE. Para obtener más información, haz clic [aquí](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).

## Ponerse en contacto con el equipo de WebView2  

Ayúdanos a crear una experiencia WebView2 más rica compartiendo tus comentarios. Visita nuestro [repositorio de comentarios](https://aka.ms/webviewfeedback) para enviar solicitudes de características o informes de errores.

También es un buen lugar para buscar problemas conocidos.
Durante la vista previa para desarrolladores, también se recopilan datos de telemetría para ayudarnos a crear una vista previa mejorada. Los usuarios pueden desactivar la recopilación de datos de WebView desplazándose a edge://settings/privacy en el explorador y desactivando la recopilación de datos del explorador.

---
description: Guía de introducción para usar WebView2 para aplicaciones de WinUI 2.
title: Introducción a WebView2 en aplicaciones de WinUI 2 (versión preliminar pública)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/30/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicaciones winui, winui, edge, CoreWebView2, control de explorador, html perimetral, introducción, Introducción, .NET
ms.openlocfilehash: b62defccc8e7369721baaabb4f114d1ad9c6040b
ms.sourcegitcommit: 66a8e3db5b63b0532ca2f4003fa37bde6bd225b0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934216"
---
# <a name="get-started-with-webview2-in-winui-2-apps-public-preview"></a>Introducción a WebView2 en aplicaciones de WinUI 2 (versión preliminar pública)

En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales de WebView2. Para obtener más información acerca de las API de WebView2 individuales, vaya a Microsoft Edge referencia de la API de[WebView2](../webview2-api-reference.md) y, a continuación, seleccione los vínculos de referencia de WinRT.

> [!NOTE]
> El paquete WinUI 2 depende de un paquete webView2 preliminar.  Para obtener compatibilidad completa con la API, usa un canal de explorador de vista previa como tiempo de ejecución (es decir, el canal Beta, Dev o Canary de Microsoft Edge).


## <a name="step-1-install-visual-studio"></a>Paso 1\: Instalar Visual Studio

1.  Instale Visual Studio versión 16.9 o posterior.  Puede aceptar los valores predeterminados.

1.  De forma predeterminada, Visual Studio no muestra números de línea en el editor de código.  Para activar los números de línea, seleccione **Herramientas**  >  **Opciones**  >  **Editor de texto Todos**los números de línea  >  ****  >  **idiomas**.  A continuación, **seleccione Aceptar**.


## <a name="step-2-install-workloads"></a>Paso 2\: Instalar cargas de trabajo

1.  En Visual Studio, seleccione **Herramientas**  >  **Obtener herramientas y características**.  Se **abre Instalador de Visual Studio** ventana.

1.  En la **pestaña Cargas de trabajo,** seleccione **Desarrollo de escritorio de .NET**.

1.  Seleccione **Desarrollo de escritorio con C++**.

1.  Seleccione **Desarrollo Windows plataforma universal.**  

1. A la derecha, expanda **Detalles**de instalación Desarrollo Windows plataforma universal y, a continuación, seleccione  >  **** **C++ (v142)** Herramientas Windows plataforma universal .

    :::image type="complex" source="media/winui2-getting-started-install-workloads.png" alt-text="Selección de cargas de trabajo para instalar para Visual Studio" lightbox="media/winui2-getting-started-install-workloads.png":::
       Selección de cargas de trabajo para instalar para Visual Studio :::image-end:::

1.  Seleccione el **botón** Modificar.  Visual Studio instala las características seleccionadas.


## <a name="step-3-create-a-uwp-app"></a>Paso 3\: Crear una aplicación para UWP

1.  En Visual Studio, seleccione **Archivo**  >  **nuevo**  >  **Project**.  O use la pantalla de inicio de Visual Studio y, a continuación, **seleccione Crear un nuevo proyecto**.  Aparece **el cuadro de diálogo** Crear un nuevo proyecto.  

1.  En la **lista desplegable Todos los idiomas,** seleccione **C#**.

1.  En la **lista desplegable Todas las** plataformas, seleccione **Windows**.

1.  En la **lista desplegable Todos los tipos de** proyecto, selecciona **UWP**.  Como resultado de las selecciones de filtro, se enumeran varios tipos de plantillas de aplicación.

1.  En la lista de plantillas de aplicación, seleccione Aplicación en blanco **(aplicación universal Windows).**

    :::image type="complex" source="media/winui2-getting-started-create-project.png" alt-text="Cuadro de diálogo "Crear un nuevo proyecto"" lightbox="media/winui2-getting-started-create-project.png":::
       Cuadro **de diálogo Crear un nuevo** proyecto
    :::image-end:::

1.  Seleccione el **botón** Siguiente.  Aparece **la página Configurar el** nuevo proyecto del cuadro de diálogo, para una aplicación en blanco **(aplicación universal Windows).**

1.  En el **Project de texto nombre,** escriba un nombre de proyecto, como `UWPSampleProject` .

    :::image type="complex" source="media/winui2-getting-started-config-new-project.png" alt-text="El cuadro de diálogo "Configurar el nuevo proyecto" para una aplicación en blanco (aplicación universal Windows)"" lightbox="media/winui2-getting-started-config-new-project.png":::
       Cuadro **de diálogo Configurar el nuevo proyecto** para una aplicación en blanco **(Windows)**
    :::image-end:::

1.  Seleccione el **botón** Crear.  Aparece **el cuadro de diálogo Nuevo** Windows de Project universal.

1.  Seleccione el **botón** Aceptar.  La **Configuración** puede abrirse, si aún no ha realizado los siguientes pasos.

1.  En la **sección Modo de** desarrollador, seleccione **Activar**.  Se **abre el cuadro de diálogo** Usar características de desarrollador para confirmar la activación del modo de desarrollador.

1.  Seleccione el **botón Sí** y, a continuación, **cierre Configuración** ventana.

Se muestra la solución y el proyecto.

:::image type="complex" source="media/new-project-created.msft.png" alt-text="El proyecto resultante" lightbox="media/new-project-created.msft.png":::
    El proyecto resultante
:::image-end:::


## <a name="step-4-install-the-winui-2-nuget-package"></a>Paso 4\: Instalar el paquete de NuGet WinUI 2

1.  Haga clic con el botón secundario en el proyecto en el Explorador de soluciones y, a continuación, seleccione **Administrar NuGet paquetes**.

1.  Seleccione la **pestaña** Examinar. 

1.  Active la **casilla Incluir versión preliminar.**

1.  En el **cuadro Buscar,** escriba `Microsoft.UI.Xaml` y, a continuación, **seleccione Microsoft.UI.Xaml**.  Asegúrese de que **version** es la versión preliminar más reciente y, a continuación, seleccione **Instalar**.

    :::image type="complex" source="media/winui2-nuget-package.msft.png" alt-text="El administrador NuGet paquetes" lightbox="media/winui2-nuget-package.msft.png":::
       El administrador NuGet paquetes
    :::image-end:::

    Aparece **el cuadro de diálogo** Vista previa de cambios.  Seleccione el **botón** Aceptar.  Tenga en cuenta que la dependencia del SDK de WebView2 se instalará así como WinUI 2.

<!-- "Microsoft.UI.Xaml" here is equiv to WinUI 2; same team -->

1.  Aparece **el cuadro de diálogo** Aceptación de licencia.  Seleccione el **botón Acepto.**  `readme.txt`Aparece.

<!-- note: install halted after only WinUI 2 component, it didn't seem to install WebView2 even though that was the 2nd item listed.  assume that's ok now on my machine. -->


## <a name="step-5-instantiate-the-webview2-control-in-xaml-code"></a>Paso 5\: Crear una instancia del control WebView2 en código XAML

### <a name="add-the-project-reference-for-the-webview2-control"></a>Agregar la referencia de proyecto para el control WebView2 

1.  En el `MainPage.xaml` archivo, en el `<Page>` elemento, agregue el siguiente atributo debajo de los otros `xmlns:` atributos.

    ```xml
    xmlns:control="using:Microsoft.UI.Xaml.Controls" 
    ```

### <a name="add-the-webview2-control-to-the-grid"></a>Agregar el control WebView2 a la cuadrícula

1.  En el `MainPage.xaml` archivo, en `<Grid>` el elemento, agregue el siguiente elemento:

    ```xml
    <control:WebView2 x:Name="wv2" Source="https://bing.com"/>
    ```

1.  Guarda el archivo.  Encima del archivo del editor de código, se muestra una vista previa del contenido `MainPage.xaml` de WebView2.

    :::image type="complex" source="media/winui2-getting-started-preview-webview2-content.png" alt-text="Vista previa del contenido de WebView2" lightbox="media/winui2-getting-started-preview-webview2-content.png":::
       Vista previa del contenido de WebView2
    :::image-end:::

### <a name="build-and-test-the-webview2-project"></a>Crear y probar el proyecto WebView2

1.  En el **menú Depurar,** seleccione **Iniciar depuración**.  Se abre la ventana de la aplicación, que muestra brevemente la cuadrícula WebView2 WebUI.

    :::image type="complex" source="media/winui2-getting-started-webview2-grid.png" alt-text="La cuadrícula aparece momentáneamente durante la depuración" lightbox="media/winui2-getting-started-webview2-grid.png":::
       La cuadrícula aparece momentáneamente durante la depuración
    :::image-end:::

1.  Después de un momento, la ventana de la aplicación muestra el sitio Bing.com, en el control WebView2 para WebUI 2.

    :::image type="complex" source="media/winui2-getting-started-webview2-with-content.png" alt-text="Una ventana de aplicación que muestra el Bing.com en el control WebView2" lightbox="media/winui2-getting-started-webview2-with-content.png":::
       Una ventana de aplicación que muestra el Bing.com en el control WebView2
    :::image-end:::

1.  En Visual Studio, en el **menú Depurar,** seleccione **Detener depuración**.  Se cierra la ventana de la aplicación.

Ahora puede cambiar el contenido del control WebView2 a su propio contenido.


## <a name="next-steps"></a>Pasos siguientes  

*   Para obtener más información sobre cómo crear aplicaciones webView2, vaya a Procedimientos recomendados de desarrollo [de WebView2][WV2BestPractices].  
*   Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].  
*   Para obtener información detallada acerca de la API de WebView2, vaya a [WebView2 spec][GithubMicrosoftMicrosoftUiXamlSpecsWebview2].  

    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Ponerse en contacto con el equipo de Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

Para enviar las solicitudes o errores de características específicas de WinUI, vaya a [Problemas - microsoft/microsoft-ui-xaml][GithubMicrosoftMicrosoftUiXamlIssues] y, a continuación, **seleccione Nuevo problema**.  

<!-- links -->  
[WV2BestPractices]: ../concepts/developer-guide.md "Procedimientos recomendados de desarrollo de WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  
<!-- external links -->
[GithubMicrosoftMicrosoftUiXamlIssues]: https://github.com/microsoft/microsoft-ui-xaml/issues "Problemas: microsoft/microsoft-ui-xaml | GitHub"  
[GithubMicrosoftMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "Especificación de WebView2: microsoft/microsoft-ui-xaml-specs | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
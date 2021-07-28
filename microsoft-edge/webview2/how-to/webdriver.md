---
description: Automatizar y probar el control WebView2 con Microsoft Edge controlador
title: Automatizar y probar WebView2 con Microsoft Edge controlador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: 3fe9661f6d1a34def6d969deaf5f87d8e9aba312
ms.sourcegitcommit: 14f24d1af5a39c890467c337468b76c7a00429d2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2021
ms.locfileid: "11676764"
---
# <a name="automate-and-test-webview2-with-microsoft-edge-driver"></a>Automatizar y probar WebView2 con Microsoft Edge controlador  

Dado que WebView2 usa la plataforma web Microsoft Edge \(Chromium\), los desarrolladores de WebView2 pueden aprovechar las herramientas web estándar para la depuración y automatización.  Selenio es una de estas herramientas.  Implementa la API de [W3C WebDriver.][W3cWebdriver2]  Puede usar Selenio para crear pruebas automatizadas para simular las interacciones del usuario.  

Introducción a los siguientes pasos.  

## <a name="step-1-download-the-webview2api-sample"></a>Paso 1: Descargar el ejemplo webView2API  

Si no tienes un proyecto de WebView2 existente, descarga la aplicación de ejemplo [WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], que es un ejemplo completo del SDK de WebView2 más reciente.  Asegúrese de que ha cumplido los [requisitos previos para la aplicación de ejemplo WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].  

Una vez clonado el repositorio, cree el proyecto en Visual Studio.  Debería tener el aspecto de la siguiente figura.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicación de ejemplo webView2API" lightbox="../media/webdriver/sample-app.png":::
   Aplicación de ejemplo webView2API  
:::image-end:::    

## <a name="step-2-install-microsoft-edge-driver"></a>Paso 2: Instalar Microsoft Edge controlador  

Siga las instrucciones para instalar [Microsoft Edge driver][WebdriverChromiumDownloadMicrosoftEdgeDriver].  Microsoft Edge Driver es el controlador específico del explorador requerido por Selenium para automatizar y probar WebView2.  

Asegúrate de que la versión de Microsoft Edge driver coincide con la versión de WebView2 Runtime que usa la aplicación.  Para que el ejemplo webView2API funcione, asegúrese de que la versión de WebView2 Runtime sea mayor o igual que la versión compatible de la última versión del SDK de WebView2.

*  Para buscar la versión más reciente del SDK de WebView2, vaya a [Notas de la versión del SDK de WebView2][Webview2ReleaseNotes].
*  Para averiguar qué versión de WebView2 Runtime tiene actualmente, vaya a `edge://settings/help` .  

## <a name="step-3-add-selenium-to-the-webview2api-sample"></a>Paso 3: Agregar selenio al ejemplo webView2API  

En este punto, ha instalado WebView2 Runtime, ha creado un proyecto webView2 e instalado Microsoft Edge driver.  A continuación, empieza a usar Selenio, como se muestra a continuación.

> [!NOTE]
> Selenium admite C\#, Java, Python, Javascript y Ruby.  Sin embargo, la siguiente guía se escribe con C\#.  

1.  Comience creando un nuevo **proyecto C# .NET Framework** en **Visual Studio**.  Seleccione **Siguiente** en la esquina inferior derecha para continuar.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Creación de un proyecto nuevo." lightbox="../media/webdriver/new-project.png":::
       Creación de un proyecto nuevo.  
    :::image-end:::  
    
1.  Asigne al proyecto un **nombre Project**, guárdelo en la **ubicación**preferida y, a continuación, seleccione **Crear**.  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar el nuevo proyecto" lightbox="../media/webdriver/app-create.png":::
       Configurar el nuevo proyecto  
    :::image-end:::  
    
    Se crea un nuevo proyecto, con todo el código colocado en el `Program.cs` archivo.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nuevo proyecto" lightbox="../media/webdriver/start-app.png":::
       Nuevo proyecto  
    :::image-end:::  
    
1.  A continuación, agregue Selenio al proyecto; instalar Selenio mediante el paquete selenio.WebDriver NuGet siguiente.  Para descargar el paquete de NuGet Selenium.WebDriver, en **** **Visual Studio**, seleccione Project  >  **Administrar NuGet paquetes**.

1.  Seleccione la **pestaña** Examinar.  Aparece la siguiente pantalla.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Descargar NuGet paquete" lightbox="../media/webdriver/download-nuget.png":::
       Descargar NuGet paquete  
    :::image-end:::  
    
1.  En la **lista desplegable Origen** del paquete, seleccione **nuget.org**.

1.  Active la **casilla Incluir versión preliminar.**

1.  Escriba `Selenium.WebDriver` en la barra **de** búsqueda y, a continuación, seleccione **Selenium.WebDriver** en los resultados.

1.  En la ventana de detalles de la derecha, asegúrese de que **la** versión esté establecida en **4.0.0-beta4** o posterior y, a continuación, seleccione **Instalar**.  NuGet descarga Selenio en el equipo.  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Administrar NuGet paquete" lightbox="../media/webdriver/nuget.png":::
       Administrar NuGet paquete  
    :::image-end:::  
    
    Para obtener más información sobre el paquete de NuGet Selenium.WebDriver, vaya a [Selenium.WebDriver 4.0.0-beta4][NugetSeleniumWebdriver700beta4].  
    
1.  Se `OpenQA.Selenium.Edge` usa agregando la instrucción `using OpenQA.Selenium.Edge;` al principio del `Program.cs` archivo.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a>Paso 4: Drive WebView2 with Selenium and Microsoft Edge Driver  

1.  Para impulsar WebView2 con Selenio y Microsoft Edge driver, primero cree el objeto, copiando y pegando el `EdgeOptions` siguiente fragmento de código.  
    
    ```csharp
    static void Main(string[] args)
    {
        EdgeOptions edgeOptions = new EdgeOptions();
    ```  
    
1.  A continuación, agregaremos código que haga lo siguiente:

    *   Configure `edgeOptions` para usar Chromium WebView2, estableciendo las opciones y en `UseChromium` `UseWebView` `true` .
    *   Establecer `edgeOptions.BinaryLocation` en la ruta de acceso de archivo del binario de la aplicación host.
    *   Cree el `EdgeDriver` objeto con `edgeOptions` .  
    
    Copie el siguiente código y péguelo a continuación `edgeOptions` .

    ```csharp
    //Set edgeOptions to use Chromium and WebView2
    edgeOptions.UseChromium = true;
    edgeOptions.UseWebView = true;

    //Set the BinaryLocation to the filepath of the WebView2API Sample runtime
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";
    EdgeDriver edgeDriver = new EdgeDriver(edgeOptions);
    ```  

1.  En el código anterior, especifique la ruta de acceso de archivo correcta del tiempo de ejecución del proyecto y el Microsoft Edge tiempo de ejecución del controlador en el equipo.  
    
    `EdgeDriver` ahora se ha configurado para impulsar webView2 en el proyecto.  Por ejemplo, si usa el ejemplo **WebView2API,** el código ahora puede navegar ejecutando el comando, como se muestra en la `https://microsoft.com` siguiente descripción de `e.Url = @"https://www.microsoft.com";` código.

1.  Compruebe que Selenium puede impulsar WebView2 estableciendo un punto de interrupción en la `e.Url` línea y ejecutando el proyecto.  
    
    ```csharp
        //Navigate the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //Exit Microsoft Edge Driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenio que ejecuta WebView2" lightbox="../media/webdriver/microsoft.png":::
       Selenio que ejecuta WebView2  
    :::image-end:::
    
¡Enhorabuena!  Ha automatizado correctamente un proyecto de WebView2 y ha controlado WebView2 mediante Selenium y Microsoft Edge Driver.  

> [!Note]
> [edge-selenium-tools][GithubSeleniumProject] es un proyecto que el equipo de Microsoft Edge creó para permitir a los usuarios de Selenium 3 impulsar Edge Chromium y WebView2 con la misma API que se proporciona en Selenium 4.

## <a name="see-also"></a>Consulte también  

*   Para obtener un vistazo completo a cómo las API de Selenium unidades WebView2 o Microsoft Edge \(Chromium\), vaya a WebDriver en la documentación [de Selenio][SeleniumWebdriver].
*   Para obtener más información sobre el control WebView2 y cómo usarlo al insertar contenido web en la aplicación nativa, vaya a [Introducción a Microsoft Edge WebView2][WebViewIndex].
*   Para obtener más información sobre la automatización Microsoft Edge \(Chromium\), vaya a [Usar WebDriver (Chromium)][WebdriverChromium]para la automatización de pruebas .
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Ponerse en contacto con el equipo de Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  
[WebdriverChromium]: ../../webdriver-chromium/index.md "Use WebDriver (Chromium) para la automatización de pruebas | Microsoft Docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Descargar controlador Microsoft Edge: usar WebDriver (Chromium) para la automatización de pruebas | Microsoft Docs"  
[WebViewIndex]: ../index.md "Introducción a Microsoft Edge WebView2 : Microsoft Docs"  
[Webview2ReleaseNotes]: ../release-notes.md "Notas de la versión de WebView2 SDK | Microsoft Docs"  
<!-- external links -->
[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar WebDriver | Microsoft Edge Programador"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Requisitos previos: ejemplo de API de WebView2 | GitHub"  

[NugetSeleniumWebdriver700beta4]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-beta4 "Selenium.WebDriver 4.0.0-beta4 | NuGet Galería"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenio"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  

[GithubSeleniumProject]: https://github.com/microsoft/edge-selenium-tools "Herramientas de selenio para Microsoft Edge"

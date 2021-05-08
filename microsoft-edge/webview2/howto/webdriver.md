---
description: Automatizar y probar el control WebView2 con Microsoft Edge controlador
title: Automatizar y probar WebView2 con Microsoft Edge controlador
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Microsoft Edge Driver
ms.openlocfilehash: c23d639582d4ce550406cf955c96171167bde7c8
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536700"
---
# <a name="automating-and-testing-webview2-with-microsoft-edge-driver"></a>Automatizar y probar WebView2 con Microsoft Edge controlador  

Dado que WebView2 usa la plataforma web Microsoft Edge \(Chromium\), los desarrolladores de WebView2 \(you\) pueden aprovechar las herramientas web estándar para la depuración y automatización.  Selenio es una de estas herramientas.  Implementa la API de [W3C WebDriver.][W3cWebdriver2]  Puede usar Selenio para crear pruebas automatizadas para simular las interacciones del usuario.  

Introducción a los siguientes pasos.  

## <a name="step-1--download-webview2api-sample"></a>Paso 1: Descargar ejemplo de WebView2API  

Si no tiene un proyecto de WebView2 existente, descargue la aplicación de ejemplo [WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], un ejemplo completo del SDK de WebView2 más reciente.  Asegúrese de que ha cumplido los [requisitos previos para la aplicación de ejemplo WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].  

Una vez clonado el repositorio, cree el proyecto en Visual Studio.  Debería tener el aspecto de la siguiente figura.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicación de ejemplo webView2API" lightbox="../media/webdriver/sample-app.png":::
   Aplicación de ejemplo webView2API  
:::image-end:::  

## <a name="step-2--install-microsoft-edge-driver"></a>Paso 2: Instalar Microsoft Edge controlador  

Siga las instrucciones para instalar [Microsoft Edge driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] específico del explorador requerido por Selenium para automatizar y probar WebView2.  

Asegúrese de que la versión de Microsoft Edge driver coincide con la versión de WebView2 Runtime que usa la aplicación.  Para que el ejemplo webView2API funcione, asegúrese de que la versión de WebView2 Runtime sea mayor o igual que la versión admitida de la última versión del SDK de WebView2.  Para buscar la última versión del SDK de WebView2, vaya a [Notas de la versión de WebView2][Webview2Releasenotes].  Para averiguar qué versión de WebView2 Runtime tiene actualmente, vaya a `edge://settings/help` .  

## <a name="step-3--add-selenium-to-the-webview2api-sample"></a>Paso 3: Agregar selenio al ejemplo webView2API  

En este momento, debe tener WebView2 Runtime instalado, creado un proyecto WebView2 e instalado Microsoft Edge driver.  Ahora, empieza a usar Selenio.  

> [!NOTE]
> Selenium admite C\#, Java, Python, Javascript y Ruby.  Sin embargo, la siguiente guía se escribe con C\#.  

1.  Comience creando un nuevo **proyecto C# .NET Framework** en **Visual Studio**.  Elija **Siguiente** en la esquina inferior derecha para continuar.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Creación de un proyecto nuevo." lightbox="../media/webdriver/new-project.png":::
       Creación de un proyecto nuevo.  
    :::image-end:::  
    
1.  Asigne un nombre al **proyecto,** guárdelo en la ubicación **preferida**y elija **Crear**.  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar el nuevo proyecto" lightbox="../media/webdriver/app-create.png":::
       Configurar el nuevo proyecto  
    :::image-end:::  
    
1.  Se crea un nuevo proyecto.  En esta guía, todo el código se escribe en el `Program.cs` archivo.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nuevo proyecto" lightbox="../media/webdriver/start-app.png":::
       Nuevo proyecto  
    :::image-end:::  
    
1.  Ahora agregue **Selenio** al proyecto.  Instale Selenium mediante el **paquete de NuGet Selenium.WebDriver**.  
    
    Para descargar el **paquete de selenio.WebDriver NuGet**, en **Visual Studio**, mantenga el mouse **en Project**y elija Administrar **NuGet paquete**.  Debería aparecer la siguiente pantalla.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Descargar NuGet paquete" lightbox="../media/webdriver/download-nuget.png":::
       Descargar NuGet paquete  
    :::image-end:::  
    
1.  Escriba en la barra de búsqueda, elija `Selenium.WebDriver` **Selenium.WebDriver** en los resultados y asegúrese de marcar la casilla junto a **incluir la versión previa**.  En la ventana del lado derecho, asegúrese de que **Version** está configurado para instalar **4.0.0-alpha04** o posterior y elija **Instalar**.  NuGet descarga Selenio en el equipo.  
    
    Para obtener más información sobre el paquete de NuGet Selenium.WebDriver, vaya a [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Administrar NuGet paquete" lightbox="../media/webdriver/nuget.png":::
       Administrar NuGet paquete  
    :::image-end:::  
    
1.  Use `OpenQA.Selenium.Edge` agregando la siguiente instrucción:  `using OpenQA.Selenium.Edge;` al principio del `Program.cs` archivo.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a>Paso 4: Drive WebView2 with Selenium and Microsoft Edge Driver  

1.  En primer lugar, cree `EdgeOptions` el objeto copiando el siguiente fragmento de código.  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    El `EdgeOptions` objeto toma los dos parámetros siguientes.  
    
    | Parámetro | Detalles |    
    |:--- |:--- |  
    | `is_legacy` | Establece en , lo que indica a Selenium que estás impulsando el nuevo `false` Chromium basado Microsoft Edge explorador. |  
    | `"webview2"` | Cadena que indica a Selenium que estás impulsando WebView2. |  
    
1.  A continuación, establezca la ruta de acceso de archivo del tiempo de ejecución del proyecto webView2, cree una cadena denominada que proporciona la ruta de acceso del archivo al lugar donde instaló el controlador de Microsoft Edge y cree una cadena denominada para almacenar el nombre del tiempo de ejecución del controlador `edgeOptions.BinaryLocation` `msedgedriverDir` de [][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads] `msedgedriverExe` Microsoft Edge.  De forma predeterminada, el tiempo de ejecución se denomina `msedgedriver.exe` . Use estas dos cadenas para construir el `EdgeDriverService` objeto como se muestra a continuación.  Por último, cree el `EdgeDriver` objeto mediante `EdgeDriverService` y `EdgeOptions` .  
    
    Puede copiar y pegar el siguiente código debajo `edgeOptions` de .  Asegúrese de especificar las rutas de acceso de archivo correctas al tiempo de ejecución del proyecto y Microsoft Edge tiempo de ejecución del controlador en el equipo.  
    
    ```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample runtime
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";
    
    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";
    
    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";
    
    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);
    
    EdgeDriver e = new EdgeDriver(service, edgeOptions);
    ```
    
3.  Ahora, `EdgeDriver` está configurado para impulsar webView2 en el proyecto.  Por ejemplo, si usa el ejemplo **WebView2API,** puede navegar `https://microsoft.com` hasta ejecutando el `e.Url = @"https://www.microsoft.com";` comando.  Compruebe la unidad selenio WebView2 estableciendo un punto de interrupción en la línea y ejecutando el proyecto.  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenio que ejecuta WebView2" lightbox="../media/webdriver/microsoft.png":::
       Selenio que ejecuta WebView2  
    :::image-end:::

¡Enhorabuena!  Ha automatizado correctamente un proyecto webView2 y ha controlado WebView2 con Selenium y Microsoft Edge Driver.  

## <a name="see-also"></a>Consulte también  

*   Para obtener un vistazo completo a cómo las API de Selenium unidades WebView2 o Microsoft Edge \(Chromium\), vaya a [WebDriver en la documentación de Selenio][SeleniumWebdriver]   
*   Para obtener más información sobre el control WebView2 y cómo usarlo al insertar contenido web en la aplicación nativa, vaya a [Introducción a Microsoft Edge WebView2][WebViewIndex].  
*   Para obtener más información sobre la automatización Microsoft Edge \(Chromium\), vaya a [Usar WebDriver (Chromium)][WebdriverChromium] para la automatización de pruebas   
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Use WebDriver (Chromium) para la automatización de pruebas | Microsoft Docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Descargar controlador Microsoft Edge: usar WebDriver (Chromium) para la automatización de pruebas | Microsoft Docs"  
[WebViewIndex]: ../index.md "Introducción a Microsoft Edge WebView2 : Microsoft Docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de la versión de WebView2 SDK | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar WebDriver | Microsoft Edge Programador"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Requisitos previos: ejemplo de API de WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium.WebDriver 4.0.0-alpha04 | NuGet Galería"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenio"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  

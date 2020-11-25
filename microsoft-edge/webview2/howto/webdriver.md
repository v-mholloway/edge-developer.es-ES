---
description: Automatizar y probar el control WebView2 con el controlador Microsoft Edge
title: Automatizar y probar WebView2 con el controlador Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, Selenium, controlador Microsoft Edge
ms.openlocfilehash: 6f7f84fa88a57e54d7b5143a489d1138c7426d88
ms.sourcegitcommit: 652c345b46aae8b7e3723eb55a01b71a4ef76bf0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "11191453"
---
# Automatizar y probar WebView2 con el controlador Microsoft Edge  

Debido a que WebView2 usa la plataforma web Microsoft Edge \ (cromo \), WebView2 desarrolladores \ (usted \) puede aprovechar las herramientas web estándar para la depuración y la automatización.  Selenium es una herramienta de este tipo.  Implementa la API [Webdriver][W3cWebdriver2] de W3C.  Puede usar Selenium para crear pruebas automatizadas para simular interacciones del usuario.  

Comience con los siguientes pasos.  

## Paso 1: Descargar ejemplo de WebView2API  

Si no tiene un proyecto de WebView2 existente, descargue la [aplicación de ejemplo WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], una muestra completa del SDK de WebView2 más reciente.  Asegúrese de que ha satisfecho los [requisitos previos para la aplicación de ejemplo WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]. 

Una vez que haya clonado el repositorio, compile el proyecto en Visual Studio.  Debería ser similar a la siguiente ilustración.  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicación de ejemplo WebView2API" lightbox="../media/webdriver/sample-app.png":::
   Aplicación de ejemplo WebView2API  
:::image-end:::  

## Paso 2: instalar el controlador de Microsoft Edge  

Siga las instrucciones para instalar el [controlador Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] el controlador específico del explorador requerido por Selenium para automatizar y probar WebView2.  

Asegúrese de que la versión del controlador de Microsoft Edge coincide con la versión de WebView2 Runtime que usa la aplicación.  Para que el ejemplo WebView2API funcione, asegúrese de que la versión de WebView2 Runtime sea mayor o igual que la versión admitida de la última versión del SDK de WebView2.  Para encontrar la versión más reciente del SDK de WebView2, vaya a las notas de la [versión de WebView2][Webview2Releasenotes].  Para saber qué versión de WebView2 Runtime tiene actualmente, vaya a `edge://settings/help` .  

## Paso 3: agregar Selenium al ejemplo WebView2API  

En este momento, deberías tener instalado WebView2 Runtime, haber creado un proyecto de WebView2 y el controlador Microsoft Edge instalado.  Ahora, empiece a usar Selenium.  

> [!NOTE]
> Selenium es compatible con C \ #, Java, Python, JavaScript y Ruby.  Sin embargo, la siguiente guía está escrita con C \ #.  

1.  Para empezar, cree un nuevo proyecto de **C# .NET Framework** en **Visual Studio**.  Elija **siguiente** en la esquina inferior derecha para continuar.  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Creación de un proyecto nuevo." lightbox="../media/webdriver/new-project.png":::
       Creación de un proyecto nuevo.  
    :::image-end:::  
    
1.  Asigne un **nombre**al proyecto, guárdelo en la **Ubicación**que prefiera y elija **crear**.  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar el nuevo proyecto" lightbox="../media/webdriver/app-create.png":::
       Configurar el nuevo proyecto  
    :::image-end:::  
    
1.  Se crea un nuevo proyecto.  En esta guía, todo el código se escribe en el `Program.cs` archivo.  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nuevo proyecto" lightbox="../media/webdriver/start-app.png":::
       Nuevo proyecto  
    :::image-end:::  
    
1.  Ahora, agregue **Selenium** al proyecto.  Instala Selenium con el **paquete de NuGet Selenium. Webdriver**.  
    
    Para descargar el **paquete de NuGet Selenium. WebDrive**, en **Visual Studio**, mantenga el mouse sobre **Project**y elija **administrar paquete Nuget**.  Debe aparecer la siguiente pantalla.  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Descargar paquete NuGet" lightbox="../media/webdriver/download-nuget.png":::
       Descargar paquete NuGet  
    :::image-end:::  
    
1.  Escriba **Selenium. WebDrive** en la barra de búsqueda, elija **Selenium. WebDrive** de los resultados y asegúrese de que marca la casilla junto a **incluir versión preliminar**. En la ventana de la derecha, asegúrese de que la **versión** está configurada para **instalar 4.0.0-alpha04** o posterior y elija **instalar**.  Descargas de Nuget Selenium a tu equipo.  
    
    Para obtener más información sobre el paquete de NuGet Selenium. WebDrive, vaya a [Selenium. WebDrive 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Administrar paquete NuGet" lightbox="../media/webdriver/nuget.png":::
       Administrar paquete NuGet  
    :::image-end:::  
    
1.  `OpenQA.Selenium.Edge`Para usarlo, agregue la siguiente instrucción: `using OpenQA.Selenium.Edge;` al principio del `Program.cs` archivo.  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## Paso 4: WebView2 con Selenium y el controlador Microsoft Edge  

1.  En primer lugar, cree el `EdgeOptions` objeto copiando el siguiente fragmento de código.  
    
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
    | `is_legacy` | Establezca en `false` , que indica a Selenium que está conduciendo el nuevo explorador Microsoft Edge basado en cromo. |  
    | `"webview2"` | Una cadena que indica A Selenium que estás WebView2. |  
    
1.  A continuación, establezca `edgeOptions.BinaryLocation` la ruta de acceso de archivo de su WebView2 proyecto en tiempo de ejecución, cree una cadena con `msedgedriverDir` el nombre que proporcione la ruta de acceso al archivo donde instaló el [controlador de Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]y cree una cadena denominada `msedgedriverExe` para almacenar el nombre del motor de tiempo de ejecución del controlador Microsoft Edge.  De forma predeterminada, el motor en tiempo de ejecución tiene el nombre `msedgedriver.exe` . Use estas dos cadenas para construir el `EdgeDriverService` objeto como se muestra a continuación.  Por último, cree el `EdgeDriver` objeto con `EdgeDriverService` and `EdgeOptions` .  
    
    Puede copiar y pegar el código siguiente debajo `edgeOptions` .  Asegúrese de especificar las rutas de archivo correctas en el tiempo de ejecución del proyecto y en el tiempo de ejecución del controlador Microsoft Edge en el equipo.  
    
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
    
3.  Ahora, `EdgeDriver` está configurado para impulsar el WebView2 en el proyecto.  Por ejemplo, si usa el **ejemplo WebView2API**, puede navegar `https://microsoft.com` por ejecutando el `e.Url = @"https://www.microsoft.com";` comando.  Compruebe la WebView2 de la unidad Selenium estableciendo un punto de interrupción en la línea y ejecutando el proyecto.  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium ejecutando WebView2" lightbox="../media/webdriver/microsoft.png":::
       Selenium ejecutando WebView2  
    :::image-end:::

¡Enhorabuena!  Has automatizado correctamente un proyecto WebView2 y WebView2 controlado con Selenium y el controlador Microsoft Edge.  

## Consulte también  

*   Para obtener una visión completa de cómo las API Selenium Drives WebView2 o Microsoft Edge \ (cromo \), vaya a [WebDrive en la documentación de Selenium][SeleniumWebdriver]   
*   Para obtener más información sobre el control de WebView2 y cómo usarlo al incrustar contenido web en la aplicación nativa, vaya a [Introducción a Microsoft Edge WebView2][WebViewIndex].  
*   Para obtener más información sobre cómo automatizar Microsoft Edge \ (cromo \), navegue para [usar Webdriver (cromo) para automatización de prueba][WebdriverChromium]   
    
## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium.md "Usar Webdriver (cromo) para automatización de prueba | Microsoft docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium.md#download-microsoft-edge-driver "Descargar el controlador Microsoft Edge: Use Webdriver (cromo) para automatización de prueba | Microsoft docs"  
[WebViewIndex]: ../index.md "Introducción a Microsoft Edge WebView2-Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar Webdriver | Desarrollador de Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Requisitos previos: ejemplo de API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium. WebDrive 4.0.0-alpha04 | Galería de NuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "Controlador WebDrive | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "Controlador WebDrive | RELATIVA"  

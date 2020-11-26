---
description: Automatizar y probar el control WebView2 con el controlador Microsoft Edge
title: Automatizar y probar WebView2 con el controlador Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, Edge, ICoreWebView2, ICoreWebView2Controller, Selenium, controlador Microsoft Edge
ms.openlocfilehash: 2af1ce222abb1dc7a279afc05e87e7e42a45fe9e
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "11191620"
---
# <span data-ttu-id="73466-104">Automatizar y probar WebView2 con el controlador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73466-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="73466-105">Debido a que WebView2 usa la plataforma web Microsoft Edge \ (cromo \), WebView2 desarrolladores \ (usted \) puede aprovechar las herramientas web estándar para la depuración y la automatización.</span><span class="sxs-lookup"><span data-stu-id="73466-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="73466-106">Selenium es una herramienta de este tipo.</span><span class="sxs-lookup"><span data-stu-id="73466-106">Selenium is one such tool.</span></span>  <span data-ttu-id="73466-107">Implementa la API [Webdriver][W3cWebdriver2] de W3C.</span><span class="sxs-lookup"><span data-stu-id="73466-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="73466-108">Puede usar Selenium para crear pruebas automatizadas para simular interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="73466-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="73466-109">Comience con los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="73466-109">Get started with the following steps.</span></span>  

## <span data-ttu-id="73466-110">Paso 1: Descargar ejemplo de WebView2API</span><span class="sxs-lookup"><span data-stu-id="73466-110">Step 1:  Download WebView2API Sample</span></span>  

<span data-ttu-id="73466-111">Si no tiene un proyecto de WebView2 existente, descargue la [aplicación de ejemplo WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], una muestra completa del SDK de WebView2 más reciente.</span><span class="sxs-lookup"><span data-stu-id="73466-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="73466-112">Asegúrese de que ha satisfecho los [requisitos previos para la aplicación de ejemplo WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span><span class="sxs-lookup"><span data-stu-id="73466-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span>  

<span data-ttu-id="73466-113">Una vez que haya clonado el repositorio, compile el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="73466-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="73466-114">Debería ser similar a la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="73466-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicación de ejemplo WebView2API" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="73466-116">Aplicación de ejemplo WebView2API</span><span class="sxs-lookup"><span data-stu-id="73466-116">WebView2API Sample app</span></span>  
:::image-end:::  

## <span data-ttu-id="73466-117">Paso 2: instalar el controlador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73466-117">Step 2:  Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="73466-118">Siga las instrucciones para instalar el [controlador Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] el controlador específico del explorador requerido por Selenium para automatizar y probar WebView2.</span><span class="sxs-lookup"><span data-stu-id="73466-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="73466-119">Asegúrese de que la versión del controlador de Microsoft Edge coincide con la versión de WebView2 Runtime que usa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="73466-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="73466-120">Para que el ejemplo WebView2API funcione, asegúrese de que la versión de WebView2 Runtime sea mayor o igual que la versión admitida de la última versión del SDK de WebView2.</span><span class="sxs-lookup"><span data-stu-id="73466-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="73466-121">Para encontrar la versión más reciente del SDK de WebView2, vaya a las notas de la [versión de WebView2][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="73466-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="73466-122">Para saber qué versión de WebView2 Runtime tiene actualmente, vaya a `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="73466-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <span data-ttu-id="73466-123">Paso 3: agregar Selenium al ejemplo WebView2API</span><span class="sxs-lookup"><span data-stu-id="73466-123">Step 3:  Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="73466-124">En este momento, deberías tener instalado WebView2 Runtime, haber creado un proyecto de WebView2 y el controlador Microsoft Edge instalado.</span><span class="sxs-lookup"><span data-stu-id="73466-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="73466-125">Ahora, empiece a usar Selenium.</span><span class="sxs-lookup"><span data-stu-id="73466-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="73466-126">Selenium es compatible con C \ #, Java, Python, JavaScript y Ruby.</span><span class="sxs-lookup"><span data-stu-id="73466-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="73466-127">Sin embargo, la siguiente guía está escrita con C \ #.</span><span class="sxs-lookup"><span data-stu-id="73466-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="73466-128">Para empezar, cree un nuevo proyecto de **C# .NET Framework** en **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="73466-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="73466-129">Elija **siguiente** en la esquina inferior derecha para continuar.</span><span class="sxs-lookup"><span data-stu-id="73466-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Creación de un proyecto nuevo." lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="73466-131">Creación de un proyecto nuevo.</span><span class="sxs-lookup"><span data-stu-id="73466-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73466-132">Asigne un **nombre**al proyecto, guárdelo en la **Ubicación**que prefiera y elija **crear**.</span><span class="sxs-lookup"><span data-stu-id="73466-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar el nuevo proyecto" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="73466-134">Configurar el nuevo proyecto</span><span class="sxs-lookup"><span data-stu-id="73466-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73466-135">Se crea un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="73466-135">A new project is created.</span></span>  <span data-ttu-id="73466-136">En esta guía, todo el código se escribe en el `Program.cs` archivo.</span><span class="sxs-lookup"><span data-stu-id="73466-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nuevo proyecto" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="73466-138">Nuevo proyecto</span><span class="sxs-lookup"><span data-stu-id="73466-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73466-139">Ahora, agregue **Selenium** al proyecto.</span><span class="sxs-lookup"><span data-stu-id="73466-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="73466-140">Instala Selenium con el **paquete de NuGet Selenium. Webdriver**.</span><span class="sxs-lookup"><span data-stu-id="73466-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="73466-141">Para descargar el **paquete de NuGet Selenium. WebDrive**, en **Visual Studio**, mantenga el mouse sobre **Project**y elija **administrar paquete Nuget**.</span><span class="sxs-lookup"><span data-stu-id="73466-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover over **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="73466-142">Debe aparecer la siguiente pantalla.</span><span class="sxs-lookup"><span data-stu-id="73466-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Descargar paquete NuGet" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="73466-144">Descargar paquete NuGet</span><span class="sxs-lookup"><span data-stu-id="73466-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73466-145">Escriba `Selenium.WebDriver` en la barra de búsqueda, elija **Selenium. WebDrive** en los resultados y asegúrese de que marca la casilla junto a **incluir versión preliminar**.</span><span class="sxs-lookup"><span data-stu-id="73466-145">Enter `Selenium.WebDriver` in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span>  <span data-ttu-id="73466-146">En la ventana de la derecha, asegúrese de que la **versión** está configurada para **instalar 4.0.0-alpha04** o posterior y elija **instalar**.</span><span class="sxs-lookup"><span data-stu-id="73466-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="73466-147">Descargas de NuGet Selenium a tu equipo.</span><span class="sxs-lookup"><span data-stu-id="73466-147">NuGet downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="73466-148">Para obtener más información sobre el paquete de NuGet Selenium. WebDrive, vaya a [Selenium. WebDrive 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="73466-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Administrar paquete NuGet" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="73466-150">Administrar paquete NuGet</span><span class="sxs-lookup"><span data-stu-id="73466-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="73466-151">`OpenQA.Selenium.Edge`Para usarlo, agregue la siguiente instrucción: `using OpenQA.Selenium.Edge;` al principio del `Program.cs` archivo.</span><span class="sxs-lookup"><span data-stu-id="73466-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <span data-ttu-id="73466-152">Paso 4: WebView2 con Selenium y el controlador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73466-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="73466-153">En primer lugar, cree el `EdgeOptions` objeto copiando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="73466-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="73466-154">El `EdgeOptions` objeto toma los dos parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="73466-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="73466-155">Parámetro</span><span class="sxs-lookup"><span data-stu-id="73466-155">Parameter</span></span> | <span data-ttu-id="73466-156">Detalles</span><span class="sxs-lookup"><span data-stu-id="73466-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="73466-157">Establezca en `false` , que indica a Selenium que está conduciendo el nuevo explorador Microsoft Edge basado en cromo.</span><span class="sxs-lookup"><span data-stu-id="73466-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="73466-158">Una cadena que indica A Selenium que estás WebView2.</span><span class="sxs-lookup"><span data-stu-id="73466-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="73466-159">A continuación, establezca `edgeOptions.BinaryLocation` la ruta de acceso de archivo de su WebView2 proyecto en tiempo de ejecución, cree una cadena con `msedgedriverDir` el nombre que proporcione la ruta de acceso al archivo donde instaló el [controlador de Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]y cree una cadena denominada `msedgedriverExe` para almacenar el nombre del motor de tiempo de ejecución del controlador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="73466-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="73466-160">De forma predeterminada, el motor en tiempo de ejecución tiene el nombre `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="73466-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="73466-161">Use estas dos cadenas para construir el `EdgeDriverService` objeto como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="73466-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="73466-162">Por último, cree el `EdgeDriver` objeto con `EdgeDriverService` and `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="73466-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="73466-163">Puede copiar y pegar el código siguiente debajo `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="73466-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="73466-164">Asegúrese de especificar las rutas de archivo correctas en el tiempo de ejecución del proyecto y en el tiempo de ejecución del controlador Microsoft Edge en el equipo.</span><span class="sxs-lookup"><span data-stu-id="73466-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
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
    
3.  <span data-ttu-id="73466-165">Ahora, `EdgeDriver` está configurado para impulsar el WebView2 en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73466-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="73466-166">Por ejemplo, si usa el **ejemplo WebView2API**, puede navegar `https://microsoft.com` por ejecutando el `e.Url = @"https://www.microsoft.com";` comando.</span><span class="sxs-lookup"><span data-stu-id="73466-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="73466-167">Compruebe la WebView2 de la unidad Selenium estableciendo un punto de interrupción en la línea y ejecutando el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73466-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenium ejecutando WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="73466-169">Selenium ejecutando WebView2</span><span class="sxs-lookup"><span data-stu-id="73466-169">Selenium running WebView2</span></span>  
    :::image-end:::

<span data-ttu-id="73466-170">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="73466-170">Congratulations.</span></span>  <span data-ttu-id="73466-171">Has automatizado correctamente un proyecto WebView2 y WebView2 controlado con Selenium y el controlador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="73466-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <span data-ttu-id="73466-172">Consulte también</span><span class="sxs-lookup"><span data-stu-id="73466-172">See also</span></span>  

*   <span data-ttu-id="73466-173">Para obtener una visión completa de cómo las API Selenium Drives WebView2 o Microsoft Edge \ (cromo \), vaya a [WebDrive en la documentación de Selenium][SeleniumWebdriver]</span><span class="sxs-lookup"><span data-stu-id="73466-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="73466-174">Para obtener más información sobre el control de WebView2 y cómo usarlo al incrustar contenido web en la aplicación nativa, vaya a [Introducción a Microsoft Edge WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="73466-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="73466-175">Para obtener más información sobre cómo automatizar Microsoft Edge \ (cromo \), navegue para [usar Webdriver (cromo) para automatización de prueba][WebdriverChromium]</span><span class="sxs-lookup"><span data-stu-id="73466-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <span data-ttu-id="73466-176">Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="73466-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Usar Webdriver (cromo) para automatización de prueba | Microsoft docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Descargar el controlador Microsoft Edge: Use Webdriver (cromo) para automatización de prueba | Microsoft docs"  
[WebViewIndex]: ../index.md "Introducción a Microsoft Edge WebView2-Microsoft docs"  
[Webview2Releasenotes]: ../releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar Webdriver | Desarrollador de Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Requisitos previos: ejemplo de API WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium. WebDrive 4.0.0-alpha04 | Galería de NuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "Controlador WebDrive | Selenium"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "Controlador WebDrive | RELATIVA"  

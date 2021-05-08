---
description: Automatizar y probar el control WebView2 con el controlador de Microsoft Edge
title: Automatizar y probar WebView2 con controlador de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Selenium, Controlador de Microsoft Edge
ms.openlocfilehash: 37c0e41e11693c8a21b7240bf9370fd658834cff
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536173"
---
# <a name="automate-and-test-webview2-with-microsoft-edge-driver"></a><span data-ttu-id="9ab8c-104">Automatizar y probar WebView2 con controlador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9ab8c-104">Automate and test WebView2 with Microsoft Edge Driver</span></span>  

<span data-ttu-id="9ab8c-105">Dado que WebView2 usa la plataforma web Microsoft Edge \(Chromium\), los desarrolladores de WebView2 \(you\) pueden aprovechar las herramientas web estándar para la depuración y automatización.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-105">Because WebView2 uses the Microsoft Edge \(Chromium\) web platform, WebView2 developers \(you\) may take advantage of standard web tooling for debugging and automation.</span></span>  <span data-ttu-id="9ab8c-106">Selenio es una de estas herramientas.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-106">Selenium is one such tool.</span></span>  <span data-ttu-id="9ab8c-107">Implementa la API de [W3C WebDriver.][W3cWebdriver2]</span><span class="sxs-lookup"><span data-stu-id="9ab8c-107">It implements the W3C [WebDriver][W3cWebdriver2] API.</span></span>  <span data-ttu-id="9ab8c-108">Puede usar Selenio para crear pruebas automatizadas para simular las interacciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-108">You may use Selenium to create automated tests to simulate user interactions.</span></span>  

<span data-ttu-id="9ab8c-109">Introducción a los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-109">Get started with the following steps.</span></span>  

## <a name="step-1--download-webview2api-sample"></a><span data-ttu-id="9ab8c-110">Paso 1: Descargar ejemplo de WebView2API</span><span class="sxs-lookup"><span data-stu-id="9ab8c-110">Step 1:  Download WebView2API Sample</span></span>  

<span data-ttu-id="9ab8c-111">Si no tiene un proyecto de WebView2 existente, descargue la aplicación de ejemplo [WebView2API][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], un ejemplo completo del SDK de WebView2 más reciente.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-111">If you do not have an existing WebView2 project, download the [WebView2API Sample app][GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample], a comprehensive sample of the latest WebView2 SDK.</span></span>  <span data-ttu-id="9ab8c-112">Asegúrese de que ha cumplido los [requisitos previos para la aplicación de ejemplo WebView2API][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span><span class="sxs-lookup"><span data-stu-id="9ab8c-112">Ensure you have satisfied the [prerequisites for the WebView2API Sample app][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites].</span></span>  

<span data-ttu-id="9ab8c-113">Una vez clonado el repositorio, cree el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-113">Once you have cloned the repo, build the project in Visual Studio.</span></span>  <span data-ttu-id="9ab8c-114">Debería tener el aspecto de la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-114">It should look like the following figure.</span></span>  

:::image type="complex" source="../media/webdriver/sample-app.png" alt-text="Aplicación de ejemplo webView2API" lightbox="../media/webdriver/sample-app.png":::
   <span data-ttu-id="9ab8c-116">Aplicación de ejemplo webView2API</span><span class="sxs-lookup"><span data-stu-id="9ab8c-116">WebView2API Sample app</span></span>  
:::image-end:::    

## <a name="step-2--install-microsoft-edge-driver"></a><span data-ttu-id="9ab8c-117">Paso 2: Instalar el controlador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9ab8c-117">Step 2:  Install Microsoft Edge Driver</span></span>  

<span data-ttu-id="9ab8c-118">Siga las instrucciones para instalar El controlador [de Microsoft Edge][WebdriverChromiumDownloadMicrosoftEdgeDriver] es el controlador específico del explorador requerido por Selenium para automatizar y probar WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-118">Follow the instructions to install [Microsoft Edge Driver][WebdriverChromiumDownloadMicrosoftEdgeDriver] the browser-specific driver required by Selenium to automate and test WebView2.</span></span>  

<span data-ttu-id="9ab8c-119">Asegúrese de que la versión del controlador de Microsoft Edge coincide con la versión de WebView2 Runtime que usa la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-119">Ensure that the version of Microsoft Edge Driver matches the version of WebView2 Runtime that you app uses.</span></span>  <span data-ttu-id="9ab8c-120">Para que el ejemplo webView2API funcione, asegúrese de que la versión de WebView2 Runtime sea mayor o igual que la versión admitida de la última versión del SDK de WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-120">For the WebView2API Sample to work, make sure that your version of WebView2 Runtime is greater than or equal than the supported version of the latest WebView2 SDK release.</span></span>  <span data-ttu-id="9ab8c-121">Para buscar la última versión del SDK de WebView2, vaya a [Notas de la versión de WebView2][Webview2ReleaseNotes].</span><span class="sxs-lookup"><span data-stu-id="9ab8c-121">To locate the latest WebView2 SDK release, navigate to [WebView2 release notes][Webview2ReleaseNotes].</span></span>  <span data-ttu-id="9ab8c-122">Para averiguar qué versión de WebView2 Runtime tiene actualmente, vaya a `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="9ab8c-122">To find out what version of WebView2 Runtime you currently have, navigate to `edge://settings/help`.</span></span>  

## <a name="step-3--add-selenium-to-the-webview2api-sample"></a><span data-ttu-id="9ab8c-123">Paso 3: Agregar selenio al ejemplo webView2API</span><span class="sxs-lookup"><span data-stu-id="9ab8c-123">Step 3:  Add Selenium to the WebView2API Sample</span></span>  

<span data-ttu-id="9ab8c-124">En este momento, debe tener WebView2 Runtime instalado, creado un proyecto webView2 e instalado controlador de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-124">At this point you should have WebView2 Runtime installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span>  <span data-ttu-id="9ab8c-125">Ahora, empieza a usar Selenio.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-125">Now, get started using Selenium.</span></span>  

> [!NOTE]
> <span data-ttu-id="9ab8c-126">Selenium admite C\#, Java, Python, Javascript y Ruby.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-126">Selenium supports C\#, Java, Python, Javascript, and Ruby.</span></span>  <span data-ttu-id="9ab8c-127">Sin embargo, la siguiente guía se escribe con C\#.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-127">However, the following guide is written using C\#.</span></span>  

1.  <span data-ttu-id="9ab8c-128">Comience creando un nuevo **proyecto C# .NET Framework** en **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-128">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span>  <span data-ttu-id="9ab8c-129">Elija **Siguiente** en la esquina inferior derecha para continuar.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-129">Choose **Next** on the bottom right-hand corner to continue.</span></span>  
    
    :::image type="complex" source="../media/webdriver/new-project.png" alt-text="Creación de un proyecto nuevo." lightbox="../media/webdriver/new-project.png":::
       <span data-ttu-id="9ab8c-131">Creación de un proyecto nuevo.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-131">Create a new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ab8c-132">Asigne un nombre al **proyecto,** guárdelo en la ubicación **preferida**y elija **Crear**.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-132">Give your project a **name**, save it to your preferred **location**, and choose **Create**.</span></span>  
    
    :::image type="complex" source="../media/webdriver/app-create.png" alt-text="Configurar el nuevo proyecto" lightbox="../media/webdriver/app-create.png":::
       <span data-ttu-id="9ab8c-134">Configurar el nuevo proyecto</span><span class="sxs-lookup"><span data-stu-id="9ab8c-134">Configure your new project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ab8c-135">Se crea un nuevo proyecto.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-135">A new project is created.</span></span>  <span data-ttu-id="9ab8c-136">En esta guía, todo el código se escribe en el `Program.cs` archivo.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-136">In this guide, all code is written to the `Program.cs` file.</span></span>  
    
    :::image type="complex" source="../media/webdriver/start-app.png" alt-text="Nuevo proyecto" lightbox="../media/webdriver/start-app.png":::
       <span data-ttu-id="9ab8c-138">Nuevo proyecto</span><span class="sxs-lookup"><span data-stu-id="9ab8c-138">New project</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ab8c-139">Ahora agregue **Selenio** al proyecto.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-139">Now add **Selenium** to the project.</span></span>  <span data-ttu-id="9ab8c-140">Instale Selenium mediante el paquete **NuGet Selenium.WebDriver**.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-140">Install Selenium using the **Selenium.WebDriver NuGet package**.</span></span>  
    
    <span data-ttu-id="9ab8c-141">Para descargar el **paquete NuGet Selenium.WebDriver**, en **Visual Studio**, mantenga el mouse en **Project**y elija Administrar **paquete NuGet**.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-141">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover on **Project**, and choose **Manage NuGet Package**.</span></span>  <span data-ttu-id="9ab8c-142">Debería aparecer la siguiente pantalla.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-142">The following screen should appear.</span></span>  
    
    :::image type="complex" source="../media/webdriver/download-nuget.png" alt-text="Descargar paquete NuGet" lightbox="../media/webdriver/download-nuget.png":::
       <span data-ttu-id="9ab8c-144">Descargar paquete NuGet</span><span class="sxs-lookup"><span data-stu-id="9ab8c-144">Download NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ab8c-145">Escriba en la barra de búsqueda, elija `Selenium.WebDriver` **Selenium.WebDriver** en los resultados y asegúrese de marcar la casilla junto a **incluir la versión previa**.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-145">Type `Selenium.WebDriver` in the search bar, choose **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span>  <span data-ttu-id="9ab8c-146">En la ventana del lado derecho, asegúrese de que **Version** está configurado para instalar **4.0.0-alpha04** o posterior y elija **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-146">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and choose **Install**.</span></span>  <span data-ttu-id="9ab8c-147">NuGet descarga Selenio en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-147">NuGet downloads Selenium to your machine.</span></span>  
    
    <span data-ttu-id="9ab8c-148">Para obtener más información sobre el paquete NuGet Selenium.WebDriver, vaya a [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span><span class="sxs-lookup"><span data-stu-id="9ab8c-148">To learn more about the Selenium.WebDriver NuGet package, navigate to [Selenium.WebDriver 4.0.0-alpha04][NugetSeleniumWebdriver400Alpha04].</span></span>  
    
    :::image type="complex" source="../media/webdriver/nuget.png" alt-text="Administrar el paquete NuGet" lightbox="../media/webdriver/nuget.png":::
       <span data-ttu-id="9ab8c-150">Administrar el paquete NuGet</span><span class="sxs-lookup"><span data-stu-id="9ab8c-150">Manage NuGet package</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9ab8c-151">Use `OpenQA.Selenium.Edge` agregando la siguiente instrucción:  `using OpenQA.Selenium.Edge;` al principio del `Program.cs` archivo.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-151">Use `OpenQA.Selenium.Edge` by adding the following statement:  `using OpenQA.Selenium.Edge;` at the beginning of `Program.cs` file.</span></span>  
    
    ```csharp
    using OpenQA.Selenium.Edge;
    
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using System.Threading.Tasks;
    ```  
    
## <a name="step-4-drive-webview2-with-selenium-and-microsoft-edge-driver"></a><span data-ttu-id="9ab8c-152">Paso 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="9ab8c-152">Step 4: Drive WebView2 with Selenium and Microsoft Edge Driver</span></span>  

1.  <span data-ttu-id="9ab8c-153">En primer lugar, cree `EdgeOptions` el objeto copiando el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-153">First, create the `EdgeOptions` object, by copying the following code snippet.</span></span>  
    
    ```csharp
    static void Main(string[] args)
    {
        // EdgeOptions() requires using OpenQA.Selenium.Edge
        // Construct EdgeOptions with is_legacy = false and the string "webview2"
        EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
    ```  
    
    <span data-ttu-id="9ab8c-154">El `EdgeOptions` objeto toma los dos parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-154">The `EdgeOptions` object takes in the following two parameters.</span></span>  
    
    | <span data-ttu-id="9ab8c-155">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9ab8c-155">Parameter</span></span> | <span data-ttu-id="9ab8c-156">Detalles</span><span class="sxs-lookup"><span data-stu-id="9ab8c-156">Details</span></span> |    
    |:--- |:--- |  
    | `is_legacy` | <span data-ttu-id="9ab8c-157">Establece en `false` , lo que indica a Selenio que estás impulsando el nuevo explorador Microsoft Edge basado en Chromium.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-157">Set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span> |  
    | `"webview2"` | <span data-ttu-id="9ab8c-158">Cadena que indica a Selenium que estás impulsando WebView2.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-158">A string that tells Selenium you are driving WebView2.</span></span> |  
    
1.  <span data-ttu-id="9ab8c-159">A continuación, establezca la ruta de acceso de archivo del tiempo de ejecución del proyecto webView2, cree una cadena denominada que proporciona la ruta de acceso del archivo al lugar donde instaló el controlador de Microsoft Edge y cree una cadena denominada para almacenar el nombre del tiempo de ejecución del controlador `edgeOptions.BinaryLocation` `msedgedriverDir` de Microsoft [][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads] `msedgedriverExe` Edge.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-159">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project runtime, create a string named `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads], and create a string named `msedgedriverExe` to store the name of the Microsoft Edge Driver runtime.</span></span>  <span data-ttu-id="9ab8c-160">De forma predeterminada, el tiempo de ejecución se denomina `msedgedriver.exe` .</span><span class="sxs-lookup"><span data-stu-id="9ab8c-160">By default, the runtime is named `msedgedriver.exe`.</span></span> <span data-ttu-id="9ab8c-161">Use estas dos cadenas para construir el `EdgeDriverService` objeto como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-161">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span>  <span data-ttu-id="9ab8c-162">Por último, cree el `EdgeDriver` objeto mediante `EdgeDriverService` y `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="9ab8c-162">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>  
    
    <span data-ttu-id="9ab8c-163">Puede copiar y pegar el siguiente código debajo `edgeOptions` de .</span><span class="sxs-lookup"><span data-stu-id="9ab8c-163">You may copy and paste the following code underneath `edgeOptions`.</span></span>  <span data-ttu-id="9ab8c-164">Asegúrese de especificar las rutas de acceso de archivo correctas al tiempo de ejecución del proyecto y al tiempo de ejecución del controlador de Microsoft Edge en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-164">Ensure you specify the correct file paths to your project runtime and the Microsoft Edge Driver runtime on your machine.</span></span>  
    
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
    
3.  <span data-ttu-id="9ab8c-165">Ahora, `EdgeDriver` está configurado para impulsar webView2 en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-165">Now, `EdgeDriver` is configured to drive the WebView2 in your project.</span></span>  <span data-ttu-id="9ab8c-166">Por ejemplo, si usa el ejemplo **WebView2API,** puede navegar `https://microsoft.com` hasta ejecutando el `e.Url = @"https://www.microsoft.com";` comando.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-166">For example, if you are using the **WebView2API Sample**, you may navigate to `https://microsoft.com` by running the `e.Url = @"https://www.microsoft.com";` command.</span></span>  <span data-ttu-id="9ab8c-167">Compruebe la unidad selenio WebView2 estableciendo un punto de interrupción en la línea y ejecutando el proyecto.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-167">Verify the Selenium drive WebView2 by setting a breakpoint on the line and running the project.</span></span>  
    
    ```csharp
        //The following navigates the WebView2API Sample from bing.com to microsoft.com
        e.Url = @"https://www.microsoft.com";
        
        //This exits the edge driver
        e.Quit();
    }
    ```  
    
    :::image type="complex" source="../media/webdriver/microsoft.png" alt-text="Selenio que ejecuta WebView2" lightbox="../media/webdriver/microsoft.png":::
       <span data-ttu-id="9ab8c-169">Selenio que ejecuta WebView2</span><span class="sxs-lookup"><span data-stu-id="9ab8c-169">Selenium running WebView2</span></span>  
    :::image-end:::
    
<span data-ttu-id="9ab8c-170">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="9ab8c-170">Congratulations.</span></span>  <span data-ttu-id="9ab8c-171">Ha automatizado correctamente un proyecto webView2 y ha controlado WebView2 con Selenio y controlador de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9ab8c-171">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ab8c-172">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9ab8c-172">See also</span></span>  

*   <span data-ttu-id="9ab8c-173">Para obtener un vistazo completo a cómo las API de Selenium unidades WebView2 o Microsoft Edge \(Chromium\), vaya a [WebDriver en la documentación de Selenio][SeleniumWebdriver]</span><span class="sxs-lookup"><span data-stu-id="9ab8c-173">For a comprehensive look at how the APIs Selenium drives WebView2 or Microsoft Edge \(Chromium\), navigate to [WebDriver on Selenium documentation][SeleniumWebdriver]</span></span>   
*   <span data-ttu-id="9ab8c-174">Para obtener más información sobre el control WebView2 y cómo usarlo al insertar contenido web en la aplicación nativa, vaya a Introducción a [Microsoft Edge WebView2][WebViewIndex].</span><span class="sxs-lookup"><span data-stu-id="9ab8c-174">To learn more about WebView2 control and how to use it when embedding web content in your native app, navigate to [Introduction to Microsoft Edge WebView2][WebViewIndex].</span></span>  
*   <span data-ttu-id="9ab8c-175">Para obtener más información sobre la automatización de Microsoft Edge \(Chromium\), vaya a [Usar WebDriver (Chromium) para la automatización de pruebas][WebdriverChromium]</span><span class="sxs-lookup"><span data-stu-id="9ab8c-175">To learn more about automating Microsoft Edge \(Chromium\), navigate to [Use WebDriver (Chromium) for test automation][WebdriverChromium]</span></span>   
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="9ab8c-176">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="9ab8c-176">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WebdriverChromium]: ../../webdriver-chromium/index.md "Use WebDriver (Chromium) para la automatización de pruebas | Microsoft Docs"  
[WebdriverChromiumDownloadMicrosoftEdgeDriver]: ../../webdriver-chromium/index.md#download-microsoft-edge-driver "Descargar controlador de Microsoft Edge: use WebDriver (Chromium) para la automatización de pruebas | Microsoft Docs"  
[WebViewIndex]: ../index.md "Introducción a Microsoft Edge WebView2 : Microsoft Docs"  
[Webview2ReleaseNotes]: ../release-notes.md "Notas de la versión de WebView2 SDK | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeWebDriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar WebDriver | Desarrollador de Microsoft Edge"  

[GithubMicrosoftedgewebview2samplesSampleappsWebview2apisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisamplePrerequisites]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample#prerequisites "Requisitos previos: ejemplo de API de WebView2 | GitHub"  

[NugetSeleniumWebdriver400Alpha04]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04 "Selenium.WebDriver 4.0.0-alpha04 | Galería nuGet"  

[SeleniumWebdriver]: https://www.selenium.dev/documentation/en/webdriver "WebDriver | Selenio"  

[W3cWebdriver2]: https://www.w3.org/TR/webdriver2 "WebDriver | W3C"  

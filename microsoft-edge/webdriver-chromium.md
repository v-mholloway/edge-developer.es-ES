---
description: Obtenga información sobre cómo probar su sitio web o aplicación en Microsoft Edge o automatizar el explorador con Webdriver.
title: WebDriver (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, WebDrive, Selenium, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: 8170820d7809f7c4c07f21c815f17a9438016305
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986216"
---
# <span data-ttu-id="04d6c-104">Usar Webdriver (cromo) para automatización de prueba</span><span class="sxs-lookup"><span data-stu-id="04d6c-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="04d6c-105">Webdriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="04d6c-105">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="04d6c-106">Las pruebas y simuladores de WebDrive se diferencian de las pruebas unitarias de JavaScript por las siguientes razones:</span><span class="sxs-lookup"><span data-stu-id="04d6c-106">WebDriver tests and simulations differ from JavaScript unit tests because of the following reasons.</span></span> 
*   <span data-ttu-id="04d6c-107">Accede a la funcionalidad y la información que no están disponibles para JavaScript que se ejecuta en exploradores.</span><span class="sxs-lookup"><span data-stu-id="04d6c-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="04d6c-108">Simula eventos de usuario o eventos a nivel de OS de forma más precisa.</span><span class="sxs-lookup"><span data-stu-id="04d6c-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="04d6c-109">Administra las pruebas en varias ventanas, pestañas y páginas web en una sola sesión de prueba.</span><span class="sxs-lookup"><span data-stu-id="04d6c-109">Manages testing across multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="04d6c-110">Ejecuta varias sesiones de Microsoft Edge en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="04d6c-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  

<span data-ttu-id="04d6c-111">En la siguiente sección se describe cómo empezar a usar Webdriver para Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="04d6c-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="04d6c-112">Instalar Microsoft Edge (cromo)</span><span class="sxs-lookup"><span data-stu-id="04d6c-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="04d6c-113">Asegúrate de instalar [Microsoft Edge (cromo)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="04d6c-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="04d6c-114">Para confirmar que tiene Microsoft Edge (cromo) instalado, vaya a `edge://settings/help` en el explorador y compruebe que el número de versión es la versión 75 o posterior.</span><span class="sxs-lookup"><span data-stu-id="04d6c-114">To confirm that you have Microsoft Edge (Chromium) installed, go to `edge://settings/help` in the browser, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="04d6c-115">Descargar el controlador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04d6c-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="04d6c-116">Para empezar a automatizar las pruebas, siga estos pasos para asegurarse de que la versión de Webdriver que instale coincide con la versión del explorador.</span><span class="sxs-lookup"><span data-stu-id="04d6c-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="04d6c-117">Vaya a `edge://settings/help` para obtener la versión de Edge.</span><span class="sxs-lookup"><span data-stu-id="04d6c-117">Go to `edge://settings/help` to get the version of Edge.</span></span>  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="El número de compilación para Microsoft Edge Canarias el 14 de enero de 2020":::
       <span data-ttu-id="04d6c-119">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="04d6c-119">Figure 1.</span></span>  <span data-ttu-id="04d6c-120">El número de compilación para Microsoft Edge Canarias el 14 de enero de 2020</span><span class="sxs-lookup"><span data-stu-id="04d6c-120">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="04d6c-121">Vaya a la página de [descargas del controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] y descargue el controlador que coincida con el número de versión de Edge.</span><span class="sxs-lookup"><span data-stu-id="04d6c-121">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the Edge version number.</span></span>  
    
    :::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Sección de descargas de la página del controlador de Microsoft Edge":::
       <span data-ttu-id="04d6c-123">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="04d6c-123">Figure 2.</span></span>  <span data-ttu-id="04d6c-124">Sección de descargas de la página del [controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="04d6c-124">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    > [!NOTE] 
    > <span data-ttu-id="04d6c-125">Para obtener más información sobre la automatización de prueba con Microsoft Edge (EdgeHTML), vea [Microsoft Webdriver para Microsoft Edge (EdgeHTML)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="04d6c-125">For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].</span></span>  

## <span data-ttu-id="04d6c-126">Elegir un enlace de idioma de controlador</span><span class="sxs-lookup"><span data-stu-id="04d6c-126">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="04d6c-127">El último componente que debe descargar es un controlador de cliente específico del idioma para traducir su código \ (Python, Java, C \ #, Ruby, JavaScript \) en comandos el controlador de Microsoft Edge se ejecuta en Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="04d6c-127">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="04d6c-128">[Descargue el enlace de idioma de Webdrives que prefiera][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="04d6c-128">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="04d6c-129">El equipo de Microsoft Edge recomienda [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] o posterior, porque es compatible con Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="04d6c-129">The Microsoft Edge team recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="04d6c-130">Sin embargo, puedes controlar Microsoft Edge \ (cromo \) en todas las versiones anteriores de Selenium, incluida la versión estable actual de Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="04d6c-130">However, you are able to control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="04d6c-131">Si anteriormente estabas automatizando o probando Microsoft Edge \ (cromo \) mediante `ChromeDriver` `ChromeOptions` clases, el código de Webdriver no se ejecuta en Microsoft edge versión 80 o posterior.</span><span class="sxs-lookup"><span data-stu-id="04d6c-131">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="04d6c-132">Para solucionar este problema, actualiza las pruebas para usar la `EdgeOptions` clase e instalar el [controlador Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="04d6c-132">To solve this problem, update your tests to use the `EdgeOptions` class and install [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="04d6c-133">Usar Selenium 3</span><span class="sxs-lookup"><span data-stu-id="04d6c-133">Use Selenium 3</span></span>  

<span data-ttu-id="04d6c-134">Si ya usas [Selenium 3][|::ref1::|], es posible que tengas pruebas de explorador existentes y quieras agregar cobertura para Microsoft Edge \ (cromo \) sin cambiar tu versión de Selenium.</span><span class="sxs-lookup"><span data-stu-id="04d6c-134">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="04d6c-135">Para usar [Selenium 3][|::ref2::|] para escribir pruebas automatizadas de Microsoft Edge \ (EdgeHTML \) y Microsoft Edge \ (cromo \), instale el paquete [de herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar el controlador actualizado.</span><span class="sxs-lookup"><span data-stu-id="04d6c-135">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="04d6c-136">Las `EdgeDriver` `EdgeDriverService` clases y incluidas en las herramientas son totalmente compatibles con los equivalentes integrados en Selenium 4.</span><span class="sxs-lookup"><span data-stu-id="04d6c-136">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="04d6c-137">Siga estos pasos para agregar las [herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] y [Selenium 3][|::ref3::|] al proyecto.</span><span class="sxs-lookup"><span data-stu-id="04d6c-137">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<span data-ttu-id="04d6c-138">C#</span><span class="sxs-lookup"><span data-stu-id="04d6c-138">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="04d6c-139">Agrega los paquetes [Microsoft. Edge. SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] y [Selenium. Webdriver][NugetPackagesSeleniumWebdriver31410] a tu proyecto de .net mediante la [CLI de NuGet][NugetCLI] o [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="04d6c-139">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>

#### [<span data-ttu-id="04d6c-140">Fundación</span><span class="sxs-lookup"><span data-stu-id="04d6c-140">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="04d6c-141">Use [PIP][PythonPip] para instalar el [msedge-Selenium-herramientas][PythonSeleniumTools] y paquetes de [Selenium][PythonSelenium] :</span><span class="sxs-lookup"><span data-stu-id="04d6c-141">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages:</span></span>

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="04d6c-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="04d6c-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="04d6c-143">Use [NPM][JavaScript|::ref4::|] para instalar los paquetes [Edge-Selenium-Tools][JavaScriptSeleniumTools] y [Selenium-Webdriver][JavaScriptSelenium] :</span><span class="sxs-lookup"><span data-stu-id="04d6c-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages:</span></span>

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="04d6c-144">Usar Microsoft Edge (cromo) con Webdriver</span><span class="sxs-lookup"><span data-stu-id="04d6c-144">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="04d6c-145">Puede ejecutar los siguientes ejemplos con Selenium 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="04d6c-145">You may run the following examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="04d6c-146">Para usar con Selenium 3, el paquete [de herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] debe estar instalado.</span><span class="sxs-lookup"><span data-stu-id="04d6c-146">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="04d6c-147">Uso básico</span><span class="sxs-lookup"><span data-stu-id="04d6c-147">Basic Usage</span></span>  

<span data-ttu-id="04d6c-148">Para usar con Microsoft Edge \ (EdgeHTML \), simplemente cree una instancia predeterminada de la `EdgeDriver` clase.</span><span class="sxs-lookup"><span data-stu-id="04d6c-148">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="04d6c-149">C#</span><span class="sxs-lookup"><span data-stu-id="04d6c-149">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code"></a>  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="04d6c-150">Fundación</span><span class="sxs-lookup"><span data-stu-id="04d6c-150">Python</span></span>](#tab/python/)  

<a id="basic-usage-code"></a>  

```python
driver = Edge()
```  

#### [<span data-ttu-id="04d6c-151">JavaScript</span><span class="sxs-lookup"><span data-stu-id="04d6c-151">JavaScript</span></span>](#tab/javascript/)  

<a id="basic-usage-code"></a>  

```javascript
let driver = edge.Driver.createSession();
```  

* * *  

### <span data-ttu-id="04d6c-152">Conduciendo Microsoft Edge (cromo)</span><span class="sxs-lookup"><span data-stu-id="04d6c-152">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="04d6c-153">Para usar con Microsoft Edge \ (cromo \), cree una `EdgeDriver` clase nueva y pásele el `EdgeOptions` objeto con la `UseChromium` propiedad establecida en `true` .</span><span class="sxs-lookup"><span data-stu-id="04d6c-153">To use with Microsoft Edge \(Chromium\), create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="04d6c-154">C#</span><span class="sxs-lookup"><span data-stu-id="04d6c-154">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="04d6c-155">Fundación</span><span class="sxs-lookup"><span data-stu-id="04d6c-155">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="04d6c-156">JavaScript</span><span class="sxs-lookup"><span data-stu-id="04d6c-156">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="04d6c-157">Si la directiva [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] se establece en `2` , el [controlador Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] no podrá conducir a [Microsoft Edge (cromo)][MicrosoftEdge] porque el controlador usa la DevTools de [Microsoft Edge][DevToolsMain].</span><span class="sxs-lookup"><span data-stu-id="04d6c-157">If the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy is set to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive [Microsoft Edge (Chromium)][MicrosoftEdge] because the driver uses the [Microsoft Edge DevTools][DevToolsMain].</span></span>  <span data-ttu-id="04d6c-158">Asegúrate de establecer la [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] política de DeveloperToolsAvailability `0` o `1` para automatizar [Microsoft Edge (cromo)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="04d6c-158">Ensure you set the [DeveloperToolsAvailability][DeployedgePoliciesDevelopertoolsavailability] policy to `0` or `1` to automate [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  

### <span data-ttu-id="04d6c-159">Elección de archivos binarios de explorador específicos (solo cromo)</span><span class="sxs-lookup"><span data-stu-id="04d6c-159">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="04d6c-160">Puede usar la `EdgeOptions` clase con binarios específicos de Microsoft Edge (cromo).</span><span class="sxs-lookup"><span data-stu-id="04d6c-160">You may use the `EdgeOptions` class with specific binaries of Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="04d6c-161">Por ejemplo, puede ejecutar pruebas usando los [canales de Microsoft Edge Preview][MicrosoftedgeinsiderDownload] , como Microsoft Edge beta.</span><span class="sxs-lookup"><span data-stu-id="04d6c-161">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="04d6c-162">C#</span><span class="sxs-lookup"><span data-stu-id="04d6c-162">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="04d6c-163">Fundación</span><span class="sxs-lookup"><span data-stu-id="04d6c-163">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="04d6c-164">JavaScript</span><span class="sxs-lookup"><span data-stu-id="04d6c-164">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="04d6c-165">Personalizar el servicio del controlador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04d6c-165">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="04d6c-166">C#</span><span class="sxs-lookup"><span data-stu-id="04d6c-166">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="04d6c-167">Cuando `EdgeDriver` se crea una instancia de clase con `EdgeOptions` Class, se crea e inicia la `EdgeDriverService` clase adecuada para Microsoft Edge \ (EdgeHTML \) o Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="04d6c-167">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="04d6c-168">Si desea crear un `EdgeDriverService` , cree uno configurado para Microsoft Edge \ (cromo \) con el `CreateChromiumService()` método.</span><span class="sxs-lookup"><span data-stu-id="04d6c-168">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="04d6c-169">Es posible que le resulte útil para personalizaciones adicionales, como habilitar la salida de registro detallado en el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="04d6c-169">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="04d6c-170">No es necesario proporcionar el `EdgeOptions` objeto cuando se pasa `EdgeDriverService` a la `EdgeDriver` instancia.</span><span class="sxs-lookup"><span data-stu-id="04d6c-170">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span> <span data-ttu-id="04d6c-171">La `EdgeDriver` clase usa las opciones predeterminadas para Microsoft Edge \ (EdgeHTML \) o Microsoft Edge \ (cromo \) según el servicio que proporcionaste.</span><span class="sxs-lookup"><span data-stu-id="04d6c-171">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on the service you provide.</span></span>  
> <span data-ttu-id="04d6c-172">Sin embargo, si desea proporcionar ambos `EdgeDriverService` y `EdgeOptions` clases, asegúrese de que ambos están configurados para la misma versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="04d6c-172">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="04d6c-173">Por ejemplo, no es posible usar una clase predeterminada de Microsoft Edge (EdgeHTML) `EdgeDriverService` y propiedades de cromo en la `EdgeOptions` clase.</span><span class="sxs-lookup"><span data-stu-id="04d6c-173">For example, it is not possible to use a default Microsoft Edge (EdgeHTML) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="04d6c-174">La `EdgeDriver` clase produce un error para evitar el uso de versiones diferentes.</span><span class="sxs-lookup"><span data-stu-id="04d6c-174">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="04d6c-175">Fundación</span><span class="sxs-lookup"><span data-stu-id="04d6c-175">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="04d6c-176">Al usar Python, el `Edge` objeto crea y administra el `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="04d6c-176">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="04d6c-177">Para configurar el `EdgeService` , pase argumentos adicionales al `Edge` objeto, tal y como se indica en el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="04d6c-177">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="04d6c-178">JavaScript</span><span class="sxs-lookup"><span data-stu-id="04d6c-178">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="04d6c-179">Al usar JavaScript, cree y configure una `Service` con la `ServiceBuilder` clase.</span><span class="sxs-lookup"><span data-stu-id="04d6c-179">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="04d6c-180">De manera opcional, puede pasar el `Service` objeto al `Driver` objeto que inicia y detiene el servicio por usted.</span><span class="sxs-lookup"><span data-stu-id="04d6c-180">You may optionally pass the `Service` object to the `Driver` object which starts and stops the service for you.</span></span>  
<span data-ttu-id="04d6c-181">Para configurar el `Service` , ejecute métodos adicionales en la `ServiceBuilder` clase antes de usar el `build()` método.</span><span class="sxs-lookup"><span data-stu-id="04d6c-181">To configure the `Service`, run additional methods in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="04d6c-182">Después, pasa el `service` as como un parámetro en el `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="04d6c-182">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * * 

### <span data-ttu-id="04d6c-183">Usar opciones específicas de cromo</span><span class="sxs-lookup"><span data-stu-id="04d6c-183">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="04d6c-184">Si establece la `UseChromium` propiedad en `true` , puede usar la `EdgeOptions` clase para obtener acceso a las mismas [propiedades y métodos específicos del cromo][SeleniumWebDriverChromeoptionsClass] que cuando automatiza otros exploradores de cromo.</span><span class="sxs-lookup"><span data-stu-id="04d6c-184">If you set the `UseChromium` property to `true`, you are able to use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] as when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="04d6c-185">C#</span><span class="sxs-lookup"><span data-stu-id="04d6c-185">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="04d6c-186">Fundación</span><span class="sxs-lookup"><span data-stu-id="04d6c-186">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="04d6c-187">JavaScript</span><span class="sxs-lookup"><span data-stu-id="04d6c-187">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```

* * *  
> [!NOTE]
> <span data-ttu-id="04d6c-188">Si la `UseChromium` propiedad se establece en `true` , no podrá usar propiedades y métodos para Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="04d6c-188">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="04d6c-189">Opciones adicionales de instalación de Webdriver</span><span class="sxs-lookup"><span data-stu-id="04d6c-189">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="04d6c-190">Chocolate</span><span class="sxs-lookup"><span data-stu-id="04d6c-190">Chocolatey</span></span>  

<span data-ttu-id="04d6c-191">Si usas [chocolate][Chocolatey] como el administrador de paquetes, instala el controlador Microsoft Edge ejecutando el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="04d6c-191">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="04d6c-192">Para obtener más información, consulta el [controlador de Selenium de cromo en chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="04d6c-192">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="04d6c-193">Docker</span><span class="sxs-lookup"><span data-stu-id="04d6c-193">Docker</span></span>  

<span data-ttu-id="04d6c-194">Si usas el [acoplador][DockerHub], descarga una imagen preconfigurada con Microsoft Edge \ (cromo \) y el [controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] preinstalado ejecutando el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="04d6c-194">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="04d6c-195">Para obtener más información, consulte [contenedor en el concentrador de acoplamiento][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="04d6c-195">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="04d6c-196">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="04d6c-196">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="04d6c-197">El equipo de Microsoft Edge está ansioso por escuchar tus comentarios sobre el uso de Webdriver, Selenium y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="04d6c-197">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="04d6c-198">Use el icono de **comentarios** en las [@EdgeDevTools][TwitterTweetEdgeDevTools] de Microsoft Edge DevTools o Tweet para que el equipo sepa lo que piensa.</span><span class="sxs-lookup"><span data-stu-id="04d6c-198">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono enviar comentarios en el DevTools de Microsoft Edge":::
   <span data-ttu-id="04d6c-200">El icono **Enviar comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="04d6c-200">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[DevToolsMain]: ./devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"
[Webdriver]: ./webdriver.md "Webdriver (EdgeHTML) | Microsoft docs"  

[DeployedgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability-Microsoft Edge-Policies | Microsoft docs"  

[Chocolatey]: https://chocolatey.org "Chocolate | Software de chocolate"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Controlador de borde de cromo de Selenium | Chocolate"  

[DockerHub]: https://hub.docker.com "Concentrador de acoplamiento"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Concentrador de acoplamiento"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selenium | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "NPM"
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/Edge-Selenium-Tools | NPM"
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "Selenium-Webdriver | NPM"

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Controlador WebDrive | Microsoft Developer"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Descargas: Webdriver | Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar nuevo explorador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | Galería de NuGet"
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium. WebDrive 3.141.0 | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium. WebDrive 4.0.0-alpha05 | Galería de NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "PIP | PyPI"
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-Selenium-herramientas | PyPI"
[PythonSelenium]: https://pypi.org/project/selenium/ "Selenium | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Descargas | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Clase ChromeOptions: Webdriver | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"

[W3CWebdriver]: https://w3.org/TR/webdriver2 "Controlador WebDrive"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin periféricos | Wikipedia"  

---
description: Obtenga información sobre cómo probar su sitio web o aplicación en Microsoft Edge o automatizar el explorador con WebDriver.
title: Usar WebDriver (Chromium) para la automatización de pruebas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, html, css, javascript, programador, webdriver, se sintaxis, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: 295985734d93c5912922be22c0af0c0e33e00a54
ms.sourcegitcommit: 070a60f634908eea0e29e260331f9fc0aa85ee78
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/30/2021
ms.locfileid: "11306251"
---
# <span data-ttu-id="820ae-104">Usar WebDriver (Chromium) para la automatización de pruebas</span><span class="sxs-lookup"><span data-stu-id="820ae-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="820ae-105">WebDriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="820ae-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="820ae-106">Las pruebas y simulaciones de WebDriver difieren de las pruebas unitarias de JavaScript porque WebDriver:</span><span class="sxs-lookup"><span data-stu-id="820ae-106">WebDriver tests and simulations differ from JavaScript unit tests because WebDriver:</span></span>  

*   <span data-ttu-id="820ae-107">Accede a la funcionalidad y la información que no están disponibles para JavaScript que se ejecuta en exploradores.</span><span class="sxs-lookup"><span data-stu-id="820ae-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="820ae-108">Simula eventos de usuario o eventos de nivel de sistema operativo de forma más precisa.</span><span class="sxs-lookup"><span data-stu-id="820ae-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="820ae-109">Administra varias ventanas, pestañas y páginas web en una sola sesión de prueba.</span><span class="sxs-lookup"><span data-stu-id="820ae-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="820ae-110">Ejecuta varias sesiones de Microsoft Edge en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="820ae-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="820ae-111">En la siguiente sección se describe cómo empezar a usar WebDriver para Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="820ae-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="820ae-112">Instalar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="820ae-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="820ae-113">Asegúrese de instalar [Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="820ae-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="820ae-114">Para confirmar que tiene Microsoft Edge \(Chromium\) instalado, vaya a y compruebe que el número de versión sea la `edge://settings/help` versión 75 o posterior.</span><span class="sxs-lookup"><span data-stu-id="820ae-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is Version 75 or later.</span></span>  

## <span data-ttu-id="820ae-115">Descargar controlador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="820ae-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="820ae-116">Para comenzar las pruebas de automatización, siga estos pasos para asegurarse de que la versión de WebDriver que instale coincida con la versión del explorador.</span><span class="sxs-lookup"><span data-stu-id="820ae-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="820ae-117">Navegue para `edge://settings/help` obtener la versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="820ae-117">Navigate to `edge://settings/help` to get the version of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-version.png" alt-text="El número de compilación de Microsoft Edge Canary el 14 de enero de 2020":::
       <span data-ttu-id="820ae-119">El número de compilación de Microsoft Edge Canary el 14 de enero de 2020</span><span class="sxs-lookup"><span data-stu-id="820ae-119">The build number for Microsoft Edge Canary on January 14, 2020</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="820ae-120">Navegue a la página [de descargas de controladores de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads] y descargue el controlador que coincida con el número de versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="820ae-120">Navigate to the [Microsoft Edge Driver downloads][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page and download the driver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/edge-driver-install.png" alt-text="La sección Descargas de la página Controlador de Microsoft Edge":::
       <span data-ttu-id="820ae-122">La sección Descargas de la [página Controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="820ae-122">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] page</span></span>
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge (EdgeHTML), see [Microsoft WebDriver for Microsoft Edge (EdgeHTML)][Webdriver].  
    -->  

## <span data-ttu-id="820ae-123">Elegir un enlace de idioma de WebDriver</span><span class="sxs-lookup"><span data-stu-id="820ae-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="820ae-124">El último componente que debes descargar es un controlador de cliente específico del idioma para traducir el código \(Python, Java, C\#, Ruby, JavaScript\) en comandos que el controlador de Microsoft Edge ejecuta en Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="820ae-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="820ae-125">[Descargue el enlace de idioma de WebDriver de su elección.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="820ae-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="820ae-126">El equipo de Microsoft Edge recomienda [Usar 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] o posterior, porque es compatible con Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="820ae-126">The Microsoft Edge team recommends [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="820ae-127">Sin embargo, puedes controlar Microsoft Edge \(Chromium\) en todas las versiones anteriores de Se sint, incluida la versión estable actual de Se sint 3.</span><span class="sxs-lookup"><span data-stu-id="820ae-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="820ae-128">Si anteriormente estaba automatizando o probando Microsoft Edge \(Chromium\) usando y clases, el código de WebDriver no se ejecuta en `ChromeDriver` `ChromeOptions` Microsoft Edge versión 80 o posterior.</span><span class="sxs-lookup"><span data-stu-id="820ae-128">If you were previously automating or testing Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="820ae-129">Para solucionar este problema, actualice las pruebas para usar la `EdgeOptions` clase y descargue el controlador de Microsoft [Edge.][MicrosoftDeveloperEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="820ae-129">To solve this problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="820ae-130">Usar Se desenlaz 3</span><span class="sxs-lookup"><span data-stu-id="820ae-130">Use Selenium 3</span></span>  

<span data-ttu-id="820ae-131">Si ya [usas Seleán 3,][|::ref1::|]es posible que ya tienes pruebas de explorador y quieras agregar cobertura para Microsoft Edge \(Chromium\) sin cambiar la versión de Sende.</span><span class="sxs-lookup"><span data-stu-id="820ae-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="820ae-132">Para usar [Seprocesamiento 3][|::ref2::|] para escribir pruebas automatizadas tanto para Microsoft Edge \(EdgeHTML\) como para Microsoft Edge \(Chromium\), instala el paquete [Herramientas de Seprocesamiento][GithubMicrosoftEdgeSeleniumTools] para Microsoft Edge para usar el controlador actualizado.</span><span class="sxs-lookup"><span data-stu-id="820ae-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="820ae-133">Las clases y las clases incluidas en las herramientas son totalmente compatibles con `EdgeDriver` `EdgeDriverService` los equivalentes integrados en Se siny 4.</span><span class="sxs-lookup"><span data-stu-id="820ae-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="820ae-134">Siga los pasos siguientes para agregar [las Herramientas de selenio para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] y Se [siny 3][|::ref3::|] al proyecto.</span><span class="sxs-lookup"><span data-stu-id="820ae-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<span data-ttu-id="820ae-135">C#</span><span class="sxs-lookup"><span data-stu-id="820ae-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="820ae-136">Agregue los [paquetes Microsoft.Edge.Setools y][NugetPackagesMicrosoftEdgeSeleniumtools] [Setools.WebDriver][NugetPackagesSeleniumWebdriver31410] a su proyecto .NET con la CLI de [NuGet][NugetCLI] [o Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="820ae-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="820ae-137">Python</span><span class="sxs-lookup"><span data-stu-id="820ae-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="820ae-138">Usa [pip][PythonPip] para instalar los [paquetes msedge-seprocesamiento-tools][PythonSeleniumTools] y [se siny.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="820ae-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="820ae-139">Java</span><span class="sxs-lookup"><span data-stu-id="820ae-139">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="820ae-140">Si el Java usa Maven, agrega [msedge-se javascript-tools-java][SonatypeMavenRepositorySearch] haciendo frente a la siguiente dependencia en el `pom.xml` archivo:</span><span class="sxs-lookup"><span data-stu-id="820ae-140">If your Java project uses Maven, add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch] by coping the following dependency to your `pom.xml` file:</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="820ae-141">El Java paquete también está disponible para descargar directamente en la página [Herramientas de disponibilidad para versiones de Microsoft Edge.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="820ae-141">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<span data-ttu-id="820ae-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="820ae-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="820ae-143">Use [npm][JavaScript|::ref4::|] para instalar los [paquetes edge-seprocesamiento-tools][JavaScriptSeleniumTools] y [seprocesamiento-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="820ae-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="820ae-144">Automatizar Microsoft Edge (Chromium) con WebDriver</span><span class="sxs-lookup"><span data-stu-id="820ae-144">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="820ae-145">Para automatizar un explorador con WebDriver, primero debe iniciar una sesión de WebDriver con el enlace de idioma de WebDriver que prefiera.</span><span class="sxs-lookup"><span data-stu-id="820ae-145">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="820ae-146">Una sesión es una única instancia en ejecución de un explorador que se puede controlar mediante comandos de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="820ae-146">A session is a single running instance of a browser that can be controlled using WebDriver commands.</span></span>  <span data-ttu-id="820ae-147">Al iniciar una sesión de WebDriver se inicia una nueva instancia del explorador.</span><span class="sxs-lookup"><span data-stu-id="820ae-147">Starting a WebDriver session launches a new browser instance.</span></span>  <span data-ttu-id="820ae-148">El explorador que se inicia permanece abierto hasta que cierra la sesión de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="820ae-148">The browser that is launched remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="820ae-149">El siguiente contenido le guiará a través del uso de Se a continuación para iniciar una sesión de WebDriver con Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="820ae-149">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="820ae-150">Puede ejecutar estos ejemplos con Se siny 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="820ae-150">You may run theses examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="820ae-151">Para usar con Se desenlaz 3, se debe instalar el paquete [Herramientas de sesón][GithubMicrosoftEdgeSeleniumTools] para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="820ae-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="820ae-152">Automatización de Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="820ae-152">Automating Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="820ae-153">Sende usa la `EdgeDriver` clase para administrar una sesión de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="820ae-153">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span> <span data-ttu-id="820ae-154">Para iniciar una sesión y automatizar Microsoft Edge \(Chromium\), cree un nuevo objeto y pásle un objeto con la `EdgeDriver` `EdgeOptions` propiedad establecida en `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="820ae-154">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="820ae-155">C#</span><span class="sxs-lookup"><span data-stu-id="820ae-155">C#</span></span>](#tab/c-sharp/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="820ae-156">Python</span><span class="sxs-lookup"><span data-stu-id="820ae-156">Python</span></span>](#tab/python/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="820ae-157">Java</span><span class="sxs-lookup"><span data-stu-id="820ae-157">Java</span></span>](#tab/java/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="820ae-158">La clase solo admite Microsoft Edge (Chromium) y no `EdgeDriver` admite Microsoft Edge (EdgeHTML).</span><span class="sxs-lookup"><span data-stu-id="820ae-158">The `EdgeDriver` class supports Microsoft Edge (Chromium) only, and does not support Microsoft Edge (EdgeHTML).</span></span> <span data-ttu-id="820ae-159">Para el uso básico, puede crear una `EdgeDriver` sin proporcionar `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="820ae-159">For basic usage, you may create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<span data-ttu-id="820ae-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="820ae-160">JavaScript</span></span>](#tab/javascript/)  

<a id="driving-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="820ae-161">Si el administrador de TI ha establecido la directiva [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] en , El controlador de Microsoft Edge no puede impulsar Microsoft Edge (Chromium) porque el controlador usa las `2` [][MicrosoftDeveloperEdgeToolsWebdriver] [DevTools de Microsoft Edge][DevtoolsIndex].</span><span class="sxs-lookup"><span data-stu-id="820ae-161">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`, [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] is not be able to drive Microsoft Edge (Chromium) because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="820ae-162">Asegúrate de [que la directiva DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] esté establecida en o para automatizar `0` Microsoft Edge `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="820ae-162">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <span data-ttu-id="820ae-163">Elección de binarios de explorador específicos (solo chromium)</span><span class="sxs-lookup"><span data-stu-id="820ae-163">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="820ae-164">Puede iniciar una sesión de WebDriver con archivos binarios específicos de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="820ae-164">You may start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="820ae-165">Por ejemplo, puede ejecutar pruebas con los canales de vista previa de [Microsoft Edge,][MicrosoftedgeinsiderDownload] como Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="820ae-165">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="820ae-166">C#</span><span class="sxs-lookup"><span data-stu-id="820ae-166">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="820ae-167">Python</span><span class="sxs-lookup"><span data-stu-id="820ae-167">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="820ae-168">Java</span><span class="sxs-lookup"><span data-stu-id="820ae-168">Java</span></span>](#tab/java/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="820ae-169">JavaScript</span><span class="sxs-lookup"><span data-stu-id="820ae-169">JavaScript</span></span>](#tab/javascript/)  

<a id="choosing-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="820ae-170">Personalización del servicio de controladores de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="820ae-170">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="820ae-171">C#</span><span class="sxs-lookup"><span data-stu-id="820ae-171">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="820ae-172">Cuando se crea una instancia de clase mediante clase, crea e inicia la clase adecuada para `EdgeDriver` `EdgeOptions` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) o Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="820ae-172">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="820ae-173">Si quieres crear una, crea una configurada `EdgeDriverService` para Microsoft Edge \(Chromium\) mediante el `CreateChromiumService()` método.</span><span class="sxs-lookup"><span data-stu-id="820ae-173">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="820ae-174">Es posible que le sea útil cuando necesite agregar personalizaciones.</span><span class="sxs-lookup"><span data-stu-id="820ae-174">You may find it useful when you need to add customizations.</span></span> <span data-ttu-id="820ae-175">Por ejemplo, el siguiente código inicia la salida del registro detallado.</span><span class="sxs-lookup"><span data-stu-id="820ae-175">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="820ae-176">No es necesario proporcionar el objeto `EdgeOptions` al pasar a la `EdgeDriverService` `EdgeDriver` instancia.</span><span class="sxs-lookup"><span data-stu-id="820ae-176">You do not need to provide the `EdgeOptions` object when passing `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="820ae-177">La clase usa las opciones predeterminadas para `EdgeDriver` Microsoft Edge \(EdgeHTML\) o Microsoft Edge \(Chromium\) en función del servicio que proporciones.</span><span class="sxs-lookup"><span data-stu-id="820ae-177">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="820ae-178">Sin embargo, si desea proporcionar ambos y clases, asegúrese de que ambos están configurados `EdgeDriverService` para la misma versión de Microsoft `EdgeOptions` Edge.</span><span class="sxs-lookup"><span data-stu-id="820ae-178">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="820ae-179">Por ejemplo, no es posible usar una clase predeterminada de Microsoft Edge \(EdgeHTML\) y propiedades `EdgeDriverService` chromium en la `EdgeOptions` clase.</span><span class="sxs-lookup"><span data-stu-id="820ae-179">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="820ae-180">La `EdgeDriver` clase produce un error para evitar el uso de diferentes versiones.</span><span class="sxs-lookup"><span data-stu-id="820ae-180">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="820ae-181">Python</span><span class="sxs-lookup"><span data-stu-id="820ae-181">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="820ae-182">Al usar Python, `Edge` el objeto crea y administra el archivo `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="820ae-182">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="820ae-183">Para configurar el `EdgeService` , pase argumentos adicionales al objeto como se indica en el siguiente `Edge` código.</span><span class="sxs-lookup"><span data-stu-id="820ae-183">To configure the `EdgeService`, pass additional arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="820ae-184">Java</span><span class="sxs-lookup"><span data-stu-id="820ae-184">Java</span></span>](#tab/java/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="820ae-185">Usa el `createDefaultService()` método para crear una configuración para Microsoft Edge `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="820ae-185">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span> <span data-ttu-id="820ae-186">Los servicios de controladores Java se personalizan mediante Java propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="820ae-186">Driver services in Java are customized using Java system properties.</span></span> <span data-ttu-id="820ae-187">Por ejemplo, el siguiente código usa la `"webdriver.edge.verboseLogging"` propiedad para habilitar la salida del registro detallado.</span><span class="sxs-lookup"><span data-stu-id="820ae-187">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to enable verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<span data-ttu-id="820ae-188">JavaScript</span><span class="sxs-lookup"><span data-stu-id="820ae-188">JavaScript</span></span>](#tab/javascript/)  

<a id="customizing-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="820ae-189">Al usar JavaScript, cree y configure una `Service` con la `ServiceBuilder` clase.</span><span class="sxs-lookup"><span data-stu-id="820ae-189">When using JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="820ae-190">Opcionalmente, puedes pasar el objeto al objeto, que inicia `Service` `Driver` \(y detiene\) el servicio por ti.</span><span class="sxs-lookup"><span data-stu-id="820ae-190">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="820ae-191">Para configurar el `Service` método , ejecute otro método en la clase antes de usar el `ServiceBuilder` `build()` método.</span><span class="sxs-lookup"><span data-stu-id="820ae-191">To configure the `Service`, run another method in the `ServiceBuilder` class before using the `build()` method.</span></span>  <span data-ttu-id="820ae-192">A continuación, `service` pase el parámetro como en el `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="820ae-192">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="820ae-193">Usar Chromium-Specific opciones</span><span class="sxs-lookup"><span data-stu-id="820ae-193">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="820ae-194">Si estableces la propiedad en , puedes usar la clase para tener acceso a las mismas propiedades y métodos específicos de Chromium que se usan al automatizar otros exploradores `UseChromium` `true` `EdgeOptions` chromium. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="820ae-194">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when automating other Chromium browsers.</span></span>  

#### [<span data-ttu-id="820ae-195">C#</span><span class="sxs-lookup"><span data-stu-id="820ae-195">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="820ae-196">Python</span><span class="sxs-lookup"><span data-stu-id="820ae-196">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="820ae-197">Java</span><span class="sxs-lookup"><span data-stu-id="820ae-197">Java</span></span>](#tab/java/)  

<a id="using-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<span data-ttu-id="820ae-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="820ae-198">JavaScript</span></span>](#tab/javascript/)  

<a id="using-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="820ae-199">Si la propiedad se establece en , no podrá usar propiedades y métodos para `UseChromium` `true` Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="820ae-199">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="820ae-200">Opciones de instalación adicionales de WebDriver</span><span class="sxs-lookup"><span data-stu-id="820ae-200">Additional WebDriver installation options</span></span>  

### <span data-ttu-id="820ae-201">Resalte</span><span class="sxs-lookup"><span data-stu-id="820ae-201">Chocolatey</span></span>  

<span data-ttu-id="820ae-202">Si [usas a Cargoy][Chocolatey] como administrador de paquetes, instala el controlador de Microsoft Edge ejecutando el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="820ae-202">If you use [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="820ae-203">Para obtener más información, consulta [Se chromium Edge Driver en Odbcy][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="820ae-203">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="820ae-204">Docker</span><span class="sxs-lookup"><span data-stu-id="820ae-204">Docker</span></span>  

<span data-ttu-id="820ae-205">Si usa [Docker,][DockerHub]descargue una imagen preconfigurada con Microsoft Edge \(Chromium\) y el controlador [de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] preinstalados ejecutando el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="820ae-205">If you use [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] pre-installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="820ae-206">Para obtener más información, vaya al [contenedor msedgedriver en Docker Hub.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="820ae-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="820ae-207">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="820ae-207">Next steps</span></span>

<span data-ttu-id="820ae-208">Para obtener más información sobre WebDriver y cómo escribir pruebas automatizadas de WebDriver con Serío, vaya a la documentación [de Se automatri.][SeleniumDocumentation]</span><span class="sxs-lookup"><span data-stu-id="820ae-208">To learn more about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <span data-ttu-id="820ae-209">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="820ae-209">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="820ae-210">El equipo de Microsoft Edge está deseando escuchar sus comentarios sobre el uso de WebDriver, Se sin embargo y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="820ae-210">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="820ae-211">Para enviar al equipo sus preguntas \*\*\*\* y comentarios, elija el icono Enviar comentarios en las DevTools de Microsoft Edge o envíe un tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="820ae-211">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Las DevTools de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="820ae-213">El **icono Enviar comentarios** en Las DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="820ae-213">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funcionalidades y opciones de EdgeOptions | Microsoft Docs"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge - Directivas | Microsoft Docs"  

[Chocolatey]: https://chocolatey.org "| Software Desalbado"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Controlador de borde Se chromium | Resalte"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Docker Hub"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-seprocesamiento-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-seprocesamiento-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SehidánHQ/sehidán | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-seprocesamiento-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "se siny-webdriver | npm"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Microsoft Developer"  
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Descargas- WebDriver | Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar el nuevo explorador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | Galería de NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.Setools | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Se siny.WebDriver 3.141.0 | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Se siny.WebDriver 4.0.0-alpha07 | Galería de NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-seprocesamiento-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "se siny | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SenioHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "El proyecto de automatización del explorador Se de Se siny:: Documentación para Se a."  
[SeleniumDownloads]: https://selenium.dev/downloads "Descargas | Se sindón"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-se javascript-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  

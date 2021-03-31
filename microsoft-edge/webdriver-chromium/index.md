---
description: Obtenga información sobre cómo probar su sitio web o aplicación en Microsoft Edge o automatizar el explorador con WebDriver
title: Usar WebDriver (Chromium) para la automatización de pruebas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, html, css, javascript, programador, webdriver, selenio, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: 87855fad02243a9d86053e43b5523013644f7e35
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398836"
---
# <a name="use-webdriver-chromium-for-test-automation"></a><span data-ttu-id="1ee77-104">Usar WebDriver (Chromium) para la automatización de pruebas</span><span class="sxs-lookup"><span data-stu-id="1ee77-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="1ee77-105">WebDriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="1ee77-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="1ee77-106">Las pruebas y simulaciones de WebDriver difieren de las pruebas unitarias de JavaScript de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="1ee77-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="1ee77-107">Tiene acceso a la funcionalidad y la información que no están disponibles para JavaScript que se ejecuta en exploradores.</span><span class="sxs-lookup"><span data-stu-id="1ee77-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="1ee77-108">Simula eventos de usuario o eventos de nivel de sistema operativo con mayor precisión.</span><span class="sxs-lookup"><span data-stu-id="1ee77-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="1ee77-109">Administra varias ventanas, pestañas y páginas web en una sola sesión de prueba.</span><span class="sxs-lookup"><span data-stu-id="1ee77-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="1ee77-110">Ejecuta varias sesiones de Microsoft Edge en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="1ee77-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="1ee77-111">En la siguiente sección se describe cómo empezar a usar WebDriver para Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <a name="install-microsoft-edge-chromium"></a><span data-ttu-id="1ee77-112">Instalar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="1ee77-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="1ee77-113">Asegúrese de instalar [Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="1ee77-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="1ee77-114">Para confirmar que tiene Instalado Microsoft Edge \(Chromium\), vaya a y compruebe que el número de versión es la `edge://settings/help` versión 75 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1ee77-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is version 75 or later.</span></span>  

## <a name="download-microsoft-edge-driver"></a><span data-ttu-id="1ee77-115">Descargar controlador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1ee77-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="1ee77-116">Para empezar a automatizar las pruebas, siga estos pasos para asegurarse de que la versión de WebDriver que instale coincida con la versión del explorador.</span><span class="sxs-lookup"><span data-stu-id="1ee77-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="1ee77-117">Para mostrar la versión de Microsoft Edge, vaya a `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="1ee77-117">To display the version of Microsoft Edge, navigate to `edge://settings/help`.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="El número de compilación de Microsoft Edge Canary el 10 de febrero de 2021" lightbox="./media/microsoft-edge-version.msft.png":::
       <span data-ttu-id="1ee77-119">El número de compilación de Microsoft Edge Canary el 10 de febrero de 2021</span><span class="sxs-lookup"><span data-stu-id="1ee77-119">The build number for Microsoft Edge Canary on February 10, 2021</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1ee77-120">Vaya a [Controlador de Microsoft Edge,][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]en la sección **Descargas,** y descargue el WebDriver que coincida con el número de versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ee77-120">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver], under the **Downloads** section, and download the WebDriver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="La sección Descargas en el controlador de Microsoft Edge" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="1ee77-122">La **sección Descargas** en el controlador de Microsoft [Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="1ee77-122">The **Downloads** section on [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span></span>  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  
    
## <a name="choose-a-webdriver-language-binding"></a><span data-ttu-id="1ee77-123">Elegir un enlace de idioma de WebDriver</span><span class="sxs-lookup"><span data-stu-id="1ee77-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="1ee77-124">El último componente que debe descargar es un controlador de cliente específico del idioma para traducir el código \(Python, Java, C\#, Ruby, JavaScript\) en comandos que el controlador de Microsoft Edge se ejecuta en Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="1ee77-125">[Descargue el enlace de idioma de WebDriver de su elección.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="1ee77-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="1ee77-126">El equipo de Microsoft Edge recomienda [Selenio 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] o posterior, ya que admite Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-126">The Microsoft Edge team recommends [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="1ee77-127">Sin embargo, puede controlar Microsoft Edge \(Chromium\) en todas las versiones anteriores de Selenio, incluida la versión estable actual de Selenio 3.</span><span class="sxs-lookup"><span data-stu-id="1ee77-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="1ee77-128">Si anteriormente había automatizado o probado Microsoft Edge \(Chromium\) con y clases, el código de WebDriver no se ejecuta en `ChromeDriver` `ChromeOptions` Microsoft Edge versión 80 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1ee77-128">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="1ee77-129">Para solucionar el problema, actualice las pruebas para usar la `EdgeOptions` clase y descargue el controlador de Microsoft [Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="1ee77-129">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <a name="use-selenium-3"></a><span data-ttu-id="1ee77-130">Usar Selenio 3</span><span class="sxs-lookup"><span data-stu-id="1ee77-130">Use Selenium 3</span></span>  

<span data-ttu-id="1ee77-131">Si ya usa [Selenio 3][|::ref1::|], es posible que tenga pruebas de explorador existentes y desee agregar cobertura para Microsoft Edge \(Chromium\) sin cambiar su versión de Selenio.</span><span class="sxs-lookup"><span data-stu-id="1ee77-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="1ee77-132">Para usar [Selenio 3][|::ref2::|] para escribir pruebas automatizadas para Microsoft Edge \(EdgeHTML\) y Microsoft Edge \(Chromium\), instale el paquete [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar el controlador actualizado.</span><span class="sxs-lookup"><span data-stu-id="1ee77-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="1ee77-133">Las clases y incluidas en las herramientas son totalmente compatibles con `EdgeDriver` `EdgeDriverService` los equivalentes integrados en Selenio 4.</span><span class="sxs-lookup"><span data-stu-id="1ee77-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="1ee77-134">Siga estos pasos para agregar [selenio Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] y [Selenium 3][|::ref3::|] al proyecto.</span><span class="sxs-lookup"><span data-stu-id="1ee77-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<a name="c"></a><span data-ttu-id="1ee77-135">C#</span><span class="sxs-lookup"><span data-stu-id="1ee77-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="1ee77-136">Agregue los [paquetes Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] y [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] al proyecto .NET mediante la CLI de [NuGet][NugetCLI] [o Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="1ee77-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<a name="python"></a><span data-ttu-id="1ee77-137">Python</span><span class="sxs-lookup"><span data-stu-id="1ee77-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="1ee77-138">Use [pip][PythonPip] para instalar los [paquetes msedge-selenium-tools][PythonSeleniumTools] y [selenio.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="1ee77-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a><span data-ttu-id="1ee77-139">Java</span><span class="sxs-lookup"><span data-stu-id="1ee77-139">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="1ee77-140">Si el Java usa Maven, copie y pegue la siguiente dependencia en el archivo para `pom.xml` agregar [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span><span class="sxs-lookup"><span data-stu-id="1ee77-140">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="1ee77-141">El Java también está disponible para descargar directamente en la página [Selenium Tools for Microsoft Edge Releases][GithubMicrosoftEdgeSeleniumToolsReleases].</span><span class="sxs-lookup"><span data-stu-id="1ee77-141">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<a name="javascript"></a><span data-ttu-id="1ee77-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1ee77-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="1ee77-143">Use [npm][JavaScript|::ref4::|] para instalar los paquetes [edge-selenium-tools][JavaScriptSeleniumTools] y [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="1ee77-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <a name="automate-microsoft-edge-chromium-with-webdriver"></a><span data-ttu-id="1ee77-144">Automatizar Microsoft Edge (Chromium) con WebDriver</span><span class="sxs-lookup"><span data-stu-id="1ee77-144">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="1ee77-145">Para automatizar un explorador con WebDriver, primero debe iniciar una sesión de WebDriver con el enlace de idioma de WebDriver preferido.</span><span class="sxs-lookup"><span data-stu-id="1ee77-145">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="1ee77-146">Una sesión es una única instancia en ejecución de un explorador controlado mediante comandos de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="1ee77-146">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="1ee77-147">Inicie una sesión de WebDriver para iniciar una nueva instancia del explorador.</span><span class="sxs-lookup"><span data-stu-id="1ee77-147">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="1ee77-148">La instancia del explorador iniciada permanece abierta hasta que cierre la sesión de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="1ee77-148">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="1ee77-149">El siguiente contenido le guiará a través del uso de Selenium para iniciar una sesión de WebDriver con Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-149">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="1ee77-150">Puede ejecutar los ejemplos con Selenio 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="1ee77-150">You may run the examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="1ee77-151">Para usar con Selenium 3, se debe instalar el paquete [Selenium Tools for Microsoft Edge.][GithubMicrosoftEdgeSeleniumTools]</span><span class="sxs-lookup"><span data-stu-id="1ee77-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <a name="automate-microsoft-edge-chromium"></a><span data-ttu-id="1ee77-152">Automatizar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="1ee77-152">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="1ee77-153">Selenio usa la `EdgeDriver` clase para administrar una sesión de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-153">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="1ee77-154">Para iniciar una sesión y automatizar Microsoft Edge \(Chromium\), cree un nuevo objeto y pásenle un objeto con `EdgeDriver` la propiedad establecida en `EdgeOptions` `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="1ee77-154">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<a name="c"></a><span data-ttu-id="1ee77-155">C#</span><span class="sxs-lookup"><span data-stu-id="1ee77-155">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="1ee77-156">Python</span><span class="sxs-lookup"><span data-stu-id="1ee77-156">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="1ee77-157">Java</span><span class="sxs-lookup"><span data-stu-id="1ee77-157">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="1ee77-158">La `EdgeDriver` clase solo admite Microsoft Edge \(Chromium\) y no admite Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-158">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="1ee77-159">Para el uso básico, puede crear un `EdgeDriver` sin proporcionar `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="1ee77-159">For basic usage, you may create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a><span data-ttu-id="1ee77-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1ee77-160">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="1ee77-161">Si el administrador de TI ha establecido la directiva [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] en , el controlador de Microsoft Edge no puede impulsar `2` Microsoft Edge \(Chromium\), ya que el controlador usa [Microsoft Edge DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="1ee77-161">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="1ee77-162">Asegúrese de [que la directiva DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] está establecida en `0` o para automatizar Microsoft Edge `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="1ee77-162">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <a name="choose-specific-browser-binaries-chromium-only"></a><span data-ttu-id="1ee77-163">Elegir binarios de explorador específicos (solo Chromium)</span><span class="sxs-lookup"><span data-stu-id="1ee77-163">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="1ee77-164">Puede iniciar una sesión de WebDriver con binarios específicos de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-164">You may start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="1ee77-165">Por ejemplo, puede ejecutar pruebas con los canales de vista previa [de Microsoft Edge,][MicrosoftedgeinsiderDownload] como Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="1ee77-165">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<a name="c"></a><span data-ttu-id="1ee77-166">C#</span><span class="sxs-lookup"><span data-stu-id="1ee77-166">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="1ee77-167">Python</span><span class="sxs-lookup"><span data-stu-id="1ee77-167">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="1ee77-168">Java</span><span class="sxs-lookup"><span data-stu-id="1ee77-168">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a><span data-ttu-id="1ee77-169">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1ee77-169">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a><span data-ttu-id="1ee77-170">Personalizar el servicio de controladores de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1ee77-170">Customize the Microsoft Edge Driver Service</span></span>  

#### [<a name="c"></a><span data-ttu-id="1ee77-171">C#</span><span class="sxs-lookup"><span data-stu-id="1ee77-171">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="1ee77-172">Cuando se usa la clase para crear una instancia de clase, se crea e inicia la clase adecuada para `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) o Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-172">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="1ee77-173">Si desea crear un , use el método `EdgeDriverService` para crear uno configurado para Microsoft Edge `CreateChromiumService()` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-173">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="1ee77-174">El `CreateChromiumService()` método es útil cuando necesita agregar personalizaciones.</span><span class="sxs-lookup"><span data-stu-id="1ee77-174">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="1ee77-175">Por ejemplo, el siguiente código inicia una salida de registro detallada.</span><span class="sxs-lookup"><span data-stu-id="1ee77-175">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="1ee77-176">No es necesario proporcionar el objeto `EdgeOptions` al pasar a la `EdgeDriverService` `EdgeDriver` instancia.</span><span class="sxs-lookup"><span data-stu-id="1ee77-176">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="1ee77-177">La clase usa las opciones predeterminadas para `EdgeDriver` Microsoft Edge \(EdgeHTML\) o Microsoft Edge \(Chromium\) en función del servicio que proporcione.</span><span class="sxs-lookup"><span data-stu-id="1ee77-177">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="1ee77-178">Sin embargo, si desea proporcionar ambos y clases, asegúrese de que ambos están `EdgeDriverService` `EdgeOptions` configurados para la misma versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ee77-178">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="1ee77-179">Por ejemplo, puede usar una clase predeterminada de Microsoft Edge \(EdgeHTML\) y `EdgeDriverService` propiedades chromium en la `EdgeOptions` clase.</span><span class="sxs-lookup"><span data-stu-id="1ee77-179">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="1ee77-180">La `EdgeDriver` clase genera un error para evitar el uso de versiones diferentes.</span><span class="sxs-lookup"><span data-stu-id="1ee77-180">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<a name="python"></a><span data-ttu-id="1ee77-181">Python</span><span class="sxs-lookup"><span data-stu-id="1ee77-181">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="1ee77-182">Cuando se usa Python, `Edge` el objeto crea y administra el archivo `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="1ee77-182">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="1ee77-183">Para configurar `EdgeService` el argumento , pase argumentos adicionales al objeto como se indica en el código `Edge` siguiente.</span><span class="sxs-lookup"><span data-stu-id="1ee77-183">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a><span data-ttu-id="1ee77-184">Java</span><span class="sxs-lookup"><span data-stu-id="1ee77-184">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="1ee77-185">Use el `createDefaultService()` método para crear una configuración para Microsoft Edge `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-185">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="1ee77-186">Use Java del sistema para personalizar los servicios de controladores en Java.</span><span class="sxs-lookup"><span data-stu-id="1ee77-186">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="1ee77-187">Por ejemplo, el siguiente código usa la `"webdriver.edge.verboseLogging"` propiedad para activar la salida de registro detallado.</span><span class="sxs-lookup"><span data-stu-id="1ee77-187">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a><span data-ttu-id="1ee77-188">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1ee77-188">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="1ee77-189">Cuando use JavaScript, cree y configure una `Service` con la `ServiceBuilder` clase.</span><span class="sxs-lookup"><span data-stu-id="1ee77-189">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="1ee77-190">Opcionalmente, puede pasar el objeto al objeto, que inicia `Service` `Driver` \(y detiene\) el servicio por usted.</span><span class="sxs-lookup"><span data-stu-id="1ee77-190">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="1ee77-191">Para configurar `Service` el método , ejecute otro método en la clase antes de usar el `ServiceBuilder` `build()` método.</span><span class="sxs-lookup"><span data-stu-id="1ee77-191">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="1ee77-192">A continuación, `service` pase el parámetro as a en el `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="1ee77-192">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a><span data-ttu-id="1ee77-193">Usar Chromium-Specific opciones</span><span class="sxs-lookup"><span data-stu-id="1ee77-193">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="1ee77-194">Si establece la propiedad en , puede usar la clase para tener acceso a las mismas propiedades y métodos específicos de Chromium que se usan al automatizar otros exploradores `UseChromium` `true` `EdgeOptions` chromium. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="1ee77-194">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<a name="c"></a><span data-ttu-id="1ee77-195">C#</span><span class="sxs-lookup"><span data-stu-id="1ee77-195">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a><span data-ttu-id="1ee77-196">Python</span><span class="sxs-lookup"><span data-stu-id="1ee77-196">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a><span data-ttu-id="1ee77-197">Java</span><span class="sxs-lookup"><span data-stu-id="1ee77-197">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a><span data-ttu-id="1ee77-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="1ee77-198">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="1ee77-199">Si la propiedad está establecida en , no puede usar propiedades y métodos para `UseChromium` `true` Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="1ee77-199">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <a name="other-webdriver-installation-options"></a><span data-ttu-id="1ee77-200">Otras opciones de instalación de WebDriver</span><span class="sxs-lookup"><span data-stu-id="1ee77-200">Other WebDriver installation options</span></span>  

### <a name="chocolatey"></a><span data-ttu-id="1ee77-201">Chocolatey</span><span class="sxs-lookup"><span data-stu-id="1ee77-201">Chocolatey</span></span>  

<span data-ttu-id="1ee77-202">Si [usas Chocolatey como][Chocolatey] administrador de paquetes, ejecuta el siguiente comando para instalar el controlador de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ee77-202">If you use [Chocolatey][Chocolatey] as your package manager, run the following command to install the Microsoft Edge Driver.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="1ee77-203">Para obtener más información, vaya [a Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="1ee77-203">For more information, navigate to [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <a name="docker"></a><span data-ttu-id="1ee77-204">Docker</span><span class="sxs-lookup"><span data-stu-id="1ee77-204">Docker</span></span>  

<span data-ttu-id="1ee77-205">Si usa [Docker,][DockerHub]ejecute el siguiente comando para descargar una imagen preconfigurada con Microsoft Edge \(Chromium\) y el controlador [de Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] preinstalados.</span><span class="sxs-lookup"><span data-stu-id="1ee77-205">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="1ee77-206">Para obtener más información, vaya al [contenedor msedgedriver en Docker Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="1ee77-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <a name="next-steps"></a><span data-ttu-id="1ee77-207">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="1ee77-207">Next steps</span></span>  

<span data-ttu-id="1ee77-208">Para obtener más información sobre WebDriver y cómo escribir pruebas automatizadas de WebDriver con Selenio, vaya a la documentación [de Selenio][SeleniumDocumentation].</span><span class="sxs-lookup"><span data-stu-id="1ee77-208">To learn more about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1ee77-209">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1ee77-209">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="1ee77-210">El equipo de Microsoft Edge está deseando escuchar sus comentarios sobre el uso de WebDriver, Selenium y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1ee77-210">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="1ee77-211">Para enviar al equipo sus preguntas  y comentarios, elija el icono Enviar comentarios en Microsoft Edge DevTools o envíe un [tweet][TwitterTweetEdgeDevTools]@EdgeDevTools .</span><span class="sxs-lookup"><span data-stu-id="1ee77-211">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Microsoft Edge DevTools" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="1ee77-213">El **icono Enviar comentarios** en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1ee77-213">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funcionalidades y EdgeOptions | Microsoft Docs"  
<!--[Webdriver]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge: directivas | Microsoft Docs"  

[Chocolatey]: https://chocolatey.org "Productos de | Software de chocolate"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Selenium Chromium Edge Driver | Chocolatey"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Concentrador de Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SelenioHQ/selenio | GitHub"  

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar nuevo explorador de Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | Galería nuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | Galería nuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | Galería nuGet"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Selenium.WebDriver 4.0.0-alpha07 | Galería nuGet"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenio | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "El proyecto de automatización del explorador selenio | Documentación para Selenio"  
[SeleniumDownloads]: https://selenium.dev/downloads "Descargas | Selenio"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  

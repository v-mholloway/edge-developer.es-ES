---
description: Obtenga información sobre cómo probar su sitio web o aplicación en Microsoft Edge o automatizar el explorador con WebDriver
title: Usar WebDriver (Chromium) para la automatización de pruebas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, html, css, javascript, programador, webdriver, se sintaxis, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: b3b8a4ef2174c7f313fe9ee71bedbdf5e2f9b771
ms.sourcegitcommit: f95812c4e1b7277f67c6c4891be2779cc1b5bdf1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/18/2021
ms.locfileid: "11343801"
---
# <span data-ttu-id="29e55-104">Usar WebDriver (Chromium) para la automatización de pruebas</span><span class="sxs-lookup"><span data-stu-id="29e55-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="29e55-105">WebDriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="29e55-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="29e55-106">Las pruebas y simulaciones de WebDriver difieren de las pruebas unitarias de JavaScript de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="29e55-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="29e55-107">Accede a la funcionalidad y la información que no están disponibles para JavaScript que se ejecuta en exploradores.</span><span class="sxs-lookup"><span data-stu-id="29e55-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="29e55-108">Simula eventos de usuario o eventos de nivel de sistema operativo de forma más precisa.</span><span class="sxs-lookup"><span data-stu-id="29e55-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="29e55-109">Administra varias ventanas, pestañas y páginas web en una sola sesión de prueba.</span><span class="sxs-lookup"><span data-stu-id="29e55-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="29e55-110">Ejecuta varias sesiones de Microsoft Edge en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="29e55-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  
    
<span data-ttu-id="29e55-111">En la siguiente sección se describe cómo empezar a usar WebDriver para Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-111">The following section describes how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="29e55-112">Instalar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="29e55-112">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="29e55-113">Asegúrese de instalar [Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="29e55-113">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="29e55-114">Para confirmar que tienes Microsoft Edge \(Chromium\) instalado, ve a y comprueba que el número de versión sea la `edge://settings/help` versión 75 o posterior.</span><span class="sxs-lookup"><span data-stu-id="29e55-114">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify the version number is version 75 or later.</span></span>  

## <span data-ttu-id="29e55-115">Descargar controlador de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="29e55-115">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="29e55-116">Para comenzar las pruebas de automatización, siga estos pasos para asegurarse de que la versión de WebDriver que instale coincida con la versión del explorador.</span><span class="sxs-lookup"><span data-stu-id="29e55-116">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="29e55-117">Para mostrar la versión de Microsoft Edge, vaya a `edge://settings/help` .</span><span class="sxs-lookup"><span data-stu-id="29e55-117">To display the version of Microsoft Edge, navigate to `edge://settings/help`.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="El número de compilación de Microsoft Edge Canary el 10 de febrero de 2021" lightbox="./media/microsoft-edge-version.msft.png":::
       <span data-ttu-id="29e55-119">El número de compilación de Microsoft Edge Canary el 10 de febrero de 2021</span><span class="sxs-lookup"><span data-stu-id="29e55-119">The build number for Microsoft Edge Canary on February 10, 2021</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="29e55-120">Vaya al [controlador de Microsoft Edge,][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]en la sección **Descargas,** y descargue el WebDriver que coincida con el número de versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="29e55-120">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver], under the **Downloads** section, and download the WebDriver that matches the version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="La sección Descargas en el controlador de Microsoft Edge" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="29e55-122">La **sección Descargas** en el controlador de Microsoft [Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="29e55-122">The **Downloads** section on [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span></span>  
    :::image-end:::  
    
    <!--  
    > [!NOTE] 
    > For more information about test automation using Microsoft Edge \(EdgeHTML\), navigate to [Microsoft Edge Driver for Microsoft Edge \(EdgeHTML\)][Webdriver].  
    -->  

## <span data-ttu-id="29e55-123">Elegir un enlace de idioma de WebDriver</span><span class="sxs-lookup"><span data-stu-id="29e55-123">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="29e55-124">El último componente que debes descargar es un controlador de cliente específico del idioma para traducir el código \(Python, Java, C\#, Ruby, JavaScript\) en comandos que el controlador de Microsoft Edge ejecuta en Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-124">The last component you must download is a language-specific client driver to translate your code \(Python, Java, C\#, Ruby, JavaScript\) into commands the Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="29e55-125">[Descargue el enlace de idioma de WebDriver de su elección.][SeleniumDownloads]</span><span class="sxs-lookup"><span data-stu-id="29e55-125">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="29e55-126">El equipo de Microsoft Edge recomienda [Usar 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] o posterior, porque es compatible con Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-126">The Microsoft Edge team recommends [Selenium 4.00-alpha07][NugetPackagesSeleniumWebdriver400alpha07] or later, because it supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="29e55-127">Sin embargo, puedes controlar Microsoft Edge \(Chromium\) en todas las versiones anteriores de Se sint, incluida la versión estable actual de Se sint 3.</span><span class="sxs-lookup"><span data-stu-id="29e55-127">However, you may control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="29e55-128">Si anteriormente ha automatizado o probado Microsoft Edge \(Chromium\) mediante y clases, el código de WebDriver no se ejecuta en `ChromeDriver` `ChromeOptions` Microsoft Edge versión 80 o posterior.</span><span class="sxs-lookup"><span data-stu-id="29e55-128">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="29e55-129">Para solucionar el problema, actualice las pruebas para usar la `EdgeOptions` clase y descargue el controlador de Microsoft [Edge.][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="29e55-129">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="29e55-130">Usar Se desenlaz 3</span><span class="sxs-lookup"><span data-stu-id="29e55-130">Use Selenium 3</span></span>  

<span data-ttu-id="29e55-131">Si ya [usas Seleán 3,][|::ref1::|]es posible que ya tienes pruebas de explorador y quieras agregar cobertura para Microsoft Edge \(Chromium\) sin cambiar la versión de Sende.</span><span class="sxs-lookup"><span data-stu-id="29e55-131">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="29e55-132">Para usar [Seprocesamiento 3][|::ref2::|] para escribir pruebas automatizadas tanto para Microsoft Edge \(EdgeHTML\) como para Microsoft Edge \(Chromium\), instala el paquete [Se de Seprocesamiento Tools para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar el controlador actualizado.</span><span class="sxs-lookup"><span data-stu-id="29e55-132">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="29e55-133">Las clases y las clases incluidas en las herramientas son totalmente compatibles con `EdgeDriver` `EdgeDriverService` los equivalentes integrados en Se siny 4.</span><span class="sxs-lookup"><span data-stu-id="29e55-133">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="29e55-134">Siga los pasos siguientes para agregar [las Herramientas de selenio para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] y Se [siny 3][|::ref3::|] al proyecto.</span><span class="sxs-lookup"><span data-stu-id="29e55-134">Use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>  

#### [<span data-ttu-id="29e55-135">C#</span><span class="sxs-lookup"><span data-stu-id="29e55-135">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="29e55-136">Agregue los [paquetes Microsoft.Edge.Setools y][NugetPackagesMicrosoftEdgeSeleniumtools] [Setools.WebDriver][NugetPackagesSeleniumWebdriver31410] al proyecto .NET con la CLI de [NuGet][NugetCLI] [o Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="29e55-136">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<span data-ttu-id="29e55-137">Python</span><span class="sxs-lookup"><span data-stu-id="29e55-137">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="29e55-138">Usa [pip][PythonPip] para instalar los [paquetes msedge-se ale-tools][PythonSeleniumTools] y [se siny.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="29e55-138">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<span data-ttu-id="29e55-139">Java</span><span class="sxs-lookup"><span data-stu-id="29e55-139">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="29e55-140">Si el Java usa Maven, copie y pegue la siguiente dependencia en el archivo para agregar `pom.xml` [msedge-se javascript-tools-java][SonatypeMavenRepositorySearch].</span><span class="sxs-lookup"><span data-stu-id="29e55-140">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="29e55-141">El Java paquete también está disponible para descargar directamente en la página [Herramientas de disponibilidad para versiones de Microsoft Edge.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="29e55-141">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<span data-ttu-id="29e55-142">JavaScript</span><span class="sxs-lookup"><span data-stu-id="29e55-142">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="29e55-143">Use [npm][JavaScript|::ref4::|] para instalar los [paquetes edge-seprocesamiento-tools][JavaScriptSeleniumTools] y [seprocesamiento-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="29e55-143">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  

## <span data-ttu-id="29e55-144">Automatizar Microsoft Edge (Chromium) con WebDriver</span><span class="sxs-lookup"><span data-stu-id="29e55-144">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="29e55-145">Para automatizar un explorador con WebDriver, primero debe iniciar una sesión de WebDriver con el enlace de idioma de WebDriver preferido.</span><span class="sxs-lookup"><span data-stu-id="29e55-145">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver language binding.</span></span>  <span data-ttu-id="29e55-146">Una sesión es una única instancia en ejecución de un explorador controlado mediante comandos de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="29e55-146">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="29e55-147">Inicie una sesión de WebDriver para iniciar una nueva instancia del explorador.</span><span class="sxs-lookup"><span data-stu-id="29e55-147">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="29e55-148">La instancia del explorador iniciada permanece abierta hasta que cierre la sesión de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="29e55-148">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="29e55-149">El siguiente contenido le guiará a través del uso de Se a continuación para iniciar una sesión de WebDriver con Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-149">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="29e55-150">Puede ejecutar los ejemplos con Se siny 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="29e55-150">You may run the examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="29e55-151">Para usar con Se desenlaz 3, debe instalarse el paquete [Herramientas de sesón][GithubMicrosoftEdgeSeleniumTools] para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="29e55-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

### <span data-ttu-id="29e55-152">Automatizar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="29e55-152">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="29e55-153">Sende usa la `EdgeDriver` clase para administrar una sesión de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-153">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="29e55-154">Para iniciar una sesión y automatizar Microsoft Edge \(Chromium\), cree un nuevo objeto y pásle un objeto con la `EdgeDriver` `EdgeOptions` propiedad establecida en `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="29e55-154">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="29e55-155">C#</span><span class="sxs-lookup"><span data-stu-id="29e55-155">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="29e55-156">Python</span><span class="sxs-lookup"><span data-stu-id="29e55-156">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### [<span data-ttu-id="29e55-157">Java</span><span class="sxs-lookup"><span data-stu-id="29e55-157">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="29e55-158">La `EdgeDriver` clase solo admite Microsoft Edge \(Chromium\) y no admite Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="29e55-158">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="29e55-159">Para el uso básico, puede crear una `EdgeDriver` sin proporcionar `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="29e55-159">For basic usage, you may create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<span data-ttu-id="29e55-160">JavaScript</span><span class="sxs-lookup"><span data-stu-id="29e55-160">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="29e55-161">Si el administrador de TI ha establecido la directiva [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] en , se bloquea el controlador de Microsoft Edge para que no maneja `2` Microsoft Edge \(Chromium\), ya que el controlador usa las [DevTools de Microsoft Edge.][DevtoolsIndex] [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="29e55-161">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="29e55-162">Asegúrate de [que la directiva DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] esté establecida en o para automatizar `0` Microsoft Edge `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="29e55-162">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <span data-ttu-id="29e55-163">Elegir archivos binarios de explorador específicos (solo Chromium)</span><span class="sxs-lookup"><span data-stu-id="29e55-163">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="29e55-164">Puede iniciar una sesión de WebDriver con archivos binarios específicos de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-164">You may start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="29e55-165">Por ejemplo, puede ejecutar pruebas con los canales de vista previa de [Microsoft Edge,][MicrosoftedgeinsiderDownload] como Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="29e55-165">For example, you may run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="29e55-166">C#</span><span class="sxs-lookup"><span data-stu-id="29e55-166">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="29e55-167">Python</span><span class="sxs-lookup"><span data-stu-id="29e55-167">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### [<span data-ttu-id="29e55-168">Java</span><span class="sxs-lookup"><span data-stu-id="29e55-168">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="29e55-169">JavaScript</span><span class="sxs-lookup"><span data-stu-id="29e55-169">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <span data-ttu-id="29e55-170">Personalizar el servicio de controladores de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="29e55-170">Customize the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="29e55-171">C#</span><span class="sxs-lookup"><span data-stu-id="29e55-171">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="29e55-172">Cuando usas la clase para crear una instancia de clase, crea e inicia la clase adecuada para `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) o Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-172">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="29e55-173">Si quieres crear una, usa el método para crear una configurada `EdgeDriverService` `CreateChromiumService()` para Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-173">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="29e55-174">El `CreateChromiumService()` método es útil cuando necesita agregar personalizaciones.</span><span class="sxs-lookup"><span data-stu-id="29e55-174">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="29e55-175">Por ejemplo, el siguiente código inicia la salida del registro detallado.</span><span class="sxs-lookup"><span data-stu-id="29e55-175">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="29e55-176">No es necesario proporcionar el `EdgeOptions` objeto al pasar a la `EdgeDriverService` `EdgeDriver` instancia.</span><span class="sxs-lookup"><span data-stu-id="29e55-176">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="29e55-177">La clase usa las opciones predeterminadas para `EdgeDriver` Microsoft Edge \(EdgeHTML\) o Microsoft Edge \(Chromium\) en función del servicio que proporciones.</span><span class="sxs-lookup"><span data-stu-id="29e55-177">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="29e55-178">Sin embargo, si desea proporcionar ambos y clases, asegúrese de que ambos están configurados `EdgeDriverService` para la misma versión de Microsoft `EdgeOptions` Edge.</span><span class="sxs-lookup"><span data-stu-id="29e55-178">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="29e55-179">Por ejemplo, puedes usar una clase predeterminada de Microsoft Edge \(EdgeHTML\) y propiedades `EdgeDriverService` chromium en la `EdgeOptions` clase.</span><span class="sxs-lookup"><span data-stu-id="29e55-179">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="29e55-180">La `EdgeDriver` clase produce un error para evitar el uso de diferentes versiones.</span><span class="sxs-lookup"><span data-stu-id="29e55-180">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="29e55-181">Python</span><span class="sxs-lookup"><span data-stu-id="29e55-181">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="29e55-182">Cuando se usa Python, `Edge` el objeto crea y administra el archivo `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="29e55-182">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="29e55-183">Para configurar el `EdgeService` , pase argumentos adicionales al objeto como se indica en el siguiente `Edge` código.</span><span class="sxs-lookup"><span data-stu-id="29e55-183">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<span data-ttu-id="29e55-184">Java</span><span class="sxs-lookup"><span data-stu-id="29e55-184">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="29e55-185">Usa el `createDefaultService()` método para crear una configuración para Microsoft Edge `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="29e55-185">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="29e55-186">Usa Java del sistema para personalizar los servicios de controladores en Java.</span><span class="sxs-lookup"><span data-stu-id="29e55-186">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="29e55-187">Por ejemplo, el siguiente código usa la `"webdriver.edge.verboseLogging"` propiedad para activar la salida de registro detallada.</span><span class="sxs-lookup"><span data-stu-id="29e55-187">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<span data-ttu-id="29e55-188">JavaScript</span><span class="sxs-lookup"><span data-stu-id="29e55-188">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="29e55-189">Cuando use JavaScript, cree y configure una con `Service` la `ServiceBuilder` clase.</span><span class="sxs-lookup"><span data-stu-id="29e55-189">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="29e55-190">Opcionalmente, puedes pasar el objeto al objeto, que inicia `Service` `Driver` \(y detiene\) el servicio por ti.</span><span class="sxs-lookup"><span data-stu-id="29e55-190">Optionally, you may pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="29e55-191">Para configurar el `Service` método , ejecute otro método en la clase antes de usar el `ServiceBuilder` `build()` método.</span><span class="sxs-lookup"><span data-stu-id="29e55-191">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="29e55-192">A continuación, `service` pase el parámetro como en el `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="29e55-192">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <span data-ttu-id="29e55-193">Usar Chromium-Specific opciones</span><span class="sxs-lookup"><span data-stu-id="29e55-193">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="29e55-194">Si estableces la propiedad en , puedes usar la clase para tener acceso a las mismas propiedades y métodos específicos de Chromium que se usan al automatizar otros exploradores `UseChromium` `true` `EdgeOptions` chromium. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="29e55-194">If you set the `UseChromium` property to `true`, you may use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<span data-ttu-id="29e55-195">C#</span><span class="sxs-lookup"><span data-stu-id="29e55-195">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="29e55-196">Python</span><span class="sxs-lookup"><span data-stu-id="29e55-196">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<span data-ttu-id="29e55-197">Java</span><span class="sxs-lookup"><span data-stu-id="29e55-197">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<span data-ttu-id="29e55-198">JavaScript</span><span class="sxs-lookup"><span data-stu-id="29e55-198">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="29e55-199">Si la propiedad se establece en , no podrá usar propiedades y métodos para `UseChromium` `true` Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="29e55-199">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="29e55-200">Otras opciones de instalación de WebDriver</span><span class="sxs-lookup"><span data-stu-id="29e55-200">Other WebDriver installation options</span></span>  

### <span data-ttu-id="29e55-201">Resalte</span><span class="sxs-lookup"><span data-stu-id="29e55-201">Chocolatey</span></span>  

<span data-ttu-id="29e55-202">Si [usas aRtay][Chocolatey] como administrador de paquetes, ejecuta el siguiente comando para instalar el controlador de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="29e55-202">If you use [Chocolatey][Chocolatey] as your package manager, run the following command to install the Microsoft Edge Driver.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="29e55-203">Para obtener más información, vaya [a Se siny Chromium Edge Driver en Rebosa.][ChocolateyPackagesSeleniumChromiumEdgeDriver]</span><span class="sxs-lookup"><span data-stu-id="29e55-203">For more information, navigate to [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="29e55-204">Docker</span><span class="sxs-lookup"><span data-stu-id="29e55-204">Docker</span></span>  

<span data-ttu-id="29e55-205">Si usa [Docker,][DockerHub]ejecute el siguiente comando para descargar una imagen preconfigurada con Microsoft Edge \(Chromium\) y el controlador [de Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] preinstalados.</span><span class="sxs-lookup"><span data-stu-id="29e55-205">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="29e55-206">Para obtener más información, vaya al [contenedor msedgedriver en Docker Hub.][DockerHubMsedgedriver]</span><span class="sxs-lookup"><span data-stu-id="29e55-206">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="29e55-207">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="29e55-207">Next steps</span></span>  

<span data-ttu-id="29e55-208">Para obtener más información sobre WebDriver y cómo escribir pruebas automatizadas de WebDriver con Serío, vaya a la documentación [de Se automatri.][SeleniumDocumentation]</span><span class="sxs-lookup"><span data-stu-id="29e55-208">To learn more about WebDriver and how to write automated WebDriver tests using Selenium, navigate to the [Selenium documentation][SeleniumDocumentation].</span></span>  

## <span data-ttu-id="29e55-209">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="29e55-209">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="29e55-210">El equipo de Microsoft Edge está deseando escuchar sus comentarios sobre el uso de WebDriver, Se sin embargo y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="29e55-210">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge.</span></span>  <span data-ttu-id="29e55-211">Para enviar al equipo sus preguntas \*\*\*\* y comentarios, elija el icono Enviar comentarios en las DevTools de Microsoft Edge o envíe un tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span><span class="sxs-lookup"><span data-stu-id="29e55-211">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Las DevTools de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="29e55-213">El **icono Enviar comentarios** en Las DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="29e55-213">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
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

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "WebDriver | Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar el nuevo explorador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet.CommandLine | Galería de NuGet"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.Setools | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Serero.WebDriver 3.141.0 | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver400alpha07]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha07 "Se siny.WebDriver 4.0.0-alpha07 | Galería de NuGet"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-seprocesamiento-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "se siny | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SenioHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "El proyecto de automatización del explorador Se desenfoca | Documentación para Se siny"  
[SeleniumDownloads]: https://selenium.dev/downloads "Descargas | Se sindón"  

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-se javascript-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  

---
description: Aprende a probar tu sitio web o aplicación en Microsoft Edge o automatizar el explorador con WebDriver
title: Usar WebDriver (Chromium) para la automatización de pruebas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/24/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, html, css, javascript, programador, webdriver, selenio, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: a1ec308fc1412ead27c4776ce0ccc2e873376652
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624678"
---
# <a name="use-webdriver-chromium-for-test-automation"></a><span data-ttu-id="563f8-104">Usar WebDriver (Chromium) para la automatización de pruebas</span><span class="sxs-lookup"><span data-stu-id="563f8-104">Use WebDriver (Chromium) for test automation</span></span>  

<span data-ttu-id="563f8-105">WebDriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="563f8-105">WebDriver allows developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="563f8-106">Las pruebas y simulaciones de WebDriver difieren de las pruebas unitarias de JavaScript de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="563f8-106">WebDriver tests and simulations differ from JavaScript unit tests in the following ways.</span></span>  

*   <span data-ttu-id="563f8-107">Tiene acceso a la funcionalidad y la información que no están disponibles para JavaScript que se ejecuta en exploradores.</span><span class="sxs-lookup"><span data-stu-id="563f8-107">Accesses functionality and information not available to JavaScript running in browsers.</span></span>  
*   <span data-ttu-id="563f8-108">Simula eventos de usuario o eventos de nivel de sistema operativo con mayor precisión.</span><span class="sxs-lookup"><span data-stu-id="563f8-108">Simulates user events or OS-level events more accurately.</span></span>  
*   <span data-ttu-id="563f8-109">Administra varias ventanas, pestañas y páginas web en una sola sesión de prueba.</span><span class="sxs-lookup"><span data-stu-id="563f8-109">Manages multiple windows, tabs, and webpages in a single test session.</span></span>  
*   <span data-ttu-id="563f8-110">Ejecuta varias sesiones de Microsoft Edge en un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="563f8-110">Runs multiple sessions of Microsoft Edge on a specific machine.</span></span>  


## <a name="relationship-between-webdriver-and-other-software"></a><span data-ttu-id="563f8-111">Relación entre WebDriver y otro software</span><span class="sxs-lookup"><span data-stu-id="563f8-111">Relationship between WebDriver and other software</span></span>

<span data-ttu-id="563f8-112">Para automatizar Microsoft Edge webDriver para simular la interacción del usuario, necesita tres componentes:</span><span class="sxs-lookup"><span data-stu-id="563f8-112">To automate Microsoft Edge with WebDriver to simulate user interaction, you need three components:</span></span>

*  <span data-ttu-id="563f8-113">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="563f8-113">Microsoft Edge</span></span>
*  <span data-ttu-id="563f8-114">Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="563f8-114">Microsoft Edge Driver</span></span>
*  <span data-ttu-id="563f8-115">Un marco de pruebas de WebDriver</span><span class="sxs-lookup"><span data-stu-id="563f8-115">A WebDriver testing framework</span></span>

<span data-ttu-id="563f8-116">La relación funcional entre estos componentes es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="563f8-116">The functional relationship between these components is as follows.</span></span>

| <span data-ttu-id="563f8-117">Tecnología</span><span class="sxs-lookup"><span data-stu-id="563f8-117">Technology</span></span> | <span data-ttu-id="563f8-118">Rol</span><span class="sxs-lookup"><span data-stu-id="563f8-118">Role</span></span> |
|---|---|
| <span data-ttu-id="563f8-119">WebDriver</span><span class="sxs-lookup"><span data-stu-id="563f8-119">WebDriver</span></span> | <span data-ttu-id="563f8-120">Un estándar W3C para un protocolo de cable de plataforma e idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="563f8-120">A W3C standard for a platform- and language-neutral wire protocol.</span></span>  <span data-ttu-id="563f8-121">Este protocolo permite que los programas fuera de proceso indiquen de forma remota el comportamiento de los exploradores web.</span><span class="sxs-lookup"><span data-stu-id="563f8-121">This protocol allows out-of-process programs to remotely instruct the behavior of web browsers.</span></span> |
| <span data-ttu-id="563f8-122">Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="563f8-122">Microsoft Edge Driver</span></span> | <span data-ttu-id="563f8-123">Implementación de Microsoft del protocolo WebDriver específicamente para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="563f8-123">Microsoft's implementation of the WebDriver protocol specifically for Microsoft Edge.</span></span>  <span data-ttu-id="563f8-124">Los autores de pruebas escriben pruebas que usan comandos de WebDriver que Microsoft Edge driver recibe.</span><span class="sxs-lookup"><span data-stu-id="563f8-124">Test authors write tests that use WebDriver commands that Microsoft Edge Driver receives.</span></span>  <span data-ttu-id="563f8-125">Microsoft Edge A continuación, el controlador es responsable de comunicar ese comando al explorador.</span><span class="sxs-lookup"><span data-stu-id="563f8-125">Microsoft Edge Driver is then responsible for communicating that command to the browser.</span></span> |
| <span data-ttu-id="563f8-126">Un marco de pruebas de WebDriver</span><span class="sxs-lookup"><span data-stu-id="563f8-126">A WebDriver testing framework</span></span> | <span data-ttu-id="563f8-127">Los autores de pruebas usan un marco de pruebas para escribir pruebas de extremo a extremo y automatizar exploradores.</span><span class="sxs-lookup"><span data-stu-id="563f8-127">Test authors use a testing framework to write end-to-end tests and automate browsers.</span></span>  <span data-ttu-id="563f8-128">Proporciona una interfaz específica del idioma que traduce el código en comandos que Microsoft Edge Driver se ejecuta en Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-128">Provides a language-specific interface that translates your code into commands that Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="563f8-129">Los marcos de prueba de WebDriver existen para todas las plataformas e idiomas principales.</span><span class="sxs-lookup"><span data-stu-id="563f8-129">WebDriver testing frameworks exist for all major platforms and languages.</span></span>  <span data-ttu-id="563f8-130">Uno de estos marcos es Selenio.</span><span class="sxs-lookup"><span data-stu-id="563f8-130">One such framework is Selenium.</span></span> |
| <span data-ttu-id="563f8-131">Controlador de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="563f8-131">Internet Explorer Driver</span></span> | <span data-ttu-id="563f8-132">Una implementación del protocolo WebDriver específicamente para Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="563f8-132">An implementation of the WebDriver protocol specifically for Internet Explorer.</span></span>  <span data-ttu-id="563f8-133">Para ejecutar pruebas de un extremo a otro heredadas para Internet Explorer, se recomienda usar el controlador de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="563f8-133">To run legacy end-to-end tests for Internet Explorer, we recommend using Internet Explorer Driver.</span></span> |

<span data-ttu-id="563f8-134">En las secciones siguientes se describe cómo empezar a usar WebDriver para Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-134">The following sections describe how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  


## <a name="install-microsoft-edge-chromium"></a><span data-ttu-id="563f8-135">Instalar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="563f8-135">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="563f8-136">Asegúrese de instalar [Microsoft Edge (Chromium).][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="563f8-136">Ensure you install [Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="563f8-137">Para confirmar que tiene Microsoft Edge \(Chromium\) instalado, vaya a y compruebe que el número de versión es `edge://settings/help` 75 o posterior.</span><span class="sxs-lookup"><span data-stu-id="563f8-137">To confirm that you have Microsoft Edge \(Chromium\) installed, navigate to `edge://settings/help`, and verify that the version number is 75 or later.</span></span>


## <a name="download-microsoft-edge-driver"></a><span data-ttu-id="563f8-138">Descargar Microsoft Edge Driver</span><span class="sxs-lookup"><span data-stu-id="563f8-138">Download Microsoft Edge Driver</span></span>

<span data-ttu-id="563f8-139">Para empezar a automatizar las pruebas, siga estos pasos para asegurarse de que la versión de WebDriver que instale coincida con la versión del explorador.</span><span class="sxs-lookup"><span data-stu-id="563f8-139">To begin automating tests, use the following steps to ensure that the WebDriver version you install matches your browser version.</span></span>  

1.  <span data-ttu-id="563f8-140">Busque la versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="563f8-140">Find your version of Microsoft Edge.</span></span>  
    1.  <span data-ttu-id="563f8-141">Vaya a `edge://settings/help`.</span><span class="sxs-lookup"><span data-stu-id="563f8-141">Navigate to `edge://settings/help`.</span></span>  
        
        :::image type="complex" source="./media/microsoft-edge-version.msft.png" alt-text="El número de compilación Microsoft Edge el 15 de abril de 2021" lightbox="./media/microsoft-edge-version.msft.png":::
           <span data-ttu-id="563f8-143">El número de compilación Microsoft Edge el 15 de abril de 2021</span><span class="sxs-lookup"><span data-stu-id="563f8-143">The build number for Microsoft Edge on April 15, 2021</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="563f8-144">Vaya a [Microsoft Edge controlador][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="563f8-144">Navigate to [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  
1.  <span data-ttu-id="563f8-145">Vaya a **Obtener la versión más reciente**.</span><span class="sxs-lookup"><span data-stu-id="563f8-145">Navigate to **Get the latest version**.</span></span>  
1.  <span data-ttu-id="563f8-146">Elija la compilación del canal que coincida con el número de versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="563f8-146">Choose the build of channel that matches your version number of Microsoft Edge.</span></span>  
    
    :::image type="complex" source="./media/microsoft-edge-driver-install.msft.png" alt-text="La sección Obtener la versión más reciente en la página Microsoft Edge driver" lightbox="./media/microsoft-edge-driver-install.msft.png":::
       <span data-ttu-id="563f8-148">La **sección Obtener la versión más** reciente en la página web Microsoft Edge [driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="563f8-148">The **Get the latest version** section on the [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] webpage</span></span>  
    :::image-end:::  
   
    
## <a name="choose-a-webdriver-testing-framework"></a><span data-ttu-id="563f8-149">Elegir un marco de pruebas de WebDriver</span><span class="sxs-lookup"><span data-stu-id="563f8-149">Choose a WebDriver testing framework</span></span>

<span data-ttu-id="563f8-150">Después de descargar Microsoft Edge driver, el último componente que debe descargar es un marco de pruebas de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="563f8-150">After downloading Microsoft Edge Driver, the last component you must download is a WebDriver testing framework.</span></span> <span data-ttu-id="563f8-151">Los autores de pruebas usan marcos de prueba de WebDriver para escribir pruebas de un extremo a otro y automatizar exploradores.</span><span class="sxs-lookup"><span data-stu-id="563f8-151">Test authors use WebDriver testing frameworks to write end-to-end tests and automate browsers.</span></span> <span data-ttu-id="563f8-152">El marco proporciona una interfaz específica del idioma que convierte el código (como Python, Java, C#, Ruby o JavaScript) en comandos que Microsoft Edge Driver se ejecuta en Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-152">The framework provides a language-specific interface that translates your code (such as Python, Java, C#, Ruby, or JavaScript) into commands that Microsoft Edge Driver runs in Microsoft Edge \(Chromium\).</span></span> <span data-ttu-id="563f8-153">Los marcos de prueba de WebDriver existen para todas las plataformas e idiomas principales.</span><span class="sxs-lookup"><span data-stu-id="563f8-153">WebDriver testing frameworks exist for all major platforms and languages.</span></span>


<span data-ttu-id="563f8-154">En este artículo se proporcionan instrucciones para usar el marco selenio, pero puede usar cualquier biblioteca, marco y lenguaje de programación compatible con WebDriver.</span><span class="sxs-lookup"><span data-stu-id="563f8-154">This article provides instructions for using the Selenium framework, but you can use any library, framework, and programming language that supports WebDriver.</span></span>  <span data-ttu-id="563f8-155">Para realizar las mismas tareas con un marco de pruebas de WebDriver distinto de Selenio, consulte la documentación oficial para su marco de elección.</span><span class="sxs-lookup"><span data-stu-id="563f8-155">To accomplish the same tasks using a WebDriver testing framework other than Selenium, consult the official documentation for your framework of choice.</span></span>

<span data-ttu-id="563f8-156">Si usa Selenio, el equipo de Microsoft Edge recomienda [Selenio 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] o posterior, ya que esa versión de Selenio admite Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-156">If you are using Selenium, the Microsoft Edge team recommends [Selenium 4.0.0-beta2][NugetPackagesSeleniumWebdriver400beta02] or later, because that version of Selenium supports Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="563f8-157">Sin embargo, puede controlar Microsoft Edge \(Chromium\) en todas las versiones anteriores de Selenio, incluida la versión estable actual de Selenio 3.</span><span class="sxs-lookup"><span data-stu-id="563f8-157">However, you can control Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="563f8-158">Si ha automatizado o probado anteriormente Microsoft Edge \(Chromium\) mediante y clases, el código de WebDriver no se ejecuta en `ChromeDriver` `ChromeOptions` Microsoft Edge versión 80 o posterior.</span><span class="sxs-lookup"><span data-stu-id="563f8-158">If you previously automated or tested Microsoft Edge \(Chromium\) using `ChromeDriver` and `ChromeOptions` classes, your WebDriver code does not run on Microsoft Edge Version 80 or later.</span></span>  <span data-ttu-id="563f8-159">Para solucionar el problema, actualice las pruebas para usar la `EdgeOptions` clase y descargue Microsoft Edge [driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="563f8-159">To solve the problem, update your tests to use the `EdgeOptions` class and download [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver].</span></span>  

### <a name="using-selenium-4"></a><span data-ttu-id="563f8-160">Uso de Selenio 4</span><span class="sxs-lookup"><span data-stu-id="563f8-160">Using Selenium 4</span></span>

<span data-ttu-id="563f8-161">El marco de pruebas de Selenium WebDriver se puede usar en cualquier plataforma y está disponible para Java, Python, C#, Ruby y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="563f8-161">The Selenium WebDriver testing framework can be used on any platform, and is available for Java, Python, C#, Ruby, and JavaScript.</span></span>

<span data-ttu-id="563f8-162">Selenium 4 tiene compatibilidad integrada con Microsoft Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="563f8-162">Selenium 4 has built-in support for Microsoft Edge (Chromium).</span></span>  <span data-ttu-id="563f8-163">Para instalar Selenio 4, vaya a [Instalación de bibliotecas de Selenio][SeleniumInstallingLibraries].</span><span class="sxs-lookup"><span data-stu-id="563f8-163">To install Selenium 4, navigate to [Installing Selenium libraries][SeleniumInstallingLibraries].</span></span>

<span data-ttu-id="563f8-164">Si usa Selenio 4, no necesita usar Herramientas de Selenio para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="563f8-164">If you use Selenium 4, you don't need to use Selenium Tools for Microsoft Edge.</span></span>  <span data-ttu-id="563f8-165">Las herramientas de selenio Microsoft Edge son solo para Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="563f8-165">Selenium Tools for Microsoft Edge are for Selenium 3 only.</span></span>  <span data-ttu-id="563f8-166">Si intenta usar Selenium 4 con Selenium Tools para Microsoft Edge e intenta crear una nueva instancia, se `EdgeDriver` produce el siguiente error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'` .</span><span class="sxs-lookup"><span data-stu-id="563f8-166">If you try to use Selenium 4 with Selenium Tools for Microsoft Edge and try to create a new `EdgeDriver` instance, you get the following error: `System.MissingMethodException: 'Method not found: 'OpenQA.Selenium.Remote.DesiredCapabilities OpenQA.Selenium.DriverOptions.GenerateDesiredCapabilities(Boolean)'`.</span></span>  

<span data-ttu-id="563f8-167">Si usa Selenio 4 y obtiene este error, quite del proyecto y asegúrese de que está usando el oficial y las clases del `Microsoft.Edge.SeleniumTools` `EdgeOptions` espacio de `EdgeDriver` `OpenQA.Selenium.Edge` nombres.</span><span class="sxs-lookup"><span data-stu-id="563f8-167">If you're using Selenium 4 and get this error, remove `Microsoft.Edge.SeleniumTools` from your project, and make sure you're using the official `EdgeOptions` and `EdgeDriver` classes from the `OpenQA.Selenium.Edge` namespace.</span></span>

### <a name="using-selenium-3"></a><span data-ttu-id="563f8-168">Uso de Selenio 3</span><span class="sxs-lookup"><span data-stu-id="563f8-168">Using Selenium 3</span></span>  

<span data-ttu-id="563f8-169">Si ya usa [Selenio 3,][|::ref1::|]es posible que tenga pruebas de explorador existentes y desee agregar cobertura para Microsoft Edge \(Chromium\) sin cambiar su versión de Selenio.</span><span class="sxs-lookup"><span data-stu-id="563f8-169">If you already use [Selenium 3][|::ref1::|], you may have existing browser tests and want to add coverage for Microsoft Edge \(Chromium\) without changing your version of Selenium.</span></span>  <span data-ttu-id="563f8-170">Para usar [Selenio 3][|::ref2::|] para escribir pruebas automatizadas para Microsoft Edge \(EdgeHTML\) y Microsoft Edge \(Chromium\), instale el paquete [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para usar el controlador actualizado.</span><span class="sxs-lookup"><span data-stu-id="563f8-170">To use [Selenium 3][|::ref2::|] to write automated tests for both Microsoft Edge \(EdgeHTML\) and Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package to use the updated driver.</span></span>  <span data-ttu-id="563f8-171">Las clases y incluidas en las herramientas son totalmente compatibles con `EdgeDriver` `EdgeDriverService` los equivalentes integrados en Selenio 4.</span><span class="sxs-lookup"><span data-stu-id="563f8-171">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium 4.</span></span>  

<span data-ttu-id="563f8-172">Si usa Selenio 3, siga estos pasos para agregar las Herramientas de [Selenio para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] y [Selenio 3][|::ref3::|] al proyecto.</span><span class="sxs-lookup"><span data-stu-id="563f8-172">If you are using Selenium 3, use the following steps to add the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] and [Selenium 3][|::ref3::|] to your project.</span></span>

#### [<a name="c"></a><span data-ttu-id="563f8-173">C#</span><span class="sxs-lookup"><span data-stu-id="563f8-173">C#</span></span>](#tab/c-sharp/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="563f8-174">Agregue los [paquetes Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] y [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] al proyecto de [.NuGet][NugetCLI] NET con la CLI o Visual Studio [.][VisualStudio]</span><span class="sxs-lookup"><span data-stu-id="563f8-174">Add the [Microsoft.Edge.SeleniumTools][NugetPackagesMicrosoftEdgeSeleniumtools] and [Selenium.WebDriver][NugetPackagesSeleniumWebdriver31410] packages to your .NET project using the [NuGet CLI][NugetCLI] or [Visual Studio][VisualStudio].</span></span>  

#### [<a name="python"></a><span data-ttu-id="563f8-175">Python</span><span class="sxs-lookup"><span data-stu-id="563f8-175">Python</span></span>](#tab/python/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="563f8-176">Use [pip][PythonPip] para instalar los [paquetes msedge-selenium-tools][PythonSeleniumTools] y [selenio.][PythonSelenium]</span><span class="sxs-lookup"><span data-stu-id="563f8-176">Use [pip][PythonPip] to install the [msedge-selenium-tools][PythonSeleniumTools] and [selenium][PythonSelenium] packages.</span></span>  

```python
pip install msedge-selenium-tools selenium==3.141
```  

#### [<a name="java"></a><span data-ttu-id="563f8-177">Java</span><span class="sxs-lookup"><span data-stu-id="563f8-177">Java</span></span>](#tab/java/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="563f8-178">Si el Java usa Maven, copie y pegue la siguiente dependencia en el archivo para `pom.xml` agregar [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span><span class="sxs-lookup"><span data-stu-id="563f8-178">If your Java project uses Maven, copy and paste the following dependency to your `pom.xml` file to add [msedge-selenium-tools-java][SonatypeMavenRepositorySearch].</span></span>  

```xml
<dependency>
    <groupId>com.microsoft.edge</groupId>
    <artifactId>msedge-selenium-tools-java</artifactId>
    <version>[3.141.0,)</version>
</dependency>
```  

<span data-ttu-id="563f8-179">El Java también está disponible para descargar directamente en la página [Herramientas de selenio para Microsoft Edge versiones.][GithubMicrosoftEdgeSeleniumToolsReleases]</span><span class="sxs-lookup"><span data-stu-id="563f8-179">The Java package is also available to download directly on the [Selenium Tools for Microsoft Edge Releases page][GithubMicrosoftEdgeSeleniumToolsReleases].</span></span>  

#### [<a name="javascript"></a><span data-ttu-id="563f8-180">JavaScript</span><span class="sxs-lookup"><span data-stu-id="563f8-180">JavaScript</span></span>](#tab/javascript/)  

<a id="selenium-tools-install"></a>  

<span data-ttu-id="563f8-181">Use [npm][JavaScript|::ref4::|] para instalar los paquetes [edge-selenium-tools][JavaScriptSeleniumTools] y [selenium-webdriver.][JavaScriptSelenium]</span><span class="sxs-lookup"><span data-stu-id="563f8-181">Use [npm][JavaScript|::ref4::|] to install the [edge-selenium-tools][JavaScriptSeleniumTools] and [selenium-webdriver][JavaScriptSelenium] packages.</span></span>  

```javascript
npm install @microsoft/edge-selenium-tools selenium-webdriver
```  

* * *  


## <a name="automate-microsoft-edge-chromium-with-webdriver"></a><span data-ttu-id="563f8-182">Automatizar Microsoft Edge (Chromium) con WebDriver</span><span class="sxs-lookup"><span data-stu-id="563f8-182">Automate Microsoft Edge (Chromium) with WebDriver</span></span>  

<span data-ttu-id="563f8-183">Para automatizar un explorador con WebDriver, primero debe iniciar una sesión de WebDriver con el marco de prueba de WebDriver preferido.</span><span class="sxs-lookup"><span data-stu-id="563f8-183">To automate a browser using WebDriver, you must first start a WebDriver session using your preferred WebDriver testing framework.</span></span>  <span data-ttu-id="563f8-184">Una sesión es una única instancia en ejecución de un explorador controlado mediante comandos de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="563f8-184">A session is a single running instance of a browser controlled using WebDriver commands.</span></span>  <span data-ttu-id="563f8-185">Inicie una sesión de WebDriver para iniciar una nueva instancia del explorador.</span><span class="sxs-lookup"><span data-stu-id="563f8-185">Start a WebDriver session to launch a new browser instance.</span></span>  <span data-ttu-id="563f8-186">La instancia del explorador iniciada permanece abierta hasta que cierre la sesión de WebDriver.</span><span class="sxs-lookup"><span data-stu-id="563f8-186">The launched browser instance remains open until you close the WebDriver session.</span></span>  

<span data-ttu-id="563f8-187">El siguiente contenido le guiará a través del uso de Selenium para iniciar una sesión de WebDriver con Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-187">The following content walks you through using Selenium to start a WebDriver session with Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="563f8-188">Puede ejecutar estos ejemplos con Selenio 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="563f8-188">You can run these examples using either Selenium 3 or 4.</span></span>  <span data-ttu-id="563f8-189">Para usar WebDriver con Selenium 3, se debe instalar el paquete [selenio Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package.</span><span class="sxs-lookup"><span data-stu-id="563f8-189">To use WebDriver with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package must be installed.</span></span>  

> [!NOTE]
> <span data-ttu-id="563f8-190">En este artículo se proporcionan instrucciones para usar el marco selenio, pero puede usar cualquier biblioteca, marco y lenguaje de programación compatible con WebDriver.</span><span class="sxs-lookup"><span data-stu-id="563f8-190">This article provides instructions for using the Selenium framework, but you can use any library, framework, and programming language that supports WebDriver.</span></span>  <span data-ttu-id="563f8-191">Para realizar las mismas tareas con otro marco, consulte la documentación oficial para su marco de elección.</span><span class="sxs-lookup"><span data-stu-id="563f8-191">To accomplish the same tasks using another framework, consult the official documentation for your framework of choice.</span></span>

### <a name="automate-microsoft-edge-chromium"></a><span data-ttu-id="563f8-192">Automatizar Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="563f8-192">Automate Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="563f8-193">Selenio usa la `EdgeDriver` clase para administrar una sesión Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-193">Selenium uses the `EdgeDriver` class to manage a Microsoft Edge \(Chromium\) session.</span></span>  <span data-ttu-id="563f8-194">Para iniciar una sesión y automatizar Microsoft Edge \(Chromium\), cree un nuevo objeto y pásalo un objeto con la propiedad `EdgeDriver` `EdgeOptions` establecida en `UseChromium` `true` .</span><span class="sxs-lookup"><span data-stu-id="563f8-194">To start a session and automate Microsoft Edge \(Chromium\), create a new `EdgeDriver` object and pass it an `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<a name="c"></a><span data-ttu-id="563f8-195">C#</span><span class="sxs-lookup"><span data-stu-id="563f8-195">C#</span></span>](#tab/c-sharp/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="563f8-196">Python</span><span class="sxs-lookup"><span data-stu-id="563f8-196">Python</span></span>](#tab/python/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="563f8-197">Java</span><span class="sxs-lookup"><span data-stu-id="563f8-197">Java</span></span>](#tab/java/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

<span data-ttu-id="563f8-198">La clase solo admite Microsoft Edge \(Chromium\) y no admite `EdgeDriver` Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="563f8-198">The `EdgeDriver` class only supports Microsoft Edge \(Chromium\), and doesn't support Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="563f8-199">Para el uso básico, puede crear un `EdgeDriver` sin proporcionar `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="563f8-199">For basic usage, you can create an `EdgeDriver` without providing `EdgeOptions`.</span></span>  

```java
EdgeDriver driver = new EdgeDriver();
```  

#### [<a name="javascript"></a><span data-ttu-id="563f8-200">JavaScript</span><span class="sxs-lookup"><span data-stu-id="563f8-200">JavaScript</span></span>](#tab/javascript/)  

<a id="drive-microsoft-edge-chromium-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);

let driver = edge.Driver.createSession(options);
```  

* * *  

> [!NOTE]
> <span data-ttu-id="563f8-201">Si el administrador de TI ha establecido la directiva [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] en , el controlador de Microsoft Edge no puede conducir `2` Microsoft Edge \(Chromium\), ya que el controlador usa [Microsoft Edge DevTools][DevtoolsIndex]. [][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]</span><span class="sxs-lookup"><span data-stu-id="563f8-201">If your IT admin has set the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy to `2`,  [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] is blocked from driving Microsoft Edge \(Chromium\), because the driver uses the [Microsoft Edge DevTools][DevtoolsIndex].</span></span>  <span data-ttu-id="563f8-202">Asegúrese de [que la directiva DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] está establecida en o para automatizar Microsoft Edge `0` `1` (Chromium).</span><span class="sxs-lookup"><span data-stu-id="563f8-202">Ensure the [DeveloperToolsAvailability][DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability] policy is set to `0` or `1` to automate Microsoft Edge (Chromium).</span></span>  

### <a name="choose-specific-browser-binaries-chromium-only"></a><span data-ttu-id="563f8-203">Elegir archivos binarios de explorador específicos (solo Chromium explorador)</span><span class="sxs-lookup"><span data-stu-id="563f8-203">Choose Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="563f8-204">Puede iniciar una sesión de WebDriver con archivos binarios Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-204">You can start a WebDriver session with specific Microsoft Edge \(Chromium\) binaries.</span></span>  <span data-ttu-id="563f8-205">Por ejemplo, puede ejecutar pruebas con los canales [Microsoft Edge vista previa,][MicrosoftedgeinsiderDownload] como Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="563f8-205">For example, you can run tests using the [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<a name="c"></a><span data-ttu-id="563f8-206">C#</span><span class="sxs-lookup"><span data-stu-id="563f8-206">C#</span></span>](#tab/c-sharp/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<a name="python"></a><span data-ttu-id="563f8-207">Python</span><span class="sxs-lookup"><span data-stu-id="563f8-207">Python</span></span>](#tab/python/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options = options)
```  

#### [<a name="java"></a><span data-ttu-id="563f8-208">Java</span><span class="sxs-lookup"><span data-stu-id="563f8-208">Java</span></span>](#tab/java/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.setBinary("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

EdgeDriver driver = new EdgeDriver(options);
```  

#### [<a name="javascript"></a><span data-ttu-id="563f8-209">JavaScript</span><span class="sxs-lookup"><span data-stu-id="563f8-209">JavaScript</span></span>](#tab/javascript/)  

<a id="choose-specific-browser-binaries-chrome-only-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.setBinaryPath("C:\\Program Files (x86)\\Microsoft\\Edge Beta\\Application\\msedge.exe");

let driver = edge.Driver.createSession(options);
```  

* * *  

### <a name="customize-the-microsoft-edge-driver-service"></a><span data-ttu-id="563f8-210">Personalizar el servicio Microsoft Edge controladores</span><span class="sxs-lookup"><span data-stu-id="563f8-210">Customize the Microsoft Edge Driver Service</span></span>  

#### [<a name="c"></a><span data-ttu-id="563f8-211">C#</span><span class="sxs-lookup"><span data-stu-id="563f8-211">C#</span></span>](#tab/c-sharp/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="563f8-212">Cuando se usa la clase para crear una instancia de clase, se crea e inicia la clase adecuada para `EdgeOptions` `EdgeDriver` Microsoft Edge `EdgeDriverService` \(EdgeHTML\) o Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-212">When you use the `EdgeOptions` class to create an `EdgeDriver` class instance, it creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="563f8-213">Si desea crear un , use el método para crear uno configurado para `EdgeDriverService` `CreateChromiumService()` Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-213">If you want to create an `EdgeDriverService`, use the `CreateChromiumService()` method to create one configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="563f8-214">El `CreateChromiumService()` método es útil cuando necesita agregar personalizaciones.</span><span class="sxs-lookup"><span data-stu-id="563f8-214">The `CreateChromiumService()` method is useful when you need to add customizations.</span></span>  <span data-ttu-id="563f8-215">Por ejemplo, el siguiente código inicia una salida de registro detallada.</span><span class="sxs-lookup"><span data-stu-id="563f8-215">For example, the following code starts verbose log output.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE] 
><span data-ttu-id="563f8-216">No es necesario proporcionar el objeto `EdgeOptions` al pasar a la `EdgeDriverService` `EdgeDriver` instancia.</span><span class="sxs-lookup"><span data-stu-id="563f8-216">You do not need to provide the `EdgeOptions` object when you pass `EdgeDriverService` to the `EdgeDriver` instance.</span></span>  <span data-ttu-id="563f8-217">La clase usa las opciones predeterminadas para `EdgeDriver` Microsoft Edge \(EdgeHTML\) o Microsoft Edge \(Chromium\) en función del servicio que proporcione.</span><span class="sxs-lookup"><span data-stu-id="563f8-217">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) based on the service you provide.</span></span>  
> <span data-ttu-id="563f8-218">Sin embargo, si desea proporcionar ambos y clases, asegúrese de que ambos están `EdgeDriverService` `EdgeOptions` configurados para la misma versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="563f8-218">However, if you want to provide both `EdgeDriverService` and `EdgeOptions` classes, ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="563f8-219">Por ejemplo, puede usar una clase Microsoft Edge \(EdgeHTML\) predeterminada y Chromium `EdgeDriverService` propiedades de la `EdgeOptions` clase.</span><span class="sxs-lookup"><span data-stu-id="563f8-219">For example, you may use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="563f8-220">La `EdgeDriver` clase genera un error para evitar el uso de versiones diferentes.</span><span class="sxs-lookup"><span data-stu-id="563f8-220">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<a name="python"></a><span data-ttu-id="563f8-221">Python</span><span class="sxs-lookup"><span data-stu-id="563f8-221">Python</span></span>](#tab/python/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="563f8-222">Cuando se usa Python, `Edge` el objeto crea y administra el archivo `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="563f8-222">When you use Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="563f8-223">Para configurar `EdgeService` el argumento , pase argumentos adicionales al objeto como se indica en el código `Edge` siguiente.</span><span class="sxs-lookup"><span data-stu-id="563f8-223">To configure the `EdgeService`, pass extra arguments to the `Edge` object as indicated in the following code.</span></span>  

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### [<a name="java"></a><span data-ttu-id="563f8-224">Java</span><span class="sxs-lookup"><span data-stu-id="563f8-224">Java</span></span>](#tab/java/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="563f8-225">Use el `createDefaultService()` método para crear una configuración para Microsoft Edge `EdgeDriverService` \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="563f8-225">Use the `createDefaultService()` method to create an `EdgeDriverService` configured for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="563f8-226">Use Java del sistema para personalizar los servicios de controladores en Java.</span><span class="sxs-lookup"><span data-stu-id="563f8-226">Use Java system properties to customize driver services in Java.</span></span>  <span data-ttu-id="563f8-227">Por ejemplo, el siguiente código usa la `"webdriver.edge.verboseLogging"` propiedad para activar la salida de registro detallado.</span><span class="sxs-lookup"><span data-stu-id="563f8-227">For example, the following code uses the `"webdriver.edge.verboseLogging"` property to turn on verbose log output.</span></span>  

```java
System.setProperty("webdriver.edge.verboseLogging", "true");
EdgeDriverService service = EdgeDriverService.createDefaultService();
EdgeOptions options = new EdgeOptions();
EdgeDriver driver = new EdgeDriver(service, options);
```  

#### [<a name="javascript"></a><span data-ttu-id="563f8-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="563f8-228">JavaScript</span></span>](#tab/javascript/)  

<a id="customize-microsoft-edge-driver-services-code"></a>  

<span data-ttu-id="563f8-229">Cuando use JavaScript, cree y configure una `Service` con la `ServiceBuilder` clase.</span><span class="sxs-lookup"><span data-stu-id="563f8-229">When you use JavaScript, create and configure a `Service` with the `ServiceBuilder` class.</span></span>  <span data-ttu-id="563f8-230">Opcionalmente, puede pasar el objeto al objeto, que inicia `Service` `Driver` \(y detiene\) el servicio por usted.</span><span class="sxs-lookup"><span data-stu-id="563f8-230">Optionally, you can pass the `Service` object to the `Driver` object, which starts \(and stops\) the service for you.</span></span>  
<span data-ttu-id="563f8-231">Para configurar `Service` el método , ejecute otro método en la clase antes de usar el `ServiceBuilder` `build()` método.</span><span class="sxs-lookup"><span data-stu-id="563f8-231">To configure the `Service`, run another method in the `ServiceBuilder` class before you use the `build()` method.</span></span>  <span data-ttu-id="563f8-232">A continuación, `service` pase el parámetro as a en el `Driver.createSession()` método.</span><span class="sxs-lookup"><span data-stu-id="563f8-232">Then pass the `service` as a parameter in the `Driver.createSession()` method.</span></span>  

```javascript
let service = new edge.ServiceBuilder().enableVerboseLogging().build();
let driver = edge.Driver.createSession(options, service);
```  

* * *  

### <a name="use-chromium-specific-options"></a><span data-ttu-id="563f8-233">Usar Chromium-Specific opciones</span><span class="sxs-lookup"><span data-stu-id="563f8-233">Use Chromium-Specific Options</span></span>  

<span data-ttu-id="563f8-234">Si establece la propiedad en , puede usar la clase para tener acceso a las mismas propiedades y métodos específicos de Chromium que se usan al automatizar otros exploradores Chromium `UseChromium` `true` `EdgeOptions` web. [][WebdriverCapabilitiesEdgeOptions]</span><span class="sxs-lookup"><span data-stu-id="563f8-234">If you set the `UseChromium` property to `true`, you can use the `EdgeOptions` class to access the same [Chromium-specific properties and methods][WebdriverCapabilitiesEdgeOptions] that are used when you automate other Chromium browsers.</span></span>  

#### [<a name="c"></a><span data-ttu-id="563f8-235">C#</span><span class="sxs-lookup"><span data-stu-id="563f8-235">C#</span></span>](#tab/c-sharp/)  

<a id="use-chromium-specific-options-code"></a>  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<a name="python"></a><span data-ttu-id="563f8-236">Python</span><span class="sxs-lookup"><span data-stu-id="563f8-236">Python</span></span>](#tab/python/)  

<a id="use-chromium-specific-options-code"></a>  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument("headless")
options.add_argument("disable-gpu")
```  

#### [<a name="java"></a><span data-ttu-id="563f8-237">Java</span><span class="sxs-lookup"><span data-stu-id="563f8-237">Java</span></span>](#tab/java/)  

<a id="use-chromium-specific-options-code"></a>  

```java
EdgeOptions options = new EdgeOptions();
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

#### [<a name="javascript"></a><span data-ttu-id="563f8-238">JavaScript</span><span class="sxs-lookup"><span data-stu-id="563f8-238">JavaScript</span></span>](#tab/javascript/)  

<a id="use-chromium-specific-options-code"></a>  

```javascript
let options = new edge.Options();
options.setEdgeChromium(true);
options.addArguments("headless");
options.addArguments("disable-gpu");
```  

* * *  

> [!NOTE]
> <span data-ttu-id="563f8-239">Si la propiedad está establecida en , no puede usar propiedades y métodos `UseChromium` `true` para Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="563f8-239">If the `UseChromium` property is set to `true`, you are not able to use properties and methods for Microsoft Edge \(EdgeHTML\).</span></span>  


## <a name="other-webdriver-installation-options"></a><span data-ttu-id="563f8-240">Otras opciones de instalación de WebDriver</span><span class="sxs-lookup"><span data-stu-id="563f8-240">Other WebDriver installation options</span></span>  

### <a name="docker"></a><span data-ttu-id="563f8-241">Docker</span><span class="sxs-lookup"><span data-stu-id="563f8-241">Docker</span></span>  

<span data-ttu-id="563f8-242">Si usa [Docker,][DockerHub]ejecute el siguiente comando para descargar una imagen preconfigurada con Microsoft Edge \(Chromium\) y [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] preinstalado.</span><span class="sxs-lookup"><span data-stu-id="563f8-242">If you use [Docker][DockerHub], run the following command to download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperMicrosoftEdgeToolsWebdriver] pre-installed.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="563f8-243">Para obtener más información, vaya al [contenedor msedgedriver en Docker Hub][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="563f8-243">For more information, navigate to the [msedgedriver container on Docker Hub][DockerHubMsedgedriver].</span></span>  


## <a name="testing-internet-explorer"></a><span data-ttu-id="563f8-244">Probar Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="563f8-244">Testing Internet Explorer</span></span>

<span data-ttu-id="563f8-245">Para probar los sitios que requieren Internet Explorer, use [El controlador de Internet Explorer][GithubSeleniumHqWikiIEDriver] con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="563f8-245">To test sites that require Internet Explorer, use [Internet Explorer Driver][GithubSeleniumHqWikiIEDriver] with Internet Explorer.</span></span>  <span data-ttu-id="563f8-246">El proyecto Selenio mantiene el controlador de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="563f8-246">Internet Explorer Driver is maintained by the Selenium project.</span></span>  <span data-ttu-id="563f8-247">Aunque Microsoft Edge admite el modo IE, no puedes usar Microsoft Edge driver con Microsoft Edge para probar sitios en modo IE.</span><span class="sxs-lookup"><span data-stu-id="563f8-247">Even though Microsoft Edge supports IE Mode, you can't use Microsoft Edge Driver with Microsoft Edge to test sites in IE Mode.</span></span>


## <a name="application-guard"></a><span data-ttu-id="563f8-248">Protección de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="563f8-248">Application Guard</span></span>

<span data-ttu-id="563f8-249">Los sitios de confianza que usan Protección de aplicaciones de Microsoft Defender (Protección de aplicaciones) se pueden automatizar con Microsoft Edge controlador.</span><span class="sxs-lookup"><span data-stu-id="563f8-249">Trusted sites that use Microsoft Defender Application Guard (Application Guard) can be automated using Microsoft Edge Driver.</span></span>

<span data-ttu-id="563f8-250">Los sitios que no son de confianza que usan Application Guard no se pueden automatizar ni manipular con Microsoft Edge controlador.</span><span class="sxs-lookup"><span data-stu-id="563f8-250">Untrusted sites that use Application Guard cannot be automated or manipulated using Microsoft Edge Driver.</span></span>  <span data-ttu-id="563f8-251">Application Guard inicia sitios que no son de confianza en un contenedor y este contenedor no expone el puerto de depuración remota que Microsoft Edge Driver debe comunicarse con el sitio.</span><span class="sxs-lookup"><span data-stu-id="563f8-251">Application Guard launches untrusted sites in a container, and this container doesn't expose the remote debugging port that Microsoft Edge Driver needs to communicate with the site.</span></span>

<span data-ttu-id="563f8-252">El administrador de la empresa define los sitios de confianza, incluidos los recursos en la nube y las redes internas.</span><span class="sxs-lookup"><span data-stu-id="563f8-252">Your enterprise administrator defines what are trusted sites, including cloud resources and internal networks.</span></span>  <span data-ttu-id="563f8-253">Los sitios que no están en la lista de sitios de confianza se consideran no confiables.</span><span class="sxs-lookup"><span data-stu-id="563f8-253">Sites that aren't in the trusted sites list are considered untrusted.</span></span>  <span data-ttu-id="563f8-254">Microsoft Edge El controlador puede automatizar las ventanas de InPrivate y los sitios de la lista de sitios de confianza.</span><span class="sxs-lookup"><span data-stu-id="563f8-254">Microsoft Edge Driver can automate both InPrivate windows, and sites in the trusted sites list.</span></span>

<span data-ttu-id="563f8-255">Para obtener más información acerca de Application Guard, vaya a:</span><span class="sxs-lookup"><span data-stu-id="563f8-255">For more information about Application Guard, navigate to:</span></span> 

*  [<span data-ttu-id="563f8-256">Compatibilidad de Microsoft Edge para la Protección de aplicaciones de Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="563f8-256">Microsoft Edge support for Microsoft Defender Application Guard</span></span>][DeployedgeMicrosoftEdgeSecurityWindowsDefenderApplicationGuard]
*  [<span data-ttu-id="563f8-257">Protección de aplicaciones de Microsoft Defender general</span><span class="sxs-lookup"><span data-stu-id="563f8-257">Microsoft Defender Application Guard overview</span></span>][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]


## <a name="see-also"></a><span data-ttu-id="563f8-258">Vea también</span><span class="sxs-lookup"><span data-stu-id="563f8-258">See also</span></span>

*  <span data-ttu-id="563f8-259">[Documentación de Selenio:][SeleniumDocumentation] información sobre WebDriver en el contexto de Selenio y cómo escribir pruebas automatizadas de WebDriver con Selenio.</span><span class="sxs-lookup"><span data-stu-id="563f8-259">[Selenium documentation][SeleniumDocumentation] - Information about WebDriver in the context of Selenium, and how to write automated WebDriver tests using Selenium.</span></span>


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="563f8-260">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="563f8-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="563f8-261">El Microsoft Edge está deseando escuchar sus comentarios acerca del uso de WebDriver, marcos de prueba de WebDriver (como Selenio) y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="563f8-261">The Microsoft Edge team is eager to hear your feedback about using WebDriver, WebDriver testing frameworks (such as Selenium), and Microsoft Edge.</span></span>  <span data-ttu-id="563f8-262">Para enviar al equipo sus preguntas \*\*\*\* y comentarios, elija el icono Enviar comentarios en el Microsoft Edge DevTools o envíe un [tweet][TwitterTweetEdgeDevTools]@EdgeDevTools .</span><span class="sxs-lookup"><span data-stu-id="563f8-262">To send the team your questions and comments, choose the **Send Feedback** icon in the Microsoft Edge DevTools or send a tweet [@EdgeDevTools][TwitterTweetEdgeDevTools].</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en las Herramientas de desarrollo del borde de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="563f8-264">El **icono Enviar comentarios** en el Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="563f8-264">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  


<!-- links -->  
[DevtoolsIndex]: ../devtools-guide-chromium/index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[WebdriverCapabilitiesEdgeOptions]: ./capabilities-edge-options.md "Funcionalidades y EdgeOptions | Microsoft Docs"  
<!-- external links -->
[DeployedgeMicrosoftEdgePoliciesDevelopertoolsavailability]: /deployedge/microsoft-edge-policies#developertoolsavailability "DeveloperToolsAvailability - Microsoft Edge- Directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgeSecurityWindowsDefenderApplicationGuard]: /deployedge/microsoft-edge-security-windows-defender-application-guard "Microsoft Edge compatibilidad con Protección de aplicaciones de Microsoft Defender | Microsoft Docs"

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Protección de aplicaciones de Microsoft Defender (Windows 10): Windows seguridad | Microsoft Docs"  

[DockerHub]: https://hub.docker.com "Docker Hub"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Concentrador de Docker"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "microsoft/edge-selenium-tools | GitHub"  
[GithubMicrosoftEdgeSeleniumToolsReleases]: https://github.com/microsoft/edge-selenium-tools/releases "microsoft/edge-selenium-tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SelenioHQ/selenio | GitHub"  
[GithubSeleniumHqWikiIEDriver]: https://github.com/SeleniumHQ/selenium/wiki/InternetExplorerDriver "Controlador de Internet Explorer: selenio | GitHub"

[JavaScriptnpm]: https://www.npmjs.com/ "npm"  
[JavaScriptSeleniumTools]: https://www.npmjs.com/package/@microsoft/edge-selenium-tools "@microsoft/edge-selenium-tools | npm"  
[JavaScriptSelenium]: https://www.npmjs.com/package/selenium-webdriver "selenium-webdriver | npm"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Microsoft Edge Controlador | Microsoft Edge Programador"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar nuevo Microsoft Edge explorador"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[NugetCLI]:https://www.nuget.org/packages/NuGet.CommandLine/ "NuGet. CommandLine | NuGet Galería"  
[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft.Edge.SeleniumTools | NuGet Galería"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium.WebDriver 3.141.0 | NuGet Galería"  
[NugetPackagesSeleniumWebdriver400beta02]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-beta2 "Selenium.WebDriver 4.0.0-beta2 | NuGet Galería"  

[PythonPip]: https://pypi.org/project/pip/ "pip | PyPI"  
[PythonSeleniumTools]: https://pypi.org/project/msedge-selenium-tools/ "msedge-selenium-tools | PyPI"  
[PythonSelenium]: https://pypi.org/project/selenium/ "selenio | PyPI"

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDocumentation]: https://www.selenium.dev/documentation "La automatización del explorador selenio Project | Documentación para Selenio"  
[SeleniumInstallingLibraries]: https://www.selenium.dev/documentation/en/selenium_installation/installing_selenium_libraries "Instalación de bibliotecas selenio | Selenio"

[SonatypeMavenRepositorySearch]: https://search.maven.org/artifact/com.microsoft.edge/msedge-selenium-tools-java/3.141.0/jar "Sonatype Maven Central Repository Search | com.microsoft.edge:msedge-selenium-tools-java"

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "WebDriver | W3C"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  

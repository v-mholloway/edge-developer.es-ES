---
description: Obtenga información sobre cómo probar su sitio web o aplicación en Microsoft Edge o automatizar el explorador con Webdriver.
title: Controlador WebDrive (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/18/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, WebDrive, Selenium, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: 810c45e1e8d7fb5a6dbefee1c4ae6eccbe573326
ms.sourcegitcommit: f5dc9d3f1e6629120e036c4298f66de636688cb7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/18/2020
ms.locfileid: "10659385"
---
# <span data-ttu-id="a5825-104">Controlador WebDrive (cromo)</span><span class="sxs-lookup"><span data-stu-id="a5825-104">WebDriver (Chromium)</span></span>  

<span data-ttu-id="a5825-105">La API [Webdriver][W3CWebdriver] W3C es una plataforma e interfaz independiente del idioma y Protocolo de conexión que permite a los programas o las secuencias de comandos controlar el comportamiento de un explorador Web, como Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="a5825-105">The W3C [WebDriver][W3CWebdriver] API is a platform and language-neutral interface and wire protocol allowing programs or scripts to control the behavior of a web browser, like Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="a5825-106">Webdriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="a5825-106">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="a5825-107">Las pruebas y simuladores de WebDrive se diferencian de las pruebas unitarias de JavaScript porque el acceso a la funcionalidad y la información que JavaScript se ejecuta en el explorador no es posible y WebDrive permite simular eventos de usuario o eventos a nivel de OS con más precisión.</span><span class="sxs-lookup"><span data-stu-id="a5825-107">WebDriver tests and simulations differ from JavaScript unit tests because WebDriver has access to functionality and information that JavaScript running in the browser does not, and WebDrive is able to more accurately simulate user events or OS-level events.</span></span>  <span data-ttu-id="a5825-108">El controlador WebDrive es capaz de administrar las pruebas en varias ventanas, pestañas y páginas web en una sola sesión de prueba.</span><span class="sxs-lookup"><span data-stu-id="a5825-108">WebDriver is able to manage testing across multiple windows, tabs and webpages in a single test session.</span></span>  

<span data-ttu-id="a5825-109">A continuación se explica cómo empezar a usar Webdriver para Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="a5825-109">Here is how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="a5825-110">Instalar Microsoft Edge (cromo)</span><span class="sxs-lookup"><span data-stu-id="a5825-110">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="a5825-111">Si todavía no lo ha hecho, [instale Microsoft Edge (cromo)][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="a5825-111">If you have not already, [install Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="a5825-112">Si estás usando una versión preinstalada de Microsoft Edge en tu equipo, verifica que dispongas de Microsoft Edge \ (cromo \) y no Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="a5825-112">If you are using a pre-installed version of Microsoft Edge on your machine, verify that you have Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="a5825-113">Una forma rápida de comprobar es cargar `edge://settings/help` en el explorador y confirmar que el número de versión es V75 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a5825-113">A quick way to check is to load `edge://settings/help` in the browser and confirm that the version number is v75 or later.</span></span>  

## <span data-ttu-id="a5825-114">Descargar el controlador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5825-114">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="a5825-115">Webdriver requiere un controlador específico del explorador para automatizar cada explorador.</span><span class="sxs-lookup"><span data-stu-id="a5825-115">WebDriver requires a browser-specific driver to automate each browser.</span></span>  <span data-ttu-id="a5825-116">Para Microsoft Edge \ (cromo \), Webdriver requiere el [controlador Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] adecuado para la compilación de Microsoft Edge que desea probar o automatizar.</span><span class="sxs-lookup"><span data-stu-id="a5825-116">For Microsoft Edge \(Chromium\), WebDriver requires the appropriate [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] for the build of Microsoft Edge you want to test or automate.</span></span>  

<span data-ttu-id="a5825-117">Para encontrar su número de compilación correcto, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="a5825-117">To find your correct build number, use the following steps.</span></span>  

1.  <span data-ttu-id="a5825-118">Iniciar Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5825-118">Launch Microsoft Edge</span></span> 
1.  <span data-ttu-id="a5825-119">Ver la versión de Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="a5825-119">View the Microsoft Edge \(Chromium\) version.</span></span>  
    *   <span data-ttu-id="a5825-120">Ve a</span><span class="sxs-lookup"><span data-stu-id="a5825-120">Navigate to</span></span> `edge://settings/help`  
    *   <span data-ttu-id="a5825-121">Seleccionar la `...`  >  **configuración**  >   **de Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="a5825-121">Select `...` > **Settings** >  **About Microsoft Edge**</span></span>  
1.  <span data-ttu-id="a5825-122">Compruebe si la versión de WebDrive es correcta para su compilación, de modo que se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="a5825-122">Verify the correct version of WebDriver for your build ensures, so it runs correctly.</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="El número de compilación para Microsoft Edge Canarias el 14 de enero de 2020":::
   <span data-ttu-id="a5825-124">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="a5825-124">Figure 1.</span></span>  <span data-ttu-id="a5825-125">El número de compilación para Microsoft Edge Canarias el 14 de enero de 2020</span><span class="sxs-lookup"><span data-stu-id="a5825-125">The build number for Microsoft Edge Canary on January 14, 2020</span></span>  
:::image-end:::  

<span data-ttu-id="a5825-126">Ahora, [descarga la versión coincidente del controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="a5825-126">Now, [download the matching version of Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Sección de descargas de la página del controlador de Microsoft Edge":::
   <span data-ttu-id="a5825-128">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="a5825-128">Figure 2.</span></span>  <span data-ttu-id="a5825-129">Sección de descargas de la página del [controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads]</span><span class="sxs-lookup"><span data-stu-id="a5825-129">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="a5825-130">Microsoft Edge \ (EdgeHTML \) no funciona con el [controlador de Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="a5825-130">Microsoft Edge \(EdgeHTML\) does not work with [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="a5825-131">Para automatizar Microsoft Edge \ (EdgeHTML \), debe descargar [Microsoft Webdriver para Microsoft Edge \ (EdgeHTML \)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="a5825-131">To automate Microsoft Edge \(EdgeHTML\), you must download [Microsoft WebDriver for Microsoft Edge \(EdgeHTML\)][Webdriver].</span></span>  

## <span data-ttu-id="a5825-132">Elegir un enlace de idioma de controlador</span><span class="sxs-lookup"><span data-stu-id="a5825-132">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="a5825-133">El último componente que debe descargar es un controlador de cliente específico del idioma.</span><span class="sxs-lookup"><span data-stu-id="a5825-133">The last component you must download is a language-specific client driver.</span></span>  <span data-ttu-id="a5825-134">El enlace de idioma traduce el código que escribiste en Python, Java, C \ #, Ruby y JavaScript en comandos que el controlador de Microsoft Edge que [descargaste en la sección anterior](#download-microsoft-edge-driver) puede ejecutarse en Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="a5825-134">The language binding translates the code you write in Python, Java, C\#, Ruby, and JavaScript into commands that the Microsoft Edge Driver you [downloaded in the previous section](#download-microsoft-edge-driver) is able to run in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="a5825-135">[Descargue el enlace de idioma de Webdrives que prefiera][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="a5825-135">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="a5825-136">El equipo de Microsoft Edge es muy recomendable [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] o una versión posterior, ya que cuenta con compatibilidad integrada para Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="a5825-136">The Microsoft Edge team highly recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, since it has built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="a5825-137">Sin embargo, puedes conducir a Microsoft Edge \ (cromo \) en todas las versiones anteriores de Selenium, incluida la versión estable actual de Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="a5825-137">However, you are able to drive Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="a5825-138">Si anteriormente estabas automatizado o probando Microsoft Edge \ (cromo \) con `ChromeDriver` y `ChromeOptions` , el código de Webdriver no se ejecuta correctamente en Microsoft Edge V80 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a5825-138">If you were previously automating or testing Microsoft Edge \(Chromium\) by using `ChromeDriver` and `ChromeOptions`, your WebDriver code does not run successfully against Microsoft Edge v80 or later.</span></span>  <span data-ttu-id="a5825-139">Este es un cambio importante y Microsoft Edge \ (cromo \) ya no acepta los comandos.</span><span class="sxs-lookup"><span data-stu-id="a5825-139">This is a breaking change and Microsoft Edge \(Chromium\) no longer accepts the commands.</span></span>  <span data-ttu-id="a5825-140">Debe cambiar las pruebas para usar el `EdgeOptions` controlador de clase y [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="a5825-140">You must change your tests to use the `EdgeOptions` class and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="a5825-141">Uso de Selenium 3</span><span class="sxs-lookup"><span data-stu-id="a5825-141">Using Selenium 3</span></span>  

<span data-ttu-id="a5825-142">[Selenium 3][|::ref1::|] es la versión estable más reciente de Selenium.</span><span class="sxs-lookup"><span data-stu-id="a5825-142">[Selenium 3][|::ref1::|] is the latest stable Selenium release.</span></span>  <span data-ttu-id="a5825-143">De forma predeterminada, Selenium 3 impulsa la versión anterior de Microsoft Edge \ (EdgeHTML \) y no tiene compatibilidad integrada para Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="a5825-143">By default, Selenium 3 drives the old Microsoft Edge \(EdgeHTML\), and does not have built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="a5825-144">Para usar Selenium 3 con Microsoft Edge \ (cromo \), instala el paquete [de herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .</span><span class="sxs-lookup"><span data-stu-id="a5825-144">To use Selenium 3 with Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package.</span></span>  <span data-ttu-id="a5825-145">Las Selenium Tools para Microsoft Edge extienden Selenium 3 con un controlador actualizado que te ayudará a escribir pruebas automatizadas de los exploradores Microsoft Edge \ (EdgeHTML \) y nuevos Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="a5825-145">The Selenium Tools for Microsoft Edge extend Selenium 3 with an updated driver to help you write automated tests for both the Microsoft Edge \(EdgeHTML\) and new Microsoft Edge \(Chromium\) browsers.</span></span>  

<span data-ttu-id="a5825-146">Selenium Tools para Microsoft Edge es una solución para desarrolladores que prefieren permanecer en Selenium 3 y los programadores que tienen pruebas de explorador existentes y desean agregar cobertura para el nuevo navegador Microsoft Edge \ (cromo \) sin cambiar las versiones de Selenium.</span><span class="sxs-lookup"><span data-stu-id="a5825-146">Selenium Tools for Microsoft Edge is a solution for developers who prefer to remain on Selenium 3 and developers who have existing browser tests and want to add coverage for the new Microsoft Edge \(Chromium\) browser without changing Selenium versions.</span></span>  <span data-ttu-id="a5825-147">Las `EdgeDriver` `EdgeDriverService` clases y incluidas en las herramientas son totalmente compatibles con los equivalentes integrados en Selenium y ejecutan Microsoft Edge \ (EdgeHTML \) de forma predeterminada, por lo que las herramientas se pueden usar como un nuevo sustituto de colocación para las clases de borde existentes en Selenium.</span><span class="sxs-lookup"><span data-stu-id="a5825-147">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium, and run Microsoft Edge \(EdgeHTML\) by default so the tools may be used as a seamless drop-in replacement for the existing Edge classes in Selenium.</span></span>  

<span data-ttu-id="a5825-148">[Instala las herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] para empezar a usar Microsoft Edge \ (cromo \) con tu proyecto de Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="a5825-148">[Install Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] to begin using Microsoft Edge \(Chromium\) with your Selenium 3 project.</span></span>  

## <span data-ttu-id="a5825-149">Usar Microsoft Edge (cromo) con Webdriver</span><span class="sxs-lookup"><span data-stu-id="a5825-149">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="a5825-150">Los siguientes ejemplos son ejecutables con Selenium 3 o 4.</span><span class="sxs-lookup"><span data-stu-id="a5825-150">The following examples are runnable using either Selenium 3 or 4.</span></span>  <span data-ttu-id="a5825-151">Para usar con Selenium 3, las [herramientas de Selenium para Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] deben estar instaladas.</span><span class="sxs-lookup"><span data-stu-id="a5825-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] must be installed.</span></span>  

### <span data-ttu-id="a5825-152">Uso básico</span><span class="sxs-lookup"><span data-stu-id="a5825-152">Basic Usage</span></span>  

<span data-ttu-id="a5825-153">Para usar con Microsoft Edge \ (EdgeHTML \), simplemente cree una instancia predeterminada de la `EdgeDriver` clase.</span><span class="sxs-lookup"><span data-stu-id="a5825-153">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="a5825-154">C#</span><span class="sxs-lookup"><span data-stu-id="a5825-154">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code" />  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="a5825-155">Fundación</span><span class="sxs-lookup"><span data-stu-id="a5825-155">Python</span></span>](#tab/python/)  

<a id="basic-usage-code" />  

```python
driver = Edge()
```  

* * *  

### <span data-ttu-id="a5825-156">Conduciendo Microsoft Edge (cromo)</span><span class="sxs-lookup"><span data-stu-id="a5825-156">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="a5825-157">Para usar con Microsoft Edge \ (cromo \) en su lugar, cree una `EdgeDriver` clase nueva y pásela el `EdgeOptions` objeto con la `UseChromium` propiedad establecida en `true` .</span><span class="sxs-lookup"><span data-stu-id="a5825-157">To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="a5825-158">C#</span><span class="sxs-lookup"><span data-stu-id="a5825-158">C#</span></span>](#tab/c-sharp/)  

<a id="diving-microsoft-edge-chromium-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="a5825-159">Fundación</span><span class="sxs-lookup"><span data-stu-id="a5825-159">Python</span></span>](#tab/python/)  

<a id="diving-microsoft-edge-chromium-code" />  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

* * *  

### <span data-ttu-id="a5825-160">Elección de archivos binarios de explorador específicos (solo cromo)</span><span class="sxs-lookup"><span data-stu-id="a5825-160">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="a5825-161">Use la `EdgeOptions` clase para elegir un binario específico.</span><span class="sxs-lookup"><span data-stu-id="a5825-161">Use the `EdgeOptions` class to choose a specific binary.</span></span>  <span data-ttu-id="a5825-162">Es útil para probar los [canales de vista previa de Microsoft Edge][MicrosoftedgeinsiderDownload] , como Microsoft Edge beta.</span><span class="sxs-lookup"><span data-stu-id="a5825-162">It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="a5825-163">C#</span><span class="sxs-lookup"><span data-stu-id="a5825-163">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="a5825-164">Fundación</span><span class="sxs-lookup"><span data-stu-id="a5825-164">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

* * *  

### <span data-ttu-id="a5825-165">Personalizar el servicio del controlador Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5825-165">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="a5825-166">C#</span><span class="sxs-lookup"><span data-stu-id="a5825-166">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

<span data-ttu-id="a5825-167">Cuando `EdgeDriver` se crea una instancia de clase con `EdgeOptions` Class, se crea e inicia automáticamente la `EdgeDriverService` clase correspondiente para Microsoft Edge \ (EdgeHTML \) o Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="a5825-167">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="a5825-168">Si desea crear un `EdgeDriverService` , cree uno configurado para Microsoft Edge \ (cromo \) con el `CreateChromiumService()` método.</span><span class="sxs-lookup"><span data-stu-id="a5825-168">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="a5825-169">Es posible que le resulte útil para personalizaciones adicionales, como habilitar la salida de registro detallado en el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="a5825-169">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> <span data-ttu-id="a5825-170">No es necesario proporcionar el `EdgeOptions` objeto cuando se pasa la `EdgeDriver` instancia de clase `EdgeDriverService` .</span><span class="sxs-lookup"><span data-stu-id="a5825-170">You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.</span></span>  <span data-ttu-id="a5825-171">La `EdgeDriver` clase usa las opciones predeterminadas para Microsoft Edge \ (EdgeHTML \) o Microsoft Edge \ (cromo \) según el tipo de servicio que proporcionaste.</span><span class="sxs-lookup"><span data-stu-id="a5825-171">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.</span></span>  
> 
> <span data-ttu-id="a5825-172">Sin embargo, si desea proporcionar tanto una `EdgeDriverService` clase como una `EdgeOptions` , debe asegurarse de que ambas estén configuradas para la misma versión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5825-172">However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="a5825-173">Por ejemplo, no es posible usar una clase predeterminada de Microsoft Edge \ (EdgeHTML \) `EdgeDriverService` y propiedades de cromo en la `EdgeOptions` clase.</span><span class="sxs-lookup"><span data-stu-id="a5825-173">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="a5825-174">La `EdgeDriver` clase produce un error para evitar el uso de versiones diferentes.</span><span class="sxs-lookup"><span data-stu-id="a5825-174">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="a5825-175">Fundación</span><span class="sxs-lookup"><span data-stu-id="a5825-175">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

<span data-ttu-id="a5825-176">Al usar Python, el `Edge` objeto crea y administra el `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="a5825-176">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="a5825-177">Para configurar el `EdgeService` , pase argumentos adicionales al `Edge` objeto:</span><span class="sxs-lookup"><span data-stu-id="a5825-177">To configure the `EdgeService`, pass additional arguments to the `Edge` object:</span></span>

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

* * *  

### <span data-ttu-id="a5825-178">Uso de opciones específicas de cromo</span><span class="sxs-lookup"><span data-stu-id="a5825-178">Using Chromium-Specific Options</span></span>  

<span data-ttu-id="a5825-179">Usar la `EdgeOptions` clase con la `UseChromium` propiedad establecida en `true` proporciona acceso a los mismos métodos y propiedades que están disponibles en la clase [ChromeOptions][SeleniumWebDriverChromeoptionsClass] en Selenium.</span><span class="sxs-lookup"><span data-stu-id="a5825-179">Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.</span></span>  <span data-ttu-id="a5825-180">Por ejemplo, al igual que con otros exploradores de cromo, usa el `EdgeOptions.AddArguments()` método para ejecutar Microsoft Edge \ (cromo \) en el [modo sin encabezado][WikiHeadlessBrowser] en el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="a5825-180">For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.</span></span>  

#### [<span data-ttu-id="a5825-181">C#</span><span class="sxs-lookup"><span data-stu-id="a5825-181">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="a5825-182">Fundación</span><span class="sxs-lookup"><span data-stu-id="a5825-182">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

* * *  

> [!NOTE]
> <span data-ttu-id="a5825-183">Las [propiedades y los métodos específicos de cromo][SeleniumWebDriverChromeoptionsClass] siempre están disponibles, pero no tienen efecto si la `UseChromium` propiedad no está configurada en `true` .</span><span class="sxs-lookup"><span data-stu-id="a5825-183">The [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.</span></span>  <span data-ttu-id="a5825-184">De forma similar, las propiedades y los métodos existentes diseñados para Microsoft Edge \ (EdgeHTML \) no tienen efecto si `UseChromium` propiedad se establece en `true` .</span><span class="sxs-lookup"><span data-stu-id="a5825-184">Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.</span></span>  

## <span data-ttu-id="a5825-185">Otras formas de configurar Webdriver</span><span class="sxs-lookup"><span data-stu-id="a5825-185">Other ways to set up WebDriver</span></span>  

### <span data-ttu-id="a5825-186">Chocolate</span><span class="sxs-lookup"><span data-stu-id="a5825-186">Chocolatey</span></span>  

<span data-ttu-id="a5825-187">Si usas [chocolate][Chocolatey] como el administrador de paquetes, instala el controlador Microsoft Edge ejecutando el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="a5825-187">If you are using [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="a5825-188">Para obtener más información, consulta el [controlador de Selenium de cromo en chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="a5825-188">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="a5825-189">Docker</span><span class="sxs-lookup"><span data-stu-id="a5825-189">Docker</span></span>  

<span data-ttu-id="a5825-190">Si está usando un [acoplador][DockerHub], Descargue una imagen preconfigurada con Microsoft Edge \ (cromo \) y el [controlador Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] ya instalado ejecutando el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="a5825-190">If you are using [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] already installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="a5825-191">Para obtener más información, consulte [contenedor en el concentrador de acoplamiento][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="a5825-191">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="a5825-192">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a5825-192">Getting in touch with the Microsoft Edge DevTools team</span></span>    

<span data-ttu-id="a5825-193">El equipo de Microsoft Edge está ansioso por escuchar sus comentarios sobre el uso de Webdriver, Selenium y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a5825-193">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge!</span></span>  <span data-ttu-id="a5825-194">Use el icono de **comentarios** en las [@EdgeDevTools][TwitterTweetEdgeDevTools] de Microsoft Edge DevTools o Tweet para que el equipo sepa lo que piensa.</span><span class="sxs-lookup"><span data-stu-id="a5825-194">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="El icono de comentarios en el DevTools de Microsoft Edge":::
   <span data-ttu-id="a5825-196">El icono de **comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a5825-196">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

<!-- links -->  

[Webdriver]: ./webdriver.md "Webdriver (EdgeHTML) | Microsoft docs"  

[Chocolatey]: https://chocolatey.org "Chocolate | Software de chocolate"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Controlador de borde de cromo de Selenium | Chocolate"  

[DockerHub]: https://hub.docker.com "Concentrador de acoplamiento"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Concentrador de acoplamiento"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selenium | GitHub"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "Controlador WebDrive | Microsoft Developer"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Descargas: Webdriver | Microsoft Developer"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Descargar nuevo explorador Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium. WebDrive 3.141.0 | Galería de NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium. WebDrive 4.0.0-alpha05 | Galería de NuGet"  

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Descargas | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Clase ChromeOptions: Webdriver | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "Controlador WebDrive"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin periféricos | Wikipedia"  

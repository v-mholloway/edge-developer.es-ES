---
description: Usar Playwright para automatizar y probar en Microsoft Edge
title: Playwright
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, desarrollador, herramientas, automatización, prueba, playwright, nodo, JavaScript, NPM
ms.openlocfilehash: 5ce51864177731dd1bafb845466abb00cce1e0aa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231086"
---
# <span data-ttu-id="023a9-104">Playwright</span><span class="sxs-lookup"><span data-stu-id="023a9-104">Playwright</span></span>  

<span data-ttu-id="023a9-105">[Playwright][|::ref1::|Main] es una biblioteca de [Node.js][NodejsMain] para automatizar [cromo][ChromiumHome], [Firefox][FirefoxMain]y [WebKit][|::ref2::|Main] con una sola API.</span><span class="sxs-lookup"><span data-stu-id="023a9-105">[Playwright][|::ref1::|Main] is a [Node.js][NodejsMain] library to automate [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref2::|Main] with a single API.</span></span>  <span data-ttu-id="023a9-106">Playwright se ha creado para permitir la automatización web entre exploradores, que es siempre verde, compatible, confiable y rápida.</span><span class="sxs-lookup"><span data-stu-id="023a9-106">Playwright is built to enable cross-browser web automation that is ever-green, capable, reliable, and fast.</span></span>  <span data-ttu-id="023a9-107">Como [Microsoft Edge está integrado en la plataforma web de cromo de código abierto][MicrosoftBlogsWindowsExperience20181206], Playwright también puede automatizar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="023a9-107">Since [Microsoft Edge is built on the open-source Chromium web platform][MicrosoftBlogsWindowsExperience20181206], Playwright is also able to automate Microsoft Edge.</span></span>  

<span data-ttu-id="023a9-108">Playwright inicia los [exploradores desatendidas][WikiHeadlessBrowser] de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="023a9-108">Playwright launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="023a9-109">Los exploradores sin encabezado no muestran una interfaz de usuario, por lo que debe usar la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="023a9-109">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="023a9-110">También puede configurar Playwright para que ejecute también Microsoft Edge \ (no headed \) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="023a9-110">You may also configure Playwright to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="023a9-111">De forma predeterminada, al instalar Playwright, el instalador descarga [cromo][ChromiumHome], [Firefox][FirefoxMain]y [WebKit][|::ref3::|Main].</span><span class="sxs-lookup"><span data-stu-id="023a9-111">By default, when you install Playwright, the installer downloads [Chromium][ChromiumHome], [Firefox][FirefoxMain], and [WebKit][|::ref3::|Main].</span></span>  <span data-ttu-id="023a9-112">Si tienes Microsoft Edge \ (cromo \) instalado también, Playwright solo necesita un cambio de código de una línea para probar tu sitio web o aplicación en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="023a9-112">If you have Microsoft Edge \(Chromium\) installed as well, Playwright just needs a one-line code change to test your website or app in Microsoft Edge.</span></span>  <span data-ttu-id="023a9-113">Para descargar Microsoft Edge \ (cromo \), navegue hasta [Descargar Microsoft Edge][MicrosoftEdgeDownload].</span><span class="sxs-lookup"><span data-stu-id="023a9-113">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge][MicrosoftEdgeDownload].</span></span>  

## <span data-ttu-id="023a9-114">Instalación de Playwright</span><span class="sxs-lookup"><span data-stu-id="023a9-114">Installing Playwright</span></span>  

<span data-ttu-id="023a9-115">Instala [Playwright][|::ref4::|Main] para probar tu sitio web o aplicación con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="023a9-115">Install [Playwright][|::ref4::|Main] to test your website or app with the following command.</span></span>  

```shell
npm i playwright
```  

## <span data-ttu-id="023a9-116">Iniciar Microsoft Edge con Playwright</span><span class="sxs-lookup"><span data-stu-id="023a9-116">Launch Microsoft Edge with Playwright</span></span>  

> [!NOTE]
> <span data-ttu-id="023a9-117">[Playwright][|::ref5::|Main] requiere Node.js versión 10,17 o superior.</span><span class="sxs-lookup"><span data-stu-id="023a9-117">[Playwright][|::ref5::|Main] requires Node.js version 10.17 or above.</span></span> <span data-ttu-id="023a9-118">Ejecute `node -v` desde la línea de comandos para asegurarse de que tiene una versión compatible de Node.js.</span><span class="sxs-lookup"><span data-stu-id="023a9-118">Run `node -v` from the command line to ensure you have a compatible version of Node.js.</span></span>  <span data-ttu-id="023a9-119">Los archivos binarios del explorador de cromo, Firefox y WebKit funcionan en Windows, macOS y Linux.</span><span class="sxs-lookup"><span data-stu-id="023a9-119">The browser binaries for Chromium, Firefox and WebKit work across Windows, macOS, and Linux.</span></span> <span data-ttu-id="023a9-120">Para obtener más información, vaya a [Playwright requisitos del sistema][PlaywrightSystemRequirements].</span><span class="sxs-lookup"><span data-stu-id="023a9-120">For more information, navigate to [Playwright System Requirements][PlaywrightSystemRequirements].</span></span>  

<span data-ttu-id="023a9-121">Playwright debería ser familiar para los usuarios de otros marcos de pruebas de explorador, como [Webdriver][WebDriverChromiumMain] o [puppeteer][PuppeteerMain].</span><span class="sxs-lookup"><span data-stu-id="023a9-121">Playwright should be familiar to users of other browser-testing frameworks like [WebDriver][WebDriverChromiumMain] or [Puppeteer][PuppeteerMain].</span></span>  <span data-ttu-id="023a9-122">Puede crear una instancia del explorador, abrir una página y, a continuación, manipularla con la [API de Playwright][PlaywrightAPIReference].</span><span class="sxs-lookup"><span data-stu-id="023a9-122">You create an instance of the browser, open a page, and then manipulate it with the [Playwright API][PlaywrightAPIReference].</span></span>  <span data-ttu-id="023a9-123">En el siguiente fragmento de código, Playwright lanza Microsoft Edge \ (cromo \), se desplaza a `https://www.microsoft.com/edge` y guarda una captura de pantalla como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="023a9-123">In the following code snippet, Playwright launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoft.com/edge`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="023a9-124">Copie el siguiente fragmento de código y guárdelo como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="023a9-124">Copy the following code snippet and save it as `example.js`.</span></span>  

```javascript
const { chromium } = require('playwright');

(async () => {
  const browser = await chromium.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoft.com/edge');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="023a9-125">Cambie `executablePath` a la instalación de Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="023a9-125">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="023a9-126">Por ejemplo, en macOS, la `executablePath` configuración de for Microsoft Edge debe establecerse en `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="023a9-126">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="023a9-127">Para encontrar el `executablePath` , navegue `edge://version` y copie la **ruta de acceso del archivo ejecutable** en esa página o instale el paquete [Edge-paths][npmEdgePaths] con el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="023a9-127">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with the following command.</span></span>  

```shell
npm i edge-paths
```  

<span data-ttu-id="023a9-128">El siguiente fragmento de código usa el paquete [Edge-paths][npmEdgePaths] para buscar mediante programación la ruta de acceso a la instalación de Microsoft Edge \ (cromo \) en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="023a9-128">The following code snippet uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

<span data-ttu-id="023a9-129">Por último, establezca `executablePath: EDGE_PATH` en `example.js` .</span><span class="sxs-lookup"><span data-stu-id="023a9-129">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="023a9-130">Haz clic en Guardar para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="023a9-130">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="023a9-131">Microsoft Edge \ (EdgeHTML \) no funciona con Playwright.</span><span class="sxs-lookup"><span data-stu-id="023a9-131">Microsoft Edge \(EdgeHTML\) does not work with Playwright.</span></span>  <span data-ttu-id="023a9-132">Para continuar siguiendo este ejemplo, debes instalar [Microsoft Edge \ (cromo \)][MicrosoftEdgeDownload] .</span><span class="sxs-lookup"><span data-stu-id="023a9-132">You must install [Microsoft Edge \(Chromium\)][MicrosoftEdgeDownload] to continue following this example.</span></span>  

<span data-ttu-id="023a9-133">Ahora se ejecuta `example.js` desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="023a9-133">Now run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

<span data-ttu-id="023a9-134">Playwright inicia Microsoft Edge, se desplaza a `https://www.microsoft.com/edge` y guarda una captura de pantalla de la página.</span><span class="sxs-lookup"><span data-stu-id="023a9-134">Playwright launches Microsoft Edge, navigates to `https://www.microsoft.com/edge`, and saves a screenshot of the page.</span></span>  <span data-ttu-id="023a9-135">Puede personalizar el tamaño de la página con [Page. setViewportSize ()][PlaywrightAPIPageSetViewport].</span><span class="sxs-lookup"><span data-stu-id="023a9-135">You may customize the page size with [page.setViewportSize()][PlaywrightAPIPageSetViewport].</span></span>  

:::image type="complex" source="../media/playwright-example.png" alt-text="El archivo de example.png producido por example.js" lightbox="../media/playwright-example.png":::
    <span data-ttu-id="023a9-137">El `example.png` archivo generado por</span><span class="sxs-lookup"><span data-stu-id="023a9-137">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

`example.js` <span data-ttu-id="023a9-138">es una simple demostración de los escenarios de automatización y pruebas habilitados por Playwright.</span><span class="sxs-lookup"><span data-stu-id="023a9-138">is just a simple demonstration of the automation and testing scenarios enabled by Playwright.</span></span>  <span data-ttu-id="023a9-139">Para realizar capturas de pantallas en varios exploradores Web, cambie el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="023a9-139">To take screenshots in multiple web browsers, change the following code.</span></span>  

*   <span data-ttu-id="023a9-140">Cromo</span><span class="sxs-lookup"><span data-stu-id="023a9-140">Chromium</span></span>  `await chromium.launch()`  
*   <span data-ttu-id="023a9-141">Firefox</span><span class="sxs-lookup"><span data-stu-id="023a9-141">Firefox</span></span>  `await firefox.launch()`  
*   <span data-ttu-id="023a9-142">WebKit</span><span class="sxs-lookup"><span data-stu-id="023a9-142">WebKit</span></span>  `await webkit.launch()`  

<span data-ttu-id="023a9-143">Para obtener más información sobre Playwright, vaya al [sitio web de Playwright][|::ref6::|Main].</span><span class="sxs-lookup"><span data-stu-id="023a9-143">For more information about Playwright, navigate to the [Playwright website][|::ref6::|Main].</span></span>  <span data-ttu-id="023a9-144">Consulta el  [repositorio de Playwright][PlaywrightRepo] en github.</span><span class="sxs-lookup"><span data-stu-id="023a9-144">Check out the  [Playwright repo][PlaywrightRepo] on GitHub.</span></span>  <span data-ttu-id="023a9-145">Para compartir sus comentarios sobre cómo automatizar y probar su sitio web o aplicación con Playwright, [envíe un problema][PlaywrightRepoNewIssue].</span><span class="sxs-lookup"><span data-stu-id="023a9-145">To share your feedback on automating and testing your website or app with Playwright, [file an issue][PlaywrightRepoNewIssue].</span></span>  

## <span data-ttu-id="023a9-146">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="023a9-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "Controlador WebDrive (cromo) | Microsoft docs"  
[PuppeteerMain]: ../puppeteer/index.md "Puppeteer | Microsoft docs"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: cómo mejorar la eficacia de la web mediante una colaboración de código abierto | Blog de experiencia de Microsoft"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Descargar Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Cromo | Proyectos de cromo"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "rutas de borde | NPM"  

[PlaywrightMain]: https://playwright.dev "Playwright"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Referencia de la API de Playwright"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "Page. setViewportSize (viewportSize) | Referencia de la API de Playwright"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Requisitos del sistema de Playwright"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Playwright | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Nuevo problema en el repositorio de Playwright | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin periféricos | Wikipedia"  

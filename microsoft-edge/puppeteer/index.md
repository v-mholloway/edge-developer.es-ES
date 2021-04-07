---
description: Usar Puppeteer para automatizar y probar en Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, desarrollador, herramientas, automatización, prueba
ms.openlocfilehash: 89a4dad3319f8e61f27487973509a8ee5ac23b6a
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480170"
---
# <a name="puppeteer-overview"></a><span data-ttu-id="24cb5-104">Información general sobre Puppeteer</span><span class="sxs-lookup"><span data-stu-id="24cb5-104">Puppeteer overview</span></span>  

<span data-ttu-id="24cb5-105">[Puppeteer][|::ref1::|Main] es una biblioteca [de nodos][NodejsMain] que proporciona una API de alto nivel para controlar Microsoft Edge \(Chromium\) mediante el [protocolo DevTools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="24cb5-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="24cb5-106">Puppeteer inicia exploradores [sin cabeza][WikiHeadlessBrowser] de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="24cb5-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="24cb5-107">Los exploradores sin cabeza no muestran una interfaz de usuario, por lo que en su lugar debes usar la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="24cb5-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="24cb5-108">También puede configurar Puppeteer para que ejecute también Microsoft Edge completo \(non-headless\).</span><span class="sxs-lookup"><span data-stu-id="24cb5-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="24cb5-109">De forma predeterminada, al instalar Puppeteer, el instalador descarga una versión reciente de [Chromium][ChromiumHome], el explorador de código abierto en el que también se basa [Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="24cb5-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="24cb5-110">Si tiene Microsoft Edge \(Chromium\) instalado, puede usar [puppeteer-core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="24cb5-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="24cb5-111">es una versión ligera de Puppeteer que inicia una instalación de explorador existente, como Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="24cb5-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="24cb5-112">Para descargar Microsoft Edge \(Chromium\), vaya a [Descargar canales insider de Microsoft Edge][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="24cb5-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <a name="installing-puppeteer-core"></a><span data-ttu-id="24cb5-113">Instalación de puppeteer-core</span><span class="sxs-lookup"><span data-stu-id="24cb5-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="24cb5-114">Puedes agregar a `puppeteer-core` tu sitio web o aplicación con uno de los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="24cb5-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a><span data-ttu-id="24cb5-115">Iniciar Microsoft Edge con puppeteer-core</span><span class="sxs-lookup"><span data-stu-id="24cb5-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="24cb5-116">se basa en node v8.9.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="24cb5-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="24cb5-117">En el ejemplo siguiente se usa lo que solo se `async` / `await` admite en node v7.6.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="24cb5-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="24cb5-118">Ejecute `node -v` desde la línea de comandos para asegurarse de que tiene una versión compatible de Node.js.</span><span class="sxs-lookup"><span data-stu-id="24cb5-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="24cb5-119">debe estar familiarizado con los usuarios de otros marcos de pruebas de explorador como [WebDriver][WebdriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="24cb5-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="24cb5-120">Cree una instancia del explorador, abra una página y, a continuación, manipule con la API de Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="24cb5-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="24cb5-121">En el siguiente ejemplo de código, `puppeteer-core` inicia Microsoft Edge \(Chromium\), navega a y guarda una captura `https://www.microsoftedgeinsider.com` de pantalla como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="24cb5-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="24cb5-122">Copie el siguiente fragmento de código y guárdelo como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="24cb5-122">Copy the following code snippet and save it as `example.js`.</span></span>  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="24cb5-123">Cambiar `executablePath` para apuntar a la instalación de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="24cb5-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="24cb5-124">Por ejemplo, en macOS, `executablePath` para Microsoft Edge Canary debe establecerse en `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="24cb5-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="24cb5-125">Para buscar el , vaya a y copie la ruta de acceso ejecutable en esa página o instale el paquete de rutas perimetrales `executablePath` con uno de los siguientes `edge://version` comandos. \*\*\*\* [][npmEdgePaths]</span><span class="sxs-lookup"><span data-stu-id="24cb5-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="24cb5-126">El ejemplo de código siguiente usa el paquete [de][npmEdgePaths] rutas de acceso perimetrales para buscar mediante programación la ruta de acceso a la instalación de Microsoft Edge \(Chromium\) en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="24cb5-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="24cb5-127">Por último, establezca `executablePath: EDGE_PATH` en `example.js` .</span><span class="sxs-lookup"><span data-stu-id="24cb5-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="24cb5-128">Haz clic en Guardar para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="24cb5-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="24cb5-129">Microsoft Edge \(EdgeHTML\) no funciona con `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="24cb5-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="24cb5-130">Debe instalar los [canales de Microsoft Edge Insider][MicrosoftedgeinsiderDownload] para seguir este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="24cb5-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="24cb5-131">Ahora, ejecute `example.js` desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="24cb5-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="24cb5-132">inicia Microsoft Edge, navega a `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla de la página web.</span><span class="sxs-lookup"><span data-stu-id="24cb5-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="24cb5-133">Personalice el tamaño de la captura de pantalla [con page.setViewport()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="24cb5-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="El example.png creado por example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="24cb5-135">El `example.png` archivo generado por</span><span class="sxs-lookup"><span data-stu-id="24cb5-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="24cb5-136">Este es solo un ejemplo sencillo de los escenarios de automatización y pruebas habilitados por Puppeteer y `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="24cb5-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="24cb5-137">Para obtener más información acerca de Puppeteer y cómo funciona, vaya a [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="24cb5-137">For more information about Puppeteer and how it works, navigate to [Puppeteer][|::ref2::|Main].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="24cb5-138">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="24cb5-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="24cb5-139">El equipo de desarrolladores de Microsoft Edge está deseando escuchar sus comentarios sobre el uso de Puppeteer `puppeteer-core` y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="24cb5-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="24cb5-140">Usa el **icono Enviar comentarios** en las Herramientas de desarrollo de Microsoft Edge o el @EdgeDevTools tweet para que el equipo de Microsoft Edge sepa lo que piensas. [][TwitterIntentTweetEdgedevtools]</span><span class="sxs-lookup"><span data-stu-id="24cb5-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en las Herramientas de desarrollo del borde de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="24cb5-142">El **icono Enviar comentarios** en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="24cb5-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][ArchiveMicrosoftEdgeLegacyDeveloperWebdriverIndex]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge:  Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Microsoft Docs"  

<!--  [ArchiveMicrosoftEdgeLegacyDeveloperWebdriverIndex]: /archive/microsoft-edge/legacy/developer/webdriver/index "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Chrome DevTools Protocol Viewer | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: mejorar la web a través de más colaboración de código | Blog de experiencia de Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Los proyectos de Chromium"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Rutas de acceso perimetrales | npm"  

[PuppeteerMain]: https://pptr.dev "Titiritero"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "titiritero vs. titiritero-core | Titiritero"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Titiritero"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools: publicar un mensaje de | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  

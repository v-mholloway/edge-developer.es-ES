---
description: Usar puppeteer para automatizar y probar en Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, desarrollador, herramientas, automatización, prueba
ms.openlocfilehash: 99d873a9b3988cb8a2827ecc9a69d574a196b037
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235934"
---
# <span data-ttu-id="ec180-104">Información general sobre Puppeteer</span><span class="sxs-lookup"><span data-stu-id="ec180-104">Puppeteer overview</span></span>  

<span data-ttu-id="ec180-105">[Puppeteer][|::ref1::|Main] es una biblioteca de [nodos][NodejsMain] que proporciona una API de alto nivel para controlar Microsoft Edge \ (cromo \) usando el [Protocolo DevTools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="ec180-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library that provides a high-level API to control Microsoft Edge \(Chromium\) using the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="ec180-106">Puppeteer inicia los [exploradores desatendidas][WikiHeadlessBrowser] de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ec180-106">Puppeteer launches [headless browsers][WikiHeadlessBrowser] by default.</span></span>  <span data-ttu-id="ec180-107">Los exploradores sin encabezado no muestran una interfaz de usuario, por lo que debe usar la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="ec180-107">Headless browsers do not display a UI, so instead you must use the command line.</span></span>  <span data-ttu-id="ec180-108">También puede configurar puppeteer para que ejecute también Microsoft Edge \ (no headed \) Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ec180-108">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge as well.</span></span>  

<span data-ttu-id="ec180-109">De forma predeterminada, al instalar puppeteer, el instalador descarga una versión reciente de [cromo][ChromiumHome], el explorador de código abierto en el que [también se ha creado Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="ec180-109">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="ec180-110">Si tienes instalado Microsoft Edge \ (cromo \), puedes usar [puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="ec180-110">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="ec180-111">es una versión ligera de puppeteer que inicia una instalación de explorador existente, como Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="ec180-111">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="ec180-112">Para descargar Microsoft Edge \ (cromo \), navegue para [descargar los canales de Insider de Microsoft Edge][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="ec180-112">To download Microsoft Edge \(Chromium\), navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>  

## <span data-ttu-id="ec180-113">Instalación de puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="ec180-113">Installing puppeteer-core</span></span>  

<span data-ttu-id="ec180-114">Puede agregar `puppeteer-core` a su sitio web o a la aplicación con uno de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="ec180-114">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="ec180-115">Iniciar Microsoft Edge con puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="ec180-115">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="ec180-116">se basa en el nodo v 8.9.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ec180-116">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="ec180-117">El ejemplo siguiente usa `async` / `await` que solo se admite en el nodo v 7.6.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ec180-117">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="ec180-118">Ejecute `node -v` desde la línea de comandos para asegurarse de que tiene una versión compatible de Node.js.</span><span class="sxs-lookup"><span data-stu-id="ec180-118">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="ec180-119">debe ser familiar para los usuarios de otras pruebas de explorador: marcos como [Webdriver][WebdriverChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="ec180-119">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebdriverChromiumMain].</span></span>  <span data-ttu-id="ec180-120">Puede crear una instancia del explorador, abrir una página y, a continuación, manipularla con la API de puppeteer.</span><span class="sxs-lookup"><span data-stu-id="ec180-120">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="ec180-121">En el siguiente ejemplo de código, se `puppeteer-core` inicia Microsoft Edge \ (cromo \), se desplaza a `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="ec180-121">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="ec180-122">Copie el siguiente fragmento de código y guárdelo como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="ec180-122">Copy the following code snippet and save it as `example.js`.</span></span>  

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

<span data-ttu-id="ec180-123">Cambie `executablePath` a la instalación de Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="ec180-123">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="ec180-124">Por ejemplo, en macOS, la `executablePath` configuración de for Microsoft Edge debe establecerse en `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="ec180-124">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="ec180-125">Para encontrar el `executablePath` , navegue `edge://version` y copie la **ruta de acceso del archivo ejecutable** en esa página o instale el paquete [Edge-paths][npmEdgePaths] con uno de los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="ec180-125">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="ec180-126">En el siguiente código de ejemplo se usa el paquete [Edge-paths][npmEdgePaths] para buscar mediante programación la ruta de acceso a la instalación de Microsoft Edge \ (cromo \) en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ec180-126">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="ec180-127">Por último, establezca `executablePath: EDGE_PATH` en `example.js` .</span><span class="sxs-lookup"><span data-stu-id="ec180-127">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="ec180-128">Haz clic en Guardar para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="ec180-128">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="ec180-129">Microsoft Edge \ (EdgeHTML \) no funciona con `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="ec180-129">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="ec180-130">Para continuar siguiendo este ejemplo, debe instalar los [canales de Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] .</span><span class="sxs-lookup"><span data-stu-id="ec180-130">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="ec180-131">Ahora, ejecute `example.js` desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="ec180-131">Now, run `example.js` from the command line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="ec180-132">inicia Microsoft Edge, navega a `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla de la Página Web.</span><span class="sxs-lookup"><span data-stu-id="ec180-132">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot of the webpage.</span></span>  <span data-ttu-id="ec180-133">Personalizar el tamaño de la captura de pantalla con [Page. setViewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="ec180-133">Customize the screenshot size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="El archivo de example.png producido por example.js" lightbox="./media/puppeteer-example.png":::
   <span data-ttu-id="ec180-135">El `example.png` archivo generado por</span><span class="sxs-lookup"><span data-stu-id="ec180-135">The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<span data-ttu-id="ec180-136">Este es solo un ejemplo sencillo de los escenarios de automatización y pruebas habilitados por puppeteer y `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="ec180-136">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="ec180-137">Para obtener más información sobre puppeteer y cómo funciona, consulte [puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="ec180-137">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="ec180-138">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ec180-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="ec180-139">El equipo de desarrollador de Microsoft Edge está ansioso por escuchar tus comentarios sobre el uso de puppeteer, `puppeteer-core` y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ec180-139">The Microsoft Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="ec180-140">Use el icono para **Enviar comentarios** de las [@EdgeDevTools][TwitterIntentTweetEdgedevtools] de Microsoft Edge DevTools o Tweet para permitir que el equipo de Microsoft Edge sepa cuál es su opinión.</span><span class="sxs-lookup"><span data-stu-id="ec180-140">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono enviar comentarios en el DevTools de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   <span data-ttu-id="ec180-142">El icono **Enviar comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ec180-142">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
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

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "Controlador WebDrive (cromo) | Microsoft docs"  
<!--  [WebdriverEdgehtmlMain]: ../edgehtml/webdriver/index.md "WebDriver (EdgeHTML) | Microsoft Docs"  -->  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visor de protocolo de cromo DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: cómo mejorar la eficacia de la web mediante una colaboración de código abierto | Blog de experiencia de Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[ChromiumHome]: https://www.chromium.org/Home "Cromo | Proyectos de cromo"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Rutas de borde | NPM"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer frente a puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setViewport (ventanilla) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools: publica un tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin periféricos | Wikipedia"  

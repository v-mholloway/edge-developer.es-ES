---
description: Usar puppeteer para automatizar y probar en Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, desarrollador, herramientas, automatización, prueba
ms.openlocfilehash: ccca46426a006651a417a22e54c8b528834b5f81
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844015"
---
# <span data-ttu-id="4e7bc-104">Puppeteer</span><span class="sxs-lookup"><span data-stu-id="4e7bc-104">Puppeteer</span></span>  

<span data-ttu-id="4e7bc-105">[Puppeteer][|::ref1::|Main] es una biblioteca de [nodos][NodejsMain] que proporciona una API de alto nivel para controlar Microsoft Edge \ (cromo \) sobre el [Protocolo DevTools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="4e7bc-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library which provides a high-level API to control Microsoft Edge \(Chromium\) over the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="4e7bc-106">Puppeteer se [ejecuta de][WikiHeadlessBrowser] forma predeterminada, lo que significa que no verás ninguna interfaz de usuario y, en su lugar, deberás usar la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-106">Puppeteer runs [headless][WikiHeadlessBrowser] by default, which means that you do not see a UI, and instead must use the command-line.</span></span>  <span data-ttu-id="4e7bc-107">También puede configurar puppeteer para que ejecute también \ Microsoft Edge \ (no headed \) Microsoft Edge o cromo.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-107">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge or Chromium as well.</span></span>  

<span data-ttu-id="4e7bc-108">De forma predeterminada, al instalar puppeteer, el instalador descarga una versión reciente de [cromo][ChromiumHome], el explorador de código abierto en el que [también se ha creado Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="4e7bc-108">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="4e7bc-109">Si tienes instalado Microsoft Edge \ (cromo \), puedes usar [puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="4e7bc-109">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="4e7bc-110">es una versión ligera de puppeteer que inicia una instalación de explorador existente, como Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="4e7bc-110">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="4e7bc-111">Para descargar Microsoft Edge \ (cromo \), consulte [descargar los canales de Insider de Microsoft Edge][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="4e7bc-111">To download Microsoft Edge \(Chromium\), see [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>

## <span data-ttu-id="4e7bc-112">Instalación de puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="4e7bc-112">Installing puppeteer-core</span></span>  

<span data-ttu-id="4e7bc-113">Puede agregar `puppeteer-core` a su sitio web o a la aplicación con uno de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="4e7bc-113">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="4e7bc-114">Iniciar Microsoft Edge con puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="4e7bc-114">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="4e7bc-115">se basa en el nodo v 8.9.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-115">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="4e7bc-116">El ejemplo siguiente usa `async` / `await` que solo se admite en el nodo v 7.6.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-116">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="4e7bc-117">Ejecute `node -v` desde la línea de comandos para asegurarse de que tiene una versión compatible de Node.js.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-117">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="4e7bc-118">debe ser familiar para los usuarios de otras pruebas de explorador: marcos como [Webdriver][WebDriverEdgehtmlMain].</span><span class="sxs-lookup"><span data-stu-id="4e7bc-118">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebDriverEdgehtmlMain].</span></span>  <span data-ttu-id="4e7bc-119">Puede crear una instancia del explorador, abrir una página y, a continuación, manipularla con la API de puppeteer.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-119">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="4e7bc-120">En el siguiente ejemplo de código, se `puppeteer-core` inicia Microsoft Edge \ (cromo \), se desplaza a `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla como `example.png` .</span><span class="sxs-lookup"><span data-stu-id="4e7bc-120">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="4e7bc-121">Copie el ejemplo de código siguiente y guárdelo como `example.js` .</span><span class="sxs-lookup"><span data-stu-id="4e7bc-121">Copy the code sample below and save it as `example.js`.</span></span>  

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

<span data-ttu-id="4e7bc-122">Cambie `executablePath` a la instalación de Microsoft Edge \ (cromo \).</span><span class="sxs-lookup"><span data-stu-id="4e7bc-122">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="4e7bc-123">Por ejemplo, en macOS, la `executablePath` configuración de for Microsoft Edge debe establecerse en `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="4e7bc-123">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="4e7bc-124">Para encontrar el `executablePath` , navegue `edge://version` y copie la **ruta de acceso del archivo ejecutable** en esa página o instale el paquete [Edge-paths][npmEdgePaths] con uno de los siguientes comandos.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-124">To find the `executablePath`, navigate to `edge://version` and copy the **Executable path** on that page or install the [edge-paths][npmEdgePaths] package with one of the following commands.</span></span>  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
<span data-ttu-id="4e7bc-125">En el siguiente código de ejemplo se usa el paquete [Edge-paths][npmEdgePaths] para buscar mediante programación la ruta de acceso a la instalación de Microsoft Edge \ (cromo \) en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-125">The code sample below uses the [edge-paths][npmEdgePaths] package to programmatically find the path to your installation of Microsoft Edge \(Chromium\) on your OS.</span></span>

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

<span data-ttu-id="4e7bc-126">Por último, establezca `executablePath: EDGE_PATH` en `example.js` .</span><span class="sxs-lookup"><span data-stu-id="4e7bc-126">Finally, set `executablePath: EDGE_PATH` in `example.js`.</span></span>  <span data-ttu-id="4e7bc-127">Haz clic en Guardar para guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-127">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="4e7bc-128">Microsoft Edge \ (EdgeHTML \) no funciona con `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="4e7bc-128">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="4e7bc-129">Para continuar siguiendo este ejemplo, debe instalar los [canales de Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] .</span><span class="sxs-lookup"><span data-stu-id="4e7bc-129">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="4e7bc-130">Ahora se ejecuta `example.js` desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-130">Now run `example.js` from the command-line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="4e7bc-131">inicia Microsoft Edge, navega hasta `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla de 800px x 600px de la página.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-131">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com` and saves an 800px x 600px screenshot of the page.</span></span>  <span data-ttu-id="4e7bc-132">Puede personalizar el tamaño de la página con [Page. setViewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="4e7bc-132">You are able to customize the page size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="El archivo de example.png producido por example.js":::
   <span data-ttu-id="4e7bc-134">Ilustración 1: el `example.png` archivo creado por</span><span class="sxs-lookup"><span data-stu-id="4e7bc-134">Figure 1:  The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

<span data-ttu-id="4e7bc-135">Este es solo un ejemplo sencillo de los escenarios de automatización y pruebas habilitados por puppeteer y `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="4e7bc-135">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="4e7bc-136">Para obtener más información sobre puppeteer y cómo funciona, consulte [puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="4e7bc-136">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="4e7bc-137">Enviar comentarios</span><span class="sxs-lookup"><span data-stu-id="4e7bc-137">Send Feedback</span></span>  

<span data-ttu-id="4e7bc-138">El equipo de desarrollo de Edge está ansioso por escuchar tus comentarios sobre el uso de puppeteer, `puppeteer-core` y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-138">The Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="4e7bc-139">Use el icono para **Enviar comentarios** de las [@EdgeDevTools][TwitterIntentTweetEdgedevtools] de Microsoft Edge DevTools o Tweet para permitir que el equipo de Microsoft Edge sepa cuál es su opinión.</span><span class="sxs-lookup"><span data-stu-id="4e7bc-139">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="El icono de comentarios en el DevTools de Microsoft Edge":::
   <span data-ttu-id="4e7bc-141">Ilustración 2: el icono de **comentarios** en el Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4e7bc-141">Figure 2:  The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
> ##### Figure 2  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The Feedback icon in the Microsoft Edge DevTools](./devtools-guide-chromium/media/devtools-feedback.png)  
-->  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge: Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- image links -->  

<!-- links -->  

[WebdriverChromiumMain]: ./webdriver-chromium.md "Controlador WebDrive (cromo)"  
[WebdriverEdgehtmlMain]: ./webdriver.md "Controlador WebDrive (EdgeHTML)"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visor de protocolo de cromo DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: cómo mejorar la eficacia de la web mediante una mayor colaboración de código abierto | Blog de experiencia de Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Cromo | Proyectos de cromo"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "NPM | Trazados de borde"

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer frente a puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setViewport (ventanilla) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools: publica un tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin periféricos | Wikipedia"  

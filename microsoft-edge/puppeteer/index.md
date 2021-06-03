---
description: Use Puppeteer para automatizar y probar en Microsoft Edge
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
# <a name="puppeteer-overview"></a>Información general sobre Puppeteer  

[Puppeteer][|::ref1::|Main] es una biblioteca [de nodos][NodejsMain] que proporciona una API de alto nivel para controlar Microsoft Edge \(Chromium\) mediante el [protocolo DevTools][GithubChromedevtoolsProtocol].  Puppeteer inicia exploradores [sin cabeza][WikiHeadlessBrowser] de forma predeterminada.  Los exploradores sin cabeza no muestran una interfaz de usuario, por lo que en su lugar debes usar la línea de comandos.  También puede configurar El titiritero para que ejecute el archivo completo \(non-headless\) Microsoft Edge.  

De forma predeterminada, al instalar Puppeteer, el instalador descarga una versión reciente de [Chromium][ChromiumHome], el explorador de código abierto en el que Microsoft Edge también se [basa][MicrosoftBlogsWindowsExperience20181206].  Si ha instalado Microsoft Edge \(Chromium\), puede usar [puppeteer-core][PuppeteerApivscore].  `puppeteer-core` es una versión ligera de Puppeteer que inicia una instalación de explorador existente, como Microsoft Edge \(Chromium\).  Para descargar Microsoft Edge \(Chromium\), vaya a [Descargar Microsoft Edge Canales insider][MicrosoftedgeinsiderDownload].  

## <a name="installing-puppeteer-core"></a>Instalación de puppeteer-core  

Puedes agregar a `puppeteer-core` tu sitio web o aplicación con uno de los siguientes comandos.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <a name="launch-microsoft-edge-with-puppeteer-core"></a>Iniciar Microsoft Edge con puppeteer-core  

> [!NOTE]
> `puppeteer-core` se basa en node v8.9.0 o posterior.  En el ejemplo siguiente se usa lo que solo se `async` / `await` admite en node v7.6.0 o posterior.  Ejecute `node -v` desde la línea de comandos para asegurarse de que tiene una versión compatible de Node.js.  

`puppeteer-core` debe estar familiarizado con los usuarios de otros marcos de pruebas de explorador como [WebDriver][WebdriverChromiumMain].  Cree una instancia del explorador, abra una página y, a continuación, manipule con la API de Puppeteer.  En el siguiente ejemplo de código, `puppeteer-core` inicia Microsoft Edge \(Chromium\), navega a y guarda una captura `https://www.microsoftedgeinsider.com` de pantalla como `example.png` .  

Copie el siguiente fragmento de código y guárdelo como `example.js` .  

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

Cambie `executablePath` para que apunte a la instalación de Microsoft Edge \(Chromium\).  Por ejemplo, en macOS, el valor `executablePath` Microsoft Edge Canary debe establecerse en `/Applications/Microsoft\ Edge\ Canary.app/` .  Para buscar el , vaya a y copie la ruta de acceso ejecutable en esa página o instale el paquete de rutas perimetrales `executablePath` con uno de los siguientes `edge://version` comandos. **** [][npmEdgePaths]  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
El ejemplo de código siguiente usa el paquete [de][npmEdgePaths] rutas de acceso perimetrales para buscar mediante programación la ruta de acceso a la instalación de Microsoft Edge \(Chromium\) en el sistema operativo.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Por último, establezca `executablePath: EDGE_PATH` en `example.js` .  Haz clic en Guardar para guardar los cambios.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) no funciona con `puppeteer-core` .  Debe instalar los [canales Microsoft Edge Insider para][MicrosoftedgeinsiderDownload] seguir este ejemplo.  

Ahora, ejecute `example.js` desde la línea de comandos.  

```shell
node example.js
```  

`puppeteer-core` inicia Microsoft Edge, navega a y guarda una captura `https://www.microsoftedgeinsider.com` de pantalla de la página web.  Personalice el tamaño de la captura de pantalla [con page.setViewport()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="El example.png creado por example.js" lightbox="./media/puppeteer-example.png":::
   El `example.png` archivo generado por `example.js`  
:::image-end:::  

Este es solo un ejemplo sencillo de los escenarios de automatización y pruebas habilitados por Puppeteer y `puppeteer-core` .  Para obtener más información acerca de Puppeteer y cómo funciona, vaya a [Puppeteer][|::ref2::|Main].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

El Microsoft Edge desarrollador está deseando escuchar sus comentarios acerca del uso de Puppeteer `puppeteer-core` y Microsoft Edge.  Usa el **icono Enviar comentarios** en el Microsoft Edge DevTools o el @EdgeDevTools tweet para que el equipo Microsoft Edge sepa lo que piensas. [][TwitterIntentTweetEdgedevtools]  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en las Herramientas de desarrollo del borde de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   El **icono Enviar comentarios** en el Microsoft Edge DevTools  
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

[ChromiumHome]: https://www.chromium.org/Home "Chromium | The Chromium Projects"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "Rutas de acceso perimetrales | npm"  

[PuppeteerMain]: https://pptr.dev "Titiritero"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "titiritero vs. titiritero-core | Titiritero"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page.setViewport(viewport) | Titiritero"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools: publicar un mensaje de | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  

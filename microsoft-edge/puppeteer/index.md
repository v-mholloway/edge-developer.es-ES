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
# Información general sobre Puppeteer  

[Puppeteer][|::ref1::|Main] es una biblioteca de [nodos][NodejsMain] que proporciona una API de alto nivel para controlar Microsoft Edge \ (cromo \) usando el [Protocolo DevTools][GithubChromedevtoolsProtocol].  Puppeteer inicia los [exploradores desatendidas][WikiHeadlessBrowser] de forma predeterminada.  Los exploradores sin encabezado no muestran una interfaz de usuario, por lo que debe usar la línea de comandos.  También puede configurar puppeteer para que ejecute también Microsoft Edge \ (no headed \) Microsoft Edge.  

De forma predeterminada, al instalar puppeteer, el instalador descarga una versión reciente de [cromo][ChromiumHome], el explorador de código abierto en el que [también se ha creado Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].  Si tienes instalado Microsoft Edge \ (cromo \), puedes usar [puppeteer-Core][PuppeteerApivscore].  `puppeteer-core` es una versión ligera de puppeteer que inicia una instalación de explorador existente, como Microsoft Edge \ (cromo \).  Para descargar Microsoft Edge \ (cromo \), navegue para [descargar los canales de Insider de Microsoft Edge][MicrosoftedgeinsiderDownload].  

## Instalación de puppeteer-Core  

Puede agregar `puppeteer-core` a su sitio web o a la aplicación con uno de los siguientes comandos:  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Iniciar Microsoft Edge con puppeteer-Core  

> [!NOTE]
> `puppeteer-core` se basa en el nodo v 8.9.0 o posterior.  El ejemplo siguiente usa `async` / `await` que solo se admite en el nodo v 7.6.0 o posterior.  Ejecute `node -v` desde la línea de comandos para asegurarse de que tiene una versión compatible de Node.js.  

`puppeteer-core` debe ser familiar para los usuarios de otras pruebas de explorador: marcos como [Webdriver][WebdriverChromiumMain].  Puede crear una instancia del explorador, abrir una página y, a continuación, manipularla con la API de puppeteer.  En el siguiente ejemplo de código, se `puppeteer-core` inicia Microsoft Edge \ (cromo \), se desplaza a `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla como `example.png` .  

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

Cambie `executablePath` a la instalación de Microsoft Edge \ (cromo \).  Por ejemplo, en macOS, la `executablePath` configuración de for Microsoft Edge debe establecerse en `/Applications/Microsoft\ Edge\ Canary.app/` .  Para encontrar el `executablePath` , navegue `edge://version` y copie la **ruta de acceso del archivo ejecutable** en esa página o instale el paquete [Edge-paths][npmEdgePaths] con uno de los siguientes comandos.  

```shell
npm i edge-paths
```  

```shell
yarn add edge-paths
```  
 
En el siguiente código de ejemplo se usa el paquete [Edge-paths][npmEdgePaths] para buscar mediante programación la ruta de acceso a la instalación de Microsoft Edge \ (cromo \) en el sistema operativo.

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```

Por último, establezca `executablePath: EDGE_PATH` en `example.js` .  Haz clic en Guardar para guardar los cambios.  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) no funciona con `puppeteer-core` .  Para continuar siguiendo este ejemplo, debe instalar los [canales de Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] .  

Ahora, ejecute `example.js` desde la línea de comandos.  

```shell
node example.js
```  

`puppeteer-core` inicia Microsoft Edge, navega a `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla de la Página Web.  Personalizar el tamaño de la captura de pantalla con [Page. setViewport ()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="El archivo de example.png producido por example.js" lightbox="./media/puppeteer-example.png":::
   El `example.png` archivo generado por `example.js`  
:::image-end:::  

Este es solo un ejemplo sencillo de los escenarios de automatización y pruebas habilitados por puppeteer y `puppeteer-core` .  Para obtener más información sobre puppeteer y cómo funciona, consulte [puppeteer][|::ref2::|Main].  

## Contactar al equipo de Microsoft Edge DevTools  

El equipo de desarrollador de Microsoft Edge está ansioso por escuchar tus comentarios sobre el uso de puppeteer, `puppeteer-core` y Microsoft Edge.  Use el icono para **Enviar comentarios** de las [@EdgeDevTools][TwitterIntentTweetEdgedevtools] de Microsoft Edge DevTools o Tweet para permitir que el equipo de Microsoft Edge sepa cuál es su opinión.  

:::image type="complex" source="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png" alt-text="El icono enviar comentarios en el DevTools de Microsoft Edge" lightbox="../devtools-guide-chromium/media/bing-devtools-send-feedback.msft.png":::
   El icono **Enviar comentarios** en el DevTools de Microsoft Edge  
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

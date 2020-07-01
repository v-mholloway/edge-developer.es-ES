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
# Puppeteer  

[Puppeteer][|::ref1::|Main] es una biblioteca de [nodos][NodejsMain] que proporciona una API de alto nivel para controlar Microsoft Edge \ (cromo \) sobre el [Protocolo DevTools][GithubChromedevtoolsProtocol].  Puppeteer se [ejecuta de][WikiHeadlessBrowser] forma predeterminada, lo que significa que no verás ninguna interfaz de usuario y, en su lugar, deberás usar la línea de comandos.  También puede configurar puppeteer para que ejecute también \ Microsoft Edge \ (no headed \) Microsoft Edge o cromo.  

De forma predeterminada, al instalar puppeteer, el instalador descarga una versión reciente de [cromo][ChromiumHome], el explorador de código abierto en el que [también se ha creado Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].  Si tienes instalado Microsoft Edge \ (cromo \), puedes usar [puppeteer-Core][PuppeteerApivscore].  `puppeteer-core` es una versión ligera de puppeteer que inicia una instalación de explorador existente, como Microsoft Edge \ (cromo \).  Para descargar Microsoft Edge \ (cromo \), consulte [descargar los canales de Insider de Microsoft Edge][MicrosoftedgeinsiderDownload].

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

`puppeteer-core` debe ser familiar para los usuarios de otras pruebas de explorador: marcos como [Webdriver][WebDriverEdgehtmlMain].  Puede crear una instancia del explorador, abrir una página y, a continuación, manipularla con la API de puppeteer.  En el siguiente ejemplo de código, se `puppeteer-core` inicia Microsoft Edge \ (cromo \), se desplaza a `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla como `example.png` .  

Copie el ejemplo de código siguiente y guárdelo como `example.js` .  

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

Ahora se ejecuta `example.js` desde la línea de comandos.  

```shell
node example.js
```  

`puppeteer-core` inicia Microsoft Edge, navega hasta `https://www.microsoftedgeinsider.com` y guarda una captura de pantalla de 800px x 600px de la página.  Puede personalizar el tamaño de la página con [Page. setViewport ()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="El archivo de example.png producido por example.js":::
   Ilustración 1: el `example.png` archivo creado por `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

Este es solo un ejemplo sencillo de los escenarios de automatización y pruebas habilitados por puppeteer y `puppeteer-core` .  Para obtener más información sobre puppeteer y cómo funciona, consulte [puppeteer][|::ref2::|Main].  

## Enviar comentarios  

El equipo de desarrollo de Edge está ansioso por escuchar tus comentarios sobre el uso de puppeteer, `puppeteer-core` y Microsoft Edge.  Use el icono para **Enviar comentarios** de las [@EdgeDevTools][TwitterIntentTweetEdgedevtools] de Microsoft Edge DevTools o Tweet para permitir que el equipo de Microsoft Edge sepa cuál es su opinión.  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="El icono de comentarios en el DevTools de Microsoft Edge":::
   Ilustración 2: el icono de **comentarios** en el Microsoft Edge DevTools  
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

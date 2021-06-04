---
description: Use Playwright para automatizar y probar en Microsoft Edge
title: Playwright
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/24/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, desarrollador, herramientas, automatización, prueba, playwright, node, javascript, npm
ms.openlocfilehash: 5ce51864177731dd1bafb845466abb00cce1e0aa
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231086"
---
# Playwright  

[Playwright][|::ref1::|Main] es una biblioteca [Node.js][NodejsMain] para automatizar [Chromium,][ChromiumHome] [Firefox][FirefoxMain]y [WebKit][|::ref2::|Main] con una única API.  Playwright está diseñado para habilitar la automatización web entre exploradores que es siempre verde, capaz, confiable y rápida.  Dado [Microsoft Edge se basa en la][MicrosoftBlogsWindowsExperience20181206]plataforma web de código Chromium de código abierto, Playwright también es capaz de automatizar Microsoft Edge.  

Playwright inicia exploradores [sin cabeza][WikiHeadlessBrowser] de forma predeterminada.  Los exploradores sin cabeza no muestran una interfaz de usuario, por lo que en su lugar debes usar la línea de comandos.  También puede configurar Playwright para que ejecute el archivo \(non-headless\) Microsoft Edge.  

De forma predeterminada, al instalar Playwright, el instalador descarga [Chromium][ChromiumHome], [Firefox][FirefoxMain]y [WebKit][|::ref3::|Main].  Si también tienes Microsoft Edge \(Chromium\), Playwright solo necesita un cambio de código de una línea para probar tu sitio web o aplicación en Microsoft Edge.  Para descargar Microsoft Edge \(Chromium\), vaya a [Descargar Microsoft Edge][MicrosoftEdgeDownload].  

##  <a name="installing-playwright--"></a>Instalación de Playwright  

Instala [Playwright para][|::ref4::|Main] probar tu sitio web o aplicación con el siguiente comando.  

```shell
npm i playwright
```  

##  <a name="launch-microsoft-edge-with-playwright--"></a>Iniciar Microsoft Edge con Playwright  

> [!NOTE]
> [Playwright][|::ref5::|Main] requiere Node.js versión 10.17 o posterior. Ejecute `node -v` desde la línea de comandos para asegurarse de que tiene una versión compatible de Node.js.  Los archivos binarios del explorador para Chromium, Firefox y WebKit funcionan en Windows, macOS y Linux. Para obtener más información, vaya [a Requisitos del sistema playwright][PlaywrightSystemRequirements].  

Playwright debe estar familiarizado con los usuarios de otros marcos de pruebas de explorador como [WebDriver][WebDriverChromiumMain] o [Puppeteer][PuppeteerMain].  Cree una instancia del explorador, abra una página y, a continuación, manipule con la [API de Playwright][PlaywrightAPIReference].  En el siguiente fragmento de código, Playwright inicia Microsoft Edge \(Chromium\), navega a y guarda una captura `https://www.microsoft.com/edge` de pantalla como `example.png` .  

Copie el siguiente fragmento de código y guárdelo como `example.js` .  

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

Cambie `executablePath` para que apunte a la instalación de Microsoft Edge \(Chromium\).  Por ejemplo, en macOS, el valor `executablePath` Microsoft Edge Canary debe establecerse en `/Applications/Microsoft\ Edge\ Canary.app/` .  Para buscar el , vaya a y copie la ruta de acceso ejecutable en esa página o instale el paquete de rutas perimetrales `executablePath` `edge://version` con el siguiente comando. **** [][npmEdgePaths]  

```shell
npm i edge-paths
```  

El siguiente fragmento de código usa el paquete [de][npmEdgePaths] rutas perimetrales para buscar mediante programación la ruta de acceso a la instalación de Microsoft Edge \(Chromium\) en el sistema operativo.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Por último, establezca `executablePath: EDGE_PATH` en `example.js` .  Haz clic en Guardar para guardar los cambios.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML\) no funciona con Playwright.  Debe instalar Microsoft Edge [\(Chromium\) para][MicrosoftEdgeDownload] seguir este ejemplo.  

Ahora ejecute `example.js` desde la línea de comandos.  

```shell
node example.js
```  

Playwright inicia Microsoft Edge, navega a `https://www.microsoft.com/edge` y guarda una captura de pantalla de la página.  Puede personalizar el tamaño de página con [page.setViewportSize()][PlaywrightAPIPageSetViewport].  

:::image type="complex" source="../media/playwright-example.png" alt-text="El example.png creado por example.js" lightbox="../media/playwright-example.png":::
    El `example.png` archivo generado por `example.js`  
:::image-end:::  

`example.js` es solo una demostración sencilla de los escenarios de automatización y pruebas habilitados por Playwright.  Para realizar capturas de pantalla en varios exploradores web, cambie el código siguiente.  

*   Chromium  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Para obtener más información acerca de Playwright, vaya al sitio [web de Playwright][|::ref6::|Main].  Echa un vistazo [al repositorio de Playwright][PlaywrightRepo] en GitHub.  Para compartir sus comentarios sobre cómo automatizar y probar su sitio web o aplicación con Playwright, [presente un problema][PlaywrightRepoNewIssue].  

##  <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../devtools-guide-chromium/includes/contact-devtools-team-note.md)]  

<!-- links -->  

[WebdriverChromiumMain]: ../webdriver-chromium/index.md "WebDriver (Chromium) | Microsoft Docs"  
[PuppeteerMain]: ../puppeteer/index.md "Titiritero | Microsoft Docs"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: mejorar la web a través de más colaboración de código | Blog de experiencia de Microsoft"  

[MicrosoftEdgeDownload]: https://microsoft.com/edge "Descargar Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | The Chromium Projects"  

[FirefoxMain]: https://www.mozilla.org/firefox "Mozilla Firefox"  

[NodejsMain]: https://nodejs.org "Node.js"  

[npmEdgePaths]: https://www.npmjs.com/package/edge-paths "rutas de acceso | npm"  

[PlaywrightMain]: https://playwright.dev "Playwright"  
[PlaywrightAPIReference]: https://playwright.dev#?path=docs/api.md "Referencia de LA API de Playwright"  
[PlaywrightAPIPageSetViewport]: https://playwright.dev#?path=docs%2Fapi.md&q=pagesetviewportsizeviewportsize "page.setViewportSize(viewportSize) | Referencia de LA API de Playwright"    
[PlaywrightSystemRequirements]: https://playwright.dev#?path=docs/intro.md&q=system-requirements "Requisitos del sistema playwright"  

[PlaywrightRepo]: https://github.com/microsoft/playwright "Playwright | GitHub"  
[PlaywrightRepoNewIssue]: https://github.com/microsoft/playwright/issues/new/choose "Nuevo problema en playwright repo | GitHub"  

[WebKitMain]: https://webkit.org "WebKit"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Explorador sin cabeza | Wikipedia"  

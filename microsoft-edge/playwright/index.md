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
# Playwright  

[Playwright][|::ref1::|Main] es una biblioteca de [Node.js][NodejsMain] para automatizar [cromo][ChromiumHome], [Firefox][FirefoxMain]y [WebKit][|::ref2::|Main] con una sola API.  Playwright se ha creado para permitir la automatización web entre exploradores, que es siempre verde, compatible, confiable y rápida.  Como [Microsoft Edge está integrado en la plataforma web de cromo de código abierto][MicrosoftBlogsWindowsExperience20181206], Playwright también puede automatizar Microsoft Edge.  

Playwright inicia los [exploradores desatendidas][WikiHeadlessBrowser] de forma predeterminada.  Los exploradores sin encabezado no muestran una interfaz de usuario, por lo que debe usar la línea de comandos.  También puede configurar Playwright para que ejecute también Microsoft Edge \(no headed \) Microsoft Edge.  

De forma predeterminada, al instalar Playwright, el instalador descarga [cromo][ChromiumHome], [Firefox][FirefoxMain]y [WebKit][|::ref3::|Main].  Si tienes Microsoft Edge \(cromo \) instalado también, Playwright solo necesita un cambio de código de una línea para probar tu sitio web o aplicación en Microsoft Edge.  Para descargar Microsoft Edge \(cromo \), navegue hasta [Descargar Microsoft Edge][MicrosoftEdgeDownload].  

## Instalación de Playwright  

Instala [Playwright][|::ref4::|Main] para probar tu sitio web o aplicación con el siguiente comando.  

```shell
npm i playwright
```  

## Iniciar Microsoft Edge con Playwright  

> [!NOTE]
> [Playwright][|::ref5::|Main] requiere Node.js versión 10,17 o superior. Ejecute `node -v` desde la línea de comandos para asegurarse de que tiene una versión compatible de Node.js.  Los archivos binarios del explorador de cromo, Firefox y WebKit funcionan en Windows, macOS y Linux. Para obtener más información, vaya a [Playwright requisitos del sistema][PlaywrightSystemRequirements].  

Playwright debería ser familiar para los usuarios de otros marcos de pruebas de explorador, como [Webdriver][WebDriverChromiumMain] o [puppeteer][PuppeteerMain].  Puede crear una instancia del explorador, abrir una página y, a continuación, manipularla con la [API de Playwright][PlaywrightAPIReference].  En el siguiente fragmento de código, Playwright lanza Microsoft Edge \(cromo \), se desplaza a `https://www.microsoft.com/edge` y guarda una captura de pantalla como `example.png` .  

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

Cambie `executablePath` a la instalación de Microsoft Edge \(cromo \).  Por ejemplo, en macOS, la `executablePath` configuración de for Microsoft Edge debe establecerse en `/Applications/Microsoft\ Edge\ Canary.app/` .  Para encontrar el `executablePath` , navegue `edge://version` y copie la **ruta de acceso del archivo ejecutable** en esa página o instale el paquete [Edge-paths][npmEdgePaths] con el siguiente comando.  

```shell
npm i edge-paths
```  

El siguiente fragmento de código usa el paquete [Edge-paths][npmEdgePaths] para buscar mediante programación la ruta de acceso a la instalación de Microsoft Edge \(cromo \) en el sistema operativo.  

```javascript
const edgePaths = require("edge-paths");

const EDGE_PATH = edgePaths.getEdgePath();
```  

Por último, establezca `executablePath: EDGE_PATH` en `example.js` .  Haz clic en Guardar para guardar los cambios.  

> [!NOTE]
> Microsoft Edge \(EdgeHTML \) no funciona con Playwright.  Para continuar siguiendo este ejemplo, debes instalar [Microsoft Edge \(cromo \)][MicrosoftEdgeDownload] .  

Ahora se ejecuta `example.js` desde la línea de comandos.  

```shell
node example.js
```  

Playwright inicia Microsoft Edge, se desplaza a `https://www.microsoft.com/edge` y guarda una captura de pantalla de la página.  Puede personalizar el tamaño de la página con [Page. setViewportSize ()][PlaywrightAPIPageSetViewport].  

:::image type="complex" source="../media/playwright-example.png" alt-text="El archivo de example.png producido por example.js" lightbox="../media/playwright-example.png":::
    El `example.png` archivo generado por `example.js`  
:::image-end:::  

`example.js` es una simple demostración de los escenarios de automatización y pruebas habilitados por Playwright.  Para realizar capturas de pantallas en varios exploradores Web, cambie el siguiente código.  

*   Cromo  `await chromium.launch()`  
*   Firefox  `await firefox.launch()`  
*   WebKit  `await webkit.launch()`  

Para obtener más información sobre Playwright, vaya al [sitio web de Playwright][|::ref6::|Main].  Consulta el  [repositorio de Playwright][PlaywrightRepo] en github.  Para compartir sus comentarios sobre cómo automatizar y probar su sitio web o aplicación con Playwright, [envíe un problema][PlaywrightRepoNewIssue].  

## Contactar al equipo de Microsoft Edge DevTools  

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

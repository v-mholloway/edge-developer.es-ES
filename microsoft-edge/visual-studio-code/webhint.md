---
description: Cómo usar webhint en Visual Studio Code
title: extensión webhint Visual Studio Code webhint
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, vs code, visual studio code, webhint
ms.openlocfilehash: 3dfd900bf818d02dbc8123c00e7928e56d9b6ade
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399277"
---
# <a name="webhint-vs-code-extension"></a>Webhint Vs Extensión de código  

Use [webhint][WebhintMain], una herramienta de linting personalizable, para mejorar la accesibilidad, el rendimiento, la compatibilidad entre exploradores, PWA compatibilidad y la seguridad del sitio.  Comprueba el código en busca de procedimientos recomendados y errores comunes. Este proyecto de código abierto, desarrollado inicialmente por el Microsoft Edge, ahora forma parte de [OpenJS Foundation][OpenjsFoundation].  El Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de pantalla de webhint Visual Studio Code extensión":::
   Captura de pantalla de webhint Visual Studio Code extensión  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

Identifique y corrija problemas en html, CSS, JavaScript, TypeScript y mucho más agregando la extensión [webhint para Visual Studio Code][VisualstudioMarketplaceWebhint].  Las sugerencias aparecen como subrayados en línea y se resumen en el **panel** Problemas.  

## <a name="configuration"></a>Configuración  

Esta extensión usa un archivo [json][GithubWebhintioIndexjson] de configuración predeterminado que activa sugerencias y analizadores para HTML, CSS, sistemas de plantillas \(JSX/TSX, Angular, etc.),JavaScript/TypeScript, etc.  

```json
{
    "connector": "local",
    "extends": [
        "accessibility",
        "progressive-web-apps"
    ],
    "formatters": [
        "html",
        "summary"
    ],
    "hints": [
        "apple-touch-icons",
        "button-type",
        "compat-api/css",
        "compat-api/html",
        "create-element-svg",
        "css-prefix-order",
        "disown-opener",
        "highest-available-document-mode",
        "manifest-exists",
        "meta-charset-utf-8",
        "meta-viewport",
        "no-bom",
        "no-protocol-relative-urls",
        "scoped-svg-styles",
        "sri",
        "typescript-config/consistent-casing",
        "typescript-config/import-helpers",
        "typescript-config/is-valid",
        "typescript-config/no-comments",
        "typescript-config/strict",
        "typescript-config/target"
    ],
    "hintsTimeout": 10000,
    "parsers": [
        "babel-config",
        "css",
        "html",
        "javascript",
        "jsx",
        "less",
        "sass",
        "typescript",
        "typescript-config",
        "webpack-config"
    ]
}
```  

Si desea tener más control sobre las sugerencias y analizadores que se activan, cree un archivo local `.hintrc` para configurar webhint.  Para obtener ayuda con la salida de sugerencias específicas, vaya a la guía del usuario [de webhint][WebhintDocsUserguideConfiguringSummary].  

## <a name="getting-in-touch-with-the-webhint-team"></a>Getting in touch with the webhint team  

Envíe sus comentarios mediante [la presentación de un problema][GithubWebhintioIssuesNew] en el repositorio GitHub [web.][GithubWebhintio]  

Para contribuir a la extensión, vaya a [webhint Visual Studio Code guía de contribución de extensión][GithubWebhintioExtensionVscodeContributing].  

## <a name="see-also"></a>Consulta también  

*   [Accesibilidad][AccessibilityIndex]  
*   [Visual Studio Code][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint Visual Studio Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Accesibilidad | Microsoft Docs"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio Code | Microsoft Docs"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Contribuir: webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index.js- webhintio/hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Nuevos problemas: webhintio/hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configuración de webhint | Documentación de webhint"  
[WebhintMain]:  https://webhint.io "webhint"  

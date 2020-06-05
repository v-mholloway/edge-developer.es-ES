---
description: Cómo usar webhint en código de Visual Studio
title: extensión de código webhint de VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, vs Code, código de Visual Studio, webhint
ms.openlocfilehash: ec218fab8cbfb8181a0416c8e0eadc0e00412529
ms.sourcegitcommit: c1b5fdd48d39d874a76c9b8f68309eb1b507fd0b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2020
ms.locfileid: "10695862"
---
# Extensión de código webhint de vs  

Use [webhint][WebhintMain], una herramienta de desplegable personalizable, para mejorar la accesibilidad, el rendimiento, la compatibilidad entre exploradores, la compatibilidad de PWA y la seguridad de su sitio.  Comprueba los procedimientos recomendados y los errores comunes de tu código. Este proyecto de código abierto, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de la [OpenJS Foundation][OpenjsFoundation].  El equipo de Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de pantalla de extensión de código webhint VS":::
   Captura de pantalla de extensión de código webhint VS  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

Identifique y solucione problemas en HTML, CSS, JavaScript, TypeScript y más agregando la [extensión webhint para vs Code][VisualstudioMarketplaceWebhint].  Las sugerencias aparecen como líneas de subrayado y se resumen en el panel **problemas** .  

## Configuración  

Esta extensión usa un archivo JSON de [configuración predeterminado][GithubWebhintioIndexjson] que activa sugerencias y analizadores para los sistemas HTML, CSS, de plantillas \ (JSX/TSX, angular, etc.), JavaScript/TypeScript y más.  

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

Si desea tener más control sobre las sugerencias y los analizadores que se activan, cree un `.hintrc` archivo local para configurar webhint.  Para obtener ayuda con la salida de sugerencias específicas, consulte [Guía para usuarios de webhint][WebhintDocsUserguideConfiguringSummary].  

## Ponerse en contacto con el equipo de webhint  

Envíe sus comentarios [archivando un problema][GithubWebhintioIssuesNew] en el [repositorio webhint de github][GithubWebhintio].  

Para contribuir a la extensión, consulte [Guía de contribución de extensión de código de vs][GithubWebhintioExtensionVscodeContributing].  

## Consulte también  

*   [Accesibilidad][AccessibilityIndex]  
*   [Visual Studio Code][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint VS Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Accesibilidad | Microsoft docs"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Código de Visual Studio | Microsoft docs"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Contribución-webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index. JSON-webhintio/Hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Problemas nuevos: webhintio/Hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Marketplace de Visual Studio"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configuración de webhint | Documentación de webhint"  
[WebhintMain]:  https://webhint.io "sugerencia"  

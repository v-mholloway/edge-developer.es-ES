---
description: Cómo usar webhint en Visual Studio code
title: webhint Visual Studio code extension
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
# <a name="webhint-vs-code-extension"></a><span data-ttu-id="ab929-104">Webhint Vs Extensión de código</span><span class="sxs-lookup"><span data-stu-id="ab929-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="ab929-105">Use [webhint][WebhintMain], una herramienta de linchado personalizable, para mejorar la accesibilidad, el rendimiento, la compatibilidad entre exploradores, la compatibilidad de PWA y la seguridad del sitio.</span><span class="sxs-lookup"><span data-stu-id="ab929-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="ab929-106">Comprueba el código en busca de procedimientos recomendados y errores comunes.</span><span class="sxs-lookup"><span data-stu-id="ab929-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="ab929-107">Este proyecto de código abierto, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="ab929-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="ab929-108">El equipo de Microsoft Edge sigue contribuyendo a la webhint junto con los desarrolladores web de la comunidad.</span><span class="sxs-lookup"><span data-stu-id="ab929-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de pantalla de webhint Visual Studio code extension":::
   <span data-ttu-id="ab929-110">Captura de pantalla de webhint Visual Studio code extension</span><span class="sxs-lookup"><span data-stu-id="ab929-110">Screenshot of webhint Visual Studio Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint Visual Studio Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="ab929-111">Identifique y corrija problemas en html, CSS, JavaScript, TypeScript y mucho más agregando la extensión [webhint Visual Studio Code][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="ab929-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for Visual Studio Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="ab929-112">Las sugerencias aparecen como subrayados en línea y se resumen en el **panel** Problemas.</span><span class="sxs-lookup"><span data-stu-id="ab929-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <a name="configuration"></a><span data-ttu-id="ab929-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="ab929-113">Configuration</span></span>  

<span data-ttu-id="ab929-114">Esta extensión usa un archivo [json][GithubWebhintioIndexjson] de configuración predeterminado que activa sugerencias y analizadores para HTML, CSS, sistemas de plantillas \(JSX/TSX, Angular, etc.),JavaScript/TypeScript, etc.</span><span class="sxs-lookup"><span data-stu-id="ab929-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

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

<span data-ttu-id="ab929-115">Si desea tener más control sobre las sugerencias y analizadores que se activan, cree un archivo local `.hintrc` para configurar webhint.</span><span class="sxs-lookup"><span data-stu-id="ab929-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="ab929-116">Para obtener ayuda con la salida de sugerencias específicas, vaya a la guía del usuario [de webhint][WebhintDocsUserguideConfiguringSummary].</span><span class="sxs-lookup"><span data-stu-id="ab929-116">For help with output from specific hints, navigate to [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <a name="getting-in-touch-with-the-webhint-team"></a><span data-ttu-id="ab929-117">Getting in touch with the webhint team</span><span class="sxs-lookup"><span data-stu-id="ab929-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="ab929-118">Envíe sus comentarios mediante [la presentación de un problema][GithubWebhintioIssuesNew] en el repositorio de [GitHub webhint][GithubWebhintio].</span><span class="sxs-lookup"><span data-stu-id="ab929-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="ab929-119">Para contribuir a la extensión, vaya a [webhint Visual Studio guía de contribución de extensión de código][GithubWebhintioExtensionVscodeContributing].</span><span class="sxs-lookup"><span data-stu-id="ab929-119">To contribute to the extension, navigate to [webhint Visual Studio Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <a name="see-also"></a><span data-ttu-id="ab929-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ab929-120">See also</span></span>  

*   [<span data-ttu-id="ab929-121">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="ab929-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="ab929-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab929-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

<!-- image links -->  

<!--[ImageWebhintExtension]: ./media/webhint-extension.png "Screenshot of webhint Visual Studio Code extension"  -->  

<!--links -->  

[AccessibilityIndex]: /microsoft-edge/accessibility "Accesibilidad | Microsoft Docs"  

[VisualstudiocodeIndex]: /microsoft-edge/visual-studio-code/index "Visual Studio código | Microsoft Docs"  

[GithubWebhintio]: https://github.com/webhintio/hint "webhint | GitHub"  
[GithubWebhintioExtensionVscodeContributing]: https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md "Contribuir: webhint | GitHub"  
[GithubWebhintioIndexjson]: https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json "index.js- webhintio/hint | GitHub"
[GithubWebhintioIssuesNew]: https://github.com/webhintio/hint/issues/new "Nuevos problemas: webhintio/hint | GitHub"  

[VisualstudioMarketplaceWebhint]: https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint "webhint | Visual Studio Marketplace"  

[OpenjsFoundation]:  https://openjsf.org "OpenJS Foundation"  

[WebhintDocsUserguideConfiguringSummary]: https://webhint.io/docs/user-guide/configuring-webhint/summary "Configuración de webhint | Documentación de webhint"  
[WebhintMain]:  https://webhint.io "webhint"  

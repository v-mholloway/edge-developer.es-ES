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
# <span data-ttu-id="9d937-104">Extensión de código webhint de vs</span><span class="sxs-lookup"><span data-stu-id="9d937-104">Webhint Vs Code Extension</span></span>  

<span data-ttu-id="9d937-105">Use [webhint][WebhintMain], una herramienta de desplegable personalizable, para mejorar la accesibilidad, el rendimiento, la compatibilidad entre exploradores, la compatibilidad de PWA y la seguridad de su sitio.</span><span class="sxs-lookup"><span data-stu-id="9d937-105">Use [webhint][WebhintMain], a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span>  <span data-ttu-id="9d937-106">Comprueba los procedimientos recomendados y los errores comunes de tu código.</span><span class="sxs-lookup"><span data-stu-id="9d937-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="9d937-107">Este proyecto de código abierto, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de la [OpenJS Foundation][OpenjsFoundation].</span><span class="sxs-lookup"><span data-stu-id="9d937-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation][OpenjsFoundation].</span></span>  <span data-ttu-id="9d937-108">El equipo de Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.</span><span class="sxs-lookup"><span data-stu-id="9d937-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>  

:::image type="complex" source="./media/webhint-extension.png" alt-text="Captura de pantalla de extensión de código webhint VS":::
   <span data-ttu-id="9d937-110">Captura de pantalla de extensión de código webhint VS</span><span class="sxs-lookup"><span data-stu-id="9d937-110">Screenshot of webhint VS Code extension</span></span>  
:::image-end:::

<!--![Screenshot of webhint VS Code extension][ImageWebhintExtension]  -->  

<span data-ttu-id="9d937-111">Identifique y solucione problemas en HTML, CSS, JavaScript, TypeScript y más agregando la [extensión webhint para vs Code][VisualstudioMarketplaceWebhint].</span><span class="sxs-lookup"><span data-stu-id="9d937-111">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code][VisualstudioMarketplaceWebhint].</span></span>  <span data-ttu-id="9d937-112">Las sugerencias aparecen como líneas de subrayado y se resumen en el panel **problemas** .</span><span class="sxs-lookup"><span data-stu-id="9d937-112">Hints appear as inline underlines and are summarized in the **Problems** pane.</span></span>  

## <span data-ttu-id="9d937-113">Configuración</span><span class="sxs-lookup"><span data-stu-id="9d937-113">Configuration</span></span>  

<span data-ttu-id="9d937-114">Esta extensión usa un archivo JSON de [configuración predeterminado][GithubWebhintioIndexjson] que activa sugerencias y analizadores para los sistemas HTML, CSS, de plantillas \ (JSX/TSX, angular, etc.), JavaScript/TypeScript y más.</span><span class="sxs-lookup"><span data-stu-id="9d937-114">This extension uses a [default configuration][GithubWebhintioIndexjson] json file that activates hints and parsers for HTML, CSS, templating systems \(JSX/TSX, Angular, and so on\), JavaScript/TypeScript, and more.</span></span>  

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

<span data-ttu-id="9d937-115">Si desea tener más control sobre las sugerencias y los analizadores que se activan, cree un `.hintrc` archivo local para configurar webhint.</span><span class="sxs-lookup"><span data-stu-id="9d937-115">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span>  <span data-ttu-id="9d937-116">Para obtener ayuda con la salida de sugerencias específicas, consulte [Guía para usuarios de webhint][WebhintDocsUserguideConfiguringSummary].</span><span class="sxs-lookup"><span data-stu-id="9d937-116">For help with output from specific hints, see [webhint user guide][WebhintDocsUserguideConfiguringSummary].</span></span>  

## <span data-ttu-id="9d937-117">Ponerse en contacto con el equipo de webhint</span><span class="sxs-lookup"><span data-stu-id="9d937-117">Getting in touch with the webhint team</span></span>  

<span data-ttu-id="9d937-118">Envíe sus comentarios [archivando un problema][GithubWebhintioIssuesNew] en el [repositorio webhint de github][GithubWebhintio].</span><span class="sxs-lookup"><span data-stu-id="9d937-118">Send your feedback by [filing an issue][GithubWebhintioIssuesNew] in [webhint GitHub repo][GithubWebhintio].</span></span>  

<span data-ttu-id="9d937-119">Para contribuir a la extensión, consulte [Guía de contribución de extensión de código de vs][GithubWebhintioExtensionVscodeContributing].</span><span class="sxs-lookup"><span data-stu-id="9d937-119">To contribute to the extension, see [webhint VS Code extension contribution guide][GithubWebhintioExtensionVscodeContributing].</span></span>  

## <span data-ttu-id="9d937-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9d937-120">See also</span></span>  

*   [<span data-ttu-id="9d937-121">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="9d937-121">Accessibility</span></span>][AccessibilityIndex]  
*   [<span data-ttu-id="9d937-122">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="9d937-122">Visual Studio Code</span></span>][VisualstudiocodeIndex]  

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

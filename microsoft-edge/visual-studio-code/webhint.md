---
description: Cómo usar webhint en código de Visual Studio
title: extensión de código webhint de VS
author: hxlnt
ms.author: raweil
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, vs Code, código de Visual Studio, webhint
ms.openlocfilehash: d3102bf4d8d4a8bba9225d8d3f68432197f775ac
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574857"
---
# <span data-ttu-id="a3846-104">extensión de código webhint de VS</span><span class="sxs-lookup"><span data-stu-id="a3846-104">webhint VS Code extension</span></span>

<span data-ttu-id="a3846-105">Use [webhint](https://webhint.io), una herramienta de desplegable personalizable, para mejorar la accesibilidad, el rendimiento, la compatibilidad entre exploradores, la compatibilidad de PWA y la seguridad de su sitio.</span><span class="sxs-lookup"><span data-stu-id="a3846-105">Use [webhint](https://webhint.io), a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span> <span data-ttu-id="a3846-106">Comprueba los procedimientos recomendados y los errores comunes de tu código.</span><span class="sxs-lookup"><span data-stu-id="a3846-106">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="a3846-107">Este proyecto de código abierto, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de la [OpenJS Foundation](https://openjsf.org/).</span><span class="sxs-lookup"><span data-stu-id="a3846-107">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation](https://openjsf.org/).</span></span> <span data-ttu-id="a3846-108">El equipo de Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.</span><span class="sxs-lookup"><span data-stu-id="a3846-108">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>

![Captura de pantalla de extensión de código webhint VS](./media/webhint-extension.png)

<span data-ttu-id="a3846-110">Identifique y solucione problemas en HTML, CSS, JavaScript, TypeScript y más agregando la [extensión webhint para vs Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span><span class="sxs-lookup"><span data-stu-id="a3846-110">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span></span> <span data-ttu-id="a3846-111">Las sugerencias aparecen como líneas de subrayado y se resumen en el panel problemas.</span><span class="sxs-lookup"><span data-stu-id="a3846-111">Hints appear as inline underlines and are summarized in the Problems pane.</span></span>

## <span data-ttu-id="a3846-112">Configuración</span><span class="sxs-lookup"><span data-stu-id="a3846-112">Configuration</span></span>

<span data-ttu-id="a3846-113">Esta extensión usa un archivo JSON de [configuración predeterminado](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) que activa sugerencias y analizadores para los sistemas HTML, CSS, de plantillas (JSX/TSX, angular, etc.), JavaScript/TypeScript y más.</span><span class="sxs-lookup"><span data-stu-id="a3846-113">This extension uses a [default configuration](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) json file that activates hints and parsers for HTML, CSS, templating systems (JSX/TSX, Angular, and so on), JavaScript/TypeScript, and more.</span></span>

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

<span data-ttu-id="a3846-114">Si desea tener más control sobre las sugerencias y los analizadores que se activan, cree un `.hintrc` archivo local para configurar webhint.</span><span class="sxs-lookup"><span data-stu-id="a3846-114">If you want more control over the hints and parsers that get activated, create a local `.hintrc` file to configure webhint.</span></span> <span data-ttu-id="a3846-115">Para obtener ayuda con la salida de sugerencias específicas, consulte la [Guía para usuarios de webhint](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span><span class="sxs-lookup"><span data-stu-id="a3846-115">For help with output from specific hints, see the [webhint user guide](https://webhint.io/docs/user-guide/configuring-webhint/summary/).</span></span>

## <span data-ttu-id="a3846-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3846-116">Feedback</span></span>

<span data-ttu-id="a3846-117">Envíenos sus comentarios [archivando un problema](https://github.com/webhintio/hint/issues/new) en el [repositorio webhint de github](https://github.com/webhintio/hint).</span><span class="sxs-lookup"><span data-stu-id="a3846-117">Send us your feedback by [filing an issue](https://github.com/webhintio/hint/issues/new) on the [webhint GitHub repo](https://github.com/webhintio/hint).</span></span> 

<span data-ttu-id="a3846-118">Para contribuir a la extensión, lee la guía de contribución de la [extensión de código de vs](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span><span class="sxs-lookup"><span data-stu-id="a3846-118">To contribute to the extension, please read the [webhint VS Code extension contribution guide](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).</span></span>

## <span data-ttu-id="a3846-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3846-119">See also</span></span>
  - [<span data-ttu-id="a3846-120">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="a3846-120">Accessibility</span></span>](/microsoft-edge/accessibility)
  - [<span data-ttu-id="a3846-121">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a3846-121">Visual Studio Code</span></span>](/microsoft-edge/visual-studio-code/)

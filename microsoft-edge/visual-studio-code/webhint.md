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
# extensión de código webhint de VS

Use [webhint](https://webhint.io), una herramienta de desplegable personalizable, para mejorar la accesibilidad, el rendimiento, la compatibilidad entre exploradores, la compatibilidad de PWA y la seguridad de su sitio. Comprueba los procedimientos recomendados y los errores comunes de tu código. Este proyecto de código abierto, desarrollado inicialmente por el equipo de Microsoft Edge, ahora forma parte de la [OpenJS Foundation](https://openjsf.org/). El equipo de Microsoft Edge continúa contribuyendo a la webhint junto con los desarrolladores web de la comunidad.

![Captura de pantalla de extensión de código webhint VS](./media/webhint-extension.png)

Identifique y solucione problemas en HTML, CSS, JavaScript, TypeScript y más agregando la [extensión webhint para vs Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint). Las sugerencias aparecen como líneas de subrayado y se resumen en el panel problemas.

## Configuración

Esta extensión usa un archivo JSON de [configuración predeterminado](https://github.com/webhintio/hint/blob/master/packages/configuration-development/index.json) que activa sugerencias y analizadores para los sistemas HTML, CSS, de plantillas (JSX/TSX, angular, etc.), JavaScript/TypeScript y más.

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

Si desea tener más control sobre las sugerencias y los analizadores que se activan, cree un `.hintrc` archivo local para configurar webhint. Para obtener ayuda con la salida de sugerencias específicas, consulte la [Guía para usuarios de webhint](https://webhint.io/docs/user-guide/configuring-webhint/summary/).

## Comentarios

Envíenos sus comentarios [archivando un problema](https://github.com/webhintio/hint/issues/new) en el [repositorio webhint de github](https://github.com/webhintio/hint). 

Para contribuir a la extensión, lee la guía de contribución de la [extensión de código de vs](https://github.com/webhintio/hint/blob/master/packages/extension-vscode/CONTRIBUTING.md).

## Consulte también
  - [Accesibilidad](/microsoft-edge/accessibility)
  - [Visual Studio Code](/microsoft-edge/visual-studio-code/)

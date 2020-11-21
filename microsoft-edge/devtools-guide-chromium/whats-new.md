---
description: Características agregadas al DevTools Microsoft Edge (cromo) en 2019 de marzo
title: Novedades de la DevTools de Microsoft Edge (cromo) en 2019 de marzo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/23/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0b592eddbd68b3bbd8ff0a9edf9a1253bd79677e
ms.sourcegitcommit: acf8ad7cb6c8ecf83a6170f8eeb9bec32878f8ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182515"
---
# Novedades de Microsoft Edge (cromo) DevTools

Muchas gracias por probar una vista previa del nuevo Microsoft Edge. Con esta versión, hemos realizado un importante cambio en la plataforma web subyacente de Microsoft Edge adoptando el proyecto de código abierto de cromo. Con este cambio, será más fácil crear y probar sus sitios web en Microsoft Edge y asegurarse de que seguirán funcionando de la manera esperada, incluso si los usuarios están explorando en un explorador de cromo diferente, como Google Chrome, Vivaldi, opera o Brave.

## El nuevo DevTools Microsoft Edge (cromo)

Si va a retirar Microsoft Edge y principalmente desarrolla en un explorador basado en cromo, debe sentirse bien en casa. Las herramientas de desarrollador de Microsoft Edge (cromo) son exactamente iguales a las herramientas de desarrollador que ya conoces y usas.

![Microsoft Edge (cromo) DevTools](./media/devtools.png)

Si desproteges el nuevo Microsoft Edge y tú desarrollas principalmente en Microsoft Edge (EdgeHTML), tenemos algunas fantásticas herramientas nuevas que esperamos que te resulte más fácil y rápido de crear y probar tus sitios web en Microsoft Edge. Para obtener más información sobre estas nuevas herramientas, consulte [la guía de DevTools Microsoft Edge (cromo)](../devtools-guide-chromium.md).

## Nuevos temas oscuros y claros para la DevTools

Hemos diseñado algunos nuevos temas oscuros y claros para la DevTools que creemos que te encantará. De forma predeterminada, el DevTools Microsoft Edge (cromo) usará el tema oscuro. Para cambiar el tema de la DevTools, pulse `Fn`  +  `F1` en Windows o Mac o desplácese a configuración con el `...` botón situado en la esquina superior derecha de la DevTools.

![Menú principal de Microsoft Edge (cromo) DevTools](./media/devtools-main-menu.png)

En configuración, puede cambiar el tema de la DevTools. Si te gustaste la manera en que el DevTools buscó en tu explorador basado en cromo, puedes hacer que la DevTools de Microsoft Edge (cromo) sea exactamente igual que selecciona los temas **oscuros (cromo)** o **Light (cromo** ), respectivamente. 

## Depurar Microsoft Edge (cromo) del código VS

Con el [depurador de la extensión de código de Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs, ahora puedes depurar Microsoft Edge (EdgeHTML) y Microsoft Edge (cromo) directamente desde el código de vs.

![Depurador para la extensión de código perimetral de VS](./media/vscode-debugger.png)

Para iniciar Microsoft Edge (cromo) en lugar de Microsoft Edge (EdgeHTML) desde VS Code, debe agregar un `version` atributo a la **launch.jsexistente en** la configuración con la versión de Microsoft Edge (cromo) que desea iniciar ( `dev` , `beta` , o `canary` ). Este es un ejemplo **launch.jsde** la configuración que iniciará la versión Canarias de Microsoft Edge (cromo) a [Bing.com](https://www.bing.com/):

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Microsoft Edge (Chromium) Canary against Bing",
    "url": "https://bing.com"
}
```

Para obtener más información, consulte [Cómo depurar Microsoft Edge (cromo) del código vs](../visual-studio-code/debugger-for-edge.md).

## Actualización de protocolo Edge DevTools

Con el turno en la plataforma web subyacente de Microsoft Edge, el protocolo Edge DevTools no recibirá más actualizaciones. El DevTools de Microsoft Edge (cromo) usará el CDP o el protocolo de DevTools de Chrome. Para consultar la documentación de los dominios y métodos de CDP, visite [el CDP Viewer](https://chromedevtools.github.io/devtools-protocol/tot/Accessibility).

En el nuevo Microsoft Edge, `ms` no se admitirá ningún método con el prefijo. Para obtener más información sobre cómo usar CDP en Microsoft Edge (cromo), consulte [DevTools Protocol (cromo)](../devtools-protocol-chromium.md).

## Problemas conocidos

Muchos vínculos de la DevTools Microsoft Edge (cromo) al contenido hospedado en sitios de terceros se han eliminado temporalmente. Tan pronto como podamos reemplazar estos vínculos, los agregaremos de nuevo a la DevTools.


Al depurar contenido web en un dispositivo Android desde Microsoft Edge (cromo), la versión de la DevTools que se inicia al hacer clic en el botón **inspeccionar** de la herramienta **dispositivos remotos** puede no coincidir con la versión del explorador de su dispositivo Android. Como resultado, es posible que vea nuevas características en el DevTools que no funcionarán en el explorador de su dispositivo Android. Si esto es algo que te encuentras, nos encantaría hablar sobre él, por lo tanto, [Enviar comentarios](../devtools-guide-chromium.md#getting-in-touch-with-the-microsoft-edge-devtools-team).

Por último, Visual Studio en Windows y Mac aún no es compatible con Microsoft Edge (cromo). Regístrese [aquí](https://visualstudio.microsoft.com/vs/preview/) para ser la primera en saber cuándo tenemos una versión preliminar de Visual Studio que admite la depuración de JavaScript dentro de Microsoft Edge (cromo) para proyectos de ASP.net.  

---
description: IE mode and the Microsoft Edge (cromo) DevTools
title: Modo Internet Explorer y DevTools
author: robpaveza
ms.author: ropaveza
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, ie11, Internet Explorer 11, modo IE
ms.openlocfilehash: 18e5f029d277e446857ec48b9cf129149f219256
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574497"
---
# Modo Internet Explorer y DevTools

Este documento describe cómo el modo de Internet Explorer (modo IE) se integra con el DevTools de Microsoft Edge (cromo).

## Descripción del modo IE

El modo IE es un mecanismo por el cual las empresas pueden especificar un conjunto de sitios web que, hasta ahora, funciona solo en Internet Explorer 11. Cuando estos sitios web se visualizan en Microsoft Edge (cromo), se está ejecutando una instancia completa de Internet Explorer 11 y se representa en la pestaña. Esto permite a las empresas administrar la compatibilidad de los modos de documento de IE, los controles ActiveX y otros componentes heredados que actualmente no son compatibles con los exploradores Web modernos.

En el modo IE, el proceso de representación está totalmente basado en Internet Explorer 11. El proceso del administrador de Microsoft Edge (cromo) administra la duración del proceso de representación, pero está limitado a la vigencia de la pestaña en un sitio o aplicación determinados. Cuando una pestaña se representa en modo IE, aparece un distintivo en la barra de direcciones de la pestaña determinada:

![Distintivo de modo IE en la barra de direcciones](./media/ie-mode-badge.png)

El modo IE está disponible actualmente en Windows 10 versión 1903 (2019 de mayo), pero pronto estará disponible para todas las plataformas de Windows compatibles.

## Iniciar DevTools en una pestaña en modo IE

Si está intentando ver el modo de documento de un sitio web en modo IE, puede hacer clic en el distintivo de la barra de direcciones.

![Ver el modo de documento mediante identificador de modo IE](./media/ie-mode-badge-doc-mode.png)

Mientras se encuentra en una pestaña en modo IE, la DevTools no funciona. Al pulsar `F12` o `Ctrl` + `Shift` + `I` solo se iniciará una instancia en blanco de la DevTools de Microsoft Edge (cromo) con un mensaje que dice: "las herramientas para desarrolladores no están disponibles en el modo Internet Explorer. Para depurar la página, ábrala en Internet Explorer 11. " El origen de la **vista** iniciará el Bloc de notas e **Inspeccionar elemento** no será visible en el menú contextual del modo IE.

Esto se debe a que una serie de componentes en el DevTools (como las herramientas de rendimiento y red) se interrumpirían cuando el motor de representación cambia de cromo a Internet Explorer 11 en modo IE. Para enviarnos comentarios, haga clic en el `:)` icono.

![DevTools iniciado en modo IE](./media/ie-mode-devtools.png)

Si está desarrollando o manteniendo una aplicación o un sitio web basado en Internet Explorer 11, le recomendamos que navegue a la misma página en Internet Explorer 11. En Windows 10, puede encontrar el acceso directo para Internet Explorer 11 en el menú Inicio, debajo de accesorios de Windows. En Windows 7, puede encontrar Internet Explorer 11 en el menú Inicio principal. A continuación, puede iniciar la DevTools de Internet Explorer pulsando `F12` o haciendo clic en **Inspeccionar elemento** en el menú contextual. Para obtener más información sobre cómo usar estas herramientas, haga clic [aquí](/previous-versions/windows/internet-explorer/ie-developer/samples/bg182326(v%3dvs.85)).

## Depuración remota y modo IE

Puede iniciar Microsoft Edge (cromo) con la depuración remota habilitada, que es, por lo general, cómo se usan herramientas como Visual Studio o VS Code Launch Edge en la línea de comandos:

`start msedge --remote-debugging-port=9222`

Cuando se inicia Microsoft Edge (cromo) con este argumento de la línea de comandos, el modo IE no estará disponible. Aún puede navegar a sitios web o aplicaciones que, de lo contrario, se verían en modo IE, pero el contenido se representará a través de cromo, no Internet Explorer 11. Puede esperar que las partes de las páginas que dependen de IE11, como los controles ActiveX, no se representen correctamente. La identificación de modo IE ya no aparecerá en la barra de direcciones.

El modo de IE permanecerá como no disponible hasta que cierre completamente Microsoft Edge (cromo).
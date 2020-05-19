---
description: Opciones de distribución al publicar una aplicación con Microsoft Edge WebView2
title: Distribución de la aplicación Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: a789b0f4f9c482670f843ed21368b4168f99abe0
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659729"
---
# Distribución de aplicaciones con WebView2 

El control WebView2 usa el explorador Microsoft Edge \ (cromo \). Al distribuir la aplicación, asegúrese de que el explorador Edge está instalado en todos los equipos de usuario donde se ejecuta la aplicación. El control WebView2 usa la versión más estable del explorador que se instala en un equipo. Por ejemplo, es posible que tenga la versión estable, beta, dev y Canarias instalados al mismo tiempo y, en esta situación, los controles de WebView2 se ejecutan en el canal estable. Asegúrese de revisar las notas de la versión para asegurarse de que la versión del explorador instalada en los equipos que ejecutan los controles de WebView2 cumpla con los requisitos de versión mínima.

## Guía básica

Reconocemos que es posible que el explorador Edge no esté disponible en todos los equipos de los usuarios en los que se ejecutará la aplicación, o que la instalación de un explorador Edge en toda la organización sea difícil. Para garantizar que la aplicación se ejecuta en todas las máquinas, independientemente del explorador Microsoft Edge instalado, lanzaremos el tiempo de ejecución de Microsoft Edge WebView2. Además, actualizaremos WebView2 para buscar la versión estable del motor en tiempo de ejecución antes de buscar las versiones preliminares del explorador instalado.

Se admitirán dos opciones de distribución con el tiempo de ejecución de WebView2: hoja perenne y versión fija.

Perenne será el modelo de distribución recomendado para la mayoría de los programadores. En este modo, las actualizaciones se insertan automáticamente en el tiempo de ejecución de WebView2 sin más esfuerzo por parte de tu aplicación. El modelo de hoja perenne garantiza que la aplicación esté aprovechando las últimas características y actualizaciones de seguridad de contenido web hospedado.

Para entornos restringidos, habrá compatibilidad con un modelo de distribución de versiones fijo. En este modelo, la aplicación selecciona y empaqueta una versión específica de WebView2. Las actualizaciones de la versión de WebView no se realizan automáticamente y serán responsabilidad de la aplicación. El modelo de versión fijo es útil cuando necesita controlar la versión del explorador y cuando se actualiza la aplicación. 

### Microsoft Edge WebView2 Runtime

El tiempo de ejecución de Microsoft Edge WebView2 empaquetará los binarios de explorador optimizados para el uso de las aplicaciones de WebView2. Funcionará de forma independiente o en paralelo con un explorador de cliente perimetral instalado. Instalar el motor de tiempo de ejecución es compatible con muchas aplicaciones de WebView2 que se ejecutan en el equipo cliente. Instalar el motor en tiempo de ejecución no aparecerá como un explorador para los usuarios finales, y no tendrá accesos directos de escritorio, puntos de entrada del menú Inicio ni registro de protocolo.

Las aplicaciones que usan el tiempo de ejecución de WebView2 deberán asegurarse de que se complete la instalación en tiempo de ejecución. Para asegurarse de que su aplicación Instale el runtime como una dependencia, podrá agregar el motor en tiempo de ejecución al flujo de instalación. 

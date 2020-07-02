---
description: Opciones de distribución al publicar una aplicación con Microsoft Edge WebView2
title: Distribución de la aplicación Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 370b5da2d42412a08a5c7f8a7401496fa70e3065
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844407"
---
# Distribución de aplicaciones con WebView2  

El control WebView2 usa la plataforma Microsoft Edge \ (cromo \).  Cuando empaquete y distribuyas tu aplicación, asegúrate de que haya una copia de la plataforma o el tiempo de ejecución de WebView2 antes de que se inicie la aplicación.  En la siguiente página se describe cómo \ (el desarrollador \) puede asegurarse de que se ha instalado el tiempo de ejecución de WebView2 y el uso de los dos modos de distribución para su aplicación de WebView2: [hoja perenne](#evergreen-distribution-mode) y [versión fija](#fixed-version-distribution-mode).  

## Modo de distribución de hoja perenne  

El modo de distribución de hoja perenne garantiza que tu aplicación esté aprovechando las últimas características y actualizaciones de seguridad.  El modo de distribución de hoja perenne tiene las siguientes características:  

*   La plataforma web se actualiza automáticamente sin ningún esfuerzo adicional por parte del usuario.  
*   Todas las aplicaciones que aprovechan el modo de distribución de hoja perenne usan una copia compartida de los binarios de la plataforma, lo que ahorra espacio en el disco.  

Hay varios canales WebView2 que las aplicaciones pueden usar como plataforma Web.  De forma predeterminada, WebView2 se destina al canal más estable disponible en el dispositivo que cumple los requisitos de versión mínima del SDK de WebView2.  Los canales siguientes aparecen ordenados en orden desde el canal más estable al menos estable.  

1.  WebView2 Runtime \ (versión preliminar \)  
1.  Canal Microsoft Edge Beta  
1.  Canal Microsoft Edge Dev  
1.  Canal Microsoft Edge Canary    

> [!NOTE]
> Se recomienda usar el modelo de distribución de hoja perenne para la mayoría de los programadores.  

> [!IMPORTANT]
> El canal estable de Microsoft Edge no es un objetivo válido para WebView2, y las razones se describen más adelante.  

Para obtener más información sobre el control de versiones, consulte el apartado sobre el [control de versiones][ConceptsVersioning] y [globales][ReferenceWin3209538WebviewIdl].  

### Comprender el programa de instalación y el tiempo de ejecución de WebView2 (vista previa)  

Es posible que el canal estable de Microsoft Edge no se instale en todos los equipos de usuario en los que se ejecuta la aplicación.  En lugar de requerir que los usuarios instalen Microsoft Edge, la aplicación puede usar el tiempo de ejecución de WebView2 perenne y el instalador \ (versión preliminar \).  El tiempo de ejecución de WebView2 es una copia personalizada de los binarios de Microsoft Edge que se usa para ejecutar las aplicaciones de WebView2.  Cuando se instala el motor en tiempo de ejecución de WebView2, los usuarios no pueden usarlo como un explorador normal.  Por ejemplo, no hay ningún acceso directo de escritorio, entrada del menú Inicio, los usuarios no pueden abrir una ventana del explorador con los binarios de tiempo de ejecución, etc.  Todas las aplicaciones de WebView2 de hoja perenne del dispositivo pueden usar una única instalación de hoja de WebView2 en tiempo de ejecución.  

Hoy, durante la vista previa, el tiempo de ejecución de WebView2 perenne y el canal de desarrollo de Microsoft Edge se actualizan al mismo tiempo y tienen la misma compilación.  En el futuro, durante la versión preliminar, el equipo de WebView2 planea actualizar el tiempo de ejecución de WebView2 y hacer coincidir la misma compilación que el canal de Microsoft Edge beta.  En el futuro, cuando WebView2 alcance la disponibilidad general \ (GA \), el equipo de WebView2 planea actualizar el tiempo de ejecución de WebView2 y coincidir con la misma compilación que el canal estable de Microsoft Edge.  Después de GA, las aplicaciones deben usar el tiempo de ejecución de WebView2 en producción.  

> [!IMPORTANT]
> No envíe aplicaciones de WebView2 en producción durante la versión preliminar.  

Use el siguiente flujo de trabajo para asegurarse de que el tiempo de ejecución de WebView2 de perenne esté disponible.  

1.  Descargue el último [instalador de WebView2 de perenne][Webview2Installer].  
1.  Incluya el instalador en el instalador o actualizador de la aplicación.  
1.  Durante la instalación o actualización de la aplicación, compruebe si el tiempo de ejecución de WebView2 perenne ya está instalado en el equipo del usuario.  Si no es así, la aplicación invoca el instalador para instalar el motor en tiempo de ejecución.  

Según el escenario, es posible que tenga que cambiar el flujo de trabajo anterior.  Por ejemplo, el instalador de la aplicación puede descargar el instalador de tiempo de ejecución de WebView2 de perenne en lugar de incluirlo en el paquete de la aplicación.  

> [!NOTE]
> Tanto el Runtime de WebView2 como el instalador de tiempo de ejecución de WebView2 están en versión preliminar.  La vista previa tiene un ámbito inicial limitado y solo está disponible como una instalación independiente por máquina en Windows 10 en x64.  En el futuro, se planea el soporte técnico para Windows 7, x86 y ARM64.  

### Procedimientos recomendados para usar WebView2 Runtime y canales de Microsoft Edge no estables  

Tenga en cuenta las siguientes recomendaciones durante la vista previa.  

*   Asegúrese de usar el [programa de instalación y el tiempo de ejecución de WebView2 de hoja perenne][Webview2Installer] para desarrollar o probar la canalización de empaquetado y distribución.  En el futuro, la aplicación de producción debe incluir el instalador.  
*   Para desarrollar la aplicación, puede usar el tiempo de ejecución de WebView2 perenne.  Sin embargo, a medida que el tiempo de ejecución se desplaza del canal de desarrollo al canal de versión beta o al canal estable, es posible que el número de compilación de tiempo de ejecución no cumpla los requisitos de versión mínimos del SDK de WebView2 Preview.  Si desea usar el SDK más reciente, instale el canal Canarias de Microsoft Edge para asegurarse de que haya una compilación compatible disponible en el dispositivo.  Para obtener más información sobre el control de versiones, consulte [control de versiones][ConceptsVersioning].  
*   Para comprobar la compatibilidad de su contenido web con los cambios de la plataforma que no está disponible en el canal estable, use el canal no estable adecuado según sea necesario.  

## Modo de distribución de versiones fijas  

> [!NOTE]
> El modelo de distribución de versiones fijo no está disponible en este momento.  

En el caso de entornos restringidos, hay planes para admitir un modo de distribución de versión corregido \ (denominado "poner en servicio").  El modo de distribución de versiones fijo le permite seleccionar y empaquetar una versión específica del tiempo de ejecución de WebView2.  El modo de distribución de versiones fijo le permite controlar qué versión de tiempo de ejecución de WebView2 usa la aplicación, y cuándo se actualizan los equipos de usuario.  El modo de distribución de versiones fijo no recibe actualizaciones automáticas y debe planear la aplicación manual de actualizaciones.  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Descripción de las versiones de explorador y WebView2 | Microsoft docs"  
[ReferenceWin3209538WebviewIdl]: ../reference/win32/0-9-538/webview2-idl.md  "GLOBALS | Microsoft docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2"  

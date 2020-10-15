---
description: Opciones de distribución al publicar una aplicación con Microsoft Edge WebView2
title: Distribución de aplicaciones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: e96ca2b26feb3883b51ad468db1fabe68ed8ad1f
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119005"
---
# Distribución de aplicaciones con WebView2  

Al distribuir tu aplicación de WebView2, asegúrate de que la plataforma web de respaldo (el [tiempo de ejecución de WebView2](#understanding-the-webview2-runtime) está presente antes de que se inicie la aplicación).  En este artículo se describe cómo los programadores pueden instalar el tiempo de ejecución de WebView2 y usar los dos modos de distribución para su aplicación de WebView2:  [hoja perenne](#evergreen-distribution-mode) y [versión corregida](#fixed-version-distribution-mode).  

## Modo de distribución de hoja perenne  

> [!NOTE]
> Se recomienda el modo de distribución de hoja perenne para la mayoría de los programadores.  

El modo de distribución de hoja perenne garantiza que tu aplicación esté aprovechando las últimas características y actualizaciones de seguridad.  Tiene las siguientes características:  

*   La plataforma web subyacente \ (WebView2 Runtime \) se actualiza automáticamente sin esfuerzos adicionales por parte de los programadores.  
*   Todas las aplicaciones que usan el modo de distribución de hoja perenne usan una copia compartida del tiempo de ejecución de WebView2 perenne, que ahorra espacio en el disco.  

### Descripción del tiempo de ejecución de WebView2  

El tiempo de ejecución de WebView2 es un Runtime redistribuible y actúa como la plataforma web de respaldo para aplicaciones de WebView2.  Este concepto es similar a VC + + o .NET Runtime para aplicaciones de/.NET de C++.  En el tiempo de ejecución, el motor en tiempo de ejecución modifica los binarios de Microsoft Edge \ (cromo \) que se han optimizado y probado para las aplicaciones.  El motor en tiempo de ejecución no aparecerá como un explorador visible para el usuario durante la instalación; por ejemplo, los usuarios no tendrán un acceso directo al escritorio del explorador ni una entrada del menú Inicio.  

Para el desarrollo y las pruebas, los desarrolladores pueden usar el motor en tiempo de ejecución o cualquier canal de explorador de Microsoft Edge \ (cromo \) no estable para la plataforma web de respaldo.  En los entornos de producción, los desarrolladores deben asegurarse de que el tiempo de ejecución está presente en los dispositivos de usuario antes de que se inicie la aplicación.  El canal estable de Microsoft Edge no está disponible para que el uso de WebView2 impida que las aplicaciones tomen una dependencia en el explorador en producción.  

Los desarrolladores no deben tomar una dependencia en el explorador porque:  

*   No se garantiza que Microsoft Edge \ (cromo \) esté presente en todos los dispositivos de usuario.  Por ejemplo, los dispositivos desconectados de Windows Update o no administrados por Microsoft directamente \ (una gran parte del mercado Enterprise/EDU \) pueden no tener el explorador.  Permitir a los desarrolladores distribuir el tiempo de ejecución de WebView2 evita tener que tomar una dependencia en el explorador como requisito previo para las aplicaciones.
*   Los exploradores y las aplicaciones tienen diferentes casos de uso, por lo que tomar una dependencia en un explorador puede tener efectos secundarios no deseados en las aplicaciones.  Por ejemplo, los administradores de TI pueden controlar el control de versiones del explorador para la compatibilidad con sitios Web internos.  WebView2 Runtime permite a las aplicaciones mantener la hoja perenne mientras se administran activamente las actualizaciones del explorador.  
*   A diferencia del explorador, el motor en tiempo de ejecución se desarrolla y se prueba para escenarios de aplicación y, en algunos casos, puede incluir correcciones de errores que aún no estén disponibles en el explorador.  

El tiempo de ejecución de WebView2 de perenne está planeado para enviar la bandeja de entrada en versiones futuras de Windows.  Antes de que el tiempo de ejecución esté más disponible universalmente, se recomienda a los programadores implementar el motor de tiempo de ejecución junto con su aplicación de producción.  

### Implementar el tiempo de ejecución de WebView2 de hoja perenne  

Solo se necesita una instalación del tiempo de ejecución de WebView2 de perenne para todas las aplicaciones de hoja perenne del dispositivo.  Hay varias herramientas disponibles en la [Página de descarga de tiempo de ejecución de WebView2][Webview2Installer] para ayudar a los desarrolladores a implementar el tiempo de ejecución de hoja perenne, como:  

*   El programa previo en tiempo de ejecución de WebView2 \ (que se publicará pronto \) es un pequeño \ (aproximadamente 2 MB \) instalador.  Este instalador descarga e instala el tiempo de ejecución de perenne de los servidores de Microsoft que coincidan con la arquitectura de dispositivo del usuario.  
*   Vínculo para descargar el programa previo \ (que se publicará pronto \) es un vínculo para que los desarrolladores descarguen el programa previo mediante programación.
*   El instalador independiente de WebView2 en tiempo de ejecución es un instalador completo que puede instalar el Runtime de WebView2 de perennes en entornos sin conexión.  

Actualmente, el programa previo y el instalador independiente solo admiten la instalación por máquina, que requiere elevación.  Cuando se ejecuta sin elevación, aparece un mensaje de control de cuenta de usuario de Windows para pedir a los usuarios que eleven los permisos.  

Recomendamos los siguientes flujos de trabajo para garantizar que el tiempo de ejecución ya esté instalado antes de que se inicie la aplicación.  Puede ajustar el flujo de trabajo en función de su escenario.  También proporcionaremos código de ejemplo en el futuro.  

#### Implementación solo en línea  

Si tiene un escenario de implementación solo en línea donde se supone que los usuarios finales tienen acceso a Internet, siga estos pasos:  

*   Durante la configuración de la aplicación, compruebe si el motor en tiempo de ejecución ya lo ha instalado:  
    *   Inspeccionar si existe la clave `pv (REG_SZ)` de aplicación en `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` o  
    *   Llamar a la API de WebView2 [GetAvailableCoreWebView2BrowserVersionString](/microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring) y comprobar si versionInfo es NULL.  
*   Si el motor en tiempo de ejecución no está instalado, usa el vínculo para descargar el programa previo mediante programación.  
*   Invocar el programa previo desde un proceso o símbolo del sistema elevado con `MicrosoftEdgeWebview2Setup.exe /silent /install` para la instalación silenciosa.  

Este flujo de trabajo le asegura que instale el Runtime solo cuando sea necesario, no es necesario que Empaquete los instaladores o detecte la arquitectura de los dispositivos de usuario, y puede instalar el motor en tiempo de ejecución de forma silenciosa.  También puede optar por empaquetar el programa previo con la aplicación en lugar de descargarlo mediante programación a petición.  

#### Implementación sin conexión  

Si tiene un escenario de implementación sin conexión en el que la implementación de aplicaciones debe trabajar sin conexión, realice los siguientes pasos:  

*   Descargue el [instalador independiente][Webview2Installer].  
*   Incluya el instalador en el instalador o actualizador de la aplicación.  
*   Durante la configuración de la aplicación, compruebe si el motor en tiempo de ejecución ya lo ha instalado:  
    *   Inspeccionar si existe la clave `pv (REG_SZ)` de aplicación en `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\ClientState\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}` o  
    *   Llamar a la API de WebView2 [GetAvailableCoreWebView2BrowserVersionString](/microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring) y comprobar si versionInfo es NULL.  
*   Si el motor en tiempo de ejecución no está instalado, invoque el instalador independiente desde un proceso con privilegios elevados o un símbolo del sistema con `MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install` para una instalación silenciosa.  

## Modo de distribución de versiones fijas  

> [!NOTE]
> El modo de distribución de versiones fijas aún no está disponible.  

En el caso de entornos restringidos, hay planes para admitir una versión fija, previamente denominada traiga-Your-Own, modo de distribución.  El modo de distribución de versiones fijo permite a los desarrolladores seleccionar y empaquetar una versión específica del tiempo de ejecución de WebView2.  El modo de distribución de versiones fijo le permite controlar qué versión de tiempo de ejecución de WebView2 usa la aplicación, y cuándo se actualizan los equipos de usuario.  El modo de distribución de versiones fijo no recibe actualizaciones automáticas y los desarrolladores deben planear la aplicación de las actualizaciones.  


<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Descripción de las versiones de explorador y WebView2 | Microsoft docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador de WebView2"  

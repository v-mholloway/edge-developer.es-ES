---
description: Una referencia para las funcionalidades de WebDriver y las opciones específicas de Microsoft Edge admitidas por EdgeDriver (Chromium).
title: Funciones y EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, html, css, javascript, programador, webdriver, se sintaxis, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: 5a48ca34e46b56fa60bcacfade2add23026be144
ms.sourcegitcommit: f95812c4e1b7277f67c6c4891be2779cc1b5bdf1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/18/2021
ms.locfileid: "11343782"
---
# Funciones y EdgeOptions  

Las funcionalidades son opciones que puede usar para personalizar y configurar una `EdgeDriver` sesión.  Para obtener información sobre cómo iniciar una nueva sesión, vaya a `EdgeDriver` Automatización de Microsoft [Edge.][WebdriverIndexAutomateMicrosoftEdgeChromium]  En este artículo se describen todas las funcionalidades admitidas [para Microsoft Edge][WebdriverIndexInstallMicrosoftEdgeChromium] y detalles sobre cómo pasar las funcionalidades a las `EdgeDriver` sesiones.  

Las funcionalidades se pasan a una sesión de WebDriver como un mapa JSON.  Los enlaces de idioma de WebDriver suelen proporcionar métodos de comodidad seguras para que no necesite configurar el mapa JSON usted mismo.  Los distintos enlaces de idioma de WebDriver usan diferentes mecanismos para configurar funcionalidades.  Navegue a la documentación de su [enlace de idioma preferido][WebdriverIndexChooseWebdriverLanguageBinding] para obtener más información sobre cómo configurar funcionalidades.  [Se siné][SeleniumMain] configura las funcionalidades a través de la `EdgeOptions` clase.  

## Uso de la clase EdgeOptions  

Cree una instancia de `EdgeOptions` , que proporciona métodos de comodidad para establecer funcionalidades específicas de Microsoft Edge.  Después de configurar el `EdgeOptions` objeto, pasa `EdgeOptions` al `EdgeDriver` constructor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Para usar funcionalidades que no tienen un método de comodidad asociado, use el `AddAdditionalCapability` método.  Debe pasar el nombre completo de la funcionalidad y un valor con el tipo correcto.  Para revisar la lista completa de las capacidades aceptadas y los tipos de valor, vaya al [objeto EdgeOptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Capacidades reconocidas  

Para obtener las funcionalidades estándar que acepta, vaya a la documentación `EdgeDriver` [de Sejunio][SharedCapabilitiesSeleniumDocumentation] y al estándar [W3C WebDriver][CapabilitiesW3cWebdriver].  En este artículo solo se enumeran las funcionalidades específicas de Microsoft Edge.  

## EdgeOptions (objeto)  

La mayoría de las funcionalidades específicas de Microsoft Edge se exponen a través del `EdgeOptions` objeto.  En algunos idiomas, la clase implementa las `EdgeOptions` capacidades.  En otros idiomas, las capacidades se almacenan en el `ms:edgeOptions` diccionario en `DesiredCapabilities` .  

| Funcionalidad | Tipo | Valor predeterminado | Detalles |  
|:--- |:--- |:--- |:--- |  
| args | lista de cadenas |  | Lista de argumentos de línea de comandos que se usarán al iniciar Microsoft Edge.  Los argumentos con un valor asociado deben estar separados por un `=` signo \(por ejemplo, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \). |  
| binary | string |  | Ruta de acceso al binario de Microsoft Edge para usar \(en macOS, la ruta de acceso debe ser el binario real, no solo la aplicación.  por ejemplo, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \). |  
| debuggerAddress | string |  | Una dirección de un servidor depurador al que se va a conectar, por `hostname/ip:port` ejemplo, en forma de . `127.0.0.1:38947` |
| desasoyen | booleano | `false` | Si , Microsoft Edge se cierra cuando se cierra el servicio WebDriver, incluso si el extremo local de `false` WebDriver no ha cerrado la sesión.  Si `true` , Microsoft Edge solo se cierra si el final local de WebDriver cierra la sesión.  Si , y el final local de WebDriver no cierra la sesión, no limpia la carpeta de datos de usuario temporal usada por la instancia `true` `EdgeDriver` de Microsoft Edge. |  
| excludeSwitches | lista de cadenas |  | Lista de modificadores de la línea de comandos de Microsoft Edge para excluir que EdgeDriver pasa de forma predeterminada al iniciar Microsoft Edge.  Evite el `--` prefijo de modificadores. |  
| extensions | lista de cadenas |  | Una lista de extensiones para instalar en el inicio.  Cada elemento de la lista debe ser una extensión empaquetada codificada en base 64 \( `.crx` \). |  
| localState | diccionario |  | Un diccionario con cada entrada que consta del nombre de la preferencia y el valor.  Las preferencias se aplican al archivo de estado local en la carpeta de datos de usuario. |  
| minidumpPath | string |  | Directorio para almacenar minidumps de Microsoft Edge.  \(Compatible solo en Linux.\) |  
| mobileEmulation | diccionario |  | Un diccionario con un valor para `deviceName` , o valores para y `deviceMetrics` `userAgent` . |  
| perfLoggingPrefs | diccionario |  | Un diccionario opcional que especifica las preferencias de registro de rendimiento.  para obtener más información, vaya al [objeto perfLoggingPrefs](#perfloggingprefs-object). |  
| prefs | diccionario |  | Un diccionario con cada entrada que consta del nombre de la preferencia y el valor.  Las preferencias solo se aplican al perfil de usuario en uso.  Para obtener ejemplos, vaya al `Preferences` archivo en la carpeta de datos de usuario de Microsoft Edge. |  
| wdpAddress | string |  | Una dirección de un servidor de Windows Device Portal al que se conecta, en forma de `hostname/ip:port` , por  `127.0.0.1:50080` ejemplo.  Para obtener más información, ve [a Depuración remota : dispositivos Con Windows 10.][DevtoolsRemoteDebuggingWindows] |  
| wdpPassword | string |  | Contraseña opcional que se usará al conectarse a un servidor de Windows Device Portal.  Obligatorio si el servidor tiene habilitada la autenticación. |  
| wdpUsername | string |  | Nombre de usuario opcional que se usará al conectarse a un servidor de Windows Device Portal.  Obligatorio si el servidor tiene habilitada la autenticación. |  
| windowsApp | string |  | Identificador de modelo de usuario de aplicación de un paquete de aplicación de Microsoft Edge para iniciar, por `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` ejemplo.  Se `windowsApp` usa en lugar de conectarse a un dispositivo o emulador de Windows `binary` 10X mediante Windows Device Portal. |  
| windowTypes | lista de cadenas |  | Una lista de tipos de ventana que se muestran en la lista de identificadores de ventana.  Para obtener acceso a los elementos de vista web de Android, `webview` incluya en la lista. |  

## perfLoggingPrefs (objeto)  

El `perfLoggingPrefs` diccionario tiene el siguiente formato \(todas las claves son opcionales\).  

| Tecla | Tipo | Valor predeterminado | Detalles |  
|:--- |:--- |:--- |:--- |  
| bufferUsageReportingInterval | entero positivo | 1000 | El número solicitado de milisegundos entre los eventos de uso del búfer de seguimiento de DevTools.  Por ejemplo, si es 1000, una vez por segundo, DevTools informa de lo lleno que está el búfer de seguimiento.  Si un informe indica que el uso del búfer es del 100%, se emite una advertencia. |  
| enableNetwork | booleano | true | Para recopilar eventos \(o no collect\) del dominio de red. |  
| enablePage | booleano | true | Para recopilar eventos \(o no collect\) del dominio page. |  
| traceCategories | string | \(empty\) | Una cadena separada por comas de categorías de seguimiento de Microsoft Edge para las que se deben recopilar eventos de seguimiento.  Una cadena no especificada o vacía deshabilita el seguimiento. |  

## Funcionalidades devueltas  

La siguiente lista contiene todas las funcionalidades específicas de Microsoft Edge que `EdgeDriver` se devuelven al crear una nueva sesión.  

| Funcionalidad | Tipo | Detalles |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | La versión de EdgeDriver. |  
| msedge.userDataDir | string | Ruta de acceso a la carpeta de datos de usuario usada por la instancia de Microsoft Edge. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Introducción a la depuración remota de dispositivos Windows 10 | Microsoft Docs"  
[WebdriverIndexChooseWebdriverLanguageBinding]: ./index.md#choose-a-webdriver-language-binding "Choose a WebDriver language binding - WebDriver (Chromium) | Microsoft Docs"
[WebdriverIndexAutomateMicrosoftEdgeChromium]: ./index.md#automate-microsoft-edge-chromium "Automatizar Microsoft Edge (Chromium) - WebDriver (Chromium) | Microsoft Docs"    
[WebdriverIndexInstallMicrosoftEdgeChromium]: ./index.md#install-microsoft-edge-chromium "Instalar Microsoft Edge (Chromium) - WebDriver (Chromium) | Microsoft Docs"  

[SeleniumMain]: https://www.selenium.dev "Automatización del explorador Se automationHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Capacidades compartidas | Documentación de Seyán"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver#capabilities "Funcionalidades: especificación de WebDriver | W3C"   

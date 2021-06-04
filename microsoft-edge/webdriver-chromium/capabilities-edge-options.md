---
description: Una referencia para las capacidades de WebDriver y Microsoft Edge opciones específicas admitidas por EdgeDriver (Chromium).
title: Funciones y EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: microsoft edge, desarrollo web, html, css, javascript, programador, webdriver, selenio, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: 5a48ca34e46b56fa60bcacfade2add23026be144
ms.sourcegitcommit: f95812c4e1b7277f67c6c4891be2779cc1b5bdf1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/18/2021
ms.locfileid: "11343782"
---
# Funciones y EdgeOptions  

Las funcionalidades son opciones que puede usar para personalizar y configurar una `EdgeDriver` sesión.  Para obtener información sobre cómo iniciar una nueva sesión, vaya a `EdgeDriver` [Automatizar Microsoft Edge][WebdriverIndexAutomateMicrosoftEdgeChromium].  En este artículo se describen todas las funcionalidades admitidas [Microsoft Edge][WebdriverIndexInstallMicrosoftEdgeChromium] detalles sobre cómo pasar las funciones a `EdgeDriver` las sesiones.  

Las funcionalidades se pasan a una sesión de WebDriver como un mapa JSON.  Los enlaces de idioma de WebDriver suelen proporcionar métodos de comodidad seguros para el tipo, por lo que no es necesario configurar el mapa JSON usted mismo.  Los diferentes enlaces de idioma de WebDriver usan diferentes mecanismos para configurar capacidades.  Vaya a la documentación del enlace [de idioma preferido][WebdriverIndexChooseWebdriverLanguageBinding] para obtener más información sobre cómo configurar las funcionalidades.  [Selenio][SeleniumMain] configura las capacidades a través de la `EdgeOptions` clase.  

##  <a name="using-the-edgeoptions-class"></a>Uso de la clase EdgeOptions  

Cree una instancia de `EdgeOptions` , que proporciona métodos de comodidad para establecer Microsoft Edge funcionalidades específicas.  Después de configurar el `EdgeOptions` objeto, pase `EdgeOptions` al `EdgeDriver` constructor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Para usar funcionalidades que no tienen un método de comodidad asociado, use el `AddAdditionalCapability` método.  Debe pasar el nombre completo de la funcionalidad y un valor con el tipo correcto.  Para revisar la lista completa de funcionalidades y tipos de valor aceptados, vaya al [objeto EdgeOptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

##  <a name="recognized-capabilities"></a>Capacidades reconocidas  

Para las funcionalidades estándar que acepta, navegue a la documentación `EdgeDriver` [de Selenium][SharedCapabilitiesSeleniumDocumentation] y al estándar [W3C WebDriver][CapabilitiesW3cWebdriver].  En este artículo solo se enumeran las funcionalidades específicas de Microsoft Edge.  

##  <a name="edgeoptions-object"></a>EdgeOptions (objeto)  

La mayoría Microsoft Edge funcionalidades específicas se exponen a través del `EdgeOptions` objeto.  En algunos idiomas, la clase implementa las `EdgeOptions` capacidades.  En otros idiomas, las capacidades se almacenan en el `ms:edgeOptions` diccionario en `DesiredCapabilities` .  

| Funcionalidad | Tipo | Valor predeterminado | Detalles |  
|:--- |:--- |:--- |:--- |  
| args | lista de cadenas |  | Lista de argumentos de línea de comandos que se deben usar al iniciar Microsoft Edge.  Los argumentos con un valor asociado deben estar separados por `=` un signo \(por ejemplo, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \). |  
| binario | string |  | Ruta de acceso al Microsoft Edge binario para usar \(en macOS, la ruta de acceso debe ser el binario real, no solo la aplicación.  por ejemplo, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \). |  
| debuggerAddress | string |  | Una dirección de un servidor depurador al que se va a conectar, en forma de `hostname/ip:port` , por ejemplo `127.0.0.1:38947` . |
| desasoy | booleano | `false` | Si , Microsoft Edge cierra cuando se cierra el servicio WebDriver, incluso si el extremo local de `false` WebDriver no ha cerrado la sesión.  Si `true` , Microsoft Edge solo se cierra si el extremo local de WebDriver cierra la sesión.  Si , y el extremo local de WebDriver no cierra la sesión, no limpia la carpeta de datos de usuario temporal que usa la instancia Microsoft Edge `true` `EdgeDriver` usuario. |  
| excludeSwitches | lista de cadenas |  | Lista de Microsoft Edge de línea de comandos para excluir que EdgeDriver pasa de forma predeterminada al iniciar Microsoft Edge.  Evite el `--` prefijo de los modificadores. |  
| extensiones | lista de cadenas |  | Una lista de extensiones que se instalarán en el inicio.  Cada elemento de la lista debe ser una extensión empaquetada codificada en base 64 \( `.crx` \). |  
| localState | diccionario |  | Diccionario con cada entrada que consta del nombre de la preferencia y el valor.  Las preferencias se aplican al archivo De estado local de la carpeta de datos del usuario. |  
| minidumpPath | string |  | Directorio para almacenar Microsoft Edge minidumps.  \(Compatible solo en Linux.\) |  
| mobileEmulation | diccionario |  | Diccionario con un valor para `deviceName` , o valores para y `deviceMetrics` `userAgent` . |  
| perfLoggingPrefs | diccionario |  | Diccionario opcional que especifica las preferencias de registro de rendimiento.  para obtener más información, vaya al [objeto perfLoggingPrefs](#perfloggingprefs-object). |  
| prefs | diccionario |  | Diccionario con cada entrada que consta del nombre de la preferencia y el valor.  Las preferencias solo se aplican al perfil de usuario en uso.  Por ejemplo, vaya al archivo de la carpeta de datos `Preferences` de usuario de Microsoft Edge. |  
| wdpAddress | string |  | Dirección de un servidor Windows Device Portal al que se conecta, en forma de `hostname/ip:port` , por ejemplo `127.0.0.1:50080` .  Para obtener más información, vaya a [Depuración remota: Windows 10 dispositivos][DevtoolsRemoteDebuggingWindows]. |  
| wdpPassword | string |  | Contraseña opcional para usar al conectarse a un servidor Windows Device Portal.  Obligatorio si el servidor tiene habilitada la autenticación. |  
| wdpUsername | string |  | Nombre de usuario opcional que se usará al conectarse a un servidor Windows Device Portal.  Obligatorio si el servidor tiene habilitada la autenticación. |  
| windowsApp | string |  | Id. de modelo de usuario de aplicación Microsoft Edge paquete de aplicación que se debe iniciar, por ejemplo `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` .  Se `windowsApp` usa en lugar de al `binary` conectarse a un Windows 10X o emulador mediante Windows Device Portal. |  
| windowTypes | lista de cadenas |  | Una lista de tipos de ventana que se muestran en la lista de identificadores de ventana.  Para obtener acceso a los elementos webview de Android, incluya `webview` en la lista. |  

##  <a name="perfloggingprefs-object"></a>perfLoggingPrefs (objeto)  

El `perfLoggingPrefs` diccionario tiene el siguiente formato \(todas las claves son opcionales\).  

| Tecla | Tipo | Valor predeterminado | Detalles |  
|:--- |:--- |:--- |:--- |  
| bufferUsageReportingInterval | entero positivo | 1000 | Número solicitado de milisegundos entre los eventos de uso del búfer de seguimiento de DevTools.  Por ejemplo, si es 1000, una vez por segundo, DevTools informa de lo lleno que está el búfer de seguimiento.  Si un informe indica que el uso del búfer es del 100 %, se emite una advertencia. |  
| enableNetwork | booleano | true | Para recopilar eventos \(o no recopilar\) del dominio de red. |  
| enablePage | booleano | true | Para recopilar eventos \(or not collect\) del dominio Page. |  
| traceCategories | string | \(empty\) | Una cadena separada por comas de Microsoft Edge de seguimiento para las que se deben recopilar los eventos de seguimiento.  Una cadena no especificada o vacía deshabilita el seguimiento. |  

##  <a name="returned-capabilities"></a>Capacidades devueltas  

La siguiente lista contiene todas las funciones Microsoft Edge específicas que `EdgeDriver` se devuelven al crear una nueva sesión.  

| Funcionalidad | Tipo | Detalles |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | La versión de EdgeDriver. |  
| msedge.userDataDir | string | Ruta de acceso a la carpeta de datos de usuario usada por la Microsoft Edge usuario. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Introducción a la depuración remota Windows 10 dispositivos | Microsoft Docs"  
[WebdriverIndexChooseWebdriverLanguageBinding]: ./index.md#choose-a-webdriver-language-binding "Elegir un enlace de idioma de WebDriver: WebDriver (Chromium) | Microsoft Docs"
[WebdriverIndexAutomateMicrosoftEdgeChromium]: ./index.md#automate-microsoft-edge-chromium "Automatizar Microsoft Edge (Chromium) - WebDriver (Chromium) | Microsoft Docs"    
[WebdriverIndexInstallMicrosoftEdgeChromium]: ./index.md#install-microsoft-edge-chromium "Instalar Microsoft Edge (Chromium) - WebDriver (Chromium) | Microsoft Docs"  

[SeleniumMain]: https://www.selenium.dev "Automatización del explorador SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Capacidades compartidas | Documentación de Selenio"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver#capabilities "Funcionalidades: especificación de WebDriver | W3C"   

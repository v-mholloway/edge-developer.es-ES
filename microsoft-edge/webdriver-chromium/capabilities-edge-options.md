---
description: Una referencia para las capacidades de Webdriver y las opciones específicas de Microsoft Edge compatibles con EdgeDriver (cromo).
title: Capacidades y EdgeOptions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, WebDrive, Selenium, pruebas, herramientas, automatización, prueba
ms.openlocfilehash: 1f6dca1b7ce3eb4fab3aaaab6450eee7cbf3eae5
ms.sourcegitcommit: 2e14ff82350f700d7eabc8d33b3ec3e5fc8c61fa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "11192261"
---
# Capacidades y EdgeOptions  

Las funciones son opciones que puede usar para personalizar y configurar una `EdgeDriver` sesión.  Para iniciar una `EdgeDriver` sesión, vaya a [conducir Microsoft Edge][DrivingEdgeWebDriverIndex].  En este artículo se documentan todas las capacidades admitidas para [Microsoft Edge][DownloadEdgeWebDriverIndex] y detalles adicionales para pasar las capacidades a una `EdgeDriver` sesión.  

Los enlaces de idioma de WebDrive proporcionan formas de pasar las funciones `EdgeDriver` .  El mecanismo exacto depende del [enlace de idioma que elija][ChooseLanguageBindingWebDriverIndex].  En [Selenium][SeleniumMain], las capacidades se proporcionan a través de la `EdgeOptions` clase.  

## Uso de la clase EdgeOptions  

Crear una instancia de `EdgeOptions` , que tiene métodos cómodos para configurar capacidades específicas de Microsoft Edge.  Una vez que haya configurado el `EdgeOptions` objeto, pase al `EdgeOptions` `EdgeDriver` constructor.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddExtensions("/path/to/extension.crx");
var driver = new EdgeDriver(options);
```  

Para las funciones que aún no tienen un método práctico, use el `AddAdditionalCapability` método.  Debe conocer el nombre de la capacidad y el tipo de valor que acepta.  Para revisar la lista completa, navegue hasta el [objeto EdgeOptions](#edgeoptions-object).  

```csharp
options.AddAdditionalCapability("wdpAddress", "remotehost:50080");
```  

## Capacidades reconocidas  

Para las capacidades estándar que `EdgeDriver` aceptan, navegue a la [documentación de Selenium][SharedCapabilitiesSeleniumDocumentation] y al [estándar Webdriver de W3C][CapabilitiesW3cWebdriver].  En este artículo solo se enumeran las capacidades específicas de Microsoft Edge.  

## Objeto EdgeOptions  

La mayoría de las capacidades específicas de Microsoft Edge se exponen a través del `EdgeOptions` objeto.  En algunos idiomas, la clase implementa las funciones `EdgeOptions` .  En otros idiomas, las capacidades se almacenan en el `ms:edgeOptions` Diccionario en `DesiredCapabilities` .  

| Funcionalidad | Tipo | Valor predeterminado | Detalles |  
|:--- |:--- |:--- |:--- |  
| EventArgs | lista de cadenas |  | Lista de los argumentos de la línea de comandos que se van a usar al iniciar Microsoft Edge.  Los argumentos con un valor asociado deberían estar separados por un `=` signo \ (por ejemplo, `['start-maximized', 'user-data-dir=/tmp/temp_profile']` \).  |  
| Binary | string |  | Ruta de acceso al binario de Microsoft Edge para usar \ (en macOS, la ruta de acceso debe ser el binario real, no solo la aplicación.  por ejemplo, `/Applications/Microsoft Edge.app/Contents/MacOS/Microsoft Edge` \).  |  
| prórroga | lista de cadenas |  | Una lista de extensiones para instalar al inicio.  Cada elemento de la lista debe ser una extensión empaquetada en base 64 \ ( `.crx` \).  |  
| localState | diccionario |  | Un diccionario con cada entrada con el nombre de la preferencia y su valor.  Las preferencias se aplican al archivo de estado local de la carpeta datos de usuario.  |  
| Prefs | diccionario |  | Un diccionario con cada entrada con el nombre de la preferencia y su valor.  Las preferencias solo se aplican al perfil de usuario en uso.  Para ver ejemplos, navegue hasta el `Preferences` archivo en el directorio de datos de usuario de Microsoft Edge.  |  
| prender | boolean | false | Si es falso, Microsoft Edge se cierra al `EdgeDriver` finalizar, tanto si la sesión se cierra como si no.  Si es true, Microsoft Edge solo se cierra si la sesión se cierra \ (o cerrada \).  **Nota**: si es verdadero y la sesión no se cierra, no `EdgeDriver` limpia el directorio de datos de usuario temporal que usa la instancia de Microsoft Edge.  |  
| debuggerAddress | string |  | Una dirección de un servidor de depuración al que conectarse, en forma de <hostname/IP: Port>, por ejemplo  `127.0.0.1:38947` .  |
| excludeSwitches | lista de cadenas |  | Lista de modificadores de la línea de comandos de Microsoft Edge para excluir que EdgeDriver pase de forma predeterminada al iniciar Microsoft Edge.  No anteponga modificadores `--` .  |  
| minidumpPath | string |  | Directorio para almacenar minivolcados de Microsoft Edge.  \ (Compatible solamente con Linux. \) |  
| mobileEmulation | diccionario |  | Un diccionario con un valor `deviceName` o valores para `deviceMetrics` y `userAgent` .  |  
| perfLoggingPrefs | diccionario |  | Un diccionario opcional que especifica las preferencias de registro de rendimiento.  para obtener más información, vaya al [objeto perfLoggingPrefs](#perfloggingprefs-object).  |  
| windowTypes | lista de cadenas |  | Una lista de los tipos de ventanas que se muestran en la lista de identificadores de ventana.  Para acceder a los elementos de WebView de Android, incluya `webview` en la lista.  |  
| wdpAddress | string |  | Dirección de un servidor de Windows Device portal al que se conecta, en forma de `hostname/ip:port` , por ejemplo,  `127.0.0.1:50080` .  Para obtener más información, vaya a [depuración remota-dispositivos con Windows 10][DevtoolsRemoteDebuggingWindows].  |  
| wdpUsername | string |  | Nombre de usuario opcional para usar al conectarse a un servidor de Windows Device portal.  Necesario si el servidor tiene habilitada la autenticación.  |  
| wdpPassword | string |  | Contraseña opcional que se usa al conectarse a un servidor de Windows Device portal.  Necesario si el servidor tiene habilitada la autenticación.  |  
| windowsApp | string |  | IDENTIFICADOR de modelo de usuario de la aplicación de un paquete de aplicación de Microsoft Edge para iniciarlo, por ejemplo `Microsoft.MicrosoftEdge.Stable_8wekyb3d8bbwe!MSEDGE` .  Use `windowsApp` en lugar de `binary` cuando se conecte a un dispositivo con Windows 10x o un emulador con Windows Device portal.  |  

## objeto perfLoggingPrefs  

El `perfLoggingPrefs` Diccionario tiene el siguiente formato \ (todas las teclas son opcionales \).  

| Tecla | Tipo | Valor predeterminado | Detalles |  
|:--- |:--- |:--- |:--- |  
| enableNetwork | booleano | true | Para recopilar \ (o no recopilar \) eventos del dominio de red.  |  
| enablePage | booleano | true | Para recopilar \ (o no recopilar \) eventos del dominio de la página.  |  
| traceCategories | string | \ (vacío \) | Una cadena separada por comas de categorías de seguimiento de Microsoft Edge para las que se deben recopilar eventos de seguimiento.  Una cadena sin especificar o vacía deshabilita el seguimiento.  |  
| bufferUsageReportingInterval | entero positivo | 1000 | Número de milisegundos solicitado entre los eventos de uso de búfer de seguimiento de DevTools.  Por ejemplo, si 1000, una vez por segundo, DevTools informa de cuánto está lleno el búfer de seguimiento.  Si un informe indica que el uso del búfer es de 100%, se emite una advertencia.  |  

## Capacidades devueltas  

La siguiente lista contiene todas las funciones específicas de Microsoft Edge que `EdgeDriver` se devuelven al crear una sesión nueva.  

| Funcionalidad | Tipo | Detalles |  
|:--- |:--- |:--- |  
| msedge.msedgedriverVersion | string | La versión de EdgeDriver. |  
| msedge.userDataDir | string | La ruta de acceso al directorio de datos de usuario que usa la instancia de Microsoft Edge. |  

<!-- links -->  

[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Introducción a la depuración remota dispositivos con Windows 10 | Microsoft docs"  
[DrivingEdgeWebDriverIndex]: ./index.md#driving-microsoft-edge-chromium "Conduciendo Microsoft Edge (cromo) | Microsoft docs"    
[DownloadEdgeWebDriverIndex]: ./index.md#install-microsoft-edge-chromium "Instalar Microsoft Edge (cromo) | Microsoft docs"  
[ChooseLanguageBindingWebDriverIndex]: ./index.md#choose-a-webdriver-language-binding "Elija un enlace de idioma WebDrive | Microsoft docs"

[SeleniumMain]: https://www.selenium.dev "Automatización de explorador SeleniumHQ"  
[SharedCapabilitiesSeleniumDocumentation]: https://www.selenium.dev/documentation/en/driver_idiosyncrasies/shared_capabilities/ "Capacidades compartidas | Documentación de Selenium"   

[CapabilitiesW3cWebdriver]: https://www.w3.org/TR/webdriver/#capabilities "Capacidades: especificación de Webdriver | RELATIVA"   

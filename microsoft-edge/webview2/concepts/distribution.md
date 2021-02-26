---
description: Opciones de distribución al liberar una aplicación con Microsoft Edge WebView2
title: Distribución de aplicaciones WebView2 de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: 14f252b0155beb6bfce0b01dc080900f2d3e57ee
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195169"
---
# Distribución de aplicaciones con WebView2  

Al distribuir la aplicación WebView2, asegúrate de que la plataforma web de copia de seguridad, [el tiempo de ejecución de WebView2][Webview2Installer], esté presente antes de iniciar la aplicación.  En este artículo se describe la instalación del tiempo de ejecución de WebView2 y se usan los dos modos de distribución para la aplicación WebView2: [Evergreen](#evergreen-distribution-mode) y [versión no editable](#fixed-version-distribution-mode).  

## Modo de distribución Evergreen  

> [!NOTE]
> El modo de distribución Evergreen es el recomendado para la mayoría de los desarrolladores.  

Garantiza que la aplicación aproveche las últimas características y actualizaciones de seguridad.  Tiene las siguientes características:  

*   La plataforma web subyacente \(tiempo de ejecución WebView2\) se actualiza automáticamente sin que tengas que hacer nada.  
*   Todas las aplicaciones con el modo de distribución Evergreen usan una copia compartida del tiempo de ejecución Evergreen WebView2, que ahorra espacio en disco.  
    
### Descripción del tiempo de ejecución de WebView2  

WebView2 es un tiempo de ejecución redistribuible y sirve como la plataforma web de respaldo para aplicaciones WebView2.  El concepto es similar a Visual C++ o las aplicaciones del tiempo de ejecución .NET para C++/.NET.  El tiempo de ejecución contiene archivos binarios modificados de Microsoft Edge \(Chromium\) que se ajustan y ponen a prueba para las aplicaciones.  Durante la instalación, el usuario no ve el tiempo de ejecución como un explorador visible.  Por ejemplo, un usuario no tiene acceso directo de escritorio del explorador ni una entrada de menú inicio.  

Durante el desarrollo y las pruebas, puedes usar cualquiera de las siguientes opciones como plataforma web de respaldo.  

*   Tiempo de ejecución de WebView2  
*   Cualquier canal de explorador de Insider \(no estable\) y Microsoft Edge \(Chromium\)  
    
En entornos de producción, debes asegurarte de que el tiempo de ejecución esté presente en los dispositivos de usuario antes de que se inicie la aplicación.  El canal estable de Microsoft Edge no está disponible para el uso de WebView2.  Esta decisión impide que las aplicaciones tomen una dependencia del explorador en la producción.

Hay varias razones para no tomar una dependencia en el explorador:  

*   No se puede garantizar que Microsoft Edge \(Chromium\) esté presente en todos los dispositivos de usuario.  Por ejemplo, es posible que los dispositivos desconectados de Windows Update o no administrados por Microsoft directamente \(una gran parte del mercado de empresa y educativo\) no tengan el explorador.  Permitir la distribución del tiempo de ejecución de WebView2 evita tener una dependencia en el explorador como requisito previo para las aplicaciones.  
*   Los exploradores y las aplicaciones se usan para diferentes situaciones, por lo que la dependencia de un explorador puede tener efectos secundarios no deseados en las aplicaciones.  Por ejemplo, los administradores de TI pueden controlar la versión del explorador para la compatibilidad interna del sitio web.  El tiempo de ejecución de WebView2 permite que las aplicaciones permanezcan siempre en Evergreen mientras se administran activamente las actualizaciones del explorador.  
*   A diferencia del explorador, el tiempo de ejecución se desarrolla y prueba para escenarios de aplicaciones y, en algunos casos, puede incluir correcciones de errores aún no disponibles en el explorador.  
    
Está previsto que el tiempo de ejecución Evergreen WebView2 venga en las próximas versiones de Windows,  pero hasta que esté disponible universalmente, implementa el tiempo de ejecución con tu aplicación de producción.  

### Implementación del tiempo de ejecución Evergreen WebView2  

Solo necesitas una instalación del tiempo de ejecución Evergreen WebView2 para todas las aplicaciones Evergreen del dispositivo.  Hay varias herramientas disponibles en la [página de descarga del tiempo de ejecución WebView2][Webview2Installer].  Las siguientes herramientas te ayudan a implementar el tiempo de ejecución Evergreen.  

*   El programa previo del tiempo de ejecución WebView2 es un instalador pequeño \(aproximadamente 2 MB\).  El programa previo del tiempo de ejecución WebView2 descarga e instala desde los servidores de Microsoft el tiempo de ejecución Evergreen que coincide con la arquitectura del dispositivo del usuario.  
*   Usa un vínculo para descargar mediante programación el programa previo.  
*   El instalador independiente del tiempo de ejecución WebView2 es un instalador completo que instala el tiempo de ejecución Evergreen WebView2 en entornos sin conexión.  
    
Actualmente, tanto el programa previo como el instalador independiente son solo compatibles con instalaciones por máquina, lo que requiere permisos elevados.  Si se ejecuta un instalador sin ellos, se pedirá al usuario que eleve los permisos.  

Usa los siguientes flujos de trabajo para asegurarte de que el tiempo de ejecución ya está instalado antes de iniciar la aplicación.  Puedes ajustar el flujo de trabajo en función de la situación.  Tienes un código de ejemplo disponible en el [repositorio de muestras][GitHubMicrosoftedgeWebView2samplesWebview2Deployment].  

#### Implementación solo en línea  

Si tienes un escenario de implementación solo en línea donde se puede asumir que los usuarios tienen acceso a Internet, sigue estos pasos.  

1.  Durante la configuración de la aplicación, asegúrate de que el tiempo de ejecución ya está instalado.  Para comprobarlo, completa una de las siguientes acciones.  
    *   Inspecciona si la clave de registro `pv (REG_SZ)` existe y no está `null` o vacía.  Busca `pv (REG_SZ)` en la siguiente ubicación.  
        
        En Windows de 64 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        En Windows de 32 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Ejecuta [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] y asegúrate de que `versionInfo` es `NULL`.  
1.  Si el tiempo de ejecución no está instalado, usa el vínculo para descargar mediante programación el programa previo.  
1.  Invoca el programa previo desde un proceso elevado o un símbolo del sistema con `MicrosoftEdgeWebview2Setup.exe /silent /install` para la instalación silenciosa.  
    
El flujo de trabajo anterior tiene las siguientes ventajas:  

*   Instala el tiempo de ejecución solo cuando sea necesario o cuando no necesites empaquetar instaladores.  
*   El programa previo detecta automáticamente la arquitectura del dispositivo e instala el tiempo de ejecución correspondiente.  
*   Instala el tiempo de ejecución de forma silenciosa.  
    
También puedes elegir empaquetar el programa previo con la aplicación en lugar de descargarlo a petición por medios de programación.  

#### Implementación sin conexión  

Si tienes un escenario de implementación sin conexión en el que la implementación de aplicaciones tiene que funcionar completamente sin conexión, sigue estos pasos.  

1.  Descarga el [instalador independiente][Webview2Installer].  
1.  En el instalador o el actualizador de la aplicación, incluye el instalador.  
1.  Durante la configuración de la aplicación, asegúrate de que el tiempo de ejecución ya está instalado.  Para comprobarlo, completa una de las siguientes acciones.  
    *   Inspecciona si la clave de registro `pv (REG_SZ)` existe y no está `null` o vacía.  Busca `pv (REG_SZ)` en la siguiente ubicación.  
        
        En Windows de 64 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        En Windows de 32 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Ejecuta [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] y asegúrate de que `versionInfo` es `NULL`.  
1.  Si el tiempo de ejecución no está instalado, ejecuta el instalador independiente.  Si deseas ejecutar una instalación silenciosa, ejecuta el instalador desde un proceso con privilegios elevados o copia y ejecuta el siguiente comando.  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### Mantener la compatibilidad en modo Evergreen  

La web está en constante evolución.  El tiempo de ejecución Evergreen WebView2 se mantiene actualizado para proporcionarte las últimas características y correcciones de seguridad.  Para garantizar que la aplicación sea compatible con la web, debes configurar la infraestructura de pruebas.  

Los canales de Microsoft Edge no estables \(Beta/Dev/Canary\) ofrecen una vista previa de las novedades del tiempo de ejecución de WebView2.  Al igual que lo harías si desarrollas sitios web para Microsoft Edge, debes poner a prueba la aplicación WebView2 con regularidad.  Prueba la aplicación WebView2 en uno de los canales no estables y actualiza tu aplicación o [informa de problemas][GithubMicrosoftedgeWebviewfeedback] si surgen. Normalmente, Dev y Beta son los canales recomendados.  Para ayudarte a decidir qué canal es el más adecuado, ve a [Información general de los canales de Microsoft Edge][DeployEdgeMicrosoftEdgeChannels].  Puedes descargar el canal de [Microsoft Edge][DownloadNonstableEdge] no estable en el entorno de pruebas y usar `regkey` o variables de entorno para indicar la preferencia del canal para la aplicación de prueba.  Para obtener más información, ve a [ CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  También puedes usar [WebDriver][HowtoWebdriver] para automatizar las pruebas de WebView2.

## Modo de distribución de versión no editable   

Para entornos restringidos con requisitos de compatibilidad estrictos, considera la posibilidad de usar el modo de distribución de versión no editable.  Elige y empaqueta una versión específica del tiempo de ejecución WebView2 con el modo de distribución de versión no editable.  Puedes especificar el tiempo de las actualizaciones en el tiempo de ejecución de la aplicación.  El modo de distribución de versión no editable no recibe actualizaciones automáticas. Planifica la actualización de la aplicación y el tiempo de ejecución.  

> [!NOTE] 
> El modo de distribución de versión no editable se denominaba anteriormente "bring-your-own".  

Para usar el modo de versión no editable, completa las siguientes acciones

1.  [Descarga][Webview2Installer] el paquete de versión no editable. 
1.  Descomprime el paquete con la línea de comandos `expand {path to the package} -F:* {path to the destination folder}` o con herramientas como WinRAR. No lo descomprimas con el Explorador de archivos, ya que puede que no genere la estructura de carpetas correcta.  
1.  Incluye los archivos binarios de versión no editable descomprimidos en el proyecto.  
1.  Indica la ruta de acceso a los archivos binarios de versión fija al crear el entorno WebView2.  
    *   En Win32 C/C++, puedes crear el entorno con la [función CreateCoreWebView2EnvironmentWithOptions.][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]  Usa el parámetro `browserExecutableFolder` para indicar la ruta de acceso a la carpeta que contiene `msedgewebview2.exe`.  
    *   Para .NET, puedes especificar el entorno con cualquiera de las siguientes opciones.  
        
        > [!NOTE]
        > Debes especificar el entorno antes de que la propiedad WebView2 `Source` entre en vigor.  
        
        *   Establece la propiedad `CreationProperties` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]/[WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\) en el elemento WebView2.  Usa el miembro `BrowserExecutableFolder` en la clase `CoreWebView2CreationProperties` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]/[WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\) para indicar la ruta de acceso a los archivos binarios de versión no editable.  
        *   Usa `EnsureCoreWebView2Async` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]/[WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\) para especificar el entorno.  Usa el parámetro `browserExecutableFolder` en [CoreWebView2Environment.CreateAsync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] para indicar la ruta de acceso a los archivos binarios de versión no editable.  
1.  Empaqueta y envía los archivos binarios de versión no editable con la aplicación.  Actualiza los archivos binarios según corresponda.  
    
### Problemas conocidos para la versión no editable   

En comparación con el tiempo de ejecución de Evergreen, la versión no editable no tiene un proceso de instalación, lo que hace que [Microsoft PlayReady][MicrosoftPlayReady] no funcione sin modificaciones.  Puedes mitigar el problema completando las siguientes acciones.  

1.  Busca la ruta de acceso en la que implementas el paquete de versión no editable en el dispositivo del usuario, como la siguiente ubicación.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Ejecuta los siguientes comandos en el dispositivo del usuario.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  PlayReady debería estar funcionando ahora en el dispositivo del usuario.  En la pestaña **Seguridad** de la carpeta **versión no editable**, debes incluir permisos para `ALL APPLICATION PACKAGES` y `ALL RESTRICTED APPLICATION PACKAGES`.  

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Permiso para PlayReady" lightbox="../media/play-ready-permission.png":::
        Permiso para PlayReady  
    :::image-end:::  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Descripción de las versiones de explorador y WebView2 | Microsoft Docs"  
[HowtoWebdriver]: ../howto/webdriver.md "Automatizar y probar WebView2 con WebDriver de Microsoft Edge | Microsoft Docs"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString - Globals | Microsoft Docs"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Información general sobre los canales de Microsoft Edge | Microsoft Docs"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "CreateAsync: clase Microsoft.Web.WebView2.Core.CoreWebView2Environment | Microsoft Docs"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "Clase EnsureCoreWebView2Async -Microsoft.Web.WebView2.Wpf.WebView2 | Microsoft Docs"  
[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "EnsureCoreWebView2Async: clase Microsoft.Web.WebView2.WinForms.WebView2 | Microsoft Docs"  
[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "Clase CoreWebView2CreationProperties- Microsoft.Web.WebView2.Wpf.CoreWebView2CreationProperties | Microsoft Docs"  
[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Clase Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "CreationProperties: clase Microsoft.Web.WebView2.Wpf.WebView2 | Microsoft Docs"  
[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Clase Microsoft.Web.WebView2.WinForms.WebView2 | Microsoft Docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Instalador WebView2 | Desarrollador de Microsoft"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView | GitHub"  

[GitHubMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "Implementación de WebView2: Muestras de MicrosoftEdge/WebView2 | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  

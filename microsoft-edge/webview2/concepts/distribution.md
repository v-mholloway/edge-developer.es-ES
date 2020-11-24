---
description: Opciones de distribución al publicar una aplicación con Microsoft Edge WebView2
title: Distribución de las aplicaciones de Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 0cbaaeade03feac766647c55bb5edabfe8e8456e
ms.sourcegitcommit: 7b16c3e6eb458e0b2458279c2498597fb227bc8c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2020
ms.locfileid: "11182912"
---
# Distribución de aplicaciones con WebView2  

Al distribuir tu aplicación de WebView2, asegúrate de que la plataforma web de respaldo, el [tiempo de ejecución de WebView2][Webview2Installer], esté presente antes de que se inicie la aplicación.  En este artículo se describe cómo \ (el desarrollador \) Instale el tiempo de ejecución de WebView2 y use los dos modos de distribución para su aplicación de WebView2:  [hoja perenne](#evergreen-distribution-mode) y [versión corregida](#fixed-version-distribution-mode).  

## Modo de distribución de hoja perenne  

> [!NOTE]
> Se recomienda el modo de distribución de hoja perenne para la mayoría de los programadores.  

El modo de distribución de hoja perenne garantiza que tu aplicación esté aprovechando las últimas características y actualizaciones de seguridad.  Tiene las siguientes características:  

*   La plataforma web subyacente \ (WebView2 Runtime \) se actualiza automáticamente sin más esfuerzo por ti.  
*   Todas las aplicaciones que usan el modo de distribución de hoja perenne usan una copia compartida del Runtime de WebView2 de perenne, que ahorra espacio en disco.  
    
### Descripción del tiempo de ejecución de WebView2  

El tiempo de ejecución de WebView2 es un Runtime redistribuible y actúa como la plataforma web de respaldo para las aplicaciones de WebView2.  El concepto es similar a Visual C++ o a .NET Runtime para aplicaciones de/.NET de C++.  El Runtime contiene binarios modificados de Microsoft Edge \ (cromo \) que se han optimizado y probado para las aplicaciones.  El motor en tiempo de ejecución no aparece como un explorador visible para el usuario después de la instalación.  Por ejemplo, un usuario no tiene un acceso directo al escritorio del explorador ni una entrada del menú Inicio.  

Durante el desarrollo y las pruebas, puedes usar cualquiera de las dos plataformas web de respaldo.  

*   El tiempo de ejecución de WebView2  
*   Cualquier Insider \ (no estable \) canal de navegador Microsoft Edge \ (cromo \)  
    
En entornos de producción, debes asegurarte de que el tiempo de ejecución esté presente en los dispositivos de usuario antes de que se inicie la aplicación.  El canal estable de Microsoft Edge no está disponible para uso de WebView2.  La decisión evita que las aplicaciones tomen una dependencia en el explorador en producción.

No tome ninguna dependencia en el explorador porque:  

*   No se garantiza que Microsoft Edge \ (cromo \) esté presente en todos los dispositivos de usuario.  Por ejemplo, los dispositivos desconectados de Windows Update o no administrados por Microsoft directamente \ (una gran parte de la empresa y del mercado EDU \) pueden no tener el explorador.  Le permite distribuir el tiempo de ejecución de WebView2 evita tener una dependencia en el explorador como requisito previo para las aplicaciones.  
*   Los exploradores y las aplicaciones tienen diferentes casos de uso, por lo que tomar una dependencia en un explorador puede tener efectos secundarios no deseados en las aplicaciones.  Por ejemplo, los administradores de TI pueden controlar el control de versiones del explorador para la compatibilidad con sitios Web internos.  El tiempo de ejecución de WebView2 permite que las aplicaciones permanezcan perennes mientras se administran activamente las actualizaciones del explorador.  
*   A diferencia del explorador, el motor en tiempo de ejecución se desarrolla y se prueba para escenarios de aplicaciones y, en algunos casos, puede incluir correcciones de errores que aún no estén disponibles en el explorador.  
    
En el futuro, el tiempo de ejecución de WebView2 de perennes planea enviarse con versiones futuras de Windows.  Implemente el motor en tiempo de ejecución con la aplicación de producción hasta que el tiempo de ejecución esté más disponible universalmente.  

### Implementar el tiempo de ejecución de WebView2 de hoja perenne  

Solo se necesita una instalación del tiempo de ejecución de WebView2 de perenne para todas las aplicaciones de hoja perenne del dispositivo.  Hay varias herramientas disponibles en la [Página de descarga en tiempo de ejecución de WebView2][Webview2Installer].  Las siguientes herramientas le ayudan a implementar el tiempo de ejecución de perenne.  

*   El programa previo en tiempo de ejecución de WebView2 es un pequeño \ (aproximadamente 2 MB \) instalador.  El programa de arranque en tiempo de ejecución de WebView2 descarga e instala el tiempo de ejecución de perenne de servidores de Microsoft que coincide con la arquitectura de dispositivo del usuario.  
*   Use un vínculo para descargar el programa previo mediante programación.  
*   El instalador independiente de tiempo de ejecución de WebView2 es un instalador completo que instala el tiempo de ejecución de WebView2 de perennes en entornos sin conexión.  
    
En la actualidad, el programa previo y el instalador independiente solo admiten instalaciones por máquina, que requieren elevación.  Si se ejecuta un instalador sin elevación, se pide al usuario que eleve los permisos.  

Usa los siguientes flujos de trabajo para asegurarte de que el tiempo de ejecución ya esté instalado antes de que se inicie la aplicación.  Puede ajustar el flujo de trabajo en función de su escenario.  El código de ejemplo está disponible en el [repositorio de ejemplos][GitHubMicrosoftedgeWebView2samplesWebview2Deployment].  

#### Implementación solo en línea  

Si tiene un escenario de implementación solo en línea donde se supone que los usuarios tienen acceso a Internet, complete los pasos siguientes.  

1.  Durante la configuración de la aplicación, asegúrate de que el tiempo de ejecución ya esté instalado.  Para comprobarlo, complete una de las siguientes acciones.  
    *   Compruebe si la `pv (REG_SZ)` clave de clave existe y no está `null` o está vacía.  Busque  `pv (REG_SZ)` en la siguiente ubicación.  
        
        En Windows de 64 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        En Windows de 32 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Ejecute [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] y asegúrese de que `versionInfo` es `NULL` .  
1.  Si el motor en tiempo de ejecución no está instalado, usa el vínculo para descargar el programa previo mediante programación.  
1.  Invocar el programa previo desde un proceso o símbolo del sistema elevado con `MicrosoftEdgeWebview2Setup.exe /silent /install` para la instalación silenciosa.  
    
El flujo de trabajo anterior tiene las siguientes ventajas.  

*   Instale el motor en tiempo de ejecución solo cuando sea necesario o cuando no necesite empaquetar instaladores.  
*   El programa previo detecta automáticamente la arquitectura del dispositivo e instala el tiempo de ejecución correspondiente.  
*   Instalar el motor en tiempo de ejecución silenciosamente.  
    
También puedes optar por empaquetar el arranque con la aplicación en lugar de descargarlo mediante programación a petición.  

#### Implementación sin conexión  

Si tiene un escenario de implementación sin conexión en el que la implementación de aplicaciones debe funcionar completamente sin conexión, complete los siguientes pasos.  

1.  Descargue el [instalador independiente][Webview2Installer].  
1.  Incluya el instalador en el instalador de la aplicación o en el actualizador.  
1.  Durante la configuración de la aplicación, asegúrate de que el tiempo de ejecución ya esté instalado.  Para comprobarlo, complete una de las siguientes acciones.  
    *   Compruebe si la `pv (REG_SZ)` clave de clave existe y no está `null` o está vacía.  Busque  `pv (REG_SZ)` en la siguiente ubicación.  
        
        En Windows de 64 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        En Windows de 32 bits  
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Ejecute [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] y asegúrese de que `versionInfo` es `NULL` .  
1.  Si el motor en tiempo de ejecución no está instalado, ejecute el instalador independiente.  Si desea ejecutar una instalación silenciosa, ejecute el instalador desde un proceso elevado o copie y ejecute el siguiente comando.  
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  
    
### Mantente en el modo de hoja perenne  

La web está evolucionando constantemente.  El tiempo de ejecución de WebView2 perenne se mantiene actualizado para proporcionarte las últimas características y correcciones de seguridad.  Para asegurarte de que tu aplicación siga siendo compatible con la web, deberías configurar la infraestructura de prueba.  

Canales de Microsoft Edge no stable \ (beta/dev/Canarias \) brindan una ojeada a lo que viene próximamente en WebView2 Runtime.  Al igual que en el desarrollo de sitios web para Microsoft Edge, deberías probar tu aplicación de WebView2 regularmente.  Prueba tu aplicación de WebView2 en uno de los canales no estables y actualiza la aplicación o [informa de problemas][GithubMicrosoftedgeWebviewfeedback] si surgen problemas. Por lo general, el desarrollo y la versión beta son los canales recomendados.  Para ayudarle a decidir cuál es el canal adecuado, vaya a [información general de los canales de Microsoft Edge][DeployEdgeMicrosoftEdgeChannels].  Puede descargar el [canal de Microsoft Edge no estable][DownloadNonstableEdge] en su entorno de prueba, y usar `regkey` variables de entorno o para indicar la preferencia de canal para su aplicación de pruebas.  Para obtener más información, vaya a [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  También puede usar [Webdriver][HowtoWebdriver] para automatizar las pruebas de WebView2.

## Modo de distribución de versiones fijas   

Para entornos restringidos con requisitos de compatibilidad estrictos, considere la posibilidad de usar el modo de distribución de versiones fijas.  Elija y empaquete una versión específica del tiempo de ejecución de WebView2 usando el modo de distribución de versiones fijas.  Puede especificar los intervalos de actualizaciones de tiempo de ejecución para la aplicación.  El modo de distribución de versiones fijo no recibe actualizaciones automáticas. Planear la actualización de la aplicación y el motor en tiempo de ejecución.  

> [!NOTE] 
> El modo de distribución de versiones fijas se llamaba previamente.  

Para usar el modo de versión corregido, complete las siguientes acciones:

1.  [Descargue][Webview2Installer] el paquete de versión fijo. 
1.  Descomprima el paquete con la línea de comandos `expand {path to the package} -F:* {path to the destination folder}` o con herramientas como Winrar. Evite descomprimir a través del explorador de archivos porque no puede generar la estructura de carpetas correcta.  
1.  Incluya los binarios de la versión fija descomprimidos en el proyecto.  
1.  Indique la ruta de acceso a los binarios de la versión fija al crear el entorno de WebView2.  
    *   Para Win32 C/C++, puede crear el entorno mediante la función [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions] .  Use el `browserExecutableFolder` parámetro para indicar la ruta de acceso a la carpeta que contiene `msedgewebview2.exe` .  
    *   En el caso de .NET, puede realizar una de las siguientes opciones para especificar el entorno.  
        
        > [!NOTE]
        > Debe especificar el entorno antes de que la `Source` propiedad WebView2 surta efecto.  
        
        *   Establezca la `CreationProperties` propiedad \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\) en el elemento WebView2.  Use el `BrowserExecutableFolder` miembro de la `CoreWebView2CreationProperties` clase \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\) para indicar la ruta de acceso a los binarios de la versión fija.  
        *   Use `EnsureCoreWebView2Async` \ ([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\) para especificar el entorno.  Use el `browserExecutableFolder` parámetro de [CoreWebView2Environment. CreateAsync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] para indicar la ruta de acceso a los binarios de la versión fija.  
1.  Empaqueta y envía los binarios de la versión fija con la aplicación.  Actualice los archivos binarios según corresponda.  
    
### Problemas conocidos de la versión fija  

En comparación con el tiempo de ejecución de hoja perenne, la versión corregida no tiene un proceso de instalación, lo que hace que [Microsoft PlayReady][MicrosoftPlayReady] no funcione sin modificaciones.  Puede mitigar el problema completando las siguientes acciones.  

1.  Ubique la ruta de acceso en la que va a implementar el paquete de versión fijo en el dispositivo del usuario, como la siguiente ubicación.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Ejecute los siguientes comandos en el dispositivo del usuario.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  PlayReady debería funcionar ahora en el dispositivo del usuario.  En la pestaña **seguridad** de la carpeta **versión fija** , debe incluir permisos para `ALL APPLICATION PACKAGES` y `ALL RESTRICTED APPLICATION PACKAGES` .  

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Permiso para PlayReady" lightbox="../media/play-ready-permission.png":::
        Permiso para PlayReady  
    :::image-end:::  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Descripción de las versiones de explorador y WebView2 | Microsoft docs"  
[HowtoWebdriver]: ../howto/webdriver.md "Automatizar y probar WebView2 con el controlador Microsoft Edge | Microsoft docs"  

[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Microsoft docs"  

[DeployEdgeMicrosoftEdgeChannels]: /deployedge/microsoft-edge-channels "Información general de los canales de Microsoft Edge | Microsoft docs"  

[ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.createasync "CreateAsync-Microsoft. Web. WebView2. Core. CoreWebView2Environment (clase) | Microsoft docs"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.wpf.webview2.ensurecorewebview2async "EnsureCoreWebView2Async-Microsoft. Web. WebView2. WPF. WebView2 (clase) | Microsoft docs"  
[ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "EnsureCoreWebView2Async-Microsoft. Web. WebView2. WinForms. WebView2 (clase) | Microsoft docs"  
[ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties "CoreWebView2CreationProperties-Microsoft. Web. WebView2. WPF. CoreWebView2CreationProperties (clase) | Microsoft docs"  
[ReferenceWinFormsMicrosoftWebWebview2WinForms]: /dotnet/api/microsoft.web.webview2.winforms "Clase Microsoft. Web. WebView2. WinForms | Microsoft docs"  
[ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties]: /dotnet/api/microsoft.web.webview2.wpf.webview2.creationproperties "CreationProperties-Microsoft. Web. WebView2. WPF. WebView2 (clase) | Microsoft docs"  
[ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Clase Microsoft. Web. WebView2. WinForms. WebView2 | Microsoft docs"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 Installer | Microsoft Developer"  

[DownloadNonstableEdge]: https://www.microsoftedgeinsider.com/download "Descargar los canales de Insider de Microsoft Edge"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView | GitHub"  

[GitHubMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "Implementación de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  

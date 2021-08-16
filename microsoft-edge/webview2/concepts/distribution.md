---
description: Opciones de distribución al liberar una aplicación con Microsoft Edge WebView2
title: Distribuir una aplicación WebView2 y El tiempo de ejecución de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/03/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: f36f12d439c71838dac5add94055dd1ae739c094
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11893676"
---
# <a name="distribute-a-webview2-app-and-the-webview2-runtime"></a>Distribuir una aplicación WebView2 y El tiempo de ejecución de WebView2

Una aplicación WebView2 depende del tiempo de ejecución de WebView2 en los equipos cliente.  Cuando distribuyas la aplicación WebView2, debes tener en cuenta cómo se distribuye WebView2 Runtime y cómo se actualiza en los equipos cliente.


## <a name="introduction-to-the-runtime-evergreen-distribution-and-fixed-version-distribution"></a>Introducción a la distribución runtime, evergreen y fixed version

### <a name="the-webview2-runtime"></a>Tiempo de ejecución de WebView2

WebView2 Runtime es un tiempo de ejecución redistribuible y sirve como la plataforma web subyacente (o de _respaldo)_ para aplicaciones webView2.  El concepto es similar a Visual C++ o las aplicaciones del tiempo de ejecución .NET para C++/.NET.  El tiempo de ejecución de WebView2 contiene archivos binarios Microsoft Edge \(Chromium\) modificados que se afinan y prueban para aplicaciones WebView2.  Después de instalar WebView2 Runtime, no aparece como una aplicación de explorador visible para el usuario.  Por ejemplo, un usuario no tiene un acceso directo de escritorio del explorador ni una entrada en el **menú** Inicio.

Hay dos formas diferentes de distribuir y actualizar WebView2 Runtime a las máquinas cliente: el modo de distribución Evergreen y el modo de distribución versión fija.

### <a name="the-evergreen-runtime-distribution-mode"></a>Modo de distribución de Evergreen Runtime

En el modo de distribución _Evergreen,_ WebView2 Runtime no se empaqueta con la aplicación, sino que se instala inicialmente en clientes mediante un arranque en línea o un instalador sin conexión.  Después, El tiempo de ejecución de WebView2 se actualiza automáticamente en los equipos cliente.  A continuación, puede distribuir actualizaciones de la aplicación WebView2 que usan las API webview2 más recientes desde el SDK de WebView2 más reciente.  El modo de distribución Evergreen es el recomendado para la mayoría de los desarrolladores.

Profesionales:
*  La plataforma web subyacente (WebView2 Runtime) se actualiza automáticamente sin más esfuerzo.
*  Se requiere menos espacio en disco para El tiempo de ejecución de WebView2 en sistemas cliente, ya que El tiempo de ejecución de WebView2 es compartido por todas las aplicaciones de WebView2 que están en el cliente.
*  En los sistemas elegibles, los archivos binarios de Microsoft Edge y Evergreen WebView2 Runtime se vinculan de forma permanente cuando están en la misma versión.  Esta vinculación proporciona ventajas para la superficie del disco, la memoria y el rendimiento.

Contras:
*  La aplicación WebView2 no puede especificar que sea necesaria una versión determinada de WebView2 Runtime.

### <a name="the-fixed-version-runtime-distribution-mode"></a>Modo de distribución en tiempo de ejecución de versión fija

En el _modo de distribución Versión_ fija, descargas una versión específica de WebView2 Runtime y la empaquetas junto con la aplicación WebView2 en el paquete de la aplicación.  WebView2 Runtime que empaquetas con la aplicación solo la usa la aplicación WebView2, no otras aplicaciones del equipo del cliente.

Profesionales:
*  Tiene más control sobre el control de versiones de WebView2 Runtime.  Sabes qué API de WebView2 están disponibles para la aplicación, ya que controlas qué versión de WebView2 Runtime está disponible para la aplicación.  La aplicación no necesita probar si las API más recientes están presentes.

Contras:
*  You need to manage the WebView2 Runtime yourself.  El tiempo de ejecución de WebView2 no se actualiza automáticamente en los clientes, por lo que para usar las API webView2 más recientes, debe actualizar periódicamente la aplicación junto con el tiempo de ejecución actualizado de WebView2.
*  Se requiere más espacio en disco en el cliente, si hay varias aplicaciones de WebView2 instaladas.
*  El tiempo de ejecución de la versión fija no se puede instalar mediante un instalador.


## <a name="understanding-the-options-at-the-runtime-download-page"></a>Descripción de las opciones en la página de descarga en tiempo de ejecución

La [sección Descargar WebView2 Runtime][Webview2Installer] de la página Microsoft Edge **WebView2** proporciona varias opciones para distribuir WebView2 Runtime a máquinas cliente.  Comprender las opciones de esta página proporciona una buena introducción, para ayudar a decidir qué enfoque desea usar.

:::image type="complex" source="../media/runtime-distrib-options.png" alt-text="Opciones para distribuir y actualizar WebView2 Runtime" lightbox="../media/runtime-distrib-options.png":::
    Opciones para distribuir y actualizar WebView2 Runtime
:::image-end:::

*   La **sección Evergreen Bootstrapper** de la página proporciona un pequeño arranque de Evergreen Runtime que se ejecuta en el equipo cliente, para los usuarios en línea.  El arranque descarga e instala el tiempo de ejecución de WebView2 Evergreen adecuado en el cliente.  Puede usar el arranque de un par de maneras diferentes:

    *   Vincular al arranque, mediante un vínculo que se obtiene del **botón Obtener el** vínculo.  La aplicación usa este vínculo para descargar mediante programación el arranque en el cliente e invocar el arranque.  Este enfoque evita la necesidad de empaquetar el arranque con la aplicación.  Este enfoque depende de la Content Delivery Network de Microsoft (CDN), para obtener el arranque.

    *   Descargue el arranque (con el **botón Descargar** de la sección **Bootstrapper)** y, a continuación, distribuya el arranque con la aplicación.  En este enfoque, empaquetas el arranque con el instalador/actualizador de la aplicación o con la propia aplicación e invocas el arranque que has incluido con la aplicación.  Este enfoque evita la dependencia de microsoft CDN, para obtener el arranque.

*  La **sección Instalador independiente de Evergreen** de la página proporciona un instalador de Evergreen grande e independiente, principalmente para usuarios sin conexión.  En este enfoque, empaquetas el instalador independiente con el instalador/actualizador o la propia aplicación e invocas al instalador de Evergreen Standalone.  Este enfoque evita la dependencia de microsoft CDN, para obtener el tiempo de ejecución.

*  La **sección Versión fija** de la página proporciona un tiempo de ejecución de versión fija, que es una versión específica del tiempo de ejecución de WebView2 que se distribuye junto con la aplicación.

El modo de distribución Evergreen se recomienda para la mayoría de las aplicaciones.


<!-- ====================================================================== -->
## <a name="details-about-the-webview2-runtime"></a>Detalles sobre El tiempo de ejecución de WebView2

Al distribuir la aplicación WebView2, asegúrese de que WebView2 Runtime está presente en el equipo cliente.  Este requisito se aplica a los modos de distribución Evergreen y Fixed Version.

Si desea usar el modo de distribución versión [fija,](#details-about-the-fixed-version-runtime-distribution-mode)puede omitir el par de secciones siguientes y navegar a Detalles sobre el modo de distribución en tiempo de ejecución de versión fija .

### <a name="runtime-or-browser-support-during-development-or-production"></a>Compatibilidad con tiempo de ejecución o explorador durante el desarrollo o la producción

Durante el desarrollo y las pruebas, una aplicación WebView2 puede usar cualquiera de las dos opciones como plataforma web de respaldo:
*   Tiempo de ejecución de WebView2.  El tiempo de ejecución generalmente proporciona las mismas capacidades de plataforma web y la cadencia de actualización que el canal estable del explorador Microsoft Edge web.  Use El tiempo de ejecución de WebView2 en un entorno de producción o para desarrollar y probar con la plataforma web que tienen los usuarios en la actualidad.
*   Una vista previa (Insider) Microsoft Edge canal del explorador \(Chromium\).  Estos Microsoft Edge de vista previa son Beta, Dev y Canary.  Usa este enfoque para probar la compatibilidad con avances de la aplicación, de modo que sepas si se está llegando a un cambio importante que requerirá actualizar la aplicación.  Para obtener más información, vaya a Cambiar a un canal de vista previa para probar las [próximas API y características](../how-to/set-preview-channel.md).

Una versión de producción de una aplicación WebView2 solo puede usar WebView2 Runtime como plataforma web de copia de seguridad, no Microsoft Edge.

#### <a name="microsoft-edge-stable-channel-isnt-supported-for-webview2"></a>Microsoft Edge El canal estable no es compatible con WebView2

Las aplicaciones webView2 no pueden usar el canal estable de Microsoft Edge como plataforma web de respaldo.  Esta restricción impide que una versión de producción de una aplicación WebView2 tome una dependencia en el explorador.  Una aplicación WebView2 no puede tener una dependencia en el explorador durante la producción, por los siguientes motivos.

*   Microsoft Edge \(Chromium\) no se garantiza que esté presente en todos los dispositivos de usuario.  Muchos dispositivos en empresas y en educación están desconectados de Windows Update o no son administrados por Microsoft directamente.  Es posible que estos dispositivos no Microsoft Edge instalados.  Requerir que la versión de producción de las aplicaciones webView2 use El tiempo de ejecución de WebView2 en lugar de Microsoft Edge evita convertir Microsoft Edge en un requisito previo para ejecutar una aplicación WebView2.

*   Los exploradores y las aplicaciones tienen diferentes casos de uso.  Si una aplicación WebView2 requiere la presencia de Microsoft Edge en el cliente, esto podría tener efectos secundarios no deseados en la aplicación WebView2.  Por ejemplo, un administrador de TI puede impedir que el explorador se actualice desde una versión específica, para mantener el explorador compatible con un sitio web interno.  Requerir que la versión de producción de una aplicación WebView2 use El tiempo de ejecución de WebView2 en lugar del explorador permite que la aplicación WebView2 permanezca siempre verde incluso si el administrador de los clientes impide las actualizaciones del explorador.

*   A diferencia del explorador, WebView2 Runtime se desarrolla y prueba en escenarios de aplicaciones y, en algunos casos, El tiempo de ejecución de WebView2 puede incluir correcciones de errores que aún no están disponibles en el explorador.  
    
Evergreen WebView2 Runtime se incluirá como parte del sistema operativo Windows 11. Varias aplicaciones webView2 han instalado Evergreen Runtime en dispositivos con un sistema operativo antes de Windows 11.  Sin embargo, es posible que algunos dispositivos no tengan el tiempo de ejecución preinstalado, por lo que es una buena práctica comprobar si el tiempo de ejecución está presente en el cliente.

Antes de que la aplicación cree un WebView2, la aplicación debe comprobar si el tiempo de ejecución de WebView2 está presente (ya sea comprobando una clave del Registro o llamando a una API) e instalar el tiempo de ejecución si falta.  La aplicación puede hacer esta comprobación al instalar o actualizar la aplicación (recomendado) o en tiempo de ejecución de la aplicación.  Para comprobar si el tiempo de ejecución está presente, vaya [a Deploying the Evergreen WebView2 Runtime below.](#deploying-the-evergreen-webview2-runtime)


<!-- ====================================================================== -->
## <a name="details-about-the-evergreen-runtime-distribution-mode"></a>Detalles sobre el modo de distribución de Evergreen Runtime

El modo de distribución Evergreen garantiza que la aplicación WebView2 aproveche las últimas características y actualizaciones de seguridad de WebView2.  El modo de distribución Evergreen tiene las siguientes características:

*  WebView2 Runtime se actualiza automáticamente sin más esfuerzo.
*  Todas las aplicaciones WebView2 que usan el modo de distribución Evergreen usan una copia compartida de Evergreen WebView2 Runtime, que ahorra espacio en disco.
*  En los sistemas elegibles, los archivos binarios de Microsoft Edge y Evergreen WebView2 Runtime se vinculan de forma permanente cuando están en la misma versión.  Esta vinculación proporciona ventajas para la superficie del disco, la memoria y el rendimiento.

Al usar el modo de distribución Evergreen de WebView2 Runtime, la aplicación WebView2 supone que los clientes tienen el tiempo de ejecución más reciente.  La aplicación no puede requerir una versión determinada de WebView2 Runtime para todas las aplicaciones del cliente.  Cuando se lanza un nuevo paquete del SDK de WebView2, ya se ha distribuido a los clientes una versión compatible de WebView2 Runtime.  Por lo tanto, está bien que la aplicación WebView2 use las API que están en la versión más reciente del SDK de WebView2.

Para obtener más información, vaya a [Understanding browser versions y WebView2][ConceptsVersioning].

### <a name="deploying-the-evergreen-webview2-runtime"></a>Implementación del tiempo de ejecución Evergreen WebView2

Solo necesitas una instalación del tiempo de ejecución Evergreen WebView2 para todas las aplicaciones Evergreen del dispositivo.  Hay varias herramientas disponibles en [Download the WebView2 Runtime][Webview2Installer] para ayudarle a implementar Evergreen Runtime.

*   Para clientes en línea: _WebView2 Runtime Bootstrapper_ es un instalador pequeño \(aproximadamente 2 MB\).  El Bootstrapper de Tiempo de ejecución de WebView2 descarga e instala Evergreen Runtime desde servidores microsoft que coinciden con la arquitectura del dispositivo del usuario.
    *   En la parte de configuración de la aplicación WebView2, vincula al programa de arranque.  Usar un vínculo para descargar mediante programación el arranque; seleccione el **botón Obtener el vínculo** en la página de descarga anterior.
    *   O bien, descarga el arranque y empaquetalo con la aplicación WebView2.

*   Para clientes sin conexión: _WebView2 Runtime Standalone Installer_ es un instalador completo que instala Evergreen WebView2 Runtime en entornos sin conexión.
    
Actualmente, tanto el programa de arranque como el instalador independiente solo admiten instalaciones por máquina, lo que requiere la elevación de permisos.  Si se ejecuta un instalador sin ellos, se pedirá al usuario que eleve los permisos.  

Usa el siguiente flujo de trabajo de implementación en línea o flujo de trabajo de implementación sin conexión para asegurarte de que el tiempo de ejecución ya está instalado antes de que se inicie la aplicación.  Puede ajustar el flujo de trabajo en función del escenario.  Tienes un código de ejemplo disponible en el [repositorio de muestras][GitHubMicrosoftedgeWebView2samplesWebview2Deployment].  

#### <a name="online-only-deployment"></a>Implementación solo en línea  

Si tiene un escenario de implementación solo en línea donde se supone que los usuarios tienen acceso a Internet, use el siguiente flujo de trabajo.

1.  Durante la instalación de la aplicación, ejecute una prueba para asegurarse de que El tiempo de ejecución de WebView2 ya está instalado.  Para comprobar que el tiempo de ejecución está instalado, use uno de los siguientes métodos:

    *   Inspeccione la `pv (REG_SZ)` clave del Registro para WebView2 Runtime en la siguiente ubicación.  Si esta clave de registro no existe, o si existe y es o una cadena vacía, significa que webView2 Runtime no está instalado `null` en el cliente.  Use esta clave de registro para detectar si el tiempo de ejecución de WebView2 está instalado y para obtener la versión de WebView2 Runtime.  Busque `pv (REG_SZ)` en la siguiente ubicación.  
        
        En 64 bits Windows:
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```
        
        En 32 bits Windows:
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Como alternativa, ejecute [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] y evalúe si `versionInfo` es `NULL` .  `NULL` indica que el tiempo de ejecución no está instalado.

1.  Si el tiempo de ejecución no está instalado, en el **** proceso de configuración de la aplicación, usa el vínculo (desde el botón Obtener el vínculo en la página de descarga) para descargar mediante programación el Arranque en tiempo de ejecución de WebView2.

1.  Invoque el Arranque en tiempo de ejecución de WebView2 desde un proceso o símbolo del sistema con privilegios elevados emitiendo el comando `MicrosoftEdgeWebview2Setup.exe /silent /install` .
    
El flujo de trabajo anterior tiene varias ventajas:
*   El tiempo de ejecución solo se instala cuando es necesario.
*   No es necesario empaquetar un instalador en tiempo de ejecución con la aplicación WebView2.
*   El arranque de Tiempo de ejecución de WebView2 detecta automáticamente la arquitectura (plataforma) del dispositivo y, a continuación, instala el tiempo de ejecución de WebView2 correspondiente.
*   El tiempo de ejecución se instala de forma silenciosa.  
    
Como alternativa, en lugar de descargar mediante programación el arranque a petición obteniendo un vínculo, como se muestra anteriormente, puedes empaquetar el Bootstrapper de Evergreen para WebView2 Runtime con la aplicación.

#### <a name="offline-deployment"></a>Implementación sin conexión  

Si tienes un escenario de implementación sin conexión, donde la implementación de aplicaciones tiene que funcionar completamente sin conexión, usa el siguiente flujo de trabajo.

1.  Descargue el Instalador independiente de Evergreen [de Descargar WebView2 Runtime][Webview2Installer] en el equipo de desarrollo.  El instalador independiente de Evergreen instala WebView2 Evergreen Runtime en el cliente.

1.  Incluye el Instalador independiente de Evergreen en el instalador o actualizador de la aplicación.  

1.  Durante la instalación de la aplicación, compruebe si WebView2 Runtime ya está instalado, con cualquiera de los siguientes métodos:

    *   Compruebe si la `pv (REG_SZ)` clave de registro existe y si la clave de registro está o está `null` vacía.  Si esta clave de registro no existe, o es o una cadena vacía, El tiempo de ejecución de WebView2 no está instalado actualmente `null` en el cliente.  Busque `pv (REG_SZ)` en la siguiente ubicación:
        
        En 64 bits Windows:
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
        En 32 bits Windows:
        
        ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\EdgeUpdate\Clients\{F3017226-FE2A-4295-8BDF-00C3A9A7E4C5}
        ```  
        
    *   Como alternativa, llame [a GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring] y compruebe si `versionInfo` es `NULL` .  Si `versionInfo` es , el tiempo de ejecución de `NULL` WebView2 no está instalado actualmente en el cliente.

1.  Si WebView2 Runtime no está instalado, ejecute el Instalador independiente de Evergreen.  Si desea ejecutar una instalación silenciosa, ejecute el instalador desde un proceso con privilegios elevados o copie y ejecute el siguiente comando:
    
    ```shell
    MicrosoftEdgeWebView2RuntimeInstaller{X64/X86/ARM64}.exe /silent /install
    ```  

### <a name="test-your-app-for-forward-compatibility"></a>Probar la compatibilidad con avances de la aplicación

La web está en constante evolución.  En el modo de distribución Evergreen, WebView2 Runtime se mantiene actualizado automáticamente en el cliente para proporcionar las últimas características y correcciones de seguridad.  Si usa la distribución Evergreen, para asegurarse de que la aplicación WebView2 sea compatible con la web, debe configurar la infraestructura de pruebas.  

Microsoft Edge los canales de vista previa \(Beta, Dev y Canary\) proporcionan un vistazo a lo que viene a continuación en El tiempo de ejecución de WebView2.  Prueba la aplicación WebView2 regularmente en un canal Microsoft Edge [][GithubMicrosoftedgeWebviewfeedback] vista previa y actualiza la aplicación o informa de problemas si surgen problemas.  Canary es el canal de vista previa recomendado, ya que se suministra con la cadencia más rápida y tiene las API más nuevas.

Para ayudarte a decidir qué canal es el más adecuado, ve a [Información general de los canales de Microsoft Edge][DeployEdgeMicrosoftEdgeChannels].  Puedes descargar [los Microsoft Edge Insider en][MicrosoftEdgeInsiderDownload] el entorno de prueba y usar o variables de entorno para indicar la preferencia del canal para la aplicación de `regkey` prueba.

Para obtener más información, ve a [ CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions].  También puede usar WebDriver para automatizar las pruebas de WebView2, como se describe en Automate, y probar [WebView2 con Microsoft Edge driver][HowToWebdriver].

### <a name="feature-detect-when-using-recent-apis"></a>Detección de características al usar API recientes

<!-- the main section about QueryInterface is in versioning.md; this section should be only a couple paragraphs -->

Si usa el modo Evergreen, cuando la aplicación WebView2 usa una nueva API de WebView2 de un SDK reciente, debe usar un enfoque como o para asegurarse de que la nueva API esté presente en el equipo del `QueryInterface` `try-catch` cliente.  Esta detección de características es un procedimiento recomendado, ya que hay casos en los que WebView2 Runtime no se actualiza.

Incluso si usa el modo de distribución Evergreen, es posible que WebView2 Runtime no se actualice, por los siguientes motivos:
*   Un administrador de TI puede desactivar las actualizaciones de WebView2 Runtime, ya que un administrador tiene el control de actualizar sus dispositivos.
*   Los clientes sin conexión no reciben el tiempo de ejecución actualizado de WebView2.

Las directivas de actualización para Microsoft Edge webView2 Runtime son independientes.  Incluso si el administrador de TI ha deshabilitado las actualizaciones automáticas de Microsoft _Edge,_ El tiempo de ejecución de _WebView2_ se actualiza automáticamente, a menos que el administrador desactiva la actualización en tiempo de ejecución.  Si el administrador deshabilita la actualización Microsoft Edge (que es algo habitual), esto no afecta a las API de WebView2 que están disponibles en el equipo cliente.

Para obtener más información, vaya a Detección de características para comprobar si el tiempo de ejecución instalado [admite API agregadas recientemente.][Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]


<!-- ====================================================================== -->
## <a name="details-about-the-fixed-version-runtime-distribution-mode"></a>Detalles sobre el modo de distribución en tiempo de ejecución de versión fija

Para entornos restringidos con requisitos de compatibilidad estrictos, considera la posibilidad de usar el modo de distribución de versión no editable.  El modo de distribución Versión fija se denominaba _anteriormente bring-your-own_.

En el modo de distribución Versión fija, controlas el tiempo de actualización del tiempo de ejecución de WebView2 para la aplicación.  Se descarga una versión específica de WebView2 Runtime y, a continuación, se empaqueta con la aplicación WebView2.  El tiempo de ejecución de WebView2 en el cliente no se actualiza automáticamente.  En su lugar, actualizas periódicamente el tiempo de ejecución de WebView2 que se empaqueta y distribuye junto con la aplicación actualizada.  El enfoque De versión fija no usa una clave del Registro para El tiempo de ejecución de WebView2.

Para usar el modo de distribución versión fija:

1.  Descargue la versión fija de WebView2 Runtime [desde Descargar WebView2 Runtime][Webview2Installer], como un paquete.

    La versión más parcheada de la última y la segunda versión principal están disponibles para su descarga en este sitio.  Mantenga una copia archivada de las versiones que necesite.

1.  Descomprima el paquete de Tiempo de ejecución de WebView2 mediante el comando de línea de comandos o mediante una herramienta `expand {path to the package} -F:* {path to the destination folder}` de descompresión como WinRAR.  Evite descomprimir a través del Explorador de archivos, ya que es posible que ese enfoque no genere la estructura de carpetas correcta.

1.  Incluye los archivos binarios de versión no editable descomprimidos en el proyecto.  

1.  Indica la ruta de acceso a los archivos binarios de versión fija al crear el entorno WebView2.  

    *   Para Win32 C/C++, puede crear el entorno mediante la [función CreateCoreWebView2EnvironmentWithOptions.][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions]  Use el `browserExecutableFolder` parámetro para indicar la ruta de acceso a la carpeta que contiene `msedgewebview2.exe` .

    *   Para .NET, debe especificar el entorno antes de que la propiedad WebView2 `Source` entre en vigor.  Para .NET, puede usar cualquiera de los siguientes métodos para especificar el entorno:

        *   Establezca la `CreationProperties` propiedad \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Creationproperties] / [WinForms][ReferenceWinFormsMicrosoftWebWebview2WinFormsWebview2]\) en el `WebView2` elemento.  Usa el miembro `BrowserExecutableFolder` en la clase `CoreWebView2CreationProperties` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfCorewebview2creationpropertiesCorewebview2creationproperties]/[WinForms][ReferenceWinFormsMicrosoftWebWebview2WinForms]\) para indicar la ruta de acceso a los archivos binarios de versión no editable.  

        *   Como alternativa, use `EnsureCoreWebView2Async` \([WPF][ReferenceWpfMicrosoftWebWebview2WpfWebview2Ensurecorewebview2async] / [WinForms][ReferenceWinformsMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]\) para especificar el entorno.  Usa el parámetro `browserExecutableFolder` en [CoreWebView2Environment.CreateAsync][ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentCreateasync] para indicar la ruta de acceso a los archivos binarios de versión no editable.  

1.  Empaqueta y envía los archivos binarios de versión no editable con la aplicación.  Actualiza los archivos binarios según corresponda.  
    
### <a name="known-issues-for-fixed-version"></a>Problemas conocidos para la versión no editable   

La instalación de la versión fija del tiempo de ejecución de WebView2 en el cliente hace [que Microsoft PlayReady][MicrosoftPlayReady] deje de funcionar.  Corrija la configuración de PlayReady de la siguiente manera.

1.  Busca la ruta de acceso en la que implementas el paquete de versión no editable en el dispositivo del usuario, como la siguiente ubicación.
    
    ```text
    D:\myapp\Microsoft.WebView2.FixedVersionRuntime.87.0.664.8.x64
    ```  
    
1.  Ejecuta los siguientes comandos en el dispositivo del usuario.

    ```shell
    icacls {Fixed Version path} /grant *S-1-15-2-2:(OI)(CI)(RX)
    icacls {Fixed Version path} /grant *S-1-15-2-1:(OI)(CI)(RX)
    ```  

1.  PlayReady debería estar funcionando ahora en el dispositivo del usuario.  Para confirmar que PlayReady está instalado **** correctamente, en la pestaña Seguridad de la carpeta **Versión** fija, asegúrese de que se conceden permisos para y , como se muestra a `ALL APPLICATION PACKAGES` `ALL RESTRICTED APPLICATION PACKAGES` continuación.

    :::image type="complex" source="../media/play-ready-permission.png" alt-text="Permiso para PlayReady" lightbox="../media/play-ready-permission.png":::
        Permiso para PlayReady  
    :::image-end:::  


<!-- ====================================================================== -->
<!-- links -->  
[ConceptsVersioning]: ./versioning.md "Descripción de las versiones de explorador y WebView2 | Microsoft Docs"  
[HowToWebdriver]: ../how-to/webdriver.md "Automatizar y probar WebView2 con Microsoft Edge Driver | Microsoft Docs"  
[Webview2ConceptsDevguideManageVersionsRuntime]: developer-guide.md#manage-new-versions-of-the-runtime "Administrar nuevas versiones del motor de tiempo de ejecución | Microsoft Docs"
[Webview2ConceptsVersioningDetermineWebview2RuntimeRequirement]: ../concepts/versioning.md#feature-detecting-to-test-whether-the-installed-runtime-supports-recently-added-apis "Detección de características para comprobar si el tiempo de ejecución instalado admite API agregadas recientemente: comprender las versiones del SDK de WebView2 | Microsoft Docs"
<!-- external links -->
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

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2#download-section "Descargue la aplicación WebView2 Runtime | Microsoft Developer"  

[MicrosoftEdgeInsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView | GitHub"  

[GitHubMicrosoftEdgeWebView2SamplesWebview2Deployment]: https://github.com/MicrosoftEdge/WebView2Samples#webview2-deployment "Implementación de WebView2: Muestras de MicrosoftEdge/WebView2 | GitHub"  

[MicrosoftPlayReady]: https://www.microsoft.com/playready "Microsoft PlayReady"  

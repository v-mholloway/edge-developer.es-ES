---
description: Mejorar progresivamente su PWA para Windows con características de aplicaciones nativas
title: Personalizar su PWA (EdgeHTML) para Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, WinRT, UWP, EdgeHTML
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 59612d8292d4c4d4d7073b843386364d1ac55c5d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236318"
---
# Personalizar su PWA (EdgeHTML) para Windows  

PWAs instalado en Windows 10 disfruta de [todas las ventajas][PwaIndexWindows10] de ejecutar como aplicaciones de la [plataforma universal de Windows \ (UWP \)][WindowsUWPGetStartedGuide] , entre ellas, la protección mediante la seguridad de espacio aislado de aplicaciones de Windows y el acceso total a las API de [Windows Runtime \ (WinRT \))][UwpApiIndex] , incluidas las de:  

*   Control de las características del dispositivo \ (como cámara, micrófono, GPS \)  
*   Acceso a los recursos de usuario \ (como calendario, contactos, documentos, música \)  
*   Iniciar o navegar por la aplicación a través de los comandos de voz Cortana  
*   Integración con el sistema operativo Windows \ (a través del centro de actividades de Windows, barra de tareas de escritorio y menús contextuales \)  
    
Estas son solo algunas de las posibilidades agregadas para su PWA \ \ (EdgeHTML \) en Windows.  

En este artículo se muestra cómo instalar, ejecutar y mejorar el PWA \ (EdgeHTML \) como una aplicación de Windows 10, sin dejar de garantizar la compatibilidad entre exploradores y plataformas.  

> [!IMPORTANT]
> Los ejemplos y los pasos de este artículo requieren Visual Studio 2017. Visual Studio 2019 no incluye la plantilla utilizada en este artículo. Para descargar Visual Studio 2017, vea [descargas de Visual Studio-2017, 2015 & versiones anteriores][PreviousVSDownloads]  


## Requisitos previos  

*   Un PWA \ (o una aplicación web hospedada \), ya sea un sitio activo o local.  Esta guía usa el ejemplo PWA de introducción [a las aplicaciones web progresivas][PwaGetStarted].  
*   Descargar la \ (gratis \) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].  También puede usar las ediciones Professional, Enterprise o [Preview][MicrosoftVisualStudioPreview] .  Desde el instalador de Visual Studio, elija las siguientes cargas de trabajo:  
    *   **Desarrollo de la plataforma universal de Windows**  
        
## Configurar y ejecutar la aplicación universal de Windows  

Un PWA \ (EdgeHTML \) instalado como una aplicación de Windows 10 se ejecuta independientemente del explorador, en una ventana \ ( `WWAHost.exe` proceso \) independiente.  Habilitar esta opción simplemente requiere un contenedor de aplicaciones ligero que contenga la aplicación web hospedada, que podrás configurar rápidamente con la plantilla de proyecto de Visual Studio `Progressive Web App (Universal Windows)` .  \ (La lógica de la aplicación, incluido el envío de solicitudes de API nativas de Windows en tiempo de ejecución, sigue apareciendo en el código original de la aplicación Web. \)  

Configure el entorno de desarrollo de aplicaciones de Windows en Visual Studio.  

1.  En la configuración de Windows, activa el [modo de desarrollador][WindowsUWPGetStartedEnable].  \ (Escriba `developer mode` el SEARCHBAR de Windows para encontrarlo. \)  
1.  Inicie Visual Studio y seleccione **crear un nuevo proyecto...**.  
1.  Elija **JavaScript**  >  **Windows universal** y seleccione **aplicación web progresiva (universal Windows)** en la lista de tipos de proyecto de Visual Studio 2017.  
1.  Seleccione la opción predeterminada Windows 10 `Target version` \ (versión más reciente \) y `Minimum version` \ (compilación 10586 o superior \) y elija **Aceptar**.  
    
    ![Cuadro de diálogo de selección de Visual Studio para compilaciones de destino de proyecto para UWP](media/vs-target-min-version.png)  
    
    El nuevo proyecto se cargará con el diseñador package. appxmanifest abierto.  Aquí es donde se configuran los detalles de la aplicación, como la identidad del paquete, las dependencias de paquete, las características necesarias, los elementos visuales y los puntos de extensibilidad.  Esta es una versión temporal, fácilmente configurable, del manifiesto del paquete de la aplicación usado durante el desarrollo de la aplicación.  
    Al compilar el proyecto de la aplicación, [Visual Studio genera un archivo AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] de estos metadatos, que se usa para instalar y ejecutar la aplicación.  Cada vez que actualice el `package.appxmanifest` archivo, asegúrese de volver a crear el proyecto para que ambos se reflejen en el tiempo de `AppxManifest.xml` ejecución.  
    
1.  En el panel de **aplicaciones** del diseñador de manifiestos, escriba la dirección URL de su PWA como `Start page` .
    
    > [!NOTE]
    > Los trabajadores del servicio son compatibles con todas las direcciones URL https \ (seguras, remotas) especificadas como `StartPage` .  Los trabajos de servicio no son compatibles de forma predeterminada en las aplicaciones web que especifican una página de inicio local.  Para habilitar la compatibilidad con los trabajadores del servicio en estos casos, agregue una entrada de [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) explícita en el manifiesto, por ejemplo: `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Panel de aplicación del diseñador package. appxmanifest](media/vs-manifest-application.png)  
    
    También puede modificar el `Display name` y el `Description` como desee.  
1.  Guarde este archivo \ (u otra imagen de 512x512 de su elección \) en el escritorio.  
    A continuación, en el panel **activos visuales** del diseñador de manifiestos, haga clic en el `Source` botón campo **...** , selecciónelo como archivo de origen y haga clic en **generar**.  \ (A continuación, haga clic en **Aceptar** para sobrescribir las imágenes de marcador de posición predeterminadas \).  
    
    ![Panel activos visuales del diseñador de Package. appxmanifest](media/vs-manifest-visual-assets.png)  
    
    Esto genera los activos visuales básicos para instalar, ejecutar, iniciar y distribuir tu aplicación en la tienda.  
    Si ve algún error en rojo \ ( `X` \) que indica que faltan imágenes, puede hacer clic en los botones **...** para seleccionar manualmente un archivo de las imágenes generadas.  
1.  En el panel **URI de contenido** del diseñador de manifiestos, reemplaza `http://example.com` por la ubicación de tu PWA \ (por ejemplo, `Rule`  =  `include` y `WinRT Access`  =  `All` \).  
    Esto concede al permiso de PWA solicitudes de API de Windows Runtime \ (WinRT \) nativas cuando se ejecuta como una aplicación de Windows 10, que se trata un poco más adelante.   Si su PWA real no requiere acceso a WinRT, puede cambiar el `WinRT Access` valor a `None` .  De cualquier forma, asegúrese de eliminar la cadena predeterminada `http://example.com` con el URI de su PWA o de que la aplicación no pueda cargarse correctamente en tiempo de ejecución.  
    Ya está listo para ejecutar y depurar PWA como una aplicación de Windows 10.  Si está usando un sitio localhost para recorrer esta guía, asegúrese de que se está ejecutando.  Luego  
1.  Compila \ ( `Ctrl` + `Shift` + `F5` \) y ejecuta \ ( `F5` \) el proyecto de PWA.  Ahora, el sitio web debe iniciarse en una ventana de la aplicación independiente.  No solo es una aplicación web hospedada; se está ejecutando como una aplicación web progresiva instalada en Windows 10.  
    
    ![PWA se ejecuta en una ventana WWAHost.exe](media/wwahost.png)  
    
## Depure su PWA \ (EdgeHTML \) como una aplicación de Windows  

Dado que un PWA \ (EdgeHTML \) es simplemente una aplicación web hospedada de forma progresiva, puede depurar el código de su servidor de la misma forma que cualquier aplicación Web, con el IDE y el flujo de trabajo habituales.  Los cambios que implemente en vivo se reflejarán en su PWA instalado la próxima vez que lo inicie \ (no es necesario que vuelva a implementar el paquete de la aplicación universal de Windows \).

Para la depuración del lado cliente dentro de la aplicación de Windows 10, debes tener la `Microsoft Edge DevTools Preview` aplicación.  Esta aplicación independiente incluye todas las funciones de la aplicación original en el explorador [Microsoft Edge DevTools][DevToolsGuide] \ (incluidas [las herramientas de PWA][DevToolsGuideServiceWorkers]\), además de compatibilidad con la [depuración remota][DevToolsProtocol01ClientsEdgePreview] básica y un [selector de destinos de depuración][DevToolsGuideMicrosoftStoreApp] para adjuntar a cualquier instancia en ejecución del motor de EdgeHTML, incluidos los complementos para Office, Cortana, webviews de aplicaciones, y obviamente  

Aquí se describe cómo configurar la depuración de su PWA \ \ (EdgeHTML \).  

1.  Instale la aplicación [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] desde Microsoft Store si aún no la tiene.  
1.  Con el sitio de PWA en marcha y ejecutándose, inicie la aplicación DevTools.  
1.  Desde Visual Studio, inicia la aplicación de Windows 10 con `Start Without Debugging` el `Ctrl` + `F5` comando ().  \ (La aplicación DevTools no se adjunta correctamente si el depurador de Visual Studio está activo. \)  
1.  En la aplicación DevTools, haga clic en el botón **Actualizar** del selector de destino de depuración local.  Ahora debe aparecer el sitio de PWA \ (EdgeHTML \).  \ (Si también se ejecuta en una ventana del explorador, es la última instancia de ese sitio en la lista).  
1.  Haga clic en la lista de sitios de PWA \ (EdgeHTML \) para abrir una nueva ficha de instancias de DevTools y empezar a depurar.  
    
    ![Selección local de destinos de depuración en la aplicación Microsoft Edge DevTools](media/devtools-local.png)  
    
1.  Puede comprobar que DevTools está adjunta a la aplicación PWA que se ejecuta como Windows.  En la **consola**de DevTools, escriba:  
    
    ```shell
    window.Windows
    ```  
    
    De esta forma, se devuelve el `Windows Runtime` objeto global que contiene todos los [espacios de nombres WinRT de nivel superior](#find-windows-runtime-winrt-apis).  Este es tu punto de vista de PWA \ \ (EdgeHTML \) a la [plataforma universal de Windows][WindowsUWPIndex]y solo está expuesto a las aplicaciones web que se ejecutan como aplicaciones de Windows 10 (que se ejecutan fuera del explorador, en un `WWAHost.exe` proceso).  
    
## Buscar API de Windows Runtime (WinRT)  

Como una aplicación de Windows instalada, tu [PWA \ (EdgeHTML \) tiene acceso completo a las API nativas de Windows Runtime][WindowsRuntime]; Identifique lo que necesita usar, obtenga los permisos necesarios y use la detección de características para enviar esa solicitud de API en entornos admitidos.  Recorra este proceso para agregar una mejora progresiva para los usuarios de escritorio de Windows de su PWA.  

Hay varias maneras de identificar las API de la plataforma universal de Windows que necesitas para tu PWA de Windows, como la búsqueda de contenido completo [documentos de UWP en el centro de desarrollo de Windows] [UWP/API/], descargar y ejecutar [muestras de código de UWP](#uwp-code-samples) con Visual Studio y examinar los fragmentos de código para las tareas comunes de PWAs en Windows.

Hay varias maneras de identificar las API de la plataforma universal de Windows que necesitas para tu Windows PWA, entre las que se incluyen la búsqueda de contenido completo [documentos de UWP en el centro de desarrollo de Windows] [UWP/API/], descargar y ejecutar [muestras de código de UWP](#uwp-code-samples) con Visual Studio y examinar los fragmentos de código de las tareas comunes de [PWAs en Windows 10 (EdgeHTML)][PwaIndexWindows10].  

En general, las API de WinRT funcionan en JavaScript de la misma forma que lo hacen en C#, por lo que puedes seguir la documentación general de la [plataforma universal de Windows][WindowsUWPIndex] y la referencia de la [API][UwpApiIndex] para su uso.  Sin embargo, tenga en cuenta las siguientes diferencias:  

*   Las características de WinRT en JavaScript usan  [diferentes convenciones de mayúsculas y minúsculas][ScriptingJsinrtUsingWinRTCasingConventions]  
*   [Los eventos se representan como identificadores de cadena][ScriptingJsinrtHandlingWinRTEvents] que se pasan a `addEventListener` / `removeEventListener` métodos de clase  
*   Los [métodos asincrónicos][ScriptingJsinrtUsingWinRT] usan el modelo de promesas de JavaScript  
*   Las aplicaciones de `Windows.UI.Xaml` JavaScript no admiten las API en el espacio de nombres, que usan la pila de procesamiento Web del motor de [EdgeHTML][DevGuideWhatsNew] \ (HTML, CSS \)  
    
Para obtener más información, consulta [usar Windows Runtime en JavaScript][WindowRuntimeUsingJavascript].  

### Muestras de código de UWP  

Consulta el repositorio de muestras de código de la [plataforma universal de Windows \ (UWP \)][MicrosoftDeveloperWindowsSamples] para examinar ejemplos de JavaScript para escenarios comunes de aplicaciones de Windows 10.  Aunque las versiones de JS de estos ejemplos usan la biblioteca [WinJS][GithubWinjsWinjs] para estructurar la plantilla de ejemplo, WinJS no es necesario para enviar las solicitudes de la API de WinRT mostradas en estos ejemplos.  

> [!NOTE]
> Si necesitas escuchar el [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] evento de la aplicación, puedes hacerlo usando la siguiente API de WinRT nativa:  
> 
> **Use este**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> ... por oposición, este tipo de solicitud de WinJS usada en las muestras:  
> 
> **No esto**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## Enviar solicitudes de API de WinRT desde tu PWA (EdgeHTML)  

En este punto, Imagine que desea agregar un menú contextual personalizado para los usuarios de Windows de nuestro PWA \ (EdgeHTML \) e identificar las API que necesita en el espacio de nombres [Windows. UI. popups][UwpApiWindowsUiPopups] .  

Para poder enviar cualquier solicitud de API de WinRT de nuestro PWA \ (EdgeHTML \), primero debes [establecer los permisos necesarios](#set-application-content-uri-rules-acurs) \ (o las reglas de URI de contenido de la aplicación \) en el archivo \ (\) del manifiesto del paquete de la aplicación de Windows `.appxmanifest` .  

Si cualquiera de estas solicitudes de API implica el acceso a recursos de usuario, como imágenes o música, o a características como la cámara o el micrófono, también tendrá que agregar [declaraciones de funcionalidades de aplicación](#app-capability-declarations) al manifiesto del paquete de la aplicación para que Windows solicite permiso al usuario.  Si, posteriormente, publica su PWA \ (EdgeHTML \) en Microsoft Store, estos [permisos de aplicación][MicrosoftSupportWindowsAppPermissions] obligatorios también se indican en la descripción de la tienda.  

#### Establecer reglas de URI de contenido de la aplicación (Acur)  

A través de las Acur, también conocidas como una lista de direcciones URL permitidas, podrás dar a las direcciones URL de tu nombre de PWA \ \ (EdgeHTML \) acceso directo a las API de Windows Runtime.  En el nivel del sistema operativo Windows, los límites de la Directiva adecuada se establecen para permitir el código hospedado en el servidor web para enviar directamente solicitudes de API de plataforma.  Estos límites se definen en el archivo de manifiesto del paquete de la aplicación al especificar las direcciones URL de PWA como `ApplicationContentUriRules` .  

Las reglas deben incluir la página de inicio de la aplicación y cualquier otra página que desee incluir en las páginas de la aplicación.  Si el usuario se desplaza a una dirección URL que no esté incluida en las reglas, Windows abrirá la dirección URL de destino en el explorador Microsoft Edge en lugar de la ventana independiente PWA \ (EdgeHTML \) \ ( `WWAHost.exe` proceso \).  También puede excluir direcciones URL específicas.  

Hay varias formas de especificar una dirección URL `Match` en las reglas:  

*   Un nombre de host exacto  
*   Se incluye un nombre de host para el que se incluya o excluya un URI con un subdominio cualquiera de ese nombre de host  
*   Un URI exacto  
*   Un URI exacto que contiene una propiedad de consulta  
*   Una ruta de acceso parcial y un comodín para indicar una extensión de archivo concreta para una regla de inclusión.  
*   Rutas de acceso relativas para reglas de exclusión  
    
Estos son algunos ejemplos de Acur en un `.appxmanifest` archivo:  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

Las direcciones URL definidas dentro de las Acur para la aplicación pueden conceder permisos a Windows en tiempo de ejecución a través del `WindowsRuntimeAccess` atributo, que acepta los siguientes valores:  

*   `all`: El código de JavaScript remoto tiene acceso a todas las API de WinRT y a cualquier componente local empaquetado.  El espacio de nombres [Windows \ (WinRT \))][UwpApiIndex] se ha insertado y está presente en el motor de secuencias de comandos.  
*   `allowForWeb`: El acceso a código remoto de JavaScript se limita a componentes empaquetados locales, incluidos los componentes personalizados de la versión C++/C #.  
*   `none`Programas.  La dirección URL especificada no tiene acceso a la plataforma.  
    
En este tutorial, ya ha establecido la única ACUR que necesita \ (paso 6 de la configuración anterior [y ejecutar](#set-up-and-run-your-universal-windows-app) la sección \ App \) para su aplicación de una sola página.  Puede confirmarlo en el panel **URI de contenido** del diseñador de Visual Studio `package.appxmanifest` .  

![Panel URI de contenido del diseñador de Visual Studio appxmanifest](media/vs-appxmanifest-editor-acurs.png)  

También puede ver el XML sin formato de su manifiesto haciendo clic con el botón secundario `package.appxmanifest` en el archivo en el explorador de soluciones de Visual Studio y seleccionando **Ver código** \ ( `F7` \).  Para volver a la vista de diseñador, seleccione **Diseñador de vistas** \ ( `Shift` + `F7` \).  

#### Declaraciones de funcionalidades de las aplicaciones  

Si tu aplicación necesita acceso mediante programación a recursos de usuario, como imágenes o música, o a dispositivos como una cámara o un micrófono, debes incluir las [declaraciones de funcionalidad][WindowsUwpPackagingAppCapabilities] de la aplicación correspondientes en el archivo de manifiesto del paquete de la aplicación.  Existen 3 categorías de declaración de funcionalidad de aplicación:  

*   [Funcionalidades de uso general][WindowsUwpPackagingAppCapabilitiesGeneralUse] que se aplican a la los escenarios de aplicaciones más habituales.  
*   [Funcionalidades de dispositivo][WindowsUwpPackagingAppCapabilitiesDevice] que permiten a tu aplicación acceder a periféricos y dispositivos internos.  
*   [Capacidades de uso especial][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] que admiten escenarios empresariales y requieren una cuenta de Microsoft Store Company.  Para obtener más información sobre las cuentas de empresa, consulta [Tipos de cuenta, ubicaciones y precios][WindowsUwpPublishAccountTypesLocationsFees].
    
La página de la aplicación Microsoft Store muestra todas las funciones que declares en el manifiesto del paquete de la aplicación, así que asegúrate de especificar solo las funcionalidades que tu aplicación realmente usa.

Algunas funciones proporcionan a las aplicaciones acceso a recursos confidenciales.  Estos recursos se consideran confidenciales porque cada uno de ellos puede acceder a los datos personales del usuario o costar dinero al usuario.  La configuración de privacidad, administrada por la aplicación [configuración][BingResultsWindows10Settings] de Windows 10, permite que el usuario controle dinámicamente el acceso a los recursos confidenciales.  Por lo tanto, es importante que la aplicación no asuma que un recurso sensible siempre esté disponible.  Para obtener más información sobre cómo acceder a recursos confidenciales, consulta las [Directrices para aplicaciones compatibles con la privacidad][WindowsUwpSecurityIndex].  

Para solicitar acceso, declara funcionalidades en el manifiesto del paquete de la aplicación.  En Visual Studio, puedes hacerlo desde el panel de **funciones** del diseñador package. appxmanifest.  

![Panel capacidades del diseñador de Visual Studio appxmanifest](media/vs-appxmanifest-editor-capabilities.png)  

En este tutorial, solo se necesita la funcionalidad predeterminada de Internet \ (cliente \), por lo que no es necesaria ninguna otra acción.  

### Usar la detección de características para invocar WinRT  

Para garantizar una experiencia de línea base de calidad para la audiencia de PWA en todas las plataformas, mejore progresivamente su experiencia de PWA en Windows usando la detección de características de WinRT.  De esta manera, podrás asegurarte de que el código específico de Windows solo se ejecuta en un contexto en el que las API de WinRT estén disponibles y sean aplicables.  

La detección de características puede ser tan simple como buscar el `Windows` objeto \ (el punto de espera del [espacio de nombres WinRT][UwpApiIndex]\) como se indica a continuación:  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

Sin embargo, dado que no todas las API de Windows están disponibles en todos los [tipos de dispositivos de Windows 10][UwpExtensionSdkDeviceFamiliesOverview], generalmente es útil usar una detección de características más específica para calificar aún más el espacio de nombres de la solicitud de API que se envía:  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

Con ese fondo, estás listo para agregar código WinRT para implementar un menú contextual personalizado.  Si usa el ejemplo PWA de introducción [a las aplicaciones web progresivas][PwaGetStarted]:

1.  Abra Visual Studio en el proyecto de sitio de PWA.  
1.  En el explorador de soluciones, abra el `views\layout.pug` archivo y agregue la línea siguiente, justo debajo de la `script` Referencia del trabajador del servicio:
    
    ```xml
    script(src='/javascripts/site.js')
    ```  
    
1.  En el explorador de soluciones, haga clic con el botón derecho en la `javascripts` carpeta y **agregue**  >  **nuevo archivo...**
1.  Asigne un nombre al archivo `site.js` y cópielo en el siguiente código:
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```
    
1.  Compare el comportamiento del menú contextual cuando ejecute su PWA en el explorador \ ( `F5` desde el proyecto de sitio de PWA \) o desde dentro de la ventana de la aplicación de Windows \ ( `F5` desde el proyecto de aplicación universal de Windows \).  En el explorador, al hacer clic con el botón secundario se le proporciona el menú contextual de Microsoft Edge predeterminado mientras que, en el `WWAHost.exe` proceso, aparece ahora el menú personalizado.  
    
    | Microsoft Edge | Aplicación de Windows 10 |  
    |:--- |:---- |  
    | ![Menú contextual predeterminado del explorador](media/browser-context-menu.png) | ![Menú contextual personalizado de la aplicación](media/app-context-menu.png) |  
    
Afortunadamente, ahora tienes una base sólida para mejorar de manera progresiva tu PWAs en Windows.  Si tienes preguntas o algo no está claro, envía un comentario.  

## Ir más allá

El [centro de desarrollo de Windows][MicrosoftDeveloperWindowsApps] es tu referencia completa para todas las fases de la creación de aplicaciones de Windows, desde [Introducción][MicrosoftDeveloperWindowsAppsGetStarted], hasta [diseñar][MicrosoftDeveloperWindowsAppsDesign], [desarrollar][MicrosoftDeveloperWindowsAppsDevelop]y [publicar][MicrosoftDeveloperStorePublishApps] en Microsoft Store.  

Para obtener información general sobre la plataforma universal de Windows \ (UWP \) y sobre cómo dirigir distintas familias de dispositivos de Windows 10, consulta [Introducción a la plataforma universal de Windows][WindowsUWPGetStartedGuide].  

Y cuando esté listo, aquí se muestra cómo \ (y por qué! \) [enviar su PWA a Microsoft Store](./microsoft-store.md).  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Introducción a las aplicaciones web progresivas | Microsoft docs"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs en Windows 10 (EdgeHTML): aplicaciones web progresivas en Windows | Microsoft docs"  
[DevToolsGuide]: ../devtools-guide/index.md "Herramientas para desarrolladores de Microsoft Edge (EdgeHTML) | Microsoft docs"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide/index.md#microsoft-store-app "Aplicación Microsoft Store: herramientas para desarrolladores de Microsoft Edge (EdgeHTML) | Microsoft docs"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Trabajadores de servicio | Microsoft docs"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Microsoft Edge DevTools Preview-clientes de protocolo DevTools | Microsoft docs"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Novedades de EdgeHTML | Microsoft docs"  
[WindowsRuntime]: ../windows-runtime/index.md "Windows Runtime (WinRT) para JavaScript | Microsoft docs"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Usar Windows Runtime en JavaScript | Microsoft docs"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Controlar eventos de Windows Runtime en JavaScript | Microsoft docs"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Uso de métodos asincrónicos de Windows Runtime | Microsoft docs"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Convenciones de las mayúsculas y minúsculas con características de Windows Runtime: uso de Windows Runtime en JavaScript | Microsoft docs"  
[UwpApiIndex]: /uwp/api/index "Espacios de nombres de Windows para UWP | Microsoft docs"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Espacio de nombres Windows. UI. popups | Microsoft docs"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "Evento WebUIApplication. activado | Microsoft docs"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Descripción general de las familias de dispositivos | Microsoft docs"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "Cómo genera Visual Studio un manifiesto del paquete de la aplicación | Microsoft docs"  
[WindowsUWPIndex]: /windows/uwp/index "Documentación de la plataforma universal de Windows | Microsoft docs"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "¿Qué es una aplicación para la plataforma universal de Windows (UWP)? | Microsoft docs"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Habilitar el dispositivo para el desarrollo | Microsoft docs"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Seguridad | Microsoft docs"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Tipos de cuenta, ubicaciones y tarifas | Microsoft docs"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Capacidades restringidas | Microsoft docs"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Capacidades del dispositivo | Microsoft docs"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Capacidades de uso general | Microsoft docs"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "Declaraciones de funcionalidades de la aplicación | Microsoft docs"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "configuración de Windows 10: Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "winjs/winjs | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Publicar aplicaciones y juegos de Windows"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Documentación de la plataforma universal de Windows"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Diseñar y codificar aplicaciones de Windows"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Desarrollar aplicaciones para UWP"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Introducción a las aplicaciones de Windows 10"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Ejemplos de código"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Vista previa de Microsoft Edge DevTools"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "Permisos de aplicación"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Descargas"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Vista previa de Visual Studio"  
[PreviousVSDownloads]: https://visualstudio.microsoft.com/vs/older-downloads/ "Descargas de Visual Studio"  

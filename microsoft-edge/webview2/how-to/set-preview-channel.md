---
description: Cómo especificar un canal Microsoft Edge vista previa que se va a usar para probar las API experimentales en un paquete de versión preliminar.
title: Cambiar a un canal de vista previa para probar las próximas API y características
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/03/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: bcec0b596ff9e1fd06e5d38507f0e00d5bffbdec
ms.sourcegitcommit: d6ecc4ab48c7e0e048fd8248f6379222642e9d41
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "11925546"
---
# <a name="switch-to-a-preview-channel-to-test-upcoming-apis-and-features"></a>Cambiar a un canal de vista previa para probar las próximas API y características

Las actualizaciones de WebView2 Evergreen Runtime suelen incluir nuevas API y características.  Algunas de estas actualizaciones podrían interrumpir la aplicación WebView2.  Para probar las API experimentales con antelación y garantizar la compatibilidad de avance de la aplicación, debes realizar pruebas de compatibilidad con un canal de vista previa de Microsoft Edge, junto con una versión preliminar del SDK de WebView2.

Al probar un paquete de SDK preliminar, debe dirigir la aplicación a usar un canal de vista previa de Microsoft Edge (Beta, Dev o Canary), en lugar de usar el tiempo de ejecución de WebView2 de forma predeterminada.  A continuación se explican varios métodos para hacerlo.

WebView2 Runtime no tiene las API experimentales de WebView2.  Para que el código webView2 se ejecute cuando se usan API experimentales en un SDK de versión preliminar, el cliente (en una máquina de desarrollo) debe tener un canal Microsoft Edge versión preliminar.  Se recomienda el canal de vista previa de Canary, ya que está por delante de los otros canales y tiene las API experimentales más recientes.

El SDK de versión preliminar funciona junto con un canal de vista previa de la siguiente manera:
*  Una versión preliminar del SDK de WebView2 contiene las firmas de método para las API experimentales, que permiten escribir código con las API experimentales de WebView2 en la aplicación.  
*  Los canales de vista previa de Microsoft Edge contienen los archivos binarios Microsoft Edge que son necesarios para ejecutar y representar la aplicación, incluida la implementación de las API experimentales.

Para obtener más información sobre cómo funcionan las versiones del SDK junto con los canales de versión en tiempo de ejecución de WebView2 o de vista previa de Microsoft Edge, vaya a Comprender las versiones del [SDK de WebView2][WebView2ConceptsVersioning].


## <a name="downloading-the-prerelease-sdk-and-a-preview-channel"></a>Descargar el SDK de versión preliminar y un canal de vista previa

Para usar API experimentales, descargue una versión preliminar del SDK de WebView2 desde el paquete [Microsoft.Web.WebView2](https://www.nuget.org/packages/Microsoft.Web.WebView2).

Para obtener un canal Microsoft Edge vista previa, vaya a [Descargar Microsoft Edge Canales insider][MicrosoftedgeinsiderDownload].


<!-- intro/overview of 4 approaches -->
## <a name="approaches-to-making-your-app-use-a-specific-browser-channel"></a>Enfoques para hacer que la aplicación use un canal de explorador específico

Hay varias maneras de hacer que la aplicación WebView2 use un canal de vista previa especificado de Microsoft Edge:
*  Llamando a una función.
*  Mediante una directiva de grupo.
*  Mediante una invalidación del Registro.
*  Mediante una variable de entorno.

Estos enfoques se describen a continuación.

### <a name="default-channel-search-order"></a>Orden de búsqueda de canal predeterminado

Esta sección se aplica al uso de una directiva de grupo, invalidación del Registro o variable de entorno.

El orden predeterminado de búsqueda de canal es:
1.  Tiempo de ejecución de WebView2.
1.  El canal beta de Microsoft Edge.
1.  Canal de desarrollo de Microsoft Edge.
1.  El canal Canary de Microsoft Edge.

Si establece la carpeta ejecutable del explorador, esto invalida el orden de búsqueda anterior.

Si establece la preferencia del canal de versión mediante una directiva de grupo, invalidación del Registro o variable de entorno, usará la inversa del orden de búsqueda predeterminado.


<!-- 1. Code ===============================================================-->
## <a name="using-code"></a>Uso de código

Si desea hacer que la aplicación use un canal Microsoft Edge vista previa mediante una llamada a una función, siga estos pasos.  

Este enfoque solo es útil para las pruebas locales y no debe enviarse.  Esto se debe a que este enfoque requiere encontrar la ruta de acceso de instalación del explorador perimetral, que podría cambiar en futuras actualizaciones.

### <a name="win32c"></a>Win32\/C++

Usaremos [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample) para demostrar este procedimiento.

1.  En el equipo de desarrollo, busque la ruta de acceso que contiene el Microsoft Edge vista previa.  Por ejemplo: 

    `C:\\Users\\myname\\AppData\\Local\\Microsoft\\Edge SxS\\Application\\93.0.929.0`

1.  Clone el [repositorio WebView2Samples.](https://github.com/MicrosoftEdge/WebView2Samples)

1.  Abra el **proyecto WebView2APISample** y, a continuación, en **Archivos de origen,** abra el `AppWindow.cpp` archivo.

1.  Busque dónde [se llama a CreateCoreWebView2EnvironmentWithOptions.][Webview2RefWin32GlobalsCreateCoreWebView2EnvironmentWithOptions]  Por ejemplo:

    ```cpp
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, m_userDataFolder.c_str(), options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
    ```

1.  Reemplace la `subFolder` variable por la ruta de acceso de carpeta Microsoft Edge canal de vista previa que desee usar.  Por ejemplo:

    ```cpp
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        L"C:\\Users\\myname\\AppData\\Local\\Microsoft\\Edge SxS\\Application\\93.0.929.0", m_userDataFolder.c_str(), options.Get(),
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
    ```

### <a name="winforms"></a>WinForms

WinForms usa un enfoque similar al enfoque de Win32/C++ descrito anteriormente.

1.  Se `CreationProperties.BrowserExecutableFolder` establece para que apunte a la ruta de acceso que contiene el Microsoft Edge de canary o dev.  Para ello, en la **solución WebView2Samples,** en el proyecto **WebView2WpfBrowser,** abra el archivo `MainWindow.xaml.cs` .

1.  Buscar `CreationProperties.BrowserExecutableFolder` .  Por ejemplo:

    ```csharp
    WebView2 GetReplacementControl(bool useNewEnvironment)
    {
        WebView2 replacementControl = new WebView2();
        ((System.ComponentModel.ISupportInitialize)(replacementControl)).BeginInit();
        // Setup properties and bindings.
        if (useNewEnvironment)
        {
            // Create a new CoreWebView2CreationProperties instance so the environment
            // is made anew.
            replacementControl.CreationProperties = new CoreWebView2CreationProperties();
            replacementControl.CreationProperties.BrowserExecutableFolder = webView.CreationProperties.BrowserExecutableFolder;
            replacementControl.CreationProperties.Language = webView.CreationProperties.Language;
            replacementControl.CreationProperties.UserDataFolder = webView.CreationProperties.UserDataFolder;
            shouldAttachEnvironmentEventHandlers = true;
        }
    ```

### <a name="wpf"></a>WPF

WPF usa un enfoque similar al enfoque de Win32/C++ descrito anteriormente.

Consulte [CoreWebView2CreationProperties.BrowserExecutableFolder (propiedad).](/dotnet/api/microsoft.web.webview2.wpf.corewebview2creationproperties.browserexecutablefolder#Microsoft_Web_WebView2_Wpf_CoreWebView2CreationProperties_BrowserExecutableFolder)


<!-- 2. Group Policy =======================================================-->
## <a name="using-a-group-policy"></a>Uso de una directiva de grupo

Si desea hacer que la aplicación use un canal de vista previa Microsoft Edge mediante una directiva de grupo, copie los archivos ADMX y ADML en la carpeta, de la `PolicyDefinitions` siguiente manera.

1.  Descargue los archivos de directiva [de Descargar e implementar Microsoft Edge para empresas](https://www.microsoft.com/edge/business/download).

1.  Copie el archivo ADMX en una carpeta de plantillas Definiciones de directiva, como `C:\Windows\PolicyDefinitions` .

1.  Copie el archivo ADML en una carpeta de configuración regional que coincida dentro de la `Policy Definitions` carpeta, como una `C:\Windows\PolicyDefinitions\en-us` carpeta.

1.  Abra el **Editor de directivas de grupo local**.  Para ello, en la barra Windows búsqueda, escriba "directiva de grupo" y, a continuación, **seleccione Editar directiva de grupo**.

1.  Expanda **Directiva de equipo local**y, a continuación, Configuración **del** equipo o Configuración de **usuario.**  A **continuación,**  >  **expanda Plantillas administrativas Microsoft Edge WebView2**.

    :::image type="complex" source="./media/local-group-policy-editor.png" alt-text="Cuadro de diálogo Editor de directivas de grupo local" lightbox="./media/local-group-policy-editor.png":::
       **Cuadro de diálogo Editor de directivas** de grupo local
    :::image-end:::  

1.  Seleccione **Carpeta ejecutable del explorador**.  Las siguientes capturas de pantalla se aplican a la configuración **de la carpeta ejecutable del explorador**.  Como alternativa, seleccione **Liberar preferencia de canal**, que usa cuadros de diálogo similares.

    :::image type="complex" source="./media/browser-executable-folder.png" alt-text="Configuración de la carpeta ejecutable del explorador" lightbox="./media/browser-executable-folder.png":::
       Configuración de la **carpeta ejecutable del explorador**
    :::image-end:::  

1.  Seleccione el **botón Mostrar.**

1.  Rellene el cuadro de **diálogo Mostrar** contenido.  En la **columna Nombre de** valor, escriba un asterisco para aplicarlo a todas las aplicaciones webView2 o un nombre de archivo que solo afecte a la aplicación `.exe` WebView2 especificada.  En la **columna** Valor, escriba la ruta de acceso al archivo ejecutable de la aplicación WebView2.

    :::image type="complex" source="./media/show-contents.png" alt-text="Cuadro de diálogo Mostrar contenido" lightbox="./media/show-contents.png":::
       Cuadro **de diálogo Mostrar** contenido
    :::image-end:::  

1.  Seleccione **Aceptar** para cerrar los cuadros de diálogo.

Para obtener más información, vea [Configure Microsoft Edge policy settings](/deployedge/configure-microsoft-edge).


<!-- 3. Registry Override ==================================================-->
## <a name="using-a-registry-override"></a>Uso de una invalidación del Registro

Al especificar un canal de vista previa mediante una invalidación del Registro, hay dos opciones:
*  Cambiar la carpeta ejecutable del explorador.
*  Cambiar la preferencia del canal de versión.

Estos dos enfoques se describen a continuación.

### <a name="registry-override-browser-executable-folder"></a>Invalidación del Registro: carpeta ejecutable del explorador

Para que la aplicación use un canal Microsoft Edge vista previa mediante una invalidación del Registro que establece la carpeta ejecutable del explorador:

1.  Abra un terminal de PowerShell o un símbolo del sistema habilitado para PowerShell.

1.  Modifique y ejecute el siguiente comando:

    `REG ADD HKLM\Software\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder /v * /t REG_SZ /d "C:\Users\myname\AppData\Local\Microsoft\Edge SxS\Application\88.0.680.0"`

    El asterisco (*) como nombre del valor hace que esta invalidación se aplique a todas las aplicaciones webView2.  Si solo quieres aplicar esta invalidación a una aplicación webView2 determinada, reemplaza el asterisco por el nombre de archivo del archivo ejecutable de la aplicación.

    Reemplace `C:\Users\myname\AppData\Local\Microsoft\Edge SxS\Application\88.0.680.0` por la ruta de acceso al canal Microsoft Edge vista previa deseado.

#### <a name="resuming-using-the-default-webview2-evergreen-runtime"></a>Reanudación con el valor predeterminado, WebView2 Evergreen Runtime

Para deshacer la configuración anterior, ejecute el siguiente comando:

`REG DELETE HKLM\Software\Policies\Microsoft\Edge\WebView2\BrowserExecutableFolder /f`

### <a name="registry-override-release-channel-preference"></a>Invalidación del Registro: preferencia de canal de publicación

Para hacer que la aplicación use un canal Microsoft Edge vista previa mediante una invalidación del Registro que cambie la preferencia del canal de versión cambiando el orden de búsqueda de un canal:

1.  Abra un terminal de PowerShell o un símbolo del sistema habilitado para PowerShell.

1.  Modifique y ejecute el siguiente comando:

    `REG ADD HKLM\Software\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference /v * /t REG_SZ /d "1"`

    El asterisco (*) como nombre del valor hace que esta invalidación se aplique a todas las aplicaciones webView2.  Si solo quieres aplicar esta invalidación a una aplicación webView2 determinada, reemplaza el asterisco por el nombre de archivo del archivo ejecutable de la aplicación.

#### <a name="resuming-using-the-default-webview2-evergreen-runtime"></a>Reanudación con el valor predeterminado, WebView2 Evergreen Runtime

Para eliminar la `ReleaseChannelPreference` invalidación del Registro, ejecute el comando:

`REG DELETE HKLM\Software\Policies\Microsoft\Edge\WebView2\ReleaseChannelPreference /f`


<!-- 4. Environment Variable ========================================================================-->
## <a name="using-an-environment-variable"></a>Uso de una variable de entorno

Para hacer que la aplicación use un canal Microsoft Edge vista previa mediante una variable de entorno:

1.  En la Windows de búsqueda, escriba "entorno" y, a continuación, **seleccione Editar las variables de entorno del sistema.**

    :::image type="complex" source="./media/search-bar-edit-sys-env-vars.png" alt-text="Uso de la Windows de búsqueda para buscar dónde editar variables de entorno" lightbox="./media/search-bar-edit-sys-env-vars.png":::
       Uso de la Windows de búsqueda para buscar dónde editar variables de entorno
    :::image-end:::  

1.  En el **cuadro de diálogo Propiedades** del sistema, seleccione la **pestaña** Avanzadas y, a continuación, seleccione el botón **Variables de** entorno.

    :::image type="complex" source="./media/system-properties-env-vars.png" alt-text="El botón Variables de entorno del cuadro de diálogo Propiedades del sistema" lightbox="./media/system-properties-env-vars.png":::
       El **botón Variables de** entorno del cuadro de diálogo **Propiedades** del sistema
    :::image-end:::  

1.  En la **sección Variables de usuario** del cuadro de diálogo **Variables** de entorno, seleccione **Nuevo**.

1.  En el **cuadro de diálogo Nueva variable** de usuario, establezca el nombre de **variable** en y establezca el valor variable en la ruta de acceso `WEBVIEW2_BROWSER_EXECUTABLE_FOLDER` al canal del explorador preferido. ****

    Como alternativa, establezca el **nombre de variable** en y establezca el valor variable `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` **en** `1` .  

1.  Seleccione **Aceptar** para cerrar los cuadros de diálogo.

    :::image type="complex" source="./media/env-vars-new-user-variable.png" alt-text="Agregar una nueva variable de entorno, como variable de usuario" lightbox="./media/env-vars-new-user-variable.png":::
       Agregar una nueva variable de entorno, como variable de usuario
    :::image-end:::  

> [!NOTE]
> Este enfoque establece la variable de entorno para todas las aplicaciones webView2, no solo la aplicación que estás probando.  Para establecer esta variable de entorno solo para la aplicación WebView2 que estás probando, si estás ejecutando la aplicación desde el símbolo del sistema, establece la variable de entorno `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE=1` .  Esto establece la variable de entorno solo para el proceso de símbolo del sistema actual y `cmd.exe` para los nuevos procesos secundarios de esa `cmd.exe` instancia.  A continuación, la variable de entorno solo se aplica a la aplicación WebView2 que estás probando.

> [!NOTE]
> Después de establecer una variable de entorno de esta manera, la variable de entorno se aplica a los nuevos procesos que se crean.  La variable de entorno no se aplica a los procesos que ya se están ejecutando.  Para asegurarse de que todos los procesos usan la nueva variable de entorno, es posible que deba reiniciar Visual Studio o cerrar sesión de Windows y, a continuación, volver a iniciar sesión.


<!--========================================================================-->
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Ponerse en contacto con el equipo de Microsoft Edge WebView

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]

<!-- links -->
[WebView2ConceptsVersioning]: ../concepts/versioning.md "Comprender las versiones de SDK de WebView2 | Microsoft Docs"
<!-- external links -->
[Webview2RefWin32GlobalsCreateCoreWebView2EnvironmentWithOptions]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs"
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"

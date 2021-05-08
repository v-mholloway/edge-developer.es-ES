---
description: Guía de introducción con WebView2 para aplicaciones WinForms
title: Introducción a webView2 para aplicaciones de WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, aplicaciones de winforms, winforms, edge, CoreWebView2, control de explorador, html perimetral, introducción, Introducción, .NET, formularios de windows
ms.openlocfilehash: 704e5732ddcff02e56f49bec37a5d1ad5f11c2b5
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536238"
---
# <a name="get-started-with-webview2-in-windows-forms"></a>Introducción a WebView2 en Windows Forms

En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obtener más información sobre las API individuales, vaya a [Referencia de api][DotnetApiMicrosoftWebWebview2Winforms].  

## <a name="prerequisites"></a>Requisitos previos  

Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.  

*   [WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en el sistema operativo compatible \(actualmente Windows 10, Windows 8.1 y Windows 7\).  
    
    > [!NOTE]
    > El equipo de WebView recomienda usar el canal Canary y la versión mínima necesaria es 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 o posterior.  
    
> [!NOTE]
> WebView2 actualmente no admite los diseñadores de .NET 5 y .NET Core.  

## <a name="step-1---create-a-single-window-app"></a>Paso 1: Crear una aplicación de una sola ventana

Comience con un proyecto de escritorio básico que contenga una sola ventana principal.  

1.  En Visual Studio, elija **Windows Forms .NET Framework App**  >  **Next**.
    
    :::image type="complex" source="./media/winforms-new-project.png" alt-text="Nuevo proyecto" lightbox="./media/winforms-new-project.png":::
       Nuevo proyecto  
    :::image-end:::
    
1.  Escriba valores para **Nombre del proyecto y** **Ubicación**.  Elija **.NET Framework 4.6.2** o posterior.  
    
    :::image type="complex" source="./media/winforms-start-proj.png" alt-text="Iniciar proyecto" lightbox="./media/winforms-start-proj.png":::
       Iniciar proyecto  
    :::image-end:::
    
1.  Para crear el proyecto, elija **Crear**.
    
## <a name="step-2---install-webview2-sdk"></a>Paso 2: Instalar WebView2 SDK

Use NuGet para agregar el SDK de WebView2 al proyecto.  

1.  Mantenga el mouse en el proyecto, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Administrar paquetes NuGet...**.  
    
    :::image type="complex" source="./media/wpf-getting-started-mng-nuget.png" alt-text="Administrar paquetes nuget":::
       Administrar paquetes nuget
    :::image-end:::
    
1.  En la barra de búsqueda, `Microsoft.Web.WebView2` escriba > **elija Microsoft.Web.WebView2**.  
    
    :::image type="complex" source="./media/install-nuget.png" alt-text="NuGet" lightbox="./media/install-nuget.png":::
       NuGet  
    :::image-end:::
    
    Comience a desarrollar aplicaciones con la API de WebView2.  Para compilar y ejecutar el proyecto, seleccione `F5` .  El proyecto en ejecución muestra una ventana vacía.  
    
    :::image type="complex" source="./media/winforms-empty-app.png" alt-text="Aplicación vacía" lightbox="./media/winforms-empty-app.png":::
       Aplicación vacía  
    :::image-end:::
    
## <a name="step-3---create-a-single-webview"></a>Paso 3: Crear un único WebView  

Agrega un WebView a la aplicación.  

1.  Abra el **Diseñador de Windows Forms**.  
1.  Busque **WebView2 en** el cuadro **de herramientas**.  
    
    > [!NOTE]
    > Si usa Visual Studio 2017, es posible que **WebView2** no se muestre de forma predeterminada en el cuadro **de herramientas**.  Para habilitar el comportamiento, elija **Opciones**  >  **de**herramientas  >  **Generales** > **** la configuración Del cuadro de herramientas Rellenar automáticamente en `True` .  
    
    Arrastre y coloque el control **WebView2** en la aplicación de Windows Forms.
    
    :::image type="complex" source="./media/winforms-toolbox.png" alt-text="Cuadro de herramientas que muestra WebView2":::
       Cuadro de herramientas que muestra WebView2  
    :::image-end:::  
    
1.  Establezca la `(Name)` propiedad en `webView` .
    
    :::image type="complex" source="./media/winforms-properties.png" alt-text="Propiedades del control WebView2":::
       Propiedades del control WebView2
    :::image-end:::
    
1.  La `Source` propiedad establece el URI inicial que se muestra en el control WebView2.  Establezca la `Source` propiedad en `https://www.microsoft.com` .  
    
    :::image type="complex" source="./media/winforms-source.png" alt-text="La propiedad Source del control WebView2":::
       La **propiedad Source** del control WebView2
    :::image-end:::  

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrese de que el control WebView2 muestra [https://www.microsoft.com][|::ref1::|Main] .

:::image type="complex" source="./media/winforms-hello-webview.png" alt-text="hello webview" lightbox="./media/winforms-hello-webview.png":::
   hello webview  
:::image-end:::    

> [!NOTE]
> Si estás trabajando en un monitor de PPP alto, es posible que debas configurar la aplicación de Windows Forms para que sea [compatible con PPP alto.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]  

## <a name="step-4---handle-window-resize-events"></a>Paso 4: Controlar eventos de cambio de tamaño de ventana  

Agrega algunos controles más a Windows Forms desde el cuadro de herramientas y, a continuación, controla los eventos de cambio de tamaño de la ventana correctamente.  

1.  En el **Diseñador de Windows Forms,** abra el **cuadro de herramientas**.  
1.  Arrastre y coloque un **textbox** en la aplicación de Windows Forms.  Asigne el **nombre TextBox** `addressBar` a la pestaña **Propiedades**.  
1.  Arrastre y coloque un **botón** en la aplicación de Windows Forms.  Cambie el texto del **botón a y** asigne un nombre al botón `Go!` **en** la `goButton` pestaña **Propiedades**.  
    
    La aplicación debe tener el aspecto de la siguiente imagen en el diseñador.  
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="Diseñador de WinForms" lightbox="./media/winforms-designer.png":::
       Diseñador de WinForms  
    :::image-end:::  

1.  En el archivo, defina para mantener los controles en su lugar cuando se cambie el tamaño de `Form1.cs` la ventana de la `Form_Resize` aplicación.
    
```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```  

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrate de que la aplicación se muestre de forma similar a la siguiente captura de pantalla.

:::image type="complex" source="./media/winforms-app.png" alt-text="aplicación" lightbox="./media/winforms-app.png":::
   Aplicación  
:::image-end:::  

## <a name="step-5---navigation"></a>Paso 5: navegación

Agregue la capacidad de permitir a los usuarios cambiar la dirección URL que muestra el control WebView2 agregando una barra de direcciones a la aplicación.  

1.  Seleccione `F5` para compilar y ejecutar el proyecto.  Confirme que la aplicación se muestra de forma similar a la siguiente captura de pantalla.  
    
    :::image type="complex" source="./media/winforms-app.png" alt-text="WinForms App" lightbox="./media/winforms-app.png":::
       WinForms App  
    :::image-end:::  
    
1.  En el `Form1.cs` archivo, para agregar el espacio `CoreWebView2` de nombres, inserte el siguiente fragmento de código en la parte superior.  
1.  En `Form1.cs` agregar el espacio de nombres `CoreWebView2` insertando el siguiente fragmento de código en la parte superior de `Form1.cs` .  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```
    
1.  En el **Diseñador de Windows Forms,** haga doble clic en el `Go!` botón para crear el método en el `goButton_Click` `Form1.cs` archivo.  Copie y pegue el siguiente fragmento de código dentro de la función.  Ahora, la `goButton_Click` función navega por WebView hasta la dirección URL especificada en la barra de direcciones.
    
    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  
    
Para compilar y ejecutar el proyecto, seleccione `F5` .  Escriba una nueva dirección URL en la barra de direcciones y seleccione **Ir**.  Por ejemplo, escriba `https://www.bing.com` .  Asegúrese de que el control WebView2 navega a la dirección URL.  

> [!NOTE]
> Asegúrese de que se ha escrito una dirección URL completa en la barra de direcciones.  Se `ArgumentException` produce un error si la dirección URL no comienza con `http://` o `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   bing.com  
:::image-end:::  

## <a name="step-6---navigation-events"></a>Paso 6: eventos de navegación  

Durante la navegación por la página web, el control WebView2 genera eventos.  La aplicación que hospeda los controles WebView2 escucha los siguientes eventos.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
    
Para obtener más información, vaya a [Eventos de navegación][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   Eventos de navegación
:::image-end:::

Cuando se produce un error, se producen los siguientes eventos y pueden depender de la navegación a una página web de error.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    
> [!NOTE]
> Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.  

Para demostrar cómo usar los eventos, empiece registrando un controlador para que cancele las solicitudes que no `NavigationStarting` usen HTTPS.  

En el `Form1.cs` archivo, actualice el constructor para que coincida con el siguiente fragmento de código y agregue la `EnsureHttps` función.  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```  

En el constructor, `EnsureHttps` se registra como el controlador de eventos en el evento en el control `NavigationStarting` WebView2.  

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrese de que al navegar a un sitio HTTP, webView permanece sin cambios.  Sin embargo, WebView navegará a los sitios HTTPS.

## <a name="step-7---scripting"></a>Paso 7: scripting  

Puede usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.  Puede realizar la tarea WebView para ejecutar JavaScript arbitrario o agregar scripts de inicialización.  JavaScript inyectado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quita JavaScript.  JavaScript inyectado se ejecuta con un tiempo específico.  

*   Ejecutarlo después de la creación del objeto global.  
*   Ejecutarlo antes de que se ejecute cualquier otro script incluido en el documento HTML.  
    
Por ejemplo, agregue scripts que envíen una alerta cuando un usuario navegue a sitios que no son HTTPS.  Modifique la `EnsureHttps` función para insertar un script en el contenido web que usa el método [ExecuteScriptAsync.][DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrate de que la aplicación muestra una alerta cuando navegas a un sitio web que no usa HTTPS.  

:::image type="complex" source="./media/winforms-https.png" alt-text="https" lightbox="./media/winforms-https.png":::
   https  
:::image-end:::  

## <a name="step-8---communication-between-host-and-web-content"></a>Paso 8: comunicación entre el contenido de host y web  

El host y el contenido web pueden `postMessage` usarse para comunicarse entre sí de la siguiente manera:  

*   El contenido web de un control WebView2 puede `window.chrome.webview.postMessage` usarse para publicar un mensaje en el host.  El host controla el mensaje con cualquier registrado `WebMessageReceived` en el host.  
*   Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON` .  Estos mensajes son capturados por controladores agregados a `window.chrome.webview.addEventListener` .  
    
El mecanismo de comunicación pasa mensajes del contenido web al host mediante funcionalidades nativas.  

En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL mostrada en el control WebView2.  

1.  En el `Form1.cs` archivo, actualice el constructor y cree una `InitializeAsync` función que coincida con el siguiente fragmento de código.  La `InitializeAsync` función espera [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] porque la inicialización de `CoreWebView2` es asincrónica.  
    
    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  
    
1.  Después `CoreWebView2` de inicializarse, registre un controlador de eventos para responder a `WebMessageReceived` .  En el `Form1.cs` archivo, actualice `InitializeAsync` y agregue con el siguiente fragmento de `UpdateAddressBar` código.  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }

    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  
    
1.  Para que WebView envíe y responda al mensaje web, después de inicializarse, el host inserta un script en el `CoreWebView2` contenido web para:  
    1.  Envíe la dirección URL al host mediante `postMessage` .
    1.  Registrar un controlador de eventos para imprimir un mensaje enviado desde el host.  
        
En el `Form1.cs` archivo, actualice `InitializeAsync` para que coincida con el siguiente fragmento de código.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Para compilar y ejecutar la aplicación, seleccione `F5` .  Ahora, la barra de direcciones muestra el URI en el control WebView2.  Además, cuando navega correctamente a una nueva dirección URL, WebView alerta al usuario de la dirección URL que se muestra en WebView.  

:::image type="complex" source="./media/winforms-final-app.png" alt-text="Aplicación final" lightbox="./media/winforms-final-app.png":::
   Aplicación final  
:::image-end:::  

Enhorabuena, has creado tu primera aplicación WebView2.  

## <a name="next-steps"></a>Pasos siguientes  

Para seguir aprendiendo más sobre WebView2, vaya a los siguientes recursos.  

*   Para obtener más información sobre cómo crear aplicaciones webView2, vaya a Procedimientos recomendados de desarrollo [de WebView2][WV2BestPractices].  
*   Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].  
*   Para obtener información detallada acerca de la API de WebView2, vaya a [Referencia de api][DotnetApiMicrosoftWebWebview2WinformsWebview2].  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Procedimientos recomendados de desarrollo de WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Clase WebView2 | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Configuración de la aplicación de Windows Forms para la compatibilidad con PPP alto: compatibilidad con PPP alto en Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desarrollador de Microsoft Edge"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

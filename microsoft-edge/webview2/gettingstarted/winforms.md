---
description: Guía de introducción a WebView2 para aplicaciones WinForms
title: Introducción a WebView2 para aplicaciones WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, webview2, WebView, webview, winforms apps, winforms, edge, CoreWebView2, control de explorador, edge html, getting started, Getting Started, .NET, windows forms
ms.openlocfilehash: 45a3b59733a57975e373df2e21258198645be2d4
ms.sourcegitcommit: d89f77d4667dfbc44ed35f2ec7e3ae64ab98bf1a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "11306169"
---
# Introducción a WebView2 en Windows Forms

En este artículo, empieza a crear tu primera aplicación WebView2 y obtén información sobre las características principales [de WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Para obtener más información sobre las API individuales, vaya a [la referencia de la API.][DotnetApiMicrosoftWebWebview2Winforms]  

## Requisitos previos  

Asegúrese de instalar la siguiente lista de requisitos previos antes de continuar.  

*   [WebView2 Runtime][MicrosoftDeveloperMicrosoftEdgeWebview2] o cualquier canal no estable de [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] instalado en el sistema operativo compatible \(actualmente Windows 10, Windows 8.1 y Windows 7\).  
    
    > [!NOTE]
    > El equipo de WebView recomienda usar el canal Canary y la versión mínima necesaria es 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2017 o posterior.  
    
> [!NOTE]
> WebView2 actualmente no admite los diseñadores .NET 5 y .NET Core.

## Paso 1: Crear una aplicación de una sola ventana

Comience con un proyecto de escritorio básico que contenga una sola ventana principal.  

1.  En Visual Studio, elija **Windows Forms .NET Framework App**  >  **Next**.
    
    :::image type="complex" source="./media/winforms-newproject.png" alt-text="Nuevo proyecto" lightbox="./media/winforms-newproject.png":::
       Nuevo proyecto  
    :::image-end:::
    
1.  Escriba los valores del **nombre del proyecto y** la **ubicación.**  Elija **.NET Framework 4.6.2** o posterior.  
    
    :::image type="complex" source="./media/winforms-startproj.png" alt-text="Iniciar proyecto" lightbox="./media/winforms-startproj.png":::
       Iniciar proyecto  
    :::image-end:::
    
1.  Para crear el proyecto, elija **Crear**.
    
## Paso 2: Instalar el SDK de WebView2

Usa NuGet para agregar el SDK de WebView2 al proyecto.  

1.  Mantenga el puntero sobre el proyecto, abra el menú contextual \(haga clic con el botón secundario\) y elija Administrar **paquetes NuGet...**.  
    
    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Administrar paquetes NuGet":::
       Administrar paquetes NuGet
    :::image-end:::
    
1.  En la barra de búsqueda, `Microsoft.Web.WebView2` escriba > **seleccione Microsoft.Web.WebView2**.  
    
    :::image type="complex" source="./media/installnuget.png" alt-text="NuGet" lightbox="./media/installnuget.png":::
       NuGet  
    :::image-end:::
    
    Empieza a desarrollar aplicaciones con la API de WebView2.  Para compilar y ejecutar el proyecto, seleccione `F5` .  El proyecto en ejecución muestra una ventana vacía.  
    
    :::image type="complex" source="./media/winforms-emptyapp.png" alt-text="Aplicación vacía" lightbox="./media/winforms-emptyapp.png":::
       Aplicación vacía  
    :::image-end:::
    
## Paso 3: Crear una vista web única  

Agrega una vista web a la aplicación.  

1.  Abra el **Diseñador de Windows Forms**.  
1.  Busque **WebView2 en** el cuadro **de herramientas.**  
    
    > [!NOTE]
    > Si usa Visual Studio 2017, es posible que **WebView2** no se muestre de forma predeterminada en el cuadro **de herramientas.**  Para habilitar el comportamiento, elija **Opciones**de herramientas general > la opción Rellenar automáticamente  >  ****  >  **** el cuadro **de** herramientas en `True` .  
    
    Arrastre y coloque el control **WebView2** en Windows Forms App.
    
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

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrese de que se muestra el control WebView2 [https://www.microsoft.com][|::ref1::|Main] .

:::image type="complex" source="./media/winforms-hellowebview.png" alt-text="hello webview" lightbox="./media/winforms-hellowebview.png":::
   hello webview  
:::image-end:::  

> [!NOTE]
> Si está trabajando en un monitor con valores altos de PPP, es posible que tenga que configurar la aplicación de Windows Forms para [que admita valores altos de PPP.][DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]  

## Paso 4: Controlar eventos de cambio de tamaño de ventana

Agregue algunos controles más a Windows Forms desde el cuadro de herramientas y, a continuación, controle los eventos de cambio de tamaño de ventana correctamente.

1.  En el **Diseñador de Windows Forms,** abra el cuadro de **herramientas**
1.  Arrastre y coloque un **TextBox** en Windows Forms App.  En la **pestaña Propiedades**, asigne el nombre **TextBox** `addressBar` .
1.  Arrastre y coloque un **botón en** Windows Forms App.  Cambie el texto del botón **a y** asigne un nombre al `Go!` botón **en** la `goButton` pestaña **Propiedades**.

    La aplicación debe tener el aspecto de la siguiente imagen en el diseñador.
    
    :::image type="complex" source="./media/winforms-designer.png" alt-text="designer" lightbox="./media/winforms-designer.png":::
       designer  
    :::image-end:::  

1.  En el archivo, define para mantener los controles en su lugar cuando se cambia el tamaño de la `Form1.cs` `Form_Resize` ventana de la aplicación.

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

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrate de que la aplicación muestra una captura de pantalla similar a la siguiente.

:::image type="complex" source="./media/winforms-app.png" alt-text="aplicación" lightbox="./media/winforms-app.png":::
   Aplicación  
:::image-end:::

## Paso 5: Navegación

Agrega la capacidad de permitir a los usuarios cambiar la dirección URL que muestra el control WebView2 agregando una barra de direcciones a la aplicación.

1.  En el `Form1.cs` archivo, para agregar el espacio `CoreWebView2` de nombres, inserte el siguiente fragmento de código en la parte superior.  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1.  En el **Diseñador de Windows Forms,** haga doble clic en el `Go!` botón para crear el método en el `goButton_Click` `Form1.cs` archivo.  Copie y pegue el siguiente fragmento de código dentro de la función.  Ahora, la `goButton_Click` función navega por la vista web hasta la dirección URL especificada en la barra de direcciones.

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Para compilar y ejecutar el proyecto, seleccione `F5` .  Escriba una nueva dirección URL en la barra de direcciones y seleccione **Ir**.  Por ejemplo, escriba `https://www.bing.com` .  Asegúrate de que el control WebView2 navega a la dirección URL.  

> [!NOTE]
> Asegúrese de que se introduce una dirección URL completa en la barra de direcciones.  Se `ArgumentException` produce un error si la dirección URL no comienza con `http://` o `https://`

:::image type="complex" source="./media/winforms-bing.png" alt-text="bing.com" lightbox="./media/winforms-bing.png":::
   bing.com  
:::image-end:::

## Paso 6: Eventos de navegación  

Durante la navegación de páginas web, el control WebView2 genera eventos.  La aplicación que hospeda los controles WebView2 escucha los siguientes eventos.  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  

Para obtener más información, vaya a [Eventos de navegación.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   Eventos de navegación
:::image-end:::

Cuando se produce un error, se producen los siguientes eventos y pueden depender de la navegación a una página web de error.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  

> [!NOTE]
> Si se produce un redireccionamiento HTTP, hay varios `NavigationStarting` eventos en una fila.  

Para demostrar cómo usar estos eventos, empiece por registrar un controlador para que cancele cualquier solicitud que `NavigationStarting` no use HTTPS.  

En el archivo, actualice el constructor para que coincida con el siguiente fragmento de código `Form1.cs` y agregue la `EnsureHttps` función.  

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

En el constructor, EnsureHttps se registra como controlador de eventos en el `NavigationStarting` evento en el control WebView2.  

Para compilar y ejecutar el proyecto, seleccione `F5` .  Asegúrese de que, al navegar a un sitio HTTP, la vista web no cambia.  Sin embargo, WebView navegará a los sitios HTTPS.

## Paso 7: Scripting  

Puedes usar aplicaciones host para insertar código JavaScript en controles WebView2 en tiempo de ejecución.  Puede hacer que WebView ejecute JavaScript arbitrario o agregue scripts de inicialización.  El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a todos los fotogramas secundarios hasta que se quite el JavaScript.  El JavaScript inyectado se ejecuta con intervalos específicos.  

*   Ejecutarlo después de la creación del objeto global.  
*   Ejecutarlo antes de ejecutar cualquier otro script incluido en el documento HTML.  

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

## Paso 8: Comunicación entre contenido de host y web  

El contenido de host y web puede `postMessage` usarse para comunicarse entre sí de la siguiente manera:  

*   El contenido web de un control WebView2 puede `window.chrome.webview.postMessage` usarse para publicar un mensaje en el host.  El host controla el mensaje mediante cualquier registrado `WebMessageReceived` en el host.  
*   Hospeda mensajes de publicación en contenido web en un control WebView2 `CoreWebView2.PostWebMessageAsString` mediante o `CoreWebView2.PostWebMessageAsJSON` .  Estos mensajes se detectan mediante controladores agregados a `window.chrome.webview.addEventListener` .  

El mecanismo de comunicación pasa mensajes desde contenido web al host mediante funcionalidades nativas.  

En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y avisa al usuario de la dirección URL que se muestra en el control WebView2.  

1.  En el `Form1.cs` archivo, actualice el constructor y cree una `InitializeAsync` función que coincida con el siguiente fragmento de código.  La `InitializeAsync` función espera a [EnsureCoreWebView2Async][DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async] porque la inicialización es `CoreWebView2` asincrónica.  

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

En el `Form1.cs` archivo, actualice para `InitializeAsync` que coincida con el siguiente fragmento de código.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Para compilar y ejecutar la aplicación, seleccione `F5` .  Ahora, la barra de direcciones muestra el URI en el control WebView2.  Además, cuando navegas correctamente a una nueva dirección URL, WebView avisa al usuario de la dirección URL que se muestra en webView.  

:::image type="complex" source="./media/winforms-finalapp.png" alt-text="Aplicación final" lightbox="./media/winforms-finalapp.png":::
   Aplicación final  
:::image-end:::

Enhorabuena, has creado tu primera aplicación WebView2.  

## Pasos siguientes  

Para continuar con el aprendizaje sobre WebView2, vaya a los siguientes recursos.  

### Consulte también  

*   Para obtener un ejemplo completo de las capacidades de WebView2, vaya a [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].  
*   Para obtener información detallada sobre la API de WebView2, vaya a la [referencia de la API.][DotnetApiMicrosoftWebWebview2WinformsWebview2]  

## Introducción al equipo de Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Eventos de navegación | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2]: /dotnet/api/microsoft.web.webview2.winforms.webview2 "Clase WebView2 | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Ensurecorewebview2async]: /dotnet/api/microsoft.web.webview2.winforms.webview2.ensurecorewebview2async "Método WebView2.EnsureCoreWebView2Async(CoreWebView2Environment) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Executescriptasync]: /dotnet/api/microsoft.web.webview2.winforms.webview2.executescriptasync "WebView2.Exemétodo cuteScriptAsync(String) | Microsoft Docs"  

[DotnetFrameworkWinformsHighDpiSupportWindowsFormsConfiguringYourWindowsFormsAppForHighDpiSupport]: /dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support "Configuración de la aplicación de Windows Forms para la compatibilidad con valores altos de PPP: compatibilidad con valores altos de PPP en Windows Forms | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 " WebView2 | Desarrollador de Microsoft Edge"  

[MicrosoftMain]: https://www.microsoft.com "Microsoft"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
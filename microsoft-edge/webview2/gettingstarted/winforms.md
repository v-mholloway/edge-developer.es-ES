---
description: Hospedar contenido web en la aplicación de Windows Forms con el control de WebView 2 de Microsoft Edge
title: Vista de WebView 2 de Microsoft Edge para aplicaciones de Windows Forms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, aplicaciones de WinForms, WinForms, Edge, CoreWebView2, control de explorador, ASP.net de Edge, introducción, introducción, .NET, Windows Forms
ms.openlocfilehash: 885524581112a208e1e5134ecd7a6f7446e331ce
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010736"
---
# Introducción a WebView2 en las aplicaciones de Windows Forms (versión preliminar)  

En este artículo, empiece a crear su primera aplicación de WebView2 y obtenga información sobre las características principales de [WebView2 (versión preliminar)](/microsoft-edge/hosting/webview2/index).  Para obtener más información sobre las API individuales, consulta referencia de la [API](../reference/dotnet/0-9-628-reference-webview2.md).  

## Requisitos previos  

Asegúrese de haber instalado la siguiente lista de requisitos previos antes de continuar:  

* [Canal Canarias de Microsoft Edge (cromo)](https://www.microsoftedgeinsider.com/download) instalado en Windows 10, Windows 8,1 o Windows 7. 
* [Visual Studio](https://visualstudio.microsoft.com) 2017 o posterior.

> [!NOTE]
> WebView2 actualmente no es compatible con el diseñador de .NET Core 3.0 [(versión preliminar)](https://visualstudio.microsoft.com/vs/preview).

## Paso 1: crear una aplicación de una sola ventana

Empiece con un proyecto de escritorio básico que contenga una única ventana principal.  

1. Abra **Visual Studio.**

1. Elija **aplicación de Windows Forms .NET Framework** y, a continuación, elija **siguiente**.

    ![NewProject](./media/winforms-newproject.png)

1. Escriba los valores para **el nombre** y la **Ubicación**del proyecto.  Seleccione **.NET Framework 4.6.2** o posterior.  

    ![startproject](./media/winforms-startproj.png)

1. Elija **crear** para crear el proyecto.

## Paso 2: instalar el SDK de WebView2

A continuación, agregue el SDK de WebView2 al proyecto.  Para obtener la vista previa, instala el SDK de WebView2 con Nuget.  

1. Abra el menú contextual en el proyecto \ (haga clic con el botón derecho \) y elija **administrar paquetes NuGet...**.  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="Nuget":::
       Nuget :::image-end:::

1. Escriba `Microsoft.Web.WebView2` en la barra de búsqueda.  Seleccione **Microsoft. Web. WebView2** en los resultados de la búsqueda.  

    > [!IMPORTANT]
    > Asegúrese de que marca la opción **incluir**versión, seleccione un paquete de versión preliminar en **versión**y, a continuación, elija **instalar**.  

    ![Nuget](./media/installnuget.png)

Ya está todo listo para empezar a desarrollar aplicaciones con la API de WebView2.  Seleccione `F5` para compilar y ejecutar el proyecto.  El proyecto en ejecución muestra una ventana vacía.  

![emptyApp](./media/winforms-emptyApp.png)

## Paso 3: crear un único WebView  

A continuación, agregue una vista de vista a la aplicación.  

1. Abra el **Diseñador de Windows Forms**.  
1. Busque **WebView2** en el **cuadro de herramientas**. Arrastre y coloque el control **WebView2** en la aplicación Windows Forms

    ![prácticas](./media/winforms-toolbox.png)

1. Cambie la `Name` propiedad a `webView` .

    ![prácticas](./media/winforms-properties.png)

1. La `Source` propiedad establece el URI inicial que se muestra en el control WebView2. Establezca la propiedad Source en <https://www.microsoft.com>

    ![prácticas](./media/winforms-source.png)

Seleccione `F5` para compilar y ejecutar el proyecto.  Confirme que se muestra el control WebView2 [https://www.microsoft.com](https://www.microsoft.com) .

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> Si está trabajando en un monitor de alta definición de PPP, es posible que tenga que [configurar la aplicación de Windows Forms para una compatibilidad con alta definición de PPP](/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).

## Paso 4: controlar los eventos de ajuste de tamaño de la ventana

Agregue algunos controles más a sus formularios Windows Forms desde el cuadro de herramientas y, a continuación, administre los eventos de tamaño de ventana correctamente.

1. En el **Diseñador de Windows Forms** , abra el **cuadro de herramientas**
1. Arrastre y coloque un **cuadro de texto** en la aplicación de formularios Windows Forms. Asigne un nombre al **cuadro** `addressBar` de texto en la **pestaña propiedades**.
1. Arrastre y coloque un **botón** en la aplicación Windows Forms. Cambie el texto del **botón** a `Go!` y asígnele el nombre **Button** `goButton` de la **pestaña propiedades**.

    La aplicación debe tener un aspecto similar al siguiente en el diseñador:
    
    ![diseñador](./media/winforms-designer.png)

1. En **Form1.CS** define `Form_Resize` para mantener los controles en su lugar cuando se cambie el tamaño de la ventana de la aplicación.

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

Seleccione `F5` para compilar y ejecutar el proyecto.  Confirme que la aplicación se muestra de forma similar a la siguiente captura de pantalla.

![aplicación](./media/winforms-app.png)

## Paso 5: navegación

Agregue una barra de direcciones a la aplicación para permitir a los usuarios que cambien la dirección URL que muestra el control WebView2.

1. En `Form1.cs` Agregar el `CoreWebView2` espacio de nombres, inserte el siguiente fragmento de código en la parte superior de `Form1.cs` .  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

1. En el **Diseñador de Windows Forms**, haga doble clic en el `Go!` botón para crear el `goButton_Click` método `Form1.cs` . Copie y pegue el siguiente fragmento de código dentro de la función. Ahora, la `goButton_Click` función navega por la vista WebView a la dirección URL que se escribe en la barra de direcciones.

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

Seleccione `F5` para compilar y ejecutar el proyecto.  Escriba una nueva dirección URL en la barra de direcciones y haga clic en **ir**.  Por ejemplo, escriba `https://www.bing.com` .  Confirme que el control WebView2 se desplaza hasta la dirección URL.  

> [!NOTE]
> Asegúrese de que se escribe una dirección URL completa en la barra de direcciones. `ArgumentException`Se inicia una si la dirección URL no comienza con `http://` o `https://`

![bing](./media/winforms-bing.png)

## Paso 6: eventos de navegación  

La aplicación que hospeda los controles WebView2 escucha los siguientes eventos provocados por el control WebView2 durante la navegación a páginas Web.  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

Para obtener más información, vea [eventos de navegación](../concepts/navigation-events.md).  

:::image type="complex" source="../media/navigation-events.png" alt-text="Eventos de navegación":::
   Eventos de navegación
:::image-end:::

Cuando se produce un error, se producen los eventos siguientes y puede que dependan de la navegación a una página de error.  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

Cuando hay una redirección de HTTP, hay varios `NavigationStarting` eventos.  

Para mostrar cómo usar estos eventos, comienza registrando un controlador para `NavigationStarting` que cancele todas las solicitudes que no usen https.  

En `Form1.cs` , modifique el constructor como se muestra a continuación y agregue la `EnsureHttps` función.  

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

En el constructor, EnsureHttps se registra como el controlador de eventos en el `NavigationStarting` evento en el control de WebView2.  

Seleccione `F5` para compilar y ejecutar el proyecto. Confirme que, al navegar a un sitio HTTP, la WebView no sufre cambios. Sin embargo, la vista Web se desplazará a sitios HTTPS.

## Paso 7: scripting  

Puede usar aplicaciones host para inyectar código JavaScript en controles WebView2 en tiempo de ejecución.  El JavaScript insertado se aplica a todos los nuevos documentos de nivel superior y a los fotogramas secundarios hasta que se quite el JavaScript.  El código JavaScript insertado se ejecuta después de la creación del objeto global y antes de que se ejecute cualquier otro script incluido en el documento HTML.  

Puede usar scripting para avisar al usuario cuando navegue a un sitio que no es HTTPS.  Modifique la `EnsureHttps` función para que inserte el script en el contenido web con el método [ExecuteScriptAsync]() .  

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

Seleccione `F5` para compilar y ejecutar el proyecto.  Confirme que la aplicación muestra una alerta cuando se desplaza a un sitio que no usa HTTPS.  

![https](./media/winforms-https.png)

## Paso 8: comunicación entre el contenido del host y el Web  

El host y el contenido web pueden comunicarse entre sí mediante las `postMessage` siguientes acciones:  

* El contenido Web de un control WebView2 puede publicar un mensaje en el host mediante `window.chrome.webview.postMessage` .  El anfitrión controla el mensaje con cualquier registro `WebMessageReceived` en el host.  
* Los anfitriones se exponen en el contenido web en un control WebView2 mediante `CoreWebView2.PostWebMessageAsString` o `CoreWebView2.PostWebMessageAsJSON` .  Estos mensajes los detectan los controladores agregados a `window.chrome.webview.addEventListener` .  

Este mecanismo de comunicación permite que el contenido web transmita mensajes al host mediante capacidades nativas.  

En el proyecto, cuando el control WebView2 navega a una dirección URL, muestra la dirección URL en la barra de direcciones y alerta al usuario de la dirección URL que se muestra en el control de WebView2.  

1. En **Form1.CS**, actualice el constructor y cree una `InitializeAsync` función tal como se muestra en el siguiente fragmento de código.  La `InitializeAsync` función espera [EnsureCoreWebView2Async]() porque la inicialización `CoreWebView2` es asincrónica.  

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

1. Después de inicializar **CoreWebView2** , registra un controlador de eventos para responder `WebMessageReceived` .  En `Form1.cs` Update `InitializeAsync` y Add, `UpdateAddressBar` use el siguiente fragmento de código.  

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

1. Para que la vista Web pueda enviar y responder al mensaje Web, después de que `CoreWebView2` se inicialice, el anfitrión inyecta una secuencia de comandos en el contenido web a:  

    1. Envíe la dirección URL al host mediante `postMessage` .
    1. Registre un controlador de eventos para imprimir un mensaje enviado desde el host.  

En `Form1.cs` , actualice `InitializeAsync` tal como se muestra en el siguiente fragmento de código.  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

Seleccione `F5` para compilar y ejecutar la aplicación.  Confirme que la barra de direcciones muestra la dirección URL del sitio que se muestra en la vista Web. Además, cuando navegues correctamente a una nueva dirección URL, WebView avisará al usuario de la dirección URL que se muestra en la vista de vista en WebView.  

![finalapp](./media/winforms-finalapp.png)

¡ Enhorabuena! has creado tu primera WebView2 aplicación.  

## Pasos siguientes 

* Desproteja el [repositorio de WebView2Samples](https://github.com/MicrosoftEdge/WebView2Samples) para obtener un ejemplo completo de las capacidades de WebView2's
* [Consulta la referencia](../reference/winforms/0-9-515/microsoft-web-webview2-winforms-webview2.md) de la API para obtener información más detallada sobre nuestras API
* Desproteja una lista de [recursos de WebView2](../index.md#next-steps) para obtener más información sobre WebView2


## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

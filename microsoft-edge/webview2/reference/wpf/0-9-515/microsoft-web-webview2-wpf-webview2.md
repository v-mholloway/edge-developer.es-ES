---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. WPF. WebView2
ms.openlocfilehash: 2dd7bf1035cf5254f4668070d56d2bd2405f1276
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880265"
---
# <span data-ttu-id="7dfd7-104">Clase Microsoft. Web. WebView2. WPF. WebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="7dfd7-105">Espacio de nombres: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="7dfd7-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="7dfd7-106">Ensamblado: Microsoft.Web.WebView2.Wpf.dll</span><span class="sxs-lookup"><span data-stu-id="7dfd7-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="7dfd7-107">Un control para incrustar contenido web en una aplicación de WPF.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="7dfd7-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="7dfd7-108">Summary</span></span>

 <span data-ttu-id="7dfd7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7dfd7-109">Members</span></span>                        | <span data-ttu-id="7dfd7-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7dfd7-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="7dfd7-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="7dfd7-112">Un contenedor para el evento CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="7dfd7-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="7dfd7-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="7dfd7-114">Este evento se desencadena cuando se ha terminado de inicializar el CoreWebView2 del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="7dfd7-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="7dfd7-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="7dfd7-116">Un contenedor para el evento CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="7dfd7-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="7dfd7-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="7dfd7-118">Un contenedor para el evento CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="7dfd7-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="7dfd7-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="7dfd7-120">Un contenedor para el evento CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="7dfd7-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="7dfd7-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="7dfd7-122">Un contenedor para el evento CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="7dfd7-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="7dfd7-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="7dfd7-124">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="7dfd7-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="7dfd7-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="7dfd7-126">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="7dfd7-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="7dfd7-128">Accede a la funcionalidad completa de la API básica. CoreWebView2 COM.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="7dfd7-129">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="7dfd7-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="7dfd7-130">Obtiene o establece una bolsa de opciones que se usan durante la inicialización de la CoreWebView2 del control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="7dfd7-131">Source</span><span class="sxs-lookup"><span data-stu-id="7dfd7-131">Source</span></span>](#source) | <span data-ttu-id="7dfd7-132">Identificador URI de nivel superior que la vista en pantalla está mostrando (o se muestra cuando finaliza la inicialización de su CoreWebView2).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="7dfd7-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="7dfd7-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="7dfd7-134">Desencadenar de forma explícita la inicialización de la CoreWebView2 del control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="7dfd7-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="7dfd7-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="7dfd7-136">Ejecuta el código de JavaScript desde el parámetro de javaScript en el documento de nivel superior actual representado en la vista de gráfico.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="7dfd7-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="7dfd7-137">GoBack</span></span>](#goback) | <span data-ttu-id="7dfd7-138">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="7dfd7-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="7dfd7-139">GoForward</span></span>](#goforward) | <span data-ttu-id="7dfd7-140">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="7dfd7-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="7dfd7-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="7dfd7-142">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="7dfd7-143">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="7dfd7-143">Reload</span></span>](#reload) | <span data-ttu-id="7dfd7-144">Vuelve a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-144">Reloads the current page.</span></span>
[<span data-ttu-id="7dfd7-145">Detener</span><span class="sxs-lookup"><span data-stu-id="7dfd7-145">Stop</span></span>](#stop) | <span data-ttu-id="7dfd7-146">Detiene todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="7dfd7-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-147">WebView2</span></span>](#webview2) | <span data-ttu-id="7dfd7-148">Crea una nueva instancia de un control WebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-148">Creates a new instance of a WebView2 control.</span></span>

<span data-ttu-id="7dfd7-149">Este control es realmente un contenedor de la API COM de WebView2, en el que puede encontrar documentación aquí: [https://aka.ms/webview2](https://aka.ms/webview2) puede acceder directamente a la interfaz de ICoreWebView2 subyacente y a toda su funcionalidad mediante el acceso a la propiedad CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-149">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="7dfd7-150">Algunas de las funciones COM más comunes también son accesibles directamente a través de métodos de contenedor/propiedades o eventos del control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-150">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="7dfd7-151">Una vez creada, la propiedad CoreWebView2 del control será null.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-151">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="7dfd7-152">Esto se debe a que la creación de CoreWebView2 es una operación costosa que implica cosas como iniciar procesos de explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-152">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="7dfd7-153">Hay dos maneras de crear el CoreWebView2:1) llama al método EnsureCoreWebView2Async.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-153">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="7dfd7-154">Esto se conoce como inicialización explícita.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-154">This is referred to as explicit initialization.</span></span> <span data-ttu-id="7dfd7-155">2) establezca la propiedad Source (que puede realizarse desde el marcado, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-155">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="7dfd7-156">Esto se conoce como inicialización implícita.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-156">This is referred to as implicit initialization.</span></span> <span data-ttu-id="7dfd7-157">Ambas opciones iniciarán la inicialización en segundo plano y regresarán a la persona que llama sin esperar a que finalice.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-157">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="7dfd7-158">Para especificar las opciones relacionadas con el proceso de inicialización, pase su propio CoreWebView2Environment a EnsureCoreWebView2Async o establezca la propiedad CreationProperties del control antes de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-158">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="7dfd7-159">Cuando la inicialización ha finalizado (independientemente de cómo se haya activado), se iniciarán las siguientes acciones, en este orden: 1) se invocará el evento CoreWebView2Ready del control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-159">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="7dfd7-160">Si necesita realizar operaciones de configuración una vez en el CoreWebView2 antes de su uso, debe hacerlo en un controlador para ese evento.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-160">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="7dfd7-161">2) si un URI se ha establecido en la propiedad de origen, el control comenzará a navegar en él en segundo plano (es decir, los pasos continuarán sin esperar a que finalice la navegación).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-161">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="7dfd7-162">3) la tarea devuelta de EnsureCoreWebView2Async se completará.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-162">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="7dfd7-163">Para obtener más información sobre cualquiera de los métodos, propiedades o eventos implicados en el proceso de inicialización, consulte su documentación específica.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-163">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="7dfd7-164">Debido a que el CoreWebView2 del control es un objeto muy pesado (posiblemente responsable de varios procesos en ejecución y megabytes de espacio en disco), el control implementa IDisposable para proporcionar un medio explícito para liberarlo.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-164">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="7dfd7-165">Al llamar a Dispose, se liberará el CoreWebView2 y sus recursos subyacentes (excepto los que también usan otras webviews), y se restablecerá CoreWebView2 a NULL.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-165">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="7dfd7-166">Una vez que se haya llamado a Dispose, CoreWebView2 no se podrá reinicializar y cualquier intento de usar la funcionalidad que lo requiera iniciará una ObjectDisposedException.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-166">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="7dfd7-167">Tenga en cuenta que este control extiende HwndHost para insertar Windows que reside fuera del ecosistema de WPF.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-167">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="7dfd7-168">Esto tiene algunas implicaciones en relación con el comportamiento de entrada y salida del control, así como con la funcionalidad que "hereda" de UIElement y FrameworkElement.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-168">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="7dfd7-169">Para obtener más información, consulta la documentación de interoperabilidad de HwndHost y WPF/Win32:</span><span class="sxs-lookup"><span data-stu-id="7dfd7-169">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="7dfd7-170">Miembros</span><span class="sxs-lookup"><span data-stu-id="7dfd7-170">Members</span></span>

#### <span data-ttu-id="7dfd7-171">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="7dfd7-171">ContentLoading</span></span> 

<span data-ttu-id="7dfd7-172">Un contenedor para el evento CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-172">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="7dfd7-173">evento público EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-173">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="7dfd7-174">La única diferencia entre este evento y CoreWebView2. ContentLoading es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-174">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="7dfd7-175">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. ContentLoading recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-175">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="7dfd7-176">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="7dfd7-176">CoreWebView2Ready</span></span> 

<span data-ttu-id="7dfd7-177">Este evento se desencadena cuando se ha terminado de inicializar el CoreWebView2 del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-177">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="7dfd7-178">evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-178">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="7dfd7-179">Debe controlar este evento si necesita realizar operaciones de configuración una vez en el CoreWebView2 el que desea afectar a todos sus usos (por ejemplo, agregar controladores de eventos, configurar valores, instalar scripts de creación de documentos, agregar objetos host).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-179">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="7dfd7-180">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-180">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="7dfd7-181">Este evento no proporciona ningún argumento, y el remitente será el control WebView2, cuya propiedad CoreWebView2 será válida (es decir, no NULL) por primera vez.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-181">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="7dfd7-182">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="7dfd7-182">NavigationCompleted</span></span> 

<span data-ttu-id="7dfd7-183">Un contenedor para el evento CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-183">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="7dfd7-184">evento público EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-184">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="7dfd7-185">La única diferencia entre este evento y CoreWebView2. NavigationCompleted es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-185">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="7dfd7-186">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. NavigationCompleted recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-186">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="7dfd7-187">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="7dfd7-187">NavigationStarting</span></span> 

<span data-ttu-id="7dfd7-188">Un contenedor para el evento CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-188">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="7dfd7-189">evento público EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-189">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="7dfd7-190">La única diferencia entre este evento y CoreWebView2. NavigationStarting es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-190">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="7dfd7-191">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. NavigationStarting recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-191">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="7dfd7-192">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="7dfd7-192">SourceChanged</span></span> 

<span data-ttu-id="7dfd7-193">Un contenedor para el evento CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-193">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="7dfd7-194">evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-194">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="7dfd7-195">La única diferencia entre este evento y CoreWebView2. SourceChanged es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-195">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="7dfd7-196">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. SourceChanged recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-196">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="7dfd7-197">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="7dfd7-197">WebMessageReceived</span></span> 

<span data-ttu-id="7dfd7-198">Un contenedor para el evento CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-198">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="7dfd7-199">evento público EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-199">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="7dfd7-200">La única diferencia entre este evento y CoreWebView2. WebMessageReceived es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-200">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="7dfd7-201">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. WebMessageReceived recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-201">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="7dfd7-202">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="7dfd7-202">CanGoBack</span></span> 

<span data-ttu-id="7dfd7-203">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-203">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="7dfd7-204">Public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-204">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="7dfd7-205">Contenedor de la propiedad CoreWebView2. CanGoBack de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-205">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="7dfd7-206">Si CoreWebView2 aún no se ha inicializado, devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-206">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="7dfd7-207">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="7dfd7-207">CanGoForward</span></span> 

<span data-ttu-id="7dfd7-208">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-208">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="7dfd7-209">Public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-209">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="7dfd7-210">Contenedor de la propiedad CoreWebView2. CanGoForward de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-210">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="7dfd7-211">Si CoreWebView2 aún no se ha inicializado, devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-211">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="7dfd7-212">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-212">CoreWebView2</span></span> 

<span data-ttu-id="7dfd7-213">Accede a la funcionalidad completa de la API básica. CoreWebView2 COM.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-213">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="7dfd7-214">CoreWebView2 pública [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-214">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="7dfd7-215">Devuelve null hasta que se haya completado la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-215">Returns null until initialization has completed.</span></span> <span data-ttu-id="7dfd7-216">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-216">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="7dfd7-217">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-217">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="7dfd7-218">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-218">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="7dfd7-219">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-219">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="7dfd7-220">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-220">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-221">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="7dfd7-221">CreationProperties</span></span> 

<span data-ttu-id="7dfd7-222">Obtiene o establece una bolsa de opciones que se usan durante la inicialización de la CoreWebView2 del control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-222">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="7dfd7-223">CoreWebView2CreationProperties pública [CreationProperties](#creationproperties)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-223">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="7dfd7-224">El establecimiento de esta propiedad no funcionará después de que se haya iniciado la inicialización de la CoreWebView2 del control (se conservará el valor anterior).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-224">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="7dfd7-225">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-225">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="7dfd7-226">Source</span><span class="sxs-lookup"><span data-stu-id="7dfd7-226">Source</span></span> 

<span data-ttu-id="7dfd7-227">Identificador URI de nivel superior que la vista en pantalla está mostrando (o se muestra cuando finaliza la inicialización de su CoreWebView2).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-227">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="7dfd7-228">[origen](#source) de URI público</span><span class="sxs-lookup"><span data-stu-id="7dfd7-228">public Uri [Source](#source)</span></span>

<span data-ttu-id="7dfd7-229">En general, la obtención de esta propiedad es equivalente a la propiedad CoreWebView2. Source de CoreWebView2 y la configuración de esta propiedad es equivalente a llamar al método CoreWebView2. Navigate en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-229">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="7dfd7-230">Si se obtiene esta propiedad antes de que se haya inicializado CoreWebView2, se recuperará el último URI que se ha establecido en él.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-230">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="7dfd7-231">Si se establece esta propiedad antes de que se haya inicializado CoreWebView2, la inicialización se iniciará en el fondo (si aún no está en curso), después de la cual el WebView2 se desplazará al identificador URI especificado.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-231">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="7dfd7-232">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-232">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="7dfd7-233">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-233">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="7dfd7-234">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-234">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-235">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="7dfd7-235">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="7dfd7-236">Desencadenar de forma explícita la inicialización de la CoreWebView2 del control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-236">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="7dfd7-237">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tareas públicas (entorno de CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-237">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="7dfd7-238">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-238">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="7dfd7-239">Parameters</span><span class="sxs-lookup"><span data-stu-id="7dfd7-239">Parameters</span></span>
* `environment` <span data-ttu-id="7dfd7-240">Un CoreWebView2Environment creado previamente que se debe usar para crear el CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-240">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="7dfd7-241">Crear su propio entorno le proporciona control sobre varias opciones que afectan a la forma en que se inicializa CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-241">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="7dfd7-242">Si pasas un entorno a este método, se invalidarán los valores especificados en la propiedad CreationProperties.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-242">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="7dfd7-243">Si pasa null (el valor predeterminado) y no se ha establecido ningún valor en CreationProperties, se creará un entorno predeterminado y se usará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-243">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="7dfd7-244">Devuelve</span><span class="sxs-lookup"><span data-stu-id="7dfd7-244">Returns</span></span>
<span data-ttu-id="7dfd7-245">Una tarea que representa el proceso de inicialización en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-245">A Task that represents the background initialization process.</span></span> <span data-ttu-id="7dfd7-246">Cuando la tarea se complete, la propiedad CoreWebView2 estará disponible para su uso (es decir, no NULL).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-246">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="7dfd7-247">Observe que el evento CoreWebView2Ready del control se invocará antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-247">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="7dfd7-248">Llamar a este método los tiempos adicionales no tendrán efecto (se ignora cualquier entorno especificado) y devolverán la misma tarea que la primera llamada.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-248">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="7dfd7-249">La llamada a este método después de la inicialización se ha desencadenado de forma implícita mediante la configuración de la propiedad Source no tendrá ningún efecto (se ignora cualquier entorno especificado) y simplemente devuelva una tarea que represente la inicialización que ya está en curso.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-249">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="7dfd7-250">Ten en cuenta que aunque este método es asincrónico y devuelve una tarea, aún debe llamarse en el subproceso de la interfaz de usuario, como la mayoría de las funciones públicas de la mayoría de los controles de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-250">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="7dfd7-251">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-251">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="7dfd7-252">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-252">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="7dfd7-253">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-253">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="7dfd7-254">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-255">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="7dfd7-255">ExecuteScriptAsync</span></span> 

<span data-ttu-id="7dfd7-256">Ejecuta el código de JavaScript desde el parámetro de javaScript en el documento de nivel superior actual representado en la vista de gráfico.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-256">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="7dfd7-257">Tarea asincrónica pública< cadena > [ExecuteScriptAsync](#executescriptasync)(cadena JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-257">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="7dfd7-258">Equivale a llamar a CoreWebView2.ExecuteScriptAsync en CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-258">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="7dfd7-259">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-259">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="7dfd7-260">Se produce si CoreWebView2 todavía no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-260">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="7dfd7-261">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-261">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="7dfd7-262">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-262">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="7dfd7-263">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-263">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-264">GoBack</span><span class="sxs-lookup"><span data-stu-id="7dfd7-264">GoBack</span></span> 

<span data-ttu-id="7dfd7-265">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-265">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="7dfd7-266">public void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="7dfd7-266">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="7dfd7-267">Equivale a llamar a CoreWebView2. GoBack en CoreWebView2 si CoreWebView2 no se ha inicializado todavía no hace nada.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-267">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="7dfd7-268">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-268">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="7dfd7-269">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-269">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="7dfd7-270">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-270">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="7dfd7-271">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-271">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-272">GoForward</span><span class="sxs-lookup"><span data-stu-id="7dfd7-272">GoForward</span></span> 

<span data-ttu-id="7dfd7-273">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-273">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="7dfd7-274">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="7dfd7-274">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="7dfd7-275">Equivale a llamar a CoreWebView2. GoForward en CoreWebView2 si CoreWebView2 no se ha inicializado aún no hace nada.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-275">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="7dfd7-276">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-276">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="7dfd7-277">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-277">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="7dfd7-278">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-278">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="7dfd7-279">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-279">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-280">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="7dfd7-280">NavigateToString</span></span> 

<span data-ttu-id="7dfd7-281">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-281">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="7dfd7-282">public void [NavigateToString](#navigatetostring)(String htmlContent)</span><span class="sxs-lookup"><span data-stu-id="7dfd7-282">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="7dfd7-283">Equivale a llamar a CoreWebView2. NavigateToString en CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-283">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="7dfd7-284">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-284">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="7dfd7-285">Se produce si CoreWebView2 todavía no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-285">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="7dfd7-286">" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-286">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="7dfd7-287">Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-287">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-288">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="7dfd7-288">Reload</span></span> 

<span data-ttu-id="7dfd7-289">Vuelve a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-289">Reloads the current page.</span></span>

> <span data-ttu-id="7dfd7-290">public void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="7dfd7-290">public void [Reload](#reload)()</span></span>

<span data-ttu-id="7dfd7-291">Equivale a llamar a CoreWebView2. Reload en CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-291">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="7dfd7-292">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-292">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="7dfd7-293">Se produce si CoreWebView2 todavía no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-293">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="7dfd7-294">" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-294">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="7dfd7-295">Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-295">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-296">Detener</span><span class="sxs-lookup"><span data-stu-id="7dfd7-296">Stop</span></span> 

<span data-ttu-id="7dfd7-297">Detiene todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-297">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="7dfd7-298">public void [Stop](#stop)()</span><span class="sxs-lookup"><span data-stu-id="7dfd7-298">public void [Stop](#stop)()</span></span>

<span data-ttu-id="7dfd7-299">Equivale a llamar a CoreWebView2. STOP en CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-299">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="7dfd7-300">Excepciones</span><span class="sxs-lookup"><span data-stu-id="7dfd7-300">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="7dfd7-301">Se produce si CoreWebView2 todavía no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-301">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="7dfd7-302">" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="7dfd7-302">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="7dfd7-303">Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-303">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="7dfd7-304">WebView2</span><span class="sxs-lookup"><span data-stu-id="7dfd7-304">WebView2</span></span> 

<span data-ttu-id="7dfd7-305">Crea una nueva instancia de un control WebView2.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-305">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="7dfd7-306">[WebView2](#webview2)pública ()</span><span class="sxs-lookup"><span data-stu-id="7dfd7-306">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="7dfd7-307">Ten en cuenta que la CoreWebView2 del control será null hasta que se inicialice.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-307">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="7dfd7-308">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-308">See the WebView2 class documentation for an initialization overview.</span></span>


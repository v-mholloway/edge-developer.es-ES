---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: f2c3bcb5334abc907a838971ebc1773b6485194f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655149"
---
# <span data-ttu-id="8bbe1-104">Clase Microsoft. Web. WebView2. WPF. WebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="8bbe1-105">Espacio de nombres: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="8bbe1-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="8bbe1-106">Ensamblado: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="8bbe1-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="8bbe1-107">Un control para incrustar contenido web en una aplicación de WPF.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="8bbe1-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="8bbe1-108">Summary</span></span>

 <span data-ttu-id="8bbe1-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8bbe1-109">Members</span></span>                        | <span data-ttu-id="8bbe1-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8bbe1-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="8bbe1-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="8bbe1-112">Un contenedor para el evento CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="8bbe1-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="8bbe1-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="8bbe1-114">Este evento se desencadena cuando se ha terminado de inicializar el CoreWebView2 del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="8bbe1-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="8bbe1-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="8bbe1-116">Un contenedor para el evento CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="8bbe1-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="8bbe1-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="8bbe1-118">Un contenedor para el evento CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="8bbe1-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="8bbe1-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="8bbe1-120">Un contenedor para el evento CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="8bbe1-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="8bbe1-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="8bbe1-122">Un contenedor para el evento CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="8bbe1-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="8bbe1-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="8bbe1-124">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="8bbe1-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="8bbe1-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="8bbe1-126">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="8bbe1-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="8bbe1-128">Accede a la funcionalidad completa de la API básica. CoreWebView2 COM.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="8bbe1-129">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="8bbe1-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="8bbe1-130">Obtiene o establece una bolsa de opciones que se usan durante la inicialización de la CoreWebView2 del control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="8bbe1-131">Source</span><span class="sxs-lookup"><span data-stu-id="8bbe1-131">Source</span></span>](#source) | <span data-ttu-id="8bbe1-132">Identificador URI de nivel superior que la vista en pantalla está mostrando (o se muestra cuando finaliza la inicialización de su CoreWebView2).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="8bbe1-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="8bbe1-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="8bbe1-134">Desencadenar de forma explícita la inicialización de la CoreWebView2 del control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="8bbe1-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="8bbe1-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="8bbe1-136">Ejecuta el código de JavaScript desde el parámetro de javaScript en el documento de nivel superior actual representado en la vista de gráfico.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="8bbe1-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="8bbe1-137">GoBack</span></span>](#goback) | <span data-ttu-id="8bbe1-138">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="8bbe1-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="8bbe1-139">GoForward</span></span>](#goforward) | <span data-ttu-id="8bbe1-140">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="8bbe1-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="8bbe1-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="8bbe1-142">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="8bbe1-143">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="8bbe1-143">Reload</span></span>](#reload) | <span data-ttu-id="8bbe1-144">Vuelve a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-144">Reloads the current page.</span></span>
[<span data-ttu-id="8bbe1-145">Detener</span><span class="sxs-lookup"><span data-stu-id="8bbe1-145">Stop</span></span>](#stop) | <span data-ttu-id="8bbe1-146">Detiene todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="8bbe1-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-147">WebView2</span></span>](#webview2) | <span data-ttu-id="8bbe1-148">Crea una nueva instancia de un control WebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-148">Creates a new instance of a WebView2 control.</span></span>
[<span data-ttu-id="8bbe1-149">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="8bbe1-149">BuildWindowCore</span></span>](#buildwindowcore) | <span data-ttu-id="8bbe1-150">Esto se ha invalidado de HwndHost y se le llama para que podamos crear nuestro HWND.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-150">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>
[<span data-ttu-id="8bbe1-151">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="8bbe1-151">DestroyWindowCore</span></span>](#destroywindowcore) | <span data-ttu-id="8bbe1-152">Esto se invalida en HwndHost y se llama para indicarnos que destruya nuestro HWND.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-152">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>
[<span data-ttu-id="8bbe1-153">Dispose</span><span class="sxs-lookup"><span data-stu-id="8bbe1-153">Dispose</span></span>](#dispose) | <span data-ttu-id="8bbe1-154">La clase base llama a esta función de acuerdo con la implementación típica del patrón IDispose.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-154">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>
[<span data-ttu-id="8bbe1-155">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="8bbe1-155">HasFocusWithinCore</span></span>](#hasfocuswithincore) | <span data-ttu-id="8bbe1-156">Esto se invalida en HwndHost y se llama cuando WPF necesita saber si el foco está en nuestro control/ventana.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-156">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>
[<span data-ttu-id="8bbe1-157">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="8bbe1-157">OnKeyDown</span></span>](#onkeydown) | <span data-ttu-id="8bbe1-158">Esto se invalida de UIElement y se llama para permitirnos controlar la entrada de presión de teclas.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-158">This is overridden from UIElement and called to allow us to handle key press input.</span></span>
[<span data-ttu-id="8bbe1-159">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="8bbe1-159">OnKeyUp</span></span>](#onkeyup) | <span data-ttu-id="8bbe1-160">Consulta OnKeyDown.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-160">See OnKeyDown.</span></span>
[<span data-ttu-id="8bbe1-161">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="8bbe1-161">OnPreviewKeyDown</span></span>](#onpreviewkeydown) | <span data-ttu-id="8bbe1-162">Esta es la "vista previa" (es decir,</span><span class="sxs-lookup"><span data-stu-id="8bbe1-162">This is the "Preview" (i.e.</span></span>
[<span data-ttu-id="8bbe1-163">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="8bbe1-163">OnPreviewKeyUp</span></span>](#onpreviewkeyup) | <span data-ttu-id="8bbe1-164">Consulta OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-164">See OnPreviewKeyDown.</span></span>
[<span data-ttu-id="8bbe1-165">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="8bbe1-165">OnWindowPositionChanged</span></span>](#onwindowpositionchanged) | <span data-ttu-id="8bbe1-166">Esto se invalida desde HwndHost y se llama cuando la ubicación de nuestro control ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-166">This is overridden from HwndHost and called when our control's location has changed.</span></span>
[<span data-ttu-id="8bbe1-167">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="8bbe1-167">TabIntoCore</span></span>](#tabintocore) | <span data-ttu-id="8bbe1-168">Esto se invalida de HwndHost y se le llama para informarnos que la tabulación ha provocado que el foco se mueva a nuestro control/ventana.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-168">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

<span data-ttu-id="8bbe1-169">Este control es realmente un contenedor de la API COM de WebView2, en el que puede encontrar documentación aquí: [https://aka.ms/webview2](https://aka.ms/webview2) puede acceder directamente a la interfaz de ICoreWebView2 subyacente y a toda su funcionalidad mediante el acceso a la propiedad CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-169">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="8bbe1-170">Algunas de las funciones COM más comunes también son accesibles directamente a través de métodos de contenedor/propiedades o eventos del control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-170">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="8bbe1-171">Una vez creada, la propiedad CoreWebView2 del control será null.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-171">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="8bbe1-172">Esto se debe a que la creación de CoreWebView2 es una operación costosa que implica cosas como iniciar procesos de explorador Edge.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-172">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="8bbe1-173">Hay dos maneras de crear el CoreWebView2:1) llama al método EnsureCoreWebView2Async.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-173">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="8bbe1-174">Esto se conoce como inicialización explícita.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-174">This is referred to as explicit initialization.</span></span> <span data-ttu-id="8bbe1-175">2) establezca la propiedad Source (que puede realizarse desde el marcado, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-175">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="8bbe1-176">Esto se conoce como inicialización implícita.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-176">This is referred to as implicit initialization.</span></span> <span data-ttu-id="8bbe1-177">Ambas opciones iniciarán la inicialización en segundo plano y regresarán a la persona que llama sin esperar a que finalice.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-177">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="8bbe1-178">Para especificar las opciones relacionadas con el proceso de inicialización, pase su propio CoreWebView2Environment a EnsureCoreWebView2Async o establezca la propiedad CreationProperties del control antes de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-178">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="8bbe1-179">Cuando la inicialización ha finalizado (independientemente de cómo se haya activado), se iniciarán las siguientes acciones, en este orden: 1) se invocará el evento CoreWebView2Ready del control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-179">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="8bbe1-180">Si necesita realizar operaciones de configuración una vez en el CoreWebView2 antes de su uso, debe hacerlo en un controlador para ese evento.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-180">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="8bbe1-181">2) si un URI se ha establecido en la propiedad de origen, el control comenzará a navegar en él en segundo plano (es decir, los pasos continuarán sin esperar a que finalice la navegación).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-181">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="8bbe1-182">3) la tarea devuelta de EnsureCoreWebView2Async se completará.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-182">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="8bbe1-183">Para obtener más información sobre cualquiera de los métodos, propiedades o eventos implicados en el proceso de inicialización, consulte su documentación específica.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-183">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="8bbe1-184">Debido a que el CoreWebView2 del control es un objeto muy pesado (posiblemente responsable de varios procesos en ejecución y megabytes de espacio en disco), el control implementa IDisposable para proporcionar un medio explícito para liberarlo.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-184">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="8bbe1-185">Al llamar a Dispose, se liberará el CoreWebView2 y sus recursos subyacentes (excepto los que también usan otras webviews), y se restablecerá CoreWebView2 a NULL.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-185">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="8bbe1-186">Una vez que se haya llamado a Dispose, CoreWebView2 no se podrá reinicializar y cualquier intento de usar la funcionalidad que lo requiera iniciará una ObjectDisposedException.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-186">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="8bbe1-187">Tenga en cuenta que este control extiende HwndHost para insertar Windows que reside fuera del ecosistema de WPF.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-187">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="8bbe1-188">Esto tiene algunas implicaciones en relación con el comportamiento de entrada y salida del control, así como con la funcionalidad que "hereda" de UIElement y FrameworkElement.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-188">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="8bbe1-189">Para obtener más información, consulta la documentación de interoperabilidad de HwndHost y WPF/Win32:</span><span class="sxs-lookup"><span data-stu-id="8bbe1-189">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="8bbe1-190">Miembros</span><span class="sxs-lookup"><span data-stu-id="8bbe1-190">Members</span></span>

#### <span data-ttu-id="8bbe1-191">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="8bbe1-191">ContentLoading</span></span> 

<span data-ttu-id="8bbe1-192">Un contenedor para el evento CoreWebView2. ContentLoading de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-192">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="8bbe1-193">evento público EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-193">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="8bbe1-194">La única diferencia entre este evento y CoreWebView2. ContentLoading es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-194">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8bbe1-195">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. ContentLoading recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-195">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8bbe1-196">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="8bbe1-196">CoreWebView2Ready</span></span> 

<span data-ttu-id="8bbe1-197">Este evento se desencadena cuando se ha terminado de inicializar el CoreWebView2 del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-197">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="8bbe1-198">evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-198">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="8bbe1-199">Debe controlar este evento si necesita realizar operaciones de configuración una vez en el CoreWebView2 el que desea afectar a todos sus usos (por ejemplo, agregar controladores de eventos, configurar valores, instalar scripts de creación de documentos, agregar objetos host).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-199">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="8bbe1-200">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-200">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="8bbe1-201">Este evento no proporciona ningún argumento, y el remitente será el control WebView2, cuya propiedad CoreWebView2 será válida (es decir, no NULL) por primera vez.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-201">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="8bbe1-202">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="8bbe1-202">NavigationCompleted</span></span> 

<span data-ttu-id="8bbe1-203">Un contenedor para el evento CoreWebView2. NavigationCompleted de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-203">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="8bbe1-204">evento público EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-204">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="8bbe1-205">La única diferencia entre este evento y CoreWebView2. NavigationCompleted es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-205">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8bbe1-206">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. NavigationCompleted recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-206">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8bbe1-207">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="8bbe1-207">NavigationStarting</span></span> 

<span data-ttu-id="8bbe1-208">Un contenedor para el evento CoreWebView2. NavigationStarting de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-208">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="8bbe1-209">evento público EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-209">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="8bbe1-210">La única diferencia entre este evento y CoreWebView2. NavigationStarting es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-210">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8bbe1-211">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. NavigationStarting recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-211">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8bbe1-212">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="8bbe1-212">SourceChanged</span></span> 

<span data-ttu-id="8bbe1-213">Un contenedor para el evento CoreWebView2. SourceChanged de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-213">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="8bbe1-214">evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-214">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="8bbe1-215">La única diferencia entre este evento y CoreWebView2. SourceChanged es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-215">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8bbe1-216">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. SourceChanged recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-216">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8bbe1-217">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="8bbe1-217">WebMessageReceived</span></span> 

<span data-ttu-id="8bbe1-218">Un contenedor para el evento CoreWebView2. WebMessageReceived de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-218">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="8bbe1-219">evento público EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-219">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="8bbe1-220">La única diferencia entre este evento y CoreWebView2. WebMessageReceived es el primer parámetro que se pasa a los controladores.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-220">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="8bbe1-221">Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. WebMessageReceived recibirán la instancia de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-221">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="8bbe1-222">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="8bbe1-222">CanGoBack</span></span> 

<span data-ttu-id="8bbe1-223">Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-223">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="8bbe1-224">Public bool [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-224">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="8bbe1-225">Contenedor de la propiedad CoreWebView2. CanGoBack de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-225">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="8bbe1-226">Si CoreWebView2 aún no se ha inicializado, devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-226">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="8bbe1-227">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="8bbe1-227">CanGoForward</span></span> 

<span data-ttu-id="8bbe1-228">Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-228">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="8bbe1-229">Public bool [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-229">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="8bbe1-230">Contenedor de la propiedad CoreWebView2. CanGoForward de CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-230">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="8bbe1-231">Si CoreWebView2 aún no se ha inicializado, devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-231">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="8bbe1-232">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-232">CoreWebView2</span></span> 

<span data-ttu-id="8bbe1-233">Accede a la funcionalidad completa de la API básica. CoreWebView2 COM.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-233">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="8bbe1-234">CoreWebView2 pública [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-234">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="8bbe1-235">Devuelve null hasta que se haya completado la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-235">Returns null until initialization has completed.</span></span> <span data-ttu-id="8bbe1-236">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-236">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="8bbe1-237">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-237">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8bbe1-238">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-238">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8bbe1-239">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-239">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8bbe1-240">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-240">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-241">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="8bbe1-241">CreationProperties</span></span> 

<span data-ttu-id="8bbe1-242">Obtiene o establece una bolsa de opciones que se usan durante la inicialización de la CoreWebView2 del control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-242">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="8bbe1-243">CoreWebView2CreationProperties pública [CreationProperties](#creationproperties)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-243">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="8bbe1-244">El establecimiento de esta propiedad no funcionará después de que se haya iniciado la inicialización de la CoreWebView2 del control (se conservará el valor anterior).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-244">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="8bbe1-245">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-245">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="8bbe1-246">Source</span><span class="sxs-lookup"><span data-stu-id="8bbe1-246">Source</span></span> 

<span data-ttu-id="8bbe1-247">Identificador URI de nivel superior que la vista en pantalla está mostrando (o se muestra cuando finaliza la inicialización de su CoreWebView2).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-247">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="8bbe1-248">[origen](#source) de URI público</span><span class="sxs-lookup"><span data-stu-id="8bbe1-248">public Uri [Source](#source)</span></span>

<span data-ttu-id="8bbe1-249">En general, la obtención de esta propiedad es equivalente a la propiedad CoreWebView2. Source de CoreWebView2 y la configuración de esta propiedad es equivalente a llamar al método CoreWebView2. Navigate en CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-249">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="8bbe1-250">Si se obtiene esta propiedad antes de que se haya inicializado CoreWebView2, se recuperará el último URI que se ha establecido en él.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-250">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="8bbe1-251">Si se establece esta propiedad antes de que se haya inicializado CoreWebView2, la inicialización se iniciará en el fondo (si aún no está en curso), después de la cual el WebView2 se desplazará al identificador URI especificado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-251">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="8bbe1-252">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-252">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="8bbe1-253">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-253">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="8bbe1-254">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-255">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="8bbe1-255">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="8bbe1-256">Desencadenar de forma explícita la inicialización de la CoreWebView2 del control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-256">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="8bbe1-257">[EnsureCoreWebView2Async](#ensurecorewebview2async)de tareas públicas (entorno de CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-257">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="8bbe1-258">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-258">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="8bbe1-259">Parameters</span><span class="sxs-lookup"><span data-stu-id="8bbe1-259">Parameters</span></span>
* `environment` <span data-ttu-id="8bbe1-260">Un CoreWebView2Environment creado previamente que se debe usar para crear el CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-260">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="8bbe1-261">Crear su propio entorno le proporciona control sobre varias opciones que afectan a la forma en que se inicializa CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-261">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="8bbe1-262">Si pasas un entorno a este método, se invalidarán los valores especificados en la propiedad CreationProperties.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-262">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="8bbe1-263">Si pasa null (el valor predeterminado) y no se ha establecido ningún valor en CreationProperties, se creará un entorno predeterminado y se usará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-263">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="8bbe1-264">Devuelve</span><span class="sxs-lookup"><span data-stu-id="8bbe1-264">Returns</span></span>
<span data-ttu-id="8bbe1-265">Una tarea que representa el proceso de inicialización en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-265">A Task that represents the background initialization process.</span></span> <span data-ttu-id="8bbe1-266">Cuando la tarea se complete, la propiedad CoreWebView2 estará disponible para su uso (es decir, no NULL).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-266">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="8bbe1-267">Observe que el evento CoreWebView2Ready del control se invocará antes de que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-267">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="8bbe1-268">Llamar a este método los tiempos adicionales no tendrán efecto (se ignora cualquier entorno especificado) y devolverán la misma tarea que la primera llamada.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-268">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="8bbe1-269">La llamada a este método después de la inicialización se ha desencadenado de forma implícita mediante la configuración de la propiedad Source no tendrá ningún efecto (se ignora cualquier entorno especificado) y simplemente devuelva una tarea que represente la inicialización que ya está en curso.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-269">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="8bbe1-270">Ten en cuenta que aunque este método es asincrónico y devuelve una tarea, aún debe llamarse en el subproceso de la interfaz de usuario, como la mayoría de las funciones públicas de la mayoría de los controles de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-270">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="8bbe1-271">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-271">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8bbe1-272">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-272">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8bbe1-273">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-273">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8bbe1-274">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-274">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-275">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="8bbe1-275">ExecuteScriptAsync</span></span> 

<span data-ttu-id="8bbe1-276">Ejecuta el código de JavaScript desde el parámetro de javaScript en el documento de nivel superior actual representado en la vista de gráfico.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-276">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="8bbe1-277">Tarea asincrónica pública< cadena > [ExecuteScriptAsync](#executescriptasync)(cadena JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-277">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="8bbe1-278">Equivale a llamar a CoreWebView2. ExecuteScriptAsync en CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-278">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="8bbe1-279">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-279">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8bbe1-280">Se produce si CoreWebView2 todavía no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-280">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="8bbe1-281">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-281">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8bbe1-282">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-282">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8bbe1-283">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-283">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-284">GoBack</span><span class="sxs-lookup"><span data-stu-id="8bbe1-284">GoBack</span></span> 

<span data-ttu-id="8bbe1-285">Navega por la vista Web a la página anterior del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-285">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="8bbe1-286">public void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="8bbe1-286">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="8bbe1-287">Equivale a llamar a CoreWebView2. GoBack en CoreWebView2 si CoreWebView2 no se ha inicializado todavía no hace nada.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-287">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="8bbe1-288">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-288">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8bbe1-289">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-289">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8bbe1-290">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-290">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8bbe1-291">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-291">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-292">GoForward</span><span class="sxs-lookup"><span data-stu-id="8bbe1-292">GoForward</span></span> 

<span data-ttu-id="8bbe1-293">Navega por la vista Web a la página siguiente del historial de navegación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-293">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="8bbe1-294">public void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="8bbe1-294">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="8bbe1-295">Equivale a llamar a CoreWebView2. GoForward en CoreWebView2 si CoreWebView2 no se ha inicializado aún no hace nada.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-295">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="8bbe1-296">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-296">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8bbe1-297">Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-297">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="8bbe1-298">Para obtener más información, consulta DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-298">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="8bbe1-299">Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-299">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-300">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="8bbe1-300">NavigateToString</span></span> 

<span data-ttu-id="8bbe1-301">Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-301">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="8bbe1-302">public void [NavigateToString](#navigatetostring)(String htmlContent)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-302">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="8bbe1-303">Equivale a llamar a CoreWebView2. NavigateToString en CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-303">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="8bbe1-304">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-304">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8bbe1-305">Se produce si CoreWebView2 todavía no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-305">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="8bbe1-306">" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-306">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="8bbe1-307">Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-307">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-308">Volver a cargar</span><span class="sxs-lookup"><span data-stu-id="8bbe1-308">Reload</span></span> 

<span data-ttu-id="8bbe1-309">Vuelve a cargar la página actual.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-309">Reloads the current page.</span></span>

> <span data-ttu-id="8bbe1-310">public void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="8bbe1-310">public void [Reload](#reload)()</span></span>

<span data-ttu-id="8bbe1-311">Equivale a llamar a CoreWebView2. Reload en CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-311">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="8bbe1-312">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-312">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8bbe1-313">Se produce si CoreWebView2 todavía no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-313">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="8bbe1-314">" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-314">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="8bbe1-315">Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-315">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-316">Detener</span><span class="sxs-lookup"><span data-stu-id="8bbe1-316">Stop</span></span> 

<span data-ttu-id="8bbe1-317">Detiene todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-317">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="8bbe1-318">public void [Stop](#stop)()</span><span class="sxs-lookup"><span data-stu-id="8bbe1-318">public void [Stop](#stop)()</span></span>

<span data-ttu-id="8bbe1-319">Equivale a llamar a CoreWebView2. STOP en CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-319">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="8bbe1-320">Excepciones</span><span class="sxs-lookup"><span data-stu-id="8bbe1-320">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="8bbe1-321">Se produce si CoreWebView2 todavía no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-321">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="8bbe1-322">" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-322">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="8bbe1-323">Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-323">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="8bbe1-324">WebView2</span><span class="sxs-lookup"><span data-stu-id="8bbe1-324">WebView2</span></span> 

<span data-ttu-id="8bbe1-325">Crea una nueva instancia de un control WebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-325">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="8bbe1-326">[WebView2](#webview2)pública ()</span><span class="sxs-lookup"><span data-stu-id="8bbe1-326">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="8bbe1-327">Ten en cuenta que la CoreWebView2 del control será null hasta que se inicialice.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-327">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="8bbe1-328">Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-328">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="8bbe1-329">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="8bbe1-329">BuildWindowCore</span></span> 

<span data-ttu-id="8bbe1-330">Esto se ha invalidado de HwndHost y se le llama para que podamos crear nuestro HWND.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-330">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>

> <span data-ttu-id="8bbe1-331">invalidación protegida HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-331">protected override HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span></span>

##### <span data-ttu-id="8bbe1-332">Parameters</span><span class="sxs-lookup"><span data-stu-id="8bbe1-332">Parameters</span></span>
* `hwndParent` <span data-ttu-id="8bbe1-333">El identificador HWND que deberíamos usar como principal del que creamos.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-333">The HWND that we should use as the parent of the one we create.</span></span>

##### <span data-ttu-id="8bbe1-334">Devuelve</span><span class="sxs-lookup"><span data-stu-id="8bbe1-334">Returns</span></span>
<span data-ttu-id="8bbe1-335">El HWND que hemos creado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-335">The HWND that we created.</span></span>

#### <span data-ttu-id="8bbe1-336">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="8bbe1-336">DestroyWindowCore</span></span> 

<span data-ttu-id="8bbe1-337">Esto se invalida en HwndHost y se llama para indicarnos que destruya nuestro HWND.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-337">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>

> <span data-ttu-id="8bbe1-338">Protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef HWND)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-338">protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef hwnd)</span></span>

##### <span data-ttu-id="8bbe1-339">Parameters</span><span class="sxs-lookup"><span data-stu-id="8bbe1-339">Parameters</span></span>
* `hwnd` <span data-ttu-id="8bbe1-340">Nuestro HWND que debemos destruir.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-340">Our HWND that we need to destroy.</span></span>

#### <span data-ttu-id="8bbe1-341">Dispose</span><span class="sxs-lookup"><span data-stu-id="8bbe1-341">Dispose</span></span> 

<span data-ttu-id="8bbe1-342">La clase base llama a esta función de acuerdo con la implementación típica del patrón IDispose.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-342">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>

> <span data-ttu-id="8bbe1-343">invalid override void [Dispose](#dispose)(bool disposing)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-343">protected override void [Dispose](#dispose)(bool disposing)</span></span>

<span data-ttu-id="8bbe1-344">Para implementarlo, lanzamos todos nuestros recursos COM subyacentes, incluido nuestro CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-344">We implement it by releasing all of our underlying COM resources, including our CoreWebView2.</span></span>

##### <span data-ttu-id="8bbe1-345">Parameters</span><span class="sxs-lookup"><span data-stu-id="8bbe1-345">Parameters</span></span>
* `disposing` <span data-ttu-id="8bbe1-346">True si la persona que llama está llamando explícitamente a Dispose, false si se está definiendo.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-346">True if a caller is explicitly calling Dispose, false if we're being finalized.</span></span>

#### <span data-ttu-id="8bbe1-347">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="8bbe1-347">HasFocusWithinCore</span></span> 

<span data-ttu-id="8bbe1-348">Esto se invalida en HwndHost y se llama cuando WPF necesita saber si el foco está en nuestro control/ventana.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-348">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>

> <span data-ttu-id="8bbe1-349">Protected override bool [HasFocusWithinCore](#hasfocuswithincore)()</span><span class="sxs-lookup"><span data-stu-id="8bbe1-349">protected override bool [HasFocusWithinCore](#hasfocuswithincore)()</span></span>

<span data-ttu-id="8bbe1-350">WPF no puede saber por sí mismo porque hospedamos una ventana que no es de WPF, por lo que en su lugar nos pidemos que nos llame.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-350">WPF can't know on its own since we're hosting a non-WPF window, so instead it asks us by calling this.</span></span> <span data-ttu-id="8bbe1-351">Para responder, solo hacemos un seguimiento del estado según los eventos CoreWebView2 que se activan cuando gana o pierde el foco.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-351">To answer, we just track state based on CoreWebView2 events that fire when it gains or loses focus.</span></span>

##### <span data-ttu-id="8bbe1-352">Devuelve</span><span class="sxs-lookup"><span data-stu-id="8bbe1-352">Returns</span></span>
<span data-ttu-id="8bbe1-353">True si el foco está en nuestro control/ventana, false si no lo está.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-353">True if the focus is in our control/window, false if it isn't.</span></span>

#### <span data-ttu-id="8bbe1-354">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="8bbe1-354">OnKeyDown</span></span> 

<span data-ttu-id="8bbe1-355">Esto se invalida de UIElement y se llama para permitirnos controlar la entrada de presión de teclas.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-355">This is overridden from UIElement and called to allow us to handle key press input.</span></span>

> <span data-ttu-id="8bbe1-356">Protected override void [onkeydown](#onkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-356">protected override void [OnKeyDown](#onkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="8bbe1-357">En realidad, WPF nunca debe llamar a esto como respuesta a eventos de teclado porque hospedamos una ventana que no es de WPF.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-357">WPF should never actually call this in response to keyboard events because we're hosting a non-WPF window.</span></span> <span data-ttu-id="8bbe1-358">Cuando la ventana tiene el foco, Windows enviará la entrada directamente, en lugar de la ventana de nivel superior y el sistema de entrada de nivel superior de WPF.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-358">When our window has focus Windows will send the input directly to it rather than to WPF's top-level window and input system.</span></span> <span data-ttu-id="8bbe1-359">Solo debe llamarse a este override cuando estamos reenviando explícitamente la entrada de la tecla de aceleración de CoreWebView2 a WPF (en CoreWebView2Controller_AcceleratorKeyPressed).</span><span class="sxs-lookup"><span data-stu-id="8bbe1-359">This override should only be called when we're explicitly forwarding accelerator key input from the CoreWebView2 to WPF (in CoreWebView2Controller_AcceleratorKeyPressed).</span></span> <span data-ttu-id="8bbe1-360">Incluso entonces, este KeyDownEvent solo se desencadena porque nuestra implementación de PreviewKeyDownEvent lo desencadena explícitamente, que coincide con el sistema habitual de WPF.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-360">Even then, this KeyDownEvent is only triggered because our PreviewKeyDownEvent implementation explicitly triggers it, matching WPF's usual system.</span></span> <span data-ttu-id="8bbe1-361">Por lo tanto, el proceso es: CoreWebView2Controller_AcceleratorKeyPressed-> produce PreviewKeyDownEvent-> OnPreviewKeyDown-> raise KeyDownEvent-> OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="8bbe1-361">So the process is: CoreWebView2Controller_AcceleratorKeyPressed -> raise PreviewKeyDownEvent -> OnPreviewKeyDown -> raise KeyDownEvent -> OnKeyDown</span></span>

#### <span data-ttu-id="8bbe1-362">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="8bbe1-362">OnKeyUp</span></span> 

<span data-ttu-id="8bbe1-363">Consulta OnKeyDown.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-363">See OnKeyDown.</span></span>

> <span data-ttu-id="8bbe1-364">Protected override void [onkeyup](#onkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-364">protected override void [OnKeyUp](#onkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="8bbe1-365">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="8bbe1-365">OnPreviewKeyDown</span></span> 

<span data-ttu-id="8bbe1-366">Esta es la "vista previa" (es decir,</span><span class="sxs-lookup"><span data-stu-id="8bbe1-366">This is the "Preview" (i.e.</span></span>

> <span data-ttu-id="8bbe1-367">Protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-367">protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="8bbe1-368">tunneling) versión de OnKeyDown, así que realmente se produce en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-368">tunneling) version of OnKeyDown, so it actually happens first.</span></span> <span data-ttu-id="8bbe1-369">Como OnKeyDown, solo se llamará si estamos reenviando explícitamente las pulsaciones de tecla de la CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-369">Like OnKeyDown, this will only ever be called if we're explicitly forwarding key presses from the CoreWebView2.</span></span> <span data-ttu-id="8bbe1-370">Para imitar el control de entrada estándar de WPF, cuando recibamos este texto, desactivamos el KeyDownEvent de propagación estándar.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-370">In order to mimic WPF's standard input handling, when we receive this we turn around and fire off the standard bubbling KeyDownEvent.</span></span> <span data-ttu-id="8bbe1-371">De ese modo, los demás miembros del árbol de WPF verán el mismo par estándar de eventos de entrada que el propio WPF habría desencadenado si estuviera manejando la pulsación de teclas.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-371">That way others in the WPF tree see the same standard pair of input events that WPF itself would have triggered if it were handling the key press.</span></span>

#### <span data-ttu-id="8bbe1-372">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="8bbe1-372">OnPreviewKeyUp</span></span> 

<span data-ttu-id="8bbe1-373">Consulta OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-373">See OnPreviewKeyDown.</span></span>

> <span data-ttu-id="8bbe1-374">Protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-374">protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="8bbe1-375">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="8bbe1-375">OnWindowPositionChanged</span></span> 

<span data-ttu-id="8bbe1-376">Esto se invalida desde HwndHost y se llama cuando la ubicación de nuestro control ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-376">This is overridden from HwndHost and called when our control's location has changed.</span></span>

> <span data-ttu-id="8bbe1-377">Protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-377">protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span></span>

<span data-ttu-id="8bbe1-378">El HwndHost se encarga de actualizar el HWND que hemos creado.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-378">The HwndHost takes care of updating the HWND we created.</span></span> <span data-ttu-id="8bbe1-379">Lo que debemos hacer es mover la CoreWebView2 para que coincida con la nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-379">What we need to do is move our CoreWebView2 to match the new location.</span></span>

#### <span data-ttu-id="8bbe1-380">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="8bbe1-380">TabIntoCore</span></span> 

<span data-ttu-id="8bbe1-381">Esto se invalida de HwndHost y se le llama para informarnos que la tabulación ha provocado que el foco se mueva a nuestro control/ventana.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-381">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

> <span data-ttu-id="8bbe1-382">Protected override bool [TabIntoCore](#tabintocore)(solicitud TraversalRequest)</span><span class="sxs-lookup"><span data-stu-id="8bbe1-382">protected override bool [TabIntoCore](#tabintocore)(TraversalRequest request)</span></span>

<span data-ttu-id="8bbe1-383">Dado que WPF no puede administrar la transición de foco a un HWND que no es WPF, lo delega aquí.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-383">Since WPF can't manage the transition of focus to a non-WPF HWND, it delegates the transition to us here.</span></span> <span data-ttu-id="8bbe1-384">Por eso, nuestro trabajo es solo para colocar el foco en nuestro HWND externo.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-384">So our job is just to place the focus in our external HWND.</span></span>

##### <span data-ttu-id="8bbe1-385">Parameters</span><span class="sxs-lookup"><span data-stu-id="8bbe1-385">Parameters</span></span>
* `request` <span data-ttu-id="8bbe1-386">Información sobre cómo se mueve el foco.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-386">Information about how the focus is moving.</span></span>

##### <span data-ttu-id="8bbe1-387">Devuelve</span><span class="sxs-lookup"><span data-stu-id="8bbe1-387">Returns</span></span>
<span data-ttu-id="8bbe1-388">True para indicar que se ha controlado la navegación, o falso para indicar que no se ha hecho.</span><span class="sxs-lookup"><span data-stu-id="8bbe1-388">True to indicate that we handled the navigation, or false to indicate that we didn't.</span></span>


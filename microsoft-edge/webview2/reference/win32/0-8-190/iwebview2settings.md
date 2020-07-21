---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 649506b28e0ecdbff33b44bbd8010ddb3d2a66b0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885803"
---
# <span data-ttu-id="1f2f3-104">0.8.355: IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="1f2f3-104">0.8.355 - interface IWebView2Settings</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="1f2f3-105">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="1f2f3-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="1f2f3-106">Summary</span></span>

 <span data-ttu-id="1f2f3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1f2f3-107">Members</span></span>                        | <span data-ttu-id="1f2f3-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1f2f3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1f2f3-109">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-109">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="1f2f3-110">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-110">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="1f2f3-111">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-111">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="1f2f3-112">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-112">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="1f2f3-113">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-113">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="1f2f3-114">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-114">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="1f2f3-115">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-115">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="1f2f3-116">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-116">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="1f2f3-117">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-117">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="1f2f3-118">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-118">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="1f2f3-119">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-119">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="1f2f3-120">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-120">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="1f2f3-121">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="1f2f3-121">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="1f2f3-122">Esta configuración ha quedado obsoleta y siempre devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-122">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="1f2f3-123">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="1f2f3-123">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="1f2f3-124">Esta configuración ha quedado obsoleta y no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-124">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="1f2f3-125">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-125">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="1f2f3-126">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-126">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="1f2f3-127">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-127">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="1f2f3-128">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-128">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="1f2f3-129">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-129">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="1f2f3-130">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-130">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="1f2f3-131">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-131">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="1f2f3-132">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-132">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="1f2f3-133">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-133">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="1f2f3-134">Miembros</span><span class="sxs-lookup"><span data-stu-id="1f2f3-134">Members</span></span>

#### <span data-ttu-id="1f2f3-135">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-135">get_IsScriptEnabled</span></span> 

<span data-ttu-id="1f2f3-136">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-136">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="1f2f3-137">[get_IsScriptEnabled](#get_isscriptenabled)de HRESULT público (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-137">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="1f2f3-138">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-138">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="1f2f3-139">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-139">It is true by default.</span></span>

```cpp
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
```

#### <span data-ttu-id="1f2f3-140">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-140">put_IsScriptEnabled</span></span> 

<span data-ttu-id="1f2f3-141">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-141">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="1f2f3-142">[put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-142">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="1f2f3-143">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-143">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="1f2f3-144">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-144">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="1f2f3-145">[get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-145">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="1f2f3-146">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="1f2f3-146">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="1f2f3-147">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="1f2f3-147">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="1f2f3-148">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-148">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="1f2f3-149">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-149">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="1f2f3-150">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-150">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="1f2f3-151">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-151">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="1f2f3-152">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-152">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="1f2f3-153">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-153">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="1f2f3-154">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-154">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="1f2f3-155">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-155">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="1f2f3-156">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-156">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="1f2f3-157">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las funciones de alerta, confirmación e petición de JavaScript).</span><span class="sxs-lookup"><span data-stu-id="1f2f3-157">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="1f2f3-158">En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-158">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="1f2f3-159">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-159">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="1f2f3-160">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-160">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="1f2f3-161">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-161">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="1f2f3-162">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="1f2f3-162">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="1f2f3-163">Esta configuración ha quedado obsoleta y siempre devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-163">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="1f2f3-164">[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)de HRESULT público (bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-164">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="1f2f3-165">Eso significa que los elementos de la vista en WebView solo rellenarán los límites de la vista de vista.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-165">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="1f2f3-166">Esta propiedad se eliminará por completo.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-166">This property will then be completely removed.</span></span> <span data-ttu-id="1f2f3-167">En su lugar, escucha el evento ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-167">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="1f2f3-168">Controla si se permite la pantalla completa para los elementos de la vista.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-168">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="1f2f3-169">Cuando está permitido, el contenido Web, como un elemento de vídeo en la vista Web, se puede mostrar a pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-169">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="1f2f3-170">Si no está permitido, ese elemento rellenará los límites de la vista previa cuando el elemento solicite la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-170">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="1f2f3-171">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-171">It is true by default.</span></span>

#### <span data-ttu-id="1f2f3-172">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="1f2f3-172">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="1f2f3-173">Esta configuración ha quedado obsoleta y no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-173">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="1f2f3-174">[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)de HRESULT público (bool IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-174">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="1f2f3-175">En su lugar, escucha el evento ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-175">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="1f2f3-176">Establezca la propiedad IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-176">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="1f2f3-177">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-177">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="1f2f3-178">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-178">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="1f2f3-179">[get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-179">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="1f2f3-180">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-180">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="1f2f3-181">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-181">It is true by default.</span></span>

#### <span data-ttu-id="1f2f3-182">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-182">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="1f2f3-183">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-183">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="1f2f3-184">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-184">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="1f2f3-185">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-185">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="1f2f3-186">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-186">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="1f2f3-187">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-187">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="1f2f3-188">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-188">It is true by default.</span></span>

#### <span data-ttu-id="1f2f3-189">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="1f2f3-189">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="1f2f3-190">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="1f2f3-190">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="1f2f3-191">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="1f2f3-191">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>


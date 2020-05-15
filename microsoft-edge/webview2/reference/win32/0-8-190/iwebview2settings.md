---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 3c799e97f8e85927e1c11b30be747d7649faeca0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655216"
---
# <span data-ttu-id="810df-104">interfaz IWebView2Settings</span><span class="sxs-lookup"><span data-stu-id="810df-104">interface IWebView2Settings</span></span> 

> [!NOTE]
> <span data-ttu-id="810df-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="810df-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="810df-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="810df-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings
  : public IUnknown
```

<span data-ttu-id="810df-107">Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.</span><span class="sxs-lookup"><span data-stu-id="810df-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="810df-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="810df-108">Summary</span></span>

 <span data-ttu-id="810df-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="810df-109">Members</span></span>                        | <span data-ttu-id="810df-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="810df-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="810df-111">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-111">get_IsScriptEnabled</span></span>](#get_isscriptenabled) | <span data-ttu-id="810df-112">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="810df-112">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>
[<span data-ttu-id="810df-113">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-113">put_IsScriptEnabled</span></span>](#put_isscriptenabled) | <span data-ttu-id="810df-114">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-114">Set the IsScriptEnabled property.</span></span>
[<span data-ttu-id="810df-115">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-115">get_IsWebMessageEnabled</span></span>](#get_iswebmessageenabled) | <span data-ttu-id="810df-116">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="810df-116">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>
[<span data-ttu-id="810df-117">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-117">put_IsWebMessageEnabled</span></span>](#put_iswebmessageenabled) | <span data-ttu-id="810df-118">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-118">Set the IsWebMessageEnabled property.</span></span>
[<span data-ttu-id="810df-119">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-119">get_AreDefaultScriptDialogsEnabled</span></span>](#get_aredefaultscriptdialogsenabled) | <span data-ttu-id="810df-120">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="810df-120">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>
[<span data-ttu-id="810df-121">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-121">put_AreDefaultScriptDialogsEnabled</span></span>](#put_aredefaultscriptdialogsenabled) | <span data-ttu-id="810df-122">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-122">Set the AreDefaultScriptDialogsEnabled property.</span></span>
[<span data-ttu-id="810df-123">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="810df-123">get_IsFullscreenAllowed_deprecated</span></span>](#get_isfullscreenallowed_deprecated) | <span data-ttu-id="810df-124">Esta configuración ha quedado obsoleta y siempre devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="810df-124">This setting is deprecated and will always return false.</span></span>
[<span data-ttu-id="810df-125">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="810df-125">put_IsFullscreenAllowed_deprecated</span></span>](#put_isfullscreenallowed_deprecated) | <span data-ttu-id="810df-126">Esta configuración ha quedado obsoleta y no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="810df-126">This setting is deprecated and will have no effect.</span></span>
[<span data-ttu-id="810df-127">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-127">get_IsStatusBarEnabled</span></span>](#get_isstatusbarenabled) | <span data-ttu-id="810df-128">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="810df-128">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>
[<span data-ttu-id="810df-129">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-129">put_IsStatusBarEnabled</span></span>](#put_isstatusbarenabled) | <span data-ttu-id="810df-130">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-130">Set the IsStatusBarEnabled property.</span></span>
[<span data-ttu-id="810df-131">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-131">get_AreDevToolsEnabled</span></span>](#get_aredevtoolsenabled) | <span data-ttu-id="810df-132">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="810df-132">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>
[<span data-ttu-id="810df-133">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-133">put_AreDevToolsEnabled</span></span>](#put_aredevtoolsenabled) | <span data-ttu-id="810df-134">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-134">Set the AreDevToolsEnabled property.</span></span>

<span data-ttu-id="810df-135">Los cambios de configuración realizados después del evento NavigationStarting no se aplicarán hasta la siguiente navegación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="810df-135">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="810df-136">Miembros</span><span class="sxs-lookup"><span data-stu-id="810df-136">Members</span></span>

#### <span data-ttu-id="810df-137">get_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-137">get_IsScriptEnabled</span></span> 

<span data-ttu-id="810df-138">Controla si la ejecución de JavaScript está habilitada en todas las navegaciones futuras de WebView.</span><span class="sxs-lookup"><span data-stu-id="810df-138">Controls if JavaScript execution is enabled in all future navigations in the WebView.</span></span>

> <span data-ttu-id="810df-139">[get_IsScriptEnabled](#get_isscriptenabled)de HRESULT público (bool \* IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-139">public HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(BOOL \* isScriptEnabled)</span></span>

<span data-ttu-id="810df-140">Esto solo afecta a los scripts del documento. los scripts inyectados con ExecuteScript se ejecutarán incluso si el script está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="810df-140">This only affects scripts in the document; scripts injected with ExecuteScript will run even if script is disabled.</span></span> <span data-ttu-id="810df-141">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="810df-141">It is true by default.</span></span>

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

#### <span data-ttu-id="810df-142">put_IsScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-142">put_IsScriptEnabled</span></span> 

<span data-ttu-id="810df-143">Establezca la propiedad IsScriptEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-143">Set the IsScriptEnabled property.</span></span>

> <span data-ttu-id="810df-144">[put_IsScriptEnabled](#put_isscriptenabled)de HRESULT público (bool IsScriptEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-144">public HRESULT [put_IsScriptEnabled](#put_isscriptenabled)(BOOL isScriptEnabled)</span></span>

#### <span data-ttu-id="810df-145">get_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-145">get_IsWebMessageEnabled</span></span> 

<span data-ttu-id="810df-146">La propiedad IsWebMessageEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="810df-146">The IsWebMessageEnabled property is used when loading a new HTML document.</span></span>

> <span data-ttu-id="810df-147">[get_IsWebMessageEnabled](#get_iswebmessageenabled)de HRESULT público (bool \* IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-147">public HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(BOOL \* isWebMessageEnabled)</span></span>

<span data-ttu-id="810df-148">Si se establece en true, se permite la comunicación desde el host al documento HTML de nivel superior de la WebView a través de PostWebMessageAsJson, PostWebMessageAsString y Window. Chrome. evento de mensaje de WebView (consulte la documentación de PostWebMessageAsJson para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="810df-148">If set to true, communication from the host to the webview's top level HTML document is allowed via PostWebMessageAsJson, PostWebMessageAsString, and window.chrome.webview's message event (see PostWebMessageAsJson documentation for details).</span></span> <span data-ttu-id="810df-149">Se permite la comunicación desde el documento HTML de nivel superior de WebView al host mediante Window. Chrome. función PostMessage de WebView y el método SetWebMessageReceivedEventHandler (consulte la documentación de SetWebMessageReceivedEventHandler para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="810df-149">Communication from the webview's top level HTML document to the host is allowed via window.chrome.webview's postMessage function and the SetWebMessageReceivedEventHandler method (see the SetWebMessageReceivedEventHandler documentation for details).</span></span> <span data-ttu-id="810df-150">Si se establece en false, no se permite la comunicación.</span><span class="sxs-lookup"><span data-stu-id="810df-150">If set to false, then communication is disallowed.</span></span> <span data-ttu-id="810df-151">PostWebMessageAsJson y PostWebMessageAsString producirán errores con E_ACCESSDENIED y Window. Chrome. Webview. PostMessage producirá un error generando una instancia de un objeto de error.</span><span class="sxs-lookup"><span data-stu-id="810df-151">PostWebMessageAsJson and PostWebMessageAsString will fail with E_ACCESSDENIED and window.chrome.webview.postMessage will fail by throwing an instance of an Error object.</span></span> <span data-ttu-id="810df-152">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="810df-152">It is true by default.</span></span>

```cpp
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### <span data-ttu-id="810df-153">put_IsWebMessageEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-153">put_IsWebMessageEnabled</span></span> 

<span data-ttu-id="810df-154">Establezca la propiedad IsWebMessageEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-154">Set the IsWebMessageEnabled property.</span></span>

> <span data-ttu-id="810df-155">[put_IsWebMessageEnabled](#put_iswebmessageenabled)de HRESULT público (bool IsWebMessageEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-155">public HRESULT [put_IsWebMessageEnabled](#put_iswebmessageenabled)(BOOL isWebMessageEnabled)</span></span>

#### <span data-ttu-id="810df-156">get_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-156">get_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="810df-157">AreDefaultScriptDialogsEnabled se usa al cargar un nuevo documento HTML.</span><span class="sxs-lookup"><span data-stu-id="810df-157">AreDefaultScriptDialogsEnabled is used when loading a new HTML document.</span></span>

> <span data-ttu-id="810df-158">[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)de HRESULT público (bool \* AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-158">public HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(BOOL \* areDefaultScriptDialogsEnabled)</span></span>

<span data-ttu-id="810df-159">Si se establece en false, WebView no procesará el cuadro de diálogo predeterminado de JavaScript (específicamente los que se muestran en las funciones de alerta, confirmación e petición de JavaScript).</span><span class="sxs-lookup"><span data-stu-id="810df-159">If set to false, then WebView won't render the default javascript dialog box (Specifically those shown by the javascript alert, confirm, and prompt functions).</span></span> <span data-ttu-id="810df-160">En su lugar, si un controlador de eventos se establece mediante SetScriptDialogOpeningEventHandler, WebView enviará un evento que contendrá toda la información del cuadro de diálogo y permitirá que la aplicación host muestre su propia interfaz de usuario personalizada.</span><span class="sxs-lookup"><span data-stu-id="810df-160">Instead, if an event handler is set by SetScriptDialogOpeningEventHandler, WebView will send an event that will contain all of the information for the dialog and allow the host app to show its own custom UI.</span></span>

#### <span data-ttu-id="810df-161">put_AreDefaultScriptDialogsEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-161">put_AreDefaultScriptDialogsEnabled</span></span> 

<span data-ttu-id="810df-162">Establezca la propiedad AreDefaultScriptDialogsEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-162">Set the AreDefaultScriptDialogsEnabled property.</span></span>

> <span data-ttu-id="810df-163">[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de HRESULT público (bool AreDefaultScriptDialogsEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-163">public HRESULT [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)(BOOL areDefaultScriptDialogsEnabled)</span></span>

#### <span data-ttu-id="810df-164">get_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="810df-164">get_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="810df-165">Esta configuración ha quedado obsoleta y siempre devolverá FALSE.</span><span class="sxs-lookup"><span data-stu-id="810df-165">This setting is deprecated and will always return false.</span></span>

> <span data-ttu-id="810df-166">[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)de HRESULT público (bool \* IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="810df-166">public HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(BOOL \* isFullscreenAllowed)</span></span>

<span data-ttu-id="810df-167">Eso significa que los elementos de la vista en WebView solo rellenarán los límites de la vista de vista.</span><span class="sxs-lookup"><span data-stu-id="810df-167">That means elements in the WebView will only fill the WebView bounds.</span></span> <span data-ttu-id="810df-168">Esta propiedad se eliminará por completo.</span><span class="sxs-lookup"><span data-stu-id="810df-168">This property will then be completely removed.</span></span> <span data-ttu-id="810df-169">En su lugar, escucha el evento ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="810df-169">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="810df-170">Controla si se permite la pantalla completa para los elementos de la vista.</span><span class="sxs-lookup"><span data-stu-id="810df-170">Controls if fullscreen is allowed for elements in the WebView.</span></span> <span data-ttu-id="810df-171">Cuando está permitido, el contenido Web, como un elemento de vídeo en la vista Web, se puede mostrar a pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="810df-171">When it is allowed, web content such as a video element in the WebView is allowed to be displayed full screen.</span></span> <span data-ttu-id="810df-172">Si no está permitido, ese elemento rellenará los límites de la vista previa cuando el elemento solicite la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="810df-172">When it is not allowed, such element will fill the WebView bounds when the element requests full screen.</span></span> <span data-ttu-id="810df-173">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="810df-173">It is true by default.</span></span>

#### <span data-ttu-id="810df-174">put_IsFullscreenAllowed_deprecated</span><span class="sxs-lookup"><span data-stu-id="810df-174">put_IsFullscreenAllowed_deprecated</span></span> 

<span data-ttu-id="810df-175">Esta configuración ha quedado obsoleta y no tendrá ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="810df-175">This setting is deprecated and will have no effect.</span></span>

> <span data-ttu-id="810df-176">[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)de HRESULT público (bool IsFullscreenAllowed)</span><span class="sxs-lookup"><span data-stu-id="810df-176">public HRESULT [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)(BOOL isFullscreenAllowed)</span></span>

<span data-ttu-id="810df-177">En su lugar, escucha el evento ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="810df-177">Please listen to the ContainsFullScreenElementChanged event instead.</span></span>

<span data-ttu-id="810df-178">Establezca la propiedad IsFullscreenAllowed.</span><span class="sxs-lookup"><span data-stu-id="810df-178">Set the IsFullscreenAllowed property.</span></span>

#### <span data-ttu-id="810df-179">get_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-179">get_IsStatusBarEnabled</span></span> 

<span data-ttu-id="810df-180">IsStatusBarEnabled controla si se mostrará la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="810df-180">IsStatusBarEnabled controls whether the status bar will be displayed.</span></span>

> <span data-ttu-id="810df-181">[get_IsStatusBarEnabled](#get_isstatusbarenabled)de HRESULT público (bool \* IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-181">public HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(BOOL \* isStatusBarEnabled)</span></span>

<span data-ttu-id="810df-182">Normalmente, la barra de estado se muestra en la parte inferior izquierda de la vista WebView y muestra aspectos como el URI de un vínculo cuando el usuario mantiene el puntero sobre él y otra información.</span><span class="sxs-lookup"><span data-stu-id="810df-182">The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information.</span></span> <span data-ttu-id="810df-183">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="810df-183">It is true by default.</span></span>

#### <span data-ttu-id="810df-184">put_IsStatusBarEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-184">put_IsStatusBarEnabled</span></span> 

<span data-ttu-id="810df-185">Establezca la propiedad IsStatusBarEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-185">Set the IsStatusBarEnabled property.</span></span>

> <span data-ttu-id="810df-186">[put_IsStatusBarEnabled](#put_isstatusbarenabled)de HRESULT público (bool IsStatusBarEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-186">public HRESULT [put_IsStatusBarEnabled](#put_isstatusbarenabled)(BOOL isStatusBarEnabled)</span></span>

#### <span data-ttu-id="810df-187">get_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-187">get_AreDevToolsEnabled</span></span> 

<span data-ttu-id="810df-188">AreDevToolsEnabled controla si el usuario puede usar el menú contextual o los métodos abreviados de teclado para abrir la ventana de DevTools.</span><span class="sxs-lookup"><span data-stu-id="810df-188">AreDevToolsEnabled controls whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.</span></span>

> <span data-ttu-id="810df-189">[get_AreDevToolsEnabled](#get_aredevtoolsenabled)de HRESULT público (bool \* AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-189">public HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(BOOL \* areDevToolsEnabled)</span></span>

<span data-ttu-id="810df-190">Es verdadero de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="810df-190">It is true by default.</span></span>

#### <span data-ttu-id="810df-191">put_AreDevToolsEnabled</span><span class="sxs-lookup"><span data-stu-id="810df-191">put_AreDevToolsEnabled</span></span> 

<span data-ttu-id="810df-192">Establezca la propiedad AreDevToolsEnabled.</span><span class="sxs-lookup"><span data-stu-id="810df-192">Set the AreDevToolsEnabled property.</span></span>

> <span data-ttu-id="810df-193">[put_AreDevToolsEnabled](#put_aredevtoolsenabled)de HRESULT público (bool AreDevToolsEnabled)</span><span class="sxs-lookup"><span data-stu-id="810df-193">public HRESULT [put_AreDevToolsEnabled](#put_aredevtoolsenabled)(BOOL areDevToolsEnabled)</span></span>


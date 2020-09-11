---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2Environment
ms.openlocfilehash: c6b1f1c62da5aa5ef64693575abb9cb46ac13851
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012674"
---
# <span data-ttu-id="1cbbc-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="1cbbc-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="1cbbc-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1cbbc-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1cbbc-106">Ensamblado: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="1cbbc-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1cbbc-107">Esto representa el entorno de WebView2.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="1cbbc-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="1cbbc-108">Summary</span></span>

 <span data-ttu-id="1cbbc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1cbbc-109">Members</span></span>                        | <span data-ttu-id="1cbbc-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="1cbbc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1cbbc-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1cbbc-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="1cbbc-112">Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="1cbbc-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="1cbbc-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="1cbbc-114">NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para su uso a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-114">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>
[<span data-ttu-id="1cbbc-115">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1cbbc-115">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="1cbbc-116">Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-116">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="1cbbc-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1cbbc-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="1cbbc-118">Cree de forma asincrónica una nueva vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="1cbbc-119">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="1cbbc-119">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="1cbbc-120">Cree un CoreWebView2PointerInfo vacío.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-120">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="1cbbc-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1cbbc-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="1cbbc-122">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-122">Create a new web resource response object.</span></span>
[<span data-ttu-id="1cbbc-123">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="1cbbc-123">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="1cbbc-124">Devuelve el proveedor de automatización de la interfaz de usuario de la CoreWebView2CompositionController que se corresponde con el HWND dado.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-124">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="1cbbc-125">Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-125">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="1cbbc-126">No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-126">Using it in different environments are not guaranteed to be compatible and may fail.</span></span> 

<span data-ttu-id="1cbbc-127">Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-127">WebViews created from an environment run on the browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="1cbbc-128">No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-128">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="1cbbc-129">Miembros</span><span class="sxs-lookup"><span data-stu-id="1cbbc-129">Members</span></span>

#### <span data-ttu-id="1cbbc-130">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1cbbc-130">BrowserVersionString</span></span> 

<span data-ttu-id="1cbbc-131">Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-131">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="1cbbc-132">cadena pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="1cbbc-132">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="1cbbc-133">Coincide con el formato de la API de GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-133">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="1cbbc-134">Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-134">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="1cbbc-135">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="1cbbc-135">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="1cbbc-136">NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para su uso a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-136">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>

> <span data-ttu-id="1cbbc-137">evento público EventHandler< > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="1cbbc-137">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="1cbbc-138">Para usar la versión más reciente del explorador, debe crear un entorno y una vista Web nuevos.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-138">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="1cbbc-139">Este evento solo se activará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-139">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="1cbbc-140">Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-140">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="1cbbc-141">Puesto que una carpeta datos de usuario solo puede ser usada por un único proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero el entorno y las vistas de web que usan la versión anterior del explorador.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-141">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="1cbbc-142">O simplemente pide al usuario que reinicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-142">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="1cbbc-143">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1cbbc-143">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1cbbc-144">Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-144">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="1cbbc-145">tarea asincrónica pública< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="1cbbc-145">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="1cbbc-146">parentWindow es el HWND en el que la aplicación se conectará al árbol visual de la vista de ventana.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-146">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="1cbbc-147">Este es el HWND que la aplicación recibirá una entrada de puntero o de mouse para la vista de ventana (y deberá usar SendMouseInput/SendPointerInput para reenviar).</span><span class="sxs-lookup"><span data-stu-id="1cbbc-147">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="1cbbc-148">Si la aplicación mueve el árbol visual WebView a una ventana distinta de otra, debe establecer CoreWebView2CompositionController. ParentWindow para actualizar el nuevo HWND primario del árbol visual.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-148">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="1cbbc-149">Establezca la propiedad RootVisualTarget en el CoreWebView2CompositionController creado para proporcionar un objeto visual que hospede el árbol visual del explorador.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-149">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="1cbbc-150">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="1cbbc-151">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="1cbbc-152">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1cbbc-152">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="1cbbc-153">Cree de forma asincrónica una nueva vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-153">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="1cbbc-154">tarea asincrónica pública< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="1cbbc-154">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="1cbbc-155">parentWindow es el HWND en el que se debe mostrar la vista en la vista previa y desde la que se recibe la entrada.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-155">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="1cbbc-156">La vista en WebView agregará una ventana secundaria a la ventana proporcionada durante la creación de WebView.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-156">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="1cbbc-157">El orden Z y otros elementos afectados por el orden de ventanas relacionados se verán afectados según corresponda.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-157">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="1cbbc-158">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-158">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="1cbbc-159">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-159">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="1cbbc-160">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="1cbbc-160">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1cbbc-161">Cree un CoreWebView2PointerInfo vacío.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-161">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="1cbbc-162">Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="1cbbc-162">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="1cbbc-163">La CoreWebView2PointerInfo devuelta debe rellenarse con toda la información relevante antes de llamar a SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-163">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="1cbbc-164">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1cbbc-164">CreateWebResourceResponse</span></span> 

<span data-ttu-id="1cbbc-165">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-165">Create a new web resource response object.</span></span>

> <span data-ttu-id="1cbbc-166">Public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(contenido de Stream, int StatusCode, String ReasonPhrase, encabezados de cadena)</span><span class="sxs-lookup"><span data-stu-id="1cbbc-166">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="1cbbc-167">La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-167">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="1cbbc-168">También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el CoreWebView2HttpResponseHeaders para construir los encabezados línea a línea.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-168">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="1cbbc-169">Para obtener información sobre otros parámetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-169">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="1cbbc-170">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="1cbbc-170">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1cbbc-171">Devuelve el proveedor de automatización de la interfaz de usuario de la CoreWebView2CompositionController que se corresponde con el HWND dado.</span><span class="sxs-lookup"><span data-stu-id="1cbbc-171">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="1cbbc-172">[GetProviderForHwnd](#getproviderforhwnd)de objeto público (HWND HWND)</span><span class="sxs-lookup"><span data-stu-id="1cbbc-172">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>


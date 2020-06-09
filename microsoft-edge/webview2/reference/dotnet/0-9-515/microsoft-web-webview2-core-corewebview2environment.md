---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 986b1dc2870375243a0ee664262216105edd95a8
ms.sourcegitcommit: 3f8c8a5643e416b0851254833f9771192883ec45
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699503"
---
# <span data-ttu-id="2b2b3-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="2b2b3-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

> [!NOTE]
> <span data-ttu-id="2b2b3-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="2b2b3-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="2b2b3-107">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2b2b3-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2b2b3-108">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="2b2b3-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2b2b3-109">Esto representa el entorno de WebView2.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-109">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="2b2b3-110">Resumen</span><span class="sxs-lookup"><span data-stu-id="2b2b3-110">Summary</span></span>

 <span data-ttu-id="2b2b3-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b2b3-111">Members</span></span>                        | <span data-ttu-id="2b2b3-112">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2b2b3-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2b2b3-113">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="2b2b3-113">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="2b2b3-114">Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-114">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="2b2b3-115">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="2b2b3-115">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="2b2b3-116">El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-116">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="2b2b3-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="2b2b3-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="2b2b3-118">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="2b2b3-119">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="2b2b3-119">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="2b2b3-120">Cree de forma asincrónica una nueva vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-120">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="2b2b3-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="2b2b3-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="2b2b3-122">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-122">Create a new web resource response object.</span></span>

<span data-ttu-id="2b2b3-123">Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-123">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="2b2b3-124">No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-124">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="2b2b3-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b2b3-125">Members</span></span>

#### <span data-ttu-id="2b2b3-126">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="2b2b3-126">BrowserVersionString</span></span> 

<span data-ttu-id="2b2b3-127">Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-127">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="2b2b3-128">cadena pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="2b2b3-128">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="2b2b3-129">Coincide con el formato de la API de GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-129">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="2b2b3-130">Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-130">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="2b2b3-131">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="2b2b3-131">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="2b2b3-132">El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-132">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="2b2b3-133">evento público EventHandler< > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="2b2b3-133">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="2b2b3-134">Para usar la versión más reciente del explorador, debe crear un entorno y una vista Web nuevos.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-134">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="2b2b3-135">Este evento solo se activará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-135">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="2b2b3-136">Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-136">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="2b2b3-137">Puesto que una carpeta datos de usuario solo puede ser usada por un único proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero el entorno y las vistas de web que usan la versión anterior del explorador.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-137">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="2b2b3-138">O simplemente pide al usuario que reinicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-138">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="2b2b3-139">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="2b2b3-139">CreateAsync</span></span> 

<span data-ttu-id="2b2b3-140">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-140">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="2b2b3-141">tarea pública estática asincrónica< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Options)</span><span class="sxs-lookup"><span data-stu-id="2b2b3-141">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="2b2b3-142">Parameters</span><span class="sxs-lookup"><span data-stu-id="2b2b3-142">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="2b2b3-143">La ruta de acceso relativa a la carpeta que contiene el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-143">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="2b2b3-144">userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-144">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="2b2b3-145">Opciones usadas para crear un entorno WebView2.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-145">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="2b2b3-146">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="2b2b3-146">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="2b2b3-147">Cree de forma asincrónica una nueva vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-147">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="2b2b3-148">tarea asincrónica pública< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="2b2b3-148">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="2b2b3-149">parentWindow es el HWND en el que se debe mostrar la vista en la vista previa y desde la que se recibe la entrada.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-149">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="2b2b3-150">La vista en WebView agregará una ventana secundaria a la ventana proporcionada durante la creación de WebView.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-150">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="2b2b3-151">El orden Z y otros elementos afectados por el orden de ventanas relacionados se verán afectados según corresponda.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-151">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="2b2b3-152">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-152">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="2b2b3-153">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-153">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="2b2b3-154">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="2b2b3-154">CreateWebResourceResponse</span></span> 

<span data-ttu-id="2b2b3-155">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-155">Create a new web resource response object.</span></span>

> <span data-ttu-id="2b2b3-156">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenido de Stream, int StatusCode, String ReasonPhrase, encabezados de cadena)</span><span class="sxs-lookup"><span data-stu-id="2b2b3-156">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="2b2b3-157">La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-157">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="2b2b3-158">También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el CoreWebView2HttpResponseHeaders para construir los encabezados línea a línea.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-158">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="2b2b3-159">Para obtener información sobre otros parámetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="2b2b3-159">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>


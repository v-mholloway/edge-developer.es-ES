---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: be8f475d4c1a886a92b46144f2bffde2d49dc9d4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655387"
---
# <span data-ttu-id="fd1dd-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="fd1dd-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="fd1dd-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fd1dd-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fd1dd-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="fd1dd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fd1dd-107">Esto representa el entorno de WebView2.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="fd1dd-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="fd1dd-108">Summary</span></span>

 <span data-ttu-id="fd1dd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd1dd-109">Members</span></span>                        | <span data-ttu-id="fd1dd-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fd1dd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fd1dd-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="fd1dd-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="fd1dd-112">Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="fd1dd-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="fd1dd-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="fd1dd-114">El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="fd1dd-115">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="fd1dd-115">CreateAsync</span></span>](#createasync) | <span data-ttu-id="fd1dd-116">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-116">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="fd1dd-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="fd1dd-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="fd1dd-118">Cree de forma asincrónica una nueva vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="fd1dd-119">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="fd1dd-119">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="fd1dd-120">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-120">Create a new web resource response object.</span></span>

<span data-ttu-id="fd1dd-121">Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="fd1dd-122">No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="fd1dd-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd1dd-123">Members</span></span>

#### <span data-ttu-id="fd1dd-124">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="fd1dd-124">BrowserVersionString</span></span> 

<span data-ttu-id="fd1dd-125">Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-125">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="fd1dd-126">cadena pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="fd1dd-126">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="fd1dd-127">Coincide con el formato de la API de GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-127">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="fd1dd-128">Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-128">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="fd1dd-129">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="fd1dd-129">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="fd1dd-130">El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-130">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="fd1dd-131">evento público EventHandler< > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="fd1dd-131">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="fd1dd-132">Para usar la versión más reciente del explorador, debe crear un entorno y una vista Web nuevos.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-132">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="fd1dd-133">Este evento solo se activará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-133">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="fd1dd-134">Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-134">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="fd1dd-135">Puesto que una carpeta datos de usuario solo puede ser usada por un único proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero el entorno y las vistas de web que usan la versión anterior del explorador.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-135">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="fd1dd-136">O simplemente pide al usuario que reinicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-136">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="fd1dd-137">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="fd1dd-137">CreateAsync</span></span> 

<span data-ttu-id="fd1dd-138">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-138">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="fd1dd-139">tarea asincrónica pública< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Options)</span><span class="sxs-lookup"><span data-stu-id="fd1dd-139">public async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="fd1dd-140">Parameters</span><span class="sxs-lookup"><span data-stu-id="fd1dd-140">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="fd1dd-141">La ruta de acceso relativa a la carpeta que contiene el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-141">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="fd1dd-142">userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-142">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="fd1dd-143">Opciones usadas para crear un entorno WebView2.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-143">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="fd1dd-144">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="fd1dd-144">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="fd1dd-145">Cree de forma asincrónica una nueva vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-145">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="fd1dd-146">tarea asincrónica pública< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="fd1dd-146">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="fd1dd-147">parentWindow es el HWND en el que se debe mostrar la vista en la vista previa y desde la que se recibe la entrada.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-147">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="fd1dd-148">La vista en WebView agregará una ventana secundaria a la ventana proporcionada durante la creación de WebView.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-148">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="fd1dd-149">El orden Z y otros elementos afectados por el orden de ventanas relacionados se verán afectados según corresponda.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-149">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="fd1dd-150">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="fd1dd-151">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="fd1dd-152">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="fd1dd-152">CreateWebResourceResponse</span></span> 

<span data-ttu-id="fd1dd-153">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-153">Create a new web resource response object.</span></span>

> <span data-ttu-id="fd1dd-154">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenido de Stream, int StatusCode, String ReasonPhrase, encabezados de cadena)</span><span class="sxs-lookup"><span data-stu-id="fd1dd-154">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="fd1dd-155">La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-155">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="fd1dd-156">También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el CoreWebView2HttpResponseHeaders para construir los encabezados línea a línea.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-156">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="fd1dd-157">Para obtener información sobre otros parámetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-157">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>


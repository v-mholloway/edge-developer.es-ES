---
description: Obtenga información sobre cómo administrar carpetas de datos de usuario en aplicaciones WebView2
title: Administrar la carpeta de datos de usuario en aplicaciones WebView2.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral, carpeta de datos de usuario
ms.openlocfilehash: a6399e59f153d4446946937461e61667f325f4ae
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536177"
---
# <a name="manage-the-user-data-folder"></a><span data-ttu-id="39cd4-104">Administrar la carpeta de datos de usuario</span><span class="sxs-lookup"><span data-stu-id="39cd4-104">Manage the User Data Folder</span></span>  

<span data-ttu-id="39cd4-105">Las aplicaciones WebView2 interactúan con carpetas de datos de usuario para almacenar datos del explorador, como cookies, permisos y recursos almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="39cd4-105">WebView2 applications interact with user data folders to store browser data, such as cookies, permissions, and cached resources.</span></span>  <span data-ttu-id="39cd4-106">Cada instancia de un control WebView2 está asociada a una carpeta de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="39cd4-106">Each instance of a WebView2 control is associated with a user data folder.</span></span>  <span data-ttu-id="39cd4-107">Cada carpeta de datos de usuario es única para un usuario.</span><span class="sxs-lookup"><span data-stu-id="39cd4-107">Each user data folder is unique to a user.</span></span>  

## <a name="best-practices"></a><span data-ttu-id="39cd4-108">Procedimientos recomendados</span><span class="sxs-lookup"><span data-stu-id="39cd4-108">Best Practices</span></span>  

<span data-ttu-id="39cd4-109">WebView2 crea automáticamente las carpetas de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="39cd4-109">User data folders are created automatically by WebView2.</span></span>  <span data-ttu-id="39cd4-110">Los programadores de WebView2 controlan la duración de la carpeta de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="39cd4-110">WebView2 developers control the lifetime of the user data folder.</span></span>  <span data-ttu-id="39cd4-111">Si la aplicación vuelve a usar datos de usuario de sesiones de aplicación, considere la posibilidad de guardar las carpetas de datos de usuario, de lo contrario, puede eliminarlos.</span><span class="sxs-lookup"><span data-stu-id="39cd4-111">If your application re-uses user data from application sessions, consider saving the user data folders, otherwise you may delete them.</span></span>  <span data-ttu-id="39cd4-112">Tenga en cuenta los siguientes escenarios al decidir cómo administrar las carpetas de datos de usuario:</span><span class="sxs-lookup"><span data-stu-id="39cd4-112">Consider the following scenarios when deciding how to manage your user data folders:</span></span>  

*   <span data-ttu-id="39cd4-113">Si el mismo usuario usa la aplicación repetidamente y el contenido web de la aplicación se basa en los datos del usuario, guarde la carpeta de datos del usuario.</span><span class="sxs-lookup"><span data-stu-id="39cd4-113">If the same user uses your application repeatedly, and the web content of the application relies on the user's data, save the user data folder.</span></span>  <span data-ttu-id="39cd4-114">Si varios usuarios usan la aplicación repetidamente, cree una nueva carpeta de datos de usuario para cada nuevo usuario y guarde la carpeta de datos de usuario de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="39cd4-114">If multiple users use your application repeatedly, create a new user data folder for each new user, and save the user data folder of each user.</span></span>
*   <span data-ttu-id="39cd4-115">Si la aplicación no tiene usuarios repetidos, cree una nueva carpeta de datos de usuario para cada usuario y elimine la carpeta de datos de usuario anterior.</span><span class="sxs-lookup"><span data-stu-id="39cd4-115">If your application does not have repeat users, create a new user data folder for each user, and delete the previous user data folder.</span></span>  
    
## <a name="create-user-data-folders"></a><span data-ttu-id="39cd4-116">Crear carpetas de datos de usuario</span><span class="sxs-lookup"><span data-stu-id="39cd4-116">Create user data folders</span></span>  

<span data-ttu-id="39cd4-117">Para especificar la ubicación de la carpeta de datos de usuario, incluya el parámetro al llamar a `userDataFolder` [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) o [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).</span><span class="sxs-lookup"><span data-stu-id="39cd4-117">To specify the location of the user data folder, include the `userDataFolder` parameter when calling [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) or [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).</span></span>  <span data-ttu-id="39cd4-118">Después de la creación, los datos del explorador del control WebView2 se almacenan en una subcarpeta de `userDataFolder` .</span><span class="sxs-lookup"><span data-stu-id="39cd4-118">After creation, browser data from your WebView2 control is stored in a subfolder of `userDataFolder`.</span></span>  <span data-ttu-id="39cd4-119">Cuando `userDataFolder` no se especifica, WebView2 crea carpetas de datos de usuario en ubicaciones predeterminadas de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="39cd4-119">When `userDataFolder` is not specified, WebView2 creates user data folders at default locations as follows:</span></span>  

*   <span data-ttu-id="39cd4-120">Para las aplicaciones empaquetadas de la Tienda Windows, la carpeta de usuario predeterminada es la `ApplicationData\LocalFolder` subcarpeta de la carpeta del paquete.</span><span class="sxs-lookup"><span data-stu-id="39cd4-120">For packaged Windows Store apps, the default user folder is the `ApplicationData\LocalFolder` subfolder in the package's  folder.</span></span>  
*   <span data-ttu-id="39cd4-121">Para las aplicaciones de escritorio existentes, la carpeta de datos de usuario predeterminada es la ruta de acceso exe de la aplicación + `.WebView2` .</span><span class="sxs-lookup"><span data-stu-id="39cd4-121">For existing desktop apps, the default user data folder is the exe path of your application + `.WebView2`.</span></span>  <span data-ttu-id="39cd4-122">En lugar de usar el valor predeterminado, se recomienda especificar una carpeta de datos de usuario y crearla en la misma carpeta donde se almacenan todos los demás datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39cd4-122">Instead of using the default, we recommend that you specify a user data folder, and that you create it in the same folder where all other app data is stored.</span></span>  
    
## <a name="delete-user-data-folders"></a><span data-ttu-id="39cd4-123">Eliminar carpetas de datos de usuario</span><span class="sxs-lookup"><span data-stu-id="39cd4-123">Delete user data folders</span></span>  

<span data-ttu-id="39cd4-124">Es posible que la aplicación necesite eliminar carpetas de datos de usuario:</span><span class="sxs-lookup"><span data-stu-id="39cd4-124">Your application may need to delete user data folders:</span></span>  

*   <span data-ttu-id="39cd4-125">Al desinstalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39cd4-125">When uninstalling your app.</span></span>  <span data-ttu-id="39cd4-126">Si desinstalas aplicaciones de la Tienda Windows empaquetadas, Windows elimina las carpetas de datos de usuario automáticamente.</span><span class="sxs-lookup"><span data-stu-id="39cd4-126">If you are uninstalling packaged Windows Store apps, Windows deletes user data folders automatically.</span></span>  
*   <span data-ttu-id="39cd4-127">Para limpiar todo el historial de datos de exploración.</span><span class="sxs-lookup"><span data-stu-id="39cd4-127">To clean up all browsing data history.</span></span>  
*   <span data-ttu-id="39cd4-128">Para recuperarse de daños en los datos.</span><span class="sxs-lookup"><span data-stu-id="39cd4-128">To recover from data corruption.</span></span>  
*   <span data-ttu-id="39cd4-129">Para quitar datos de sesión anteriores.</span><span class="sxs-lookup"><span data-stu-id="39cd4-129">To remove previous session data.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="39cd4-130">Es posible que los archivos de las carpetas de datos de usuario aún se usen después de cerrar la aplicación WebView2.</span><span class="sxs-lookup"><span data-stu-id="39cd4-130">Files in user data folders may still be in use after the WebView2 application is closed.</span></span>  <span data-ttu-id="39cd4-131">En esta situación, espere a que el proceso del explorador y todos los procesos secundarios se cierren antes de eliminar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="39cd4-131">In this situation, wait for the browser process and all child processes to exit before deleting the folder.</span></span>  <span data-ttu-id="39cd4-132">Puede recuperar el identificador de proceso del proceso del explorador mediante la `BrowserProcessId` propiedad webView2.</span><span class="sxs-lookup"><span data-stu-id="39cd4-132">You may retrieve the process id of the browser process using the `BrowserProcessId` property of the WebView2.</span></span>  

## <a name="share-user-data-folders"></a><span data-ttu-id="39cd4-133">Compartir carpetas de datos de usuario</span><span class="sxs-lookup"><span data-stu-id="39cd4-133">Share user data folders</span></span>  

<span data-ttu-id="39cd4-134">Los controles WebView2 pueden compartir las mismas carpetas de datos de usuario para:</span><span class="sxs-lookup"><span data-stu-id="39cd4-134">WebView2 controls may share the same user data folders to:</span></span>  

*   <span data-ttu-id="39cd4-135">[Optimice los recursos del](../concepts/process-model.md) sistema ejecutándose en un proceso de explorador.</span><span class="sxs-lookup"><span data-stu-id="39cd4-135">[Optimize system resources](../concepts/process-model.md) by running in one browser process.</span></span>  
*   <span data-ttu-id="39cd4-136">Compartir el historial del explorador y los recursos almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="39cd4-136">Share browser history and cached resources.</span></span>  
    
<span data-ttu-id="39cd4-137">Tenga en cuenta lo siguiente al compartir carpetas de datos de usuario:</span><span class="sxs-lookup"><span data-stu-id="39cd4-137">Consider the following when sharing user data folders:</span></span>  

1.  <span data-ttu-id="39cd4-138">Al volver a crear controles WebView2 para actualizar las versiones del explorador mediante [eventos add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \(Win32\) o [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \(.NET\), asegúrese de que los procesos del explorador salen y cierran los controles webView2 que comparten la misma carpeta de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="39cd4-138">When re-creating WebView2 controls to update browser versions using [add_NewBrowserVersionAvailable](/microsoft-edge/webview2/reference/win32/icorewebview2environment#add_newbrowserversionavailable) \(Win32\) or [NewBrowserVersionAvailable](/dotnet/api/microsoft.web.webview2.core.corewebview2environment.newbrowserversionavailable) \(.NET\) events, ensure browser processes exit and close WebView2 controls that share the same user data folder.</span></span>  <span data-ttu-id="39cd4-139">Para recuperar el identificador de proceso del proceso del explorador, use la `BrowserProcessId` propiedad del control WebView2.</span><span class="sxs-lookup"><span data-stu-id="39cd4-139">To retrieve the process id of the browser process, use the `BrowserProcessId` property of the WebView2 control.</span></span>  
1.  <span data-ttu-id="39cd4-140">Los controles WebView2 que comparten la misma carpeta de datos de usuario deben usar las mismas opciones para [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) o [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).</span><span class="sxs-lookup"><span data-stu-id="39cd4-140">WebView2 controls that share the same user data folder must use the same options for [ICoreWebView2Environment](/microsoft-edge/webview2/reference/win32/icorewebview2environment) \(Win32\) or [CoreWebView2Environment](/dotnet/api/microsoft.web.webview2.core.corewebview2environment) \(.NET\).</span></span>  <span data-ttu-id="39cd4-141">Si no es así, la creación de WebView2 producirá un error con `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` .</span><span class="sxs-lookup"><span data-stu-id="39cd4-141">If not, the WebView2 creation will fail with `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)`.</span></span>  
    
<span data-ttu-id="39cd4-142">Para aislar diferentes partes de la aplicación o cuando no es necesario compartir datos entre controles WebView2, puede elegir usar diferentes carpetas de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="39cd4-142">To isolate different parts of your application or when sharing data between WebView2 controls is not needed, you may choose to use different user data folders.</span></span>  <span data-ttu-id="39cd4-143">Por ejemplo, una aplicación puede estar formada por dos controles WebView2, uno para mostrar un anuncio y otro para mostrar contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39cd4-143">For example, an application may consist of two WebView2 controls, one for displaying an advertisement and the other for displaying application content.</span></span>  <span data-ttu-id="39cd4-144">En este escenario, los desarrolladores pueden optar por usar diferentes carpetas de datos de usuario para cada control WebView2.</span><span class="sxs-lookup"><span data-stu-id="39cd4-144">In this scenario, developers may opt to use different user data folders for each WebView2 control.</span></span>  

> [!NOTE]
> <span data-ttu-id="39cd4-145">Cada proceso de explorador webView2 consume memoria adicional y espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="39cd4-145">Each WebView2 browser process consumes additional memory and disk space.</span></span>  <span data-ttu-id="39cd4-146">Por lo tanto, se recomienda no ejecutar WebView2s con demasiadas carpetas de datos de usuario diferentes al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="39cd4-146">Therefore, we recommend not running WebView2s with too many different user data folders at the same time.</span></span>  
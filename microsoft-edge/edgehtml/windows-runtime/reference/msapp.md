---
title: Referencia de api de MSApp
description: Proporciona funciones auxiliares que permiten crear objetos Blob y MSStream.  Los objetos y miembros de MSApp son compatibles con aplicaciones de Windows con JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carga de archivos, Blog, MSStream, aplicaciones de Windows 10, uwp, edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0607929971b1dd2956571304230f69f756497e32
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439727"
---
# <a name="msapp"></a><span data-ttu-id="1298a-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="1298a-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="1298a-106">El objeto MSApp y sus miembros solo son compatibles con aplicaciones de Windows con JavaScript \(incluidos los PWA que acceden a las características de la API de Windows\).</span><span class="sxs-lookup"><span data-stu-id="1298a-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="1298a-107">El objeto MSApp solo existe en el contexto local de un documento HTML en una aplicación de Windows cargada mediante el esquema uri ms-appx; de lo contrario, el objeto no existe (y, por lo tanto, ninguno de sus métodos y propiedades están disponibles).</span><span class="sxs-lookup"><span data-stu-id="1298a-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="1298a-108">Proporciona funciones auxiliares que permiten crear [objetos Blob](https://developer.mozilla.org/docs/Web/API/Blob) y [MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="1298a-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="1298a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1298a-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1298a-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource ,](#gethtmlprintdocumentsource)[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span><span class="sxs-lookup"><span data-stu-id="1298a-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="1298a-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="1298a-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="1298a-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="1298a-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="1298a-113">Interfaz MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="1298a-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="1298a-114">start</span><span class="sxs-lookup"><span data-stu-id="1298a-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <a name="msapp-methods"></a><span data-ttu-id="1298a-115">Métodos MSApp</span><span class="sxs-lookup"><span data-stu-id="1298a-115">MSApp methods</span></span>  

### <a name="cleartemporarywebdataasync"></a><span data-ttu-id="1298a-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="1298a-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-117">Borra los datos de caché e indexedDB para la aplicación o [WebView](../../hosting/webview/index.md).</span><span class="sxs-lookup"><span data-stu-id="1298a-117">Clears cache and indexedDB data for the app or [WebView](../../hosting/webview/index.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-118">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-118">Parameters</span></span>**  
      
      <span data-ttu-id="1298a-119">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1298a-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-120">Return value</span></span>**  
      
      <span data-ttu-id="1298a-121">Tipo: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="1298a-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="1298a-122">Representa una acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1298a-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-123">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-123">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-124">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-125">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-126">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-127">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createblobfromrandomaccessstream"></a><span data-ttu-id="1298a-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="1298a-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-129">Crea un [blob](https://developer.mozilla.org/docs/Web/API/Blob) a partir de [un objeto IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)</span><span class="sxs-lookup"><span data-stu-id="1298a-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="1298a-130">Este método debe usarse al tratar con objetos de aplicaciones para crear un objeto basado en `IRandomAccessStream` W3C a partir de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1298a-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="1298a-131">Una vez creado el blob, se puede usar con [filereader](https://developer.mozilla.org/docs/Web/API/FileReader), [API de dirección URL](https://developer.mozilla.org/docs/Web/API/URL)y [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="1298a-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-132">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="1298a-133">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-133">[in]</span></span>  
      
      | <span data-ttu-id="1298a-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-134">Type</span></span> | <span data-ttu-id="1298a-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="1298a-136">String</span></span> | <span data-ttu-id="1298a-137">Tipo de contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="1298a-137">Content type of the data.</span></span>  <span data-ttu-id="1298a-138">Esta cadena debe tener el formato especificado en el token de tipo multimedia definido en la sección 3.7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="1298a-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="1298a-139">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-139">[in]</span></span>  
      
      | <span data-ttu-id="1298a-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-140">Type</span></span> | <span data-ttu-id="1298a-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-142">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-142">Any</span></span> | <span data-ttu-id="1298a-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) que se almacenará en el blob.</span><span class="sxs-lookup"><span data-stu-id="1298a-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-144">Return value</span></span>**  
      
      | <span data-ttu-id="1298a-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-145">Type</span></span> | <span data-ttu-id="1298a-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-147">Blob</span><span class="sxs-lookup"><span data-stu-id="1298a-147">Blob</span></span> | <span data-ttu-id="1298a-148">Nuevo objeto blob que contiene la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1298a-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-149">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="1298a-150">Excepción</span><span class="sxs-lookup"><span data-stu-id="1298a-150">Exception</span></span> | <span data-ttu-id="1298a-151">Condición</span><span class="sxs-lookup"><span data-stu-id="1298a-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="1298a-152">TypeMismatchError</span></span> | <span data-ttu-id="1298a-153">El tipo de nodo es incompatible con el tipo de parámetro esperado.</span><span class="sxs-lookup"><span data-stu-id="1298a-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="1298a-154">Para las versiones anteriores a Internet Explorer 10, TYPE_MISMATCH_ERR se devuelve.</span><span class="sxs-lookup"><span data-stu-id="1298a-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-155">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-156">Crea un blob a partir de tipos de Windows Runtime a través del espacio de nombres MSApp en el objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="1298a-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="1298a-157">Este método creará un blob que es esencialmente un contenedor de luz sobre el [objeto RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) que se le proporciona.</span><span class="sxs-lookup"><span data-stu-id="1298a-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="1298a-158">El blob es propietario de la duración de esta secuencia y la secuencia se cerrará cuando se destruya el blob.</span><span class="sxs-lookup"><span data-stu-id="1298a-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-159">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-159">Example</span></span>**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackage"></a><span data-ttu-id="1298a-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="1298a-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-161">Convierte el intervalo especificado del usuario o de la aplicación en un fragmento HTML que se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="1298a-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="1298a-163">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-163">[in]</span></span>  
      
      | <span data-ttu-id="1298a-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-164">Type</span></span> | <span data-ttu-id="1298a-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-166">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-166">Any</span></span> | <span data-ttu-id="1298a-167">Este intervalo se puede crear a partir de un objeto de selección, por ejemplo: `window.selection.getRangeAt(0)` o manualmente.</span><span class="sxs-lookup"><span data-stu-id="1298a-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-168">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-168">Return value</span></span>**  
      
      | <span data-ttu-id="1298a-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-169">Type</span></span> | <span data-ttu-id="1298a-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-171">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-171">Any</span></span> | <span data-ttu-id="1298a-172">Contiene el marcado HTML del intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="1298a-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-173">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-173">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-174">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-175">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-176">Este método solo admite el intervalo del modelo de objetos de documento [(DOM),](https://developer.mozilla.org/docs/Web/API/Range)no [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="1298a-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="1298a-177">El paquete de datos devuelto para el intervalo especificado contiene marcado HTML en formato portapapeles.</span><span class="sxs-lookup"><span data-stu-id="1298a-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="1298a-178">No hay propiedades disponibles para el paquete de datos devuelto.</span><span class="sxs-lookup"><span data-stu-id="1298a-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-179">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-179">Example</span></span>**  
      
      <span data-ttu-id="1298a-180">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createdatapackagefromselection"></a><span data-ttu-id="1298a-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="1298a-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-182">Convierte la selección del usuario o de la aplicación en un fragmento HTML que se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="1298a-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-183">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-183">Parameters</span></span>**  
      
      <span data-ttu-id="1298a-184">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1298a-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-185">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-185">Return value</span></span>**  
      
      | <span data-ttu-id="1298a-186">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-186">Type</span></span> | <span data-ttu-id="1298a-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-188">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-188">Any</span></span> | <span data-ttu-id="1298a-189">Contiene el marcado HTML del intervalo especificado.</span><span class="sxs-lookup"><span data-stu-id="1298a-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-190">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-190">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-191">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-192">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-192">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-193">El paquete de datos devuelto para la selección contiene marcado HTML en formato portapapeles.</span><span class="sxs-lookup"><span data-stu-id="1298a-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="1298a-194">Si no hay ninguna selección de usuario en ninguna parte de la interfaz de usuario de la aplicación, `createDataPackageFromSelection` devuelve `null` .</span><span class="sxs-lookup"><span data-stu-id="1298a-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="1298a-195">No hay propiedades disponibles para el paquete de datos devuelto.</span><span class="sxs-lookup"><span data-stu-id="1298a-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-196">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <a name="createfilefromstoragefile"></a><span data-ttu-id="1298a-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="1298a-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-198">Convierte un objeto [StorageFile de](/uwp/api/windows.storage.storagefile) [WinRT](/uwp/api/) en un objeto [File](https://developer.mozilla.org/docs/Web/API/File) W3C estándar.</span><span class="sxs-lookup"><span data-stu-id="1298a-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-199">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="1298a-200">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-200">[in]</span></span>
      
      | <span data-ttu-id="1298a-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-201">Type</span></span> | <span data-ttu-id="1298a-202">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-203">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-203">Any</span></span> | <span data-ttu-id="1298a-204">Contiene el archivo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="1298a-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-205">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-205">Return value</span></span>**
      
      <span data-ttu-id="1298a-206">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1298a-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-207">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="1298a-208">Excepción</span><span class="sxs-lookup"><span data-stu-id="1298a-208">Exception</span></span> | <span data-ttu-id="1298a-209">Condición</span><span class="sxs-lookup"><span data-stu-id="1298a-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="1298a-210">TypeMismatchError</span></span> | <span data-ttu-id="1298a-211">La referencia de archivo W3C especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="1298a-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="1298a-212">Para versiones anteriores a Internet Explorer 10, `TYPE_MISMATCH_ERR` se devuelve.</span><span class="sxs-lookup"><span data-stu-id="1298a-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-213">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-213">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-214">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-215">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="createstreamfrominputstream"></a><span data-ttu-id="1298a-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="1298a-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-217">Crea un [MSStream](https://msdn.microsoft.com/library/hh772328) a partir de [un InputStream](https://msdn.microsoft.com/library/hh772327).</span><span class="sxs-lookup"><span data-stu-id="1298a-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="1298a-219">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-219">[in]</span></span>
      
      | <span data-ttu-id="1298a-220">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-220">Type</span></span> | <span data-ttu-id="1298a-221">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-222">DOMString</span></span> | <span data-ttu-id="1298a-223">Tipo de contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="1298a-223">Content type of the data.</span></span>  <span data-ttu-id="1298a-224">Esta cadena debe tener el formato especificado en el token de tipo multimedia definido en la sección 3.7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="1298a-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="1298a-225">\([Ver tipos MIME,]( https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) como , , , , , , , y `text/plain` así `text/html` `image/jpeg` `image/png` `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` sucesivamente\).</span><span class="sxs-lookup"><span data-stu-id="1298a-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="1298a-226">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-226">[in]</span></span>
      
      | <span data-ttu-id="1298a-227">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-227">Type</span></span> | <span data-ttu-id="1298a-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-229">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-229">Any</span></span> | <span data-ttu-id="1298a-230">[IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) que se va a almacenar en `MSStream` el archivo .</span><span class="sxs-lookup"><span data-stu-id="1298a-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-231">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-231">Return value</span></span>**
      
      <span data-ttu-id="1298a-232">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-233">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-233">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-234">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-235">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-235">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-236">Este método toma un tipo de contenido y la `IInputStream` referencia.</span><span class="sxs-lookup"><span data-stu-id="1298a-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="1298a-237">A continuación, el método comprueba que la referencia de secuencia pasada es una instancia de tipo y, si `IInputStream` no es así, inicia `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="1298a-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="1298a-238">Si no se produce ningún error, `createStreamFromInputStream` crea `MSStream` un \(a partir de sus entradas\).</span><span class="sxs-lookup"><span data-stu-id="1298a-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-239">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-239">Example</span></span>**  
      
      <span data-ttu-id="1298a-240">An `IInputStream` se puede usar para crear un archivo `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="1298a-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="1298a-241">Al igual que los objetos de uso único inherentes, todas las direcciones URL creadas por se revocan la primera vez que el elemento image lo `MSStreams` `URL.createObjectURL` resuelve.</span><span class="sxs-lookup"><span data-stu-id="1298a-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="1298a-242">Además, se producirá un error en las solicitudes de una segunda dirección URL en este objeto después de usar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="1298a-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execasyncatpriority"></a><span data-ttu-id="1298a-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="1298a-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-244">Programa una devolución de llamada para que se ejecute más adelante según la prioridad especificada.</span><span class="sxs-lookup"><span data-stu-id="1298a-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="1298a-246">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-246">[in]</span></span>
      
      | <span data-ttu-id="1298a-247">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-247">Type</span></span> | <span data-ttu-id="1298a-248">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-249">Función</span><span class="sxs-lookup"><span data-stu-id="1298a-249">Function</span></span> | <span data-ttu-id="1298a-250">Función de devolución de llamada para ejecutarse de forma asincrónica, enviada con la prioridad dada.</span><span class="sxs-lookup"><span data-stu-id="1298a-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="1298a-251">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-251">[in]</span></span>
      
      | <span data-ttu-id="1298a-252">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-252">Type</span></span> | <span data-ttu-id="1298a-253">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-254">DOMString</span></span> | <span data-ttu-id="1298a-255">Valor de prioridad contextual en el que se ejecuta la devolución de llamada asynchronousCallback.</span><span class="sxs-lookup"><span data-stu-id="1298a-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="1298a-256">Vea [MSApp Constants](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="1298a-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="1298a-257">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-257">[in]</span></span>
      
      | <span data-ttu-id="1298a-258">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-258">Type</span></span> | <span data-ttu-id="1298a-259">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="1298a-260">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-260">Any</span></span> | <span data-ttu-id="1298a-261">Una serie opcional de argumentos que se pasan a la función de devolución de llamada sincrónicaCallback \(como parámetros 1 y así sucesivamente\).</span><span class="sxs-lookup"><span data-stu-id="1298a-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-262">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-262">Return value</span></span>**  
      
      <span data-ttu-id="1298a-263">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="1298a-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-264">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-264">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-265">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-266">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-266">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-267">La función `asynchronousCallback` de devolución de llamada proporcionada se ejecuta de forma asincrónica más adelante.</span><span class="sxs-lookup"><span data-stu-id="1298a-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="1298a-268">se enviará de acuerdo con la prioridad proporcionada.</span><span class="sxs-lookup"><span data-stu-id="1298a-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="1298a-269">La prioridad normal es equivalente al método [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existente.</span><span class="sxs-lookup"><span data-stu-id="1298a-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="1298a-270">Cuando se ejecuta la devolución de llamada, la prioridad contextual actual se establece en el valor del parámetro priority proporcionado durante la ejecución de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1298a-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="1298a-271">El `asynchronousCallback` parámetro callback puede ser cualquier función.</span><span class="sxs-lookup"><span data-stu-id="1298a-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="1298a-272">Si se proporcionan argumentos después del parámetro, todos se pasarán `priority` a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1298a-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="1298a-273">A diferencia de , cualquier objeto devuelto por la función de devolución de llamada se omite `execAtPriority` `asynchronousCallback` \(y no se devuelve a través `execAsyncAtPriority` de \).</span><span class="sxs-lookup"><span data-stu-id="1298a-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-274">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="execatpriority"></a><span data-ttu-id="1298a-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="1298a-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-276">Ejecuta la función de devolución de llamada especificada con la prioridad contextual especificada.</span><span class="sxs-lookup"><span data-stu-id="1298a-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-277">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="1298a-278">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-278">[in]</span></span>  
      
      | <span data-ttu-id="1298a-279">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-279">Type</span></span> | <span data-ttu-id="1298a-280">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-281">Función</span><span class="sxs-lookup"><span data-stu-id="1298a-281">Function</span></span> | <span data-ttu-id="1298a-282">Función de devolución de llamada para ejecutarse sincrónicamente con la prioridad contextual de prioridad dada.</span><span class="sxs-lookup"><span data-stu-id="1298a-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="1298a-283">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-283">[in]</span></span>  
      
      | <span data-ttu-id="1298a-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-284">Type</span></span> | <span data-ttu-id="1298a-285">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-286">DOMString</span></span> | <span data-ttu-id="1298a-287">Valor de prioridad especificado en el que se establecerá el valor de prioridad contextual actual al ejecutar la `synchronousCallback` función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1298a-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="1298a-288">Vea [MSApp Constants](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="1298a-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="1298a-289">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-289">[in]</span></span>  
      
      | <span data-ttu-id="1298a-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-290">Type</span></span> | <span data-ttu-id="1298a-291">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-292">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-292">Any</span></span> | <span data-ttu-id="1298a-293">Una serie opcional de argumentos que se pasan a la función de devolución de llamada `synchronousCallback` \(como parámetros 1 y así sucesivamente\).</span><span class="sxs-lookup"><span data-stu-id="1298a-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-294">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-294">Return value</span></span>**  
      
      | <span data-ttu-id="1298a-295">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-295">Type</span></span> | <span data-ttu-id="1298a-296">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-297">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-297">Any</span></span> | <span data-ttu-id="1298a-298">Devuelve el valor devuelto de la `synchronousCallback` devolución de llamada \(as applicable\).</span><span class="sxs-lookup"><span data-stu-id="1298a-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-299">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-299">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-300">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-301">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-301">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-302">El método `synchronousCallback` de devolución de llamada proporcionado se ejecuta sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="1298a-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="1298a-303">La prioridad contextual actual se cambia al valor de prioridad proporcionado (dado por el argumento priority) durante la duración de la función de devolución de llamada proporcionada.</span><span class="sxs-lookup"><span data-stu-id="1298a-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="1298a-304">Una vez que la función de devolución de llamada termina de ejecutarse, se devuelve prioridad al valor anterior antes de la `execAtPriority` llamada.</span><span class="sxs-lookup"><span data-stu-id="1298a-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="1298a-305">El valor devuelto de `execAtPriority` es el valor devuelto del método de devolución de llamada \(como se proporciona\).</span><span class="sxs-lookup"><span data-stu-id="1298a-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="1298a-306">El `synchronousCallback` parámetro callback puede ser cualquier función.</span><span class="sxs-lookup"><span data-stu-id="1298a-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="1298a-307">Si se proporcionan argumentos después del parámetro priority, se pasarán al método de devolución de llamada proporcionado.</span><span class="sxs-lookup"><span data-stu-id="1298a-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="1298a-308">Si el parámetro callback devuelve un valor, este valor se convierte también en el valor `execAtPriority` devuelto.</span><span class="sxs-lookup"><span data-stu-id="1298a-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-309">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-309">Example</span></span>**  
      
      ```javascript
      var user = Windows.System.UserProfile.UserInformation;
      
      MSApp.execAtPriority(function () { // This callback executes synchronously.
        user.getFirstNameAsync().then(function () { // Dispatches at high priority.
          return user.getLastNameAsync();
        }).done(function () { // Dispatches at high priority.
          // USEFUL CODE HERE
        });
      }, MSApp.HIGH); // The second argument of the execAtPriority method.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="getcurrentpriority"></a><span data-ttu-id="1298a-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="1298a-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-311">Devuelve la prioridad contextual actual.</span><span class="sxs-lookup"><span data-stu-id="1298a-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-312">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-312">Parameters</span></span>**  
      
      <span data-ttu-id="1298a-313">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-314">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-314">Return value</span></span>**  
      
      | <span data-ttu-id="1298a-315">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-315">Type</span></span> | <span data-ttu-id="1298a-316">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-317">DOMString</span></span> | <span data-ttu-id="1298a-318">El valor devuelto es una de las cadenas `MSApp.HIGH` `MSApp.NORMAL` , o `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="1298a-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-319">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-319">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-320">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-321">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-321">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-322">Este método devuelve la prioridad contextual actual \(see [MSApp Constants](#msapp-constants)\), que se puede cambiar a través `execAtPriority` de y `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="1298a-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-323">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-323">Example</span></span>**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="gethtmlprintdocumentsource"></a><span data-ttu-id="1298a-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="1298a-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="1298a-325">API sincrónica que ha quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="1298a-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="1298a-326">Para Windows 10, consulta `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="1298a-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="1298a-327">Para las aplicaciones de Windows 8 y 8.1, consulta la entrada de MSDN [para getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="1298a-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <a name="gethtmlprintdocumentsourceasync"></a><span data-ttu-id="1298a-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="1298a-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-329">Devuelve el contenido de origen que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="1298a-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-330">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="1298a-331">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-331">[in]</span></span>  
      
      | <span data-ttu-id="1298a-332">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-332">Type</span></span> | <span data-ttu-id="1298a-333">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-334">Documento</span><span class="sxs-lookup"><span data-stu-id="1298a-334">Document</span></span> | <span data-ttu-id="1298a-335">Documento HTML que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="1298a-335">The HTML document to be printed.</span></span>  <span data-ttu-id="1298a-336">Puede ser el documento raíz, el documento en un iframe, un fragmento de documento o un documento SVG.</span><span class="sxs-lookup"><span data-stu-id="1298a-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="1298a-337">Tenga en cuenta que htmlDoc debe ser un documento, no un elemento.</span><span class="sxs-lookup"><span data-stu-id="1298a-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-338">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-338">Return value</span></span>**
      
      <span data-ttu-id="1298a-339">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-340">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-340">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-341">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-342">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-342">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-343">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-344">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="1298a-344">Example 1</span></span>**  
      
      ```javascript
      var printTask = event.request.createPrintTask(title, function (args) {
              var deferral = args.getDeferral();
              var getPrintDocumentSourceAsync;
              if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                  getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
              } else {
                  getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
              }
              getPrintDocumentSourceAsync.then(function (source) {
                  args.setSource(source);
                  deferral.complete();
              }, function (error) {
                  console.error(error);
                  deferral.complete();
              });
      });
      ```  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-345">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="1298a-345">Example 2</span></span>**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
      }
      
      // Variable to hold the document source to print
      var gHtmlPrintDocumentSource = null;
      
      // Print event handler for printing via the PrintManager API.
      function onPrintTaskRequested(printEvent) {
          var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
              args.setSource(gHtmlPrintDocumentSource);
      
              // Register the handler for print task completion event
              printTask.oncompleted = onPrintTaskCompleted;
          });
      }
      
      // Print Task event handler is invoked when the print job is completed.
      function onPrintTaskCompleted(printTaskCompletionEvent) {
          // Notify the user about the failure
          if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
              console.log("Failed to print.", "sample", "error");
          }
      }
      
      // Executed just before printing.
      var beforePrint = function () {
          // Replace with code to be executed just before printing the current document:
      };
      
      // Executed immediately after printing.
      var afterPrint = function () {
          // Replace with code to be executed immediately after printing the current document:
      };
      
      function printButtonHandler() {
          // Optionally, functions to be executed immediately before and after printing can be configured as following:
          window.document.body.onbeforeprint = beforePrint;
          window.document.body.onafterprint = afterPrint;
          
          // Get document source to print
          MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
              gHtmlPrintDocumentSource = htmlPrintDocumentSource;
      
              // If the print contract is registered, the print experience is invoked.
              Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
          });
      }
      ```  
   :::column-end:::
:::row-end:::  

### <a name="getviewid"></a><span data-ttu-id="1298a-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="1298a-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-347">Compatibilidad con varias ventanas.</span><span class="sxs-lookup"><span data-stu-id="1298a-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="1298a-348">En Win8.1, las aplicaciones para UWP de JavaScript admiten varias ventanas con LAS API dom de MSApp que ahora están depricadas.</span><span class="sxs-lookup"><span data-stu-id="1298a-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="1298a-349">Para Windows 10, usa `window.open` , y el nuevo `window` `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="1298a-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="1298a-350">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-350">Description</span></span> |<span data-ttu-id="1298a-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="1298a-351">Windows 10</span></span> | <span data-ttu-id="1298a-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1298a-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="1298a-353">Crear nueva ventana</span><span class="sxs-lookup"><span data-stu-id="1298a-353">Create new window</span></span> | [<span data-ttu-id="1298a-354">window.open</span><span class="sxs-lookup"><span data-stu-id="1298a-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="1298a-355">MSApp.createNewView</span><span class="sxs-lookup"><span data-stu-id="1298a-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="1298a-356">Nuevo objeto window</span><span class="sxs-lookup"><span data-stu-id="1298a-356">New window object</span></span> | [<span data-ttu-id="1298a-357">ventana</span><span class="sxs-lookup"><span data-stu-id="1298a-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="1298a-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="1298a-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-359">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="1298a-360">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-360">Type</span></span> | <span data-ttu-id="1298a-361">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-362">DOMString</span></span> | <span data-ttu-id="1298a-363">Un objeto que representa una ventana que contiene un documento DOM.</span><span class="sxs-lookup"><span data-stu-id="1298a-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-364">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="1298a-365">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-365">Type</span></span> | <span data-ttu-id="1298a-366">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-367">Número</span><span class="sxs-lookup"><span data-stu-id="1298a-367">Number</span></span> | <span data-ttu-id="1298a-368">Se puede usar con las distintas [API de Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="1298a-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-369">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-369">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-370">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-371">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-371">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-372">Usa [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) y [window](https://developer.mozilla.org/docs/Web/API/Window) para crear ventanas nuevas, pero luego para interactuar con las API de WinRT, agrega la `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="1298a-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="1298a-373">Toma un objeto como parámetro y devuelve un número que se puede usar con las `window` `viewId` distintas API [de Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="1298a-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="1298a-374">Retrasar la visibilidad</span><span class="sxs-lookup"><span data-stu-id="1298a-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="1298a-375">Las vistas de WinRT normalmente comienzan ocultas y el desarrollador final usa algo parecido a mostrar la vista una vez `TryShowAsStandaloneAsync` que está totalmente preparada.</span><span class="sxs-lookup"><span data-stu-id="1298a-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="1298a-376">En el mundo web, muestra una ventana inmediatamente y el usuario final puede ver cómo se carga y `window.open` representa el contenido.</span><span class="sxs-lookup"><span data-stu-id="1298a-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="1298a-377">Para que las ventanas nuevas actúen como vistas en WinRT y no se muestren inmediatamente, hemos agregado una `window.open` opción.</span><span class="sxs-lookup"><span data-stu-id="1298a-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="1298a-378">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="1298a-379">Diferencias de ventana principal</span><span class="sxs-lookup"><span data-stu-id="1298a-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="1298a-380">La ventana principal que abre inicialmente el sistema operativo actúa de forma diferente que las ventanas secundarias que se abren:</span><span class="sxs-lookup"><span data-stu-id="1298a-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="1298a-381">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-381">Description</span></span> | <span data-ttu-id="1298a-382">Principal</span><span class="sxs-lookup"><span data-stu-id="1298a-382">Primary</span></span> | <span data-ttu-id="1298a-383">Secundario</span><span class="sxs-lookup"><span data-stu-id="1298a-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="1298a-384">window.open</span><span class="sxs-lookup"><span data-stu-id="1298a-384">window.open</span></span> | <span data-ttu-id="1298a-385">Se permite</span><span class="sxs-lookup"><span data-stu-id="1298a-385">Allowed</span></span> | <span data-ttu-id="1298a-386">No permitido</span><span class="sxs-lookup"><span data-stu-id="1298a-386">Disallowed</span></span> |  
          | <span data-ttu-id="1298a-387">window.close</span><span class="sxs-lookup"><span data-stu-id="1298a-387">window.close</span></span> | <span data-ttu-id="1298a-388">Cerrar aplicación</span><span class="sxs-lookup"><span data-stu-id="1298a-388">Close app</span></span> | <span data-ttu-id="1298a-389">Cerrar ventana</span><span class="sxs-lookup"><span data-stu-id="1298a-389">Close window</span></span> |  
          | <span data-ttu-id="1298a-390">Restricciones de navegación</span><span class="sxs-lookup"><span data-stu-id="1298a-390">Navigation restrictions</span></span> | <span data-ttu-id="1298a-391">Solo ACUR</span><span class="sxs-lookup"><span data-stu-id="1298a-391">ACUR only</span></span> | <span data-ttu-id="1298a-392">Sin restricciones</span><span class="sxs-lookup"><span data-stu-id="1298a-392">No restrictions</span></span> |  
          
         <!-- The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).  -->  
      
      *   <span data-ttu-id="1298a-393">Restricciones de comunicación del mismo origen</span><span class="sxs-lookup"><span data-stu-id="1298a-393">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="1298a-394">Hay un problema técnico difícil que impide que se admitan correctamente las llamadas sincrónicas, del mismo origen, entre ventanas y scripts.</span><span class="sxs-lookup"><span data-stu-id="1298a-394">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="1298a-395">Al abrir una ventana que tiene el mismo origen, el script de una ventana puede llamar directamente a las funciones de la otra ventana y algunas de estas llamadas producirán un error.</span><span class="sxs-lookup"><span data-stu-id="1298a-395">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="1298a-396">las llamadas funcionan bien y es la forma recomendada de hacer las cosas si es posible.</span><span class="sxs-lookup"><span data-stu-id="1298a-396">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="1298a-397">Se está trabajando para mejorar este problema.</span><span class="sxs-lookup"><span data-stu-id="1298a-397">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-398">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-398">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <a name="istaskscheduledatpriorityorhigher"></a><span data-ttu-id="1298a-399">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="1298a-399">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-400">Devuelve un valor booleano que indica si hay trabajo pendiente en el nivel de prioridad dado o superior.</span><span class="sxs-lookup"><span data-stu-id="1298a-400">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-401">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-401">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="1298a-402">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-402">[in]</span></span>
      
      | <span data-ttu-id="1298a-403">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-403">Type</span></span> | <span data-ttu-id="1298a-404">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-404">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-405">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-405">DOMString</span></span> | <span data-ttu-id="1298a-406">Valor de prioridad \(vea [MSApp Constants](#msapp-constants)\) que especifica el nivel de prioridad y superior para consultar cualquier trabajo en cola pendiente.</span><span class="sxs-lookup"><span data-stu-id="1298a-406">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-407">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-407">Return value</span></span>**  
      
      | <span data-ttu-id="1298a-408">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-408">Type</span></span> | <span data-ttu-id="1298a-409">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-409">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-410">Booleano</span><span class="sxs-lookup"><span data-stu-id="1298a-410">Boolean</span></span> | <span data-ttu-id="1298a-411">Devuelve si hay algún trabajo en cola en el nivel de prioridad especificado `true` o superior, de lo `false` contrario.</span><span class="sxs-lookup"><span data-stu-id="1298a-411">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-412">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-412">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-413">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-413">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-414">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-414">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-415">El método proporciona un medio para que el código JavaScript determine si hay trabajo pendiente en los distintos niveles de prioridad \(o superior\) con la intención de que el código JavaScript que llama pueda decidir ceder al trabajo de mayor `isTaskScheduledAtPriorityOrHigher` prioridad.</span><span class="sxs-lookup"><span data-stu-id="1298a-415">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-416">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-416">Example</span></span>**  
      
      ```javascript
      function performIdleWork(array_in) {
          var idx = 0;
          
          function performIdleWorkHelper() {
              for (; idx < array_in.length; ++idx) {
                  
                  // USEFUL CODE HERE 
                  
                  if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
                      MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
                      break;
                  } // if
              } // for
          } // performIdleWorkHelper
          
          performIdleWorkHelper();
      } // performIdleWork
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="pagehandlesallapplicationactivations"></a><span data-ttu-id="1298a-417">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="1298a-417">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-418">Se usa para evitar una actualización de la ruta de inicio (recarga de página) antes de cada evento de activación \(como hacer clic en una notificación o en un icono anclado\).</span><span class="sxs-lookup"><span data-stu-id="1298a-418">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-419">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-419">Parameters</span></span>**  
      
      | <span data-ttu-id="1298a-420">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-420">Type</span></span> | <span data-ttu-id="1298a-421">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-421">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-422">Booleano</span><span class="sxs-lookup"><span data-stu-id="1298a-422">Boolean</span></span> | <span data-ttu-id="1298a-423">Se usa para omitir siempre actualizar la ruta de inicio (recarga de página) y, en su lugar, saltar directamente a `MSApp.pageHandlesAllApplicationActivations(true)` activar el `WebUIApplication` evento activado.</span><span class="sxs-lookup"><span data-stu-id="1298a-423">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="1298a-424">Requiere que todas las páginas controle los eventos de activación por separado.</span><span class="sxs-lookup"><span data-stu-id="1298a-424">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="1298a-425">Al definir este método como , al hacer clic en un evento activado \(like a notification\) no se desencadenará la recarga, algo esencial para las aplicaciones de una sola página que deseen evitar las `true` recargas de página.</span><span class="sxs-lookup"><span data-stu-id="1298a-425">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-426">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-426">Return value</span></span>**
      
      <span data-ttu-id="1298a-427">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-427">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-428">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-428">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-429">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-429">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-430">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-430">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-431">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-431">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-432">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-432">Example</span></span>**  
      
      ```javascript
      // Without this, the app will first refresh to the start path before every activate event
      window.MSApp.pageHandlesAllApplicationActivations(true); 
      
      // This must not be deffered so that it can receive the initial `activated` event in time
      window.Windows.UI.WebUI.WebUIApplication.addEventListener(
          `activated`,
          e =>
              microsoftInterface.handleActivatedEvent(e);
          }),
          false
      );
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="suppresssubdownloadcredentialprompts"></a><span data-ttu-id="1298a-433">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="1298a-433">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-434">Controla si una aplicación suprime los posibles mensajes de autenticación durante la descarga de recursos.</span><span class="sxs-lookup"><span data-stu-id="1298a-434">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-435">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-435">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="1298a-436">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-436">[in]</span></span>
      
      | <span data-ttu-id="1298a-437">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-437">Type</span></span> | <span data-ttu-id="1298a-438">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-438">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-439">Booleano</span><span class="sxs-lookup"><span data-stu-id="1298a-439">Boolean</span></span> | <span data-ttu-id="1298a-440">Un valor true suprime los mensajes de autenticación potenciales.</span><span class="sxs-lookup"><span data-stu-id="1298a-440">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="1298a-441">Un valor de false no suprime los posibles mensajes de autenticación del usuario.</span><span class="sxs-lookup"><span data-stu-id="1298a-441">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-442">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-442">Return value</span></span>**  
      
      <span data-ttu-id="1298a-443">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-443">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-444">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-444">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-445">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-445">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-446">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-446">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-447">El método controla si una aplicación suprime los posibles mensajes de `suppressSubdownloadCredentialPrompts` autenticación durante la descarga de recursos.</span><span class="sxs-lookup"><span data-stu-id="1298a-447">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="1298a-448">El comportamiento predeterminado es no suprimir los mensajes de credenciales.</span><span class="sxs-lookup"><span data-stu-id="1298a-448">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="1298a-449">está diseñada para su uso por aplicaciones que pueden cargar un número excesivo de recursos que requieren autenticación, como una aplicación de correo \(que podría contener un boletín que contenga un número de imágenes donde cada imagen requiere autenticación\).</span><span class="sxs-lookup"><span data-stu-id="1298a-449">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="1298a-450">Cuando se suprimen los mensajes de credenciales, los cuadros de diálogo para la autenticación en los servidores no se mostrarán al obtener acceso a los recursos que requieren autenticación y el recurso no se descargará.</span><span class="sxs-lookup"><span data-stu-id="1298a-450">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="1298a-451">Tenga en cuenta que no afecta a otros mensajes posibles, como la autenticación proxy o los cuadros de diálogo de solicitud de certificación de cliente, ni afecta `suppressSubdownloadCredentialPrompts` a XHR.</span><span class="sxs-lookup"><span data-stu-id="1298a-451">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="1298a-452">Tenga en cuenta `suppressSubdownloadCredentialPrompts` que afecta a todo el contenido de la aplicación, incluido el contenido hospedado en el `webview` elemento.</span><span class="sxs-lookup"><span data-stu-id="1298a-452">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="1298a-453">Las decisiones de solicitud de credenciales se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="1298a-453">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="1298a-454">Por lo tanto, mientras se suprimen los mensajes de credenciales tendrá efecto inmediatamente, para que los mensajes de credenciales después de suprimirlos necesiten una recarga del documento para que su efecto.</span><span class="sxs-lookup"><span data-stu-id="1298a-454">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-455">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-455">Example</span></span>**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="terminateapp"></a><span data-ttu-id="1298a-456">terminateApp</span><span class="sxs-lookup"><span data-stu-id="1298a-456">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-457">Termina la aplicación actual y genera un informe de errores.</span><span class="sxs-lookup"><span data-stu-id="1298a-457">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-458">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-458">Parameters</span></span>**  
      
      `error` <span data-ttu-id="1298a-459">[in]</span><span class="sxs-lookup"><span data-stu-id="1298a-459">[in]</span></span>
      
      | <span data-ttu-id="1298a-460">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-460">Type</span></span> | <span data-ttu-id="1298a-461">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-461">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-462">Error</span><span class="sxs-lookup"><span data-stu-id="1298a-462">Error</span></span> | <span data-ttu-id="1298a-463">Objeto `Error` que puede usar para describir el error que desencadenó la terminación.</span><span class="sxs-lookup"><span data-stu-id="1298a-463">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="1298a-464">El objeto debe contener el número, la descripción y las propiedades de la pila; no se generará un informe de errores si el objeto no `Error` contiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1298a-464">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-465">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-465">Return value</span></span>**
      
      <span data-ttu-id="1298a-466">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-466">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-467">Excepciones</span><span class="sxs-lookup"><span data-stu-id="1298a-467">Exceptions</span></span>**  
      
      <span data-ttu-id="1298a-468">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-468">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-469">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1298a-469">Remarks</span></span>**  
      
      <span data-ttu-id="1298a-470">Si el problema notificado por se convierte en uno de los 5 problemas principales de la aplicación, aparecerá en la página `terminateApp` Calidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1298a-470">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-471">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-471">Example</span></span>**  
      
      <span data-ttu-id="1298a-472">En este ejemplo se `terminateApp` llama cuando se encuentra una excepción.</span><span class="sxs-lookup"><span data-stu-id="1298a-472">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="1298a-473">Usa el objeto `Error` proporcionado al detectar una excepción.</span><span class="sxs-lookup"><span data-stu-id="1298a-473">It uses the `Error` object provided when you catch an exception.</span></span>  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <a name="msapp-constants"></a><span data-ttu-id="1298a-474">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="1298a-474">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-475">Valores de prioridad permitidos `execAsyncAtPriority` asociados con `execAtPriority` , , `getCurrentPriority` y `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="1298a-475">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <a name="current"></a><span data-ttu-id="1298a-476">Actual</span><span class="sxs-lookup"><span data-stu-id="1298a-476">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="1298a-477">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-477">Type</span></span> | <span data-ttu-id="1298a-478">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-478">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-479">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-479">DOMString</span></span> | <span data-ttu-id="1298a-480">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span><span class="sxs-lookup"><span data-stu-id="1298a-480">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="high"></a><span data-ttu-id="1298a-481">Alto</span><span class="sxs-lookup"><span data-stu-id="1298a-481">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="1298a-482">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-482">Type</span></span> | <span data-ttu-id="1298a-483">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-483">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-484">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-484">DOMString</span></span> | <span data-ttu-id="1298a-485">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span><span class="sxs-lookup"><span data-stu-id="1298a-485">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <a name="idle"></a><span data-ttu-id="1298a-486">Inactivo</span><span class="sxs-lookup"><span data-stu-id="1298a-486">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="1298a-487">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-487">Type</span></span> | <span data-ttu-id="1298a-488">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-488">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-489">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-489">DOMString</span></span> | <span data-ttu-id="1298a-490">Cuando se usa con el método adecuado \(Vea también section\), el método usará una prioridad inferior a la normal al ejecutar la operación solicitada y se enviará la operación después de cualquier trabajo de prioridad `ideal` normal existente.</span><span class="sxs-lookup"><span data-stu-id="1298a-490">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <a name="normal"></a><span data-ttu-id="1298a-491">Normal</span><span class="sxs-lookup"><span data-stu-id="1298a-491">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="1298a-492">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-492">Type</span></span> | <span data-ttu-id="1298a-493">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-493">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-494">DOMString</span><span class="sxs-lookup"><span data-stu-id="1298a-494">DOMString</span></span> | <span data-ttu-id="1298a-495">Cuando se usa con el método adecuado (vea también la sección), el método usará la prioridad existente normal al `normal` ejecutar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="1298a-495">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-496">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1298a-496">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-497">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1298a-497">Requirements</span></span>**  
      
      | <span data-ttu-id="1298a-498">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-498">Type</span></span> | <span data-ttu-id="1298a-499">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-499">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-500">IDL</span><span class="sxs-lookup"><span data-stu-id="1298a-500">IDL</span></span> | <span data-ttu-id="1298a-501">Mshtml.idl</span><span class="sxs-lookup"><span data-stu-id="1298a-501">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <a name="msappasyncoperation"></a><span data-ttu-id="1298a-502">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="1298a-502">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <a name="start"></a><span data-ttu-id="1298a-503">start</span><span class="sxs-lookup"><span data-stu-id="1298a-503">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="1298a-504">Inicia `MSAppAsyncOperation` el archivo .</span><span class="sxs-lookup"><span data-stu-id="1298a-504">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="1298a-505">Parameters</span><span class="sxs-lookup"><span data-stu-id="1298a-505">Parameters</span></span>**  
      
      <span data-ttu-id="1298a-506">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-506">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="1298a-507">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1298a-507">Return value</span></span>**
      
      <span data-ttu-id="1298a-508">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="1298a-508">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="1298a-509">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1298a-509">Properties</span></span>**  
      
      `error` <span data-ttu-id="1298a-510">propiedad</span><span class="sxs-lookup"><span data-stu-id="1298a-510">property</span></span>  
      
      | <span data-ttu-id="1298a-511">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-511">Type</span></span> | <span data-ttu-id="1298a-512">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-512">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-513">DOMError</span><span class="sxs-lookup"><span data-stu-id="1298a-513">DOMError</span></span> | <span data-ttu-id="1298a-514">Representa un error en `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1298a-514">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="1298a-515">propiedad</span><span class="sxs-lookup"><span data-stu-id="1298a-515">property</span></span>  
      
      | <span data-ttu-id="1298a-516">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-516">Type</span></span> | <span data-ttu-id="1298a-517">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-517">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-518">EventHandler</span><span class="sxs-lookup"><span data-stu-id="1298a-518">EventHandler</span></span> | <span data-ttu-id="1298a-519">Propiedad para establecer un controlador de eventos al completar `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1298a-519">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="1298a-520">propiedad</span><span class="sxs-lookup"><span data-stu-id="1298a-520">property</span></span>  
      
      | <span data-ttu-id="1298a-521">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-521">Type</span></span> | <span data-ttu-id="1298a-522">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-522">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-523">EventHandler</span><span class="sxs-lookup"><span data-stu-id="1298a-523">EventHandler</span></span> | <span data-ttu-id="1298a-524">Propiedad para establecer un controlador de eventos tras un error durante `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1298a-524">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="1298a-525">propiedad</span><span class="sxs-lookup"><span data-stu-id="1298a-525">property</span></span>  
      
      | <span data-ttu-id="1298a-526">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-526">Type</span></span> | <span data-ttu-id="1298a-527">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-527">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-528">Número</span><span class="sxs-lookup"><span data-stu-id="1298a-528">Number</span></span> | <span data-ttu-id="1298a-529">Representa el estado de la operación asincrónica dentro de la aplicación windows mediante JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1298a-529">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="1298a-530">Los valores incluyen: `Started[0]` `Completed[1]` , , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="1298a-530">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="1298a-531">propiedad</span><span class="sxs-lookup"><span data-stu-id="1298a-531">property</span></span>  
      
      | <span data-ttu-id="1298a-532">Tipo</span><span class="sxs-lookup"><span data-stu-id="1298a-532">Type</span></span> | <span data-ttu-id="1298a-533">Descripción</span><span class="sxs-lookup"><span data-stu-id="1298a-533">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="1298a-534">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="1298a-534">Any</span></span> |<span data-ttu-id="1298a-535">Representa el resultado de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="1298a-535">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

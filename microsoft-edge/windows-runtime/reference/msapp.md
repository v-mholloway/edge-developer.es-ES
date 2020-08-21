---
title: Referencia de la API de MSApp
description: Proporciona funciones auxiliares que permiten crear objetos BLOB y MSStream.  Los objetos y miembros de MSApp son compatibles con las aplicaciones de Windows que usan JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/29/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carga de archivos, blog, MSStream, aplicaciones de Windows 10, UWP, Edge
ms.openlocfilehash: 4966f6afbe4e971d6a366de7e9b4f5a6cd2305e0
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942163"
---
# <span data-ttu-id="cd389-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="cd389-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="cd389-106">El objeto MSApp y sus miembros solo se admiten en aplicaciones de Windows que usen JavaScript \ (incluyendo PWAs de acceso a las características de la API de Windows \).</span><span class="sxs-lookup"><span data-stu-id="cd389-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="cd389-107">El objeto MSApp solo existe en el contexto local de un documento HTML en una aplicación de Windows que se carga mediante el esquema de URI MS-appx; de lo contrario, el objeto no existe (y, por lo tanto, ninguno de sus métodos y propiedades está disponible).</span><span class="sxs-lookup"><span data-stu-id="cd389-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="cd389-108">Proporciona funciones auxiliares que permiten crear objetos [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) y [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="cd389-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="cd389-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd389-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cd389-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority, getHtmlPrintDocumentSource](#getcurrentpriority),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId, isTaskScheduledAtPriorityOrHigher](#getviewid) [, pageHandlesAllApplicationActivations](#istaskscheduledatpriorityorhigher) [, suppressSubdownloadCredentialPrompts, terminateApp.](#pagehandlesallapplicationactivations) [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource) [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts) [terminateApp](#terminateapp)</span><span class="sxs-lookup"><span data-stu-id="cd389-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cd389-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="cd389-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cd389-112">[actual](#current), [alta](#high), [inactiva](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="cd389-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cd389-113">Interfaz MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="cd389-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="cd389-114">start</span><span class="sxs-lookup"><span data-stu-id="cd389-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="cd389-115">Métodos de MSApp</span><span class="sxs-lookup"><span data-stu-id="cd389-115">MSApp methods</span></span>  

### <span data-ttu-id="cd389-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="cd389-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-117">Borra los datos de caché y indexedDB de la aplicación o [WebView](../../webview.md).</span><span class="sxs-lookup"><span data-stu-id="cd389-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-118">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-118">Parameters</span></span>**  
      
      <span data-ttu-id="cd389-119">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cd389-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-120">Return value</span></span>**  
      
      <span data-ttu-id="cd389-121">Escriba: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="cd389-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="cd389-122">Representa una acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cd389-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-123">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-123">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-124">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-125">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-126">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cd389-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="cd389-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-129">Crea un objeto [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) a partir de un objeto [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) .</span><span class="sxs-lookup"><span data-stu-id="cd389-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="cd389-130">Este método se debe usar cuando se trata de `IRandomAccessStream` objetos en aplicaciones para crear un objeto basado en el consorcio desde la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cd389-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="cd389-131">Una vez creado el BLOB, se puede usar con el [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), las [API de la dirección URL](https://developer.mozilla.org/docs/Web/API/URL)y [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="cd389-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-132">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="cd389-133">por</span><span class="sxs-lookup"><span data-stu-id="cd389-133">[in]</span></span>  
      
      | <span data-ttu-id="cd389-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-134">Type</span></span> | <span data-ttu-id="cd389-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="cd389-136">String</span></span> | <span data-ttu-id="cd389-137">Tipo de contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="cd389-137">Content type of the data.</span></span>  <span data-ttu-id="cd389-138">Esta cadena debe estar en el formato especificado en el símbolo de tipo multimedia definido en la sección 3,7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="cd389-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="cd389-139">por</span><span class="sxs-lookup"><span data-stu-id="cd389-139">[in]</span></span>  
      
      | <span data-ttu-id="cd389-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-140">Type</span></span> | <span data-ttu-id="cd389-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-142">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-142">Any</span></span> | <span data-ttu-id="cd389-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) que se va a almacenar en el BLOB.</span><span class="sxs-lookup"><span data-stu-id="cd389-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-144">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-144">Return value</span></span>**  
      
      | <span data-ttu-id="cd389-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-145">Type</span></span> | <span data-ttu-id="cd389-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-147">Manchas</span><span class="sxs-lookup"><span data-stu-id="cd389-147">Blob</span></span> | <span data-ttu-id="cd389-148">Nuevo objeto BLOB que contiene la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cd389-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-149">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="cd389-150">Excepción</span><span class="sxs-lookup"><span data-stu-id="cd389-150">Exception</span></span> | <span data-ttu-id="cd389-151">Condición</span><span class="sxs-lookup"><span data-stu-id="cd389-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="cd389-152">TypeMismatchError</span></span> | <span data-ttu-id="cd389-153">El tipo de nodo es incompatible con el tipo de parámetro esperado.</span><span class="sxs-lookup"><span data-stu-id="cd389-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="cd389-154">En el caso de versiones anteriores a Internet Explorer 10, se devuelve TYPE_MISMATCH_ERR.</span><span class="sxs-lookup"><span data-stu-id="cd389-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-155">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-156">Crea un BLOB a partir de los tipos de Windows Runtime a través del espacio de nombres MSApp en el objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="cd389-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="cd389-157">Este método creará un BLOB que es esencialmente un contenedor de luz sobre el objeto [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="cd389-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="cd389-158">El BLOB es propietario de la duración de esta secuencia y la secuencia se cerrará cuando se destruya el BLOB.</span><span class="sxs-lookup"><span data-stu-id="cd389-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-159">Example</span></span>**  
      
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

### <span data-ttu-id="cd389-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="cd389-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-161">Convierte el intervalo especificado del usuario o la aplicación en un fragmento de HTML que se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="cd389-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-162">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="cd389-163">por</span><span class="sxs-lookup"><span data-stu-id="cd389-163">[in]</span></span>  
      
      | <span data-ttu-id="cd389-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-164">Type</span></span> | <span data-ttu-id="cd389-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-166">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-166">Any</span></span> | <span data-ttu-id="cd389-167">Este rango puede crearse desde un objeto de selección, por ejemplo: `window.selection.getRangeAt(0)` , o manualmente.</span><span class="sxs-lookup"><span data-stu-id="cd389-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-168">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-168">Return value</span></span>**  
      
      | <span data-ttu-id="cd389-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-169">Type</span></span> | <span data-ttu-id="cd389-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-171">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-171">Any</span></span> | <span data-ttu-id="cd389-172">Contiene el formato HTML del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="cd389-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-173">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-173">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-174">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-175">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-176">Este método solo admite el [rango Dom (modelo de objetos de documento)](https://developer.mozilla.org/docs/Web/API/Range), no [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="cd389-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="cd389-177">El paquete de datos devuelto para el intervalo especificado contiene formato HTML en el formato del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="cd389-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="cd389-178">No hay ninguna propiedad disponible para el paquete de datos devuelto.</span><span class="sxs-lookup"><span data-stu-id="cd389-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-179">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-179">Example</span></span>**  
      
      <span data-ttu-id="cd389-180">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cd389-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="cd389-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-182">Convierte la selección del usuario o la aplicación en un fragmento HTML que se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="cd389-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-183">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-183">Parameters</span></span>**  
      
      <span data-ttu-id="cd389-184">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cd389-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-185">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-185">Return value</span></span>**  
      
      | <span data-ttu-id="cd389-186">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-186">Type</span></span> | <span data-ttu-id="cd389-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-188">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-188">Any</span></span> | <span data-ttu-id="cd389-189">Contiene el formato HTML del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="cd389-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-190">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-190">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-191">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-192">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-192">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-193">El paquete de datos devuelto para la selección contiene marcado HTML en formato de Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="cd389-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="cd389-194">Si no hay ninguna selección del usuario en ninguna parte de la interfaz de usuario de la aplicación, devuelve el número `createDataPackageFromSelection` `null` .</span><span class="sxs-lookup"><span data-stu-id="cd389-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="cd389-195">No hay ninguna propiedad disponible para el paquete de datos devuelto.</span><span class="sxs-lookup"><span data-stu-id="cd389-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <span data-ttu-id="cd389-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="cd389-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-198">Convierte un [StorageFile](/uwp/api/windows.storage.storagefile) de [WinRT](/uwp/api/) en un objeto de [archivo](https://developer.mozilla.org/docs/Web/API/File) W3C estándar.</span><span class="sxs-lookup"><span data-stu-id="cd389-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-199">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="cd389-200">por</span><span class="sxs-lookup"><span data-stu-id="cd389-200">[in]</span></span>
      
      | <span data-ttu-id="cd389-201">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-201">Type</span></span> | <span data-ttu-id="cd389-202">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-203">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-203">Any</span></span> | <span data-ttu-id="cd389-204">Contiene el archivo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="cd389-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-205">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-205">Return value</span></span>**
      
      <span data-ttu-id="cd389-206">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd389-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-207">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="cd389-208">Excepción</span><span class="sxs-lookup"><span data-stu-id="cd389-208">Exception</span></span> | <span data-ttu-id="cd389-209">Condición</span><span class="sxs-lookup"><span data-stu-id="cd389-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="cd389-210">TypeMismatchError</span></span> | <span data-ttu-id="cd389-211">La referencia del archivo W3C especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="cd389-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="cd389-212">Para las versiones anteriores a Internet Explorer 10, `TYPE_MISMATCH_ERR` se devuelve.</span><span class="sxs-lookup"><span data-stu-id="cd389-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-213">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-213">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-214">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-215">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cd389-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="cd389-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-217">Crea un [MSStream](https://msdn.microsoft.com/library/hh772328) a partir de [InputStream](https://msdn.microsoft.com/library/hh772327).</span><span class="sxs-lookup"><span data-stu-id="cd389-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-218">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="cd389-219">por</span><span class="sxs-lookup"><span data-stu-id="cd389-219">[in]</span></span>
      
      | <span data-ttu-id="cd389-220">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-220">Type</span></span> | <span data-ttu-id="cd389-221">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-222">DOMString</span></span> | <span data-ttu-id="cd389-223">Tipo de contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="cd389-223">Content type of the data.</span></span>  <span data-ttu-id="cd389-224">Esta cadena debe estar en el formato especificado en el símbolo de tipo multimedia definido en la sección 3,7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="cd389-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="cd389-225">\ ([Ver tipos MIME] (como https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) ,, `text/plain` `text/html` `image/jpeg` , `image/png` , `audio/mpeg` , `audio/ogg` , `audio/*` ,, etc `video/mp4` . \).</span><span class="sxs-lookup"><span data-stu-id="cd389-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="cd389-226">por</span><span class="sxs-lookup"><span data-stu-id="cd389-226">[in]</span></span>
      
      | <span data-ttu-id="cd389-227">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-227">Type</span></span> | <span data-ttu-id="cd389-228">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-229">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-229">Any</span></span> | <span data-ttu-id="cd389-230">El [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) se almacena en `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="cd389-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-231">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-231">Return value</span></span>**
      
      <span data-ttu-id="cd389-232">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-233">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-233">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-234">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-235">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-235">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-236">Este método toma un tipo de contenido y la `IInputStream` referencia.</span><span class="sxs-lookup"><span data-stu-id="cd389-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="cd389-237">El método comprueba entonces que la referencia de la secuencia que se ha pasado es una instancia de tipo `IInputStream` y, si no es así, se inicia `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="cd389-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="cd389-238">Si no se produce ningún error, `createStreamFromInputStream` crea un `MSStream` \ (a partir de las entradas \).</span><span class="sxs-lookup"><span data-stu-id="cd389-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-239">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-239">Example</span></span>**  
      
      <span data-ttu-id="cd389-240">`IInputStream`Se puede usar una para crear un `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="cd389-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="cd389-241">Al igual que los `MSStreams` objetos de un solo uso, todas las direcciones URL creadas por `URL.createObjectURL` se revocan la primera vez que el elemento de imagen las resuelve.</span><span class="sxs-lookup"><span data-stu-id="cd389-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="cd389-242">Además, se producirá un error en las solicitudes de una segunda dirección URL en este objeto después de que se haya usado la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cd389-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
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

### <span data-ttu-id="cd389-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="cd389-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-244">Programa una devolución de llamada que se ejecutará en un momento posterior según la prioridad dada.</span><span class="sxs-lookup"><span data-stu-id="cd389-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-245">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="cd389-246">por</span><span class="sxs-lookup"><span data-stu-id="cd389-246">[in]</span></span>
      
      | <span data-ttu-id="cd389-247">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-247">Type</span></span> | <span data-ttu-id="cd389-248">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-249">Función</span><span class="sxs-lookup"><span data-stu-id="cd389-249">Function</span></span> | <span data-ttu-id="cd389-250">Función de devolución de llamada que se ejecuta de forma asincrónica, distribuida a la prioridad de prioridad dada.</span><span class="sxs-lookup"><span data-stu-id="cd389-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="cd389-251">por</span><span class="sxs-lookup"><span data-stu-id="cd389-251">[in]</span></span>
      
      | <span data-ttu-id="cd389-252">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-252">Type</span></span> | <span data-ttu-id="cd389-253">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-254">DOMString</span></span> | <span data-ttu-id="cd389-255">El valor de prioridad contextual en el que se ejecuta la devolución de llamada de asynchronousCallback.</span><span class="sxs-lookup"><span data-stu-id="cd389-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="cd389-256">Consulta [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="cd389-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="cd389-257">por</span><span class="sxs-lookup"><span data-stu-id="cd389-257">[in]</span></span>
      
      | <span data-ttu-id="cd389-258">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-258">Type</span></span> | <span data-ttu-id="cd389-259">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="cd389-260">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-260">Any</span></span> | <span data-ttu-id="cd389-261">Una serie opcional de argumentos que se pasan a la función de devolución de llamada synchronousCallback \ (como parámetros 1 y así sucesivamente \).</span><span class="sxs-lookup"><span data-stu-id="cd389-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-262">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-262">Return value</span></span>**  
      
      <span data-ttu-id="cd389-263">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="cd389-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-264">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-264">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-265">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-266">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-266">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-267">La `asynchronousCallback` función de devolución de llamada proporcionada se ejecuta de forma asincrónica más adelante.</span><span class="sxs-lookup"><span data-stu-id="cd389-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="cd389-268">se enviarán según la prioridad proporcionada.</span><span class="sxs-lookup"><span data-stu-id="cd389-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="cd389-269">La prioridad normal es equivalente al método [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) existente.</span><span class="sxs-lookup"><span data-stu-id="cd389-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="cd389-270">Cuando se ejecuta la devolución de llamada, la prioridad contextual actual se establece en el valor de parámetro de prioridad proporcionado para la duración de la ejecución de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="cd389-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="cd389-271">El `asynchronousCallback` parámetro callback puede ser cualquier función.</span><span class="sxs-lookup"><span data-stu-id="cd389-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="cd389-272">Si se proporcionan argumentos después del `priority` parámetro, todos se transferirán a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="cd389-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="cd389-273">A diferencia `execAtPriority` de, cualquier objeto devuelto por la `asynchronousCallback` función callback se omite \ (y no se devuelve a través de `execAsyncAtPriority` \).</span><span class="sxs-lookup"><span data-stu-id="cd389-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-274">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cd389-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="cd389-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-276">Ejecuta la función de devolución de llamada especificada en la prioridad contextual indicada.</span><span class="sxs-lookup"><span data-stu-id="cd389-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-277">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="cd389-278">por</span><span class="sxs-lookup"><span data-stu-id="cd389-278">[in]</span></span>  
      
      | <span data-ttu-id="cd389-279">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-279">Type</span></span> | <span data-ttu-id="cd389-280">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-281">Función</span><span class="sxs-lookup"><span data-stu-id="cd389-281">Function</span></span> | <span data-ttu-id="cd389-282">Función de devolución de llamada que se ejecuta sincrónicamente a la prioridad de prioridad dada.</span><span class="sxs-lookup"><span data-stu-id="cd389-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="cd389-283">por</span><span class="sxs-lookup"><span data-stu-id="cd389-283">[in]</span></span>  
      
      | <span data-ttu-id="cd389-284">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-284">Type</span></span> | <span data-ttu-id="cd389-285">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-286">DOMString</span></span> | <span data-ttu-id="cd389-287">El valor de prioridad especificado al que se establecerá el valor de prioridad contextual actual al ejecutar la `synchronousCallback` función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="cd389-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="cd389-288">Consulta [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="cd389-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="cd389-289">por</span><span class="sxs-lookup"><span data-stu-id="cd389-289">[in]</span></span>  
      
      | <span data-ttu-id="cd389-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-290">Type</span></span> | <span data-ttu-id="cd389-291">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-292">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-292">Any</span></span> | <span data-ttu-id="cd389-293">Una serie opcional de argumentos que se pasan a la `synchronousCallback` función de devolución de llamada \ (como parámetros 1 y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="cd389-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-294">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-294">Return value</span></span>**  
      
      | <span data-ttu-id="cd389-295">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-295">Type</span></span> | <span data-ttu-id="cd389-296">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-297">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-297">Any</span></span> | <span data-ttu-id="cd389-298">Devuelve el valor devuelto de la `synchronousCallback` devolución de llamada \ (según corresponda \).</span><span class="sxs-lookup"><span data-stu-id="cd389-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-299">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-299">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-300">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-301">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-301">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-302">El `synchronousCallback` método de devolución de llamada proporcionado se ejecuta de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="cd389-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="cd389-303">La prioridad actual contextual se cambia al valor de prioridad proporcionado (dado por el argumento Priority) para la duración de la función de devolución de llamada proporcionada.</span><span class="sxs-lookup"><span data-stu-id="cd389-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="cd389-304">Una vez que la función de devolución de llamada termine de ejecutarse, la prioridad se devuelve al valor anterior antes de la `execAtPriority` llamada.</span><span class="sxs-lookup"><span data-stu-id="cd389-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="cd389-305">El valor devuelto de `execAtPriority` es el valor devuelto del método de devolución de llamada \ (según se indica \).</span><span class="sxs-lookup"><span data-stu-id="cd389-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="cd389-306">El `synchronousCallback` parámetro callback puede ser cualquier función.</span><span class="sxs-lookup"><span data-stu-id="cd389-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="cd389-307">Si se proporciona cualquier argumento después del parámetro Priority, se pasarán al método de devolución de llamada proporcionado.</span><span class="sxs-lookup"><span data-stu-id="cd389-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="cd389-308">Si el parámetro callback devuelve un valor, este valor también se convierte en el valor devuelto `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="cd389-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-309">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-309">Example</span></span>**  
      
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

### <span data-ttu-id="cd389-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="cd389-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-311">Devuelve la prioridad contextual actual.</span><span class="sxs-lookup"><span data-stu-id="cd389-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-312">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-312">Parameters</span></span>**  
      
      <span data-ttu-id="cd389-313">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-314">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-314">Return value</span></span>**  
      
      | <span data-ttu-id="cd389-315">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-315">Type</span></span> | <span data-ttu-id="cd389-316">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-317">DOMString</span></span> | <span data-ttu-id="cd389-318">El valor devuelto es una de las cadenas `MSApp.HIGH` , `MSApp.NORMAL` , o `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="cd389-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-319">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-319">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-320">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-321">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-321">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-322">Este método devuelve la prioridad contextual actual \ (vea [constantes MSApp](#msapp-constants)\), que se puede cambiar mediante `execAtPriority` y `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="cd389-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-323">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-323">Example</span></span>**  
      
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

### <span data-ttu-id="cd389-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="cd389-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="cd389-325">API sincrónica que ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="cd389-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="cd389-326">Para Windows 10, consulte `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="cd389-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="cd389-327">Para las aplicaciones de Windows 8 y 8,1, consulte la entrada de MSDN para [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="cd389-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="cd389-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="cd389-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-329">Devuelve el contenido de origen que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="cd389-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-330">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="cd389-331">por</span><span class="sxs-lookup"><span data-stu-id="cd389-331">[in]</span></span>  
      
      | <span data-ttu-id="cd389-332">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-332">Type</span></span> | <span data-ttu-id="cd389-333">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-334">Documento</span><span class="sxs-lookup"><span data-stu-id="cd389-334">Document</span></span> | <span data-ttu-id="cd389-335">Documento HTML que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="cd389-335">The HTML document to be printed.</span></span>  <span data-ttu-id="cd389-336">Puede ser el documento raíz, el documento en un iframe, un fragmento de documento o un documento SVG.</span><span class="sxs-lookup"><span data-stu-id="cd389-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="cd389-337">Tenga en cuenta que htmlDoc debe ser un documento, no un elemento.</span><span class="sxs-lookup"><span data-stu-id="cd389-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-338">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-338">Return value</span></span>**
      
      <span data-ttu-id="cd389-339">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-340">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-340">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-341">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-342">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-342">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-343">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-344">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd389-344">Example 1</span></span>**  
      
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
      **<span data-ttu-id="cd389-345">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="cd389-345">Example 2</span></span>**  
      
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

### <span data-ttu-id="cd389-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="cd389-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-347">Compatibilidad con varias ventanas.</span><span class="sxs-lookup"><span data-stu-id="cd389-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="cd389-348">En las aplicaciones para UWP con JavaScript para Windows 8.1, se admiten varias ventanas con las API de MSApp DOM que ahora son depricated.</span><span class="sxs-lookup"><span data-stu-id="cd389-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="cd389-349">Para Windows 10, use `window.open` , `window` y el nuevo `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="cd389-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="cd389-350">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-350">Description</span></span> |<span data-ttu-id="cd389-351">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cd389-351">Windows 10</span></span> | <span data-ttu-id="cd389-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cd389-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="cd389-353">Crear nueva ventana</span><span class="sxs-lookup"><span data-stu-id="cd389-353">Create new window</span></span> | [<span data-ttu-id="cd389-354">Window. Open</span><span class="sxs-lookup"><span data-stu-id="cd389-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="cd389-355">MSApp.createNewView</span><span class="sxs-lookup"><span data-stu-id="cd389-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="cd389-356">Nuevo objeto de ventana</span><span class="sxs-lookup"><span data-stu-id="cd389-356">New window object</span></span> | [<span data-ttu-id="cd389-357">ventana</span><span class="sxs-lookup"><span data-stu-id="cd389-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="cd389-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="cd389-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-359">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="cd389-360">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-360">Type</span></span> | <span data-ttu-id="cd389-361">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-362">DOMString</span></span> | <span data-ttu-id="cd389-363">Un objeto que representa una ventana que contiene un documento DOM.</span><span class="sxs-lookup"><span data-stu-id="cd389-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-364">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="cd389-365">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-365">Type</span></span> | <span data-ttu-id="cd389-366">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-367">Número</span><span class="sxs-lookup"><span data-stu-id="cd389-367">Number</span></span> | <span data-ttu-id="cd389-368">Puede usarse con las diversas API [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .</span><span class="sxs-lookup"><span data-stu-id="cd389-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-369">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-369">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-370">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-371">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-371">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-372">Usa [window. Open](https://developer.mozilla.org/docs/Web/API/Window/open) y [Window](https://developer.mozilla.org/docs/Web/API/Window) para crear nuevas ventanas, pero después, para interactuar con las API de WinRT, agrega la `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="cd389-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="cd389-373">Toma un `window` objeto como parámetro y devuelve un `viewId` número que se puede usar con las distintas API de [Windows. UI. ViewManagement. ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) .</span><span class="sxs-lookup"><span data-stu-id="cd389-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="cd389-374">Retrasar la visibilidad</span><span class="sxs-lookup"><span data-stu-id="cd389-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="cd389-375">Normalmente, las vistas de WinRT se inician de forma oculta y el desarrollador final usa algo como `TryShowAsStandaloneAsync` para mostrar la vista una vez que se ha preparado por completo.</span><span class="sxs-lookup"><span data-stu-id="cd389-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="cd389-376">En el mundo web, `window.open` muestra inmediatamente una ventana y el usuario final puede ver que el contenido se carga y se representa.</span><span class="sxs-lookup"><span data-stu-id="cd389-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="cd389-377">Para que la nueva Windows funcione como vistas en WinRT y no se muestre inmediatamente, hemos añadido una `window.open` opción.</span><span class="sxs-lookup"><span data-stu-id="cd389-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="cd389-378">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cd389-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="cd389-379">Diferencias entre ventanas principales</span><span class="sxs-lookup"><span data-stu-id="cd389-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="cd389-380">La ventana principal que inicialmente abre el sistema operativo funciona de forma diferente a la de las ventanas secundarias que abre:</span><span class="sxs-lookup"><span data-stu-id="cd389-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="cd389-381">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-381">Description</span></span> | <span data-ttu-id="cd389-382">Principal</span><span class="sxs-lookup"><span data-stu-id="cd389-382">Primary</span></span> | <span data-ttu-id="cd389-383">Secundario</span><span class="sxs-lookup"><span data-stu-id="cd389-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="cd389-384">Window. Open</span><span class="sxs-lookup"><span data-stu-id="cd389-384">window.open</span></span> | <span data-ttu-id="cd389-385">Se permite</span><span class="sxs-lookup"><span data-stu-id="cd389-385">Allowed</span></span> | <span data-ttu-id="cd389-386">No permitido</span><span class="sxs-lookup"><span data-stu-id="cd389-386">Disallowed</span></span> |  
          | <span data-ttu-id="cd389-387">Window. Close</span><span class="sxs-lookup"><span data-stu-id="cd389-387">window.close</span></span> | <span data-ttu-id="cd389-388">Cerrar aplicación</span><span class="sxs-lookup"><span data-stu-id="cd389-388">Close app</span></span> | <span data-ttu-id="cd389-389">Cerrar ventana</span><span class="sxs-lookup"><span data-stu-id="cd389-389">Close window</span></span> |  
          | <span data-ttu-id="cd389-390">Restricciones de navegación</span><span class="sxs-lookup"><span data-stu-id="cd389-390">Navigation restrictions</span></span> | <span data-ttu-id="cd389-391">ACUR solo</span><span class="sxs-lookup"><span data-stu-id="cd389-391">ACUR only</span></span> | <span data-ttu-id="cd389-392">Sin restricciones</span><span class="sxs-lookup"><span data-stu-id="cd389-392">No restrictions</span></span> |  
          
          <span data-ttu-id="cd389-393">La restricción para no permitir la apertura de ventanas secundarias podría cambiar en el futuro en función de los [comentarios](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span><span class="sxs-lookup"><span data-stu-id="cd389-393">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>  
      
      *   <span data-ttu-id="cd389-394">Restricciones de comunicación del mismo origen</span><span class="sxs-lookup"><span data-stu-id="cd389-394">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="cd389-395">Hay un difícil problema técnico que evita que se admitan las llamadas a secuencias de comandos sincrónicas, del mismo origen y de ventana cruzada.</span><span class="sxs-lookup"><span data-stu-id="cd389-395">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="cd389-396">Cuando se abre una ventana que tiene el mismo origen, se permite que la secuencia de comandos de una ventana llame directamente a las funciones de la otra ventana y se producirá un error en algunas de estas llamadas.</span><span class="sxs-lookup"><span data-stu-id="cd389-396">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="cd389-397">las llamadas funcionan perfectamente y es la manera recomendada de hacer cosas si es posible.</span><span class="sxs-lookup"><span data-stu-id="cd389-397">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="cd389-398">El trabajo para mejorar este problema está en curso.</span><span class="sxs-lookup"><span data-stu-id="cd389-398">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-399">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-399">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <span data-ttu-id="cd389-400">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="cd389-400">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-401">Devuelve un valor de tipo Boolean que indica si hay trabajo pendiente en el nivel de prioridad dado o superior.</span><span class="sxs-lookup"><span data-stu-id="cd389-401">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-402">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-402">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="cd389-403">por</span><span class="sxs-lookup"><span data-stu-id="cd389-403">[in]</span></span>
      
      | <span data-ttu-id="cd389-404">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-404">Type</span></span> | <span data-ttu-id="cd389-405">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-405">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-406">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-406">DOMString</span></span> | <span data-ttu-id="cd389-407">Un valor de prioridad \ (vea [constantes MSApp](#msapp-constants)\) especificando el nivel de prioridad o superior para consultar cualquier trabajo pendiente en cola.</span><span class="sxs-lookup"><span data-stu-id="cd389-407">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-408">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-408">Return value</span></span>**  
      
      | <span data-ttu-id="cd389-409">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-409">Type</span></span> | <span data-ttu-id="cd389-410">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-410">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-411">Booleano</span><span class="sxs-lookup"><span data-stu-id="cd389-411">Boolean</span></span> | <span data-ttu-id="cd389-412">Devuelve `true` si hay algún trabajo en cola en el nivel de prioridad especificado o superior, de `false` lo contrario.</span><span class="sxs-lookup"><span data-stu-id="cd389-412">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-413">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-413">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-414">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-414">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-415">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-415">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-416">El `isTaskScheduledAtPriorityOrHigher` método proporciona un medio para que el código de JavaScript determine si hay trabajo pendiente en los distintos niveles de prioridad \ (o superior \) con la intención de que el código JavaScript de la llamada pueda decidir dar lugar a un trabajo de prioridad más alto.</span><span class="sxs-lookup"><span data-stu-id="cd389-416">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-417">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-417">Example</span></span>**  
      
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

### <span data-ttu-id="cd389-418">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="cd389-418">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-419">Se usa para evitar una actualización de la ruta de inicio (volver a cargar la página) antes de cada evento Activate \ (como hacer clic en una notificación o en un mosaico anclado \).</span><span class="sxs-lookup"><span data-stu-id="cd389-419">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-420">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-420">Parameters</span></span>**  
      
      | <span data-ttu-id="cd389-421">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-421">Type</span></span> | <span data-ttu-id="cd389-422">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-422">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-423">Booleano</span><span class="sxs-lookup"><span data-stu-id="cd389-423">Boolean</span></span> | <span data-ttu-id="cd389-424">Use `MSApp.pageHandlesAllApplicationActivations(true)` esta para omitir siempre la actualización de la ruta de inicio (volver a cargar la página) y, en su lugar, saltar directamente al desencadenar el `WebUIApplication` evento activado.</span><span class="sxs-lookup"><span data-stu-id="cd389-424">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="cd389-425">Requiere que todas las páginas manejen los eventos de activación por separado.</span><span class="sxs-lookup"><span data-stu-id="cd389-425">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="cd389-426">Al definir este método como `true` , al hacer clic en un evento activado \ (como una notificación \), no se activará la recarga, que es esencial para las aplicaciones de una sola página que deseen evitar la recarga de la página.</span><span class="sxs-lookup"><span data-stu-id="cd389-426">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-427">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-427">Return value</span></span>**
      
      <span data-ttu-id="cd389-428">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-428">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-429">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-429">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-430">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-430">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-431">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-431">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-432">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-432">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-433">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-433">Example</span></span>**  
      
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

### <span data-ttu-id="cd389-434">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="cd389-434">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-435">Controla si una aplicación suprime posibles mensajes de autenticación durante la descarga de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd389-435">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-436">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-436">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="cd389-437">por</span><span class="sxs-lookup"><span data-stu-id="cd389-437">[in]</span></span>
      
      | <span data-ttu-id="cd389-438">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-438">Type</span></span> | <span data-ttu-id="cd389-439">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-439">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-440">Booleano</span><span class="sxs-lookup"><span data-stu-id="cd389-440">Boolean</span></span> | <span data-ttu-id="cd389-441">El valor true suprime las solicitudes de autenticación potenciales.</span><span class="sxs-lookup"><span data-stu-id="cd389-441">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="cd389-442">El valor false no suprime ninguna solicitud de autenticación potencial del usuario.</span><span class="sxs-lookup"><span data-stu-id="cd389-442">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-443">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-443">Return value</span></span>**  
      
      <span data-ttu-id="cd389-444">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-444">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-445">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-445">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-446">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-446">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-447">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-447">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-448">El `suppressSubdownloadCredentialPrompts` método controla si una aplicación suprime las solicitudes de autenticación potenciales durante la descarga de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd389-448">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="cd389-449">El comportamiento predeterminado es no suprimir las solicitudes de credenciales.</span><span class="sxs-lookup"><span data-stu-id="cd389-449">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="cd389-450">está pensado para que lo usen las aplicaciones que pueden cargar un número excesivo de recursos que requieren autenticación, como una aplicación de correo \ (que puede contener un boletín con un número de imágenes en el que cada imagen requiera autenticación \).</span><span class="sxs-lookup"><span data-stu-id="cd389-450">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="cd389-451">Al suprimir las solicitudes de credenciales, los cuadros de diálogo para autenticar a los servidores no se mostrarán al acceder a los recursos que requieren autenticación, y el recurso no se descargará.</span><span class="sxs-lookup"><span data-stu-id="cd389-451">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="cd389-452">Tenga en cuenta que no `suppressSubdownloadCredentialPrompts` afecta otros indicadores posibles, como la autenticación de proxy o los cuadros de diálogo de solicitud de certificación del cliente, ni afecta a XHR.</span><span class="sxs-lookup"><span data-stu-id="cd389-452">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="cd389-453">Tenga en cuenta que `suppressSubdownloadCredentialPrompts` afecta a todo el contenido de la aplicación, incluido el contenido hospedado en el `webview` elemento.</span><span class="sxs-lookup"><span data-stu-id="cd389-453">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="cd389-454">Las decisiones de solicitud de credenciales se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="cd389-454">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="cd389-455">Por lo tanto, aunque la supresión de las solicitudes de credenciales surtirá efecto inmediatamente, es posible que sea necesario volver a cargar el documento para permitir las solicitudes de credenciales después de suprimirlas.</span><span class="sxs-lookup"><span data-stu-id="cd389-455">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-456">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-456">Example</span></span>**  
      
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

### <span data-ttu-id="cd389-457">terminateApp</span><span class="sxs-lookup"><span data-stu-id="cd389-457">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-458">Finaliza la aplicación actual y genera un informe de error.</span><span class="sxs-lookup"><span data-stu-id="cd389-458">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-459">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-459">Parameters</span></span>**  
      
      `error` <span data-ttu-id="cd389-460">por</span><span class="sxs-lookup"><span data-stu-id="cd389-460">[in]</span></span>
      
      | <span data-ttu-id="cd389-461">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-461">Type</span></span> | <span data-ttu-id="cd389-462">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-462">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-463">Error</span><span class="sxs-lookup"><span data-stu-id="cd389-463">Error</span></span> | <span data-ttu-id="cd389-464">Un `Error` objeto que se puede usar para describir el error que ha desencadenado la finalización.</span><span class="sxs-lookup"><span data-stu-id="cd389-464">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="cd389-465">El `Error` objeto debe contener las propiedades Number, Description y stack; no se generará un informe de errores si el objeto no contiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd389-465">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-466">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-466">Return value</span></span>**
      
      <span data-ttu-id="cd389-467">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-467">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-468">Excepciones</span><span class="sxs-lookup"><span data-stu-id="cd389-468">Exceptions</span></span>**  
      
      <span data-ttu-id="cd389-469">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-469">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-470">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd389-470">Remarks</span></span>**  
      
      <span data-ttu-id="cd389-471">Si el problema notificado por `terminateApp` se convierte en uno de los cinco principales problemas de la aplicación, se mostrará en la página calidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cd389-471">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-472">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-472">Example</span></span>**  
      
      <span data-ttu-id="cd389-473">Este ejemplo llama `terminateApp` cuando se encuentra una excepción.</span><span class="sxs-lookup"><span data-stu-id="cd389-473">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="cd389-474">Usa el `Error` objeto proporcionado cuando se detecta una excepción.</span><span class="sxs-lookup"><span data-stu-id="cd389-474">It uses the `Error` object provided when you catch an exception.</span></span>  
      
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

### <span data-ttu-id="cd389-475">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="cd389-475">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-476">Valores de prioridad permitidos asociados con `execAsyncAtPriority` ,, `execAtPriority` `getCurrentPriority` y `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="cd389-476">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="cd389-477">Actual</span><span class="sxs-lookup"><span data-stu-id="cd389-477">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="cd389-478">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-478">Type</span></span> | <span data-ttu-id="cd389-479">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-479">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-480">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-480">DOMString</span></span> | <span data-ttu-id="cd389-481">Cuando `current` se usa con el método adecuado \ (vea también la sección \), el método usará la prioridad contextual actual al ejecutar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="cd389-481">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="cd389-482">Alto</span><span class="sxs-lookup"><span data-stu-id="cd389-482">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="cd389-483">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-483">Type</span></span> | <span data-ttu-id="cd389-484">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-484">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-485">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-485">DOMString</span></span> | <span data-ttu-id="cd389-486">Cuando `high` se usa con el método adecuado \ (vea también la sección \), el método usará una prioridad mayor que la normal al ejecutar la operación solicitada y se enviará la operación antes de que se realice cualquier trabajo de prioridad normal existente.</span><span class="sxs-lookup"><span data-stu-id="cd389-486">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="cd389-487">Inactivo</span><span class="sxs-lookup"><span data-stu-id="cd389-487">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="cd389-488">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-488">Type</span></span> | <span data-ttu-id="cd389-489">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-489">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-490">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-490">DOMString</span></span> | <span data-ttu-id="cd389-491">Cuando `ideal` se usa con el método adecuado \ (vea también la sección \), el método usará la prioridad inferior a la normal al ejecutar la operación solicitada y se enviará la operación después de cualquier trabajo de prioridad normal existente.</span><span class="sxs-lookup"><span data-stu-id="cd389-491">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="cd389-492">Normal</span><span class="sxs-lookup"><span data-stu-id="cd389-492">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="cd389-493">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-493">Type</span></span> | <span data-ttu-id="cd389-494">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-494">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-495">DOMString</span><span class="sxs-lookup"><span data-stu-id="cd389-495">DOMString</span></span> | <span data-ttu-id="cd389-496">Cuando `normal` se usa con el método adecuado (vea también la sección), el método usará la prioridad normal existente al ejecutar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="cd389-496">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-497">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd389-497">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-498">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd389-498">Requirements</span></span>**  
      
      | <span data-ttu-id="cd389-499">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-499">Type</span></span> | <span data-ttu-id="cd389-500">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-500">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-501">IDL</span><span class="sxs-lookup"><span data-stu-id="cd389-501">IDL</span></span> | <span data-ttu-id="cd389-502">Mshtml. idl</span><span class="sxs-lookup"><span data-stu-id="cd389-502">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="cd389-503">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="cd389-503">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <span data-ttu-id="cd389-504">start</span><span class="sxs-lookup"><span data-stu-id="cd389-504">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="cd389-505">Inicia el `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cd389-505">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="cd389-506">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd389-506">Parameters</span></span>**  
      
      <span data-ttu-id="cd389-507">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-507">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="cd389-508">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd389-508">Return value</span></span>**
      
      <span data-ttu-id="cd389-509">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cd389-509">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="cd389-510">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd389-510">Properties</span></span>**  
      
      `error` <span data-ttu-id="cd389-511">propiedad</span><span class="sxs-lookup"><span data-stu-id="cd389-511">property</span></span>  
      
      | <span data-ttu-id="cd389-512">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-512">Type</span></span> | <span data-ttu-id="cd389-513">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-513">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-514">DOMError</span><span class="sxs-lookup"><span data-stu-id="cd389-514">DOMError</span></span> | <span data-ttu-id="cd389-515">Representa un error en `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cd389-515">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="cd389-516">propiedad</span><span class="sxs-lookup"><span data-stu-id="cd389-516">property</span></span>  
      
      | <span data-ttu-id="cd389-517">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-517">Type</span></span> | <span data-ttu-id="cd389-518">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-518">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-519">EventHandler</span><span class="sxs-lookup"><span data-stu-id="cd389-519">EventHandler</span></span> | <span data-ttu-id="cd389-520">Propiedad para establecer un controlador de eventos finalizado `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cd389-520">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="cd389-521">propiedad</span><span class="sxs-lookup"><span data-stu-id="cd389-521">property</span></span>  
      
      | <span data-ttu-id="cd389-522">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-522">Type</span></span> | <span data-ttu-id="cd389-523">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-523">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-524">EventHandler</span><span class="sxs-lookup"><span data-stu-id="cd389-524">EventHandler</span></span> | <span data-ttu-id="cd389-525">Propiedad para establecer un controlador de eventos cuando se produce un error `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cd389-525">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="cd389-526">propiedad</span><span class="sxs-lookup"><span data-stu-id="cd389-526">property</span></span>  
      
      | <span data-ttu-id="cd389-527">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-527">Type</span></span> | <span data-ttu-id="cd389-528">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-528">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-529">Número</span><span class="sxs-lookup"><span data-stu-id="cd389-529">Number</span></span> | <span data-ttu-id="cd389-530">Representa el estado de la operación asincrónica dentro de la aplicación de Windows con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cd389-530">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="cd389-531">Entre los valores se incluyen: `Started[0]` , `Completed[1]` , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="cd389-531">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="cd389-532">propiedad</span><span class="sxs-lookup"><span data-stu-id="cd389-532">property</span></span>  
      
      | <span data-ttu-id="cd389-533">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd389-533">Type</span></span> | <span data-ttu-id="cd389-534">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd389-534">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="cd389-535">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="cd389-535">Any</span></span> |<span data-ttu-id="cd389-536">Representa el resultado de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="cd389-536">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

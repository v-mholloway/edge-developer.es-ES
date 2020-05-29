---
title: Referencia de la API de MSApp
description: Proporciona funciones auxiliares que permiten crear objetos BLOB y MSStream. Los objetos y miembros de MSApp son compatibles con las aplicaciones de Windows que usan JavaScript.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, carga de archivos, blog, MSStream, aplicaciones de Windows 10, UWP, Edge
ms.openlocfilehash: 0ed8cefa918bd44f3b2c4e8312d2c1d3b4ace8fc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574921"
---
# <span data-ttu-id="94045-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="94045-105">MSApp</span></span>

<span data-ttu-id="94045-106">El objeto MSApp y sus miembros solo se admiten en aplicaciones de Windows que usen JavaScript (incluyendo PWAs de acceso a las características de la API de Windows).</span><span class="sxs-lookup"><span data-stu-id="94045-106">The MSApp object and its members are supported only for Windows apps using JavaScript (including PWAs accessing Windows API features).</span></span> <span data-ttu-id="94045-107">El objeto MSApp solo existe en el contexto local de un documento HTML en una aplicación de Windows que se carga mediante el esquema de URI MS-appx; de lo contrario, el objeto no existe (y, por lo tanto, ninguno de sus métodos y propiedades está disponible).</span><span class="sxs-lookup"><span data-stu-id="94045-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>

<span data-ttu-id="94045-108">Proporciona funciones auxiliares que permiten crear objetos [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) y [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="94045-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**<span data-ttu-id="94045-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="94045-109">Methods</span></span>**](#msapp-methods) | <span data-ttu-id="94045-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority, getHtmlPrintDocumentSource](#getcurrentpriority),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId, isTaskScheduledAtPriorityOrHigher](#getviewid) [, pageHandlesAllApplicationActivations](#istaskscheduledatpriorityorhigher) [, suppressSubdownloadCredentialPrompts, terminateApp.](#pagehandlesallapplicationactivations) [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource) [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts) [terminateApp](#terminateapp)</span><span class="sxs-lookup"><span data-stu-id="94045-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span> |

| | |
| :--- | :--- |
| [**<span data-ttu-id="94045-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="94045-111">Constants</span></span>**](#msapp-constants) | <span data-ttu-id="94045-112">[actual](#current), [alta](#high), [inactiva](#idle), [normal](#normal).</span><span class="sxs-lookup"><span data-stu-id="94045-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>|

| | |
| :--- | :--- |
| [<span data-ttu-id="94045-113">Interfaz **MSAppAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="94045-113">**MSAppAsyncOperation** interface</span></span>](#msappasyncoperation) | [<span data-ttu-id="94045-114">start</span><span class="sxs-lookup"><span data-stu-id="94045-114">start</span></span>](#start) |

## <span data-ttu-id="94045-115">Métodos de MSApp</span><span class="sxs-lookup"><span data-stu-id="94045-115">MSApp Methods</span></span>

### <span data-ttu-id="94045-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="94045-116">clearTemporaryWebDataAsync</span></span> 
<span data-ttu-id="94045-117">Borra los datos de caché y indexedDB de la aplicación o [WebView](../../webview.md).</span><span class="sxs-lookup"><span data-stu-id="94045-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### <span data-ttu-id="94045-118">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-118">Parameters</span></span>
<span data-ttu-id="94045-119">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="94045-119">This method has no parameters.</span></span>

#### <span data-ttu-id="94045-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-120">Return value</span></span>
<span data-ttu-id="94045-121">Escrita[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="94045-121">Type: [`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span></span>

<span data-ttu-id="94045-122">Representa una acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="94045-122">Represents an asynchronous action.</span></span>

### <span data-ttu-id="94045-123">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="94045-123">createBlobFromRandomAccessStream</span></span>
<span data-ttu-id="94045-124">Crea un objeto [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) a partir de un [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) objeto.</span><span class="sxs-lookup"><span data-stu-id="94045-124">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span> <span data-ttu-id="94045-125">Este método se debe usar cuando se trata de `IRandomAccessStream` objetos en aplicaciones para crear un objeto basado en el consorcio desde la secuencia.</span><span class="sxs-lookup"><span data-stu-id="94045-125">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span> <span data-ttu-id="94045-126">Una vez creado el BLOB, se puede usar con el [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), las [API de la dirección URL](https://developer.mozilla.org/docs/Web/API/URL)y [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="94045-126">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span> 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### <span data-ttu-id="94045-127">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-127">Parameters</span></span>

`type` <span data-ttu-id="94045-128">por</span><span class="sxs-lookup"><span data-stu-id="94045-128">[in]</span></span>

|<span data-ttu-id="94045-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-129">Type</span></span> | <span data-ttu-id="94045-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-130">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="94045-131">String</span></span> | <span data-ttu-id="94045-132">Tipo de contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="94045-132">Content type of the data.</span></span> <span data-ttu-id="94045-133">Esta cadena debe estar en el formato especificado en el símbolo de tipo multimedia definido en la sección 3,7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="94045-133">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>

`stream` <span data-ttu-id="94045-134">por</span><span class="sxs-lookup"><span data-stu-id="94045-134">[in]</span></span>

|<span data-ttu-id="94045-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-135">Type</span></span> | <span data-ttu-id="94045-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-136">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-137">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-137">Any</span></span> | <span data-ttu-id="94045-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) que se va a almacenar en el BLOB.</span><span class="sxs-lookup"><span data-stu-id="94045-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>

#### <span data-ttu-id="94045-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-139">Return value</span></span>
|<span data-ttu-id="94045-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-140">Type</span></span> | <span data-ttu-id="94045-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-141">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-142">Manchas</span><span class="sxs-lookup"><span data-stu-id="94045-142">Blob</span></span> | <span data-ttu-id="94045-143">Nuevo objeto BLOB que contiene la secuencia.</span><span class="sxs-lookup"><span data-stu-id="94045-143">New blob object that contains the stream.</span></span>

#### <span data-ttu-id="94045-144">Excepciones</span><span class="sxs-lookup"><span data-stu-id="94045-144">Exceptions</span></span>
|<span data-ttu-id="94045-145">Excepción</span><span class="sxs-lookup"><span data-stu-id="94045-145">Exception</span></span> | <span data-ttu-id="94045-146">Condición</span><span class="sxs-lookup"><span data-stu-id="94045-146">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-147">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="94045-147">TypeMismatchError</span></span> | <span data-ttu-id="94045-148">El tipo de nodo es incompatible con el tipo de parámetro esperado.</span><span class="sxs-lookup"><span data-stu-id="94045-148">The node type is incompatible with the expected parameter type.</span></span> <span data-ttu-id="94045-149">En el caso de versiones anteriores a Internet Explorer 10, se devuelve TYPE_MISMATCH_ERR.</span><span class="sxs-lookup"><span data-stu-id="94045-149">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

#### <span data-ttu-id="94045-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-150">Remarks</span></span>
<span data-ttu-id="94045-151">Crea un BLOB a partir de los tipos de Windows Runtime a través del espacio de nombres MSApp en el objeto de ventana.</span><span class="sxs-lookup"><span data-stu-id="94045-151">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span> <span data-ttu-id="94045-152">Este método creará un BLOB que es esencialmente un contenedor de luz sobre el objeto que se [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) le proporciona.</span><span class="sxs-lookup"><span data-stu-id="94045-152">This method will create a blob that is essentially a light wrapper over the [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span> <span data-ttu-id="94045-153">El BLOB es propietario de la duración de esta secuencia y la secuencia se cerrará cuando se destruya el BLOB.</span><span class="sxs-lookup"><span data-stu-id="94045-153">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span> 

#### <span data-ttu-id="94045-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-154">Example</span></span>

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### <span data-ttu-id="94045-155">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="94045-155">createDataPackage</span></span>
<span data-ttu-id="94045-156">Convierte el intervalo especificado del usuario o la aplicación en un fragmento de HTML que se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="94045-156">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### <span data-ttu-id="94045-157">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-157">Parameters</span></span>
`object` <span data-ttu-id="94045-158">por</span><span class="sxs-lookup"><span data-stu-id="94045-158">[in]</span></span>

|<span data-ttu-id="94045-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-159">Type</span></span> | <span data-ttu-id="94045-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-160">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-161">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-161">Any</span></span> | <span data-ttu-id="94045-162">Este rango puede crearse desde un objeto de selección, por ejemplo: `window.selection.getRangeAt(0)` , o manualmente.</span><span class="sxs-lookup"><span data-stu-id="94045-162">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>

#### <span data-ttu-id="94045-163">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-163">Return value</span></span>
|<span data-ttu-id="94045-164">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-164">Type</span></span> | <span data-ttu-id="94045-165">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-165">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-166">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-166">Any</span></span> | <span data-ttu-id="94045-167">Contiene el formato HTML del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="94045-167">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="94045-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-168">Remarks</span></span>
<span data-ttu-id="94045-169">Este método solo admite el [rango Dom (modelo de objetos de documento)](https://developer.mozilla.org/docs/Web/API/Range), no [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="94045-169">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span> <span data-ttu-id="94045-170">El paquete de datos devuelto para el intervalo especificado contiene formato HTML en el formato del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="94045-170">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>

<span data-ttu-id="94045-171">No hay ninguna propiedad disponible para el paquete de datos devuelto.</span><span class="sxs-lookup"><span data-stu-id="94045-171">There are no available properties for the returned data package.</span></span>

### <span data-ttu-id="94045-172">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="94045-172">createDataPackageFromSelection</span></span> 
<span data-ttu-id="94045-173">Convierte la selección del usuario o la aplicación en un fragmento HTML que se puede compartir.</span><span class="sxs-lookup"><span data-stu-id="94045-173">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### <span data-ttu-id="94045-174">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-174">Parameters</span></span>
<span data-ttu-id="94045-175">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="94045-175">This method has no parameters.</span></span>

#### <span data-ttu-id="94045-176">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-176">Return value</span></span>
|<span data-ttu-id="94045-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-177">Type</span></span> | <span data-ttu-id="94045-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-178">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-179">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-179">Any</span></span> | <span data-ttu-id="94045-180">Contiene el formato HTML del rango especificado.</span><span class="sxs-lookup"><span data-stu-id="94045-180">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="94045-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-181">Remarks</span></span>
<span data-ttu-id="94045-182">El paquete de datos devuelto para la selección contiene marcado HTML en formato de Portapapeles.</span><span class="sxs-lookup"><span data-stu-id="94045-182">The returned data package for the selection contains HTML markup in clipboard format.</span></span> <span data-ttu-id="94045-183">Si no hay ninguna selección del usuario en ninguna parte de la interfaz de usuario de la aplicación, `createDataPackageFromSelection` devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="94045-183">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns null.</span></span>

<span data-ttu-id="94045-184">No hay ninguna propiedad disponible para el paquete de datos devuelto.</span><span class="sxs-lookup"><span data-stu-id="94045-184">There are no available properties for the returned data package.</span></span>
 
### <span data-ttu-id="94045-185">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="94045-185">createFileFromStorageFile</span></span> 
<span data-ttu-id="94045-186">Convierte un [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) en un objeto estándar de W3C [`File`](https://developer.mozilla.org/docs/Web/API/File) .</span><span class="sxs-lookup"><span data-stu-id="94045-186">Converts a [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) to a standard W3C [`File`](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### <span data-ttu-id="94045-187">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-187">Parameters</span></span>
`storageFile` <span data-ttu-id="94045-188">por</span><span class="sxs-lookup"><span data-stu-id="94045-188">[in]</span></span>

|<span data-ttu-id="94045-189">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-189">Type</span></span> | <span data-ttu-id="94045-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-190">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-191">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-191">Any</span></span> | <span data-ttu-id="94045-192">Contiene el archivo de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="94045-192">Contains the storage file.</span></span>

#### <span data-ttu-id="94045-193">Excepciones</span><span class="sxs-lookup"><span data-stu-id="94045-193">Exceptions</span></span>
|<span data-ttu-id="94045-194">Excepción</span><span class="sxs-lookup"><span data-stu-id="94045-194">Exception</span></span> | <span data-ttu-id="94045-195">Condición</span><span class="sxs-lookup"><span data-stu-id="94045-195">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-196">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="94045-196">TypeMismatchError</span></span> | <span data-ttu-id="94045-197">La referencia del archivo W3C especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="94045-197">The specified W3C file reference is invalid.</span></span> <span data-ttu-id="94045-198">En el caso de versiones anteriores a Internet Explorer 10, se devuelve TYPE_MISMATCH_ERR.</span><span class="sxs-lookup"><span data-stu-id="94045-198">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

### <span data-ttu-id="94045-199">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="94045-199">createStreamFromInputStream</span></span>  

<span data-ttu-id="94045-200">Crea una [`MSStream`](https://msdn.microsoft.com/library/hh772328) a partir de una [`InputStream`](https://msdn.microsoft.com/library/hh772327) .</span><span class="sxs-lookup"><span data-stu-id="94045-200">Creates an [`MSStream`](https://msdn.microsoft.com/library/hh772328) from an [`InputStream`](https://msdn.microsoft.com/library/hh772327).</span></span>  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### <span data-ttu-id="94045-201">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-201">Parameters</span></span>
`type` <span data-ttu-id="94045-202">por</span><span class="sxs-lookup"><span data-stu-id="94045-202">[in]</span></span>

|<span data-ttu-id="94045-203">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-203">Type</span></span> | <span data-ttu-id="94045-204">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-204">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-205">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-205">DOMString</span></span> | <span data-ttu-id="94045-206">Tipo de contenido de los datos.</span><span class="sxs-lookup"><span data-stu-id="94045-206">Content type of the data.</span></span> <span data-ttu-id="94045-207">Esta cadena debe estar en el formato especificado en el símbolo de tipo multimedia definido en la sección 3,7 de RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="94045-207">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span> <span data-ttu-id="94045-208">([Consulte tipos MIME,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. texto/sin formato, texto/HTML, image/JPEG, image/png, audio/MPEG, audio/OGG, audio/\*, Video/MP4, etc.).</span><span class="sxs-lookup"><span data-stu-id="94045-208">([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) ie. text/plain, text/html, image/jpeg, image/png, audio/mpeg, audio/ogg, audio/\*, video/mp4, etc.).</span></span> 

`inputStream` <span data-ttu-id="94045-209">por</span><span class="sxs-lookup"><span data-stu-id="94045-209">[in]</span></span>

|<span data-ttu-id="94045-210">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-210">Type</span></span> | <span data-ttu-id="94045-211">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-211">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-212">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-212">Any</span></span> | <span data-ttu-id="94045-213">El [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) que se va a almacenar en `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="94045-213">The [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>

#### <span data-ttu-id="94045-214">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-214">Remarks</span></span>
<span data-ttu-id="94045-215">Este método toma un tipo de contenido y la `IInputStream` referencia.</span><span class="sxs-lookup"><span data-stu-id="94045-215">This method takes a content-type, and the `IInputStream` reference.</span></span> <span data-ttu-id="94045-216">El método comprueba entonces que la referencia de la secuencia que se ha pasado es una instancia de tipo `IInputStream` y, si no es así, se inicia `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="94045-216">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span> <span data-ttu-id="94045-217">Si no se produce ningún error, `createStreamFromInputStream` crea una `MSStream` (a partir de sus entradas).</span><span class="sxs-lookup"><span data-stu-id="94045-217">If no error occurs, `createStreamFromInputStream` creates an `MSStream` (from its inputs).</span></span>

#### <span data-ttu-id="94045-218">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-218">Example</span></span>
<span data-ttu-id="94045-219">`IInputStream`Se puede usar una para crear un `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="94045-219">An `IInputStream` can be used to create an `MSStream`.</span></span> <span data-ttu-id="94045-220">Al igual que los `MSStreams` objetos de un solo uso, todas las direcciones URL creadas por `URL.createObjectURL` se revocan la primera vez que el elemento de imagen las resuelve.</span><span class="sxs-lookup"><span data-stu-id="94045-220">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span> <span data-ttu-id="94045-221">Además, se producirá un error en las solicitudes de una segunda dirección URL en este objeto después de que se haya usado la secuencia.</span><span class="sxs-lookup"><span data-stu-id="94045-221">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### <span data-ttu-id="94045-222">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="94045-222">execAsyncAtPriority</span></span> 
<span data-ttu-id="94045-223">Programa una devolución de llamada que se ejecutará en un momento posterior según la prioridad dada.</span><span class="sxs-lookup"><span data-stu-id="94045-223">Schedules a callback to be executed at a later time according to the given priority.</span></span> 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### <span data-ttu-id="94045-224">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-224">Parameters</span></span>
`asynchronousCallback` <span data-ttu-id="94045-225">por</span><span class="sxs-lookup"><span data-stu-id="94045-225">[in]</span></span>

|<span data-ttu-id="94045-226">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-226">Type</span></span> | <span data-ttu-id="94045-227">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-227">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-228">Función</span><span class="sxs-lookup"><span data-stu-id="94045-228">Function</span></span> | <span data-ttu-id="94045-229">Función de devolución de llamada que se ejecuta de forma asincrónica, distribuida a la prioridad de prioridad dada.</span><span class="sxs-lookup"><span data-stu-id="94045-229">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>

`priority` <span data-ttu-id="94045-230">por</span><span class="sxs-lookup"><span data-stu-id="94045-230">[in]</span></span>

|<span data-ttu-id="94045-231">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-231">Type</span></span> | <span data-ttu-id="94045-232">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-232">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-233">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-233">DOMString</span></span> | <span data-ttu-id="94045-234">El valor de prioridad contextual en el que se ejecuta la devolución de llamada de asynchronousCallback.</span><span class="sxs-lookup"><span data-stu-id="94045-234">The contextual priority value at which the asynchronousCallback callback is run.</span></span> <span data-ttu-id="94045-235">Consulta [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="94045-235">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="94045-236">por</span><span class="sxs-lookup"><span data-stu-id="94045-236">[in]</span></span>

|<span data-ttu-id="94045-237">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-237">Type</span></span> | <span data-ttu-id="94045-238">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-238">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-239">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-239">Any</span></span> | <span data-ttu-id="94045-240">Una serie opcional de argumentos que se pasan a la función de devolución de llamada synchronousCallback (como parámetros 1 y on).</span><span class="sxs-lookup"><span data-stu-id="94045-240">An optional series of arguments that are passed to the synchronousCallback callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="94045-241">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-241">Return value</span></span>
<span data-ttu-id="94045-242">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="94045-242">This method does not return a value.</span></span>

#### <span data-ttu-id="94045-243">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-243">Remarks</span></span>
<span data-ttu-id="94045-244">La `asynchronousCallback` función de devolución de llamada proporcionada se ejecuta de forma asincrónica más adelante.</span><span class="sxs-lookup"><span data-stu-id="94045-244">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span> `asynchronousCallback` <span data-ttu-id="94045-245">se enviarán según la prioridad proporcionada.</span><span class="sxs-lookup"><span data-stu-id="94045-245">will be dispatched according to the provided priority.</span></span> <span data-ttu-id="94045-246">La prioridad normal es equivalente al [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) método existente.</span><span class="sxs-lookup"><span data-stu-id="94045-246">Normal priority is equivalent to the existing [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span> <span data-ttu-id="94045-247">Cuando se ejecuta la devolución de llamada, la prioridad contextual actual se establece en el valor de parámetro de prioridad proporcionado para la duración de la ejecución de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="94045-247">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>

<span data-ttu-id="94045-248">El `asynchronousCallback` parámetro callback puede ser cualquier función.</span><span class="sxs-lookup"><span data-stu-id="94045-248">The `asynchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="94045-249">Si se proporcionan argumentos después del `priority` parámetro, todos se transferirán a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="94045-249">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>

<span data-ttu-id="94045-250">A diferencia `execAtPriority` de, cualquier objeto devuelto por la `asynchronousCallback` función callback se omite (y no se devuelve a través de `execAsyncAtPriority` ).</span><span class="sxs-lookup"><span data-stu-id="94045-250">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored (and not returned via `execAsyncAtPriority`).</span></span>

### <span data-ttu-id="94045-251">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="94045-251">execAtPriority</span></span> 
<span data-ttu-id="94045-252">Ejecuta la función de devolución de llamada especificada en la prioridad contextual indicada.</span><span class="sxs-lookup"><span data-stu-id="94045-252">Runs the specified callback function at the given contextual priority.</span></span>

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### <span data-ttu-id="94045-253">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-253">Parameters</span></span>
`synchronousCallback` <span data-ttu-id="94045-254">por</span><span class="sxs-lookup"><span data-stu-id="94045-254">[in]</span></span>

|<span data-ttu-id="94045-255">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-255">Type</span></span> | <span data-ttu-id="94045-256">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-256">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-257">Función</span><span class="sxs-lookup"><span data-stu-id="94045-257">Function</span></span> | <span data-ttu-id="94045-258">Función de devolución de llamada que se ejecuta sincrónicamente a la prioridad de prioridad dada.</span><span class="sxs-lookup"><span data-stu-id="94045-258">The callback function to run synchronously at the given priority contextual priority.</span></span>

`priority` <span data-ttu-id="94045-259">por</span><span class="sxs-lookup"><span data-stu-id="94045-259">[in]</span></span>

|<span data-ttu-id="94045-260">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-260">Type</span></span> | <span data-ttu-id="94045-261">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-261">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-262">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-262">DOMString</span></span> | <span data-ttu-id="94045-263">El valor de prioridad especificado al que se establecerá el valor de prioridad contextual actual al ejecutar la `synchronousCallback` función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="94045-263">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span> <span data-ttu-id="94045-264">Consulta [constantes MSApp](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="94045-264">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="94045-265">por</span><span class="sxs-lookup"><span data-stu-id="94045-265">[in]</span></span>

|<span data-ttu-id="94045-266">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-266">Type</span></span> | <span data-ttu-id="94045-267">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-267">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-268">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-268">Any</span></span> | <span data-ttu-id="94045-269">Una serie opcional de argumentos que se pasan a la `synchronousCallback` función de devolución de llamada (como parámetros 1 y on).</span><span class="sxs-lookup"><span data-stu-id="94045-269">An optional series of arguments that are passed to the `synchronousCallback` callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="94045-270">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-270">Return value</span></span>
|<span data-ttu-id="94045-271">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-271">Type</span></span> | <span data-ttu-id="94045-272">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-272">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-273">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-273">Any</span></span> | <span data-ttu-id="94045-274">Devuelve el valor devuelto de la `synchronousCallback` devolución de llamada (según corresponda).</span><span class="sxs-lookup"><span data-stu-id="94045-274">Returns the return value of the `synchronousCallback` callback (as applicable).</span></span>

#### <span data-ttu-id="94045-275">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-275">Remarks</span></span>
<span data-ttu-id="94045-276">El `synchronousCallback` método de devolución de llamada proporcionado se ejecuta de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="94045-276">The provided `synchronousCallback` callback method is execute synchronously.</span></span> <span data-ttu-id="94045-277">La prioridad actual contextual se cambia al valor de prioridad proporcionado (dado por el argumento Priority) para la duración de la función de devolución de llamada proporcionada.</span><span class="sxs-lookup"><span data-stu-id="94045-277">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span> <span data-ttu-id="94045-278">Una vez que la función de devolución de llamada termine de ejecutarse, la prioridad se devuelve al valor anterior antes de la `execAtPriority` llamada.</span><span class="sxs-lookup"><span data-stu-id="94045-278">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span> <span data-ttu-id="94045-279">El valor devuelto de `execAtPriority` es el valor devuelto del método de devolución de llamada (tal y como se proporciona).</span><span class="sxs-lookup"><span data-stu-id="94045-279">The return value from `execAtPriority` is the return value of the callback method (as provided).</span></span>
 
<span data-ttu-id="94045-280">El `synchronousCallback` parámetro callback puede ser cualquier función.</span><span class="sxs-lookup"><span data-stu-id="94045-280">The `synchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="94045-281">Si se proporciona cualquier argumento después del parámetro Priority, se pasarán al método de devolución de llamada proporcionado.</span><span class="sxs-lookup"><span data-stu-id="94045-281">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span> <span data-ttu-id="94045-282">Si el parámetro callback devuelve un valor, este valor también se convierte en el valor devuelto `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="94045-282">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>

#### <span data-ttu-id="94045-283">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-283">Example</span></span>

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

### <span data-ttu-id="94045-284">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="94045-284">getCurrentPriority</span></span> 
<span data-ttu-id="94045-285">Devuelve la prioridad contextual actual.</span><span class="sxs-lookup"><span data-stu-id="94045-285">Returns the current contextual priority.</span></span>

```javascript
var retval = MSApp.getCurrentPriority();
```

#### <span data-ttu-id="94045-286">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-286">Parameters</span></span>
<span data-ttu-id="94045-287">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="94045-287">None.</span></span> 

#### <span data-ttu-id="94045-288">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-288">Return value</span></span>
|<span data-ttu-id="94045-289">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-289">Type</span></span> | <span data-ttu-id="94045-290">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-290">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-291">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-291">DOMString</span></span> | <span data-ttu-id="94045-292">El valor devuelto es una de las cadenas `MSApp.HIGH` , `MSApp.NORMAL` , o `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="94045-292">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>

#### <span data-ttu-id="94045-293">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-293">Remarks</span></span>
<span data-ttu-id="94045-294">Este método devuelve la prioridad contextual actual (vea la [`MSApp Constants`](#msapp-constants) ), que puede cambiarse a través `execAtPriority` de y `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="94045-294">This method returns the current contextual priority (see [`MSApp Constants`](#msapp-constants)), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>

#### <span data-ttu-id="94045-295">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-295">Example</span></span>

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### <span data-ttu-id="94045-296">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="94045-296">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="94045-297">API sincrónica que ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="94045-297">Synchronous API that has been deprecated.</span></span> <span data-ttu-id="94045-298">Para Windows 10, consulte `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="94045-298">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span> <span data-ttu-id="94045-299">Para las aplicaciones de Windows 8 y 8,1, consulte la entrada de MSDN para [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="94045-299">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="94045-300">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="94045-300">getHtmlPrintDocumentSourceAsync</span></span>
<span data-ttu-id="94045-301">Devuelve el contenido de origen que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="94045-301">Returns the source content that is to be printed.</span></span>

#### <span data-ttu-id="94045-302">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-302">Parameters</span></span>
`htmlDoc` <span data-ttu-id="94045-303">por</span><span class="sxs-lookup"><span data-stu-id="94045-303">[in]</span></span>

|<span data-ttu-id="94045-304">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-304">Type</span></span> | <span data-ttu-id="94045-305">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-305">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-306">Documento</span><span class="sxs-lookup"><span data-stu-id="94045-306">Document</span></span> | <span data-ttu-id="94045-307">Documento HTML que se va a imprimir.</span><span class="sxs-lookup"><span data-stu-id="94045-307">The HTML document to be printed.</span></span> <span data-ttu-id="94045-308">Puede ser el documento raíz, el documento en un iframe, un fragmento de documento o un documento SVG.</span><span class="sxs-lookup"><span data-stu-id="94045-308">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span> <span data-ttu-id="94045-309">Tenga en cuenta que htmlDoc debe ser un documento, no un elemento.</span><span class="sxs-lookup"><span data-stu-id="94045-309">Be aware that htmlDoc must be a document, not an element.</span></span>

#### <span data-ttu-id="94045-310">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="94045-310">Example 1</span></span>

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

#### <span data-ttu-id="94045-311">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="94045-311">Example 2</span></span>

```javascript
    function registerForPrintContract() {
            var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
            printManager.onprinttaskrequested = onPrintTaskRequested;
            console.log("Print Contract registered. Use the Print button to print.", "sample", "status");
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

### <span data-ttu-id="94045-312">getViewId</span><span class="sxs-lookup"><span data-stu-id="94045-312">getViewId</span></span> 
<span data-ttu-id="94045-313">Compatibilidad con varias ventanas.</span><span class="sxs-lookup"><span data-stu-id="94045-313">Support for multiple windows.</span></span> 

> [!NOTE] 
> <span data-ttu-id="94045-314">En las aplicaciones para UWP con JavaScript para Windows 8.1, se admiten varias ventanas con las API de MSApp DOM que ahora son depricated.</span><span class="sxs-lookup"><span data-stu-id="94045-314">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span> <span data-ttu-id="94045-315">Para Windows 10, use `window.open` , `window` y el nuevo `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="94045-315">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>

| <span data-ttu-id="94045-316">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-316">Description</span></span> |<span data-ttu-id="94045-317">Windows 10</span><span class="sxs-lookup"><span data-stu-id="94045-317">Windows 10</span></span> | <span data-ttu-id="94045-318">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="94045-318">Windows 8.1</span></span> |  
|:---- |:---- |:--- |  
| <span data-ttu-id="94045-319">Crear nueva ventana</span><span class="sxs-lookup"><span data-stu-id="94045-319">Create new window</span></span> | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|<span data-ttu-id="94045-320">Nuevo objeto de ventana</span><span class="sxs-lookup"><span data-stu-id="94045-320">New window object</span></span> | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### <span data-ttu-id="94045-321">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-321">Parameters</span></span>
`window`

|<span data-ttu-id="94045-322">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-322">Type</span></span> | <span data-ttu-id="94045-323">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-323">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-324">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-324">DOMString</span></span> | <span data-ttu-id="94045-325">Un objeto que representa una ventana que contiene un documento DOM.</span><span class="sxs-lookup"><span data-stu-id="94045-325">An object representing a window containing a DOM document.</span></span> | 

#### <span data-ttu-id="94045-326">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-326">Return value</span></span>

`viewId`

|<span data-ttu-id="94045-327">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-327">Type</span></span> | <span data-ttu-id="94045-328">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-328">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-329">Número</span><span class="sxs-lookup"><span data-stu-id="94045-329">Number</span></span> | <span data-ttu-id="94045-330">Puede usarse con las distintas [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API.</span><span class="sxs-lookup"><span data-stu-id="94045-330">Can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

#### <span data-ttu-id="94045-331">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-331">Remarks</span></span>
<span data-ttu-id="94045-332">Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) y [`window`](https://developer.mozilla.org/docs/Web/API/Window) para crear nuevas ventanas, pero después, para interactuar con las API de WinRT, agregue la `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="94045-332">Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) and [`window`](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span> <span data-ttu-id="94045-333">Toma un `window` objeto como parámetro y devuelve un `viewId` número que se puede usar con las distintas [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API.</span><span class="sxs-lookup"><span data-stu-id="94045-333">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

##### <span data-ttu-id="94045-334">Retrasar la visibilidad</span><span class="sxs-lookup"><span data-stu-id="94045-334">Delaying Visibility</span></span> 
<span data-ttu-id="94045-335">Normalmente, las vistas de WinRT se inician de forma oculta y el desarrollador final usa algo como `TryShowAsStandaloneAsync` para mostrar la vista una vez que se ha preparado por completo.</span><span class="sxs-lookup"><span data-stu-id="94045-335">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span> <span data-ttu-id="94045-336">En el mundo web, `window.open` muestra inmediatamente una ventana y el usuario final puede ver que el contenido se carga y se representa.</span><span class="sxs-lookup"><span data-stu-id="94045-336">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span> <span data-ttu-id="94045-337">Para que la nueva Windows funcione como vistas en WinRT y no se muestre inmediatamente, hemos añadido una `window.open` opción.</span><span class="sxs-lookup"><span data-stu-id="94045-337">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span> <span data-ttu-id="94045-338">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="94045-338">For example:</span></span>
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### <span data-ttu-id="94045-339">Diferencias entre ventanas principales</span><span class="sxs-lookup"><span data-stu-id="94045-339">Primary Window Differences</span></span>
<span data-ttu-id="94045-340">La ventana principal que inicialmente abre el sistema operativo funciona de forma diferente a la de las ventanas secundarias que abre:</span><span class="sxs-lookup"><span data-stu-id="94045-340">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span> 

|<span data-ttu-id="94045-341">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-341">Description</span></span> | <span data-ttu-id="94045-342">Principal</span><span class="sxs-lookup"><span data-stu-id="94045-342">Primary</span></span> | <span data-ttu-id="94045-343">Secundario</span><span class="sxs-lookup"><span data-stu-id="94045-343">Secondary</span></span> |
|:---- |:--- |:--- |
|<span data-ttu-id="94045-344">Window. Open</span><span class="sxs-lookup"><span data-stu-id="94045-344">window.open</span></span> | <span data-ttu-id="94045-345">Se permite</span><span class="sxs-lookup"><span data-stu-id="94045-345">Allowed</span></span> | <span data-ttu-id="94045-346">No permitido</span><span class="sxs-lookup"><span data-stu-id="94045-346">Disallowed</span></span> |
|<span data-ttu-id="94045-347">Window. Close</span><span class="sxs-lookup"><span data-stu-id="94045-347">window.close</span></span> | <span data-ttu-id="94045-348">Cerrar aplicación</span><span class="sxs-lookup"><span data-stu-id="94045-348">Close app</span></span> | <span data-ttu-id="94045-349">Cerrar ventana</span><span class="sxs-lookup"><span data-stu-id="94045-349">Close window</span></span> |
| <span data-ttu-id="94045-350">Restricciones de navegación</span><span class="sxs-lookup"><span data-stu-id="94045-350">Navigation restrictions</span></span> | <span data-ttu-id="94045-351">ACUR solo</span><span class="sxs-lookup"><span data-stu-id="94045-351">ACUR only</span></span> | <span data-ttu-id="94045-352">Sin restricciones</span><span class="sxs-lookup"><span data-stu-id="94045-352">No restrictions</span></span> |

<span data-ttu-id="94045-353">La restricción para no permitir la apertura de ventanas secundarias podría cambiar en el futuro en función de los [comentarios](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span><span class="sxs-lookup"><span data-stu-id="94045-353">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>

##### <span data-ttu-id="94045-354">Restricciones de comunicación del mismo origen</span><span class="sxs-lookup"><span data-stu-id="94045-354">Same Origin Communication Restrictions</span></span> 
<span data-ttu-id="94045-355">Hay un difícil problema técnico que evita que se admitan las llamadas a secuencias de comandos sincrónicas, del mismo origen y de ventana cruzada.</span><span class="sxs-lookup"><span data-stu-id="94045-355">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span> <span data-ttu-id="94045-356">Cuando se abre una ventana que tiene el mismo origen, se permite que la secuencia de comandos de una ventana llame directamente a las funciones de la otra ventana y se producirá un error en algunas de estas llamadas.</span><span class="sxs-lookup"><span data-stu-id="94045-356">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span> `postMessage` <span data-ttu-id="94045-357">las llamadas funcionan perfectamente y es la manera recomendada de hacer cosas si es posible.</span><span class="sxs-lookup"><span data-stu-id="94045-357">calls work just fine and is the recommended way to do things if possible.</span></span> <span data-ttu-id="94045-358">El trabajo para mejorar este problema está en curso.</span><span class="sxs-lookup"><span data-stu-id="94045-358">Work to improve this issue is in progress.</span></span>


### <span data-ttu-id="94045-359">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="94045-359">isTaskScheduledAtPriorityOrHigher</span></span> 
<span data-ttu-id="94045-360">Devuelve un valor de tipo Boolean que indica si hay trabajo pendiente en el nivel de prioridad dado o superior.</span><span class="sxs-lookup"><span data-stu-id="94045-360">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### <span data-ttu-id="94045-361">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-361">Parameters</span></span>
`priority` <span data-ttu-id="94045-362">por</span><span class="sxs-lookup"><span data-stu-id="94045-362">[in]</span></span>

|<span data-ttu-id="94045-363">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-363">Type</span></span> | <span data-ttu-id="94045-364">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-364">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-365">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-365">DOMString</span></span> | <span data-ttu-id="94045-366">Un valor de prioridad (vea [constantes MSApp](#msapp-constants)) que especifica el nivel de prioridad y superior para consultar cualquier trabajo pendiente en la cola.</span><span class="sxs-lookup"><span data-stu-id="94045-366">A priority value (see [MSApp Constants](#msapp-constants)) specifying the priority level and above to query for any outstanding queued work.</span></span>

#### <span data-ttu-id="94045-367">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-367">Return value</span></span>
|<span data-ttu-id="94045-368">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-368">Type</span></span> | <span data-ttu-id="94045-369">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-369">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-370">Booleano</span><span class="sxs-lookup"><span data-stu-id="94045-370">Boolean</span></span> | <span data-ttu-id="94045-371">Devuelve `true` si hay algún trabajo en cola en el nivel de prioridad especificado o superior, de `false` lo contrario.</span><span class="sxs-lookup"><span data-stu-id="94045-371">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>

#### <span data-ttu-id="94045-372">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-372">Remarks</span></span>
<span data-ttu-id="94045-373">El `isTaskScheduledAtPriorityOrHigher` método proporciona un medio para que el código de JavaScript determine si hay trabajo pendiente en los distintos niveles de prioridad (o posteriores) con la intención de que el código JavaScript de la llamada pueda decidir dar lugar a un trabajo de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="94045-373">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels (or above) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>

#### <span data-ttu-id="94045-374">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-374">Example</span></span>

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

### <span data-ttu-id="94045-375">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="94045-375">pageHandlesAllApplicationActivations</span></span>
<span data-ttu-id="94045-376">Se usa para evitar una actualización de la ruta de acceso de inicio (volver a cargar la página) antes de cada evento Activate (es decir, haciendo clic en una notificación o en un mosaico anclado).</span><span class="sxs-lookup"><span data-stu-id="94045-376">Used to avoid a refresh of the start path (page reload) before every activate event (ie. clicking a notification or a pinned tile).</span></span> 

#### <span data-ttu-id="94045-377">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-377">Parameters</span></span>

|<span data-ttu-id="94045-378">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-378">Type</span></span> | <span data-ttu-id="94045-379">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-379">Description</span></span> |
|:---- |:--- |
<span data-ttu-id="94045-380">Booleano</span><span class="sxs-lookup"><span data-stu-id="94045-380">Boolean</span></span> | <span data-ttu-id="94045-381">Use `MSApp.pageHandlesAllApplicationActivations(true)` esta para omitir siempre la actualización de la ruta de inicio (volver a cargar la página) y, en su lugar, saltar directamente al desencadenar el `WebUIApplication` evento activado.</span><span class="sxs-lookup"><span data-stu-id="94045-381">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span> <span data-ttu-id="94045-382">Requiere que todas las páginas manejen los eventos de activación por separado.</span><span class="sxs-lookup"><span data-stu-id="94045-382">Requires that all pages handle activation events separately.</span></span> <span data-ttu-id="94045-383">Al definir este método como `true` , al hacer clic en un evento activado (como un notificaiton), no se activará la recarga, una de las aplicaciones básicas para las aplicaciones de una sola página que deseen evitar la recarga de la página.</span><span class="sxs-lookup"><span data-stu-id="94045-383">By defining this method as `true`, clicking an activated event (like a notificaiton) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>

#### <span data-ttu-id="94045-384">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-384">Example</span></span> 

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

### <span data-ttu-id="94045-385">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="94045-385">suppressSubdownloadCredentialPrompts</span></span> 
<span data-ttu-id="94045-386">Controla si una aplicación suprime posibles mensajes de autenticación durante la descarga de recursos.</span><span class="sxs-lookup"><span data-stu-id="94045-386">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### <span data-ttu-id="94045-387">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-387">Parameters</span></span>
`suppress` <span data-ttu-id="94045-388">por</span><span class="sxs-lookup"><span data-stu-id="94045-388">[in]</span></span>

|<span data-ttu-id="94045-389">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-389">Type</span></span> | <span data-ttu-id="94045-390">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-390">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-391">Booleano</span><span class="sxs-lookup"><span data-stu-id="94045-391">Boolean</span></span> | <span data-ttu-id="94045-392">El valor true suprime las solicitudes de autenticación potenciales.</span><span class="sxs-lookup"><span data-stu-id="94045-392">A value of true suppresses potential authentication prompts.</span></span> <span data-ttu-id="94045-393">El valor false no suprime ninguna solicitud de autenticación potencial del usuario.</span><span class="sxs-lookup"><span data-stu-id="94045-393">A value of false does not suppress any potential authentication prompts from the user.</span></span>

#### <span data-ttu-id="94045-394">Valor returado</span><span class="sxs-lookup"><span data-stu-id="94045-394">Returan value</span></span>
<span data-ttu-id="94045-395">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="94045-395">None.</span></span>

#### <span data-ttu-id="94045-396">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-396">Remarks</span></span>
<span data-ttu-id="94045-397">El `suppressSubdownloadCredentialPrompts` método controla si una aplicación suprime las solicitudes de autenticación potenciales durante la descarga de recursos.</span><span class="sxs-lookup"><span data-stu-id="94045-397">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span> <span data-ttu-id="94045-398">El comportamiento predeterminado es no suprimir las solicitudes de credenciales.</span><span class="sxs-lookup"><span data-stu-id="94045-398">The default behavior is to not suppress credential prompts.</span></span>

`suppressSubdownloadCredentialPrompts` <span data-ttu-id="94045-399">está pensado para que lo usen aplicaciones que pueden cargar un número excesivo de recursos que requieren autenticación, como una aplicación de correo (que puede contener un boletín con un número de imágenes en el que cada imagen requiera autenticación).</span><span class="sxs-lookup"><span data-stu-id="94045-399">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app (which could contain a newsletter containing a number of images where each image requires authentication).</span></span>

<span data-ttu-id="94045-400">Al suprimir las solicitudes de credenciales, los cuadros de diálogo para autenticar a los servidores no se mostrarán al acceder a los recursos que requieren autenticación, y el recurso no se descargará.</span><span class="sxs-lookup"><span data-stu-id="94045-400">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span> <span data-ttu-id="94045-401">Tenga en cuenta que no `suppressSubdownloadCredentialPrompts` afecta otros indicadores posibles, como la autenticación de proxy o los cuadros de diálogo de solicitud de certificación del cliente, ni afecta a XHR.</span><span class="sxs-lookup"><span data-stu-id="94045-401">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>

<span data-ttu-id="94045-402">Tenga en cuenta que `suppressSubdownloadCredentialPrompts` afecta a todo el contenido de la aplicación, incluido el contenido hospedado en el `webview` elemento.</span><span class="sxs-lookup"><span data-stu-id="94045-402">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>
 
<span data-ttu-id="94045-403">**Importante:**  Las decisiones de solicitud de credenciales se almacenan en caché.</span><span class="sxs-lookup"><span data-stu-id="94045-403">**Important:**  Credential prompt decisions are cached.</span></span> <span data-ttu-id="94045-404">Por lo tanto, aunque la supresión de las solicitudes de credenciales surtirá efecto inmediatamente, es posible que sea necesario volver a cargar el documento para permitir las solicitudes de credenciales después de suprimirlas.</span><span class="sxs-lookup"><span data-stu-id="94045-404">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>

#### <span data-ttu-id="94045-405">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-405">Example</span></span>

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### <span data-ttu-id="94045-406">terminateApp</span><span class="sxs-lookup"><span data-stu-id="94045-406">terminateApp</span></span>
<span data-ttu-id="94045-407">Finaliza la aplicación actual y genera un informe de error.</span><span class="sxs-lookup"><span data-stu-id="94045-407">Terminates the current application and generates a failure report.</span></span> 

```javascript
MSApp.terminateApp(error); 
```

#### <span data-ttu-id="94045-408">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-408">Parameters</span></span>
`error` <span data-ttu-id="94045-409">por</span><span class="sxs-lookup"><span data-stu-id="94045-409">[in]</span></span>

<span data-ttu-id="94045-410">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-410">Type</span></span> | <span data-ttu-id="94045-411">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-411">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-412">Error</span><span class="sxs-lookup"><span data-stu-id="94045-412">Error</span></span> | <span data-ttu-id="94045-413">Un `Error` objeto que se puede usar para describir el error que ha desencadenado la finalización.</span><span class="sxs-lookup"><span data-stu-id="94045-413">An `Error` object that you can use to describe the error that triggered the termination.</span></span> <span data-ttu-id="94045-414">El `Error` objeto debe contener las propiedades Number, Description y stack; no se generará un informe de errores si el objeto no contiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="94045-414">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>

#### <span data-ttu-id="94045-415">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-415">Return value</span></span>
<span data-ttu-id="94045-416">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="94045-416">None.</span></span>

#### <span data-ttu-id="94045-417">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94045-417">Remarks</span></span>
<span data-ttu-id="94045-418">Si el problema notificado por `terminateApp` se convierte en uno de los cinco principales problemas de la aplicación, se mostrará en la página calidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="94045-418">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>

#### <span data-ttu-id="94045-419">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-419">Example</span></span>
<span data-ttu-id="94045-420">Este ejemplo llama `terminateApp` cuando se encuentra una excepción.</span><span class="sxs-lookup"><span data-stu-id="94045-420">This example calls `terminateApp` when an exception is encountered.</span></span> <span data-ttu-id="94045-421">Usa el `Error` objeto proporcionado cuando se detecta una excepción.</span><span class="sxs-lookup"><span data-stu-id="94045-421">It uses the `Error` object provided when you catch an exception.</span></span> 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### <span data-ttu-id="94045-422">Constantes MSApp</span><span class="sxs-lookup"><span data-stu-id="94045-422">MSApp Constants</span></span>
<span data-ttu-id="94045-423">Valores de prioridad permitidos asociados con `execAsyncAtPriority` ,, `execAtPriority` `getCurrentPriority` y `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="94045-423">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>

#### <span data-ttu-id="94045-424">Actual</span><span class="sxs-lookup"><span data-stu-id="94045-424">Current</span></span>
`current`

|<span data-ttu-id="94045-425">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-425">Type</span></span> | <span data-ttu-id="94045-426">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-426">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-427">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-427">DOMString</span></span> | <span data-ttu-id="94045-428">Cuando `current` se usa con el método adecuado (vea también la sección), el método usará la prioridad contextual actual al ejecutar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="94045-428">When `current` is used with the appropriate method (See also section), the method will use the current contextual priority when executing the requested operation.</span></span>

#### <span data-ttu-id="94045-429">Alto</span><span class="sxs-lookup"><span data-stu-id="94045-429">High</span></span>
`high`

|<span data-ttu-id="94045-430">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-430">Type</span></span> | <span data-ttu-id="94045-431">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-431">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-432">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-432">DOMString</span></span> | <span data-ttu-id="94045-433">Cuando `high` se usa con el método adecuado (vea también la sección), el método usará una prioridad mayor que la normal al ejecutar la operación solicitada y se enviará la operación antes de que se realice cualquier trabajo de prioridad normal existente.</span><span class="sxs-lookup"><span data-stu-id="94045-433">When `high` is used with the appropriate method (See also section), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>

#### <span data-ttu-id="94045-434">Inactivo</span><span class="sxs-lookup"><span data-stu-id="94045-434">Idle</span></span>
`idle`

|<span data-ttu-id="94045-435">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-435">Type</span></span> | <span data-ttu-id="94045-436">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-436">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-437">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-437">DOMString</span></span> | <span data-ttu-id="94045-438">Cuando `ideal` se usa con el método adecuado (vea también la sección), el método usará la prioridad inferior a la normal al ejecutar la operación solicitada y se enviará la operación después de cualquier trabajo de prioridad normal existente.</span><span class="sxs-lookup"><span data-stu-id="94045-438">When `ideal` is used with the appropriate method (See also section), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>

#### <span data-ttu-id="94045-439">Normal</span><span class="sxs-lookup"><span data-stu-id="94045-439">Normal</span></span>
`normal`

|<span data-ttu-id="94045-440">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-440">Type</span></span> | <span data-ttu-id="94045-441">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-441">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-442">DOMString</span><span class="sxs-lookup"><span data-stu-id="94045-442">DOMString</span></span> | <span data-ttu-id="94045-443">Cuando `normal` se usa con el método adecuado (vea también la sección), el método usará la prioridad normal existente al ejecutar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="94045-443">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>

#### <span data-ttu-id="94045-444">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="94045-444">Example</span></span>

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### <span data-ttu-id="94045-445">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94045-445">Requirements</span></span>
|<span data-ttu-id="94045-446">IDL</span><span class="sxs-lookup"><span data-stu-id="94045-446">IDL</span></span> | <span data-ttu-id="94045-447">Mshtml. idl</span><span class="sxs-lookup"><span data-stu-id="94045-447">Mshtml.idl</span></span> |
|:---- |:--- |

## <span data-ttu-id="94045-448">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="94045-448">MSAppAsyncOperation</span></span>

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### <span data-ttu-id="94045-449">start</span><span class="sxs-lookup"><span data-stu-id="94045-449">start</span></span>
<span data-ttu-id="94045-450">Inicia el `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="94045-450">Starts the `MSAppAsyncOperation`.</span></span>

```javascript
var retval = MSAppAsyncOperation.start();
```

#### <span data-ttu-id="94045-451">Parameters</span><span class="sxs-lookup"><span data-stu-id="94045-451">Parameters</span></span>
<span data-ttu-id="94045-452">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="94045-452">None.</span></span>

#### <span data-ttu-id="94045-453">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94045-453">Return value</span></span>
<span data-ttu-id="94045-454">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="94045-454">None.</span></span>

#### <span data-ttu-id="94045-455">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94045-455">Properties</span></span>
`error` <span data-ttu-id="94045-456">propiedad</span><span class="sxs-lookup"><span data-stu-id="94045-456">property</span></span>

|<span data-ttu-id="94045-457">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-457">Type</span></span> | <span data-ttu-id="94045-458">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-458">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-459">DOMError</span><span class="sxs-lookup"><span data-stu-id="94045-459">DOMError</span></span> | <span data-ttu-id="94045-460">Representa un error en `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="94045-460">Represents an error in `MSAppAsyncOperation`.</span></span>

```javascript
p = object.error
```

`oncomplete` <span data-ttu-id="94045-461">propiedad</span><span class="sxs-lookup"><span data-stu-id="94045-461">property</span></span>

|<span data-ttu-id="94045-462">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-462">Type</span></span> | <span data-ttu-id="94045-463">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-463">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-464">EventHandler</span><span class="sxs-lookup"><span data-stu-id="94045-464">EventHandler</span></span> | <span data-ttu-id="94045-465">Propiedad para establecer un controlador de eventos finalizado `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="94045-465">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.oncomplete
```

`onerror` <span data-ttu-id="94045-466">propiedad</span><span class="sxs-lookup"><span data-stu-id="94045-466">property</span></span>

|<span data-ttu-id="94045-467">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-467">Type</span></span> | <span data-ttu-id="94045-468">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-468">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-469">EventHandler</span><span class="sxs-lookup"><span data-stu-id="94045-469">EventHandler</span></span> | <span data-ttu-id="94045-470">Propiedad para establecer un controlador de eventos cuando se produce un error `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="94045-470">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>

```javascript
p = object.onerror
```

`readyState` <span data-ttu-id="94045-471">propiedad</span><span class="sxs-lookup"><span data-stu-id="94045-471">property</span></span>

|<span data-ttu-id="94045-472">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-472">Type</span></span> | <span data-ttu-id="94045-473">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-473">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-474">Número</span><span class="sxs-lookup"><span data-stu-id="94045-474">Number</span></span> | <span data-ttu-id="94045-475">Representa el estado de la operación asincrónica dentro de la aplicación de Windows con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="94045-475">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span> <span data-ttu-id="94045-476">Los valores son: iniciada [0], completada el [1], error [2].</span><span class="sxs-lookup"><span data-stu-id="94045-476">Values include: Started[0], Completed[1], Error[2].</span></span>

```javascript
p = object.readyState
```

`result` <span data-ttu-id="94045-477">propiedad</span><span class="sxs-lookup"><span data-stu-id="94045-477">property</span></span>

|<span data-ttu-id="94045-478">Tipo</span><span class="sxs-lookup"><span data-stu-id="94045-478">Type</span></span> | <span data-ttu-id="94045-479">Descripción</span><span class="sxs-lookup"><span data-stu-id="94045-479">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="94045-480">Cualquiera</span><span class="sxs-lookup"><span data-stu-id="94045-480">Any</span></span> |<span data-ttu-id="94045-481">Representa el resultado de `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="94045-481">Represents the result of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.result
```

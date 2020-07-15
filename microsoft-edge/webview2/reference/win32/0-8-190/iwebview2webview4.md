---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 8b029202843dd006be4d9ecdadc63161bebb6b39
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878060"
---
# <span data-ttu-id="cf1ab-104">0.8.355: IWebView2WebView4</span><span class="sxs-lookup"><span data-stu-id="cf1ab-104">0.8.355 - interface IWebView2WebView4</span></span> 

> [!NOTE]
> <span data-ttu-id="cf1ab-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="cf1ab-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

<span data-ttu-id="cf1ab-107">Funcionalidad adicional implementada por el objeto WebView principal.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="cf1ab-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="cf1ab-108">Summary</span></span>

 <span data-ttu-id="cf1ab-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf1ab-109">Members</span></span>                        | <span data-ttu-id="cf1ab-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cf1ab-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cf1ab-111">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf1ab-111">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="cf1ab-112">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-112">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="cf1ab-113">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf1ab-113">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="cf1ab-114">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-114">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="cf1ab-115">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="cf1ab-115">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="cf1ab-116">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-116">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="cf1ab-117">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="cf1ab-117">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="cf1ab-118">Agregue un controlador de eventos para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-118">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="cf1ab-119">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="cf1ab-119">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="cf1ab-120">Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-120">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="cf1ab-121">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="cf1ab-121">WEBVIEW2_KEY_EVENT_TYPE</span></span>](#webview2_key_event_type) | <span data-ttu-id="cf1ab-122">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-122">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="cf1ab-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="cf1ab-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#webview2_physical_key_status) | <span data-ttu-id="cf1ab-124">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-124">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="cf1ab-125">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="cf1ab-125">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="cf1ab-126">Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1ab-126">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="cf1ab-127">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf1ab-127">Members</span></span>

#### <span data-ttu-id="cf1ab-128">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf1ab-128">AddRemoteObject</span></span> 

<span data-ttu-id="cf1ab-129">Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-129">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="cf1ab-130">[ADDREMOTEOBJECT](#addremoteobject)HRESULT público (LPCWSTR Name, Variant \* Object)</span><span class="sxs-lookup"><span data-stu-id="cf1ab-130">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="cf1ab-131">Los objetos de host se exponen como proxies de objetos remotos a través de `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="cf1ab-131">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="cf1ab-132">Los proxies de objetos remotos son promesas y se resolverán como un objeto que represente el objeto de host.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-132">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="cf1ab-133">La promesa se rechaza si la aplicación no ha agregado un objeto con el nombre.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-133">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="cf1ab-134">Cuando el código de JavaScript tiene acceso a una propiedad o método del objeto, se devuelve una promesa, que se resolverá con el valor devuelto por el host para la propiedad o el método, o se rechazará en caso de error, como no se trata de una propiedad o método en el objeto o los parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-134">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="cf1ab-135">Por ejemplo, cuando el código de la aplicación hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cf1ab-135">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="cf1ab-136">El código de JavaScript de WebView podrá acceder a appObject como sigue y, a continuación, a los atributos y métodos de appObject:</span><span class="sxs-lookup"><span data-stu-id="cf1ab-136">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="cf1ab-137">Tenga en cuenta que aunque se admiten tipos simples, IDispatch y matriz, no se admiten IUnknown genérico, VT_DECIMAL o VT_RECORD Variant.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-137">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="cf1ab-138">Los objetos remotos de JavaScript, como las funciones de devolución de llamada, se representan como una variante VT_DISPATCH con el objeto que implementa IDispatch.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-138">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="cf1ab-139">El método de devolución de llamada de JavaScript se puede invocar con DISPID_VALUE para el DispId.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-139">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="cf1ab-140">Las matrices anidadas se admiten hasta una profundidad de 3.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-140">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="cf1ab-141">No se admiten las matrices de los tipos de referencia.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-141">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="cf1ab-142">VT_EMPTY y VT_NULL se asignan a JavaScript como null.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-142">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="cf1ab-143">En JavaScript, los valores NULL y undefined se asignan a VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-143">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="cf1ab-144">Además, todos los objetos remotos se exponen como `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="cf1ab-144">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="cf1ab-145">Aquí los objetos host se exponen como proxies de objetos remotos sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-145">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="cf1ab-146">No se trata de promesas ni llamadas a funciones o acceso a propiedad de forma sincrónica bloquear la ejecución de scripts en espera de comunicar el proceso cruzado para que se ejecute el código de host.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-146">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="cf1ab-147">Por consiguiente, esto puede dar lugar a problemas de confiabilidad y se recomienda usar la API asíncrona basada en Promise `window.chrome.webview.remoteObjects.<name>` descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-147">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="cf1ab-148">Los proxies de objetos remotos sincrónicos y los proxies asincrónicos de objetos remotos pueden tener como proxy el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-148">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="cf1ab-149">Los cambios remotos realizados por un proxy se reflejarán en cualquier otro proxy de ese mismo objeto remoto, ya sean otros servidores proxy, sincrónicos o asíncronos.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-149">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="cf1ab-150">Aunque JavaScript está bloqueado en una llamada sincrónica al código nativo, ese código nativo no puede devolver la llamada a JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-150">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="cf1ab-151">Los intentos de hacerlo fallarán con HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="cf1ab-151">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="cf1ab-152">Los proxies de objetos remotos son objetos proxy de JavaScript que interceptan todas las llamadas a propiedades get, Set Property y Method.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-152">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="cf1ab-153">Las propiedades o métodos que forman parte de la función o del prototipo de objeto se ejecutan de forma local.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-153">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="cf1ab-154">Además, cualquier propiedad o método de la matriz se `chrome.webview.remoteObjects.options.forceLocalProperties` ejecutará de forma local.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-154">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="cf1ab-155">De forma predeterminada, se incluyen métodos opcionales que tienen significado en JavaScript como `toJSON` y `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="cf1ab-155">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="cf1ab-156">Puede agregar más a esta matriz, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-156">You can add more to this array as required.</span></span>

<span data-ttu-id="cf1ab-157">Hay un método que puede resultar `chrome.webview.remoteObjects.cleanupSome` más conveniente para la recolección de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-157">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="cf1ab-158">Los proxies de objetos remotos también tienen los siguientes métodos que se ejecutan de forma local:</span><span class="sxs-lookup"><span data-stu-id="cf1ab-158">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="cf1ab-159">applyRemote, getRemote, setRemote: realizar una invocación de método, una propiedad get o un conjunto de propiedades en el objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-159">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="cf1ab-160">Puede usarlos para obligar a que un método o una propiedad se ejecuten de forma remota si hay una propiedad o un método local en conflicto.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-160">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="cf1ab-161">Por ejemplo, `proxy.toString()` ejecutará el método toString local en el objeto de proxy.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-161">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="cf1ab-162">Pero `proxy.applyRemote('toString')` se ejecuta `toString` en el objeto remoto a través del proxy.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-162">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="cf1ab-163">getLocal, setLocal: realizar obtención de propiedad o conjunto de propiedades de forma local.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-163">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="cf1ab-164">Puede usar estos métodos para forzar o establecer una propiedad en el proxy del objeto remoto, en lugar de hacerlo en el objeto remoto al que representa.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-164">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="cf1ab-165">Por ejemplo, `proxy.unknownProperty` obtendrá la propiedad nombrada `unknownProperty` desde el objeto remoto a través del proxy.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-165">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="cf1ab-166">Pero `proxy.getLocal('unknownProperty')` obtendrá el valor de la propiedad `unknownProperty` en el propio objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-166">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="cf1ab-167">sincronizar: los proxies de objetos remotos asincrónicos exponen un método de sincronización que devuelve una promesa de un proxy de objetos remotos sincrónico para el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-167">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="cf1ab-168">Por ejemplo, `chrome.webview.remoteObjects.sample.methodCall()` devuelve un proxy asincrónico de objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-168">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="cf1ab-169">Puede usar el `sync` método para obtener un proxy de objetos remotos sincrónico en su lugar:</span><span class="sxs-lookup"><span data-stu-id="cf1ab-169">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="cf1ab-170">Async: los proxies de objetos remotos sincrónicos exponen un método Async que bloquea y devuelve un proxy de objetos remotos asincrónicos para el mismo objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-170">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="cf1ab-171">Por ejemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` devuelve un proxy de objeto remoto sincrónico.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-171">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="cf1ab-172">Se llama al `async` método de este bloque y, a continuación, se devuelve un proxy de objeto remoto asincrónico para el mismo objeto remoto:</span><span class="sxs-lookup"><span data-stu-id="cf1ab-172">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="cf1ab-173">después: los proxies de objetos remotos asincrónicos tienen un método then.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-173">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="cf1ab-174">Esto permite que sean esperados.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-174">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="cf1ab-175">devolverá una promesa que se resolverá con una representación del objeto remoto.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-175">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="cf1ab-176">Si el proxy representa un literal de JavaScript, se devuelve una copia de forma local.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-176">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="cf1ab-177">Si el proxy representa una función, se devuelve un proxy que no es de espera.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-177">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="cf1ab-178">Si el proxy representa un objeto de JavaScript con una combinación de propiedades literales y propiedades de función, se devuelve una copia del objeto con algunas propiedades como proxy de objetos remotos.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-178">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="cf1ab-179">Todas las demás invocaciones a propiedades y métodos (excepto los métodos anteriores de proxy de objeto remoto, la lista de forceLocalProperties y las propiedades de los prototipos de funciones y objetos) se ejecutan de forma remota.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-179">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="cf1ab-180">Los proxies de objetos remotos asincrónicos devuelven una promesa que representa la finalización asincrónica de la invocación remota del método u obtiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-180">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="cf1ab-181">La función Promise se resuelve después de que las operaciones remotas se completen y las promesas se resuelven en el valor resultante de la operación.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-181">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="cf1ab-182">Los proxy de objetos remotos sincrónicos funcionan de manera similar pero bloquean la ejecución remota y esperan a que se complete la operación remota.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-182">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="cf1ab-183">Establecer una propiedad en un proxy de objetos remotos asincrónicos funciona de forma ligeramente distinta.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-183">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="cf1ab-184">El conjunto devolverá inmediatamente y el valor devuelto es el valor que se establecerá.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-184">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="cf1ab-185">Este es un requisito del objeto proxy de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-185">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="cf1ab-186">Si necesita esperar de forma asincrónica para que se complete el conjunto de propiedades, use el método setRemote que devuelve una promesa según se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-186">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="cf1ab-187">La propiedad sincrónico del conjunto de propiedades de objeto se bloquea de forma sincrónica hasta que se establece la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-187">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="cf1ab-188">Por ejemplo, supongamos que tiene un objeto COM con la siguiente interfaz</span><span class="sxs-lookup"><span data-stu-id="cf1ab-188">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 <span data-ttu-id="cf1ab-189">Podemos añadir una instancia de esta interfaz a nuestro JavaScript con `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="cf1ab-189">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="cf1ab-190">En este caso, lo hemos denominado `sample` :</span><span class="sxs-lookup"><span data-stu-id="cf1ab-190">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 <span data-ttu-id="cf1ab-191">A continuación, en el documento HTML podemos usar este objeto COM mediante `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="cf1ab-191">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### <span data-ttu-id="cf1ab-192">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="cf1ab-192">RemoveRemoteObject</span></span> 

<span data-ttu-id="cf1ab-193">Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-193">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="cf1ab-194">[REMOVEREMOTEOBJECT](#removeremoteobject)HRESULT público (LPCWSTR Name)</span><span class="sxs-lookup"><span data-stu-id="cf1ab-194">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="cf1ab-195">Aunque se denegarán nuevos intentos de acceso, si el código de JavaScript ya ha obtenido el objeto, el código de JavaScript seguirá teniendo acceso a ese objeto.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-195">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="cf1ab-196">Llamar a este método para un nombre que ya se ha quitado o no se ha agregado nunca producirá un error.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-196">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="cf1ab-197">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="cf1ab-197">OpenDevToolsWindow</span></span> 

<span data-ttu-id="cf1ab-198">Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-198">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="cf1ab-199">[OPENDEVTOOLSWINDOW](#opendevtoolswindow)HRESULT público ()</span><span class="sxs-lookup"><span data-stu-id="cf1ab-199">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="cf1ab-200">No hace nada si se llama cuando la ventana de DevTools ya está abierta</span><span class="sxs-lookup"><span data-stu-id="cf1ab-200">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="cf1ab-201">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="cf1ab-201">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="cf1ab-202">Agregue un controlador de eventos para el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-202">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="cf1ab-203">[add_AcceleratorKeyPressed](#add_acceleratorkeypressed)de HRESULT público ([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="cf1ab-203">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="cf1ab-204">AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-204">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="cf1ab-205">Una clave se considera un acelerador si:</span><span class="sxs-lookup"><span data-stu-id="cf1ab-205">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="cf1ab-206">La tecla Ctrl o Alt se está retenida actualmente, o bien</span><span class="sxs-lookup"><span data-stu-id="cf1ab-206">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="cf1ab-207">la tecla presionada no se asigna a un carácter.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-207">the pressed key does not map to a character.</span></span> <span data-ttu-id="cf1ab-208">Algunas teclas específicas nunca se consideran aceleradores, como Mayús.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-208">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="cf1ab-209">La tecla de escape se considera siempre un acelerador.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-209">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="cf1ab-210">Los eventos de teclas autorepetidos que se provocan al mantener presionada la tecla también desencadenan este evento.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-210">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="cf1ab-211">Puedes filtrarlos comprobando los argumentos del evento ' KeyEventLParam o PhysicalKeyStatus.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-211">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="cf1ab-212">En el modo de ventana, se llama a este controlador de eventos de forma sincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-212">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="cf1ab-213">Hasta que llames al controlador () en los argumentos del evento o se devuelva el controlador de eventos, el proceso del explorador se bloqueará y las llamadas COM salientes entre procesos generarán un error con RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-213">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="cf1ab-214">Sin embargo, todos los métodos de la API de WebView2 funcionarán.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-214">All WebView2 API methods will work, however.</span></span>

<span data-ttu-id="cf1ab-215">En el modo sin ventana, se llama al controlador de eventos de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-215">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="cf1ab-216">La entrada de datos adicionales no llegará al explorador hasta que el controlador de eventos devuelva o se llame a (), pero el proceso del explorador en sí no se bloqueará y las llamadas COM salientes funcionarán normalmente.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-216">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="cf1ab-217">Se recomienda que llame al controlador (TRUE) tan pronto como sepa que desea controlar la tecla de aceleración.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-217">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_webView->add_AcceleratorKeyPressed(
        Callback<IWebView2AcceleratorKeyPressedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2AcceleratorKeyPressedEventArgs* args)
                -> HRESULT {
                WEBVIEW2_KEY_EVENT_TYPE type;
                CHECK_FAILURE(args->get_KeyEventType(&type));
                // We only care about key down events.
                if (type == WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN ||
                    type == WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->Handle(TRUE));

                        // Filter out autorepeated keys.
                        WEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="cf1ab-218">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="cf1ab-218">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="cf1ab-219">Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-219">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="cf1ab-220">[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="cf1ab-220">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="cf1ab-221">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="cf1ab-221">WEBVIEW2_KEY_EVENT_TYPE</span></span> 

<span data-ttu-id="cf1ab-222">El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-222">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="cf1ab-223">[WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) enum</span><span class="sxs-lookup"><span data-stu-id="cf1ab-223">enum [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span></span>

 <span data-ttu-id="cf1ab-224">Los</span><span class="sxs-lookup"><span data-stu-id="cf1ab-224">Values</span></span>                         | <span data-ttu-id="cf1ab-225">Descripciones</span><span class="sxs-lookup"><span data-stu-id="cf1ab-225">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="cf1ab-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="cf1ab-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span></span>            | <span data-ttu-id="cf1ab-227">Corresponde a WM_KEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-227">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="cf1ab-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="cf1ab-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span></span>            | <span data-ttu-id="cf1ab-229">Corresponde a WM_KEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-229">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="cf1ab-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="cf1ab-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="cf1ab-231">Corresponde a WM_SYSKEYDOWN de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-231">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="cf1ab-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="cf1ab-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="cf1ab-233">Corresponde a WM_SYSKEYUP de mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-233">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="cf1ab-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="cf1ab-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="cf1ab-235">Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.</span><span class="sxs-lookup"><span data-stu-id="cf1ab-235">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="cf1ab-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="cf1ab-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span></span>

<span data-ttu-id="cf1ab-237">Para obtener más información, consulte la documentación de WM_KEYDOWN en[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="cf1ab-237">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>


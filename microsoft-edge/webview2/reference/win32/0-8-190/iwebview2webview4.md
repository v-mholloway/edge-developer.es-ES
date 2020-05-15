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
ms.openlocfilehash: 6ebed9e61bf7eda60e6e16b7a417306baa5d07bf
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655075"
---
# interfaz IWebView2WebView4 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

Funcionalidad adicional implementada por el objeto WebView principal.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[AddRemoteObject](#addremoteobject) | Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.
[RemoveRemoteObject](#removeremoteobject) | Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.
[OpenDevToolsWindow](#opendevtoolswindow) | Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Agregue un controlador de eventos para el evento AcceleratorKeyPressed.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.
[WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) | El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.
[WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status) | Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.

Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md). Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .

## Miembros

#### AddRemoteObject 

Agregue el objeto host proporcionado a la secuencia de comandos que se ejecuta en la vista Webcon el nombre especificado.

> [ADDREMOTEOBJECT](#addremoteobject)HRESULT público (LPCWSTR Name, Variant * Object)

Los objetos de host se exponen como proxies de objetos remotos a través de `window.chrome.webview.remoteObjects.<name>` . Los proxies de objetos remotos son promesas y se resolverán como un objeto que represente el objeto de host. La promesa se rechaza si la aplicación no ha agregado un objeto con el nombre. Cuando el código de JavaScript tiene acceso a una propiedad o método del objeto, se devuelve una promesa, que se resolverá con el valor devuelto por el host para la propiedad o el método, o se rechazará en caso de error, como no se trata de una propiedad o método en el objeto o los parámetros no son válidos. Por ejemplo, cuando el código de la aplicación hace lo siguiente: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 El código de JavaScript de WebView podrá acceder a appObject como sigue y, a continuación, a los atributos y métodos de appObject: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Tenga en cuenta que aunque se admiten tipos simples, IDispatch y matriz, no se admiten IUnknown genérico, VT_DECIMAL o VT_RECORD Variant. Los objetos remotos de JavaScript, como las funciones de devolución de llamada, se representan como una variante VT_DISPATCH con el objeto que implementa IDispatch. El método de devolución de llamada de JavaScript se puede invocar con DISPID_VALUE para el DispId. Las matrices anidadas se admiten hasta una profundidad de 3. No se admiten las matrices de los tipos de referencia. VT_EMPTY y VT_NULL se asignan a JavaScript como null. En JavaScript, los valores NULL y undefined se asignan a VT_EMPTY.

Además, todos los objetos remotos se exponen como `window.chrome.webview.remoteObjects.sync.<name>` . Aquí los objetos host se exponen como proxies de objetos remotos sincrónicos. No se trata de promesas ni llamadas a funciones o acceso a propiedad de forma sincrónica bloquear la ejecución de scripts en espera de comunicar el proceso cruzado para que se ejecute el código de host. Por consiguiente, esto puede dar lugar a problemas de confiabilidad y se recomienda usar la API asíncrona basada en Promise `window.chrome.webview.remoteObjects.<name>` descrita anteriormente.

Los proxies de objetos remotos sincrónicos y los proxies asincrónicos de objetos remotos pueden tener como proxy el mismo objeto remoto. Los cambios remotos realizados por un proxy se reflejarán en cualquier otro proxy de ese mismo objeto remoto, ya sean otros servidores proxy, sincrónicos o asíncronos.

Aunque JavaScript está bloqueado en una llamada sincrónica al código nativo, ese código nativo no puede devolver la llamada a JavaScript. Los intentos de hacerlo fallarán con HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Los proxies de objetos remotos son objetos proxy de JavaScript que interceptan todas las llamadas a propiedades get, Set Property y Method. Las propiedades o métodos que forman parte de la función o del prototipo de objeto se ejecutan de forma local. Además, cualquier propiedad o método de la matriz se `chrome.webview.remoteObjects.options.forceLocalProperties` ejecutará de forma local. De forma predeterminada, se incluyen métodos opcionales que tienen significado en JavaScript como `toJSON` y `Symbol.toPrimitive` . Puede agregar más a esta matriz, según sea necesario.

Hay un método que puede resultar `chrome.webview.remoteObjects.cleanupSome` más conveniente para la recolección de objetos remotos.

Los proxies de objetos remotos también tienen los siguientes métodos que se ejecutan de forma local:

* applyRemote, getRemote, setRemote: realizar una invocación de método, una propiedad get o un conjunto de propiedades en el objeto remoto. Puede usarlos para obligar a que un método o una propiedad se ejecuten de forma remota si hay una propiedad o un método local en conflicto. Por ejemplo, `proxy.toString()` ejecutará el método toString local en el objeto de proxy. Pero `proxy.applyRemote('toString')` se ejecuta `toString` en el objeto remoto a través del proxy.

* getLocal, setLocal: realizar obtención de propiedad o conjunto de propiedades de forma local. Puede usar estos métodos para forzar o establecer una propiedad en el proxy del objeto remoto, en lugar de hacerlo en el objeto remoto al que representa. Por ejemplo, `proxy.unknownProperty` obtendrá la propiedad nombrada `unknownProperty` desde el objeto remoto a través del proxy. Pero `proxy.getLocal('unknownProperty')` obtendrá el valor de la propiedad `unknownProperty` en el propio objeto proxy.

* sincronizar: los proxies de objetos remotos asincrónicos exponen un método de sincronización que devuelve una promesa de un proxy de objetos remotos sincrónico para el mismo objeto remoto. Por ejemplo, `chrome.webview.remoteObjects.sample.methodCall()` devuelve un proxy asincrónico de objeto remoto. Puede usar el `sync` método para obtener un proxy de objetos remotos sincrónico en su lugar: `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: los proxies de objetos remotos sincrónicos exponen un método Async que bloquea y devuelve un proxy de objetos remotos asincrónicos para el mismo objeto remoto. Por ejemplo, `chrome.webview.remoteObjects.sync.sample.methodCall()` devuelve un proxy de objeto remoto sincrónico. Se llama al `async` método de este bloque y, a continuación, se devuelve un proxy de objeto remoto asincrónico para el mismo objeto remoto: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* después: los proxies de objetos remotos asincrónicos tienen un método then. Esto permite que sean esperados. `then` devolverá una promesa que se resolverá con una representación del objeto remoto. Si el proxy representa un literal de JavaScript, se devuelve una copia de forma local. Si el proxy representa una función, se devuelve un proxy que no es de espera. Si el proxy representa un objeto de JavaScript con una combinación de propiedades literales y propiedades de función, se devuelve una copia del objeto con algunas propiedades como proxy de objetos remotos.

Todas las demás invocaciones a propiedades y métodos (excepto los métodos anteriores de proxy de objeto remoto, la lista de forceLocalProperties y las propiedades de los prototipos de funciones y objetos) se ejecutan de forma remota. Los proxies de objetos remotos asincrónicos devuelven una promesa que representa la finalización asincrónica de la invocación remota del método u obtiene la propiedad. La función Promise se resuelve después de que las operaciones remotas se completen y las promesas se resuelven en el valor resultante de la operación. Los proxy de objetos remotos sincrónicos funcionan de manera similar pero bloquean la ejecución remota y esperan a que se complete la operación remota.

Establecer una propiedad en un proxy de objetos remotos asincrónicos funciona de forma ligeramente distinta. El conjunto devolverá inmediatamente y el valor devuelto es el valor que se establecerá. Este es un requisito del objeto proxy de JavaScript. Si necesita esperar de forma asincrónica para que se complete el conjunto de propiedades, use el método setRemote que devuelve una promesa según se describe anteriormente. La propiedad sincrónico del conjunto de propiedades de objeto se bloquea de forma sincrónica hasta que se establece la propiedad.

Por ejemplo, supongamos que tiene un objeto COM con la siguiente interfaz

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

 Podemos añadir una instancia de esta interfaz a nuestro JavaScript con `AddRemoteObject` . En este caso, lo hemos denominado `sample` :

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

 A continuación, en el documento HTML podemos usar este objeto COM mediante `chrome.webview.remoteObjects.sample` :

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

#### RemoveRemoteObject 

Quite el objeto host especificado por el nombre para que ya no se pueda tener acceso al mismo desde el código de JavaScript de la vista.

> [REMOVEREMOTEOBJECT](#removeremoteobject)HRESULT público (LPCWSTR Name)

Aunque se denegarán nuevos intentos de acceso, si el código de JavaScript ya ha obtenido el objeto, el código de JavaScript seguirá teniendo acceso a ese objeto. Llamar a este método para un nombre que ya se ha quitado o no se ha agregado nunca producirá un error.

#### OpenDevToolsWindow 

Abre la ventana DevTools para el documento actual en la vista de vistas en WebView.

> [OPENDEVTOOLSWINDOW](#opendevtoolswindow)HRESULT público ()

No hace nada si se llama cuando la ventana de DevTools ya está abierta

#### add_AcceleratorKeyPressed 

Agregue un controlador de eventos para el evento AcceleratorKeyPressed.

> [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)de HRESULT público ([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) * EventHandler, EventRegistrationToken * token)

AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa. Una clave se considera un acelerador si:

1. La tecla Ctrl o Alt se está retenida actualmente, o bien

1. la tecla presionada no se asigna a un carácter. Algunas teclas específicas nunca se consideran aceleradores, como Mayús. La tecla de escape se considera siempre un acelerador.

Los eventos de teclas autorepetidos que se provocan al mantener presionada la tecla también desencadenan este evento. Puedes filtrarlos comprobando los argumentos del evento ' KeyEventLParam o PhysicalKeyStatus.

En el modo de ventana, se llama a este controlador de eventos de forma sincrónica. Hasta que llames al controlador () en los argumentos del evento o se devuelva el controlador de eventos, el proceso del explorador se bloqueará y las llamadas COM salientes entre procesos generarán un error con RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Sin embargo, todos los métodos de la API de WebView2 funcionarán.

En el modo sin ventana, se llama al controlador de eventos de forma asincrónica. La entrada de datos adicionales no llegará al explorador hasta que el controlador de eventos devuelva o se llame a (), pero el proceso del explorador en sí no se bloqueará y las llamadas COM salientes funcionarán normalmente.

Se recomienda que llame al controlador (TRUE) tan pronto como sepa que desea controlar la tecla de aceleración.

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

#### remove_AcceleratorKeyPressed 

Quitar un controlador de eventos agregado previamente con add_AcceleratorKeyPressed.

> [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)de HRESULT público (token EventRegistrationToken)

#### WEBVIEW2_KEY_EVENT_TYPE 

El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.

> [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) enum

 Los                         | Descripciones
--------------------------------|---------------------------------------------
WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN            | Corresponde a WM_KEYDOWN de mensaje de ventana.
WEBVIEW2_KEY_EVENT_TYPE_KEY_UP            | Corresponde a WM_KEYUP de mensaje de ventana.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN            | Corresponde a WM_SYSKEYDOWN de mensaje de ventana.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP            | Corresponde a WM_SYSKEYUP de mensaje de ventana.

#### WEBVIEW2_PHYSICAL_KEY_STATUS 

Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.

> typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)

Para obtener más información, consulte la documentación de WM_KEYDOWN en[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)


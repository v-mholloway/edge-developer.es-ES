---
description: Use el motor de JavaScript de Chakra basado en estándares para agregar capacidades de scripting a su aplicación para Windows.
title: Hospedar el Runtime de JavaScript | Microsoft docs
ms.custom: ''
ms.date: 01/15/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 30ec744e-57cc-4ef5-8fe1-d2c27b946548
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9077284d96ff0d9ae22e152329efe9304081ae39
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573550"
---
# Hospedaje de JavaScript en tiempo de ejecución
Las API de JavaScript Runtime (JsRT) proporcionan una manera de usar aplicaciones de escritorio, de la tienda Windows y del servidor que se ejecutan en el sistema operativo Windows para agregar capacidades de scripting a la aplicación con el motor de JavaScript de Chakra basado en estándares que también usa Microsoft Edge e Internet Explorer. Estas API están disponibles en Windows 10 y cualquier versión del sistema operativo Windows que tenga Internet Explorer versión 11,0 instalado en el equipo. Para obtener más información, consulta [referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md). Para obtener información sobre el uso de JsRT en aplicaciones de la tienda Windows, consulta [JsRT y la plataforma universal de Windows](#Windows).  
  
> [!NOTE]
>  En esta documentación se supone que está trabajando general con el lenguaje JavaScript.  
  
## Conceptos  
 Comprender cómo hospedar el motor de JavaScript con las API de JsRT depende de dos conceptos clave: runtimes y contextos de ejecución.  
  
 Un *Runtime* representa un entorno de ejecución de JavaScript completo. Cada Runtime que se crea tiene su propia pila aislada de recolección de elementos no utilizados y, de forma predeterminada, su propio subproceso del compilador Just-in-Time (JIT) y subproceso de recopilación de elementos no utilizados (GC). Un *contexto de ejecución* representa un entorno de JavaScript que tiene su propio objeto global de JavaScript distinto del resto de contextos de ejecución. Un tiempo de ejecución puede contener varios contextos de ejecución y, en esos casos, todos los contextos de ejecución comparten el compilador JIT y el subproceso GC asociados con el motor en tiempo de ejecución.  
  
 Los Runtime representan un único subproceso de ejecución. Solo puede haber un Runtime activo en un subproceso determinado a la vez, y un tiempo de ejecución solo puede estar activo en un subproceso a la vez. Los Runtimes tienen un subproceso de alquiler, por lo que un Runtime que no está activo en ese momento en un subproceso (es decir, no se ejecuta ningún código de JavaScript o responde a las llamadas del host) se puede usar en cualquier subproceso que aún no tenga un Runtime activo en él.  
  
 Los contextos de ejecución están vinculados a un Runtime en particular y ejecutan código dentro de ese Runtime. A diferencia de los motores de tiempo de ejecución, los contextos de ejecución múltiple pueden activarse en un subproceso al mismo tiempo. Por lo tanto, un host puede hacer una llamada en un contexto de ejecución, ese contexto de ejecución puede devolver la llamada al host y el anfitrión puede hacer una llamada en un contexto de ejecución diferente.  
  
 ![Varios contextos de ejecución](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting")  
  
 En la práctica, a menos que un host necesite ejecutar código en entornos separados, se puede usar un solo contexto de ejecución. De forma similar, a menos que un host necesite ejecutar varios fragmentos de código de forma simultánea, un único tiempo de ejecución es suficiente.  
  
## Administración de memoria  
 JavaScript es un lenguaje recolectado de elementos no usados y, por lo tanto, hay varias consideraciones que deben tenerse en cuenta al trabajar con las API de JsRT desde otro idioma.  
  
 La principal consideración es que el recolector de elementos no utilizados de JavaScript solo puede ver referencias a valores en dos lugares: el montón de su tiempo de ejecución y la pila. Por lo tanto, el recolector de elementos no utilizados siempre verá una referencia a un valor de JavaScript que se almacena dentro de otro valor de JavaScript o en una variable local de la pila. Pero las referencias almacenadas en otras ubicaciones, como montones administradas por el host o el sistema, no se verán en el recolector de elementos no utilizados y pueden provocar una recolección prematura de valores que el host aún usa.  
  
> [!IMPORTANT]
>  Algunos compiladores de lenguaje (como el compilador C++ de Visual Studio) optimizarán las variables locales siempre que sea posible. Se debe tener cuidado para asegurarse de que las variables locales que hacen referencia a valores de JavaScript estén en la pila si se espera que mantengan esos valores activos.  
  
 Si una referencia a un valor de JavaScript se va a almacenar en una ubicación que no es visible para el recolector de elementos no utilizados, el host debe agregar y quitar las referencias de forma manual con las API de JsRT.  
  
## Control de excepciones  
 Cuando se produce una excepción de JavaScript durante la ejecución del script, el Runtime que lo contiene se coloca en un estado de excepción. Mientras se encuentra en estado de excepción, no se puede ejecutar ningún código y todas las llamadas a través de la API generarán un error con el código de error `JsErrorInExceptionState` hasta que el host recupere y borre la excepción con la `JsGetAndClearException` API. Si el host devuelve una devolución de llamada de JavaScript sin borrar el motor en tiempo de ejecución de un estado de excepción, la excepción de JavaScript se volverá a iniciar tan pronto como el control vuelva al motor de JavaScript. Esto también permite que las devoluciones de llamada de hospedaje "inicien" una excepción de JavaScript al establecer el Runtime en un estado de excepción y, a continuación, devolver desde una devolución de llamada de host.  
  
 Un host no puede permitir que sus propias excepciones internas se propaguen a través de una devolución de llamada de host: cualquier método de devolución de llamada debe detectar todas las excepciones de host antes de devolver el control al motor en tiempo de ejecución.  
  
## Uso de recursos en tiempo de ejecución  
 Las API de JsRT exponen una serie de maneras de supervisar y modificar la manera en que los Runtime usan los recursos. Por lo general, se dividen en las siguientes categorías:  
  
-   **Uso de subprocesos**. De forma predeterminada, cada Runtime creará un subproceso de compilador JIT dedicado y un subproceso GC dedicado que prestan servicio a ese motor en tiempo de ejecución. Si se crea un Runtime con la `JsRuntimeAttributeDisableBackgroundWork` marca, el trabajo JIT y el GC se realizará en el propio subproceso en tiempo de ejecución en lugar de subprocesos de fondo independientes para cada uno de ellos. Un host puede proporcionar también una devolución de llamada del servicio de subprocesos a la `JsCreateRuntime` llamada, lo que permitirá al host programar el trabajo JIT y el catálogo global de la manera más adecuada.  
  
-   **Uso**de la memoria. Hay varias maneras de supervisar y modificar el uso de memoria de un motor en tiempo de ejecución. Si el tiempo de ejecución se va a ejecutar durante mucho tiempo, el host puede especificar la `JsRuntimeAttributeEnableIdleProcessing` marca al crear el Runtime y, después, llamar `JsIdle` cuando el host se encuentra en estado de inactividad. Esto permite que el motor postergue la limpieza de la memoria y el trabajo de contabilidad hasta el tiempo de inactividad.  
  
     El host puede supervisar las recolecciones de elementos no utilizados llamando a `JsSetRuntimeBeforeCollectCallback` . También puede supervisar las asignaciones realizadas por el montón llamando a `JsSetRuntimeMemoryAllocationCallback` . Ten en cuenta que esta API no vuelve a llamar en todas las asignaciones de JavaScript, solo cuando el montón del Runtime necesita más espacio del que asignar. La devolución de llamada de asignación de memoria puede denegar la solicitud, lo que desencadenará una recolección de elementos no utilizados y, si no hay memoria disponible, se producirá un error de memoria insuficiente en el tiempo de ejecución.  
  
     El anfitrión también puede llamar `JsSetRuntimeMemoryLimit` para establecer un límite para la cantidad de memoria que puede usar un tiempo de ejecución. Cuando un tiempo de ejecución alcanza un límite, desencadena una recolección de elementos no utilizados y, si no hay memoria disponible, el motor en tiempo de ejecución generará un error de memoria insuficiente.  
  
-   **Interrupción y evaluación de la secuencia de comandos**. El anfitrión puede llamar `JsDisableRuntimeExecution` para finalizar la ejecución en un tiempo de ejecución. Esta llamada se puede realizar en cualquier momento y desde cualquier conversación. Debido a que la terminación del script depende de alcanzar puntos de protección insertados en el código, es posible que un script no finalice en el momento exacto, pero lo hará muy pronto. De forma predeterminada, los puntos de protección de terminación se colocan con cautela en el código generado y es posible que no cubran todas las situaciones, como un bucle infinito. Crear el motor en tiempo de ejecución con la `JsRuntimeAttributeAllowScriptInterrupt` marca hace que el motor en tiempo de ejecución Inserte comprobaciones adicionales para los bucles infinitos, a menudo a costa de una pequeña sobrecarga de rendimiento.  
  
     Si un host desea impedir la generación de código nativo mediante el compilador JIT, puede especificar la `JsRuntimeAttributeDisableNativeCodeGeneration` marca. Un host también puede impedir que se ejecuten los scripts de forma dinámica al especificar la `JsRuntimeAttributeDisableEval` marca.  
  
## Depuración y generación de perfiles  
 Las API de JsRT admiten la depuración y la generación de perfiles mediante la tecnología Active Scripting.  
  
 A partir de Windows 10, el motor de JavaScript de Chakra es compatible con el motor heredado de Internet Explorer (MSHTML) y el nuevo motor de Microsoft Edge (EdgeHTML) y puede dirigirse en JsRT (vea [dirigirse a Microsoft Edge frente a motores heredados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md) para obtener más información). La depuración de un script en Visual Studio funciona de manera diferente entre el motor heredado y el motor de Microsoft Edge. Con el motor heredado, el hospedador debe proporcionar un puntero de [interfaz IDebugApplication](/scripting/winscript/reference/idebugapplication-interface) , que se puede obtener desde una instancia de la [interfaz IProcessDebugManager](/scripting/winscript/reference/iprocessdebugmanager-interface) . Con el motor Microsoft Edge, `IDebugApplication` está obsoleto y el motor de Chakra habilita las capacidades de depuración nativa y de script a través del depurador de Visual Studio sin requerir una implementación del `IDebugApplication` usuario.  
  
 Para que los scripts en un contexto de ejecución se depuren, el motor de Chakra debe cambiar al uso de métodos de ejecución de código menos eficientes. Por lo tanto, el código depurable se ejecuta más lentamente que el código no depurable. Como resultado, con el motor heredado, un host puede elegir iniciar la depuración en un contexto de ejecución desde el principio proporcionando el `IDebugApplication` puntero hacia arriba `JsCreateContext` o puede esperar hasta que se necesite la depuración y, a continuación, llamar `JsStartDebugging` . Con el motor de Microsoft Edge, `JsCreateContext` ya no se usa un `IDebugApplication` parámetro y, como resultado, solo se podrá depurar el script después de la `JsStartDebugging` llamada. Al depurar con Visual Studio, la opción de depurador "script" debe estar habilitada.  
  
 El código de JavaScript en un contexto de ejecución se puede mostrar de una de dos maneras. El generador de perfiles de la línea de comandos de Visual Studio (VSPerf. exe) se puede usar en Windows 8,1 y versiones posteriores con el modificador/JS para generar un informe destinado al código de JavaScript que se ejecuta en la aplicación. O bien, el anfitrión puede llamar directamente `JsStartProfiling` y `JsStopProfiling` proporcionar una devolución de llamada para realizar la generación de perfiles. El host también puede examinar el estado de la pila de recolección de elementos no utilizados mediante una llamada `JsEnumerateHeap` . La generación de perfiles en JsRT funciona de la misma manera entre el motor heredado y el motor Microsoft Edge. Sin embargo, las API de generación `JsStartProfiling` de perfiles de JsRT (,, `JsStopProfiling` `JsEnumerateHeap` , y `JsIsEnumeratingHeap` ) no están disponibles para las aplicaciones universales de Windows.  
  
<a name="Windows"></a>   
## JsRT y la plataforma universal de Windows  

Puedes usar las API de JsRT para agregar capacidades de scripting a una aplicación universal de Windows. Una aplicación universal de Windows que use las API de JsRT necesitará dirigirse a las API de Microsoft Edge JSRT, que a su vez tienen como destino el motor de Chakra perimetral. Para obtener más información, consulta [apuntar a Microsoft Edge frente a motores heredados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md). La API completa de JsRT está disponible para las aplicaciones universales de Windows, excepto para la generación de perfiles y la compatibilidad de la enumeración de montones ( `JsStartProfiling` ,, `JsStopProfiling` `JsEnumerateHeap` y `JsIsEnumeratingHeap` no son compatibles).  
  
JsRT también permite que los scripts accedan de forma nativa a cualquier API de la [plataforma universal de Windows (UWP)](https://msdn.microsoft.com/library/windows/apps/br211377.aspx) después de exponer el espacio de nombres de la API a través de la API de Microsoft Edge JsRT `JsProjectWinRTNamespace` . Aunque las aplicaciones universales para Windows no necesitan ninguna configuración, además de proyectar espacios de nombres necesarios, en una aplicación de Windows clásica (Win32), debe habilitarse un mecanismo de bombeo delegado inicializado por COM `JsSetProjectionEnqueueCallback` para habilitar eventos y API asincrónicas. En el siguiente ejemplo de Win32 se usan las API asincrónicas de UWP para crear un cliente http y obtener el contenido de un URI:  
  
```cpp  
typedef struct _jsCall {  
    JsProjectionCallback jsCallback;  
    JsProjectionCallbackContext jsContext;  
    HANDLE event;  
} jsCall;  
  
// Set up delegated pumping mechanism; not necessary in UWP applications.  
jsCall outstandingCall = {};  
CoInitializeEx(nullptr, COINIT_MULTITHREADED);  
JsSetProjectionEnqueueCallback([](JsProjectionCallback jsCallback,   
JsProjectionCallbackContext jsContext, void *callbackState) {  
    jsCall* call = (jsCall*)callbackState;  
    call->jsCallback = jsCallback;  
    call->jsContext = jsContext;  
    SetEvent(call->event);  
    },  
&outstandingCall);  
HANDLE event = CreateEventEx(NULL, NULL, CREATE_EVENT_MANUAL_RESET, EVENT_ALL_ACCESS);  
outstandingCall.event = event;  
  
// Project necessary namespaces.  
JsProjectWinRTNamespace(L"Windows.Foundation");  
JsProjectWinRTNamespace(L"Windows.Web");  
  
// Get content from an Uri.  
JsRunScript(L"var uri = new Windows.Foundation.Uri(\"http://somedatasource.com\"); " \  
    L"var httpClient = new Windows.Web.Http.HttpClient();" \  
    L"httpClient.getStringAsync(uri).done(function (content) { " \  
    L"    // do something with the string content " \    
    L"}, onError); " \  
    L"function onError(reason) { " \  
    L"    // error handling " \        
    L"}",   
    currentSourceContext, L"", &result);  
  
// Wait for async call to come in and then execute; not necessary in UWP applications.  
WaitForSingleObjectEx(outstandingCall.event, 10000, FALSE) == WAIT_OBJECT_0;  
outstandingCall.jsCallback(outstandingCall.jsContext);  
  
```  
  
## Consulta también  
 [Aplicación de ejemplo en tiempo de ejecución de JavaScript](https://go.microsoft.com/fwlink/p/?LinkID=306674&clcid=0x409)   
 [Referencia (tiempo de ejecución de JavaScript)](../chakra-hosting/reference-javascript-runtime.md)   
 [Hospedaje en tiempo de ejecución de JavaScript](../javascript-runtime-hosting.md)  
 
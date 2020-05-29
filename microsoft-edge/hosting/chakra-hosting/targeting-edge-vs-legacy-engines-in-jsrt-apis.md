---
description: 'Más información sobre cómo destinar los diferentes motores de JavaScript de Windows 10. '
title: Dirigirse a Microsoft Edge frente a motores heredados en API de JsRT | Microsoft docs
ms.custom: ''
ms.date: 03/05/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ed0dc8c67b8189a7433d52185aa995997edb70a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573386"
---
# <span data-ttu-id="5cd33-103">Dirigirse a Microsoft Edge frente a motores heredados en las API de JsRT</span><span class="sxs-lookup"><span data-stu-id="5cd33-103">Targeting Microsoft Edge vs. Legacy Engines in JsRT APIs</span></span>

<span data-ttu-id="5cd33-104">Windows 10 es compatible con dos motores de JavaScript diferentes:</span><span class="sxs-lookup"><span data-stu-id="5cd33-104">Windows 10 supports two different JavaScript engines:</span></span>

-   <span data-ttu-id="5cd33-105">El antiguo motor de chakra (también denominado *motor heredado* o jscript9. dll que se incluye a continuación), que se envía y es compatible con Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="5cd33-105">The old Chakra engine (also called the *legacy engine* or jscript9.dll below) that ships with and supports Internet Explorer 11.</span></span> <span data-ttu-id="5cd33-106">Este motor se congela en el tiempo y permanecerá de forma fundamentalmente inalterado desde la versión de Windows 8.1/IE11.</span><span class="sxs-lookup"><span data-stu-id="5cd33-106">This engine is frozen in time and will remain fundamentally unchanged from Win8.1/IE11 release.</span></span>  
  
-   <span data-ttu-id="5cd33-107">El nuevo motor de chakra (también denominado el *motor de Edge* o Chakra. dll que se incluye a continuación), que se envía con el nuevo explorador en Windows 10, Microsoft Edge y es compatible con él.</span><span class="sxs-lookup"><span data-stu-id="5cd33-107">The new Chakra engine (also called the *Edge engine* or chakra.dll below) that ships with and supports the new browser in Windows 10, Microsoft Edge.</span></span> <span data-ttu-id="5cd33-108">Este motor se actualizará continuamente y será compatible con un motor de [borde](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) "vivo".</span><span class="sxs-lookup"><span data-stu-id="5cd33-108">This engine will be continually updated and will support a "living" [Edge](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) engine.</span></span> <span data-ttu-id="5cd33-109">Un motor de la vida de Microsoft Edge implica que, a diferencia del motor heredado, el motor de Microsoft Edge no transcurrirá ninguna forma de funcionalidad de scripting de versiones a participar.</span><span class="sxs-lookup"><span data-stu-id="5cd33-109">A living Microsoft Edge engine implies that unlike the legacy engine, the Microsoft Edge engine would not carry forward any form of versioning script functionality to opt into.</span></span>  
  
 <span data-ttu-id="5cd33-110">Al crear una aplicación con la API de hospedaje en tiempo de ejecución de JavaScript (JsRT), puede elegir destinar el motor heredado o Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5cd33-110">When creating an app using the JavaScript Runtime Hosting (JsRT) API, you can choose to target either the legacy or the Microsoft Edge engine.</span></span>  
  
-   <span data-ttu-id="5cd33-111">Si necesita enfatizar la compatibilidad con versiones anteriores de las aplicaciones existentes, diríjase al motor heredado.</span><span class="sxs-lookup"><span data-stu-id="5cd33-111">If you need to emphasize backward compatibility of your existing applications, target the legacy engine.</span></span>  
  
-   <span data-ttu-id="5cd33-112">Si desea que la aplicación vaya adelante y admita nuevas características de JavaScript a medida que se publican (por ejemplo, ECMAScript 6), destine el motor Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5cd33-112">If you want your app to be forward looking and support new JavaScript features as they are released (for example, ECMAScript 6), target the Microsoft Edge engine.</span></span>  
  
 <span data-ttu-id="5cd33-113">En este tema se incluyen detalles que describen cómo destinar los distintos motores.</span><span class="sxs-lookup"><span data-stu-id="5cd33-113">This topic includes details that describe how to target the different engines.</span></span>  
  
## <span data-ttu-id="5cd33-114">Apuntar a tu versión preferida</span><span class="sxs-lookup"><span data-stu-id="5cd33-114">Target your preferred version</span></span>  
 <span data-ttu-id="5cd33-115">Al crear una aplicación, puede seleccionar la versión de JsRT que admita el motor Microsoft Edge o el motor heredado.</span><span class="sxs-lookup"><span data-stu-id="5cd33-115">When creating an app, you can select the version of the JsRT that supports either the Microsoft Edge engine or the legacy engine.</span></span> <span data-ttu-id="5cd33-116">Puede elegir la versión de JsRT según las pautas anteriores.</span><span class="sxs-lookup"><span data-stu-id="5cd33-116">You can choose the JsRT version based on the guidelines above.</span></span> <span data-ttu-id="5cd33-117">Para dar cabida a estas distinciones, se han realizado los cambios siguientes, `JsCreateRuntime` `JsCreateContext` y `JsStartDebugging` .</span><span class="sxs-lookup"><span data-stu-id="5cd33-117">To accommodate these distinctions, the following changes have been made to `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging`.</span></span>  
  
 <span data-ttu-id="5cd33-118">Para `JsCreateRuntime` :</span><span class="sxs-lookup"><span data-stu-id="5cd33-118">For `JsCreateRuntime`:</span></span>  
  
-   <span data-ttu-id="5cd33-119">Cuando el destino es el motor heredado, el valor de la `JsRuntimeVersionEdge` enumeración está obsoleto y un mensaje sugerirá usar el `JsRuntimeVersionInternetExplorer11` valor en su lugar.</span><span class="sxs-lookup"><span data-stu-id="5cd33-119">When targeting the legacy engine, the `JsRuntimeVersionEdge` enumeration value is deprecated, and a message will suggest using the `JsRuntimeVersionInternetExplorer11` value instead.</span></span>  
  
-   <span data-ttu-id="5cd33-120">Cuando el destino es el motor Microsoft Edge, el parámetro version se omite de la `JsCreateRuntime` función.</span><span class="sxs-lookup"><span data-stu-id="5cd33-120">When targeting the Microsoft Edge engine, the version parameter is omitted from the `JsCreateRuntime` function.</span></span>  
  
    ```cpp  
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
    ```  
  
 <span data-ttu-id="5cd33-121">Para `JsCreateContext` y `JsStartDebugging` :</span><span class="sxs-lookup"><span data-stu-id="5cd33-121">For `JsCreateContext` and `JsStartDebugging`:</span></span>  
  
-   <span data-ttu-id="5cd33-122">Cuando el destino es el motor heredado, la `IDebugApplication` interfaz se usa para proporcionar sus propios métodos de depuración no remotos.</span><span class="sxs-lookup"><span data-stu-id="5cd33-122">When targeting the legacy engine, the `IDebugApplication` interface is used to supply your own non-remote debugging methods.</span></span> <span data-ttu-id="5cd33-123">Para fines de depuración, `JsCreateContext` y `JsStartDebugging` las funciones toman `IDebugApplication` como parámetro.</span><span class="sxs-lookup"><span data-stu-id="5cd33-123">For debugging purposes, `JsCreateContext` and `JsStartDebugging` functions take `IDebugApplication` as parameter.</span></span>  
  
-   <span data-ttu-id="5cd33-124">Cuando el destino es el motor Microsoft Edge, la `IDebugApplication` interfaz ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="5cd33-124">When targeting the Microsoft Edge engine, the `IDebugApplication` interface is deprecated.</span></span> <span data-ttu-id="5cd33-125">El motor de Chakra permite la capacidad de depuración nativa y de script con el depurador de Visual Studio sin requerir una implementación de `IDebugApplication` from.</span><span class="sxs-lookup"><span data-stu-id="5cd33-125">The Chakra engine enables native and script debugging capability with Visual Studio debugger without requiring an implementation of `IDebugApplication` from user.</span></span> <span data-ttu-id="5cd33-126">La interfaz ya no es un parámetro `JsCreateContext` y `JsStartDebugging` , como resultado.</span><span class="sxs-lookup"><span data-stu-id="5cd33-126">The interface is no longer a parameter for `JsCreateContext` and `JsStartDebugging` as a result.</span></span>  
  
 <span data-ttu-id="5cd33-127">Las firmas de las API anteriores en el motor heredado son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="5cd33-127">The signatures for the preceding APIs in the legacy engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);  
```  
  
 <span data-ttu-id="5cd33-128">Las firmas de las API anteriores en el motor de Microsoft Edge son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="5cd33-128">The signatures for the preceding APIs in the Microsoft Edge engine are as follows:</span></span>  
  
```cpp  
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);  
  
JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);  
  
JsErrorCode JsStartDebugging();  
```  
  
## <span data-ttu-id="5cd33-129">Compilar la versión preferida con Visual C++</span><span class="sxs-lookup"><span data-stu-id="5cd33-129">Compile for your preferred version using Visual C++</span></span>  
 <span data-ttu-id="5cd33-130">Cuando use Visual C++, importe la API de JsRT incluyendo el encabezado JsRT. h y asegúrese de que JsRT. lib está incluido en la lista de archivos de entrada del vinculador:</span><span class="sxs-lookup"><span data-stu-id="5cd33-130">When using Visual C++, import the JsRT API by including the jsrt.h header, and ensure that jsrt.lib is included in your linker input files list:</span></span>  
  
```cpp  
#include <jsrt.h>  
```  
  
 ![Agregar jsrt. lib como un archivo de entrada del vinculador](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  
  
 <span data-ttu-id="5cd33-132">Si desea especificar los archivos binarios del motor Microsoft Edge, debe definir la macro `USE_EDGEMODE_JSRT` antes de incluir jsrt. h y, en lugar de vincular con jsrt. lib, debe vincular a chakrart. lib:</span><span class="sxs-lookup"><span data-stu-id="5cd33-132">If you want to target the Microsoft Edge engine binaries, you need to define the macro `USE_EDGEMODE_JSRT` before including jsrt.h, and instead of linking against jsrt.lib, you should link against chakrart.lib:</span></span>  
  
```cpp  
#define USE_EDGEMODE_JSRT  
#include <jsrt.h>  
```  
  
 ![Agregar chakrart. lib como un archivo de entrada del vinculador](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  
  
 <span data-ttu-id="5cd33-134">Si está empezando con una nueva aplicación, ya está listo para empezar a escribir código en la API de JsRT.</span><span class="sxs-lookup"><span data-stu-id="5cd33-134">If you're starting with a new application, you are now ready to start writing code against the JsRT API.</span></span>  
  
## <span data-ttu-id="5cd33-135">Compilar la versión preferida con .NET</span><span class="sxs-lookup"><span data-stu-id="5cd33-135">Compile for your preferred version using .NET</span></span>  
 <span data-ttu-id="5cd33-136">Si usa .NET y P/Invoke, debe cambiar las declaraciones de la API de JsRT [DllImport] para importar Chakra. dll en lugar de jscript9. dll.</span><span class="sxs-lookup"><span data-stu-id="5cd33-136">If you're using .NET and P/Invoke, you must change your JsRT API [DllImport] declarations to import chakra.dll instead of jscript9.dll.</span></span> <span data-ttu-id="5cd33-137">Además, cambie la definición de `JsCreateRuntime` para quitar el `JsRuntimeVersion` parámetro y la definición de `JsCreateContext` y `JsStartDebugging` para quitar el `IDebugApplication` parámetro.</span><span class="sxs-lookup"><span data-stu-id="5cd33-137">In addition, change the definition of `JsCreateRuntime` to remove the `JsRuntimeVersion` parameter and the definition of `JsCreateContext` and `JsStartDebugging` to remove the `IDebugApplication` parameter.</span></span>  
  
 <span data-ttu-id="5cd33-138">Para el motor heredado, use el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="5cd33-138">For the legacy engine, use the following code.</span></span>  
  
```c#  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsRuntimeVersion version,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    IDebugApplication debugApplication,  
    out JsContextRef newContext  
);   
  
[DllImport("jscript9.dll")]  
public static extern JsErrorCode JsStartDebugging(  
    IDebugApplication debugApplication,  
);  
```  
  
 <span data-ttu-id="5cd33-139">Para el motor Microsoft Edge, use el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="5cd33-139">For the Microsoft Edge engine, use the following code.</span></span>  
  
```c#  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateRuntime(  
    JsRuntimeAttributes attributes,  
    JsThreadServiceCallback callback,  
    out JsRuntimeSafeHandle runtime  
);  
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsCreateContext(  
    JsRuntimeSafeHandle runtime,  
    out JsContextRef newContext  
);   
  
[DllImport("chakra.dll")]  
public static extern JsErrorCode JsStartDebugging();  
```  
  
> [!CAUTION]
>  <span data-ttu-id="5cd33-140">Si va a calcular manualmente el valor del puntero de función (por ejemplo, a través de LoadLibrary o GetProcAddress), es muy importante que no mezcle las declaraciones del método o, de lo contrario, desequilibrará la pila, lo que provocará un comportamiento imprevisible, como por ejemplo, que se bloquee la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5cd33-140">If you are manually marshaling the function pointer (such as via LoadLibrary/GetProcAddress), it is critical that you do not mix the declarations of the method, or else you will unbalance the stack, which will result in unpredictable behavior such as causing your app to crash.</span></span> <span data-ttu-id="5cd33-141">El mismo problema ocurrirá si realiza una búsqueda y reemplazo global de instancias de jscript9. dll en el código de importación, porque perderá el `version` parámetro que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="5cd33-141">The same problem will occur if you perform a global search-and-replace of instances of jscript9.dll in your import code, because you'll miss the `version` parameter being dropped.</span></span>  
  
## <span data-ttu-id="5cd33-142">Resumen</span><span class="sxs-lookup"><span data-stu-id="5cd33-142">Summary</span></span>  
 <span data-ttu-id="5cd33-143">En Windows 10, las API de hospedaje en tiempo de ejecución de JavaScript se dividen en dos.</span><span class="sxs-lookup"><span data-stu-id="5cd33-143">In Windows 10, the JavaScript Runtime Hosting APIs are splitting into two.</span></span> <span data-ttu-id="5cd33-144">Estas API ahora son compatibles con un motor "vivo" de Microsoft Edge, cuyas capacidades de idioma se alinearán con el motor "viviendo" de Microsoft Edge en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5cd33-144">These APIs now support a "living" Microsoft Edge engine, whose language capabilities will be aligned with the "living" Microsoft Edge engine in the Microsoft Edge.</span></span> <span data-ttu-id="5cd33-145">Puede aprovechar estas capacidades de su escritorio o aplicaciones de la tienda para crear nuevas y emocionantes maneras de ampliar su aplicación y aprovechar habilidades web modernas en su base de código existente.</span><span class="sxs-lookup"><span data-stu-id="5cd33-145">You can leverage these capabilities from your desktop or Store apps to create new and exciting ways to extend your application and to leverage modern Web skills in your existing code base.</span></span> <span data-ttu-id="5cd33-146">Sin embargo, dado que existen diferencias sutiles entre las versiones anteriores, debe tener en cuenta los siguientes puntos cuando dirigen el procesador perimetral o heredado.</span><span class="sxs-lookup"><span data-stu-id="5cd33-146">However, because there are subtle differences between previous versions, you must be aware of the following points when targeting the Edge or legacy engine.</span></span>  
  
-   <span data-ttu-id="5cd33-147">La aplicación solo puede admitir una versión de JsRT por proceso.</span><span class="sxs-lookup"><span data-stu-id="5cd33-147">Your app can support only one version of JsRT per process.</span></span>  
  
     <span data-ttu-id="5cd33-148">Por ejemplo, no puede crear un tiempo de ejecución de motor de Microsoft Edge y, a continuación, un Runtime de motor heredado y esperar que se ejecute correctamente en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="5cd33-148">For example, you can't create a Microsoft Edge engine runtime and then a legacy engine runtime and expect them to run correctly in the same process.</span></span> <span data-ttu-id="5cd33-149">Esto no es compatible y puede dar lugar a un comportamiento no documentado, como el error de carga de la segunda DLL.</span><span class="sxs-lookup"><span data-stu-id="5cd33-149">This is unsupported and may result in undocumented behavior, such as failure to load the second DLL.</span></span>  
  
-   <span data-ttu-id="5cd33-150">Cuando el destino es el motor Microsoft Edge, la aplicación puede adquirir características nuevas inesperadamente cuando la plataforma subyacente se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5cd33-150">When targeting the Microsoft Edge engine, your app may unexpectedly acquire new features when the underlying platform is automatically updated.</span></span>  
  
     <span data-ttu-id="5cd33-151">Por ejemplo, el modo Internet Explorer 11 del motor en tiempo de ejecución heredado admite declaraciones de variables de ámbito de bloque, como `let` y `const` .</span><span class="sxs-lookup"><span data-stu-id="5cd33-151">For example, the Internet Explorer 11 mode of the legacy runtime supports block-scoping variable declarations such as `let` and `const`.</span></span> <span data-ttu-id="5cd33-152">Si el comportamiento de la versión automática del motor Microsoft Edge ya había sido el estándar, es posible que el código que ha funcionado en el modo Internet Explorer 10, que no tiene reglas de ámbito de bloqueo, haya iniciado el error cuando la plataforma se había actualizado automáticamente.</span><span class="sxs-lookup"><span data-stu-id="5cd33-152">If the Microsoft Edge engine automatic versioning behavior had been the standard previously, code that had worked in Internet Explorer 10 mode, which did not have block-scoping rules, may have started failing when the platform had automatically upgraded.</span></span> <span data-ttu-id="5cd33-153">Esto debe tenerse en cuenta a la hora de elegir el modelo en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5cd33-153">This must be a consideration when choosing which runtime model to use.</span></span> <span data-ttu-id="5cd33-154">Aunque creemos que debes dirigirte al motor de Microsoft Edge siempre que sea posible, debes tener cuidado con el uso de estructuras de código de JavaScript que pueden no ser válidas en el futuro.</span><span class="sxs-lookup"><span data-stu-id="5cd33-154">While we believe you should target the Microsoft Edge engine whenever possible, you must be careful about using JavaScript code structures that may become invalid in the future.</span></span>  
  
-   <span data-ttu-id="5cd33-155">JsRT para la tienda Windows solo es compatible con el motor de Microsoft Edge (Chakra. dll).</span><span class="sxs-lookup"><span data-stu-id="5cd33-155">JsRT for the Windows Store only supports the Microsoft Edge engine (chakra.dll).</span></span> <span data-ttu-id="5cd33-156">Las aplicaciones que intentan vincularse con cualquier API de JsRT en jscript9. dll producirán un error de certificación.</span><span class="sxs-lookup"><span data-stu-id="5cd33-156">Apps attempting to link against any JsRT API in jscript9.dll will fail certification.</span></span>  
  
-   <span data-ttu-id="5cd33-157">Es muy importante que no confunda la declaración de `JsCreateRuntime` , `JsCreateContext` y `JsStartDebugging` entre jscript9. dll y Chakra. dll, porque se impedirá que se equilibre la pila.</span><span class="sxs-lookup"><span data-stu-id="5cd33-157">It is critical that you do not confuse the declaration of `JsCreateRuntime`, `JsCreateContext`, and `JsStartDebugging` between jscript9.dll and chakra.dll, because it will result in imbalancing the stack.</span></span>  
  
     <span data-ttu-id="5cd33-158">Al usar C y C++, recibirá un error del vinculador si intenta usar una declaración incorrecta, siempre y cuando no esté haciendo algo como llamar `LoadLibrary` y, después, `GetProcAddress` .</span><span class="sxs-lookup"><span data-stu-id="5cd33-158">When using C and C++, you will receive a linker error if you try to use the wrong declaration, as long as you're not doing something like calling `LoadLibrary` and then `GetProcAddress`.</span></span> <span data-ttu-id="5cd33-159">Es posible que los desarrolladores de .NET no encuentren este problema con facilidad, así que vuelve a comprobar el código cuando use esta característica.</span><span class="sxs-lookup"><span data-stu-id="5cd33-159">.NET developers may not find this problem as easily, so double-check your code when using this feature.</span></span>  
  
## <span data-ttu-id="5cd33-160">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5cd33-160">See Also</span></span>  
 [<span data-ttu-id="5cd33-161">Hospedaje en tiempo de ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="5cd33-161">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)
 
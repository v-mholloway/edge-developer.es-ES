---
description: 'Más información sobre cómo destinar los diferentes motores de JavaScript de Windows 10. '
title: Dirigirse a Microsoft Edge frente a motores heredados en las API de JsRT
ms.date: 06/18/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: cbc7df6c-0bc9-48f5-b9ad-b9ed31c42f92
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 99a3143dd5f995332524a99e5c6c5019b955fea8
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752230"
---
# Dirigirse a Microsoft Edge frente a motores heredados en las API de JsRT  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Windows 10 es compatible con dos motores de JavaScript diferentes:  

*   El antiguo motor de chakra (también denominado *motor heredado* o jscript9.dll a continuación), que se envía y es compatible con Internet Explorer 11. Este motor se congela en el tiempo y permanecerá de forma fundamentalmente inalterado desde la versión de Windows 8.1/IE11.  
*   El nuevo motor de chakra (también llamado el *motor de borde* o chakra.dll a continuación) que se envía con el nuevo explorador y lo admite en Windows 10, Microsoft Edge. Este motor se actualizará continuamente y será compatible con un motor de [borde](https://blogs.msdn.com/b/ie/archive/2014/11/11/living-on-the-edge-our-next-step-in-interoperability.aspx) "vivo". Un motor de la vida de Microsoft Edge implica que, a diferencia del motor heredado, el motor de Microsoft Edge no transcurrirá ninguna forma de funcionalidad de scripting de versiones a participar.  

 Al crear una aplicación con la API de hospedaje en tiempo de ejecución de JavaScript (JsRT), puede elegir destinar el motor heredado o Microsoft Edge.  

*   Si necesita enfatizar la compatibilidad con versiones anteriores de las aplicaciones existentes, diríjase al motor heredado.  
*   Si desea que la aplicación vaya adelante y admita nuevas características de JavaScript a medida que se publican (por ejemplo, ECMAScript 6), destine el motor Microsoft Edge.  

En este tema se incluyen detalles que describen cómo destinar los distintos motores.  

## Apuntar a tu versión preferida  

Al crear una aplicación, puede seleccionar la versión de JsRT que admita el motor Microsoft Edge o el motor heredado. Puede elegir la versión de JsRT según las pautas anteriores. Para dar cabida a estas distinciones, se han realizado los cambios siguientes, `JsCreateRuntime` `JsCreateContext` y `JsStartDebugging` .  

Para `JsCreateRuntime` :  

*   Cuando el destino es el motor heredado, el valor de la `JsRuntimeVersionEdge` enumeración está obsoleto y un mensaje sugerirá usar el `JsRuntimeVersionInternetExplorer11` valor en su lugar.  
*   Cuando el destino es el motor Microsoft Edge, el parámetro version se omite de la `JsCreateRuntime` función.  
    
    ```cpp
    JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);
    ```  
    
 Para `JsCreateContext` y `JsStartDebugging` :  

*   Cuando el destino es el motor heredado, la `IDebugApplication` interfaz se usa para proporcionar sus propios métodos de depuración no remotos. Para fines de depuración, `JsCreateContext` y `JsStartDebugging` las funciones toman `IDebugApplication` como parámetro.  
*   Cuando el destino es el motor Microsoft Edge, la `IDebugApplication` interfaz ha quedado obsoleta. El motor de Chakra permite la capacidad de depuración nativa y de script con el depurador de Visual Studio sin requerir una implementación de `IDebugApplication` from. La interfaz ya no es un parámetro `JsCreateContext` y `JsStartDebugging` , como resultado.  

Las firmas de las API anteriores en el motor heredado son las siguientes:  

```cpp
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsRuntimeVersion version, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);

JsErrorCode JsCreateContext(JsRuntimeHandle runtime, IDebugApplication *debugApplication, JsContextRef *newContext);

JsErrorCode JsStartDebugging(IDebugApplication *debugApplication);
```  

Las firmas de las API anteriores en el motor de Microsoft Edge son las siguientes:  

```cpp
JsErrorCode JsCreateRuntime(JsRuntimeAttributes attributes, JsThreadServiceCallback callback, _Out_ JsRuntimeHandle* runtime);

JsErrorCode JsCreateContext(JsRuntimeHandle runtime, JsContextRef *newContext);

JsErrorCode JsStartDebugging();
```  

## Compilar la versión preferida con Visual C++  

Cuando use Visual C++, importe la API de JsRT incluyendo el encabezado JsRT. h y asegúrese de que JsRT. lib está incluido en la lista de archivos de entrada del vinculador:  

```cpp
#include <jsrt.h>
```  

![Agregar jsrt. lib como un archivo de entrada del vinculador](../chakra-hosting/media/js-chakra.png "JS_Chakra_")  

Si desea especificar los archivos binarios del motor Microsoft Edge, debe definir la macro `USE_EDGEMODE_JSRT` antes de incluir jsrt. h y, en lugar de vincular con jsrt. lib, debe vincular a chakrart. lib:  

```cpp
#define USE_EDGEMODE_JSRT
#include <jsrt.h>
```  

![Agregar chakrart. lib como un archivo de entrada del vinculador](../chakra-hosting/media/js-chakra-hosting.png "JS_Chakra_Hosting_")  

Si está empezando con una nueva aplicación, ya está listo para empezar a escribir código en la API de JsRT.  

## Compilar la versión preferida con .NET  

Si usa .NET y P/Invoke, debe cambiar las declaraciones de la API de JsRT [DllImport] para importar chakra.dll en lugar de jscript9.dll. Además, cambie la definición de `JsCreateRuntime` para quitar el `JsRuntimeVersion` parámetro y la definición de `JsCreateContext` y `JsStartDebugging` para quitar el `IDebugApplication` parámetro.  

Para el motor heredado, use el siguiente código.  

```csharp
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

Para el motor Microsoft Edge, use el siguiente código.  

```csharp
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
> Si va a calcular manualmente el valor del puntero de función (por ejemplo, a través de LoadLibrary o GetProcAddress), es muy importante que no mezcle las declaraciones del método o, de lo contrario, desequilibrará la pila, lo que provocará un comportamiento imprevisible, como por ejemplo, que se bloquee la aplicación. Se producirá el mismo problema si realiza una búsqueda y reemplazo global de instancias de jscript9.dll en el código de importación, porque perderá el `version` parámetro que se va a eliminar.  

## Resumen  

En Windows 10, las API de hospedaje en tiempo de ejecución de JavaScript se dividen en dos. Estas API ahora son compatibles con un motor "vivo" de Microsoft Edge, cuyas capacidades de idioma se alinearán con el motor "viviendo" de Microsoft Edge en Microsoft Edge. Puede aprovechar estas capacidades de su escritorio o aplicaciones de la tienda para crear nuevas y emocionantes maneras de ampliar su aplicación y aprovechar habilidades web modernas en su base de código existente. Sin embargo, dado que existen diferencias sutiles entre las versiones anteriores, debe tener en cuenta los siguientes puntos cuando dirigen el procesador perimetral o heredado.  

*   La aplicación solo puede admitir una versión de JsRT por proceso.  
    
    Por ejemplo, no puede crear un tiempo de ejecución de motor de Microsoft Edge y, a continuación, un Runtime de motor heredado y esperar que se ejecute correctamente en el mismo proceso. Esto no es compatible y puede dar lugar a un comportamiento no documentado, como el error de carga de la segunda DLL.  
    
*   Cuando el destino es el motor Microsoft Edge, la aplicación puede adquirir características nuevas inesperadamente cuando la plataforma subyacente se actualiza automáticamente.  
    
    Por ejemplo, el modo Internet Explorer 11 del motor en tiempo de ejecución heredado admite declaraciones de variables de ámbito de bloque, como `let` y `const` . Si el comportamiento de la versión automática del motor Microsoft Edge ya había sido el estándar, es posible que el código que ha funcionado en el modo Internet Explorer 10, que no tiene reglas de ámbito de bloqueo, haya iniciado el error cuando la plataforma se había actualizado automáticamente. Esto debe tenerse en cuenta a la hora de elegir el modelo en tiempo de ejecución. Aunque creemos que debes dirigirte al motor de Microsoft Edge siempre que sea posible, debes tener cuidado con el uso de estructuras de código de JavaScript que pueden no ser válidas en el futuro.  
    
*   JsRT para la tienda Windows solo es compatible con el motor de Microsoft Edge (chakra.dll). Las aplicaciones que intentan vincularse con cualquier API de JsRT en jscript9.dll producirán un error de certificación.  
*   Es muy importante que no confunda la declaración de `JsCreateRuntime` , `JsCreateContext` y `JsStartDebugging` entre jscript9.dll y chakra.dll, porque se impedirá que se equilibre la pila.  
    
    Al usar C y C++, recibirá un error del vinculador si intenta usar una declaración incorrecta, siempre y cuando no esté haciendo algo como llamar `LoadLibrary` y, después, `GetProcAddress` . Es posible que los desarrolladores de .NET no encuentren este problema con facilidad, así que vuelve a comprobar el código cuando use esta característica.  
    
## Consulte también  

*   [Hospedaje en tiempo de ejecución de JavaScript](../javascript-runtime-hosting.md)
 
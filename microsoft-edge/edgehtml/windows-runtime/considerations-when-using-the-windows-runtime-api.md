---
description: Consideraciones al usar la API de Windows Runtime
title: Consideraciones al usar la API de Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 170374fd109802bff0aa0fc93cea6c8d50c9d7c7
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399347"
---
# <a name="considerations-when-using-the-windows-runtime-api"></a>Consideraciones al usar la API de Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Puedes usar casi todos los elementos de la API de Windows Runtime en JavaScript.  Sin embargo, hay algunos aspectos de la representación de JavaScript de los elementos de Windows Runtime que debes tener en cuenta.  

> [!IMPORTANT]
> Para obtener información sobre cómo crear componentes de Windows Runtime en C++, C# o Visual Basic y consumirlos en JavaScript, consulta Crear componentes de Windows Runtime en [C++][WindowsUwpComponentsCreatingCpp] y Crear componentes de [Windows Runtime][WindowsUwpComponentsCreatingCsharpVb]en C# y Visual Basic .  

## <a name="special-cases-in-the-javascript-representation-of-windows-runtime-types"></a>Casos especiales en la representación de JavaScript de tipos de Windows Runtime  

:::row:::
   :::column span="1":::
      Cadenas  
   :::column-end:::
   :::column span="3":::
      Una cadena sin inicializar se pasa a un método de Windows Runtime como la cadena "undefined", y una cadena establecida en se pasa como `null` la cadena "null".  \(Esto es true siempre que un valor o se coaccione a una cadena.\) Antes de pasar una cadena a un método de Windows Runtime, debe inicializar como la cadena `null` `undefined` vacía \(""\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Interfaces  
   :::column-end:::
   :::column span="3":::
      No puedes implementar una interfaz de Windows Runtime en JavaScript.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Matrices  
   :::column-end:::
   :::column span="3":::
      Las matrices de Windows Runtime no se pueden cambiar de tamaño, por lo que los métodos que cambian el tamaño de las matrices en JavaScript no funcionan en matrices de Windows Runtime.  
      *   Matrices: si pasas un valor de matriz de JavaScript a un método de Windows Runtime, se copiará la matriz.  El método Windows Runtime no puede modificar la matriz ni sus miembros y devolverla a la aplicación JavaScript.  Sin embargo, puede usar matrices con tipo \(por ejemplo, [Int32Array Object][MDNInt32array]\), que no se copian.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Estructuras  
   :::column-end:::
   :::column span="3":::
      Las estructuras de Windows Runtime son objetos en JavaScript.  Si quieres pasar una estructura de Windows Runtime a un método de Windows Runtime, no creas una instancia de la estructura con la palabra `new` clave.  En su lugar, cree un objeto y agregue los miembros relevantes y sus valores.  Los nombres de los miembros deben estar en mayúsculas y minúsculas: `SomeStruct.firstMember` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Objetos  
   :::column-end:::
   :::column span="3":::
      Los objetos JavaScript no son los mismos que los objetos de código administrado \( `System.Object` \).  No puedes pasar un objeto JavaScript a un método de Windows Runtime que requiere un `System.Object` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Identidad de objeto  
   :::column-end:::
   :::column span="3":::
      En la mayoría de los casos, los objetos que se pasan entre Windows Runtime y JavaScript no cambian.  El motor de JavaScript mantiene un mapa de objetos conocidos.  Cuando se devuelve un objeto de Windows Runtime, coincide con el mapa y, si no existe, se crea un nuevo objeto.  Se sigue el mismo procedimiento para objetos que representan interfaces que devuelven los métodos de Windows Runtime.  Hay dos tipos de excepciones:  
      
      *   Los objetos que se devuelven desde una llamada de Windows Runtime y, a continuación, tienen nuevas propiedades \(expando\), no conservan sus nuevas propiedades cuando se pasan de nuevo a Windows Runtime.  Sin embargo, cuando se devuelven a la aplicación JavaScript, ya que coinciden con el objeto existente, el objeto devuelto tiene las propiedades expando.  
      *   Las estructuras y los delegados de Windows Runtime no se pueden identificar como idénticos a estructuras o delegados usados anteriormente.  Cada vez que se devuelve una estructura o delegado, obtiene una nueva referencia.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Colisiones de nombres  
   :::column-end:::
   :::column span="3":::
      Varias interfaces de Windows Runtime pueden tener miembros con los mismos nombres.  Si se combinan en un solo objeto JavaScript (que puede ser una representación de una clase en tiempo de ejecución o una interfaz), los miembros se representan con nombres completos.  Puede llamar a estos miembros mediante la siguiente sintaxis:  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      En el código siguiente, dos interfaces tienen un método Draw y una clase en tiempo de ejecución implementa ambas interfaces.  
      
      ```cpp
      namespace CollisionExample {
          interface InterfaceA
          {
              HRESULT Draw([in] Int32 a);
          }
          interface InterfaceB
          {
              HRESULT Draw([in] HString a);
          }
          runtimeclass ExampleObject {
            interface InterfaceA
            interface InterfaceB
          }
      }
      ```  
      
      A continuación se muestra cómo se puede llamar al código anterior en JavaScript.  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` parámetros  
   :::column-end:::
   :::column span="3":::
      Si un método de Windows Runtime tiene varios parámetros, en JavaScript el método tiene un objeto JavaScript como su valor devuelto y el objeto tiene propiedades que `out` corresponden al `out` parámetro.  Por ejemplo, considere la siguiente firma de Windows Runtime en C++.  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      La versión de JavaScript de esta firma es:  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      En este ejemplo, `returnValue` es un objeto JavaScript que tiene dos campos: `first` y `second` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Miembros estáticos  
   :::column-end:::
   :::column span="3":::
      Windows Runtime define tanto miembros estáticos como miembros de instancia.  En JavaScript, los miembros estáticos se agregan al objeto asociado a la clase o interfaz de Windows Runtime.  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
Para obtener más información acerca de la representación de JavaScript de tipos básicos de Windows Runtime, consulta [Representación de JavaScript de tipos de Windows Runtime.][WindowsRuntimeJavascriptTypes]  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Representación de JavaScript de tipos de Windows Runtime | Microsoft Docs"  

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes de Windows Runtime con C++/CX | Microsoft Docs"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes de Windows Runtime con C# y Visual Basic | Microsoft Docs"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  

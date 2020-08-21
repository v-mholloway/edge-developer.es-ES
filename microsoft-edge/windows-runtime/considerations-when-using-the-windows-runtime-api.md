---
title: Consideraciones al usar la API de Windows Runtime
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6b460fe514927590382613b7454a69c89a5a5f8b
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942212"
---
# Consideraciones al usar la API de Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Puedes usar casi todos los elementos de la API de Windows Runtime en JavaScript.  Sin embargo, hay algunos aspectos de la representación de JavaScript de elementos de Windows Runtime que debes tener en cuenta.  

> [!IMPORTANT]
> Para obtener información sobre la creación de componentes de Windows Runtime en C++, C# o Visual Basic y cómo consumirlos en JavaScript, consulta [creación de componentes de Windows Runtime en c++][WindowsUwpComponentsCreatingCpp] y [creación de componentes de Windows Runtime en C# y Visual Basic][WindowsUwpComponentsCreatingCsharpVb].  

## Casos especiales en la representación de JavaScript de los tipos de Windows Runtime  

:::row:::
   :::column span="1":::
      Cadena  
   :::column-end:::
   :::column span="3":::
      Una cadena no inicializada se pasa a un método de Windows Runtime como la cadena "undefined", y una cadena establecida en `null` se pasa como la cadena "null".  \ (Esto es verdadero cuando una `null` o un `undefined` valor se convierte en una cadena. \) antes de pasar una cadena a un método de Windows Runtime, se debe inicializar como la cadena vacía \ ("" \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Interactúa  
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
      Las matrices de Windows Runtime no se pueden cambiar de tamaño, por lo que los métodos que cambien el tamaño de las matrices en JavaScript no funcionan en matrices de Windows Runtime.  
      *   Matrices: Si pasa un valor de matriz de JavaScript a un método de Windows Runtime, se copia la matriz.  El método de Windows Runtime no puede modificar la matriz o sus miembros y devolverlo a la aplicación de JavaScript.  Sin embargo, puede usar matrices con tipo \ (por ejemplo, [objeto Int32Array][MDNInt32array]\), que no se copian.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Estructuras  
   :::column-end:::
   :::column span="3":::
      Las estructuras de Windows Runtime son objetos en JavaScript.  Si deseas pasar una estructura de Windows en tiempo de ejecución a un método de Windows Runtime, no cree instancias de la estructura con la `new` palabra clave.  En su lugar, cree un objeto y agregue los miembros relevantes y sus valores.  Los nombres de los miembros deberían estar en mayúsculas y minúsculas: `SomeStruct.firstMember` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Objeto  
   :::column-end:::
   :::column span="3":::
      Los objetos de JavaScript no son iguales que los objetos de código administrado \ ( `System.Object` \).  No puedes pasar un objeto de JavaScript a un método de Windows Runtime que requiera un `System.Object` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Identidad de objeto  
   :::column-end:::
   :::column span="3":::
      En la mayoría de los casos, los objetos transferidos entre Windows Runtime y JavaScript no cambian.  El motor de JavaScript mantiene un mapa de objetos conocidos.  Cuando se devuelve un objeto de Windows Runtime, se hace coincidir con el mapa y, si no existe, se crea un nuevo objeto.  Se sigue el mismo procedimiento para los objetos que representan interfaces devueltas por métodos de Windows Runtime.  Existen dos tipos de excepciones:  
      
      *   Los objetos que se devuelven de una llamada en tiempo de ejecución de Windows y, a continuación, tienen propiedades nuevas \ (Expando \) agregadas, no conservan las nuevas propiedades cuando se vuelven a pasar a Windows Runtime.  Sin embargo, cuando se devuelven a la aplicación de JavaScript, dado que se hacen coincidir con el objeto existente, el objeto devuelto tiene las propiedades expando.  
      *   Las estructuras y los delegados de Windows Runtime no se pueden identificar como idénticos a los delegados o estructuras usados previamente.  Cada vez que se devuelve una estructura o un delegado, obtiene una nueva referencia.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Colisiones de nombres  
   :::column-end:::
   :::column span="3":::
      Varias interfaces de Windows Runtime pueden tener miembros con el mismo nombre.  Si se combinan en un solo objeto de JavaScript (que puede ser una representación de una clase en tiempo de ejecución o una interfaz), los miembros se representan con nombres completos.  Puede llamar a estos miembros con la siguiente sintaxis:  
      
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
      
      A continuación te mostramos cómo puedes llamar al código anterior en JavaScript.  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` los  
   :::column-end:::
   :::column span="3":::
      Si un método de Windows Runtime tiene varios `out` parámetros, en JavaScript el método tiene un objeto de JavaScript como valor devuelto y el objeto tiene propiedades que corresponden al `out` parámetro.  Por ejemplo, ten en cuenta la siguiente firma de Windows Runtime en C++.  
      
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
      
      En este ejemplo, `returnValue` es un objeto de JavaScript que tiene dos campos: `first` y `second` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Miembros estáticos  
   :::column-end:::
   :::column span="3":::
      Windows Runtime define miembros estáticos y miembros de instancia.  En JavaScript, los miembros estáticos se agregan al objeto que está asociado a la clase o interfaz de Windows Runtime.  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
Para obtener más información sobre la representación de JavaScript de los tipos básicos de Windows Runtime, consulta [representación de JavaScript de los tipos de Windows Runtime][WindowsRuntimeJavascriptTypes].  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Representación de JavaScript de tipos de Windows Runtime | Microsoft docs"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes de Windows en tiempo de ejecución con C++/CX | Microsoft docs"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes de Windows en tiempo de ejecución con C# y Visual Basic | Microsoft docs"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
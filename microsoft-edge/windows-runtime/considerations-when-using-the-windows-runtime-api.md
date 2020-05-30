---
title: Consideraciones al usar la API de Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: 95b082e27c4f247b841a9540e13bd49bd4c8bd67
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574928"
---
# <span data-ttu-id="7be20-102">Consideraciones al usar la API de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="7be20-102">Considerations when Using the Windows Runtime API</span></span>  

<span data-ttu-id="7be20-103">Puedes usar casi todos los elementos de la API de Windows Runtime en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7be20-103">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="7be20-104">Sin embargo, hay algunos aspectos de la representación de JavaScript de elementos de Windows Runtime que debes tener en cuenta.</span><span class="sxs-lookup"><span data-stu-id="7be20-104">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="7be20-105">Para obtener información sobre la creación de componentes de Windows Runtime en C++, C# o Visual Basic y cómo consumirlos en JavaScript, consulta [creación de componentes de Windows Runtime en c++][WindowsUwpComponentsCreatingCpp] y [creación de componentes de Windows Runtime en C# y Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="7be20-105">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <span data-ttu-id="7be20-106">Casos especiales en la representación de JavaScript de los tipos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="7be20-106">Special Cases in the JavaScript Representation of Windows Runtime Types</span></span>  

*   <span data-ttu-id="7be20-107">Cadenas: una cadena no inicializada se pasa a un método de Windows Runtime como la cadena "undefined" y una cadena establecida en `null` se pasa como la cadena "null".</span><span class="sxs-lookup"><span data-stu-id="7be20-107">Strings: An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="7be20-108">\ (Esto es verdadero cuando una `null` o un `undefined` valor se convierte en una cadena. \) antes de pasar una cadena a un método de Windows Runtime, se debe inicializar como la cadena vacía \ ("" \).</span><span class="sxs-lookup"><span data-stu-id="7be20-108">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
*   <span data-ttu-id="7be20-109">Interfaces: no puede implementar una interfaz de Windows Runtime en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7be20-109">Interfaces: You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
*   <span data-ttu-id="7be20-110">Matrices: las matrices de Windows Runtime no se pueden cambiar de tamaño, por lo que los métodos que cambien el tamaño de las matrices en JavaScript no funcionan en matrices de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="7be20-110">Arrays: Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
*   <span data-ttu-id="7be20-111">Matrices: Si pasa un valor de matriz de JavaScript a un método de Windows Runtime, se copia la matriz.</span><span class="sxs-lookup"><span data-stu-id="7be20-111">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="7be20-112">El método de Windows Runtime no puede modificar la matriz o sus miembros y devolverlo a la aplicación de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7be20-112">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="7be20-113">Sin embargo, puede usar matrices con tipo \ (por ejemplo, [objeto Int32Array][MDNInt32array]\), que no se copian.</span><span class="sxs-lookup"><span data-stu-id="7be20-113">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
*   <span data-ttu-id="7be20-114">Estructuras: las estructuras de Windows Runtime son objetos en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7be20-114">Structures: Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="7be20-115">Si deseas pasar una estructura de Windows en tiempo de ejecución a un método de Windows Runtime, no cree instancias de la estructura con la `new` palabra clave.</span><span class="sxs-lookup"><span data-stu-id="7be20-115">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="7be20-116">En su lugar, cree un objeto y agregue los miembros relevantes y sus valores.</span><span class="sxs-lookup"><span data-stu-id="7be20-116">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="7be20-117">Los nombres de los miembros deberían estar en mayúsculas y minúsculas: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="7be20-117">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
*   <span data-ttu-id="7be20-118">Objetos: los objetos de JavaScript no son iguales que los objetos de código administrado \ ( `System.Object` \).</span><span class="sxs-lookup"><span data-stu-id="7be20-118">Objects: JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="7be20-119">No puedes pasar un objeto de JavaScript a un método de Windows Runtime que requiera un `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="7be20-119">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
*   <span data-ttu-id="7be20-120">Identidad de objeto: en la mayoría de los casos, los objetos pasados entre Windows Runtime y JavaScript no cambian.</span><span class="sxs-lookup"><span data-stu-id="7be20-120">Object identity: In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="7be20-121">El motor de JavaScript mantiene un mapa de objetos conocidos.</span><span class="sxs-lookup"><span data-stu-id="7be20-121">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="7be20-122">Cuando se devuelve un objeto de Windows Runtime, se hace coincidir con el mapa y, si no existe, se crea un nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="7be20-122">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="7be20-123">Se sigue el mismo procedimiento para los objetos que representan interfaces devueltas por métodos de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="7be20-123">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="7be20-124">Existen dos tipos de excepciones:</span><span class="sxs-lookup"><span data-stu-id="7be20-124">There are two kinds of exceptions:</span></span>  

    *   <span data-ttu-id="7be20-125">Los objetos que se devuelven de una llamada en tiempo de ejecución de Windows y, a continuación, tienen propiedades nuevas \ (Expando \) agregadas, no conservan las nuevas propiedades cuando se vuelven a pasar a Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="7be20-125">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="7be20-126">Sin embargo, cuando se devuelven a la aplicación de JavaScript, dado que se hacen coincidir con el objeto existente, el objeto devuelto tiene las propiedades expando.</span><span class="sxs-lookup"><span data-stu-id="7be20-126">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
    *   <span data-ttu-id="7be20-127">Las estructuras y los delegados de Windows Runtime no se pueden identificar como idénticos a los delegados o estructuras usados previamente.</span><span class="sxs-lookup"><span data-stu-id="7be20-127">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="7be20-128">Cada vez que se devuelve una estructura o un delegado, obtiene una nueva referencia.</span><span class="sxs-lookup"><span data-stu-id="7be20-128">Every time a structure or delegate is returned, it gets a new reference.</span></span>  

*   <span data-ttu-id="7be20-129">Colisiones de nombre: varias interfaces de Windows Runtime pueden tener miembros con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="7be20-129">Name collisions: Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="7be20-130">Si se combinan en un solo objeto de JavaScript (que puede ser una representación de una clase en tiempo de ejecución o una interfaz), los miembros se representan con nombres completos.</span><span class="sxs-lookup"><span data-stu-id="7be20-130">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="7be20-131">Puede llamar a estos miembros con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="7be20-131">You can call these members by using the following syntax:</span></span>  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    <span data-ttu-id="7be20-132">En el código siguiente, dos interfaces tienen un método Draw y una clase en tiempo de ejecución implementa ambas interfaces.</span><span class="sxs-lookup"><span data-stu-id="7be20-132">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
    
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
    
    <span data-ttu-id="7be20-133">A continuación te mostramos cómo puedes llamar al código anterior en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7be20-133">Here is how you can call the above code in JavaScript.</span></span>  
    
    ```javascript
    var example = new ExampleObject();
    example["CollisionExample.InterfaceA.draw"](12);
    example["CollisionExample.InterfaceB.draw"]("hello");
    ```  
    
*   `Out` <span data-ttu-id="7be20-134">parámetros: Si un método de Windows Runtime tiene varios `out` parámetros, en JavaScript el método tiene un objeto de JavaScript como valor devuelto y el objeto tiene propiedades que corresponden al `out` parámetro.</span><span class="sxs-lookup"><span data-stu-id="7be20-134">parameters: If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="7be20-135">Por ejemplo, ten en cuenta la siguiente firma de Windows Runtime en C++.</span><span class="sxs-lookup"><span data-stu-id="7be20-135">For example, consider the following Windows Runtime signature in C++.</span></span>  
    
    ```cpp
    void ExampleMethod(
      [OutAttribute] char^ first,
      [OutAttribute] char^ second
    )
    ```  
    
    <span data-ttu-id="7be20-136">La versión de JavaScript de esta firma es:</span><span class="sxs-lookup"><span data-stu-id="7be20-136">The JavaScript version of this signature is:</span></span>  
    
    ```javascript
    var returnValue = exampleMethod();
    ```  
    
    <span data-ttu-id="7be20-137">En este ejemplo, `returnValue` es un objeto de JavaScript que tiene dos campos: `first` y `second` .</span><span class="sxs-lookup"><span data-stu-id="7be20-137">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
    
*   <span data-ttu-id="7be20-138">Miembros estáticos: Windows Runtime define tanto miembros estáticos como miembros de instancia.</span><span class="sxs-lookup"><span data-stu-id="7be20-138">Static members: The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="7be20-139">En JavaScript, los miembros estáticos se agregan al objeto que está asociado a la clase o interfaz de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="7be20-139">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
<span data-ttu-id="7be20-140">Para obtener más información sobre la representación de JavaScript de los tipos básicos de Windows Runtime, consulta [representación de JavaScript de los tipos de Windows Runtime][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="7be20-140">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Representación de JavaScript de los tipos de Windows Runtime"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes de Windows Runtime con C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes de Windows en tiempo de ejecución con C# y Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  
---
description: Proporciona instrucciones para personalizar la visualización del botón mostrar contraseñas
title: Personalizar el botón mostrar contraseña
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidad, plataforma web, mostrar contraseña, icono de ojo
ms.openlocfilehash: af8120aad7316ffc051113591e770fa913814eb3
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327729"
---
# <span data-ttu-id="951c6-104">Personalizar el botón mostrar contraseña</span><span class="sxs-lookup"><span data-stu-id="951c6-104">Customize the password reveal button</span></span>  

<span data-ttu-id="951c6-105">El `password` tipo de entrada en Microsoft Edge incluye un control de **revelación de** contraseñas.</span><span class="sxs-lookup"><span data-stu-id="951c6-105">The `password` input type in Microsoft Edge includes a **password reveal** control.</span></span>  <span data-ttu-id="951c6-106">Un usuario puede elegir el botón **de entrada de** contraseña para mostrar el campo **de** contraseña.</span><span class="sxs-lookup"><span data-stu-id="951c6-106">A user may choose the **password input** button to reveal the **password** field.</span></span>  <span data-ttu-id="951c6-107">El campo de **contraseña revelada** ayuda al usuario a comprobar si la contraseña es correcta.</span><span class="sxs-lookup"><span data-stu-id="951c6-107">The revealed **password** field helps the user verify if the password is correctly.</span></span>  <span data-ttu-id="951c6-108">Una vez que un  usuario ha escrito texto  en el campo de contraseña, un usuario puede elegir el botón mostrar contraseña o seleccionar para alternar la `Alt` + `F8` visibilidad de la entrada.</span><span class="sxs-lookup"><span data-stu-id="951c6-108">After a user has entered text in the **password** field, a user may choose the **password reveal** button or select `Alt`+`F8` to toggle visibility of the input.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="951c6-109">Un **campo de** contraseña con puntos que ocultan los caracteres escritos por un usuario.</span><span class="sxs-lookup"><span data-stu-id="951c6-109">A **password** field with dots hiding the characters entered by a user.</span></span>  <span data-ttu-id="951c6-110">El **botón Mostrar** contraseña aparece a la derecha del campo **de** contraseña.</span><span class="sxs-lookup"><span data-stu-id="951c6-110">The **password reveal** button appears to the right of the **password** field.</span></span>
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-off.msft.png" alt-text="El icono con forma de ojo aparece junto a los puntos que ocultan el texto de la contraseña" lightbox="./media/mdn-demo-password-reveal-off.msft.png":::
         <span data-ttu-id="951c6-112">El icono con forma de ojo aparece junto a los puntos que ocultan el texto de la contraseña</span><span class="sxs-lookup"><span data-stu-id="951c6-112">The eye-shaped icon appears next to the dots that hide the password text</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="951c6-113">Alterna el **botón mostrar** contraseña para cambiar el icono de ojo a un icono de ojo con una barra diagonal y para mostrar el texto de la contraseña original.</span><span class="sxs-lookup"><span data-stu-id="951c6-113">Toggle the **password reveal** button to change the eye icon to an eye icon with a slash through it, and to reveal the original password text.</span></span>  
      
      :::image type="complex" source="./media/mdn-demo-password-reveal-on.msft.png" alt-text="El icono con forma de ojo tiene una barra diagonal y se muestra el texto de la contraseña original" lightbox="./media/mdn-demo-password-reveal-on.msft.png":::
         <span data-ttu-id="951c6-115">El icono con forma de ojo tiene una barra diagonal y se muestra el texto de la contraseña original</span><span class="sxs-lookup"><span data-stu-id="951c6-115">The The eye-shaped icon has a slash on it and the original password text is displayed</span></span> :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="951c6-116">De forma predeterminada, **el botón mostrar** contraseña se inserta en el DOM de sombra de todos los elementos HTML con el conjunto en `input` `type` `"password"` .</span><span class="sxs-lookup"><span data-stu-id="951c6-116">By default, the **password reveal** button inserts into the Shadow DOM of all HTML `input` elements with the `type` set to `"password"`.</span></span>  <span data-ttu-id="951c6-117">A partir de la versión 87 de Microsoft Edge, los usuarios o [empresas][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] pueden deshabilitar esta característica globalmente.</span><span class="sxs-lookup"><span data-stu-id="951c6-117">Starting with Microsoft Edge Version 87, users or [enterprises][DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled] may disable this feature globally.</span></span>  <span data-ttu-id="951c6-118">Usted, los diseñadores web y los desarrolladores, deben esperar que la mayoría de los usuarios de Microsoft Edge tengan la experiencia predeterminada.</span><span class="sxs-lookup"><span data-stu-id="951c6-118">You, web designers and developers, should expect most Microsoft Edge users to have the default experience.</span></span>  

## <span data-ttu-id="951c6-119">Quitar el control de revelación de contraseñas</span><span class="sxs-lookup"><span data-stu-id="951c6-119">Remove the password reveal control</span></span>  

<span data-ttu-id="951c6-120">Puedes quitar por completo el botón **para mostrar** contraseñas apuntando al `::-ms-reveal` pseudo elemento.</span><span class="sxs-lookup"><span data-stu-id="951c6-120">You may completely remove the **password reveal** button by targeting the `::-ms-reveal` pseudo element.</span></span>  

```css
::-ms-reveal {
    display: none;
}
```  

<span data-ttu-id="951c6-121">Sin embargo, debes considerar la posibilidad de aprovechar el botón **para mostrar la** contraseña.</span><span class="sxs-lookup"><span data-stu-id="951c6-121">However, you should consider taking advantage of the **password reveal** button.</span></span>  <span data-ttu-id="951c6-122">El botón **mostrar contraseña** nativa tiene importantes [medidas de seguridad integradas](#visibility-of-the-control) en el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="951c6-122">The native **password reveal** button has important [security measures](#visibility-of-the-control) built into the behavior.</span></span>  

## <span data-ttu-id="951c6-123">Personalizar el estilo de control</span><span class="sxs-lookup"><span data-stu-id="951c6-123">Customize the control style</span></span>  

<span data-ttu-id="951c6-124">En lugar de quitar completamente el control, puede  modificar el estilo del botón mostrar contraseña para que coincida mejor con el lenguaje visual del sitio web.</span><span class="sxs-lookup"><span data-stu-id="951c6-124">Instead of fully removing the control, you may instead modify the styling of the **password reveal** button to better match the visual language of the website.</span></span>  <span data-ttu-id="951c6-125">El siguiente fragmento de código proporciona un ejemplo de este estilo.</span><span class="sxs-lookup"><span data-stu-id="951c6-125">The following snippet provides an example of such styling.</span></span>  

```css
::-ms-reveal {
    border: 1px solid transparent;
    border-radius: 50%;
    box-shadow: 0 0 3px currentColor;
}
```  

<span data-ttu-id="951c6-126">Ten en cuenta lo siguiente al aplicar estilo al botón **Mostrar** contraseña.</span><span class="sxs-lookup"><span data-stu-id="951c6-126">Keep the following things in mind when you style the **password reveal** button.</span></span>  

*   <span data-ttu-id="951c6-127">El icono de ojo se implementa como una imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="951c6-127">The eye icon implements as a background image.</span></span>  <span data-ttu-id="951c6-128">Para agregar un color de fondo al **botón** Mostrar contraseña, usa la propiedad CSS en lugar de `background-color` la propiedad `background` abreviada.</span><span class="sxs-lookup"><span data-stu-id="951c6-128">To add a background color to the **password reveal** button, use the CSS `background-color` property instead of the `background` shorthand property.</span></span>  
*   <span data-ttu-id="951c6-129">Puedes ajustar el tamaño y la escala del botón mostrar **contraseña.**</span><span class="sxs-lookup"><span data-stu-id="951c6-129">You may adjust the size and scale of the **password reveal** button.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="951c6-130">El explorador oculta cualquier desbordamiento fuera de los límites del control de entrada de contraseña.</span><span class="sxs-lookup"><span data-stu-id="951c6-130">The browser hides any overflow outside of the bounds of the password input control.</span></span>  
    
*   <span data-ttu-id="951c6-131">Actualmente, no hay selectores de estado disponibles para aplicar estilo al estado de alternancia del botón **mostrar contraseña.**</span><span class="sxs-lookup"><span data-stu-id="951c6-131">Currently, no state selectors are available to style the toggled state of the **password reveal** button.</span></span>  
    
## <span data-ttu-id="951c6-132">Visibilidad del control</span><span class="sxs-lookup"><span data-stu-id="951c6-132">Visibility of the control</span></span>  

<span data-ttu-id="951c6-133">El **botón mostrar** contraseña no está disponible hasta que el usuario escribe texto en el campo **de** contraseña.</span><span class="sxs-lookup"><span data-stu-id="951c6-133">The **password reveal** button is unavailable until the user enters text into the **password** field.</span></span>  <span data-ttu-id="951c6-134">Para ayudar a proteger la entrada de contraseña del usuario, el explorador suprime el botón en los siguientes escenarios.</span><span class="sxs-lookup"><span data-stu-id="951c6-134">To help keep the user's password entry secure, the browser suppresses the button in the following scenarios.</span></span>

*   <span data-ttu-id="951c6-135">Si el foco se aleja del campo **de contraseña,** el explorador quita el botón **mostrar contraseña.**</span><span class="sxs-lookup"><span data-stu-id="951c6-135">If focus moves away from the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="951c6-136">Si los scripts modifican **el campo de** contraseña, el explorador quita el botón mostrar **contraseña.**</span><span class="sxs-lookup"><span data-stu-id="951c6-136">If scripts modify the **password** field, the browser removes the **password reveal** button.</span></span>  
*   <span data-ttu-id="951c6-137">Si un usuario quita el **botón** mostrar contraseña, el  usuario debe  eliminar el contenido del campo de contraseña antes de que el botón mostrar contraseña se muestre de nuevo.</span><span class="sxs-lookup"><span data-stu-id="951c6-137">If a user removes the **password reveal** button, the user must delete the contents of the **password** field before the **password reveal** button displays again.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="951c6-138">Esta característica impide que alguien haga un pequeño ajuste para ver la contraseña, en caso de que el usuario salga de un dispositivo desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="951c6-138">This feature prevents someone from making a minor adjustment to view the password, should the user step away from an unlocked device.</span></span>
    
<span data-ttu-id="951c6-139">El **botón mostrar** contraseña no está disponible si el campo de contraseña se rellena automáticamente con el administrador de contraseñas. </span><span class="sxs-lookup"><span data-stu-id="951c6-139">The **password reveal** button is unavailable if the **password** field autofills using the password manager.</span></span>  

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesPasswordrevealenabled]: /deployedge/microsoft-edge-policies#passwordrevealenabled "PasswordRevealEnabled - Microsoft Edge - Directivas | Microsoft Docs"  

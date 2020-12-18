---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Más información sobre cómo se puede usar la API de notificaciones web para permitir que los sitios web envíen notificaciones de usuario fuera del contexto del explorador Microsoft Edge.
title: 'API de notificaciones Web: Guía para desarrolladores'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2be201a790c6fca1526c8b6eb13e4203e8e53206
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236374"
---
# <span data-ttu-id="cc286-104">API de notificaciones Web</span><span class="sxs-lookup"><span data-stu-id="cc286-104">Web Notifications API</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="cc286-105">La API de notificaciones web permite a los sitios web enviar notificaciones de usuarios fuera del contexto de una página web dentro del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cc286-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span>  <span data-ttu-id="cc286-106">Un ejemplo de esta característica en acción sería con una aplicación de mensajería como Skype.</span><span class="sxs-lookup"><span data-stu-id="cc286-106">An example of this feature in action would be with a messaging application like Skype.</span></span>  <span data-ttu-id="cc286-107">Cuando un usuario recibe un mensaje nuevo, aparece una notificación en el escritorio para avisarle del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cc286-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span>  <span data-ttu-id="cc286-108">Las notificaciones Web se integran completamente con la plataforma de notificación y el centro de actividades de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cc286-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span>  

## <span data-ttu-id="cc286-109">Crear una notificación</span><span class="sxs-lookup"><span data-stu-id="cc286-109">Creating a notification</span></span>  

<span data-ttu-id="cc286-110">En el CodePen siguiente se crea una notificación de Skype ficticia haciendo que el objeto de [notificación](https://msdn.microsoft.com/library/mt710818) se establezca con las opciones de [título](https://msdn.microsoft.com/library/mt710826), [icono](https://msdn.microsoft.com/library/mt710814)y [cuerpo](https://msdn.microsoft.com/library/mt710811) :</span><span class="sxs-lookup"><span data-stu-id="cc286-110">The CodePen below creates a mock Skype notification by making a [Notification](https://msdn.microsoft.com/library/mt710818) object with the [title](https://msdn.microsoft.com/library/mt710826), [icon](https://msdn.microsoft.com/library/mt710814), and [body](https://msdn.microsoft.com/library/mt710811) options set:</span></span>  

<iframe height='295' scrolling='no' title='<span data-ttu-id="cc286-111">Notificaciones Web</span><span class="sxs-lookup"><span data-stu-id="cc286-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="cc286-112">Vea las <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notificaciones web del lápiz de </a> documentos de Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) en <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="cc286-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

<span data-ttu-id="cc286-113">Es muy recomendable especificar un **icono** para cada notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-113">It is strongly recommended that an **icon** be specified for each notification.</span></span>  <span data-ttu-id="cc286-114">Esto no solo mejora una notificación desde un punto de vista de la interfaz de usuario, sino que también ayuda a alertar a los usuarios de dónde se envían las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="cc286-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>  

<span data-ttu-id="cc286-115">Vea el siguiente vídeo para obtener un tutorial sobre la creación de una notificación web y para ver su comportamiento en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cc286-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### <span data-ttu-id="cc286-116">Propiedades de notificación</span><span class="sxs-lookup"><span data-stu-id="cc286-116">Notification properties</span></span>  

<span data-ttu-id="cc286-117">Las notificaciones se pueden establecer con las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="cc286-117">Notifications can be set with the following properties:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-118">body</span><span class="sxs-lookup"><span data-stu-id="cc286-118">body</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-119">Texto del cuerpo de la notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-119">The body text of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-120">dir</span><span class="sxs-lookup"><span data-stu-id="cc286-120">dir</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-121">La dirección del texto de la notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-121">The direction of the notification's text.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-122">icon</span><span class="sxs-lookup"><span data-stu-id="cc286-122">icon</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-123">La dirección URL de la notificación que se usa para su icono.</span><span class="sxs-lookup"><span data-stu-id="cc286-123">The notification's URL that is used for its icon.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-124">Moreno</span><span class="sxs-lookup"><span data-stu-id="cc286-124">lang</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-125">El idioma de la notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-125">The language of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-126">permiso</span><span class="sxs-lookup"><span data-stu-id="cc286-126">permission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-127">El permiso para mostrar la notificación actual que el usuario ha concedido para el origen actual.</span><span class="sxs-lookup"><span data-stu-id="cc286-127">The current notification display permission the user has granted for the current origin.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-128">tag</span><span class="sxs-lookup"><span data-stu-id="cc286-128">tag</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-129">La etiqueta de la notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-129">The tag of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-130">title</span><span class="sxs-lookup"><span data-stu-id="cc286-130">title</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-131">El título de la notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-131">The title of the notification.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cc286-132">Eventos de notificación</span><span class="sxs-lookup"><span data-stu-id="cc286-132">Notification events</span></span>  

<span data-ttu-id="cc286-133">Los eventos siguientes se usan con el objeto de [notificación](https://developer.mozilla.org/docs/Web/API/Notification) :</span><span class="sxs-lookup"><span data-stu-id="cc286-133">The following events are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-134">OnClick</span><span class="sxs-lookup"><span data-stu-id="cc286-134">onclick</span></span>](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-135">Se desencadena cuando el usuario hace clic en una notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-135">Fires when a notification is clicked by the user.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-136">OnClose</span><span class="sxs-lookup"><span data-stu-id="cc286-136">onclose</span></span>](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-137">Se desencadena cuando el usuario cierra una notificación o se produce un tiempo de espera automático.</span><span class="sxs-lookup"><span data-stu-id="cc286-137">Fires when a notification is closed by the user or an auto timeout.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-138">OnError</span><span class="sxs-lookup"><span data-stu-id="cc286-138">onerror</span></span>](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-139">Se desencadena cuando se produce un error durante la administración de una notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-139">Fires when an error occurs while handling a notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-140">Mostrar</span><span class="sxs-lookup"><span data-stu-id="cc286-140">onshow</span></span>](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-141">Se desencadena cuando se muestra una notificación.</span><span class="sxs-lookup"><span data-stu-id="cc286-141">Fires when a notification is displayed.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="cc286-142">Métodos de notificación</span><span class="sxs-lookup"><span data-stu-id="cc286-142">Notification methods</span></span>  

<span data-ttu-id="cc286-143">Los métodos siguientes se usan con el objeto [Notification](https://developer.mozilla.org/docs/Web/API/Notification) :</span><span class="sxs-lookup"><span data-stu-id="cc286-143">The following methods are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-144">cerrar</span><span class="sxs-lookup"><span data-stu-id="cc286-144">close</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-145">Cierra una notificación que se muestra.</span><span class="sxs-lookup"><span data-stu-id="cc286-145">Closes a displayed notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="cc286-146">requestPermission</span><span class="sxs-lookup"><span data-stu-id="cc286-146">requestPermission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="cc286-147">Solicita permiso al usuario para permitir que las notificaciones sean mostradas por el origen actual.</span><span class="sxs-lookup"><span data-stu-id="cc286-147">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="cc286-148">Permisos de notificación</span><span class="sxs-lookup"><span data-stu-id="cc286-148">Notification permissions</span></span>  

<span data-ttu-id="cc286-149">Microsoft Edge permite a los usuarios administrar los permisos de notificaciones para cada dominio de sitio web específico.</span><span class="sxs-lookup"><span data-stu-id="cc286-149">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span>  <span data-ttu-id="cc286-150">El usuario puede seleccionar **sí** o **no** cuando lo solicite el dominio para permitirle Mostrar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="cc286-150">It's up to the user to either select **Yes** or **No** when asked by the domain to let it show notifications.</span></span>  <span data-ttu-id="cc286-151">El método [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) se usa para indicar el estado de los permisos como `granted` , `denied` o `default` .</span><span class="sxs-lookup"><span data-stu-id="cc286-151">The [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span>  <span data-ttu-id="cc286-152">Un valor de `default` indica que el usuario no ha tomado una decisión, que se ve como equivalente `denied` .</span><span class="sxs-lookup"><span data-stu-id="cc286-152">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>  

## <span data-ttu-id="cc286-153">Referencia de las API</span><span class="sxs-lookup"><span data-stu-id="cc286-153">API reference</span></span>  

[<span data-ttu-id="cc286-154">Notificaciones Web</span><span class="sxs-lookup"><span data-stu-id="cc286-154">Web Notifications</span></span>](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## <span data-ttu-id="cc286-155">Estadístico</span><span class="sxs-lookup"><span data-stu-id="cc286-155">Specification</span></span>  

[<span data-ttu-id="cc286-156">Notificaciones Web</span><span class="sxs-lookup"><span data-stu-id="cc286-156">Web Notifications</span></span>](https://notifications.spec.whatwg.org)  

---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Más información sobre cómo se puede usar la API de notificaciones web para permitir que los sitios web envíen notificaciones de usuario fuera del contexto del explorador Microsoft Edge.
title: 'Guía para desarrolladores: API de notificaciones Web'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/18/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: da563a333491ef699925adec6f97b3c21d3e54a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573306"
---
# <span data-ttu-id="ac354-104">API de notificaciones Web</span><span class="sxs-lookup"><span data-stu-id="ac354-104">Web Notifications API</span></span>

<span data-ttu-id="ac354-105">La API de notificaciones web permite a los sitios web enviar notificaciones de usuarios fuera del contexto de una página web dentro del explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ac354-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span> <span data-ttu-id="ac354-106">Un ejemplo de esta característica en acción sería con una aplicación de mensajería como Skype.</span><span class="sxs-lookup"><span data-stu-id="ac354-106">An example of this feature in action would be with a messaging application like Skype.</span></span> <span data-ttu-id="ac354-107">Cuando un usuario recibe un mensaje nuevo, aparece una notificación en el escritorio para avisarle del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ac354-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span> <span data-ttu-id="ac354-108">Las notificaciones Web se integran completamente con la plataforma de notificación y el centro de actividades de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ac354-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span> 

## <span data-ttu-id="ac354-109">Crear una notificación</span><span class="sxs-lookup"><span data-stu-id="ac354-109">Creating a notification</span></span>

<span data-ttu-id="ac354-110">En el CodePen siguiente se crea una notificación de Skype ficticia haciendo un [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto con el [`title`](https://msdn.microsoft.com/library/mt710826) , el y el conjunto de [`icon`](https://msdn.microsoft.com/library/mt710814) [`body`](https://msdn.microsoft.com/library/mt710811) Opciones:</span><span class="sxs-lookup"><span data-stu-id="ac354-110">The CodePen below creates a mock Skype notification by making a [`Notification`](https://msdn.microsoft.com/library/mt710818) object with the [`title`](https://msdn.microsoft.com/library/mt710826), [`icon`](https://msdn.microsoft.com/library/mt710814), and [`body`](https://msdn.microsoft.com/library/mt710811) options set:</span></span>


<iframe height='295' scrolling='no' title='<span data-ttu-id="ac354-111">Notificaciones Web</span><span class="sxs-lookup"><span data-stu-id="ac354-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="ac354-112">Vea las <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notificaciones web del lápiz de </a> documentos de Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) en <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="ac354-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span>
</iframe>

<span data-ttu-id="ac354-113">Se recomienda especificar un nombre `icon` para cada notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-113">It is strongly recommended that an `icon` be specified for each notification.</span></span> <span data-ttu-id="ac354-114">Esto no solo mejora una notificación desde un punto de vista de la interfaz de usuario, sino que también ayuda a alertar a los usuarios de dónde se envían las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ac354-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>

<span data-ttu-id="ac354-115">Vea el siguiente vídeo para obtener un tutorial sobre la creación de una notificación web y para ver su comportamiento en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ac354-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### <span data-ttu-id="ac354-116">Propiedades de notificación</span><span class="sxs-lookup"><span data-stu-id="ac354-116">Notification properties</span></span>

<span data-ttu-id="ac354-117">Las notificaciones se pueden establecer con las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ac354-117">Notifications can be set with the following options:</span></span>

<span data-ttu-id="ac354-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac354-118">Property</span></span> | <span data-ttu-id="ac354-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac354-119">Description</span></span>
:-------- | :----------
[<span data-ttu-id="ac354-120">body</span><span class="sxs-lookup"><span data-stu-id="ac354-120">body</span></span>](https://msdn.microsoft.com/library/mt710811) | <span data-ttu-id="ac354-121">Texto del cuerpo de la notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-121">The body text of the notification.</span></span>
[<span data-ttu-id="ac354-122">dir</span><span class="sxs-lookup"><span data-stu-id="ac354-122">dir</span></span>](https://msdn.microsoft.com/library/mt710813) | <span data-ttu-id="ac354-123">La dirección del texto de la notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-123">The direction of the notification's text.</span></span>
[<span data-ttu-id="ac354-124">icon</span><span class="sxs-lookup"><span data-stu-id="ac354-124">icon</span></span>](https://msdn.microsoft.com/library/mt710814) | <span data-ttu-id="ac354-125">La dirección URL de la notificación que se usa para su icono.</span><span class="sxs-lookup"><span data-stu-id="ac354-125">The notification's URL that is used for its icon.</span></span>
[<span data-ttu-id="ac354-126">Moreno</span><span class="sxs-lookup"><span data-stu-id="ac354-126">lang</span></span>](https://msdn.microsoft.com/library/mt710815) | <span data-ttu-id="ac354-127">El idioma de la notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-127">The language of the notification.</span></span>
[<span data-ttu-id="ac354-128">permiso</span><span class="sxs-lookup"><span data-stu-id="ac354-128">permission</span></span>](https://msdn.microsoft.com/library/mt670637) | <span data-ttu-id="ac354-129">El permiso para mostrar la notificación actual que el usuario ha concedido para el origen actual.</span><span class="sxs-lookup"><span data-stu-id="ac354-129">The current notification display permission the user has granted for the current origin.</span></span>
[<span data-ttu-id="ac354-130">tag</span><span class="sxs-lookup"><span data-stu-id="ac354-130">tag</span></span>](https://msdn.microsoft.com/library/mt710825) | <span data-ttu-id="ac354-131">La etiqueta de la notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-131">The tag of the notification.</span></span>
[<span data-ttu-id="ac354-132">title</span><span class="sxs-lookup"><span data-stu-id="ac354-132">title</span></span>](https://msdn.microsoft.com/library/mt710826) | <span data-ttu-id="ac354-133">El título de la notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-133">The title of the notification.</span></span>

### <span data-ttu-id="ac354-134">Eventos de notificación</span><span class="sxs-lookup"><span data-stu-id="ac354-134">Notification events</span></span>

<span data-ttu-id="ac354-135">Los eventos siguientes se usan con el [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto:</span><span class="sxs-lookup"><span data-stu-id="ac354-135">The following events are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="ac354-136">Evento</span><span class="sxs-lookup"><span data-stu-id="ac354-136">Event</span></span> | <span data-ttu-id="ac354-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac354-137">Description</span></span>
:-------- | :----------
[<span data-ttu-id="ac354-138">OnClick</span><span class="sxs-lookup"><span data-stu-id="ac354-138">onclick</span></span>](https://msdn.microsoft.com/library/mt712180) | <span data-ttu-id="ac354-139">Se desencadena cuando el usuario hace clic en una notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-139">Fires when a notification is clicked by the user.</span></span>
[<span data-ttu-id="ac354-140">OnClose</span><span class="sxs-lookup"><span data-stu-id="ac354-140">onclose</span></span>](https://msdn.microsoft.com/library/mt712178) | <span data-ttu-id="ac354-141">Se desencadena cuando el usuario cierra una notificación o se produce un tiempo de espera automático.</span><span class="sxs-lookup"><span data-stu-id="ac354-141">Fires when a notification is closed by the user or an auto timeout.</span></span>
[<span data-ttu-id="ac354-142">OnError</span><span class="sxs-lookup"><span data-stu-id="ac354-142">onerror</span></span>](https://msdn.microsoft.com/library/mt712181) | <span data-ttu-id="ac354-143">Se desencadena cuando se produce un error durante la administración de una notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-143">Fires when an error occurs while handling a notification.</span></span>
[<span data-ttu-id="ac354-144">Mostrar</span><span class="sxs-lookup"><span data-stu-id="ac354-144">onshow</span></span>](https://msdn.microsoft.com/library/mt712182) | <span data-ttu-id="ac354-145">Se desencadena cuando se muestra una notificación.</span><span class="sxs-lookup"><span data-stu-id="ac354-145">Fires when a notification is displayed.</span></span>

### <span data-ttu-id="ac354-146">Métodos de notificación</span><span class="sxs-lookup"><span data-stu-id="ac354-146">Notification methods</span></span>

<span data-ttu-id="ac354-147">Los métodos siguientes se usan con el [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto:</span><span class="sxs-lookup"><span data-stu-id="ac354-147">The following methods are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="ac354-148">Método</span><span class="sxs-lookup"><span data-stu-id="ac354-148">Method</span></span> | <span data-ttu-id="ac354-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac354-149">Description</span></span>
:-------- | :----------
[<span data-ttu-id="ac354-150">cerrar</span><span class="sxs-lookup"><span data-stu-id="ac354-150">close</span></span>](https://msdn.microsoft.com/library/mt670636) | <span data-ttu-id="ac354-151">Cierra una notificación que se muestra.</span><span class="sxs-lookup"><span data-stu-id="ac354-151">Closes a displayed notification.</span></span>
[<span data-ttu-id="ac354-152">requestPermission</span><span class="sxs-lookup"><span data-stu-id="ac354-152">requestPermission</span></span>](https://msdn.microsoft.com/library/mt710824) | <span data-ttu-id="ac354-153">Solicita permiso al usuario para permitir que las notificaciones sean mostradas por el origen actual.</span><span class="sxs-lookup"><span data-stu-id="ac354-153">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>

## <span data-ttu-id="ac354-154">Permisos de notificación</span><span class="sxs-lookup"><span data-stu-id="ac354-154">Notification permissions</span></span>

<span data-ttu-id="ac354-155">Microsoft Edge permite a los usuarios administrar los permisos de notificaciones para cada dominio de sitio web específico.</span><span class="sxs-lookup"><span data-stu-id="ac354-155">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span> <span data-ttu-id="ac354-156">El usuario puede seleccionar "sí" o "no" cuando el dominio lo solicite para permitirle Mostrar notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ac354-156">It's up to the user to either select "Yes" or "No" when asked by the domain to let it show notifications.</span></span> <span data-ttu-id="ac354-157">El [`requestPermission`](https://msdn.microsoft.com/library/mt710824) método se usa para indicar el estado de los permisos como `granted` , `denied` o `default` .</span><span class="sxs-lookup"><span data-stu-id="ac354-157">The [`requestPermission`](https://msdn.microsoft.com/library/mt710824) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span> <span data-ttu-id="ac354-158">Un valor de `default` indica que el usuario no ha tomado una decisión, que se ve como equivalente `denied` .</span><span class="sxs-lookup"><span data-stu-id="ac354-158">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>




## <span data-ttu-id="ac354-159">Referencia de la API</span><span class="sxs-lookup"><span data-stu-id="ac354-159">API reference</span></span>

[<span data-ttu-id="ac354-160">Notificaciones Web</span><span class="sxs-lookup"><span data-stu-id="ac354-160">Web Notifications</span></span>](https://msdn.microsoft.com/library/mt710827)

## <span data-ttu-id="ac354-161">Estadístico</span><span class="sxs-lookup"><span data-stu-id="ac354-161">Specification</span></span>

[<span data-ttu-id="ac354-162">Notificaciones Web</span><span class="sxs-lookup"><span data-stu-id="ac354-162">Web Notifications</span></span>](https://notifications.spec.whatwg.org)

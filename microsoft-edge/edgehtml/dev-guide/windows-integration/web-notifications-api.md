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
# API de notificaciones Web  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

La API de notificaciones web permite a los sitios web enviar notificaciones de usuarios fuera del contexto de una página web dentro del explorador Microsoft Edge.  Un ejemplo de esta característica en acción sería con una aplicación de mensajería como Skype.  Cuando un usuario recibe un mensaje nuevo, aparece una notificación en el escritorio para avisarle del mensaje.  Las notificaciones Web se integran completamente con la plataforma de notificación y el centro de actividades de Windows 10.  

## Crear una notificación  

En el CodePen siguiente se crea una notificación de Skype ficticia haciendo que el objeto de [notificación](https://msdn.microsoft.com/library/mt710818) se establezca con las opciones de [título](https://msdn.microsoft.com/library/mt710826), [icono](https://msdn.microsoft.com/library/mt710814)y [cuerpo](https://msdn.microsoft.com/library/mt710811) :  

<iframe height='295' scrolling='no' title='Notificaciones Web' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Vea las <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notificaciones web del lápiz de </a> documentos de Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) en <a href='https://codepen.io'> CodePen </a> .</iframe>  

Es muy recomendable especificar un **icono** para cada notificación.  Esto no solo mejora una notificación desde un punto de vista de la interfaz de usuario, sino que también ayuda a alertar a los usuarios de dónde se envían las notificaciones.  

Vea el siguiente vídeo para obtener un tutorial sobre la creación de una notificación web y para ver su comportamiento en Windows 10.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### Propiedades de notificación  

Las notificaciones se pueden establecer con las siguientes propiedades:  

:::row:::
   :::column span="1":::
      [body](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      Texto del cuerpo de la notificación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [dir](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      La dirección del texto de la notificación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [icon](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      La dirección URL de la notificación que se usa para su icono.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Moreno](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      El idioma de la notificación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [permiso](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      El permiso para mostrar la notificación actual que el usuario ha concedido para el origen actual.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [tag](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      La etiqueta de la notificación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [title](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      El título de la notificación.  
   :::column-end:::
:::row-end:::  

### Eventos de notificación  

Los eventos siguientes se usan con el objeto de [notificación](https://developer.mozilla.org/docs/Web/API/Notification) :  

:::row:::
   :::column span="1":::
      [OnClick](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      Se desencadena cuando el usuario hace clic en una notificación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [OnClose](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      Se desencadena cuando el usuario cierra una notificación o se produce un tiempo de espera automático.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [OnError](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      Se desencadena cuando se produce un error durante la administración de una notificación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Mostrar](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      Se desencadena cuando se muestra una notificación.  
   :::column-end:::
:::row-end:::  

### Métodos de notificación  

Los métodos siguientes se usan con el objeto [Notification](https://developer.mozilla.org/docs/Web/API/Notification) :  

:::row:::
   :::column span="1":::
      [cerrar](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      Cierra una notificación que se muestra.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      Solicita permiso al usuario para permitir que las notificaciones sean mostradas por el origen actual.  
   :::column-end:::
:::row-end:::  

## Permisos de notificación  

Microsoft Edge permite a los usuarios administrar los permisos de notificaciones para cada dominio de sitio web específico.  El usuario puede seleccionar **sí** o **no** cuando lo solicite el dominio para permitirle Mostrar notificaciones.  El método [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) se usa para indicar el estado de los permisos como `granted` , `denied` o `default` .  Un valor de `default` indica que el usuario no ha tomado una decisión, que se ve como equivalente `denied` .  

## Referencia de las API  

[Notificaciones Web](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## Estadístico  

[Notificaciones Web](https://notifications.spec.whatwg.org)  

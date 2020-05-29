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
# API de notificaciones Web

La API de notificaciones web permite a los sitios web enviar notificaciones de usuarios fuera del contexto de una página web dentro del explorador Microsoft Edge. Un ejemplo de esta característica en acción sería con una aplicación de mensajería como Skype. Cuando un usuario recibe un mensaje nuevo, aparece una notificación en el escritorio para avisarle del mensaje. Las notificaciones Web se integran completamente con la plataforma de notificación y el centro de actividades de Windows 10. 

## Crear una notificación

En el CodePen siguiente se crea una notificación de Skype ficticia haciendo un [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto con el [`title`](https://msdn.microsoft.com/library/mt710826) , el y el conjunto de [`icon`](https://msdn.microsoft.com/library/mt710814) [`body`](https://msdn.microsoft.com/library/mt710811) Opciones:


<iframe height='295' scrolling='no' title='Notificaciones Web' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Vea las <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> notificaciones web del lápiz de </a> documentos de Microsoft Edge ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) en <a href='https://codepen.io'> CodePen </a> .
</iframe>

Se recomienda especificar un nombre `icon` para cada notificación. Esto no solo mejora una notificación desde un punto de vista de la interfaz de usuario, sino que también ayuda a alertar a los usuarios de dónde se envían las notificaciones.

Vea el siguiente vídeo para obtener un tutorial sobre la creación de una notificación web y para ver su comportamiento en Windows 10.


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### Propiedades de notificación

Las notificaciones se pueden establecer con las siguientes opciones:

Propiedad | Descripción
:-------- | :----------
[body](https://msdn.microsoft.com/library/mt710811) | Texto del cuerpo de la notificación.
[dir](https://msdn.microsoft.com/library/mt710813) | La dirección del texto de la notificación.
[icon](https://msdn.microsoft.com/library/mt710814) | La dirección URL de la notificación que se usa para su icono.
[Moreno](https://msdn.microsoft.com/library/mt710815) | El idioma de la notificación.
[permiso](https://msdn.microsoft.com/library/mt670637) | El permiso para mostrar la notificación actual que el usuario ha concedido para el origen actual.
[tag](https://msdn.microsoft.com/library/mt710825) | La etiqueta de la notificación.
[title](https://msdn.microsoft.com/library/mt710826) | El título de la notificación.

### Eventos de notificación

Los eventos siguientes se usan con el [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto:

Evento | Descripción
:-------- | :----------
[OnClick](https://msdn.microsoft.com/library/mt712180) | Se desencadena cuando el usuario hace clic en una notificación.
[OnClose](https://msdn.microsoft.com/library/mt712178) | Se desencadena cuando el usuario cierra una notificación o se produce un tiempo de espera automático.
[OnError](https://msdn.microsoft.com/library/mt712181) | Se desencadena cuando se produce un error durante la administración de una notificación.
[Mostrar](https://msdn.microsoft.com/library/mt712182) | Se desencadena cuando se muestra una notificación.

### Métodos de notificación

Los métodos siguientes se usan con el [`Notification`](https://msdn.microsoft.com/library/mt710818) objeto:

Método | Descripción
:-------- | :----------
[cerrar](https://msdn.microsoft.com/library/mt670636) | Cierra una notificación que se muestra.
[requestPermission](https://msdn.microsoft.com/library/mt710824) | Solicita permiso al usuario para permitir que las notificaciones sean mostradas por el origen actual.

## Permisos de notificación

Microsoft Edge permite a los usuarios administrar los permisos de notificaciones para cada dominio de sitio web específico. El usuario puede seleccionar "sí" o "no" cuando el dominio lo solicite para permitirle Mostrar notificaciones. El [`requestPermission`](https://msdn.microsoft.com/library/mt710824) método se usa para indicar el estado de los permisos como `granted` , `denied` o `default` . Un valor de `default` indica que el usuario no ha tomado una decisión, que se ve como equivalente `denied` .




## Referencia de la API

[Notificaciones Web](https://msdn.microsoft.com/library/mt710827)

## Estadístico

[Notificaciones Web](https://notifications.spec.whatwg.org)

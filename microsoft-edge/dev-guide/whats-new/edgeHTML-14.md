---
description: Esta página proporciona una descripción general de las novedades de EdgeHTML 14.
title: Nuevas características y API en EdgeHTML 14
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 7f3fcbbf84873fbf0851e1652bde48632e6c4378
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941910"
---
# Novedades de EdgeHTML 14  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Estos son los cambios que se han enviado con EdgeHTML 14, a partir de la [actualización de aniversario de Windows 10](https://blogs.windows.com/windowsexperience/2016/06/29) \ (08/2016, compilación 14393 \).  Para obtener información general sobre los cambios en el explorador general de Microsoft Edge, consulte [Introducción a EdgeHTML 14 con la actualización de aniversario de Windows 10](https://blogs.windows.com/msedgedev/2016/08/04).  

Este es el vínculo permanente de la siguiente lista de cambios: [https://aka.ms/devguide_edgehtml_14](./edgehtml-14.md) .  

## Nuevas características  

### Extensions  

Las extensiones son pequeños programas que se pueden usar para agregar nuevas características a Microsoft Edge o modificar la funcionalidad existente.  Las extensiones están pensadas para mejorar la experiencia de exploración diaria de un usuario al proporcionar características de nicho que son importantes para las audiencias de destino.  Microsoft Edge admite un modelo de extensión basado en HTML, JavaScript y CSS.  Este nuevo modelo es compatible con Chrome, lo que significa que los programadores de extensiones de Chrome existentes podrán migrar sus extensiones a Microsoft Edge con cambios mínimos.  Para obtener más información, consulte los documentos para desarrolladores de [Microsoft Edge Extensions](../../extensions/index.md) .  

### API de captura  
La [API fetch](https://fetch.spec.whatwg.org#fetch-api) usa el `fetch` método de obtención de recursos.  En el pasado, se logró `XMLHttpRequest` .  La recuperación no solo es más sencilla, sino que también proporciona acceso de nivel inferior a las solicitudes y las respuestas.  Obtenga más información sobre la API de Fetch en la entrada de blog de Microsoft Edge, [Fetch (o las limitaciones innegables de XHR)](https://blogs.windows.com/msedgedev/2016/05/24).  

### JavaScript  

EdgeHTML 14 ofrece varias características nuevas y experimentales para Chakra, el motor de JavaScript que enciende Microsoft Edge:  

#### Nuevas características  

Activado de forma predeterminada  

*   [Parámetros predeterminados](https://developer.microsoft.com/microsoft-edge/platform/status/defaultparameteres6) \ (ES2015 \)
*   [Operador exponencial](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016) \ (ES2016 \)
*   [Array. prototype. incluye](https://developer.microsoft.com/microsoft-edge/platform/status/arrayprototypeincludeses2016) \ (ES2016 \)
*   [Object. Values](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/values) y [Object. Entries](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object/entries) \ (ES2017 \)  

#### Características experimentales de JavaScript  

Habilitado con `about:flags`  

*   [Modules](https://blogs.windows.com/msedgedev/2016/05/17) \ (ES2015 \)  
*   [Async/Await](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctionses2016) \ (ES2017 \)  
*   [Símbolos de Regex](https://developer.microsoft.com/microsoft-edge/platform/status/regexpbuiltinses6) \ (ES2015 \)  

Para obtener más información, consulte la [vista previa de los módulos de ES6 y mucho más de ES2015, ES2016 y más allá,](https://blogs.windows.com/msedgedev/2016/05/17) y el [código asincrónico es más fácil con ES2016 compatibilidad con funciones asincrónicas de Chakra y Microsoft Edge](https://blogs.windows.com/msedgedev/2015/09/30).  

### API de autenticación Web  

API Web de FIDO 2,0  

La API \ (anteriormente FIDO 2,0 \) en Microsoft Edge permite a las aplicaciones web usar [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) biometría para la autenticación de usuarios, de modo que usted y sus usuarios puedan evitar todos los problemas y riesgos de la administración de contraseñas, entre los que se incluyen averiguaciones de contraseñas, suplantación de identidad y ataques de keylogging.  La implementación actual de Microsoft Edge \ ( `ms-` precorregido \) se basa en un borrador anterior de la especificación de autenticación Web y es probable que cambie en el futuro.  Más información sobre la autenticación Web: la  [autenticación Web y Windows Hello](../windows-integration/web-authentication.md).

### Notificaciones Web
Las notificaciones web permiten a los sitios Mostrar notificaciones para avisar a los usuarios fuera del contexto de la página web y del explorador, mantener a los usuarios informados de mensajes nuevos o alertas y permitir que los sitios mejoren la participación de los usuarios.  Las notificaciones Web en Microsoft Edge están totalmente integradas con la plataforma de notificaciones y el centro de actividades en Windows 10, lo que proporciona una experiencia coherente con otras aplicaciones del sistema y controla fácilmente los permisos y las horas de silencio.  Para obtener más información, consulta [notificaciones Web en Microsoft Edge](https://blogs.windows.com/msedgedev/2016/05/16) .  

### API de voz web
La [API de voz para web](https://dvcs.w3.org/hg/speech-api/raw-file/tip/speechapi.html) es una API de JavaScript formada por dos partes: reconocimiento de voz y síntesis de voz \ (o texto a voz \).  En este momento, Microsoft Edge solo admite la síntesis de voz.  La síntesis de voz incluye la conversión de texto a voz que un usuario escucha a través de los altavoces.  Consulte el artículo de la guía para desarrolladores de [voz: síntesis de voz](https://developer.mozilla.org/docs/Web/API/Web_Speech_API) para obtener más información.  

## Nuevas API en EdgeHTML 14

Esta es la lista completa de las API nuevas en EdgeHTML 14.  Se muestran en el formato de `[interface name].[api name]` .  

<iframe height='585' scrolling='no' title='Nuevas API en EdgeHTML 14' src='//codepen.io/MSEdgeDev/embed/oWMEPE/?height=585&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulta las <a href='https://codepen.io/MSEdgeDev/pen/oWMEPE/'> nuevas API de Pen en EdgeHTML 14 de </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='https://codepen.io'> CodePen </a> .</iframe>  

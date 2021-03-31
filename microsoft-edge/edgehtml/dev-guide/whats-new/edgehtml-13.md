---
description: Esta página proporciona una descripción general de las novedades de EdgeHTML 13.
title: Nuevas características y API en EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2119e576a637d5f78e073f49a3cb1868a7ce1ca4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236560"
---
# Novedades de EdgeHTML 13  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Estos son los cambios que se han enviado con EdgeHTML 13, el motor que enciende el explorador Microsoft Edge en la [primera actualización principal](https://blogs.windows.com/windowsexperience/2015/11/12) para Windows 10 \(11/2015, compilación 10586 \).  Para obtener información general sobre los cambios en el explorador general de Microsoft Edge, consulta [Introducción a EdgeHTML 13, nuestra primera actualización de plataforma para Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).  

Este es el vínculo permanente de la siguiente lista de cambios:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) .  

## Características  

### CSS  

EdgeHTML 13 es compatible con las nuevas características de CSS, entre las que se incluyen:  

*   [Pseudo-clases de mutabilidad CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [Pseudo-clases de rango CSS](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   Palabras clave [iniciales](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) y no [ANULAdas](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) de CSS  

### Extensiones de medios cifrados  

Microsoft Edge ahora es compatible con las nuevas API de [extensiones de medios cifradas sin](https://w3.org/TR/encrypted-media) prefijos.  Extensiones de medios cifrados \(EME \) extiende los elementos de audio y vídeo para habilitar el contenido protegido de administración de derechos digitales \(DRM \) sin usar complementos.  Más información sobre EME:  [extensiones de medios cifradas](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).  

### Gráficos  

EdgeHTML 13 presenta las siguientes actualizaciones de gráficos:  

*   [Elipse del lienzo](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [Modos de fusión de Canvas](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> Element](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [Contenido externo SVG](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### JavaScript  

EdgeHTML 13 incluye [mejoras importantes y compatibilidad con nuevas características en Chakra](https://blogs.windows.com/msedgedev/2015/09/30), el motor de JavaScript que enciende Microsoft Edge, que incluye:  

#### Nuevas características  

Activado de forma predeterminada  

*   [asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) habilitado de forma predeterminada \([entrada de blog](https://blogs.windows.com/msedgedev/2015/11/10), [Demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)  
*   [Clases](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015 \)  

#### Características experimentales de JavaScript  

Habilitado con `about:flags`  

*   [Funciones asincrónicas](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016 \)  
*   [Operador exponencial](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016 \)  
*   [Desestructurar](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015 \)  

### Entrada de usuario  

Las siguientes características presentadas en EdgeHTML 13 mejoran la entrada de los usuarios:  

*   [\<meter\> Element](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [controlador de eventos no válido para el documento y la ventana de elementos](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### Bloqueo de puntero  

Microsoft Edge ahora es compatible con la API de bloqueo de puntero \(denominado previamente bloqueo de mouse \) para acceder a movimiento sin formato del mouse, bloquear el destino de los eventos del mouse a un solo elemento, eliminando los límites de la distancia hasta la que se puede mover el mouse en una sola dirección y quitando el cursor de la vista.  

## Nuevas API en EdgeHTML 13  

Esta es la lista completa de las API nuevas en EdgeHTML 13.  Se muestran en el formato de `[interface name].[api name]` .  

<iframe height='584' scrolling='no' title='Nuevas API en EdgeHTML 13' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'>Consulta las <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> nuevas API de Pen en EdgeHTML 13 de </a> docs Edge ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) en <a href='http://codepen.io'> CodePen </a> .</iframe>  

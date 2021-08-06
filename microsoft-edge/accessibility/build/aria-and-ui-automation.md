---
ms.assetid: ffd1bc60-2ef1-4f11-8156-b63544cede77
description: Obtén información Microsoft Edge reconocer la información de ARIA y, a continuación, exponerla a tecnologías de asistencia que luego pueden usar las API de automatización de la interfaz de usuario de Microsoft.
title: 'Accesibilidad: automatización de ARIA e interfaz de usuario'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, edge, desarrollo web, ARIA, desarrollador, UIA, Automatización de la interfaz de usuario
ms.custom: seodec18
ms.openlocfilehash: bfe67fa9a869cea8e7f573c0818441650225f7e509bdfb4e41479aee32dec941
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11799649"
---
# <a name="aria-and-ui-automation-in-microsoft-edge"></a>Automatización de ARIA y ui en Microsoft Edge

W3C define Aplicaciones de Internet enriquecidas accesibles (ARIA) como una sintaxis para hacer accesible el contenido web dinámico y la interfaz de usuario personalizada. Microsoft Edge reconoce la información de roles, estados y propiedades de ARIA y la expone a tecnologías de asistencia, que a su vez pueden usar las API de automatización de la interfaz de usuario de [Microsoft](https://blogs.msdn.microsoft.com/winuiautomation/) para recuperar la información.

Visite [HTML5Accessibility para](https://html5accessibility.com) obtener información sobre las nuevas características html5 que son compatibles de forma Microsoft Edge.

El Microsoft Edge de representación (EdgeHTML) crea una proyección accesible de páginas web, conforme a las siguientes especificaciones de W3C:

1. La [especificación de asignaciones de la API](https://w3.org/TR/html-aam-1.0/) de accesibilidad HTML define cómo se asignan los elementos HTML y los atributos a objetos ARIA y automatización de la interfaz de usuario.
   * [Borrador de trabajo:](https://w3.org/TR/html-aam-1.0/) versión estable de la especificación
   * [Borrador del editor:](https://w3c.github.io/html-aam/) trabajo en curso. Tenga en cuenta que aunque esta especificación tiene los cambios más recientes, es posible que los cambios no estén disponibles en Microsoft Edge momento.


2. La [especificación asignaciones de API](https://w3.org/TR/core-aam-1.1/) de accesibilidad principal define los principios generales para crear el árbol de accesibilidad y asignar elementos y atributos de ARIA a objetos de automatización de la interfaz de usuario.
   * [Borrador de trabajo:](https://w3.org/TR/core-aam-1.1/) versión estable de la especificación
   * [Borrador del editor:](https://w3c.github.io/core-aam/) trabajo en curso. Tenga en cuenta que aunque esta especificación tiene los cambios más recientes, es posible que los cambios no estén disponibles en Microsoft Edge momento.  

3. La [especificación Accessible Name and Description: Computation and API Mappings](https://w3.org/TR/accname-aam-1.1/) define cómo calcular el nombre y la descripción de los objetos accesibles dados los valores html y de los elementos y atributos ARIA disponibles para los elementos accesibles.
   * [Borrador de trabajo:](https://w3.org/TR/accname-aam-1.1/) versión estable de la especificación  
   * [Borrador del editor:](https://w3c.github.io/accname/) trabajo en curso. Tenga en cuenta que aunque esta especificación tiene los cambios más recientes, es posible que los cambios no estén disponibles en Microsoft Edge momento.   

Para obtener más información acerca de la arquitectura de accesibilidad en Microsoft Edge, consulte la entrada de blog Creación de [una plataforma web más](https://blogs.windows.com/msedgedev/2016/04/20/building-a-more-accessible-web-platform/) accesible.  Para obtener ejemplos de cómo la nueva arquitectura mejora la experiencia del usuario final y, específicamente, cómo define el marcado la experiencia de navegar con tecnologías de asistencia como lectores de pantalla, visite [Building a more accessible user experience with HTML5 and UIA](https://blogs.windows.com/msedgedev/2016/05/12/accessible-ux-with-html5-and-uia/).

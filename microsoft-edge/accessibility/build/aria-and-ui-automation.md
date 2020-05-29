---
ms.assetid: ffd1bc60-2ef1-4f11-8156-b63544cede77
description: Más información sobre cómo Microsoft Edge puede reconocer la información ARIA y, a continuación, exponerla en tecnologías de asistencia que pueden usar las API de automatización de la interfaz de usuario de Microsoft.
title: 'Accesibilidad: ARIA y automatización de la interfaz de usuario'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, Edge, desarrollo web, ARIA, desarrollador, UIA, automatización de la interfaz de usuario
ms.custom: seodec18
ms.openlocfilehash: 2fcc8160c830b5a62d8023a5cb7cc9df376c49ca
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572943"
---
# ARIA y automatización de la interfaz de usuario en Microsoft Edge

El W3C define las aplicaciones de Internet enriquecidas accesibles (ARIA) como una sintaxis para que el contenido Web dinámico y la interfaz de usuario personalizada sean accesibles. Microsoft Edge reconoce el rol de ARIA, el estado y la información de propiedad y lo expone a tecnologías de asistencia, que a su vez pueden usar las API de automatización de la [interfaz de usuario de Microsoft](https://blogs.msdn.microsoft.com/winuiautomation/) para recuperar la información.

Visita [HTML5Accessibility](https://html5accessibility.com) para obtener información sobre qué nuevas características de HTML5 son compatibles con Microsoft Edge.

El motor de representación de Microsoft Edge (EdgeHTML) crea una proyección accesible de páginas web, conforme a las siguientes especificaciones del W3C:

1. La especificación de las asignaciones de la [API de accesibilidad de HTML](https://w3.org/TR/html-aam-1.0/) define cómo se asignan los atributos y elementos HTML a los objetos de automatización Aria y UI.
   * Versión estable de [borrador](https://w3.org/TR/html-aam-1.0/) de la especificación
   * [Borrador del](https://w3c.github.io/html-aam/) trabajo en curso del editor. Ten en cuenta que, aunque esta especificación tiene los cambios más recientes, es posible que los cambios aún no estén disponibles en Microsoft Edge.


2. La especificación básica de las [asignaciones de API de accesibilidad](https://w3.org/TR/core-aam-1.1/) define los principios generales para crear el árbol de accesibilidad y asignar atributos y elementos Aria a los objetos de automatización de la interfaz de usuario.
   * Versión estable de [borrador](https://w3.org/TR/core-aam-1.1/) de la especificación
   * [Borrador del](https://w3c.github.io/core-aam/) trabajo en curso del editor. Ten en cuenta que, aunque esta especificación tiene los cambios más recientes, es posible que los cambios aún no estén disponibles en Microsoft Edge.  

3. La especificación [nombre y descripción accesibles: cálculo y asignaciones de API](https://w3.org/TR/accname-aam-1.1/) define cómo se calculan el nombre y la descripción de los objetos accesibles dados los valores de atributos y elementos HTML y Aria disponibles para los elementos accesibles.
   * Versión estable de [borrador](https://w3.org/TR/accname-aam-1.1/) de la especificación  
   * [Borrador del](https://w3c.github.io/accname/) trabajo en curso del editor. Ten en cuenta que, aunque esta especificación tiene los cambios más recientes, es posible que los cambios aún no estén disponibles en Microsoft Edge.   

Para obtener más información sobre la arquitectura de accesibilidad en Microsoft Edge, consulte el tema sobre cómo crear una entrada de blog de [plataforma web más accesible](https://blogs.windows.com/msedgedev/2016/04/20/building-a-more-accessible-web-platform/) .  Para obtener ejemplos de cómo la nueva arquitectura mejora la experiencia del usuario final, y específicamente cómo el marcado define la experiencia de navegar con tecnologías de asistencia como lectores de pantalla, visite [crear una experiencia de usuario más accesible con HTML5 y UIA](https://blogs.windows.com/msedgedev/2016/05/12/accessible-ux-with-html5-and-uia/).

---
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
description: Aprenda a crear, diseñar y probar sitios web accesibles en Microsoft Edge.
title: Accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, Edge, desarrollo web, ARIA, desarrollador, UIA, automatización de la interfaz de usuario
ms.openlocfilehash: 6ad95e9c250aa6a4a61ca09470cea86efd715427
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583108"
---
# Accesibilidad  

> "\ [T \] el impacto de la incapacidad se modifica radicalmente en la web, ya que la web elimina las barreras de comunicación e interacción que muchas personas se enfrentan en el mundo físico." [(Accesibilidad | RELATIVA][W3CAccessibility]  

La [Organización Mundial][WHODisabilities] de la salud define la incapacidad como "no coincidencia en la interacción entre las características del cuerpo de una persona y las características del entorno en el que viven".  Las discapacidades van desde discapacidades por situaciones, como una movilidad limitada mientras mantienen un bebé o una luz solar en un teléfono, a otras deficiencias físicas, auditivas, visuales o de edad.  

El diseño de sitios web y otras tecnologías para la inclusión crea una experiencia divertida por parte de cada usuario.  El diseño inclusivo y la accesibilidad web facultan y ayudan a todo el mundo a usar la Web.  

Estos son algunos procedimientos recomendados, ejemplos de código y otros recursos para obtener más información sobre cómo [diseñar][AccessibilityDesign], [crear][AccessibilityBuild]y [probar][AccessibilityTest] sitios web accesibles en Microsoft Edge.  

## Accesibilidad en Microsoft Edge  

En Microsoft Edge, hemos introducido la moderna API de automatización de la [interfaz de usuario][WindowsWin32AutoEntryui] (UIA API \).  El cambio a UIA era una gran inversión en la accesibilidad del explorador y constituye la base para una experiencia web más inclusiva para los usuarios que dependen de la tecnología de asistencia en Windows 10.  Los usuarios también se benefician de la naturaleza de la perenne del motor de cromo.  

El sistema de accesibilidad de Microsoft Edge es compatible de forma inherente con los estándares web modernos, incluidos ARIA, HTML5 y CSS3.  El siguiente diagrama de la canalización de explorador simplificada sigue el contenido de las páginas web a una capa de presentación accesible.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="El contenido transformado en el modelo de motor se proyecta en vistas visuales y de accesibilidad que se presentan como una presentación visual o accesible.":::
   Figura 1.  El contenido transformado en el modelo de motor se proyecta en vistas visuales y de accesibilidad que se presentan como una presentación visual o accesible.
:::image-end:::

<!--![Figure 1.  Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation][ImageAccessibilityArchitecture]  -->  

El equipo de Microsoft Edge funciona con el W3C y otros proveedores de exploradores de manera continua para garantizar que las nuevas características de plataforma web tengan la accesibilidad integrada suficiente.  

Para obtener información sobre las nuevas características de HTML5 compatibles con Microsoft Edge, visite [HTML5Accessibility][HTML5Accessibility].  

## Recursos  

#### Blog de automatización de la interfaz de usuario de Microsoft Windows  

El [blog de automatización de la interfaz de usuario de Microsoft Windows][ArchiveBlogsWinuiautomation] incluye temas relacionados con la API de automatización de Windows.  

#### Iniciativa de accesibilidad para web (WAI)  

La [iniciativa de accesibilidad web (WAI)][W3CWaiHome] proporcionó BT el W3C es un esfuerzo para ayudarle a mejorar la accesibilidad de la Web.  El sitio proporciona una variedad de recursos para [empezar a usar la accesibilidad web][W3CWaiGettingstartedOverview], [diseñar la inclusión][W3CWaiFundamentals], [tutoriales y presentaciones][W3CWaiTeachAdvocate], entre otras.  


<!-- image links -->  

<!--[ImageAccessibilityArchitecture]: ./media/accessibilityarchitecture.png "Figure 1: Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation"  -->  

<!-- links -->  

[AccessibilityBuild]: ./accessibility/build.md "Creación de sitios web accesibles"  
[AccessibilityDesign]: ./accessibility/design.md "Diseñar sitios web accesibles"  
[AccessibilityTest]: ./accessibility/test.md "Pruebas de accesibilidad"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Automatización de la interfaz de usuario"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog de automatización de la interfaz de usuario de Microsoft Windows"  

[HTML5Accessibility]: https://html5accessibility.com "Accesibilidad de HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Accesibilidad | RELATIVA"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Introducción a la accesibilidad web | Iniciativa de accesibilidad web (WAI) | RELATIVA"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Introducción: hacer que un sitio web sea accesible | Iniciativa de accesibilidad web (WAI) | RELATIVA"  
[W3CWaiHome]: https://w3.org/wai "Iniciativa de accesibilidad web (WAI) | RELATIVA"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Información general de enseñar y abogar | Iniciativa de accesibilidad web (WAI) | RELATIVA"  

[WHODisabilities]: https://who.int/topics/disabilities "Discapacidades | CON"  


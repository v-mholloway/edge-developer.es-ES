---
description: Obtenga información sobre cómo crear, diseñar y probar sitios web accesibles en Microsoft Edge.
title: Accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 1e5c42a7-4604-46ac-ad7b-a65390e5b36a
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, edge, desarrollo web, ARIA, desarrollador, UIA, Automatización de la interfaz de usuario
ms.openlocfilehash: ae2b0a876b60e0475e283cc52ffd14275fc32aba
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236054"
---
# Información general sobre accesibilidad  

> "\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world." [(Accesibilidad | W3C)][W3CAccessibility]  

La [Organización Mundial de][WHODisabilities] la Salud define la discapacidad como "un error de interacción entre las características del cuerpo de una persona y las características del entorno en el que viven".  Las discapacidades van desde discapacidades situacionales, como la movilidad limitada mientras se mantiene un niño o luz solar brillante en un teléfono, hasta otras discapacidades físicas, auditivas, visuales o relacionadas con la edad.  

El diseño de sitios web y otras tecnologías para su inclusión crea una experiencia agradable para cada persona.  El diseño inclusivo y la accesibilidad web permiten y ayudan a todos a usar la web.  

Estos son algunos procedimientos recomendados, ejemplos de código y [][AccessibilityBuild]recursos adicionales para obtener más información sobre el [diseño,][AccessibilityDesign]la creación y las pruebas de sitios web accesibles en Microsoft Edge. [][AccessibilityTest]  

##  <a name="accessibility-in-microsoft-edge"></a>Accesibilidad en Microsoft Edge  

En Microsoft Edge, presentamos la [API][WindowsWin32AutoEntryui] moderna de automatización de la interfaz de usuario \(API de UIA\).  El cambio a UIA fue una inversión importante en accesibilidad de exploradores, y se asoma la base para una experiencia web más inclusiva para los usuarios que dependen de la tecnología de asistencia en Windows 10.  Los usuarios también se benefician de la naturaleza perenne del Chromium motor.  

El sistema de accesibilidad de Microsoft Edge admite inherentemente estándares web modernos, incluidos ARIA, HTML5 y CSS3.  El siguiente diagrama de la canalización del explorador simplificado sigue el contenido de la página web a una capa de presentación accesible.  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="El contenido transformado en el modelo de motor se proyecta en vistas visuales y de accesibilidad que se presentan como presentación visual o accesible":::
   El contenido transformado en el modelo de motor se proyecta en vistas visuales y de accesibilidad que se presentan como presentación visual o accesible  
:::image-end:::  

El Microsoft Edge trabaja con W3C y otros proveedores de exploradores de forma continua para garantizar que las nuevas características de la plataforma web tengan suficiente accesibilidad integrada.  

Para obtener información sobre a qué nuevas características html5 se admiten de forma Microsoft Edge, vaya a [HTML5Accessibility][HTML5Accessibility].  

##  <a name="resources"></a>Recursos  

#### Blog Windows automatización de la interfaz de usuario de Microsoft  

El [blog Windows automatización de la interfaz de][ArchiveBlogsWinuiautomation] usuario de Microsoft trata temas relacionados con la API Windows automatización.  

#### Iniciativa de accesibilidad web (WAI)  

The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.  El sitio proporciona una variedad de recursos para Introducción a la accesibilidad [web,][W3CWaiGettingstartedOverview]diseño para la [inclusión,][W3CWaiFundamentals]tutoriales y [presentaciones,][W3CWaiTeachAdvocate]etc.  

<!-- links -->  

[AccessibilityBuild]: ./build/index.md "Creación de sitios web accesibles | Microsoft Doc"  
[AccessibilityDesign]: ./design.md "Diseño de sitios web accesibles | Microsoft Doc"  
[AccessibilityTest]: ./test.md "Pruebas de accesibilidad | Microsoft Docs"  

[WindowsWin32AutoEntryui]: /windows/win32/winauto/entry-uiauto-win32 "Automatización de la interfaz de usuario | Microsoft Doc"  

[ArchiveBlogsWinuiautomation]: /archive/blogs/winuiautomation/ "Blog Windows automatización de la interfaz de usuario de Microsoft | Microsoft Doc"  

[HTML5Accessibility]: https://html5accessibility.com "Accesibilidad HTML5"  

[W3CAccessibility]: https://w3.org/standards/webdesign/accessibility "Accesibilidad | W3C"  
[W3CWaiFundamentals]: https://w3.org/wai/fundamentals/accessibility-intro "Introducción a la accesibilidad web | Iniciativa de accesibilidad web (WAI) | W3C"  
[W3CWaiGettingstartedOverview]: https://w3.org/wai/gettingstarted/Overview "Introducción: Hacer que un sitio web sea accesible | Iniciativa de accesibilidad web (WAI) | W3C"  
[W3CWaiHome]: https://w3.org/wai "Iniciativa de accesibilidad web (WAI) | W3C"  
[W3CWaiTeachAdvocate]: https://w3.org/wai/teach-advocate "Información general sobre profesores y | Iniciativa de accesibilidad web (WAI) | W3C"  

[WHODisabilities]: https://who.int/topics/disabilities "Discapacidades | Quién"  


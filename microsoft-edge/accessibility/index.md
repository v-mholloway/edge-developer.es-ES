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
# <span data-ttu-id="c4b08-104">Información general sobre accesibilidad</span><span class="sxs-lookup"><span data-stu-id="c4b08-104">Accessibility overview</span></span>  

> <span data-ttu-id="c4b08-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span><span class="sxs-lookup"><span data-stu-id="c4b08-105">"\[T\]he impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world."</span></span> [<span data-ttu-id="c4b08-106">(Accesibilidad | W3C)</span><span class="sxs-lookup"><span data-stu-id="c4b08-106">(Accessibility | W3C)</span></span>][W3CAccessibility]  

<span data-ttu-id="c4b08-107">La [Organización Mundial de][WHODisabilities] la Salud define la discapacidad como "un error de interacción entre las características del cuerpo de una persona y las características del entorno en el que viven".</span><span class="sxs-lookup"><span data-stu-id="c4b08-107">The [World Health Organization][WHODisabilities] defines disability as "a mismatch in interaction between the features of a person's body and the features of the environment in which they live".</span></span>  <span data-ttu-id="c4b08-108">Las discapacidades van desde discapacidades situacionales, como la movilidad limitada mientras se mantiene un niño o luz solar brillante en un teléfono, hasta otras discapacidades físicas, auditivas, visuales o relacionadas con la edad.</span><span class="sxs-lookup"><span data-stu-id="c4b08-108">Disabilities range from situational disabilities, like limited mobility while holding a baby or bright sunlight on a phone, to other physical, auditory, visual, or age-related impairments.</span></span>  

<span data-ttu-id="c4b08-109">El diseño de sitios web y otras tecnologías para su inclusión crea una experiencia agradable para cada persona.</span><span class="sxs-lookup"><span data-stu-id="c4b08-109">Designing websites and other technologies for inclusion creates an experience enjoyable by every person.</span></span>  <span data-ttu-id="c4b08-110">El diseño inclusivo y la accesibilidad web permiten y ayudan a todos a usar la web.</span><span class="sxs-lookup"><span data-stu-id="c4b08-110">Inclusive design and web accessibility empowers and assists everyone to use the web.</span></span>  

<span data-ttu-id="c4b08-111">Estos son algunos procedimientos recomendados, ejemplos de código y [][AccessibilityBuild]recursos adicionales para obtener más información sobre el [diseño,][AccessibilityDesign]la creación y las pruebas de sitios web accesibles en Microsoft Edge. [][AccessibilityTest]</span><span class="sxs-lookup"><span data-stu-id="c4b08-111">Here are some best practices, code samples, and further resources for you to learn more about [Designing][AccessibilityDesign], [Building][AccessibilityBuild], and [Testing][AccessibilityTest] accessible websites in Microsoft Edge.</span></span>  

## <span data-ttu-id="c4b08-112">Accesibilidad en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c4b08-112">Accessibility in Microsoft Edge</span></span>  

<span data-ttu-id="c4b08-113">En Microsoft Edge, presentamos la [API][WindowsWin32AutoEntryui] moderna de automatización de la interfaz de usuario \(API de UIA\).</span><span class="sxs-lookup"><span data-stu-id="c4b08-113">In Microsoft Edge, we introduced modern [UI Automation API][WindowsWin32AutoEntryui] \(UIA API\).</span></span>  <span data-ttu-id="c4b08-114">El cambio a UIA fue una inversión importante en accesibilidad de exploradores, y se asoma la base para una experiencia web más inclusiva para los usuarios que dependen de la tecnología de asistencia en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c4b08-114">The change to UIA was a major investment in browser accessibility, and it lays the foundation for a more inclusive web experience for users who depend on assistive technology in Windows 10.</span></span>  <span data-ttu-id="c4b08-115">Los usuarios también se benefician de la naturaleza perenne del Chromium motor.</span><span class="sxs-lookup"><span data-stu-id="c4b08-115">Users also benefit from the evergreen nature of the Chromium engine.</span></span>  

<span data-ttu-id="c4b08-116">El sistema de accesibilidad de Microsoft Edge admite inherentemente estándares web modernos, incluidos ARIA, HTML5 y CSS3.</span><span class="sxs-lookup"><span data-stu-id="c4b08-116">The accessibility system in Microsoft Edge inherently supports modern web standards including ARIA, HTML5, and CSS3.</span></span>  <span data-ttu-id="c4b08-117">El siguiente diagrama de la canalización del explorador simplificado sigue el contenido de la página web a una capa de presentación accesible.</span><span class="sxs-lookup"><span data-stu-id="c4b08-117">The following diagram of the simplified browser pipeline follows webpage content into an accessible presentation layer.</span></span>  

:::image type="complex" source="./media/accessibilityarchitecture.png" alt-text="El contenido transformado en el modelo de motor se proyecta en vistas visuales y de accesibilidad que se presentan como presentación visual o accesible":::
   <span data-ttu-id="c4b08-119">El contenido transformado en el modelo de motor se proyecta en vistas visuales y de accesibilidad que se presentan como presentación visual o accesible</span><span class="sxs-lookup"><span data-stu-id="c4b08-119">Content transformed to the engine model is projected into visual and accessibility views that are presented either as visual or accessible presentation</span></span>  
:::image-end:::  

<span data-ttu-id="c4b08-120">El Microsoft Edge trabaja con W3C y otros proveedores de exploradores de forma continua para garantizar que las nuevas características de la plataforma web tengan suficiente accesibilidad integrada.</span><span class="sxs-lookup"><span data-stu-id="c4b08-120">The Microsoft Edge team works with the W3C and other browser vendors on an ongoing basis to ensure that new web platform features have sufficient built-in accessibility.</span></span>  

<span data-ttu-id="c4b08-121">Para obtener información sobre a qué nuevas características html5 se admiten de forma Microsoft Edge, vaya a [HTML5Accessibility][HTML5Accessibility].</span><span class="sxs-lookup"><span data-stu-id="c4b08-121">For information on which new HTML5 features are accessibly supported by Microsoft Edge, navigate to [HTML5Accessibility][HTML5Accessibility].</span></span>  

## <span data-ttu-id="c4b08-122">Recursos</span><span class="sxs-lookup"><span data-stu-id="c4b08-122">Resources</span></span>  

#### <span data-ttu-id="c4b08-123">Blog Windows automatización de la interfaz de usuario de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c4b08-123">Microsoft Windows UI Automation Blog</span></span>  

<span data-ttu-id="c4b08-124">El [blog Windows automatización de la interfaz de][ArchiveBlogsWinuiautomation] usuario de Microsoft trata temas relacionados con la API Windows automatización.</span><span class="sxs-lookup"><span data-stu-id="c4b08-124">The [Microsoft Windows UI Automation blog][ArchiveBlogsWinuiautomation] covers topics related to the Windows Automation API.</span></span>  

#### <span data-ttu-id="c4b08-125">Iniciativa de accesibilidad web (WAI)</span><span class="sxs-lookup"><span data-stu-id="c4b08-125">Web Accessibility Initiative (WAI)</span></span>  

<span data-ttu-id="c4b08-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span><span class="sxs-lookup"><span data-stu-id="c4b08-126">The [Web Accessibility Initiative (WAI)][W3CWaiHome] provided bt the W3C is an effort to help improve the accessibility of the web.</span></span>  <span data-ttu-id="c4b08-127">El sitio proporciona una variedad de recursos para Introducción a la accesibilidad [web,][W3CWaiGettingstartedOverview]diseño para la [inclusión,][W3CWaiFundamentals]tutoriales y [presentaciones,][W3CWaiTeachAdvocate]etc.</span><span class="sxs-lookup"><span data-stu-id="c4b08-127">The site provides a variety of resources for [Getting Started with Web Accessibility][W3CWaiGettingstartedOverview], [Designing for Inclusion][W3CWaiFundamentals], [tutorials and presentations][W3CWaiTeachAdvocate], and more.</span></span>  

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


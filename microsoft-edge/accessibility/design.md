---
description: Obtenga información sobre los recursos para herramientas de diseño inclusivas y procedimientos recomendados.
title: 'Accesibilidad: diseño'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 8468f8e1-9f4a-426c-a969-76eab9419137
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, edge, desarrollo web, ARIA, desarrollador, UIA, Automatización de la interfaz de usuario
ms.openlocfilehash: 8d31f7b32cb92794ff8592c239436f3b101a3859
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230820"
---
# <span data-ttu-id="5fb95-104">Diseño de sitios web accesibles</span><span class="sxs-lookup"><span data-stu-id="5fb95-104">Designing Accessible Websites</span></span>  

<span data-ttu-id="5fb95-105">Al crear un diseño inclusivo, todas las personas pueden hacer uso de la tecnología independientemente de su edad, educación, ubicación geográfica, idioma o discapacidad.</span><span class="sxs-lookup"><span data-stu-id="5fb95-105">Creating an inclusive design makes technology usable by all people no matter their age, education, geographic location, language, or disability.</span></span>  <span data-ttu-id="5fb95-106">Las personas que usan tecnología y exploran la web tienen una amplia variedad de capacidades y preferencias.</span><span class="sxs-lookup"><span data-stu-id="5fb95-106">People using technology and browsing the web have a wide range of abilities and preferences.</span></span>  <span data-ttu-id="5fb95-107">Al diseñar su sitio web, tenga en cuenta los siguientes escenarios clave de accesibilidad:</span><span class="sxs-lookup"><span data-stu-id="5fb95-107">As you design your website, keep in mind the following key accessibility scenarios:</span></span>

*   <span data-ttu-id="5fb95-108">Lectores de pantalla: los usuarios ciegos o con discapacidad visual dependen de los lectores de pantalla para interpretar e interactuar con la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fb95-108">Screen readers—Users who are blind or visually impaired rely on screen readers to interpret and interact with the UI of your app.</span></span>  <span data-ttu-id="5fb95-109">La interpretación implica leer los nombres de los elementos de la interfaz de usuario, los roles, los valores, entre otros, e interactuar con la interfaz de usuario implica mover el foco de un elemento a otro e invocar la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="5fb95-109">Interpreting involves reading the UI element names, roles, values, and so on, and interacting with the UI involves moving the focus from one element to another and invoking functionality.</span></span>
*   <span data-ttu-id="5fb95-110">Accesibilidad de teclado: muchos usuarios de accesibilidad dependen del teclado para navegar y operar la interfaz de usuario mediante:</span><span class="sxs-lookup"><span data-stu-id="5fb95-110">Keyboard accessibility—Many accessibility users rely on the keyboard to navigate and operate the UI by:</span></span>
    *   <span data-ttu-id="5fb95-111">Mover el foco entre los elementos mediante la tecla Tab.</span><span class="sxs-lookup"><span data-stu-id="5fb95-111">Moving focus among elements by using the Tab key.</span></span>
    *   <span data-ttu-id="5fb95-112">Navegar en elementos contenedor como listas, cuadrículas y vistas de árbol mediante las teclas de flecha.</span><span class="sxs-lookup"><span data-stu-id="5fb95-112">Navigating in container elements such as lists, grids, and tree views by using the arrow keys.</span></span>
    *   <span data-ttu-id="5fb95-113">Activar la funcionalidad \(invocar acciones\) mediante la tecla Entrar o Espacio.</span><span class="sxs-lookup"><span data-stu-id="5fb95-113">Activating functionality \(invoking actions\) by using the Enter or Space key.</span></span>
    *   <span data-ttu-id="5fb95-114">Usar teclas de método abreviado para acceder de forma eficaz a otras funciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5fb95-114">Using shortcut keys to efficiently access other app functionality.</span></span>
*   <span data-ttu-id="5fb95-115">Experiencia visual accesible: los usuarios con discapacidad visual necesitan una relación de contraste de texto suficiente para el contenido de texto y una buena experiencia visual con temas de contraste alto en general.</span><span class="sxs-lookup"><span data-stu-id="5fb95-115">Accessible visual experience—Users who are visually impaired need a sufficient text contrast ratio for text content, and a good visual experience with high contrast themes overall.</span></span>  <span data-ttu-id="5fb95-116">Los usuarios que son daltónimos necesitan que la información se transmita de formas distintas a través del color.</span><span class="sxs-lookup"><span data-stu-id="5fb95-116">Users who are color blind need information to be conveyed in ways other than through color.</span></span>

<span data-ttu-id="5fb95-117">Muchos problemas comunes de accesibilidad en la web se pueden resolver a través de una buena práctica de codificación.</span><span class="sxs-lookup"><span data-stu-id="5fb95-117">Many common accessibility issues on the web can be solved through good coding practice.</span></span>  <span data-ttu-id="5fb95-118">La documentación de las Directrices de accesibilidad de contenido web [(WCAG) 2.0](https://www.w3.org/TR/WCAG20) proporciona técnicas y procedimientos recomendados para ayudarle a diseñar aplicaciones web dinámicas más accesibles.</span><span class="sxs-lookup"><span data-stu-id="5fb95-118">The [Web Content Accessibility Guidelines (WCAG) 2.0](https://www.w3.org/TR/WCAG20) documentation provides techniques and best practices to help you design more accessible dynamic web applications.</span></span>  <span data-ttu-id="5fb95-119">Para obtener más información sobre la creación de sitios web accesibles, vaya a [Crear sitios web accesibles.](./build/index.md)</span><span class="sxs-lookup"><span data-stu-id="5fb95-119">For more information on building accessible websites, navigate to [Building Accessible Websites](./build/index.md) .</span></span>

## <span data-ttu-id="5fb95-120">Recursos</span><span class="sxs-lookup"><span data-stu-id="5fb95-120">Resources</span></span>  

#### [<span data-ttu-id="5fb95-121">Diseño para inclusión</span><span class="sxs-lookup"><span data-stu-id="5fb95-121">Designing for Inclusion</span></span>](https://w3.org/WAI/users/Overview.html)  

<span data-ttu-id="5fb95-122">El diseño para la inclusión por parte de W3C Web Accessibility Initiative proporciona recursos que le ayudarán a comprender mejor a los usuarios con discapacidades y a diseñar su sitio web pensando en ellos.</span><span class="sxs-lookup"><span data-stu-id="5fb95-122">Designing for Inclusion by the W3C Web Accessibility Initiative provides resources to help you better understand users with disabilities and how to design your website with them in mind.</span></span>

#### [<span data-ttu-id="5fb95-123">Diseño de software inclusivo</span><span class="sxs-lookup"><span data-stu-id="5fb95-123">Designing inclusive software</span></span>](https://msdn.microsoft.com/windows/uwp/accessibility/designing-inclusive-software)  

<span data-ttu-id="5fb95-124">El diseño de software inclusivo describe los principios y prácticas de diseño de Microsoft para la Plataforma Windows universal (UWP).</span><span class="sxs-lookup"><span data-stu-id="5fb95-124">Designing inclusive software discusses Microsoft design principles and practices for the Universal Windows Platform (UWP).</span></span>

#### [<span data-ttu-id="5fb95-125">Cómo las personas con discapacidades usan la Web</span><span class="sxs-lookup"><span data-stu-id="5fb95-125">How People with Disabilities Use the Web</span></span>](https://www.w3.org/WAI/intro/people-use-web/Overview.html)  

<span data-ttu-id="5fb95-126">Este recurso de W3C presenta cómo las personas con discapacidades, incluidas las personas con discapacidades relacionadas con la edad, usan la Web.</span><span class="sxs-lookup"><span data-stu-id="5fb95-126">This resource by the W3C introduces how people with disabilities, including people with age-related impairments, use the Web.</span></span>

#### [<span data-ttu-id="5fb95-127">Diseño inclusivo Toolkit</span><span class="sxs-lookup"><span data-stu-id="5fb95-127">Inclusive Design Toolkit</span></span>](https://www.microsoft.com/design/practice#howwemake-section)  

<span data-ttu-id="5fb95-128">Microsoft desarrolló el diseño inclusivo Toolkit mostrar cómo la diversidad humana puede crear mejores restricciones de diseño y cómo conectar soluciones aparentemente nicho a mercados más amplios.</span><span class="sxs-lookup"><span data-stu-id="5fb95-128">Microsoft developed the Inclusive Design Toolkit to show how human diversity can create better design constraints and how to connect seemingly niche solutions to broader markets.</span></span>

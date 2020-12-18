---
ms.assetid: 1b3ebc25-d023-4f23-bbba-dce066c20de8
description: Recorra la forma en que las mejores prácticas y las aplicaciones de Internet enriquecidas accesibles (ARIA) pueden reunirse para crear un sitio web accesible.
title: Crear | Accesibilidad
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: accesibilidad, accesibilidad para desarrolladores, sitios web accesibles, Edge, desarrollo web, ARIA, desarrollador, UIA, automatización de la interfaz de usuario
ms.custom: seodec18
ms.openlocfilehash: 40ab1acd0b5356ad4696cde0762f656708a67890
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236055"
---
# <span data-ttu-id="5e876-104">Creación de sitios web accesibles</span><span class="sxs-lookup"><span data-stu-id="5e876-104">Building Accessible Websites</span></span>

<span data-ttu-id="5e876-105">La web está rellenada con sitios web dinámicos y complejos, aplicaciones e interfaces de usuario generadas con una combinación de HTML, CSS y JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5e876-105">The web is filled with dynamic and complex websites, applications, and user interfaces built using a combination of HTML, CSS, and JavaScript.</span></span>  <span data-ttu-id="5e876-106">Sin embargo, cuando se diseñan y se crean sin problemas de accesibilidad, los usuarios que dependen de las tecnologías de [asistencia](https://webaim.org/articles/motor/assistive) para explorar la web son difíciles de usar.</span><span class="sxs-lookup"><span data-stu-id="5e876-106">However, when designed and built without accessibility in mind, these complex websites are difficult to use by people who rely on [assistive technologies](https://webaim.org/articles/motor/assistive) to browse the web.</span></span> <span data-ttu-id="5e876-107">La creación de sitios web que sean accesibles para personas con discapacidades requiere información semántica acerca de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5e876-107">Building websites that are accessible to people with disabilities requires semantic information about the user interface.</span></span> <span data-ttu-id="5e876-108">Esto permite que las tecnologías de asistencia, como los lectores de pantalla, transmitan la información necesaria para ayudar a las personas con una amplia variedad de funciones a usar el sitio Web.</span><span class="sxs-lookup"><span data-stu-id="5e876-108">This allows for assistive technologies, like screen readers, to convey the necessary information to help people with a range of abilities use the website.</span></span>

<span data-ttu-id="5e876-109">Visita [HTML5Accessibility](https://html5accessibility.com) para obtener información sobre qué nuevas características de HTML5 son compatibles con Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5e876-109">Visit [HTML5Accessibility](https://html5accessibility.com) for information on which new HTML5 features are accessibly supported by Microsoft Edge.</span></span>

## <span data-ttu-id="5e876-110">Cómo funciona la accesibilidad</span><span class="sxs-lookup"><span data-stu-id="5e876-110">How Accessibility Works</span></span>

<span data-ttu-id="5e876-111">Las tecnologías de asistencia agregan capacidades que los equipos no suelen tener.</span><span class="sxs-lookup"><span data-stu-id="5e876-111">Assistive technologies add capabilities that computers don't usually have.</span></span> <span data-ttu-id="5e876-112">Por ejemplo, un usuario con deficiencias visuales puede usar su teclado en combinación con tecnología de asistencia, como un lector de pantalla, en lugar de usar directamente el explorador con el mouse y la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5e876-112">For example, a visually impaired user might use their keyboard in combination with assistive technology such as a screen reader, rather than directly using the browser with the mouse and screen.</span></span> <span data-ttu-id="5e876-113">Para las aplicaciones de las plataformas de Microsoft y en la web, la tecnología de asistencia interactúa con la automatización de la [interfaz de usuario](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx)de Microsoft, un modelo de objetos específico de la aplicación, como el modelo de objetos de documento (dom) en Microsoft Edge, o una combinación de estos.</span><span class="sxs-lookup"><span data-stu-id="5e876-113">For applications on Microsoft platforms and on the web, the assistive technology interacts with Microsoft [UI Automation](https://msdn.microsoft.com/library/windows/desktop/bb892135.aspx), an application-specific object model such as the Document Object Model (DOM) in Microsoft Edge, or a combination of these.</span></span>

<span data-ttu-id="5e876-114">Para los desarrolladores web, determinados elementos HTML se asignan a objetos de automatización de la interfaz de usuario, por lo que al seleccionarlos, el desarrollador puede usar las propiedades y los eventos de accesibilidad integrados en esos elementos.</span><span class="sxs-lookup"><span data-stu-id="5e876-114">For web developers, certain HTML elements are mapped to UI Automation objects, so in selecting those HTML elements, the developer can use the accessibility properties and events built in to those elements.</span></span> <span data-ttu-id="5e876-115">Al desarrollar su sitio web, normalmente solo debe preocuparse de asegurarse de que la API esté escrita correctamente en (o que se especifique el elemento apropiado), para que la aplicación sea accesible.</span><span class="sxs-lookup"><span data-stu-id="5e876-115">While developing your website, you usually only need to be concerned with ensuring that the API is correctly written to (or that the appropriate element is specified), in order for the application to be accessible.</span></span> <span data-ttu-id="5e876-116">Para obtener más información [, consulta Aria y la automatización de la interfaz de usuario en Microsoft Edge](./ARIA-and-UI-Automation.md) .</span><span class="sxs-lookup"><span data-stu-id="5e876-116">Check out [ARIA and UI Automation in Microsoft Edge](./ARIA-and-UI-Automation.md) for more information.</span></span>  <span data-ttu-id="5e876-117">Para obtener información sobre las aplicaciones de la plataforma universal de Windows (UWP) accesibles, consulta el tema [accesibilidad](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) en el centro de desarrollo de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e876-117">For information on accessible Universal Windows Platform (UWP) apps, see the [Accessibility](https://msdn.microsoft.com/windows/uwp/accessibility/accessibility) topic in the Windows Dev Center.</span></span>

<span data-ttu-id="5e876-118">Muchos de los problemas de accesibilidad comunes con el contenido dinámico se pueden resolver mediante una buena práctica de programación y la documentación de [WCAG 2,0](https://go.microsoft.com/fwlink/p/?LinkID=24629) incluye muchas técnicas y procedimientos recomendados para ayudarle a crear aplicaciones web dinámicas más accesibles.</span><span class="sxs-lookup"><span data-stu-id="5e876-118">Many common accessibility issues with dynamic content can be addressed by good coding practice, and the [WCAG 2.0](https://go.microsoft.com/fwlink/p/?LinkID=24629) documentation includes many techniques and best practices to help you create more accessible dynamic web applications.</span></span> <span data-ttu-id="5e876-119">Sin embargo, incluso cuando se codifica correctamente, el contenido dinámico no es necesariamente accesible.</span><span class="sxs-lookup"><span data-stu-id="5e876-119">Even when coded properly, however, dynamic content is not necessarily accessible.</span></span> <span data-ttu-id="5e876-120">[Las aplicaciones de Internet enriquecidas accesibles (Aria)](#aria) ayudan a solucionar este problema.</span><span class="sxs-lookup"><span data-stu-id="5e876-120">[Accessible Rich Internet Applications (ARIA)](#aria) helps overcome this issue.</span></span>  

<span data-ttu-id="5e876-121">Para obtener más información sobre accesibilidad web, consulte la [Introducción a la accesibilidad web](https://www.w3.org/WAI/intro/accessibility.php) de la [iniciativa de accesibilidad para web](https://www.w3.org/WAI/) (WAI).</span><span class="sxs-lookup"><span data-stu-id="5e876-121">For more information on web accessibility, check out the [Introduction to Web Accessibility](https://www.w3.org/WAI/intro/accessibility.php) by the [Web Accessibility Initiative](https://www.w3.org/WAI/) (WAI).</span></span>

## <span data-ttu-id="5e876-122">ARIA</span><span class="sxs-lookup"><span data-stu-id="5e876-122">ARIA</span></span>

<span data-ttu-id="5e876-123">La especificación de [aplicaciones de Internet enriquecidas accesibles](https://www.w3.org/TR/wai-aria/) (Aria) por la [iniciativa de accesibilidad web](https://www.w3.org/WAI/) de W3C's define como una sintaxis para hacer que el contenido Web dinámico y las interfaces de usuario personalizadas sean accesibles para todas las personas.</span><span class="sxs-lookup"><span data-stu-id="5e876-123">The [Accessible Rich Internet Applications](https://www.w3.org/TR/wai-aria/) (ARIA) specification by the W3C's [Web Accessibility Initiative](https://www.w3.org/WAI/) defines as a syntax for making dynamic web content and custom user interfaces accessible to all people.</span></span> <span data-ttu-id="5e876-124">ARIA extiende el código HTML mediante atributos adicionales (roles, propiedades y Estados) que están diseñados para transmitir la semántica personalizada.</span><span class="sxs-lookup"><span data-stu-id="5e876-124">ARIA extends HTML by using additional attributes (roles, properties, and states) that are designed to convey custom semantics.</span></span> <span data-ttu-id="5e876-125">Los exploradores usan estos atributos para pasar el estado y la función de los controles a la API de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e876-125">These attributes are used by browsers to pass along the controls' state and role to the accessibility API.</span></span>

### <span data-ttu-id="5e876-126">Roles, propiedades y Estados</span><span class="sxs-lookup"><span data-stu-id="5e876-126">Roles, Properties, and States</span></span>

<span data-ttu-id="5e876-127">Los roles de ARIA se establecen en los elementos que usan el [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) atributo para proporcionar tecnologías de asistencia y información sobre las API de accesibilidad sobre el elemento.</span><span class="sxs-lookup"><span data-stu-id="5e876-127">ARIA roles are set on elements using the [`role`](https://msdn.microsoft.com/library/cc304102(v=vs.85).aspx) attribute to give assistive technologies and accessibility APIs information about the element.</span></span> <span data-ttu-id="5e876-128">Por ejemplo, el `<li>` elemento siguiente está asignado `role="menuitem"` para indicar que es un elemento de un menú.</span><span class="sxs-lookup"><span data-stu-id="5e876-128">For example, the below `<li>` element is assigned `role="menuitem"` to signify it's an item in a menu.</span></span>

```html
<li role="menuitem">Home</li>
```

<span data-ttu-id="5e876-129">Los Estados y las propiedades de ARIA son atributos prefijos de Aria que proporcionan información específica sobre un objeto para ayudar en la definición de la naturaleza de los roles.</span><span class="sxs-lookup"><span data-stu-id="5e876-129">ARIA states and properties are aria-prefixed attributes that provide specific information about an object to help form the definition of the nature of roles.</span></span> <span data-ttu-id="5e876-130">Las propiedades son atributos que son esenciales para la naturaleza de un objeto, como [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) y [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e876-130">Properties are attributes that are essential to the nature of an object, like [`aria-readonly`](https://msdn.microsoft.com/library/cc304089(v=vs.85).aspx) and [`aria-haspopup`](https://msdn.microsoft.com/library/cc304081(v=vs.85).aspx).</span></span> <span data-ttu-id="5e876-131">Cambiar una propiedad afecta al significado del objeto.</span><span class="sxs-lookup"><span data-stu-id="5e876-131">Changing a property affects the meaning of the object.</span></span> <span data-ttu-id="5e876-132">En el ejemplo siguiente, la propiedad `aria-haspopup="true"` se establece en un `<li>` elemento de menú para indicar que tiene un elemento emergente.</span><span class="sxs-lookup"><span data-stu-id="5e876-132">In the example below, the property `aria-haspopup="true"` is set on a `<li>` menu item to signify it has a popup.</span></span>

```html
<li role="menuitem" aria-haspopup="true">Open</li>
```

<span data-ttu-id="5e876-133">Los Estados no cambian la naturaleza del objeto, pero representan información asociada al objeto o a la interacción del usuario con el objeto, como [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) o [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5e876-133">States do not change the nature of the object, but represent information associated with the object or user interaction with the object, like [`aria-hidden`](https://msdn.microsoft.com/library/cc304083(v=vs.85).aspx) or [`aria-checked`](https://msdn.microsoft.com/library/cc304075(v=vs.85).aspx).</span></span> <span data-ttu-id="5e876-134">Por ejemplo, el estado del `aria-checked="false"` ejemplo siguiente representa que la casilla no está marcada.</span><span class="sxs-lookup"><span data-stu-id="5e876-134">For example, the state `aria-checked="false"` in the example below represents that the checkbox is not checked.</span></span>

```html
<div role="checkbox" aria-checked="false">Accept</div>
```

<span data-ttu-id="5e876-135">Vaya al [modelo de roles](https://www.w3.org/TR/wai-aria-1.1/#roles) de W3C para ver una lista completa de los roles, las propiedades y los Estados.</span><span class="sxs-lookup"><span data-stu-id="5e876-135">Go to [The Roles Model](https://www.w3.org/TR/wai-aria-1.1/#roles) by the W3C to see a full list of roles, properties, and states.</span></span>

<span data-ttu-id="5e876-136">Para obtener más información sobre ARIA, vea ARIA en la sección de [recursos](#resources) .</span><span class="sxs-lookup"><span data-stu-id="5e876-136">For more information on ARIA, see the ARIA in the [Resources](#resources) section.</span></span>

## <span data-ttu-id="5e876-137">Pruebas de compatibilidad de tecnología de asistencia</span><span class="sxs-lookup"><span data-stu-id="5e876-137">Assistive Technology Compatibility Testing</span></span>  

<span data-ttu-id="5e876-138">Comprobar que el sitio web que está creando funciona con tecnologías de asistencia reales es la mejor manera de garantizar una buena experiencia para los usuarios con discapacidades.</span><span class="sxs-lookup"><span data-stu-id="5e876-138">Verifying that the website you are building works with real assistive technologies is the best way to ensure a good experience for your users with disabilities.</span></span>  <span data-ttu-id="5e876-139">Dado que muchas tecnologías de asistencia hacen uso del teclado, probar la accesibilidad del teclado de tu sitio web es un buen lugar para comenzar.</span><span class="sxs-lookup"><span data-stu-id="5e876-139">Since many assistive technologies make use of the keyboard, testing the keyboard accessibility of your website is a good place to start.</span></span>  <span data-ttu-id="5e876-140">La [prueba de compatibilidad del teclado][W3cPerspectiveVideosKeyboard] valida que los usuarios tengan acceso a todos los controles interactivos sin necesidad de un mouse.</span><span class="sxs-lookup"><span data-stu-id="5e876-140">[Keyboard compatibility testing][W3cPerspectiveVideosKeyboard] validates that users have access to all interactive controls without requiring a mouse.</span></span>  <span data-ttu-id="5e876-141">Microsoft [Accessibility Insights para web][AccessibilityinsightsWebOverview] es una extensión de explorador para Microsoft Edge y Chrome que le guía y revela varios problemas comunes.</span><span class="sxs-lookup"><span data-stu-id="5e876-141">Microsoft [Accessibility Insights for Web][AccessibilityinsightsWebOverview] is a browser extension for Microsoft Edge and Chrome that guides you and reveals several common issues.</span></span>  

<span data-ttu-id="5e876-142">Una vez que tenga la seguridad de que su sitio web funciona bien con un teclado, pruébelo con otras tecnologías de asistencia, como los lectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="5e876-142">Once you are confident that your website works well with a keyboard, try it with other assistive technologies, such as screen readers.</span></span>  <span data-ttu-id="5e876-143">Descubre problemas en los siguientes.</span><span class="sxs-lookup"><span data-stu-id="5e876-143">It uncover issues in the following.</span></span>

*   <span data-ttu-id="5e876-144">Su HTML, ARIA y CSS.</span><span class="sxs-lookup"><span data-stu-id="5e876-144">Your HTML, ARIA, and CSS.</span></span>  
*   <span data-ttu-id="5e876-145">El nivel de compatibilidad de una tecnología de asistencia para una característica o técnica.</span><span class="sxs-lookup"><span data-stu-id="5e876-145">The level of support of an assistive technology for a feature or technique.</span></span>  
    
<span data-ttu-id="5e876-146">Los distintos exploradores pueden asignar elementos a las API de accesibilidad de la plataforma de forma diferente a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5e876-146">Different browsers may map elements to platform accessibility APIs differently than Microsoft Edge.</span></span>  <span data-ttu-id="5e876-147">Al crear la interfaz, es importante considerar cada diferencia.</span><span class="sxs-lookup"><span data-stu-id="5e876-147">While building your interface, it is important to consider each difference.</span></span>  

<span data-ttu-id="5e876-148">WebAIM realiza encuestas con [lectores de pantalla][WebaimProjectsScreenreadersurvey8] y usuarios con deficiencias [visuales][WebaimProjectsLowvisionsurvey2] que le ayudan a decidir qué exploradores y tecnologías de asistencia desea probar.</span><span class="sxs-lookup"><span data-stu-id="5e876-148">WebAIM conducts surveys with [screen reader][WebaimProjectsScreenreadersurvey8] and [low vision][WebaimProjectsLowvisionsurvey2] users that help you decide which assistive technologies and browsers you want to test.</span></span>  

### <span data-ttu-id="5e876-149">Aprender a probar</span><span class="sxs-lookup"><span data-stu-id="5e876-149">Learning How to Test</span></span>  

<span data-ttu-id="5e876-150">Las tecnologías de asistencia son herramientas sofisticadas.</span><span class="sxs-lookup"><span data-stu-id="5e876-150">Assistive technologies are sophisticated tools.</span></span>  <span data-ttu-id="5e876-151">No dé por supuesto que puede comenzar inmediatamente las pruebas con una tecnología de asistencia sin conocer primero cómo funciona.</span><span class="sxs-lookup"><span data-stu-id="5e876-151">Do not assume that you are able to immediately start testing with an assistive technology without first learning about how it works.</span></span>  <span data-ttu-id="5e876-152">Aprender a probar con un lector de pantalla tiene una curva de aprendizaje especialmente pronunciada.</span><span class="sxs-lookup"><span data-stu-id="5e876-152">Learning to test with a screen reader has an especially steep learning curve.</span></span>  <span data-ttu-id="5e876-153">Un usuario del lector de pantalla inexperto puede suponer que se ha producido un error de lector de pantalla mientras el problema está relacionado con el uso incorrecto del lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="5e876-153">A novice screen reader user may assume that a screen reader bug has occurred while the issue is related to misuse of the screen reader.</span></span>  

<span data-ttu-id="5e876-154">Para obtener más información sobre cómo aprender a probar las tecnologías de asistencia, vaya a [pruebas con lectores de pantalla][WebaimArticlesScreenreaderTesting] en webaim.</span><span class="sxs-lookup"><span data-stu-id="5e876-154">For more information about learning to test with assistive technologies, navigate to [Testing with Screen Readers][WebaimArticlesScreenreaderTesting] on WebAIM.</span></span>  

### <span data-ttu-id="5e876-155">Comprobación local</span><span class="sxs-lookup"><span data-stu-id="5e876-155">Testing Locally</span></span>  

<span data-ttu-id="5e876-156">La mayoría de los dispositivos incluye tecnología de asistencia que está integrada en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5e876-156">Most devices include assistive technology that is built-in to the OS.</span></span>  <span data-ttu-id="5e876-157">Microsoft Windows incluye el lector de pantalla [narrador de Windows][MicrosoftSupport22798] y el [ampliador de Windows][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].</span><span class="sxs-lookup"><span data-stu-id="5e876-157">Microsoft Windows includes the [Windows Narrator][MicrosoftSupport22798] screen reader and [Windows Magnifier][MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198].</span></span>  <span data-ttu-id="5e876-158">las tecnologías de asistencia de terceros, como [NVDA][NvaccessAboutNvda], [FreedomscientificSoftwareJaws]y [ZoomText][FreedomscientificSoftwareZoomtext] , están disponibles para su descarga.</span><span class="sxs-lookup"><span data-stu-id="5e876-158">3rd party assistive technologies like [NVDA][NvaccessAboutNvda], [FreedomscientificSoftwareJaws], and [ZoomText][FreedomscientificSoftwareZoomtext] are available to download.</span></span>  <span data-ttu-id="5e876-159">Apple macOS incluye el lector de pantalla [VoiceOver][AppleAccessibilityMacVision] .</span><span class="sxs-lookup"><span data-stu-id="5e876-159">Apple macOS includes the [VoiceOver][AppleAccessibilityMacVision] screen reader.</span></span>  <span data-ttu-id="5e876-160">Además, iOS, Android y Linux admiten una variedad de tecnologías de asistencia.</span><span class="sxs-lookup"><span data-stu-id="5e876-160">And iOS, Android, and Linux all support a variety of assistive technologies.</span></span>  

### <span data-ttu-id="5e876-161">Pruebas en máquinas virtuales y emuladores</span><span class="sxs-lookup"><span data-stu-id="5e876-161">Testing in Virtual Machines and Emulators</span></span>  

<span data-ttu-id="5e876-162">En macOS, si desea probar con una tecnología de asistencia que solo está disponible para Windows, como narrador de Windows o NVDA, cree una máquina virtual de Windows.</span><span class="sxs-lookup"><span data-stu-id="5e876-162">Under macOS, if you want to test with an assistive technology only available for Windows, like Windows Narrator or NVDA, create a Windows virtual machine.</span></span>  <span data-ttu-id="5e876-163">Las máquinas virtuales con Microsoft Edge \ (EdgeHTML \) e IE están disponibles para VirtualBox y VMWare en la [Página de descarga de máquinas virtuales][MicrosoftDeveloperEdgeVms].</span><span class="sxs-lookup"><span data-stu-id="5e876-163">Virtual machines with Microsoft Edge \(EdgeHTML\) and IE are available for VirtualBox and VMWare on the [Virtual Machines download page][MicrosoftDeveloperEdgeVms].</span></span>  

<span data-ttu-id="5e876-164">[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] incluye un emulador que para que pruebe las tecnologías de asistencia del [conjunto de accesibilidad de Android][GooglePlayStoreAndroidAccessibilitySuite].</span><span class="sxs-lookup"><span data-stu-id="5e876-164">[Android Studio][AndroidDeveloperSdkInstallingStudioHtml] includes an emulator that for you to test assistive technologies in the [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite].</span></span>  <span data-ttu-id="5e876-165">Siga las instrucciones para [configurar un dispositivo virtual][AndroidDeveloperDevicesManagingAvdsHtml] e [iniciar el emulador][AndroidDeveloperDevicesEmulatorHtml], a continuación, instale el [conjunto de accesibilidad de Android][GooglePlayStoreAndroidAccessibilitySuite] desde la tienda GooglePlay.</span><span class="sxs-lookup"><span data-stu-id="5e876-165">Follow the instructions to [set up a virtual device][AndroidDeveloperDevicesManagingAvdsHtml] and [start the emulator][AndroidDeveloperDevicesEmulatorHtml], then install [Android Accessibility Suite][GooglePlayStoreAndroidAccessibilitySuite] from the GooglePlay store.</span></span>  

> [!NOTE]
> <span data-ttu-id="5e876-166">En este momento, el simulador iOS no incluye VoiceOver.</span><span class="sxs-lookup"><span data-stu-id="5e876-166">The iOS Simulator does not currently include VoiceOver.</span></span>  

### <span data-ttu-id="5e876-167">Herramientas de prueba basadas en la nube</span><span class="sxs-lookup"><span data-stu-id="5e876-167">Cloud-based Testing Tools</span></span>  

<span data-ttu-id="5e876-168">Si la tecnología de asistencia no está disponible en el sistema operativo o no es posible instalar una en una máquina virtual o un emulador, las herramientas de prueba de tecnología de asistencia basadas en la nube son la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="5e876-168">If an assistive technology is not available on your OS or you not possible to install one on a virtual machine or emulator, cloud-based assistive technology testing tools are the next best thing.</span></span>  

*   <span data-ttu-id="5e876-169">[Assistiv Labs (Commercial)][AssistivlabsMain] le permite probar manualmente con tecnologías de asistencia a través de cualquier explorador web moderno.</span><span class="sxs-lookup"><span data-stu-id="5e876-169">[Assistiv Labs (commercial)][AssistivlabsMain] enables you to manually test with assistive technologies through any modern web browser.</span></span>  <span data-ttu-id="5e876-170">Elija una tecnología de asistencia y un explorador y se lo conectará a una máquina virtual, un emulador o un dispositivo real con el que puede interactuar.</span><span class="sxs-lookup"><span data-stu-id="5e876-170">Choose an assistive technology and browser and it connects you with a virtual machine, emulator, or real device with which you may interact.</span></span>  

## <span data-ttu-id="5e876-171">Recursos</span><span class="sxs-lookup"><span data-stu-id="5e876-171">Resources</span></span>

### <span data-ttu-id="5e876-172">Conceptos básicos sobre accesibilidad</span><span class="sxs-lookup"><span data-stu-id="5e876-172">Accessibility Basics</span></span>

#### [<span data-ttu-id="5e876-173">El proyecto A11Y</span><span class="sxs-lookup"><span data-stu-id="5e876-173">The A11Y Project</span></span>](http://a11yproject.com/)

<span data-ttu-id="5e876-174">El proyecto A11Y es un esfuerzo basado en la comunidad para facilitar la accesibilidad Web.</span><span class="sxs-lookup"><span data-stu-id="5e876-174">The A11Y Project is a community-driven effort to make web accessibility easier.</span></span> <span data-ttu-id="5e876-175">Consulte [el sitio del proyecto A11Y](https://a11yproject.com/) para obtener información sobre los principios de accesibilidad básicos, su patrón accesible y la [biblioteca](https://a11yproject.com/patterns)widget, y sus [recursos](http://a11yproject.com/resources.html) sobre el software de accesibilidad, los blogs, los libros y las herramientas.</span><span class="sxs-lookup"><span data-stu-id="5e876-175">Check out [The A11Y Project](https://a11yproject.com/) site to learn about basic accessibility principles, their accessible pattern and widget [library](https://a11yproject.com/patterns), and their [resources](http://a11yproject.com/resources.html) on accessibility software, blogs, books, and tools.</span></span>

#### [<span data-ttu-id="5e876-176">Iniciativa de accesibilidad para web (WAI)</span><span class="sxs-lookup"><span data-stu-id="5e876-176">Web Accessibility Initiative (WAI)</span></span>](https://w3.org/WAI/)

<span data-ttu-id="5e876-177">La iniciativa de accesibilidad Web W3C (WAI) es un esfuerzo para ayudar a mejorar la accesibilidad de la Web.</span><span class="sxs-lookup"><span data-stu-id="5e876-177">The W3C Web Accessibility Initiative (WAI) is an effort to help improve the accessibility of the web.</span></span> <span data-ttu-id="5e876-178">Su sitio proporciona una variedad de recursos para [empezar a usar la accesibilidad web](https://www.w3.org/WAI/gettingstarted/Overview.html), [diseñar la inclusión](https://www.w3.org/WAI/users/Overview.html), [tutoriales y presentaciones](https://www.w3.org/WAI/train.html), entre otras.</span><span class="sxs-lookup"><span data-stu-id="5e876-178">Their site provides a variety of resources for [Getting Started with Web Accessibility](https://www.w3.org/WAI/gettingstarted/Overview.html), [Designing for Inclusion](https://www.w3.org/WAI/users/Overview.html), [tutorials and presentations](https://www.w3.org/WAI/train.html), and more.</span></span>

### <span data-ttu-id="5e876-179">Blogs de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="5e876-179">Accessibility Blogs</span></span>

#### [<span data-ttu-id="5e876-180">El grupo Paciello Group</span><span class="sxs-lookup"><span data-stu-id="5e876-180">The Paciello Group</span></span>](https://www.paciellogroup.com/blog/)

<span data-ttu-id="5e876-181">El grupo Paciello Group ofrece asesoramiento y soluciones tecnológicas a organizaciones de todo el mundo para garantizar que sus clientes llegan a todas las audiencias de manera eficaz y eficaz, mientras cumplen los estándares gubernamentales e internacionales.</span><span class="sxs-lookup"><span data-stu-id="5e876-181">The Paciello Group provides consulting and technology solutions to organizations around the world to ensure their clients reach all audiences effectively and efficiently, while meeting governmental and international standards.</span></span> <span data-ttu-id="5e876-182">Su blog cubre temas como procedimientos recomendados de accesibilidad para Web, herramientas de accesibilidad y tendencias de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e876-182">Their blog covers topics like web accessibility best practices, accessibility tools, and accessibility trends.</span></span>

#### [<span data-ttu-id="5e876-183">Simple accesible</span><span class="sxs-lookup"><span data-stu-id="5e876-183">Simply Accessible</span></span>](http://simplyaccessible.com/articles/)

<span data-ttu-id="5e876-184">Simplemente accesible es un equipo de especialistas en accesibilidad que proporciona aprendizaje de accesibilidad, consultoría y más para cambiar la percepción de la accesibilidad en la Web.</span><span class="sxs-lookup"><span data-stu-id="5e876-184">Simply Accessible is a team of accessibility specialists providing accessibility training, consulting and more to change the perception of accessibility on the web.</span></span> <span data-ttu-id="5e876-185">En la sección de [artículos](http://simplyaccessible.com/articles/) se describen los procedimientos recomendados para accesibilidad web, diseño accesible y mucho más.</span><span class="sxs-lookup"><span data-stu-id="5e876-185">Their [Articles](http://simplyaccessible.com/articles/) section discusses best practices for web accessibility, accessible design, and more.</span></span>

#### [<span data-ttu-id="5e876-186">Grupo de la Jesús SSB (SSB)</span><span class="sxs-lookup"><span data-stu-id="5e876-186">SSB BART Group (SSB)</span></span>](http://www.ssbbartgroup.com/blog/)

<span data-ttu-id="5e876-187">El grupo SSB Jesús es una empresa de accesibilidad digital que apoya a sus clientes en el desarrollo e implementación de productos y servicios accesibles.</span><span class="sxs-lookup"><span data-stu-id="5e876-187">SSB BART Group is a digital accessibility firm supporting their clients in developing and deploying accessible products and services.</span></span> <span data-ttu-id="5e876-188">Su blog aborda temas como procedimientos recomendados de ARIA, tendencias de accesibilidad, seminarios por Web, etc.</span><span class="sxs-lookup"><span data-stu-id="5e876-188">Their blog addresses topics like ARIA best practices, accessibility trends, webinars, and more.</span></span>

### <span data-ttu-id="5e876-189">Ejemplos accesibles</span><span class="sxs-lookup"><span data-stu-id="5e876-189">Accessible Examples</span></span>

#### [<span data-ttu-id="5e876-190">Tutoriales de ally.js</span><span class="sxs-lookup"><span data-stu-id="5e876-190">ally.js - Tutorials</span></span>](http://allyjs.io/tutorials/)

<span data-ttu-id="5e876-191">Biblioteca de JavaScript para ayudar a las aplicaciones web modernas a tener dificultades de accesibilidad, simplificando la accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e876-191">JavaScript library to help modern web applications with accessibility concerns by making accessibility simpler.</span></span>

#### [<span data-ttu-id="5e876-192">Ejemplos de Heydonworks-ARIA</span><span class="sxs-lookup"><span data-stu-id="5e876-192">Heydonworks - ARIA Examples</span></span>](http://heydonworks.com/practical_aria_examples/)

<span data-ttu-id="5e876-193">Ejemplos prácticos de ARIA para mejorar la accesibilidad de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5e876-193">Practical ARIA examples to enhance your application accessibility</span></span>

#### [<span data-ttu-id="5e876-194">Ejemplos de OpenAjax</span><span class="sxs-lookup"><span data-stu-id="5e876-194">OpenAjax Examples</span></span>](http://oaa-accessibility.org/)

<span data-ttu-id="5e876-195">El sitio web de OpenAjax Alliance es un excelente recurso para verificar las reglas de WAI-ARIA y proporciona una serie de ejemplos de implementaciones de WAI-ARIA.</span><span class="sxs-lookup"><span data-stu-id="5e876-195">The OpenAjax Alliance website is an excellent resource for verifying the rules for WAI-ARIA and provides a number of examples of WAI-ARIA implementations.</span></span>

#### [<span data-ttu-id="5e876-196">Modos</span><span class="sxs-lookup"><span data-stu-id="5e876-196">Patterns</span></span>](http://a11yproject.com/patterns.html)

<span data-ttu-id="5e876-197">[El proyecto A11Y](http://a11yproject.com/) ofrece una biblioteca de widgets y patrones accesibles, como menús, botones, información sobre herramientas, etc.</span><span class="sxs-lookup"><span data-stu-id="5e876-197">[The A11Y Project](http://a11yproject.com/) offers a library of accessible widgets and patterns like menus, buttons, tooltips, and more.</span></span>

### <span data-ttu-id="5e876-198">Técnicas de accesibilidad & herramientas</span><span class="sxs-lookup"><span data-stu-id="5e876-198">Accessibility Techniques & Tools</span></span>

#### [<span data-ttu-id="5e876-199">Accesibilidad: crear iconos de extensión accesibles para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5e876-199">Accessibility: Creating accessible extension icons for Microsoft Edge</span></span>](../../edgehtml/extensions/guides/accessibility.md)

<span data-ttu-id="5e876-200">Obtén orientación sobre cómo crear iconos de extensiones accesibles para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5e876-200">Get guidance on creating accessible extensions icons for Microsoft Edge.</span></span>

#### [<span data-ttu-id="5e876-201">Nombre accesible y descripción: cálculo y asignaciones 1,1</span><span class="sxs-lookup"><span data-stu-id="5e876-201">Accessible Name and Description: Computation and Mappings 1.1</span></span>](https://www.w3.org/TR/accname-1.1/)

<span data-ttu-id="5e876-202">Este documento de asignación del W3C explica cómo los exploradores determinan el nombre y las descripciones de los objetos accesibles de los idiomas de contenido web y los exponen en las API de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e876-202">This W3C mapping document explains how browsers determine name and descriptions of accessible objects from web content languages and expose them in accessibility APIs.</span></span>

#### [<span data-ttu-id="5e876-203">Recursos de evaluación de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="5e876-203">Accessibility Evaluation Resources</span></span>](https://www.w3.org/WAI/eval/Overview.html)

<span data-ttu-id="5e876-204">Recursos de evaluación de accesibilidad es un recurso de varias páginas que describe los diferentes enfoques para evaluar los sitios web para accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e876-204">Accessibility Evaluation Resources is a multi-page resource by the W3C that outlines different approaches for evaluating websites for accessibility.</span></span>

#### [<span data-ttu-id="5e876-205">Pruebas de compatibilidad con tecnología de asistencia</span><span class="sxs-lookup"><span data-stu-id="5e876-205">Assistive technology compatibility tests</span></span>](http://www.powermapper.com/tests/)

<span data-ttu-id="5e876-206">Resultados de la prueba que muestran cómo se comportan diferentes tipos de contenido y estándares en las tecnologías de asistencia (AT) como los lectores de pantalla.</span><span class="sxs-lookup"><span data-stu-id="5e876-206">Test results showing how different content types and standards behave in assistive technologies (AT) like screen readers.</span></span>

#### [<span data-ttu-id="5e876-207">Crear sitios web accesibles ahora es mucho más fácil</span><span class="sxs-lookup"><span data-stu-id="5e876-207">Building accessible websites just got a lot easier</span></span>](https://blogs.msdn.microsoft.com/webdev/2016/05/02/building-accessible-websites-just-got-a-lot-easier/)

<span data-ttu-id="5e876-208">Este mensaje de blog de herramientas y desarrollo web de .NET describe el [Comprobador de accesibilidad web](https://go.microsoft.com/fwlink/p/?linkid=841539)de extensiones de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5e876-208">This .NET Web Development and Tools blog post describes the Visual Studio extension [Web Accessibility Checker](https://go.microsoft.com/fwlink/p/?linkid=841539).</span></span>

#### [<span data-ttu-id="5e876-209">Asignaciones básicas de API de accesibilidad 1,1</span><span class="sxs-lookup"><span data-stu-id="5e876-209">Core Accessibility API Mappings 1.1</span></span>](https://www.w3.org/TR/core-aam-1.1/)

<span data-ttu-id="5e876-210">Este documento de asignación del W3C explica cómo se expone la semántica de los lenguajes de contenido web a las API de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e876-210">This W3C mapping document explains how the semantics of web content languages are exposed to accessibility APIs.</span></span>  

#### [<span data-ttu-id="5e876-211">Comprobaciones fáciles: una primera revisión de accesibilidad web</span><span class="sxs-lookup"><span data-stu-id="5e876-211">Easy Checks – A First Review of Web Accessibility</span></span>](https://www.w3.org/WAI/eval/preliminary.html)

<span data-ttu-id="5e876-212">Una serie de comprobaciones rápidas por el WAI que le ayudan a evaluar la accesibilidad de una página web.</span><span class="sxs-lookup"><span data-stu-id="5e876-212">A series of quick checks by the WAI that help you asses the accessibility of a web page.</span></span>

#### [<span data-ttu-id="5e876-213">Cómo cumplir con las WCAG 2,0</span><span class="sxs-lookup"><span data-stu-id="5e876-213">How to Meet WCAG 2.0</span></span>](https://www.w3.org/WAI/WCAG20/quickref/)

<span data-ttu-id="5e876-214">Referencia rápida a los requisitos de accesibilidad de contenido web (WCAG) 2,0 (criterios de éxito) y técnicas.</span><span class="sxs-lookup"><span data-stu-id="5e876-214">A quick reference to Web Content Accessibility Guidelines (WCAG) 2.0 requirements (success criteria) and techniques.</span></span>

#### [<span data-ttu-id="5e876-215">Asignaciones de API de accesibilidad de HTML 1,0</span><span class="sxs-lookup"><span data-stu-id="5e876-215">HTML Accessibility API Mappings 1.0</span></span>](https://www.w3.org/TR/html-aam-1.0/)

<span data-ttu-id="5e876-216">Este documento de las asignaciones del consorcio W3C explica cómo los atributos y elementos HTML 5.1 se asignan a las API de accesibilidad de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="5e876-216">This W3C mappings document explains how HTML5.1 element and attributes map to platform accessibility APIs.</span></span>

#### [<span data-ttu-id="5e876-217">Sugerencias rápidas</span><span class="sxs-lookup"><span data-stu-id="5e876-217">Quick Tips</span></span>](http://a11yproject.com/#Quick-tips)

<span data-ttu-id="5e876-218">Una lista de sugerencias de desarrollo rápido para la web para accesibilidad mediante [el proyecto A11Y](http://a11yproject.com/).</span><span class="sxs-lookup"><span data-stu-id="5e876-218">A list of quick web development tips for accessibility by [The A11Y Project](http://a11yproject.com/).</span></span>

#### [<span data-ttu-id="5e876-219">Exploración del sitio</span><span class="sxs-lookup"><span data-stu-id="5e876-219">Site Scan</span></span>](https://developer.microsoft.com/microsoft-edge/tools/staticscan/)

<span data-ttu-id="5e876-220">La herramienta de exploración del sitio del centro de desarrollo de Microsoft Edge busca bibliotecas no actualizadas, problemas de diseño y problemas de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e876-220">The Site Scan tool on Microsoft Edge Dev Center checks for out-of-date libraries, layout issues, and accessibility issues.</span></span>

#### [<span data-ttu-id="5e876-221">Técnicas para WCAG 2,0</span><span class="sxs-lookup"><span data-stu-id="5e876-221">Techniques for WCAG 2.0</span></span>](https://www.w3.org/TR/WCAG20-TECHS/Overview.html)

<span data-ttu-id="5e876-222">Técnicas del W3C que proporcionan instrucciones para los desarrolladores web en las [directrices de accesibilidad de contenido Web de reunión (WCAG) 2,0](https://w3.org/TR/WCAG20/) criterios de éxito.</span><span class="sxs-lookup"><span data-stu-id="5e876-222">Techniques from the W3C that provide guidance for web developers on meeting [Web Content Accessibility Guidelines (WCAG) 2.0](https://w3.org/TR/WCAG20/) success criteria.</span></span>

#### [<span data-ttu-id="5e876-223">Sugerencias sobre el desarrollo para accesibilidad web</span><span class="sxs-lookup"><span data-stu-id="5e876-223">Tips on Developing for Web Accessibility</span></span>](https://w3.org/WAI/gettingstarted/tips/developing.html)

<span data-ttu-id="5e876-224">Sugerencias de W3C sobre el desarrollo de contenido web que sea más accesible para personas con discapacidades.</span><span class="sxs-lookup"><span data-stu-id="5e876-224">Tips from the W3C on developing web content that is more accessible to people with disabilities.</span></span>

#### [<span data-ttu-id="5e876-225">Prácticas de creación de WAI-ARIA 1,1</span><span class="sxs-lookup"><span data-stu-id="5e876-225">WAI-ARIA Authoring Practices 1.1</span></span>](http://w3c.github.io/aria-practices/)

<span data-ttu-id="5e876-226">Un documento de W3C que proporciona a los lectores comprensión de cómo usar WAI-ARIA 1,1 y recomienda métodos para hacer que los widgets, la navegación y los comportamientos sean accesibles mediante los roles WAI-ARIA, los Estados y las propiedades.</span><span class="sxs-lookup"><span data-stu-id="5e876-226">A document by the W3C that provides readers with an understanding of how to use WAI-ARIA 1.1 and recommends approaches to make widgets, navigation, and behaviors accessible using WAI-ARIA roles, states, and properties.</span></span>

#### [<span data-ttu-id="5e876-227">Directrices y técnicas WAI</span><span class="sxs-lookup"><span data-stu-id="5e876-227">WAI Guidelines and Techniques</span></span>](https://w3.org/WAI/guid-tech.html)

<span data-ttu-id="5e876-228">Una serie de pautas y estándares de accesibilidad de web desarrollados por el WAI.</span><span class="sxs-lookup"><span data-stu-id="5e876-228">A series of web accessibility guidelines and standards developed by the WAI.</span></span>  

#### [<span data-ttu-id="5e876-229">Lista herramientas de evaluación de accesibilidad web</span><span class="sxs-lookup"><span data-stu-id="5e876-229">Web Accessibility Evaluation Tools List</span></span>](https://www.w3.org/WAI/ER/tools/index.html)

<span data-ttu-id="5e876-230">Una lista de herramientas de evaluación de accesibilidad web para determinar si los sitios web cumplen con las directrices de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e876-230">A list of web accessibility evaluation tools to help determine if websites meet accessibility guidelines.</span></span>

#### [<span data-ttu-id="5e876-231">Perspectivas de accesibilidad web: Explore el impacto y las ventajas para todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="5e876-231">Web Accessibility Perspectives: Explore the Impact and Benefits for Everyone</span></span>](https://w3.org/WAI/perspectives/)

<span data-ttu-id="5e876-232">Una serie de vídeos a corto plazo de W3C sobre el impacto de la accesibilidad y los beneficios para todos.</span><span class="sxs-lookup"><span data-stu-id="5e876-232">A series of short situational videos by the W3C about the impact of accessibility and the benefits for everyone.</span></span>

<!-- links -->  

<!--todo: link updates and acrolinx  -->  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Máquinas virtuales | Desarrollador de Microsoft Edge"  

[MicrosoftSupport22798]: https://support.microsoft.com/help/22798 "Guía completa para narrador | Soporte técnico de Microsoft"  
[MicrosoftSupportWindows414948ba8b1cD3bd86150e5e32204198]: https://support.microsoft.com/windows/414948ba-8b1c-d3bd-8615-0e5e32204198 "Use la lupa para facilitar la visualización de los elementos de la pantalla | Soporte técnico de Microsoft"  

[AccessibilityinsightsWebOverview]: https://accessibilityinsights.io/docs/web/overview "Información de accesibilidad para Web | Información de accesibilidad"  

[AndroidDeveloperDevicesManagingAvdsHtml]: https://developer.android.com/tools/devices/managing-avds.html "Crear y administrar dispositivos virtuales | Desarrolladores de Android"  
[AndroidDeveloperDevicesEmulatorHtml]: https://developer.android.com/tools/devices/emulator.html "Ejecutar aplicaciones en el emulador de Android | Desarrolladores de Android"  
[AndroidDeveloperSdkInstallingStudioHtml]: https://developer.android.com/sdk/installing/studio.html "Descargar Android Studio | Desarrolladores de Android"  

[AppleAccessibilityMacVision]: https://www.apple.com/accessibility/mac/vision "Accesibilidad de la vista-Mac | Apple"  

[AssistivlabsMain]: https://assistivlabs.com "Laboratorios de assistiv"  

[FreedomscientificSoftwareJaws]: https://www.freedomscientific.com/products/software/jaws "Jaws® | Freedom Scientific"  
[FreedomscientificSoftwareZoomtext]: https://www.freedomscientific.com/products/software/zoomtext "ZoomText | Freedom Scientific"  

[GooglePlayStoreAndroidAccessibilitySuite]: https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback "Conjunto de accesibilidad de Android | Tienda GooglePlay"  

[NvaccessAboutNvda]: https://www.nvaccess.org/about-nvda "Acerca de NVDA | Acceso NV"  

[W3cPerspectiveVideosKeyboard]: https://www.w3.org/WAI/perspective-videos/keyboard "Compatibilidad del teclado | RELATIVA"  

[WebaimProjectsLowvisionsurvey2]: https://webaim.org/projects/lowvisionsurvey2 "Encuesta de usuarios con problemas de visión con deficiencias visuales \ #2 | WebAIM"  
[WebaimProjectsScreenreadersurvey8]: https://webaim.org/projects/screenreadersurvey8 "Reconocimiento de usuario de lector de pantalla \ #8 resultados | WebAIM"  
[WebaimArticlesScreenreaderTesting]: https://webaim.org/articles/screenreader_testing "Pruebas con lectores de pantalla | WebAIM"  

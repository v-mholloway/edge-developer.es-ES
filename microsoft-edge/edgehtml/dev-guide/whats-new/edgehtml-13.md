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
# <span data-ttu-id="4bb3b-104">Novedades de EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="4bb3b-104">What's new in EdgeHTML 13</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="4bb3b-105">Estos son los cambios que se han enviado con EdgeHTML 13, el motor que enciende el explorador Microsoft Edge en la [primera actualización principal](https://blogs.windows.com/windowsexperience/2015/11/12) para Windows 10 \(11/2015, compilación 10586 \).</span><span class="sxs-lookup"><span data-stu-id="4bb3b-105">Here are the changes shipped with EdgeHTML 13, the engine powering the Microsoft Edge browser in the [first major update](https://blogs.windows.com/windowsexperience/2015/11/12) for Windows 10 \(11/2015, Build 10586\).</span></span>  <span data-ttu-id="4bb3b-106">Para obtener información general sobre los cambios en el explorador general de Microsoft Edge, consulta [Introducción a EdgeHTML 13, nuestra primera actualización de plataforma para Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span><span class="sxs-lookup"><span data-stu-id="4bb3b-106">For an overview of changes to the overall Microsoft Edge browser, see [Introducing EdgeHTML 13, our first platform update for Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span></span>  

<span data-ttu-id="4bb3b-107">Este es el vínculo permanente de la siguiente lista de cambios:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md) .</span><span class="sxs-lookup"><span data-stu-id="4bb3b-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md).</span></span>  

## <span data-ttu-id="4bb3b-108">Características</span><span class="sxs-lookup"><span data-stu-id="4bb3b-108">Features</span></span>  

### <span data-ttu-id="4bb3b-109">CSS</span><span class="sxs-lookup"><span data-stu-id="4bb3b-109">CSS</span></span>  

<span data-ttu-id="4bb3b-110">EdgeHTML 13 es compatible con las nuevas características de CSS, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="4bb3b-110">EdgeHTML 13 supports new CSS features, including:</span></span>  

*   [<span data-ttu-id="4bb3b-111">Pseudo-clases de mutabilidad CSS</span><span class="sxs-lookup"><span data-stu-id="4bb3b-111">CSS Mutability Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [<span data-ttu-id="4bb3b-112">Pseudo-clases de rango CSS</span><span class="sxs-lookup"><span data-stu-id="4bb3b-112">CSS Range Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   <span data-ttu-id="4bb3b-113">Palabras clave [iniciales](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) y no [ANULAdas](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) de CSS</span><span class="sxs-lookup"><span data-stu-id="4bb3b-113">CSS [initial](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) and [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) keywords</span></span>  

### <span data-ttu-id="4bb3b-114">Extensiones de medios cifrados</span><span class="sxs-lookup"><span data-stu-id="4bb3b-114">Encrypted Media Extensions</span></span>  

<span data-ttu-id="4bb3b-115">Microsoft Edge ahora es compatible con las nuevas API de [extensiones de medios cifradas sin](https://w3.org/TR/encrypted-media) prefijos.</span><span class="sxs-lookup"><span data-stu-id="4bb3b-115">Microsoft Edge now supports the new unprefixed [Encrypted Media Extensions](https://w3.org/TR/encrypted-media) APIs.</span></span>  <span data-ttu-id="4bb3b-116">Extensiones de medios cifrados \(EME \) extiende los elementos de audio y vídeo para habilitar el contenido protegido de administración de derechos digitales \(DRM \) sin usar complementos.  Más información sobre EME:  [extensiones de medios cifradas](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span><span class="sxs-lookup"><span data-stu-id="4bb3b-116">Encrypted Media Extensions \(EME\) extends the video and audio elements to enable Digital Rights Management \(DRM\) protected content without using plug-ins.  Read more about EME:  [Encrypted Media Extensions](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span></span>  

### <span data-ttu-id="4bb3b-117">Gráficos</span><span class="sxs-lookup"><span data-stu-id="4bb3b-117">Graphics</span></span>  

<span data-ttu-id="4bb3b-118">EdgeHTML 13 presenta las siguientes actualizaciones de gráficos:</span><span class="sxs-lookup"><span data-stu-id="4bb3b-118">EdgeHTML 13 introduces the following graphics updates:</span></span>  

*   [<span data-ttu-id="4bb3b-119">Elipse del lienzo</span><span class="sxs-lookup"><span data-stu-id="4bb3b-119">Canvas ellipse</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [<span data-ttu-id="4bb3b-120">Modos de fusión de Canvas</span><span class="sxs-lookup"><span data-stu-id="4bb3b-120">Canvas blending modes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> <span data-ttu-id="4bb3b-121">Element</span><span class="sxs-lookup"><span data-stu-id="4bb3b-121">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [<span data-ttu-id="4bb3b-122">Contenido externo SVG</span><span class="sxs-lookup"><span data-stu-id="4bb3b-122">SVG external content</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### <span data-ttu-id="4bb3b-123">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4bb3b-123">JavaScript</span></span>  

<span data-ttu-id="4bb3b-124">EdgeHTML 13 incluye [mejoras importantes y compatibilidad con nuevas características en Chakra](https://blogs.windows.com/msedgedev/2015/09/30), el motor de JavaScript que enciende Microsoft Edge, que incluye:</span><span class="sxs-lookup"><span data-stu-id="4bb3b-124">EdgeHTML 13 includes [major improvements and new feature support in Chakra](https://blogs.windows.com/msedgedev/2015/09/30), the JavaScript engine powering Microsoft Edge, including:</span></span>  

#### <span data-ttu-id="4bb3b-125">Nuevas características</span><span class="sxs-lookup"><span data-stu-id="4bb3b-125">New features</span></span>  

<span data-ttu-id="4bb3b-126">Activado de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="4bb3b-126">On by default</span></span>  

*   <span data-ttu-id="4bb3b-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) habilitado de forma predeterminada \([entrada de blog](https://blogs.windows.com/msedgedev/2015/11/10), [Demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span><span class="sxs-lookup"><span data-stu-id="4bb3b-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) enabled by default \([blog post](https://blogs.windows.com/msedgedev/2015/11/10), [demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span></span>  
*   <span data-ttu-id="4bb3b-128">[Clases](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015 \)</span><span class="sxs-lookup"><span data-stu-id="4bb3b-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)</span></span>  

#### <span data-ttu-id="4bb3b-129">Características experimentales de JavaScript</span><span class="sxs-lookup"><span data-stu-id="4bb3b-129">Experimental JavaScript features</span></span>  

<span data-ttu-id="4bb3b-130">Habilitado con</span><span class="sxs-lookup"><span data-stu-id="4bb3b-130">Enabled with</span></span> `about:flags`  

*   <span data-ttu-id="4bb3b-131">[Funciones asincrónicas](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016 \)</span><span class="sxs-lookup"><span data-stu-id="4bb3b-131">[Async functions](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)</span></span>  
*   <span data-ttu-id="4bb3b-132">[Operador exponencial](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016 \)</span><span class="sxs-lookup"><span data-stu-id="4bb3b-132">[Exponentiation operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)</span></span>  
*   <span data-ttu-id="4bb3b-133">[Desestructurar](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015 \)</span><span class="sxs-lookup"><span data-stu-id="4bb3b-133">[Destructuring](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)</span></span>  

### <span data-ttu-id="4bb3b-134">Entrada de usuario</span><span class="sxs-lookup"><span data-stu-id="4bb3b-134">User Input</span></span>  

<span data-ttu-id="4bb3b-135">Las siguientes características presentadas en EdgeHTML 13 mejoran la entrada de los usuarios:</span><span class="sxs-lookup"><span data-stu-id="4bb3b-135">The following features introduced in EdgeHTML 13 improve user input:</span></span>  

*   [\<meter\> <span data-ttu-id="4bb3b-136">Element</span><span class="sxs-lookup"><span data-stu-id="4bb3b-136">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [<span data-ttu-id="4bb3b-137">controlador de eventos no válido para el documento y la ventana de elementos</span><span class="sxs-lookup"><span data-stu-id="4bb3b-137">oninvalid event handler for the element document and window</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### <span data-ttu-id="4bb3b-138">Bloqueo de puntero</span><span class="sxs-lookup"><span data-stu-id="4bb3b-138">Pointer Lock</span></span>  

<span data-ttu-id="4bb3b-139">Microsoft Edge ahora es compatible con la API de bloqueo de puntero \(denominado previamente bloqueo de mouse \) para acceder a movimiento sin formato del mouse, bloquear el destino de los eventos del mouse a un solo elemento, eliminando los límites de la distancia hasta la que se puede mover el mouse en una sola dirección y quitando el cursor de la vista.</span><span class="sxs-lookup"><span data-stu-id="4bb3b-139">Microsoft Edge now supports the Pointer Lock API \(previously called Mouse Lock\) for access to raw mouse movement, locking the target of mouse events to a single element, eliminating limits of how far mouse movement can go in a single direction, and removing the cursor from view.</span></span>  

## <span data-ttu-id="4bb3b-140">Nuevas API en EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="4bb3b-140">New APIs in EdgeHTML 13</span></span>  

<span data-ttu-id="4bb3b-141">Esta es la lista completa de las API nuevas en EdgeHTML 13.</span><span class="sxs-lookup"><span data-stu-id="4bb3b-141">Here's the full list of new APIs in EdgeHTML 13.</span></span>  <span data-ttu-id="4bb3b-142">Se muestran en el formato de `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="4bb3b-142">They are listed in the format of `[interface name].[api name]`.</span></span>  

<iframe height='584' scrolling='no' title='<span data-ttu-id="4bb3b-143">Nuevas API en EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="4bb3b-143">New APIs in EdgeHTML 13</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'><span data-ttu-id="4bb3b-144">Consulta las <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> nuevas API de Pen en EdgeHTML 13 de </a> docs Edge ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) en <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="4bb3b-144">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'>New APIs in EdgeHTML 13</a> by Microsoft Edge Docs (<a href='http://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span></iframe>  

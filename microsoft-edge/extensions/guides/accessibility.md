---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Para asegurarse de que el icono de extensión esté visible mientras se encuentra en modo Light y Dark, siga la guía de accesibilidad.
title: 'Extensiones: accesibilidad'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 514e68fc1b797a28c76bda79c8fab88b4ea2216c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573662"
---
# <span data-ttu-id="49b62-104">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="49b62-104">Accessibility</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="49b62-105">Crear iconos de extensión accesibles para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="49b62-105">Creating accessible extension icons for Microsoft Edge</span></span>

<span data-ttu-id="49b62-106">Se recomienda a los desarrolladores de extensiones de terceros que usen recursos de imagen que cumplan con los requisitos de accesibilidad estrictos de Microsoft, de modo que los iconos estén claramente visibles para los temas Light y Dark.</span><span class="sxs-lookup"><span data-stu-id="49b62-106">Third-party extension developers are encouraged to use image assets that meet Microsoft’s strict accessibility requirements so that icons are clearly visible for both light and dark themes.</span></span> <span data-ttu-id="49b62-107">Recomendamos que todos los iconos de extensión tengan una relación de 14:1 entre el color de fondo del icono y el color dominante del propio icono.</span><span class="sxs-lookup"><span data-stu-id="49b62-107">We recommend that all extension icons have a 14:1 ratio between the icon’s background color and the dominant color of the icon itself.</span></span>


<span data-ttu-id="49b62-108">Las extensiones de origen desarrolladas por Microsoft aplican un tratamiento visual "adhesivo" para cumplir con estos requisitos.</span><span class="sxs-lookup"><span data-stu-id="49b62-108">First-party extensions developed by Microsoft apply a “stickering” visual treatment to satisfy these requirements.</span></span>

### <span data-ttu-id="49b62-109">Ejemplos de la "pegatina"</span><span class="sxs-lookup"><span data-stu-id="49b62-109">Examples of the "stickering"</span></span>

<span data-ttu-id="49b62-110">El principal objetivo de "etiquetar" es hacer que el icono sea visualmente accesible en cualquier color de fondo.</span><span class="sxs-lookup"><span data-stu-id="49b62-110">The main goal of “stickering” is to make the icon visually accessible on any background color.</span></span> <span data-ttu-id="49b62-111">La relación de color recomendada entre el trazo exterior blanco y el icono debe ser de 14:1 para admitir los requisitos de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="49b62-111">The recommended color ratio between the white outer stroke and your icon should be 14:1 to support the high contrast requirements.</span></span>

#### <span data-ttu-id="49b62-112">Icono de buena</span><span class="sxs-lookup"><span data-stu-id="49b62-112">Good icon</span></span>
<span data-ttu-id="49b62-113">Con las pegatinas, un icono oscuro principalmente permanecerá visible en cualquier color de fondo.</span><span class="sxs-lookup"><span data-stu-id="49b62-113">With stickering, a primarily dark icon will remain visible on any background color.</span></span>


![imagen del icono visible en cualquier color de fondo](./../media/accessibility-light-to-dark-good.png)

#### <span data-ttu-id="49b62-115">Icono incorrecto</span><span class="sxs-lookup"><span data-stu-id="49b62-115">Bad icon</span></span>
<span data-ttu-id="49b62-116">Sin etiquetar, un icono se puede fusionar con el fondo y resulta imposible de ver.</span><span class="sxs-lookup"><span data-stu-id="49b62-116">Without stickering, an icon could blend in with the background and become impossible to see.</span></span>


![imagen de la combinación de iconos en el fondo negro](./../media/accessibility-light-to-dark-bad.png)

### <span data-ttu-id="49b62-118">Icono de extensión</span><span class="sxs-lookup"><span data-stu-id="49b62-118">"Stickering" your extension icon</span></span>

<span data-ttu-id="49b62-119">Los siguientes cinco pasos describen el método sugerido para crear un icono de extensión que cumpla con los requisitos de accesibilidad de Microsoft:</span><span class="sxs-lookup"><span data-stu-id="49b62-119">The following five steps outline the suggested method of creating an extension icon that meets Microsoft’s accessibility requirements:</span></span>


| <span data-ttu-id="49b62-120">Paso 1</span><span class="sxs-lookup"><span data-stu-id="49b62-120">Step 1</span></span>                                       | <span data-ttu-id="49b62-121">Paso 2</span><span class="sxs-lookup"><span data-stu-id="49b62-121">Step 2</span></span>                                       | <span data-ttu-id="49b62-122">Paso 3</span><span class="sxs-lookup"><span data-stu-id="49b62-122">Step 3</span></span>                                                                                 | <span data-ttu-id="49b62-123">Paso 4</span><span class="sxs-lookup"><span data-stu-id="49b62-123">Step 4</span></span>                                                                          | <span data-ttu-id="49b62-124">Paso 5</span><span class="sxs-lookup"><span data-stu-id="49b62-124">Step 5</span></span>                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="49b62-125">Establezca el icono en la cuadrícula especificada.</span><span class="sxs-lookup"><span data-stu-id="49b62-125">Set your icon within your specified grid.</span></span>    | <span data-ttu-id="49b62-126">Reduzca el tamaño del icono en 2 píxeles.</span><span class="sxs-lookup"><span data-stu-id="49b62-126">Reduce your icon size by 2 pixels.</span></span>           | <span data-ttu-id="49b62-127">Copie el icono y péguelo en su sitio.</span><span class="sxs-lookup"><span data-stu-id="49b62-127">Copy your icon and paste in place.</span></span> <span data-ttu-id="49b62-128">Crear un trazo exterior de 2 píxeles con esquinas redondeadas.</span><span class="sxs-lookup"><span data-stu-id="49b62-128">Create a 2 pixel outer stroke with rounded corners.</span></span> | <span data-ttu-id="49b62-129">Esquematizar el trazo, soltar el trazado compuesto y combinar las formas restantes.</span><span class="sxs-lookup"><span data-stu-id="49b62-129">Outline your stroke, release the compound path, and merge the remaining shapes.</span></span> | <span data-ttu-id="49b62-130">Colorea el trazo exterior blanco y el icono interno como desee.</span><span class="sxs-lookup"><span data-stu-id="49b62-130">Color the outer stroke white and the inner icon as you wish.</span></span> |
| ![step1](./../media/accessibility-step1.png) | ![step2](./../media/accessibility-step2.png) | ![step3](./../media/accessibility-step3.png)                                           | ![step4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |


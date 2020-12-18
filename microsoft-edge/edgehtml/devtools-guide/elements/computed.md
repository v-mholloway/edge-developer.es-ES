---
description: Usar el panel calculado para comprender cómo se organizan en cascada y se calculan CSS en elementos de página
title: 'DevTools-Elements: calculado'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, elementos, CSS, valor calculado, modelo de cuadro
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e88b96a08ac22c56ac6578495311931d265247bb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236014"
---
# <span data-ttu-id="09f41-104">Calculado</span><span class="sxs-lookup"><span data-stu-id="09f41-104">Computed</span></span>

<span data-ttu-id="09f41-105">Vea un diagrama de modelo de cuadro (ancho, relleno, borde, margen y valores de desplazamiento) del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="09f41-105">See a box model diagram (width, padding, border, margin and offset values) of the selected element.</span></span> <span data-ttu-id="09f41-106">Si activa la herramienta de **resaltado de elementos** ( `Ctrl+Shift+L` ), las mismas regiones de colores en el diagrama (para ancho, relleno, etc.) superpuesto al elemento representado al seleccionarlo en la página.</span><span class="sxs-lookup"><span data-stu-id="09f41-106">If you turn on the **Element highlighting** tool (`Ctrl+Shift+L`), the same colored regions in the diagram (for width, padding, etc.) that will overlay the rendered element when you select it on the page.</span></span> <span data-ttu-id="09f41-107">Puede modificar cualquier valor del diagrama haciendo clic en él.</span><span class="sxs-lookup"><span data-stu-id="09f41-107">You can edit any value in the diagram by clicking it.</span></span> 

<span data-ttu-id="09f41-108">Debajo del diagrama de modelo de cuadro se encuentra una lista modificable y editable de propiedades de estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="09f41-108">Below the box model diagram is a filterable and editable list of computed style properties.</span></span> <span data-ttu-id="09f41-109">Si se desactiva una propiedad actualmente activa, se activa la siguiente propiedad de la cascada, si existe alguna.</span><span class="sxs-lookup"><span data-stu-id="09f41-109">Turning off a currently active property activates the next property in the cascade, if one exists.</span></span> <span data-ttu-id="09f41-110">Puede ver los cambios en el panel de [**cambios**](./changes.md) .</span><span class="sxs-lookup"><span data-stu-id="09f41-110">You can view your changes in the [**Changes**](./changes.md) pane.</span></span>

<span data-ttu-id="09f41-111">De forma predeterminada, el botón **Mostrar solo estilos de usuario** está activado.</span><span class="sxs-lookup"><span data-stu-id="09f41-111">The **Display user styles only** button is on by default.</span></span> <span data-ttu-id="09f41-112">Al presionar el botón se incluirán estilos de la *hoja* de estilos predeterminada de Microsoft Edge en la lista de estilos calculados.</span><span class="sxs-lookup"><span data-stu-id="09f41-112">Depressing the button will include styles from the *default stylesheet* of Microsoft Edge in the computed styles list.</span></span>

![Panel calculado](../media/elements_computed.png)

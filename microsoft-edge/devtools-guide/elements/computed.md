---
description: Usar el panel calculado para comprender cómo se organizan en cascada y se calculan CSS en elementos de página
title: 'DevTools-Elements: calculado'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/10/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, elementos, CSS, valor calculado, modelo de cuadro
ms.custom: seodec18
ms.openlocfilehash: c7b1b7c86f30e6947442c9b3d0e8856074ce4c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574616"
---
# <span data-ttu-id="f5869-104">Calcula</span><span class="sxs-lookup"><span data-stu-id="f5869-104">Computed</span></span>

<span data-ttu-id="f5869-105">Vea un diagrama de modelo de cuadro (ancho, relleno, borde, margen y valores de desplazamiento) del elemento seleccionado.</span><span class="sxs-lookup"><span data-stu-id="f5869-105">See a box model diagram (width, padding, border, margin and offset values) of the selected element.</span></span> <span data-ttu-id="f5869-106">Si activa la herramienta de **resaltado de elementos** ( `Ctrl+Shift+L` ), las mismas regiones de colores en el diagrama (para ancho, relleno, etc.) superpuesto al elemento representado al seleccionarlo en la página.</span><span class="sxs-lookup"><span data-stu-id="f5869-106">If you turn on the **Element highlighting** tool (`Ctrl+Shift+L`), the same colored regions in the diagram (for width, padding, etc.) that will overlay the rendered element when you select it on the page.</span></span> <span data-ttu-id="f5869-107">Puede modificar cualquier valor del diagrama haciendo clic en él.</span><span class="sxs-lookup"><span data-stu-id="f5869-107">You can edit any value in the diagram by clicking it.</span></span> 

<span data-ttu-id="f5869-108">Debajo del diagrama de modelo de cuadro se encuentra una lista modificable y editable de propiedades de estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="f5869-108">Below the box model diagram is a filterable and editable list of computed style properties.</span></span> <span data-ttu-id="f5869-109">Si se desactiva una propiedad actualmente activa, se activa la siguiente propiedad de la cascada, si existe alguna.</span><span class="sxs-lookup"><span data-stu-id="f5869-109">Turning off a currently active property activates the next property in the cascade, if one exists.</span></span> <span data-ttu-id="f5869-110">Puede ver los cambios en el panel de [**cambios**](./changes.md) .</span><span class="sxs-lookup"><span data-stu-id="f5869-110">You can view your changes in the [**Changes**](./changes.md) pane.</span></span>

<span data-ttu-id="f5869-111">De forma predeterminada, el botón **Mostrar solo estilos de usuario** está activado.</span><span class="sxs-lookup"><span data-stu-id="f5869-111">The **Display user styles only** button is on by default.</span></span> <span data-ttu-id="f5869-112">Al presionar el botón se incluirán estilos de la *hoja* de estilos predeterminada de Microsoft Edge en la lista de estilos calculados.</span><span class="sxs-lookup"><span data-stu-id="f5869-112">Depressing the button will include styles from the *default stylesheet* of Microsoft Edge in the computed styles list.</span></span>

![Panel calculado](../media/elements_computed.png)
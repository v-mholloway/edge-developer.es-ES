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
# Calcula

Vea un diagrama de modelo de cuadro (ancho, relleno, borde, margen y valores de desplazamiento) del elemento seleccionado. Si activa la herramienta de **resaltado de elementos** ( `Ctrl+Shift+L` ), las mismas regiones de colores en el diagrama (para ancho, relleno, etc.) superpuesto al elemento representado al seleccionarlo en la página. Puede modificar cualquier valor del diagrama haciendo clic en él. 

Debajo del diagrama de modelo de cuadro se encuentra una lista modificable y editable de propiedades de estilo calculado. Si se desactiva una propiedad actualmente activa, se activa la siguiente propiedad de la cascada, si existe alguna. Puede ver los cambios en el panel de [**cambios**](./changes.md) .

De forma predeterminada, el botón **Mostrar solo estilos de usuario** está activado. Al presionar el botón se incluirán estilos de la *hoja* de estilos predeterminada de Microsoft Edge en la lista de estilos calculados.

![Panel calculado](../media/elements_computed.png)
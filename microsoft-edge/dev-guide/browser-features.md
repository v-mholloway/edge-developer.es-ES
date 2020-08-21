---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Guías para las características del explorador en Microsoft Edge.
title: Guía para desarrolladores y exploradores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 854b0e8ac057db3cc8b53af6205404d0841dfdb4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942039"
---
# Características del explorador  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

## Directivas de reproducción automática  

 Microsoft Edge proporciona a los clientes la posibilidad de personalizar sus preferencias de navegación en sitios web con sonido de reproducción automática con el fin de minimizar las distracciones en la web y ahorrar ancho de banda.  Los usuarios pueden personalizar el comportamiento de los medios con controles de reproducción automática globales y por sitio.  Además, Microsoft Edge elimina automáticamente la reproducción automática de los elementos multimedia en las pestañas de fondo.  

Consulte [directivas de reproducción automática](./browser-features/autoplay-policies.md) para obtener detalles y procedimientos recomendados para garantizar una buena experiencia de usuario con los elementos multimedia hospedados en su sitio.  

## Flash  

Si se usa Flash en la página pero el usuario no lo ha habilitado, Microsoft Edge normalmente mostrará un icono de pieza de Puzzle en la barra de direcciones.  Si va a agregar dinámicamente el control de flash después de que se cargue la página, es posible que no se muestre el icono del rompecabezas, en cuyo caso deseará [comprobar si flash está cargado y proporcionar una experiencia de reserva correcta](./browser-features/flash.md) si no está presente.  

## Vista de lectura  

Microsoft Edge ofrece una [vista de lectura](./browser-features/reading-view.md) para obtener una experiencia de lectura más fluida, como las páginas web, sin la distracción de contenido no relacionado u otro contenido secundario en la página.  Estas son algunas sugerencias sobre cómo garantizar una estupenda experiencia de lectura con el sitio, así como instrucciones para que el sitio quede fuera de la vista de lectura.  

## Búsqueda de detección de proveedor  

La barra de direcciones de Microsoft Edge está integrada en la integración de búsqueda enriquecida, incluidas las sugerencias de búsqueda, los resultados de la web, el historial de exploración y los favoritos.  [Aquí tienes más información sobre los proveedores de búsqueda](./browser-features/search-provider-discovery.md) que desean proporcionar soporte técnico para Microsoft Edge.  

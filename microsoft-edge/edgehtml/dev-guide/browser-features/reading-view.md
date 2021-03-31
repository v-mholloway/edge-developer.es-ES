---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Vea cómo Microsoft Edge proporciona una vista de lectura para las páginas web para habilitar la lectura sin adición.
title: 'Vista de lectura: Guía para desarrolladores'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 30c01d61ff896cca7b0af90b345a8619307f91c0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236452"
---
# Vista de lectura  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Microsoft Edge ofrece una vista de lectura para obtener una experiencia de lectura más fluida y simplificada de las páginas web sin la distracción de contenido no relacionado u otro contenido secundario de la página.  La vista de lectura se puede activar o desactivar desde la **vista de lectura** \(icono de libro \) en la barra de direcciones o con `Ctrl` + `Shift` + `R` .  La vista de lectura extrae los siguientes metadatos de una página:  

*   Title
*   Autorización
*   Date
*   Publicador
*   Imagen dominante \(s \)
*   Títulos de la imagen dominante \(s \)
*   Imágenes secundarias
*   Contenido de texto principal de la página
*   Copyright

Los usuarios pueden ajustar el contraste de la página y el tamaño de la fuente en el panel de **configuración** de Microsoft Edge.  

## Extracción de metadatos  

Estos son los detalles de los metadatos de página representados por la vista de lectura.  

### Title  

Para asegurarse de que la vista de lectura represente el título del artículo:  

*   Incluir un `title` elemento en el encabezado  
*   Incluir una etiqueta meta con `name="title"`  
*   Busque el texto de título en el cuerpo del artículo con la cadena de contenido de la etiqueta meta.  Canalizaciones \( `|` \) en la cadena de contenido impiden que la vista de lector se active, intente usar guiones \( `-` \) en su lugar.  

### Autorización  

La vista de lectura buscará un elemento `class = "byline-name"` .  El procedimiento recomendado es colocar el nombre del autor después del título y antes del cuerpo del artículo.  

```html
<div class="byline-name">Author name</div>
```  

### Date  

La vista de lectura representará el editor y la información de fecha en la misma línea, con estilos adicionales para resaltar esta información.  La fecha de publicación del artículo se representará exactamente como aparece en la cadena.  La vista de lectura no se convierte en un formato de fecha específico.  

Si tiene una fecha en el cuerpo del artículo y desea que la vista de lectura la represente, asigne el elemento que contiene la fecha con la clase `'dateline'` :  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

Si no tiene una fecha en el cuerpo del artículo pero desea que la vista de lectura represente la fecha, use la etiqueta meta `name='displaydate'` :  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### Publicador  

La vista de lectura buscará el protocolo Open Graph `"og:site_name"` para representar la información del editor.  También busca `source_organization` y `publisher` los atributos de cualquier etiqueta HTML como un indicador secundario de la información de Publisher en la página.  El texto del editor se hipervínculo a la dirección URL de la página con el estilo de hipervínculo de la página vista de lectura.  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### Imágenes  

La vista de lectura captura la mayoría de las imágenes sin formato con ancho >= 400px y relación de aspecto >= 1/3 y =< 3,0.  Es posible que todavía se extraigan las imágenes que no cumplan con estas dimensiones, como las que tienen un ancho menor que 400px, pero tienen subtítulos.  La primera imagen elegible se convierte en la imagen dominante del artículo.  La imagen dominante se representa como la primera pieza de contenido y tiene un ancho de columna completo.  Todas las imágenes siguientes se representan como imágenes en línea en el artículo.  

### Subtítulos  

El procedimiento recomendado es colocar imágenes en etiquetas de [figura](https://developer.mozilla.org/docs/Web/HTML/Element/figure) con un máximo de dos etiquetas [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) anidadas.  

### Body  

Para asegurarse de que se captura todo el texto del cuerpo de la página en la vista de lectura, es útil mantener la mayor parte del texto del artículo con el mismo tamaño de fuente y profundidad del DOM.  El algoritmo vista de lectura permite una cierta desviación de esta regla para que los editores tengan la libertad de enfatizar las líneas o las palabras.  

### Copyright  

La vista de lectura extrae y muestra información de copyright denotada por etiquetas meta con `name = "copyright"` o si no existe información de metaetiquetas, un nodo de texto que contiene el símbolo de copyright \( `©` \).  Vista de lectura muestra información de propiedad intelectual al final del artículo cuerpo principal, con un estilo con un tamaño de fuente más pequeño que el texto del cuerpo principal.  

```html
<meta name="copyright" content="Your copyright information">
```  

## Retirar la vista de lectura  

Si cree que el contenido no es una buena opción para la vista de lectura, puede usar la siguiente etiqueta meta para no participar en esta característica:  

```html
<meta name="IE_RM_OFF" content="true">
```  

Con esta etiqueta, el botón **vista de lectura** no aparecerá en la barra de direcciones cuando los usuarios vean la página.  

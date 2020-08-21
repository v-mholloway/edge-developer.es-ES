---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Vea cómo Microsoft Edge proporciona una vista de lectura para las páginas web para habilitar la lectura sin adición.
title: 'Vista de lectura: Guía para desarrolladores'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: 0d2076a63f97ecf2b4699795b0036736d0f95c9c
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942001"
---
# <span data-ttu-id="a0209-104">Vista de lectura</span><span class="sxs-lookup"><span data-stu-id="a0209-104">Reading view</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="a0209-105">Microsoft Edge ofrece una vista de lectura para obtener una experiencia de lectura más fluida y simplificada de las páginas web sin la distracción de contenido no relacionado u otro contenido secundario de la página.</span><span class="sxs-lookup"><span data-stu-id="a0209-105">Microsoft Edge provides a reading view for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="a0209-106">La vista de lectura se puede activar o desactivar desde la **vista de lectura** \ (icono de libro \) en la barra de direcciones o con `Ctrl` + `Shift` + `R` .</span><span class="sxs-lookup"><span data-stu-id="a0209-106">Reading view can be toggled on or off from the **Reading view** \(book icon\) button on the address bar or with `Ctrl`+`Shift`+`R`.</span></span>  <span data-ttu-id="a0209-107">La vista de lectura extrae los siguientes metadatos de una página:</span><span class="sxs-lookup"><span data-stu-id="a0209-107">Reading view extracts the following metadata from a page:</span></span>  

*   <span data-ttu-id="a0209-108">Title</span><span class="sxs-lookup"><span data-stu-id="a0209-108">Title</span></span>
*   <span data-ttu-id="a0209-109">Autorización</span><span class="sxs-lookup"><span data-stu-id="a0209-109">Author</span></span>
*   <span data-ttu-id="a0209-110">Date</span><span class="sxs-lookup"><span data-stu-id="a0209-110">Date</span></span>
*   <span data-ttu-id="a0209-111">Publicador</span><span class="sxs-lookup"><span data-stu-id="a0209-111">Publisher</span></span>
*   <span data-ttu-id="a0209-112">Imagen dominante \ (s \)</span><span class="sxs-lookup"><span data-stu-id="a0209-112">Dominant image\(s\)</span></span>
*   <span data-ttu-id="a0209-113">Títulos de la imagen dominante \ (s \)</span><span class="sxs-lookup"><span data-stu-id="a0209-113">Captions of dominant image\(s\)</span></span>
*   <span data-ttu-id="a0209-114">Imágenes secundarias</span><span class="sxs-lookup"><span data-stu-id="a0209-114">Secondary images</span></span>
*   <span data-ttu-id="a0209-115">Contenido de texto principal de la página</span><span class="sxs-lookup"><span data-stu-id="a0209-115">Main text content of the page</span></span>
*   <span data-ttu-id="a0209-116">Copyright</span><span class="sxs-lookup"><span data-stu-id="a0209-116">Copyright</span></span>

<span data-ttu-id="a0209-117">Los usuarios pueden ajustar el contraste de la página y el tamaño de la fuente en el panel de **configuración** de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a0209-117">Users can then adjust the page contrast and font size from the Microsoft Edge **Settings** panel.</span></span>  

## <span data-ttu-id="a0209-118">Extracción de metadatos</span><span class="sxs-lookup"><span data-stu-id="a0209-118">Metadata extraction</span></span>  

<span data-ttu-id="a0209-119">Estos son los detalles de los metadatos de página representados por la vista de lectura.</span><span class="sxs-lookup"><span data-stu-id="a0209-119">Here are details of the page metadata rendered by reading view.</span></span>  

### <span data-ttu-id="a0209-120">Title</span><span class="sxs-lookup"><span data-stu-id="a0209-120">Title</span></span>  

<span data-ttu-id="a0209-121">Para asegurarse de que la vista de lectura represente el título del artículo:</span><span class="sxs-lookup"><span data-stu-id="a0209-121">To ensure Reading view renders your article's title:</span></span>  

*   <span data-ttu-id="a0209-122">Incluir un `title` elemento en el encabezado</span><span class="sxs-lookup"><span data-stu-id="a0209-122">Include a `title` element in your header</span></span>  
*   <span data-ttu-id="a0209-123">Incluir una etiqueta meta con</span><span class="sxs-lookup"><span data-stu-id="a0209-123">Include a meta tag with</span></span> `name="title"`  
*   <span data-ttu-id="a0209-124">Busque el texto de título en el cuerpo del artículo con la cadena de contenido de la etiqueta meta.</span><span class="sxs-lookup"><span data-stu-id="a0209-124">Match the title text in your article body with the content string of your meta tag.</span></span>  <span data-ttu-id="a0209-125">Canalizaciones \ ( `|` \) en la cadena de contenido impiden que la vista de lector se active, intente usar guiones \ ( `-` \) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a0209-125">Pipes \(`|`\) in your content string prevent the reader view from becoming active, try using hyphens \(`-`\) instead.</span></span>  

### <span data-ttu-id="a0209-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="a0209-126">Author</span></span>  

<span data-ttu-id="a0209-127">La vista de lectura buscará un elemento `class = "byline-name"` .</span><span class="sxs-lookup"><span data-stu-id="a0209-127">Reading View will look for an element with `class = "byline-name"`.</span></span>  <span data-ttu-id="a0209-128">El procedimiento recomendado es colocar el nombre del autor después del título y antes del cuerpo del artículo.</span><span class="sxs-lookup"><span data-stu-id="a0209-128">Best practice is to place the author name after the title and before the article body.</span></span>  

```html
<div class="byline-name">Author name</div>
```  

### <span data-ttu-id="a0209-129">Date</span><span class="sxs-lookup"><span data-stu-id="a0209-129">Date</span></span>  

<span data-ttu-id="a0209-130">La vista de lectura representará el editor y la información de fecha en la misma línea, con estilos adicionales para resaltar esta información.</span><span class="sxs-lookup"><span data-stu-id="a0209-130">Reading view will render the publisher and date information together on the same line, with additional styling to highlight this information.</span></span>  <span data-ttu-id="a0209-131">La fecha de publicación del artículo se representará exactamente como aparece en la cadena.</span><span class="sxs-lookup"><span data-stu-id="a0209-131">The article's publishing date will render exactly as it appears in the string.</span></span>  <span data-ttu-id="a0209-132">La vista de lectura no se convierte en un formato de fecha específico.</span><span class="sxs-lookup"><span data-stu-id="a0209-132">Reading view does not convert to a specific date format.</span></span>  

<span data-ttu-id="a0209-133">Si tiene una fecha en el cuerpo del artículo y desea que la vista de lectura la represente, asigne el elemento que contiene la fecha con la clase `'dateline'` :</span><span class="sxs-lookup"><span data-stu-id="a0209-133">If you have a date in your article body and would like Reading view to render it, assign the element containing the date with the class `'dateline'`:</span></span>  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

<span data-ttu-id="a0209-134">Si no tiene una fecha en el cuerpo del artículo pero desea que la vista de lectura represente la fecha, use la etiqueta meta `name='displaydate'` :</span><span class="sxs-lookup"><span data-stu-id="a0209-134">If you don't have a date in the article body but would like Reading view to render the date, use the meta tag `name='displaydate'`:</span></span>  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### <span data-ttu-id="a0209-135">Publicador</span><span class="sxs-lookup"><span data-stu-id="a0209-135">Publisher</span></span>  

<span data-ttu-id="a0209-136">La vista de lectura buscará el protocolo Open Graph `"og:site_name"` para representar la información del editor.</span><span class="sxs-lookup"><span data-stu-id="a0209-136">Reading view will look for the Open Graph protocol `"og:site_name"` to render the publisher information.</span></span>  <span data-ttu-id="a0209-137">También busca `source_organization` y `publisher` los atributos de cualquier etiqueta HTML como un indicador secundario de la información de Publisher en la página.</span><span class="sxs-lookup"><span data-stu-id="a0209-137">It also looks for `source_organization` and `publisher` attributes in any html tag as a secondary indicator of publisher information on the page.</span></span>  <span data-ttu-id="a0209-138">El texto del editor se hipervínculo a la dirección URL de la página con el estilo de hipervínculo de la página vista de lectura.</span><span class="sxs-lookup"><span data-stu-id="a0209-138">The publisher text will be hyperlinked to the URL of page using the Reading view page hyperlink style.</span></span>  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### <span data-ttu-id="a0209-139">Imágenes</span><span class="sxs-lookup"><span data-stu-id="a0209-139">Images</span></span>  

<span data-ttu-id="a0209-140">La vista de lectura captura la mayoría de las imágenes sin formato con ancho >= 400px y relación de aspecto >= 1/3 y =< 3,0.</span><span class="sxs-lookup"><span data-stu-id="a0209-140">Reading view captures most raw images with width >= 400px and aspect ratio >= 1/3 and =< 3.0.</span></span>  <span data-ttu-id="a0209-141">Es posible que todavía se extraigan las imágenes que no cumplan con estas dimensiones, como las que tienen un ancho menor que 400px, pero tienen subtítulos.</span><span class="sxs-lookup"><span data-stu-id="a0209-141">Images that do not meet these dimensions may still be extracted, such as images that are smaller than 400px in width but have captions.</span></span>  <span data-ttu-id="a0209-142">La primera imagen elegible se convierte en la imagen dominante del artículo.</span><span class="sxs-lookup"><span data-stu-id="a0209-142">The first eligible image becomes the dominant image of the article.</span></span>  <span data-ttu-id="a0209-143">La imagen dominante se representa como la primera pieza de contenido y tiene un ancho de columna completo.</span><span class="sxs-lookup"><span data-stu-id="a0209-143">The dominant image is rendered as the first piece of content and given full column width.</span></span>  <span data-ttu-id="a0209-144">Todas las imágenes siguientes se representan como imágenes en línea en el artículo.</span><span class="sxs-lookup"><span data-stu-id="a0209-144">All following images are rendered as inline images within the article.</span></span>  

### <span data-ttu-id="a0209-145">Subtítulos</span><span class="sxs-lookup"><span data-stu-id="a0209-145">Captions</span></span>  

<span data-ttu-id="a0209-146">El procedimiento recomendado es colocar imágenes en etiquetas de [figura](https://developer.mozilla.org/docs/Web/HTML/Element/figure) con un máximo de dos etiquetas [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) anidadas.</span><span class="sxs-lookup"><span data-stu-id="a0209-146">Best practice is to place images in [figure](https://developer.mozilla.org/docs/Web/HTML/Element/figure) tags with no more than two nested [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) tags.</span></span>  

### <span data-ttu-id="a0209-147">Body</span><span class="sxs-lookup"><span data-stu-id="a0209-147">Body</span></span>  

<span data-ttu-id="a0209-148">Para asegurarse de que se captura todo el texto del cuerpo de la página en la vista de lectura, es útil mantener la mayor parte del texto del artículo con el mismo tamaño de fuente y profundidad del DOM.</span><span class="sxs-lookup"><span data-stu-id="a0209-148">To ensure that all the body text of your page is captured by Reading view, it helps to keep most of the article text the same font size and DOM depth.</span></span>  <span data-ttu-id="a0209-149">El algoritmo vista de lectura permite una cierta desviación de esta regla para que los editores tengan la libertad de enfatizar las líneas o las palabras.</span><span class="sxs-lookup"><span data-stu-id="a0209-149">The reading view algorithm allows for some deviation from this rule so publishers can have the freedom to add emphasis to lines or words.</span></span>  

### <span data-ttu-id="a0209-150">Copyright</span><span class="sxs-lookup"><span data-stu-id="a0209-150">Copyright</span></span>  

<span data-ttu-id="a0209-151">La vista de lectura extrae y muestra información de copyright denotada por etiquetas meta con `name = "copyright"` o si no existe información de metaetiquetas, un nodo de texto que contiene el símbolo de copyright \ ( `©` \).</span><span class="sxs-lookup"><span data-stu-id="a0209-151">Reading view extracts and displays copyright information denoted by meta tags with `name = "copyright"`, or if no meta tag information exists, a text node that contains the copyright \(`©`\) symbol.</span></span>  <span data-ttu-id="a0209-152">Vista de lectura muestra información de propiedad intelectual al final del artículo cuerpo principal, con un estilo con un tamaño de fuente más pequeño que el texto del cuerpo principal.</span><span class="sxs-lookup"><span data-stu-id="a0209-152">Reading view displays copyright information at the end of the article main body, styled using a smaller font size than the main body text.</span></span>  

```html
<meta name="copyright" content="Your copyright information">
```  

## <span data-ttu-id="a0209-153">Retirar la vista de lectura</span><span class="sxs-lookup"><span data-stu-id="a0209-153">Opting out of Reading View</span></span>  

<span data-ttu-id="a0209-154">Si cree que el contenido no es una buena opción para la vista de lectura, puede usar la siguiente etiqueta meta para no participar en esta característica:</span><span class="sxs-lookup"><span data-stu-id="a0209-154">If you feel your content is not a good fit for Reading view, you can use the following meta tag to opt out of this feature:</span></span>  

```html
<meta name="IE_RM_OFF" content="true">
```  

<span data-ttu-id="a0209-155">Con esta etiqueta, el botón **vista de lectura** no aparecerá en la barra de direcciones cuando los usuarios vean la página.</span><span class="sxs-lookup"><span data-stu-id="a0209-155">With this tag, the **Reading view** button will not appear in the address bar when your users view your page.</span></span>  

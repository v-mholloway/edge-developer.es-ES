---
description: Referencia para el dominio CSS. Este dominio expone las operaciones de lectura y escritura de CSS. Todos los objetos CSS (hojas de estilos, reglas y estilos) tienen un `id` uso asociado en las siguientes operaciones en el objeto relacionado. Cada tipo de objeto tiene una `id` estructura específica, y no se pueden cambiar entre objetos de diferentes tipos. Los objetos CSS se pueden cargar mediante las `get*ForNode()` llamadas (que aceptan un identificador de nodo DOM). Un cliente también puede realizar un seguimiento de las hojas de estilos a través de los `styleSheetAdded` / `styleSheetRemoved` eventos y cargar posteriormente el contenido de la hoja de estilos necesaria con los `getStyleSheet[Text]()` métodos.
title: 'Dominio CSS: DevTools Protocol versión 0,2'
author: pelavall
ms.author: pelavall
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 939eda0ae2f5228657d35899ab75b39493eff917
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573746"
---
# <span data-ttu-id="dbf12-108">CSS</span><span class="sxs-lookup"><span data-stu-id="dbf12-108">CSS</span></span>
<span data-ttu-id="dbf12-109">Este dominio expone las operaciones de lectura y escritura de CSS.</span><span class="sxs-lookup"><span data-stu-id="dbf12-109">This domain exposes CSS read/write operations.</span></span> <span data-ttu-id="dbf12-110">Todos los objetos CSS (hojas de estilos, reglas y estilos) tienen un `id` uso asociado en las siguientes operaciones en el objeto relacionado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-110">All CSS objects (stylesheets, rules, and styles) have an associated `id` used in subsequent operations on the related object.</span></span> <span data-ttu-id="dbf12-111">Cada tipo de objeto tiene una `id` estructura específica, y no se pueden cambiar entre objetos de diferentes tipos.</span><span class="sxs-lookup"><span data-stu-id="dbf12-111">Each object type has a specific `id` structure, and those are not interchangeable between objects of different kinds.</span></span> <span data-ttu-id="dbf12-112">Los objetos CSS se pueden cargar mediante las `get*ForNode()` llamadas (que aceptan un identificador de nodo DOM).</span><span class="sxs-lookup"><span data-stu-id="dbf12-112">CSS objects can be loaded using the `get*ForNode()` calls (which accept a DOM node id).</span></span> <span data-ttu-id="dbf12-113">Un cliente también puede realizar un seguimiento de las hojas de estilos a través de los `styleSheetAdded` / `styleSheetRemoved` eventos y cargar posteriormente el contenido de la hoja de estilos necesaria con los `getStyleSheet[Text]()` métodos.</span><span class="sxs-lookup"><span data-stu-id="dbf12-113">A client can also keep track of stylesheets via the `styleSheetAdded`/`styleSheetRemoved` events and subsequently load the required stylesheet contents using the `getStyleSheet[Text]()` methods.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="dbf12-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbf12-114">Methods</span></span>**](#methods) | <span data-ttu-id="dbf12-115">[enable](#enable), [Disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span><span class="sxs-lookup"><span data-stu-id="dbf12-115">[enable](#enable), [disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode)</span></span> |
| [**<span data-ttu-id="dbf12-116">Eventos</span><span class="sxs-lookup"><span data-stu-id="dbf12-116">Events</span></span>**](#events) | <span data-ttu-id="dbf12-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span><span class="sxs-lookup"><span data-stu-id="dbf12-117">[styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved)</span></span> |
| [**<span data-ttu-id="dbf12-118">Tipos</span><span class="sxs-lookup"><span data-stu-id="dbf12-118">Types</span></span>**](#types) | <span data-ttu-id="dbf12-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage, CSSKeyframesRule](#platformfontusage) [, CSSKeyframeRule](#csskeyframesrule) [, CSSComputedStyleProperty](#csskeyframerule), [CSSStyleSheetHeader](#cssstylesheetheader) [CSSStyleSheetHeader](#csscomputedstyleproperty)</span><span class="sxs-lookup"><span data-stu-id="dbf12-119">[StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage](#platformfontusage), [CSSKeyframesRule](#csskeyframesrule), [CSSKeyframeRule](#csskeyframerule), [CSSComputedStyleProperty](#csscomputedstyleproperty), [CSSStyleSheetHeader](#cssstylesheetheader)</span></span> |
| [**<span data-ttu-id="dbf12-120">Dependencias</span><span class="sxs-lookup"><span data-stu-id="dbf12-120">Dependencies</span></span>**](#dependencies) | [<span data-ttu-id="dbf12-121">DOM</span><span class="sxs-lookup"><span data-stu-id="dbf12-121">DOM</span></span>](dom.md) |
## <span data-ttu-id="dbf12-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbf12-122">Methods</span></span>

### <span data-ttu-id="dbf12-123">habilitar</span><span class="sxs-lookup"><span data-stu-id="dbf12-123">enable</span></span>
<span data-ttu-id="dbf12-124">Habilita el agente de CSS para la página dada.</span><span class="sxs-lookup"><span data-stu-id="dbf12-124">Enables the CSS agent for the given page.</span></span> <span data-ttu-id="dbf12-125">Los clientes no deben suponer que el agente CSS se ha habilitado hasta que se recibe el resultado de este comando.</span><span class="sxs-lookup"><span data-stu-id="dbf12-125">Clients should not assume that the CSS agent has been enabled until the result of this command is received.</span></span>

</p>

---

### <span data-ttu-id="dbf12-126">deshabilitar </span><span class="sxs-lookup"><span data-stu-id="dbf12-126">disable</span></span>
<span data-ttu-id="dbf12-127">Deshabilita el agente de CSS para la página dada.</span><span class="sxs-lookup"><span data-stu-id="dbf12-127">Disables the CSS agent for the given page.</span></span>

</p>

---

### <span data-ttu-id="dbf12-128">getInlineStylesForNode</span><span class="sxs-lookup"><span data-stu-id="dbf12-128">getInlineStylesForNode</span></span>
<span data-ttu-id="dbf12-129">Devuelve los estilos definidos en línea (explícitamente en el atributo "style" y, de forma implícita, usando atributos DOM) para un nodo DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="dbf12-129">Returns the styles defined inline (explicitly in the "style" attribute and implicitly, using DOM attributes) for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-130">Parameters</span><span class="sxs-lookup"><span data-stu-id="dbf12-130">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-131">nodeId</span><span class="sxs-lookup"><span data-stu-id="dbf12-131">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-132">Devuelve</span><span class="sxs-lookup"><span data-stu-id="dbf12-132">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-133">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="dbf12-133">inlineStyle</span></span> <br /> <i><span data-ttu-id="dbf12-134">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-134">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="dbf12-135">Estilo en línea del nodo DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-135">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-136">attributesStyle</span><span class="sxs-lookup"><span data-stu-id="dbf12-136">attributesStyle</span></span> <br /> <i><span data-ttu-id="dbf12-137">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-137">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="dbf12-138">Estilo de elemento definido por atributo (por ejemplo, Obtenido de "width = 20 height = 100%").</span><span class="sxs-lookup"><span data-stu-id="dbf12-138">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="dbf12-139">getMatchedStylesForNode</span><span class="sxs-lookup"><span data-stu-id="dbf12-139">getMatchedStylesForNode</span></span>
<span data-ttu-id="dbf12-140">Devuelve los estilos solicitados para un nodo DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="dbf12-140">Returns requested styles for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-141">Parameters</span><span class="sxs-lookup"><span data-stu-id="dbf12-141">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-142">nodeId</span><span class="sxs-lookup"><span data-stu-id="dbf12-142">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-143">Devuelve</span><span class="sxs-lookup"><span data-stu-id="dbf12-143">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-144">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="dbf12-144">inlineStyle</span></span> <br /> <i><span data-ttu-id="dbf12-145">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-145">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="dbf12-146">Estilo en línea del nodo DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-146">Inline style for the specified DOM node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-147">attributesStyle</span><span class="sxs-lookup"><span data-stu-id="dbf12-147">attributesStyle</span></span> <br /> <i><span data-ttu-id="dbf12-148">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-148">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="dbf12-149">Estilo de elemento definido por atributo (por ejemplo, Obtenido de "width = 20 height = 100%").</span><span class="sxs-lookup"><span data-stu-id="dbf12-149">Attribute-defined element style (e.g. resulting from "width=20 height=100%").</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-150">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="dbf12-150">matchedCSSRules</span></span> <br /> <i><span data-ttu-id="dbf12-151">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-151">optional</span></span></i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="dbf12-152">Reglas CSS que coinciden con este nodo de todas las hojas de estilo vigentes.</span><span class="sxs-lookup"><span data-stu-id="dbf12-152">CSS rules matching this node, from all applicable stylesheets.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-153">pseudoElements</span><span class="sxs-lookup"><span data-stu-id="dbf12-153">pseudoElements</span></span> <br /> <i><span data-ttu-id="dbf12-154">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-154">optional</span></span></i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td><span data-ttu-id="dbf12-155">Coincidencias de pseudo estilo para este nodo.</span><span class="sxs-lookup"><span data-stu-id="dbf12-155">Pseudo style matches for this node.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-156">heredan</span><span class="sxs-lookup"><span data-stu-id="dbf12-156">inherited</span></span> <br /> <i><span data-ttu-id="dbf12-157">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-157">optional</span></span></i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td><span data-ttu-id="dbf12-158">Una cadena de estilos heredados (desde el elemento primario del nodo inmediato hasta la raíz del árbol DOM).</span><span class="sxs-lookup"><span data-stu-id="dbf12-158">A chain of inherited styles (from the immediate node parent up to the DOM tree root).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-159">cssKeyframesRules</span><span class="sxs-lookup"><span data-stu-id="dbf12-159">cssKeyframesRules</span></span> <br /> <i><span data-ttu-id="dbf12-160">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-160">optional</span></span></i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td><span data-ttu-id="dbf12-161">Una lista de animaciones con fotogramas clave CSS que coinciden con este nodo.</span><span class="sxs-lookup"><span data-stu-id="dbf12-161">A list of CSS keyframed animations matching this node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="dbf12-162">getPlatformFontsForNode</span><span class="sxs-lookup"><span data-stu-id="dbf12-162">getPlatformFontsForNode</span></span>
<span data-ttu-id="dbf12-163">Solicita información sobre las fuentes de la plataforma que usamos para representar el TextNodes secundario en el nodo dado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-163">Requests information about platform fonts which we used to render child TextNodes in the given node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-164">Parameters</span><span class="sxs-lookup"><span data-stu-id="dbf12-164">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-165">nodeId</span><span class="sxs-lookup"><span data-stu-id="dbf12-165">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-166">Devuelve</span><span class="sxs-lookup"><span data-stu-id="dbf12-166">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-167">otras</span><span class="sxs-lookup"><span data-stu-id="dbf12-167">fonts</span></span></td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td><span data-ttu-id="dbf12-168">Estadísticas de uso para cada fuente de plataforma empleada.</span><span class="sxs-lookup"><span data-stu-id="dbf12-168">Usage statistics for every employed platform font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="dbf12-169">getComputedStyleForNode</span><span class="sxs-lookup"><span data-stu-id="dbf12-169">getComputedStyleForNode</span></span>
<span data-ttu-id="dbf12-170">Devuelve el estilo calculado de un nodo DOM identificado por `nodeId` .</span><span class="sxs-lookup"><span data-stu-id="dbf12-170">Returns the computed style for a DOM node identified by `nodeId`.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-171">Parameters</span><span class="sxs-lookup"><span data-stu-id="dbf12-171">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-172">nodeId</span><span class="sxs-lookup"><span data-stu-id="dbf12-172">nodeId</span></span></td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-173">Devuelve</span><span class="sxs-lookup"><span data-stu-id="dbf12-173">Returns</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-174">computedStyle</span><span class="sxs-lookup"><span data-stu-id="dbf12-174">computedStyle</span></span></td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td><span data-ttu-id="dbf12-175">Estilo calculado para el nodo DOM especificado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-175">Computed style for the specified DOM node.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="dbf12-176">Eventos</span><span class="sxs-lookup"><span data-stu-id="dbf12-176">Events</span></span>

### <span data-ttu-id="dbf12-177">styleSheetAdded</span><span class="sxs-lookup"><span data-stu-id="dbf12-177">styleSheetAdded</span></span>
<span data-ttu-id="dbf12-178">Se desencadena cuando se agrega una hoja de estilos de un documento activo.</span><span class="sxs-lookup"><span data-stu-id="dbf12-178">Fired whenever an active document stylesheet is added.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-179">Parameters</span><span class="sxs-lookup"><span data-stu-id="dbf12-179">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-180">header</span><span class="sxs-lookup"><span data-stu-id="dbf12-180">header</span></span></td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td><span data-ttu-id="dbf12-181">Se ha agregado metainformación de hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf12-181">Added stylesheet metainfo.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="dbf12-182">styleSheetChanged</span><span class="sxs-lookup"><span data-stu-id="dbf12-182">styleSheetChanged</span></span>
<span data-ttu-id="dbf12-183">Se desencadena cuando se cambia una hoja de estilos como resultado de la operación del cliente.</span><span class="sxs-lookup"><span data-stu-id="dbf12-183">Fired whenever a stylesheet is changed as a result of the client operation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-184">Parameters</span><span class="sxs-lookup"><span data-stu-id="dbf12-184">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-185">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="dbf12-185">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### <span data-ttu-id="dbf12-186">styleSheetRemoved</span><span class="sxs-lookup"><span data-stu-id="dbf12-186">styleSheetRemoved</span></span>
<span data-ttu-id="dbf12-187">Se desencadena cuando se quita una hoja de estilos de un documento activo.</span><span class="sxs-lookup"><span data-stu-id="dbf12-187">Fired whenever an active document stylesheet is removed.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-188">Parameters</span><span class="sxs-lookup"><span data-stu-id="dbf12-188">Parameters</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-189">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="dbf12-189">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="dbf12-190">Identificador de la hoja de estilos que se ha quitado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-190">Identifier of the removed stylesheet.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="dbf12-191">Tipos</span><span class="sxs-lookup"><span data-stu-id="dbf12-191">Types</span></span>

### <a name="stylesheetid"></a> <span data-ttu-id="dbf12-192">StyleSheetId</span><span class="sxs-lookup"><span data-stu-id="dbf12-192">StyleSheetId</span></span> `string`



</p>

---

### <a name="pseudoelementmatches"></a> <span data-ttu-id="dbf12-193">PseudoElementMatches</span><span class="sxs-lookup"><span data-stu-id="dbf12-193">PseudoElementMatches</span></span> `object`

<span data-ttu-id="dbf12-194">Colección de reglas CSS para un solo pseudonombre.</span><span class="sxs-lookup"><span data-stu-id="dbf12-194">CSS rule collection for a single pseudo style.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-195">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-195">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-196">pseudoType</span><span class="sxs-lookup"><span data-stu-id="dbf12-196">pseudoType</span></span></td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td><span data-ttu-id="dbf12-197">Tipo de seudoelemento.</span><span class="sxs-lookup"><span data-stu-id="dbf12-197">Pseudo element type.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-198">Match</span><span class="sxs-lookup"><span data-stu-id="dbf12-198">matches</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="dbf12-199">Coincidencias de reglas CSS aplicables al pseudo estilo.</span><span class="sxs-lookup"><span data-stu-id="dbf12-199">Matches of CSS rules applicable to the pseudo style.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> <span data-ttu-id="dbf12-200">InheritedStyleEntry</span><span class="sxs-lookup"><span data-stu-id="dbf12-200">InheritedStyleEntry</span></span> `object`

<span data-ttu-id="dbf12-201">Colección de reglas CSS heredada del nodo antecesor.</span><span class="sxs-lookup"><span data-stu-id="dbf12-201">Inherited CSS rule collection from ancestor node.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-202">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-202">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-203">inlineStyle</span><span class="sxs-lookup"><span data-stu-id="dbf12-203">inlineStyle</span></span> <br /> <i><span data-ttu-id="dbf12-204">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-204">optional</span></span></i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="dbf12-205">El estilo en línea del nodo antecesor, si lo hay, en la cadena de herencia de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf12-205">The ancestor node's inline style, if any, in the style inheritance chain.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-206">matchedCSSRules</span><span class="sxs-lookup"><span data-stu-id="dbf12-206">matchedCSSRules</span></span></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td><span data-ttu-id="dbf12-207">Coincidencias de reglas CSS que coinciden con el nodo antecesor de la cadena de herencia de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf12-207">Matches of CSS rules matching the ancestor node in the style inheritance chain.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> <span data-ttu-id="dbf12-208">RuleMatch</span><span class="sxs-lookup"><span data-stu-id="dbf12-208">RuleMatch</span></span> `object`

<span data-ttu-id="dbf12-209">Coincidencia de datos para una regla CSS.</span><span class="sxs-lookup"><span data-stu-id="dbf12-209">Match data for a CSS rule.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-210">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-210">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-211">Filete</span><span class="sxs-lookup"><span data-stu-id="dbf12-211">rule</span></span></td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td><span data-ttu-id="dbf12-212">Regla CSS en la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-212">CSS rule in the match.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> <span data-ttu-id="dbf12-213">Valor</span><span class="sxs-lookup"><span data-stu-id="dbf12-213">Value</span></span> `object`

<span data-ttu-id="dbf12-214">Datos de un selector simple (delimitados por comas en una lista de selectores).</span><span class="sxs-lookup"><span data-stu-id="dbf12-214">Data for a simple selector (these are delimited by commas in a selector list).</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-215">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-215">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-216">texto</span><span class="sxs-lookup"><span data-stu-id="dbf12-216">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-217">Texto del valor.</span><span class="sxs-lookup"><span data-stu-id="dbf12-217">Value text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-218">rango</span><span class="sxs-lookup"><span data-stu-id="dbf12-218">range</span></span> <br /> <i><span data-ttu-id="dbf12-219">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-219">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="dbf12-220">Intervalo de valores en el recurso subyacente (si está disponible).</span><span class="sxs-lookup"><span data-stu-id="dbf12-220">Value range in the underlying resource (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> <span data-ttu-id="dbf12-221">SelectorList</span><span class="sxs-lookup"><span data-stu-id="dbf12-221">SelectorList</span></span> `object`

<span data-ttu-id="dbf12-222">Datos de la lista de selección.</span><span class="sxs-lookup"><span data-stu-id="dbf12-222">Selector list data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-223">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-223">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-224">selectores</span><span class="sxs-lookup"><span data-stu-id="dbf12-224">selectors</span></span></td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td><span data-ttu-id="dbf12-225">Selectores de la lista.</span><span class="sxs-lookup"><span data-stu-id="dbf12-225">Selectors in the list.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-226">texto</span><span class="sxs-lookup"><span data-stu-id="dbf12-226">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-227">Texto del selector de reglas.</span><span class="sxs-lookup"><span data-stu-id="dbf12-227">Rule selector text.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> <span data-ttu-id="dbf12-228">CSSRule</span><span class="sxs-lookup"><span data-stu-id="dbf12-228">CSSRule</span></span> `object`

<span data-ttu-id="dbf12-229">Representación de las reglas CSS.</span><span class="sxs-lookup"><span data-stu-id="dbf12-229">CSS rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-230">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-230">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-231">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="dbf12-231">styleSheetId</span></span> <br /> <i><span data-ttu-id="dbf12-232">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-232">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="dbf12-233">Identificador de hoja de estilos CSS (ausente para la hoja de estilos del agente de usuario y reglas de hoja de estilos especificadas por el usuario) esta regla proviene de.</span><span class="sxs-lookup"><span data-stu-id="dbf12-233">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-234">selectorList</span><span class="sxs-lookup"><span data-stu-id="dbf12-234">selectorList</span></span> <br /> <i><span data-ttu-id="dbf12-235">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-235">optional</span></span></i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td><span data-ttu-id="dbf12-236">Datos del selector de reglas.</span><span class="sxs-lookup"><span data-stu-id="dbf12-236">Rule selector data.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-237">origen</span><span class="sxs-lookup"><span data-stu-id="dbf12-237">origin</span></span> <br /> <i><span data-ttu-id="dbf12-238">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-238">optional</span></span></i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="dbf12-239">Origen de la hoja de estilos principal.</span><span class="sxs-lookup"><span data-stu-id="dbf12-239">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-240">estilo</span><span class="sxs-lookup"><span data-stu-id="dbf12-240">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="dbf12-241">Declaración de estilo asociada.</span><span class="sxs-lookup"><span data-stu-id="dbf12-241">Associated style declaration.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-242">medios</span><span class="sxs-lookup"><span data-stu-id="dbf12-242">media</span></span> <br /> <i><span data-ttu-id="dbf12-243">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-243">optional</span></span></i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td><span data-ttu-id="dbf12-244">Matriz de la lista de medios (para las reglas que implican consultas multimedia).</span><span class="sxs-lookup"><span data-stu-id="dbf12-244">Media list array (for rules involving media queries).</span></span> <span data-ttu-id="dbf12-245">La matriz enumera las consultas multimedia comenzando por la más interna, saliendo hacia afuera.</span><span class="sxs-lookup"><span data-stu-id="dbf12-245">The array enumerates media queries starting with the innermost one, going outwards.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> <span data-ttu-id="dbf12-246">SourceRange</span><span class="sxs-lookup"><span data-stu-id="dbf12-246">SourceRange</span></span> `object`

<span data-ttu-id="dbf12-247">Intervalo de texto dentro de un recurso.</span><span class="sxs-lookup"><span data-stu-id="dbf12-247">Text range within a resource.</span></span> <span data-ttu-id="dbf12-248">Los números se basan en cero.</span><span class="sxs-lookup"><span data-stu-id="dbf12-248">All numbers are zero-based.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-249">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-249">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-250">startLine</span><span class="sxs-lookup"><span data-stu-id="dbf12-250">startLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="dbf12-251">Línea de inicio del rango.</span><span class="sxs-lookup"><span data-stu-id="dbf12-251">Start line of range.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-252">Columnainicio</span><span class="sxs-lookup"><span data-stu-id="dbf12-252">startColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="dbf12-253">Columna de inicio del rango (incluido).</span><span class="sxs-lookup"><span data-stu-id="dbf12-253">Start column of range (inclusive).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-254">Fin</span><span class="sxs-lookup"><span data-stu-id="dbf12-254">endLine</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="dbf12-255">Línea de finalización de rango</span><span class="sxs-lookup"><span data-stu-id="dbf12-255">End line of range</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-256">Columnafin</span><span class="sxs-lookup"><span data-stu-id="dbf12-256">endColumn</span></span></td>
            <td><code class="flyout">integer</code></td>
            <td><span data-ttu-id="dbf12-257">Columna final del intervalo (exclusivo).</span><span class="sxs-lookup"><span data-stu-id="dbf12-257">End column of range (exclusive).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> <span data-ttu-id="dbf12-258">ShorthandEntry</span><span class="sxs-lookup"><span data-stu-id="dbf12-258">ShorthandEntry</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-259">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-259">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-260">name</span><span class="sxs-lookup"><span data-stu-id="dbf12-260">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-261">Nombre abreviado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-261">Shorthand name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-262">value</span><span class="sxs-lookup"><span data-stu-id="dbf12-262">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-263">Valor abreviado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-263">Shorthand value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-264">interés</span><span class="sxs-lookup"><span data-stu-id="dbf12-264">important</span></span> <br /> <i><span data-ttu-id="dbf12-265">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-265">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-266">Si la propiedad tiene una anotación "! Important" (implica `false` si no está presente).</span><span class="sxs-lookup"><span data-stu-id="dbf12-266">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> <span data-ttu-id="dbf12-267">CSSStyle</span><span class="sxs-lookup"><span data-stu-id="dbf12-267">CSSStyle</span></span> `object`

<span data-ttu-id="dbf12-268">Representación de estilo CSS.</span><span class="sxs-lookup"><span data-stu-id="dbf12-268">CSS style representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-269">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-269">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-270">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="dbf12-270">styleSheetId</span></span> <br /> <i><span data-ttu-id="dbf12-271">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-271">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="dbf12-272">Identificador de hoja de estilos CSS (ausente para la hoja de estilos del agente de usuario y reglas de hoja de estilos especificadas por el usuario) esta regla proviene de.</span><span class="sxs-lookup"><span data-stu-id="dbf12-272">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-273">cssProperties</span><span class="sxs-lookup"><span data-stu-id="dbf12-273">cssProperties</span></span></td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td><span data-ttu-id="dbf12-274">Propiedades de CSS en el estilo.</span><span class="sxs-lookup"><span data-stu-id="dbf12-274">CSS properties in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-275">shorthandEntries</span><span class="sxs-lookup"><span data-stu-id="dbf12-275">shorthandEntries</span></span></td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td><span data-ttu-id="dbf12-276">Valores calculados para todas las abreviaturas que se encuentran en el estilo.</span><span class="sxs-lookup"><span data-stu-id="dbf12-276">Computed values for all shorthands found in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-277">cssText</span><span class="sxs-lookup"><span data-stu-id="dbf12-277">cssText</span></span> <br /> <i><span data-ttu-id="dbf12-278">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-278">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-279">Texto de declaración de estilo (si está disponible).</span><span class="sxs-lookup"><span data-stu-id="dbf12-279">Style declaration text (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-280">rango</span><span class="sxs-lookup"><span data-stu-id="dbf12-280">range</span></span> <br /> <i><span data-ttu-id="dbf12-281">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-281">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="dbf12-282">Rango de declaración de estilo en la hoja de estilos envolvente (si está disponible).</span><span class="sxs-lookup"><span data-stu-id="dbf12-282">Style declaration range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> <span data-ttu-id="dbf12-283">CSSProperty</span><span class="sxs-lookup"><span data-stu-id="dbf12-283">CSSProperty</span></span> `object`

<span data-ttu-id="dbf12-284">Datos de declaración de propiedad de CSS.</span><span class="sxs-lookup"><span data-stu-id="dbf12-284">CSS property declaration data.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-285">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-285">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-286">name</span><span class="sxs-lookup"><span data-stu-id="dbf12-286">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-287">Nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="dbf12-287">The property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-288">value</span><span class="sxs-lookup"><span data-stu-id="dbf12-288">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-289">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="dbf12-289">The property value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-290">interés</span><span class="sxs-lookup"><span data-stu-id="dbf12-290">important</span></span> <br /> <i><span data-ttu-id="dbf12-291">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-291">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-292">Si la propiedad tiene una anotación "! Important" (implica `false` si no está presente).</span><span class="sxs-lookup"><span data-stu-id="dbf12-292">Whether the property has "!important" annotation (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-293">implícita</span><span class="sxs-lookup"><span data-stu-id="dbf12-293">implicit</span></span> <br /> <i><span data-ttu-id="dbf12-294">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-294">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-295">Si la propiedad es implícita (implica que está `false` ausente).</span><span class="sxs-lookup"><span data-stu-id="dbf12-295">Whether the property is implicit (implies `false` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-296">texto</span><span class="sxs-lookup"><span data-stu-id="dbf12-296">text</span></span> <br /> <i><span data-ttu-id="dbf12-297">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-297">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-298">El texto de propiedad completo según se especifica en el estilo.</span><span class="sxs-lookup"><span data-stu-id="dbf12-298">The full property text as specified in the style.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-299">parsedOk</span><span class="sxs-lookup"><span data-stu-id="dbf12-299">parsedOk</span></span> <br /> <i><span data-ttu-id="dbf12-300">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-300">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-301">Si el explorador entiende la propiedad (indica si no `true` existe).</span><span class="sxs-lookup"><span data-stu-id="dbf12-301">Whether the property is understood by the browser (implies `true` if absent).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-302">habilitar</span><span class="sxs-lookup"><span data-stu-id="dbf12-302">disabled</span></span> <br /> <i><span data-ttu-id="dbf12-303">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-303">optional</span></span></i></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-304">Si la propiedad está deshabilitada por el usuario (presente solo para las propiedades basadas en origen).</span><span class="sxs-lookup"><span data-stu-id="dbf12-304">Whether the property is disabled by the user (present for source-based properties only).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-305">rango</span><span class="sxs-lookup"><span data-stu-id="dbf12-305">range</span></span> <br /> <i><span data-ttu-id="dbf12-306">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-306">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="dbf12-307">Todo el rango de propiedades de la declaración de estilo envolvente (si está disponible).</span><span class="sxs-lookup"><span data-stu-id="dbf12-307">The entire property range in the enclosing style declaration (if available).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> <span data-ttu-id="dbf12-308">CSSMedia</span><span class="sxs-lookup"><span data-stu-id="dbf12-308">CSSMedia</span></span> `object`

<span data-ttu-id="dbf12-309">Descriptor de regla multimedia de CSS.</span><span class="sxs-lookup"><span data-stu-id="dbf12-309">CSS media rule descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-310">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-310">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-311">texto</span><span class="sxs-lookup"><span data-stu-id="dbf12-311">text</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-312">Texto de consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-312">Media query text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-313">origen</span><span class="sxs-lookup"><span data-stu-id="dbf12-313">source</span></span></td>
            <td><code class="flyout">string</code> <br /> <i><span data-ttu-id="dbf12-314">Valores permitidos: mediaRule, importRule, linkedSheet, inlineSheet</span><span class="sxs-lookup"><span data-stu-id="dbf12-314">Allowed values: mediaRule, importRule, linkedSheet, inlineSheet</span></span></i></td>
            <td><span data-ttu-id="dbf12-315">Origen de la consulta multimedia: "mediaRule" si se especifica mediante una regla @media, "importRule" si se especifica mediante una regla @import, "linkedSheet" si se especifica mediante un atributo "multimedia" en la etiqueta de vínculo de una hoja de estilos vinculada, "inlineSheet" si se especifica mediante un atributo "multimedia" en la etiqueta STYLE de una hoja de estilos en línea.</span><span class="sxs-lookup"><span data-stu-id="dbf12-315">Source of the media query: "mediaRule" if specified by a @media rule, "importRule" if specified by an @import rule, "linkedSheet" if specified by a "media" attribute in a linked stylesheet's LINK tag, "inlineSheet" if specified by a "media" attribute in an inline stylesheet's STYLE tag.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-316">sourceURL</span><span class="sxs-lookup"><span data-stu-id="dbf12-316">sourceURL</span></span> <br /> <i><span data-ttu-id="dbf12-317">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-317">optional</span></span></i></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-318">Dirección URL del documento que contiene la descripción de la consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-318">URL of the document containing the media query description.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-319">rango</span><span class="sxs-lookup"><span data-stu-id="dbf12-319">range</span></span> <br /> <i><span data-ttu-id="dbf12-320">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-320">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="dbf12-321">El intervalo de encabezado de la regla asociada (@media o @import) en la hoja de estilos envolvente (si está disponible).</span><span class="sxs-lookup"><span data-stu-id="dbf12-321">The associated rule (@media or @import) header range in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-322">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="dbf12-322">styleSheetId</span></span> <br /> <i><span data-ttu-id="dbf12-323">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-323">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="dbf12-324">Identificador de la hoja de estilos que contiene este objeto (si existe).</span><span class="sxs-lookup"><span data-stu-id="dbf12-324">Identifier of the stylesheet containing this object (if exists).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-325">mediaL</span><span class="sxs-lookup"><span data-stu-id="dbf12-325">mediaList</span></span> <br /> <i><span data-ttu-id="dbf12-326">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-326">optional</span></span></i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td><span data-ttu-id="dbf12-327">Matriz de consultas de medios.</span><span class="sxs-lookup"><span data-stu-id="dbf12-327">Array of media queries.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> <span data-ttu-id="dbf12-328">MediaQuery</span><span class="sxs-lookup"><span data-stu-id="dbf12-328">MediaQuery</span></span> `object`

<span data-ttu-id="dbf12-329">Descriptor de consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-329">Media query descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-330">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-330">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-331">manifestación</span><span class="sxs-lookup"><span data-stu-id="dbf12-331">expressions</span></span></td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td><span data-ttu-id="dbf12-332">Matriz de expresiones de consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-332">Array of media query expressions.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-333">activa</span><span class="sxs-lookup"><span data-stu-id="dbf12-333">active</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-334">Si se cumple la condición de la consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-334">Whether the media query condition is satisfied.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> <span data-ttu-id="dbf12-335">MediaQueryExpression</span><span class="sxs-lookup"><span data-stu-id="dbf12-335">MediaQueryExpression</span></span> `object`

<span data-ttu-id="dbf12-336">Descriptor de expresión de consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-336">Media query expression descriptor.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-337">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-337">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-338">value</span><span class="sxs-lookup"><span data-stu-id="dbf12-338">value</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="dbf12-339">Valor de la expresión de consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-339">Media query expression value.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-340">Departamento</span><span class="sxs-lookup"><span data-stu-id="dbf12-340">unit</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-341">Unidades de expresión de consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-341">Media query expression units.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-342">característica</span><span class="sxs-lookup"><span data-stu-id="dbf12-342">feature</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-343">Característica de expresión de consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="dbf12-343">Media query expression feature.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-344">valueRange</span><span class="sxs-lookup"><span data-stu-id="dbf12-344">valueRange</span></span> <br /> <i><span data-ttu-id="dbf12-345">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-345">optional</span></span></i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td><span data-ttu-id="dbf12-346">El intervalo asociado del texto del valor de la hoja de estilos envolvente (si está disponible).</span><span class="sxs-lookup"><span data-stu-id="dbf12-346">The associated range of the value text in the enclosing stylesheet (if available).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-347">computedLength</span><span class="sxs-lookup"><span data-stu-id="dbf12-347">computedLength</span></span> <br /> <i><span data-ttu-id="dbf12-348">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-348">optional</span></span></i></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="dbf12-349">Longitud calculada de la expresión de consulta multimedia (si corresponde).</span><span class="sxs-lookup"><span data-stu-id="dbf12-349">Computed length of media query expression (if applicable).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> <span data-ttu-id="dbf12-350">PlatformFontUsage</span><span class="sxs-lookup"><span data-stu-id="dbf12-350">PlatformFontUsage</span></span> `object`

<span data-ttu-id="dbf12-351">Información sobre la cantidad de glifos representados con la fuente dada.</span><span class="sxs-lookup"><span data-stu-id="dbf12-351">Information about amount of glyphs that were rendered with given font.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-352">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-352">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-353">familyName</span><span class="sxs-lookup"><span data-stu-id="dbf12-353">familyName</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-354">Nombre de familia de la fuente informado por la plataforma.</span><span class="sxs-lookup"><span data-stu-id="dbf12-354">Font's family name reported by platform.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-355">isCustomFont</span><span class="sxs-lookup"><span data-stu-id="dbf12-355">isCustomFont</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-356">Indica si la fuente se ha descargado o resuelto localmente.</span><span class="sxs-lookup"><span data-stu-id="dbf12-356">Indicates if the font was downloaded or resolved locally.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-357">glyphCount</span><span class="sxs-lookup"><span data-stu-id="dbf12-357">glyphCount</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="dbf12-358">Cantidad de glifos representados con esta fuente.</span><span class="sxs-lookup"><span data-stu-id="dbf12-358">Amount of glyphs that were rendered with this font.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> <span data-ttu-id="dbf12-359">CSSKeyframesRule</span><span class="sxs-lookup"><span data-stu-id="dbf12-359">CSSKeyframesRule</span></span> `object`

<span data-ttu-id="dbf12-360">Representación de regla de fotogramas clave CSS.</span><span class="sxs-lookup"><span data-stu-id="dbf12-360">CSS keyframes rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-361">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-361">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-362">animationName</span><span class="sxs-lookup"><span data-stu-id="dbf12-362">animationName</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="dbf12-363">Nombre de la animación.</span><span class="sxs-lookup"><span data-stu-id="dbf12-363">Animation name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-364">fotogramas clave</span><span class="sxs-lookup"><span data-stu-id="dbf12-364">keyframes</span></span></td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td><span data-ttu-id="dbf12-365">Lista de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="dbf12-365">List of keyframes.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> <span data-ttu-id="dbf12-366">CSSKeyframeRule</span><span class="sxs-lookup"><span data-stu-id="dbf12-366">CSSKeyframeRule</span></span> `object`

<span data-ttu-id="dbf12-367">Representación de la regla de fotograma clave CSS.</span><span class="sxs-lookup"><span data-stu-id="dbf12-367">CSS keyframe rule representation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-368">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-368">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-369">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="dbf12-369">styleSheetId</span></span> <br /> <i><span data-ttu-id="dbf12-370">opcional</span><span class="sxs-lookup"><span data-stu-id="dbf12-370">optional</span></span></i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="dbf12-371">Identificador de hoja de estilos CSS (ausente para la hoja de estilos del agente de usuario y reglas de hoja de estilos especificadas por el usuario) esta regla proviene de.</span><span class="sxs-lookup"><span data-stu-id="dbf12-371">The css style sheet identifier (absent for user agent stylesheet and user-specified stylesheet rules) this rule came from.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-372">origen</span><span class="sxs-lookup"><span data-stu-id="dbf12-372">origin</span></span></td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td><span data-ttu-id="dbf12-373">Origen de la hoja de estilos principal.</span><span class="sxs-lookup"><span data-stu-id="dbf12-373">Parent stylesheet's origin.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-374">keyText</span><span class="sxs-lookup"><span data-stu-id="dbf12-374">keyText</span></span></td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td><span data-ttu-id="dbf12-375">Texto de clave asociada.</span><span class="sxs-lookup"><span data-stu-id="dbf12-375">Associated key text.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-376">estilo</span><span class="sxs-lookup"><span data-stu-id="dbf12-376">style</span></span></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td><span data-ttu-id="dbf12-377">Declaración de estilo asociada.</span><span class="sxs-lookup"><span data-stu-id="dbf12-377">Associated style declaration.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> <span data-ttu-id="dbf12-378">CSSComputedStyleProperty</span><span class="sxs-lookup"><span data-stu-id="dbf12-378">CSSComputedStyleProperty</span></span> `object`



<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-379">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-379">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-380">name</span><span class="sxs-lookup"><span data-stu-id="dbf12-380">name</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-381">Nombre de propiedad de estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-381">Computed style property name.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-382">value</span><span class="sxs-lookup"><span data-stu-id="dbf12-382">value</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-383">Valor de propiedad de estilo calculado.</span><span class="sxs-lookup"><span data-stu-id="dbf12-383">Computed style property value.</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> <span data-ttu-id="dbf12-384">CSSStyleSheetHeader</span><span class="sxs-lookup"><span data-stu-id="dbf12-384">CSSStyleSheetHeader</span></span> `object`

<span data-ttu-id="dbf12-385">Metainformación CSS de hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf12-385">CSS stylesheet metainformation.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="dbf12-386">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbf12-386">Properties</span></span></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><span data-ttu-id="dbf12-387">styleSheetId</span><span class="sxs-lookup"><span data-stu-id="dbf12-387">styleSheetId</span></span></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td><span data-ttu-id="dbf12-388">Identificador de la hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf12-388">The stylesheet identifier.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-389">sourceURL</span><span class="sxs-lookup"><span data-stu-id="dbf12-389">sourceURL</span></span></td>
            <td><code class="flyout">string</code></td>
            <td><span data-ttu-id="dbf12-390">Dirección URL de recurso de hoja de estilos.</span><span class="sxs-lookup"><span data-stu-id="dbf12-390">Stylesheet resource URL.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-391">habilitar</span><span class="sxs-lookup"><span data-stu-id="dbf12-391">disabled</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-392">Indica si la hoja de estilos está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="dbf12-392">Denotes whether the stylesheet is disabled.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-393">isInline</span><span class="sxs-lookup"><span data-stu-id="dbf12-393">isInline</span></span></td>
            <td><code class="flyout">boolean</code></td>
            <td><span data-ttu-id="dbf12-394">Si se crea esta hoja de estilos para la etiqueta de estilo mediante Parser.</span><span class="sxs-lookup"><span data-stu-id="dbf12-394">Whether this stylesheet is created for STYLE tag by parser.</span></span> <span data-ttu-id="dbf12-395">Esta marca no está configurada para las etiquetas de estilo document. escrito.</span><span class="sxs-lookup"><span data-stu-id="dbf12-395">This flag is not set for document.written STYLE tags.</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-396">startLine</span><span class="sxs-lookup"><span data-stu-id="dbf12-396">startLine</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="dbf12-397">Desplazamiento de línea de la hoja de estilos en el recurso (basado en cero).</span><span class="sxs-lookup"><span data-stu-id="dbf12-397">Line offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-398">Columnainicio</span><span class="sxs-lookup"><span data-stu-id="dbf12-398">startColumn</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="dbf12-399">Desplazamiento de columna de la hoja de estilos dentro del recurso (basado en cero).</span><span class="sxs-lookup"><span data-stu-id="dbf12-399">Column offset of the stylesheet within the resource (zero based).</span></span></td>
        </tr>
        <tr>
            <td><span data-ttu-id="dbf12-400">longitud</span><span class="sxs-lookup"><span data-stu-id="dbf12-400">length</span></span></td>
            <td><code class="flyout">number</code></td>
            <td><span data-ttu-id="dbf12-401">Tamaño del contenido (en caracteres).</span><span class="sxs-lookup"><span data-stu-id="dbf12-401">Size of the content (in characters).</span></span></td>
        </tr>
    </tbody>
</table>
</p>

---

## <span data-ttu-id="dbf12-402">Dependencias</span><span class="sxs-lookup"><span data-stu-id="dbf12-402">Dependencies</span></span>

[<span data-ttu-id="dbf12-403">DOM</span><span class="sxs-lookup"><span data-stu-id="dbf12-403">DOM</span></span>](dom.md)

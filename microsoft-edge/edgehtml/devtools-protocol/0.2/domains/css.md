---
description: Referencia para el dominio CSS. Este dominio expone las operaciones de lectura y escritura de CSS. Todos los objetos CSS (hojas de estilos, reglas y estilos) tienen un `id` uso asociado en las siguientes operaciones en el objeto relacionado. Cada tipo de objeto tiene una `id` estructura específica, y no se pueden cambiar entre objetos de diferentes tipos. Los objetos CSS se pueden cargar mediante las `get*ForNode()` llamadas (que aceptan un identificador de nodo DOM). Un cliente también puede realizar un seguimiento de las hojas de estilos a través de los `styleSheetAdded` / `styleSheetRemoved` eventos y cargar posteriormente el contenido de la hoja de estilos necesaria con los `getStyleSheet[Text]()` métodos.
title: 'Dominio CSS: DevTools Protocol versión 0,2'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cf5efdef09b7e2d9041cd8536faaff8fb99a7f71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236344"
---
# CSS

Este dominio expone las operaciones de lectura y escritura de CSS. Todos los objetos CSS (hojas de estilos, reglas y estilos) tienen un `id` uso asociado en las siguientes operaciones en el objeto relacionado. Cada tipo de objeto tiene una `id` estructura específica, y no se pueden cambiar entre objetos de diferentes tipos. Los objetos CSS se pueden cargar mediante las `get*ForNode()` llamadas (que aceptan un identificador de nodo DOM). Un cliente también puede realizar un seguimiento de las hojas de estilos a través de los `styleSheetAdded` / `styleSheetRemoved` eventos y cargar posteriormente el contenido de la hoja de estilos necesaria con los `getStyleSheet[Text]()` métodos.

| | |
|-|-|
| [**Métodos**](#methods) | [enable](#enable), [Disable](#disable), [getInlineStylesForNode](#getinlinestylesfornode), [getMatchedStylesForNode](#getmatchedstylesfornode), [getPlatformFontsForNode](#getplatformfontsfornode), [getComputedStyleForNode](#getcomputedstylefornode) |
| [**Eventos**](#events) | [styleSheetAdded](#stylesheetadded), [styleSheetChanged](#stylesheetchanged), [styleSheetRemoved](#stylesheetremoved) |
| [**Tipos**](#types) | [StyleSheetId](#stylesheetid), [PseudoElementMatches](#pseudoelementmatches), [InheritedStyleEntry](#inheritedstyleentry), [RuleMatch](#rulematch), [Value](#value), [SelectorList](#selectorlist), [CSSRule](#cssrule), [SourceRange](#sourcerange), [ShorthandEntry](#shorthandentry), [CSSStyle](#cssstyle), [CSSProperty](#cssproperty), [CSSMedia](#cssmedia), [MediaQuery](#mediaquery), [MediaQueryExpression](#mediaqueryexpression), [PlatformFontUsage, CSSKeyframesRule](#platformfontusage) [, CSSKeyframeRule](#csskeyframesrule) [, CSSComputedStyleProperty](#csskeyframerule), [](#cssstylesheetheader) [CSSStyleSheetHeader](#csscomputedstyleproperty) |
| [**Dependencias**](#dependencies) | [DOM](dom.md) |
## Métodos

### habilitar
Habilita el agente de CSS para la página dada. Los clientes no deben suponer que el agente CSS se ha habilitado hasta que se recibe el resultado de este comando.

</p>

---

### deshabilitar 
Deshabilita el agente de CSS para la página dada.

</p>

---

### getInlineStylesForNode
Devuelve los estilos definidos en línea (explícitamente en el atributo "style" y, de forma implícita, usando atributos DOM) para un nodo DOM identificado por `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devuelve</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Estilo en línea del nodo DOM especificado.</td>
        </tr>
        <tr>
            <td>attributesStyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Estilo de elemento definido por atributo (por ejemplo, Obtenido de "width = 20 height = 100%").</td>
        </tr>
    </tbody>
</table>
</p>

---

### getMatchedStylesForNode
Devuelve los estilos solicitados para un nodo DOM identificado por `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devuelve</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Estilo en línea del nodo DOM especificado.</td>
        </tr>
        <tr>
            <td>attributesStyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Estilo de elemento definido por atributo (por ejemplo, Obtenido de "width = 20 height = 100%").</td>
        </tr>
        <tr>
            <td>matchedCSSRules <br /> <i>opcional</i></td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Reglas CSS que coinciden con este nodo de todas las hojas de estilo vigentes.</td>
        </tr>
        <tr>
            <td>pseudoElements <br /> <i>opcional</i></td>
            <td><a href="#pseudoelementmatches"><code class="flyout">PseudoElementMatches[]</code></a></td>
            <td>Coincidencias de pseudo estilo para este nodo.</td>
        </tr>
        <tr>
            <td>heredan <br /> <i>opcional</i></td>
            <td><a href="#inheritedstyleentry"><code class="flyout">InheritedStyleEntry[]</code></a></td>
            <td>Una cadena de estilos heredados (desde el elemento primario del nodo inmediato hasta la raíz del árbol DOM).</td>
        </tr>
        <tr>
            <td>cssKeyframesRules <br /> <i>opcional</i></td>
            <td><a href="#csskeyframesrule"><code class="flyout">CSSKeyframesRule[]</code></a></td>
            <td>Una lista de animaciones con fotogramas clave CSS que coinciden con este nodo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getPlatformFontsForNode
Solicita información sobre las fuentes de la plataforma que usamos para representar el TextNodes secundario en el nodo dado.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devuelve</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>otras</td>
            <td><a href="#platformfontusage"><code class="flyout">PlatformFontUsage[]</code></a></td>
            <td>Estadísticas de uso para cada fuente de plataforma empleada.</td>
        </tr>
    </tbody>
</table>
</p>

---

### getComputedStyleForNode
Devuelve el estilo calculado de un nodo DOM identificado por `nodeId` .

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>nodeId</td>
            <td><a href="dom.md#nodeid"><code class="flyout">DOM.NodeId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
<table>
    <thead>
        <tr>
            <th>Devuelve</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>computedStyle</td>
            <td><a href="#csscomputedstyleproperty"><code class="flyout">CSSComputedStyleProperty[]</code></a></td>
            <td>Estilo calculado para el nodo DOM especificado.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Eventos

### styleSheetAdded
Se desencadena cuando se agrega una hoja de estilos de un documento activo.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>header</td>
            <td><a href="#cssstylesheetheader"><code class="flyout">CSSStyleSheetHeader</code></a></td>
            <td>Se ha agregado metainformación de hoja de estilos.</td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetChanged
Se desencadena cuando se cambia una hoja de estilos como resultado de la operación del cliente.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td></td>
        </tr>
    </tbody>
</table>
</p>

---

### styleSheetRemoved
Se desencadena cuando se quita una hoja de estilos de un documento activo.

<table>
    <thead>
        <tr>
            <th>Parameters</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificador de la hoja de estilos que se ha quitado.</td>
        </tr>
    </tbody>
</table>
</p>

---

## Tipos

### <a name="stylesheetid"></a> StyleSheetId `string`



</p>

---

### <a name="pseudoelementmatches"></a> PseudoElementMatches `object`

Colección de reglas CSS para un solo pseudonombre.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>pseudoType</td>
            <td><a href="dom.md#pseudotype"><code class="flyout">DOM.PseudoType</code></a></td>
            <td>Tipo de seudoelemento.</td>
        </tr>
        <tr>
            <td>Match</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Coincidencias de reglas CSS aplicables al pseudo estilo.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="inheritedstyleentry"></a> InheritedStyleEntry `object`

Colección de reglas CSS heredada del nodo antecesor.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>inlineStyle <br /> <i>opcional</i></td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>El estilo en línea del nodo antecesor, si lo hay, en la cadena de herencia de estilos.</td>
        </tr>
        <tr>
            <td>matchedCSSRules</td>
            <td><a href="#rulematch"><code class="flyout">RuleMatch[]</code></a></td>
            <td>Coincidencias de reglas CSS que coinciden con el nodo antecesor de la cadena de herencia de estilos.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="rulematch"></a> RuleMatch `object`

Coincidencia de datos para una regla CSS.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Filete</td>
            <td><a href="#cssrule"><code class="flyout">CSSRule</code></a></td>
            <td>Regla CSS en la coincidencia.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="value"></a> Valor `object`

Datos de un selector simple (delimitados por comas en una lista de selectores).

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>texto</td>
            <td><code class="flyout">string</code></td>
            <td>Texto del valor.</td>
        </tr>
        <tr>
            <td>rango <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Intervalo de valores en el recurso subyacente (si está disponible).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="selectorlist"></a> SelectorList `object`

Datos de la lista de selección.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>selectores</td>
            <td><a href="#value"><code class="flyout">Value[]</code></a></td>
            <td>Selectores de la lista.</td>
        </tr>
        <tr>
            <td>texto</td>
            <td><code class="flyout">string</code></td>
            <td>Texto del selector de reglas.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssrule"></a> CSSRule `object`

Representación de las reglas CSS.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>opcional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificador de hoja de estilos CSS (ausente para la hoja de estilos del agente de usuario y reglas de hoja de estilos especificadas por el usuario) esta regla proviene de.</td>
        </tr>
        <tr>
            <td>selectorList <br /> <i>opcional</i></td>
            <td><a href="#selectorlist"><code class="flyout">SelectorList</code></a></td>
            <td>Datos del selector de reglas.</td>
        </tr>
        <tr>
            <td>origen <br /> <i>opcional</i></td>
            <td><<!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Origen de la hoja de estilos principal.</td>
        </tr>
        <tr>
            <td>estilo</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Declaración de estilo asociada.</td>
        </tr>
        <tr>
            <td>medios <br /> <i>opcional</i></td>
            <td><a href="#cssmedia"><code class="flyout">CSSMedia[]</code></a></td>
            <td>Matriz de la lista de medios (para las reglas que implican consultas multimedia). La matriz enumera las consultas multimedia comenzando por la más interna, saliendo hacia afuera.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="sourcerange"></a> SourceRange `object`

Intervalo de texto dentro de un recurso. Los números se basan en cero.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">integer</code></td>
            <td>Línea de inicio del rango.</td>
        </tr>
        <tr>
            <td>Columnainicio</td>
            <td><code class="flyout">integer</code></td>
            <td>Columna de inicio del rango (incluido).</td>
        </tr>
        <tr>
            <td>Fin</td>
            <td><code class="flyout">integer</code></td>
            <td>Línea de finalización de rango</td>
        </tr>
        <tr>
            <td>Columnafin</td>
            <td><code class="flyout">integer</code></td>
            <td>Columna final del intervalo (exclusivo).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="shorthandentry"></a> ShorthandEntry `object`



<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre abreviado.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valor abreviado.</td>
        </tr>
        <tr>
            <td>interés <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la propiedad tiene una anotación "! Important" (implica `false` si no está presente).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstyle"></a> CSSStyle `object`

Representación de estilo CSS.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>opcional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificador de hoja de estilos CSS (ausente para la hoja de estilos del agente de usuario y reglas de hoja de estilos especificadas por el usuario) esta regla proviene de.</td>
        </tr>
        <tr>
            <td>cssProperties</td>
            <td><a href="#cssproperty"><code class="flyout">CSSProperty[]</code></a></td>
            <td>Propiedades de CSS en el estilo.</td>
        </tr>
        <tr>
            <td>shorthandEntries</td>
            <td><a href="#shorthandentry"><code class="flyout">ShorthandEntry[]</code></a></td>
            <td>Valores calculados para todas las abreviaturas que se encuentran en el estilo.</td>
        </tr>
        <tr>
            <td>cssText <br /> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Texto de declaración de estilo (si está disponible).</td>
        </tr>
        <tr>
            <td>rango <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Rango de declaración de estilo en la hoja de estilos envolvente (si está disponible).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssproperty"></a> CSSProperty `object`

Datos de declaración de propiedad de CSS.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de la propiedad.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valor de la propiedad.</td>
        </tr>
        <tr>
            <td>interés <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la propiedad tiene una anotación "! Important" (implica `false` si no está presente).</td>
        </tr>
        <tr>
            <td>implícita <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la propiedad es implícita (implica que está `false` ausente).</td>
        </tr>
        <tr>
            <td>texto <br /> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>El texto de propiedad completo según se especifica en el estilo.</td>
        </tr>
        <tr>
            <td>parsedOk <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si el explorador entiende la propiedad (indica si no `true` existe).</td>
        </tr>
        <tr>
            <td>habilitar <br /> <i>opcional</i></td>
            <td><code class="flyout">boolean</code></td>
            <td>Si la propiedad está deshabilitada por el usuario (presente solo para las propiedades basadas en origen).</td>
        </tr>
        <tr>
            <td>rango <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>Todo el rango de propiedades de la declaración de estilo envolvente (si está disponible).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssmedia"></a> CSSMedia `object`

Descriptor de regla multimedia de CSS.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>texto</td>
            <td><code class="flyout">string</code></td>
            <td>Texto de consulta multimedia.</td>
        </tr>
        <tr>
            <td>origen</td>
            <td><code class="flyout">string</code> <br /> <i>Valores permitidos: mediaRule, importRule, linkedSheet, inlineSheet</i></td>
            <td>Origen de la consulta multimedia: "mediaRule" si se especifica mediante una regla @media, "importRule" si se especifica mediante una regla @import, "linkedSheet" si se especifica mediante un atributo "multimedia" en la etiqueta de vínculo de una hoja de estilos vinculada, "inlineSheet" si se especifica mediante un atributo "multimedia" en la etiqueta STYLE de una hoja de estilos en línea.</td>
        </tr>
        <tr>
            <td>sourceURL <br /> <i>opcional</i></td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL del documento que contiene la descripción de la consulta multimedia.</td>
        </tr>
        <tr>
            <td>rango <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>El intervalo de encabezado de la regla asociada (@media o @import) en la hoja de estilos envolvente (si está disponible).</td>
        </tr>
        <tr>
            <td>styleSheetId <br /> <i>opcional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificador de la hoja de estilos que contiene este objeto (si existe).</td>
        </tr>
        <tr>
            <td>mediaL <br /> <i>opcional</i></td>
            <td><a href="#mediaquery"><code class="flyout">MediaQuery[]</code></a></td>
            <td>Matriz de consultas de medios.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaquery"></a> MediaQuery `object`

Descriptor de consulta multimedia.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>manifestación</td>
            <td><a href="#mediaqueryexpression"><code class="flyout">MediaQueryExpression[]</code></a></td>
            <td>Matriz de expresiones de consulta multimedia.</td>
        </tr>
        <tr>
            <td>activa</td>
            <td><code class="flyout">boolean</code></td>
            <td>Si se cumple la condición de la consulta multimedia.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="mediaqueryexpression"></a> MediaQueryExpression `object`

Descriptor de expresión de consulta multimedia.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>value</td>
            <td><code class="flyout">number</code></td>
            <td>Valor de la expresión de consulta multimedia.</td>
        </tr>
        <tr>
            <td>Departamento</td>
            <td><code class="flyout">string</code></td>
            <td>Unidades de expresión de consulta multimedia.</td>
        </tr>
        <tr>
            <td>característica</td>
            <td><code class="flyout">string</code></td>
            <td>Característica de expresión de consulta multimedia.</td>
        </tr>
        <tr>
            <td>valueRange <br /> <i>opcional</i></td>
            <td><a href="#sourcerange"><code class="flyout">SourceRange</code></a></td>
            <td>El intervalo asociado del texto del valor de la hoja de estilos envolvente (si está disponible).</td>
        </tr>
        <tr>
            <td>computedLength <br /> <i>opcional</i></td>
            <td><code class="flyout">number</code></td>
            <td>Longitud calculada de la expresión de consulta multimedia (si corresponde).</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="platformfontusage"></a> PlatformFontUsage `object`

Información sobre la cantidad de glifos representados con la fuente dada.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>familyName</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de familia de la fuente informado por la plataforma.</td>
        </tr>
        <tr>
            <td>isCustomFont</td>
            <td><code class="flyout">boolean</code></td>
            <td>Indica si la fuente se ha descargado o resuelto localmente.</td>
        </tr>
        <tr>
            <td>glyphCount</td>
            <td><code class="flyout">number</code></td>
            <td>Cantidad de glifos representados con esta fuente.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframesrule"></a> CSSKeyframesRule `object`

Representación de regla de fotogramas clave CSS.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>animationName</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Nombre de la animación.</td>
        </tr>
        <tr>
            <td>fotogramas clave</td>
            <td><a href="#csskeyframerule"><code class="flyout">CSSKeyframeRule[]</code></a></td>
            <td>Lista de fotogramas clave.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csskeyframerule"></a> CSSKeyframeRule `object`

Representación de la regla de fotograma clave CSS.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId <br /> <i>opcional</i></td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificador de hoja de estilos CSS (ausente para la hoja de estilos del agente de usuario y reglas de hoja de estilos especificadas por el usuario) esta regla proviene de.</td>
        </tr>
        <tr>
            <td>origen</td>
            <td><!--  <a href="#stylesheetorigin">  --><code class="flyout">StyleSheetOrigin</code><!--  </a>  --></td>
            <td>Origen de la hoja de estilos principal.</td>
        </tr>
        <tr>
            <td>keyText</td>
            <td><a href="#value"><code class="flyout">Value</code></a></td>
            <td>Texto de clave asociada.</td>
        </tr>
        <tr>
            <td>estilo</td>
            <td><a href="#cssstyle"><code class="flyout">CSSStyle</code></a></td>
            <td>Declaración de estilo asociada.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="csscomputedstyleproperty"></a> CSSComputedStyleProperty `object`



<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>name</td>
            <td><code class="flyout">string</code></td>
            <td>Nombre de propiedad de estilo calculado.</td>
        </tr>
        <tr>
            <td>value</td>
            <td><code class="flyout">string</code></td>
            <td>Valor de propiedad de estilo calculado.</td>
        </tr>
    </tbody>
</table>
</p>

---

### <a name="cssstylesheetheader"></a> CSSStyleSheetHeader `object`

Metainformación CSS de hoja de estilos.

<table>
    <thead>
        <tr>
            <th>Propiedades</th>
            <th></th>
            <th></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>styleSheetId</td>
            <td><a href="#stylesheetid"><code class="flyout">StyleSheetId</code></a></td>
            <td>Identificador de la hoja de estilos.</td>
        </tr>
        <tr>
            <td>sourceURL</td>
            <td><code class="flyout">string</code></td>
            <td>Dirección URL de recurso de hoja de estilos.</td>
        </tr>
        <tr>
            <td>habilitar</td>
            <td><code class="flyout">boolean</code></td>
            <td>Indica si la hoja de estilos está deshabilitada.</td>
        </tr>
        <tr>
            <td>isInline</td>
            <td><code class="flyout">boolean</code></td>
            <td>Si se crea esta hoja de estilos para la etiqueta de estilo mediante Parser. Esta marca no está configurada para las etiquetas de estilo document. escrito.</td>
        </tr>
        <tr>
            <td>startLine</td>
            <td><code class="flyout">number</code></td>
            <td>Desplazamiento de línea de la hoja de estilos en el recurso (basado en cero).</td>
        </tr>
        <tr>
            <td>Columnainicio</td>
            <td><code class="flyout">number</code></td>
            <td>Desplazamiento de columna de la hoja de estilos dentro del recurso (basado en cero).</td>
        </tr>
        <tr>
            <td>longitud</td>
            <td><code class="flyout">number</code></td>
            <td>Tamaño del contenido (en caracteres).</td>
        </tr>
    </tbody>
</table>
</p>

---

## Dependencias

[DOM](dom.md)

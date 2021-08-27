---
description: Copie las declaraciones de una regla de estilo de una manera que esté formatada para JavaScript y lista para pegar en un archivo JavaScript.  Edite las reglas de estilo definidas inicialmente por una función CSSOM.
title: Edición de estilos para marcos CSS-in-JS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, css, css-in-js
ms.openlocfilehash: 036228bde8e8f4c8ba714fe127ed92f3e0e3ebea
ms.sourcegitcommit: d6ecc4ab48c7e0e048fd8248f6379222642e9d41
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "11925583"
---
<!-- Copyright Alex Rudenko

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->
# <a name="style-editing-for-css-in-js-frameworks"></a>Edición de estilos para marcos CSS-in-JS


<!-- ====================================================================== -->
## <a name="copying-style-rule-declarations-to-paste-them-with-javascript-syntax"></a>Copiar declaraciones de regla de estilo para pegarlas con sintaxis de JavaScript

Desde el **panel Estilos,** puede copiar declaraciones de una regla de estilo de una forma que esté formatada para JavaScript y lista para pegar en un archivo JavaScript.

Al usar bibliotecas CSS-in-JS, puede copiar declaraciones CSS (una propiedad CSS y un valor) para que se les formatee automáticamente para JavaScript.  No tiene que editar manualmente el CSS copiado para que coincida con la sintaxis de JavaScript.  Puede copiar una sola declaración CSS o todas las declaraciones de una regla de estilo y, a continuación, pegarlas directamente en un archivo JavaScript sin tener problemas de sintaxis.

Para copiar una regla de estilo como JavaScript:

1. En el **panel Estilos** de la **herramienta Elementos,** abra el menú contextual \(hacer clic con el botón secundario\) en una declaración de una regla de estilo.

1. Seleccione **Copiar declaración como JS** o Copiar todas las **declaraciones como JS**.

1. Pegue el CSS copiado en un archivo JavaScript en el editor de texto, como Visual Studio Code.  Por ejemplo: `'--more-link': 'lime'`.

:::image type="complex" source="images/copy-declaration-as-js.msft.png" alt-text="Menú contextual para una regla de estilo, incluidos los comandos Copiar declaración como JS y Copiar todas las declaraciones como JS." lightbox="images/copy-declaration-as-js.msft.png":::
   Menú contextual de una regla de estilo, incluida **la declaración Copiar como JS** y Copiar todas las **declaraciones como comandos JS**
:::image-end:::

Esta característica está disponible a partir Microsoft Edge versión 93. <!-- delete statement sometime after September 2, 2021 --> Para obtener más información sobre cómo ver y cambiar CSS, vaya a [Referencia css][CssReference].


<!-- ====================================================================== -->
## <a name="editing-style-rules-that-were-initially-defined-by-a-cssom-function"></a>Editar reglas de estilo definidas inicialmente por una función CSSOM

<!-- from https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#style-editing-for-css-in-js-frameworks -->

El **panel Estilos** admite los estilos de edición creados con las API del modelo de objetos CSS [(CSSOM).][CsswgDraftsCssom]  Muchos marcos y bibliotecas de CSS en JS usan las API del modelo de objetos CSS bajo el capó para crear estilos.

Puede editar los estilos agregados en JavaScript con hojas de estilos [constructables][WicgConstructStylesheet].  Las hojas de estilos constructables son una forma de crear y distribuir estilos reutilizables al usar [Shadow DOM][MdnShadowDom].

### <a name="example"></a>Por ejemplo:

En este código de ejemplo, las reglas de estilo se definen inicialmente llamando a una función de modelo de objetos CSS (CSSOM) y, a continuación, las reglas de estilo se modifican mediante el **panel Estilos.**  El `CSSStyleSheet` objeto contiene las API cssom, como `insertRule()` .  Los `h1` estilos que se agregaron inicialmente por una función se pueden editar en el panel `CSSStyleSheet` **Estilos.**

```javascript
//Add CSS-in-JS button

function addStyle() {
  const sheet = new CSSStyleSheet();
  sheet.insertRule(`h1 {
    background: pink;
    text-transform: uppercase;
  }`);
  document.adoptedStyleSheets = [sheet];
}
```

En este ejemplo se muestra cómo cambiar la propiedad de los estilos agregados `background` por la función modelo de objetos CSS `h1` `insertRule()` .  El color se establece inicialmente llamando a una función modelo de objetos CSS y, a continuación, se puede cambiar de a `background` `pink` mediante el panel `lightblue` **Estilos.**

:::image type="complex" source="../media/css-in-js.msft.png" alt-text="Cambiar la propiedad de fondo de los estilos h1 agregados con CSSStyleSheet de rosa a azul claro" lightbox="../media/css-in-js.msft.png":::
   Cambiar la `background` propiedad de los estilos `h1` agregados con de a `CSSStyleSheet` `pink` `lightblue` .
:::image-end:::

Pruebe esta característica con un [ejemplo que use CSS-in-JS][CodepenZoherghadyaliAbdgrpz].


<!-- ====================================================================== -->
## <a name="what-is-css-in-js"></a>¿Qué es CSS-in-JS?

Esta sección es un extracto de la entrada de blog [css-in-JS support in DevTools][BlogCssInJsInDevTools].

Esto es lo que queremos decir con _CSS-in-JS_y cómo es diferente de CSS normal.  La definición de _CSS-in-JS_ es algo imprecisa.  En un sentido amplio, es un enfoque para administrar código CSS con JavaScript.  Por ejemplo, podría significar que el contenido CSS se define con JavaScript y la aplicación genera el resultado css final sobre la marcha.

En el contexto de DevTools, _CSS-in-JS_ significa que el contenido CSS se inserta en la página mediante las API del modelo de objetos CSS.  Css normal se inserta mediante o elementos, y tiene un origen estático (como un nodo `<style>` DOM o un recurso de `<link>` red).  En cambio, CSS-in-JS a menudo no tiene un origen estático.  Un caso especial aquí es que el contenido de un elemento se puede actualizar mediante la API del modelo de objetos CSS, lo que hace que el origen no esté sincronizado con la hoja de estilos `<style>` CSS real.

Si usa cualquier biblioteca CSS-in-JS (como styled-component, Emotion o JSS), es posible que la biblioteca inyecte estilos con LAS API del modelo de objetos CSS bajo el capó, según el modo de desarrollo y el explorador.

Veamos algunos ejemplos de cómo insertar una hoja de estilos mediante la API del modelo de objetos CSS, similar al método usado por algunas bibliotecas CSS-in-JS.

```javascript
// Insert new rule to an existing CSS stylesheet
const element = document.querySelector('style');
const stylesheet = element.sheet;
stylesheet.replaceSync('.some { color: blue; }');
stylesheet.insertRule('.some { color: green; }');
```

También puede crear una hoja de estilos completamente nueva:

```javascript
// Create a completely new stylesheet
const sheet = new CSSStyleSheet();
stylesheet.replaceSync('.some { color: blue; }');
stylesheet.insertRule('.some { color: green; }');
```

```javascript
// Apply constructed stylesheet to the document
document.adoptedStyleSheets = [...document.adoptedStyleSheets, sheet];
```

### <a name="css-support-in-devtools"></a>Compatibilidad con CSS en DevTools

En DevTools, la característica más usada al tratar con CSS es el **panel Estilos.**  En el **panel Estilos,** puede ver lo que las reglas CSS-in-JS se aplican a un elemento determinado.  También puede editar las reglas CSS-in-JS y ver los cambios en la página en tiempo real.

El **panel Estilos** admite reglas CSS que puede modificar mediante las API del modelo de objetos CSS.  Los estilos CSS-in-JS a veces se describen como creados _,_ para indicar que estos estilos se crearon mediante API web.

<!-- video https://storage.googleapis.com/chrome-gcs-uploader.appspot.com/video/dPDCek3EhZgLQPGtEG3y0fTn4v82/Jy8q9gPbQknRturLyCsq.mp4 -->


<!-- ====================================================================== -->
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].
> La página original se encuentra [aquí](https://developer.chrome.com/blog/css-in-js/) y está redactada por [Alex Rudenko][AlexRudenko] \(Technical Writer, Chrome DevTools \& Lighthouse\).

[ ![ Creative Commons License][CCby4Image]][CCA4IL] Este trabajo se concede bajo una licencia de Creative Commons [Attribution 4.0 International License][CCA4IL].


<!-- ====================================================================== -->
<!-- links -->
[CssReference]: reference.md "Referencia CSS | Microsoft Docs"
<!-- external links -->
[BlogCssInJsInDevTools]: https://developers.google.com/web/updates/2021/02/css-in-js "Compatibilidad con CSS-in-JS en DevTools | Google Blog "
[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de objetos CSS (CSSOM) | Borradores del editor de grupo de trabajo CSS de W3C"
[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos de hoja de estilos | Web Incubator CG"
[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Uso de dom de sombra | MDN"
[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edición de estilos para marcos CSS-in-JS | CodePen"

[CCA4IL]: https://creativecommons.org/licenses/by/4.0
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
[AlexRudenko]: https://developers.google.com/web/resources/contributors#alex-rudenko

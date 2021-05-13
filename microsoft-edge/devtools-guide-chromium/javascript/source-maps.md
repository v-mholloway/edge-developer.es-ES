---
description: Mantenga el código del lado cliente legible y depurable incluso después de combinarlo, minificarlo o compilarlo.
title: Asignar código preprocesado al código fuente
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 3240e437a917dd7074a0584b91dcc6c34576ca24
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564052"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="map-preprocessed-code-to-source-code"></a>Asignar código preprocesado al código fuente  

Mantenga el código del lado cliente legible y depurable incluso después de combinarlo, minificarlo o compilarlo.  Use mapas de origen para asignar el código fuente al código compilado.  

### <a name="summary"></a>Resumen  

*   Use source Mapas para asignar código minificado al código fuente.  A continuación, puede leer y depurar código compilado en el origen original.  
*   Solo use procesadores previos que puedan producir datos de origen Mapas.  
*   Compruebe que el servidor web es capaz de servir a source Mapas.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <a name="get-started-with-preprocessors"></a>Introducción a los preprocesadores  

En este artículo se explica cómo interactuar con los orígenes de JavaScript Mapas en la herramienta Orígenes de DevTools.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; navigate to Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <a name="use-a-supported-preprocessor"></a>Usar un preprocesador compatible  

Use un rectificador que sea capaz de crear mapas de origen.  <!--For the most popular options, navigate to preprocessor support section.  -->  Para obtener una vista extendida, vaya [a Mapas de origen: idiomas, herramientas y otra página][GitHubWikiSourceMapsLanguagesTools] wiki de información.  

<!--todo: add link to display the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Los siguientes tipos de preprocesadores se usan comúnmente en combinación con source Mapas:  

*   Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compiladores \([Compilador de cierre][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dardo][DartMain]\)  
*   Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)  
    
## <a name="source-maps-in-devtools-sources-tool"></a>Source Mapas in DevTools Sources tool  

Los Mapas origen de los preprocesadores hacen que DevTools cargue los archivos originales además de los minificados.  A continuación, use los originales para establecer puntos de interrupción y pasar por el código.  Mientras tanto, Microsoft Edge está ejecutando el código minificado.  La ejecución del código le ofrece la ilusión de ejecutar un sitio de desarrollo en producción.  

Al ejecutar source Mapas en DevTools, debe observar que JavaScript no está compilado y que se muestran todos los archivos JavaScript individuales a los que hace referencia.  El Mapas de devTools usa la asignación de origen, pero la funcionalidad subyacente ejecuta realmente el código compilado.  Los errores, registros y puntos de interrupción se asignan al código de desarrollo para una depuración increíble.  Por lo tanto, en efecto, te da la ilusión de que estás ejecutando un sitio de desarrollo en producción.  

### <a name="enable-source-maps-in-settings"></a>Habilitar el Mapas de origen en la configuración  

Los Mapas de origen están habilitados de forma predeterminada<!-- \(as of Microsoft Edge 39\)-->, pero si desea comprobarlos o habilitarlos; primero abra DevTools, elija **Personalizar y controlar DevTools** \( `...` \) > **Configuración**.  En el **panel Preferencias,** en **Orígenes**, active Habilitar origen **de JavaScript Mapas**.  También puede activar la opción Habilitar origen **CSS Mapas**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Habilitar origen Mapas" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **Habilitar código fuente de JavaScript Mapas**  
:::image-end:::  

### <a name="debugging-with-source-maps"></a>Depuración con origen Mapas  

Al depurar el código y el código Mapas habilitados, el Mapas muestra en dos lugares:  

1.  En la consola \(el vínculo al origen debe ser el archivo original, no el generado\)  
1.  Al pasar por el código \(los vínculos de la pila de llamadas deben abrir el archivo de origen original\)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <a name="sourceurl-and-displayname"></a>@sourceURL y displayName  

Aunque no forma parte de la especificación de mapa de origen, permite facilitar el desarrollo al `@sourceURL` trabajar con evales.  La aplicación auxiliar se muestra de forma similar a la `//# sourceMappingURL` propiedad y se menciona en las especificaciones de Source Map V3.  

Al incluir el siguiente comentario especial en el código, que se evita, puede nombrar evales y scripts en línea y estilos para que cada uno aparezca como nombres más lógicos en sus DevTools.  

```javascript
//# sourceURL=source.coffee
```  

Vaya a la página siguiente.  

*   [demo][CssNinjaDemoSourceMapping]

Complete las siguientes acciones.  

1.  Abra DevTools y vaya a la **herramienta Orígenes.**  
1.  Escriba un nombre de archivo en el **campo Nombre del código:** entrada.  
1.  Elija el **botón compilar.**  
1.  Aparece una alerta que muestra la suma evaluada del origen de CoffeeScript.  
    
Si expande el sub panel **Orígenes,** ahora mostrará un nuevo archivo con el nombre de archivo personalizado que escribió anteriormente.  Si hace doble clic para ver este archivo, contiene el JavaScript compilado para el origen original.  Sin embargo, en la última línea hay un `// @sourceURL` comentario que indica el archivo de origen original.  Esto puede ayudarle con la depuración mientras trabaja con abstracciones de idioma.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Trabajar con sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Trabajar con `sourceURL`  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel es un compilador de JavaScript"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Un ejemplo sencillo de nomenclatura eval //# sourceURL"  

[DartMain]: https://www.dartlang.org "Lenguaje de programación de Dardo"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "google/closure-compiler | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Mapas de origen: idiomas, herramientas y otra información | GitHub wiki"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Introducción: google/traceur-compiler | GitHub wiki"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original [](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) se encuentra aquí y está redactada por [Meggin Kearney][MegginKearney] \(Tech Writer\) y [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  

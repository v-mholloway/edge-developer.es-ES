---
title: Asignar código preprocesado al código fuente
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c791a4af4446a1209d6db77ca4787fee80d45e5c
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981780"
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





# Asignar código preprocesado a código fuente   




Mantenga el código de cliente legible y depurable incluso después de combinarlo, minifylo o compilarlo.  Use mapas de origen para asignar el código fuente al código compilado.  

### Resumen  

*   Use mapas de origen para asignar código de minified al código fuente. Después, podrá leer y depurar el código compilado en el origen original.  
*   Usa previamente procesadores que puedan generar mapas de origen.  
*   Compruebe que el servidor web puede atender mapas de origen.  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## Introducción a los preprocesadores  

En este artículo se explica cómo interactuar con mapas de origen de JavaScript en el panel de orígenes de DevTools.  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## Usar un preprocesador admitido  

Debe usar un minifier que sea capaz de crear mapas de origen.  <!--For the most popular options, see the preprocessor support section.  -->  Para obtener una vista extendida, consulte la página de [mapas de origen: idiomas, herramientas y otra información][GitHubWikiSourceMapsLanguagesTools] .  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

Los siguientes tipos de preprocesadores se suelen usar en combinación con mapas de origen:  

*   Transpiladores \ ([Babel][BabelJS], [traceur][GitHubWikiGoogleTraceurCompiler]\)  
*   Compiladores \ ([compilador de cierre][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)  
*   Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)  
    
## Mapas de origen en el panel de orígenes de DevTools  

Los mapas de origen de los preprocesadores hacen que DevTools cargue los archivos originales además de sus minified.  A continuación, puede usar los originales para establecer puntos de interrupción y recorrer el código.  Mientras tanto, Microsoft Edge ejecuta el código de minified. Esto le ofrece la ilusión de ejecutar un sitio de desarrollo en producción.  

Al ejecutar mapas de origen en DevTools, debes tener en cuenta que el código JavaScript no está compilado y que puedes ver todos los archivos JavaScript individuales a los que hace referencia.  Este es el uso de la asignación de origen, pero, en realidad, ejecuta el código compilado en segundo plano.  Los errores, registros y puntos de interrupción se asignan al código de desarrollo para la depuración formidable.  Por ello, le da la sensación de que está ejecutando un sitio de desarrollo en producción.  

### Habilitar mapas de origen en la configuración  

Los mapas de origen están habilitados de forma predeterminada <!--\(as of Microsoft Edge 39\)-->, pero si deseas volver a activarlos o habilitarlos; en primer lugar, abre DevTools, haz clic en el botón **personalizar DevTools** \ ( `...` \) y selecciona **configuración**.  En el panel **preferencias** , en **fuentes**, active la casilla **Habilitar mapas de origen de JavaScript**.  También puede **Activar habilitar mapas de origen CSS**.  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Habilitar mapas de origen" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   Habilitar mapas de origen  
:::image-end:::  

### Depurar con mapas de origen  

Al depurar el código y los mapas de origen habilitados, los mapas de origen se muestran en dos lugares:  

1.  En la consola \ (el vínculo al origen debe ser el archivo original, no el generado \)  
1.  Al repasar por el código \ (los vínculos en la pila de llamadas deben abrir el archivo de origen original \)  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/debug/breakpoints/step-code ""  -->  

## @sourceURL y displayName  

Aunque no forme parte de la especificación del mapa de origen, el `@sourceURL` le permite hacer un desarrollo mucho más fácil cuando se trabaja con evaluaciones.  Este ayudante es muy similar a la `//# sourceMappingURL` propiedad y se menciona realmente en las especificaciones del mapa de origen V3.  

Al incluir el siguiente comentario especial en el código, que se evaluación, podrás nombrar las evaluaciones y los estilos y los scripts en línea, de modo que cada uno aparezca como más nombres lógicos en tu DevTools.  

```javascript
//# sourceURL=source.coffee
```  

Vaya a la página siguiente.  

*   [demo][CssNinjaDemoSourceMapping]
    
Siga estos pasos.  

1.  Abra el DevTools y vaya al panel **fuentes** .  
1.  Escribe un nombre de archivo en el campo **nombre de tu código:** entrada.  
1.  Haga clic en el botón **compilar** .  
1.  Aparece una alerta con la suma evaluada del origen de CoffeeScript.  
    
Si expande el subpanel **orígenes** , ahora verá un nuevo archivo con el nombre de archivo personalizado que escribió anteriormente.  Si hace doble clic para ver este archivo, contiene el JavaScript compilado para el origen original.  En la última línea, sin embargo, es un `// @sourceURL` comentario que indica el archivo de origen original.  Esto puede ayudarle a realizar la depuración mientras trabaja con abstracciones de lenguaje.  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Trabajar con sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   Trabajar con sourceURL  
:::image-end:::  

<!--  
## Feedback   


-->  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel es un compilador de JavaScript"  
[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  
[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Un ejemplo sencillo de nombre de evaluación de//# sourceURL"  
[DartMain]: https://www.dartlang.org "Lenguaje de programación DART"  
[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/cierre-compilador | GitHub"  
[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  
[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Mapas de origen: idiomas, herramientas y otra información | Wiki de GitHub"  
[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Introducción-Google/traceur-Compiler | Wiki de GitHub"  
[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Paul Bakaus][PaulBakaus] \ (Open Web Developer defensor, Google: Tools, performance, Animation y UX \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  

---
title: Novedades de DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6de8f7b11edb476f2656dd6f16e02413b1873ed8
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684716"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  







# Novedades de DevTools (Microsoft Edge 81)   



## Anuncios del equipo de Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge. Compruébelos para probar las nuevas características de la DevTools, las extensiones de código de VS y mucho más.  Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].  

### Mejoras de accesibilidad para el DevTools  

El equipo de DevTools ha contribuido a 170 cambios en cromo para solucionar problemas de alto impacto en el contraste de color, el teclado y el lector de pantalla en el DevTools.  Cada desarrollador que crea la web debe poder usar el DevTools.  

> ##### Figura 1  
> La herramienta de rendimiento en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla  
> ![La herramienta de rendimiento en el DevTools con la navegación con el teclado y las mejoras del lector de pantalla][ImagePerformanceToolKeyboardReaderImprovements]  

¿Desea saber cómo hacer que su página web sea accesible para todos los usuarios?  Descargue [Insight Insights][AccessibilityInsights] y extensiones [Webhint][WebhintBrowserExtension] para Microsoft Edge para comenzar.  

Si usa lectores de pantalla o el teclado para desplazarse por la DevTools, envíenos sus comentarios con un [Tweet][PostTweetEdgeDevTools] o haga clic en el icono de [comentarios](#feedback) .  

[#963183][crbug963183] de problemas de cromo  

### Usar el DevTools en otros idiomas  

Muchos programadores usan otras herramientas de desarrollo, como StackOverflow y VS Code, en su idioma nativo, no solo en inglés.  Nos complace anunciar la localización de la DevTools, que ahora puedes usar en uno de los 10 idiomas además del inglés:  

:::row:::
   :::column span="":::
      Chino \ (simplificado \)- &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;
   :::column-end:::
   :::column span="":::
      Chino (tradicional \)- &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Francés: Francisco&#231;AIS
   :::column-end:::
   :::column span="":::
      Alemán-Deutsch
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Italiano-Italiano
   :::column-end:::
   :::column span="":::
       &#26085;&#26412;&#35486; japonés
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Coreano:  &#54620;&#44397;&#50612;
   :::column-end:::
   :::column span="":::
      Portugués-Portugu&#234;s
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      Ruso:  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;
   :::column-end:::
   :::column span="":::
      Español-Espa&#241;ol
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

El DevTools coincide automáticamente con el idioma que usas para Microsoft Edge en `edge://settings/languages` .  

Si desea que Microsoft Edge esté en un idioma y que su DevTools permanezca en inglés, presione `F1` la DevTools para abrir la [configuración][Settings] y deshabilitar el **idioma del explorador**.  

> ##### Figura 2  
> El DevTools en alemán  
> ![El DevTools en alemán][ImageLocalizedGerman]  

Los mensajes de **consola** no se localizan.  Solo las cadenas usadas en la interfaz de usuario de DevTools se muestran en el idioma que usas para Microsoft Edge.  

Si desea usar la DevTools en un idioma diferente al de los que están disponibles, [Tweet][PostTweetEdgeDevTools] o haga clic en el icono de [comentarios](#feedback) .  

[#941561][crbug941561] de problemas de cromo  

### extensión webhint de Microsoft Edge  

La extensión webhint de Microsoft Edge te permite examinar fácilmente tu página web y obtener comentarios sobre la accesibilidad, la compatibilidad de explorador, la seguridad, el rendimiento y mucho más dentro de la DevTools.  Para obtener más información, consulte [https://webhint.io][Webhint] .  

> ##### Imagen 3  
> La pestaña sugerencias de la DevTools cuando está instalada la extensión de explorador webhint  
> ![La pestaña sugerencias de la DevTools cuando está instalada la extensión de explorador webhint][ImageHintsTabWebhintExtension]  

[Prueba la extensión de explorador webhint en Microsoft Edge][MicrosoftEdgeInsiderAddons].  Una vez que haya instalado la extensión, abra el DevTools y seleccione la pestaña sugerencias.  Desde aquí, ejecute un examen de sitios personalizable.  Visita [webhint.IO][WebhintBrowserExtension] para obtener más información.  

### Vista 3D  

Use la **vista 3D** para depurar la aplicación web desplazándose por el [modelo de objeto de documento \ (Dom \)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z][MDNZIndex] .  

> ##### Imagen 4  
> Vista 3D en el DevTools  
> ![Vista 3D en el DevTools][Image3DView]  

Para acceder a la vista 3D, pulse `Ctrl`  +  `Shift`  +  `P` , escriba en la **vista 3D** y seleccione **Mostrar vista en 3D**.  

Trabajamos en la interfaz de usuario y agregamos más funcionalidad a la vista 3D; por lo tanto, envíanos tus [comentarios](#feedback).  

[#987787][crbug987787] de problemas de cromo  

### Extensiones de código de Visual Studio  

El equipo de DevTools también ha publicado algunas extensiones para [Visual Studio Code \ (vs Code \)][VisualStudioCode] que te permiten usar la potencia de DevTools directamente desde tu editor de texto. Consulta las siguientes extensiones:  

#### Elementos de Microsoft Edge  

Use la herramienta elementos de VS Code agregando los [elementos de la extensión de código de Microsoft Edge \ (cromo \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] .  

> ##### Imagen 5  
> La herramienta elementos en VS Code uso de los elementos de la extensión de Microsoft Edge ![ la herramienta elementos en vs Code usando los elementos de la extensión de Microsoft Edge][ImageElementsVisualStudioCode]  

Para obtener más información, consulta [los elementos de la extensión de código de Microsoft Edge vs][VisualStudioCodeElementEdgeExtension].  

#### Depurador para Microsoft Edge  

Con el [depurador para la extensión de código de Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] vs, depure JavaScript que se ejecuta en Microsoft Edge directamente desde el código de vs.  

> ##### Imagen 6  
> El depurador para la extensión de Microsoft Edge en VS Code  
> ![El depurador para la extensión de Microsoft Edge en VS Code][ImageDebuggerExtensionVisualStudioCode]  

Para obtener más información, consulte [Cómo depurar Microsoft Edge desde vs Code][VisualStudioCodeDebuggerEdgeExtension].  

#### sugerencia  

La extensión de código [webhint][VisualStudioMarketplaceWebhintExtension] de vs usa `webhint` para mejorar la página web mientras la escribes. Esta extensión ejecuta y notifica diagnósticos en los archivos de área de trabajo según el `webhint` análisis.  

> ##### Imagen 7  
> La extensión de código de webhint VS analizando un archivo. TSX en VS Code  
> ![La extensión de código de webhint VS analizando un archivo. TSX en VS Code][ImageWebhintVisualStudioCodeExtensionWorkspace]  

[Más información sobre la extensión webhint de vs Code][WebhintVisualStudioCodeExtension].  

### Integración con Visual Studio  

En Visual Studio 2019 versión 16,2 o posterior, usa el depurador de Visual Studio para depurar JavaScript que se ejecuta en Microsoft Edge.  [Descarga Visual Studio 2019][MicrosoftVisualStudioDownloads] para probar esta característica.  

> ##### Imagen 8  
> Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta  
> ![Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta][ImageVisualStudioLaunchWebApp]  

[Obtenga más información sobre la depuración de Microsoft Edge desde Visual Studio][MicrosoftVisualStudio].  

### Mensajes de la consola de prevención de seguimiento  

La prevención de seguimiento es una característica exclusiva de Microsoft Edge que le protege de ser rastreada por los sitios web que no ha visitado antes.  La configuración predeterminada de prevención de rastreo es el modo equilibrado, que bloquea los rastreadores de terceros y los rastreadores maliciosos conocidos para obtener una experiencia que equilibre la compatibilidad de la privacidad y la Web.  Para obtener más información sobre la compatibilidad de su página web cuando se bloquean determinados rastreadores, también hemos añadido mensajes de advertencia en la consola cuando se bloquea un rastreador.  

> ##### Imagen 9  
> Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador  
> ![Mensajes en la consola cuando el seguimiento de prevención bloquea el acceso al almacenamiento de un rastreador][ImageTrackingPrevention]  

[Obtenga más información acerca de la prevención de seguimiento y el equilibrio entre privacidad y compatibilidad web][TrackingPrevention].



## Anuncios del proyecto de cromo  

En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 81 que se han contribuido al proyecto de código abierto.  

### Compatibilidad de moto G4 en el modo de dispositivo 

Después de [Habilitar la barra de herramientas del dispositivo][DeviceToolbar], simule las dimensiones de una ventanilla de moto G4 en la lista de **dispositivos** .  

> ##### Imagen 10  
> Simulación de una ventanilla de moto G4  
> ![Simulación de una ventanilla de moto G4][ImageMotoG4]  

Haga clic en [Mostrar marco del dispositivo][DeviceFrame] para mostrar el hardware de moto G4 en la ventanilla.  

> ##### Imagen 11  
> Mostrar el hardware de moto G4  
> ![Mostrar el hardware de moto G4][ImageMotoG4Frame]  

Características relacionadas:  

*   Abra el [menú de comandos][CommandMenu] y ejecute el `Capture screenshot` comando para tomar una captura de pantalla de la ventanilla que incluye el hardware moto G4 (después de habilitar **Mostrar marco de dispositivo**).  
*   [Limite la red y la CPU][ThrottleNetworkAndCpu] para simular de forma más precisa las condiciones de navegación web de un usuario móvil.  

[#924693][crbug924693] de problemas de cromo  

### Actualizaciones relacionadas con cookies   

#### Cookies bloqueados en el panel cookies   

El panel cookies en el panel de la aplicación ahora muestra las cookies bloqueadas con un fondo amarillo.  

> ##### Imagen 12  
> Cookies bloqueados en el panel de cookies del panel de aplicaciones  
> ![Cookies bloqueados en el panel de cookies del panel de aplicaciones][ImageBlockedCookies]  

[#1030258][crbug|::ref1::|] de problemas de cromo  

#### Prioridad de la cookie en el panel de cookies   

Las tablas de cookies de los paneles red y aplicación ahora incluyen una columna de **prioridad** .  

> [!CAUTION]
> Los exploradores basados en cromo, como Microsoft Edge, son los únicos exploradores que admiten la prioridad de las cookies.  

[#1026879][crbug1026879] de problemas de cromo  

#### Editar todos los valores de cookies   

Ahora todas las celdas de las tablas de cookies se pueden editar, excepto las celdas de la columna **tamaño** , porque esa columna representa el tamaño de red de la cookie, en bytes.  Vea [los campos][CookiesFields] para obtener una explicación de cada columna.  

> ##### Imagen 13  
> Editar un valor de cookie  
> ![Editar un valor de cookie][ImageEditCookie]  

#### Copiar como la búsqueda de node. js para incluir datos de cookies   

Haga clic con el botón derecho en una solicitud de red y seleccione **copiar**  >  **copia como nodo. js fetch** para obtener una `fetch` expresión que incluya datos de cookies.  

> ##### Imagen 14  
> Copiar como fetch de node. js  
> ![Copiar como fetch de node. js][ImageCopyFetch]  

[#1029826][crbug1029826] de problemas de cromo  

### Iconos más exactos del manifiesto de la aplicación Web   

Anteriormente, el panel manifiesto del panel de aplicaciones enviaba sus propias solicitudes para mostrar los iconos del manifiesto de la aplicación Web.  DevTools ahora muestra el mismo icono de manifiesto que usa Microsoft Edge.  

> ##### Imagen 15  
> Iconos en el panel manifiesto  
> ![Iconos en el panel manifiesto][ImageManifestIcon]   

[#985402][crbug985402] de problemas de cromo  

### Mantenga el mouse sobre las propiedades de contenido CSS para ver valores sin escape   

Desplace el puntero sobre el valor de una `content` propiedad para ver la versión sin escape del valor.  

Por ejemplo, en esta [demostración][CSSContentDemo] , cuando Inspeccione el `p::after` seudoelemento, verá una cadena de escape en el panel Estilos:  

> ##### Imagen 16  
> La cadena de escape  
> ![La cadena de escape][ImageEscapedString]   

Cuando pasa el puntero sobre el `content` valor, Ve el valor unescape:  

> ##### Imagen 17  
> Valor sin escape  
> ![Valor sin escape][ImageUnescapedString]   

### Errores de mapas de origen más detallados en la consola   

La consola ahora proporciona más información sobre por qué no se pudo cargar o analizar un mapa de origen.  Anteriormente, se ha proporcionado un error sin explicar qué falló.  

> ##### Ilustración 18  
> Un error de carga del mapa de origen en la consola  
> ![Un error de carga del mapa de origen en la consola][ImageSourcemapError]  

### Configuración para deshabilitar el desplazamiento más allá del final de un archivo   

Abrir [configuración][Settings] y deshabilitar **preferencias**  >  **orígenes**:  >  **permite desplazarse más allá del final del archivo** para deshabilitar el comportamiento predeterminado de la interfaz de usuario que permite desplazarse hasta el final de un archivo en el panel **fuentes** .  

> ##### Ilustración 19  
> Deshabilitar la **opción permitir el desplazamiento más allá del final del archivo** en configuración  
> ![Deshabilitar la opción permitir el desplazamiento más allá del final del archivo][ImageSettings]  

> ##### Ilustración 20  
> El desplazamiento más allá del final de un archivo ya está deshabilitado en el panel orígenes  
> ![El desplazamiento más allá del final de un archivo ya está deshabilitado en el panel orígenes][ImageScroll]  

## Comentarios   



Para comentar las nuevas características y cambios de esta publicación, o cualquier otro tema relacionado con DevTools:  

*   Envíe sus comentarios con el icono de **comentarios** en el DevTools  

> ##### Ilustración 21  
> El icono de **comentarios** en el DevTools de Microsoft Edge  
> ![El icono * * comentarios * * en Microsoft Edge DevTools][ImageFeedbackIcon]  

*   Tweet a [@EdgeDevTools][PostTweetEdgeDevTools]  
*   Enviar una sugerencia a [la web][TheWebWeWant] que queremos  
*   Archivar errores en este documento en el repositorio [Edge-desarrollador][GitHubMicrosoftDocsEdgeDeveloperNewIssue]  

## Descargar los canales de Microsoft Edge Preview   

Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.  

<!-- <<../../_shared/devtools-feedback.md>>

<<../../_shared/canary.md>>

<<../../_shared/discover.md>> -->



<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Ilustración 1: la herramienta de rendimiento en DevTools con la navegación con el teclado y las mejoras del lector de pantalla"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Ilustración 2: el DevTools en alemán"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Ilustración 3: la pestaña sugerencias en Microsoft Edge DevTools cuando la extensión de explorador webhint está instalada"  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Ilustración 4: vista 3D en el DevTools de Microsoft Edge"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Ilustración 5: la herramienta elementos en VS Code que usa los elementos de la extensión de Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Ilustración 6: el depurador para la extensión de Microsoft Edge en VS Code"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Ilustración 7: la extensión de código webhint de VS analizando un archivo. TSX en VS Code"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Ilustración 8: Visual Studio con la opción de iniciar la aplicación web en Microsoft Edge Canarias, dev o beta"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Ilustración 9: mensajes en la consola cuando el control de prevención bloquea el acceso al almacenamiento de un rastreador" 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Ilustración 10: simular una ventanilla de moto G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Ilustración 11: mostrar el hardware de moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Ilustración 12: cookies bloqueadas en el panel de cookies del panel de aplicaciones"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Ilustración 13: edición de un valor de cookie"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Ilustración 14: copiar como fetch de node. js"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Ilustración 15: iconos en el panel manifiesto"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Ilustración 16: la cadena de escape"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Ilustración 17: el valor sin escape"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Ilustración 18: un error de carga del mapa de origen en la consola"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Ilustración 19: deshabilitar la opción permitir el desplazamiento más allá del final del archivo en configuración"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Ilustración 20: el desplazamiento más allá del final de un archivo ya está deshabilitado en el panel orígenes"
[ImageFeedbackIcon]: ../../images/2020/01/feedback-icon.msft.png "Ilustración 21: el icono * * comentarios * * en el DevTools de Microsoft Edge."


<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Simular un área de visualización móvil con el modo de dispositivo en Microsoft Edge DevTools"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Seleccione Mostrar marco del dispositivo para mostrar el marco del dispositivo físico en la ventanilla."
[CommandMenu]: ../../../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Limite la red y la CPU para simular de forma más precisa las condiciones de navegación web de un usuario móvil."
[crbug924693]: https://crbug.com/924693 "924693: solicitud de característica: agregar moto G4 a la lista de modos de dispositivo"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: la pestaña de cookies ya no muestra la prioridad en la consola de desarrollo"
[CookiesFields]: ../../../storage/cookies.md#fields "Los campos de la tabla cookies"
[crbug1029826]: https://crbug.com/1029826 "1029826: red > clic con el botón secundario para solicitar > copiar-> copia como fetch no copia las cookies"
[crbug985402]: https://crbug.com/985402 "985402: las cadenas de error del icono del manifiesto de la aplicación web son confusas"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Demostración de contenido CSS sin escape"
[Settings]: ../../../customize/index.md#settings "Personalizar Microsoft Edge DevTools con la configuración"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/Edge-Developer"  
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de Microsoft Edge Preview"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Depurador para la extensión de código de Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Elementos de la extensión de código de Microsoft Edge VS"  
[crbug963183]: https://crbug.com/963183 "963183-DevTools no cumplen la norma WCAG"
[crbug941561]: https://crbug.com/941561 "941561: localizabilidad del DevTools"
[crbug987787]: https://crbug.com/987787 "987787-vista 3D Dom"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Información de accesibilidad"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Complementos de Insider de Microsoft Edge"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Descargar Visual Studio 2019 para Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "índice z | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Código de Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Depurador para Microsoft Edge-Marketplace de Visual Studio"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Elementos de Microsoft Edge \ (cromo \)-Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint-catálogo de soluciones de Visual Studio"
[Webhint]: https://aka.ms/webhint "sugerencia"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Extensión de explorador webhint | documentación de webhint"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Extensión de código de VS webhint | documentación de webhint"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Mejorar la prevención de seguimiento en la entrada de blog de Microsoft Edge"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/01/devtools/index) y está creada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
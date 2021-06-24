---
description: Feature differences between Microsoft Edge and WebView2 title: Feature differences between Microsoft Edge and WebView2 author: MSEdgeTeam ms.author: msedgedevrel ms.date: 06/23/2021 ms.topic: conceptual ms.prod: microsoft-edge ms.technology: webview keywords: IWebView2, IWebView2WebView, WebView2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, edge html no-loc:
- "Autofill for Addresses"
- "Autofill for Passwords"
- "Autofill for Payments""
- "Browser Extensions""
- "Browser Task Manager"
- "Collections"
- "Continue-where-I-left-off prompt"
- "Downloads"
- "Edge Shopping"
- "Family Safety"
- "Favorites"
- "Hotkeys"
- "IE Mode"
- "Immersive Reader"
- "Intrusive Ads"
- "Read Aloud"
- "Smart Screen"
- "Translate"
- "Tracking Prevention"
- "Profile and Identity"
- "Web Payment API"
- "Windows Defender Application Guard"
- "edge:// URLs"

---
# <a name="feature-differences-between-microsoft-edge-and-webview2"></a>Diferencias de características entre Microsoft Edge y WebView2  

WebView2 se basa en el nuevo Microsoft Edge explorador.  Tienes la oportunidad de ampliar las características del explorador a las aplicaciones basadas en WebView2, lo que resulta útil.  Sin embargo, dado que WebView2 no está limitado a aplicaciones de explorador, hay algunas características del explorador que deben modificarse o quitarse.  En este artículo se proporciona la siguiente información.  

*   Características del explorador modificadas e información de soporte técnico.   
*   La capacidad de activar o desactivar la característica.  
*   Instrucciones sobre métodos abreviados de teclado.  
    
## <a name="design-guidelines"></a>Directrices de diseño  

En el contexto de WebView2, las características del explorador se adhieren a las siguientes directrices de diseño.  

*   La mayoría de las características funcionan igual en WebView2 y Microsoft Edge.  Si una característica no tiene sentido en el contexto de WebView2 o por otras razones, la característica se modifica o se apaga. 
*   Las características de WebView2 no incluyen Microsoft Edge personal de marca.  
    
## <a name="browser-features"></a>Características del explorador  

En la tabla siguiente se muestran las características de WebView2 que difieren del Microsoft Edge explorador.   

*   **El estado** predeterminado indica que la característica forma parte de la experiencia predeterminada en una nueva instancia webView2.  
*   **Configurable** indica que puede activar o desactivar la característica mediante API de WebView2 o modificadores de línea de comandos.  
    
> [!NOTE]  
> En este artículo no se trata la modificación de características mediante modificadores de línea de comandos.  Para obtener más información acerca de cómo activar y desactivar características con modificadores de línea de comandos, vaya a Lista de Chromium [modificadores de línea de comandos][PeterExperimentsChromiumCommandLineSwitches].  
    
| Característica | Estado predeterminado | Configurable | Detalles |  
|:--- |:--- |:--- | :--- |  
| Autofill for Addresses | Activado | Sí | Esta característica está activada de forma predeterminada, puede activarla o desactivarla con las API de autorrelleno de WebView2.  |  
| Autofill for Passwords | Activado | Sí | Esta característica está activada de forma predeterminada, puede activarla o desactivarla con las API de autorrelleno de WebView2.  |  
| Autorrellenar para pagos | Desactivado | No | Esta característica está desactivada.  |  
| Extensiones del explorador | Desactivado | No | Esta característica está desactivada.  |  
| Browser Task Manager | Desactivado | No | Esta característica está desactivada.  |  
| Collections | Desactivado | No | Esta característica está desactivada.  |  
| Continue-where-I-left-off prompt | Desactivado | No | Esta característica está desactivada.  |  
| Downloads | Activado | Sí | WebView2 proporciona una API que permite personalizar la interfaz de usuario de descarga para manipular las descargas. Por ejemplo, puede bloquear, redirigir, guardar, pausar, y así sucesivamente.  <!--For more information, navigate to [download API][Webview2ReferenceDownloadApi].--> |  
| Edge Shopping | Desactivado | No | Esta característica está desactivada.  |  
| Family Safety | Desactivado | No | Esta característica está desactivada.  |  
| Favorites | Desactivado | No | Esta característica está desactivada.  |  
| IE Mode | Desactivado | No | Esta característica está desactivada. WebView2 no admite el modo IE y tiene diferencias de comportamiento en comparación con IE (como compatibilidad con MHT o BIN). |  
| Immersive Reader | Desactivado | No | Esta característica depende de la interfaz de usuario del explorador para la interacción.  Esta característica está desactivada.  |  
| Intrusive Ads | Desactivado | No | Esta característica está desactivada.  |  
| Métodos abreviados de teclado. | Revisar detalles | Revisar detalles | Los métodos abreviados de teclado que están desactivados de forma predeterminada no tienen sentido o causan problemas en WebView2.  No puede activar ni desactivar estos métodos abreviados.  En su lugar, puede escuchar una combinación de teclas con el `AcceleratorKeyPressed` evento y crear una respuesta personalizada si es necesario.  Para obtener más información, vaya a [Información adicional de métodos abreviados de teclado](#additional-keyboard-shortcuts-information). | 
| Read Aloud | Desactivado | No | Esta característica está desactivada.  |  
| Smart Screen | Activado`*` | No | `*` La interfaz de usuario de esta característica se ha quitado, pero la funcionalidad subyacente sigue estando disponible.  Además, puede desactivar el Smart Screen uso de un modificador de línea de comandos.  |  
| Translate | Desactivado | No | Esta característica está desactivada.  |  
| Tracking Prevention | Activado`*` | No | `*` La interfaz de usuario de esta característica se ha quitado, pero la funcionalidad subyacente sigue estando disponible.  La prevención de seguimiento siempre está establecida en equilibrada.|  
| Profile and Identity | Desactivado | No | La característica que sincroniza tus favoritos, cookies, y así sucesivamente, está desactivada.  | 
| Windows Defender Application Guard | Desactivado | No | Esta característica está desactivada.  |  
| edge:// URLs | Revisar detalles | No | Configuración para el explorador Microsoft Edge están en `edge://` direcciones URL.  Dado que la mayoría de estas páginas web Microsoft Edge personal de marca o no tienen sentido en el contexto de WebView2, algunas de estas direcciones URL están desactivadas.  Para obtener más información, vaya [a Direcciones URL internas bloqueadas](#blocked-internal-urls).  |  

## <a name="web-platform-features"></a>Características de la plataforma web

En la tabla siguiente se muestran las características de la plataforma WebView2 que actualmente no están disponibles.

| Característica | Detalles |  
|:--- | :--- |  
| Notificaciones de inserción | Esta característica no se implementa en WebView2. |  
| Web Payment API | Esta característica está desactivada. | 

## <a name="blocked-internal-urls"></a>Direcciones URL internas bloqueadas  

Las páginas web Microsoft Edge y configuración de Google Chrome no están disponibles en WebView2.  

*   `chrome-search://local-ntp/local-ntp.html`  
*   `edge://application-guard-internals`  
*   `edge://apps`  
*   `edge://compat`  
*   `edge://extensions`  
*   `edge://favorites`  
*   `edge://help`  
*   `edge://management`  
*   `edge://network-error`  
*   `edge://new-tab-page`  
*   `edge://newtab`  
*   `edge://omnibox`  
*   `edge://settings`  
*   `edge://supervised-user-internals`  
*   `edge://version`  
    
## <a name="additional-keyboard-shortcuts-information"></a>Información adicional de métodos abreviados de teclado  

Los métodos abreviados de teclado o los enlaces de teclas se admiten en Microsoft Edge WebView2. Cuando Microsoft Edge actualizaciones, los enlaces de clave predeterminados pueden cambiar.  Además, un método abreviado de teclado que está desactivado de forma predeterminada puede activarse si la característica ahora es compatible con WebView2. Para evitar cambios en los métodos abreviados de teclado, puede establecer en , que desactiva todas las teclas que tienen acceso a las características del explorador, pero mantiene activados todos los métodos abreviados básicos de edición de texto y `AreBrowserAcceleratorKeysEnabled` `FALSE` movimiento.  

En la tabla siguiente se enumeran los accesos directos que siempre están desactivados en WebView2.  Un carácter asterisco \( \) indica que el acceso directo no está desactivado, pero la característica a la que tiene acceso está desactivada o no se aplica a `*` WebView2.  

| Acción | Windows |  
|:--- |:--- |  
| Agregar a Favorites | `Ctrl`+`D` |  
| Agregar todas las pestañas a Favorites | `Ctrl`+`Shift`+`D` |  
| Ubicación de foco | `Ctrl`+`L, Alt`+`D` |  
| Pegar y ir | `Ctrl`+`Shift`+`L` |  
| Abrir archivo | `Ctrl`+`O` |  
| Read Aloud `*` | `Ctrl`+`Shift`+`U` |  
| Captura web `*` | `Ctrl`+`Shift`+`S` |  
| Barra lateral `*` | `Ctrl`+`Shift`+`E` |  
| Guardar página | `Ctrl`+`S` |  
| Seleccionar última pestaña | `Ctrl`+`9` |  
| Seleccionar pestaña Siguiente | `Ctrl`+`Tab` |  
| Seleccionar ficha Anterior | `Ctrl`+`Shift`+`Tab` |  
| Seleccionar pestaña \(1 - 8\) | `Ctrl`+`(1-8)` |  
| Mostrar Favorites barra `*` | `Ctrl`+`Shift`+`B` |  
| Ayuda | `F1` |  
| Panel Siguiente de foco `*` | `F6` |  
| Panel anterior de foco `*` | `Shift`+`F6` |  
| Exploración de la caret `*` | `F7` |  
| Vista de lectura `*` | `F9` |  
| Barra de menús de foco | `F10` |  
| Menú Mostrar identidad `*` | `Ctrl`+`Shift`+`M` |  
| Browser Task Manager `*` | `Shift`+`Escape` |  
| Comentarios perimetrales `*` | `Shift`+`Alt`+`I` |  
| Ficha Silenciar `*` | `Ctrl`+`M` |  
| Nueva ventana incógnito | `Ctrl`+`Shift`+`N` |  
| Nueva pestaña | `Ctrl`+`T` |  
| Nueva ventana | `Ctrl`+`N` |  
| Restaure la pestaña Last Closed | `Ctrl`+`Shift`+`T` |  
| Enfoque Favorites | `Alt`+`Shift`+`B` |  
| Elemento emergente inactivo de foco | `Alt`+`Shift`+`A` |  
| Búsqueda de foco | `Ctrl`+`E`, `Ctrl`+`K`, `Search Key` |  
| Pestaña Duplicada | `Ctrl`+`Shift`+`K` |  
| Barra de herramientas de foco `*` | `Alt`+`Shift`+`T` |  
| Inicio | `Alt`+`Home`, `Browser Home Key` |  
| Menú Mostrar aplicación | `Alt`+`E, Alt`+`F` |  
| Mostrar Favorites | `Ctrl`+`Shift`+`O` |  
| Mostrar Downloads | `Ctrl`+`J` |  
| Mostrar historial | `Ctrl`+`H` |  
| Mostrar barra de modo de lectura `*` | `Shift`+`Alt`+`R` |  
| Mostrar Collections `*` | `Ctrl`+`Shift`+`Y` |  

Los siguientes métodos abreviados de teclado siempre están desactivados, excepto en las ventanas que se muestran cuando no `NewWindowRequested` se controla el evento.

| Acción | Windows |  
|:--- |:--- |  
| Pestaña Cerrar | `Ctrl`+`W, Ctrl`+`F4` |  
| Cerrar ventana | `Ctrl`+`Shift`+`W` |  
| Pantalla completa | `F11` |  

Si establece en , se desactivarán `AreBrowserAcceleratorKeysEnabled` `FALSE` los siguientes métodos abreviados de teclado adicionales.  

| Acción | Windows |  
|:--- |:--- |  
| Detener | `Escape` |  
| Buscar en la página | `Ctrl`+`F` |  
| Buscar siguiente | `Ctrl`+`G` |  
| Buscar anterior | `Ctrl`+`Shift`+`G` |  
| Imprimir | `Ctrl`+`P` |  
| Actualizar | `Ctrl`+`R`, `F5`, `Reload Key` |  
| Actualizar sin caché | `Ctrl`+`Shift`+`R`, `Ctrl`+`F5`, `Shift`+`F5`, `Ctrl`+`Refresh`, `Shift`+`Refresh` |  
| Alejar | `Ctrl`+`-` |  
| Acercar | `Ctrl`+`+` |  
| Restablecer zoom | `Ctrl`+`0` |  
| Buscar siguiente | `F3` |  
| Buscar anterior | `Shift`+`F3` |  
| Atrás | `Alt`+`Left, Browser Back Key` |  
| Adelante | `Alt`+`Right`, `Browser Forward Key` |  
| Imprimir | `Ctrl`+`P` |  
| Abrir y cerrar DevTools | `Ctrl`+`Shift`+`I` |  
| Abrir la consola de DevTools | `Ctrl`+`Shift`+`J` |  
| Abrir Inspección de DevTools | `Ctrl`+`Shift`+`C` |  

> [!Note] 
> Para personalizar cualquiera de las claves individualmente, use el [evento AcceleratorKeyPressed.][DotnetApiMicrosoftWebWebview2CoreCorewebview2controllerAcceleratorkeypressedViewWebview2Dotnet1077444]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview2-team"></a>Getting in touch with the Microsoft Edge WebView2 team  

[!INCLUDE [contact WebView2 team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

<!--[Webview2ReferenceDownloadApi]: ./download-api.md "download API | Microsoft Docs"  -->  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2controllerAcceleratorkeypressedViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2controller.acceleratorkeypressed?view=webview2-dotnet-1.0.774.44&preserve-view=true "Evento CoreWebView2Controller.AcceleratorKeyPressed | Microsoft Docs"  

[DevtoolsShortcutsIndex]: ../../devtools-guide-chromium/shortcuts/index.md "Microsoft Edge Métodos abreviados de teclado de DevTools | Microsoft Docs"  

[GithubMicrosoftedgeWebview2feedbackIssues308]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/308 "Agregar compatibilidad con la API de notificación HTML5 (#308) | GitHub"  

[PeterExperimentsChromiumCommandLineSwitches]: https://peter.sh/experiments/chromium-command-line-switches "Lista de Chromium modificadores de línea de comandos | Peter Beverloo"  

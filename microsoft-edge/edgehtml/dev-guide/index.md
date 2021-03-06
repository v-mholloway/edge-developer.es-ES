---
description: En esta guía se proporciona información general sobre las características y estándares del desarrollador incluidos en Microsoft Edge.
title: Novedades de EdgeHTML 18
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: edge, desarrollo web, html, css, javascript, developer, devtools
ms.custom: RS5
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6b53163115ad7db8e5b792cadda0c59b93b6711b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399228"
---
# <a name="microsoft-edge-developer-guide"></a>Guía para desarrolladores de Microsoft Edge  

> [!TIP]
> Nos hemos [](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) asociado con otros exploradores y la comunidad web para adoptar [MDN Web Docs](https://developer.mozilla.org/) como el lugar definitivo para la documentación útil, imparcial y independiente del explorador para las tecnologías web basadas en estándares actuales y emergentes.  Puede encontrar detalles sobre la compatibilidad con la API de EdgeHTML directamente en cada página de la [biblioteca de referencia web de MDN](https://developer.mozilla.org/docs/Web).  Visite el estado de la plataforma [de](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) Microsoft Edge para ver las características más recientes admitidas en Microsoft Edge.  

## <a name="whats-new-in-edgehtml-18"></a>Novedades de EdgeHTML 18  

EdgeHTML 18 incluye las siguientes características nuevas y actualizadas que se incluyen en la versión actual de la plataforma Microsoft Edge, a partir de la actualización de Windows 10 de octubre de [2018](/windows/uwp/whats-new/windows-10-build-17763) \(10/2018, compilación 17763\).  Para ver los cambios en compilaciones específicas de [Windows Insider](https://insider.windows.com) Preview, consulta el Registro de cambios de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog) y Novedades [de EdgeHTML](./whats-new.md).  

Este es el vínculo permanente para la siguiente lista de cambios: [https://docs.microsoft.com/microsoft-edge/dev-guide](#new-apis-in-edgehtml-18) .  

## <a name="new-and-updated-features"></a>Características nuevas y actualizadas  

### <a name="autoplay-policies"></a>Directivas de reproducción automática  

Con Windows 10 October 2018 Update, Microsoft Edge ofrece a los clientes la capacidad de personalizar sus preferencias de navegación en sitios web que reproducción automática de medios con sonido para minimizar distracciones en la web y conservar el ancho de banda.  Los usuarios pueden personalizar el comportamiento multimedia con controles de reproducción automática globales y por sitio.  Además, Microsoft Edge suprime automáticamente la reproducción automática de medios en pestañas en segundo plano.  

Consulte la [Guía de directivas de reproducción](./browser-features/autoplay-policies.md) automática para obtener detalles y procedimientos recomendados para garantizar una buena experiencia de usuario con los medios hospedados en su sitio.  

### <a name="chakra-improvements"></a>Mejoras de Chakra  

EdgeHTML 18 incluye actualizaciones del motor de JavaScript de Chakra para admitir nuevas características de ES y WASM, además de mejoras de rendimiento e interoperabilidad.  Consulte las Notas de [la versión de ChakraCore 1.11](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111) para obtener más información.  

### <a name="css-updates"></a>Actualizaciones css  

Hemos avanzado aún más en nuestra implementación experimental de [enmascaramiento CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) \(detrás de la marca Habilitar máscara *CSS\)* con compatibilidad agregada para máscara [compuesta,](https://developer.mozilla.org/docs/Web/CSS/mask-composite)posición [de](https://developer.mozilla.org/docs/Web/CSS/mask-position)máscara y [máscara-repetición](https://developer.mozilla.org/docs/Web/CSS/mask-repeat).  Para la compatibilidad de sitios, Microsoft Edge también admite las siguientes propiedades *-webkit-mask:* -webkit-mask, -webkit-mask-composite, -webkit-mask-image, -webkit-mask-position, -webkit-mask-position-x, -webkit-mask-position-y, -webkit-mask-repeat, -webkit-mask-size.  

Además, Microsoft Edge ahora admite el ajuste [de](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap) desbordamiento y la compatibilidad parcial con el comportamiento de [sobrescroll](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) \( `auto` y `contain` values\).  

### <a name="developer-tools"></a>Herramientas de desarrollo  

La actualización más reciente de Microsoft Edge DevTools agrega una serie de comodidades tanto a la interfaz de usuario como bajo el capó, incluidos los nuevos paneles dedicados para los trabajadores de servicio y el almacenamiento, las herramientas de búsqueda de archivos de origen en el depurador y los nuevos dominios del protocolo Edge DevTools para la depuración de estilo/diseño y las API de consola.  

[DevTools en la última actualización de Windows 10 (EdgeHTML 18)](./whats-new.md) tiene todos los detalles.  

### <a name="listening-to-your-feedback"></a>Escuchar sus comentarios  

Escuchamos sus comentarios y hemos implementado la compatibilidad con varias API solicitadas en EdgeHTML 18, incluido el método [DataTransfer.setDragImage()](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) usado para establecer una imagen personalizada al arrastrar y colocar, y [secureConnectionStart](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart), una propiedad de la API de sincronización de recursos de rendimiento, que se puede usar para devolver una marca de tiempo inmediatamente antes de que el explorador inicie el proceso de protocolo de enlace para proteger la conexión actual.  

Además, a nadie le gusta enumerar la colección de atributos, por lo que hemos agregado compatibilidad con [Element.getAttributeNames](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) para devolver los nombres de atributo del elemento como una matriz de cadenas, así como [Element.toggleAttribute](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) para alternar un atributo booleano \(quitando si está presente y agregando si no es así\).  

### <a name="progressive-web-apps"></a>Aplicaciones web progresivas  

#### <a name="lifetime-background-script"></a>Script en segundo plano de vigencia  

Las aplicaciones JavaScript de Windows 10 \(aplicaciones web que se ejecutan en un proceso\) ahora admiten un script en segundo plano opcional por aplicación que se inicia antes de que se activen las vistas y se ejecuten durante la duración del `WWAHost.exe` proceso.  Con esto, puede supervisar y modificar las navegaciónes, realizar un seguimiento del estado de las navegaciónes, supervisar errores de navegación y ejecutar código antes de que se activen las vistas.  

Cuando se especifica como [StartPage](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) en el manifiesto de la aplicación [,](/uwp/schemas/appxpackage/appx-package-manifest)cada una de las vistas de la aplicación \(windows\) se exponen al script como instancias de la nueva [clase WebUIView,](/uwp/api/windows.ui.webui.webuiview) proporcionando los mismos eventos, propiedades y métodos que un [webView](/uwp/api/windows.web.ui.iwebviewcontrol)general \(Win32\) .  El script puede escuchar el evento [NewWebUIViewCreated](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) para interceptar el control de la navegación de una nueva vista:  

```javascript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```  

 Cualquier activación de la aplicación con el script en segundo plano como el `StartPage` se basará en el propio script para la navegación.  

#### <a name="text-scaling"></a>Ajuste de escala de texto  

La actualización de Windows 10 de octubre [](/windows/uwp/design/input/text-scaling#user-experience) de 2018 presenta la configuración Hacer que el texto sea más grande para mejorar la accesibilidad del usuario final, y los PWA instalados en Windows \(además UWP y la mayoría de las aplicaciones de escritorio\) ahora admiten esta característica automáticamente.  Para los controles PWA y WebView, la escala de texto funciona del mismo modo que la escala de PPP.  Si un usuario cambia tanto la escala de texto como la escala de PPP, el resultado es el producto de los dos.  

 Para obtener instrucciones de diseño, consulta la [guía para](/windows/uwp/design/input/text-scaling) UWP de escalado de texto en el Centro de desarrollo *de Windows.*  

### <a name="service-worker-updates"></a>Actualizaciones del trabajador de servicio  

Para obtener un actualizador sobre lo que son los trabajadores de servicio y cómo funcionan, consulte el resumen de [la API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) de trabajador de servicio escrito por nuestros asociados en MDN.  Hubo varias actualizaciones de Microsoft Edge que admiten trabajadores de servicio en EdgeHTML 18.  Permite al trabajador de servicio usar preloadResponse para prometer una respuesta `fetchEvent` y [el resultingClientId](https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) para devolver el identificador del cliente que controla el trabajador de servicio actual. [](https://developer.mozilla.org/docs/Web/API/FetchEvent)  
La [interfaz NavigationPreloadManager](https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) proporciona métodos para administrar la precarga de recursos, lo que le permite realizar una solicitud en paralelo mientras un trabajador de servicio está arrancando, evitando cualquier retraso de tiempo.  Consulte las propiedades [de api que se](#new-apis-in-edgehtml-18) han admitido recientemente para obtener la lista de métodos y propiedades de precarga del trabajador de servicio.  

### <a name="web-authentication"></a>Autenticación Web  

Microsoft Edge ahora incluye [compatibilidad sin](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge) colocar para la nueva API de autenticación web \(aka [WebAuthN](https://w3c.github.io/webauthn)\).  La autenticación web proporciona una solución abierta, escalable e interoperable para simplificar la autenticación, lo que permite mejores y más seguras experiencias de usuario mediante la sustitución de contraseñas por credenciales más sólidas enlazadas por hardware.  La implementación en Microsoft Edge permite el uso de [Windows Hello](https://www.microsoft.com/windows/windows-hello) que permite a los usuarios iniciar sesión con su rostro, huella digital o PIN, además de autenticadores [externos](https://fidoalliance.org) como claves de seguridad FIDO2 o claves de seguridad de FIDO U2F, para autenticarse de forma segura en sitios web.  

Para obtener más información, diríjase a la entrada de blog Introducción a la autenticación [web en Microsoft Edge](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge).  

### <a name="webdriver"></a>WebDriver  

WebDriver es ahora una característica de [Windows](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) a petición \(FoD\) lo que facilita más que nunca automatizar las pruebas en Microsoft Edge y obtener la versión correcta para el dispositivo.  Ya no necesitarás hacer coincidir manualmente la compilación, la rama o el sabor al instalar WebDriver, tu [WebDriver](https://www.w3.org/TR/webdriver) se actualizará automáticamente para que coincida con las actualizaciones nuevas de Windows 10.  

Puede instalar WebDriver al activar el Modo de desarrollador o **** instalarlo como independiente yendo a Configuración aplicaciones & características administrar  >  ****  >  ****  >  **características opcionales.**  Para obtener más información, consulte el anuncio [de WebDriver en el sitio del Blog de Windows](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand).  

### <a name="web-notification-properties"></a>Propiedades de notificación web  

Ahora se admiten cuatro nuevas propiedades para las notificaciones web:  [acciones](https://developer.mozilla.org/docs/Web/API/notification/actions) [,](https://developer.mozilla.org/docs/Web/API/notification/badge) [distintivo,](https://developer.mozilla.org/docs/Web/API/notification/image)imagen y , mejorando nuestra capacidad para crear notificaciones en la web que sean compatibles con los sistemas de notificaciones existentes, mientras que permanecen independientes de la  `maxActions` plataforma.  

### <a name="webview"></a>WebView  

#### <a name="service-workers"></a>Trabajadores de servicios  

[Los trabajadores](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) de servicio ahora son compatibles con el control WebView, además del explorador Microsoft Edge y las aplicaciones JavaScript de Windows 10.  Todos los tipos de la vista web de Microsoft Edge \([PWA](/microsoft-edge/hosting/webview), [UWP](/uwp/api/Windows.UI.Xaml.Controls.WebView), [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)\) admiten trabajadores de servicio, pero ten en cuenta que la [API](https://developer.mozilla.org/docs/Web/API/Push_API) de inserción aún no está disponible para las versiones de UWP y Win32.  

Las arquitecturas de aplicaciones x64 requieren paquetes neutros \(Any CPU\) o x64, ya que los trabajadores de servicio no son compatibles con procesos woW64.  \(Para conservar el espacio en disco, la versión WoW de las DLL necesarias no se incluye de forma nativa en Windows.\)  

#### <a name="win32-webview-updates"></a>Actualizaciones de Win32 WebView  

Las aplicaciones edgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) para escritorio de Windows \(Win32\) se han actualizado con varias características nuevas, incluida la capacidad de insertar scripts al cargar la página antes de que se ejecuten otros scripts de la página \([AddInitializeScript](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript)\) y saber cuándo un WebViewControl determinado recibe o pierde el foco \([GotFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [LostFocus](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus)\).  

Además, ahora puede crear un nuevo WebViewControl como la ventana abierta desde [window.open](https://developer.mozilla.org/docs/Web/API/Window/open).  El evento [NewWindowRequested](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) todavía notifica a una aplicación cuando el script dentro de WebViewControl llama a window.open como siempre lo ha hecho, pero con EdgeHTML 18 su [NewWindowRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) incluye la capacidad de tomar un aplazamiento \([GetDeferral](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral)\) para establecer un nuevo WebViewControl \([NewWindow](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow)\) como destino de window.open:  

```csharp
WebViewControlProcess wvProc;
WebViewControl webView;

void OnWebViewControlNewWindowRequested(WebViewControl sender, WebViewControlNewWindowRequestedEventArgs args)
{

    if (args.Uri.Domain == "mydomain.com")
    {
        using deferral = args.GetDeferral();
        args.NewWindow = await wvProc.CreateWebViewControlAsync(
            parentWindow, targetWebViewBounds);
        deferral.Complete();
    }
    else
    {
        // Prevent WebView from launching in the default browser.
        args.Handled = true;
    }
}

String htmlContent = "<html><script>window.open('http://mydomain.com')</script><body></body></html>";

webView.NavigateToString(htmlContent);
```  

Por último, es posible que los usuarios avanzados observen la aplicación del Visor web de aplicaciones de escritorio \(anteriormente denominado Win32WebViewHost\), una aplicación de sistema interna que representa Win32 WebView, en los siguientes lugares:  

*   En el Centro de acciones de Windows 10.  El origen de estas notificaciones debe entenderse desde un WebView hospedado desde una aplicación win32.  
*   En la interfaz de usuario de configuración de acceso al dispositivo \( `Settings`  >  `Privacy`  >  `Camera/Location/Microphone` \).  Deshabilitar cualquiera de estas opciones de configuración deniega el acceso de todas las WebView hospedadas en aplicaciones de Win32.  

![Configuración de acceso a dispositivos de Desktop App Web Viewer](./media/desktop-app-web-viewer.png)  

## <a name="deprecated-features"></a>Características en desuso  

### <a name="xss-filter-now-retired"></a>Filtro XSS ahora retirado  

Con EdgeHTML 18, estamos retirando el filtro XSS en Microsoft Edge.  Nuestros clientes permanecen protegidos gracias a estándares modernos como la directiva de seguridad de contenido [(CSP),](https://developer.mozilla.org/docs/Web/HTTP/CSP)que proporcionan mecanismos más eficaces, eficaces y seguros para proteger contra ataques de inyección de contenido, con alta compatibilidad en los exploradores modernos.  

## <a name="new-apis-in-edgehtml-18"></a>Nuevas API en EdgeHTML 18  

Consulte la lista completa de nuevas API en EdgeHTML 18.  Se enumeran con el formato de [nombre de interfaz]. [nombre de api].  

> [!NOTE] 
> Aunque las siguientes API se exponen en el DOM, el comportamiento de extremo a extremo de algunas puede estar todavía en desarrollo y oculto detrás de una marca experimental.  Consulte Estado de  [la plataforma Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) para obtener información oficial sobre la compatibilidad con características.  

<iframe height='580' scrolling='no' title='Nuevas API en EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Vea las API nuevas del lápiz <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> en EdgeHTML 18 </a> por MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) en </a> <a href='https://codepen.io'> CodePen </a> .</iframe>  

## <a name="previous-edgehtml-releases"></a>Versiones anteriores de EdgeHTML  

[EdgeHTML 13 / Windows build 10586 (11/2015)](./whats-new/edgehtml-13.md)  

[EdgeHTML 14 / Compilación de Windows 14393 (8/2016)](./whats-new/edgehtml-14.md)  

[EdgeHTML 15 / Windows build 15063 (4/2017)](./whats-new/edgehtml-15.md)  

[EdgeHTML 16 / Compilación de Windows 16299 (10/2017)](./whats-new/edgehtml-16.md)  

[EdgeHTML 17 / Compilación de Windows 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)  

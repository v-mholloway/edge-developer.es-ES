---
title: Novedades de EdgeHTML 18
description: Esta guía proporciona una descripción general de las características y los estándares del desarrollador que se incluyen en Microsoft Edge.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/06/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, DevTools
ms.custom: RS5
ms.openlocfilehash: b9285be7169f197a687e9f754a20cf67bbde160d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572974"
---
# Guía para desarrolladores de Microsoft Edge

> [!TIP]
> Hemos [colaborado](https://blogs.windows.com/msedgedev/2017/10/18/documenting-web-together-mdn-web-docs/) con otros exploradores y la comunidad web en la adopción de [documentos web de MDN](https://developer.mozilla.org/) como lugar definitivo para la documentación útil, no sesgada y independiente del explorador para las tecnologías web basadas en estándares actuales y emergentes. Puede encontrar detalles sobre la compatibilidad con la API de EdgeHTML directamente en cada página de la [biblioteca de referencia Web de MDN](https://developer.mozilla.org/docs/Web). Visita el estado de la [plataforma](https://developer.microsoft.com/microsoft-edge/platform/status/?q=edge%3AShipped%20edge%3APrefixed%20edge%3A'Preview%20Release) de Microsoft Edge para obtener las características más recientes compatibles con Microsoft Edge. 


## Novedades de EdgeHTML 18

EdgeHTML 18 incluye las siguientes características nuevas y actualizadas que se incluyen en la versión actual de la plataforma Microsoft Edge, a partir de la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) (10/2018, compilación 17763). Para obtener información sobre los cambios en las compilaciones específicas de [Windows Insider](https://insider.windows.com/) Preview, vea el registro de cambios de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/changelog/) y las novedades [de EdgeHTML](./dev-guide/whats-new.md).

Este es el vínculo permanente de la siguiente lista de cambios: [https://aka.ms/devguide_edgehtml_18](https://aka.ms/devguide_edgehtml_18) .

## Características nuevas y actualizadas

### Directivas de reproducción automática

Con la actualización del 2018 de octubre de Windows 10, Microsoft Edge proporciona a los clientes la posibilidad de personalizar sus preferencias de navegación en sitios web con sonido automático para minimizar las distracciones en Internet y ahorrar ancho de banda. Los usuarios pueden personalizar el comportamiento de los medios con controles de reproducción automática globales y por sitio. Además, Microsoft Edge elimina automáticamente la reproducción automática de los elementos multimedia en las pestañas de fondo.

Consulte la guía de [directivas de reproducción automática](./dev-guide/browser-features/autoplay-policies.md) para obtener detalles y procedimientos recomendados para garantizar una buena experiencia de usuario con los elementos multimedia hospedados en su sitio.

### Mejoras de Chakra

EdgeHTML 18 incluye actualizaciones para el motor de JavaScript de Chakra para admitir nuevas características s y WASM, además de mejoras de rendimiento y interoperabilidad. Consulte las notas de la [versión de ChakraCore 1,11](https://github.com/Microsoft/ChakraCore/wiki/Roadmap#chakracore-111) para obtener más información.

### Actualizaciones de CSS

Hemos progresado aún más en nuestra implementación experimental de [enmascaramiento de CSS](https://developer.mozilla.org/docs/Web/CSS/CSS_Masking) (detrás de la marca de *Habilitar máscaras CSS* ) con compatibilidad añadida para [máscara: composición](https://developer.mozilla.org/docs/Web/CSS/mask-composite), [posición de máscara](https://developer.mozilla.org/docs/Web/CSS/mask-position)y [repeticiones de máscara](https://developer.mozilla.org/docs/Web/CSS/mask-repeat). Para la compatibilidad del sitio, Microsoft Edge también admite las siguientes: *WebKit-* Properties:-WebKit-Mask,-WebKit-Mask-composite,-WebKit-Mask,,-barra.-barra. de-a,-barra... y-máscara: repite.-barra. de-x. por.

Además, Microsoft Edge ahora es compatible con [el desbordamiento de desbordamiento](https://developer.mozilla.org/docs/Web/CSS/overflow-wrap
) y la compatibilidad parcial para [el redesplazamiento, comportamiento](https://developer.mozilla.org/docs/Web/CSS/overscroll-behavior) ( `auto` y `contain` valores).


### Herramientas de desarrollo

La actualización más reciente de Microsoft Edge DevTools agrega varias ventajas a la interfaz de usuario y al Capó, incluidos nuevos paneles dedicados para el almacenamiento y los trabajos de servicio, las herramientas de búsqueda de archivos de origen en el depurador y los nuevos dominios de protocolo de DevTools de borde para la depuración de estilo o diseño y las API de consola.

[DevTools en la actualización más reciente de Windows 10 (EdgeHTML 18)](./devtools-guide/whats-new.md) tiene todos los detalles.

### Cómo escuchar sus comentarios

Escuchamos sus comentarios y hemos implementado la compatibilidad con varias API solicitadas en EdgeHTML 18, incluido el [`DataTransfer.setDragImage()`](https://developer.mozilla.org/docs/Web/API/DataTransfer/setDragImage) método usado para establecer una imagen personalizada al arrastrar y colocar, y [`secureConnectionStart`](https://developer.mozilla.org/docs/Web/API/PerformanceResourceTiming/secureConnectionStart) una propiedad de la API de temporización de recursos de rendimiento, que se puede usar para devolver una marca de tiempo inmediatamente antes de que el explorador inicie el proceso de enlace para proteger la conexión actual. 

Además, nadie me gusta la enumeración de la colección de atributos, así que hemos agregado compatibilidad con para [`Element.getAttributeNames`](https://developer.mozilla.org/docs/Web/API/Element/getAttributeNames) devolver los nombres de atributo del elemento como una matriz de cadenas, así como [`Element.toggleAttribute`](https://developer.mozilla.org/docs/Web/API/Element/toggleAttribute) para activar o desactivar un atributo booleano (quitando si está presente y agregando si no).

### Aplicaciones web progresivas

#### Script de fondo de duración

Las aplicaciones de Windows 10 de JavaScript (aplicaciones web que se ejecutan en un proceso *WWAHost. exe* ) ahora son compatibles con un script de fondo opcional por aplicación que se inicia antes de que se activen las vistas y se ejecuta durante la duración del proceso. De esta forma, puede supervisar y modificar la navegación, realizar un seguimiento del estado en todas las navegaciones, supervisar los errores de navegación y ejecutar el código antes de que se activen las vistas. 

Cuando se especifica como el [`StartPage`](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) en el manifiesto de la [aplicación](/uwp/schemas/appxpackage/appx-package-manifest), cada una de las vistas de la aplicación (Windows) se expone en el script como instancias de la nueva [`WebUIView`](/uwp/api/windows.ui.webui.webuiview) clase, lo que proporciona los mismos eventos, propiedades y métodos que una [vista previa](/uwp/api/windows.web.ui.iwebviewcontrol)general (Win32). El script puede escuchar el [`NewWebUIViewCreated`](/uwp/api/windows.ui.webui.newwebuiviewcreatedeventargs) evento para interceptar el control de la navegación para una nueva vista:

```JavaScript
Windows.UI.WebUI.WebUIApplication.addEventListener("newwebuiviewcreated", newWebUIViewCreatedEventHandler);
```

 Cualquier activación de la aplicación con el script de fondo como dependerá de `StartPage` la propia secuencia de comandos para la navegación.

#### Ajuste de escala de texto

La actualización de Windows 10 de octubre de 2018 introduce la configuración [*aumentar el tamaño del texto*](https://review.docs.microsoft.com/windows/uwp/design/input/text-scaling?branch=master#user-experience) para mejorar la accesibilidad del usuario final, y PWAs instalado en Windows (además UWP y la mayoría de las aplicaciones de escritorio) ahora admite esta característica automáticamente. Para los controles PWAs y WebView, la escala de texto funciona de la misma manera que el escalado de PPP. Si un usuario cambia la escala de texto y la escala de PPP, el resultado es el producto de los dos.

 Para obtener ayuda sobre el diseño, consulta la guía de [escala de texto](/windows/uwp/design/input/text-scaling) de UWP en el centro de *desarrollo de Windows*.

### Actualizaciones de trabajo de servicio 

Para obtener un repaso sobre qué son los trabajos de servicio y cómo funcionan, consulte el Resumen de [API de trabajadores del servicio]( https://developer.mozilla.org/docs/Web/API/Service_Worker_API) escrito por nuestros socios en MDN.  Hubo varias actualizaciones para los trabajadores del servicio de soporte técnico de Microsoft Edge en EdgeHTML 18. El `fetchEvent` permite al trabajador del servicio usar [`preloadResponse`]( https://developer.mozilla.org/docs/Web/API/FetchEvent) para comprometer una respuesta y el [`resultingClientId`]( https://developer.mozilla.org/docs/Web/API/FetchEvent/clientId) para que devuelva el identificador del cliente que controla el trabajador de servicio actual.  
La [`NavigationPreloadManager`]( https://developer.mozilla.org/docs/Web/API/NavigationPreloadManager) interfaz proporciona métodos para administrar la carga previa de recursos, lo que le permite hacer una solicitud en paralelo mientras se está iniciando un trabajo de servicio, evitando cualquier retraso de tiempo. Consulte las propiedades de la [API recientemente admitidas](#new-apis-in-edgehtml-18) para la lista de métodos y propiedades de carga previa de los trabajos del servicio. 

### Autenticación Web

Microsoft Edge ahora incluye [compatibilidad no prefijada para la nueva API de autenticación Web](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge/) (también conocido como [webauthn](https://w3c.github.io/webauthn/)). La autenticación Web ofrece una solución abierta, escalable e interoperable para simplificar la autenticación, lo que permite experiencias de usuario mejores y más seguras reemplazando las contraseñas con credenciales de hardware más seguras. La implementación en Microsoft Edge permite el uso de [Windows Hello](https://www.microsoft.com/windows/windows-hello) para permitir que los usuarios inicien sesión con su cara, huella dactilar o PIN, además de [autenticadores externos](https://fidoalliance.org) como las claves de seguridad de FIDO2 o Fido U2F claves de seguridad, para autenticar de manera segura en sitios Web.

Para obtener más información, vaya a la entrada de blog que [presenta la autenticación Web en Microsoft Edge](https://blogs.windows.com/msedgedev/2018/07/30/introducing-web-authentication-microsoft-edge).

### WebDriver

Webdriver es ahora una [característica de Windows a petición](https://docs.microsoft.com/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (du) que hace que sea más fácil que nunca automatizar las pruebas en Microsoft Edge y obtener la versión adecuada para el dispositivo. Ya no necesitarás hacer coincidir la compilación, rama o sabor de forma manual al instalar Webdriver, el [controlador WebDrive](https://www.w3.org/TR/webdriver) se actualizará automáticamente para coincidir con las nuevas actualizaciones de Windows 10. 

Puede instalar webdrives activando el modo de desarrollador o instalarlo como independiente yendo a configuración > aplicaciones > aplicaciones & características > administrar características opcionales. Para obtener más información, consulte el [anuncio de Webdriver en el sitio del blog de Windows](https://blogs.windows.com/msedgedev/2018/06/14/webdriver-w3c-recommendation-feature-on-demand).

### Propiedades de la notificación Web
Ahora se admiten cuatro nuevas propiedades para las notificaciones Web: [`actions`](https://developer.mozilla.org/docs/Web/API/notification/actions) ,, [`badge`](https://developer.mozilla.org/docs/Web/API/notification/badge) [`image`](https://developer.mozilla.org/docs/Web/API/notification/image) y `maxActions` , mejorar nuestra capacidad de crear notificaciones en la web que sean compatibles con los sistemas de notificación existentes, sin importar la plataforma.

### WebView

#### Trabajadores de servicio
Los [trabajadores del servicio](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) ahora son compatibles con el control WebView, además de las aplicaciones Microsoft Edge browser y JavaScript de Windows 10. Todas las versiones de la WebView de Microsoft Edge ([PWA](/microsoft-edge/hosting/webview), [UWP](/uwp/api/Windows.UI.Xaml.Controls.WebView), [Win32](/windows/communitytoolkit/controls/wpf-winforms/webview)) son compatibles con los trabajadores del servicio; sin embargo, ten en cuenta que la [API Push](https://developer.mozilla.org/docs/Web/API/Push_API) aún no está disponible para las versiones para UWP y Win32.

las arquitecturas de aplicaciones x64 requieren paquetes *neutros* (cualquier CPU) o *x64* , ya que los trabajos de servicio no son compatibles con los procesos de WOW64. (Para ahorrar espacio en el disco, la versión de WoW de los archivos dll necesarios no se incluye de forma nativa en Windows).

#### Actualizaciones de WebView Win32

Las aplicaciones de EdgeHTML [WebViewControl](/windows/communitytoolkit/controls/wpf-winforms/webview) para escritorio de Windows (Win32) se han actualizado con varias características nuevas, entre las que se incluyen la capacidad de inyectar script tras la carga de páginas antes de que se ejecuten otros scripts de la página ( [`AddInitializeScript`](/uwp/api/windows.web.ui.interop.webviewcontrol.addinitializescript) ) y saber cuándo un WebViewControl determinado recibe o pierde el foco ( [`GotFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.gotfocus) / [`LostFocus`](/uwp/api/windows.web.ui.interop.webviewcontrol.lostfocus) ).

Además, ahora puede crear un nuevo WebViewControl como la ventana abierta de [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) . El [`NewWindowRequested`](/uwp/api/windows.web.ui.iwebviewcontrol.newwindowrequested) evento sigue notificando a una aplicación cuando hay una secuencia de comandos en la ventana de llamadas de WebViewControl. se abre como siempre, pero con EdgeHTML 18 se [`NewWindowRequestedEventArgs`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs) incluye la capacidad de realizar un aplazamiento ( [`GetDeferral`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.getdeferral) ) para establecer una nueva WebViewControl ( [`NewWindow`](/uwp/api/windows.web.ui.webviewcontrolnewwindowrequestedeventargs.newwindow) ) como destino de la ventana. abrir:

```C#
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

Por último, es posible que los usuarios avanzados perciban el apppearance de la *aplicación de escritorio Web Viewer* (anteriormente denominado *Win32WebViewHost*), una aplicación interna del sistema que representa la WebView de Win32, en los siguientes lugares:
- En el *centro de actividades de Windows 10*. El origen de estas notificaciones debe entenderse a partir de una vista previa hospedada desde una aplicación Win32.
- En la interfaz de usuario de la configuración de acceso del dispositivo (*configuración->privacidad->cámara/ubicación/micrófono*). Al deshabilitar cualquiera de estas opciones de configuración, se deniega el acceso desde todas las vistas que se hospedan en aplicaciones Win32.

![Configuración de acceso de dispositivo de la aplicación de escritorio Web Viewer](./dev-guide/media/desktop-app-web-viewer.png)


## Características obsoletas

### Filtro XSS retirados

Con EdgeHTML 18, estamos retirando el filtro XSS en Microsoft Edge. Nuestros clientes siguen estando protegidos gracias a estándares modernos como la [política de seguridad de contenido (CSP)](https://developer.mozilla.org/docs/Web/HTTP/CSP), que proporcionan mecanismos más eficaces, de rendimiento y seguridad para protegerse contra ataques de inyección de contenido, con compatibilidad elevada entre los exploradores modernos.

## Nuevas API en EdgeHTML 18

Consulte la lista completa de las API nuevas en EdgeHTML 18. Se muestran en el formato de [nombre de interfaz]. [nombre de la API].

> [!NOTE] 
> A pesar de que las siguientes API están expuestas en el DOM, el comportamiento end-to-end de algunos puede estar en desarrollo y estar oculto detrás de una marca experimental. Consulta el [Estado de la plataforma de Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status/) para la compatibilidad de características de Word oficial.

<iframe height='580' scrolling='no' title='Nuevas API en EdgeHTML 18' src='//codepen.io/MSEdgeDev/embed/5d7be9404d82575162b486e79d0dd58f
/?height=608&theme-id=23401&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulta las <a href='https://codepen.io/MSEdgeDev/pen/5d7be9404d82575162b486e79d0dd58f'> nuevas API de Pen en EdgeHTML 18 de </a> MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='https://codepen.io'> CodePen </a> .</iframe>

## Versiones anteriores de EdgeHTML

[EdgeHTML 13/Windows compilación 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows compilación 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)

[EdgeHTML 15/Windows compilación 15063 (4/2017)](https://aka.ms/devguide_edgehtml_15)

[EdgeHTML 16/Windows compilación 16299 (10/2017)](https://aka.ms/devguide_edgehtml_16)

[EdgeHTML 17/Windows compilación 17134 (04/2018)](https://aka.ms/devguide_edgehtml_17)

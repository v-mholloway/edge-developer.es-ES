---
description: Asegúrate de que tu PWA proporciona una gran experiencia para Xbox
title: Aplicaciones web progresivas para Xbox One
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, UWP, Xbox, Xbox One, TVJS
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3ac4174c821f221d6d666a25880867275ca5cbd5
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397674"
---
# <a name="progressive-web-apps-for-xbox-one"></a>Aplicaciones web progresivas para Xbox One  

Puedes extender una aplicación web y hacer que esté disponible como una aplicación de Xbox One a través de Microsoft Store mientras sigues usando los marcos existentes, la red CDN y el back-end del servidor.  Y al igual que todas las aplicaciones de la Plataforma universal de Windows \(UWP\), las aplicaciones web progresivas \(PWAs\) que se ejecutan en Xbox One también pueden llamar a las API nativas de Windows 10.  Ya hay varias PWA disponibles para Xbox One, especialmente en la categoría de aplicaciones [de reproducción multimedia.](#media-pwas-on-xbox)  

En su mayoría, puedes empaquetar tu PWA para Xbox One de la misma manera que lo harías con [Windows,](./windows-features.md)usando las herramientas del Generador de [PWA](https://www.pwabuilder.com) o el IDE de [Visual Studio](https://visualstudio.microsoft.com/vs) para generar el archivo necesario para ejecutar tu PWA como una aplicación `appxmanifest` para UWP.  Sin embargo, hay varias diferencias clave que esta guía le guiará.  

## <a name="deploying-and-testing-pwas-on-xbox"></a>Implementación y prueba de PWA en Xbox  

Para empezar, sigue estos [pasos para activar el modo para *desarrolladores de Xbox One*](/windows/uwp/xbox-apps/devkit-activation).  Con el modo de desarrollador activado, [configura Device Portal para Xbox *para* ](/windows/uwp/debug-test-perf/device-portal-xbox) obtener acceso remoto a tu Xbox desde el explorador en el entorno de desarrollo.  

Ahora estás listo para implementar la aplicación para pruebas con PWA Builder o Visual Studio.  

### <a name="option-1--pwa-builder"></a>Opción 1: PWA Builder  

[PWA Builder](https://www.pwabuilder.com) es una Node.js que puedes instalar desde Node Administrador de paquetes \(NPM\).  Usa los metadatos de tu sitio web para generar aplicaciones hospedadas nativas en Android, iOS y Windows.  Si el sitio ya tiene un [manifiesto de aplicación web,](https://developer.mozilla.org/docs/Web/Manifest)PWA Builder lo usará para generar paquetes de instalación específicos de la plataforma.  De lo contrario, PWA Builder generará un archivo `manifest.json` básico en función de las características del sitio.  

#### <a name="requirements"></a>Requisitos  

*   [Node.js](https://nodejs.org), que incluye NPM.  

#### <a name="setup"></a>Programa de instalación  

1.  Abra un símbolo del sistema node para instalar PWA Builder:  
    
    ```shell
    npm install pwabuilder --global
    ```  
    
1.  Ejecute el Generador de PWA en la dirección URL del sitio web:  
    
    ```shell
    pwabuilder https://example.com/ -windows10
    ```  
    
    La *marca -windows10* limita la generación de paquetes a Windows 10 \(UWP\).  Puedes omitirlo para generar paquetes en todas las plataformas compatibles, incluidos iOS y Android.  Consulta los [documentos del Generador de PWA](https://docs.pwabuilder.com) para obtener más información.  
    
1.  Desde el Portal de dispositivos para [Xbox,](/windows/uwp/debug-test-perf/device-portal-xbox)ve a Inicio Mis juegos & **** Aplicaciones Agregar , elige la opción para cargar archivos sueltos y selecciona la carpeta de manifiesto de la aplicación de Windows  >  ****  >  **** 10 **** generada por PWA Builder en el directorio actual.  
1.  Pase por el asistente para completar el proceso de instalación.  Una vez instalado.  podrás ver e iniciar tu PWA desde el panel de Xbox One.  
    
### <a name="option-2--visual-studio"></a>Opción 2: Visual Studio  

La comunidad gratuita de [Visual Studio 2017](https://visualstudio.microsoft.com/vs/community) incluye herramientas para desarrolladores de Windows 10, plantillas de aplicaciones universales, un editor de código, un eficaz depurador, emuladores de Windows Mobile, compatibilidad con idiomas enriquecidos y mucho más, todo listo para usarse en producción.  Las [versiones Profesional y Enterprise](https://visualstudio.microsoft.com/vs/compare) proporcionan aún más características.  

#### <a name="requirements"></a>Requisitos  

*   [Visual Studio 2017:](https://visualstudio.microsoft.com/vs)Cualquier versión, incluida la edición gratuita de la Comunidad.  
*   [SDK de Windows 10:](/windows/uwp/xbox-apps/development-environment-setup)seleccione este componente opcional en el instalador Visual Studio 2017.  

#### <a name="setup"></a>Programa de instalación  

1.  Sigue los pasos para [configurar y ejecutar tu PWA como una aplicación universal de Windows](./windows-features.md#set-up-and-run-your-universal-windows-app).  Con esto, tendrás una aplicación de Windows 10 totalmente funcional capaz de acceder a las API universales de Windows.  
1.  Ahora puedes implementar y depurar tu PWA \(como una aplicación para UWP\) en Xbox One \(como con cualquier otro dispositivo remoto de Windows 10\) mediante el depurador remoto Visual Studio [.](/visualstudio/debugger/run-windows-store-apps-on-a-remote-machine?view=vs-2017&preserve-view=true
)  Como alternativa, puedes instalar tu PWA mediante [el Portal de dispositivos para Xbox](/windows/uwp/debug-test-perf/device-portal-xbox) mediante los siguientes pasos.  
1.  Desde el Portal de dispositivos para Xbox, ve a Inicio Mis juegos ****  >  **\& aplicaciones**Agregar , elige la opción para cargar El paquete de aplicaciones  >  **** **y dependencias**.  
1.  Vaya a la carpeta del paquete que generó para la aplicación en el paso 1 y seleccione `.appx` el archivo para cargarlo.  El [archivo .appx](/windows/uwp/packaging/packaging-uwp-apps) es un archivo de paquete de la aplicación para UWP que se puede descargar localmente en cualquier dispositivo con fines de prueba.  
1.  A continuación, pulsa **el** botón Dependencias y selecciona la `dependencies` sub-carpeta de la aplicación y carga cada una de ellas.  Este paso solo es necesario para implementar aplicaciones desde el Portal de dispositivos para Xbox.  Visual Studio proporciona dependencias cuando la depuración remota y la máquina del usuario final ya las tendrán instaladas cuando se entreguen desde Microsoft Store.  
1.  Con el paquete de la aplicación y las dependencias cargadas, haz clic en el botón **Ir** en la sección *Implementar* y se instalará la aplicación.  ¡Estás listo para iniciar la aplicación desde Xbox!  

## <a name="ux-considerations-for-pwas-on-xbox"></a>Consideraciones sobre la experiencia de usuario para las PWA en Xbox  

### <a name="design-for-the-10-foot-experience"></a>Diseño para la "experiencia de 10 pies"  

Xbox One se considera una "experiencia de 10 pies", lo que significa que es probable que los usuarios se sientan a un mínimo de 10 pies de la pantalla.  Por lo tanto, ten en cuenta cómo se puede usar la aplicación a esa distancia en lugar de la experiencia tradicional del explorador web de escritorio con un mouse y un teclado.  Para obtener instrucciones de diseño y experiencia de usuario, consulte [Designing for Xbox and TV](/windows/uwp/design/devices/designing-for-tv).  

### <a name="understand-the-tv-safezone"></a>Comprender el "TV SafeZone"  

Los fabricantes de televisión [aplicarán una zona segura](/windows/uwp/design/devices/designing-for-tv#tv-safe-area) alrededor del contenido que puede recortar la aplicación.  De forma predeterminada, aplicamos un borde seguro alrededor de la aplicación para tener en cuenta esto, pero puedes asegurarte de que la aplicación toma el tamaño de pantalla completa llamando a [setDesiredBoundsMode](/uwp/api/windows.ui.viewmanagement.applicationview.setdesiredboundsmode) y especificando [useCoreWindow](/uwp/api/windows.ui.viewmanagement.applicationviewboundsmode):  

```javascript
var applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
applicationView.setDesiredBoundsMode(Windows.UI.ViewManagement.ApplicationViewBoundsMode.useCoreWindow);
```  

Para obtener más información, consulta la documentación del espacio de [nombres Windows.UI.ViewManagement.](/uwp/api/windows.ui.viewmanagement)  

### <a name="manage-xy-focus-and-navigation"></a>Administrar el foco Y XY y la navegación  

Los métodos de entrada de usuario para Xbox son el controlador para juegos o el control remoto, que usan un sistema de navegación [XY,](/windows/uwp/design/devices/designing-for-tv#xy-focus-navigation-and-interaction)lo que permite al usuario cambiar el foco del control al control moviendo hacia arriba, abajo, izquierda y derecha.  

Por lo tanto, querrás asegurarte de que la aplicación funciona bien con la navegación XY.  Además, asegúrate de deshabilitar [el modo de mouse](/windows/uwp/xbox-apps/how-to-disable-mouse-mode), que está desactivado de forma predeterminada para las aplicaciones para UWP \(y probablemente no sea aplicable a la experiencia de Xbox de la aplicación\).  

El siguiente código desactiva el `mouse` modo y permite que la entrada del mando genere eventos de teclado DOM:  

```javascript
navigator.gamepadInputEmulation = "keyboard";
```  

Como alternativa, puedes especificar , que también desactiva el mouse, no genera eventos de teclado DOM y te permite usar las API estándar de web y/o de bloc de juegos `gamepad` winRT.  

Para habilitar la navegación direccional, consulte la [biblioteca de TVJS,](#tvjs)que se describe a continuación.  

### <a name="tvjs"></a>TVJS  

[TVJS es una colección de bibliotecas auxiliares](https://github.com/Microsoft/TVHelpers) que facilitan la creación de aplicaciones web para el televisor.  Si estás creando una aplicación web hospedada que también se ejecutará en xbox, TVJS puede ayudar a agregar compatibilidad para la navegación *direccional,* así como proporcionar varios controles que facilitan la interacción con el contenido del televisor.  

[La navegación direccional](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) es una característica TVJS que proporciona navegación bidimensional automática dentro de las páginas de la aplicación de TV.  Con él, no es necesario capturar y controlar la navegación dentro de las páginas de la aplicación, ni especificar explícitamente todos los destinos de foco válidos para cada elemento de la interfaz de usuario.  El control automático de focos permite a los usuarios navegar de una manera intuitiva y sólida.  

A medida que el usuario navega por la interfaz de usuario de la aplicación con los botones de dirección del controlador, el algoritmo de enfoque automático examina el conjunto de posibles destinos de foco, determina el siguiente elemento al que desplazarse y, a continuación, establece automáticamente el foco en ese elemento.  Para determinar el siguiente elemento, el algoritmo combina la entrada direccional, el historial de focos pasado y el diseño físico de los elementos de la interfaz de usuario en la página.  

Para habilitar la navegación direccional, incluya la siguiente referencia de script:  

```html
<script src="directionalnavigation-1.0.0.0.js"></script>
```  

De forma predeterminada, `<a>` solo , , , y los elementos se pueden `<button>` `<input>` `<select>` `<textarea>` centrar.  Para habilitar el foco en otros elementos, asígneles una [tabindex válida.](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex)  

```html
<div tabindex="0″>This div is eligible for focus</div>
```  

Consulte la documentación [de DirectionalNavigation](https://github.com/Microsoft/TVHelpers/wiki/DirectionalNavigation) para obtener información sobre cómo cambiar el elemento raíz, establecer el foco inicial, invalidar el siguiente foco, optimizar los controles para el foco, personalizar la entrada.  También hay una serie de otras muestras útiles.

## <a name="media-pwas-on-xbox"></a>PwAs multimedia en Xbox  

Si estás creando un PWA de reproducción multimedia para Xbox One, ten en cuenta las siguientes consideraciones.  

### <a name="encrypted-media-extensions-eme-in-the-browser"></a>Extensiones multimedia cifradas (EME) en el explorador  

El explorador Microsoft Edge en Xbox One no admite extensiones multimedia [cifradas](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) \(EME\).  Si tu PWA multimedia lo usa para la administración de derechos digitales \(DRM\), no podrás ejecutarlo desde el explorador en tu Xbox.  En su lugar, prototipo y pruebe como una aplicación de Xbox One con [PWABuilder o Visual Studio](#deploying-and-testing-pwas-on-xbox), como se describe anteriormente.  También puedes ejecutarlo en el explorador Microsoft Edge en Windows, donde EME es totalmente compatible.  

### <a name="integrating-with-system-media-transport-controls"></a>Integración con controles de transporte de medios del sistema  

Si la aplicación es una aplicación multimedia, es importante que la aplicación responda a los controles multimedia iniciados [](/windows/uwp/audio-video-camera/system-media-transport-controls) por el usuario a través de botones en pantalla, comandos de [voz cortana,](https://support.xbox.com/xbox-one/console/cortana-voice-commands)los controles de transporte multimedia del sistema en el panel de navegación o las aplicaciones [SmartGlass](https://www.microsoft.com/p/xbox-one-smartglass/9wzdncrfhvx2) de [Xbox](https://www.microsoft.com/p/xbox/9wzdncrfjbd8
) y Xbox One en otros dispositivos.  Echa un vistazo al control [MediaPlayer](https://github.com/Microsoft/TVHelpers/wiki/MediaPlayer-Overview) de la [biblioteca DE TVJS,](#tvjs)que se integra automáticamente con estos controles.  Como alternativa, puede integrar manualmente con los controles de transporte de medios [del sistema.](/windows/uwp/audio-video-camera/system-media-transport-controls)  

### <a name="playready-content-encryption"></a>Cifrado de contenido de PlayReady  

En el momento de esta escritura, la compatibilidad con codificación [cbcs](/playready/packaging/content-encryption-modes#support-for-the-cbcs-aes-cbc-encryption-scheme) está limitada al cliente PlayReady para XBox One \(versión 1709 o posterior\).  Si los medios de tu PWA solo admiten cifrado **de cbcs,** ten en cuenta que es probable que la funcionalidad de la aplicación esté limitada \(o completamente no disponible\) en Windows.  

## <a name="see-also"></a>Consulte también  

[Vídeo de South Ridge:](https://github.com/Microsoft/uwp-experiences/tree/master/apps/video)una aplicación de vídeo de ejemplo para Xbox creada React.js y hospedada en un servidor web.  

[Diseño para Xbox](/windows/uwp/design/devices/designing-for-tv)y TV: diseña tu aplicación de la Plataforma universal de Windows \(UWP\) para que se vea bien y funcione bien en Xbox One y en las pantallas de televisión.  

[Procedimientos recomendados de Xbox:](/windows/uwp/xbox-apps/tailoring-for-xbox)siga estos procedimientos recomendados para adaptar la aplicación a Xbox One.  

[PWAs en microsoft store:](./microsoft-store.md)así es cómo \(y por qué?\) enviar tu PWA a Microsoft Store.  

[UWP en Xbox One:](/windows/uwp/xbox-apps/index)guía completa para el desarrollo de aplicaciones para UWP para Xbox One.  

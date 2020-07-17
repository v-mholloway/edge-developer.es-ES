---
description: Asegúrate de que tu PWA ofrezca una excelente experiencia para Xbox
title: Aplicaciones web progresivas para Xbox One
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, UWP, Xbox, Xbox One, TVJS
ms.openlocfilehash: dfa2b2d252bb788c0010017de57ab147d407c5f7
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882856"
---
# Aplicaciones web progresivas para Xbox One  

Puede extender una aplicación web y hacer que esté disponible como una aplicación de Xbox One a través de Microsoft Store y seguir usando los marcos, la CDN y el back-end existentes.  Y, al igual que todas las aplicaciones de la plataforma universal de Windows (UWP), las aplicaciones web progresivas (PWAs) que se ejecutan en Xbox One también pueden llamar a las API de Windows 10 nativas.  Ya hay una serie de PWAs disponibles para Xbox One, especialmente en la categoría de aplicaciones de [reproducción multimedia](#media-pwas-on-xbox).  

En la mayoría de los casos, puedes empaquetar tu PWA para Xbox One de la [misma manera que lo harías para Windows](./windows-features.md), usando las herramientas del [creador de PWA](https://www.pwabuilder.com/) o el IDE de [Visual Studio](https://visualstudio.microsoft.com/vs/) para generar el archivo *appxmanifest* necesario para ejecutar PWA como una aplicación para UWP. Sin embargo, existen varias diferencias clave que le guiarán en esta guía.

## Implementación y prueba de PWAs en Xbox

Para empezar, sigue estos [pasos para activar el *modo de desarrollador de Xbox One* ](/windows/uwp/xbox-apps/devkit-activation) . Con el modo de desarrollador activado, [configura *portal de dispositivos para Xbox* ](/windows/uwp/debug-test-perf/device-portal-xbox) para obtener acceso remoto a tu Xbox desde el explorador de tu entorno de desarrollo.

Ahora ya está listo para implementar la aplicación para realizar pruebas con el *creador de PWA* o con *Visual Studio*.

### Opción 1: creador de PWA

El [creador de PWA](https://www.pwabuilder.com/) es una aplicación de Node.js que puede instalar desde el administrador de paquetes de nodos (NPM). Usa los metadatos de tu sitio web para generar aplicaciones nativas hospedadas en Android, iOS y Windows. Si su sitio ya tiene un [manifiesto de aplicación web](https://developer.mozilla.org/docs/Web/Manifest), el creador de PWA lo usará para generar paquetes de instalación específicos de la plataforma. En caso contrario, el creador de PWA generará una *manifest.jsbásica en* el archivo basándose en las características del sitio.

#### Requisitos
 - [Node.js](https://nodejs.org/en/), que incluye NPM.

#### Programa de instalación

1. Abra un símbolo del sistema de nodo para instalar el creador de PWA:

    ```
    npm install pwabuilder --global
    ```

2. Ejecute el creador de PWA en la dirección URL de su sitio web:

    ```
    pwabuilder https://example.com/ -windows10
    ```

    La marca *-windows10* limita la generación de paquetes a Windows 10 (UWP). Puede omitirlo para generar paquetes en todas las plataformas compatibles, entre las que se incluyen iOS y Android. Para obtener más información, consulta los [documentos del creador de PWA](https://docs.pwabuilder.com/) .

3. Desde [Device portal para Xbox](/windows/uwp/debug-test-perf/device-portal-xbox), vaya a **casa**  >  **mi juego & aplicaciones**  >  **Agregar**, elija la opción para *cargar archivos sueltos*y seleccione la carpeta del manifiesto de la aplicación Windows 10 generada por el creador de PWA en el directorio actual.

4. Siga los pasos del Asistente para completar el proceso de instalación. Una vez instalado. podrás ver e iniciar tu PWA desde el panel de Xbox One.


### Opción 2: Visual Studio

La comunidad completa gratuita de [Visual Studio Community 2017](https://visualstudio.microsoft.com/vs/community/) incluye herramientas para desarrolladores de Windows 10, plantillas de aplicaciones universales, un editor de código, un depurador eficaz, emuladores de Windows Mobile, compatibilidad con lenguajes enriquecidos y mucho más, todo listo para usarse en producción. Las versiones [ *Professional* y *Enterprise* ](https://visualstudio.microsoft.com/vs/compare/) proporcionan aún más características.

#### Requisitos

 - [**Visual Studio 2017**](https://visualstudio.microsoft.com/vs/
): cualquier versión, incluida la edición gratuita de la *comunidad* .
 - [**SDK de Windows 10**](/windows/uwp/xbox-apps/development-environment-setup): Seleccione este componente opcional en el *instalador de Visual Studio 2017*.

#### Programa de instalación

1. Siga los pasos para [configurar y ejecutar PWA como una aplicación universal de Windows](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#set-up-and-run-your-universal-windows-app). Con esto, tendrás una aplicación de Windows 10 totalmente funcional capaz de acceder a las API de Windows universales.

2. Ahora puedes implementar y depurar tu PWA (como una aplicación para UWP) en la Xbox One (como en cualquier otro dispositivo remoto de Windows 10) mediante el [Depurador remoto de Visual Studio](/visualstudio/debugger/run-windows-store-apps-on-a-remote-machine?view=vs-2017
). Como alternativa, puedes instalar tu PWA con [Device portal para Xbox](/windows/uwp/debug-test-perf/device-portal-xbox) siguiendo los pasos que se indican a continuación.

3. Desde Device portal para Xbox, vaya a Inicio > mis juegos & aplicaciones > agregar, elija la opción para cargar el *paquete de la aplicación y las dependencias*.

4. Vaya a la carpeta del paquete que ha generado para la aplicación en el paso 1 y seleccione el archivo *. appx* para cargarlo. El [archivo *. appx* ](/windows/uwp/packaging/packaging-uwp-apps) es un archivo de paquete de la aplicación para UWP que se puede usar localmente en cualquier dispositivo para realizar pruebas.

5. Después, pulse el botón **dependencias** y seleccione la subcarpeta de *dependencias* de la aplicación y cargue cada una de ellas. Este paso solo es necesario para implementar aplicaciones desde Device portal para Xbox. Visual Studio proporciona dependencias cuando la depuración remota y el equipo del usuario final ya tendrán estas aplicaciones instaladas cuando se entreguen desde Microsoft Store.

6. Con el paquete de la aplicación y las dependencias cargadas, haga clic en el botón **ir** en la sección *implementar* y se instalará la aplicación. Ya puedes iniciar tu aplicación desde Xbox.

## Consideraciones sobre la experiencia del usuario para PWAs en Xbox

### Diseño para la "experiencia de 3 metros"

Xbox One se considera una "experiencia de 3 pies", lo que significa que es probable que los usuarios se encuentren con un mínimo de 10 metros de distancia de la pantalla. Como tal, ten en cuenta que tu aplicación podría usarse a esa distancia en lugar de la experiencia de explorador Web de escritorio tradicional con un mouse y un teclado. Para obtener instrucciones sobre el diseño y la experiencia del usuario, consulta [diseño para Xbox y TV](/windows/uwp/design/devices/designing-for-tv).

### Comprender el "TV SafeZone"

Los fabricantes de televisión aplicarán una ["zona segura"](/windows/uwp/design/devices/designing-for-tv#tv-safe-area) a todo el contenido que puede recortar la aplicación. De forma predeterminada, aplicamos un borde seguro de la aplicación para que lo tenga en cuenta, pero puede asegurarse de que la aplicación toma el tamaño de pantalla completa al llamar [`setDesiredBoundsMode`](/uwp/api/windows.ui.viewmanagement.applicationview.setdesiredboundsmode) y especificar [`useCoreWindow`](/uwp/api/windows.ui.viewmanagement.applicationviewboundsmode) :

```JavaScript
var applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
applicationView.setDesiredBoundsMode(Windows.UI.ViewManagement.ApplicationViewBoundsMode.useCoreWindow);
```

Para obtener más información, consulta la [`Windows.UI.ViewManagement`](/uwp/api/windows.ui.viewmanagement) documentación del espacio de nombres.

### Administrar el foco XY y la navegación

Los métodos de entrada de usuario para Xbox son el controlador para juegos o el control remoto, que usan un [sistema de navegación XY](/windows/uwp/design/devices/designing-for-tv#xy-focus-navigation-and-interaction), lo que permite al usuario desplazar el foco de control a control desplazándose hacia arriba, abajo, izquierda y derecha.

Por lo tanto, querrás asegurarte de que tu aplicación funcione bien con la navegación XY. Además, asegúrate de [deshabilitar el *modo de mouse*](/windows/uwp/xbox-apps/how-to-disable-mouse-mode), que está activado de forma predeterminada para las aplicaciones para UWP (y probablemente no es aplicable a la experiencia de Xbox de la aplicación).

El siguiente código desactiva el `mouse` modo y habilita la entrada del controlador para generar eventos de teclado de Dom:

```JavaScript
navigator.gamepadInputEmulation = "keyboard";
```

Como alternativa, puedes especificar `gamepad` , que también desactiva el mouse, no genera eventos de teclado de Dom y te permite usar las API estándar del controlador para juegos WinRT o web estándar.

Para habilitar la navegación direccional, consulte la [biblioteca TVJS](#tvjs), que se describe a continuación.

### TVJS

[TVJS es una colección de bibliotecas auxiliares](https://github.com/Microsoft/TVHelpers) que facilitan la creación de aplicaciones web para el televisor. Si va a crear una aplicación web hospedada que también se ejecutará en la Xbox, TVJS puede ayudar a agregar compatibilidad con la *navegación direccional*, además de proporcionar varios controles que faciliten la interacción con el contenido del televisor.

La [navegación direccional](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) es una característica de TVJS que proporciona navegación bidimensional automática dentro de las páginas de la aplicación de TV. Con él, no hay necesidad de interceptar y controlar la navegación dentro de las páginas de la aplicación, ni de especificar de forma explícita todos los destinos de foco válidos para cada elemento de la interfaz de usuario. El manejo automático de focos permite a los usuarios navegar en un modo intuitivo y intuitivo.

A medida que el usuario navega por la interfaz de usuario de la aplicación con los botones de dirección del controlador, el algoritmo de foco automático busca el conjunto de posibles destinos de foco, determina el elemento siguiente al que se va a mover y, a continuación, establece el foco en ese elemento. Para determinar el elemento siguiente, el algoritmo combina la entrada direccional, el historial de foco Past y el diseño físico de los elementos de la interfaz de usuario en la página.

Para habilitar la navegación direccional, incluya la siguiente referencia de script:

```HTML
<script src="directionalnavigation-1.0.0.0.js"></script>
```

De forma predeterminada, `<a>` los elementos solo,,, `<button>` `<input>` y pueden recibir el `<select>` `<textarea>` foco. Para habilitar el foco en otros elementos, asígneles un [TabIndex](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex)válido.

```HTML
<div tabindex="0″>This div is eligible for focus</div>
```

Consulte la documentación de [DirectionalNavigation](https://github.com/Microsoft/TVHelpers/wiki/DirectionalNavigation) para obtener información sobre cómo cambiar el elemento raíz, establecer el foco inicial, invalidar el próximo enfoque, optimizar los controles para el foco, personalizar la entrada. También existen otras muestras útiles.

## PWAs multimedia en Xbox

Si vas a crear una reproducción de contenido multimedia de PWA para Xbox One, ten en cuenta las siguientes consideraciones:

### Extensiones de medios cifrados (EME) en el explorador

El explorador Microsoft Edge en Xbox One no es compatible con [las extensiones de medios cifrados](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API) (EME). Si su media PWA la usa para la administración de derechos digitales (DRM), no podrá ejecutarla desde el explorador en la Xbox. En su lugar, puede crear prototipos y probarlos como una [aplicación de Xbox One con PWABuilder o Visual Studio](#deploying-and-testing-pwas-on-xbox), tal y como se describe anteriormente. También puede ejecutarlo en el explorador Microsoft Edge en Windows, donde EME es totalmente compatible.

### Integración con controles de transporte de contenido multimedia del sistema

Si la aplicación es una aplicación multimedia, es importante que la aplicación responda a los controles de medios iniciados por el usuario a través de los botones en pantalla, los [comandos de voz Cortana](https://support.xbox.com/xbox-one/console/cortana-voice-commands), los [controles de transporte multimedia del sistema](/windows/uwp/audio-video-camera/system-media-transport-controls) del panel de navegación o las aplicaciones de [Xbox](https://www.microsoft.com/p/xbox/9wzdncrfjbd8
) y [Xbox One SmartGlass](https://www.microsoft.com/p/xbox-one-smartglass/9wzdncrfhvx2) en otros dispositivos. Eche un vistazo al control [MediaPlayer](https://github.com/Microsoft/TVHelpers/wiki/MediaPlayer-Overview) de la [biblioteca TVJS](#tvjs), que se integra automáticamente con estos controles. Como alternativa, puede integrar manualmente [con los controles de transporte de contenido multimedia del sistema](https://msdn.microsoft.com/windows/uwp/audio-video-camera/system-media-transport-controls).

### Cifrado de contenido de PlayReady

En el momento de escribir este artículo, la [ `cbcs` compatibilidad con la codificación se limita](/playready/packaging/content-encryption-modes#support-for-the-cbcs-aes-cbc-encryption-scheme) al cliente PlayReady para Xbox one (versión 1709 o superior). Si el elemento multimedia de su PWA solo admite el cifrado de *CBCS* , tenga en cuenta que la funcionalidad de la aplicación probablemente será limitada (o totalmente no disponible) en Windows.



## Consulta también
[Vídeo de cresta de sur](https://github.com/Microsoft/uwp-experiences/tree/master/apps/video): una aplicación de vídeo de ejemplo para Xbox creada con React.js y hospedada en un servidor Web.

[Diseñar para Xbox y TV](/windows/uwp/design/devices/designing-for-tv): diseña tu aplicación para la plataforma universal de Windows (UWP) para que se vea bien y funcione correctamente en Xbox One y en las pantallas de televisión.

[Prácticas recomendadas de Xbox](/windows/uwp/xbox-apps/tailoring-for-xbox): siga estos procedimientos recomendados para personalizar la aplicación para Xbox One.

[PWAs en Microsoft Store](/microsoft-edge/progressive-web-apps-edgehtml/microsoft-store): aquí se explica cómo (y por qué) enviar su PWA a Microsoft Store.

[UWP en Xbox One](/windows/uwp/xbox-apps/): guía completa para el desarrollo de aplicaciones para UWP para Xbox One.

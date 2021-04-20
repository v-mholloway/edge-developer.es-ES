---
description: Las últimas características experimentales de Microsoft Edge para aplicaciones web
title: Características experimentales | Aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 641b6fd5185e7f96289c1de6482764979ee0981d
ms.sourcegitcommit: 9cc54ba3e731ecc8b713c3cf215018848f7405b9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/19/2021
ms.locfileid: "11496757"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a>Características experimentales en aplicaciones web progresivas (PWA)  

Microsoft Edge proporciona acceso a características experimentales que aún están en desarrollo.  Para determinar si cada característica está lista y cuándo liberar cada una, pruebe y [proporcione comentarios](#providing-feedback-on-experimental-features).  

Las características experimentales están disponibles en todos los canales de Microsoft Edge, pero las últimas características experimentales solo están disponibles en el canal de Microsoft Edge Canary.  

## <a name="turn-on-experimental-features"></a>Activar características experimentales  

Para activar las características experimentales \(or off\) en Microsoft Edge, siga estos pasos.  
  
1.  Abra Microsoft Edge.   
    
    > [!NOTE]
    > Asegúrese de usar una versión de Microsoft Edge que tenga el experimento enumerado en este artículo.  Vaya a [Características experimentales](#features-that-are-available-to-test).  
    
1.  Vaya a `edge://flags` .  
1.  Vaya al experimento correspondiente.  
1.  Elija el menú desplegable junto a la descripción del experimento y elija `Enabled` .  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Elija Habilitado para activar un experimento" lightbox="../media/turn-on-experimental-flag.png":::
       Elija **Habilitado** para activar un experimento  
    :::image-end:::  
    
    > [!NOTE]
    > Cada experimento suele tener un menú desplegable para elegir los siguientes valores.  Si una característica experimental no tiene una entrada en **Experimentos,** se proporcionan instrucciones para iniciar Microsoft Edge con esa característica mediante la línea de comandos.
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  Reiniciar MicrosoftEdge.  
    
### <a name="origin-trials"></a>Pruebas de origen  

Microsoft Edge a veces usa pruebas de origen para probar características para dominios o sitios web específicos.  Es posible que desee usar una versión de prueba de origen para su sitio web para aplicar una característica específica.  Si es propietario de un sitio web, puede inscribirse en una prueba de origen.  Una versión de prueba de origen proporciona características a un porcentaje de usuarios de Microsoft Edge que visitan su sitio web.

Para obtener más información acerca de las pruebas de Origen, vaya a [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].  
    
> [!NOTE]
> Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.  Para desactivar una característica experimental, vaya a [Activar características experimentales,](#turn-on-experimental-features)vaya al experimento y, a continuación, elija `Disabled` .  

## <a name="features-that-are-available-to-test"></a>Características que están disponibles para probar  

En la siguiente lista se describen las nuevas características experimentales de la aplicación web que están disponibles para probar y validar en Microsoft Edge.  

| Característica | Versión de Microsoft Edge | Plataforma |  
|:--- |:--- |:--- |  
| [Administración del protocolo URI](#uri-protocol-handling) | 91 o posterior | Windows y Linux |    
| [Administración de vínculos URL](#url-link-handling) | 91 o posterior | Windows|
| [Superposición de controles de ventana para aplicaciones de escritorio](#window-controls-overlay-for-installed-desktop-web-apps) | 91 o posterior | Windows 10|   
| [Ejecutar en inicio de sesión del sistema operativo](#run-on-os-login) | 88 o posterior | Todos |  
| [Accesos directos](#shortcuts) | 87 o posterior | Todos |  
| [Administración de archivos](#file-handling) | 83 o posterior | Todo el escritorio |  


## <a name="uri-protocol-handling"></a>Administración del protocolo URI  

Se puede usar un identificador uniforme de recursos \(URI\) para definir algo más que vínculos a páginas web y contenido web mediante el protocolo HTTP o FTP.  Los URI pueden usarse para describir vínculos a todo lo que codifique en un esquema.  Por ejemplo, el protocolo se usa para describir un vínculo de correo electrónico y el sistema operativo \(OS\) o el explorador decide qué página web o aplicación debe controlar `mailto://` ese protocolo.  

Para obtener más información acerca de la compatibilidad basada en explorador existente, vaya a [Controladores de protocolo basados][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]en web.  

Esta característica le permite completar las siguientes acciones.  

*   Registrar tu PWA con el sistema operativo host mediante el manifiesto de la aplicación web
*   Declarar que una PWA controla un protocolo URI específico  
     
Después de registrar un PWA como controlador de protocolo, cuando un usuario elige un hipervínculo con un esquema específico, como un explorador o una aplicación nativa, el sistema operativo activa la PWA registrada y recibe el `mailto://` `web+music://` URI.  

Esta característica requiere que actualices el manifiesto de la aplicación web para incluir una matriz, en la `protocol_handlers` matriz debes especificar dos campos:  

*   `protocol`: el protocolo para controlar la solicitud, por ejemplo `mailto` o `web+jngl` .  
*   `url`: URI HTTPS en el ámbito de la aplicación que controla el protocolo.  En el futuro, el URI a partir del esquema de controladores de protocolo está planeado para reemplazar el `%s` token.  
    
Actualice el manifiesto para admitir el protocolo que desea registrar.  Después de activar esta característica, Microsoft Edge completa las siguientes acciones.  

1.  Detecta cambios en el manifiesto  
1.  Registra la aplicación para el protocolo  
    
Si más de una aplicación registra un protocolo, se muestra al usuario un mensaje.  El usuario elige la aplicación adecuada de la lista presentada por el sistema operativo o el explorador.  

Para obtener una vista previa del control de protocolos en Microsoft Edge en Windows, vaya a Activar características [experimentales](#turn-on-experimental-features) y active El control del **protocolo PWA de escritorio.**  

Para obtener más información acerca de la versión de prueba de origen que se está ejecutando para los controladores de protocolo, vaya a Registrar para el registro del controlador de [protocolo de aplicación web.][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]  

### <a name="example-manifest"></a>Manifiesto de ejemplo

En este ejemplo, un manifiesto de aplicación web declara que la aplicación debe registrarse para controlar los protocolos `web+jngl` y `web+jnglstore` .

```json
{
  "name": "Jungle",
  "description": "A plant encyclopedia",
  "protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ],
  "icons": [
    {
      "src": "images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
  ],
  "background_color": "#007f87",

  "display": "standalone",
  "start_url": "/",
}
```  
 
## <a name="url-link-handling"></a>Administración de vínculos URL  

Un localizador uniforme de recursos \(URL\) es un tipo de URI.  Crea una experiencia más atractiva cuando las aplicaciones web progresivas \(PWAs\) se registren como controladores para URI https.  Las PWA pueden solicitar que se inicien cuando se activen los URI asociados.  Por ejemplo, si un usuario elige un vínculo a un artículo de noticias de un mensaje de correo electrónico.  Se inicia automáticamente un PWA asociado para mostrar artículos de noticias para controlar la activación del vínculo.  

Esta característica te permite registrar un PWA con el explorador mediante el manifiesto de la aplicación web y declarar que el explorador controla vínculos específicos.  Para registrar un PWA con el explorador, agregue el miembro `url_handlers` opcional al archivo de manifiesto.  El `url_handlers` miembro es un que agrupa los orígenes de los URI que la aplicación desea `object[]` controlar.  

El explorador valida el control de vínculos mediante un `web-app-origin-association` archivo JSON que se encuentra en el origen.  El archivo de origen afina aún más las rutas de acceso incluidas o excluidas en el origen.  Para obtener instrucciones detalladas sobre cómo probar el controlador de direcciones URL, vaya a [PWA como controladores de dirección URL][GithubWicgPwaUrlHandlerBlobMainExplainerMd].  

Para obtener una vista previa del control de vínculos url en Microsoft Edge en Windows, vaya a Activar características [experimentales](#turn-on-experimental-features) y active Control de **direcciones URL de PWA de escritorio.**  

### <a name="example-of-the-url_handlers-in-the-manifest"></a>Ejemplo de la url_handlers en el manifiesto  

El siguiente fragmento de código es un manifiesto de aplicación web de ejemplo con el `url_handlers` miembro.  

```json 
{
    "name": "Contoso Business App",
    "display": "standalone",
    "icons": [
        {
            "src": "images/icons-144.png",
            "type": "image/png",
            "sizes": "144x144"
        }
    ],
    "capture_links": "existing_client_event",
    "url_handlers" : [
        {
            "origin": "https://contoso.com"
        },
        {
            "origin": "https://conto.so"
        },
        {
            "origin": "https://*.contoso.com"
        }
    ]
}
```  

Un PWA coincide con un URI para el control de direcciones URL si el URI coincide con una de las cadenas de origen y el explorador valida que el origen acepta permitir que esta aplicación controle `url_handlers` dicho URI.  

El miembro contiene un origen que abarca el ámbito y otros orígenes no relacionados `url_handlers` de la PWA solicitante.  No restringir los URI al mismo ámbito o dominio que el PWA solicitante permite usar nombres de dominio diferentes para el mismo contenido, pero controlarlos con el mismo PWA.  

#### <a name="wildcard-matching"></a>Coincidencia de caracteres comodín  

Use el carácter comodín \( `*` \) para que coincida con uno o más caracteres.  

Se usa un prefijo comodín en las cadenas de origen del `url_handlers` miembro para que coincidan con los subdominios diferentes.  El prefijo debe ser `*.` para este uso.  El `https` esquema se asume cuando se usa un prefijo comodín.  

Por ejemplo, el `url_handlers` valor de miembro se establece en `*.contoso.com` coincidencias y , pero no `tenant.contoso.com` coincide con `www.tenant.contoso.com` `contoso.com` .  

## <a name="window-controls-overlay-for-installed-desktop-web-apps"></a>Superposición de controles de ventana para aplicaciones web de escritorio instaladas  

Para crear una barra de título envolvente como una aplicación **** nativa para la aplicación web instalada en el escritorio, la característica Superposición de controles de ventana completa las siguientes acciones.  
    
1.  Quita la barra de título reservada del sistema.  Normalmente abarca el ancho del marco de cliente.  
1.  Lo reemplaza por una superposición.  Contiene solo los controles de ventana necesarios para que un usuario controle la propia ventana.  
    
Después de proporcionar una superposición, todo el área de cliente web está disponible para su uso.  Esta característica incluye una actualización de manifiesto.  Proporciona formas de determinar el tamaño y la posición de la superposición para ayudarle a organizar el contenido.  

Para obtener una vista previa de las superposiciones de controles de ventana en Microsoft Edge para Windows 10, vaya a Activar características [experimentales](#turn-on-experimental-features) y vaya a Escritorio **PWA Window Controls Overlay**.   

### <a name="examples-of-title-bar-area-customization"></a>Ejemplos de personalización del área de la barra de título  

Esta característica se basa en la capacidad de las aplicaciones nativas para personalizar la barra de título.  Puedes personalizar una barra de título para las notificaciones o acciones importantes de la aplicación.  Revise los siguientes ejemplos para Microsoft Visual Studio Code y Microsoft Teams.  

#### <a name="visual-studio-code"></a>Visual Studio Code  

Microsoft Visual Studio Code es un editor popular basado en Electron que se incluye en varias plataformas de escritorio.  

En el ejemplo siguiente se muestra cómo Visual Studio Code usa la barra de título para maximizar el estado real de pantalla disponible para incluir el nombre de archivo actual y la estructura de menús de nivel superior en la barra de título.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="Un ejemplo de la barra de título en Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   Un ejemplo de la barra de título en Visual Studio Code  
:::image-end:::  

#### <a name="microsoft-teams"></a>Microsoft Teams  

La herramienta de comunicación y colaboración en el lugar de trabajo Microsoft Teams también se ha creado con Electron y está disponible en varias plataformas de escritorio.  En el siguiente ejemplo, Microsoft Teams muestra y `back` `forward` botones de navegación, un cuadro de búsqueda y controles de perfil de usuario.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="Un ejemplo de la barra de título en Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   Un ejemplo de la barra de título en Microsoft Teams  
:::image-end:::  

### <a name="overlay-window-controls-on-a-frameless-window"></a>Superponer controles de ventana en una ventana sin marco  

Para maximizar el área direccionable para el contenido web, el explorador crea una ventana sin marco.  Una ventana sin marco quita toda la interfaz de usuario del explorador, excepto los controles de ventana proporcionados como una superposición.  La superposición de controles de ventana permite a los usuarios minimizar, maximizar, restaurar y cerrar la aplicación.  También proporciona acceso a controles de explorador relevantes mediante el menú de la aplicación web.  Para los exploradores basados en Chromium, la superposición incluye los siguientes controles.  

*   Una región arrastrable con el mismo ancho y alto de cada uno de los botones de control de ventana  
*   El **botón Configuración y más** \(...\)  
*   Los botones de control de ventana minimizan, maximizan, restauran y cierran  
    
Además de los controles enumerados anteriormente, la interfaz de usuario mostrada en la superposición cambia de tamaño dinámicamente en los siguientes escenarios.  

*   Cuando se inicia una aplicación web instalada, el origen de la página web se muestra a la izquierda del menú **Configuración** y más \(...\) durante unos segundos y, a continuación, desaparece.  
*   Si un usuario interactúa con **** una extensión mediante el menú Configuración y más \(...\), el icono de la extensión se muestra en la superposición a la izquierda del menú de tres puntos.  Después de salir de cualquier cuadro de diálogo de extensión, el icono se quita de la superposición.  
    
| Dirección del idioma | Ubicación de superposición | Detalles |  
|:--- |:--- |:--- |  
| De izquierda a derecha \(LTR\) | Superior izquierda del área de cliente | Los controles se voltearán |  
| De derecha a izquierda \(RTL\) | Esquina superior derecha del área de cliente |  |  

> [!IMPORTANT]
> La superposición siempre está en la parte superior del índice Z del contenido web y acepta todas las entradas del usuario sin pasarla al contenido web.  

### <a name="working-around-the-window-controls-overlay"></a>Trabajar alrededor de la superposición de controles de ventana  

El contenido web debe tener en cuenta el área reservada para la superposición de controles.  Asegúrese de que el área reservada no espera la interacción del usuario.  Consulta al explorador el rectángulo de límite y la visibilidad de la superposición de controles.  La información se proporciona a través de las API de JavaScript y las variables de entorno CSS.  

#### <a name="javascript-apis"></a>API de JavaScript  

Un nuevo objeto de la propiedad permite consultar el `windowControlsOverlay` rectángulo delimitador de la `window.navigator` superposición de controles.  

El `windowControlsOverlay` objeto tiene los dos objetos siguientes.  

*   `getBoundingClientRect()` devuelve un `DOMRect` objeto.  El `DOMRect` objeto representa el área debajo de la superposición de controles de ventana.  
*   `visible` es un valor booleano que indica que la superposición de controles se representa y se muestra.  
    
> [!IMPORTANT]
> Por motivos de privacidad, los elementos del `windowControlsOverlay` contenido web no son `iframe` accesibles.  

Cada vez que se cambia el tamaño de la superposición, se ejecuta un evento en el objeto para notificar al `geometrychange` cliente que recalcula el diseño de `navigator.windowControlsOverlay` contenido.  El diseño de contenido recalculado se basa en el nuevo rectángulo delimitador de la superposición.  

#### <a name="css-environment-variables"></a>Variables de entorno CSS  

Además de la API de JavaScript, puede usar CSS para consultar el rectángulo delimitador de la superposición de controles.  Use las siguientes cuatro nuevas variables de entorno CSS para realizar la consulta.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### <a name="define-draggable-regions-in-web-content"></a>Definir regiones arrastrables en contenido web  

Los usuarios esperan agarrar y arrastrar la región superior de una ventana.  Para dar cabida a la expectativa, declare elementos específicos del contenido web como arrastrables.  
Para especificar que un elemento se puede arrastrar, use la propiedad CSS propietaria de `-webkit-app-region` WebKit.  El grupo de trabajo css continúa los esfuerzos para estandarizar la `app-region` propiedad.  

### <a name="custom-title-bar-example"></a>Ejemplo de barra de título personalizada  

En el ejemplo siguiente se muestra cómo las nuevas características crean una aplicación web con una barra de título personalizada.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Ejemplo de una barra de título personalizada en Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Ejemplo de una barra de título personalizada en Microsoft Teams  
:::image-end:::  

#### <a name="manifestwebmanifest"></a>manifest.webmanifest  

En el manifiesto, establezca `display_override` la matriz en  `window-controls-overlay` .  Establece el `theme_color` color que elijas para la barra de título.  Establezca el modo de presentación en una reserva adecuada para cuando se `display_override` admite o `window-controls-overlay` no.  

El siguiente fragmento de código incluye las actualizaciones de manifiesto recomendadas.  

```json
{
  "name": "Example PWA",
  "display": "standalone",
  "display_override": [ 
    "window-controls-overlay" 
  ],
  "theme_color": "#254B85"
}
```  

### <a name="indexhtml"></a>index.html  

Los siguientes IDs representan las dos regiones principales de la página web.  

*   `titleBarContainer`  
*   `mainContent`  
    
El elemento con el identificador se establece en y el elemento secundario del cuadro de `div` búsqueda se establece en `titleBar` `draggable` `input` `nonDraggable` .  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

En el `div` elemento con el `titleBarContainer` identificador, el con el identificador representa `div` la parte visible del área de la barra de `titleBar` título.  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Example PWA</title>
    <link rel="stylesheet" href="style.css">
    <link rel="manifest" href="./manifest.webmanifest">
  </head>
  <body>
    <div id="titleBarContainer">
      <div id="titleBar" class=" draggable">
        <span class="draggable">Example PWA</span>
        <input class="nonDraggable" type="text" placeholder="Search"></input>
      </div>
    </div>
    <div id="mainContent"><!-- The rest of the webpage --></div>
  </body>
</html>
```  

### <a name="stylecss"></a>style.css  

Las regiones arrastrables y no arrastrables se establecen mediante `-webkit-app-region: drag` y `-webkit-app-region: no-drag` .  

```css
.draggable {
    app-region: drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: drag;
}

.nonDraggable {
    app-region: no-drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: no-drag;
}
```  

Para el elemento, los márgenes se establecen para garantizar que la barra `body` de título llegue a los bordes de la `0` ventana.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

El `titleBarContainer` identificador usa y establece el valor en , que adjunta el contenedor a la parte superior `position: absolute` de la página `top` `titlebar-area-inset-top` web.  Se establece en y vuelve a si la superposición de controles de ventana `bottom` `titlebar-area-inset-bottom` no está `100% - var(--fallback-title-bar-height)` visible.  El color de fondo del `titleBarContainer` identificador es el mismo que el `theme_color` .  El ancho se establece en , de modo que el elemento rellena el ancho de la página web y fluye debajo de la superposición cuando está visible para una `100%` `div` apariencia contigua.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

El `titleBar` identificador también usa y para `position: absolute` `top: titlebar-area-inset-top` adjuntarlo a la parte superior de la ventana.  De forma predeterminada, consume el ancho completo de la ventana.  Los `left` bordes y se establecen en y `right` respectivamente, ambos se `titlebar-area-inset-left` `titlebar-area-inset-right` resonarán `0` cuando no se establecen los valores.  También se establece para evitar cualquier intento de arrastrar la ventana consumida en su lugar `user-select: none` resalta el texto del `div` elemento.  

```css
#titleBar {
    position: absolute;
    top: 0;
    display: flex;
    user-select: none;
    height: 100%;
    left: env(titlebar-area-x, 0);
    right: env(titlebar-area-width, 0);
    color: #FFFFFF;
    font-weight: bold;
    text-align: center;
}

#titleBar > span {
    margin: auto;
    padding: 0px 16px 0px 16px;
}

#titleBar > input {
    flex: 1;
    margin: 8px;
    border-radius: 5px;
    border: none;
    padding: 8px;
}
```

El contenedor del identificador también se fija en su lugar `mainContent` y se adjunta a la parte inferior de la página `position: absolute` web.  The `height` is set to and falls back to to fill the remaining space below the title `titlebar-area-inset-bottom` `100% - var(--fallback-titlebar-height)` bar.  Se establece `overflow-y: scroll` para permitir que el contenido se desplace verticalmente en el contenedor.  

```css
#mainContent {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    overflow-y: scroll;
}
```

En los casos en los que el explorador no admite la superposición de controles de ventana, se agrega una variable CSS para establecer un alto predeterminado para la barra de título.  Los límites de los e IDs se establecen inicialmente para rellenar todo el área de cliente y no es necesario cambiarlo si no se admite `titleBarContainer` `mainContent` la superposición.  

El siguiente fragmento de código incluye todas las actualizaciones CSS recomendadas.

```css
:root {
  --fallback-title-bar-height: 40px;
}

.draggable {
  app-region: drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: drag;
}

.nonDraggable {
  app-region: no-drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: no-drag;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
}

#titleBarContainer {
  position: absolute;
  top: env(titlebar-area-y, 0);
  bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  width: 100%;
  background-color:#254B85;
}

#titleBar {
  position: absolute;
  top: 0;
  display: flex;
  user-select: none;
  height: 100%;
  left: env(titlebar-area-x, 0);
  right: env(titlebar-area-width, 0);
  color: #FFFFFF;
  font-weight: bold;
  text-align: center;
}

#titleBar > span {
  margin: auto;
  padding: 0px 16px 0px 16px;
}

#titleBar > input {
  flex: 1;
  margin: 8px;
  border-radius: 5px;
  border: none;
  padding: 8px;
}

#mainContent {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  overflow-y: scroll;
}
```  

## <a name="run-on-os-login"></a>Ejecutar en inicio de sesión del sistema operativo  

Esta característica te permite configurar la aplicación para que se inicie automáticamente cuando el usuario inicie sesión en Microsoft Windows.  Varias clases de aplicaciones aprovechan la funcionalidad.  Las clases de aplicaciones incluyen correo electrónico, chat, panel de supervisión y aplicaciones para mostrar datos en tiempo real.  La funcionalidad permite a un usuario interactuar con las aplicaciones tan pronto como el usuario inicia sesión en el sistema operativo.  Esta característica inicia automáticamente el PWA de la misma manera que se inicia manualmente.  

> [!IMPORTANT]
> **Ejecutar en inicio de sesión del sistema** operativo es una característica [eficaz.][GithubW3cPermissionsPowerfulFeature]  Los usuarios deben decidir si se activa la funcionalidad de la aplicación web instalada.  

### <a name="turn-on-run-on-os-login"></a>Activar Ejecutar inicio de sesión del sistema operativo  

Para obtener una vista previa de las funciones **Ejecutar** en el inicio de sesión del sistema operativo para su PWA, vaya a Activar características [experimentales](#turn-on-experimental-features) y active Las PWA de escritorio se ejecutan en el inicio **de sesión del sistema operativo.**  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Activar las PWA de escritorio que se ejecutan en el experimento inicio de sesión del sistema operativo" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   Activar las **PWA de escritorio que se ejecutan en el experimento de inicio de sesión del sistema** operativo  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a>Activar la característica de la aplicación web instalada  

Para activar la `Start app when you sign in` característica de un PWA instalado, 

1.  Abra Microsoft Edge.   
1.  Vaya a `edge://apps` .  
1.  Mantenga el mouse en la aplicación.  
1.  Abra el menú contextual \(right-click\) y, a continuación, elija **Iniciar aplicación al iniciar sesión**.  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Usa el menú contextual para activar la aplicación Inicio al iniciar sesión en la característica de Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       Usa el menú contextual para activar la **aplicación Inicio al iniciar sesión en** la característica de Microsoft Edge  
    :::image-end:::  
    
## <a name="shortcuts"></a>Accesos directos  

`Shortcuts` es un nuevo miembro del archivo de manifiesto.  Te permite definir vínculos a elementos, páginas web clave o acciones en la aplicación web.  Microsoft Windows lo integra como **jumplists**.  **Las listas de accesos** emergentes definen menús emergentes que aparecen cuando se encuentra en uno de los siguientes elementos de la interfaz de usuario y se abre un menú contextual \(hacer clic con el botón secundario\).  

*   Un icono en el menú Inicio  
*   Un icono en la barra de tareas  
    
Cuando un usuario invoca un acceso directo, el usuario navega a la dirección especificada por el `url` miembro del acceso directo.  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Un ejemplo de listas de saltos en Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   Un ejemplo de **listas de saltos** en Windows 10  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a>Accesos directos en el archivo de manifiesto  

```json
"shortcuts" : [
  {
    "name": "Today's agenda",
    "url": "/today",
    "description": "List of events planned for today"
  },
  {
    "name": "New event",
    "url": "/create/event"
  },
  {
    "name": "New reminder",
    "url": "/create/reminder"
  }
]
```  

#### <a name="properties-of-shortcuts"></a>Propiedades de accesos directos  

Las siguientes propiedades definen cada acceso directo.  

| Propiedad | Detalles |  
|:--- |:--- |  
| `name` | Cadena que se muestra al usuario en **listas de saltos** o en el menú contextual. |  
| `short_name` | Cadena que se muestra cuando hay espacio insuficiente para mostrar el nombre completo del acceso directo. |  
| `description` | Cadena que describe el propósito del acceso directo.  Es posible que se pueda acceder a ella mediante tecnología de asistencia. |  
| `url` | Uri de la aplicación web que se abre cuando se activa el acceso directo. |  
| `icons` | Un conjunto de iconos que representa el acceso directo. |  

## <a name="file-handling"></a>Administración de archivos  

La capacidad de registrarse como un controlador de tipos de archivo está en la fase de experimentación.  Puedes especificar los tipos de archivo que controla la aplicación en una entrada de manifiesto.  Durante la instalación, el sistema operativo host del usuario registra la aplicación como un controlador de archivos para los tipos de archivo enumerados.  Asegúrese de la existencia de la característica en el código de inicio de las `launchQueue` aplicaciones y de que controla el archivo.  

Los exploradores basados en Chromium están probando y dando forma a esta característica.  Para obtener más información, incluidos los ejemplos de código, vaya a [Permitir que las aplicaciones web sean controladores de archivos][WebDevFileHandling].  

Para obtener una vista previa del control de archivos en Microsoft Edge para Windows 10, vaya a Activar características [experimentales](#turn-on-experimental-features) y active api **de administración de archivos.**  
    
## <a name="providing-feedback-on-experimental-features"></a>Proporcionar comentarios sobre características experimentales  

Para proporcionar comentarios sobre los experimentos de la aplicación web de Microsoft Edge.  

*   Envíe sus comentarios con **Configuración y Más** \( `...` \) > Enviar comentarios a **Microsoft**.  
*   Seleccione `Alt` + `Shift` + `I` .  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Enviar comentarios desde su PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   Enviar comentarios desde su PWA  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Pruebas de origen | Desarrollador de Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registrar para el registro del controlador de protocolo de aplicación web | Microsoft Developer"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Controladores de protocolo basados en web | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Característica eficaz: permisos | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PwAs como controladores de dirección URL | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Permitir que las aplicaciones web sean controladores de archivos | web.dev"  

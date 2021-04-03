---
description: Las últimas características experimentales de Microsoft Edge para aplicaciones web
title: Características experimentales | Aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 587797bc8577f1c1aaca42394eecb997d21e9955
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474989"
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
| [Administración del protocolo URI](#uri-protocol-handling) | 91 o posterior | Windows |    
| [Administración de vínculos URL](#url-link-handling) | 91 o posterior | Windows|  
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

Para obtener una vista previa del control de protocolos en Microsoft Edge en Windows, vaya a Activar características [experimentales](#turn-on-experimental-features) y active **Desktop Web Apps support Protocol Handlers**.  

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

<!-- Hold for future release -->  
<!--  ## Window Controls Overlay for installed desktop web apps  

To create an immersive title bar similar to a native app for your desktop installed web app.  The **Window Controls Overlay** feature  completes the following actions.  
    
1.  Removes the system reserved title bar.  It usually spans the width of the client frame.  
1.  Replaces it with an overlay.  It contains just the critical system required window controls necessary for a user to control the window itself.  
    
After it provides an overlay, the entire web client area is available for you to use.  This feature includes a manifest update.  It provides ways for you to determine the size and position of the overlay to help you arrange content.  
    
### Examples of title bar area customization  

This feature is based on the ability in native apps to customize the title bar.  You may customize a title bar for important app actions or notifications.  Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.  

#### Visual Studio Code  

Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.  

The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="An example of the title bar in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   An example of the title bar in Visual Studio Code  
:::image-end:::  

#### Microsoft Teams  

Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.  In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="An example of the title bar in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   An example of the title bar in Microsoft Teams  
:::image-end:::  

### Overlay Window Controls on a Frameless Window  

To provide the maximum addressable area for web content, the browser creates a frameless window, removing all browser UI except for the window controls provided as an overlay.  
The window controls overlay ensures users still minimize, maximize, restore, and close the app.  It also provides access to relevant browser controls using the web app menu.  For Chromium-based browsers, the controls in the overlay.

*   A draggable region the same width and height of each of the window control buttons  
*   The **Settings and more** \(...\) button  
*   The window control buttons minimize, maximize, restore, and close  
    
The following scenarios include when browser displays other content in the controls overlay.  

*   When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.  
*   If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.  After you exit any extension dialog, the icon is removed from the overlay.  
    
| Language direction | Overlay location | Details |  
|:--- |:--- |:--- |  
| Left-to-right \(LTR\) | Upper left of the client area | The controls are flipped |  
| Right-to-left \(RTL\) | Upper right corner of the client area |  |  

>[!IMPORTANT]
> The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.  

### Working around the Window Controls Overlay  

Your web content must be aware of the reserved area for the controls overlay.  Ensure the reserved area doesn't expect user interaction.  Query the browser for the bounding rectangle and visibility of the controls overlay.  The information is provided to you through JavaScript APIs and CSS environment variables.  

#### JavaScript APIs  

A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.  

The `windowControlsOverlay` object has the following two objects.  

*   `getBoundingClientRect()` returns a `DOMRect` object.  The `DOMRect` object represents the area under the window controls overlay.  
*   `visible` is a boolean that indicates that the controls overlay is rendered and displayed.  
    
> [!IMPORTANT]
> For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.  

Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.  The recalculated content layout is based on the new bounding rectangle of the overlay.  

#### CSS Environment Variables  

Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.  Use the following four new CSS environment variables to accomplish to query.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### Define Draggable Regions in Web Content  

Users expect to grab and drag the upper region of a window.  To accommodate the expectation, declare specific parts of the web content as draggable.  
To specify an element is draggable, use the webkit proprietary `-webkit-app-region` CSS property.  The CSS working group continues efforts to standardize the `app-region` property.  

To preview this feature in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.   

### Custom title bar example  

The following example displays how the new features create a web app with a custom title bar.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Example of a custom title bar in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Example of a custom title bar in Microsoft Teams  
:::image-end:::  

#### manifest.webmanifest  

In the manifest, set `display_override` array to  `window-controls-overlay`.  Set the `theme_color` to your choice of color for the title bar.  Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.  

The following code snippet includes the recommended manifest updates.  

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

### index.html  

The following IDs represent the two main regions of the webpage.  

*   `titleBarContainer`  
*   `mainContent`  
    
The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.  

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
    <div id="mainContent">The rest of the webpage</div>
  </body>
</html>
```  

### style.css  

The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.  

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

For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.  The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.  The background color of the `titleBarContainer` ID is the same as the `theme_color`.  The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.  By default, it consumes the full width of the window.  The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.  It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.  

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

The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.  The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.  It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.  

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

For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.  The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.  

The following code snippet includes all of the recommended css updates.

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
-->  

## <a name="run-on-os-login"></a>Ejecutar en inicio de sesión del sistema operativo  

Esta característica te permite configurar la aplicación para que se inicie automáticamente cuando el usuario inicie sesión en Microsoft Windows.  Varias clases de aplicaciones aprovechan la funcionalidad.  Las clases de aplicaciones incluyen correo electrónico, chat, panel de supervisión y aplicaciones para mostrar datos en tiempo real.  La funcionalidad permite a un usuario interactuar con las aplicaciones tan pronto como el usuario inicia sesión en el sistema operativo.  Esta característica inicia automáticamente el PWA de la misma manera que se inicia manualmente.  

> [!IMPORTANT]
> **Ejecutar en inicio de sesión del sistema** operativo es una característica [eficaz.][GithubW3cPermissionsPowerfulFeature]  Los usuarios deben decidir si se activa la funcionalidad de la aplicación web instalada.  

### <a name="turn-on-run-on-os-login"></a>Activar Ejecutar inicio de sesión del sistema operativo  

Para activar ejecutar las **capacidades** de inicio de sesión del sistema operativo para su PWA, vaya a Activar características [experimentales](#turn-on-experimental-features) y active Las PWA de escritorio se ejecutan en el inicio **de sesión del sistema operativo.**  

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

Para obtener una vista previa del control de archivos en Microsoft Edge para sistemas operativo de escritorio, vaya a Activar características [experimentales](#turn-on-experimental-features) y active api **de administración de archivos.**  
    
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

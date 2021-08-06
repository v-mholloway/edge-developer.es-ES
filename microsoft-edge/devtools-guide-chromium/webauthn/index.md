---
description: Emular Autenticadores y Depurar WebAuthn en Microsoft Edge DevTools.
title: Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 668cefd1728d1383df249417a026ae28827b3601079e250d2a6d32a85f5df336
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11798933"
---
# <a name="emulate-authenticators-and-debug-webauthn-in-microsoft-edge-devtools"></a>Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools  

En lugar de depurar la autenticación web en tu sitio web o aplicación con autenticadores físicos, usa la herramienta **WebAuthn** en Microsoft Edge DevTools para crear e interactuar con autenticadores virtuales basados en software.  

## <a name="before-you-begin"></a>Antes de empezar  

Un excelente lugar para empezar a usar la autenticación web es la especificación [de la API de autenticación web.][GithubW3cWebauthn]  

## <a name="set-up-the-webauthn-tool"></a>Configurar la herramienta WebAuthn  

1.  Navegue a una página web que use WebAuthn, como el siguiente sitio web de demostración.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Inicie sesión en el sitio web.  
1.  [Abra DevTools][DevtoolsGuideChromiumOpen].  
1.  Para abrir la **herramienta WebAuthn,** elija el icono Personalizar y **controlar DevTools** \( \) > `...` Más **herramientas**  >  **WebAuthn**.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Herramienta WebAuthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       **Herramienta WebAuthn**  
    :::image-end:::  
    
1.  En la **herramienta WebAuthn,** active la casilla Habilitar **entorno de autenticación virtual.**  
1.  Una vez habilitada, se muestra una nueva sección denominada **Nuevo autenticador.**  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Habilitar el entorno de autenticación virtual" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Habilitar el entorno de autenticación virtual**  
    :::image-end:::  
    
1.  En la **sección Nuevo autenticador,** configure las siguientes opciones.  
    
    | Opción | Valor | Detalles |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] o [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | El protocolo que usa el autenticador virtual para codificar y decodificar |  
    | `Transport` |   `usb`, `nfc` , `ble` o `internal` | El autenticador virtual simula el transporte seleccionado para comunicarse con los clientes con el fin de obtener una aserción para una credencial específica.  Para obtener más información, vaya [a Authenticator enumeración de transporte][GithubW3cWebauthnEnumTransport] |  
    |  `Supports resident keys` | Activar \(o desactivar\) con la casilla | Activar si la aplicación web se basa en claves residentes \(también conocidas como credenciales detectables del lado cliente\).  Para obtener más información, vaya a [Enumeración de requisitos de clave residente][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Activar \(o desactivar\) con la casilla | Activar si la aplicación web se basa en la autorización local mediante modalidades de gestos como el código táctil más pin, la entrada de contraseña o el reconocimiento biométrico.  Para obtener más información, vaya a [Verificación de usuarios][GithubW3cWebauthnEnumUserverification] |  
    
1.  Elija el **botón** Agregar.  
1.  Se muestra una nueva sección del autenticador recién creado.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Authenticator" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
La **Authenticator** incluye una **tabla Credenciales.**  La tabla está vacía hasta que se registra una credencial en el autenticador.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Sin credenciales" lightbox="../media/webauthn-no-cred.msft.png":::
   Sin credenciales  
:::image-end:::  

## <a name="register-a-new-credential"></a>Registrar una nueva credencial  

Para registrar una nueva credencial, siga estos pasos.  Para obtener más información acerca de lo que está haciendo la [API de][GithubW3cWebauthn] autenticación web al registrar una nueva credencial, vaya a Crear una [nueva credencial][GithubW3cWebauthnSctnCreatecredential].  

1.  En el sitio web de demostración, elija **Registrar nueva credencial**.  
1.  Ahora se agrega una nueva credencial a la **tabla Credenciales** de la herramienta WebAuthn.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Ver credenciales" lightbox="../media/webauthn-view-cred.msft.png":::
       Ver credenciales  
    :::image-end:::  
    
En el sitio web de demostración, elija el **botón Autenticar.**  Compruebe que el [número de signos][GithubW3cWebauthnSctnSignCounter] de la credencial de la tabla **Credenciales** aumentó en 1, lo que marca una operación [authenticatorGetAssertion correcta.][GithubW3cWebauthnAuthenticatorgetassertion]  

## <a name="export-and-remove-credentials"></a>Exportar y quitar credenciales  

Para exportar o quitar una credencial, elija el **botón Exportar** **o** Quitar.  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Exportar o quitar una credencial" lightbox="../media/webauthn-export-remove.msft.png":::
   Exportar o quitar una credencial  
:::image-end:::  

## <a name="rename-an-authenticator"></a>Cambiar el nombre de un autenticador  

Para cambiar el nombre de un autenticador, siga estos pasos.  

1.  Junto al nombre del autenticador, elija el **botón** Editar.  
1.  Edite el nombre y, a continuación, **elija Entrar** para guardar los cambios.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Cambiar el nombre de un autenticador" lightbox="../media/webauthn-rename.msft.png":::
   Cambiar el nombre de un autenticador  
:::image-end:::  

## <a name="set-the-active-authenticator"></a>Establecer el autenticador activo  

Un autenticador recién creado se activa automáticamente.  Para usar otro autenticador virtual, elija el **botón de** radio Activo junto al autenticador.  

> [!NOTE]
> DevTools solo admite un autenticador virtual activo en cualquier momento.  Si quita el autenticador activo, otro autenticador no se activará automáticamente.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Establecer autenticador activo" lightbox="../media/webauthn-set-active.msft.png":::
   Establecer autenticador activo  
:::image-end:::  

## <a name="remove-a-virtual-authenticator"></a>Quitar un autenticador virtual  

Para quitar un autenticador virtual, junto al autenticador, elija el **botón** Quitar.  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Quitar autenticador" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Quitar autenticador  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abrir Microsoft Edge DevTools | Microsoft Docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Demostración de webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Protocolo de Authenticator (CTAP) | alianza de fido"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "Información general sobre el factor universal 2nd (U2F) | alianza de fido"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "La operación authenticatorGetAssertion: autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Authenticator Enumeración de transporte (enumeración AuthenticatorTransport): autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | W3C"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeración de requisitos de clave residente (enumeración ResidentKeyRequirement): autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | W3C"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Comprobación del usuario: autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | W3C"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Create a New Credential - PublicKeyCredential's [[Create]](origin, options, sameOriginWithAncestors) Method - Web Authentication: An API for accessing Public Key Credentials Level 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Consideraciones del contador de firmas: autenticación web: una API para obtener acceso a credenciales de clave pública nivel 2 | GitHub"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

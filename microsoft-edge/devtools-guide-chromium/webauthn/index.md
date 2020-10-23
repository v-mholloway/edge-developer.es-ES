---
description: Emular autenticadores y depurar webauthn en Microsoft Edge DevTools.
title: Emular autenticadores y depurar webauthn en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6727e9aeea1a51689a80570a2f1c9df880a8c9db
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134234"
---
# Emular autenticadores y depurar webauthn en Microsoft Edge DevTools  

En lugar de depurar la autenticación Web en su sitio web o aplicación con autenticadores físicos, use la herramienta **Webauthn** en Microsoft Edge DevTools para crear e interactuar con autenticadores virtuales basados en software.  

## Antes de comenzar  

Un buen lugar para empezar a usar la autenticación Web es la [especificación de API de autenticación Web][GithubW3cWebauthn].  

## Configurar la herramienta webauthn  

1.  Vaya a una página web que use webauthn, como el siguiente sitio web de demostración.  
    
    [webauthndemo.appspot.com][AppspotWebauthndemo]  
    
1.  Inicie sesión en el sitio Web.  
1.  [Abra DevTools][DevtoolsGuideChromiumOpen].  
1.  Para abrir la herramienta **webauthn** , elija el icono **personalizar y controlar DevTools** \ ( `...` \) > **más herramientas**  >  **webauthn**.  
    
    :::image type="complex" source="../media/webauthn-webauthn-tab.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-webauthn-tab.msft.png":::
       Herramienta **Webauthn**  
    :::image-end:::  
    
1.  En la herramienta **Webauthn** , elija la casilla que se encuentra junto a **Habilitar el entorno de autenticador virtual**.  
1.  Una vez que se haya habilitado, aparecerá una nueva sección llamada **nuevo autenticador** .  
    
    :::image type="complex" source="../media/webauthn-enable-virtual-auth.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-enable-virtual-auth.msft.png":::
        **Habilitar el entorno de autenticador virtual**  
    :::image-end:::  
    
1.  En la sección **nuevo autenticador** , configure las opciones siguientes.  
    
    | Opción | Valor | Detalles |  
    |:--- |:--- |:--- |  
    | `Protocol` | [ctap2][FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml] o [u2f][FidoallianceSpecsU2fV12Ps20170411OverviewHtml] | El protocolo que el autenticador virtual usa para codificar y descodificar |  
    | `Transport` |   `usb`, `nfc` , `ble` o `internal` | El autenticador virtual simula el transporte seleccionado para comunicarse con los clientes a fin de obtener una aserción para una credencial específica.  Para obtener más información, vaya a la [enumeración de transporte de autenticador][GithubW3cWebauthnEnumTransport] |  
    |  `Supports resident keys` | Activar \ (o desactivar \) con la casilla | Active esta opción si su aplicación web depende de las claves residentes \ (también conocidas como credenciales detectables del cliente \).  Para obtener más información, vaya a la [enumeración de requisitos clave residente][GithubW3cWebauthnEnumResidentkeyrequirement]. |  
    | `Supports user verification` | Activar \ (o desactivar \) con la casilla | Active esta opción si su aplicación web se basa en la autorización local con modalidades de gestos como toque, código PIN, entrada de contraseña o reconocimiento biométrico.  Para obtener más información, vaya a verificación por el [usuario][GithubW3cWebauthnEnumUserverification] |  
    
1.  Elija el botón **Agregar** .  
1.  Aparece una nueva sección del autenticador recién creado.  
    
    :::image type="complex" source="../media/webauthn-authenticator.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-authenticator.msft.png":::
       Authenticator  
    :::image-end:::  
    
La sección **Authenticator** incluye una tabla de **credenciales** .  La tabla está vacía hasta que se registra una credencial para el autenticador.  

:::image type="complex" source="../media/webauthn-no-cred.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-no-cred.msft.png":::
   No hay credenciales  
:::image-end:::  

## Registrar una nueva credencial  

Siga los pasos que se indican a continuación para registrar una nueva credencial.  Para obtener más información sobre lo que hace la [API de autenticación Web][GithubW3cWebauthn] al registrar una credencial nueva, vaya a [crear una credencial nueva][GithubW3cWebauthnSctnCreatecredential].  

1.  En el sitio web de demostración, elija **registrar nueva credencial**.  
1.  Ahora se agrega una nueva credencial a la tabla de **credenciales** en la herramienta webauthn.  
    
    :::image type="complex" source="../media/webauthn-view-cred.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-view-cred.msft.png":::
       Ver credenciales  
    :::image-end:::  
    
En el sitio web de demostración, elija el botón **autenticar** .  Compruebe que el [recuento de firma][GithubW3cWebauthnSctnSignCounter] de la credencial en la tabla de **credenciales** aumentó en 1, lo que marca una operación de [authenticatorGetAssertion][GithubW3cWebauthnAuthenticatorgetassertion] correcta.  

## Exportar y quitar credenciales  

Para exportar o quitar una credencial, seleccione el botón **exportar** o **quitar** .  

:::image type="complex" source="../media/webauthn-export-remove.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-export-remove.msft.png":::
   Exportar o quitar una credencial  
:::image-end:::  

## Cambiar el nombre de un autenticador  

Para cambiar el nombre de un autenticador, siga los pasos que se indican a continuación.  

1.  Junto al nombre de autenticador, seleccione el botón **Editar** .  
1.  Edite el nombre y, a continuación, elija **entrar** para guardar los cambios.  

:::image type="complex" source="../media/webauthn-rename.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-rename.msft.png":::
   Cambiar el nombre de un autenticador  
:::image-end:::  

## Establecer el autenticador activo  

Un autenticador recién creado se activa automáticamente.  Para usar otro autenticador virtual, seleccione el botón de radio **activo** junto al autenticador.  

> [!NOTE]
> DevTools solo admite autenticadores virtuales activos en cualquier momento.  Si quita el autenticador activo, otro autenticador no se activará automáticamente.  

:::image type="complex" source="../media/webauthn-set-active.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-set-active.msft.png":::
   Establecer autenticador activo  
:::image-end:::  

## Quitar un autenticador virtual  

Para quitar un autenticador virtual, junto al autenticador, seleccione el botón **quitar** .  

:::image type="complex" source="../media/webauthn-remove-authenticator.msft.png" alt-text="Herramienta webauthn" lightbox="../media/webauthn-remove-authenticator.msft.png":::
   Quitar autenticador  
:::image-end:::  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

[AppspotWebauthndemo]: https://webauthndemo.appspot.com "Demostración de webauthn | Appspot"  

[FidoallianceSpecsV20Id20180227ClientToAuthenticatorProtocolHtml]: https://fidoalliance.org/specs/fido-v2.0-id-20180227/fido-client-to-authenticator-protocol-v2.0-id-20180227.html "Protocolo de cliente a autenticador (CTAP) | Fido Alliance"  
[FidoallianceSpecsU2fV12Ps20170411OverviewHtml]: https://fidoalliance.org/specs/fido-u2f-v1.2-ps-20170411/fido-u2f-overview-v1.2-ps-20170411.html "2º factor universal (U2F) Descripción general | Fido Alliance"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnAuthenticatorgetassertion]: https://w3c.github.io/webauthn#authenticatorgetassertion "La operación authenticatorGetAssertion-autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnEnumTransport]: https://w3c.github.io/webauthn#enum-transport "Enumeración de transporte de autenticadores (enumeración de AuthenticatorTransport)-autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | RELATIVA"  
[GithubW3cWebauthnEnumResidentkeyrequirement]: https://w3c.github.io/webauthn#enum-residentKeyRequirement "Enumeración de requisitos clave residentes (enumeración ResidentKeyRequirement)-autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | RELATIVA"  
[GithubW3cWebauthnEnumUserverification]: https://w3c.github.io/webauthn#user-verification "Verificación de usuario: autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | RELATIVA"  
[GithubW3cWebauthnSctnCreatecredential]: https://w3c.github.io/webauthn#sctn-createCredential "Crear una nueva credencial-PublicKeyCredential [[Create]] (origen, opciones, sameOriginWithAncestors) método-autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | GitHub"  
[GithubW3cWebauthnSctnSignCounter]: https://w3c.github.io/webauthn/#sctn-sign-counter "Consideraciones del contador de firmas: autenticación Web: una API para el acceso a las credenciales de clave pública nivel 2 | GitHub"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/webauthn/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

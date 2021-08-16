---
description: Nuevas características para aplicaciones web progresivas (PWA).
title: Novedades de las aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/09/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, pwas, pwa, aplicaciones web progresivas
ms.openlocfilehash: 9643c8846ccea373c3051b137cc4299ba617dad7
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11893546"
---
# <a name="whats-new-in-progressive-web-apps"></a>Novedades de las aplicaciones web progresivas

[!INCLUDE [contact DevTools team note](includes/edge-whats-new-note.md)]


## <a name="whats-new-in-microsoft-edge-93"></a>Novedades de Microsoft Edge 93

Microsoft Edge versión 93 se convirtió en el canal beta de Microsoft Edge el 3 de agosto de 2021. En este artículo se enumeran las actualizaciones realizadas en las aplicaciones web progresivas (PWA) tanto desde el punto de vista del desarrollador como del consumidor.

## <a name="window-controls-overlay-origin-trials"></a>Pruebas de origen de superposición de controles de ventana

Para tener más control sobre el área de la barra de título que se muestra actualmente en modo de presentación independiente, es posible que desee experimentar con la superposición de controles de ventana. La superposición de controles de ventana (WCO) es un conjunto de características que funcionan juntas para proporcionar solo los controles esenciales necesarios para la ventana de la aplicación. Este diseño libera más espacio para la capa de contenido web. WCO está disponible para las PWA de escritorio instaladas. 

Obtenga más información sobre cómo experimentar con la superposición de controles de ventana [en las características experimentales de Las aplicaciones web progresivas (PWA).][ExpWCO]

Registra tu origen para la prueba De superposición de controles de ventana en nuestra [consola de desarrollador de pruebas de origen.][WCOOT]

## <a name="url-handlers-origin-trial"></a>Prueba de origen de controladores de dirección URL

Los desarrolladores ahora pueden usar la característica experimental Controladores de url de aplicación web en la versión de prueba de origen. Esta característica permite el registro de una PWA para abrir vínculos de otras aplicaciones que hacen referencia a su ámbito.

Obtenga más información sobre cómo experimentar con controladores de direcciones URL en [Características experimentales de Progressive Web Apps (PWAs).][ExpURLHandler]

Registre su dominio para la versión de prueba del controlador de direcciones URL en nuestra consola del desarrollador [de pruebas de Origin.][URLHandlerOT]

## <a name="support-for-the-share-api-on-macos"></a>Compatibilidad con la API de Share en macOS

Hemos implementado la compatibilidad con la `navigator.share` API para macOS. La característica se está implementando de forma estable Microsoft Edge exploradores en macOS en las próximas semanas. 

Obtenga más información sobre la [API navigator.share().][mdnShareAPI]


## <a name="whats-new-in-microsoft-edge-92"></a>Novedades de Microsoft Edge 92

Microsoft Edge versión 92 se convirtió en el canal estable de Microsoft Edge el 22 de julio de 2021. En este artículo se enumeran las actualizaciones realizadas en las aplicaciones web progresivas (PWA) tanto desde el punto de vista del desarrollador como del consumidor.

## <a name="protocol-handlers-origin-trial"></a>Prueba de origen de controladores de protocolo 

Ahora puede registrar su PWA para controlar protocolos específicos con el sistema operativo host. La Windows de prueba para controladores de protocolo ya está disponible. Puede registrar su origen para la prueba en la página de registro [de prueba de origen][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].

Obtenga más información sobre el uso de controladores de protocolo con su PWA características experimentales en [Progressive Web Apps (PWA).][ExpProtocolHandlers]

## <a name="streamlined-app-info-menu"></a>Menú Información de la aplicación optimizada

Cuando un usuario selecciona el botón puntos suspensivos (**...**) en la barra de título de la aplicación, se muestra el menú Información de la aplicación. ****  Hemos actualizado el **** menú Información de la aplicación y hemos optimizado la experiencia del usuario de las siguientes maneras, para proporcionar una experiencia de usuario más parecido a una aplicación de escritorio que a una interfaz de usuario del explorador:
*  Movió la **aplicación Publisher** información al nivel superior y la hizo lo primero que un usuario ve.

   :::image type="complex" source="media/app-info.png" alt-text="El nuevo menú de información de la aplicación simplificado" lightbox="media/app-info.png":::
      El nuevo menú de información **de la aplicación simplificado**
   :::image-end:::

*  Movió la información de privacidad y los controles a un menú privacidad dedicado **de** 2nd level.

   :::image type="complex" source="media/privacy-menu.png" alt-text="Controles de privacidad en el menú privacidad dedicado" lightbox="media/privacy-menu.png":::
      Controles de privacidad en el menú **privacidad** dedicado
   :::image-end:::

*  Movió las herramientas relacionadas con el contenido a un menú dedicado de 2nd-level **Más** herramientas.

   :::image type="complex" source="media/more-tools.png" alt-text="Las herramientas relacionadas con el contenido ahora se encuentran en el menú Más herramientas" lightbox="media/more-tools.png":::
      Las herramientas relacionadas con el contenido ahora se encuentran en el **menú Más** herramientas
   :::image-end:::


## <a name="post-install-flyout-dialog-box"></a>Cuadro de diálogo desplegable posterior a la instalación

Después de PWA desde el explorador Microsoft Edge en Windows, los usuarios ahora pueden seleccionar entre cuatro opciones para iniciar fácilmente sus aplicaciones: 
*  **Anclar a la barra de tareas** 
*  **Anclar a Inicio**
*  **Crear acceso directo de escritorio**
*  **Inicio automático en el inicio de sesión del dispositivo**

Para mayor comodidad, este cuadro de diálogo desplegable se muestra la primera vez que se inicia la aplicación.

:::image type="complex" source="media/postInstallFlyout.png" alt-text="Cuadro de diálogo desplegable posterior a la instalación con opciones para Anclar a la barra de tareas, Anclar a Inicio, Crear acceso directo de escritorio y Inicio automático en el inicio de sesión del dispositivo" lightbox="media/postInstallFlyout.png":::
   Cuadro de diálogo desplegable posterior a la instalación con opciones **** para Anclar a la barra de **tareas,** Anclar a **Inicio,** Crear acceso directo de escritorio y Inicio automático en el inicio de sesión **del dispositivo**
:::image-end:::

Esta característica se está implantando gradualmente para todos los usuarios. Mientras tanto, si desea usar esta característica, vaya a y habilite el cuadro de diálogo de instalación posterior de aplicaciones web de `edge://flags` **marca**.

## <a name="restore-web-apps"></a>Restaurar aplicaciones web

Los sitios instalados y los PWA que se ejecutaban antes de un apagado inesperado ahora se restaurarán (es decir, se reiniciarán) cuando se recupere el sistema.

Puede producirse un apagado inesperado debido a un error del proceso, al reinicio del sistema o a una interrupción del suministro eléctrico. Antes de este cambio, los sitios instalados y los PWA tenían un comportamiento indeterminado al restaurar el sistema.  

<!-- links -->  

<!--[ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]: /archive/microsoft-edge/legacy/developer/progressive-web-apps/index#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[ExpWCO]: ../experimental-features/index.md#window-controls-overlay-for-installed-desktop-web-apps "Superposición de controles de ventana para aplicaciones web de escritorio instaladas: características experimentales"

[ExpProtocolHandlers]: ../experimental-features/index.md#uri-protocol-handling "Administración de protocolo URI: características experimentales"

[ExpURLHandler]: ../experimental-features/index.md#url-link-handling "Administración de vínculos URL: características experimentales"

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Pruebas de origen | Microsoft Edge Programador"

[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registrar para el registro del controlador de protocolo de aplicación web | Microsoft Developer"  

[URLHandlerOT]: https://developer.microsoft.com/en-us/microsoft-edge/origin-trials/web-app-url-handlers/registration/ "Registrar para el controlador de direcciones URL de la aplicación web | Microsoft Developer" 

[WCOOT]: https://developer.microsoft.com/en-us/microsoft-edge/origin-trials/web-app-window-controls-overlay/registration/ "Registrar para la superposición de controles de ventana de aplicación web"

[mdnShareAPI]: https://developer.mozilla.org/en-US/docs/Web/API/Navigator/share

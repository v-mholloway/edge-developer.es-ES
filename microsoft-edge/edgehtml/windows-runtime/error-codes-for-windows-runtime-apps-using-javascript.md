---
description: Códigos de error para aplicaciones de Windows Runtime con JavaScript
title: Códigos de error para aplicaciones de Windows Runtime con JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
f1_keywords:
- JavaScript, Windows Runtime error codes
- VS.WebClient.Help.APPHOST9601
- VS.WebClient.Help.APPHOST9602
- VS.WebClient.Help.APPHOST9603
- VS.WebClient.Help.APPHOST9604
- VS.WebClient.Help.APPHOST9605
- VS.WebClient.Help.APPHOST9606
- VS.WebClient.Help.APPHOST9607
- VS.WebClient.Help.APPHOST9608
- VS.WebClient.Help.APPHOST9610
- VS.WebClient.Help.APPHOST9611
- VS.WebClient.Help.APPHOST9613
- VS.WebClient.Help.APPHOST9614
- VS.WebClient.Help.APPHOST9615
- VS.WebClient.Help.APPHOST9616
- VS.WebClient.Help.APPHOST9617
- VS.WebClient.Help.APPHOST9618
- VS.WebClient.Help.APPHOST9619
- VS.WebClient.Help.APPHOST9620
- VS.WebClient.Help.APPHOST9623
- VS.WebClient.Help.APPHOST9624
- VS.WebClient.Help.APPHOST9626
ms.assetid: 4c6d4e90-602a-4b56-ae74-3458929da442
caps.latest.revision: 1
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e7241d675a6f488e70eefb20c40149683f965c8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398493"
---
# <a name="error-codes-for-windows-runtime-apps-using-javascript"></a>Códigos de error para aplicaciones de Windows Runtime con JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Estos son los códigos de error que muestra la consola de Microsoft Visual Studio al desarrollar aplicaciones de Windows Runtime con JavaScript.  

| Error | Observaciones |  
|:--- |:--- |  
| APPHOST9601: "No se puede cargar *remoteURI*.  Una aplicación no puede cargar contenido web remoto en el contexto local". | Para obtener más información acerca de lo que se permite en el contexto web, consulta [Características y restricciones por contexto.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9602: "'javascript:' es un valor de atributo no válido y se omitirá.  No use URI de 'javascript:' en el contexto local". | Por motivos de seguridad, no puede usar URI de 'javascript:' en el contexto local.  Para obtener más información sobre lo que se permite en el contexto local, consulta [Características y restricciones por contexto.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9603: "No se puede cargar el complemento ActiveX que tiene el identificador de *clase classID*.  Las aplicaciones no pueden cargar ActiveX controles". | Las aplicaciones de Windows Runtime que usan JavaScript no admiten Microsoft ActiveXcontrols personalizado.  Si necesitas un control de interfaz de usuario, usa un control web estándar, una biblioteca de controles o crea tu propio control personalizado.  Si necesitas realizar una lógica personalizada, crea un objeto personalizado de Windows Runtime en su lugar.  Para obtener información sobre otras diferencias de HTML, CSS y JavaScript, vea [HTML, CSS y JavaScript features and differences][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: "No se puede navegar a *uri* porque usa una codificación de caracteres no válida.  Una aplicación solo puede navegar a archivos codificados en UTF8". | Todos los HTML, JavaScript y CSS a los que tiene acceso un Windows Runtime deben codificarse como formato de transformación Unicode de 8 bits (UTF-8).  Para obtener información sobre otras diferencias de HTML, CSS y JavaScript, vea [HTML, CSS y JavaScript features and differences][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605: "No se puede navegar a *targetURI* desde *sourceURI* porque el URI de destino está en una zona de mayor seguridad.  No puede navegar desde una zona con menor seguridad a una zona con mayor seguridad a menos que vaya a un URI de contexto local desde un URI de contexto web y haya registrado el URI de contexto local con el método MSApp.addPublicLocalApplicationUri". | Para obtener más información, [consulta MSApp.addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: "No se puede cargar *uri* porque usa una conexión HTTP y el elemento meta ms-https-connections-only está presente.  Solo se permiten las conexiones HTTPS cuando se usa el elemento meta ms-https-connections-only.  Use una conexión HTTPS o, si no necesita una conexión segura, quite el elemento meta". | Para obtener más información, [consulta How to require an HTTPS connection][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607: "La aplicación no puede iniciar el URI en *uri* debido a este error: *failureCode*." | Un recurso que falta o un archivo no válido son causas comunes de este error.  |  
| APPHOST9608: "La aplicación no pudo navegar a la página about:blank debido a este error: *errorCode*." |  |  

| Error | Observaciones |  
|:--- |:--- |  
| APPHOST9610: "La aplicación encontró un error al prepararse para navegar a una página de error personalizada: *errorCode*." |  |  
| APPHOST9611: "La aplicación no pudo navegar a una página de error personalizada debido a este error: *errorCode*." |  |  
| APPHOST9613: "La aplicación no pudo navegar a *uri*  debido a este error: *errorCode*." |  |  
| APPHOST9614: "Un documento dentro de un iframe solicitó el modo doc *requestedDocMode,* pero el sistema aplica el *modo doc currentDocMode.*  El iframe usará el *modo doc currentDocMode."* | Para obtener más información sobre cómo mostrar contenido web remoto, consulta [Cómo vincular a páginas web externas.][PreviousVersionsWindowsAppsHh780594]  |  
| APPHOST9615: "La aplicación no puede descargar el archivo en *uri* porque se invocó mediante programación fuera del contexto local". | Se produce cuando el contenido en el contexto web intenta descargar mediante programación un archivo.  |  
| APPHOST9616: "Este URI no puede usar API de geolocalización.  Las API de geolocalización solo se pueden invocar desde un URI que forma parte del paquete o se incluye en el elemento ApplicationContentUris del manifiesto". | Para obtener más información acerca de lo que se permite en el contexto web, consulta [Características y restricciones por contexto.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9617: "Este URI no puede usar API del Portapapeles.  Las API del portapapeles solo se pueden invocar desde un URI que forma parte del paquete o se incluye en el elemento ApplicationContentUris del manifiesto". | Para obtener más información acerca de lo que se permite en el contexto web, consulta [Características y restricciones por contexto.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9618: "Este URI no puede usar window.close.  El método window.close solo se puede invocar desde contenido empaquetado que se cargó con un esquema uri ms-appx". | Para obtener más información acerca de lo que se permite en el contexto web, consulta [Características y restricciones por contexto.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9619: "La aplicación no puede navegar a *uri* porque una página en el contexto web no puede ser el documento de nivel superior de la aplicación.  Cargue la página en un iframe en su lugar." | No puedes navegar por la página de nivel superior a una página web remota, pero la aplicación puede mostrar una página web en un [iframe][MDNIframe].  Para obtener más información sobre cómo mostrar contenido web remoto, consulta [Cómo vincular a páginas web externas.][PreviousVersionsWindowsAppsHh780594]  |  

| Error | Observaciones |  
|:--- |:--- |  
| APPHOST9620: "Esta aplicación se cerró porque usaba una conexión HTTP y el elemento meta ms-https-connections-only está presente.  Solo se permiten las conexiones HTTPS cuando se usa el elemento meta ms-https-connections-only.  Use una conexión HTTPS o, si no necesita una conexión segura, quite el elemento meta". | Para obtener más información, [consulta How to require an HTTPS connection][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623: "La aplicación no pudo resolver *la dirección URL* debido a este error: *errorCode*." | Una causa común de este error es un archivo que falta.  |  
| APPHOST9624: "La aplicación no puede usar el script para cargar la dirección *URL* porque la dirección URL inicia otra aplicación.  Solo la interacción directa del usuario puede iniciar otra aplicación". | Las aplicaciones no pueden iniciar otras aplicaciones directamente.  El usuario puede iniciar otras aplicaciones cuando la aplicación implementa determinados contratos.  Para más información, consulta el tema sobre las [extensiones y los contratos entre aplicaciones][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "Se detectó una referencia directa al `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` archivo de recursos.  Esta referencia provoca errores cuando se usa fuera del entorno de depuración". | Debido a la ruta de acceso de archivo de , este archivo PNG se trata como un recurso localizado, lo que provoca el error en que no se puede hacer referencia directamente `logo.scale-140.png` a los recursos localizados.  Consulta [Globalizar la aplicación (HTML)][PreviousVersionsWindowsAppsHh465006] si quieres usar este archivo como un recurso de idioma.  De lo contrario, intente cambiar el nombre del directorio problemático.  |  

## <a name="see-also"></a>Consulte también  

[Use Windows en tiempo de ejecución en JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Uso de Windows Runtime en JavaScript | Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Clase Geolocator | Microsoft Docs"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "addPublicLocalApplicationUri (método) | Microsoft Docs"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Cómo requerir una conexión HTTPS (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Contratos de aplicaciones y extensiones (aplicaciones de Windows Runtime) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Globalización de la aplicación (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Características y restricciones por contexto (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Características y diferencias html, CSS y JavaScript (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Cómo vincular a páginas web externas (HTML) | Microsoft Docs"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: el elemento Frame en línea | MDN"  

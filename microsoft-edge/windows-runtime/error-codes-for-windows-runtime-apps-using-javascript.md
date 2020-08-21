---
title: Códigos de error para aplicaciones de Windows en tiempo de ejecución con JavaScript
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
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
manager: ''
ms.openlocfilehash: 7779da61da9f011e55eeb496c7332e5b7cd5a023
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942155"
---
# Códigos de error para aplicaciones de Windows en tiempo de ejecución con JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Estos son los códigos de error que se muestran en la consola de Microsoft Visual Studio al desarrollar aplicaciones de Windows en tiempo de ejecución con JavaScript.  

| Error | Observaciones |  
|:--- |:--- |  
| APPHOST9601: "no se puede cargar *remoteURI*.  Una aplicación no puede cargar contenido Web remoto en el contexto local. | Para obtener más información sobre lo que se permite en el contexto Web, consulta [características y restricciones por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9602: "' JavaScript: ' es un valor de atributo no válido y se omitirá.  No uses los URI ' JavaScript: ' en el contexto local. " | Por razones de seguridad, no puede usar los URI ' JavaScript: ' en el contexto local.  Para obtener más información sobre lo que se permite en el contexto local, consulta [características y restricciones por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9603: "no se puede cargar el complemento ActiveX con el identificador de clase *classID*.  Las aplicaciones no pueden cargar controles ActiveX. | Las aplicaciones de Windows en tiempo de ejecución que usen JavaScript no admiten Microsoft ActiveXcontrols personalizado.  Si necesitas un control de la interfaz de usuario, usa un control Web estándar, una biblioteca de controles o crea tu propio control personalizado.  Si necesitas realizar una lógica personalizada, crea un objeto personalizado de Windows en tiempo de ejecución en su lugar.  Para obtener información sobre otras diferencias HTML, CSS y JavaScript, consulta [las características y las diferencias de HTML, CSS y JavaScript][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: "no se puede navegar al *URI* porque usa una codificación de caracteres no válida.  Una aplicación solo puede navegar a archivos codificados con UTF8. " | Todo el código HTML, JavaScript y CSS al que tiene acceso Windows Runtime debe codificarse como formato de transformación Unicode de 8 bits (UTF-8).  Para obtener información sobre otras diferencias HTML, CSS y JavaScript, consulta [las características y las diferencias de HTML, CSS y JavaScript][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605: "no se puede navegar a *targetURI* desde *SOURCEURI* porque el URI de destino está en una zona de seguridad superior.  No puede navegar desde una zona con menor seguridad a una zona con mayor seguridad, a menos que vaya a un URI de contexto local de un URI de contexto web y haya registrado el URI del contexto local con el método MSApp. addPublicLocalApplicationUri. | Para obtener más información, consulta [MSApp. addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: "no se puede cargar el *URI* porque usa una conexión http y el elemento meta MS-https-Connections-only está presente.  Solo se permiten conexiones HTTPS cuando se usa el elemento meta MS-https-Connections-only.  Use una conexión HTTPS o, si no necesita una conexión segura, quite el elemento meta. " | Para obtener más información, consulta [Cómo requerir una conexión HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607: "la aplicación no puede iniciar el URI en el *URI* debido a este error: *failureCode*". | Un recurso que falta o un archivo no válido son causas comunes de este error.  |  
| APPHOST9608: "la aplicación no pudo navegar a la página acerca de: en blanco debido a este error: *ErrorCode*." |  |  

| Error | Observaciones |  
|:--- |:--- |  
| APPHOST9610: "la aplicación encontró un error al prepararse para navegar a una página de error personalizada: *ErrorCode*." |  |  
| APPHOST9611: "la aplicación no pudo navegar a una página de error personalizada debido a este error: *ErrorCode*." |  |  
| APPHOST9613: "la aplicación no pudo navegar a *URI*  por este error: *ErrorCode*." |  |  
| APPHOST9614: "un documento dentro de un iframe solicitó el modo de documento *requestedDocMode* , pero el sistema aplica el modo de documento *currentDocMode* .  El iframe usará el modo de documento de *currentDocMode* . " | Para obtener más información sobre cómo mostrar contenido Web remoto, consulte [cómo establecer un vínculo a páginas web externas][PreviousVersionsWindowsAppsHh780594].  |  
| APPHOST9615: "la aplicación no puede descargar el archivo en el *URI* porque se invocó mediante programación fuera del contexto local". | Se produce cuando el contenido del contexto Web intenta descargar un archivo mediante programación.  |  
| APPHOST9616: "este URI no puede usar las API de ubicación geográfica.  Las API de ubicación geográfica solo se pueden invocar desde un URI que forme parte del paquete o esté incluido en el elemento ApplicationContentUris del manifiesto. " | Para obtener más información sobre lo que se permite en el contexto Web, consulta [características y restricciones por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9617: "este URI no puede usar las API del portapapeles.  Las API de Portapapeles solo se pueden invocar desde un URI que forme parte del paquete o esté incluido en el elemento ApplicationContentUris del manifiesto. " | Para obtener más información sobre lo que se permite en el contexto Web, consulta [características y restricciones por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9618: "este URI no puede usar Window. Close.  El método window. Close solo se puede invocar desde contenido empaquetado que se haya cargado con un esquema URI MS-appx. | Para obtener más información sobre lo que se permite en el contexto Web, consulta [características y restricciones por contexto][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9619: "la aplicación no puede navegar a *URI* porque una página en el contexto web no puede ser el documento de nivel superior de la aplicación.  Cargue la página en un iframe en su lugar. " | No puede navegar por la página de nivel superior a una página web remota, pero la aplicación puede mostrar una página web en un [iframe][MDNIframe].  Para obtener más información sobre cómo mostrar contenido Web remoto, consulte [cómo establecer un vínculo a páginas web externas][PreviousVersionsWindowsAppsHh780594].  |  

| Error | Observaciones |  
|:--- |:--- |  
| APPHOST9620: "esta aplicación se cerró porque usó una conexión HTTP y el elemento meta MS-https-Connections-only está presente.  Solo se permiten conexiones HTTPS cuando se usa el elemento meta MS-https-Connections-only.  Use una conexión HTTPS o, si no necesita una conexión segura, quite el elemento meta. " | Para obtener más información, consulta [Cómo requerir una conexión HTTPS][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623: "la aplicación no pudo resolver la *dirección URL* debido a este error: *ErrorCode*." | Una causa común de este error es que falta un archivo.  |  
| APPHOST9624: "la aplicación no puede usar el script para cargar la dirección URL de la *Dirección* URL porque la dirección URL inicia otra aplicación.  Solo la interacción directa del usuario puede iniciar otra aplicación. | Las aplicaciones no pueden iniciar otras aplicaciones directamente.  El usuario puede iniciar otras aplicaciones cuando la aplicación implementa determinados contratos.  Para más información, consulta el tema sobre las [extensiones y los contratos entre aplicaciones][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "se detectó una referencia directa al archivo de recursos `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` .  Esta referencia provoca errores cuando se usa fuera del entorno de depuración. " | Debido a la ruta de acceso del archivo `logo.scale-140.png` , este archivo PNG se trata como un recurso localizado, lo que provoca que no se pueda hacer referencia directamente al error en los recursos localizados.  Vea [globaling Your App (html)][PreviousVersionsWindowsAppsHh465006] si tiene previsto usar este archivo como recurso de idioma.  De lo contrario, intente cambiar el nombre del directorio problemático.  |  

## Consulte también  

[Use Windows en tiempo de ejecución en JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar Windows Runtime en JavaScript | Microsoft docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Clase geolocator | Microsoft docs"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "método addPublicLocalApplicationUri | Microsoft docs"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Cómo requerir una conexión HTTPS (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Contratos y extensiones de aplicaciones (aplicaciones de Windows en tiempo de ejecución) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Globalizar la aplicación (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Características y restricciones por contexto (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Características y diferencias de HTML, CSS y JavaScript (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Cómo establecer un vínculo a páginas web externas (HTML) | Microsoft docs"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> iframe: el elemento marco alineado | MDN"  

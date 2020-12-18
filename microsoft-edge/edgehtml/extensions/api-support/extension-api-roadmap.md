---
description: Buscar información sobre el progreso actual para completar la API de la extensión Microsoft Edge.
title: Guía básica de API de extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, API, extensiones, JavaScript, desarrollador
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d3552fede729a37ff83ac4b19cfadf89d6917a75
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236600"
---
# Guía básica de API de extensión de Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Además de las API Web, la API de extensión permite que las extensiones alcancen una mayor integración con el host del explorador. Esta API proporciona a los desarrolladores acceso a las características del explorador de Microsoft Edge, como la manipulación de pestañas y ventanas. En la siguiente tabla, se detallan las API que se admiten o en desarrollo para Windows 10 compilaciones publicadas de Microsoft Edge de forma pública.


|     Las     |                                                              Descripción                                                              |                Estado: número de compilación                 |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
|   marcadores   |                                          Se usa para crear, organizar y manipular marcadores.                                          | Compatible: Microsoft Edge (40)/Windows 10 (15063) |
| browserAction |                                 Habilita las extensiones para agregar un botón persistente en Microsoft Edge.                                  | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
| comandos      |                                                      Define los métodos abreviados de teclado.                                                      | En consideración
| contextMenus  |                           Agrega un elemento de menú contextual en una dirección URL específica, en el contexto especificado de una página web.                            | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|    cookies    |                                 Se usa para consultar y modificar cookies, así como para notificar cuando cambien.                                 | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|   descargas   |                           Se usa para iniciar, supervisar, manipular y buscar descargas mediante programación.                           |                 En consideración                  |
|   extensiones   |                                      Contiene utilidades que pueden ser usadas por cualquier página de extensiones.                                       | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|    historial    |                                         Interactúa con el registro del explorador de las páginas visitadas.                                         |                 En consideración                  |
|     i18n      |                                         Implementa la internacionalización en una extensión.                                          | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|   identidad    |                                       Se usa para obtener un código de autorización de OAuth2 o un token de acceso.                                       |                 En consideración                  |
|     está      |                                       Se usa para detectar cuándo cambia el estado de inactividad de la máquina.                                        | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|  Administración   |                                              Obtiene información sobre los complementos instalados.                                                |                 En consideración                  |
| notificaciones |                      Permite la creación de notificaciones mediante plantillas que se mostrarán en la bandeja del sistema del usuario.                      | Compatible con Microsoft Edge (42)/Windows 10 (17134) |
|  pageAction   |                                      Permite que las extensiones agreguen un botón en la barra de direcciones.                                       | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|  permisos  |                   Permite a los usuarios seleccionar los permisos opcionales a los que desean conceder acceso a la extensión.                   |                 En consideración                  |
|    motores    | Recupera la página de fondo, devuelve detalles sobre el manifiesto y escucha y responde a los eventos del ciclo de vida de la extensión. | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|    almacenamiento    |                                      Utilizado por la extensión para leer y escribir datos, y para sincronizar datos.                                       | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|     pestañas      |                Interactúa con el sistema de pestañas de Microsoft Edge creando, modificando y reorganizando las pestañas en el explorador.                | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
| navegación en |                           Se usa para recibir notificaciones sobre el estado de las solicitudes de navegación en vuelo.                            | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|  WebRequest   |        Permite el uso de la API de WebRequest para observar y analizar el tráfico y para interceptar, bloquear o modificar solicitudes.        | Compatible: Microsoft Edge (38)/Windows 10 (14393) |
|    windows    |                              Interactúa con el explorador creando, modificando y reorganizando ventanas.                              | Compatible: Microsoft Edge (38)/Windows 10 (14393) |

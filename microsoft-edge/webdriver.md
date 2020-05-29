---
ms.assetid: e56172c0-b635-4c02-8e0c-56bf8cb4c164
description: Aprenda a empezar a usar Webdriver, un protocolo de cable que permite a los programas y scripts controlar el comportamiento del explorador Web.
title: Controlador WebDrive (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, WebDrive, Selenium, pruebas
ms.openlocfilehash: 0a6ef78103852234a6b52dfe88e60273cc3bd3d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574933"
---
# Controlador WebDrive (EdgeHTML)
La API [Webdriver](https://www.w3.org/TR/webdriver/) de W3C es una plataforma e interfaz independiente del idioma y Protocolo de conexión que permite a los programas o las secuencias de comandos controlar el comportamiento de un explorador Web.

Webdriver permite a los desarrolladores crear pruebas automatizadas que simulan la interacción del usuario. Esto es diferente de las pruebas unitarias de JavaScript porque Webdriver tiene acceso a la funcionalidad e información que JavaScript ejecuta en el explorador, y puede simular con más precisión los eventos de usuario o los eventos de nivel de sistema operativo. Webdriver también puede administrar las pruebas en varias ventanas, pestañas y páginas web en una sola sesión de prueba.

A continuación se explica cómo empezar a usar Webdriver para Microsoft Edge (EdgeHTML).

La implementación de Webdriver de Microsoft Edge (EdgeHTML) admite tanto la especificación del [controlador WebDrive](https://www.w3.org/TR/webdriver/) de W3C como el [Protocolo de transmisión de JSON](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol) para la compatibilidad con las pruebas existentes.

## Introducción a Webdriver para Microsoft Edge (EdgeHTML)
* Instala Windows 10.
* Descargue el servidor [Microsoft WebDrive](https://developer.microsoft.com/microsoft-edge/tools/webdriver/) adecuado para su compilación de Windows y Microsoft Edge (EdgeHTML).
* Descargue el enlace de idioma de webdrives que prefiera. [Todos los enlaces de lenguaje Selenium son compatibles con Microsoft Edge (EdgeHTML)](https://docs.seleniumhq.org/download/).

> [!NOTE]
> Puede encontrar ayuda, problemas de informes y solicitudes de características de archivo en la [asistencia & de comentarios de Microsoft Edge (EdgeHTML)](https://developer.microsoft.com/microsoft-edge/support/).


## Uso de Webdriver
Para empezar a usar Webdriver con Microsoft Edge (EdgeHTML), consulte estos ejemplos:

* [C \ # código de ejemplo](https://gist.github.com/InstyleVII/baf25274c55e891076d5#file-webdriver-cs) para abrir una ventana del explorador, vaya a Bing.com y busque "Webdriver" (githuby).

## Indicadores de línea de comandos del servidor Webdriver
Lista de indicadores de la línea de comandos para el servidor Webdriver.

| Nombre    | Descripción                                                                                                      | Versión disponible |
|:--------|:-----------------------------------------------------------------------------------------------------------------|:------------------|
| Hospedaje    | IP de host para usar en el servidor WebDrive (valor predeterminado: localhost)                                                     | 14393             |
| puerto    | Puerto para usar en el servidor WebDrive (valor predeterminado: 17556)                                                            | 14393             |
| package | ApplicationUserModelId (AUMID) para que la aplicación sea iniciada por el servidor WebDrive                        | 14393             |
| detallado | Envía las solicitudes recibidas y las respuestas enviadas por el servidor Webdriver                                             | 14393             |
| silent  | No produce ningún resultado                                                                                                  | 15063             |
| version | Genera la versión de MicrosoftWebDriver. exe.                                                                    | 17763             |
| relativa     | Usar el protocolo Webdriver de W3C (opción predeterminada)                                                                      | 17763             |
| jwp     | Usar protocolo de cable JSON                                                                                           | 17763             |
| Limpie | Limpiar los datos temporales y las claves del registro establecidas por el servidor Webdriver para--. Se omiten otros parámetros | 17763             |

## Webdriver de W3C
Compatibilidad con una base de comandos para la [especificación W3C Webdriver](https://www.w3.org/TR/webdriver/).

### Funcionalidades
| Funcionalidad                       | Key                       | Estado                   | Versión disponible |
|:---------------------------------|:--------------------------|:-------------------------|:------------------|
| Nombre del explorador                     | "browserName"             | Se admite                | 17763             |
| Versión del explorador                  | "browserVersion"          | Se admite                | 17763             |
| Nombre de la plataforma                    | "platformName"            | Se admite                | 17763             |
| Aceptar certificados TLS no seguros | "acceptInsecureCerts"     | No &nbsp; compatible       | N/D               |
| Estrategia de carga de páginas               | "pageLoadStrategy"        | Se admite                | 17763             |
| Configuración de proxy              | servidor                   | No &nbsp; compatible       | N/D               |
| Acotación/posicionamiento de ventanas  | SetWindowRect           | Se admite                | 17763             |
| Configuración de tiempos de espera de sesión   | los tiempos                | Se admite                | 17763             |
| Comportamiento de mensaje no controlado        | "unhandledPromptBehavior" | Parcialmente &nbsp; compatible | 17763             |
| InPrivate                        | "MS: InPrivate"            | Se admite                | 17763             |
| Rutas de extensión                  | "Sra: extensionPaths"       | Se admite                | 17763             |
| Página de inicio                       | "MS: startPage"            | Se admite                | 17763             |

### Estrategias de localizador
| Estrategia del localizador                                                        | Estado    | Versión disponible |
|:------------------------------------------------------------------------|:----------|:------------------|
| [Selectores de CSS](https://www.w3.org/TR/webdriver/#css-selectors)         | Se admite | 17763             |
| [Vincular texto](https://www.w3.org/TR/webdriver/#link-text)                 | Se admite | 17763             |
| [Texto del vínculo parcial](https://www.w3.org/TR/webdriver/#partial-link-text) | Se admite | 17763             |
| [Nombre de etiqueta](https://www.w3.org/TR/webdriver/#tag-name)                   | Se admite | 17763             |
| [Instrucción](https://www.w3.org/TR/webdriver/#xpath)                         | Se admite | 17763             |

### Comandos
| Método HTTP | Plantilla URI                                                   | Comando                                                                                   | Estado             | Versión disponible |
|:------------|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------|:-------------------|:----------------  |
| POST        | /session                                                       | [Nueva sesión](https://www.w3.org/TR/webdriver/#new-session)                               | Se admite          | 17763             |
| DELETE      | identificador de/Session/{Session}                                          | [Eliminar sesión](https://www.w3.org/TR/webdriver/#delete-session)                         | Se admite          | 17763             |
| GET         | /status                                                        | [Estado](https://www.w3.org/TR/webdriver/#status)                                         | Se admite          | 17763             |
| GET         | /Session/{Session ID}/timeouts                                 | [Obtener tiempos de espera](https://www.w3.org/TR/webdriver/#get-timeouts)                             | Se admite          | 17763             |
| POST        | /Session/{Session ID}/timeouts                                 | [Establecer tiempos de espera](https://www.w3.org/TR/webdriver/#set-timeouts)                             | Se admite          | 17763             |
| POST        | /Session/{Session ID}/URL                                      | [Ir a](https://www.w3.org/TR/webdriver/#navigate-to)                               | Se admite          | 17763             |
| GET         | /Session/{Session ID}/URL                                      | [Obtener dirección URL actual](https://www.w3.org/TR/webdriver/#get-current-url)                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/back                                     | [Atrás](https://www.w3.org/TR/webdriver/#back)                                             | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Forward                                  | [Adelante](https://www.w3.org/TR/webdriver/#forward)                                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Refresh                                  | [Actualizar](https://www.w3.org/TR/webdriver/#refresh)                                       | Se admite          | 17763             |
| GET         | /Session/{Session ID}/title                                    | [Obtener título](https://www.w3.org/TR/webdriver/#get-title)                                   | Se admite          | 17763             |
| GET         | /Session/{Session ID}/window                                   | [Controlador de la ventana obtener](https://www.w3.org/TR/webdriver/#get-window-handle)                   | Se admite          | 17763             |
| DELETE      | /Session/{Session ID}/window                                   | [Cerrar ventana](https://www.w3.org/TR/webdriver/#close-window)                             | Se admite          | 17763             |
| POST        | /Session/{Session ID}/window                                   | [Cambiar a ventana](https://www.w3.org/TR/webdriver/#switch-to-window)                     | Se admite          | 17763             |
| GET         | /Session/{Session ID}/window/handles                           | [Obtener identificadores de ventana](https://www.w3.org/TR/webdriver/#get-window-handles)                 | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Frame                                    | [Cambiar a marco](https://www.w3.org/TR/webdriver/#switch-to-frame)                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Frame/Parent                             | [Cambiar al marco principal](https://www.w3.org/TR/webdriver/#switch-to-parent-frame)         | Se admite          | 17763             |
| GET         | /Session/{Session ID}/window/Rect                              | [Obtener ventana rectangular](https://www.w3.org/TR/webdriver/#get-window-rect)                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/window/Rect                              | [Establecer ventana Rect](https://www.w3.org/TR/webdriver/#set-window-rect)                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/window/Maximize                          | [Maximizar ventana](https://www.w3.org/TR/webdriver/#maximize-window)                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/window/miniMIZE                          | [Minimizar ventana](https://www.w3.org/TR/webdriver/#minimize-window)                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/window/Fullscreen                        | [Ventana de pantalla completa](https://www.w3.org/TR/webdriver/#fullscreen-window)                   | No &nbsp; compatible | N/D               |
| GET         | /Session/{Session ID}/Element/Active                           | [Obtener elemento activo](https://www.w3.org/TR/webdriver/#get-active-element)                 | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Element                                  | [Elemento Find](https://www.w3.org/TR/webdriver/#find-element)                             | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Elements                                 | [Buscar elementos](https://www.w3.org/TR/webdriver/#find-elements)                           | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Element/{Element}/Element             | [Buscar elemento desde elemento](https://www.w3.org/TR/webdriver/#find-element-from-element)   | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Element/{Element}/Elements            | [Buscar elementos de un elemento](https://www.w3.org/TR/webdriver/#find-elements-from-element) | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element}/Selected            | [Está elemento seleccionado](https://www.w3.org/TR/webdriver/#is-element-selected)               | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element}/Attribute/{Name}    | [Atributo de elemento Get](https://www.w3.org/TR/webdriver/#get-element-attribute)           | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element}/Property/{Name}     | [Propiedad de elemento obtener](https://www.w3.org/TR/webdriver/#get-element-property)             | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element}/CSS/{Property nombre} | [Valor CSS del elemento Get](https://www.w3.org/TR/webdriver/#get-element-css-value)           | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element ID}/Text                | [Obtener texto de elemento](https://www.w3.org/TR/webdriver/#get-element-text)                     | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element}/Name                | [Nombre de etiqueta del elemento Get](https://www.w3.org/TR/webdriver/#get-element-tag-name)             | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element}/Rect                | [Elemento de obtención](https://www.w3.org/TR/webdriver/#get-element-rect)                     | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Element/{Element}/Enabled             | [Está habilitado para elemento](https://www.w3.org/TR/webdriver/#is-element-enabled)                 | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Element/{Element}/click               | [Clic en elemento](https://www.w3.org/TR/webdriver/#element-click)                           | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Element/{Element}/Clear               | [Elemento borrar](https://www.w3.org/TR/webdriver/#element-clear)                           | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Element/{Element}/sendKeys            | [Teclas de envío de elementos](https://www.w3.org/TR/webdriver/#element-send-keys)                   | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Source                                   | [Obtener origen de página](https://www.w3.org/TR/webdriver/#get-page-source)                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Execute/Sync                             | [Ejecutar script](https://www.w3.org/TR/webdriver/#execute-script)                         | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Execute/Async                            | [Ejecutar script asincrónico](https://www.w3.org/TR/webdriver/#execute-async-script)             | Se admite          | 17763             |
| GET         | /Session/{Session ID}/cookie                                   | [Obtener todas las cookies](https://www.w3.org/TR/webdriver/#get-all-cookies)                       | Se admite          | 17763             |
| GET         | /Session/{Session ID}/cookie/{Name}                            | [Obtener cookie con nombre](https://www.w3.org/TR/webdriver/#get-named-cookie)                     | Se admite          | 17763             |
| POST        | /Session/{Session ID}/cookie                                   | [Agregar cookie](https://www.w3.org/TR/webdriver/#add-cookie)                                 | Se admite          | 17763             |
| DELETE      | /Session/{Session ID}/cookie/{Name}                            | [Eliminar cookie](https://www.w3.org/TR/webdriver/#delete-cookie)                           | Se admite          | 17763             |
| DELETE      | /Session/{Session ID}/cookie                                   | [Eliminar todas las cookies](https://www.w3.org/TR/webdriver/#delete-all-cookies)                 | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Actions                                  | [Realizar acciones](https://www.w3.org/TR/webdriver/#perform-actions)                       | Se admite          | 17763             |
| DELETE      | /Session/{Session ID}/Actions                                  | [Acciones de lanzamiento](https://www.w3.org/TR/webdriver/#release-actions)                       | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Alert/Dismiss                            | [Descartar alerta](https://www.w3.org/TR/webdriver/#dismiss-alert)                           | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Alert/Accept                             | [Aceptar alerta](https://www.w3.org/TR/webdriver/#accept-alert)                             | Se admite          | 17763             |
| GET         | /Session/{Session ID}/Alert/Text                               | [Obtener texto de alerta](https://www.w3.org/TR/webdriver/#get-alert-text)                         | Se admite          | 17763             |
| POST        | /Session/{Session ID}/Alert/Text                               | [Enviar mensaje de alerta](https://www.w3.org/TR/webdriver/#send-alert-text)                       | Se admite          | 17763             |
| GET         | /Session/{Session ID}/screenshot                               | [Capturar captura de pantalla](https://www.w3.org/TR/webdriver/#take-screenshot)                       | Se admite          | 17763             |
| GET         | /Session/{Session ID}/screenshot/{Element}                  | [Captura de pantalla de elemento Take](https://www.w3.org/TR/webdriver/#take-element-screenshot)       | Se admite          | 17763             |

## Protocolo de transmisión por cable JSON
Compatibilidad con cada comando para el [Protocolo de conexión JSON](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol).

### Comandos
| Método HTTP | Ruta de acceso                                                                                                                                                         | Estado             | Versión disponible |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------|:------------------|
| GET         | [/status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#status)                                                                               | Se admite          | 10240             |
| POST        | [/session](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#session-1)                                                                           | Se admite          | 10240             |
| GET         | [/sessions](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessions)                                                                           | Se admite          | 10240             |
| GET         | [/Session/: sessionId](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Se admite          | 10240             |
| DELETE      | [/Session/: sessionId](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionid)                                                         | Se admite          | 10240             |
| POST        | [/Session/: sessionId/timeouts](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeouts)                                        | Se admite          | 10240             |
| POST        | [/Session/: sessionId/timeouts/async_script](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsasync_script)               | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/timeouts/implicit_wait](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtimeoutsimplicit_wait)             | Se admite          | 10586             |
| GET         | [/Session/: sessionId/window_handle](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handle)                              | Se admite          | 10586             |
| GET         | [/Session/: sessionId/window_handles](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow_handles)                            | Se admite          | 10586             |
| GET         | [/Session/: sessionId/URL](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Se admite          | 10240             |
| POST        | [/Session/: sessionId/URL](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidurl)                                                  | Se admite          | 10240             |
| POST        | [/Session/: sessionId/Forward](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidforward)                                          | Se admite          | 10240             |
| POST        | [/Session/: Idsesión/back](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidback)                                                | Se admite          | 10240             |
| POST        | [/Session/: Idsesión/Refresh](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidrefresh)                                          | Se admite          | 10240             |
| POST        | [/Session/: sessionId/Execute](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute)                                          | Se admite          | 10240             |
| POST        | [/Session/: sessionId/execute_async](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidexecute_async)                              | Se admite          | 10586             |
| GET         | [/Session/: sessionId/captura de pantalla](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidscreenshot)                                    | Se admite          | 10240             |
| GET         | [/Session/: sessionId/IME/available_engines](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeavailable_engines)               | No &nbsp; compatible | N/D               |
| GET         | [/Session/: sessionId/IME/active_engine](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactive_engine)                       | No &nbsp; compatible | N/D               |
| GET         | [/Session/: sessionId/IME/activado](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivated)                               | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/IME/Deactivate](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimedeactivate)                             | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/IME/Activate](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidimeactivate)                                 | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Frame](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframe)                                              | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Frame/Parent](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidframeparent)                                 | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Se admite          | 10586             |
| DELETE      | [/Session/: sessionId/Window](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindow)                                            | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Window/: windowHandle/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Window/: windowHandle/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlesize)         | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Window/: windowHandle/Position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Window/: windowHandle/Position](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandleposition) | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Window/: windowHandle/Maximize](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidwindowwindowhandlemaximize) | Se admite          | 10586             |
| GET         | [/Session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Se admite          | 10586             |
| POST        | [/Session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Se admite          | 10240             |
| DELETE      | [/Session/: sessionId/cookie](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookie)                                            | Se admite          | 10586             |
| DELETE      | [/Session/: sessionId/cookie/: nombre](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidcookiename)                                  | Se admite          | 10240             |
| GET         | [/Session/: sessionId/Source](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsource)                                            | Se admite          | 10586             |
| GET         | [/Session/: sessionId}/title](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtitle)                                             | Se admite          | 10240             |
| POST        | [/Session/: sessionId/Element](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelement)                                          | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Elements](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelements)                                        | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Element/Active](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementactive)                             | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Element/: ID](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementid)                                    | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Element/: ID/Element](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelement)                     | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Element/: ID/Elements](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidelements)                   | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Element/: ID/click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclick)                         | Se admite          | 10240             |
| POST        | [/Session/: sessionId/Element/: ID/Submit](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsubmit)                       | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Element/: ID/Text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidtext)                           | Se admite          | 10240             |
| POST        | [/Session/: sessionId/Element/: ID/Value](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidvalue)                         | Se admite          | 10240             |
| POST        | [/Session/: sessionId/Keys](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidkeys)                                                | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Element/: ID/Name](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidname)                           | Se admite          | 10240             |
| POST        | [/Session/: sessionId/Element/: ID/CLEAR](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidclear)                         | Se admite          | 10240             |
| GET         | [/Session/: sessionId/Element/: ID/Selected](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidselected)                   | Se admite          | 10240             |
| GET         | [/Session/: sessionId/Element/: ID/Enabled](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidenabled)                     | Se admite          | 10240             |
| GET         | [/Session/: sessionId/Element/: ID/Attribute/: nombre](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidattribute/:name)     | Se admite          | 10240             |
| GET         | [/Session/: sessionId/Element/: ID/Equals/: Other](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidequals/:other)         | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Element/: ID/mostrado](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementiddisplayed)                 | Se admite          | 10240             |
| GET         | [/Session/: sessionId/Element/: ID/Location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation)                   | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Element/: ID/location_in_view](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidlocation_in_view)   | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Element/: ID/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidsize)                           | Se admite          | 10586             |
| GET         | [/Session/: sessionId/Element/: ID/CSS/:p ropertyName](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidelementidcss/:propertyName) | Se admite          | 10240             |
| GET         | [/Session/: Idsesión/Orientation](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | No &nbsp; compatible | N/D               |
| POST        | [/Session/: Idsesión/Orientation](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidorientation)                                  | No &nbsp; compatible | N/D               |
| GET         | [/Session/: sessionId/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Se admite          | 10240             |
| POST        | [/Session/: sessionId/alert_text](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidalert_text)                                    | Se admite          | 10586             |
| POST        | [/Session/: sessionId/accept_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidaccept_alert)                                | Se admite          | 10240             |
| POST        | [/Session/: sessionId/dismiss_alert](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddismiss_alert)                              | Se admite          | 10240             |
| POST        | [/Session/: sessionId/moveTo](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidmoveto)                                            | Se admite          | 10586             |
| POST        | [/Session/: sessionId/click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidclick)                                              | Se admite          | 10240             |
| POST        | [/Session/: sessionId/buttondown](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttondown)                                    | Se admite          | 10586             |
| POST        | [/Session/: sessionId/buttonup](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidbuttonup)                                        | Se admite          | 10586             |
| POST        | [/Session/: sessionId/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessioniddoubleclick)                                  | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Touch/click](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchclick)                                   | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Touch/Down](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdown)                                     | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Touch/Up](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchup)                                         | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Touch/Move](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchmove)                                     | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Touch/scroll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll)                                 | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Touch/scroll](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchscroll-1)                               | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Touch/DoubleClick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchdoubleclick)                       | No &nbsp; compatible | N/D               |
| POST        | [/Session/: sessionId/Touch/longclick](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchlongclick)                           | No &nbsp; compatible | N/D               |
| POST        | [/Session/: Idsesión/Touch/gesto](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick)                                   | No &nbsp; compatible | N/D               |
| POST        | [/Session/: Idsesión/Touch/gesto](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidtouchflick-1)                                 | No &nbsp; compatible | N/D               |
| GET         | [/Session/: sessionId/Location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Se admite          | 10586             |
| POST        | [/Session/: sessionId/Location](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocation)                                        | Se admite          | 10586             |
| GET         | [/Session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Se admite          | 10586             |
| POST        | [/Session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Se admite          | 10586             |
| DELETE      | [/Session/: sessionId/local_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storage)                              | Se admite          | 10586             |
| GET         | [/Session/: sessionId/local_storage/Key/: clave](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Se admite          | 10586             |
| DELETE      | [/Session/: sessionId/local_storage/Key/: clave](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagekeykey)               | Se admite          | 10586             |
| GET         | [/Session/: sessionId/local_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlocal_storagesize)                     | Se admite          | 10586             |
| GET         | [/Session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Se admite          | 10586             |
| POST        | [/Session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Se admite          | 10586             |
| DELETE      | [/Session/: sessionId/session_storage](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storage)                          | Se admite          | 10586             |
| GET         | [/Session/: sessionId/session_storage/Key/: clave](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Se admite          | 10586             |
| DELETE      | [/Session/: sessionId/session_storage/Key/: clave](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagekeykey)           | Se admite          | 10586             |
| GET         | [/Session/: sessionId/session_storage/size](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidsession_storagesize)                 | Se admite          | 10586             |
| GET         | [/Session/: sessionId/log](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlog)                                                  | No &nbsp; compatible | N/D               |
| GET         | [/Session/: sessionId/log/Types](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidlogtypes)                                       | No &nbsp; compatible | N/D               |
| GET         | [/Session/: sessionId/application_cache/status](https://github.com/SeleniumHQ/selenium/wiki/JsonWireProtocol#sessionsessionidapplication_cachestatus)         | Se admite          | 10586             |  

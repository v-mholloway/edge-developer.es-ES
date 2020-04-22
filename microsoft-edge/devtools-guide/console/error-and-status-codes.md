---
ms.assetid: 961ca575-6b93-4367-a72b-f3f02e5b9568
description: Referencia a códigos comunes de consola y correcciones sugeridas
title: DevTools-códigos de estado y error de la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, códigos de consola
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: aa667941f619dcc0eac2411a087dbdfcf2fda613
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574645"
---
# Códigos de estado y errores de consola  

Esta referencia ayuda a interpretar los mensajes de estado y error de la [consola](../console.md)de DevTools.  Use la tabla siguiente para buscar códigos por su prefijo \ (donde "x" representa un número&ndash;de 0 9 dígitos \):

| Prefijo de código | Área | Descripción |  
|:--- | :--- |:--- |  
| [CSP143xx](#csp-codes) | Directiva de seguridad de contenido | Recursos bloqueados por el uso de `Content-Security-Policy` un encabezado HTTP.  |  
| [CSS31xx](#css-codes) | Hojas de estilos | Errores relacionados con el *formato de fuente abierta web* \ (WOFF \) y los problemas de origen de fuente *OpenType* \ (EOT \) y servidor host.  |  
| [HTML1112-1300](#html-codes) | HTML | La mayoría son códigos heredados específicos de conceptos de Microsoft Internet Explorer, como el *modo de documento* y la *vista de compatibilidad*.  |  
| [HTML1400-1532](#html5-parser-warnings) | Análisis de HTML5 | Advertencias de validación iniciadas por el analizador de HTML5.  |  
| [HTTP](#http-codes) | Errores y estado del servidor | Códigos devueltos de los servidores remotos en respuesta a las solicitudes HTTP.  |  
| [SCRIPT10xx](#javascript-syntax-errors) | Errores de sintaxis de JavaScript | Se produce cuando la estructura de una de las instrucciones de JavaScript infringe una o más de las reglas sintácticas.  |  
| [SCRIPT50xx](#javascript-run-time-errors) | Errores en tiempo de ejecución de JavaScript | Se produce cuando el script intenta realizar una acción que el sistema no puede ejecutar.  |  
| [SEC71xx](#security-codes) | Seguridad | Refleja las condiciones de seguridad que Microsoft Edge aplica, como el *contenido mixto* y la *protección de rastreo*.  |  
| [SVG560x](#svg-codes) | Gráficos vectoriales escalables |  La amplia depuración de SVG no es compatible actualmente, pero se proporcionan algunos mensajes de la consola para fines de depuración.  |  
| WebGL11_xxx | WebGL | Mensajes de error del contexto WebGL.  Consulte también [errores de GLSL](https://msdn.microsoft.com/library/dn611835.aspx).  |  
| [XML5xxx](#xml-codes) | XML | Errores en el análisis y validación de XML.  |  

## Códigos CSP  

Los recursos bloqueados por el uso `Content-Security-Policy` de un encabezado HTTP se notifican a través de la consola de DevTools y, opcionalmente, como un informe al servidor.

| Código | Mensaje | Descripción | Corrección sugerida |
|:--- |:--- |:--- |:--- |
| CSP14301 | "Error al analizar el \ [tipo de directiva \] porque \ <el motivo de cancelación de la operación \ >--se omitirá la Directiva." | Error en el tipo de directiva de seguridad especificado \ (por ejemplo, script-src, base-URI \) por la razón identificada y se omitirá.  | Asegúrese de que se enumeran todos los recursos necesarios de un tipo específico en una sola directiva.  Por ejemplo, en `script-src https://host1.com; script-src https://host2.com`, se omitirá la segunda Directiva.  La siguiente es correctamente especifica ambos orígenes como válidos: `script-src https://host1.com https://host2.com`.  |
| CSP14302 | "Error al analizar el origen en \ [tipo de directiva \] para la Directiva \ [tipo de directiva \] en \ [URL de origen \]--se omitirá el origen."                                                         | La mayoría de las directivas CSP requieren uno o varios orígenes de contenido \ (que indican una dirección URL en la que se puede cargar el contenido \).  Este error señala una directiva con una directiva que contiene una dirección URL de origen que produjo un error cuando se intentó analizar.  | Compruebe el origen de contenido \ (normalmente una dirección URL \) que se define en la Directiva especificada, que puede encontrar en el tipo de directiva especificado.  Corrija o reemplace la dirección URL de origen o quite la Directiva.  <br /> *\ * La Directiva debe incluir una directiva de directiva predeterminada src, que es una reserva para otros tipos de recursos cuando no tienen directivas propias.* |
| CSP14303 | "La Directiva [tipo de directiva] estaba vacía". | El tipo de directiva \ (por ejemplo, Content-Security-Policy en el encabezado HTTP \) está vacío.  | Puede encontrar una referencia rápida para configurar una política de seguridad de contenido en [http://content-security-policy.com](http://content-security-policy.com).  |
| CSP14304 | "Origen desconocido \ [URL de origen \] para la Directiva \ [tipo de directiva \] en \ [tipo de directiva \] origen se omitirá". | Los orígenes del contenido \ (Safe \) de la Directiva identificada son desconocidos y se pasarán por alto.  | Compruebe el origen de contenido identificado \ (a menudo es una dirección URL \) para asegurarse de que es correcta.  |
| CSP14305 | "No se admite el origen \ [URL de origen \] para la Directiva [tipo de directiva] en \ [tipo de directiva \] origen se omitirá". | El origen \ (URL, palabra clave o datos) enumerado en esta Directiva no es compatible y se ignorará.  | La dirección del sitio de origen puede incluir un carácter comodín inicial opcional \ (el carácter `*`asterisco, \).  Por ejemplo, http://`*`. foo.com o mail.foo.com: *.  Los hosts están delimitados por espacios.  Los orígenes también pueden ser palabras clave \ (ninguno, autolínea no segura e evaluación no segura son compatibles \) \ (datos: Uri, MediaStream: URI \).  |
| CSP14306 | "No se proporcionan orígenes para la Directiva \ [tipo de directiva \] para \ [tipo de directiva \]--Esto equivale a usar" ninguno "y evitará la descarga de todos los recursos de este tipo". | Otorgar una directiva y no incluir ningún origen para que el contenido seguro pueda obtener acceso es lo mismo que no permitir que se descarguen los recursos del tipo especificado en la Directiva.  | Un origen puede ser uno o más nombres de host de Internet o direcciones IP, así como un esquema de dirección URL opcional o un número de puerto.  |
| CSP14307 | Ya se ha proporcionado "source [Source URL] para la Directiva \ [tipo de directiva \] para \ [tipo de directiva \]". | Un origen \ (URL, palabra clave o datos \) duplicado se ha incluido en la lista de la Directiva y se ignorará.  | Quite el origen duplicado identificado.  |
| CSP14308 | "Error al analizar la Directiva en \ [tipo de directiva \] en [nombre de la Directiva]." | Error en la Directiva identificada.  Para obtener instrucciones sobre cómo escribir las directivas admitidas [http://content-security-policy.com](http://content-security-policy.com/), consulte.  | Las directivas deben estar separadas por punto y coma.  Por ejemplo, si tiene una aplicación que carga todos sus recursos desde una red de entrega de contenido \ (por ejemplo, `https://cdn.example.net`\) y sabe que no necesita contenido enmarcado o complementos, la Directiva podría tener el siguiente aspecto: `Content-Security-Policy: default-src https://cdn.example.net; child-src 'none'; object-src 'none'.` *\ * mientras se separan las directivas con punto y coma, los orígenes dentro de una directiva solo se deben separar con un espacio.* |
| CSP14309 | "Directiva desconocida en \ [nombre de la Directiva \] en \ [tipo de directiva \]--se omitirá la Directiva". | La directiva establecida en la Directiva CSP es desconocida y se omitirá.  | Para obtener una lista de las directivas admitidas, consulte [http://content-security-policy.com](http://content-security-policy.com/).  |
| CSP14310 | "Directiva no compatible [nombre de la Directiva] en \ [tipo de directiva]--se omitirá la Directiva". | Se encontró una directiva durante el análisis en el tipo de directiva \ (por ejemplo `Content-Security-policy-Report-Only` , el campo de encabezado \) que no es compatible y se omitirá.  Para las directivas compatibles, [http://content-security-policy.com](http://content-security-policy.com/)consulte.  | Quite la Directiva no admitida.  **Nota**: algunas directivas no se admiten en el elemento \ <meta \ > o en `Content-Security-policy-Report-Only` el campo de encabezado.  |
| CSP14311 | "La Directiva \ [nombre de directiva \] ya se ha proporcionado en \ [tipo de directiva \]--se pasará por alto la directiva duplicada." | Se encontró una directiva duplicada durante el análisis, se omitirán la segunda Directiva y sus expresiones de origen.  | Quite el script duplicado.  |
| CSP14312 | "Recurso infringido (Directiva) [nombre de la Directiva] en [tipo de directiva]: [URI de destino].  El recurso se bloqueará. " | En este ejemplo: "secuencia de comandos de" recurso infringido ": origen MS-appx: datos: ' Unsafe-eval ' en la Directiva definida por el host: script en línea.  El recurso se bloqueará. " | Se bloqueó un script en línea \ (URI de destino \) debido a `'script-src ms-appx: data: 'unsafe-eval'` la Directiva de la Directiva ' definido por el host '.  <br /> Los autores necesitan mover todo el script y estilo en línea porque el agente de usuario no puede determinar si un atacante ha insertado una secuencia de comandos en línea.  Quite el script en línea y colóquelo en un archivo externo.  |
| CSP14313 | "Recurso infringido (Directiva) [nombre de la Directiva] en [tipo de directiva]: [URI de destino].  El recurso no se bloqueará debido a la Directiva de solo informes. | Se identificó un recurso que infringe la Directiva especificada en el `Content-Security-policy-Report-Only` campo de encabezado.  Como está en un `Report-Only` tipo de Directiva, el recurso no se bloqueará.  | Mueva la Directiva a un campo de encabezado de seguridad de contenido si este recurso debe estar bloqueado para proteger su sitio.  |
| CSP14314 | "No se pudo enviar el informe de infracción de directivas a [destino URI de destino] porque [motivo de cancelación de la operación]." | Hubo un problema con la notificación de una infracción de la Directiva, el destino al que se ha designado el informe y el motivo por el que no se ha enviado.  | La `report-uri` Directiva especifica una dirección URL en la que un explorador enviará informes cuando se infrinja una directiva de seguridad de contenido.  *\ * No se puede usar en las etiquetas de \ <meta \ >.* |
| CSP14315 | "No se pudo aplicar la Directiva de espacio aislado en [tipo de directiva] porque [motivo de cancelación de la operación]." | Error en la Directiva de espacio aislado por las razones especificadas.  Esta directiva impone restricciones en las acciones que puede llevar a cabo la página, en lugar de hacerlo en los recursos que se pueden cargar.  Si la Directiva de espacio aislado está presente, la página se trata como si se hubiera cargado dentro de un iframe.  Puede evitar los elementos emergentes y los complementos y la ejecución de scripts de bloque.  | Mantenga el valor de espacio aislado vacío para mantener todas las restricciones impuestas o `allow-forms`agregue `allow-same-origin`valores `allow-scripts`:, `allow-top-navigation`, y.  *\ * La Directiva de espacio aislado no se admite en el elemento \ <meta \ > o `Content-Security-policy-Report-Only` en el campo de encabezado.* |
| CSP14316 | "Se permite la evaluación de scripts debido a la suplantación de host". | Cuando se incluye `script-src` la `default-src` Directiva o o, la secuencia de comandos `eval()` en línea se deshabilita, `unsafe-inline` a `unsafe-eval`menos que se especifique and, respectivamente.  | `'unsafe-eval'` permite el uso de `eval()` métodos similares para crear código a partir de cadenas.  Debes incluir las comillas simples.  ***Nota**: esta no es segura y puede abrir su sitio web para detectar vulnerabilidades de scripting entre sitios. * |
| CSP14317 | "Se permite el fotograma [nombre de origen] a causa de la invalidación de host". | Se permitió el marco de origen identificado debido a un conjunto de anulación de la Directiva de CSP de host.  | Una Directiva puede contener una expresión de origen nonce, lo que significa que la fuente solo se puede usar en una ocasión, y el servidor debe generar un valor actualizado para la Directiva cada vez que transmita una directiva.  Nonces invalidan las restricciones de la Directiva en la que están presentes.  |

> [!NOTE]
> En el caso de los sitios web de la zona de seguridad de confianza de un usuario, Microsoft Edge no comprueba el tipo MIME de una hoja de estilos.  

## Códigos CSS  

Estos errores se encuentran en el formato de CSS31xx y están relacionados con el *formato de fuente abierto Web* \ (WOFF \) y los problemas de origen de fuente *OpenType* \ (EOT \) y de servidor de host.  

| Código | Mensaje | Descripción | Corrección sugerida |
|:--- |:--- |:--- |:--- |
| CSS3111 | "error desconocido de la cara @font" | Se ha encontrado un problema desconocido con "web Open Font Format \ (WOFF \)", y "Embedded OpenType Font \ (EOT \)" de la fuente \ hoja de estilos en cascada \ (CSS \).  | Comprobar el origen de las fuentes WOFF.  Pruebe la fuente o el origen de la fuente alternativa para ver si puede reproducir el problema.  |
| CSS3112 | "error en la comprobación de integridad del WOFF @font" | La fuente del formato de fuente abierta web \ (WOFF \) podría estar dañada, incompleta o no es el formato correcto.  | Comprobar el origen de las fuentes.  Pruebe una fuente o fuente de fuente de buen estado para ver si puede reproducir el problema.  |
| CSS3113 | "no coincide @font cara entre el origen del documento y la cadena de raíz del EOT" | La fuente no se puede usar porque la dirección URL \ (rootstring \) en la fuente OpenType \ (EOT \) incrustada no coincide con el dominio del documento con la fuente.  | La suma de comprobación de la dirección URL en el EOT rootstring podría ser incorrecta, lo que indica una dirección URL dañada o modificada para la fuente.  Asegúrese de que la fuente tiene licencia o tiene permisos para el sitio web en el que se está usando.  |
| CSS3114 | comprobación de los permisos "@font de la incrustación de OpenType con error".  El permiso debe ser instalable. | La cara de la fuente no tiene permisos para instalar con la página web actual.  | Obtenga el permiso o las licencias correctos para incrustar la fuente.  |
| CSS3115 | "@font-Face no puede cargar una fuente OpenType no válida". | El tipo de letra de la fuente no es válido para este uso.  | Obtener el permiso o las licencias para la fuente de la fuente actual y la válida.  |
| CSS3116 | "error en la solicitud de origen cruzado del" rostro @font.  Sin encabezado Access-Control-Allow-Origin " | Es posible que la fuente no esté configurada para el acceso entre dominios.  | La fuente no sirve desde el mismo origen que el documento.  Asegúrese de que el hospedaje que atiende la fuente permite el uso de esta fuente mediante el encabezado HTTP "Access-Control-Allow-Origin".                        |
| CSS3117 | "error en la solicitud de origen cruzado del" rostro @font.  El acceso a recursos está restringido. " | Es posible que el encabezado "Access-Control-Allow-Origin" no esté configurado correctamente o que la fuente no permita que la página use esta fuente.  | Asegúrese de que el recurso tiene los permisos correctos y un encabezado de respuesta HTTP configurado correctamente que tiene el origen de acceso entre dominios del host que atiende las fuentes.  |
| CSS3118 | "No se pudo crear una nueva hoja de estilos.  Hay más de \ [máximo \] hojas de estilo en el documento. " | Microsoft Edge ha creado más de 4095 objetos de hoja de estilos durante el proceso de procesamiento de la página.  | Puede ser un proceso de JavaScript fuera de control o un error del sistema de compilación.  Reduzca el número de objetos de hoja de estilos que se generan.  |
| CSS3119 | "La consulta multimedia: el estado MS-View ha quedado obsoleto.  -las consultas multimedia de estado de MS-View pueden modificarse o no estar disponibles para las versiones posteriores a Windows 8,1.  En su lugar, use las consultas Max-width y min-width. " | Su CSS contiene una `-ms-view-state` consulta de medios.  | Use Max-width y min-width.  |

## Códigos HTML

Estos códigos tienen el formato HTML1xxx, como HTML1115.  Muchos de estos son códigos heredados específicos de conceptos de Internet Explorer, como el *modo de documento* y la *vista de compatibilidad*  

| Código | Mensaje | Descripción | Corrección sugerida |  
| :--- |:--- |:--- |:--- |  
| HTML1112 | "Reinicio de página de códigos desde \ [Encoding \] por \ [Encoding \]" | Se especificó una página de códigos que difiere de la página de códigos del servidor.  | Use la misma página de códigos que el servidor para evitar este error.  |  
| HTML1113 | "Modo documento restar from \ [Mode \] to \ [Mode \]" | La página web requiere un modo de documento diferente al del explorador actualmente configurado.  | Este mensaje puede aparecer cuando el usuario se desplaza desde otra página, y lo saca del control del desarrollador.  |  
| HTML1114 | "CodePage \ [Encoding \] de \ [Domain \] invalida la página de códigos en conflicto \ [Encoding \] de \ [Domain \]" | Las páginas de código especificadas en los encabezados HTTP \ (de servidor \) y \ \ (en-página \) difieren unas de otras.  | Cambiar una para que coincidan.  |  
| HTML1115 | "Etiqueta META compatible con X-UA \ (`[META tag]`\) omitida porque el modo documento ya está finalizado" | Normalmente, la etiqueta META se colocó después de una declaración "script" o "style", que recorrigió el modo de documento de la página.  | Mueva la etiqueta META compatible con X-UA a la fase inicial del encabezado, como sea posible.  Es una buena práctica ponerlo inmediatamente después de \ <title \ > y el valor de charset.  |  
| HTML1116 | "Etiqueta META compatible con x-UA \ (`[META tag]`\) omitida debido a una etiqueta meta de x-UA-compatible`[META tag]`anterior \ (\)" | Hay más de una etiqueta "X-UA-compatible" "META" en la sección \ <Head \ > del código fuente.  | Quite todas las etiquetas META ' X-UA-compatible, excepto una, y asegúrese de que es lo más temprano posible en el encabezado.  Una buena práctica es colocarla inmediatamente después de los \ <title \ > y el valor de charset.  |  
| HTML1121 | "Página de códigos \ [codificación \] no está permitida, solo se permite la página de códigos \ [codificación \]." | El contenido de la página web ha invocado una codificación de caracteres no permitida en este contexto.  | Asegúrese de que todo el contenido usa la codificación permitida que se especifica en el mensaje.  |  
| HTML1122 | "Internet Explorer se está ejecutando en modo de empresa, emulando IE8" | La página se está representando actualmente en modo de empresa, que es una emulación de Windows Internet Explorer 8.  | Este modo lo configura la administración de TI para sitios específicos.  Si un usuario individual tiene que desactivarlo en una página web, desactive la opción modo de empresa en el menú herramientas.  Para obtener más información sobre la administración del modo de empresa, consulte la [documentación de ti](https://technet.microsoft.com/library/dn640687.aspx).  |  
| HTML1201 | "`[domain]` es un sitio web que ha agregado a la vista de compatibilidad." | El usuario ha seleccionado el botón **vista de compatibilidad** para el sitio web actual o lo ha agregado a través de la configuración de vista de **compatibilidad**.  | Iniciada por el usuario.  |  
| HTML1202 | "`[domain]` se está ejecutando en la vista de compatibilidad porque está activada la opción" Mostrar sitios de la intranet en la vista de compatibilidad ". | El usuario ha seleccionado la casilla **Mostrar sitios de intranet en la vista de compatibilidad** en la configuración de la vista de **compatibilidad**.  | El usuario debe presionar ALT + T, seleccionar la configuración de la **vista de compatibilidad**y, a continuación, desactivar la casilla **Mostrar sitios de intranet en vista de compatibilidad** .  |  
| HTML1203 | "`[domain]` se ha configurado para ejecutarse en la vista de compatibilidad mediante la Directiva de grupo." | El administrador de red especificó que la página web se ejecutará en la vista de compatibilidad.  | Debe ponerse en contacto con el administrador de la red.  |  
| HTML1204 | "`[domain]` se está ejecutando en la vista de compatibilidad porque está activada la opción" Mostrar todos los sitios web en la vista de compatibilidad ". | El usuario ha activado la casilla de verificación **Mostrar todos los sitios web en la vista de compatibilidad** en la configuración de la **vista de compatibilidad**.  | El usuario debe presionar ALT + T, seleccionar la configuración de la **vista de compatibilidad**y, a continuación, desactivar la casilla de verificación **Mostrar todos los sitios web en vista de compatibilidad** .  |  
| HTML1300 | "Navegación" | Se navegó a una página nueva o se actualizó la página actual.  | Este es un mensaje informativo, no un error.  |  

## Advertencias del analizador de HTML5  

Las advertencias siguientes pueden ocurrir como parte de la validación realizada durante el análisis de HTML.  Estas advertencias no necesariamente significan que una página está dañada, pero que el código HTML proporcionado no es válido según el estándar HTML5.  Es posible que el contenido creado en conformidad con versiones anteriores de las especificaciones HTML o XHTML no sea válido en HTML5, especialmente en relación con el uso de DOCTYPEs.

Estas advertencias suelen indicar caracteres que faltan o adicionales y etiquetas no coincidentes.  Al resolver estas advertencias, debería mejorar la compatibilidad con exploradores anteriores y la compatibilidad de una página web con el estándar de HTML5.  Para ayudar a identificar el origen de una advertencia, incluye información de desplazamiento de caracteres y líneas, junto con un vínculo que apunta a la ubicación en la que se encontró el problema.

| Código     | Mensaje |  
| :--- |:--- |  
| HTML1400 | "Carácter inesperado al principio de la referencia de caracteres numéricos.  Se esperaba [0-9]. " |  
| HTML1401 | "Carácter inesperado al principio de la referencia de caracteres numéricos hexadecimales.  Expect ED [0-9], [a-f] o [A-F]. " |  
| HTML1402 | "La referencia de caracteres no tiene un punto y coma final"; "." |  
| HTML1403 | "La referencia a caracteres numéricos no se resuelve como un carácter válido". |  
| HTML1404 | "Referencia de caracteres con nombre no reconocida". |  
| HTML1405 | "Carácter no válido: U + 0000 NULL.  No se deben usar caracteres nulos. " |  
| HTML1406 | "Inicio de etiqueta no válido: \ < \?.  Los signos de interrogación no deben iniciar etiquetas. |  
| HTML1407 | "Nombre de etiqueta no válido.  El primer carácter debe coincidir con [a-zA-Z]. " |  
| HTML1408 | "Etiqueta final no válida \ </\ >.  Las etiquetas finales no deben estar vacías. |  
| HTML1409 | "Carácter de nombre de atributo no válido.  Los nombres de atributo no deben contener \ (\ "\), \ (\ ' \), \ (\ < \) o \ (= \)." |  
| HTML1410 | "Valor de atributo sin comillas no válido.  Los valores de atributo sin comillas no deben contener \ (\ "\), \ (\ ' \), \ (\ < \), \ (= \) o \ (\ ' \)." |  
| HTML1411 | "Final de archivo inesperado". |  
| HTML1412 | "Comentario mal formado.  Los comentarios deberían comenzar por \ < \!--\ >. " |  
| HTML1413 | "Carácter inesperado: U + 003E mayor que el signo \ (\ > \)" |  
| HTML1414 | "Carácter inesperado: signo de exclamación de U + 0021 \ (\! \)" |  
| HTML1415 | "Carácter inesperado: U + 002D guión-menos \ (-\)" |  
| HTML1416 | "Carácter inesperado en el extremo del comentario.  Se esperaba "--\ >". " |  
| HTML1417 | "DOCTYPE vacío.  El doctype más corto es \ < \! DOCTYPE HTML \ > ". |  
| HTML1418 | "Carácter inesperado en DOCTYPE". |  
| HTML1419 | "Palabra clave inesperada en DOCTYPE.  Se esperaba "PUBLIC" o "SYSTEM". " |  
| HTML1420 | "Presupuesto inesperado después de la palabra clave" PUBLIC "o" SYSTEM ".  Espacio en blanco esperado. " |  
| HTML1421 | "Etiqueta final incorrecta.  Las etiquetas finales no deben contener atributos. |  
| HTML1422 | "Etiqueta inicial mal formada.  Una barra diagonal de autocierre debe ir seguida de un signo mayor que U + 003E superior a \ (\ > \). " |  
| HTML1423 | "Etiqueta inicial mal formada.  Los atributos deben estar separados por espacios en blanco ". |  
| HTML1424 | "Carácter no válido" |  
| HTML1500 | "La etiqueta no puede ser autoidentificable.  Usar una etiqueta de cierre explícita. |  
| HTML1501 | "Final de archivo inesperado". |  
| HTML1502 | "DOCTYPE inesperado.  Solo se permite un DOCTYPE y debe aparecer antes de cualquier elemento. " |  
| HTML1503 | "Etiqueta de apertura inesperada". |  
| HTML1504 | "Etiqueta final inesperada". |  
| HTML1505 | "Token de caracteres inesperado". |  
| HTML1506 | "Token inesperado". |  
| HTML1507 | "Carácter inesperado: U + 0000 NULL.  No se deben usar caracteres nulos. " |  
| HTML1508 | "Etiqueta final no coincidentes". |  
| HTML1509 | "Etiqueta final no coincidentes". |  
| HTML1510 | "Nodos requeridos fuera de ámbito". |  
| HTML1511 | "Se encontró un elemento de nivel de cabezal inesperado fuera de \ <Head \ >". |  
| HTML1512 | "Etiqueta final no coincidentes". |  
| HTML1513 | "Extra \ <HTML \ etiqueta de >  Solo debe existir una etiqueta \ <HTML \ > por documento. " |  
| HTML1514 | Se encontró la etiqueta "extra \ <cuerpo \ >.  Solo debe existir una etiqueta \ <cuerpo \ > por documento ". |  
| HTML1515 | "Se encontró \ <FRAMESET \ > demasiado abajo en el documento.  Esta etiqueta debe ocurrir antes de que se cree un \ <cuerpo \ >. " |  
| HTML1516 | "Anidamiento no válido.  Una etiqueta de encabezado como \ <H1 \ > o \ <H2 \ > no debe colocarse dentro de otra etiqueta de encabezado. " |  
| HTML1517 | "Anidamiento no válido.  Una etiqueta \ <formulario \ > no debe colocarse dentro de otra \ <formulario \ > ". |  
| HTML1518 | "Anidamiento no válido.  Una etiqueta \ <Button \ > no debe colocarse dentro de otro \ <botón \ >. |  
| HTML1519 | "Anidamiento no válido.  Una etiqueta \ <a \ > no debe colocarse dentro de otra \ <de \ >. |  
| HTML1520 | "Etiqueta de apertura inesperada: el elemento \ <de ISINDEX \ > está obsoleto y no debe usarse". |  
| HTML1521 | "Inesperado \ </body\ > o final del archivo.  Todos los elementos abiertos deben cerrarse antes del final del documento. |  
| HTML1522 | "Etiqueta final no válida: \ </br\ >.  Usa \ <br \ > o \ <br/\ > en su lugar. " |  
| HTML1523 | "Etiqueta de cierre superpuesto.  Las etiquetas deben estar estructuradas como \ <b \ > \ <i \ > \ </i\ > \ </b\ > en lugar de \ <b \ > \ <i \ > \ < > \ </i\ >. " |  
| HTML1524 | "DOCTYPE no válido.  El doctype más corto es \ < \! DOCTYPE HTML \ > ". |  
| HTML1525 | "Se encontró una etiqueta HTML inesperada en el contenido externo \ (MathML/SVG \)". |  
| HTML1526 | "Anidamiento no válido.  Una etiqueta \ <nobr \ > no debe colocarse dentro de otra \ <nobr \ >. |  
| HTML1527 | "Se esperaba DOCTYPE.  El doctype más corto es \ < \! DOCTYPE HTML \ > ". |  
| HTML1528 | "\ <imagen \ > en contenido HTML.  Usa \ <IMG \ > en su lugar. " |  
| HTML1529 | "Valor de atributo xmlns: XLink no válido.  El valor debe ser "\ <https://w3.org/1999/xlink\>". " |  
| HTML1530 | "Se ha encontrado texto en un elemento de tabla estructural.  El texto de la tabla solo se puede colocar dentro de \ <Caption \ >, \ <TD \ > o \ <º \ > los elementos. " |  
| HTML1531 | "Valor de atributo xmlns no válido.  Para los elementos SVG, el valor debe ser " https://w3.org/2000/svg/\>\ <". " |  
| HTML1532 | "Valor de atributo xmlns no válido.  Para los elementos de MathML, el valor debe ser https://w3.org/1998/Math/MathML/\>"\ <".  |  

## Códigos HTTP  

Los códigos de error HTTP son devueltos por los servidores remotos en respuesta a las solicitudes.  Probablemente el más familiar es HTTP404, que se devuelve cuando el servidor no puede encontrar la página o el documento especificados en el identificador de recursos uniforme \ (URI \).

| Código | Mensaje | Descripción |  
| :--- |:--- |:--- |  
| HTTP400 | SOLICITUD INCORRECTA | El servidor no pudo procesar la solicitud porque la sintaxis no es válida.  |  
| HTTP401 | DENEGADO | El recurso solicitado requiere autenticación de usuario.  |  
| HTTP402 | PAGO OBLIGATORIO | Actualmente no está implementado en el protocolo HTTP.  |  
| HTTP403 | PERMITIDO | El servidor entendió la solicitud pero no lo cumplió.  |  
| HTTP404 | NO ENCONTRADO | El servidor no ha encontrado ninguna coincidencia con el URI solicitado.  |  
| HTTP405 | MÉTODO INCORRECTO | El verbo HTTP usado no está permitido.  |  
| HTTP406 | NINGUNA ACEPTABLE | No se encontraron respuestas aceptables para el cliente.  |  
| HTTP407 | AUTENTICACIÓN DE PROXY OBLIGATORIA | Se requiere autenticación de proxy.  |  
| HTTP408 | SOLICITAR TIEMPO DE ESPERA | El servidor ha agotado el tiempo de espera de la solicitud.  |  
| HTTP409 | CONTRADICTORIO | No se pudo completar la solicitud debido a un conflicto con el estado actual del recurso.  |  
| HTTP410 | VACACIONES | El recurso solicitado ya no está disponible en el servidor y no se conoce ninguna dirección de reenvío.  |  
| HTTP411 | LONGITUD REQUERIDA | El servidor no acepta la solicitud sin una longitud de contenido definida.  |  
| HTTP412 | ERROR EN LA CONDICIÓN PREVIA | La condición previa proporcionada en uno o varios de los campos de encabezado de la solicitud se evaluó como false cuando se probó en el servidor.  |  
| HTTP413 | CARGA DEMASIADO GRANDE | El servidor no puede procesar una solicitud porque la entidad de solicitud es más grande de lo que el servidor está dispuesto o capaz de procesar.  |  
| HTTP414 | URI DEMASIADO LARGO | El servidor rechaza la solicitud porque el URI de la solicitud es más largo del que el servidor está dispuesto a interpretar.  |  
| HTTP415 | TIPO DE MEDIO NO ADMITIDO | El servidor rechaza la solicitud porque la entidad de la solicitud está en un formato que no es compatible con el recurso solicitado para el método solicitado.  |  
| HTTP416 | EL RANGO SOLICITADO NO SATISFIABLE | El servidor no puede proporcionar la parte del archivo que el cliente ha solicitado.  La parte puede extenderse más allá del final del archivo.  |  
| HTTP417 | ERROR DE EXPECTATIVA | El servidor no puede cumplir los requisitos del campo de encabezado de solicitud Expect.  |  
| HTTP418 | ENVIAR UN TEAPOT | El servidor es un TEAPOT; no puede cerveza café.  |  
| HTTP419 | TIEMPO DE ESPERA DE AUTENTICACIÓN | La autenticación anterior válida ha expirado.  |  
| HTTP422 | ENTIDAD NO PROCESABLE | La solicitud ha sido correcta pero no se pudo procesar debido a errores semánticos.  |  
| HTTP423 | BLOQUE | El recurso al que se está accediendo está bloqueado.  |  
| HTTP424 | DEPENDENCIA FALLIDA | Error en la solicitud debido al error de una solicitud anterior.  |  
| HTTP426 | ACTUALIZACIÓN NECESARIA | El cliente debe cambiar a otro protocolo.  |  
| HTTP428 | CONDICIÓN PREVIA REQUERIDA | El servidor de origen requiere que la solicitud sea condicional.  |  
| HTTP429 | DEMASIADAS SOLICITUDES | El servidor se niega a atender la solicitud porque el cliente envió demasiadas solicitudes.  |  
| HTTP431 | LOS CAMPOS DE ENCABEZADO DE SOLICITUD SON DEMASIADO GRANDES | El servidor rechaza la solicitud porque un campo de encabezado o todos los campos de encabezado colectivamente son mayores de lo que el servidor está dispuesto o capaz de procesar.  |  
| HTTP449 | REINTENTAR CON | Debe volver a intentarse la solicitud después de tomar la acción adecuada.  |  
| HTTP500 | ERROR DE SERVIDOR | El servidor encontró una condición inesperada que le impidió completar la solicitud.  |  
| HTTP501 | NO COMPATIBLE | El servidor no es compatible con la funcionalidad requerida para completar la solicitud.  |  
| HTTP502 | PUERTA DE ENLACE INCORRECTA | El servidor, mientras actuaba como puerta de enlace o proxy, recibió una respuesta no válida del servidor que precede en la cadena al que acpidió para completar la solicitud.  |  
| HTTP503 | SERVICIO NO DISPONIBLE | El servicio está sobrecargado temporalmente.  |  
| HTTP504 | TIEMPO DE ESPERA DE GATEWAY | Se agotó el tiempo de espera de la solicitud mientras se esperaba una puerta de enlace.  |  
| HTTP505 | VERSIÓN NO ADMITIDA | El servidor no admite o rechaza la versión del protocolo HTTP que se usó en el mensaje de solicitud.  |  
| HTTP506 | LA VARIANTE TAMBIÉN NEGOCIA | La negociación de contenido transparente para la solicitud dio como resultado referencias circulares.  |  
| HTTP507 | ALMACENAMIENTO INSUFICIENTE | El servidor no puede almacenar la representación necesaria para completar la solicitud.  |  
| HTTP508 | BUCLE DETECTADO | El servidor ha detectado un bucle infinito durante el servicio de la solicitud.  |  
| HTTP510 | NO AMPLIADO | El servidor necesita más extensiones para la solicitud.  |  
| HTTP511 | AUTENTICACIÓN DE RED OBLIGATORIA | El cliente debe autenticarse para obtener acceso a la red.  |  

## Errores de sintaxis de JavaScript  

Los errores de sintaxis de JavaScript se producen cuando la estructura de una de las instrucciones infringe una o más de las reglas sintácticas.  

| Número de error | Descripción |  
| --- | --- |  
| 1019 | [No puede haber ' break ' fuera de un bucle](/scripting/javascript/misc/can-t-have-break-outside-of-loop) |  
| 1020 | [No puede haber ' Continue ' fuera de un bucle](/scripting/javascript/misc/can-t-have-continue-outside-of-loop) |  
| 1030 | [La compilación condicional está desactivada](/scripting/javascript/misc/conditional-compilation-is-turned-off) |  
| 1027 | [' default ' solo puede aparecer una vez en una instrucción ' switch '](/scripting/javascript/misc/default-can-only-appear-once-in-a-switch-statement) |  
| 1005 | [Se esperaba ' \ ('](/scripting/javascript/misc/expected-left-parenthesis-javascript) |  
| 1006 | [Se esperaba ' \) '](/scripting/javascript/misc/expected-right-parenthesis-javascript) |  
| 1012 | [Se esperaba '/'](/scripting/javascript/misc/expected-minus) |  
| 1003 | [Se esperaba ': '](/scripting/javascript/misc/expected-colon) |  
| 1004 | [Se esperaba '; '](/scripting/javascript/misc/expected-semicolon) |  
| 1032 | [Se esperaba ' @ '](/scripting/javascript/misc/expected-at) |  
| 1029 | [Se esperaba ' @end '](/scripting/javascript/misc/expected-at-end) |  
| 1007 | [Se esperaba ' \] '](/scripting/javascript/misc/expected-right-square-bracket) |  
| 1008 | [Se esperaba ' {'](/scripting/javascript/misc/expected-left-curly-brace) |  
| 1009 | [Se esperaba '} '](/scripting/javascript/misc/expected-right-curly-brace) |  
| 1011 | [Se esperaba ' = '](/scripting/javascript/misc/expected-equal-javascript) |  
| 1033 | [Se esperaba ' Catch '](/scripting/javascript/misc/expected-catch) |  
| 1031 | [Constante esperada](/scripting/javascript/misc/expected-constant) |  
| 1023 | [Se esperaba un dígito hexadecimal](/scripting/javascript/misc/expected-hexadecimal-digit) |  
| 1010 | [Identificador esperado](/scripting/javascript/misc/expected-identifier-javascript) |  
| 1028 | [Se esperaba un identificador, una cadena o un número](/scripting/javascript/misc/expected-identifier-string-or-number) |  
| 1024 | [Se esperaba ' while '](/scripting/javascript/misc/expected-while) |  
| 1014 | [Carácter no válido](/scripting/javascript/misc/invalid-character-javascript) |  
| 1026 | [Etiqueta no encontrada](/scripting/javascript/misc/label-not-found) |  
| 1025 | [Etiqueta redefinida](/scripting/javascript/misc/label-redefined) |  
| 1018 | [la instrucción ' Return ' está fuera de la función](/scripting/javascript/misc/return-statement-outside-of-function) |  
| 1002 | [Error de sintaxis](/scripting/javascript/misc/syntax-error-javascript) |  
| 1035 | [Iniciar debe ir seguido de una expresión en la misma línea de origen](/scripting/javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line) |  
| 1016 | [Comentario no terminado](/scripting/javascript/misc/unterminated-comment) |  
| 1015 | [Constante de cadena no terminada](/scripting/javascript/misc/unterminated-string-constant-javascript) |  
  
### Errores de script host  

Los siguientes errores se aplican al host de script, pero es posible que se muestren ocasionalmente:  
  
| Error | HRESULT | Descripción |  
| ---| --- | --- |  
| SCRIPT_E_RECORDED | 0x86664004 | Se grabó un error y pasó entre el motor de script y el host.  El anfitrión debe pasar el código de error a la persona que llama.  |  
| SCRIPT_E_REPORTED | 0x80020101 | El motor de scripts ha notificado una excepción no controlada al host a través de IActiveScriptSite:: OnScriptError.  El anfitrión puede ignorar este error.  |  
| SCRIPT_E_PROPAGATE | 0x8002010 | Un error de script que se propague a la persona que llama puede estar en un subproceso diferente.  El anfitrión debe pasar el código de error a la persona que llama.  |  

## Errores en tiempo de ejecución de JavaScript

Los errores en tiempo de ejecución de JavaScript se producen cuando el script intenta realizar una acción que el sistema no puede ejecutar.  Es posible que vea errores en tiempo de ejecución cuando se evalúan expresiones variables o cuando se asigna memoria.

| Número de error | Descripción |  
| --- | --- |  
| 4 | [Acceso denegado](/scripting/javascript/misc/access-is-denied) |  
| 438 | [El objeto no admite esta propiedad o método](/scripting/javascript/misc/object-doesn-t-support-this-property-or-method) |  
| 1001 | Memoria insuficiente |  

### Errores de Windows Runtime  

 Si usas las API \ (WinRT \) de Windows Runtime, es posible que veas errores de JavaScript que se hayan convertido de los HRESULT de Windows Runtime.  Los HRESULTs de Windows Runtime en el intervalo de sobre 0x80070000 se convierten en errores de JavaScript al tomar el valor hexadecimal de los bits bajos y convertirlo en un decimal.  Por ejemplo, el HRESULT 0x80070032 se convierte en el valor decimal 50, y el error de JavaScript es SCRIPT50.  El HRESULT 0x80074005 se convierte en el valor decimal 16389 y el error de JavaScript es SCRIPT16389.

| Número de error | Descripción |  
| --- | --- |  
| 5029 | [La longitud de la matriz debe ser un entero positivo finito](/scripting/javascript/misc/array-length-must-be-a-finite-positive-integer) |  
| 5030 | [La longitud de la matriz debe tener un número positivo finito](/scripting/javascript/misc/array-length-must-be-assigned-a-finite-positive-number) |  
| 5028 | [Se esperaba un objeto Array o arguments](/scripting/javascript/misc/array-or-arguments-object-expected) |  
| 5010 | [Se esperaba booleano](/scripting/javascript/misc/boolean-expected) |  
| 5003 | [No se puede asignar al resultado de una función](/scripting/javascript/misc/cannot-assign-to-a-function-result) |  
| 5000 | [No se puede asignar a ' this '](/scripting/javascript/misc/cannot-assign-to-this) |  
| 5034 | [Referencia circular en argumento de valor no compatible](/scripting/javascript/misc/circular-reference-in-value-argument-not-supported) |  
| 5006 | [Se esperaba un objeto de fecha](/scripting/javascript/misc/date-object-expected) |  
| 5015 | [Se esperaba un objeto enumerador](/scripting/javascript/misc/enumerator-object-expected) |  
| 5022 | [Excepción iniciada y no detectada](/scripting/javascript/misc/exception-thrown-and-not-caught) |  
| 5020 | [Se esperaba ') ' en una expresión regular](/scripting/javascript/misc/expected-right-parenthesis-in-regular-expression-javascript) |  
| 5019 | [Se esperaba ' &#93; ' en una expresión regular](/scripting/javascript/misc/expected-right-square-bracket-in-regular-expression-javascript) |  
| 5023 | [La función no tiene un objeto prototipo válido](/scripting/javascript/misc/function-does-not-have-a-valid-prototype-object) |  
| 5002 | [Se esperaba una función](/scripting/javascript/misc/function-expected) |  
| 5008 | [Asignación ilegal](/scripting/javascript/misc/illegal-assignment-javascript) |  
| 5021 | [Rango no válido en el conjunto de caracteres](/scripting/javascript/misc/invalid-range-in-character-set-javascript) |  
| 5035 | [Argumento de reemplazador no válido](/scripting/javascript/misc/invalid-replacer-argument) |  
| 5014 | [Objeto de JavaScript esperado](/scripting/javascript/misc/javascript-object-expected) |  
| 5001 | [Se esperaba un número](/scripting/javascript/misc/number-expected) |  
| 5007 | [Objeto esperado](/scripting/javascript/misc/object-expected) |  
| 5012 | [Miembro de objeto esperado](/scripting/javascript/misc/object-member-expected) |  
| 5016 | [Se esperaba un objeto de expresión regular](/scripting/javascript/misc/regular-expression-object-expected) |  
| 5005 | [Se esperaba una cadena](/scripting/javascript/misc/string-expected) |  
| 5017 | [Error de sintaxis en expresión regular](/scripting/javascript/misc/syntax-error-in-regular-expression-javascript) |  
| 5026 | [El número de dígitos fraccionarios está fuera del rango](/scripting/javascript/misc/the-number-of-fractional-digits-is-out-of-range) |  
| 5027 | [La precisión está fuera del rango](/scripting/javascript/misc/the-precision-is-out-of-range) |  
| 5025 | [El URI que se va a descodificar no es una codificación válida](/scripting/javascript/misc/the-uri-to-be-decoded-is-not-a-valid-encoding) |  
| 5024 | [El URI que se va a codificar contiene un carácter no válido.](/scripting/javascript/misc/the-uri-to-be-encoded-contains-an-invalid-character) |  
| 5009 | [Identificador no definido](/scripting/javascript/misc/undefined-identifier) |  
| 5018 | [Cuantificador inesperado](/scripting/javascript/misc/unexpected-quantifier-javascript) |  
| 5013 | [Se esperaba VBArray](/scripting/javascript/misc/vbarray-expected) |  

## Códigos de seguridad

Los códigos de error de seguridad `SEC7xxx` tienen el formato, `SEC7113`como.  Estos errores reflejan condiciones de seguridad que Microsoft Edge aplica, como el contenido mixto y la protección de rastreo.

| Código | Mensaje | Descripción | Corrección sugerida |  
| :--- |:--- |:--- |:--- |  
| SEC7111 | "Seguridad HTTPS comprometida por [nombre del recurso]" | Una página de protocolo de transferencia de hipertexto seguro \ (HTTPS \) tiene contenido de un origen no seguro.  | Asegúrese de que todo el contenido de la página, incluidos los scripts, los objetos de hoja de estilos y las imágenes, sea de orígenes HTTPS.  |  
| SEC7112 | "La secuencia de comandos de [URL] se bloqueó debido a un error de coincidencia de tipo MIME" | El encabezado de respuesta HTTP del archivo JavaScript especificado por la dirección URL tiene un encabezado "X-Content-Type-Options: nosniffing" y no tiene una declaración de tipo de contenido reconocido.  | Actualice el servidor para enviar el tipo de contenido correcto para el archivo de JavaScript \ (como texto/JavaScript, aplicación/JavaScript ", por ejemplo \) en el encabezado de respuesta HTTP.  Para obtener más información y una lista completa de los tipos de contenido, consulte [cambios en el procesamiento de MIME en Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7113 | "Se omitió el CSS debido a que el tipo MIME no coincide" | No se usó una hoja de estilos importada porque se encontraba un tipo MIME incorrecto en el encabezado HTTP.  | Asegúrese de que el archivo de hoja de estilos se entregue con el encabezado de respuesta HTTP correcto, que incluye un tipo de contenido de texto o CSS.  Para obtener más información, consulta [cambios en el control de MIME en Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7114 | "Una descarga de esta página fue bloqueada por la protección de rastreo. [Dirección URL proporcionada aquí] " | El usuario bloqueó un script o contenido mediante la protección de rastreo.  | Ninguno: usuario iniciado.  |  
| SEC7115 | ": visitado y: los estilos de vínculo solo pueden diferir por color.  Algunos estilos no se aplicaron a: visitado. | Se han cambiado más de un atributo, como la fuente o el tamaño, usando los estilos visitados y vinculados.  | Cambiar solo el atributo de color.  |  
| SEC7116 | "Acceso denegado.  Error al revocar la dirección URL de origen cruzado: [URL]. | Un script que tiene un sitio de origen diferente que el BLOB ha intentado revocar una dirección URL de BLOB.  Debido a las directivas de origen de BLOB, no se pudo realizar el intento.  | Asegúrese de que todas las direcciones URL de BLOB se revocan mediante scripts del mismo sitio de origen que el documento que creó la dirección URL del BLOB.  |  
| SEC7120 | "El origen [dominio] no se encuentra en el encabezado Access-Control-Allow-Origin". | En la respuesta a XMLHttpRequest, el encabezado Access-Control-Allow-Origin se devolvió con un valor que no contiene ni coincide con el valor de origen del sitio.  | El recurso devuelve el tipo correcto de códigos de encabezado pero no permite su sitio.  Póngase en contacto con el desarrollador encargado del recurso y pídale que actualice su encabezado Access-Control-Allow-Origin para que se permita su sitio.  Puede dirigirlos a [CORS para XHR en IE10](https://blogs.msdn.microsoft.com/ie/2012/02/09/cors-for-xhr-in-ie10/) para obtener más información sobre CORS en los encabezados de respuesta.  |  
| SEC7121 | "No se permite el comodín en Access-Control-Allow-Origin cuando la marca de credenciales está establecida en true". | El servidor devuelve "Access-Control-Allow-Origin: *" en los encabezados, pero esto no está permitido cuando la `withCredentials` marca está establecida en **true** en XMLHttpRequest.  | El controlador del lado del servidor debe modificarse para que devuelva un encabezado Access-Control-Allow-Origin que permita específicamente su punto de origen en este tipo de solicitud.  Si no controla el controlador del lado del servidor, tendrá que hablar con el desarrollador que lo hace.  |  
| SEC7122 | "La marca de credencial se estableció como true, pero Access-Control-Allow-Credentials no estaba presente o no se estableció en" true ". | Se realizó una XMLHttpRequest mediante la `withCredentials` bandera.  Un encabezado Access-Control-Allow-Credentials no se devolvió o se devolvió con un valor distinto de **true**.  | Es posible que haya un problema con sus credenciales o con la respuesta del servidor.  Consulte la [especificación de nivel 2 de XMLHttpRequest](https://w3.org/TR/XMLHttpRequest2/) para obtener información sobre las solicitudes de credenciales.  |  
| SEC7123 | "El encabezado de solicitud [encabezado] no estaba presente en la lista Access-Control-Allow-Heads". | Se incluyó un tipo de encabezado personalizado en la solicitud, pero la lista Access-Control-Allow-headers de la respuesta no la incluía.  | Asegúrese de que el servidor permite encabezados personalizados y permite específicamente que el envío se envíe en la solicitud.  |  
| SEC7124 | "El método de solicitud [método] no estaba presente en la lista Access-Control-Allow-Methods". | Se usó un método de solicitud, como publicación, en XMLHttpRequest, pero la respuesta devolvió un encabezado Access-Control-Allow-Methods que no lo incluía.  | Asegúrese de que el servidor permite este tipo de método de solicitud y de que está `withCredentials` usando correctamente si ese método tiene acceso restringido.  |  
| SEC7125 | "XMLHttpRequest para [URL] causó un error de análisis de los encabezados de respuesta". | No se pudieron analizar los encabezados de respuesta del servidor, por lo que no se pudo realizar la solicitud.  | Use la [herramienta red](https://msdn.microsoft.com/library/dn255004.aspx) para capturar e inspeccionar los encabezados de respuesta para asegurarse de que cumplen con las [Especificaciones de CORS](https://w3.org/TR/cors/).  |  
| SEC7126 | "No se permiten redireccionamientos para solicitudes de comprobaciones preparatorias de CORS". | Se ha detectado una redirección en el encabezado de origen y el agente de usuario no seguirá las redirecciones durante una comprobación previa.  | Use la [herramienta red](https://msdn.microsoft.com/library/dn255004.aspx) para capturar e inspeccionar los encabezados de la solicitud y asegurarse de que hay un único origen directo.  |  
| SEC7127 | "Se bloqueó el redireccionamiento para la solicitud de CORS". | La ruta de acceso al recurso de CORS contenía una redirección que infringe las reglas de seguridad.  | Asegúrese de que tiene la ruta de acceso más directa al recurso de CORS en su XMLHttpRequest.  |  
| SEC7128 | "No se permiten varios encabezados Access-Control-Allow-Origin para la respuesta de CORS". | El encabezado de la respuesta incluía varios encabezados Access-Control-Allow-Origin.  | Este es un error del servidor.  El servidor debe devolver un único encabezado Access-Control-Allow-Origin.  Notificar este error al desarrollador encargado del recurso del lado del servidor.
| SEC7129 | "No se permiten varios encabezados Access-Control-Allow-Credentials para la respuesta de CORS". | El encabezado de la respuesta contenía varios encabezados Access-Control-Allow-Credentials.  | Este es un error del servidor.  El servidor debe devolver un único encabezado Access-Control-Allow-Credentials.  Notificar este error al desarrollador encargado del recurso del lado del servidor.  |  
| SEC7130 | "Se detectó un posible scripting entre sitios en [URL].  El contenido ha sido modificado por el filtro XSS. " | El [filtro XSS](https://msdn.microsoft.com/library/dd565647.aspx) detectó contenido potencialmente malintencionado en la respuesta del recurso y quitó el contenido ofensivo.  | Más información sobre el [filtro XSS](https://msdn.microsoft.com/library/dd565647.aspx).  |  
| SEC7131 | "La seguridad de un iframe de espacio aislado puede verse comprometida al permitir el acceso a secuencias de comandos y el mismo origen". | Si el contenido de un iframe de espacio aislado proviene de un origen no confiable o no seguro, podría escapar el recinto de seguridad cuando se permita el acceso al script y al mismo origen.  | Este es un mensaje de advertencia informativo y no debería afectar a la funcionalidad.  Le recomendamos que evite combinar estos permisos a menos que esté seguro de qué se ejecutará en el iframe.  |  
| SEC7132 | "El certificado que protege este sitio Web usa criptografía débil" | El certificado de seguridad TLS usado por este sitio Web usa criptografía débil | Actualizar el certificado TLS del servidor |  

> [!NOTE]
> En el caso de los sitios web de la zona de seguridad de confianza de un usuario, Microsoft Edge no comprueba el tipo MIME de una hoja de estilos.

## Códigos SVG  

DevTools actualmente no admite la depuración de gráficos vectoriales ampliables escalables \ (SVG \), pero se proporcionan algunos mensajes de la consola para ayudar con la depuración.

| Código | Mensaje | Descripción | Corrección sugerida |  
| :--- |:--- |:--- |:--- |  
| SVG5601 | "La ruta de acceso a SVG tiene un formato incorrecto y no se pudo analizar por completo". | La cadena de la [ruta de acceso](https://msdn.microsoft.com/library/ff972086.aspx) SVG no tiene el formato correcto o contiene comandos no reconocidos.  | Compruebe el formato de los comandos.  |  
| SVG5602 | "La lista de puntos SVG tiene un formato incorrecto y no se pudo analizar por completo". | La lista de puntos que se usa para un elemento, como una [polilínea](https://msdn.microsoft.com/library/ff972113.aspx), tiene un formato incorrecto.  | Asegúrese de que los puntos estén completos y tengan el formato correcto para el sistema de coordenadas de los usuarios.  |  

## Códigos XML  

Los códigos XML tienen el formato XML5xxx, como XML5603.  

| Código | Mensaje |  
|:--- |:--- |  
| XML5001 | "Aplicando el control integrado de XSLT". |  
| XML5601 | "MX_E_MX" |  
| XML5602 | "Final de entrada inesperado". |  
| XML5603 | "Codificación no reconocida". |  
| XML5604 | "No se puede cambiar la codificación". |  
| XML5605 | "Firma de codificación de entrada no reconocida". |  
| XML5606 | "WC_E_WC" |  
| XML5607 | "Espacio en blanco esperado" |  
| XML5608 | "Se esperaba punto y coma". |  
| XML5609 | "Esperado" > "." |  
| XML5610 | "Se esperaba un carácter de Comillas". |  
| XML5611 | "Expected" = "." |  
| XML5612 | "No se permite el carácter < en los valores de atributos". |  
| XML5613 | "Se esperaba un dígito hexadecimal". |  
| XML5614 | "Se esperaba un dígito decimal". |  
| XML5615 | "Esperado" ["." |  
| XML5616 | "Expected" ("." |  
| XML5617 | "Carácter XML no válido". |  
| XML5618 | "Carácter de nombre no válido". |  
| XML5619 | "Sintaxis de documento incorrecta". |  
| XML5620 | "Sintaxis de sección CDATA incorrecta". |  
| XML5621 | "Sintaxis de comentarios incorrecta". |  
| XML5622 | "Sintaxis de sección condicional incorrecta". |  
| XML5623 | "Sintaxis de declaración ATTLIST incorrecta". |  
| XML5624 | "Sintaxis de declaración DOCTYPE incorrecta". |  
| XML5625 | "Sintaxis de declaración de elemento incorrecta". |  
| XML5626 | "Sintaxis de declaración de entidad incorrecta". |  
| XML5627 | "Sintaxis de declaración NOTATION incorrecta". |  
| XML5628 | "Se esperaba" NDATA "." |  
| XML5629 | "Se esperaba" PUBLIC "." |  
| XML5630 | "Sistema esperado". " |  
| XML5631 | "Nombre no válido". |  
| XML5632 | "Solo se permite un elemento raíz". |  
| XML5633 | "El nombre de la etiqueta final no coincide con el nombre de la etiqueta inicial correspondiente". |  
| XML5634 | "Ya existe un atributo con el mismo nombre en este elemento". |  
| XML5635 | "Solo se permite una declaración XML al principio del archivo". |  
| XML5636 | "XML inicial". " |  
| XML5637 | "Sintaxis de declaración de texto incorrecta". |  
| XML5638 | "Sintaxis de declaración XML incorrecta". |  
| XML5639 | "Sintaxis de nombre de codificación incorrecta". |  
| XML5640 | "Sintaxis de identificador público incorrecta". |  
| XML5641 | "No se permiten referencias de entidad de parámetro dentro de declaraciones de marcado en un subconjunto DTD interno". |  
| XML5642 | "El texto de sustitución para las referencias de entidad de parámetro que se usan entre las declaraciones de marcado debe contener una serie de declaraciones de marcado completas". |  
| XML5643 | "Una entidad analizada no debe contener una referencia directa o indirecta a sí misma." |  
| XML5644 | "El contenido de la entidad especificada no es correcto". |  
| XML5645 | "La entidad especificada no se ha declarado". |  
| XML5646 | "La referencia de entidad no puede contener el nombre de una entidad sin analizar". |  
| XML5647 | "Los valores de atributo no deben contener referencias directas o indirectas a entidades externas". |  
| XML5648 | "Sintaxis de la instrucción de procesamiento incorrecta". |  
| XML5649 | "Sintaxis incorrecta del identificador del sistema". |  
| XML5650 | "Se esperaba un signo de interrogación \ (\? \)." |  
| XML5651 | "El delimitador CDATA-Section-Close"]] > "no debe usarse en el contenido del elemento". |  
| XML5652 | "No se han leído todos los fragmentos de datos". |  
| XML5653 | "Se encontró una DTD, pero está prohibido." |  
| XML5654 | "Atributo XML: Space encontrado con un valor no válido.  Los valores válidos son "preserve" o "default". " |  
| XML5655 | "NC_E_NC" |  
| XML5656 | "Carácter de nombre completo no válido". |  
| XML5657 | "Varios signos de dos puntos": "no deben aparecer en un nombre completo." |  
| XML5658 | "Un signo de dos puntos": "no debe aparecer en un nombre." |  
| XML5659 | "Prefijo declarado". |  
| XML5660 | "El prefijo especificado no se ha declarado". |  
| XML5661 | "Las declaraciones de espacios de nombres no predeterminadas no deben tener un URI vacío." |  
| XML5662 | "El prefijo" XML "está reservado y debe tener el URI<https://w3.org/XML/1998/namespace/>" "." |  
| XML5663 | "El prefijo" xmlns "está reservado para su uso por XML". |  
| XML5664 | "El URI del espacio de nombres XML \ https://w3.org/XML/1998/namespace/\>\) (\ <solo debe asignarse al prefijo" XML "." |  
| XML5665 | "El URI del espacio de nombres xmlns \ https://w3.org/2000/xmlns/\>\) (\ <está reservado y no debe usarse". |  
| XML5666 | "SC_E_SC" |  
| XML5667 | "Se ha superado la profundidad máxima de elementos anidados." |  
| XML5668 | "Se ha superado el número máximo de expansiones de entidad". |  
| XML5669 | "WR_E_WR" |  
| XML5670 | "WR_E_NONWHITESPACE: redactor: la cadena especificada no es un espacio en blanco." |  
| XML5671 | "WR_E_NSPREFIXDECLARED: redactor: el prefijo del espacio de nombres ya está declarado con un espacio de nombres diferente". |  
| XML5672 | "WR_E_NSPREFIXWITHEMPTYNSURI: redactor: no se puede usar un prefijo con un URI de espacio de nombres vacío". |  
| XML5673 | "WR_E_DUPLICATEATTRIBUTE: redactor: atributo duplicado". |  
| XML5674 | "WR_E_XMLNSPREFIXDECLARATION: redactor: no se puede volver a definir el prefijo xmlns." |  
| XML5675 | El prefijo "WR_E_XMLPREFIXDECLARATION: redactor: XML debe tener el https://w3.org/XML/1998/namespace/\> URI \ <". |  
| XML5676 | "WR_E_XMLURIDECLARATION: redactor: el URI del espacio de nombres XML https://w3.org/XML/1998/namespace/\>\) \ (\ <debe asignarse solo al prefijo" XML "." |  
| XML5677 | "WR_E_XMLNSURIDECLARATION: redactor: el espacio de nombres URI \ ( https://w3.org/2000/xmlns/\>\) \ <está reservado y no debe usarse". |  
| XML5678 | "WR_E_NAMESPACEUNDECLARED: redactor: no se ha declarado el espacio de nombres." |  
| XML5679 | "WR_E_INVALIDXMLSPACE: redactor: valor no válido de atributo XML: Space \ (los valores permitidos son" default "y" preserve "\)". |  
| XML5680 | "WR_E_INVALIDACTION: redactor: la realización de la acción solicitada daría lugar a un documento XML no válido". |  
| XML5681 | "WR_E_INVALIDSURROGATEPAIR: redactor: Input contiene un par suplente no válido o incompleto". |  
| XML5682 | "Carácter inesperado en la entidad de caracteres.  Se esperaba un dígito decimal. " |  
| XML5683 | "Carácter inesperado en la entidad de caracteres.  Se esperaba un dígito hexadecimal. " |  
| XML5684 | "El valor Unicode de la entidad de caracteres especificada no es válido". |  
| XML5685 | "Codificación no válida". |  
| XML5686 | "Error de XML no especificado". |  

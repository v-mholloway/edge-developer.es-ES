---
ms.assetid: 961ca575-6b93-4367-a72b-f3f02e5b9568
description: Referencia a códigos de consola y correcciones sugeridas comunes
title: 'DevTools: códigos de estado y error de la consola'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas F12, DevTools y códigos de consola
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: da9facaa65b2bd2403d454c2041e2ad30dfcd112
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236618"
---
# Códigos de estado y error de la consola  

Esta referencia te ayudará a interpretar mensajes de estado y error de la consola de [DevTools](../console.md).  Usa la tabla siguiente para buscar códigos por el prefijo \(donde "x" representa un número de 0&ndash;9 dígitos\):

| Prefijo del código | Área | Descripción |  
|:--- | :--- |:--- |  
| [CSP143xx](#csp-codes) | Directiva de seguridad de contenido | Recursos bloqueados por el uso de un encabezado HTTP `Content-Security-Policy`.  |  
| [CSS31xx](#css-codes) | Hojas de estilos | Errores relacionados con origen de fuente y servidor host del *Formato de fuente abierta web* \(WOFF\) y *OpenType incrustado* \(EOT\).  |  
| [HTML1112-1300](#html-codes) | HTML | La mayoría son códigos heredados específicos de los conceptos de Microsoft Internet Explorer, como Modo de documento y la *Vista de compatibilidad*.  |  
| [HTML1400-1532](#html5-parser-warnings) | Análisis de HTML5 | Advertencias de validación iniciadas por el analizador de HTML5.  |  
| [HTTP](#http-codes) | Estado y errores del servidor | Códigos que devuelven los servidores remotos en respuesta a solicitudes HTTP.  |  
| [SCRIPT10xx](#javascript-syntax-errors) | Errores de sintaxis de JavaScript | Se producen cuando la estructura de una de las instrucciones de JavaScript infringe una o varias de las reglas sintácticas.  |  
| [SCRIPT50xx](#javascript-run-time-errors) | Errores de tiempo de ejecución de JavaScript | Se producen cuando el script intenta realizar una acción que el sistema no puede ejecutar.  |  
| [SEC71xx](#security-codes) | Seguridad | Refleja las condiciones de seguridad que exige Microsoft Edge, como Contenido mixto y la *Protección de seguimiento*.  |  
| [SVG560x](#svg-codes) | Scalable Vector Graphics |  Actualmente, no se ofrece una depuración extensa de SVG, pero se proporcionan algunos mensajes de consola para propósitos de depuración.  |  
| WebGL11_xxx | WebGL | Mensaje de error de un contexto de WebGL.  Consulta también [Errores de GLSL](https://msdn.microsoft.com/library/dn611835.aspx).  |  
| [XML5xxx](#xml-codes) | XML | Errores en el análisis y validación de XML.  |  

## Códigos CSP  

Los recursos bloqueados mediante el uso de un encabezado HTTP `Content-Security-Policy` se notifican a través de la consola de DevTools y, opcionalmente, se muestran como un informe al servidor.

| Código | Mensaje | Descripción | Corrección propuesta |
|:--- |:--- |:--- |:--- |
| CSP14301 | "Error al analizar el \[tipo de directiva\] porque se omitirá la directiva \<the reason for canceling the operation\>". | Se produjo un error en el tipo de directiva de seguridad especificado \(por ejemplo, script-src, base-uri\) por el motivo identificado y se ignorará.  | Asegúrate de que enumera todos los recursos necesarios de un tipo específico en una única directiva.  Por ejemplo, en `script-src https://host1.com; script-src https://host2.com`, se pasará por alto la segunda directiva.  Esta es la forma correcta de especificar ambos orígenes como válidos: `script-src https://host1.com https://host2.com`.  |
| CSP14302 | "Se produjo un error al analizar el origen en \[tipo de directiva\] para la directiva \[tipo de directiva\] en \[URL de origen\]. El origen se pasará por alto".                                                         | La mayoría de las directivas CSP requieren uno o más orígenes de contenido \(que indican una dirección URL desde la que se puede cargar el contenido\).  Este error señala una directiva que contiene una dirección URL de origen que dio errores cuando se intentó analizar.  | Comprueba el origen de contenido \(normalmente, una dirección URL\) definida en la directiva especificada que puede encontrar en el tipo de directiva especificado.  Corrige o cambia la dirección URL de origen o quítala.  <br /> *\*La directiva debe incluir una directiva predeterminada src, que es un recurso alternativo para otros tipos de recursos que no tienen directivas propias.* |
| CSP14303 | "La directiva [tipo de directiva] está vacía". | El tipo de directiva \(por ejemplo, la directiva de seguridad de contenido del encabezado HTTP\) está vacío.  | Puedes encontrar una referencia rápida para configurar una directiva de seguridad de contenido en [http://content-security-policy.com](http://content-security-policy.com).  |
| CSP14304 | "El origen desconocido \[URL de origen\] para la directiva \[tipo de directiva\] en origen \[tipo de directiva\] se pasará por alto". | Los orígenes de contenido \(seguro\) aprobados en las directivas identificadas son desconocidos y se pasarán por alto.  | Comprueba el origen de contenido identificado \(normalmente se trata de una dirección URL\) para asegurarse de que es correcto.  |
| CSP14305 | "El origen incompatible \[URL de origen\] para la directiva \[tipo de directiva\] en origen \[tipo de directiva\] se pasará por alto". | La \(dirección URL, palabra clave o datos\) de origen en esta directiva no son compatibles y se pasarán por alto.  | Es posible que la dirección del sitio de origen incluya un carácter comodín inicial opcional \(el asterisco, `*`\).  Por ejemplo, http://`*`.foo.com o mail.foo.com:*.  Los hosts tienen un espacio limitado.  Los orígenes también pueden ser palabras clave \(none, self, unsafe-inline y unsafe-eval son compatibles\), o datos \(data:URIs, mediastream:URIs\).  |
| CSP14306 | "No se proporcionó ningún origen para la directiva \[tipo de directiva\] para\ [tipo de directiva\]. Esto equivale al uso de "none" y evitará la descarga de todos los recursos de este tipo". | Conceder una directiva y no incluir ninguna fuente de contenido seguro para tener acceso equivale a no permitir la descarga de los recursos del tipo especificado en la directiva.  | Un origen puede ser uno o más nombres de host de Internet o direcciones IP, así como un esquema de URL o un número de puerto opcionales.  |
| CSP14307 | "El origen [URL fuente] ya se ofreció para la directiva \[tipo de directiva\] para \[tipo de directiva\]". | Se ha indicado un origen duplicado \(dirección URL, una palabra clave o datos\) en esta directiva, por lo que se pasarán por alto.  | Quitar el origen duplicado identificado.  |
| CSP14308 | "Se produjo un error al analizar la directiva en \[tipo de directiva\] en [nombre de directiva]". | Se ha producido un error en la directiva identificada.  Para obtener instrucciones sobre cómo escribir directivas compatibles, consulta [http://content-security-policy.com](http://content-security-policy.com/).  | Las directivas deben estar separadas por un punto y coma.  Por ejemplo, si tienes una aplicación que carga todos tus recursos desde una red de entrega de contenido \(por ejemplo, `https://cdn.example.net`\), y estás seguro de que no necesitas contenido en un marco ni complementos, es posible que la directiva tenga el aspecto siguiente: `Content-Security-Policy: default-src https://cdn.example.net; child-src 'none'; object-src 'none'.` *\*Las directivas se separan con punto y coma, mientras que los orígenes de una directiva solo se deben separar con un espacio.* |
| CSP14309 | "Directiva desconocida en \[nombre de directiva\] en \[tipo de directiva\]. Se omitirá la directiva". | La directiva establecida en la Directiva CSP es desconocida y se pasará por alto.  | Para ver una lista de directivas admitidas, consulta [http://content-security-policy.com](http://content-security-policy.com/).  |
| CSP14310 | "Directiva no compatible [nombre de directiva] en \[tipo de directiva]. Se omitirá la directiva". | Se encontró una directiva durante el análisis en el tipo de directiva \(por ejemplo, el campo de encabezado de `Content-Security-policy-Report-Only`\) que no es compatible y se omitirá.  Para ver las directivas admitidas, consulta [http://content-security-policy.com](http://content-security-policy.com/).  | Quita la directiva no compatible.  **NOTA**: Las directivas no se admiten en el elemento \<meta\> o en el campo de encabezado `Content-Security-policy-Report-Only`.  |
| CSP14311 | "La directiva \[nombre de directiva\] ya estaba ofrecida en \[tipo de directiva\]. Se omitirá la directiva duplicada". | Se encontró una directiva duplicada en el análisis, la segunda directiva y sus expresiones de origen se pasarán por alto.  | Quita el script duplicado.  |
| CSP14312 | "El recurso infringe la directiva [nombre de la directiva] en [tipo de directiva]: [uri de destino].  Se bloqueará el recurso". | En este ejemplo: "el recurso infringió la directiva 'script-src ms-appx: data: 'unsafe-eval' en la Directiva definida por el host: script en línea.  Se bloqueará el recurso". | Se ha bloqueado el script insertado \(uri de destino\) debido a la directiva `'script-src ms-appx: data: 'unsafe-eval'` en la directiva "host definido".  <br /> Los autores deben quitar todo el script y estilo que tengan en línea, ya que el agente de usuario no puede determinar si un atacante ha insertado un script en línea.  Quita scripts en línea y colócalos en un archivo externo.  |
| CSP14313 | "El recurso infringe la directiva [nombre de la directiva] en [tipo de directiva]: [uri de destino].  El recurso no se bloqueará porque la directiva es solo de informe". | Se identificó un recurso que infringe la directiva especificada en el campo de encabezado de `Content-Security-policy-Report-Only`.  Ya que se encuentra en un tipo de directiva `Report-Only`, el recurso no se bloqueará.  | Mueve la directiva a un campo de encabezado Content-Security-Policy si este recurso debe bloquearse para proteger el sitio.  |
| CSP14314 | "No se pudo enviar el informe de infracción de directiva a [uri de destino] porque [motivo de cancelación de la operación]". | Hubo un problema al notificar una infracción de directiva, el destino donde se indica el envío del informe y el motivo por el que no se envía deben identificarse.  | La directiva de `report-uri` especifica una dirección URL donde un explorador enviará informes cuando se infrinja una directiva de seguridad de contenido.  *\* No se puede usar en etiquetas \<meta\>.* |
| CSP14315 | "No se pudo aplicar la directiva de espacio aislado en [tipo de directiva] porque [motivo de cancelación de la operación]". | La directiva de espacio aislado ha producido un error por los motivos especificados.  Esta directiva coloca restricciones en las acciones que puede realizar la página en lugar de en los recursos que puede cargar la página.  Si la directiva de espacio aislado está presente, la página se trata como si se hubiera cargado en un iframe.  Puede evitar el acceso de las ventanas emergentes y las secuencias de comandos de bloqueo.  | Deja el valor del espacio aislado en blanco para mantener todas las restricciones en su sitio o agrega los valores: `allow-forms`, `allow-same-origin`, `allow-scripts`y `allow-top-navigation`.  *\*La directiva de espacio aislado no se admite en el elemento \<meta\> o en el campo de encabezado `Content-Security-policy-Report-Only`.* |
| CSP14316 | "Se permite la evaluación de scripts debido a la suplantación de host". | Cuando se incluye la directiva `script-src` o `default-src`, se deshabilitan el script en línea y `eval()`, a menos que especifique `unsafe-inline` y `unsafe-eval`, respectivamente.  | `'unsafe-eval'` Permite el uso de `eval()` y métodos similares para crear código a partir de cadenas.  No olvides incluir las comillas simples.  ***NOTA**: esto no es seguro y puede dejar su sitio vulnerable para ataques entre sitios.* |
| CSP14317 | "Se permite el marco [nombre de origen] debido a la suplantación de host". | El marco de origen identificado se ha permitido debido a un conjunto de anulaciones en la directiva CSP de host.  | Una directiva puede contener una expresión de origen nonce, lo que significa que el origen puede usarse solo una vez y el servidor debe generar un nuevo valor para la directiva cada vez que transmita una directiva.  Los nonces suplantan las restricciones de las directivas en las que están presentes.  |

> [!NOTE]
> En el caso de los sitios web de una zona de seguridad de confianza de un usuario, Microsoft Edge no comprueba el tipo MIME de una hoja de estilos.  

## Códigos CSS  

Estos errores están en formato CSS31xx y relacionados con problemas de origen de fuente y servidor de host de *Formato de fuente abierta web* \(WOFF\) y la fuente *OpenType incrustada* \(EOT\).  

| Código | Mensaje | Descripción | Corrección propuesta |
|:--- |:--- |:--- |:--- |
| CSS3111 | "@font-face encontró un error desconocido" | Se ha detectado un problema desconocido con "Formato de fuente abierta web \(WOFF\)" y "Fuente OpenType incrustada \(EOT\)" de la fuente hojas de estilos en cascada \(CSS\).  | Comprueba el origen de las fuentes WOFF.  Prueba un font-face u otro tipo de origen alternativos para ver si puedes reproducir el problema.  |
| CSS3112 | "@font-face no ha superado la comprobación de integridad WOFF" | El Formato de fuente abierta web \(WOFF\) puede estar dañado, incompleto o no tener el formato correcto.  | Comprobar el origen de las fuentes.  Prueba un font-face u otro tipo de origen conocido y confiable para ver si puedes reproducir el problema.  |
| CSS3113 | "Error de coincidencia @font-face entre el origen del documento y la cadena raíz EOT" | La fuente no se puede usar porque la dirección URL \(rootstring\) en la fuente OpenType incrustrada \(EOT\) no coincide con el dominio del documento que usa la fuente.  | La suma de comprobación de la dirección URL en la cadena de raíz EOT podría ser incorrecta, lo que indica que se ha modificado la dirección URL de la fuente.  Asegúrate de que la fuente tiene licencia o permisos para el sitio web en el que se usa.  |
| CSS3114 | "@font-face no superó la comprobación de permiso OpenType incrustado.  El permiso debe ser instalable". | Font-face no tiene permisos de instalación en la página web actual.  | Obtén los permisos o licencias correctos para insertar la fuente.  |
| CSS3115 | "@font-face no puede cargar una fuente OpenType no válida". | Font-face no es válido para este uso.  | Obtén los permisos o licencias para el font-face actual y válido.  |
| CSS3116 | "Se ha producido un error en la solicitud de origen cruzado de @font-face.  No hay encabezado Access-Control-Allow-Origin". | Es posible que la fuente no esté configurada para el acceso entre dominios.  | La fuente no se sirve desde el mismo origen que el documento.  Asegúrate de que el host que atiende la fuente permita el uso de esta fuente mediante el encabezado HTTP "Access-Control-Allow-Origin".                        |
| CSS3117 | "Se ha producido un error en la solicitud de origen cruzado de @font-face.  El acceso a los recursos está restringido". | Es posible que el encabezado "Access-Control-Allow-Origin" no se haya configurado correctamente o que el host de fuentes no permita que la página use esta fuente.  | Asegúrate de que el recurso tiene los permisos correctos y un encabezado de respuesta HTTP configurado correctamente con un origen de acceso entre dominios en el host que atiende las fuentes.  |
| CSS3118 | "No se pudo crear una nueva hoja de estilos.  Hay más de \[n.º máximo\] hojas de estilo en el documento". | Microsoft Edge ha creado más de 4095 objetos de hoja de estilo durante el proceso de procesamiento de la página.  | Puede tratarse de un proceso de JavaScript fuera de control o un error del sistema de compilación.  Reduce el número de objetos de hoja de estilo que se generan.  |
| CSS3119 | "El estado de la consulta multimedia: -ms-view-state está en desuso.  las consultas multimedia de -ms-view-state pueden modificarse o no estar disponibles para las versiones de Windows 8.1.  En su lugar, usa max-width y min-width". | Tu CSS contiene una consulta de medios `-ms-view-state`.  | Usa max-width y min-width.  |

## Códigos HTML

Estos códigos se encuentran en el formato HTML1xxx, como HTML1115.  Muchos son códigos heredados específicos de los conceptos de Internet Explorer, como *Modo de documento* y la *Vista de compatibilidad*.  

| Código | Mensaje | Descripción | Corrección propuesta |  
| :--- |:--- |:--- |:--- |  
| HTML1112 | "Reinicio de la página de códigos desde \[codificación\] a \[codificación\]" | Se especificó una página de códigos que es diferente de la página de códigos del servidor.  | Usa la misma página de códigos que el servidor para evitar este error.  |  
| HTML1113 | "Reinicio de modo de documento desde \[modo\] a \[modo\]" | La página web necesita un modo de documento distinto del configurado actualmente en el explorador.  | Este mensaje puede aparecer cuando el usuario se desplaza desde otra página, por lo que el desarrollador no tiene el control.  |  
| HTML1114 | La página de código \[codificación\] de \[dominio\] suplanta la página de código en conflicto \[codificación\] de \[dominio\]". | Las páginas de códigos especificadas en los encabezados HTTP \(desde el servidor\) y HTML \(en la página\) son diferentes entre sí.  | Cambia una para que coincidan.  |  
| HTML1115 | "Se ignoró la etiqueta META X-UA-Compatible \(`[META tag]`\) porque ya ha finalizado el modo de documento" | Por lo general, la etiqueta META se insertó después de la declaración "Script" o "Style", que corrigió el modo de documento de la página.  | Mueve la etiqueta META X-UA-Compatible tan al principio en el encabezado como puedas.  Se recomienda colocarla inmediatamente después de los valores de \<title\> y charset.  |  
| HTML1116 | "Se ignoró la etiqueta META X-UA-Compatible \(`[META tag]`\) debido a la etiqueta META \(`[META tag]`\)". | Hay más de una etiqueta "META" "X-UA-Compatible" en la sección \<head\> del código fuente.  | Suprime todas las etiquetas excepto la etiqueta META "X-UA-Compatible" y asegúrate de que aparezca tan al principio del encabezado como sea posible.  Se recomienda colocarla inmediatamente después de los valores de \<title\> y charset.  |  
| HTML1121 | "La página de códigos \[codificación\] no se permite, solo se permite la página de códigos \[codificación\]. | El contenido de la página web ha invocado una codificación de caracteres que no se permite en este contexto.  | Asegúrate de que todo el contenido usa la codificación permitida que se especifica en el mensaje.  |  
| HTML1122 | "Internet Explorer está en ejecución en el Modo de empresa emulando IE8". | La página se está procesando actualmente en el Modo de empresa, que es una emulación de Windows Internet Explorer 8.  | Este modo lo configura la administración de TI para sitios específicos.  Si un usuario individual necesita desactivarlo en una página web, desactiva la opción Modo de empresa en el menú Herramientas.  Para obtener más información sobre la administración del Modo de empresa, consulta la documentación [TI](https://technet.microsoft.com/library/dn640687.aspx).  |  
| HTML1201 | "`[domain]` es un sitio web que has agregado a la Vista de compatibilidad". | El usuario seleccionó el botón **Vista de compatibilidad** para el sitio web actual o lo ha agregado a través de la **configuración de la Vista de compatibilidad**.  | Iniciado por el usuario.  |  
| HTML1202 | "`[domain]` está en ejecución en la Vista de compatibilidad, porque se ha marcado la opción 'Mostrar sitios de intranet en la Vista de compatibilidad'". | El usuario ha activado la casilla de verificación Mostrar sitios de intranet en la Vista de compatibilidad en la **configuración de la Vista de compatibilidad**.  | El usuario debe presionar ALT + T, seleccionar **configuración de la Vista de compatibilidad** y, a continuación, desactivar la casilla de verificación **Mostrar sitios de intranet en la Vista de compatibilidad**.  |  
| HTML1203 | "`[domain]` se ha configurado para que se ejecute en la Vista de compatibilidad con una directiva de grupo". | El administrador de red especificó que la página web se ejecute en la Vista de compatibilidad.  | Tendrás que ponerte en contacto con el administrador de la red.  |  
| HTML1204 | "`[domain]` está en ejecución en la Vista de compatibilidad, porque se ha marcado la opción 'Mostrar todos los sitios Web en la Vista de compatibilidad'". | El usuario ha activado la casilla de verificación **Mostrar todos los sitios Web en la Vista de compatibilidad** en la **configuración de la Vista de compatibilidad**.  | El usuario debe presionar ALT + T, seleccionar **configuración de la Vista de compatibilidad** y, a continuación, desactivar la casilla de verificación **Mostrar todos los sitios Web en la Vista de compatibilidad**.  |  
| HTML1300 | "La navegación ha tenido lugar" | Se ha navegado por una nueva página o se ha actualizado la página actual.  | Se trata de un mensaje informativo, no un error.  |  

## Advertencias del analizador HTML5  

Las advertencias siguientes pueden producirse como parte de la validación realizada durante el análisis HTML.  Las advertencias no significan que una página está dañada, sino que el código HTML proporcionado no es válido por el estándar HTML5.  Es posible que el contenido creado en conformidad con versiones anteriores de las especificaciones HTML o XHTML no sea válido en HTML5, especialmente en lo que respecta al uso de DOCTYPE.

Estas advertencias suelen indicar caracteres faltantes o adicionales, o que no coinciden las etiquetas.  Resolver estas advertencias debería mejorar la compatibilidad con los exploradores antiguos y ofrecer una página web que cumpla con el estándar de HTML5.  Para que te resulte más fácil identificar el origen de una advertencia, se incluye información sobre el desplazamiento de caracteres y líneas, así como un vínculo que señala la ubicación en la que se encontró el problema.

| Código     | Mensaje |  
| :--- |:--- |  
| HTML1400 | "Carácter inesperado al comienzo de la referencia de carácter numérico.  Se esperaba [0-9]". |  
| HTML1401 | "Carácter inesperado al comienzo de la referencia de carácter numérico hexadecimal.  Se esperaba [0-9], [a-f] o [A-F]". |  
| HTML1402 | "Falta un punto y coma final en la referencia de carácter ";"". |  
| HTML1403 | "La referencia de carácter numérico no se resuelve en un carácter válido". |  
| HTML1404 | "Referencia de caracteres con nombre no reconocida". |  
| HTML1405 | "Carácter no válido: U+0000 NULL.  No se deben usar caracteres nulos". |  
| HTML1406 | "Inicio de etiqueta no válido: \<\?.  Los signos de interrogación no deben iniciar etiquetas". |  
| HTML1407 | "Nombre de etiqueta no válido.  El primer carácter debe coincidir con [a-zA-Z]". |  
| HTML1408 | "Etiqueta final no válida \</\>.  Las etiquetas finales no pueden estar vacías". |  
| HTML1409 | "Carácter de nombre de atributo no válido.  Los nombres de atributo no deben contener \(\"\), \(\'\), \(\<\), o \(=\)". |  
| HTML1410 | "Valor de atributo sin comillas no válido.  Los nombres de atributo sin comillas no deben contener \(\"\), \(\'\), \(\<\), \(=\) o \(\`\)". |  
| HTML1411 | "Fin de archivo inesperado". |  
| HTML1412 | "Comentario mal formado.  Los comentarios deben empezar con \<\!-- \>". |  
| HTML1413 | "Carácter inesperado: U+003E corchete angular de cierre \(\>\)" |  
| HTML1414 | "Carácter inesperado: U+0021 signo de exclamación \(\!\)" |  
| HTML1415 | "Carácter inesperado: U+002D signo menos \(-\)" |  
| HTML1416 | "Carácter imprevisto en el final del comentario.  Se esperaba "--\>"." |  
| HTML1417 | "DOCTYPE vacío.  El doctype más corto posible es \<\!DOCTYPE html\>". |  
| HTML1418 | "Carácter imprevisto en el final de DOCTYPE. |  
| HTML1419 | "Palabra clave inesperada en DOCTYPE.  Se esperaba 'PUBLIC' o 'SYSTEM'". |  
| HTML1420 | "Comilla inesperada después de palabra clave "PUBLIC" o "SYSTEM".  Se esperaba un espacio en blanco". |  
| HTML1421 | "Etiqueta final mal formada.  Las etiquetas finales no deberían contener atributos". |  
| HTML1422 | "Etiqueta inicial mal formada.  Una barra diagonal de autocierre debe ir seguida de un signo U+003E corchete angular de cierre \(\>\)". |  
| HTML1423 | "Etiqueta inicial mal formada.  Los atributos se deben separar por espacios en blanco". |  
| HTML1424 | "Carácter no válido   " |  
| HTML1500 | "No se puede cerrar la etiqueta automáticamente.  Usa una etiqueta de cierre explícita". |  
| HTML1501 | "Fin de archivo inesperado". |  
| HTML1502 | "DOCTYPE inesperado.  Solo se permite un DOCTYPE y este debe producirse antes de cualquier elemento". |  
| HTML1503 | "Etiqueta inicial inesperada". |  
| HTML1504 | "Etiqueta final inesperada". |  
| HTML1505 | "Token de carácter inesperado". |  
| HTML1506 | "Token inesperado". |  
| HTML1507 | "Carácter inesperado". U+0000 NULL.  No se deben usar caracteres nulos". |  
| HTML1508 | "Etiqueta final no emparejada". |  
| HTML1509 | "Etiqueta final no emparejada". |  
| HTML1510 | "Nodos necesarios fuera de ámbito". |  
| HTML1511 | "Se encontró un elemento inesperado de nivel de encabezado fuera de \<head\>". |  
| HTML1512 | "Etiqueta final no emparejada". |  
| HTML1513 | "Etiqueta adicional de \<html\>.  Solo debe haber una etiqueta \<html\> por documento". |  
| HTML1514 | "Se encontró una etiqueta adicional de \<body\>.  Solo debe haber una etiqueta \<body\> por documento". |  
| HTML1515 | "Se encontró \<frameset\> situado demasiado abajo en el documento.  Esta etiqueta debe ser anterior a la creación de \<body\>". |  
| HTML1516 | "Anidamiento no válido.  Una etiqueta de encabezado como \<h1\> o \<h2\> no debe colocarse dentro de otra etiqueta de encabezado". |  
| HTML1517 | "Anidamiento no válido.  Una etiqueta \<form\> no se puede colocar dentro de otra etiqueta ". |  
| HTML1518 | "Anidamiento no válido.  Una etiqueta \<button\> no se puede colocar dentro de otra etiqueta ". |  
| HTML1519 | "Anidamiento no válido.  Una etiqueta \<a\> no se puede colocar dentro de otra etiqueta \<a\>". |  
| HTML1520 | "Etiqueta inicial imprevista: el elemento \<isindex\> está en desuso y no se debe usar". |  
| HTML1521 | "\</body\> o fin de archivo inesperados.  Todos los elementos abiertos deben cerrarse antes del final del documento". |  
| HTML1522 | "Etiqueta final no válida: \</br\>.  Usa \<br\> o \<br /\> en su lugar". |  
| HTML1523 | "Etiqueta final superpuesta.  Las etiquetas se deben estructurar como \<b\>\<i\>\</i\>\</b\> en lugar de \<b\>\<i\>\</b\>\</i\>". |  
| HTML1524 | "DOCTYPE no válido.  El doctype más corto posible es \<\!DOCTYPE html\>". |  
| HTML1525 | "Se encontró una etiqueta HTML inesperada en el contenido externo \(MathML/SVG\)". |  
| HTML1526 | "Anidamiento no válido.  Una etiqueta \<nobr\> no se puede estar dentro de otra etiqueta ". |  
| HTML1527 | "DOCTYPE esperado.  El doctype más corto posible es \<\!DOCTYPE html\>". |  
| HTML1528 | "\<image\> inesperada en el contenido HTML.  Usa \<img\> en su lugar". |  
| HTML1529 | "El valor de atributo xmlns:xlink no es válido.  Este valor debe ser '\<https://w3.org/1999/xlink\>'". |  
| HTML1530 | "Se encontró texto en un elemento de tabla estructural.  El texto de la tabla solo puede colocarse dentro de elementos \<caption\>, \<td\> o \<th\>". |  
| HTML1531 | "El valor de atributo xmlns no es válido.  Para los elementos SVG, el valor debe ser "\<https://w3.org/2000/svg/\>". |  
| HTML1532 | "El valor de atributo xmlns no es válido.  Para los elementos MathML, el valor debe ser "\<https://w3.org/1998/Math/MathML/\>".  |  

## Códigos HTTP  

Los códigos de error HTTP son devueltos por los servidores remotos en respuesta a las solicitudes.  Probablemente, el más conocido es HTTP404, que se devuelve cuando el servidor no encuentra la página o el documento especificado en el identificador uniforme de recursos (URI).

| Código | Mensaje | Descripción |  
| :--- |:--- |:--- |  
| HTTP400 | SOLICITUD INCORRECTA | El servidor no pudo procesar la solicitud porque la sintaxis no es válida.  |  
| HTTP401 | DENEGADO | El recurso solicitado requiere autenticación de usuarios.  |  
| HTTP402 | PAGO REQUERIDO | Actualmente no implementado en el protocolo HTTP.  |  
| HTTP403 | PROHIBIDO | El servidor comprendió la solicitud pero se niega a satisfacerla.  |  
| HTTP404 | NO ENCONTRADO | El servidor no encontró nada que coincidiera con el URI solicitado.  |  
| HTTP405 | MÉTODO INCORRECTO | El verbo HTTP usado no está permitido.  |  
| HTTP406 | NINGUNA RESPUESTA ACEPTABLE | No se encontraron respuestas aceptables para el cliente.  |  
| HTTP407 | SE REQUIERE AUTENTICACIÓN POR PROXY | Se requiere autenticación por proxy  |  
| HTTP408 | TIEMPO DE ESPERA DE SOLICITUD SUPERADO | El servidor agotó el tiempo de espera para la solicitud.  |  
| HTTP409 | CONFLICTO | La solicitud no se pudo completar debido a un conflicto con el estado actual del recurso.  |  
| HTTP410 | NO EXISTE | El recurso solicitado ya no está disponible en el servidor y no se conoce ninguna dirección de reenvío.  |  
| HTTP411 | LONGITUD OBLIGATORIA | El servidor se niega a aceptar la solicitud sin una longitud de contenido definida.  |  
| HTTP412 | ERROR EN LA CONDICIÓN PREVIA | La condición previa proporcionada en uno o más de los campos de encabezado de la solicitud dio como resultado "false" cuando se probó en el servidor.  |  
| HTTP413 | CARGA ÚTIL DEMASIADO GRANDE | El servidor se niega a procesar una solicitud porque la entidad de solicitud es más grande de lo que el servidor está dispuesto a procesar.  |  
| HTTP414 | URI DEMASIADO LARGO | El servidor rechaza la solicitud porque el URI de solicitud es más largo de lo que el servidor está dispuesto a interpretar.  |  
| HTTP415 | TIPO DE MEDIO NO COMPATIBLE | El servidor rechaza la solicitud porque la entidad de la solicitud está en un formato que no es compatible con el recurso solicitado para el método solicitado.  |  
| HTTP416 | EL RANGO SOLICITADO NO ES ACPETABLE | El servidor no puede proporcionar la parte del archivo solicitado por el cliente.  La parte puede extenderse más allá del final del archivo.  |  
| HTTP417 | ERROR DE EXPECTATIVA | El servidor no cumple los requisitos del campo de encabezado de solicitud Expect.  |  
| HTTP418 | SOY UNA TETERA | El servidor es una tetera; no puede hacer café.  |  
| HTTP419 | TIEMPO DE ESPERA DE AUTENTICACIÓN | La autenticación anteriormente válida ha expirado.  |  
| HTTP422 | ENTIDAD QUE NO SE PUEDE PROCESAR | La solicitud tenía el formato correcto, pero no se pudo procesar debido a errores semánticos.  |  
| HTTP423 | BLOQUEADO | El recurso al que se accede está bloqueado.  |  
| HTTP424 | FALLO EN LA DEPENDENCIA | Se ha producido un error en la solicitud por un fallo en la solicitud anterior.  |  
| HTTP426 | ACTUALIZACIÓN NECESARIA | El cliente debe cambiar a otro protocolo.  |  
| HTTP428 | CONDICIÓN PREVIA NECESARIA | El servidor de origen requiere la solicitud para ser condicional.  |  
| HTTP429 | DEMASIADAS SOLICITUDES | El servidor se niega a procesar la solicitud porque el cliente envió demasiadas solicitudes.  |  
| HTTP431 | CAMPOS DE ENCABEZADO DE SOLICITUD DEMASIADO LARGOS | El servidor rechaza la solicitud porque un campo de encabezado, o todos los campos de encabezado de forma conjunta, superan el tamaño que el servidor está dispuesto o puede procesar.  |  
| HTTP449 | INTENTAR DE NUEVO CON | Se debe volver a intentar la solicitud después de tomar las medidas adecuadas.  |  
| HTTP500 | ERROR DEL SERVIDOR | El servidor encontró una condición inesperada que le impide completar la solicitud.  |  
| HTTP501 | NO SE ADMITE | El servidor no admite la funcionalidad necesaria para completar la solicitud.  |  
| HTTP502 | PUERTA DE ENLACE NO VÁLIDA | Mientras actuaba como puerta de enlace o proxy, el servidor recibió una respuesta no válida del servidor ascendente al que tenía acceso mientras intentaba completar la solicitud.  |  
| HTTP503 | SERVICIO NO DISPONIBLE | El servicio está sobrecargado temporalmente.  |  
| HTTP504 | TIEMPO DE ESPERA DE LA PUERTA DE ENLACE AGOTADO | Se agotó el tiempo de espera de la solicitud mientras se esperaba a una puerta de enlace.  |  
| HTTP505 | VERSIÓN NO COMPATIBLE | El servidor no es compatible con la versión del protocolo HTTP que se utilizó en el mensaje de solicitud o no la admite.  |  
| HTTP506 | LA VARIANTE TAMBIÉN NEGOCIA | La negociación de contenido transparente para la solicitud ha resultado en referencias circulares.  |  
| HTTP507 | ALMACENAMIENTO INSUFICIENTE | El servidor no puede almacenar la representación necesaria para completar la solicitud.  |  
| HTTP508 | BUCLE DETECTADO | El servidor ha detectado un bucle infinito mientras se atiende la solicitud.  |  
| HTTP510 | NO EXTENDIDO | Se requieren más extensiones a la solicitud para que el servidor la satisfaga.  |  
| HTTP511 | AUTENTICACIÓN DE RED NECESARIA | El cliente tiene que autenticarse para acceder a la red.  |  

## Errores de sintaxis de JavaScript  

Se producen errores de sintaxis de JavaScript cuando la estructura de una de las instrucciones infringe una o varias de las reglas sintácticas.  

| Número de error | Descripción |  
| --- | --- |  
| 1019 | [No puede haber un "break" fuera del bucle](/scripting/javascript/misc/can-t-have-break-outside-of-loop) |  
| 1020 | [No puede haber un "continue" fuera del bucle](/scripting/javascript/misc/can-t-have-continue-outside-of-loop) |  
| 1030 | [Compilación condicional desactivada](/scripting/javascript/misc/conditional-compilation-is-turned-off) |  
| 1027 | ["Default" solo puede aparecer una vez en una instrucción "switch".](/scripting/javascript/misc/default-can-only-appear-once-in-a-switch-statement) |  
| 1005 | [Se esperaba "\("](/scripting/javascript/misc/expected-left-parenthesis-javascript) |  
| 1006 | [Se esperaba "\)"](/scripting/javascript/misc/expected-right-parenthesis-javascript) |  
| 1012 | [Se esperaba "/"](/scripting/javascript/misc/expected-minus) |  
| 1003 | [Se esperaba ":"](/scripting/javascript/misc/expected-colon) |  
| 1004 | [Se esperaba ";"](/scripting/javascript/misc/expected-semicolon) |  
| 1032 | [Se esperaba "@"](/scripting/javascript/misc/expected-at) |  
| 1029 | [Se esperaba "@end"](/scripting/javascript/misc/expected-at-end) |  
| 1007 | [Se esperaba "\]"](/scripting/javascript/misc/expected-right-square-bracket) |  
| 1008 | [Se esperaba "{"](/scripting/javascript/misc/expected-left-curly-brace) |  
| 1009 | [Se esperaba "}"](/scripting/javascript/misc/expected-right-curly-brace) |  
| 1011 | [Se esperaba "="](/scripting/javascript/misc/expected-equal-javascript) |  
| 1033 | [Se esperaba "catch"](/scripting/javascript/misc/expected-catch) |  
| 1031 | [Se esperaba una constante](/scripting/javascript/misc/expected-constant) |  
| 1023 | [Se esperaba un dígito hexadecimal](/scripting/javascript/misc/expected-hexadecimal-digit) |  
| 1010 | [Se esperaba un identificador](/scripting/javascript/misc/expected-identifier-javascript) |  
| 1028 | [Se esperaba un identificador, una cadena o un número](/scripting/javascript/misc/expected-identifier-string-or-number) |  
| 1024 | [Se esperaba "while"](/scripting/javascript/misc/expected-while) |  
| 1014 | [Carácter no válido](/scripting/javascript/misc/invalid-character-javascript) |  
| 1026 | [Etiqueta no encontrada](/scripting/javascript/misc/label-not-found) |  
| 1025 | [Etiqueta redefinida](/scripting/javascript/misc/label-redefined) |  
| 1018 | ["Return" está fuera de la función](/scripting/javascript/misc/return-statement-outside-of-function) |  
| 1002 | [Error de sintaxis](/scripting/javascript/misc/syntax-error-javascript) |  
| 1035 | ["Throw" debe ir seguido de una expresión en la misma línea de origen](/scripting/javascript/misc/throw-must-be-followed-by-an-expression-on-the-same-source-line) |  
| 1016 | [Comentario sin finalizar](/scripting/javascript/misc/unterminated-comment) |  
| 1015 | [Constante de cadena sin finalizar](/scripting/javascript/misc/unterminated-string-constant-javascript) |  
  
### Errores de host de script  

Los siguientes errores están más relacionados con el host de scripts, pero es posible que los veas de vez en cuando:  
  
| Error | HRESULT | Descripción |  
| ---| --- | --- |  
| SCRIPT_E_RECORDED | 0x86664004 | Se ha grabado un error y ha pasado entre el motor de scripts y el host.  El host necesita pasar el código de error al autor de la llamada.  |  
| SCRIPT_E_REPORTED | 0x80020101 | El motor de script ha notificado una excepción no controlada al host a través de IActiveScriptSite::OnScriptError.  El host puede omitir este error.  |  
| SCRIPT_E_PROPAGATE | 0x8002010 | Un error de script propagado al autor de la llamada puede estar en otro subproceso.  El host debe pasar el código de error al autor de la llamada.  |  

## Errores de tiempo de ejecución de JavaScript

Se producen cuando el script intenta realizar una acción que el sistema no puede ejecutar.  Es posible que veas errores de tiempo de ejecución al evaluar expresiones de variables o al asignar la memoria.

| Número de error: | Descripción |  
| --- | --- |  
| 5 | [Acceso denegado.](/scripting/javascript/misc/access-is-denied) |  
| 438 | [El objeto no es compatible con esta propiedad o método](/scripting/javascript/misc/object-doesn-t-support-this-property-or-method) |  
| 1001 | Memoria insuficiente |  

### Errores de Windows Runtime  

 Si usas las API de Windows Runtime \(WinRT\), es posible que veas errores de JavaScript que se han convertido a partir de los HRESULT de Windows Runtime.  Los valores HRESULT de Windows Runtime en el rango por encima de 0x80070000 se convierten en errores de JavaScript al tomar el valor hexadecimal de los bits bajos y convertirlos en decimal.  Por ejemplo, el resultado HRESULT 0x80070032 se convierte en el valor decimal 50 y el error JavaScript es SCRIPT50.  El resultado HRESULT 0x80074005 se convierte en el valor decimal 16389 y el error JavaScript es SCRIPT16389.

| Número de error | Descripción |  
| --- | --- |  
| 5029 | [La longitud de la matriz debe ser un número entero positivo y finito](/scripting/javascript/misc/array-length-must-be-a-finite-positive-integer) |  
| 5030 | [La longitud de la matriz se debe asignar a un número positivo y finito](/scripting/javascript/misc/array-length-must-be-assigned-a-finite-positive-number) |  
| 5028 | [Se esperaba una matriz o un objeto de argumentos](/scripting/javascript/misc/array-or-arguments-object-expected) |  
| 5010 | [Se esperaba un valor booleano](/scripting/javascript/misc/boolean-expected) |  
| 5003 | [No se puede asignar al resultado de una función](/scripting/javascript/misc/cannot-assign-to-a-function-result) |  
| 5000 | [No se puede asignar a "this"](/scripting/javascript/misc/cannot-assign-to-this) |  
| 5034 | [No se admite la referencia circular en el argumento de valor](/scripting/javascript/misc/circular-reference-in-value-argument-not-supported) |  
| 5006 | [Se esperaba un objeto de fecha](/scripting/javascript/misc/date-object-expected) |  
| 5015 | [Se esperaba un objeto de enumerador](/scripting/javascript/misc/enumerator-object-expected) |  
| 5022 | [Excepción iniciada y no capturada](/scripting/javascript/misc/exception-thrown-and-not-caught) |  
| 5020 | [Se esperaba ")" en la expresión regular](/scripting/javascript/misc/expected-right-parenthesis-in-regular-expression-javascript) |  
| 5019 | [Se esperaba "&#93;" en la expresión regular](/scripting/javascript/misc/expected-right-square-bracket-in-regular-expression-javascript) |  
| 5023 | [La función no tiene un objeto prototipo válido](/scripting/javascript/misc/function-does-not-have-a-valid-prototype-object) |  
| 5002 | [Se esperaba una función](/scripting/javascript/misc/function-expected) |  
| 5008 | [Asignación no válida](/scripting/javascript/misc/illegal-assignment-javascript) |  
| 5021 | [Rango incorrecto en conjunto de caracteres](/scripting/javascript/misc/invalid-range-in-character-set-javascript) |  
| 5035 | [Argumento de reemplazo no válido](/scripting/javascript/misc/invalid-replacer-argument) |  
| 5014 | [Se esperaba un objeto JavaScript](/scripting/javascript/misc/javascript-object-expected) |  
| 5001 | [Se esperaba un número](/scripting/javascript/misc/number-expected) |  
| 5007 | [Se esperaba un objeto](/scripting/javascript/misc/object-expected) |  
| 5012 | [Se esperaba un objeto miembro](/scripting/javascript/misc/object-member-expected) |  
| 5016 | [Se esperaba un objeto de expresión regular](/scripting/javascript/misc/regular-expression-object-expected) |  
| 5005 | [Se esperaba una cadena](/scripting/javascript/misc/string-expected) |  
| 5017 | [Error de sintaxis en la expresión regular](/scripting/javascript/misc/syntax-error-in-regular-expression-javascript) |  
| 5026 | [El número de dígitos fraccionarios está fuera del intervalo](/scripting/javascript/misc/the-number-of-fractional-digits-is-out-of-range) |  
| 5027 | [La precisión está fuera del intervalo](/scripting/javascript/misc/the-precision-is-out-of-range) |  
| 5025 | [El URI a descodificar no es una codificación válida](/scripting/javascript/misc/the-uri-to-be-decoded-is-not-a-valid-encoding) |  
| 5024 | [El URI a codificar contiene un carácter no válido.](/scripting/javascript/misc/the-uri-to-be-encoded-contains-an-invalid-character) |  
| 5009 | [Identificador no definido](/scripting/javascript/misc/undefined-identifier) |  
| 5018 | [Cuantificador no esperado](/scripting/javascript/misc/unexpected-quantifier-javascript) |  
| 5013 | [Se esperaba VBArray](/scripting/javascript/misc/vbarray-expected) |  

## Códigos de seguridad

Los códigos de error de seguridad están en formato `SEC7xxx`, como `SEC7113`.  Estos errores reflejan las condiciones de seguridad que exige Microsoft Edge, como contenido mixto y la protección de seguimiento.

| Código | Mensaje | Descripción | Corrección propuesta |  
| :--- |:--- |:--- |:--- |  
| SEC7111 | "Seguridad HTTPS comprometida por [nombre del recurso]" | Una página del protocolo seguro de transferencia de hipertexto \(HTTPS\) tiene contenido de un origen no seguro.  | Asegúrate de que todo el contenido de la página, incluidos los scripts, los objetos de hojas de estilo y las imágenes provienen de orígenes HTTPS.  |  
| SEC7112 | "Se ha bloqueado el script desde [URL] debido a un error de coincidencia de tipos MIME" | El encabezado de respuesta HTTP del archivo de JavaScript especificado por la dirección URL tiene un encabezado "X-Content-Type-Options: nosniff" y no tiene ninguna declaración de tipo de contenido reconocible.  | Actualiza el servidor para que envíe el tipo de contenido correcto para el archivo de JavaScript \(como "text/javascript, application/javascript", por ejemplo\) en el encabezado de respuesta HTTP.  Para obtener más información y una lista completa de los tipos de contenido, consulta [Cambios en el control de MIME en Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7113 | "Se ignoró CSS debido a un error de coincidencia de tipos MIME" | No se ha usado una hoja de estilos importada porque el tipo MIME es incorrecto en el encabezado HTTP.  | Asegúrate de que el archivo de la hoja de estilos se entrega con el encabezado de respuesta HTTP correcto, que incluye un tipo de contenido de texto o CSS.  Para obtener más información, consulta [Cambios en el control de MIME en Internet Explorer](https://blogs.msdn.microsoft.com/ie/2010/10/26/mime-handling-changes-in-internet-explorer/).  |  
| SEC7114 | "Se ha bloqueado una descarga en esta página al rastrear la protección. [URL proporcionada aquí]" | El usuario bloqueó un script o contenido mediante la protección de seguimiento.  | Ninguna: acción iniciada por el usuario.  |  
| SEC7115 | "Los estilos :visited y :link solo pueden diferir en el color.  Algunos estilos no se aplicaron a :visited". | Se cambió más de un atributo, como la fuente o el tamaño, mediante los estilos :visited y :link.  | Cambiar solo el atributo color.  |  
| SEC7116 | "Acceso denegado  No se pudo revocar la dirección URL de origen cruzado: [URL]". | El script tiene un sitio de origen distinto al del documento que creó la dirección URL de blob.  El intento falló por las directivas de origen de blob.  | Asegúrate de que todas las direcciones URL del blob estén revocadas mediante scripts del mismo sitio de origen que el documento que creó la URL de blob.  |  
| SEC7120 | "El origen [dominio] no se encuentra en el encabezado Access-Control-Allow-Origin". | En la respuesta a XMLHttpRequest, el encabezado Access-Control-Allow-Origin se devolvió con un valor que no contiene ni coincide con el valor de origen del sitio.  | El recurso devuelve el tipo correcto de códigos de encabezado, pero no permite su sitio.  Ponte en contacto con el desarrollador encargado del recurso y pídele que actualice el encabezado Access-Control-Allow-Origin para que se permita el sitio.  Puedes indicarle que consulte [CORS para XHR en IE10](https://blogs.msdn.microsoft.com/ie/2012/02/09/cors-for-xhr-in-ie10/) para obtener más información sobre CORS en encabezados de respuesta.  |  
| SEC7121 | "El carácter comodín en Access-Control-Allow-Origin no está permitido cuando el indicador predefinido de los credenciales está establecido como true". | El servidor devuelve "Access-Control-Allow-Origin: *" en los encabezados, pero esto no se permite cuando el indicador `withCredentials` está establecido en **true** en XMLHttpRequest.  | El controlador del lado del servidor debe modificarse para devolver un encabezado Access-Control-Allow-Origin que permita específicamente el punto de origen en este tipo de solicitud.  Si no te ocupas del controlador del servidor, tendrás que ponerte en contacto con el desarrollador encargado de ello.  |  
| SEC7122 | "El indicador de credenciales se ha definido como verdadero, pero Access-Control-Allow-Credentials no aparece o no se ha establecido en "true". | Se ha realizado una solicitud XMLHttpRequest con la marca `withCredentials`.  Un encabezado Access-Control-Allow-Credentials no se devolvió o se devolvió con un valor distinto de **true**.  | Es posible que haya un problema con las credenciales o la respuesta del servidor.  Consulta la [especificación de nivel 2 de XMLHttpRequest](https://w3.org/TR/XMLHttpRequest2/) para obtener información sobre las solicitudes con credenciales.  |  
| SEC7123 | "El encabezado de solicitud [encabezado] no se encuentra en la lista Access-Control-Allow-Headers". | Se incluyó un tipo de encabezado personalizado en la solicitud, pero la lista Access-Control-Allow-Headers de la respuesta no lo incluía.  | Asegúrate de que el servidor admite encabezados personalizados y que, especialmente, permite el que se envía en la solicitud.  |  
| SEC7124 | "El método de solicitud [método] no se encuentra en la lista Access-Control-Allow-Methods". | Se usó un método de solicitud como POST en XMLHttpRequest, pero la respuesta devolvió un encabezado Access-Control-Allow-Methods que no lo incluía.  | Asegúrate de que el servidor admite este tipo de método de solicitud y que usas correctamente `withCredentials` si el método tiene acceso restringido.  |  
| SEC7125 | "XMLHttpRequest para [URL] provocó un error en el análisis de los encabezados de respuesta". | No se pudieron analizar los encabezados de respuesta del servidor, por lo que no se pudo realizar la solicitud.  | Usa la herramienta [Red](https://msdn.microsoft.com/library/dn255004.aspx) para capturar e inspeccionar los encabezados de respuesta y asegurarte de que cumplan las [especificaciones de CORS](https://w3.org/TR/cors/).  |  
| SEC7126 | "No se permite redirigir las solicitudes de comprobación preparatoria de CORS". | Se ha detectado una redirección en el encabezado de origen y el agente de usuario no seguirá las redirecciones durante una comprobación preparatoria.  | Usa la herramienta [Red](https://msdn.microsoft.com/library/dn255004.aspx) para capturar e inspeccionar los encabezados de la solicitud y asegurarte de que hay un único origen directo.  |  
| SEC7127 | "Se bloqueó el redireccionamiento para la solicitud CORS". | La ruta de acceso al recurso de CORS contenía una redirección que infringe las reglas de seguridad.  | Asegúrate de que usas la ruta más directa al recurso CORS en XMLHttpRequest.  |  
| SEC7128 | "No se permiten varios encabezados Access-Control-Allow-Origin para la respuesta de CORS". | El encabezado de la respuesta incluía múltiples encabezados Access-Control-Allow-Origin.  | Este es un error del servidor.  El servidor debe devolver un único encabezado Access-Control-Allow-Origin.  Notifica este error al programador encargado de los recursos del servidor.
| SEC7129 | "No se permiten varios encabezados Access-Control-Allow-Credentials para la respuesta de CORS". | El encabezado de la respuesta incluía múltiples encabezados Access-Control-Allow-Credentials.  | Este es un error del servidor.  El servidor debe devolver un único encabezado Access-Control-Allow-Credentials.  Notifica este error al programador encargado de los recursos del servidor.  |  
| SEC7130 | "Se detectaron posibles scripts entre sitios en [URL].  El contenido se ha modificado mediante el filtro XSS". | El [filtro XSS](https://msdn.microsoft.com/library/dd565647.aspx) detectó contenido potencialmente malintencionado en la respuesta del recurso y ha quitado el contenido infractor.  | Obtener más información acerca del [filtro XSS](https://msdn.microsoft.com/library/dd565647.aspx).  |  
| SEC7131 | "La seguridad de un iframe en espacio aislado es susceptible de estar comprometida al permitir acceso al script y al mismo origen". | Si el contenido de un iframe de espacio aislado proviene de una fuente que no es de confianza o no es segura, puede que salga del espacio aislado cuando se permita el script y el acceso al mismo origen.  | Este es un mensaje de advertencia informativo y no debe afectar a la funcionalidad.  Se recomienda no combinar estos permisos, excepto si está seguro de lo que se ejecutará en el iframe.  |  
| SEC7132 | "El certificado que protege este sitio Web usa criptografía deficiente" | El certificado de seguridad de TLS usado por este sitio Web usa una criptografía deficiente. | Actualiza el certificado TLS del servidor. |  

> [!NOTE]
> En el caso de los sitios web de una zona de seguridad de confianza de un usuario, Microsoft Edge no comprueba el tipo MIME de una hoja de estilos.

## Códigos SVG  

DevTools no es compatible actualmente con una depuración en profundidad de gráficos vectoriales escalables \(SVG\), pero se proporcionan algunos mensajes en la consola para ayudar con la depuración.

| Código | Mensaje | Descripción | Corrección propuesta |  
| :--- |:--- |:--- |:--- |  
| SVG5601 | "Los datos de la ruta de acceso SVG tienen un formato incorrecto y no se pueden analizar completamente". | La cadena de la ruta de acceso [SVG](https://msdn.microsoft.com/library/ff972086.aspx) no tiene el formato correcto o contiene comandos no reconocidos.  | Comprueba el formato de los comandos.  |  
| SVG5602 | "La lista de puntos SVG tiene un formato incorrecto y no se puede analizar completamente". | La lista de puntos utilizados para un elemento, como una [polilínea](https://msdn.microsoft.com/library/ff972113.aspx), tiene un formato incorrecto.  | Asegúrate de que los puntos estén completos y tengan el formato correcto para el sistema de coordenadas de los usuarios.  |  

## Códigos XML  

Los códigos XML están en la forma XML5xxx, como XML5603.  

| Código | Mensaje |  
|:--- |:--- |  
| XML5001 | "Aplicando control de XSLT integrado". |  
| XML5601 | "MX_E_MX" |  
| XML5602 | "Fin de entrada inesperado". |  
| XML5603 | "Codificación no reconocida". |  
| XML5604 | "No se puede cambiar la codificación". |  
| XML5605 | "Firma de codificación de entrada no reconocida". |  
| XML5606 | "WC_E_WC" |  
| XML5607 | "Se esperaba un espacio en blanco". |  
| XML5608 | "Se esperaba punto y coma". |  
| XML5609 | "Se esperaba '>'". |  
| XML5610 | "Se esperaba un carácter de comillas". |  
| XML5611 | "Se esperaba '='". |  
| XML5612 | "El carácter < no está permitido en los valores de los atributos". |  
| XML5613 | "Se esperaba un dígito hexadecimal". |  
| XML5614 | "Se esperaba un dígito decimal". |  
| XML5615 | "Se esperaba '['". |  
| XML5616 | "Se esperaba '('". |  
| XML5617 | "Carácter XML no válido". |  
| XML5618 | "Carácter de nombre no válido". |  
| XML5619 | "Sintaxis de documento incorrecta". |  
| XML5620 | "Sintaxis de sección CDATA incorrecta". |  
| XML5621 | "Sintaxis de comentario incorrecta". |  
| XML5622 | "Sintaxis de sección condicional incorrecta". |  
| XML5623 | "Sintaxis de declaración ATTLIST incorrecta". |  
| XML5624 | "Sintaxis de declaración DOCTYPE incorrecta". |  
| XML5625 | "Sintaxis de declaración ELEMENT incorrecta". |  
| XML5626 | "Sintaxis de declaración ENTITY incorrecta". |  
| XML5627 | "Sintaxis de declaración NOTATION incorrecta". |  
| XML5628 | "Se esperaba 'NDATA'". |  
| XML5629 | "Se esperaba 'PUBLIC'". |  
| XML5630 | "Se esperaba 'SYSTEM'". |  
| XML5631 | "Nombre no válido". |  
| XML5632 | "Solo se permite un elemento raíz". |  
| XML5633 | "El nombre final de la etiqueta no coincide con el nombre de etiqueta inicial correspondiente". |  
| XML5634 | "Ya existe un atributo con el mismo nombre en este elemento". |  
| XML5635 | "Solo se permite una declaración XML al comienzo del archivo". |  
| XML5636 | "'Xml' inicial". |  
| XML5637 | "Sintaxis de declaración de texto incorrecta". |  
| XML5638 | "Sintaxis de declaración de XML incorrecta". |  
| XML5639 | "Sintaxis de nombre de codificación incorrecta". |  
| XML5640 | "Sintaxis de identificador pública incorrecta". |  
| XML5641 | "No se permiten referencias de entidad de parámetro en declaraciones de marcado en un subconjunto DTD interno". |  
| XML5642 | "El texto reemplazado para referencias de entidad de parámetro que se usan entre declaraciones de marcado debe contener una serie de declaraciones de marcado completas". |  
| XML5643 | "Una entidad analizada no debe contener una referencia directa o indirecta a sí misma". |  
| XML5644 | "El contenido de la entidad especificada no tiene el formato correcto". |  
| XML5645 | "No se ha declarado la entidad especificada". |  
| XML5646 | "La referencia de entidad no puede contener el nombre de una entidad sin analizar". |  
| XML5647 | "Los valores de atributo no deben contener referencias directas o indirectas a entidades externas". |  
| XML5648 | "Sintaxis de instrucción de procesamiento incorrecta". |  
| XML5649 | "Sintaxis de identificador de sistema incorrecta". |  
| XML5650 | "Se esperaba el signo de interrogación \(\?\)". |  
| XML5651 | "El delimitador de cierre de sección CDATA "]]>" no se debe usar en el contenido del elemento". |  
| XML5652 | "No se han leído todos los segmentos de datos". |  
| XML5653 | "Se encontró DTD, pero está prohibido". |  
| XML5654 | "Se encontró un atributo xml:space cuyo valor no es válido.  Los valores válidos son 'preserve' o 'default'". |  
| XML5655 | "NC_E_NC" |  
| XML5656 | "Carácter de nombre completo no válido". |  
| XML5657 | "Varios signos de dos puntos ":" no deben aparecer en un nombre completo". |  
| XML5658 | "Un signo de dos puntos ":" no debe aparecer en un nombre". |  
| XML5659 | "Prefijo declarado". |  
| XML5660 | "No se ha declarado el prefijo especificado". |  
| XML5661 | "Las declaraciones de espacios de nombres no predeterminados no deben tener un URI vacío". |  
| XML5662 | "El prefijo "xml" está reservado y debe tener el URI '<https://w3.org/XML/1998/namespace/>'". |  
| XML5663 | "El prefijo "xmlns" está reservado para su uso con XML". |  
| XML5664 | "Solo se debe asignar al prefijo "xml" el URI de espacio de nombres XML \(\<https://w3.org/XML/1998/namespace/\>\). |  
| XML5665 | "El URI del espacio de nombres xmlns \(\<https://w3.org/2000/xmlns/\>\) está reservado y no debe usarse". |  
| XML5666 | "SC_E_SC" |  
| XML5667 | "Se ha superado la profundidad máxima de elementos anidados". |  
| XML5668 | "Se ha superado el número máximo de expansiones de la entidad". |  
| XML5669 | "WR_E_WR" |  
| XML5670 | "WR_E_NONWHITESPACE: writer: la cadena especificada no es un espacio en blanco". |  
| XML5671 | "WR_E_NSPREFIXDECLARED: writer: ya se ha declarado el prefijo de espacio de nombres con un espacio de nombres distinto". |  
| XML5672 | "WR_E_NSPREFIXWITHEMPTYNSURI: writer: no se puede usar un prefijo con URI de espacio de nombres vacío". |  
| XML5673 | "WR_E_DUPLICATEATTRIBUTE: writer: atributo duplicado". |  
| XML5674 | "WR_E_XMLNSPREFIXDECLARATION: writer: no se puede volver a definir el prefijo xmlns". |  
| XML5675 | "WR_E_XMLPREFIXDECLARATION: writer: el prefijo XML debe tener el URI de \<https://w3.org/XML/1998/namespace/\>". |  
| XML5676 | "WR_E_XMLURIDECLARATION: writer: el URI de espacio de nombres xml \(\<https://w3.org/XML/1998/namespace/\>\) debe asignarse solo al prefijo 'xml'". |  
| XML5677 | "WR_E_XMLNSURIDECLARATION: writer: El URI del espacio de nombres xmlns \(\<https://w3.org/2000/xmlns/\>\) está reservado y no debe usarse". |  
| XML5678 | "WR_E_NAMESPACEUNDECLARED: writer: el espacio de nombres no se ha declarado". |  
| XML5679 | "WR_E_INVALIDXMLSPACE: writer: valor no válido de atributo xml:space \(los valores permitidos son "default" y "preserve"\)". |  
| XML5680 | "WR_E_INVALIDACTION: writer: la realización de la acción solicitada daría como resultado un documento XML no válido". |  
| XML5681 | "WR_E_INVALIDSURROGATEPAIR: writer: la entrada contiene un par suplente no válido o incompleto". |  
| XML5682 | "Carácter imprevisto en la entidad del carácter.  Se esperaba un dígito decimal". |  
| XML5683 | "Carácter imprevisto en la entidad del carácter.  Se esperaba un dígito hexadecimal". |  
| XML5684 | "El valor unicode de la entidad de carácter especificada no es válido". |  
| XML5685 | "Codificación no válida". |  
| XML5686 | "Error de XML sin especificar". |  

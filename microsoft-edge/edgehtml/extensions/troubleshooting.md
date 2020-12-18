---
ms.assetid: 8b7f362f-da09-43db-8a42-cfa128c1808c
description: Obtén respuestas a preguntas habituales que puede tener al cargar extensiones desempaquetadas.
title: 'Extensiones: solución de problemas'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 74743923000766473a96b56a97d302b6ab79a9e3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236118"
---
# Solución de problemas  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Si está intentando cargar extensiones desempaquetadas y está experimentando problemas, la siguiente información puede resultarle útil:

## 1. veo el error "no pudimos cargar esta extensión"

Normalmente, esto significa que Microsoft Edge no puede tener acceso a la carpeta de extensión que intentaste cargar.

A continuación se muestra un resumen de los posibles errores que puede encontrar:

Mensaje de error | Detalles
:--------- | :------------
Error de análisis de manifiesto: falta el archivo de manifiesto o tiene el formato incorrecto. | Es posible que el archivo `"manifest.json"` no se encuentre en la ubicación especificada o que haya algún problema con el archivo. Para resolver el problema, asegúrese de que la carpeta especificada contiene el manifiesto en el nivel superior y, a continuación, vuelva a comprobar las comas, las comillas y los corchetes.
Error de análisis de manifiesto: `"content_scripts"` debe definir una matriz. | El campo `"content_scripts"` debe ser una matriz. Para resolver el problema, vuelva a comprobar la sintaxis. Por ejemplo: `"content_scripts": [{"matches": [...],"css": [...],"js": [...] }]`
Error de análisis de manifiesto: `"content_scripts"` debe definir el valor de la `"matches"` propiedad. | La propiedad `"matches"` es obligatoria. Para resolver el problema, especifique el valor de la propiedad con una matriz de cadenas. Por ejemplo: `"content_scripts": [ {... "matches": ["http://www.bing.com"] ...} ]`
Error de análisis de manifiesto: `"content_scripts"` debe hacer referencia a un archivo. CSS o. js como mínimo. | Al menos una propiedad `"css"` o `"js"` es obligatoria. Para resolver el problema, especifique el valor de la propiedad con una matriz de cadenas. Por ejemplo: `"content_scripts": [ { ... "js": ["myScript1.js", "myScript2.js"] ...} ]`
Error de análisis de manifiesto: `"<field>"` debe definir el valor de la <property> propiedad "". | La propiedad `<property>` para el campo `<field>` es obligatoria. Para resolver el problema, especifique un valor válido para `<property>` .
Error de análisis de manifiesto: `"content_scripts"` referencias valor no válido para el campo "run_at". | La propiedad `"run_at"` especifica un valor desconocido. Para resolver el problema, especifique uno de los `"document_start"` , `"document_end"` o `"document_idle"` . Por ejemplo: `"content_scripts": [ {... "run_at": "document_start" ... } ]`
Error de análisis de manifiesto: falta el `"<field>"` campo. | El campo `<field>` es obligatorio. Para resolver el problema, defina el campo con un valor válido.
Error de análisis de manifiesto: se encontró un campo no válido `"<field1>"` en `"<field2>"` . | El campo del <field1> campo <field2> especifica un valor desconocido. Para resolver el problema, especifique un valor válido para <field1> .
Error de análisis de manifiesto: valor no válido para el <field> campo "". | El campo <field> especifica un valor desconocido. Para resolver el problema, especifique un valor válido.
Error de análisis de manifiesto: la versión actual de Microsoft Edge no admite la extensión. | La propiedad `"minimum_edge_version"` especifica una versión más reciente de Microsoft Edge distinta de la suya. Para encontrar la versión actual, abre el "..." (Más) y seleccionando "configuración" (sección inferior "acerca de esta aplicación"). Para resolver el problema, actualice el explorador a una versión más reciente o cambie el valor del manifiesto. Por ejemplo: `"minimum_edge_version": "x.xxxx.xxxx.x"`
Error de análisis de manifiesto: `"background"` debe definir el valor de la propiedad "página" o "scripts". | La propiedad "página" o "scripts" son obligatorias para el campo "background". Para resolver el problema, especifique una cadena para "Page" o una matriz de cadenas para "scripts". Por ejemplo: `"background": { ... "scripts": ["background.js"] ... }`
Error de análisis de manifiesto: `"background"` debe definir el valor de la `"persistent"` propiedad. | La propiedad `"persistent"` es obligatoria. Para resolver el problema, especifique un valor verdadero o falso. Por ejemplo: `"background": {... "persistent": true ...}`
Error de análisis de manifiesto: `"browser_action"` solo `"page_action"` se puede definir uno o un. | Una extensión no puede definir una acción de página y una acción de explorador al mismo tiempo. Para resolver el problema, quite cualquiera de las definiciones.
Error no especificado: `<error>` | Mensaje de error genérico catch-all. `<error>` se reemplazará por el error especificado.


## 2. no veo el botón "cargar extensión"
Hasta que las extensiones estén disponibles a través de Microsoft Store, este botón *debería* estar visible de forma predeterminada. Si abre el menú "más" (...), selecciona el elemento de menú "extensiones" y no ve el botón, siga estos pasos:

1. En la barra de direcciones, escriba **"acerca de: flags"** y presione la tecla **"entrar"** .
2. En el encabezado **"configuración del programador"** Asegúrese de que la casilla que se encuentra junto a **"habilitar características de desarrollador de extensiones"** está seleccionada.

   ![Acerca de las marcas](./media/aboutflags.PNG)  

3. Cierre y vuelva a abrir Microsoft Edge y compruebe si el botón **"cargar extensión"** ahora está visible.

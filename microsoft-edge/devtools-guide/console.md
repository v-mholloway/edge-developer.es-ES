---
description: Use la herramienta de consola para la depuración interactiva y las pruebas ad hoc.
title: DevTools-consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, consola
ms.custom: seodec18
ms.openlocfilehash: f2733cac57ed5f2364747ee64e669fa83aae41f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573847"
---
# Console

La herramienta de desarrollador de consola de Microsoft Edge registra información que está asociada a una página web, como JavaScript, solicitudes de red y errores de seguridad. Puede usar la consola para la depuración interactiva y las pruebas ad hoc. 

Para abrir la herramienta de consola en Microsoft Edge, presione la tecla F12 para acceder a la ventana de la herramienta de desarrollador (o haga clic con el botón derecho en la página y, a continuación, seleccione **Inspeccionar elemento**). Después, seleccione la pestaña de **consola** en la parte superior de la ventana. 

También puede usar la herramienta de consola para comunicarse con una página web en ejecución y desde ella. Puede usar la consola para:

- Publique [códigos de estado y errores](./console/error-and-status-codes.md) estándar y mensajes informativos mientras se ejecuta el código.
- Genera registros de depuración personalizados de las llamadas [API de consola](./console/console-api.md) que incluyas en el código.
- Proporciona una [línea de comandos](./console/command-line.md) y una vista de árbol interactiva para inspeccionar los valores devueltos actuales de las variables y funciones clave.

## Partes de la consola

La imagen siguiente muestra las partes principales de la consola:

![La consola de Microsoft Edge DevTools](./media/console.png)

1. **Errores**  /  **Advertencias**  /  **Información**  /  Botones de **registro** : filtrar la salida de consola por el tipo especificado. Puede seleccionar varios botones manteniendo presionada la tecla **Ctrl** . El botón **todo** borra todos los filtros.

2. Botón **Borrar** (**Ctrl + L**): el botón **Borrar** borra la pantalla actual de la consola.

3. Casilla de verificación **conservar registro** : al seleccionar la casilla de verificación **conservar registro** , se conserva la salida de la consola en las actualizaciones de página y se cierra y vuelve a abrir DevTools. El historial de consola se borra solo cuando se cierra la pestaña o cuando se borra manualmente la consola.

4. **Destino**: Use el menú desplegable de **destino** para cambiar a un contexto de ejecución diferente, como un `<iframe>` en la página o una extensión en curso. De forma predeterminada, se selecciona el marco de nivel superior de la página. Al mantener el puntero sobre un marco seleccionado, se muestra la información sobre herramientas que muestra la dirección URL completa de ese recurso.

5. **Mostrar consola**  /  **Ocultar** botón de consola (**Ctrl** +  **&grave;** ): además del panel de consola, puede usar la consola desde la parte inferior de cualquier otro panel de DevTools pulsando el **Show Console**  /  botón**ocultar** consola de la consola. El botón no surte efecto cuando DevTools está abierto en el panel de consola.
 
6. **Filtrar registros** (**Ctrl + b**): también puede filtrar los registros mediante una cadena de texto específica en el cuadro de búsqueda.

7. **Depurador**: Seleccione cualquier vínculo de origen azul para abrir el depurador de DevTools a esa línea de código en particular para su posterior inspección.

## Abreviados

Acción                                            | Método abreviado               
:-------------------------------------------------| :----------------------
Iniciar DevTools con la consola en el foco             | **Ctrl**  +  **MAYÚS**  +  **J** 
Cambiar a la consola                                 | **Ctrl**  +  **2**           
Mostrar u ocultar la consola de otra ficha de DevTools       | **Ctrl**  +  Ctrl **&grave;** (marca atrás)  
Ejecutar (comando de una sola línea)                     | **Entrar**                
Salto de línea sin ejecutar (comando de varias líneas) | **MAYÚS**  +  **Entrar** o **Ctrl +**  +  **entrar**      
Borrar la consola de todos los mensajes                 | **Ctrl**  +  **L**           
Filtrar registros (establecer el foco en el cuadro de búsqueda)             | **Ctrl**  +  **F**           
Aceptar la sugerencia de finalización automática (cuando está en el foco) | **Entrar** o **Tab**       
Sugerencia de finalización automática anterior o siguiente          | Tecla de flecha **arriba** / **Tecla de dirección abajo**   



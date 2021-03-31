---
description: Probar la extensión mediante la transferencia local en el explorador
title: Transferir la extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-cromo, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104779"
---
# Transferir localmente una extensión

Durante el desarrollo, puedes usar el explorador Microsoft Edge \(cromo \) para ejecutar y depurar tu extensión de forma segura. Si instalas localmente tu extensión en tu explorador, puedes ejecutar y probar la extensión. En este artículo se explica cómo transferir extensiones a Microsoft Edge.

Para realizar la transferencia de la extensión, siga estos pasos.

1.  Abra la `edge://extensions` página seleccionando los puntos suspensivos en la parte superior del explorador y, a continuación, seleccione **extensiones**.

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Abrir la página edge://extensions":::
          Abrir la página edge://extensions :::image-end:::

1.  En la página de administración de extensiones de `edge://extensions` , active el **modo de desarrollador** con el botón de alternancia de la parte inferior izquierda de la página.

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Abrir la página edge://extensions":::
          Activar el modo de desarrollador :::image-end:::

1.  Cuando instale la extensión por primera vez, elija **cargar sin empaquetar**.  Se le pedirá el directorio con los archivos de origen de la extensión.  La extensión se instala en el explorador, de forma similar a las extensiones instaladas desde la tienda.  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Abrir la página edge://extensions":::
          Página de extensiones instaladas que muestra una extensión de transferible :::image-end:::

Durante el desarrollo, es posible que también tenga que realizar las siguientes tareas.
* Actualice la extensión. Vaya a `edge://extensions` y, a continuación, seleccione **volver a cargar** para actualizar la extensión.  
* Quite la extensión de su explorador. Vaya a `edge://extensions` y, a continuación, seleccione `Remove` en la extensión.
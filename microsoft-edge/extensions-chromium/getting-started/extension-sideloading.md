---
description: Probar la extensión mediante la instalación local en el explorador
title: Instalación local de la extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo web, html, css, javascript, desarrollador, extensiones
ms.openlocfilehash: 7070878b9608e6d239179078390f2315e0b289a1
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104779"
---
# Transferir localmente una extensión

Durante el desarrollo, puede usar el Microsoft Edge \(Chromium\) para ejecutar y depurar la extensión de forma segura. Al descargar localmente la extensión en el explorador, puede ejecutar y probar la extensión. En este artículo se explica cómo usar extensiones en Microsoft Edge.

Para descargar localmente la extensión, siga estos pasos.

1.  Abra la página eligiendo los tres puntos en la parte superior del explorador y, a `edge://extensions` continuación, seleccione **Extensiones**.

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Abra la edge://extensions web":::
          Abra la edge://extensions web :::image-end:::

1.  En la página de administración de extensiones en , active el modo programador con el botón de alternancia `edge://extensions` en la parte inferior izquierda de la página. ****

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Activar el modo de desarrollador":::
          Activar el modo de desarrollador :::image-end:::

1.  Al instalar la extensión por primera vez, elija **Load Unpacked**.  Se le pedirá el directorio con los archivos de origen de extensión.  La extensión está instalada en el explorador, de forma similar a las extensiones instaladas desde la tienda.  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Página de extensiones instaladas que muestra una extensión de instalación local":::
          Página de extensiones instaladas que muestra una extensión de instalación local :::image-end:::

Durante el desarrollo, es posible que también necesite realizar las siguientes tareas.
* Actualice la extensión. Vaya a `edge://extensions` y, a continuación, **seleccione Volver a cargar** para actualizar la extensión.  
* Quite la extensión del explorador. Vaya a `edge://extensions` y, a continuación, `Remove` seleccione en la extensión.
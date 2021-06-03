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
# <span data-ttu-id="9f58c-104">Transferir localmente una extensión</span><span class="sxs-lookup"><span data-stu-id="9f58c-104">Sideload an extension</span></span>

<span data-ttu-id="9f58c-105">Durante el desarrollo, puede usar el Microsoft Edge \(Chromium\) para ejecutar y depurar la extensión de forma segura.</span><span class="sxs-lookup"><span data-stu-id="9f58c-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="9f58c-106">Al descargar localmente la extensión en el explorador, puede ejecutar y probar la extensión.</span><span class="sxs-lookup"><span data-stu-id="9f58c-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="9f58c-107">En este artículo se explica cómo usar extensiones en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9f58c-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="9f58c-108">Para descargar localmente la extensión, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="9f58c-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="9f58c-109">Abra la página eligiendo los tres puntos en la parte superior del explorador y, a `edge://extensions` continuación, seleccione **Extensiones**.</span><span class="sxs-lookup"><span data-stu-id="9f58c-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Abra la edge://extensions web":::
          <span data-ttu-id="9f58c-111">Abra la edge://extensions web</span><span class="sxs-lookup"><span data-stu-id="9f58c-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="9f58c-112">En la página de administración de extensiones en , active el modo programador con el botón de alternancia `edge://extensions` en la parte inferior izquierda de la página. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9f58c-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Activar el modo de desarrollador":::
          <span data-ttu-id="9f58c-114">Activar el modo de desarrollador</span><span class="sxs-lookup"><span data-stu-id="9f58c-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="9f58c-115">Al instalar la extensión por primera vez, elija **Load Unpacked**.</span><span class="sxs-lookup"><span data-stu-id="9f58c-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="9f58c-116">Se le pedirá el directorio con los archivos de origen de extensión.</span><span class="sxs-lookup"><span data-stu-id="9f58c-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="9f58c-117">La extensión está instalada en el explorador, de forma similar a las extensiones instaladas desde la tienda.</span><span class="sxs-lookup"><span data-stu-id="9f58c-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Página de extensiones instaladas que muestra una extensión de instalación local":::
          <span data-ttu-id="9f58c-119">Página de extensiones instaladas que muestra una extensión de instalación local</span><span class="sxs-lookup"><span data-stu-id="9f58c-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="9f58c-120">Durante el desarrollo, es posible que también necesite realizar las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="9f58c-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="9f58c-121">Actualice la extensión.</span><span class="sxs-lookup"><span data-stu-id="9f58c-121">Update the extension.</span></span> <span data-ttu-id="9f58c-122">Vaya a `edge://extensions` y, a continuación, **seleccione Volver a cargar** para actualizar la extensión.</span><span class="sxs-lookup"><span data-stu-id="9f58c-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="9f58c-123">Quite la extensión del explorador.</span><span class="sxs-lookup"><span data-stu-id="9f58c-123">Remove the extension from your browser.</span></span> <span data-ttu-id="9f58c-124">Vaya a `edge://extensions` y, a continuación, `Remove` seleccione en la extensión.</span><span class="sxs-lookup"><span data-stu-id="9f58c-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>
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
# <span data-ttu-id="de78d-104">Transferir localmente una extensión</span><span class="sxs-lookup"><span data-stu-id="de78d-104">Sideload an extension</span></span>

<span data-ttu-id="de78d-105">Durante el desarrollo, puedes usar el explorador Microsoft Edge \ (cromo \) para ejecutar y depurar tu extensión de forma segura.</span><span class="sxs-lookup"><span data-stu-id="de78d-105">During development, you may use the Microsoft Edge \(Chromium\) browser to run and debug your extension safely.</span></span> <span data-ttu-id="de78d-106">Si instalas localmente tu extensión en tu explorador, puedes ejecutar y probar la extensión.</span><span class="sxs-lookup"><span data-stu-id="de78d-106">By sideloading your extension locally in your browser, you can run and test your extension.</span></span> <span data-ttu-id="de78d-107">En este artículo se explica cómo transferir extensiones a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="de78d-107">This article explains how to sideload extensions into Microsoft Edge.</span></span>

<span data-ttu-id="de78d-108">Para realizar la transferencia de la extensión, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="de78d-108">To sideload your extension, follow these steps.</span></span>

1.  <span data-ttu-id="de78d-109">Abra la `edge://extensions` página seleccionando los puntos suspensivos en la parte superior del explorador y, a continuación, seleccione **extensiones**.</span><span class="sxs-lookup"><span data-stu-id="de78d-109">Open the `edge://extensions` page by choosing the three dots at the top of your browser, and then selecting **Extensions**.</span></span>

       :::image type="complex" source="./media/part1-threedots.png" alt-text="Abrir la página edge://extensions":::
          <span data-ttu-id="de78d-111">Abrir la página edge://extensions</span><span class="sxs-lookup"><span data-stu-id="de78d-111">Open the edge://extensions page</span></span> :::image-end:::

1.  <span data-ttu-id="de78d-112">En la página de administración de extensiones de `edge://extensions` , active el **modo de desarrollador** con el botón de alternancia de la parte inferior izquierda de la página.</span><span class="sxs-lookup"><span data-stu-id="de78d-112">On the extension management page at `edge://extensions`, turn on **Developer mode** using the toggle at the bottom left of the page.</span></span>

       :::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Abrir la página edge://extensions":::
          <span data-ttu-id="de78d-114">Activar el modo de desarrollador</span><span class="sxs-lookup"><span data-stu-id="de78d-114">Turn on Developer Mode</span></span> :::image-end:::

1.  <span data-ttu-id="de78d-115">Cuando instale la extensión por primera vez, elija **cargar sin empaquetar**.</span><span class="sxs-lookup"><span data-stu-id="de78d-115">When installing your extension for the first time, choose **Load Unpacked**.</span></span>  <span data-ttu-id="de78d-116">Se le pedirá el directorio con los archivos de origen de la extensión.</span><span class="sxs-lookup"><span data-stu-id="de78d-116">You'll be prompted for the directory with your extension source files.</span></span>  <span data-ttu-id="de78d-117">La extensión se instala en el explorador, de forma similar a las extensiones instaladas desde la tienda.</span><span class="sxs-lookup"><span data-stu-id="de78d-117">Your extension is installed in your browser, similar to extensions installed from the store.</span></span>  

       :::image type="complex" source="./media/part1-installed-extension.png" alt-text="Abrir la página edge://extensions":::
          <span data-ttu-id="de78d-119">Página de extensiones instaladas que muestra una extensión de transferible</span><span class="sxs-lookup"><span data-stu-id="de78d-119">Installed extensions page showing a sideloaded extension</span></span> :::image-end:::

<span data-ttu-id="de78d-120">Durante el desarrollo, es posible que también tenga que realizar las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="de78d-120">During development, you may also need to perform the following tasks.</span></span>
* <span data-ttu-id="de78d-121">Actualice la extensión.</span><span class="sxs-lookup"><span data-stu-id="de78d-121">Update the extension.</span></span> <span data-ttu-id="de78d-122">Vaya a `edge://extensions` y, a continuación, seleccione **volver a cargar** para actualizar la extensión.</span><span class="sxs-lookup"><span data-stu-id="de78d-122">Navigate to `edge://extensions`, and then select **Reload** to update your extension.</span></span>  
* <span data-ttu-id="de78d-123">Quite la extensión de su explorador.</span><span class="sxs-lookup"><span data-stu-id="de78d-123">Remove the extension from your browser.</span></span> <span data-ttu-id="de78d-124">Vaya a `edge://extensions` y, a continuación, seleccione `Remove` en la extensión.</span><span class="sxs-lookup"><span data-stu-id="de78d-124">Navigate to `edge://extensions`, and then select `Remove` on your extension.</span></span>
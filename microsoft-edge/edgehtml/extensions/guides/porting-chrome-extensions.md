---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Aprende a migrar tu extensión Chrome a Microsoft Edge con el kit de herramientas de Microsoft Edge Extension.
title: Migrar las extensiones de Chrome
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f226d79dbc9efdc43eb68bfb353fa12748198371
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236468"
---
# <span data-ttu-id="72a7d-104">Migración de una extensión de Chrome a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="72a7d-104">Porting an extension from Chrome to Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="72a7d-105">Migrar una extensión de Chrome a Microsoft Edge es fácil con la ayuda del kit de [herramientas de extensión de Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="72a7d-105">Porting an extension from Chrome to Microsoft Edge is made easy with the help of the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span> <span data-ttu-id="72a7d-106">Esta herramienta de desarrollador convierte una extensión Chrome desempaquetada en una extensión de Microsoft Edge desempaquetada mediante el puente de las API y expone cualquier error en el `manifest.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="72a7d-106">This developer tool converts an unpacked Chrome extension to an unpacked Microsoft Edge extension by bridging APIs and surfacing any errors in your `manifest.json` file.</span></span>


### <span data-ttu-id="72a7d-107">Puentes de API</span><span class="sxs-lookup"><span data-stu-id="72a7d-107">API bridges</span></span>
<span data-ttu-id="72a7d-108">Para permitir la migración fluida de las API de Chrome a las API de Microsoft Edge compatibles, se agregan dos scripts a la carpeta de la extensión.</span><span class="sxs-lookup"><span data-stu-id="72a7d-108">In order to allow for seamless porting of Chrome APIs to supported Microsoft Edge APIs, two scripts are added to your extension's folder.</span></span> <span data-ttu-id="72a7d-109">Estas API de puente de scripts (si es necesario), lo que significa que no tendrá que preocuparse por cambiar cualquier código específico de Chrome en el script de fondo o los scripts de contenido.</span><span class="sxs-lookup"><span data-stu-id="72a7d-109">These scripts bridge APIs (polyfiling where necessary), meaning you won't have to worry about changing any Chrome specific code in your background script or content scripts.</span></span>

<span data-ttu-id="72a7d-110">Después de la conversión, los verás incluidos en el archivo de manifiesto de la extensión con la `"-ms-preload"` clave:</span><span class="sxs-lookup"><span data-stu-id="72a7d-110">After conversion, you will see them included in the manifest file of your extension with the `"-ms-preload"` key:</span></span>

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## <span data-ttu-id="72a7d-111">Usar el kit de herramientas de Microsoft Edge Extension</span><span class="sxs-lookup"><span data-stu-id="72a7d-111">Using the Microsoft Edge Extension Toolkit</span></span>

<span data-ttu-id="72a7d-112">Las instrucciones siguientes detallan cómo convertir la extensión de Chrome para que se ejecute en Microsoft Edge en la edición de actualización de aniversario de Windows 10:</span><span class="sxs-lookup"><span data-stu-id="72a7d-112">The following instructions detail how to convert your Chrome extension to run on Microsoft Edge in the Windows 10 Anniversary Update edition:</span></span>

1. <span data-ttu-id="72a7d-113">Instalar el [Kit de herramientas de Microsoft Edge Extension](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span><span class="sxs-lookup"><span data-stu-id="72a7d-113">Install the [Microsoft Edge Extension Toolkit](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).</span></span>
2. <span data-ttu-id="72a7d-114">Haga una copia de la carpeta de su extensión Chrome para mantener la seguridad.</span><span class="sxs-lookup"><span data-stu-id="72a7d-114">Make a copy of your Chrome extension's folder for safe keeping.</span></span> <span data-ttu-id="72a7d-115">El proceso de conversión sobrescribirá el código.</span><span class="sxs-lookup"><span data-stu-id="72a7d-115">The conversion process will overwrite the code.</span></span> 
3. <span data-ttu-id="72a7d-116">Ejecute el kit de herramientas de Microsoft Edge extension y cargue la copia de la extensión.</span><span class="sxs-lookup"><span data-stu-id="72a7d-116">Run the Microsoft Edge Extension Toolkit and load the copy of your extension.</span></span>  
 ![botón cargar extensión](./../media/save-folder.png)
4. <span data-ttu-id="72a7d-118">Corrija todos los errores que se notifican en el editor de texto de la herramienta.</span><span class="sxs-lookup"><span data-stu-id="72a7d-118">Correct all the errors that are reported within the tool's text editor.</span></span> <span data-ttu-id="72a7d-119">Seleccione "volver a validar" para comprobar si hay errores después de realizar correcciones.</span><span class="sxs-lookup"><span data-stu-id="72a7d-119">Select "Re-validate" to check for errors after making corrections.</span></span>  
 ![Extensión-kit de herramientas buscar errores](./../media/extension-toolkit.png)
5. <span data-ttu-id="72a7d-121">Seleccione "guardar archivos".</span><span class="sxs-lookup"><span data-stu-id="72a7d-121">Select "Save files".</span></span>

<span data-ttu-id="72a7d-122">Ahora puedes salir del kit de herramientas y cargar tu extensión en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="72a7d-122">You can now exit out of the toolkit and load your extension in Microsoft Edge!</span></span> 

<span data-ttu-id="72a7d-123">Puede buscar problemas de plataforma conocidos con el [EdgeHTML Issue Tracker](http://issues.microsoftedge.com).</span><span class="sxs-lookup"><span data-stu-id="72a7d-123">You can search for known platform issues with the [EdgeHTML issue tracker](http://issues.microsoftedge.com).</span></span> <span data-ttu-id="72a7d-124">Si cree que ha encontrado algo nuevo, [abra un problema](https://developer.microsoft.com/microsoft-edge/platform/issues/new/).</span><span class="sxs-lookup"><span data-stu-id="72a7d-124">If you think you've found something new, [open an issue](https://developer.microsoft.com/microsoft-edge/platform/issues/new/)!</span></span>

---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Consulta cómo empaquetar la extensión de Microsoft Edge en un instante con ManifoldJS, la herramienta de código abierto de node. js.
title: Uso de ManifoldJS para empaquetar extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: cca83a26c9f80eca6454e3b5b329f72a7491b6e2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573575"
---
# <span data-ttu-id="33e79-104">Uso de ManifoldJS para crear paquetes AppX de extensión</span><span class="sxs-lookup"><span data-stu-id="33e79-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="33e79-105">ManifoldJS es una herramienta de Open Source. js que le permite crear de forma rápida y fácilmente un paquete que se puede usar para enviarlo a Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="33e79-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>

<span data-ttu-id="33e79-106">Si usa mensajería nativa en su extensión, debe omitir esta acción e ir a la [Mensajería nativa en Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) para obtener instrucciones de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="33e79-106">If you use native messaging in your extension, you should skip this and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span> 

<span data-ttu-id="33e79-107">Antes de empezar, aún necesitarás leer los artículos siguientes:</span><span class="sxs-lookup"><span data-stu-id="33e79-107">Before getting started, you will still need to read up on the following articles:</span></span>

- [<span data-ttu-id="33e79-108">Extensiones en el centro de desarrollo de Windows</span><span class="sxs-lookup"><span data-stu-id="33e79-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)
- [<span data-ttu-id="33e79-109">Localización de paquetes de extensiones</span><span class="sxs-lookup"><span data-stu-id="33e79-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)

> [!NOTE]
> <span data-ttu-id="33e79-110">El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.</span><span class="sxs-lookup"><span data-stu-id="33e79-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="33e79-111">Una vez que hayas creado, embalado y probado tu extensión, envía una solicitud en nuestro [formulario de envío de extensiones](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="33e79-111">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>


## <span data-ttu-id="33e79-112">Instalar node. js y ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="33e79-112">Installing Node.js and ManifoldJS</span></span>

<span data-ttu-id="33e79-113">Lo primero que debe hacer es instalar [node. js lts](https://nodejs.org/en/download/).</span><span class="sxs-lookup"><span data-stu-id="33e79-113">The first things you'll need to do is install [Node.js LTS](https://nodejs.org/en/download/).</span></span>
<span data-ttu-id="33e79-114">Una vez que tenga node, desde una línea de comandos (preferiblemente PowerShell), ejecute el siguiente comando para instalar ManifoldJS:</span><span class="sxs-lookup"><span data-stu-id="33e79-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS:</span></span>

`npm install -g manifoldjs`

<span data-ttu-id="33e79-115">Para verificar que ha instalado correctamente ManifoldJS, ejecute `manifoldjs` desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="33e79-115">To verify that you've correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="33e79-116">Si no se reconoció ManifoldJS, añada `%APPDATA%\npm` a las variables de la ruta.</span><span class="sxs-lookup"><span data-stu-id="33e79-116">If ManifoldJS wasn't recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>

## <span data-ttu-id="33e79-117">Embalaje con ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="33e79-117">Packaging with ManifoldJS</span></span>

<span data-ttu-id="33e79-118">Para iniciar el proceso de empaquetado, tendrá que abrir una línea de comandos y cambiar los directorios a una carpeta que será el destino de la extensión empaquetada.</span><span class="sxs-lookup"><span data-stu-id="33e79-118">To start the packaging process, you'll need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>

<span data-ttu-id="33e79-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="33e79-119">For example:</span></span>

`cd C:\manifoldJSTest`

> [!NOTE]
> <span data-ttu-id="33e79-120">ManifoldJS se enviará en el directorio actual y podrá sobrescribir el contenido.</span><span class="sxs-lookup"><span data-stu-id="33e79-120">ManifoldJS will output in the current directory and can overwrite content.</span></span>



<span data-ttu-id="33e79-121">Ahora que se encuentra en la carpeta de destino, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="33e79-121">Now that you're in your destination folder, run the following command:</span></span>

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


<span data-ttu-id="33e79-122">Este comando se puede dividir en las siguientes partes:</span><span class="sxs-lookup"><span data-stu-id="33e79-122">This command can be broken down into the following parts:</span></span>
 -    <span data-ttu-id="33e79-123">**-l depurar**: cambia el nivel de registro a "debug" para obtener una impresión completa.</span><span class="sxs-lookup"><span data-stu-id="33e79-123">**-l debug**: Changes the log level to "debug" to get a full print out.</span></span>
 -    <span data-ttu-id="33e79-124">**-p edgeextension**: establece la única plataforma en la que se ejecutará la conversión en edgeextension.</span><span class="sxs-lookup"><span data-stu-id="33e79-124">**-p edgeextension**: Sets the only platform to run the conversion on to edgeextension.</span></span>
 -    <span data-ttu-id="33e79-125">**-f edgeextension**: indica al programa que el formato del manifiesto es un formato de edgeextension y no se produce un error en la validación.</span><span class="sxs-lookup"><span data-stu-id="33e79-125">**-f edgeextension**: Tells the program that the format of the manifest is an edgeextension format and not to care if it fails validation.</span></span>
 -    <span data-ttu-id="33e79-126">**-m \ < ubicación de la extensión > \manifest.JSON**: la ruta de acceso al manifiesto de la extensión que desea convertir.</span><span class="sxs-lookup"><span data-stu-id="33e79-126">**-m \<EXTENSION LOCATION>\manifest.json**: The path to the extension manifest that you want to convert.</span></span>


<span data-ttu-id="33e79-127">Cuando ManifoldJS haya terminado de ejecutarse, tendrá una carpeta con el siguiente contenido:</span><span class="sxs-lookup"><span data-stu-id="33e79-127">After ManifoldJS has finished running, you'll have a folder with the following contents:</span></span>

    My Extension
        edgeextension
            generationInfo.json
            manifest
                   appxmanifest.xml
                Assets
                    Square150x150Logo.png
                    Square44x44Logo.png
                    StoreLogo.png    
                Extension
                    manifest.json
                    popup.html
                    ...
                ...

<span data-ttu-id="33e79-128">El archivo generationInfo. JSON es un registro generado al ejecutar ManifoldJS y no se incluirá en el paquete de extensión.</span><span class="sxs-lookup"><span data-stu-id="33e79-128">The generationInfo.json file is a log produced by running ManifoldJS and won't be included in your extension package.</span></span> <span data-ttu-id="33e79-129">Solo se empaquetará el contenido de la carpeta del **manifiesto** .</span><span class="sxs-lookup"><span data-stu-id="33e79-129">Only the contents of the **manifest** folder will be packaged.</span></span> <span data-ttu-id="33e79-130">En la carpeta de manifiesto, la carpeta activos contiene las imágenes que se usarán en la interfaz de usuario de Windows y de Microsoft Store, mientras que la carpeta de extensiones tiene el contenido de la extensión dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="33e79-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>


<span data-ttu-id="33e79-131">Ahora que tienes los archivos correctos, tendrás que editar el archivo AppXManifest generado dentro de la carpeta del **manifiesto** .</span><span class="sxs-lookup"><span data-stu-id="33e79-131">Now that you have the correct files, you'll need to edit the generated AppXManifest file within the **manifest** folder.</span></span> <span data-ttu-id="33e79-132">Si el archivo manifest. JSON de la extensión tiene una cadena internacionalizada para el campo "Name", una vez ejecutado ManifoldJS, el nombre de la carpeta de capas más alta no tendrá subrayado e incluirá "MSG".</span><span class="sxs-lookup"><span data-stu-id="33e79-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="33e79-133">Por ejemplo, un archivo manifest. JSON con el siguiente `"name"` campo:</span><span class="sxs-lookup"><span data-stu-id="33e79-133">For example, a manifest.json file with the following `"name"` field:</span></span>

`"name" : "__MSG_appName__"`

<span data-ttu-id="33e79-134">tendrá una carpeta de manifiesto que vive `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="33e79-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>

<span data-ttu-id="33e79-135">En el archivo AppXManifest, tendrás que:</span><span class="sxs-lookup"><span data-stu-id="33e79-135">In the AppXManifest file, you'll need to:</span></span>
 -    <span data-ttu-id="33e79-136">Reemplace los campos de identidad obligatorios y el campo PublisherDisplayName como se describe [aquí](./creating-and-testing-extension-packages.md#app-identity-template-values).</span><span class="sxs-lookup"><span data-stu-id="33e79-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="33e79-137">Ten en cuenta que si solo tienes que empaquetar para pruebas o para la distribución empresarial, puedes usar valores de marcador de posición en lugar de registrarse para una cuenta del centro de desarrollo de Windows.</span><span class="sxs-lookup"><span data-stu-id="33e79-137">Note that if you're only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>
 -    <span data-ttu-id="33e79-138">Reemplace los iconos de marcador de posición de la carpeta activos por los iconos de la extensión con los mismos tamaños (150x150, 50x50, 44x44) y nombres.</span><span class="sxs-lookup"><span data-stu-id="33e79-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="33e79-139">Consulte la guía de [diseño](./../design.md#icons-for-packaging) para obtener información sobre dónde se usan estos iconos.</span><span class="sxs-lookup"><span data-stu-id="33e79-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>
 - <span data-ttu-id="33e79-140">Si su extensión está localizada, siga la guía de localización completa de [extensiones para Edge de Microsoft](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="33e79-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="33e79-141">Si no está localizado, lea solo el [nombre y la descripción del localizador en la sección Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="33e79-141">If it isn't localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>

<span data-ttu-id="33e79-142">Una vez que el archivo appxmanifest. XML esté ordenado, ejecuta el siguiente comando para crear el paquete:</span><span class="sxs-lookup"><span data-stu-id="33e79-142">Once your appxmanifest.xml file is sorted out, run the following command to create your package:</span></span>

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

<span data-ttu-id="33e79-143">El paquete estará ahora en la carpeta **Package** que se encuentra en la carpeta edgeextension.</span><span class="sxs-lookup"><span data-stu-id="33e79-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="33e79-144">Consulte la sección sobre cómo crear y [probar paquetes](./creating-and-testing-extension-packages.md#testing-an-appx-package) de extensiones ' para obtener información sobre cómo transferir el nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="33e79-144">See Creating and testing extension packages' [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section for info on how to sideload your new package.</span></span>

<span data-ttu-id="33e79-145">Una vez que se haya probado el paquete, puedes enviar una solicitud en nuestro [formulario de envío de extensiones](https://aka.ms/extension-request) para que la publiques en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="33e79-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>

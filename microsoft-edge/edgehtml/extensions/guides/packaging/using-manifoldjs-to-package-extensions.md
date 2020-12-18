---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Consulta cómo empaquetar la extensión de Microsoft Edge en un instante con ManifoldJS, la Node.js herramienta de código abierto.
title: Usar ManifoldJS para empaquetar extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 151a8b2ababb25e0964a6fbc2696b5fdc059d084
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236473"
---
# <span data-ttu-id="bc3a7-104">Uso de ManifoldJS para crear paquetes AppX de extensión</span><span class="sxs-lookup"><span data-stu-id="bc3a7-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="bc3a7-105">ManifoldJS es un código abierto Node.js herramienta que le permite crear rápidamente y fácilmente crear un paquete que podrá usar para enviar a Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>  

<span data-ttu-id="bc3a7-106">Si usa mensajería nativa en su extensión, debe omitir el artículo siguiente e ir a la [Mensajería nativa en Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) para obtener instrucciones de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-106">If you use native messaging in your extension, you should skip the following article and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span>  

<span data-ttu-id="bc3a7-107">Antes de empezar, aún necesitarás leer los artículos siguientes.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-107">Before getting started, you will still need to read up on the following articles.</span></span>  

*   [<span data-ttu-id="bc3a7-108">Extensiones en el centro de desarrollo de Windows</span><span class="sxs-lookup"><span data-stu-id="bc3a7-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)  
*   [<span data-ttu-id="bc3a7-109">Localizar paquetes de extensión</span><span class="sxs-lookup"><span data-stu-id="bc3a7-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)  

> [!NOTE]
> <span data-ttu-id="bc3a7-110">El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="bc3a7-111">Una vez que hayas creado, embalado y probado tu extensión, envía una solicitud en nuestro [formulario de envío de extensiones](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span><span class="sxs-lookup"><span data-stu-id="bc3a7-111">Once you have created, packaged and tested your extension, please submit a request on our [extension submission form](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span></span>  

## <span data-ttu-id="bc3a7-112">Instalación de Node.js y ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="bc3a7-112">Installing Node.js and ManifoldJS</span></span>  

<span data-ttu-id="bc3a7-113">Lo primero que debe hacer es instalar [Node.js lts](https://nodejs.org/en/download).</span><span class="sxs-lookup"><span data-stu-id="bc3a7-113">The first things you will need to do is install [Node.js LTS](https://nodejs.org/en/download).</span></span>  
<span data-ttu-id="bc3a7-114">Una vez que tenga node, desde una línea de comandos (preferiblemente PowerShell), ejecute el siguiente comando para instalar ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS.</span></span>  

```shell
npm install -g manifoldjs
```  

<span data-ttu-id="bc3a7-115">Para verificar que ha instalado correctamente ManifoldJS, ejecute `manifoldjs` desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-115">To verify that you have correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="bc3a7-116">Si no se reconoció ManifoldJS, añada `%APPDATA%\npm` a las variables de la ruta.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-116">If ManifoldJS was not recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>  

## <span data-ttu-id="bc3a7-117">Embalaje con ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="bc3a7-117">Packaging with ManifoldJS</span></span>  

<span data-ttu-id="bc3a7-118">Para iniciar el proceso de empaquetado, tendrá que abrir una línea de comandos y cambiar los directorios a una carpeta que será el destino de la extensión empaquetada.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-118">To start the packaging process, you will need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>  

<span data-ttu-id="bc3a7-119">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bc3a7-119">For example:</span></span>

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> <span data-ttu-id="bc3a7-120">El `manifoldjs` comando genera el directorio actual y sobrescribe el contenido.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-120">The `manifoldjs` command outputs in the current directory and overwrites content.</span></span>  

<span data-ttu-id="bc3a7-121">Ahora que se encuentra en la carpeta de destino, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-121">Now that you are in your destination folder, run the following command.</span></span>  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

<span data-ttu-id="bc3a7-122">El `mainifoldjs` comando se puede desglosar en las siguientes partes.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-122">The `mainifoldjs` command can be broken down into the following parts.</span></span>  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bc3a7-123">Cambia el nivel de registro a `debug` para obtener una impresión completa.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-123">Changes the log level to `debug` to get a full print out.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bc3a7-124">Establece la única plataforma en la que ejecutar la conversión `edgeextension` .</span><span class="sxs-lookup"><span data-stu-id="bc3a7-124">Sets the only platform to run the conversion on to `edgeextension`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bc3a7-125">Indica al programa que el formato del manifiesto es un `edgeextension` formato y no tiene que preocuparse si no se puede realizar la validación.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-125">Tells the program that the format of the manifest is an `edgeextension` format and not to care if it fails validation.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="bc3a7-126">La ruta de acceso al manifiesto de la extensión que desea convertir.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-126">The path to the extension manifest that you want to convert.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="bc3a7-127">Cuando ManifoldJS haya terminado de ejecutarse, tendrá una carpeta con el siguiente contenido.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-127">After ManifoldJS has finished running, you will have a folder with the following contents.</span></span>  

```text
┌ My Extension
└┬ edgeextension
 ├- generationInfo.json
 └┬ manifest
  ├- appxmanifest.xml
  ├┬ Assets
  |├- Square150x150Logo.png
  |├- Square44x44Logo.png
  |└- StoreLogo.png    
  └┬ Extension
   ├- manifest.json
   └- popup.html
```  
<!-- 
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
-->  

<span data-ttu-id="bc3a7-128">El generationInfo.jsen archivo es un registro generado al ejecutar ManifoldJS y no se incluirá en el paquete de extensión.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-128">The generationInfo.json file is a log produced by running ManifoldJS and will not be included in your extension package.</span></span> <span data-ttu-id="bc3a7-129">Solo se empaquetará el contenido de la `manifest` carpeta.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-129">Only the contents of the `manifest` folder will be packaged.</span></span> <span data-ttu-id="bc3a7-130">En la carpeta de manifiesto, la carpeta activos contiene las imágenes que se usarán en la interfaz de usuario de Windows y de Microsoft Store, mientras que la carpeta de extensiones tiene el contenido de la extensión dentro de ella.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>  

<span data-ttu-id="bc3a7-131">Ahora que tienes los archivos correctos, tendrás que editar el archivo AppXManifest generado dentro de la `manifest` carpeta.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-131">Now that you have the correct files, you will need to edit the generated AppXManifest file within the `manifest` folder.</span></span> <span data-ttu-id="bc3a7-132">Si el manifest.jsde la extensión de archivo tiene una cadena internacionalizada para el campo "nombre", una vez ejecutado ManifoldJS, el nombre de la carpeta de capas más alta no tendrá subrayado e incluirá "MSG".</span><span class="sxs-lookup"><span data-stu-id="bc3a7-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="bc3a7-133">Por ejemplo, una manifest.jsen un archivo con el `"name"` campo siguiente.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-133">For example, a manifest.json file with the following `"name"` field.</span></span>  

```shell
"name" : "__MSG_appName__"
```  

<span data-ttu-id="bc3a7-134">tendrá una carpeta de manifiesto que vive `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="bc3a7-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>  

<span data-ttu-id="bc3a7-135">En el archivo AppXManifest, necesitarás lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bc3a7-135">In the AppXManifest file, you will need to:</span></span>  

 *   <span data-ttu-id="bc3a7-136">Reemplace los campos de identidad obligatorios y el campo PublisherDisplayName como se describe [aquí](./creating-and-testing-extension-packages.md#app-identity-template-values).</span><span class="sxs-lookup"><span data-stu-id="bc3a7-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="bc3a7-137">Tenga en cuenta que si solo está empaquetando para fines de prueba o para la distribución empresarial, puede usar valores de marcador de posición en lugar de registrarse para una cuenta del centro de desarrollo de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-137">Note that if you are only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>  
 *   <span data-ttu-id="bc3a7-138">Reemplace los iconos de marcador de posición de la carpeta activos por los iconos de la extensión con los mismos tamaños (150x150, 50x50, 44x44) y nombres.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="bc3a7-139">Consulte la guía de [diseño](./../design.md#icons-for-packaging) para obtener información sobre dónde se usan estos iconos.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>  
 *   <span data-ttu-id="bc3a7-140">Si su extensión está localizada, siga la guía de localización completa de [extensiones para Edge de Microsoft](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="bc3a7-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="bc3a7-141">Si no está localizado, solo Lea el [nombre de localizador y la descripción en la sección Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="bc3a7-141">If it is not localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>  

<span data-ttu-id="bc3a7-142">Una vez que el `appxmanifest.xml` archivo esté ordenado, ejecute el siguiente comando para crear el paquete.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-142">Once your `appxmanifest.xml` file is sorted out, run the following command to create your package.</span></span>  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

<span data-ttu-id="bc3a7-143">El paquete estará ahora en la carpeta **Package** que se encuentra en la carpeta edgeextension.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="bc3a7-144">Para obtener más información sobre cómo transferir el nuevo paquete, consulte la sección [pruebas](./creating-and-testing-extension-packages.md#testing-an-appx-package) de creación y prueba de paquetes de extensión.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-144">For more information about how to sideload your new package, see [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing extension packages.</span></span>  

<span data-ttu-id="bc3a7-145">Una vez que se haya probado el paquete, puedes enviar una solicitud en nuestro [formulario de envío de extensiones](https://aka.ms/extension-request) para que la publiques en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="bc3a7-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>  

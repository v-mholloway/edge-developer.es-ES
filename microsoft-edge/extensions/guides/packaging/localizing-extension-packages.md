---
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
description: Aprende a localizar tu paquete de extensión de Microsoft Edge para que esté listo para varias configuraciones regionales en el momento de la publicación.
title: Localización de paquetes de extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: a6a920b80e915bb14c7ea24abcc54105e5b34eb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573579"
---
# <span data-ttu-id="7bfab-104">Localizar las extensiones de Microsoft Edge para Windows y Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7bfab-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="7bfab-105">En esta guía se explica cómo localizar su extensión de Microsoft Edge de modo que esté lista para varias configuraciones regionales en el momento de la publicación.</span><span class="sxs-lookup"><span data-stu-id="7bfab-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span> <span data-ttu-id="7bfab-106">Para localizar completamente su extensión, tendrá que seguir los pasos para Windows y Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7bfab-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>

<span data-ttu-id="7bfab-107">Si desea localizar sus recursos de extensión para Microsoft Edge, puede obtener información sobre cómo usar el marco de i18n en la [Guía de internacionalización](../internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="7bfab-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>


> [!NOTE]
> <span data-ttu-id="7bfab-108">Si tu extensión no es compatible con varios idiomas, puedes omitir [la localización de nombres y descripciones en Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="7bfab-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>


## <span data-ttu-id="7bfab-109">Información general del proceso de localización</span><span class="sxs-lookup"><span data-stu-id="7bfab-109">The localization process overview</span></span>

<span data-ttu-id="7bfab-110">El primer paso para conseguir que tu extensión esté disponible para una gran audiencia es [configurar su AppxManifest](#configuring-the-appxmanifest) para varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="7bfab-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span> <span data-ttu-id="7bfab-111">En Microsoft Store, se mostrará a los usuarios qué idiomas son compatibles con la extensión.</span><span class="sxs-lookup"><span data-stu-id="7bfab-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span> <span data-ttu-id="7bfab-112">Algunos campos en el AppxManifest también deben cambiarse si quieres que el nombre de tu extensión esté [localizado en la interfaz de usuario de Windows y en Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="7bfab-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>


<span data-ttu-id="7bfab-113">Una vez que hayas configurado tu AppxManifest, tendrás que [crear recursos de cadena de JSON](#creating-json-string-resources) para los idiomas que indicaste como admitidos.</span><span class="sxs-lookup"><span data-stu-id="7bfab-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span> <span data-ttu-id="7bfab-114">Esto requiere la creación de un archivo. resjson para cada idioma, en el que cada archivo tiene todas las cadenas de interfaz de usuario de ese idioma.</span><span class="sxs-lookup"><span data-stu-id="7bfab-114">This requires creating a .resjson file for each language, where each file has all the UI strings of that language within it.</span></span>


<span data-ttu-id="7bfab-115">Una vez que se hayan realizado los archivos. resjson para los idiomas admitidos, [será necesario crear un archivo de recursos. PRI](#creating-the-resources-file).</span><span class="sxs-lookup"><span data-stu-id="7bfab-115">After the .resjson files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="7bfab-116">Esto se creará usando un archivo de configuración para la herramienta **MakePRI** que viene con el [SDK de Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="7bfab-116">This will be created by using a configuration file to the **MakePRI** tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span> 

> [!NOTE]
> <span data-ttu-id="7bfab-117">Si solo descarga el SDK de Windows 10 para usar la herramienta MakePri. exe, puede seleccionar solo las características "herramientas de firma del SDK de Windows para aplicaciones de escritorio" y "SDK de Windows para aplicaciones administradas por UWP" para mantener la descarga más clara.</span><span class="sxs-lookup"><span data-stu-id="7bfab-117">If you are only downloading the Windows 10 SDK to use the MakePri.exe tool, you can select only the "Windows SDK Signing Tools for Desktop Apps" and "Windows SDK for UWP Managed Apps" features to keep the download lighter.</span></span> <span data-ttu-id="7bfab-118">La herramienta MakePri. exe aparecerá en subcarpetas de C:\Archivos de programa (x86) \Windows Kits\10\bin\10.0.17713.0.</span><span class="sxs-lookup"><span data-stu-id="7bfab-118">The MakePri.exe tool will appear in subfolders of C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0.</span></span>


<span data-ttu-id="7bfab-119">Una vez que haya cargado su extensión, el paso final es [localizar el nombre y la descripción en Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="7bfab-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>

> [!NOTE]
> <span data-ttu-id="7bfab-120">El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.</span><span class="sxs-lookup"><span data-stu-id="7bfab-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="7bfab-121">Póngase en [contacto con nosotros](https://aka.ms/extension-request) con sus solicitudes para formar parte de Microsoft Store y le daremos una actualización futura.</span><span class="sxs-lookup"><span data-stu-id="7bfab-121">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>



## <span data-ttu-id="7bfab-122">Configuración de AppXManifest</span><span class="sxs-lookup"><span data-stu-id="7bfab-122">Configuring the AppXManifest</span></span>

<span data-ttu-id="7bfab-123">La lista "idiomas admitidos" de la extensión de Microsoft Store se genera en función de sus valores de AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="7bfab-123">Your extension's "Supported languages" list in the Microsoft Store is generated based on its AppXManifest values.</span></span> <span data-ttu-id="7bfab-124">Esta lista se especifica con el `Resource` elemento.</span><span class="sxs-lookup"><span data-stu-id="7bfab-124">This list is specified using the `Resource` element.</span></span>


![imagen de configuración](./../../media/language-app-details.png)

<span data-ttu-id="7bfab-126">Para especificar la lista de idiomas admitidos por su extensión, puede Agregar un `Resource` elemento en el formato que se muestra a continuación (este `Resource` elemento mostrará compatibilidad para inglés, alemán y francés en Microsoft Store):</span><span class="sxs-lookup"><span data-stu-id="7bfab-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below (this `Resource` element will show support for English, German, and French in the Microsoft Store):</span></span>

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

<span data-ttu-id="7bfab-127">Consulte [idiomas admitidos](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) para obtener información sobre los idiomas y códigos de idioma que admite Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7bfab-127">See [Supported languages](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>


<span data-ttu-id="7bfab-128">Para poder especificar cadenas localizadas para todos los elementos públicamente visibles en el AppxManifest, tendrás que usar un identificador de recursos en el formato de `ms-resource:<resource id>` .</span><span class="sxs-lookup"><span data-stu-id="7bfab-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>

<span data-ttu-id="7bfab-129">Los siguientes fragmentos de código hacen que AppxManifest completo.</span><span class="sxs-lookup"><span data-stu-id="7bfab-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="7bfab-130">Los siguientes valores deben recuperarse de archivos de recursos localizados:</span><span class="sxs-lookup"><span data-stu-id="7bfab-130">The following values should be retrieved from localized resource files:</span></span>

- <span data-ttu-id="7bfab-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="7bfab-131">Properties\DisplayName</span></span>
- <span data-ttu-id="7bfab-132">Properties\Description</span><span class="sxs-lookup"><span data-stu-id="7bfab-132">Properties\Description</span></span>
- <span data-ttu-id="7bfab-133">Properties\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="7bfab-133">Properties\PublisherDisplayName</span></span>


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- <span data-ttu-id="7bfab-134">Applications\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="7bfab-134">Applications\Application\VisualElements\DisplayName</span></span>
- <span data-ttu-id="7bfab-135">Applications\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="7bfab-135">Applications\Application\VisualElements\Description</span></span>
- <span data-ttu-id="7bfab-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="7bfab-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>

```xml
<Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
            DisplayName="ms-resource:DisplayName"
       Square150x150Logo="Assets\Square150x150Logo.png"
       Square44x44Logo="Assets\Square44x44Logo.png"
            Description="ms-resource:Description"
        BackgroundColor="transparent">
      </uap:VisualElements>
      <Extensions>
      <uap3:Extension Category="windows.appExtension">
        <uap3:AppExtension Name="com.microsoft.edge.extension"
            Id="MicrosoftTranslate"
            PublicFolder="Extension"
            DisplayName="ms-resource:DisplayName">
        </uap3:AppExtension>
      </uap3:Extension>
      </Extensions>
    </Application>
  </Applications>
```


## <span data-ttu-id="7bfab-137">Localización de recursos de extensión para Windows y Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7bfab-137">Localizing extension resources for Windows and the Microsoft Store</span></span>

<span data-ttu-id="7bfab-138">Ahora que tu AppxManifest está configurado para varios idiomas, hay algunas diferencias clave que debes saber para poder localizar la interfaz de usuario dentro de la extensión y localizar la extensión de Windows y de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7bfab-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>

<span data-ttu-id="7bfab-139">Mientras que las extensiones de Microsoft Edge no se ejecutan fuera de Microsoft Edge, la administración de estas puede ocurrir en Windows.</span><span class="sxs-lookup"><span data-stu-id="7bfab-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span> <span data-ttu-id="7bfab-140">Por ejemplo, los usuarios pueden administrar sus extensiones en la aplicación configuración:</span><span class="sxs-lookup"><span data-stu-id="7bfab-140">For example, users can manage their extensions in the Settings app:</span></span>


![imagen de configuración](./../../media/settings.png)



<span data-ttu-id="7bfab-142">El nombre de la extensión que aparece en la aplicación configuración de Windows procede del AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="7bfab-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span> <span data-ttu-id="7bfab-143">Si este valor está codificado en inglés, la versión en inglés del nombre se mostrará en dispositivos que no están en inglés.</span><span class="sxs-lookup"><span data-stu-id="7bfab-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span> <span data-ttu-id="7bfab-144">Si la marca de su extensión es solo en inglés, puede dejarla codificada.</span><span class="sxs-lookup"><span data-stu-id="7bfab-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>


> [!NOTE]
> <span data-ttu-id="7bfab-145">Si desea usar nombres localizados para su extensión de Microsoft Edge en Windows, asegúrese de que los nombres localizados también estén [disponibles y reservados](./extensions-in-the-windows-dev-center.md#name-reservation) antes de realizar los cambios en el archivo AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="7bfab-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span> <span data-ttu-id="7bfab-146">Si los nombres no están reservados, recibirá el siguiente error al cargar el paquete final en el centro de desarrollo de Windows:</span><span class="sxs-lookup"><span data-stu-id="7bfab-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span></br></br>

![error de idioma](./../../media/language-error.png)</br></br>


<span data-ttu-id="7bfab-148">La infraestructura de localización basada en i18n que se define para las extensiones de JavaScript solo es aplicable dentro del entorno de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7bfab-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>

<span data-ttu-id="7bfab-149">Fuera de Microsoft Edge, dentro de Windows y Microsoft Store, el único marco de trabajo de localización admitido se basa en el marco de localización de la plataforma universal de Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="7bfab-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>

<span data-ttu-id="7bfab-150">Aunque se admiten recursos basados en JSON para aplicaciones de Windows basadas en HTML, el esquema de los recursos de JSON no coincide con el definido para las extensiones de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7bfab-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>


<span data-ttu-id="7bfab-151">A continuación se muestran las diferencias clave en las [aplicaciones de Windows basadas en HTML](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span><span class="sxs-lookup"><span data-stu-id="7bfab-151">The following are the key differences in [HTML based Windows apps](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span></span>
-    <span data-ttu-id="7bfab-152">Los recursos se especifican en archivos. resjson en lugar de archivos. JSON.</span><span class="sxs-lookup"><span data-stu-id="7bfab-152">Resources are specified in .resjson files instead of .json files.</span></span>
-    <span data-ttu-id="7bfab-153">Las configuraciones regionales deben especificarse en el archivo AppXManifest, siendo la primera configuración regional la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7bfab-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>
-    <span data-ttu-id="7bfab-154">Los recursos de aplicaciones de Windows basadas en HTML usan el siguiente esquema:</span><span class="sxs-lookup"><span data-stu-id="7bfab-154">HTML based Windows apps resources use the following schema:</span></span>
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    <span data-ttu-id="7bfab-155">El par de nombre y valor denotado por un carácter de subrayado es comentarios para el recurso de cadena correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7bfab-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>
-    <span data-ttu-id="7bfab-156">los archivos. resjson se compilan en archivos. PRI, que deben incluirse durante la creación del paquete AppX.</span><span class="sxs-lookup"><span data-stu-id="7bfab-156">.resjson files are compiled into .pri files which must be included during AppX package creation.</span></span>


### <span data-ttu-id="7bfab-157">Creación de recursos de cadena JSON</span><span class="sxs-lookup"><span data-stu-id="7bfab-157">Creating JSON string resources</span></span>
<span data-ttu-id="7bfab-158">Con un AppxManifest configurado y las diferencias entre los marcos de trabajo de i18n y UWP resaltados, ya está listo para crear los archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bfab-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>

<span data-ttu-id="7bfab-159">Solo se puede aplicar una cadena de recurso en el manifiesto a paquetes de extensión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7bfab-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span> <span data-ttu-id="7bfab-160">La `DisplayName` cadena suele estar localizada en extensiones de JavaScript y se puede asignar fácilmente a los archivos. resjson que Windows espera.</span><span class="sxs-lookup"><span data-stu-id="7bfab-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the .resjson files that Windows expects.</span></span> <span data-ttu-id="7bfab-161">Suponiendo que este es el único recurso que desea localizar, este es un archivo. resjson de ejemplo que debe crearse:</span><span class="sxs-lookup"><span data-stu-id="7bfab-161">Assuming that this is the only resource that you would like to localize, here is a sample .resjson file that should be created:</span></span>

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

<span data-ttu-id="7bfab-162">El identificador de recurso de cada archivo. resjson debe coincidir con el identificador usado en el AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="7bfab-162">The resource ID in each .resjson file needs to match the ID used in the AppXManifest.</span></span> <span data-ttu-id="7bfab-163">Con el fragmento de código de ejemplo. resjson anterior, la entrada AppXManifest correspondiente debe ser:</span><span class="sxs-lookup"><span data-stu-id="7bfab-163">Using the example .resjson snippet above, the corresponding AppXManifest entry should be:</span></span>

`DisplayName="ms-resource:DisplayName"`

<span data-ttu-id="7bfab-164">Cada idioma que admita la extensión debería tener un archivo resources. resjson correspondiente y colocarse en la siguiente estructura de carpetas:</span><span class="sxs-lookup"><span data-stu-id="7bfab-164">Each language that your extension supports should have a corresponding resources.resjson file and be placed in the following folder structure:</span></span>

![estructura de carpetas de idioma](./../../media/resources-folder.png)


### <span data-ttu-id="7bfab-166">Crear el archivo de recursos</span><span class="sxs-lookup"><span data-stu-id="7bfab-166">Creating the resources file</span></span>
<span data-ttu-id="7bfab-167">Una vez que haya creado todos los archivos. resjson, estará listo para crear el archivo de índice de recursos (PRI) del paquete.</span><span class="sxs-lookup"><span data-stu-id="7bfab-167">Once you've created all your .resjson files, you're ready to create your package resource index (PRI) file.</span></span> <span data-ttu-id="7bfab-168">Este archivo almacena los recursos de todos los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="7bfab-168">This file stores the resources for all your supported languages.</span></span> <span data-ttu-id="7bfab-169">Para hacerlo, puede usar la herramienta **MakePRI** , que se incluye con el SDK de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7bfab-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>


<span data-ttu-id="7bfab-170">En primer lugar, tendrá que crear el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="7bfab-170">First you'll need to create the configuration file.</span></span> <span data-ttu-id="7bfab-171">Define los calificadores y la plataforma predeterminados para los recursos.</span><span class="sxs-lookup"><span data-stu-id="7bfab-171">This defines the default qualifiers and platform for the resources.</span></span> <span data-ttu-id="7bfab-172">Para este ejemplo, convierta el idioma predeterminado inglés (Estados Unidos) y la plataforma Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7bfab-172">For this example, make the default language English (US) and the platform Windows 10.</span></span> <span data-ttu-id="7bfab-173">Para ello, cree un archivo priconfig. XML con el siguiente contenido en la [carpeta raíz]:</span><span class="sxs-lookup"><span data-stu-id="7bfab-173">To do this, create a priconfig.xml file with the following content in the [Root folder]:</span></span>

![priconfig en carpeta](./../../media/priconfig.png)


```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<resources targetOsVersion="10.0.0" majorVersion="1">
    <index root="\" startIndexAt="\">
        <default>
            <qualifier name="Language" value="en-US"/>
            <qualifier name="Contrast" value="standard"/>
            <qualifier name="HomeRegion" value="001"/>
            <qualifier name="TargetSize" value="256"/>
            <qualifier name="LayoutDirection" value="LTR"/>
            <qualifier name="Theme" value="dark"/>
            <qualifier name="AlternateForm" value=""/>
            <qualifier name="DXFeatureLevel" value="DX9"/>
            <qualifier name="Configuration" value=""/>
            <qualifier name="DeviceFamily" value="Universal"/>
            <qualifier name="Custom" value=""/>
        </default>
        <indexer-config type="folder" foldernameAsQualifier="true" filenameAsQualifier="true" qualifierDelimiter="."/>
        <indexer-config type="resw" convertDotsToSlashes="true" initialPath=""/>
        <indexer-config type="resjson" initialPath=""/>
        <indexer-config type="PRI"/>
    </index>
</resources>
```

<span data-ttu-id="7bfab-175">Ahora puede usar el archivo de configuración y la herramienta MakePRI para crear el archivo resources. PRI.</span><span class="sxs-lookup"><span data-stu-id="7bfab-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span> <span data-ttu-id="7bfab-176">Para este ejemplo, la ubicación raíz para el proyecto será [carpeta raíz].</span><span class="sxs-lookup"><span data-stu-id="7bfab-176">For this example, the root location for the project will be [Root folder].</span></span>


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

<span data-ttu-id="7bfab-177">Ahora debe tener un archivo resources. PRI en la carpeta raíz:</span><span class="sxs-lookup"><span data-stu-id="7bfab-177">You should now have one resources.pri file in your root folder:</span></span>

![carpeta recursos](./../../media/resources.png)


## <span data-ttu-id="7bfab-179">Localizar el nombre y la descripción en Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="7bfab-179">Localizing name and description in the Microsoft Store</span></span>

<span data-ttu-id="7bfab-180">Una vez que intentes cargar el paquete localizado completo, el centro de desarrollo de Windows detectará que se admite más de un idioma y verifica que tienes nombres localizados y descripciones para cada uno.</span><span class="sxs-lookup"><span data-stu-id="7bfab-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span> <span data-ttu-id="7bfab-181">Si falta alguno de los valores localizados, el envío se bloqueará hasta que proporcione los valores.</span><span class="sxs-lookup"><span data-stu-id="7bfab-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>

<span data-ttu-id="7bfab-182">Si solo le interesa proporcionar un nombre localizado y una descripción de Microsoft Store (y no de Windows), puede hacerlo si [reserva todos los nombres localizados para su extensión](./extensions-in-the-windows-dev-center.md#name-reservation).</span><span class="sxs-lookup"><span data-stu-id="7bfab-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>


<span data-ttu-id="7bfab-183">Una vez que hayas reservado nombres localizados adicionales, puedes crear un envío actualizado.</span><span class="sxs-lookup"><span data-stu-id="7bfab-183">Once you've reserved additional localized names, you can create an updated submission.</span></span> <span data-ttu-id="7bfab-184">En la sección Descripción puede administrar idiomas adicionales para la descripción de Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="7bfab-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>

![Descripción de la aplicación en Japonés](./../../media/manage-description-languages.png)

<span data-ttu-id="7bfab-186">Una vez que haya seleccionado "administrar idiomas adicionales", tendrá que seleccionar los idiomas que desea agregar a la descripción de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7bfab-186">Once you've selected "Manage additional languages", you'll get to select which languages you want to add to your Microsoft Store listing.</span></span> <span data-ttu-id="7bfab-187">El nuevo idioma se mostrará como "idioma de Descripción adicional" en la sección "Descripción".</span><span class="sxs-lookup"><span data-stu-id="7bfab-187">The new language will show up as 'Additional description language' in the "Description" section.</span></span>

<span data-ttu-id="7bfab-188">Puede hacer clic en el vínculo individual de la sección "Descripción" para proporcionar un nombre localizado y una descripción, notas de la versión y recursos visuales para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="7bfab-188">You can click on the individual link in the "Description" section to provide a localized name and description, release notes, and visual assets for each language.</span></span> <span data-ttu-id="7bfab-189">La descripción de Microsoft Store no se extrae del AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="7bfab-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span> <span data-ttu-id="7bfab-190">Cada descripción localizada debe introducirse manualmente en el centro de desarrollo de Windows:</span><span class="sxs-lookup"><span data-stu-id="7bfab-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>

![Descripción de la aplicación en Japonés](./../../media/japanese-app-description.png)

<span data-ttu-id="7bfab-192">Una vez que se envíen las descripciones localizadas y se publique la extensión, cualquier persona que tenga acceso a una página localizada de la extensión en Microsoft Store verá la siguiente interfaz de usuario:</span><span class="sxs-lookup"><span data-stu-id="7bfab-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>

![tienda Windows en Japonés](./../../media/japanese-windows-store.png)
 

## <span data-ttu-id="7bfab-194">Ejemplos de AppxManifest</span><span class="sxs-lookup"><span data-stu-id="7bfab-194">AppxManifest samples</span></span>

### <span data-ttu-id="7bfab-195">AppxManifest no localizado</span><span class="sxs-lookup"><span data-stu-id="7bfab-195">Non-localized AppxManifest</span></span>
<span data-ttu-id="7bfab-196">En el ejemplo siguiente se muestra un AppxManifest que no está localizado y solo admite la configuración regional "en-es".</span><span class="sxs-lookup"><span data-stu-id="7bfab-196">The following example shows an AppxManifest that isn't localized, and only supports the "en-us" locale.</span></span>


```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>Jigsaw</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="Jigsaw"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="This is a jigsaw puzzle app"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="Jigsaw">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```


#### <span data-ttu-id="7bfab-197">AppxManifest localizado</span><span class="sxs-lookup"><span data-stu-id="7bfab-197">Localized AppxManifest</span></span>
<span data-ttu-id="7bfab-198">Este ejemplo AppxManifest está localizado para ocho otras configuraciones regionales además de "en-es".</span><span class="sxs-lookup"><span data-stu-id="7bfab-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="7bfab-199">Observe las `ms-resource:<resource id>` apariciones:</span><span class="sxs-lookup"><span data-stu-id="7bfab-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>


```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>ms-resource:DisplayName</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
        <Resource Language="de" />
        <Resource Language="en" />
        <Resource Language="en-gb" />
        <Resource Language="es" />
        <Resource Language="fr" />
        <Resource Language="it" />
        <Resource Language="ja" />
        <Resource Language="zh-cn" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="ms-resource:DisplayName"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="ms-resource:Description"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="ms-resource:DisplayName">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```

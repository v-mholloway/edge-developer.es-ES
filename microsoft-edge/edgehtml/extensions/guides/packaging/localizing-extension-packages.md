---
description: Obtenga información sobre cómo encontrar el paquete de extensión de Microsoft Edge para que esté listo para varias configuraciones regionales tras la versión.
title: Localizar paquetes de extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
keywords: edge, web development, html, css, javascript, developer
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5dd21f82fd746ad619e9d89a1526ff6a511d615
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397723"
---
# <a name="localizing-microsoft-edge-extensions-for-windows-and-the-microsoft-store"></a><span data-ttu-id="2a91c-104">Localización de extensiones de Microsoft Edge para Windows y Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="2a91c-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="2a91c-105">En esta guía se explica cómo encontrar la extensión de Microsoft Edge para que esté lista para varias configuraciones regionales tras la versión.</span><span class="sxs-lookup"><span data-stu-id="2a91c-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span>  <span data-ttu-id="2a91c-106">Para encontrar completamente la extensión, tendrás que seguir los pasos para Windows y la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="2a91c-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>  

<span data-ttu-id="2a91c-107">Si desea encontrar los recursos de extensión para Microsoft Edge, puede obtener información sobre cómo usar el marco de i18n en la [guía de internacionalización](../internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="2a91c-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="2a91c-108">Si la extensión no admite varios idiomas, puedes pasar a [Localización](#localizing-name-and-description-in-the-microsoft-store)de nombre y descripción en Microsoft Store .</span><span class="sxs-lookup"><span data-stu-id="2a91c-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>  

## <a name="the-localization-process-overview"></a><span data-ttu-id="2a91c-109">Introducción al proceso de localización</span><span class="sxs-lookup"><span data-stu-id="2a91c-109">The localization process overview</span></span>  

<span data-ttu-id="2a91c-110">El primer paso para que la extensión esté disponible para una amplia audiencia es [configurar su AppxManifest](#configuring-the-appxmanifest) para varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="2a91c-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span>  <span data-ttu-id="2a91c-111">En Microsoft Store, esto mostrará a los usuarios qué idiomas admite la extensión.</span><span class="sxs-lookup"><span data-stu-id="2a91c-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span>  <span data-ttu-id="2a91c-112">Algunos campos de AppxManifest también tendrán que cambiarse si quieres que el nombre de la extensión esté localizado en la interfaz de usuario de Windows y la [Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="2a91c-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>  

<span data-ttu-id="2a91c-113">Una vez configurado appxManifest, tendrás que crear recursos de cadena [JSON](#creating-json-string-resources) para los idiomas que indicaste como compatibles.</span><span class="sxs-lookup"><span data-stu-id="2a91c-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span>  <span data-ttu-id="2a91c-114">Esto requiere crear un archivo para cada idioma, donde cada archivo tiene todas las cadenas de interfaz de usuario `.resjson` de ese idioma dentro de él.</span><span class="sxs-lookup"><span data-stu-id="2a91c-114">This requires creating a `.resjson` file for each language, where each file has all the UI strings of that language within it.</span></span>  

<span data-ttu-id="2a91c-115">Una vez creados los archivos para los idiomas compatibles, tendrá que crearse un archivo de recursos `.resjson` [.pri](#creating-the-resources-file).</span><span class="sxs-lookup"><span data-stu-id="2a91c-115">After the `.resjson` files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="2a91c-116">Esto se creará mediante el uso de un archivo de configuración para la herramienta MakePRI que viene con [el SDK de Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="2a91c-116">This will be created by using a configuration file to the MakePRI tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span>  

> [!NOTE]
> <span data-ttu-id="2a91c-117">Si solo estás descargando el SDK de Windows 10 para usar la herramienta, solo puedes seleccionar las características herramientas de firma de Windows SDK para aplicaciones de escritorio y Windows SDK para aplicaciones administradas para UWP para mantener la descarga más `MakePri.exe` ligera.  </span><span class="sxs-lookup"><span data-stu-id="2a91c-117">If you are only downloading the Windows 10 SDK to use the `MakePri.exe` tool, you can select only the **Windows SDK Signing Tools for Desktop Apps** and **Windows SDK for UWP Managed App** features to keep the download lighter.</span></span>  <span data-ttu-id="2a91c-118">La `MakePri.exe` herramienta aparecerá en subcarpetas de `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0` .</span><span class="sxs-lookup"><span data-stu-id="2a91c-118">The `MakePri.exe` tool will appear in subfolders of `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0`.</span></span>  

<span data-ttu-id="2a91c-119">Una vez que hayas cargado la extensión, el paso final es encontrar el nombre y la [descripción en Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="2a91c-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>  

> [!NOTE]
> <span data-ttu-id="2a91c-120">Enviar una extensión de Microsoft Edge a la Microsoft Store es actualmente una funcionalidad restringida.</span><span class="sxs-lookup"><span data-stu-id="2a91c-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="2a91c-121">**Llámenos con** sus solicitudes para formar parte de Microsoft Store y le consideraremos para una actualización futura.</span><span class="sxs-lookup"><span data-stu-id="2a91c-121">**Reach out to us** with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>  

## <a name="configuring-the-appxmanifest"></a><span data-ttu-id="2a91c-122">Configuración de AppXManifest</span><span class="sxs-lookup"><span data-stu-id="2a91c-122">Configuring the AppXManifest</span></span>  

<span data-ttu-id="2a91c-123">La lista de idiomas admitidos de la extensión en Microsoft Store se genera en función de sus valores de AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="2a91c-123">Your extension's Supported languages list in the Microsoft Store is generated based on its AppXManifest values.</span></span>  <span data-ttu-id="2a91c-124">Esta lista se especifica mediante el `Resource` elemento.</span><span class="sxs-lookup"><span data-stu-id="2a91c-124">This list is specified using the `Resource` element.</span></span>  

![Detalles de la aplicación](../../media/language-app-details.png)  

<span data-ttu-id="2a91c-126">Para especificar la lista de idiomas compatibles con la extensión, puede agregar un elemento en el formato que se muestra a continuación \(Este elemento mostrará compatibilidad con inglés, alemán y francés en `Resource` `Resource` Microsoft Store\):</span><span class="sxs-lookup"><span data-stu-id="2a91c-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below \(this `Resource` element will show support for English, German, and French in the Microsoft Store\):</span></span>  

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```  

<span data-ttu-id="2a91c-127">Consulta [Idiomas admitidos](/windows/uwp/publish/supported-languages) para obtener información sobre los idiomas/códigos de idioma compatibles con Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="2a91c-127">See [Supported languages](/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>  

<span data-ttu-id="2a91c-128">Para especificar cadenas localizadas para todos los elementos visibles públicamente en AppxManifest, tendrá que usar un identificador de recursos con el formato `ms-resource:<resource id>` de .</span><span class="sxs-lookup"><span data-stu-id="2a91c-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>  

<span data-ttu-id="2a91c-129">Los fragmentos de código siguientes hacen un AppxManifest completo.</span><span class="sxs-lookup"><span data-stu-id="2a91c-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="2a91c-130">Los siguientes valores deben recuperarse de los archivos de recursos localizados:</span><span class="sxs-lookup"><span data-stu-id="2a91c-130">The following values should be retrieved from localized resource files:</span></span>  

*   <span data-ttu-id="2a91c-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a91c-131">Properties\DisplayName</span></span>  
*   <span data-ttu-id="2a91c-132">Propiedades\Descripción</span><span class="sxs-lookup"><span data-stu-id="2a91c-132">Properties\Description</span></span>  
*   <span data-ttu-id="2a91c-133">Properties\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="2a91c-133">Properties\PublisherDisplayName</span></span>  

```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```  

*   <span data-ttu-id="2a91c-134">Aplicaciones\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a91c-134">Applications\Application\VisualElements\DisplayName</span></span>  
*   <span data-ttu-id="2a91c-135">Aplicaciones\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="2a91c-135">Applications\Application\VisualElements\Description</span></span>  
*   <span data-ttu-id="2a91c-136">Aplicaciones\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a91c-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>  

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

## <a name="localizing-extension-resources-for-windows-and-the-microsoft-store"></a><span data-ttu-id="2a91c-137">Localización de recursos de extensión para Windows y Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="2a91c-137">Localizing extension resources for Windows and the Microsoft Store</span></span>  

<span data-ttu-id="2a91c-138">Ahora que AppxManifest está configurado para varios idiomas, hay algunas diferencias clave que debes saber entre la localización de la interfaz de usuario dentro de la extensión y la localización de la extensión para Windows y microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="2a91c-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>  

<span data-ttu-id="2a91c-139">Aunque las extensiones de Microsoft Edge no se ejecutan fuera de Microsoft Edge, la administración de ellas puede producirse en Windows.</span><span class="sxs-lookup"><span data-stu-id="2a91c-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span>  <span data-ttu-id="2a91c-140">Por ejemplo, los usuarios pueden administrar sus extensiones en la aplicación Configuración:</span><span class="sxs-lookup"><span data-stu-id="2a91c-140">For example, users can manage their extensions in the Settings app:</span></span>  

![aplicación de configuración](../../media/settings.png)  

<span data-ttu-id="2a91c-142">El nombre de la extensión que aparece en la aplicación Configuración de Windows proviene del AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="2a91c-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span>  <span data-ttu-id="2a91c-143">Si este valor está codificado en inglés, la versión en inglés del nombre aparecerá en dispositivos Windows que no son de inglés.</span><span class="sxs-lookup"><span data-stu-id="2a91c-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span>  <span data-ttu-id="2a91c-144">Si la personal de marca de la extensión es solo en inglés, está bien dejarla codificada de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="2a91c-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>  

> [!NOTE]
> <span data-ttu-id="2a91c-145">Si quieres usar nombres localizados para la extensión de Microsoft Edge [](./extensions-in-the-windows-dev-center.md#name-reservation) en Windows, asegúrate de que los nombres localizados también estén disponibles y reservados antes de realizar los cambios en el archivo AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="2a91c-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span>  <span data-ttu-id="2a91c-146">Si los nombres no están reservados, se producirá el siguiente error al cargar el paquete final en el Centro de desarrollo de Windows:</span><span class="sxs-lookup"><span data-stu-id="2a91c-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span>  
> 
> ![error de idioma](../../media/language-error.png)  

<span data-ttu-id="2a91c-148">La infraestructura de localización basada en i18n que se define para las extensiones de JavaScript solo se aplica en el entorno de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a91c-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>  

<span data-ttu-id="2a91c-149">Fuera de Microsoft Edge, dentro de Windows y microsoft Store, el único marco de localización compatible se basa en el marco de localización de la Plataforma universal de Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="2a91c-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>  

<span data-ttu-id="2a91c-150">Aunque se admiten recursos basados en JSON para aplicaciones de Windows basadas en HTML, el esquema de los recursos JSON no coincide con el definido para las extensiones de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2a91c-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>  

<span data-ttu-id="2a91c-151">Las siguientes son las principales diferencias en las [aplicaciones de Windows basadas en HTML:](/previous-versions/windows/apps/hh465228(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="2a91c-151">The following are the key differences in [HTML based Windows apps](/previous-versions/windows/apps/hh465228(v=win.10)):</span></span>  

*   <span data-ttu-id="2a91c-152">Los recursos se especifican en `.resjson` archivos en lugar de `.json` archivos.</span><span class="sxs-lookup"><span data-stu-id="2a91c-152">Resources are specified in `.resjson` files instead of `.json` files.</span></span>  
*   <span data-ttu-id="2a91c-153">Las configuraciones regionales admitidas deben especificarse en el archivo AppXManifest, siendo la primera configuración regional la configuración regional predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2a91c-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>  
*   <span data-ttu-id="2a91c-154">Los recursos de aplicaciones de Windows basados en HTML usan el esquema siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a91c-154">HTML based Windows apps resources use the following schema:</span></span>  
    
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```  
    
    <span data-ttu-id="2a91c-155">El par nombre/valor que indica un carácter de subrayado son comentarios para el recurso de cadena correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2a91c-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>  
*   `.resjson` <span data-ttu-id="2a91c-156">los archivos se compilan en `.pri` archivos que deben incluirse durante la creación del paquete AppX.</span><span class="sxs-lookup"><span data-stu-id="2a91c-156">files are compiled into `.pri` files which must be included during AppX package creation.</span></span>  
    
### <a name="creating-json-string-resources"></a><span data-ttu-id="2a91c-157">Creación de recursos de cadena JSON</span><span class="sxs-lookup"><span data-stu-id="2a91c-157">Creating JSON string resources</span></span>  

<span data-ttu-id="2a91c-158">Con un AppxManifest configurado en la mano y las diferencias entre los marcos de localización de i18n y UWP resaltados, estás listo para crear los archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a91c-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>  

<span data-ttu-id="2a91c-159">Solo se aplica una cadena de recurso en el manifiesto a los paquetes de extensión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a91c-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span>  <span data-ttu-id="2a91c-160">La cadena se localiza comúnmente en extensiones de JavaScript y se puede asignar fácilmente a `DisplayName` los archivos que Windows `.resjson` espera.</span><span class="sxs-lookup"><span data-stu-id="2a91c-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the `.resjson` files that Windows expects.</span></span>  <span data-ttu-id="2a91c-161">Suponiendo que este es el único recurso que le gustaría encontrar, este es un archivo de ejemplo `.resjson` que debe crearse:</span><span class="sxs-lookup"><span data-stu-id="2a91c-161">Assuming that this is the only resource that you would like to localize, here is a sample `.resjson` file that should be created:</span></span>  

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```  

<span data-ttu-id="2a91c-162">El identificador de recurso de cada `.resjson` archivo debe coincidir con el identificador usado en AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="2a91c-162">The resource ID in each `.resjson` file needs to match the ID used in the AppXManifest.</span></span>  <span data-ttu-id="2a91c-163">Con el fragmento `.resjson` de código anterior, la entrada AppXManifest correspondiente debe ser:</span><span class="sxs-lookup"><span data-stu-id="2a91c-163">Using the example `.resjson` snippet above, the corresponding AppXManifest entry should be:</span></span>  

`DisplayName="ms-resource:DisplayName"`  

<span data-ttu-id="2a91c-164">Cada idioma compatible con la extensión debe tener un archivo de recursos correspondiente `.resjson` y colocarse en la siguiente estructura de carpetas:</span><span class="sxs-lookup"><span data-stu-id="2a91c-164">Each language that your extension supports should have a corresponding resources `.resjson` file and be placed in the following folder structure:</span></span>  

![estructura de carpetas de idioma](../../media/resources-folder.png)  

### <a name="creating-the-resources-file"></a><span data-ttu-id="2a91c-166">Creación del archivo de recursos</span><span class="sxs-lookup"><span data-stu-id="2a91c-166">Creating the resources file</span></span>  

<span data-ttu-id="2a91c-167">Una vez que haya creado todos los archivos, estará listo para crear el archivo de índice de recursos del `.resjson` paquete \(PRI\).</span><span class="sxs-lookup"><span data-stu-id="2a91c-167">Once you've created all your `.resjson` files, you're ready to create your package resource index \(PRI\) file.</span></span>  <span data-ttu-id="2a91c-168">Este archivo almacena los recursos para todos los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="2a91c-168">This file stores the resources for all your supported languages.</span></span>  <span data-ttu-id="2a91c-169">Para ello, puedes usar la **herramienta MakePRI** que se incluye con el SDK de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2a91c-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>  

<span data-ttu-id="2a91c-170">Primero tendrá que crear el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a91c-170">First you'll need to create the configuration file.</span></span>  <span data-ttu-id="2a91c-171">Esto define los calificadores y la plataforma predeterminados para los recursos.</span><span class="sxs-lookup"><span data-stu-id="2a91c-171">This defines the default qualifiers and platform for the resources.</span></span>  <span data-ttu-id="2a91c-172">Para este ejemplo, haz que el idioma predeterminado `English (US)` y la plataforma Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2a91c-172">For this example, make the default language `English (US)` and the platform Windows 10.</span></span>  <span data-ttu-id="2a91c-173">Para ello, cree un `priconfig.xml` archivo con el siguiente contenido en `[Root folder]` :</span><span class="sxs-lookup"><span data-stu-id="2a91c-173">To do this, create a `priconfig.xml` file with the following content in the `[Root folder]`:</span></span>  

![priconfig en la carpeta](../../media/priconfig.png)  

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

<span data-ttu-id="2a91c-175">Ahora puede usar el archivo de configuración y la herramienta MakePRI para crear el archivo resources.pri.</span><span class="sxs-lookup"><span data-stu-id="2a91c-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span>  <span data-ttu-id="2a91c-176">En este ejemplo, la ubicación raíz del proyecto será `[Root folder]` .</span><span class="sxs-lookup"><span data-stu-id="2a91c-176">For this example, the root location for the project will be `[Root folder]`.</span></span>  

```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```  

<span data-ttu-id="2a91c-177">Ahora debería tener un archivo resources.pri en la carpeta raíz:</span><span class="sxs-lookup"><span data-stu-id="2a91c-177">You should now have one resources.pri file in your root folder:</span></span>  

![carpeta resources](../../media/resources.png)  

## <a name="localizing-name-and-description-in-the-microsoft-store"></a><span data-ttu-id="2a91c-179">Localización de nombre y descripción en Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="2a91c-179">Localizing name and description in the Microsoft Store</span></span>  

<span data-ttu-id="2a91c-180">Una vez que intentes cargar el paquete completo y localizado, el Centro de desarrollo de Windows detectará que se admite más de un idioma y comprobará que tienes nombres y descripciones localizados correspondientes para cada uno.</span><span class="sxs-lookup"><span data-stu-id="2a91c-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span>  <span data-ttu-id="2a91c-181">Si falta alguno de los valores localizados, el envío se bloqueará hasta que proporcione los valores.</span><span class="sxs-lookup"><span data-stu-id="2a91c-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>  

<span data-ttu-id="2a91c-182">Si solo estás interesado en proporcionar un nombre localizado y una descripción para la Microsoft Store (y no Windows), puedes hacerlo reservando todos los nombres localizados para [la extensión](./extensions-in-the-windows-dev-center.md#name-reservation).</span><span class="sxs-lookup"><span data-stu-id="2a91c-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>  

<span data-ttu-id="2a91c-183">Una vez reservados los nombres localizados adicionales, puede crear un envío actualizado.</span><span class="sxs-lookup"><span data-stu-id="2a91c-183">Once you've reserved additional localized names, you can create an updated submission.</span></span>  <span data-ttu-id="2a91c-184">En la sección descripción, puedes administrar idiomas adicionales para tu descripción de Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="2a91c-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>  

![Administrar idiomas de descripción](../../media/manage-description-languages.png)  

<span data-ttu-id="2a91c-186">Una vez que hayas seleccionado **Administrar idiomas**adicionales, podrás seleccionar los idiomas que quieres agregar a la descripción de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="2a91c-186">Once you've selected **Manage additional languages**, you'll get to select which languages you want to add to your Microsoft Store listing.</span></span>  <span data-ttu-id="2a91c-187">El nuevo idioma se mostrará como **Idioma de descripción adicional en** la **sección** Descripción.</span><span class="sxs-lookup"><span data-stu-id="2a91c-187">The new language will show up as **Additional description language** in the **Description** section.</span></span>  

<span data-ttu-id="2a91c-188">Puede hacer clic en el  vínculo individual de la sección Descripción para proporcionar un nombre y una descripción localizados, notas de la versión y activos visuales para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="2a91c-188">You can click on the individual link in the **Description** section to provide a localized name and description, release notes, and visual assets for each language.</span></span>  <span data-ttu-id="2a91c-189">La descripción de Microsoft Store no se extrae de AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="2a91c-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span>  <span data-ttu-id="2a91c-190">Cada descripción localizada debe especificarse manualmente en el Centro de desarrollo de Windows:</span><span class="sxs-lookup"><span data-stu-id="2a91c-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>  

![Descripción de la aplicación japonesa](../../media/japanese-app-description.png)  

<span data-ttu-id="2a91c-192">Una vez que se envían las descripciones localizadas y se publica la extensión, cualquier persona que acceda a una página localizada de la extensión en Microsoft Store verá la siguiente interfaz de usuario:</span><span class="sxs-lookup"><span data-stu-id="2a91c-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>  

![Tienda de windows japonesa](../../media/japanese-windows-store.png)  

## <a name="appxmanifest-samples"></a><span data-ttu-id="2a91c-194">Ejemplos de AppxManifest</span><span class="sxs-lookup"><span data-stu-id="2a91c-194">AppxManifest samples</span></span>  

### <a name="non-localized-appxmanifest"></a><span data-ttu-id="2a91c-195">AppxManifest no localizado</span><span class="sxs-lookup"><span data-stu-id="2a91c-195">Non-localized AppxManifest</span></span>  

<span data-ttu-id="2a91c-196">En el ejemplo siguiente se muestra un AppxManifest que no está localizado y solo admite la `en-us` configuración regional.</span><span class="sxs-lookup"><span data-stu-id="2a91c-196">The following example shows an AppxManifest that isn't localized, and only supports the `en-us` locale.</span></span>  

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

#### <a name="localized-appxmanifest"></a><span data-ttu-id="2a91c-197">Localized AppxManifest</span><span class="sxs-lookup"><span data-stu-id="2a91c-197">Localized AppxManifest</span></span>  

<span data-ttu-id="2a91c-198">Esta muestra de AppxManifest se localiza para otras ocho configuraciones regionales además de "en-us".</span><span class="sxs-lookup"><span data-stu-id="2a91c-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="2a91c-199">Observe las `ms-resource:<resource id>` repeticiones:</span><span class="sxs-lookup"><span data-stu-id="2a91c-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>  

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

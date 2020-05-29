---
ms.assetid: 5eefa3d8-8626-4486-bd90-1361400d6468
description: Más información sobre cómo empaquetar la extensión de Microsoft Edge manualmente y probarla para ver si está empaquetada correctamente.
title: Crear y probar paquetes de extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, empaquetado
ms.custom: seodec18
ms.openlocfilehash: a76737d76c8f08c8e79992f0804fdbd34d4ed970
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573584"
---
# <span data-ttu-id="2caa7-104">Crear y probar un paquete AppX de extensión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2caa7-104">Creating and testing a Microsoft Edge extension AppX package</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="2caa7-105">Las extensiones de Microsoft Edge se empaquetan como AppX, de forma similar a como se empaquetan las aplicaciones universales de Windows.</span><span class="sxs-lookup"><span data-stu-id="2caa7-105">Microsoft Edge extensions are packaged as AppX, similar to how Universal Windows Apps are packaged.</span></span> <span data-ttu-id="2caa7-106">A partir de la actualización de aniversario de Windows 10, se ha introducido un nuevo esquema para AppX que permite a un AppX incluir una extensión de Microsoft Edge como contenido.</span><span class="sxs-lookup"><span data-stu-id="2caa7-106">As of Windows 10 Anniversary Update, a new schema has been introduced for AppX that allows an AppX to include a Microsoft Edge extension as its content.</span></span>

<span data-ttu-id="2caa7-107">Si ya sabes cómo se crean las extensiones de Microsoft Edge AppXs, puedes omitir el uso de la [extensión de ManifoldJS a empaquetar](./using-manifoldjs-to-package-extensions.md) para obtener más información sobre cómo usar una herramienta basada en node. js para hacer todo esto.</span><span class="sxs-lookup"><span data-stu-id="2caa7-107">If you already know how Microsoft Edge extension AppXs are created, you can skip to [Using ManifoldJS to package extension](./using-manifoldjs-to-package-extensions.md) to learn how to use a Node.js based tool to do all of this for you!</span></span>

> [!NOTE]
> <span data-ttu-id="2caa7-108">El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.</span><span class="sxs-lookup"><span data-stu-id="2caa7-108">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="2caa7-109">Una vez que hayas creado, embalado y probado tu extensión, envía una solicitud en nuestro [formulario de envío de extensiones](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="2caa7-109">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>



## <span data-ttu-id="2caa7-110">Preparar la carpeta de presentación</span><span class="sxs-lookup"><span data-stu-id="2caa7-110">Preparing the submission folder</span></span>

<span data-ttu-id="2caa7-111">Para preparar la extensión para el envío, debe crear una carpeta con la estructura siguiente:</span><span class="sxs-lookup"><span data-stu-id="2caa7-111">To prepare your extension for submission, you need to create a folder with the following structure:</span></span>

![imagen de la estructura de carpetas.](./../../media/packaging_folder-structure.png)

<span data-ttu-id="2caa7-114">En la raíz de la carpeta, debes incluir un archivo AppXManifest. Xml.</span><span class="sxs-lookup"><span data-stu-id="2caa7-114">At the root of the folder, you should include an AppXManifest.xml file.</span></span> <span data-ttu-id="2caa7-115">Este archivo se usa para especificar el contenido y el diseño del paquete.</span><span class="sxs-lookup"><span data-stu-id="2caa7-115">This file is used to specify the contents and layout of the package.</span></span>

<span data-ttu-id="2caa7-116">También debe tener una carpeta de activos que contenga los activos de la interfaz de usuario que se usarán en Microsoft Store y una carpeta de extensiones que contiene los archivos de extensión (scripts, iconos, etc.).</span><span class="sxs-lookup"><span data-stu-id="2caa7-116">You should also have an Assets folder which contains the UI assets to be used in the Microsoft Store, and an Extension folder that contains your extension's files (scripts, icons, etc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2caa7-117">Puede crear una estructura de carpetas diferente para el paquete, pero la estructura de carpetas debe coincidir con los valores de AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="2caa7-117">You can create a different folder structure for your package, but the folder structure must match the AppXManifest values.</span></span>

### <span data-ttu-id="2caa7-118">AppXManifest. XML</span><span class="sxs-lookup"><span data-stu-id="2caa7-118">AppXManifest.xml</span></span>
<span data-ttu-id="2caa7-119">El archivo AppXManifest es un documento XML que contiene información que el sistema necesita para implementar, mostrar o actualizar una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="2caa7-119">The AppXManifest file is an XML document that contains info the system needs to deploy, display, or update a Windows app.</span></span> <span data-ttu-id="2caa7-120">Este archivo también incluye identidad de paquete, capacidades y elementos visuales.</span><span class="sxs-lookup"><span data-stu-id="2caa7-120">This file also includes package identity, capabilities, and visual elements.</span></span> <span data-ttu-id="2caa7-121">Cada paquete de la aplicación debe incluir un archivo AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="2caa7-121">Every app package must include one AppXManifest file.</span></span>

<span data-ttu-id="2caa7-122">Los desarrolladores pueden usar la siguiente plantilla para el archivo AppXManifest. xml:</span><span class="sxs-lookup"><span data-stu-id="2caa7-122">Developers can use the following template for their AppXManifest.xml file:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
  xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
  xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
  xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
  IgnorableNamespaces="uap3">

  <Identity
    Name="[REPLACE WITH PACKAGE/IDENTITYNAME]"
    Publisher="[REPLACE WITH PACKAGE/IDENTITY/PUBLISHER]"
    Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]"/>

  <Properties>
    <DisplayName>[REPLACE WITH RESERVED STORE NAME]</DisplayName>
    <PublisherDisplayName>[REPLACE WITH PACKAGE/PROPERTIES/PUBLISHERDISPLAYNAME]</PublisherDisplayName>
    <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
  </Properties>

  <Dependencies>
    <TargetDeviceFamily Name="Windows.Desktop"
      MinVersion="10.0.14393.0"
      MaxVersionTested="10.0.14800.0" />
  </Dependencies>

  <Resources>
    <Resource Language="en-us"/>
  </Resources>

  <Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
        DisplayName="[REPLACE WITH RESERVED STORE NAME]"
        Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
        Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
        Description="This is the description of the extension"
        BackgroundColor="white">
      </uap:VisualElements>
    <Extensions>
    <uap3:Extension Category="windows.appExtension">
    <uap3:AppExtension Name="com.microsoft.edge.extension"
        Id="EdgeExtension"
        PublicFolder="Extension"
      DisplayName="[REPLACE WITH RESERVED STORE NAME]">
    </uap3:AppExtension>
    </uap3:Extension>
    </Extensions>
 </Application>
</Applications>
</Package>
```

#### <span data-ttu-id="2caa7-123">Valores de la plantilla de identidad de aplicación</span><span class="sxs-lookup"><span data-stu-id="2caa7-123">App identity template values</span></span>
<span data-ttu-id="2caa7-124">Una vez que hayas [reservado el nombre de tu extensión](./extensions-in-the-windows-dev-center.md#name-reservation) a través del centro de desarrollo de Windows, podrás encontrar la información de identidad del paquete necesaria para reemplazar los siguientes valores en AppXManifest. xml:</span><span class="sxs-lookup"><span data-stu-id="2caa7-124">Once you've [reserved the name of your extension](./extensions-in-the-windows-dev-center.md#name-reservation) through the Windows Dev Center, you'll be able to find the necessary package identity information needed to replace the following values in AppXManifest.xml:</span></span>

- `Name`
- `Publisher`
- `DisplayName`
- `PublisherDisplayName`

<span data-ttu-id="2caa7-125">Puede acceder a la página identidad de la aplicación siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="2caa7-125">You can access your App identity page using the following steps:</span></span>

1. <span data-ttu-id="2caa7-126">Vaya al [centro de desarrollo de Windows](https://developer.microsoft.com/windows/).</span><span class="sxs-lookup"><span data-stu-id="2caa7-126">Navigate to [Windows Dev Center](https://developer.microsoft.com/windows/).</span></span>
2. <span data-ttu-id="2caa7-127">Inicie sesión en su cuenta de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="2caa7-127">Sign in to your developer account.</span></span>
3. <span data-ttu-id="2caa7-128">Vaya al panel.</span><span class="sxs-lookup"><span data-stu-id="2caa7-128">Navigate to the Dashboard.</span></span>
4. <span data-ttu-id="2caa7-129">Seleccione el nombre de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2caa7-129">Select the name of your extension.</span></span>

   ![lista de extensiones](./../../media/select-app.png)
5. <span data-ttu-id="2caa7-131">Vaya a la página identidad de la aplicación, que se encuentra en la sección Administración de aplicaciones (después de haber registrado la aplicación).</span><span class="sxs-lookup"><span data-stu-id="2caa7-131">Navigate to the App identity page which is under the App management section (after you've registered your app).</span></span>

   ![Página identidad de la aplicación](./../../media/app-identity.png)


<span data-ttu-id="2caa7-133">Ahora puede rellenar la plantilla AppXManifest con los valores de la página identidad de la aplicación, como se indica en la plantilla:</span><span class="sxs-lookup"><span data-stu-id="2caa7-133">You can now populate the AppXManifest template with values from the App identity page, as indicated in the template:</span></span>


```xml
<Identity
  Name="37369abigailc.MyExtension"
  Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
  Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]" />

<Properties>
  <DisplayName>My Extension</DisplayName>
  <PublisherDisplayName>abigailc</PublisherDisplayName>
  <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
</Properties>
```

#### <span data-ttu-id="2caa7-134">Valores de plantilla de manifiesto de JSON</span><span class="sxs-lookup"><span data-stu-id="2caa7-134">JSON manifest template values</span></span>
<span data-ttu-id="2caa7-135">Algunos valores de AppXManifest necesitan coincidir con los que se definen en el manifiesto JSON.</span><span class="sxs-lookup"><span data-stu-id="2caa7-135">Some values in the AppXManifest need to match those that are defined in the JSON manifest.</span></span> <span data-ttu-id="2caa7-136">Actualiza los siguientes valores en appxmanifest. XML en función del manifiesto JSON de la extensión:</span><span class="sxs-lookup"><span data-stu-id="2caa7-136">Please update the following values in appxmanifest.xml based on your extension JSON manifest:</span></span>

- `Version` <span data-ttu-id="2caa7-137">-Esta es la versión que aparece en el manifiesto JSON de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2caa7-137">- This is the version listed in your extension's JSON manifest.</span></span> <span data-ttu-id="2caa7-138">La cadena debe coincidir con el formato X. x. x, donde el último entero tiene que ser 0.</span><span class="sxs-lookup"><span data-stu-id="2caa7-138">The string needs to match the X.X.X.X format where the last integer has to be 0.</span></span> <span data-ttu-id="2caa7-139">P. ej.</span><span class="sxs-lookup"><span data-stu-id="2caa7-139">E.g.</span></span> <span data-ttu-id="2caa7-140">1.2.3.0</span><span class="sxs-lookup"><span data-stu-id="2caa7-140">1.2.3.0</span></span>

   ```xml
   <Identity
     Name="37369abigailc.MyExtension"
     Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
     Version="1.0.0.0" />
   ```

- `Description` <span data-ttu-id="2caa7-141">-Esta es una copia de la descripción en el manifiesto JSON de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2caa7-141">- This is a copy of the description in your extension's JSON manifest.</span></span>

  ```xml
  <uap:VisualElements
    AppListEntry="none"
    DisplayName="My Extension"
    Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
    Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
    Description="This extension will allow you to quickly print by clicking the browser action."
    BackgroundColor="white">
  </uap:VisualElements>
  ```


### <span data-ttu-id="2caa7-142">Carpeta activos</span><span class="sxs-lookup"><span data-stu-id="2caa7-142">Assets folder</span></span>

<span data-ttu-id="2caa7-143">Dentro de la carpeta activos necesitarás tres tamaños de icono diferentes.</span><span class="sxs-lookup"><span data-stu-id="2caa7-143">Within the Assets folder you will need three different icon sizes.</span></span> <span data-ttu-id="2caa7-144">Estos iconos se usarán en Microsoft Store y en la interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="2caa7-144">These icons will be used in the Microsoft Store and the Windows UI.</span></span> <span data-ttu-id="2caa7-145">Para obtener más información sobre estos iconos, consulte la guía de [diseño](./../design.md#icons-for-packaging) .</span><span class="sxs-lookup"><span data-stu-id="2caa7-145">For more information on these icons, see the [Design](./../design.md#icons-for-packaging) guide.</span></span>

![carpeta activos con tres tamaños de icono](./../../media/assets-folder.png)

<span data-ttu-id="2caa7-147">Una vez que hayas creado los activos de interfaz de usuario necesarios, actualiza AppXManifest. XML para apuntar a los archivos correctos:</span><span class="sxs-lookup"><span data-stu-id="2caa7-147">Once you've created the necessary UI assets, update AppXManifest.xml to point to the correct files:</span></span>

- <span data-ttu-id="2caa7-148">44x44</span><span class="sxs-lookup"><span data-stu-id="2caa7-148">44x44</span></span>

   ```xml
   Square44x44Logo="Assets/icon_44.png"
   ```

- <span data-ttu-id="2caa7-149">50x50</span><span class="sxs-lookup"><span data-stu-id="2caa7-149">50x50</span></span>

  ```xml
   <Logo>Assets/icon_50.png</Logo>
  ```

- <span data-ttu-id="2caa7-150">150x150</span><span class="sxs-lookup"><span data-stu-id="2caa7-150">150x150</span></span>

  ```xml
  Square150x150Logo="Assets/icon_150.png"
  ```


### <span data-ttu-id="2caa7-151">Carpeta de extensión</span><span class="sxs-lookup"><span data-stu-id="2caa7-151">Extension folder</span></span>
<span data-ttu-id="2caa7-152">Copie los archivos de extensión (manteniendo la estructura de carpetas) en la carpeta de extensiones.</span><span class="sxs-lookup"><span data-stu-id="2caa7-152">Copy your extension files (keeping the folder structure) into the Extension folder.</span></span> <span data-ttu-id="2caa7-153">Asegúrese de que `manifest.json` está en la raíz de la carpeta de extensión.</span><span class="sxs-lookup"><span data-stu-id="2caa7-153">Make sure `manifest.json` is at the root your Extension folder.</span></span>

![carpeta de extensión con todos los archivos de extensión](./../../media/extension-folder.png)


### <span data-ttu-id="2caa7-155">Compatibilidad con más de una configuración regional</span><span class="sxs-lookup"><span data-stu-id="2caa7-155">Supporting more than one locale</span></span>
<span data-ttu-id="2caa7-156">Si tu extensión es compatible con más de un idioma, es posible que desees configurar el paquete AppX con todas las configuraciones regionales que necesites para que aparezca el icono y la descripción correctos en la tienda de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2caa7-156">If your extension supports more than one language, you may want to configure the AppX package with all the locales that you need so that the correct localized icon and description appear in the Microsoft Store.</span></span> <span data-ttu-id="2caa7-157">Para obtener más información, consulta [localización de paquetes de extensión](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="2caa7-157">See [Localizing extension packages](./localizing-extension-packages.md) for more information.</span></span>

### <span data-ttu-id="2caa7-158">Crear un appx</span><span class="sxs-lookup"><span data-stu-id="2caa7-158">Creating an Appx</span></span>

<span data-ttu-id="2caa7-159">Para crear un appx, tendrás que buscar la ruta de acceso a makeappx.</span><span class="sxs-lookup"><span data-stu-id="2caa7-159">To create an Appx, you'll need to find the path for makeappx.</span></span> <span data-ttu-id="2caa7-160">Esto suele encontrarse en la siguiente ubicación si se encuentra en un equipo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2caa7-160">This is usually located in the following location if you're on a 64-bit machine.</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

<span data-ttu-id="2caa7-161">Ejecuta el siguiente comando para crear el paquete AppX para tu extensión:</span><span class="sxs-lookup"><span data-stu-id="2caa7-161">Execute the following command to create the AppX package for your extension:</span></span>

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

<span data-ttu-id="2caa7-162">Debe tener un aspecto similar a este, una vez que haya rellenado las rutas:</span><span class="sxs-lookup"><span data-stu-id="2caa7-162">This should look something like this once you've filled in the paths:</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### <span data-ttu-id="2caa7-163">Desempaquetar un appx</span><span class="sxs-lookup"><span data-stu-id="2caa7-163">Unpacking an Appx</span></span>
<span data-ttu-id="2caa7-164">Es posible que quieras desempaquetar un AppX generado previamente y usarlo como punto de partida para la siguiente iteración de la extensión o para confirmar que el AppX se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2caa7-164">You may want to unpack a previously generated AppX and use it as a starting point for the next iteration of your extension or to confirm that the AppX was created correctly.</span></span>

<span data-ttu-id="2caa7-165">Para ello, puedes ejecutar el siguiente comando para desempaquetar el paquete AppX de la extensión de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="2caa7-165">To do this, you can execute the following command to unpack the AppX package of your Microsoft Edge extension:</span></span>

`[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]`

<span data-ttu-id="2caa7-166">Debe tener un aspecto similar a este:</span><span class="sxs-lookup"><span data-stu-id="2caa7-166">This should look something like this when filled out:</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"`





## <span data-ttu-id="2caa7-167">Probar un paquete AppX</span><span class="sxs-lookup"><span data-stu-id="2caa7-167">Testing an AppX package</span></span>

<span data-ttu-id="2caa7-168">Puedes probar el paquete AppX de la extensión de Microsoft Edge si lo instalas en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2caa7-168">You can test your Microsoft Edge extension AppX package by sideloading it in Microsoft Edge.</span></span> <span data-ttu-id="2caa7-169">La transferencia local el paquete AppX de extensión es similar a transferir una aplicación universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="2caa7-169">Sideloading the extension AppX package is similar to sideloading a Universal Windows app.</span></span> <span data-ttu-id="2caa7-170">Tendrá que crear un certificado para firmar el paquete y, a continuación, agregar el paquete a Windows.</span><span class="sxs-lookup"><span data-stu-id="2caa7-170">You will need to create a certificate for signing the package, and then add the package to Windows.</span></span>

### <span data-ttu-id="2caa7-171">Digital</span><span class="sxs-lookup"><span data-stu-id="2caa7-171">Signing</span></span>

<span data-ttu-id="2caa7-172">Consulta [Cómo crear un certificado de firma de paquete de aplicación](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) y [cómo firmar un paquete de la aplicación con SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) para obtener información sobre el proceso de firma y certificación de los paquetes.</span><span class="sxs-lookup"><span data-stu-id="2caa7-172">See [How to create an app package signing certificate](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) and [How to sign an app package using SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) for info on the signing and certification process for packages.</span></span>

> [!NOTE]
> <span data-ttu-id="2caa7-173">No es necesario firmar un paquete de extensión antes de enviarlo a Microsoft Store; el proceso de recopilación de la tienda se encargará de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="2caa7-173">You do not need to sign an extension package before submitting it to the Microsoft Store; the Store ingestion process will take care of that for you!</span></span>

<span data-ttu-id="2caa7-174">Después de firmar el paquete con el certificado que ha creado, el certificado seguirá sin confiar en el equipo local para la implementación de paquetes de la aplicación hasta que lo instale en el almacén de certificados de confianza del equipo local.</span><span class="sxs-lookup"><span data-stu-id="2caa7-174">After you've signed the package with the certificate that you created, the certificate is still not trusted by the local machine for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="2caa7-175">Para ello, puede usar certutil. exe, que se incluye con Windows.</span><span class="sxs-lookup"><span data-stu-id="2caa7-175">You can use Certutil.exe, which comes with Windows to do this.</span></span>

<span data-ttu-id="2caa7-176">Para instalar certificados con WindowsCertutil. exe, ejecute cmd. exe como administrador y ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="2caa7-176">To install certificates with WindowsCertutil.exe, run Cmd.exe as administrator and run the following command:</span></span>

`Certutil -addStore TrustedPeople MyKey.cer`

<span data-ttu-id="2caa7-177">Una vez que los certificados ya no se usan, se recomienda quitarlos ejecutando el siguiente comando desde un símbolo del sistema de administrador:</span><span class="sxs-lookup"><span data-stu-id="2caa7-177">Once the certificates are no longer in use, it is recommended that you remove them by running the following command from an administrator command prompt:</span></span>

`Certutil -delStore TrustedPeople certID`

<span data-ttu-id="2caa7-178">CertID es el número de serie del certificado.</span><span class="sxs-lookup"><span data-stu-id="2caa7-178">The certID is the serial number of the certificate.</span></span> <span data-ttu-id="2caa7-179">Para determinar el número de serie del certificado, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="2caa7-179">To determine the certificate serial number, run the following command:</span></span>

`Certutil -store TrustedPeople`

### <span data-ttu-id="2caa7-180">Implementar</span><span class="sxs-lookup"><span data-stu-id="2caa7-180">Deploying</span></span>
<span data-ttu-id="2caa7-181">Para implementar el paquete AppX de la extensión de Microsoft Edge, ejecute el siguiente comando en PowerShell (como administrador):</span><span class="sxs-lookup"><span data-stu-id="2caa7-181">You can deploy the Microsoft Edge Extension AppX package by running the following command in PowerShell (as administrator):</span></span>

`Add-AppxPackage [path to AppX]`

## <span data-ttu-id="2caa7-182">Pruebas automatizadas con Webdriver</span><span class="sxs-lookup"><span data-stu-id="2caa7-182">Automated testing with WebDriver</span></span>

<span data-ttu-id="2caa7-183">A partir de la actualización de aniversario, puedes transferir mediante programación la extensión en Microsoft Edge con Webdriver, lo que permite realizar pruebas automatizadas de extensiones cuando se inicia Microsoft Edge en el modo Webdriver.</span><span class="sxs-lookup"><span data-stu-id="2caa7-183">As of the Anniversary Update, you can programmatically sideload your extension in Microsoft Edge with WebDriver, enabling automated testing of extensions when Microsoft Edge is launched in WebDriver mode.</span></span> <span data-ttu-id="2caa7-184">Esto le permitirá configurar pruebas automatizadas para cualquier extensión que manipule el contenido de una página y comprobar que se exhibe el comportamiento correcto.</span><span class="sxs-lookup"><span data-stu-id="2caa7-184">This will allow you to set up automated tests for any extension that manipulates content on a page and verify that the correct behavior is exhibited.</span></span>

<span data-ttu-id="2caa7-185">Para realizar una prueba automatizada de su extensión, tendrá que almacenar la carpeta de su extensión en `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` .</span><span class="sxs-lookup"><span data-stu-id="2caa7-185">To sideload your extension for automated testing, you'll need to store your extension's folder under `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\`.</span></span> <span data-ttu-id="2caa7-186">Una vez que la extensión esté en el `LocalState` directorio, tendrá que crear un [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) objeto y agregarle la `extensionPaths` funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="2caa7-186">Once your extension is in the `LocalState` directory, you'll need to create an [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) object, and add the `extensionPaths` capability to it.</span></span> <span data-ttu-id="2caa7-187">El valor de esta funcionalidad es una matriz de rutas absolutas a las extensiones (en el `LocalState` directorio) que desea que se cargue cuando se inicia Microsoft Edge en el modo Webdriver.</span><span class="sxs-lookup"><span data-stu-id="2caa7-187">The value of this capability is an array of absolute paths to the extensions (in the `LocalState` directory) you wish to have side loaded when Microsoft Edge starts in WebDriver mode.</span></span>

<span data-ttu-id="2caa7-188">Consulte el siguiente [archivo de C#](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) para obtener un ejemplo completo de las extensiones de carga de cara en Microsoft Edge con Webdriver.</span><span class="sxs-lookup"><span data-stu-id="2caa7-188">Check out the following [C# file](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) for a complete sample on side loading extensions in Microsoft Edge with WebDriver.</span></span>

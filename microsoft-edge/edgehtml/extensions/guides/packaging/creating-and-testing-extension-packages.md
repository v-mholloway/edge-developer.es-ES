---
ms.assetid: 5eefa3d8-8626-4486-bd90-1361400d6468
description: Más información sobre cómo empaquetar la extensión de Microsoft Edge manualmente y probarla para ver si está empaquetada correctamente.
title: Crear y probar paquetes de extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, empaquetado
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 44316f4dd47b3b6b26014ff24673ddfd16a72ddb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236488"
---
# Crear y probar un paquete AppX de extensión de Microsoft Edge  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Las extensiones de Microsoft Edge se empaquetan como AppX, de forma similar a como se empaquetan las aplicaciones universales de Windows. A partir de la actualización de aniversario de Windows 10, se ha introducido un nuevo esquema para AppX que permite a un AppX incluir una extensión de Microsoft Edge como contenido.

Si ya sabes cómo se crean las extensiones de Microsoft Edge AppXs, puedes omitir el uso de la [extensión de ManifoldJS a empaquetar](./using-manifoldjs-to-package-extensions.md) para obtener más información sobre cómo usar una herramienta basada en Node.js.

> [!NOTE]
> El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida. Una vez que hayas creado, embalado y probado tu extensión, envía una solicitud en nuestro [formulario de envío de extensiones](https://aka.ms/extension-request).

## Preparar la carpeta de presentación

Para preparar la extensión para el envío, debe crear una carpeta con la estructura siguiente:

![imagen de la estructura de carpetas. En mi carpeta de extensiones se encuentra AppxManifest.xml, carpeta de extensión y carpeta de activos](./../../media/packaging_folder-structure.png)

En la raíz de la carpeta, debe incluir un archivo de AppXManifest.xml. Este archivo se usa para especificar el contenido y el diseño del paquete.

También debe tener una carpeta de activos que contenga los activos de la interfaz de usuario que se usarán en Microsoft Store y una carpeta de extensiones que contiene los archivos de extensión (scripts, iconos, etc.).

> [!IMPORTANT]
> Puede crear una estructura de carpetas diferente para el paquete, pero la estructura de carpetas debe coincidir con los valores de AppXManifest.

### AppXManifest.xml
El archivo AppXManifest es un documento XML que contiene información que el sistema necesita para implementar, mostrar o actualizar una aplicación de Windows. Este archivo también incluye identidad de paquete, capacidades y elementos visuales. Cada paquete de la aplicación debe incluir un archivo AppXManifest.

Los programadores pueden usar la siguiente plantilla para su AppXManifest.xml archivo:

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

#### Valores de la plantilla de identidad de aplicación
Una vez que hayas [reservado el nombre de tu extensión](./extensions-in-the-windows-dev-center.md#name-reservation) a través del centro de desarrollo de Windows, podrás encontrar la información de identidad del paquete necesaria para reemplazar los siguientes valores de AppXManifest.xml:

-   `Name`
-   `Publisher`
-   `DisplayName`
-   `PublisherDisplayName`

Puede acceder a la página identidad de la aplicación siguiendo estos pasos:

1.  Vaya al [centro de desarrollo de Windows](https://developer.microsoft.com/windows/).
2.  Inicie sesión en su cuenta de desarrollador.
3.  Vaya al panel.
4.  Seleccione el nombre de la extensión.
    
    ![lista de extensiones](./../../media/select-app.png)
    
5.  Vaya a la página identidad de la aplicación, que se encuentra en la sección Administración de aplicaciones (después de haber registrado la aplicación).
    
    ![Página identidad de la aplicación](./../../media/app-identity.png)
    
Ahora puede rellenar la plantilla AppXManifest con los valores de la página identidad de la aplicación, como se indica en la plantilla:

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

#### Valores de plantilla de manifiesto de JSON
Algunos valores de AppXManifest necesitan coincidir con los que se definen en el manifiesto JSON. Actualiza los siguientes valores en appxmanifest.xml según el manifiesto JSON de la extensión:

-   `Version` -Esta es la versión que aparece en el manifiesto JSON de la extensión. La cadena debe coincidir con el formato X. x. x, donde el último entero tiene que ser 0. P. ej. 1.2.3.0
    
    ```xml
    <Identity
         Name="37369abigailc.MyExtension"
         Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
         Version="1.0.0.0" />
    ```  
    
-   `Description` -Esta es una copia de la descripción en el manifiesto JSON de la extensión.
    
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
    
### Carpeta activos

Dentro de la carpeta activos necesitarás tres tamaños de icono diferentes. Estos iconos se usarán en Microsoft Store y en la interfaz de usuario de Windows. Para obtener más información sobre estos iconos, consulte la guía de [diseño](./../design.md#icons-for-packaging) .

![carpeta activos con tres tamaños de icono](./../../media/assets-folder.png)

Una vez que haya creado los recursos de la interfaz de usuario necesarios, actualice AppXManifest.xml para que apunten a los archivos correctos:

-   44x44
    
    ```xml
    Square44x44Logo="Assets/icon_44.png"
    ```  
    
-   50x50
    
    ```xml
    <Logo>Assets/icon_50.png</Logo>
    ```  
    
-   150x150
    
    ```xml
    Square150x150Logo="Assets/icon_150.png"
    ```  
    
### Carpeta de extensión
Copie los archivos de extensión (manteniendo la estructura de carpetas) en la carpeta de extensiones. Asegúrese de que `manifest.json` está en la raíz de la carpeta de extensión.

![carpeta de extensión con todos los archivos de extensión](./../../media/extension-folder.png)

### Compatibilidad con más de una configuración regional
Si tu extensión es compatible con más de un idioma, es posible que desees configurar el paquete AppX con todas las configuraciones regionales que necesites para que aparezca el icono y la descripción correctos en la tienda de Microsoft. Para obtener más información, consulta [localización de paquetes de extensión](./localizing-extension-packages.md) .

### Crear un appx

Para crear un appx, tendrás que buscar la ruta de acceso a makeappx. Esto suele encontrarse en la siguiente ubicación si se encuentra en un equipo de 64 bits.

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

Ejecuta el siguiente comando para crear el paquete AppX para tu extensión:

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

Debe tener un aspecto similar a este, una vez que haya rellenado las rutas:

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### Desempaquetar un appx
Es posible que quieras desempaquetar un AppX generado previamente y usarlo como punto de partida para la siguiente iteración de la extensión o para confirmar que el AppX se ha creado correctamente.

Para ello, puedes ejecutar el siguiente comando para desempaquetar el paquete AppX de la extensión de Microsoft Edge:

```shell
[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]
```  

Debe tener un aspecto similar a este:

```text
C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"
```  

## Probar un paquete AppX

Puedes probar el paquete AppX de la extensión de Microsoft Edge si lo instalas en Microsoft Edge. La transferencia local el paquete AppX de extensión es similar a transferir una aplicación universal de Windows. Tendrá que crear un certificado para firmar el paquete y, a continuación, agregar el paquete a Windows.

### Digital

Consulta [Cómo crear un certificado de firma de paquete de aplicación](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) y [cómo firmar un paquete de la aplicación con SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) para obtener información sobre el proceso de firma y certificación de los paquetes.

> [!NOTE]
> No es necesario firmar un paquete de extensión antes de enviarlo a Microsoft Store; el proceso de recopilación de la tienda se encargará de hacerlo.

Después de firmar el paquete con el certificado que ha creado, el certificado seguirá sin confiar en el equipo local para la implementación de paquetes de la aplicación hasta que lo instale en el almacén de certificados de confianza del equipo local. Para ello, puedes usar Certutil.exe, que se incluye con Windows.

Para instalar certificados con WindowsCertutil.exe, ejecute Cmd.exe como administrador y ejecute el siguiente comando:

```shell
Certutil -addStore TrustedPeople MyKey.cer
```  

Una vez que los certificados ya no se usan, se recomienda quitarlos ejecutando el siguiente comando desde un símbolo del sistema de administrador:

```shell
Certutil -delStore TrustedPeople certID
```  

CertID es el número de serie del certificado. Para determinar el número de serie del certificado, ejecute el siguiente comando:

```shell
Certutil -store TrustedPeople
```  

### Implementar
Para implementar el paquete AppX de la extensión de Microsoft Edge, ejecute el siguiente comando en PowerShell (como administrador):

```powershell
Add-AppxPackage [path to AppX]
```  

## Pruebas automatizadas con Webdriver

A partir de la actualización de aniversario, puedes transferir mediante programación la extensión en Microsoft Edge con Webdriver, lo que permite realizar pruebas automatizadas de extensiones cuando se inicia Microsoft Edge en el modo Webdriver. Esto le permitirá configurar pruebas automatizadas para cualquier extensión que manipule el contenido de una página y comprobar que se exhibe el comportamiento correcto.

Para realizar una prueba automatizada de su extensión, tendrá que almacenar la carpeta de su extensión en `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` . Una vez que la extensión esté en el `LocalState` directorio, tendrá que crear un [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) objeto y agregarle la `extensionPaths` funcionalidad. El valor de esta funcionalidad es una matriz de rutas absolutas a las extensiones (en el `LocalState` directorio) que desea que se cargue cuando se inicia Microsoft Edge en el modo Webdriver.

Consulte el siguiente [archivo de C#](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) para obtener un ejemplo completo de las extensiones de carga de cara en Microsoft Edge con Webdriver.

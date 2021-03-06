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
# <a name="localizing-microsoft-edge-extensions-for-windows-and-the-microsoft-store"></a>Localización de extensiones de Microsoft Edge para Windows y Microsoft Store  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

En esta guía se explica cómo encontrar la extensión de Microsoft Edge para que esté lista para varias configuraciones regionales tras la versión.  Para encontrar completamente la extensión, tendrás que seguir los pasos para Windows y la Microsoft Store.  

Si desea encontrar los recursos de extensión para Microsoft Edge, puede obtener información sobre cómo usar el marco de i18n en la [guía de internacionalización](../internationalization.md).  

> [!NOTE]
> Si la extensión no admite varios idiomas, puedes pasar a [Localización](#localizing-name-and-description-in-the-microsoft-store)de nombre y descripción en Microsoft Store .  

## <a name="the-localization-process-overview"></a>Introducción al proceso de localización  

El primer paso para que la extensión esté disponible para una amplia audiencia es [configurar su AppxManifest](#configuring-the-appxmanifest) para varios idiomas.  En Microsoft Store, esto mostrará a los usuarios qué idiomas admite la extensión.  Algunos campos de AppxManifest también tendrán que cambiarse si quieres que el nombre de la extensión esté localizado en la interfaz de usuario de Windows y la [Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).  

Una vez configurado appxManifest, tendrás que crear recursos de cadena [JSON](#creating-json-string-resources) para los idiomas que indicaste como compatibles.  Esto requiere crear un archivo para cada idioma, donde cada archivo tiene todas las cadenas de interfaz de usuario `.resjson` de ese idioma dentro de él.  

Una vez creados los archivos para los idiomas compatibles, tendrá que crearse un archivo de recursos `.resjson` [.pri](#creating-the-resources-file). Esto se creará mediante el uso de un archivo de configuración para la herramienta MakePRI que viene con [el SDK de Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).  

> [!NOTE]
> Si solo estás descargando el SDK de Windows 10 para usar la herramienta, solo puedes seleccionar las características herramientas de firma de Windows SDK para aplicaciones de escritorio y Windows SDK para aplicaciones administradas para UWP para mantener la descarga más `MakePri.exe` ligera. **** ****  La `MakePri.exe` herramienta aparecerá en subcarpetas de `C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0` .  

Una vez que hayas cargado la extensión, el paso final es encontrar el nombre y la [descripción en Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).  

> [!NOTE]
> Enviar una extensión de Microsoft Edge a la Microsoft Store es actualmente una funcionalidad restringida.  **Llámenos con** sus solicitudes para formar parte de Microsoft Store y le consideraremos para una actualización futura.  

## <a name="configuring-the-appxmanifest"></a>Configuración de AppXManifest  

La lista de idiomas admitidos de la extensión en Microsoft Store se genera en función de sus valores de AppXManifest.  Esta lista se especifica mediante el `Resource` elemento.  

![Detalles de la aplicación](../../media/language-app-details.png)  

Para especificar la lista de idiomas compatibles con la extensión, puede agregar un elemento en el formato que se muestra a continuación \(Este elemento mostrará compatibilidad con inglés, alemán y francés en `Resource` `Resource` Microsoft Store\):  

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```  

Consulta [Idiomas admitidos](/windows/uwp/publish/supported-languages) para obtener información sobre los idiomas/códigos de idioma compatibles con Microsoft Store.  

Para especificar cadenas localizadas para todos los elementos visibles públicamente en AppxManifest, tendrá que usar un identificador de recursos con el formato `ms-resource:<resource id>` de .  

Los fragmentos de código siguientes hacen un AppxManifest completo. Los siguientes valores deben recuperarse de los archivos de recursos localizados:  

*   Properties\DisplayName  
*   Propiedades\Descripción  
*   Properties\PublisherDisplayName  

```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```  

*   Aplicaciones\Application\VisualElements\DisplayName  
*   Aplicaciones\Application\VisualElements\Description  
*   Aplicaciones\Application\Extensions\Extension\AppExtension\DisplayName  

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

## <a name="localizing-extension-resources-for-windows-and-the-microsoft-store"></a>Localización de recursos de extensión para Windows y Microsoft Store  

Ahora que AppxManifest está configurado para varios idiomas, hay algunas diferencias clave que debes saber entre la localización de la interfaz de usuario dentro de la extensión y la localización de la extensión para Windows y microsoft Store.  

Aunque las extensiones de Microsoft Edge no se ejecutan fuera de Microsoft Edge, la administración de ellas puede producirse en Windows.  Por ejemplo, los usuarios pueden administrar sus extensiones en la aplicación Configuración:  

![aplicación de configuración](../../media/settings.png)  

El nombre de la extensión que aparece en la aplicación Configuración de Windows proviene del AppXManifest.  Si este valor está codificado en inglés, la versión en inglés del nombre aparecerá en dispositivos Windows que no son de inglés.  Si la personal de marca de la extensión es solo en inglés, está bien dejarla codificada de forma rígida.  

> [!NOTE]
> Si quieres usar nombres localizados para la extensión de Microsoft Edge [](./extensions-in-the-windows-dev-center.md#name-reservation) en Windows, asegúrate de que los nombres localizados también estén disponibles y reservados antes de realizar los cambios en el archivo AppXManifest.  Si los nombres no están reservados, se producirá el siguiente error al cargar el paquete final en el Centro de desarrollo de Windows:  
> 
> ![error de idioma](../../media/language-error.png)  

La infraestructura de localización basada en i18n que se define para las extensiones de JavaScript solo se aplica en el entorno de Microsoft Edge.  

Fuera de Microsoft Edge, dentro de Windows y microsoft Store, el único marco de localización compatible se basa en el marco de localización de la Plataforma universal de Windows (UWP).  

Aunque se admiten recursos basados en JSON para aplicaciones de Windows basadas en HTML, el esquema de los recursos JSON no coincide con el definido para las extensiones de JavaScript.  

Las siguientes son las principales diferencias en las [aplicaciones de Windows basadas en HTML:](/previous-versions/windows/apps/hh465228(v=win.10))  

*   Los recursos se especifican en `.resjson` archivos en lugar de `.json` archivos.  
*   Las configuraciones regionales admitidas deben especificarse en el archivo AppXManifest, siendo la primera configuración regional la configuración regional predeterminada.  
*   Los recursos de aplicaciones de Windows basados en HTML usan el esquema siguiente:  
    
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```  
    
    El par nombre/valor que indica un carácter de subrayado son comentarios para el recurso de cadena correspondiente.  
*   `.resjson` los archivos se compilan en `.pri` archivos que deben incluirse durante la creación del paquete AppX.  
    
### <a name="creating-json-string-resources"></a>Creación de recursos de cadena JSON  

Con un AppxManifest configurado en la mano y las diferencias entre los marcos de localización de i18n y UWP resaltados, estás listo para crear los archivos de recursos.  

Solo se aplica una cadena de recurso en el manifiesto a los paquetes de extensión de Microsoft Edge.  La cadena se localiza comúnmente en extensiones de JavaScript y se puede asignar fácilmente a `DisplayName` los archivos que Windows `.resjson` espera.  Suponiendo que este es el único recurso que le gustaría encontrar, este es un archivo de ejemplo `.resjson` que debe crearse:  

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```  

El identificador de recurso de cada `.resjson` archivo debe coincidir con el identificador usado en AppXManifest.  Con el fragmento `.resjson` de código anterior, la entrada AppXManifest correspondiente debe ser:  

`DisplayName="ms-resource:DisplayName"`  

Cada idioma compatible con la extensión debe tener un archivo de recursos correspondiente `.resjson` y colocarse en la siguiente estructura de carpetas:  

![estructura de carpetas de idioma](../../media/resources-folder.png)  

### <a name="creating-the-resources-file"></a>Creación del archivo de recursos  

Una vez que haya creado todos los archivos, estará listo para crear el archivo de índice de recursos del `.resjson` paquete \(PRI\).  Este archivo almacena los recursos para todos los idiomas admitidos.  Para ello, puedes usar la **herramienta MakePRI** que se incluye con el SDK de Windows 10.  

Primero tendrá que crear el archivo de configuración.  Esto define los calificadores y la plataforma predeterminados para los recursos.  Para este ejemplo, haz que el idioma predeterminado `English (US)` y la plataforma Windows 10.  Para ello, cree un `priconfig.xml` archivo con el siguiente contenido en `[Root folder]` :  

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

Ahora puede usar el archivo de configuración y la herramienta MakePRI para crear el archivo resources.pri.  En este ejemplo, la ubicación raíz del proyecto será `[Root folder]` .  

```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```  

Ahora debería tener un archivo resources.pri en la carpeta raíz:  

![carpeta resources](../../media/resources.png)  

## <a name="localizing-name-and-description-in-the-microsoft-store"></a>Localización de nombre y descripción en Microsoft Store  

Una vez que intentes cargar el paquete completo y localizado, el Centro de desarrollo de Windows detectará que se admite más de un idioma y comprobará que tienes nombres y descripciones localizados correspondientes para cada uno.  Si falta alguno de los valores localizados, el envío se bloqueará hasta que proporcione los valores.  

Si solo estás interesado en proporcionar un nombre localizado y una descripción para la Microsoft Store (y no Windows), puedes hacerlo reservando todos los nombres localizados para [la extensión](./extensions-in-the-windows-dev-center.md#name-reservation).  

Una vez reservados los nombres localizados adicionales, puede crear un envío actualizado.  En la sección descripción, puedes administrar idiomas adicionales para tu descripción de Microsoft Store:  

![Administrar idiomas de descripción](../../media/manage-description-languages.png)  

Una vez que hayas seleccionado **Administrar idiomas**adicionales, podrás seleccionar los idiomas que quieres agregar a la descripción de Microsoft Store.  El nuevo idioma se mostrará como **Idioma de descripción adicional en** la **sección** Descripción.  

Puede hacer clic en el **** vínculo individual de la sección Descripción para proporcionar un nombre y una descripción localizados, notas de la versión y activos visuales para cada idioma.  La descripción de Microsoft Store no se extrae de AppXManifest.  Cada descripción localizada debe especificarse manualmente en el Centro de desarrollo de Windows:  

![Descripción de la aplicación japonesa](../../media/japanese-app-description.png)  

Una vez que se envían las descripciones localizadas y se publica la extensión, cualquier persona que acceda a una página localizada de la extensión en Microsoft Store verá la siguiente interfaz de usuario:  

![Tienda de windows japonesa](../../media/japanese-windows-store.png)  

## <a name="appxmanifest-samples"></a>Ejemplos de AppxManifest  

### <a name="non-localized-appxmanifest"></a>AppxManifest no localizado  

En el ejemplo siguiente se muestra un AppxManifest que no está localizado y solo admite la `en-us` configuración regional.  

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

#### <a name="localized-appxmanifest"></a>Localized AppxManifest  

Esta muestra de AppxManifest se localiza para otras ocho configuraciones regionales además de "en-us". Observe las `ms-resource:<resource id>` repeticiones:  

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

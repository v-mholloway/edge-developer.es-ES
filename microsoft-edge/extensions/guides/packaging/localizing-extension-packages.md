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
# Localizar las extensiones de Microsoft Edge para Windows y Microsoft Store  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

En esta guía se explica cómo localizar su extensión de Microsoft Edge de modo que esté lista para varias configuraciones regionales en el momento de la publicación. Para localizar completamente su extensión, tendrá que seguir los pasos para Windows y Microsoft Store.

Si desea localizar sus recursos de extensión para Microsoft Edge, puede obtener información sobre cómo usar el marco de i18n en la [Guía de internacionalización](../internationalization.md).


> [!NOTE]
> Si tu extensión no es compatible con varios idiomas, puedes omitir [la localización de nombres y descripciones en Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).


## Información general del proceso de localización

El primer paso para conseguir que tu extensión esté disponible para una gran audiencia es [configurar su AppxManifest](#configuring-the-appxmanifest) para varios idiomas. En Microsoft Store, se mostrará a los usuarios qué idiomas son compatibles con la extensión. Algunos campos en el AppxManifest también deben cambiarse si quieres que el nombre de tu extensión esté [localizado en la interfaz de usuario de Windows y en Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).


Una vez que hayas configurado tu AppxManifest, tendrás que [crear recursos de cadena de JSON](#creating-json-string-resources) para los idiomas que indicaste como admitidos. Esto requiere la creación de un archivo. resjson para cada idioma, en el que cada archivo tiene todas las cadenas de interfaz de usuario de ese idioma.


Una vez que se hayan realizado los archivos. resjson para los idiomas admitidos, [será necesario crear un archivo de recursos. PRI](#creating-the-resources-file). Esto se creará usando un archivo de configuración para la herramienta **MakePRI** que viene con el [SDK de Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk). 

> [!NOTE]
> Si solo descarga el SDK de Windows 10 para usar la herramienta MakePri. exe, puede seleccionar solo las características "herramientas de firma del SDK de Windows para aplicaciones de escritorio" y "SDK de Windows para aplicaciones administradas por UWP" para mantener la descarga más clara. La herramienta MakePri. exe aparecerá en subcarpetas de C:\Archivos de programa (x86) \Windows Kits\10\bin\10.0.17713.0.


Una vez que haya cargado su extensión, el paso final es [localizar el nombre y la descripción en Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).

> [!NOTE]
> El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida. Póngase en [contacto con nosotros](https://aka.ms/extension-request) con sus solicitudes para formar parte de Microsoft Store y le daremos una actualización futura.



## Configuración de AppXManifest

La lista "idiomas admitidos" de la extensión de Microsoft Store se genera en función de sus valores de AppXManifest. Esta lista se especifica con el `Resource` elemento.


![imagen de configuración](./../../media/language-app-details.png)

Para especificar la lista de idiomas admitidos por su extensión, puede Agregar un `Resource` elemento en el formato que se muestra a continuación (este `Resource` elemento mostrará compatibilidad para inglés, alemán y francés en Microsoft Store):

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

Consulte [idiomas admitidos](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) para obtener información sobre los idiomas y códigos de idioma que admite Microsoft Store.


Para poder especificar cadenas localizadas para todos los elementos públicamente visibles en el AppxManifest, tendrás que usar un identificador de recursos en el formato de `ms-resource:<resource id>` .

Los siguientes fragmentos de código hacen que AppxManifest completo. Los siguientes valores deben recuperarse de archivos de recursos localizados:

- Properties\DisplayName
- Properties\Description
- Properties\PublisherDisplayName


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- Applications\Application\VisualElements\DisplayName
- Applications\Application\VisualElements\Description
- Applications\Application\Extensions\Extension\AppExtension\DisplayName

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


## Localización de recursos de extensión para Windows y Microsoft Store

Ahora que tu AppxManifest está configurado para varios idiomas, hay algunas diferencias clave que debes saber para poder localizar la interfaz de usuario dentro de la extensión y localizar la extensión de Windows y de Microsoft Store.

Mientras que las extensiones de Microsoft Edge no se ejecutan fuera de Microsoft Edge, la administración de estas puede ocurrir en Windows. Por ejemplo, los usuarios pueden administrar sus extensiones en la aplicación configuración:


![imagen de configuración](./../../media/settings.png)



El nombre de la extensión que aparece en la aplicación configuración de Windows procede del AppXManifest. Si este valor está codificado en inglés, la versión en inglés del nombre se mostrará en dispositivos que no están en inglés. Si la marca de su extensión es solo en inglés, puede dejarla codificada.


> [!NOTE]
> Si desea usar nombres localizados para su extensión de Microsoft Edge en Windows, asegúrese de que los nombres localizados también estén [disponibles y reservados](./extensions-in-the-windows-dev-center.md#name-reservation) antes de realizar los cambios en el archivo AppXManifest. Si los nombres no están reservados, recibirá el siguiente error al cargar el paquete final en el centro de desarrollo de Windows:</br></br>

![error de idioma](./../../media/language-error.png)</br></br>


La infraestructura de localización basada en i18n que se define para las extensiones de JavaScript solo es aplicable dentro del entorno de Microsoft Edge.

Fuera de Microsoft Edge, dentro de Windows y Microsoft Store, el único marco de trabajo de localización admitido se basa en el marco de localización de la plataforma universal de Windows (UWP).

Aunque se admiten recursos basados en JSON para aplicaciones de Windows basadas en HTML, el esquema de los recursos de JSON no coincide con el definido para las extensiones de JavaScript.


A continuación se muestran las diferencias clave en las [aplicaciones de Windows basadas en HTML](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):
-    Los recursos se especifican en archivos. resjson en lugar de archivos. JSON.
-    Las configuraciones regionales deben especificarse en el archivo AppXManifest, siendo la primera configuración regional la predeterminada.
-    Los recursos de aplicaciones de Windows basadas en HTML usan el siguiente esquema:
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    El par de nombre y valor denotado por un carácter de subrayado es comentarios para el recurso de cadena correspondiente.
-    los archivos. resjson se compilan en archivos. PRI, que deben incluirse durante la creación del paquete AppX.


### Creación de recursos de cadena JSON
Con un AppxManifest configurado y las diferencias entre los marcos de trabajo de i18n y UWP resaltados, ya está listo para crear los archivos de recursos.

Solo se puede aplicar una cadena de recurso en el manifiesto a paquetes de extensión de Microsoft Edge. La `DisplayName` cadena suele estar localizada en extensiones de JavaScript y se puede asignar fácilmente a los archivos. resjson que Windows espera. Suponiendo que este es el único recurso que desea localizar, este es un archivo. resjson de ejemplo que debe crearse:

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

El identificador de recurso de cada archivo. resjson debe coincidir con el identificador usado en el AppXManifest. Con el fragmento de código de ejemplo. resjson anterior, la entrada AppXManifest correspondiente debe ser:

`DisplayName="ms-resource:DisplayName"`

Cada idioma que admita la extensión debería tener un archivo resources. resjson correspondiente y colocarse en la siguiente estructura de carpetas:

![estructura de carpetas de idioma](./../../media/resources-folder.png)


### Crear el archivo de recursos
Una vez que haya creado todos los archivos. resjson, estará listo para crear el archivo de índice de recursos (PRI) del paquete. Este archivo almacena los recursos de todos los idiomas admitidos. Para hacerlo, puede usar la herramienta **MakePRI** , que se incluye con el SDK de Windows 10.


En primer lugar, tendrá que crear el archivo de configuración. Define los calificadores y la plataforma predeterminados para los recursos. Para este ejemplo, convierta el idioma predeterminado inglés (Estados Unidos) y la plataforma Windows 10. Para ello, cree un archivo priconfig. XML con el siguiente contenido en la [carpeta raíz]:

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

Ahora puede usar el archivo de configuración y la herramienta MakePRI para crear el archivo resources. PRI. Para este ejemplo, la ubicación raíz para el proyecto será [carpeta raíz].


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

Ahora debe tener un archivo resources. PRI en la carpeta raíz:

![carpeta recursos](./../../media/resources.png)


## Localizar el nombre y la descripción en Microsoft Store

Una vez que intentes cargar el paquete localizado completo, el centro de desarrollo de Windows detectará que se admite más de un idioma y verifica que tienes nombres localizados y descripciones para cada uno. Si falta alguno de los valores localizados, el envío se bloqueará hasta que proporcione los valores.

Si solo le interesa proporcionar un nombre localizado y una descripción de Microsoft Store (y no de Windows), puede hacerlo si [reserva todos los nombres localizados para su extensión](./extensions-in-the-windows-dev-center.md#name-reservation).


Una vez que hayas reservado nombres localizados adicionales, puedes crear un envío actualizado. En la sección Descripción puede administrar idiomas adicionales para la descripción de Microsoft Store:

![Descripción de la aplicación en Japonés](./../../media/manage-description-languages.png)

Una vez que haya seleccionado "administrar idiomas adicionales", tendrá que seleccionar los idiomas que desea agregar a la descripción de Microsoft Store. El nuevo idioma se mostrará como "idioma de Descripción adicional" en la sección "Descripción".

Puede hacer clic en el vínculo individual de la sección "Descripción" para proporcionar un nombre localizado y una descripción, notas de la versión y recursos visuales para cada idioma. La descripción de Microsoft Store no se extrae del AppXManifest. Cada descripción localizada debe introducirse manualmente en el centro de desarrollo de Windows:

![Descripción de la aplicación en Japonés](./../../media/japanese-app-description.png)

Una vez que se envíen las descripciones localizadas y se publique la extensión, cualquier persona que tenga acceso a una página localizada de la extensión en Microsoft Store verá la siguiente interfaz de usuario:

![tienda Windows en Japonés](./../../media/japanese-windows-store.png)
 

## Ejemplos de AppxManifest

### AppxManifest no localizado
En el ejemplo siguiente se muestra un AppxManifest que no está localizado y solo admite la configuración regional "en-es".


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


#### AppxManifest localizado
Este ejemplo AppxManifest está localizado para ocho otras configuraciones regionales además de "en-es". Observe las `ms-resource:<resource id>` apariciones:


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

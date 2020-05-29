---
description: Póngase en contacto con el mundo de los clientes de Windows 10 distribuyendo su PWA a través de Microsoft Store.
title: Aplicaciones web progresivas en Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, Microsoft Store, índice PWA de Bing
ms.openlocfilehash: a4491f19b89e8b0f6fa511f146744499e2074f22
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574895"
---
# Aplicaciones web progresivas en Microsoft Store

Al publicar la aplicación web progresiva (PWA) en [Microsoft Store](https://developer.microsoft.com/store), la posible audiencia de la aplicación se expande a toda la base de instalación de Windows 10 de casi 700 millones usuarios mensuales activos. 

PWAs en Microsoft Store disfruta de varias ventajas:

- **Detectabilidad** : las aplicaciones de Microsoft Store se exhiben en diferentes categorías, colecciones de protegida y filtros de búsqueda, lo que proporciona una experiencia de navegación y de compra sencilla para clientes potenciales de la aplicación. Incluso puedes [mejorar tu descripción de la tienda](/windows/uwp/publish/app-screenshots-and-images) con capturas de pantalla, una imagen principal y los finalizadores de video.

- **Confiabilidad** : los clientes de Windows saben que pueden confiar en las compras y descargas de Microsoft Store porque cumplen con las rigurosas [normas de calidad y seguridad](/legal/windows/agreements/store-policies)de Microsoft.

- **Instalación sencilla** : Microsoft Store proporciona una experiencia de instalación coherente y fácil de usar en [todas las aplicaciones de Windows 10](https://www.microsoft.com/store/apps/windows?icid=CNavAppsWindowsApps), lo que permite a todos los clientes instalar fácilmente PWA, independientemente del nivel técnico.

- **Información empresarial** : el panel del [centro de desarrollo de Windows](/windows/uwp/publish/using-the-windows-dev-center-dashboard) para Microsoft Store le ofrece [análisis detallados](/windows/uwp/publish/analytics) sobre el número de clientes de Windows que su PWA ha alcanzado, así como su uso y qué es lo que tienen que decir. También puedes encontrar datos sobre métricas y telemetría en el estado de la aplicación, el uso de los anuncios y mucho más.

Existen dos opciones para obtener su PWA en Microsoft Store:

1. Puedes [enviarlo manualmente](#submitting-your-pwa-manually), o

2. Si su PWA cumple con [determinados criterios](#criteria-for-automatic-submission), el rastreador web de Bing puede [indizarlo automáticamente](#automatic-pwa-importing-with-bing) . (También tienes la opción de no [participar](#opting-out-of-automatic-microsoft-store-import) en la presentación automática).

Independientemente del método de envío, una vez que se acepte su PWA en Microsoft Store, tendrá acceso a todos los beneficios descritos anteriormente.

## Envío manual de PWA

Para poder distribuir y promocionar una aplicación a través de Microsoft Store, tendrás que enviarla como un paquete de la aplicación de Windows (archivo *. appx* ).  Para aplicaciones web hospedadas en el servidor, como PWAs, este paquete simplemente contiene metadatos de la aplicación y los iconos de la pantalla principal (y ninguno del código de la aplicación real). Con esto, tu aplicación web se puede instalar e iniciar desde la pantalla principal, junto con otras [aplicaciones de Windows 10](/windows/uwp/get-started/whats-a-uwp) , ejecutando un contenedor de aplicación nativa ligero (proceso*WWAHost. exe* ), independiente de la ventana del explorador Microsoft Edge.  

> [!IMPORTANT]
> El motor de plataforma web de EdgeHTML es utilizado por el contenedor de la aplicación WWAHost, que podría presentar diferencias de compatibilidad para el PWA basado en Microsoft Edge (cromo).  Asegúrese de realizar un paso de prueba completa en su aplicación con Microsoft Edge (EdgeHTML) antes de enviar la aplicación a Microsoft Store, ya que el motor de EdgeHTML ya no se actualiza con los estándares web más nuevos.  

Aquí le mostramos cómo hacerlo.

### Requisitos previos

- **Un PWA existente**. A continuación se explica cómo [convertir la aplicación web en un PWA](./get-started.md) si aún no lo es. 
- **Una herramienta de empaquetado de appx de Windows para PWAs**. A continuación se explica cómo [crear y ejecutar PWA en Windows](./windows-features.md) con Visual Studio. También puede usar el [generador PWA](https://www.pwabuilder.com/) para crear un paquete de Windows.
- [**Cuenta de desarrollador de la aplicación Microsoft Store**](/windows/uwp/publish/opening-a-developer-account). Hay una [tarifa única](/windows/uwp/publish/account-types-locations-and-fees) según el tipo de cuenta y la ubicación que hayas elegido, y el registro requiere una cuenta válida de [Microsoft](https://account.microsoft.com/).


### Almacenar el envío a través de *Visual Studio* 

Siga estos pasos para [crear un archivo de carga de paquete](/windows/uwp/packaging/packaging-uwp-apps#create-an-app-package-upload-file) de la aplicación para su PWA en Visual Studio. Para obtener más información general sobre este proceso, consulta [*empaquetar una aplicación para UWP con Visual Studio*](/windows/uwp/packaging/packaging-uwp-apps) .

Las instrucciones también le guiarán a través de la ejecución del [**Kit de certificación de aplicaciones de Windows**](https://developer.microsoft.com/windows/develop/app-certification-kit) para probar la aplicación para el cumplimiento de los requisitos de Microsoft Store. Esto es opcional, pero muy recomendable.

### Envío de la tienda a través del *centro de desarrollo de Windows*

A continuación se explica cómo usar el *creador de PWA* para generar un paquete de aplicación para cargarlo en el centro de desarrollo de Windows.

1. Genera tu aplicación de Windows 10. A continuación se explica cómo ejecutar su [PWA como una aplicación de Windows con Visual Studio](./windows-features.md). También puede usar el [creador de PWA](https://www.pwabuilder.com/) para generar la aplicación de Windows 10.

2. Para reservar el nombre de la aplicación de Microsoft Store, inicia sesión en el [panel del centro de desarrollo de Windows](https://developer.microsoft.com/dashboard/windows/overview) con la información de tu cuenta y sigue los pasos para [crear la aplicación al reservar un nombre](/windows/uwp/publish/create-your-app-by-reserving-a-name). Cada nombre reservado debe ser único en toda la Microsoft Store.

3. Al cargar los paquetes de la aplicación, los valores *displayName*, *Name*, *Publisher*y *PublisherDisplayName* en el archivo *. appxmanifest* deben coincidir con los valores asignados a la aplicación en el panel del centro de desarrollo de Windows al reservar su nombre. 

    Inicia sesión en el [panel del centro de desarrollo de Windows](https://developer.microsoft.com/dashboard/windows/overview)y busca los valores de identidad de la aplicación en identidad de la aplicación de administración de **aplicaciones**  >  **App identity**:

    ![Panel del centro de desarrollo de Windows, configuración de identidad de la aplicación](./media/dashboard-app-identity.png)

    Después, busca el `appxmanifest.xml` archivo y reemplaza los siguientes valores por los que están asignados en el panel del centro de desarrollo de Windows:

    - **<Identity name = "** *paquete/identidad/nombre*
    - **<Identity Publisher = "** *paquete/identidad/editor*
    - **<DisplayName** **>** *Nombre que has reservado para tu aplicación* 
    - **<PublisherDisplayName** **>** *Paquete/propiedades/PublisherDisplayName***</PublisherDisplayName>**

4. Ahora ya está listo para compilar todos los recursos de PWA en un solo `.appx` archivo que puede cargar a Microsoft Store. Desde un símbolo del sistema, navegue hasta el directorio del manifiesto web y cree un paquete de Windows 10 (especificado a continuación con el registro de depuración opcional):

    ```
    pwabuilder package -p windows10 -l debug
    ```

    El archivo. appx se generará en esta ubicación: `PWA\Store packages\windows10\package\windows.appx` .

5. Antes de cargar la aplicación para Submisison en Microsoft Store, es una buena idea probar la aplicación para el cumplimiento de las directivas de Microsoft Store. Para ello, descarga el kit para la [**certificación de aplicaciones en Windows**](https://developer.microsoft.com/windows/develop/app-certification-kit), lo inicia y selecciona el archivo *. appx* de la aplicación para realizar las pruebas. Recibirá un informe de las áreas que puede resolver una vez que se hayan completado todas las pruebas.

6. Para cargar el paquete y completar el envío, vuelve a iniciar sesión en el [panel del centro de desarrollo de Windows](https://developer.microsoft.com/dashboard/windows/overview) y expande el panel **envíos**  >  **Submisison 1** . Sigue la lista de comprobación para completar la información de descripción de la [tienda requerida](/windows/uwp/publish/app-submissions) y [cargar el paquete de la aplicación](/windows/uwp/publish/upload-app-packages).

Para obtener más información sobre todas las características y servicios disponibles para los programadores de aplicaciones de Microsoft Store, vea [*publicar aplicaciones de Windows*](https://developer.microsoft.com/store/publish-apps) en el [centro de desarrollo de Windows](https://developer.microsoft.com/windows).

## Importación automática de PWA con Bing

Al igual que el manifiesto de la [aplicación web](https://developer.mozilla.org/docs/Web/Manifest) de PWA es una señal para las plataformas de soporte que la aplicación está desconectada y está lista para ser presentada como una experiencia de aplicación completamente integrada, también es una sugerencia para el rastreador web de Bing que se debe considerar que su PWA se debe considerar para su inclusión automática en Microsoft Store. 

Si su PWA cumple los siguientes requisitos, el servicio de indización de Bing empaquetará automáticamente su PWA con el formato [*. appx*](#submitting-your-pwa-manually) necesario para la instalación en Windows 10 y ensamblará la página de productos de la tienda de la aplicación en función de los metadatos de su manifiesto de la aplicación Web. Después de reclamar su PWA, podrá personalizar aún más la página de la tienda y obtener acceso a análisis de usuarios y otras herramientas de administración de aplicaciones a través del panel del centro de desarrollo de Windows.

### Criterios para el envío automático

Para empaquetar automáticamente y enumerar en Microsoft Store, su PWA necesitará lo siguiente:

- [X] un archivo de manifiesto de aplicación web no vacío, con como mínimo:

  - Nombre
  - Descripción
  - Icono de la aplicación de un mínimo de 512 x 512 píxeles

- [X] lógica básica única (código no modificada de forma mínima desde una plantilla de [aplicaciones reutilizable](https://en.wikipedia.org/wiki/Boilerplate_code) )

- [X] para ser servido a través de una conexión segura (HTTPS)

- [X] scripts de trabajo de servicio

- [X] para no infringir las leyes ni [las directivas de Microsoft Store](/legal/windows/agreements/store-policies).

No inscribirás todas las aplicaciones que cumplan estos criterios, pero las incluirás en nuestras consideraciones para candidatos, ya que expandimos gradualmente nuestro programa.

### Cómo optar por la importación automática de Microsoft Store

Su PWA puede anular la importación automática a Microsoft Store al servir un `robots.txt` archivo que contiene lo siguiente:

```
User-agent: bingbot
Disallow: /manifest.json
```

Esto hace que el rastreador web de Bing (bingbot) ignore el archivo de manifiesto web para fines de indización de PWA. Esto no afectará la clasificación de búsqueda del sitio en el [proceso de indización de web](https://www.bing.com/webmaster/help/help-center-661b2d18)habitual de Bing.

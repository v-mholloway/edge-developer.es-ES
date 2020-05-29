---
description: Proceso escalonado para publicar extensiones de Edge (cromo) en Microsoft Store.
title: Publicar una extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 7b5be511af1e81efd5da4fc4bc0691f317437f94
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607381"
---
# Publicar una extensión  

Publicar la extensión en el catálogo de complementos de Microsoft Edge \ (complementos de Microsoft Edge \).  Primero debes crear un envío en el [centro de Partners][MicrosoftPartnerCenter] y enviarlo.  En este documento se enumeran todos los detalles que debe proporcionar para crear un envío de extensión.  

## Antes de empezar  

*   Debe tener una cuenta de desarrollador activa en el [centro de Partners][MicrosoftPartnerCenter] para enviar su extensión en los complementos de Microsoft Edge.  Si no tiene una, [cree una nueva][MicrosoftPartnerCenter].  
*   Cree un archivo zip de su paquete de extensión y asegúrese de que contiene estos archivos:  
    *   El archivo de manifiesto y debe definir el nombre y la versión de la extensión.  
    *   Las imágenes y otros archivos necesarios para la extensión.  


Si no ha empezado a crear una extensión, puede consultar el tutorial de [Introducción][ExtensionsGettingStarted] para crear una extensión de cromo de Microsoft Edge.  

Para crear un envío de extensión en el [centro de Partners][MicrosoftPartnerCenter], siga estos pasos.  

## Paso 1: iniciar una nueva presentación  

Vaya a su [Panel de programadores][MicrosoftPartnerCenter].  En la página Descripción general, haga clic en **crear nueva extensión**.  

## Paso 2: cargar el archivo zip de extensión  

La página del **paquete** es el lugar donde se carga el archivo zip para el envío de la extensión.  Solo puedes cargar un paquete a la vez, por lo que si la extensión no está completa, puedes cargar un paquete de trabajo en progreso y actualizarlo en cualquier momento antes de publicarlo.  Asegúrese de que el paquete contiene el `manifest.json` archivo y de que funciona correctamente en Microsoft Edge antes de cargarlo.  
Cargue el paquete arrastrándolo al campo cargar o seleccionando **examinar los archivos**.  La página Package valida el archivo zip Extensions y muestra el **Estado de éxito o error de la carga**.  Si el paquete supera la validación; se cargó correctamente y verá un mensaje de éxito.  Si se produce un error de validación en el paquete; el paquete no se acepta y se muestra un mensaje de error.  Si hay errores en el paquete, solucione los problemas e intente cargarlo de nuevo.  

Después de cargar correctamente, revise los detalles de la extensión y haga clic en **siguiente** para continuar.  

## Paso 3: proporcionar detalles de disponibilidad  

### Definir la visibilidad  

Seleccione una opción de **visibilidad** para definir la audiencia que puede descubrir y adquirir la extensión.  Esto le da la opción de especificar si los usuarios deben buscar su extensión en los complementos de Microsoft Edge o ver el listado.  En este momento, tiene dos opciones en visibilidad:  

*   `Public`  
    Esta es la opción predeterminada.  
    Si seleccionas `Public` , tu extensión estará disponible y podrá ser detectada para todos los usuarios de los complementos de Microsoft Edge.  Deje esta opción seleccionada si quiere que la extensión aparezca en complementos de Microsoft Edge para que los usuarios la encuentren a través de la búsqueda, la navegación y el vínculo directo de su extensión.  

*   `Hidden`  
    Si selecciona `Hidden` , la extensión quedará oculta en los complementos de Microsoft Edge de los usuarios que busquen o exploren; debe compartir la dirección URL de su registro para distribuir la extensión.  Los usuarios que tienen el vínculo directo al listado pueden descargarlo en Microsoft Edge \ (es posible que encuentres la URL de tu anuncio en la página de **Descripción general** de la extensión del envío de la extensión \).  

> [!NOTE]
> Si envía una extensión como **pública** y la cambia posteriormente a **privada**, los usuarios que instalaron la extensión cuando ésta era pública siguen teniendo acceso y recibirán futuras actualizaciones.  

### Definir mercados  

Debe definir los mercados específicos en los que está ofreciendo la extensión, seleccione **Mostrar opciones** en la sección **mercados** de la página **disponibilidad** .  Se muestra la ventana emergente de selección de mercado, donde deberías elegir los mercados.  De forma predeterminada, se seleccionan todos los mercados, incluidos los **mercados futuros** que se pueden añadir más adelante.  Puede anular la selección de cada uno de los mercados para excluirlos, o puede hacer clic en **anular selección** y, después, agregar mercados individuales de su elección.  

> [!NOTE]
> Si los usuarios ya tienen su extensión en un mercado determinado y después lo quita, los usuarios que ya tienen la extensión en ese mercado pueden continuar utilizándolo, pero no obtienen las actualizaciones posteriores que envíe.  

Haga clic en **Guardar** para ir a la sección de **propiedades** .  

## Paso 4: seleccionar las propiedades de la extensión  

### Propiedades de extensión  

*   [Categoría](#category)  
*   [Requisitos de la política de privacidad](#privacy-policy-requirements)  
*   [Dirección URL de la directiva de privacidad](#privacy-policy-url)  
*   [Dirección URL del sitio web](#website-url)  
*   [Dirección URL de soporte/dirección de correo electrónico](#support-urlemail-address)  
*   [Clasificación de extensión](#extension-rating)  

#### Categoría  

El listado de tu extensión en la categoría adecuada ayuda a los usuarios a encontrar tu extensión fácilmente y a entender más acerca de ella.  Seleccione la categoría que mejor describa la extensión.  

**Valores posibles**:  

*   `Accessibility`  
*   `Blogging`  
*   `Developer Tools`  
*   `Fun`  
*   `News & Weather`  
*   `Photos`  
*   `Productivity`  
*   `Search Tools`  
*   `Shopping`  
*   `Social & Communication`  
*   `Sports`  

#### Requisitos de la política de privacidad  

Indique si su extensión accede, recopila o transmite cualquier tipo de información personal.  

> [!NOTE]
> Si tu extensión requiere una política de privacidad y no proporcionaste ninguna, tu envío puede dar error de certificación.  

**Valores posibles**:  

*   `No`: Una dirección URL de política de privacidad es opcional.  
*   `Yes`: Es necesaria una dirección URL de política de privacidad.  

#### Dirección URL de la directiva de privacidad  

Usted es responsable de asegurar que su extensión cumpla con las leyes y regulaciones de privacidad, y para proporcionar una URL de política de privacidad válida, si es necesario.  Debe proporcionar una URL de política de privacidad Si su extensión accede, transmite o recopila toda la información personal.  
Para determinar si su extensión requiere una política de privacidad, revise el [contrato para desarrolladores de Microsoft Edge][MicrosoftAppDeveloperAgreement] y el [documento directivas para desarrolladores de catálogos de Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valores posibles**:  

*   `{url}`  

#### Dirección URL del sitio web  

Esta propiedad es opcional.  
Dirección URL de la Página Web de la extensión.  Esta dirección URL debe apuntar a una página de su propio sitio web, no a la lista de sitios web para su extensión en los complementos de Microsoft Edge.  

**Valores posibles**:  

*   `{url}`  

#### Dirección URL de soporte/dirección de correo electrónico  

Esta propiedad es opcional.  
La dirección URL de la página web en la que los usuarios van por soporte técnico con la extensión o una dirección de correo electrónico para ponerse en contacto con usted para obtener asistencia.  Incluye información de soporte técnico para todos los recibos, de modo que los usuarios sepan cómo obtener asistencia de usted.  

**Valores posibles**:  

*   `{email_address}`  
*   `{url}`  

#### Clasificación de extensión  

La clasificación de extensión nos ayuda a determinar la edad del público objetivo de tu extensión.  
Para ayudarle a determinar si las extensiones tienen un contenido adulto, revise el [documento Microsoft Edge addons Catalog Policies][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valores posibles**:  

*   Adultos \ (casilla de verificación \): Active esta casilla si su extensión contiene algún contenido maduro.  Si seleccionas adultos para tu extensión, tu registro estará disponible con una etiqueta independiente para indicar que la extensión contiene contenido para adultos.  

Haz clic en **Guardar** para ir a la sección de inscripción.  

## Paso 5: agregar información de registros para la extensión  

Esta es la información que los usuarios ven al ver el listado en los complementos de Microsoft Edge.  Muchos de los campos de un registro son opcionales, pero sugerimos proporcionar la mayor cantidad de información posible para hacer que su registro destaque.  El mínimo requerido para que tu registro en los complementos de Microsoft Edge se considere completo es la [Descripción de texto](#description), el [logotipo de extensión](#store-logo)y el [pequeño mosaico promocional](#small-promotional-tile) en cada idioma mencionado en el paquete de extensión.  

### Campos de descripción de la tienda  

*   [Idiomas de la descripción de la Store](#store-listing-languages)  
*   [Nombre para mostrar de la tienda](#store-display-name)  
*   [Descripción](#description)  
*   [Logotipo de la tienda](#store-logo)  
*   [Pequeño mosaico promocional](#small-promotional-tile)  
*   [Multimedia](#media)  
*   [Descripción corta](#short-description)  
*   [Términos de búsqueda](#search-terms)  

#### Idiomas de la descripción de la Store  

Si tu paquete de extensión admite varios idiomas, tu extensión debe tener una página de registro para cada uno.  
Debe completar los detalles de la lista \ (Descripción de texto, imágenes, etc.) para cada idioma por separado, incluso si usa el mismo contenido para cada idioma.  Si tu extensión está localizada en más de un idioma, esos idiomas se mostrarán en la página de la parte superior de la lista.  

1.  Seleccione cualquier nombre de idioma en la lista desplegable **idiomas** .  
1.  Rellene los detalles del registro.  
1.  Haga clic en **Guardar**.  
1.  Repita el procedimiento para todos los idiomas admitidos.  

> [!NOTE]
> Para agregar o quitar idiomas para su registro en los complementos de Microsoft Edge, debe modificar la lista de idiomas admitidos por el paquete de extensión y volver a cargarlo.  

**Valores posibles**:  

*   `English (United States)`: Este es el valor predeterminado.  Si no menciona ningún idioma en su paquete, establecemos el idioma predeterminado en inglés \ (Estados Unidos \) y debe proporcionar un registro en inglés \ (Estados Unidos \).  
*   `{language}` \(`{Country}`\)  

#### Nombre para mostrar de la tienda  

El nombre de la extensión según se indica en el manifiesto del paquete de extensión.  

> [!NOTE]
> Para editar el nombre, debe actualizar el manifiesto en el paquete de extensión y volver a cargarlo.  

#### Descripción  

Este campo es obligatorio.  
La descripción de los usuarios de lo que hace la extensión.  

**Valores posibles**:  

*   {plain_text}: menos de 10.000 caracteres.  

#### Logotipo de la tienda  

Este campo es obligatorio.  
Una imagen de 1:1 para tu logotipo de extensión.  

**Valores posibles**:  

*   128px x 128px, PNG \ (. png \)  
*   150px x 140px, PNG \ (. png \)  
*   300px x 300px, PNG \ (. png \): el tamaño recomendado.  

#### Pequeño mosaico promocional  

Este campo es obligatorio.  
Un mosaico promocional de tamaño pequeño.  Tu registro se muestra en este icono.  

**Valores posibles**:  

*   440px x 280x, PNG \ (. png \)  

#### Multimedia  

Este campo es opcional.  
Debes proporcionar estos activos para ayudar a mostrar tu producto de forma más eficaz.  

*   Capturas de pantalla  
    Las imágenes de la extensión que describen lo que hace la extensión.  
    
*   Iconos de promoción grandes  
    Un gran mosaico promocional para que sea más destacado en los complementos de Microsoft Edge.  
    
*   Dirección URL de vídeo de YouTube  
    Una [dirección URL de vídeo de YouTube válida para la extensión][MicrosoftEdgeAddonsUploadYouTubeVideo].  El video debe ser de buena calidad y longitud mínima.  El vídeo de YouTube debe superar la certificación antes de publicar su extensión en los complementos de Microsoft Edge.  Compruebe que el vídeo de YouTube cumple con el [documento de directivas para desarrolladores de catálogos de Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  

**Valores posibles**:  

*   10 capturas de pantallas como máximo.  
    *   640px x 480px, PNG \ (. png \): capturas de pantallas.  
    *   1280px x 800px, PNG \ (. png \): capturas de pantallas.  
*   1400px x 560px, PNG \ (. png \): mosaicos de promoción grandes.  
*   60 segundos o más corto y 2GB o menos, dirección URL de vídeo de YouTube.  

#### Descripción corta  

Una descripción breve y breve que se puede usar en la parte superior de la lista de productos.  Si no se proporciona, se usan las primeras líneas de la descripción más larga.  Debido a que tu descripción también aparece debajo de este texto, debes proporcionar una breve descripción con distintos textos para que el registro sea menos repetitivo.  La descripción breve de tu extensión se selecciona directamente desde el archivo de manifiesto del paquete.  

> [!NOTE]
> Para modificar la descripción breve, debe actualizar el manifiesto en el paquete de extensión y volver a cargarla.  

#### Términos de búsqueda  

Los términos de búsqueda son palabras individuales o frases cortas que no se muestran a los usuarios, pero ayudan a que la extensión se pueda detectar en los complementos de Microsoft Edge cuando los usuarios buscan las condiciones.  

**Requisitos**:  

*   7 o menos términos de búsqueda  
*   30 o menos caracteres por término de búsqueda  
*   21 o menos palabras para los términos de búsqueda combinados  

Haz clic en **Guardar** para continuar con la sección guardar la lista.  Haga clic en **publicar** para proporcionar detalles de presentación.  

## Paso 6: completar el envío y hacer clic en publicar  

En la página de opciones de envío del proceso de envío de extensión se proporciona más información para ayudarnos a probar el producto correctamente.  Este paso es opcional, pero se recomienda para muchos supuestos.  

### Opciones de suspensión de publicación  

De forma predeterminada, tu envío se publicará tan pronto como pase la certificación.  Puede optar por suspender la presentación hasta una fecha específica.  A continuación se describen las opciones de esta sección.  

*   **Publicar el envío tan pronto como pase la certificación**  

    Esta es la selección predeterminada.  Significa que su envío comienza el proceso de publicación tan pronto como pase la certificación  

*   **Empezar a publicar el envío en una fecha determinada**  

    Elija **empezar a publicar su presentación en una fecha determinada** para asegurarse de que el envío no se publique hasta una fecha específica.  Con esta opción, tu envío se lanzará tan pronto como sea posible en la fecha que especifiques o después de ella.  La fecha debe ser al menos 24 horas después del momento actual.  Además de la fecha, puedes especificar la hora a la que debe comenzar a publicarse el envío.  

### Notas para la certificación  

A medida que envíe la extensión, tendrá la opción de usar la página notas para el certificado para proporcionar información adicional a los evaluadores de certificación.  Esta información ayuda a garantizar que tu extensión se pruebe correctamente.  Si no podemos probar completamente su envío, es posible que se produzca un error de certificación.  

Asegúrese de incluir el siguiente \ (si corresponde a la extensión \):  

*   Nombres de usuario y contraseñas para cuentas de prueba.  
*   Pasos para tener acceso a las características ocultas o bloqueadas.  
*   Se esperaban diferencias en el comportamiento según la configuración regional o de otro usuario.  
*   Información sobre lo que ha cambiado en una actualización de la aplicación.  
*   Todo lo que cree que los evaluadores debe conocer sobre su envío.  

Después de completar los detalles anteriores, haga clic en **publicar** para enviar la extensión en los complementos de Microsoft Edge.  

Cuando haya terminado de crear el envío para su extensión y haga clic en **publicar**, el envío entra en el paso de certificación.  Este proceso generalmente se completa dentro de un par de días, aunque en algunos casos puede demorar hasta 7 días hábiles.  Una vez que el envío pase la certificación, su extensión se publicará en los complementos de Microsoft Edge, a menos que haya seleccionado las opciones de conservación de publicaciones para especificar que no se debe liberar hasta una fecha determinada.  Recibirá una notificación cuando se publique el envío y el estado de la extensión en el panel cambiará a `In the Store` .  

<!-- image links -->  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introducción a las extensiones de Microsoft Edge \ (cromo \) | Microsoft docs"  

[MicrosoftEdgeAddonsUploadYouTubeVideo]: ./upload-video.md "Cargar un vídeo de YouTube | Microsoft docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Directivas para desarrolladores de catálogos de Microsoft Edge addons | Microsoft docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Acuerdo de desarrollador de aplicaciones | Microsoft docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de socios"  

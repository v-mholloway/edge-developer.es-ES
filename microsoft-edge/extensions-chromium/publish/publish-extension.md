---
description: Publicar Microsoft Edge (Chromium) en Microsoft Edge de complementos
title: Publicar la extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 7a53db81e20c9bef61cb6daf094db0c218883652083a415757618bcf4a01ec52
ms.sourcegitcommit: 48101fb3ad5c688ce066e8a64c29fd9cbffdaaab
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/12/2021
ms.locfileid: "11881723"
---
# <a name="publish-your-extension"></a>Publicar la extensión  

Después de desarrollar y probar la extensión, estás listo para distribuir la extensión. Usa el Microsoft Edge complementos para distribuir la extensión.  Para liberar la extensión de Chromium existente para Microsoft Edge usuarios, navegue para [portabilidad de la extensión Chromium existente.][PortChromiumExtension]  

Publique la extensión en el almacén Microsoft Edge complementos para aumentar el alcance de la extensión y hacer que esté disponible para otros Microsoft Edge usuarios.  En este artículo se proporciona el proceso para enviar la extensión al Microsoft Edge de complementos.  

## <a name="before-you-begin"></a>Antes de empezar  

Debe tener listo un prototipo de trabajo de la extensión.  Para obtener información sobre cómo crear una extensión, consulte el [tutorial Introducción][ExtensionsGettingStarted].  

Para publicar la extensión en el Microsoft Edge complementos, use su cuenta de desarrollador activa en [el Centro de partners][MicrosoftPartnerCenter].  Si no tienes una cuenta de desarrollador, crea una nueva cuenta de desarrollador.  Para abrir una nueva cuenta de desarrollador y registrarse en el Complementos para Microsoft Edge, vaya a [Registro de desarrollador][DeveloperRegistration].  

Cree un archivo zip que represente el paquete de extensión.  El paquete de extensión debe incluir los siguientes archivos.  

*   Manifiesto de extensión que especifica detalles como el nombre de la extensión, la descripción breve, los permisos y el idioma predeterminado.  
*   Imágenes y otros archivos requeridos por la extensión.  
    
Los siguientes campos del manifiesto se incluyen automáticamente en los detalles de la descripción de la tienda.  Los campos son de solo lectura en la **página web de listas de la** Tienda.  La página web de listados de la tienda se describe más adelante en este artículo.  Asegúrese de que los valores de campo coinciden con la pantalla preferida en la página web de detalles de la tienda antes de cargar el paquete en el Centro de partners.  Para obtener un ejemplo del código necesario para el archivo de manifiesto, revise los conceptos básicos del archivo de manifiesto.  

*   `Name` campo en el archivo de manifiesto, que es el **nombre para mostrar** en la página web de detalles de la tienda.  
*   `Description` campo en el archivo de manifiesto, que es la **descripción breve** en la página web de detalles de la tienda.  Proporcione una descripción breve y pegajoso para mostrar en la parte superior de la descripción de la extensión.  Si incluye la descripción breve en el archivo de manifiesto de extensión, se muestra en la descripción de la tienda.  Si no incluyes una breve descripción en el archivo de manifiesto, las primeras líneas de presentación en la descripción `Description` de la tienda.  Proporcione una breve descripción para evitar la repetición de contenido en la página web de descripción de la tienda.  
    
## <a name="submit-your-extension-to-microsoft-edge-add-ons-store"></a>Enviar la extensión a Microsoft Edge de complementos  

Para enviar la extensión al [Centro de partners,][MicrosoftPartnerCenter]siga estos pasos.  

## <a name="step-1--start-a-new-submission"></a>Paso 1: Iniciar un nuevo envío  

Vaya al panel [del desarrollador y,][MicrosoftPartnerCenter] a continuación, **seleccione Crear nueva extensión en** la página web **Información** general.  

## <a name="step-2--upload-the-extension-package"></a>Paso 2: Upload el paquete de extensión  

Use la **página web Paquetes** para cargar el archivo zip del paquete de extensión.  Solo puede cargar un paquete a la vez.  El envío se bloquea si la carga del paquete no se realiza correctamente en la página web **Paquetes.**  

Para cargar el paquete, seleccione y arrastre el paquete al campo de carga.  Además, puede seleccionar **Examinar los archivos**.  Después de cargar el paquete, el paquete se valida.  Después de que la validación se realiza correctamente, revise los detalles de la extensión y, a continuación, **seleccione Siguiente** para continuar.  Si hay errores de validación, resuelva los problemas e intente cargar de nuevo.  

## <a name="step-3--provide-availability-details"></a>Paso 3: Proporcionar detalles de disponibilidad  

En la **página web Disponibilidad,** escriba la siguiente información sobre la disponibilidad de la extensión.  

### <a name="visibility"></a>Visibilidad  

Seleccione una de las siguientes opciones de visibilidad para definir si la extensión se puede detectar en el Microsoft Edge complementos.  

*   `Public` \(default\)  
    Public permite a todos descubrir la extensión mediante la búsqueda, la exploración en el almacén de complementos de Microsoft Edge o el uso de la dirección URL de descripción de la extensión en el almacén de complementos de Microsoft Edge.  La dirección URL de descripción está disponible en el panel del Centro de partners en la página web Información **general sobre** la extensión.  
*   `Hidden`  
    Oculto quita las extensiones de los resultados de búsqueda o la exploración en el Microsoft Edge complementos.  Para distribuir extensiones ocultas en el Microsoft Edge complementos, debes compartir la dirección URL de la descripción con la extensión con los clientes.  
    
> [!NOTE]
> Puede cambiar la visibilidad de la extensión de **Public** a **Hidden**.  Los usuarios que instalaron la extensión mientras la visibilidad se estableció en público conservan el acceso a la extensión y reciben las actualizaciones que haga disponibles a través del sitio Complementos para Microsoft Edge web.  

### <a name="markets"></a>Mercados  

Defina los mercados específicos en los que tiene previsto ofrecer la extensión.  La configuración predeterminada para los mercados es todos los mercados y eso incluye los mercados futuros que se agregan más adelante.  Para elegir mercados específicos, seleccione **Cambiar mercados**.  Alterna los mercados individuales para excluir cada uno o selecciona Anular la selección de **todos** y, a continuación, agrega mercados individuales de tu elección.  

> [!NOTE]
> Puede cambiar los mercados donde se ofrece la extensión.  Un usuario que instala la extensión mientras está disponible en el mercado del usuario conserva el acceso a la extensión.  Sin embargo, el usuario no tiene acceso a actualizaciones futuras enviadas al Microsoft Edge de complementos.  

Seleccione **Guardar** para continuar con la **sección Propiedades.**  

## <a name="step-4-select-properties-for-your-extension"></a>Paso 4: Seleccionar propiedades para la extensión  

En la **página web Propiedades,** escriba la siguiente información para especificar las propiedades de la extensión.  Las propiedades se muestran a los usuarios en el Microsoft Edge complementos.  

| Nombre de la propiedad Extension | Descripción |  
|:--- |:--- |  
| Categoría \(required\) | La categoría que mejor describe la extensión.  Enumerar la extensión en la categoría correcta ayuda a los usuarios a encontrar la extensión fácilmente y a comprender más sobre ella.  |  
| Requisitos de la directiva de privacidad \(required\) | Indica si la extensión tiene acceso, recopila o transmite información personal.  La extensión puede producir un error en el paso de certificación si selecciona **Sí** y no proporciona un `Privacy policy URL` .  |  
| Dirección URL de la directiva de privacidad | Una dirección URL válida de la directiva de privacidad para comunicar cómo se sigue la extensión a las leyes y normativas de privacidad.  Eres responsable de asegurarte de que la extensión se desvía de las leyes y normativas de privacidad.  También es responsable de proporcionar una dirección URL de directiva de privacidad si su extensión está accediendo, transmitiendo o recopilando información personal.  Para determinar si la extensión requiere una directiva de privacidad, vaya a Microsoft Edge [Developer Agreement][MicrosoftAppDeveloperAgreement] y Microsoft Edge de desarrolladores del almacén de [complementos.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  |  
| DIRECCIÓN URL del sitio web | Una página web que proporciona información adicional acerca de la extensión.  Debe apuntar a una página web en su propio sitio web, no a la descripción web de la extensión en el Microsoft Edge `Website URL` complementos.  Ayuda `Website URL` a los usuarios a obtener más información sobre la extensión, sus características y cualquier otra información relevante.  |  
| Detalles de contacto de soporte técnico | La dirección URL de la página web de soporte técnico o la dirección de correo electrónico para ponerse en contacto con el equipo de soporte técnico.  |  
| Contenido maduro | Casilla para especificar si la extensión incluye contenido maduro.  La clasificación de extensión ayuda a determinar el grupo de edad adecuado de la audiencia de destino de la extensión.  Para ayudar a determinar si la extensión tiene contenido maduro, vaya a Microsoft Edge directivas de desarrollador de [la tienda de complementos][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  

Selecciona **Guardar** para continuar con la **sección Listados de la** Tienda.  

> [!Important]
> El nombre del desarrollador/organización, la dirección URL del sitio web y los detalles de contacto de soporte técnico que envió durante el registro se muestran a los usuarios en el Microsoft Edge complementos.  

## <a name="step-5-add-store-listing-details-for-your-extension"></a>Paso 5: Agregar detalles de descripción de la Tienda para la extensión  

La información proporcionada en la siguiente sección se muestra a los usuarios que revisan la descripción en el Microsoft Edge complementos.  Aunque algunos campos son opcionales, debe proporcionar tanta información como sea posible.  Para enumerar la extensión en la tienda, se requieren los siguientes detalles.  

*   **Descripción** de cada idioma del paquete de extensión. Para admitir varios idiomas, puede usar la API de internacionalización ([chrome.i18n](https://go.microsoft.com/fwlink/?linkid=2167478)).  
*   **Logotipo de la Tienda de extensiones** para cada idioma del paquete de extensión.  
    
> [!NOTE]
> Los detalles mínimos necesarios de la descripción de la tienda deben rellenarse para al menos uno de los idiomas mencionados en el paquete zip de extensión.  Para agregar o quitar idiomas en la descripción de la tienda en **** la tienda de complementos de Microsoft Edge, usa la lista desplegable Agregar un idioma en la página web de listas **de la** Tienda.  Además, puedes duplicar los activos de un idioma en otros usando el botón **Funcionalidad** duplicada de la página web **Detalles del** idioma.  

| Nombre de la propiedad Detalles del idioma | Descripción |  
|:--- |:--- |  
| Nombre para mostrar \(required\) | La `name` extensión especificada en el archivo de manifiesto de la extensión.  Para cambiar el nombre para mostrar del almacén después del envío, puede actualizar el nombre en el archivo de manifiesto, crear un nuevo paquete de extensión y, a continuación, volver a cargarlo.  |  
| Descripción \(required\) | El campo se centra en explicar qué hace la extensión, por qué los usuarios deben instalarla u otra información relevante que los usuarios `description` necesitan saber.  Debe tener menos de 10 000 caracteres.  |  
| Logotipo del Almacén de extensiones \(required\) | Imagen que representa la empresa o con una relación de aspecto de 1 y un tamaño recomendado de `extension logo` 300 x 300 píxeles.  Además, puedes copiar el activo de un idioma a todos los demás idiomas mediante el botón Duplicar.  Este botón se encuentra siguiendo el campo después de cargar el logotipo para el idioma.  |  
| Pequeño icono promocional \(optional\) | La `Small promotional tile` imagen se usa para mostrar la extensión junto con otras extensiones en el almacén.  El tamaño de la imagen debe ser de 440 x 280 píxeles.  Además, puedes copiar el activo de un idioma a todos los demás idiomas mediante el botón Duplicar.  El botón se encuentra siguiendo el campo después de cargar un icono promocional para el idioma.  |  
| Capturas de pantalla \(optional\) | Puede enviar un máximo de 10 `screenshots` describiendo detalladamente la funcionalidad de la extensión.  El tamaño de las capturas de pantalla debe ser de 640 x 480 píxeles o 1280 x 800 píxeles.  Además, puedes copiar el activo de un idioma a todos los demás idiomas mediante el botón Duplicar.  El botón se encuentra siguiendo el campo después de cargar al menos uno para el idioma.|  
| Icono promocional grande \(optional\) | `Large promotion tiles` se usan en la tienda para características de extensiones más prominentes en el sitio Complementos para Microsoft Edge web.  Las imágenes, si se envían, son visibles para los usuarios.  El tamaño de los archivos PNG debe ser de 1400 x 560 píxeles.  Además, puedes copiar el activo de un idioma a todos los demás idiomas mediante el botón Duplicar.  El botón se encuentra siguiendo el campo después de cargar un icono promocional para el idioma.  |  
| Url de vídeo de YouTube \(optional\) | Puedes incluir un vídeo promocional de YouTube de tu extensión.  El vídeo se muestra en la página web de descripción `YouTube video URL` de la tienda de la extensión.  |  
| Descripción breve \(required\) | Para editar el , debe actualizar el campo de descripción del archivo de manifiesto del paquete de extensión y `short description` volver a cargarlo.  |  
| Términos de búsqueda \(optional\) | `Search terms` son palabras o frases únicas que ayudan a descubrir la extensión cuando un usuario busca en el Microsoft Edge complementos.  Los términos de búsqueda no se muestran a los usuarios.  |  

### <a name="youtube-video-url-requirements"></a>Requisitos de url de vídeo de YouTube  

Asegúrese de que el vídeo cumple los siguientes requisitos.  

*   Compruebe que el contenido del vídeo de YouTube sigue las Microsoft Edge directivas de desarrollador del [almacén de complementos.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  
*   Desactiva los anuncios en el vídeo.  Para obtener más información, vaya [a Establecer los formatos de anuncios predeterminados][GoogleYoutubeAnswer2531367Topic7072227] y [Anuncios en vídeos incrustados.][GoogleYoutubeAnswer132596]  
*   Activa la inserción para tus vídeos.  Para obtener más información, vaya a [Insertar vídeos & listas de reproducción][GoogleYoutubeAnswer171780].  
    
Para enviar la dirección URL de vídeo de YouTube del vídeo, siga estos pasos.  

1.  En YouTube, busca el vídeo que quieres agregar a la página web de descripción de la tienda.  
1.  En el vídeo, seleccione **Compartir**  >  **insertar**.  
1.  Copie el código HTML que se muestra.  
1.  En la página web de detalles de la descripción de la tienda, pegue el código HTML en el `YouTube video URL` campo.  
    
### <a name="search-terms-requirements"></a>Requisitos de términos de búsqueda  

Los términos de búsqueda deben cumplir los siguientes requisitos.  

*   Puede escribir términos de búsqueda para usar hasta un máximo de 21 palabras.  Tanto si se usa como palabras individuales, frases o una combinación de ambas, solo se te permite un máximo de 21 palabras.  
*   Hasta un máximo de siete términos de búsqueda: una sola palabra o frases.  Cada término de búsqueda tiene un límite de caracteres de 30 caracteres.  
    
## <a name="step-6-complete-your-submission"></a>Paso 6: Completar el envío  

On the **Submit your extension** webpage, add notes for certification to help test your extension.  

### <a name="notes-for-certification-optional"></a>Notas para la certificación (opcional)  

Cuando envíe la extensión, use la página web **Notas** para la certificación para proporcionar información adicional a los evaluadores de certificación.  La información adicional ayuda a garantizar que la extensión se prueba correctamente.  Si la extensión no está totalmente probada, podría fallar la certificación.  

Asegúrese de incluir la siguiente información, según sea necesario.  

*   Nombres de usuario y contraseñas para cuentas de prueba.  
*   Pasos para acceder a características ocultas o bloqueadas.  
*   Diferencias previstas en la funcionalidad en función de la región u otra configuración de usuario.  
*   Si el envío es una actualización de una extensión existente, incluya información sobre los cambios realizados en la extensión.  
*   Cualquier información adicional que los evaluadores deben comprender acerca del envío.  
    
Después de proporcionar la información, seleccione **Publicar** para enviar la extensión al Microsoft Edge complementos.  El envío continúa con el paso de certificación.  El proceso de certificación puede tardar hasta siete días laborables después del envío.  

Una vez que el envío pasa la certificación, la extensión se publica en Microsoft Edge de complementos.  El estado de la extensión en el panel del Centro de partners cambia a `In the Store` .  

> [!NOTE]
> Si encuentra algún problema en el proceso de envío o registro, presente un vale de soporte técnico en [Extensiones Nueva][ExtensionsSupportForm] solicitud de soporte técnico o envíe un correo electrónico a [ext_dev_support@microsoft.com][MailtoExtDevSupportMicrosoftCom].  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introducción a Microsoft Edge (Chromium) extensiones | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registrarse como desarrollador Microsoft Edge extensiones de | Microsoft Docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Port your Chromium extension to Microsoft Edge | Microsoft Docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Microsoft Edge Directivas de desarrollador del almacén de complementos | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "App Developer Agreement | Microsoft Docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensiones Nueva solicitud de | Soporte técnico de Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Establecer los formatos de anuncio predeterminados | Ayuda de YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anuncios en vídeos incrustados | Ayuda de YouTube"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Insertar vídeos & listas de reproducción | Ayuda de YouTube"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Enviar correo electrónico a ext_dev_support@microsoft.com" 


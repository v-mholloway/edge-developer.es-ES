---
description: Publicar extensiones de Microsoft Edge (Chromium) en el almacén de complementos de Microsoft Edge
title: Publicar la extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 67fdbdb39f3ef0b2b6cef2831520849933ffeeec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399130"
---
# <a name="publish-your-extension"></a>Publicar la extensión  

Después de desarrollar y probar la extensión, estás listo para distribuir la extensión. Usa el almacén de complementos de Microsoft Edge para distribuir la extensión.  Para liberar la extensión chromium existente para los usuarios de Microsoft Edge, navegue para [portabilidad de la extensión chromium existente.][PortChromiumExtension]  

Publique la extensión en el almacén de complementos de Microsoft Edge para aumentar el alcance de la extensión y hacer que esté disponible para los usuarios de Microsoft Edge.  En este artículo se proporciona el proceso para enviar la extensión al almacén de complementos de Microsoft Edge.  

## <a name="before-you-begin"></a>Antes de comenzar  

Debe tener listo un prototipo de trabajo de la extensión.  Para obtener información sobre cómo crear una extensión, consulte el [tutorial Introducción][ExtensionsGettingStarted].  

Para publicar la extensión en el almacén de complementos de Microsoft Edge, use su cuenta de desarrollador activa en [el Centro de partners.][MicrosoftPartnerCenter]  Si no tienes una cuenta de desarrollador, crea una nueva cuenta de desarrollador.  Para abrir una nueva cuenta de desarrollador y registrarse en el programa de complementos de Microsoft Edge, vaya a [Registro de desarrollador.][DeveloperRegistration]  

Cree un archivo zip que represente el paquete de extensión.  El paquete de extensión debe incluir los siguientes archivos.  

*   Manifiesto de extensión que especifica detalles como el nombre de la extensión, la descripción breve, los permisos y el idioma predeterminado.  
*   Imágenes y otros archivos requeridos por la extensión.  

Los siguientes campos del manifiesto se incluyen automáticamente en los detalles de la descripción de la tienda.  Los campos son de solo lectura en la **página Listados de la** Tienda.  La página de listados de la tienda se describe más adelante en este artículo.  Asegúrese de que los valores de campo coincidan con su presentación preferida en la página de detalles de la tienda antes de cargar el paquete en el Centro de partners.  Para obtener un ejemplo del código necesario para el archivo de manifiesto, revise los conceptos básicos del archivo de manifiesto.  

*   `Name` campo del archivo de manifiesto, que es el **nombre para mostrar** en la página de detalles de la tienda.  
*   `Description` campo del archivo de manifiesto, que es la **descripción breve** de la página de detalles de la tienda.  Proporcione una descripción breve y pegajoso para mostrar en la parte superior de la descripción de la extensión.  Cuando se incluye, la breve descripción especificada en el archivo de manifiesto de extensión se muestra en la descripción de la tienda.  Si no se incluye una breve descripción en el archivo de manifiesto, se muestran las primeras líneas de Descripción.  Proporcione una breve descripción para evitar la repetición de contenido en la página de descripción de la tienda.  

## <a name="submit-your-extension-to-microsoft-edge-add-ons-store"></a>Enviar la extensión al almacén de complementos de Microsoft Edge  

Para enviar la extensión al [Centro de partners,][MicrosoftPartnerCenter]siga estos pasos.  

#### <a name="step-1--start-a-new-submission"></a>Paso 1: Iniciar un nuevo envío  

Vaya al panel [del desarrollador][MicrosoftPartnerCenter] y elija Crear nueva **extensión en** la página **Información** general.  

#### <a name="step-2--upload-the-extension-package"></a>Paso 2: Cargar el paquete de extensión  

Use la **página** Paquetes para cargar el archivo zip del paquete de extensión.  Solo puedes cargar un paquete a la vez.  No puede continuar con el envío si la carga del paquete no se realiza correctamente en la **página** Paquetes.  

Para cargar el paquete, elija y arrastre el paquete al campo de carga. También puede elegir Examinar **los archivos**.  Una vez cargado el paquete, el paquete se valida.  Una vez que la validación se realiza correctamente, revise los detalles de la extensión y, a continuación, elija **Siguiente** para continuar.  Si hay errores de validación, resuelva los problemas e intente cargar de nuevo.  

#### <a name="step-3--provide-availability-details"></a>Paso 3: Proporcionar detalles de disponibilidad  

En la **página Disponibilidad,** escriba la siguiente información sobre la disponibilidad de la extensión.  

##### <a name="visibility"></a>Visibilidad  

Elija una de las siguientes opciones de visibilidad para definir si la extensión se puede detectar en el almacén de complementos de Microsoft Edge.  

*   `Public` \(default\)  
    Public permite a todos descubrir la extensión a través de la búsqueda, la exploración en el almacén de complementos de Microsoft Edge o el uso de la dirección URL de descripción de la extensión en el almacén de complementos de Microsoft Edge.  La dirección URL de descripción está disponible en el panel del Centro de partners en la página Información **general sobre** la extensión.  
    
*   `Hidden`  
    Oculto quita las extensiones de los resultados de búsqueda o la exploración en el almacén de complementos de Microsoft Edge.  Para distribuir extensiones ocultas en el almacén de complementos de Microsoft Edge, debes compartir la dirección URL de la descripción con la extensión con los clientes.  
    
> [!NOTE]
> Puede cambiar la visibilidad de la extensión de **Public** a **Hidden**.  Los usuarios que instalaron la extensión mientras la visibilidad estaba establecida en público conservan el acceso a la extensión y reciben las actualizaciones que haga disponibles a través del sitio web de complementos de Microsoft Edge.  

##### <a name="markets"></a>Mercados  

Defina los mercados específicos en los que tiene previsto ofrecer la extensión.  La configuración predeterminada para los mercados es todos los mercados y eso incluye los mercados futuros que se agregan más adelante.  Para elegir mercados específicos, elija **Cambiar mercados**.  Alterna los mercados individuales para excluir cada uno o elige Anular la selección **de todos** y, a continuación, agrega mercados individuales de tu elección.  

> [!NOTE]
> Puede cambiar los mercados en los que se ofrece la extensión.  Un usuario que instala la extensión mientras está disponible en el mercado del usuario conserva el acceso a la extensión.  Sin embargo, el usuario no tiene acceso a actualizaciones futuras enviadas al almacén de complementos de Microsoft Edge.  

Seleccione **Guardar** para continuar con la **sección Propiedades.**  

#### <a name="step-4-select-properties-for-your-extension"></a>Paso 4: Seleccionar propiedades para la extensión  

En la **página Propiedades,** escriba la siguiente información para especificar las propiedades de la extensión.  Las propiedades se muestran a los usuarios en el almacén de complementos de Microsoft Edge.  

| Nombre de la propiedad Extension | Descripción |  
|:--- |:--- |  
| Categoría \(required\) | La categoría que mejor describe la extensión.  Enumerar la extensión en la categoría correcta ayuda a los usuarios a encontrar la extensión fácilmente y a comprender más sobre ella.  |  
| Requisitos de la directiva de privacidad \(required\) | Indica si la extensión tiene acceso, recopila o transmite información personal.  La extensión puede producir un error en el paso de certificación si elige **Sí** y no proporciona un `Privacy policy URL` .  |  
| Dirección URL de la directiva de privacidad | Una dirección URL válida de la directiva de privacidad para comunicar cómo se sigue la extensión a las leyes y normativas de privacidad.  Eres responsable de asegurarte de que la extensión se desvía de las leyes y normativas de privacidad.  También es responsable de proporcionar una dirección URL de directiva de privacidad si su extensión está accediendo, transmitiendo o recopilando información personal.  Para determinar si la extensión requiere una directiva de privacidad, vaya a [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement] y Microsoft Edge [Add-ons store developer policies][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  
| DIRECCIÓN URL del sitio web | Una página web que proporciona información adicional acerca de la extensión.  Debe apuntar a una página de su propio sitio web, no a la descripción web de la extensión en el `Website URL` almacén de complementos de Microsoft Edge.  Ayuda `Website URL` a los usuarios a obtener más información sobre la extensión, sus características y cualquier otra información relevante.  |  
| Detalles de contacto de soporte técnico | La dirección URL de la página web de soporte técnico o la dirección de correo electrónico para ponerse en contacto con el equipo de soporte técnico.  |  
| Contenido maduro | Casilla para especificar si la extensión incluye contenido maduro.  La clasificación de extensión ayuda a determinar el grupo de edad adecuado de la audiencia de destino de la extensión.  Para ayudar a determinar si la extensión tiene contenido maduro, vaya a [Microsoft Edge Add-ons store developer policies][MicrosoftEdgeAddonsCatalogDeveloperPolicies].  |  

Elija **Guardar** para continuar con la **sección Desc. De la** Tienda.  

> [!Important]
> El nombre del desarrollador/organización, la dirección URL del sitio web y los detalles de contacto de soporte técnico que envió durante el registro se muestran a los usuarios en el almacén de complementos de Microsoft Edge.  

#### <a name="step-5-add-store-listing-details-for-your-extension"></a>Paso 5: Agregar detalles de descripción de la Tienda para la extensión  

La información proporcionada en la siguiente sección se muestra a los usuarios que revisan su descripción en el almacén de complementos de Microsoft Edge.  Aunque algunos campos son opcionales, debe proporcionar tanta información como sea posible.  Para enumerar la extensión en la tienda, se requieren los siguientes detalles.  

*   **Descripción** de cada idioma del paquete de extensión.  
*   **Logotipo de la Tienda de extensiones** para cada idioma del paquete de extensión.  
    
> [!NOTE]
> Los detalles mínimos necesarios de la descripción de la tienda deben rellenarse para al menos uno de los idiomas mencionados en el paquete zip de extensión.  Para agregar o quitar idiomas en la descripción de la tienda **** en la tienda complementos de Microsoft Edge, usa la lista desplegable Agregar un idioma en la página **Listados de la** Tienda.  Además, puede elegir duplicar los activos de un idioma en otros usando el botón de funcionalidad duplicada en la página de detalles del idioma.  

| Nombre de la propiedad Detalles del idioma | Descripción |  
|:--- |:--- |  
| Nombre para mostrar \(required\) | La `name` extensión especificada en el archivo de manifiesto de la extensión.  Para cambiar el nombre para mostrar de la tienda después del envío, puede actualizar el nombre en el archivo de manifiesto, crear un nuevo paquete de extensión y, a continuación, volver a cargarlo.  |  
| Descripción \(required\) | El campo se centra en explicar qué hace la extensión, por qué los usuarios deben instalarla u otra información relevante que los usuarios `description` necesitan saber.  Debe tener menos de 10 000 caracteres.  |  
| Logotipo del Almacén de extensiones \(required\) | Imagen que representa la empresa o con una relación de aspecto de 1 y un tamaño recomendado de `extension logo` 300 x 300 píxeles.  Además, puede elegir copiar el activo de un idioma a todos los demás idiomas mediante el botón duplicado.  El botón se encuentra siguiendo el campo después de cargar el logotipo del idioma.  |  
| Pequeño icono promocional \(optional\) | La `Small promotional tile` imagen se usa para mostrar la extensión junto con otras extensiones en el almacén.  El tamaño de la imagen debe ser de 440 x 280 píxeles.  Además, puede elegir copiar el activo de un idioma a todos los demás idiomas mediante el botón duplicado.  El botón se encuentra siguiendo el campo después de cargar un icono promocional para el idioma.  |  
| Capturas de pantalla \(optional\) | Puede enviar un máximo de 10 `screenshots` describiendo detalladamente la funcionalidad de la extensión.  El tamaño de las capturas de pantalla debe ser de 640 x 480 píxeles o 1280 x 800 píxeles.  Además, puede elegir copiar el activo de un idioma a todos los demás idiomas mediante el botón duplicado.  El botón se encuentra siguiendo el campo después de cargar al menos uno para el idioma.|  
| Icono promocional grande \(optional\) | `Large promotion tiles` se usan en la tienda para características extensiones más prominentes en el sitio web de complementos de Microsoft Edge.  Las imágenes, si se envían, son visibles para los usuarios.  El tamaño de los archivos PNG debe ser de 1400 x 560 píxeles.  Además, puede elegir copiar el activo de un idioma a todos los demás idiomas mediante el botón duplicado.  El botón se encuentra siguiendo el campo después de cargar un icono promocional para el idioma.  |  
| Url de vídeo de YouTube \(optional\) | Puedes incluir un vídeo promocional de YouTube de tu extensión.  El `YouTube video URL` vídeo se muestra en la página de descripción de la tienda de la extensión.  |  
| Descripción breve \(required\) | Para editar el , debe actualizar el campo de descripción del archivo de manifiesto del paquete de extensión y `short description` volver a cargarlo.  |  
| Términos de búsqueda \(optional\) | `Search terms` son palabras o frases únicas que ayudan a los usuarios a descubrir la extensión al buscar en el almacén de complementos de Microsoft Edge.  Los términos de búsqueda no se muestran a los usuarios.  |  

##### <a name="youtube-video-url-requirements"></a>Requisitos de url de vídeo de YouTube  

Asegúrese de que el vídeo cumple los siguientes requisitos.  

*   Compruebe que el contenido del vídeo de YouTube sigue las directivas de desarrollador del almacén de complementos de [Microsoft Edge.][MicrosoftEdgeAddonsCatalogDeveloperPolicies]  
*   Desactiva los anuncios en el vídeo.  Para obtener más información, vaya [a Establecer los formatos de anuncios predeterminados][GoogleYoutubeAnswer2531367Topic7072227] y [Anuncios en vídeos incrustados.][GoogleYoutubeAnswer132596]  
*   Activa la inserción para tus vídeos.  Para obtener más información, vaya a [Insertar vídeos & listas de reproducción][GoogleYoutubeAnswer171780].  
    
Para enviar la dirección URL de vídeo de YouTube del vídeo, siga estos pasos.  

1.  En YouTube, busca el vídeo que quieras agregar a la página de descripción de la tienda.  
1.  En el vídeo, elija **Compartir**  >  **insertar**.  
1.  Copie el código HTML que se muestra.  
1.  En la página de detalles de la descripción de la tienda, pegue el código HTML en el `YouTube video URL` campo.  
    
##### <a name="search-terms-requirements"></a>Requisitos de términos de búsqueda  

Los términos de búsqueda deben cumplir los siguientes requisitos.  

*   Puede escribir términos de búsqueda para usar hasta un máximo de 21 palabras.  Tanto si se usa como palabras individuales, frases o una combinación de ambas, solo se te permite un máximo de 21 palabras.  
*   Hasta un máximo de siete términos de búsqueda: una sola palabra o frases.  Cada término de búsqueda tiene un límite de caracteres de 30 caracteres.  
    
#### <a name="step-6-complete-your-submission"></a>Paso 6: Completar el envío  

En la **página Enviar la extensión,** agregue notas para la certificación para ayudar a probar la extensión.  

##### <a name="notes-for-certification-optional"></a>Notas para la certificación (opcional)  

Al enviar la extensión, use la página **Notas para** la certificación para proporcionar información adicional a los evaluadores de certificación.  La información adicional ayuda a garantizar que la extensión se prueba correctamente.  Si la extensión no está totalmente probada, puede que no se pueda certificar.  

Asegúrese de incluir la siguiente información, según sea necesario.  

*   Nombres de usuario y contraseñas para cuentas de prueba.  
*   Pasos para acceder a características ocultas o bloqueadas.  
*   Diferencias previstas en la funcionalidad en función de la región u otra configuración de usuario.  
*   Si el envío es una actualización de una extensión existente, incluya información sobre los cambios realizados en la extensión.  
*   Cualquier información adicional que los evaluadores deben comprender acerca del envío.  

Después de proporcionar la información, elija **Publicar** para enviar la extensión al almacén de complementos de Microsoft Edge.  El envío continúa con el paso de certificación.  El proceso de certificación puede tardar hasta siete días laborables después de su envío.  

Cuando el envío pasa la certificación, la extensión se publica en el almacén de complementos de Microsoft Edge.  El estado de la extensión en el panel del Centro de partners cambia a `In the Store` .  

> [!NOTE]
> Si encuentra algún problema en el proceso de envío o registro, presente un vale de soporte técnico en [Extensiones Nueva][ExtensionsSupportForm] solicitud de soporte técnico o envíe un correo electrónico a [ext_dev_support@microsoft.com][MailtoExtDevSupportMicrosoftCom].  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introducción a las extensiones de Microsoft Edge (Chromium) | Microsoft Docs"  
[DeveloperRegistration]: ./create-dev-account.md "Registrarse como desarrollador de extensiones de Microsoft Edge | Microsoft Docs"  
[PortChromiumExtension]: ../developer-guide/port-chrome-extension.md "Port your Chromium extension to Microsoft Edge | Microsoft Docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Microsoft Edge Add-ons store Developer Policies | Microsoft Docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "App Developer Agreement | Microsoft Docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  

[ExtensionsSupportForm]: https://support.microsoft.com/supportrequestform/e7a381be-9c9a-fafb-ed76-262bc93fd9e4 "Extensiones Nueva solicitud de | Soporte técnico de Microsoft"  

[GoogleYoutubeAnswer2531367Topic7072227]: https://support.google.com/youtube/answer/2531367?ref_topic=7072227 "Establecer los formatos de anuncio predeterminados | Ayuda de YouTube"  

[GoogleYoutubeAnswer132596]: https://support.google.com/youtube/answer/132596 "Anuncios en vídeos incrustados | Ayuda de YouTube"  
[GoogleYoutubeAnswer171780]: https://support.google.com/youtube/answer/171780 "Insertar vídeos & listas de reproducción | Ayuda de YouTube"  

[MailtoExtDevSupportMicrosoftCom]: mailto:ext_dev_support@microsoft.com "Enviar correo electrónico a ext_dev_support@microsoft.com" 
